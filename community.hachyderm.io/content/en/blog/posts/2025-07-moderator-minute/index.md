---
date: 2025-07-05
title: "A Minute from the Moderators"
linkTitle: "July Moderator Minute"
description: |
  Back to moderator minutes, spam account sign up wave.
author: Quintessence ([@quintessence](https://hachyderm.io/@quintessence))
---

Hello Hachydermia!

It's been a while since we had one of these, and we thank you for your patience. We have more posts queued up on additional topics, but as promised we've been handling a sign up wave so we wanted to take time to explain what we're seeing and how we're working on it.

As always: processes grow over time, and moderation decisions are appealable. In cases like account applications, especially with regard to verifying identity, we won't typically accept an appeal via the Appeal button unless we explicitly request an appeal that way. When that happens, the email that we send you will explain how to appeal that type of decision. We'll get into appeals in a moment, but first we want to explain a concept called “inauthentic activity”.


## Inauthentic Activity

Inauthentic activity is a term that you may hear in moderation in a variety of contexts. To be clear about what we mean when using the term in this post:

> Inauthentic activity is any activity that intends to mislead.

It is important to understand this concept, because like all things inauthentic activity has a spectrum. The most extreme cases of inauthentic activity are activities like: harassment, stalking, and so forth. However, there are less extreme forms of inauthentic activity such as fake accounts which are created to post spamming links or text.


## Case in point: Nicole, Fediverse Chick

Many on the Fediverse have encountered inauthentic account creation already. A notable example of this type of activity involved a wave of nearly identical accounts across the Fediverse that is likely familiar to all: Nicole, the Fediverse Chick. These accounts typically shared the same display name (“Nicole”) and a nearly identical profile bio. "Nicole" accounts engaged in mass direct messaging, and often introduced themselves in a uniform, scripted way.

Though each account had a unique handle (evading simple filters), they functioned as a coordinated spam campaign. The accounts were not genuinely attempting to represent an individual named “Nicole”, they were created to distribute spam making them a clear case of inauthentic account creation. There are also numerous posts and analysis on the Fediverse regarding elements that indicated a potential targeted harassment campaign, compounding the nature of the activity.


## What Hachyderm is seeing

So what are we seeing right now? The primary form of inauthentic account creation attempts we're seeing on Hachyderm specifically are accounts that are created with the intent to post spam links and/or text. Most of the spam is what we'll loosely call "relatively benign". By that we mean they *mostly* do not appear to be attempts to phish, post traumatic or other forms of harmful content, and so forth.

While none of these types of spam accounts are new, the main change we're seeing now is that more and more of the account creators seem to be using automation to generate "plausible reasons to join". While there are more than a fair few that we suspect (or have enough text that we can confirm) are using AI text generation tools to "write a human sounding reason to join an instance", simple scripting can also accomplish the same end. This basically means that historically it was more straightforward to determine if an account was a "bot or not" because, candidly, most bots [prima facie](https://en.wikipedia.org/wiki/Prima_facie) looked like bots. Now that is no longer the case, so we're continuing to improve our processes to adapt to this new reality.


## How Hachyderm is currently handling applications 

Right now we’re trying to find the right balance between reasonable friction to reduce inauthentic activity, while still allowing a smooth onboarding experience for new Hachydermians. We know this will introduce more friction than was present in the past, but we’ll continue to re-evaluate our decisions as different inauthentic activity campaigns occur, and we welcome your feedback on ways we could make this easier. 

To help future Hachydermians and to provide better transparency, this post is to explain and set expectations on the process, its limitations, and how you can help make the process faster and smoother.


### How we're using the Mastodon tools

It's important to understand how the tooling works to then understand how pending applications can be actioned. Right now, it is not possible to directly message a pending account on Hachyderm via Mastodon’s platform tooling while the account application is still in a “pending” state. That means there are two ways to try to contact account applicants:

1. Attempt to contact the applicant via the email on the account application 
2. Still try to contact the applicant in-platform 

While there are situations where we would try to reach someone via email, we generally prefer to do so via Mastodon. This is doubly true for cases of identity verification. Because it's easy to create new email addresses—and many people use unique addresses for different services as a security measure—email alone isn't a reliable way to determine whether an account is inauthentic

That means that we try to find alternative ways to contact applicants where we can. There are two things we are doing:

* If an applicant says they are migrating from a different account or Fediverse instance, we message that account to verify their identity. We will only do this by sending a DM ("mentions-only message") from the official hachyderm@hachyderm.io account.
* If we need to contact the account holder for a different reason, we may need to “Approve” the account to get it out of “Pending” state, and then take a moderation action, such as a [”Freeze” or “Suspend”](https://community.hachyderm.io/docs/moderation/actions-and-appeals/).

This process can feel confusing—particularly when an approval is quickly followed by a freeze or suspension. We handle it this way because suspensions and freezes can be appealed and reversed, whereas application rejections are final and can't be undone. Until we have better processes or tools to manage this more cleanly, we’ll continue approving and then freezing / suspending suspected inauthentic accounts to leave room for correction if we've made an error.


## How applicants and Hachydermians can help


### For applicants

Writing at least a sentence makes it easier to determine if an account is a bot or not. You don't need to write an essay, but one word reasons don't really help the "bot or not" assessment. If a Hachydermian has offered to vouch for you, please include their handle as well.

If you're moving instances, or are otherwise applying and referencing an existing Fediverse account either on Hachyderm or elsewhere, watch for a DM from our official [hachyderm@hachyderm.io](https://hachyderm.io/@hachyderm) account to verify your application. 

This information is helpful even if you're not migrating accounts and are planning to either have two separate accounts or if you plan to eventually delete one. In either case, we can refer to / work with your existing account to do the necessary checks to approve your Hachyderm account application.

This is doubly true for entity accounts (projects, community based conferences, etc.) as we want to make sure that people are not creating third party accounts claiming to be managed by someone who isn't managing them.

If you miss a DM from us or have otherwise haven’t heard from us in more than a few days, don't worry! We may put your account temporarily into an "approve-suspend" state until we hear back from you. In this case, the email you receive will include what to do next.

If you believe that we've made a mistake, just let us know by sending us an email at [admin@hachyderm.io](mailto:admin@hachyderm.io). If you have other issues that you want to get a hold of, please read the “[Reporting Issues and Communicating with Moderators](https://community.hachyderm.io/docs/moderation/reporting/)” page.


### For Hachydermians

If you know that you've recommended that someone joins our instance specifically, and you know them well enough to vouch for them, please let them know to include your Hachyderm handle as part of their application. When we receive their application we'll reach out to you also to confirm that you did in-fact vouch for them. Please know that we do not share any 1:1 communications outside of the moderation team, so if you cannot vouch for them and/or have other information you need to provide, it will be kept in confidence. If you would like to report any other issues or if you need to get a hold of the moderation team, please review the “[Reporting Issues and Communicating with Moderators](https://community.hachyderm.io/docs/moderation/reporting/)” page.
