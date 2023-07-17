---
date: 2023-05-16
title: "Security incident: Redis cache exposed to public internet (July 16, 2023)"
linkTitle: "2023-07-16 Security incident: Redis exposure"
description: "Production security incident. Redis cache exposed to internet. No user action required."
author: Esk ([@esk](https://hachyderm.io/@esk))
---

## Background

Between July 9 and July 16, 2023, one of Hachyderm’s Redis cache servers was exposed to the public internet. On July 16, 2023, the Hachyderm Infrastructure team identified a misconfiguration of our firewall on the cache server which allowed access to the redis interface from the public Internet. After a routine system update, the nftables firewall service was not brought up automatically after a restart, which exposed the Redis cache to the internet for a period of seven days.

Normally, Hachyderm servers run nftables to block all except necessary traffic from the Internet. We leverage Tailscale for inter-service communication and only expose ports to the Internet as needed to run Mastodon and administer our systems.

As of July 16, 2023 11:17 UTC, the Hachyderm team has corrected the configuration on our systems and blocked external actors from accessing this Redis instance.

## Impact

Highly sensitive information like passwords, private keys, and private posts were NOT available as part of this incident. No action is required from the user.

The affected Redis cache stored the following types of information with a 10 minute time-to-live before getting deleted:

Email and IP Address of users who used the logged in during this period. Note that if you had a cached session during this period, this data would not have been included.
Rails-generated HTML content
Some UI-related settings for individual users (examples being toggles for reducing motion, auto play gifs, and the selected UI font).
Public posts rendered by Mastodon in the affected period.
Other non-critical information like emojis, blocked IPs, status counts, and other normally public information of the instance.

We do not have sufficient monitoring to confirm precisely when the compromise occurred. We also have no confirmation if any of the above data was actually sent to a third party, but since the information was available to them, we assume the data was compromised. Fortunately, this particular Redis cache expires information after 10 minutes, so the window of opportunity for any particular chunk of information was small.

Finally, during the attack, the Redis cache put itself in a defensive read only mode. Because no new data could be written to the cache, after the Redis server flipped read-only, all data still present in the cache expired ten minutes thereafter.

## Timeline

| **Date/Time (UTC)**                            | **Event**                                                                                                                                                                                                                                                                        | **Phase**        |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| 2023-07-09 19:16                           | Fritz was updated, and part of the upgrade process required a restart of the system. Nftables, our system firewall, was not reenabled across reboots on this server. Fritz acted normally throughout our monitoring period.                                                  |  Before      |
| Between 2023-07-10 to 2023-07-16 | The adversary adds a non-Hachyderm host as the fritz Redis write primary, causing Fritz to go into read-only mode. Sometime thereafter, Fritz’s Redis encounters a synchronization error, causing it to not synchronize further with the non-Hachyderm host.                 |  Before      |
| 2023-07-16 10:45                           | Hachyderm Infra Engineer (HIE1) identifies that, when attempting to run a standard administrative task sees Mastodon logs are alerting that RedisCacheStore: write_entry failed, returned false: Redis::CommandError: READONLY You can't write against a read only replica.  |  Identify    |
| 2023-07-16 10:56                           | After reviewing the system configuration further, HIE1 identifies that the Redis cache on fritz is targeting an unknown host IP as a write primary; overall Redis is in a degraded state.                                                                                    |  Identify    |
| 2023-07-16 11:10                           | HIE1 confirms the unknown host IP is not a Hachyderm host and that nftables on fritz is not enabled as expected.                                                                                                                                                             |  Identify    |
| 2023-07-16 11:17                           | HIE1 stops Redis and re-enables nftables on fritz, closing unbounded communication from the Internet.                                                                                                                                                                        |  Remediate   |
| 2023-07-16 13:02                           | HIE1 confirms the type of information stored in the cache, including e-mail + IP address for logins.                                                                                                                                                                         |  Investigate |

## Analysis

## What went well & where did we get lucky

- We got lucky that it was the caching redis server, which primarily holds Rails generated HTML content, UI related settings per user, and rack based login throttling.
- No user data outside of a subset of IP addresses and Emails from people using the login form in the compromised period were possibly shared.
- Redis had a TTL of ten (10) minutes on any data in this cache.
- Redis was put into a READONLY mode when the compromise occurred, so it is likely no data was pushed to the adversary after the timestamp of the compromise. This, coupled with the ten minute cache, caused the cache itself to empty fairly quickly.

## What didn’t go well

- Process: While we have a standard process for updating Mastodon, and while our servers are version-controlled into git, they are individually unique creations, which makes it challenging to understand if a server is configured correctly because each server can be just a *little* different.
- System: We don’t leverage authentication or restrictive IP block binds on our Redis server, so once the firewall was down, Redis would become available on the Internet and trivial to connect to and see what data it contained.
- It took us a long time to identify the issue:
  - Observability: We don't currently have detective control to alert us if a critical configuration on a server is set correctly or not.
  - Observability: Furthermore, we didn’t have any outlier detection or redis alerts set up to notify us that Redis had gone into read only mode.
- Observability: Due to how journalctl had been set up to rotate logs by size, and the explosive amount of RedisCacheStore: write_entry failed entries generated per successful page load, we quickly lost the ability to look back on our log history to see the exact date the access happened.

## Corrective Actions

The Hachyderm infrastructure team is taking/will take the following actions to mitigate the impact of this incident:

| Action                                                                                                                        | Expected Date | Status |
|-------------------------------------------------------------------------------------------------------------------------------|---------------|--------|
| Enable nftables on fritz and ensure it will re-enable upon system or service restart on all systems                           |  Jul 16, 2023 |  Done  |
| Perform system audit to identify potential additional compromise beyond Redis                                                 |  Jul 16, 2023 |  Done  |
| Update system update runbooks to include validating that nftables is running as expected after restarts                       |  Jul 17, 2023 |  To Do |
| Bind Redis only to expected IP blocks for Hachyderm’s servers                                                                 |  Jul 17, 2023 |  To Do |
| Publish full causal analysis graph and update corrective actions based on findings                                            |  Jul 21, 2023 |  To Do |
| Identify tooling to keep logs for a defined time period that would not be affected by large log files.                        |  Jul 28, 2023 |  To Do |
| Identify plan to require authentication on Redis instances                                                                    |  Jul 28, 2023 |  To Do |
| Identity mechanism for detective controls to alert if critical services are not running on servers & create plan to implement |  Jul 28, 2023 |  To Do |
| Explore possibility of using cloud-based firewall rules as an extra layer of protection & plan to implement                   |  Jul 28, 2023 |  To Do |
