---
date: 2024-01-14
title: "A Minute from the Moderators"
linkTitle: "January Moderator Minute"
description: |
  Threads Update, Community Collaboration, and Trusted Reporters
author: Hachyderm Moderation ([@Hachyderm](https://hachyderm.io/@Hachyderm))
---
 
We hope everyone had a wonderful and safe new year celebration!
 
In today’s moderator minutes we will be focused on the continuing conversations around Threads and how Hachyderm moderation is continuing to expand our collaboration with our community
 
## What’s going on with Threads?

### Status

As of December 13, 2023, Threads has begun to test their implementation of ActivityPub. As of January 5, 2023, there are nine users from Threads are federating with Hachyderm’s instance. This is an increase of two users from our prior report.

When reviewing their available Terms of Use and Supplemental Privacy Policy provided by Meta, we don’t see any significant changes. This is not official legal or privacy advice for individual users and we recommend evaluating the linked documents yourself to determine for yourselves.

It’s important to remember a few things:
- The Mastodon/ActivityPub at their core uses a form of caching of information in order to make the process as seamless as possible. For example, when you create a verified link on your profile, every instance that your profile opens on does its own checks of the links and saves the validation on that third party server. This helps prevent malicious actors from falsifying their verified links that would then trickle out to other instances.
- We don’t transmit user IPs to any third party instances as part of your interaction. If Meta is able to collect your IP, it would be through a direct interaction with a post on their server or CDN.

For more details, review our original update about Threads (https://community.hachyderm.io/blog/2023/12/23/threads-update/)

### Limiting Threads

Based on user concern, we are shifting to a Limited status with Threads.

We have included the definition of limit below that comes from the mastodon documentation. (https://docs.joinmastodon.org/admin/moderation/#limit-user)

A limited account is hidden from all other users on that instance, except for its followers. All of the content is still there, and it can still be found via search, mentions, and following, but the content is invisible publicly.

What this means:
- You will still be able to follow people from Threads when they federate those users
- You will not see Threads posts on your timelines unless you follow the user
- You will be required to approve all followers from Threads
- You will be required to accept a prompt before viewing a Threads user’s account unless you are following them

### Next Steps

As Threads continues to implement their integration with ActivityPub and the Fediverse at large, we will watch how those users integrate with our community and how their service interacts with our servers. If you would like to learn more about our criteria for how Hachyderm handles federating with other instances, please review our A Minute from the Moderators - July Edition where we list out our criteria.

##### Very, very quick Q&A on Threads

**Q: What happens if there is a problematic account on Threads that is federating?**

A: They will be blocked by our existing moderation policies.

**Q: What happens if there are multiple problematic accounts on Threads that are federating?**

A: Depending on the volume, we will either block all those individual accounts or Threads as a whole.

**Q: I am concerned about anti-trans and other hate content that may come from Threads.**

A: We are too! And we continue to monitor the instance for any of these behaviors. If and when that type of content appears, we will block it the way we do with any other instance.

**Q: Why are you giving Threads “a chance”? We know about the parent company.**

A: We’re not giving Threads “a chance” so much as meeting the current situation where it’s at with plans to continue to adapt as the situation changes. Since there are 9 users, we’re treating this instance like a 9 user instance. In cases with instances that are ~50 users or less, unless the instance is cohesive (e.g. examplenazi.com where they all espouse that ideology), we moderate individual accounts. This means that regardless of the status of Threads as a whole or the number of federating accounts, accounts like Libs of Tik Tok would never federate with Hachyderm for being in violation of our federating policy.

## Community Collaboration\

### Community Votes
In the approximately 15 months since Hachyderm scaled, we have limited or suspended federation with 19 instances per month for a total of 285 instances. These instances in large part have been banned in order to pre-emptively protect our users. In almost every case, we know that these instances go against everything we stand for as a group. However, in a few of those cases, it’s more nuanced to determine if/when we should block an instance and how we should communicate those changes.

For example, when we blocked exampleillegal.com for illicit materials. We didn’t announce the change and we expect that none of our users will take issue with us blocking that material.

In contrast, on Jun 30, 2023, 22:12  UTC, we made the following announcement:

>👋 Hello Hachydermia!
>
>Due to the number of Twitter/Bird Site relay servers that have gone offline after the pricing update to Twitter's API, we have recently started cleaning up servers that federate with our environment but appear to be offline.
>
>If we removed a server that was functional and it has impacted your experience, please open a ticket on our GitHub issue page and we can evaluate reestablishing access.

Since making that decision, we had a few requests from users to re-evaluate 2 instances that we blocked but the other instances that we blocked remain blocked and the search box is clear of those invalid instances. While it was a change that was made for convenience and not protection, it is a change that had a large scale impact.

There are some cases that are more complicated and we would like to gather feedback from our community to determine which route best aligns with the entire community. We are releasing a new process to collect that information.
1. Moderation team determines that we need a survey from the community
1. Moderation team develops a multiple choice set of options for how to respond
1. Moderation team will make a post informing the community about a survey
1. A new announcement will be published
1. Users will be able to respond to the announcement for 72 hours
1. At the end of the 72 hours, the moderation team will collect the results from the community and close the poll.

This method isn’t perfect, but we are excited to continue to work on a method to collaborate with our community in convenient and meaningful ways.

### Trusted reporters

Starting this month, the moderation team will be reaching out to select users to ask them to join our Trusted Reporters group. These users will be selected based upon the quality of the reports that they have submitted that have resulted in actions by the moderation team. This group of individuals will be given an opportunity to learn more about the moderation process. The goal is to ensure that community members are able to deliver the most meaningful reports to our moderation team. In exchange, these trusted reports will have a more direct line of communication to a few members within the moderation team that can help assist in the event of a time critical need for moderator support.

### How to become a trusted reporter

It’s important to note that Trusted Reporters will not have access to the moderation interface, admin interface, infrastructure, or tooling. The primary goal of the Trusted Reporters reporters program is to ensure the delivery of high quality reports and faster responses for time critical issues. As a result, the moderation team will select trusted reporters by reviewing users that submit quality reports that contain:
- What - Ensure that all of your reports include the posts that you are concerned about
- Why - Ensure that you provide a written explanation of your concern and categorize the report appropriately

Thanks to everyone in the Hachyderm family for the laughs, love, and support through 2023. We look forward to an incredible 2024!

Your Hachyderm Moderation Team!
