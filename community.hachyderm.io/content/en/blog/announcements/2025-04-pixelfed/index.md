
---
title: "Pixelfed Vulnerability and Impacts to Federation"
linkTitle: "Pixelfed Vulnerability"
date: 2025-04-03
author: Hachyderm ([@hachyderm](https://hachyderm.io/@hachyderm))
description: >
  Pixelfed CVE-2025-30741
---
A recent Pixelfed vulnerability and how it impacts Hachyderm.

If you’re an instance admin and need to reach out to us to refederate, please skip to the “For mods and admins” section (linked on the right nav menu).


## Information about the vulnerability

Pixelfed v0.12.5, released 24 Mar 2025, fixes a flaw in how Follows and Followers Only posts were handled by PixelFed. Before this release, private accounts (accounts that require follower approval) could be followed without approval, and any visible post to any user on a Pixelfed instance was accessible to all users on the entire instance. This allowed unintended access to private content. This is true for all instances federating with the Pixelfed instance, not just the instance itself or other Pixelfed instances.

You can read more about this vulnerability here:

* [NIST CVE-2025-30741](https://nvd.nist.gov/vuln/detail/CVE-2025-30741) ([Web Archive Link](https://web.archive.org/web/20250330013243/https://nvd.nist.gov/vuln/detail/CVE-2025-30741))
* [Github Advisory](https://github.com/advisories/GHSA-7287-grhx-542x)
* [Forkus.Cool Blog Post 25 Mar 2025](https://fokus.cool/2025/03/25/pixelfed-vulnerability.html) ([Web Archive Link](https://web.archive.org/web/20250329184426mp_/https://fokus.cool/2025/03/25/pixelfed-vulnerability.html))
* [Fediverse Report for 1 April 2025](https://fediversereport.com/fediverse-report-110/)


## Why are we talking about Pixelfed and how does this impact Hachyderm?

To restate succinctly:

This vulnerability can expose followers-only posts on all follower-only accounts for all instances using the ActivityPub protocol, regardless of what implementation they are using.

**How? The short version.**

Understanding the gist of the vulnerability requires understanding a couple of mechanics around followers / following and followers-only posts. For the former, when you “lock” your account or make it “private,” what you are enabling is the ability to manually approve followers. Only once you have approved the follow request is the follower approved and the follower allowed to follow you. (For public accounts approval is automatic unless the account’s instance is otherwise moderated by you or your instance.)

Another part of follow / following mechanics is a process referred to as synchronization. This is the process that makes sure your followers list stays updated. For example, if someone deletes their account, this process removes it from your follower list.

Furthermore, when you make a followers-only post, what is supposed to happen is that post should go to your followers collection only. This means notifying the instances hosting the accounts of your followers to relay that post to accounts specifically in your followers collection.

What was happening with Pixelfed versions 0.12.4 and earlier was that Pixelfed hadn’t correctly implemented account following, which means “locked” / “private” accounts can be followed by any Pixelfed user without explicit approval. This means that posts federated with Pixelfed instances that were marked as “followers-only” were being displayed to accounts that Pixelfed had allowed to follow you, but were not necessarily the followers you intended.

Since Hachyderm is a Mastodon instance, that also means that any instances running Pixelfed v0.12.4 or earlier that we federate with can expose private posts on Hachyderm to these instances, additionally, any pixelfed servers running v0.12.5 may still be exposing followers-only content until Pixelfed implements follower collection synchronization.

**What about other ActivityPub implementations?**

This same type of vulnerability *can* happen in other federated software using ActivityPub as well.

This is why you should never post sensitive or highly private content: the privacy of that content is only as strong as the least secure part of the network or software. (The software itself, the server it’s running on, and everything else it needs to run.)

For highly sensitive content, we recommend using services that support end-to-end encryption and limiting who you are sharing it with. Depending on the type of content and how you need to share it, this can include options like Signal or Matrix.


## What actions we have taken

Due to the severity of the issue, we have defederated with all Pixelfed instances that are not running version 0.12.5, since versions prior to 0.12.5 allowed for followers that were not approved to access followers-only content.

In addition, since defederation is a silent action (a defederated instance doesn’t receive a notification), we have reached out to impacted instances, where their contact information was available, to explain the situation and how we can resolve and refederate.

### Determining the impact

It is always important to make an informed decision when making a server-wide decision as a moderation team. This includes understanding what options are available to you and their impact.

In this case, the only real tool that prevents data exposure on this scale is defederation. All other solutions, like limiting, still allow data to be shared and thus exposed.

Since we knew we were going to need to make multiple defederations, we made sure we knew the full scope of the impact of this action. This is doubly true for this CVE, as we typically prefer to give instance admins time to react to information they receive, and, as many of us in tech know, upgrade paths are not always smooth and straightforward.

For the impact analysis, we gathered the following data:

1. How many Pixelfed instances are we federating with?
2. What versions of Pixelfed are those instances running?
3. How much cross-pollination (followers / following) is occurring on those instances?

As a result of our analysis, we determined that the risk to Hachydermian’s private data was high and the cross-pollination on the impacted instances was very low.


### The impact data

Prior to the vulnerability, Hachyderm was federating with 96 instances running Pixelfed. Due to the CVE, we have defederated with 63 of those instances.

(Since this action is due to a security vulnerability, we will refederate with instances that patch the vulnerability. Head to the mods and admins section of this post to learn more.)

A breakdown of the Pixelfed instances we are/were federating with:

* 33 are running 0.12.5 (released 24 Mar 2025)
* 46 are running 0.12.4 (released 8 Nov 2024)
* 17 are running a version earlier than 0.12.4 (0.12.3 was released 1 Jul 2024)

There isn’t a robust way to query Mastodon for how many offline instances it is still trying to federate with, so an unknown percentage of these were already offline with one or more failed retries to connect. To put it another way, it is likely that a number of instances that haven’t been updated “in a long while” were just offline and that information didn’t propagate properly. There just is not a good way to know exactly how many or which. (This is not a bug in Pixelfed, this is common for federating software.)

For the follower / following relationships:

* For 93 of all 96 Pixelfed instances, regardless of software version, there were 5 or fewer following in either direction.
* For 2 of the instances, there were between 5 and 10 following in either direction.
* pixelfed.social is the outlier and outlined in the next section


### What about pixelfed.social

Since pixelfed.social is the largest instance, by far, we’re going to show a little more data. To say it first so it isn’t missed:

> pixelfed.social is running v0.12.5, so we will not be defederating with pixelfed.social as part of the response to this CVE. The additional information below is only because we provided comparable information, in aggregate, for the other 95 Pixelfed instances.

Now on to the data:

* pixelfed.social is running Pixelfed v0.12.5
* There are 1073 unique Hachyderm accounts following 956 unique pixelfed.social accounts and 864 unique pixelfed.social accounts following 651 unique Hachyderm accounts.


## For mods and admins running Pixelfed instances

First and foremost: HugOps. Planning urgent upgrades for CVEs (and related) is stressful and time-consuming, and that is even more true for the volunteer teams across the Fediverse. You've got this!

We’ve also got this with you. We’ve done our best to find contact information to reach out to your admins and mod teams depending on what was listed on your instance or documentation if present, to ensure that you were aware of the situation. Due to the volume of instances impacted by this, this process is still ongoing at the time of publishing this blog post.

We’re happy to refederate with any instance that was defederated from as a result of this CVE. As mentioned in our emails as well, please email us once you have upgraded to 0.12.5 and we will refederate with you. You can also respond to the email that we sent out with the same information.

For anyone looking to communicate with Hachyderm moderation in general, please see both our [documentation landing page](https://community.hachyderm.io/docs/#i-am-the-mod--admin-of-another-instance-and-need-to-contact-the-hachyderm-mods--admins) and our [Reporting and Communication page](https://community.hachyderm.io/docs/moderation/reporting/).


## For fellow Mastodon admins

In the interest of expediency, we published this announcement so that people can see the analysis and impact of our decision. We will publish a separate, shorter, post to include our methods for gathering the above information for the benefit of the broader Mastodon community.
