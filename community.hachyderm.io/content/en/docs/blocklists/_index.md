---
title: "Blocklists"
linkTitle: "Blocklists"
weight: 4
description: >
  Community information about Blocklists and how Blocklists are built.
---

## The Basics of Blocklists

### General Purpose

Blocklists are one way that a Mastodon instance can handle unwanted
content on the instance level. When a Mastodon domain is on the Blocklist,
this means that the server administrators have limited or completely
suspended activity with the server at that domain. The specific actions
are:

- Suspend<br />This is the most commonly known one, as it prevents all
instance-to-instance activity.
- Limit<br />Previously known as "silencing". This means that accounts on
the home server can follow accounts on the limited server, but that general
content from that server does not show up on the Federated timeline.
- Reject Media<br />Media from the moderated server will not display on the
home server, this includes not only media in the posts themselves but
avatars and headers as well.

[Mastodon has these features in their documentation](https://docs.joinmastodon.org/admin/moderation/#server-wide-moderation).

### Moderator vs User Actions

Users can _also_ take individual action to prevent themselves from seeing
unwanted content by blocking or limiting other accounts on the user level.
This is recommended for cases where the content is perhaps unwanted by
an individual user, but that content does not violate the home server's
ethos.

Mastodon has additional documentation about actions that individual
users can take on their [Dealing with unwanted content documentation page](https://docs.joinmastodon.org/user/moderating/).

## How Hachyderm's Blocklist is Built

At Hachyderm, we do our best to balance what actions should be taken at the
instance level and what should be handled at the user level both when it
comes to our own users and when we receive reports of users on other
instances or the instances themselves. The vast majority of the moderator
action we have taken on servers on our Blocklist is to either
silence/limit or suspend/block. The domains that are included on this list are:

- Curated from a variety of published Blocklists on other Mastodon instances
- Added based on user reports. This can mean either:
  - A domain has been reported, researched, and moderated individually, _or_
  - A high volume of reports regarding several users on an instance have led
    to an instance being researched and moderated

Although suspension is the most well-known and discussed moderation action,
domains may be limited as well. For example, we might limit a server that
has several bots that are taking over the Federated timeline but not
suspend so users can continue to follow individual accounts.

### Concerns that go into building the Blocklist

There are a few top level concerns that go into determining adding servers
to the Blocklist:

1. Does the ethos of a specific server violate the ethos of this server?<br />A few
   easily understood examples would be if a server is anti-Black, anti-queer,
   or endorses either direct or dog-whistled hate speech and content.
1. Is there a security concern around this server?<br />As a broad example,
   if we see malicious traffic coming from a specific server or servers.
1. What risk does the server pose to our users?<br />We prioritize the safety and
   experience of our users that are in historically underrepresented
   groups.
1. What do our user reports look like? Are they user level on a given
   server or are they indicative of malicious patterns server-wide?
1. What level of moderation is needed? Limit/silence or block/suspend?

It is our opinion that it is in our users' best interest to federate with
as much of the Fediverse as possible so that we can all share our joys,
sorrows, growth, learning, etc. with each other.

Our goal with the maintenance of the Blocklist is to ensure that all of
our users are safe on Hachyderm. That means when we move forward with taking
moderation action on a server, that we will take the best course of
action to ensure that safety. We will prioritize the safety of our
marginalized users over the broader experience of a completely open
and unmoderated (at the server level) Fediverse.

When we take moderation action against a server, we consider:

- The items called out in the numbered list above
- Balancing open participation with curating a safe space

### Concerns that go into transparency around the Blocklist

Some servers have reasons attached to their moderation action and
others do not. In addition, we may or may not announce when we
limit/silence or block/suspend individual instances. Why is this?

When we choose what level of notification to send, and how
transparent to be, with moderation actions we consider:

1. The impact of the change
1. The interest level in the change
1. The risk of publicizing/being transparent about the change

For example, if we were to take moderation action against
any of the large, popular Mastodon instances we would err on
the side of transparency as this would be a significant and
user impacting event.

Whenever we take action on a server that has malicious activity,
and this can be in the form of attacks on our server or in the
form of social attacks like stalking and harrassment, we err on
the side of safety. This means what level of information
we provide and how loudly (notifications, etc.) we provide
it will be based on what is safest for all of our users.

The vast, vast majority of instances fall between these two
extremes and thus the resulting decisions do not fall
perfectly in the "fully transparent" or "completely silent" buckets.
This means:

- Servers may not have reasons attached to their moderation
  decisions, but that doesn't mean they are a security or safety concern.
  <br />To do this would immediately out them as a security
  concern, by the absence of information.
- Not all changes to individual server status will be loudly announced, but some
  will.<br />
  We will use the decision making process outlined above when
  announcing.
- Not announcing that a server has changed status does not
  mean that server is or was a cause of concern. It can
  also, and frequently will, mean that the server size doesn't impact
  enough of our users to make a large announcement.

## Requesting Moderation Changes for a Server

### What to do there is a domain on the Blocklist in error

We are all human and are prone to mistakes. If there is a domain that is
moderated on our Blocklist that seems to be in error, please open a
[GitHub Issue in our Community repo](https://github.com/hachyderm/community/issues)
to request that we take another look at the domain. Please include
as much relevant context as you can to help us make our decision.
Note that depending on the circumstances, and as outlined above, we may
not be able to be fully transparent with our decision - but we commit
to erring on the side of transparency with these reports as often as possible.
For more information about how to file a report in our community
repo, please take a look at our [Reporting
Documentation](/docs/reporting).

### What to do if you would like us to moderate a server

If there is a server that is not currently moderated, i.e. either
limited/silenced or banned/suspended, then please file a report
via the Hachyderm (Mastodon) UI or [GitHub Issue in our Community repo](https://github.com/hachyderm/community/issues)
for us to take a look at that domain or domains. As before, please
include as much context as possible. If there is a concern around the
domain(s) you would like to report that would be risky to report in our
GitHub Issue tracker, please email us at [admin@hachyderm.io](mailto:admin@hachyderm.io).
For more information about filing reports and how to choose
between the Mastodon UI and the GitHub Issue tracker, please look
at our [Reporting Documentation](/docs/reporting).

### What not to do in either of these cases

There are far, far more Hachydermians than moderators. We do not follow
tags, posts, etc. to make changes to our Blocklist - we only use the sources
outlined above.
