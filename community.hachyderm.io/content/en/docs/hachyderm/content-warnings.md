---
title: "Content Warnings"
linkTitle: "Content Warnings"
weight: 40
description: >
  How to use content warnings on Hachyderm.
---

This document describes how to use content warnings and how they are
moderated. To understand the feature itself, please look
at [our content warning feature doc](/docs/mastodon/user/content-warnings/).
In this document:

- [What is a content warning?](#what-is-a-content-warning)
- [When to use content warnings](#when-to-use-content-warnings)
- [Common examples of content warnings](#common-examples-of-content-warnings)
- [How to structure a good content warning](#how-to-structure-a-good-content-warning)
  - ["Spoilers, Sweetie"](#spoilers-sweetie)
  - [Protecting Psychological Safety](#protecting-psychological-safety)
      - [Composing content warnings for psychological safety](#composing-content-warnings-for-psychological-safety)
      - [Nuance and growth](#nuance-and-growth)
- [What Do the Moderators Enforce](#what-do-the-moderators-enforce)

## What is a content warning?

Content warnings are the text that displays first instead of the text and/or
media that you have included in your post. Since the goal of the content warning
is to put a buffer between a passerby and your underlying content, it is important
to have something that is descriptive enough to be helpful for someone to
decide if they should click through the content warning or not.

## When to use content warnings

The two main use cases for content warnings:

* A content warning should be used to protect the psychological safety of
  others in a responsible way
* Spoilers

A central concept to content warnings is "opt-in". By using a content
warning, you are creating a situation where other users are opted-out
of the detail of your post by default. They must _consent_ to opt-in.
In an ideal scenario, other users are able to make an informed decision
to opt-in, i.e. _informed consent_.

## Common examples of content warnings

There are a few situations where content warnings are commonly used on the
Fediverse (these are not exclusive to Hachyderm):

1. Images of faces with eye contact
1. Images of food and alcohol, even if they are not being consumed in excess
   * Though they will also be behind a content warning if they are
1. Text or media describing or showcasing violence
   * This is common when discussing news around war violence or shootings
   * Also common when sharing stories of personal trauma
1. NSFW content
   * Please see our [Sexual Content Policy](/docs/nsfw-policy/) for information
     that is specific to Hachyderm.
1. Fandom-specific spoilers for various forms of entertainment like TV shows, movies, and books.

Content warnings feature heavily in [our Accessible Posting doc](../accessible-posts/),
especially in the [Interpretive Accessibility sections](../accessible-posts/#interpretive).

## How to structure a good content warning

The goal of a content warning is to communicate what another person needs
to know, so they can determine if clicking through the warning is something
they want to do or should be doing, especially if the content is describing
a situation that may be a traumatic, lived, experience or news event. The
question you should ask yourself when you have written your content warning is:

> If I was a user that **_did not_** want to engage with this post, would
> I know to avoid this post with the information provided?

The follow-up question you then need to ask is:

> If I was a user that **_did not_** want to engage with this post, but did
> by mistake and/or an unclear content warning, what is the **_impact_**?

##### Quick example <!-- omit from toc -->

Before going further, take a look at these two options to be used as a
content warning for the same post about the first episode of the most recent
season of The Mandalorian:

1. "Spoilers"
1. "Spoilers for the New Season of The Mandalorian"

Which of these two content warnings let you know if you want to interact with this
post from the prospective of:

1. A non-Star Wars fan
2. A fan of The Mandalorian who _does not_ care about spoilers
3. A fan of The Mandalorian who _does_ care about spoilers

Also: what is the _impact_ to each of these groups if they click through your content
warning and see content they did not want to see?

Remember: The goal is for the content warning text to be descriptive enough that
all of these prospective audiences can decide to opt-in or opt-out. The impact in
this example is intentionally low, someone will see spoilers, but there are
situations where the impact will be higher.

### "Spoilers, Sweetie"

(Quote attributed to River Song of Doctor Who fame.)

Preventing the spread of spoilers is an excellent "off label" use of the
content warning feature. Spoilers most commonly refers to current books,
television, and movies. One quick, easy example would be using a content
warning when discussing Game of Thrones when it was actively airing.
Another would be discussing the results of a football / soccer match that
people maybe haven't been able to catch up on yet. Different fandoms have
different expectations around what should be a protected spoiler or not,
so the general rule of thumb here is to treat other fans the way you'd
want to be treated.

As for moderation, we do not moderate spoiler tags. That said, and as always,
please [Don't Be A Dick](/docs/rule-explainer/).

### Protecting Psychological Safety

This topic is covered second because it requires a lot of explanation
for the implementation details. In fact, protecting psychological safety
is a life-long journey and involves understanding others unlike yourself.
The short version of when to use this content warning:

> You should use a content warning whenever the psychologically safest
option is to opt into a conversation rather than to default into that
conversation.

Let's start with a hopefully clear example. If you want to share news
about human rights abuses around the world, you will likely
be sharing links and media that shows the reality of those situations.
This could include a lot of violent and traumatic video and images. Due to
the need to raise awareness, you may want to make sure that people can
see the content to avoid turning a blind eye.

That said: you cannot control the reach of your information.
This means if you do not use a content warning, not only will the people
you wish would pay attention potentially see it (or not, depending on how
their home instance federates), but you could also be exposing victims
of that same violence to content that triggers their trauma. So what's the
psychologically safest option? To protect the most vulnerable, in this case
the people with trauma, and that means use a content warning. The post will
still have the same reach, but it allows people to opt into that conversation.
In these cases it is to your benefit to use clear content warnings,
e.g. "article about the war in Ukraine, includes
images of physical violence in the war zone". A content warning that is clear
like this serves the dual purpose of labeling the topic of the post
while also explaining why it is behind a content warning.

Similar cases to the above would be any posts that include text
descriptions of, or images and/or video of, violent actions. To be clear:
our definition of violence includes physical, psychological, or sexual
violence. Animal abuse _also_ counts as violence.
(For more clarification on the various rules, like
"No violence", please see [our Rule Explainer](/docs/rule-explainer/).)

##### Composing content warnings for psychological safety

Being conscientious about composing a content warning that is intended to
preserve the psychological safety of others is important. The impact
is significantly higher than if someone sees a spoiler before they have a chance to
experience the "unspoiled" content.

When you are composing this type of content warning, ask yourself two
questions:

1. Why am I putting this behind a content warning?
1. What differs between this and other posts about this topic that
   I would _not_ put behind a content warning?

The answer to your first question will likely be short. "It's about war",
"it's about yet another shooting", "domestic violence", "eating disorders",
and so forth.

The answer to the _second_ question is what will provide the nuance.
In the example near the top of the post, it is the difference between "it's
a spoiler" and "it's about the latest episode of The Mandalorian". For
psychological safety, you might find yourself providing answers like:

* 1 ) It's about the war in Ukraine<br />
  2 ) It shows images of people in the aftermath of an explosion.
  * Example content warning text:<br />
    "Ukraine War - images and video of bomb injuries and death"
* 1 ) It's about another shooting in the US<br />
  2 ) It was at a school and children are scared and crying in the
      images / video in the news report.
  * Example content warning text:<br />
    "School Shooting - images / video of traumatized children but no injuries shown"

Asking the questions in this way allows you to supply the broad topic
_as well as_ describe the nuance that informed your decision to put the
post behind a content warning, especially if you wouldn't necessarily
do so for the broad topic area by itself.

##### Nuance and growth

Areas that might take more learning and growth to understand and adopt
are normally those that involve understanding intersectionality of users
on the platform. For example, you may see people use content warnings on
images with faces (especially with eye contact) or over food. With these
specific examples, using a content warning for faces and eye contact is to
help neurodiverse users on the platform who struggle with these and have
strong adverse reactions to it, and for the latter it can be to help those
with eating disorders or who are recovering. (Or similar for images of
alcohol for users who struggle / are recovering from alcohol addiction.)

For taking an active part in keeping Hachyderm a psychologically safe
place to be, it is important to do the work of understanding others
and apply that knowledge to how you interact with each other. There is
a lot to be said here, and it would exceed this document's scope, but a good place
to start is learning about anti-racism, accessibility, and anti-ableism.

## What Do the Moderators Enforce

Succinctly:

* Moderators will not take moderation action against spoilers, but
  it really is in poor form to openly share spoilers.
* Moderators will protect the psychological safety of users and prioritize
  the most vulnerable.
* Moderators will not, in general, take moderator action due to content warnings (or their lack).
  * To rephrase: moderators will _request_ and _recommend_ effective ways to use content
    warnings as opposed to _requiring_ them.
  * Any exceptions to this are called out on a case-by-case basis.
* Using a content warning as a workaround is not actually a workaround.
  * This means that rule violations are not less severe or otherwise
    mitigated by putting the offending content behind a content warning.
