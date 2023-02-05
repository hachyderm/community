---
title: "Bot and Post Automation"
linkTitle: "Bots and Post Automation"
weight: 40
description: >
  For all types of automated and scheduled content.
---

If you are running a bot account and/or plan on making use of post scheduling - this
article is for you!

## Overview

- Automated posts and bot accounts
- Posting rules for automated content
- Posting rules and behavior restrictions for bots
- All bots must be [verified](../application/)

## A bit about post automation

Not all posting automation is bot, or bot-like, in nature. Many specialized accounts make
use of post scheduling to help communicate with their intended userbase so things are not
forgotten. This can include, but not be limited to, sign up windows for an event that must
be done in a specific time frame, automated posts when a blog is updated, and so on.

The line between automated posts and bot posts is a thin one, and mostly dependent on
whether a human composed a post (whether is scheduled for now or later) and whether or not
that post is intended to repeat (the "say it once" policy on the [covenant](../covenant/)).

As with many of our rules on Hachyderm, the rules and regulations for bot and automated posting
is about their impact on the server. We want that impact to be positive and non-invasive. It is
our belief that collaboration thrives where there is genuine connection. Genuine connection _can_
happen via bot and automated posts, but cannot thrive if those posts become invasive or compete with
each other negatively.

When we enforce the rules and regulations on bots and automated content, as outlined in the next
section, we do so with the goal of increasing the connected, collaborative nature of the
Hachyderm community.

## Posting Rules

All accounts that make use of automated and/or scheduled posts must adhere to the following:

- **There is an upper limit of 5 curated/scheduled/automated posts per day. Lower is better.**
- Posts cannot violate other rules
  - This includes server rules disallowing spam, fundrasing, NSFW/18+ content (et al)
  - Hybrid accounts, those that make use of scheudled posts and are also another specialized type,
    are bound to all sets of rules for their combined, hybrid, account type.
  - Posts cannot violate the [covenant](../covenant/)
- There is one exception: automated posts _can_ skirt the "say it once" policy, unless it
  becomes spam-worthy (**_community descretion_**). So if you need to post about your event,
  blog, etc. and stay within the total number of posts per day, this is fine.

Accounts that violate the above may be limited or suspended.

### Bot Specific Rules

#### Account Configuration

- All bot accounts must [be verified](../application/), which means they agree to [the covenant](../covenant/).
- All bots must select the bot checkbox in their profile settings. (Open image in new window to enlarge.)<br />
  <img src="../mastodon-bot-account.png"
       alt="Screenshot of four check boxes in account settings: require follow
       requests, this is a bot account, suggest account to others, and hide
       your social graph" 
       width="400px" />
- Bots are required to put the `#hachybots` hashtag in _all_ posts so
  users can opt into, or out of, bot posts.

#### Restrictions on Behavior

All bot accounts, and bot-like posts, must respect consent (i.e. opt-in). This means:

- Bots may respond directly to posts that they have been tagged in.
- Reactionary bots may only be trigged / "summoned" by posts that include their handle.
  - But they cannot "doom spiral". Essentially: they _cannot_ continue to respond to every response in
    a thread, because they were tagged once, and thus auto-tagged in all subsequent responses.
- Bots _cannot_ respond to hashtags, keywords, etc. without being tagged - e.g. bots that respond to user posts based on keywords and similar.
- Bots designed to consume, use, store, or otherwise handle data (even public data) can only do so with consent (opt-in).
- Bots designed for fun _can_ skirt the "say it once" policy, unless it becomes spam-worthy (**_commmunity descretion_**). So if your
  bot only responds with "honk", and only when summoned, this is fine.

Bot accounts that violate any of the above may be limited or banned.
