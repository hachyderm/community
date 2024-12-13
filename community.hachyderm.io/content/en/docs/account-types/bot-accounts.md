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
- All bots must be [verified with Hachyderm](../verification/)
- Where applicable, accounts should [be verified](../../mastodon/user/verification/)
  with their relevant domain(s).

## A bit about post automation

Not all posting automation is bot, or bot-like, in nature. Many specialized accounts make
use of post scheduling to help communicate with their intended userbase.
This can include, but not be limited to, sign up windows for an event that must
be done in a specific time frame, automated posts when a blog is updated, and so on.

The line between automated posts and bot posts is a thin one, and mostly dependent on
whether a human composed a post (whether it is scheduled for now or later) and whether or not
that post is intended to repeat (the "say it once" policy on the [Specialized Account Expectations](../covenant/)).

As with many of our rules on Hachyderm, the rules and regulations for bot and automated posting
is about their impact on the server. We want that impact to be positive and non-invasive. It is
our belief that collaboration thrives where there is genuine connection. Genuine connection _can_
happen via bot and automated posts, but cannot thrive if those posts become invasive or compete with
each other negatively.

When we enforce the rules and regulations on bots and automated content, as outlined in the next
section, we do so with the goal of increasing the connected, collaborative nature of the
Hachyderm community.

Enforcement of rules
around all account types, including bot accounts, are to help
foster a sense of community. Bots that focus on humanity, such as
accessibility or care, are given greater flexibility than bots
used for promotions.

## Posting Rules

All accounts that make use of automated and/or scheduled posts must adhere to the following:

- There is an upper limit of 5 curated/scheduled/automated posts per day, with allowed exceptions on request or other approval.
  - If your bot's posting patterns have been approved as part of
	an invitation or conversation for approval, you do not need to
	chnage your bots posting behavior as part of joining
	Hachyderm.
- Posts cannot violate other rules
  - This includes server rules disallowing spam, fundraising, NSFW/18+ content (et al)
  - Hybrid accounts, those that make use of scheduled posts and are also another specialized type,
    are bound to all sets of rules for their combined, hybrid, account type.
  - Posts cannot violate the [Specialized Account Expectations](../covenant/)
- There is one exception: automated posts _can_ skirt the "say it once" policy, unless it
  becomes spam-worthy (**_community discretion_**). So, if you need to post about your event,
  blog, etc. and stay within the total number of posts per day, this is fine.

Accounts that violate the above may be limited or suspended.

### Bot Specific Rules

#### Account Configuration

- All bot accounts must [be verified with Hachyderm](../verification/), which means they agree to the [Specialized Account Expectations](../covenant/).
- All bots must select the bot checkbox in their profile settings. (Open image in new window to enlarge.)<br />
  <img src="../mastodon-bot-account.png"
       alt="Screenshot of four check boxes in account settings: require follow
       requests, this is a bot account, suggest account to others, and hide
       your social graph" 
       width="400px" />
- Bots must be clearly marked as bots so that people can easily
  opt-out of bot posts if they wish.
  - Almost all bots are required to have the `#hachybots` hashtag
	in all posts so users can easily opt-out.
  - Invited / approved bots for comunity benefit may be allowed to
	bypass this rule as long as the account itself is clearly marked as
	a bot account.

#### Restrictions on Behavior

All bot accounts, and bot-like posts, must respect consent (i.e. opt-in). This means:

- Bots may respond directly to posts that they have been tagged in.
- Reactionary bots may only be triggered / "summoned" by posts that include their handle.
  - But they cannot "doom spiral". Essentially: they _cannot_ continue to respond to every response in
    a thread, because they were tagged once, and thus auto-tagged in all subsequent responses.
- Bots _cannot_ respond to hashtags, keywords, etc. without being tagged - e.g. bots that respond to user posts based on keywords and similar.
- Bots designed to consume, use, store, or otherwise handle data (even public data) can only do so with consent (opt-in).
- Bots designed for fun _can_ skirt the "say it once" policy, unless it becomes spam-worthy (**_community discretion_**). So, if your bot only responds with "honk", and only when summoned, this is fine.

Bot accounts that violate any of the above may be limited or banned.
