---
title: "Content Warnings"
linkTitle: "Content Warnings"
weight: 40
description: >
  Describes what the content warning feature is and how it operates.
---

{{% pageinfo %}}
This page documents features and processes maintained by Mastodon. For
issues related to these features and/or processes, please reach out to the Mastodon team
directly on [the Mastodon project's GitHub](https://github.com/mastodon/mastodon).

For issues with this doc page itself, please reach out to us on
[Hachyderm's Community Issue tracker](https://github.com/hachyderm/community/issues).
{{% /pageinfo %}}

## What are content warnings?

Content warnings are a feature that allows you to
obscure your content in such a way that it is hidden by default in other
users' timelines. Instead, only the text of the content warning is
displayed. To put it another way, if you were to put a content warning on
one of your posts that read "descriptions of war violence" while discussing
current or past wars, users would only see that description and could then
choose to click through the content warning to view the content (or not).

## How to apply a content warning

In order to apply a content warning use the "CW" in the post field:

<img src="mastodon-content-warning-button.png" 
     width="400"
     alt="Screenshot of the post field with the CW circled and with
          an arrow pointing to it" />

An example post with a content warning on the text and image looks like
this:

<img src="mastodon-content-warning.png"
     alt="Screenshot of a post with content warning 'Politics (CO)' and the
          blurred out content labeled 'Sensitive Content'"
     width="400"/>

## Threads with a content warning

Whenever someone replies to a post with a content warning, by default their
response will carry the same content warning. Here is an example:

<img src="mastodon-content-warning-thread.png"
      alt="Screenshot of a thread with an example content warning,
           that reads Example Content Warning, showing that when a user
           replies that content warning is pre-populated" />

This is the default due to the nature of the content warning: if the top-most
post of a thread needs a content warning due to what's being shown or discussed,
then the rest of that thread _probably_ needs the same content warning. This is
true both for when you respond to your own posts or when other users respond to
your posts.

When you reply to a post with a content warning you can manually disable and
delete the content warning, but please do so with care. When you remove the content
warning from your post all replies _to you_ will _also_ no longer be behind
a content warning by default, even if they should be.

## When are content warnings used

Content warnings are generally used to either hide spoilers or to provide
a buffer when it is psychologically safer to choose to opt in to a conversation
as opposed to being opted in by default (seeing it in a timeline). For more
information on the nuance for how and when to use content warnings, please
take a look at our [doc on how to use content warnings](/docs/hachyderm/content-warnings/).
