---
title: "Preserving Your Mental Health"
linkTitle: "Mental Health"
weight: 40
description: >
  How to use the Mastodon tools help preserve your mental health on the Fediverse.
---

FIXME - revisit individual paragraph phrasing
FIXME - reconcile the opt-in, opt in, opt-out, opt out differences
FIXME - consistently case fediverse Fediverse
FIXME - hyphen consistency : instance-level, instance level; server level, server-level

## Social media and your mental health <!-- omit from toc -->

There are many articles available online about social media, general online
engagement, and mental health. This document is going to focus on a subset
of these and focus on helping you use the Mastodon tools to uphold your
personal needs and boundaries.

- [Moderation action and individual action](#moderation-action-and-individual-action)
- [Mastodon tools at your disposal](#mastodon-tools-at-your-disposal)
  - [Unwanted content](#unwanted-content)
  - [Additional features](#additional-features)
- [Patterns for a better Fediverse experience](#patterns-for-a-better-fediverse-experience)
  - [Control what content you are exposed to](#control-what-content-you-are-exposed-to)
    - [Proactively filter content](#proactively-filter-content)
    - [Proactively obscure media](#proactively-obscure-media)
  - [Control your personal information](#control-your-personal-information)
    - [Protect your personal information](#protect-your-personal-information)
    - [Limit how and who can interact with your account as needed](#limit-how-and-who-can-interact-with-your-account-as-needed)
  - [Collective action requires a collective](#collective-action-requires-a-collective)
    - [Give yourself permission](#give-yourself-permission)
  - [Create and maintain interpersonal boundaries](#create-and-maintain-interpersonal-boundaries)
      - [When someone violates your boundaries](#when-someone-violates-your-boundaries)
      - [When you violate someone else's boundaries](#when-you-violate-someone-elses-boundaries)
- [Context Setting](#context-setting)

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

A couple examples of discussions that can have a positive impact on the community as a whole
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

## Patterns for a better Fediverse experience

Here we are detailing patterns that you can implement and iterate to improve
your Fediverse experience. The tools that can assist are directly referenced
in each section. For how to implement, please see the docs linked in the above
[Mastodon tools at your disposal](#mastodon-tools-at-your-disposal) section.

### Control what content you are exposed to

The mental model that helps the most here is to realize that social media by design opts
everyone into all content by default. Additional tooling constrains this default opt
in, either by creating a new default of opt out or by creating situational opt outs.

Deciding which opt outs you want to implement will inform what tools you choose to
use for your benefit. 

#### Proactively filter content

There will be times that you will want and need to filter content. This might be
permanent or temporary. 

* Active opt in<br />
  Following keywords and hashtags can provide relief when you need to decompress. Cats, math,
  stomatopoda - anything that helps.
* Active opt out<br />
  You can filter out keywords and hashtags to either temporarily or permanently remove yourself
  from certain content and discussions.

We recommend filtering out words, phrases, and/or hashtags that:

* You do not want to be exposed to, for any reason.
  * This includes not wanting to be exposed to messages of support,
    which can have the unintended, added consequence of reminding you
    why support is needed. "For any reason" is for any reason.
* You do not want to exposed to even via reference in a content warning.

Filters will filter out posts with content warnings as well.
When you filter out content you will still be able to see other posts from other users
you do not actively block in both your follows, local, and federated timelines.

Note that you can still choose to filter or block content after [reporting it
to the mods](/docs/moderation/reporting/). We will still see the report.

#### Proactively obscure media

When changing the default opt in for media, you can either:

* Opt in to all media<br />
  This will display all media, regardless of whether the media is parked as sensitive.
* Obscure media marked as sensitive<br />
  This will only obscure media if the person posting it marked it as sensitive.
* Obscure all media<br />
  This will obscure all media, regardless of whether the person posting it marked it
  as sensitive.

[Please visit the Mastodon preferences doc to show how hidden media
appears](https://docs.joinmastodon.org/user/preferences/#sensitive).

We recommend obscuring media:

* If images and other media are a frequent trigger of any kind.
* If you do not want to be exposed to media that you do not explicity opt in to.

### Control your personal information 

#### Protect your personal information

There are a few tools that you can use to protect your personal information

FIXME - post visibility, account visibility; auto-delete posts; hide social graph
* auto-delete posts from a "content visibilty" perspective might be controversial, just be aware

#### Limit how and who can interact with your account as needed

Follower/following, DMs (always on), public vs private account

This is where you can control who can interact with your account and how they can
do so.

### Collective action requires a collective

It is common to feel the impulse to respond to content that we see that has a negative
impact on ourselves and/or others. When these engagements go well, it is/was an opportunity
to help others grow on their journey to be better humans. When they do not, however,
they can be a source of stress at best or result in harassment at worst.

Improving the experiences of yourself and others on social media is a form of collective
action. There are many, many articles about maintaining or improving your mental health while
taking part in collective action of some kind.

While the research and self care in that broader context exceeds the scope of this article,
what everyone should remember is this:

> It is important for everyone to do their part to create and maintain safe communities
> (and build a better world). The reason this is called collective action is because it
> takes more than one person to accomplish group-level and societal changes. As with any
> effort to build something better, individuals that are doing their part for others must
> also remember to do their part for themselves.

#### Give yourself permission

Questions you should ask yourself when you are deciding whether or not to engage in a
thread / conversation that has a negative impact on yourself and/or others:

* Do you, specifically, need to engage at this moment or can another member of the
  community (collective) do it?
* If you need to be the one that engages, either due to expertise or some other reason,
  do you have the capacity to do in the current moment? If not, can you defer until a
  time that you do? 

Remember:

* The Fediverse is vast and if you see an issue, especially one that the community commonly catches,
  it is likely someone else will say / do something. 
* Even if you do not have the capacity at the moment and no one else does, protecting your mental
  health will ensure your ability to continue to sustainably help others while growing yourself. 

Being able to make contributions over long periods of time will almost always yield more and better
results than doing short bursts of high volume.

Relevantly:

* You can leave conversations at any time for any reason. You do not need to justify or inform when
  you do, especially if doing so will continue to inflame the situation.
* You can opt-out of any content at any time for any reason. You to not need to justify or inform
  when you do, especially if doing so will be negatively impactful to yourself.
* You can also opt-in to content at any time. Any time you feel the need to opt-out of content,
  the ability is always there to opt back in when you're ready.

Opting in and out of topics, especially those that might be personally relevant and soul straining
for you, is a very useful tactic for creating personal boundaries. It limits when and how you are
exposed to that type of content, especially if / when there is a news cycle or other event increasing
the discussion frequency.

### Create and maintain interpersonal boundaries

First and foremost: it is not ok for someone to violate your boundaries or for you to
violate someone else's. To be clear, this section is _not_ referring to stalking and other forms
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

Both of these patterns involve having a healthy understanding of public spaces and consent.
A conversation thread being on social media does not necessarily mean it is for everyone to
engage with. This concept should feel familiar: if a group is going for a walk and talking
together in a park it does not mean that their walk and conversation is for everyone in that
park at that time. That said, there are also public performances that happen in public
spaces which _are_ intended for everyone. Similar to the examples just provided, there are
frequently communciated boundaries and expectations around private and public engagements
happening in public spaces.

##### When someone violates your boundaries

If you have asked someone to stop engaging with you and/or a your thread, the main tools at
your disposal are:

* Mute the user<br />
  They will still be able to follow you and see your posts. They will not be notified they are muted.
* Block the user<br />
  They will not be able to follow you, see your posts, etc. They will not be notified that they are
  blocked, but they will be able to tell that they are blocked.
* [Report the user](/docs/moderation/reporting/)<br />
  Remember you can always escalate to the moderation team.

Which of these actions you take is entirely up to you. Your account is how you navigate the fediverse
and you are the one that will need to decide which of these are warranted for the situation you are in.

Note that we do _not_ recommend announcing when you have muted / blocked someone, as that defeats
the purpose of removing yourself from the conflict. There are reasonable exceptions to this involving
the safety of others and/or the overall community. In this case we request that you
[report the situation to the mods](/docs/moderation/reporting), whether you post about it or not,
as it is the job of moderation to handle instance-level policy such as this.

##### When you violate someone else's boundaries

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

