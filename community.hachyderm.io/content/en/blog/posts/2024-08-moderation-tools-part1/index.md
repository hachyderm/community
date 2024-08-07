---
date: 2024-08-06
title: "Hachyderm's Introduction to Mastodon Moderation: Part 1"
linkTitle: "Intro to Moderation Part 1"
description: |
  The first post in a series about Mastodon moderation tooling.
  This post focuses on context for the upcoming posts.
author: Hachyderm Moderation ([@Hachyderm](https://hachyderm.io/@Hachyderm))
---

Hello Hachydermia! There has been recent extensive interest in Mastodon's moderation tooling and moderation in the Fediverse, in general. As part of that conversation, it became apparent that the Mastodon admin tools aren't well known or understood. In the past, we've only provided a [light amount of "Mastodon docs" type of documentation](https://community.hachyderm.io/docs/mastodon/), for a few reasons:

* We didn't want to host Mastodon project documentation, as that belongs with the Mastodon project.
* Due to software release cycles, documentation can fall out of date which would add to the burden of maintaining the documentation for software we don't control (as we are not Mastodon maintainers).
* Since we are not Mastodon maintainers, it could also cause confusion with what the appropriate "source of truth" is if our documentation differs from the Mastodon project documentation.

For reference, Mastodon's documentation is here:

[https://docs.joinmastodon.org/](https://docs.joinmastodon.org/)

We also, truthfully, did not expect as much interest in the high level detail of How Stuff Works as there appears to be. All of that said: there is an interest, there is confusion, so we're happy to help contribute to the corpus of information that makes being on the Fediverse better.

## Expectation setting

Some expectations for the blog posts (and any docs):

* To state it again, none of us are Mastodon maintainers.
* All of these blog posts will likely be long.
* These blog posts and any docs _are_ Mastodon specific and Mastodon is not the only tool in the Fediverse.
* As such, there is a variety of "what moderation tools are even available" depending on what type of Fediverse software is in use on a specific instance. We won't be covering the broader Fediverse, only Mastodon.
* We will be showcasing the version of Mastodon that we are currently running, which is v4.2.10.
* We are not running any forks of Mastodon, such as [Glitch](https://glitch-soc.github.io/docs/) or [Hometown](https://github.com/hometown-fork/hometown), so we will not be covering / discussing them or their peers.
* These blog posts neither praises nor criticisms of Mastodon or instances running it; they are simply providing information to help us all meet the situation where it's at.
* There may be mention of third party tools that we (Hachyderm) use such as email, GitHub, etc. Other instances may use different, but similar, tools in similar contexts. We're not suggesting these as "one size fits all", we're only providing information.
* Due to the labor involved, each post will likely take a couple of weeks. We, like many instances on the Fediverse, are volunteer run.

## Some context: a common paradigm we see

Before we focus heavily on "how do the moderation tools work", we wanted to acknowledge and explain a common pattern we see a _lot_ on the Fediverse:

> Person A: YOU HAVE NO IDEA THE HARASSMENT I RECEIVE!<br />
> Person B: Oh no! Have you tried changing instances?<br />
> Person C: OMG is your instance not moderated?<br />
> Person D: I don't see it? What are you even talking about?<br />
> Person E: Are you reporting these to your mods? People can't fix what they don't see!<br />
> Person F: Are you reporting these to other mods? People can't fix what they don't see!

Intentions behind Persons B-E aside, here are a few "did you knows":

**Issues with Person B's Suggestion**

* Did you know that when you migrate instances you lose your posting history?
* Did you know that migrating instances is not as simple as "create account on new instance, point old account to new account"? You need to export and then import data to keep your: followers, following, filters, and so on?

**Issues with Person C's Suggestion**

* Do you know how the moderation tools work (highly relevant to upcoming blog posts)?
* Have you thought about how moderators are informed of abusive behavior? For example, does the target of the harassment need to be exposed to the harassment, and thus the harm done, before it is reported, regardless of outcome?
* Regarding the previous, have you considered that some communities may have a higher risk of impact than others when it comes to moderation?
* Is the issue they're experiencing systemic and omnipresent? If so, while moderation _will help_ it cannot stop what is happening by itself.

**Issues with Person D's Suggestion**

* Are you a marginalized person? If not, then you're not a target of what Person A is experiencing.
* Are you a marginalized person, but not the same as Person A? i.e. There are some types of hate that target specific demographics. If that's not you, then you're not a target of what Person A is experiencing.
* Did you know that depending on what your instance is or is not moderating on a server level influences what you see? Therefore if one or more sources that are targeting Person A are moderated on Person D's server, then no one on Person D's server will see those posts from their home instance. They'd need to log out to see them. (Moderator note: you can do this as an exercise in empathy, but _please proceed with caution_. Reply guys are not the only situations that are moderated on instances: instances also moderate violence, jump scare gore, CSAM, slurs, and so forth.)
* Did you know that you can choose to limit who can see your reply to a specific post to "followers only"? Did you connect that this same feature can be used to harass so that the _only_ people who can see the harassment are the harasser and the target?

**Issues with Person E's & F's Suggestions**

* If a user needs to report their own harm, that's harm experienced. ([Our blog post with this topic](https://community.hachyderm.io/blog/2023/05/08/a-minute-from-the-moderators/#harm-prevention-and-mitigation-on-large-instance).) So a report may prevent future harm from that same source, but reporting in and of itself won't stop the next time.
* When you send reports, there are options on who to send it to (more on this later). If you see, for example, a slur do you, as in you personally the ally who Wants To Do Good, know if that instance will moderate that? Do you know if the moderators for that instance use reports as vectors of harassment, screenshotting their report queues for their followers? With all this in mind: where do you choose to forward the report? (We'll be revisiting this one again when we discuss reporting.)
* If you, Person E or F, are not on Person A's instance, do you know how to send the report to _their_ moderators either instead of or in addition to 1 ) your own moderators and 2 ) the offenders moderators?

## Why this is important

**Issues with All the Suggestions, Broadly**

They assume that the problem Person A is experiencing is easy to solve. If it was easy to solve, then a better assumption would be that Person A would've done those things to protect themselves already.

**How does this apply to moderation**

Visibility into how the moderation tools work will absolutely help people understand what actions are even possible. That said, it's important to understand that good behavior, or "being a good citizen of the Fediverse", is about more than what the tools are or are not doing. It's about individual behaviors as well.

## Shit, is it all hopeless? How do I/we help?

No, it's not hopeless! We need to work together. Understanding what tools are available is only part of the solution. Our shared humanity, communication, empathy, and respect are required to do the rest.

**Helping the Fediverse**

* If you're reading something that "you can solve" in 30 seconds or less, pause to see if there's any information as to why it hasn't been solved in 30 seconds or less already. This will likely require some searching.
* Whenever you have an idea to improve Fediverse tooling, look for existing solutions first. There are many groups working on Fediverse tools, and it's better for the community to focus our energy and support on these existing projects rather than develop yet another one. Supporting projects run by marginalized groups is also important, as they are the ones that are on the receiving end of tooling abuse.
* Prioritizing existing projects also increases the number of instances that are using whatever that software is - more collective safety - than would be otherwise possible if you have it as your pet project.

**Trauma informed communication**

* Don't feel like you need to fix everything. A common response to bearing witness to another's trauma is to try and fix it. We don't want others to suffer. That said, you may not be offering what the other person or group is clearly stating they need. If they need you to listen, and you choose to act but not listen, then you have both not supported them in their trauma and violated a boundary. ([Our docs page about mental health covers boundaries](https://community.hachyderm.io/docs/hachyderm/mental-health/#create-and-maintain-interpersonal-boundaries).)
* Don't offer solutions you don't have, especially things that fall out of your lived experience. Listen, learn.
* If you're not sure, ask: does the person need someone to listen,
* someone to help, or some space? ([This 30 second video can help](https://www.facebook.com/optionbcommunity/videos/ill-give-you-3-options/377179557326498/). Apologies for the Facebook link, but that's where the [OptionB organization](https://optionb.org/about) is.)

**Clarifying your own communication**

* Ask direct questions. If what you are looking for is a specific answer, like an outcome of a specific situation, asking very broad questions about policies in general or tooling in general will get you answers to what you asked for but will not answer the question you actually have.
* Assert boundaries when you need boundaries, request actions when you need actions. If you ask someone to leave a conversation when what you want is an apology, then when they (hopefully) respect your boundary you won't have what you were really looking for.

## What will be in our next post

In our next post we'll be covering the report feature in Mastodon. We'll specifically show:

* What it looks like when you report an issue
* What moderators see, and the difference between local and remote reports
* The different actions that moderators can take, which can vary between local users, remote users, and remote instances. (Yes, moderators can moderate individual remote users.)
* What communications come from the platform (or not) when moderation actions are taken.

In order to showcase the above, we're going to generate faux reports using our main and test instances. As always, we look forward to your questions and feedback.

