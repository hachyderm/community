---
title: "Reporting Issues and Communicating with Moderators"
linkTitle: "Reporting and Communication"
weight: 4
description: >
  How to report issues and interact with the moderation team.
---

There are two main ways to report issues to the moderation team:
in the GitHub Community Issue tracker and in the Mastodon UI
itself. In general, the Mastodon UI (i.e. the "report" feature on
Hachyderm.io) is used for reporting specific posts, users, and
domains. The GitHub Community Issue tracker is for other types of
reports as well as raising other questions and conversations with
the Hachyderm Moderation Team.

There are three ways to correspond with the Hachyderm Moderation
team:

* [Email](#how-and-when-to-use-email)
* [The Mastodon UI](#how-and-when-to-use-the-mastodon-ui)
* The Issue Tracker on the Community Repo

## How and When to use Email

The moderation team should, in general, only be contacted via
email to:

* Supplement a report in the Mastodon UI
* Provide a report or other communication that cannot be in a
public forum, like the GitHub Issue tracker, and cannot be
submitted via the Mastodon UI

In short: please prioritize using the Mastodon UI and/or GitHub
issues as often as possible. That said, if you would need to reach
out to the admin team for either of the above situations, please
use [admin@hachyderm.io](mailto:admin@hachyderm.io).

## How and When to use the Mastodon UI

The Mastodon UI, i.e. what you see when you're using Hachyderm.io
or your home Mastodon instance of choice, should generally be used
for reporting issues that can be reported via reporting individual
posts. This typically is used for:

* Reporting individual posts but not the user overall
* Reporting a user via their posts
* Reporting a domain via the posts of their users

### How to report

1. Click on the hamburger menu below the post and select
"report"<br /> 
<img src="report-post-drop-down-menu.png"
     alt="Example post with the text This is a blob fox
     appreciation post and three blob fox emoji. The UI menu is
     expanded to show copy link to post, embed, mention the user,
     mute the user, block the user, or report the user. The
     following steps are for reporting the user."
     width="400" />
1. Select why you're reporting.<br />
<img src="report-post-why-part1.png"
     alt="Dialog box with four options to select for reporting a
     user. The options are I don't like it, It's spam, It violates
     server rules, and It's something else. In the example, It
     violates server rules is selected."
     width="400" />
1. If you selected Server Rules for the reason, as we did in this
   example, then you'll be asked to select which and can select
   more than one:<br />
<img src="report-post-why-part2.png"
     alt="Additonal dialog box to allow user to select which rules
     are violated. All the server rules, including Don't be a
     dick, No hacking, No violence, etc. are shown. You can select
     one or more server rules as being violated. Here only Don't
     be a dick is selected."
     width="400" />
1. Please select any and all additional posts to include in the
report<br />
<img src="report-post-why-part3.png"
     alt="Dialog that allows you to select other user posts that
     may be related to the report. The posts shown are not all in
     one thread, but all of the user's recent posts. In this case,
     an additional two posts about a form announcement and a
     response window are shown. Only the Blob Fox Appreciation
     post is selected."
     width="400" />
1. Please include all relevant context to help us
   process the report:<br />
<img src="report-post-why-part4-submit.png"
     alt="Additional Comments dialog box, with a limit of 1000
     characters, to allow users to supply additional information
     with their report."
     width="400" />
1. You can **optionally** choose to unfollow, mute, or block
   the user before you click "Done".<br />
<img src="report-post-why-part5-done.png"
      alt="You can optionally unfollow, mute, or block the user you are
      reporting before selecting Done. You do not need to do any of
      these actions for the report to be submitted."
      width="400" />

The Additional Comments step is very important. To help us process reports
efficiently there should _always_ be additional context in the
Additional Comments field - the more the better. This should be done
**_even if the report seems self explanatory_**. In the case of
reports of posts, users, and domains that are in languages other
than English, we will need an English translation supplied.

The most important limitation you should know at this stage is
that the Additional Comments field has a character limit of 1000
characters (as of this writing). If you need to supply more
context, or the translation takes more than 1000 characters,
please:

* File the report with what you can
* Make sure to leave enough space to tell us there is a
  supplementary email
* Email us at [admin@hachyderm.io](mailto:admin@hachyderm.io)

### What a Filed Report Looks Like

For an example, I had Björn's user create a report against my Blob
Fox Appreciation Post that I used for the screenshots above. When
a member of the moderation team reviews the report, it looks like
this:

<img src="filed-report-overview.png"
     alt="Zoomed out view of what the report looks like for a
     Mastodon admin. The text is too small to read, but the
     sections show the user stats at top, report reason in the
     middle, any comments provided by the user filing the report,
     and then a section for moderator actions. These are described
     in detail below."
     width="400" />

Since that is a very zoomed out view, let's look at each of the
sections. At the top is the same user information you'd see if you
navigated to the top of a user's profile page:

<img src="filed-report-top.png"
     alt="This is the top of the same report. The user is user
     quintessence with 1.01K posts, 3.61K followers, and 115
     following. The first line of her bio is visible, as is her
     header and avatar. The report date and time as well as the
     reporting user, Björn, are visible. The Category of the
     report is shown as violates server rules - Don't be a dick."
     width="400" />

This section also shows the moderator team why the report was
filed, in this case the "Don't Be A Dick" rule is selected.

Underneath that is the comment that the user supplied when they
filed the report as well as all the posts they selected to include
with it. If the user is a Hachydermian, the user name is
supplied as you can see here. If the user is off our server, only
the source server is supplied.

<img src="filed-report-user-comment.png"
     alt="This section shows the additional information provided
     by the user. In this case, only the text This is what was in
     the additional comments field for the reporting user comment
     as well as the post that was included in the report."
     width="400" />

At the bottom is the section where moderators can leave comments
and choose what action to take:

<img src="filed-report-mod-comment-and-action.png"
     alt="Moderator actions are shown here as Mark As Resolved -
     no action, Delete posts, Limit user, Suspend User, and
     Custom. There is also an additional field for moderator
     comments."
     width="400" />

Moderators can choose to close the issue with only an explaining
comment, or to take one of the shown actions and close the issue.
For visibility the moderation actions are:

1. Mark as Resolved (No moderator action)
1. Delete posts (Moderator resolves by deleting the offending
post(s))
1. Limit (Formerly known as "silence". The user can still
participate but they will not show in Local or Federated feeds.)
1. Warn (Moderators send a note through the interface to the
reported user. Note this option is not visible on the screenshot.)
1. Suspend (Also known as "ban". If the user is a Hachydermian
then their account is removed from our server. If they are on a
different server that user is banned from interacting with our
server.)

#### Who can see moderation reports

All moderators can see all reports **_except_** the following:

* A moderator cannot see any reports filed against them, but
  others on the moderation team can to take action. (Note: I
  needed to have a different member of the team take screenshots
  of the above for me to write this article.)
* A moderator cannot see any report that they have filed against a
  user. This means that a single moderator cannot file and decide
  on a single report. That report must be seen and acted on by
  another moderator.

Regular users do _not_ have access to moderator reports.

#### Not all moderation action is visible

Of the above actions, the only moderation actions that are visible
are if a moderator deletes a post or suspends an account. When an
issue is closed without action or when a user is warned or
limited, the action is not visible to the reporting user or other
users.

#### Limitations of the Mastodon Admin Interface

When we receive a report in the admin tools, there are two main
drawbacks:

* We cannot follow up with the reporting user to ask for
  additional information
* We cannot follow up with the reported user, even if they file an
  appeal

How this impacts you:

* If you are reporting an issue and do not include enough
  information and/or a way for us to get in touch with you to
  clarify, we might not be able to take the appropriate action.
* If you are appealing a moderation decision and do not include
  enough information for us to make a decision and a way to
  contact you, we might not have enough information to reverse the
  decision and no way to request more information from you.

**_Please note: if we receive an empty report and cannot see a
clear cause, we will close the report without moderator action._**

### Important: What we need when you file a report

We wanted to put this section intentionally below the limitations
of the interface, so that the context of what we're asking for
here is clear. If you are filing an issue that needs moderator
input or if you are filing an appeal that may need additional
discussion, please provide your preferred email so we can reach
out to you for clarifications as needed.

## How and When to use the GitHub Issue Tracker

TBD: Will be in next commit.

## Expectations for Interaction with the Moderation Team

TBD: Will be in next commit.
