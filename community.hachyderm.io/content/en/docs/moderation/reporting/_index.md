---
title: "Reporting Issues and Communicating with Moderators"
linkTitle: "Reporting and Communication"
weight: 40
description: >
  How to report issues and interact with the moderation team.
---

There are three ways to correspond with the Hachyderm Moderation
team:

- [Expectations](#expectations)
- [How and When to use Email](#how-and-when-to-use-email)
- [How and When to use the Mastodon UI](#how-and-when-to-use-the-mastodon-ui)
  - [What you should include in your report](#what-you-should-include-in-your-report)
    - [Limitations of the Mastodon Admin Interface](#limitations-of-the-mastodon-admin-interface)
- [How and When to use the GitHub Issue Tracker](#how-and-when-to-use-the-github-issue-tracker)

In general, the Mastodon UI (i.e. the "report" feature on
Hachyderm.io) is used for reporting specific posts, users, and
domains. The GitHub Community Issue tracker is for other types of
reports as well as raising other questions and conversations with
the Hachyderm Moderation Team. Optionally, users may also send us
information via email if neither Mastodon reports nor the
GitHub Community Issues are appropriate for the conversation.

## Expectations

Our server rules still apply when filing a report or otherwise
communicating with the moderation and infrastructure teams.

## How and When to use Email

The moderation team should, in general, only be contacted via
email to:

* Supplement a report in the Mastodon UI
* Provide a report or other communication that cannot be in a
public forum, like the GitHub Issue tracker, and cannot be
submitted via the Mastodon UI.
* Request information about creating a [specialized account](../../account-types/).

In short: please prioritize using the Mastodon UI and/or GitHub
issues as often as possible. That said, if you would need to reach
out to the admin team for any of the above situations or another
grey area, please use [admin@hachyderm.io](mailto:admin@hachyderm.io).

## How and When to use the Mastodon UI

The Mastodon UI, i.e. what you see when you're using Hachyderm.io
or your home Mastodon instance of choice, should generally be used
for reporting issues that can be reported via reporting individual
posts. This typically is used for:

* Reporting individual posts but not the user overall
* Reporting a user via their posts
* Reporting a domain via the posts of their users

For information about the report feature, and what we see when you
send us a report, please look at our [Report Feature doc page](../../mastodon/moderation/report-feature/).

### What you should include in your report

* Include specific posts where relevant
    * This includes if you're reporting a specific user as an individual or as
    as a general representation of a server dedicated to that type of behavior.
    * Note that it is important to include posts, where relevant, as the report
      feature does keep the posts even if the user / their server admin deletes
      the posts or suspends the user's account. So if a user has been posting
      and deleting those posts, we won't see it by looking at the timeline but
      the UI will keep them if you include them.
* Always include the context when you are prompted for Additional Comments,
  even if it is obvious. This can be as succinct as "spam".
    * If you are sending us a report for a server violation and the posted
      content is not in English, please supply the translation and relevant
      context. In many cases, online translation tools can only directly
      translate the words but not the commonly understood (or dogwhistled)
      meaning. If you run out of characters, please submit the report and tell
      us you have emailed us, and email us at [admin@hachyderm.io](mailto:admin@hachyderm.io).
    * If you are sending us a report with a short / one-word description, please make sure it
      correctly captures the situation. If the reported description does not align
      with what is included with the report, we will close the report.
    * If you are sending us a report of problematic content where the visuals
      may be traumatizing in and of themselves, you _can_ choose not to include
      the posts but please always include what we will see when we look
      at the reported user's account or the reported server. We have moderators
      opt-in to tasks like these when they appear.

 
What to know about the Additional Comments:

The most important limitation you should know is
that the Additional Comments field has a character limit of 1000
characters (as of this writing). If you need to supply more
context, or the translation takes more than 1000 characters,
please:

* File the report with what you can
* Make sure to leave enough space to tell us there is a
  supplementary email
* Email us at [admin@hachyderm.io](mailto:admin@hachyderm.io)

**_Please note: if we receive an empty report and cannot see a
clear cause, we will close the report without moderator action._**

#### Limitations of the Mastodon Admin Interface

When we receive a report, we cannot follow up with the reporting user to ask for
additional information using the admin tools.

How this impacts you:

If you are reporting an issue and do not include enough
information and/or a way for us to get in touch with you to
clarify, we might not be able to take the appropriate action.
So please do make sure to include posts as needed, comments and
context, and email us at [admin@hachyderm.io](mailto:admin@hachyderm.io)
as needed.

## How and When to use the GitHub Issue Tracker

The [Community's GitHub Issues](https://github.com/hachyderm/community/issues),
a.k.a. Issue Tracker, is for communiticating with the moderation
_and_ infrastructure teams, as needed. To create an issue:

1. Go to [github.com/hachyderm/community/issues](https://github.com/hachyderm/community/issues)
1. Click on "New Issue" in the upper right side.
1. Select one of the issue templates that applies to you / your situation
1. Enter the information needed on the Issue. Depending on the template, there
   may be some prompts for what information should be included.

The Community Issues can still be used to report domains, as you would do in the UI.
It can also be used to request emoji, report a service outage (you can also use
[omg.hachyderm.io](https://omg.hachyderm.io) for this),
request updates / changes to the docs, and so on. There are issue
templates for the most common issues that prompt users for the information
we need to respond to requests efficiently. Depending on whether the request / 
conversation is about moderation issue or a partial / full outage, a member
of the corresponding team or teams will respond.
