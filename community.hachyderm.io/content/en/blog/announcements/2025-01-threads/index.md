
---
title: "Defederation from Threads"
linkTitle: "Defederation from Threads"
date: 2025-01-09
author: Hachyderm ([@hachyderm](https://hachyderm.io/@hachyderm))
description: >
  Hachyderm defederation from Threads, Jan 2025.
---



# Defederating from Threads

Hello Hachyderm! In alignment with our prior posts about inter-instance federation, and Threads in particular, Hachyderm has defederated with Threads due to their changes in moderation policy as of the publication of this post.

For those interested in learning more about Threads specifically, please read on.


## Changes to Meta's moderation policies and published statements by Mark Zuckerberg

On Tuesday, 7 Jan 2025, [Mark Zuckerberg published a series of posts](https://www.threads.net/@zuck/post/DEhgYx4JbEG) that described changes to Threads moderation practice, and [Wired published an article](https://www.wired.com/story/meta-immigration-gender-policies-change/) about [Meta's updated moderation (Hateful Conduct) policies](https://transparency.meta.com/policies/community-standards/hateful-conduct/). Since then other articles were published while we worked on this blog post as the decisions and implications evolve.

In short, Meta updated its Hateful Content policy to explicitly allow harassment for targeted groups and remove earlier protections. We strongly encourage others, especially moderation teams, to look beyond the current version of their [Hateful Content policy](https://transparency.meta.com/policies/community-standards/hateful-conduct/) and also look at the diff between their 2024 and 2025 policies to see what was altered and removed. You can do this by clicking on the Jan 2025 date on the left nav bar.


## Threads is now in conflict with Hachyderm's inter-instance moderation policies

When we consider defederating instances we consider the Hachyderm community, especially vulnerable members. This means that when we evaluate other instances we look at the impacts of those communities on our community.

We initially Limited Threads primarily to make Threads content "opt in", as much as Mastodon tools allow, as there are several news sources, government accounts (people and agencies), and so forth on Threads. (Relevantly, among the top followed Threads accounts were POTUS and Barack Obama.) This meant we also committed to manually moderating individual harmful accounts, and interactions with their content, to maintain community safety on Hachyderm while Threads was Limited.

Threads’ recent changes in their moderation policies, both what they've put in and what they've taken out (read the diff), puts their moderation practices in direct conflict with ours. Essentially, Threads may indeed be large enough that many users are just looking to exist somewhere on social media and are not necessarily de facto fans of Mark Zuckerberg et al, but we anticipate these changes to moderation will shift the user base of Threads in a way that is damaging to the Hachyderm community, so we are defederating from them before that can occur.


## Risk and Value Considerations

When we consider defederating, another factor we consider is actual or perceived loss of value to members of the Hachyderm community. Being able to follow and interact with POTUS, local politicians, government agencies, family, friends, etc. from Hachyderm is potentially valuable.

Mid-2024 it seemed likely that Threads would be the social media platform many of those accounts would use or use as their primary social media presence. So it appeared that the long-term value was medium to high, while the slow rollout of federation allowed us ability and time to moderate Threads manually with low to low-medium community risk.

Between Meta’s policy changes and increasing popularity of Bluesky, it seems many individuals are abandoning Threads. It seems likely that politicians and government agencies will or are moving their primary social media presence elsewhere. It now appears that the long-term value is low, and even with the slow rollout for federation the risk to our community changed to high.

There’s no perfect "calculation" here, but essentially the long-term risk/reward ratio went from overall medium-high to very low because of how significantly these policy changes increase risk of harm.


## What was the data on Threads prior to defederation?

Part of how we handled Threads was meeting the situation where it was at any given time. This is why we were watching their policies, interactions with Hachyderm, news cycles, etc. This is also another reason that we mention here, and in earlier posts, about the slow roll out of federation. It means that the "instance", in the federation sense, is significantly smaller than the broader platform. To clarify what this means:



* Not all Threads accounts are federating, in fact most are not.
* Of the Threads accounts that are federating, not all are fully federating.
    * In practice, this means that Fediverse users can see and read a user's Threads posts, the Threads user cannot see Fediverse interactions with their posts. Functionally, this is/was similar to the experience of posting and boosting posts from Twitter bridges.

Specific data:



* There were ~10,000 total Threads accounts federating with Hachyderm.
    * There is no way from the data to tell how many of these are fully or partially federating.
    * To put in perspective:
        * This is significantly smaller than Mastodon Social (~265k accounts) and approximately the same size as other larger Fedi instances including Mastodon Online (~25k accounts).
        * This is approximately 0.0036% of Threads users overall, as Threads has approximately 275 million active users ([as of Nov 2024](https://techcrunch.com/2024/11/03/threads-now-has-275m-monthly-active-users/)).
* There was one user-generated report regarding a Threads user. In that case it was not about harmful content but a user interaction. There were no other reports sent to Hachyderm moderation about Threads interactions.
    * To put in perspective (and acknowledging that these two instances *do not* have the same moderation policy that Threads now does) we've fielded ~500 reports (in total) regarding Mastodon Social and 45 reports (in total) regarding Mastodon Online.
	* There were 2033 unique Hachyderm accounts following 919 unique Threads accounts and 26 unique Threads accounts following 22 uniqueHachyderm accounts.

    	* For other mods, note that the queries to figure out are not what the Admin Dashboard is running. We'll put the queries at the bottom of this blog post.

How does this tie into our overall moderation decision? Essentially, the changes to their moderation policy, whether they revert them or not, increase the risk of harm drastically and with high likelihood of changing the Threads platform account demographics faster than our ability to manually moderate them. In that respect, the decision that we would need to defederate from Threads was made after we reviewed Threads current policy and its diff when it was released on Tuesday.

Before enacting the decision, we needed to understand the impact on the Hachyderm community and prepare this statement. Since the queries on the dashboard didn't provide the level of granularity we needed, Hachyderm moderation and infrastructure coordinated to ensure that we were surfacing the correct data to inform our decision (the last bullet point above and the queries in the next section). This allows us to know how many Hachydermians would be impacted and to what degree. Thank you for your patience in this regard, as due to the significance of the follow/following severances that are occurring we wanted to be accurate in providing this data.

#### Queries to run to gather the above data

The query to run for "how many unique accounts on my instance are
following Threads accounts" is:

```
Follow.joins(:target_account).merge(Account.where(domain: 'threads.net')).group(:account_id).count.keys.size
```

Our result in this case is 2033.

The query to run for "how many unique Threads accounts are
following accounts on my instance" is: 

```
Follow.joins(:account).merge(Account.where(domain: 'threads.net')).group(:account_id).count.keys.size

```

Our result in this case is 26.


The query to run for "how many unique Threads accounts do accounts
on my instance follow" is:

```
Follow.joins(:target_account).merge(Account.where(domain: 'threads.net')).group(:target_account_id).count.keys.size

```

Our result in this case is 919.

These numbers are different from what appears in the admin dashboard (`instanceDomain.com/admin/instances/threads.net`) because the dashboard runs different queries.

The "Their Followers Here" query is:

```
Follow.joins(:target_account).merge(Account.where(domain: domain)).count
```

The "Our Followers There" query is:

```
Follow.joins(:account).merge(Account.where(domain: 'threads.net')).count
```

Essentially, these numbers aren't deduplicated so the results may
look larger than you'd want, depending on what data you need.
