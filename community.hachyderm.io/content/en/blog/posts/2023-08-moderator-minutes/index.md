---
date: 2023-08-13
title: "A Minute from the Moderators"
linkTitle: "August Moderator Minute"
description: |
  Investigating the DarkFedi and Potecting Our Users
author: Arjun ([@arbdev](https://hachyderm.io/@arbdev))
---

In today's Moderator Minutes, we will be discussing the DarkFedi and what Hachyderm is doing to protect its users. The DarkFedi is a part of the federated social media network (FediVerse) that is known for it's user base that focuses on topics that are typically illegal, taboo, controversial, or outside the mainstream, including but not limited to, CSAM, racism, violence, etc.

- [What's the DarkFedi?](#whats-the-darkfedi)
- [What is Hachyderm doing to protect its users?](#what-is-hachyderm-doing-to-protect-its-users)
  - [How do we learn about potential DarkFedi content?](#how-do-we-learn-about-potential-darkfedi-content)
  - [What do we do when we learn about potential DarkFedi content?](#what-do-we-do-when-we-learn-about-potential-darkfedi-content)
  - [How we vet the actual posts](#how-we-vet-the-actual-posts)
- [What can a user do to protect themselves?](#what-can-a-user-do-to-protect-themselves)


## What's the DarkFedi?
The DarkFedi is often associated with alternative or underground communities, embracing freedom of expression and resisting censorship. Some characteristics of the DarkFedi include:

- Anonymity: Users on the DarkFedi can often choose to remain anonymous or use pseudonyms, allowing for greater privacy and protection.
- Content diversity: The DarkFedi allows for a wide range of content, including discussions around sensitive or controversial topics, alternative lifestyles, and explicit or adult content.
- Lack of moderation: While some instances on the DarkFedi have moderation policies in place, there are also instances that have little to no moderation, allowing for a more unfiltered and uncensored experience.

It's important to note that while the DarkFedi provides a platform for some forms of free expression, it may also include content that some individuals may find offensive, illegal, or unethical. Hachyderm works to preemptively review and moderate content that is illegal or violates our rules, which predominately comes from the DarkFedi.

## What is Hachyderm doing to protect its users?
Hachyderm is committed to providing a safe and secure platform for all of our users. We have a dedicated team of moderators who review and remove reported content that is illegal or violates our rules. In addition, we are constantly monitoring the DarkFedi and other parts of the federated social media network to ensure that our users are not exposed to any illegal or harmful content.

### How do we learn about potential DarkFedi content?
There are a few ways that we learn about potential DarkFedi content:
- Reports from our users, other instances, or the general public
- Conversations that are shared on the Fediverse and is visible to our moderators (ie, public posts, public conversations, or tools like [The Bad Space](https://thebad.space/))
- Preemptive monitoring of the DarkFedi and other parts of the Fediverse through user associations, tags, and other identifiers

### What do we do when we learn about potential DarkFedi content?
When we learn about potential DarkFedi content, we take the following steps:
- Check the domain in our admin tools for size and any prior reports
- Check the /public firehose, if there is one, for examples of extremist content
- Check a few sample users from the instance to see if their current posts content examples of extremist content
  - This is especially necessary if there is not a public firehose/timeline
- If we need to de-federate with the domain, we need to gather relevant censored information prior to de-federating, otherwise that information is lost (deleted by Mastodon almost immediately)
- Review the following and followers of predominate accounts on the instance to see if there are any other instances that we need to investigate

### How we vet the actual posts
- When there is a public firehose, it should be pretty easy to see if there is problematic content appearing regularly.
- When there is not a public firehose, we need to check a few sample users from the instance to see if their current posts content examples of extremist content
  - When we vet the posts of individual users, we will likely need to review older post to see if They're A Problem Or Not as not all users are as online as others and problematic behavior doesn't happen all the time. For example / basically there can be accounts with a mix of cat memes and racist memes.
- We do not review the entire history of an user or instance as this is not scalable.
- In addition, we only review enough content to determine the pattern for the account in order to reduce exposure to potentially harmful content.
- However, we do evaluate beyond the content of the posts, including the following:
  - The user's bio, profile picture, display name, associated users, and associated instances
  - The implications of the user's posts

## What can a user do to protect themselves?
- Be aware of the content you are viewing and sharing on the Fediverse. If you come across any content that is illegal or violates our rules, please report it to our moderators immediately.
- Block specific tags, instances, or users that you know are harmful or offensive to you.