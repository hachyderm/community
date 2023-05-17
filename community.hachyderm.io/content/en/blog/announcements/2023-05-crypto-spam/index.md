---
date: 2023-05-17
title: "Crypto Spam Attacks on Fediverse"
linkTitle: "Crypo Spam"
description: "Updates and information regarding the ongoing crypto spam attacks in May 2023."
author: Quintessence ([@quintessence](https://hachyderm.io/@quintessence))
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

## The Situation 

Over the past week, starting around 8 May 2023, various Fediverse instances are being
inundated with crypto spam.

<img src="generated-doge-meme-for-crypto.jpg" 
     alt="Generated doge meme with the text no no no and stop signs and money bags
         prinkled over image" />

<br />
When it appeared that only one or two instances were impacted, we made a single site-wide
announcement for each instance and explained that we were limiting the instance. As the
situation has progressed, we now know we need to change our communication strategy
for it to be more effective.

So far we have seen waves of spam from Mastodon Social, Mastodon World, and now
TechHub Social. These waves usually mean that we see over 100-200 reports in less
than a few hours. (By contrast, we usually receive ~20 reports _per week_ .)

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
you from an instance that's been limited, and for you to view their profile page,
as you would if we had only Limited that specific user.

For users on the impacted instances, these messages should not be taken as the
individual user has engaged in any sort of malicious activity. In general, when
we see individual-level malicious activity, we suspend federation (block) the
individual user rather than Limit them. Instead, these messages are only a
consequence of us needing to Limit the servers while they are doing their best
to manage the spam attacks they are undergoing.

## The impacted instances

We are maintaining the list of instances that we are limiting as a result of the
current crypto spam attack here. Note that this is not _all_ instances we currently
have limited for any reason, only the ones that are experiencing this specific
scenario. We will continue to announce when new instances are added to this list
via [our Hachyderm Hachyderm account](https://hachyderm.io/@hachyderm) and link
back to this blog post. Instances that are no longer impacted will be un-Limited.

* Mastodon Social
* Mastodon World
* TechHub Social