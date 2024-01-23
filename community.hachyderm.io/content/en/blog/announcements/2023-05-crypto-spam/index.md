---
date: 2023-05-17
title: "Crypto Spam Attacks on Fediverse"
linkTitle: "Crypto Spam"
description: "Updates and information regarding the ongoing crypto spam attacks in May 2023."
author: Quintessence ([@quintessence](https://hachyderm.io/@quintessence))
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

## The Situation 

Starting around 8 May 2023, we began to receive reports that
Mastodon Social was being inundated with crypto spam.

<img src="generated-doge-meme-for-crypto.jpg" 
     alt="Generated doge meme with the text no no no and stop signs and money bags
         prinkled over image" />

Initially, it appeared that only Mastodon Social, and then
Mastodon World, were impacted. In each case we Limited the
instance and made a site-wide announcement. As the issue
progressed, it became clear that more instances were being
targeted for this same style of crypto spam. As a result, we
have decided to change our communication strategy to utilize
this blog post as a source for what's happening and who is being
impacted, rather than relying on increasingly frequent site-wide
announcements.

As it stands: right now we have seen waves of spam from Mastodon
Social, Mastodon World, and now TechHub Social. These waves
usually mean that we receive over 100-200 reports in less than a
few hours. (By contrast, we usually receive ~20 reports _per week_.)

## What this means for Hachydermians (and Mastodon users in general)

Spam attacks seem to make use of open federation to either find accounts to misuse
follow/unfollow behaviors, DMs, comments, and other invasive behaviors. In general,
Limiting a server is sufficient for mitigating the impacts of these behaviors. Limiting
means that Hachydermian's posts no longer show up in the Federated feeds of impacted 
instances, which means that bots can no longer use the Federated feed as a vector for
malicious behavior. While this is a good thing and means that these bots will no longer
be able to spam Hachydermians, the Limit works both ways. This means:

* The posts for Limited instances will no longer show up on the Federated feed
* You will receive approval requests for all accounts on Limited instances
* User profiles will appear to have been "Hidden by instance moderators"

The UI messages for the latter two are a little difficult at times to determine
what it means. Essentially, you will see the same message for a user to follow
you from an instance that's been Limited, and for you to view their profile page,
as you would if we had only Limited that specific user.

For users on the impacted instances, these messages should not be taken as the
individual user has engaged in any sort of malicious activity. In general, when
we see individual-level malicious activity, we suspend federation (block) the
individual user rather than Limit them. Instead, these messages are only a
consequence of us needing to Limit the servers while they are doing their best
to manage the spam attacks they are undergoing.

## The impacted instances

We are maintaining the list of instances that we are Limiting as a result of the
current crypto spam attack here. Note that this is not _all_ instances we currently
have Limited for any reason, only the ones that are experiencing this specific
scenario. We will continue to announce when new instances are added to this list
via [our Hachyderm Hachyderm account](https://hachyderm.io/@hachyderm) and link
back to this blog post. Instances that are no longer impacted will be un-Limited
and removed from the list below. (When the list is empty, that means that all
instances have been un-Limited.)

### Updates

Update 25 May 2023 - we've been crypto spam free from Mastodon
Social and Mastodon World, so we've gone ahead an un-Limited those
instances.

Update 2 Jun 2023 - we've been crypto spam free from TechHub Social,
so we've gone ahead and un-Limited that instance! That's the last
one, so this incident is resolved.
