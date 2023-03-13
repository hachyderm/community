---
title: "Preserving Your Mental Health"
linkTitle: "Mental Health"
weight: 40
description: >
  How to use the Mastodon tools help preserve your mental health on the Fediverse.
---

## Social media and your mental health <!-- omit from toc -->

There are many articles available online about social media, general online
engagement, and mental health. This document is going to focus on a subset
of these and focus on helping you use the Mastodon tools to uphold your
personal needs and boundaries.

- [Moderation action and individual action](#moderation-action-and-individual-action)
- [Mastodon tools at your disposal](#mastodon-tools-at-your-disposal)
  - [Unwanted content](#unwanted-content)
  - [Additional features](#additional-features)
- [Common negative impacts and ideas to address them](#common-negative-impacts-and-ideas-to-address-them)
- [Patterns to proactively protect your mental health](#patterns-to-proactively-protect-your-mental-health)
  - [Collective action: a grain of sand](#collective-action-a-grain-of-sand)
  - [Give yourself permission](#give-yourself-permission)
  - [Keywords, filtering, and hashtags: a proactive approach](#keywords-filtering-and-hashtags-a-proactive-approach)
  - [Setting healthy boundaries and protecting your personal information](#setting-healthy-boundaries-and-protecting-your-personal-information)
  - [Creating some proactive boundaries](#creating-some-proactive-boundaries)
  - [Enforcing boundaries and what happens they're violated](#enforcing-boundaries-and-what-happens-theyre-violated)
  - [How and who can interact with your account](#how-and-who-can-interact-with-your-account)
  - [Control what content you want to be exposed to](#control-what-content-you-want-to-be-exposed-to)
  - [Control what cadence (?)](#control-what-cadence-)
- [Context Setting](#context-setting)
- [Know when to engage the moderators](#know-when-to-engage-the-moderators)
- [Creating space for yourself](#creating-space-for-yourself)

## Moderation action and individual action

As you navigate the Fediverse, you will frequently run into situations where you need
to decide if a situation can or should be handled by you individually, by the moderation team,
or both. When you are deciding which action(s) to take, the main question you should ask is:

> Is the discussion / interaction that I encountered something that I need to avoid
> for my own mental health or is it something that poses a community risk that needs to
> be handled by moderation?

A couple examples of discussions or interactions that would have a negative impact on the community:

* Any posts that are supporting or perpetuating racist, homophobic, transphobic, and other \*ist / \*phobic viewpoints.
* Any interactions where a user or users is targeting an individual or group for stalking and/or harassment.

A couple of examples of discussions that can have a positive impact on the community as a whole
but can have a negative impact on individuals:

* Posts sharing and discussing news cycles around individual or state violence,<br />
  even if they are condemning that violence.
  * Individuals and communities that are the current or historic target of that violence may be triggered.
* Posts about individual exposure to, or recovery from, various forms of trauma.
  * Individuals who have been exposed to the same, or similar, situations may be triggered.

The above examples are not comprehensive, but do show situations where you may need to protect
your own individual mental health even as communities across the Fediverse discuss and interact
in ways that show collective growth.

## Mastodon tools at your disposal 

Being online is a bit like being in a crowded room or stadium, depending on
the audience size. That means when you go to take a step back, you may need
to use some of the Mastodon tools to help you maintain the space you're trying
to create for yourself either temporarily or permanently. 

### Unwanted content

These are the features that Mastodon built and highlighted for dealing with
[unwanted content](https://docs.joinmastodon.org/user/moderating):

* Filtering
  * You can filter by hashtag and/or keyword
  * You can filter permanently or set an expiration date for the filter
  * This feature is most useful when you want to completely opt-in or opt-out of content.
    * Opt-in: perhaps you want to follow all Caturday posts in a separate panel or follow cat posts generally.
    * Opt-out: you do not want to be subject to the unpredictable news cycles around events that
               impact a group you're a member of. Even if people are expressing support for you, you just
               do not want to see any of it at all ever.
* Other users
  * Following/Unfollowing
    * Following: explicit opt-in to another user's posts, boosts, etc.
    * Unfollowing / not following: a passive opt-out. You will still see posts / etc. if a user you are
          following interacts with them.
  * Muting / Blocking
    * Mute: You will not see another user's posts, boosts, etc. but they can see and interact with yours. (Note:
          you will not see them doing so.) Users are not notified when they are muted.
    * Block: You will not see another user's posts, boosts, etc. _and_ they cannot see yours. Users are not
          notified when they are blocked, but as your content "disappears" for them most users can tell if
          they're blocked.
    * Hiding boosts
      * Less commonly used tool, mainly helpful if you feel another account's boosts are "noisy" but their
        content is otherwise fine.
* Other instances 
  * Block
    * This is the only action available to individual users. Moderation tools allow for more nuanced
      instance-level implementations including allowing posts but hiding media. (Please see [Mastodon's instance
      moderation documentation page](https://docs.joinmastodon.org/admin/moderation/) for the complete list.)
    * When you block another server you will not see any activity from any user on that instance. Instance
      admins and other users are not notified when you have blocked their instance.

How to implement all of these features are on [Mastodon's Dealing with unwanted content doc page](https://docs.joinmastodon.org/user/moderating/).
Please refer to the documentation page for the implementation detail for each.

### Additional features

There are many more Mastodon features that you can use to help improve your experience of the Fediverse,
in particular in your account profile and preferences settings. These features mostly control the visibility of
your profile, your posts, and the posts of others.

* Limiting how other accounts interact with yours (or not)
  * Follow requests
    * When enabled, you need to explicitly approve a potential follower. Only approved accounts can follow you.
  * Hide your social graph
    * When enabled, other accounts cannot see your followers or who you're following.
  * Suggest your account to others.
    * Disabled by default. When enabled your account is suggested to others to follow, increasing your visibility.
  * DMs, important notes:
    * DMs cannot be disabled and you cannot restrict who is able to DM you (e.g. Followers Only).
    * When you include a new user to an existing DM, they can see the DM entire DM history. This is more like adding
      a new user to a private Slack channel than the way other tools handle DMs by creating a new group thread with no history.
* Limiting post / account visibility (or not)
  * Posting privacy
    * Can be set to public, followers only, or "unlisted". The latter means that someone can see your activity by going
      to your profile, but cannot see your activity in any of their individual, local, or federating timelines.
  * Opting out of search engine indexing
    * [Important note that there are limitations to this feature](https://nexusofprivacy.net/mastodon-privacy-remember-that-public-and-unlisted-posts-can-be-indexed-by-search-engines/). Treat all of your data
      as public data.
  * How media displays
    * Can be set to always show, always hide, or to only hide when marked sensitive. If you find that media such as static
      and/or animated images, video, etc. have a negative impact on your mental health, you might want to enable Always Hide.
  * Disable content warnings
    * If you find that content warnings create more barriers than access, you may want to enable "always expand posts marked
      with content warnings".
  * Slow mode
    * Enabling this feature means you will need to refresh for new posts to be added to the timeline you're
      currently viewing.

The above are all set in your profile and preferences. We have documented how to configure these settings on
our our [Mastodon User Profile and Preferences](/docs/mastodon/user/profile-preferences/)
doc page.

## Common negative impacts and ideas to address them

FIXME - this needs to be moved to under the next section.

There are a few patterns on social media that are detrimental to us as
individuals, even if there is a collective benefit.

## Patterns to proactively protect your mental health

There are a few patterns that you can use to get ahead of posts that will negatively impact your
mental health.

### Collective action: a grain of sand

FIXME: likly rewrite, but essentially "collective action requires a collective: find your collective"

The "a grain of sand" analogy is a great metaphor for individual or collective action. This analogy also
features heavily when evaluating different ideas and recommendations to improve and protect your
experience on the Fediverse.

The analogy itself is succinct: one grain of sand does not make or shift a dune, but all the grains together
comprise its shape. When wind or water move an individual grain of sand the dune remains the same shape. Over time,
dunes shift. In extensions of the analogy, canyons are carved.

The reason this analogy is relevant here: you do not need to sacrifice your individual mental health, in
solitude, for collective action. How you implement this and what it means to you will depend on your
individual needs and boundaries.

You will see other references to this analogy in this document.

### Give yourself permission

This is not a Mastodon tool, but a mindset. For anyone who wants or needs to have it stated:

* You can leave conversations at any time for any reason. You do not need to justify or inform when
  you do, especially if doing so will continue to inflame the situation.
* You can opt-out of any content at any time for any reason. You to not need to justify or inform
  when you do, especially if doing so will be negatively impactful to yourself.

About leaving conversations: contributing to change is a bit like general elections. There may be thousands, or
even millions, partaking in the election. The individual vote may be a grain of sand on a dune,
but the collective vote provides consensus (the shape of the dune). This means that while it is
important to have individual and collective conversations that improve the lives of yourself and
others, that _each individual_ conversation is the grain of sand and the _net benefit_ is the dune.
If a particular attempt at conversation to inspire change in someone else isn't doing so, and
especially if their response negatively impacts you, remember to walk away for any reason. There
will always be next time, with another grain of sand or the same one, and you do not need to
continue a current conversation that is ineffective and/or damaging.

About opting-out of content: some forms of content are community-beneficial and individually harmful.
This is especially true of conversations around news cycles, their impacts, and responses (including
protests and so forth). When you're a member of a group or community that is being targeted by another,
this means that you periodically inundated with Everyone's Thoughts, Opinions, and Questions About What To Do
at unpredictable times. While you may support the community supporting you, for your own mental health
you may want to not feel like you should partake in those conversations. In fact you may
even prefer to navigate social media as if those conversations aren't happening.


### Keywords, filtering, and hashtags: a proactive approach

The two main uses of filtering is to either opt into or out of content. You might follow,
or create a filter, for Caturday posts because cats are precious. You might use the same
mechanism to opt _out_ of content about a specific news cycle, or that uses certain tags,
because you do not want to engage with that content either temporarily or permanently.

### Setting healthy boundaries and protecting your personal information

### Creating some proactive boundaries

* for large accounts, accounts for people / communities that are at risk
* Auto-deleting posts after a certain period of time
  * Why there might be disagreement with this / disappearing / linked content

### Enforcing boundaries and what happens they're violated

First and foremost: it is not ok for someone to violate your boundaries or for you to
violate someone else's. To be clear, this section is _not_ for stalking and other forms
of harassment. If you are experiencing these, please [report it to the moderation team](/docs/moderation/reporting).

The common patterns you'll see here:

* When someone is asked to stop engaging in a topic of conversation, thread, or with someone else overall and they do not. e.g.:
  * "Please don't talk about TOPIC in this thread."
  * "Please don't continue to engage with this conversation."
  * "Please don't continue to engage with me."
* When a person who is a member of a community posts and clearly identifies an [in-group](https://en.wikipedia.org/wiki/In-group_and_out-group)
  thread and non-members / out-group persons respond. e.g.:
  * "Black Mastodon users..." -> If you are not Black, do not respond.
  * "Non-native English speakers..." -> If your native language is English, do not respond.

For the latter: it is not feasiable for anyone to try and individually block or otherwise filter out who they
suspect is not a member of the in-group they are attempting to converse with. If you know that you are not
in the requested group, do not respond for any reason. If you do and you're a Hachydermian, you will be in
violation of our [Don't Be A Dick](/docs/rule-explainer) policy (at a minimum).

For the former, please read on.

##### Someone violating your boundaries <!-- omit from toc -->

If you have asked someone to stop engaging with you and/or a your thread, the main tools at
your disposal are:

* Mute the user<br />
  They will still be able to follow you and see your posts. They will not be notified they are muted.
* Block the user<br />
  They will not be able to follow you, see your posts, etc. They will not be notified that they are
  blocked, but they will be able to tell that they are blocked.

Which of these actions you take is entirely up to you. Your account is how you navigate the fediverse
and you are the one that will need to decide which of these are warranted for the situation you are in.

Note that we do _not_ recommend announcing when you have muted / blocked someone, as that defeats
the purpose of de-escalating the conflict. There are reasonable exceptions to this involving
the safety of others and/or the overall community. In this case we request that you
[report the situation to the mods](/docs/moderation/reporting), whether you post about it or not,
as it is the job of moderation to handle instance level policy such as this.

##### You're violating someone else's boundaries <!-- omit from toc -->

* Step away / adhere to the request. This is true regardless of who is "in the right". The
  conversation is not effective and should cease.
* Apologize, as appropriate. You will need to use good judgement here and should only apologize
  if and when you are not emotionally charged in a way that prevents you from using good judgement.
  * Depending on the impact to the person setting the boundary, if they've asked you to stop engaging
    there are going to be times when an apology results in further corrective action from them
    including muting, blocking, or reporting to the moderators.
  * If this happens this is not a flaw in them or necessarily a flaw in you. Allow them to meet
    their own needs without judgement or further engagement.
  * If you are a Hachydermian, refusing to let someone walk away regardless of whether they accepted
    or rejected your apology, or if/when you don't have clarity on whether they've accepted or
    rejected your apology, is a violation of our [Don't Be A Dick](/docs/rule-explainer)
    policy at a minimum.

### How and who can interact with your account

Follower/following, DMs, public vs private account

This is where you can control who can interact with your account and how they can
do so.

### Control what content you want to be exposed to

Filtering, etc. Display images or not, boosts or not, etc.

This is where you can control what content you are exposed to and either increase
or decrease certain types of content based on hashtags and keywords.

### Control what cadence (?)

Doomscrolling.


---

---

---

FIXME - make sure to pepper through / repeat the followng: preserve your mental health,
also report to mods when appropriate. This should not be used in lieu of reporting.

:warning:️ Self awareness -> know when to step away and what situations your prone to "stepping in to".

## Context Setting

There are situations where individual Hachydermians may need to create
space to preserve their mental health. Some common situations include
not limited to:

* When there content that you do not want to engage with in general, but
  is not in and of itself problematic.
* When there is an event in a news cycle, viral post, and so on that negatively
  impacts your mental health.
* When you don't want to see content from specific users, but the users
  themselves are not otherwise harmful or warranting moderation.

## Know when to engage the moderators

The goal of this doc is to help you create space for yourself when
on Hachyderm. The goal is not to avoid situations where users and
servers should be [reported to the moderator team](/docs/moderation/reports/).

## Creating space for yourself

It is important to use the tools available to you to your benefit. In the
context of creating mental and emotional space, or setting and maintaining
boundaries, there are 

FIXME - need to write out the following:

- Remember to block content that is triggering _to you_, so
  blocking hashtags, spoilers, traumatizing content
- We as mods can only moderate at the community level, users need
  to (to a point - clarify) moderate at the individual level.
- Hashtags - fedihire, feditips, fediblock, etc.
- Protecting your Online Experience / Mental Health might be a better phrasing


What you should do to protect your mental health:

- Don't doomscroll
  - Mastodon feature to assist with this?
- Don't engage with users that are negatively impacting your mental health
  - This means not going onto their threads to engage with them as well as
  - not responding when they engage with you.
  - This means setting boundaries for persisent people, and enforcing them
  - as needed (blocking, muting, etc.)
  - Just the whole "stepping away" thing.
- Report users and content that needs server-wide policy
  - The difference between "is this bad for me or is this bad for the community"
- For content that is "bad for me, fine for server":
  - Use block, mute, etc. to limit or prevent individual interactions
- Be mindful of whether your forwarding a report to another server's mods or not
  - In the cases of brigading, the domain is run by the same people you're reporting
  - and the report is an attack vector pointing them to you. You can always choose
  - to not forward a report.
- Interactions that do not go the way you intend note.
- Too many followers? Limit who can follow you by requiring them to request.
- Personal bounardaries are more about the software, know yourself
  - What topics are unsafe for you? How can you keep them away from you?
  - Unsafe / frustrating / traumatizing == avoid for any reason you wish
  - What topics do you frequently want to Fix Others Mindset on that Frequently
  - Results in Negative Experiences for you? -> Filter / block / mute, prevent temptation.
- Don't forget that unfollowing is an option along with block / etc.
- Can users prevent DMs? Can users individually prevent media from loading?
- That image about "Slack"tivism: online petition, social media posts, but no real change.
  - Change is change, if the person you are arguing with immediately changes their view,
  - is the negative consequence to you worth it for that interaction?
  - Does it move the social justice issue forward?
    - Yes, understood that it's a collective effort to shift collective minds, this is a
    - one off situation.
- Any statements on privacy: images of you, your pets, your home, your family, the usual PII warnings.
  - May exceed scope of this page, but these are frequent doxxing tactics. People can doxx
    pretty easily, actually.
- Self service: service to the self