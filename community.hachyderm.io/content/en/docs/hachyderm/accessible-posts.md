---
title: "Accessible Posting"
linkTitle: "Accessible Posting"
weight: 40
description: >
  Introduction to posting accessibly for new users.
---

FIXME - all the following content and possibly description.<br />
FIXME - we lose in the weeds "what to _DO_" in each case. Content warning vs alt text, etc.

## How to create accessible posts <!-- omit from toc -->

This doc page is meant to server as a place to start learning how to
post accessibily. This means it is not all inclusive, and that you
should continue your learning and growth after and beyond reading this
post. There is a lot to say here.

If you are looking for the short version and our asks, we
recommend reading the "What do we mean when we talk about accessibility"
and "Summary" sections, the latter of which contains our requests of
the community.

- [What do we mean when we talk about accessibility?](#what-do-we-mean-when-we-talk-about-accessibility)
  - [Interactions on the internet](#interactions-on-the-internet)
  - [Mastodon and Hachyderm](#mastodon-and-hachyderm)
- [Navigating the complexity](#navigating-the-complexity)
  - [Sensory](#sensory)
    - [Visual](#visual)
    - [Audio](#audio)
    - [Noise](#noise)
  - [Interpretive](#interpretive)
    - [Neurodiverse](#neurodiverse)
    - [Medical](#medical)
    - [Traumas and phobias](#traumas-and-phobias)
    - [Language accessibility and ease of translation](#language-accessibility-and-ease-of-translation)
  - [Economic](#economic)
- [Summary](#summary)


## What do we mean when we talk about accessibility?

Accessibility means that as many people as possible can
access your content if they choose to. Accessibility does not mean
that you cannot otherwise _intentionally_ gate your content,
for example via a [content warning](../content-warnings/). Rather,
accesssibility refers to the many ways that people typically create
_unintentional_ gates around their content.


### Interactions on the internet

Breaking down the different ways that we send, receive, and interpret
content on the internet can help when building an internal framework
for "what is accessible".

When _receiving_ content on the internet, that content is typically:

* Visual<br />
  The text on this page, static or animated images, video
* Auditory<br />
  Non-visual audio content like podcasts, or audio content with visuals like a video.
* Economic<br />
  Content that requires individual purchase or subscription to access.

When _sending_ content on the internet, the content is typically:

* Visual<br />
  Same as the above, but something we are sending rather than receiving.
* Auditory<br />
  Same as the above, but something we are sending rather than receiving.
* Tactile<br />
  Typically how we interact with visual content by "clicking here" or otherwise
  interacting with the content we are receiving.<br />
  FIXME - is this sending or receiving or both?

When _interpreting_ content on the internet, we are using:

* Our available senses
* Our neurodiversity
* Our lived experiences, including but not limited to our socialization and culture
* Our moral compasses and ethical alignments
* Our primary language(s), spoken and signed
* And so on.

Generating _accessible content_ is the combinatorics problem of the above. Most commonly,
accessibiliy is implemented by creating a "sensory backup" of the primary delivery of the
content. For example, if the content is audio it will have a (visual) transcript. If the
content is visual, it will have descriptive text that can be auditorily read. And so on.

The interpretation aspect content is where "sensory backups" alone fall short. If
someone is a trauma survivor, having a "sensory backup" of the content does not
solve the particular difficulty they are having. If someone is having sensory overwhelm,
pivoting to a different sense _may_ solve the particular difficulty they are having
but it may also not. To dive into that a little deeper: if the difficulty they are
having is that the web page is visually noisy, having a transcript that deeply
describes all that visual noise and instead makes it auditory doesn't necessarily
solve the difficulty. In fact, it might not even be desireable.

### Mastodon and Hachyderm

For the rest of this article, we will describe the ways that Hachydermians can
begin to maximize the accessibility of their posts within the context of Mastodon.
We will _not_ describe how the Mastodon software itself can be improved.
This is only because that exceeds the scope of this
page and our influence, not because it is unimportant. For those of you who have
ideas for how Mastodon itself can be more accessible, we recommend
[making PRs or opening GitHub issues on the Mastodon project repo](https://github.com/mastodon/mastodon).


## Navigating the complexity

To restate, this an introduction to some of what you will want to learn and internalize
in order to create posts that are more accessible. Note that we didn't say "posts that
are accessible", only "posts that are more accessible". The reason for this is the
scope of humanity is broad, and learning about others is a lifelong journey. Being
truly accessible not only with posts, but with software design and just general life,
is an end goal you should strive to attain even if it can't be truly acheived.

### Sensory

This first set of "things to consider" when you are creating content is based on
the senses we described above that are used when others are _receiving_ the content
you are creating.

#### Visual

This section will be the longest one and will interplay with other sections below. That is
because a lot of the content on Mastodon is _visual_ in nature, whether it is plain text,
memes, or animated GIFs. Some common examples:

* Images, static and animated
* Videos
* "Fancy Text" and special characters
* Emoji
* Hashtags

The direct asks for each of these:

* Include effective alt text
* Should have a summary, similar to the function of alt text
* Minimize usage of "fancy text" and special characters
* Favor longer, complete emoji names over shorter names
* Use CamelCase

##### The context <!-- omit from toc -->

How do people who do not see, or see clearly, the above interact with the content? Typically,
via screenreaders. Screenreaders are designed to not only read plaintext documents, like this page,
but also to read any text associated with a visual. For images and video:

* Images: will need to have alt text
    * [Article about how to write good descriptive text by Harvard Digital Accessibility](https://accessibility.huit.harvard.edu/describe-content-images)
* Videos: either a summary description and/or full transcript as appropriate
    * [W3C Web Accessibility Initiative page for Audio and Video Content](https://www.w3.org/WAI/media/av/av-content/)

But what about "fancy text", emoji, and hashtags? In fact, what do we mean by "fancy text"?

"Fancy text" / special characters actually warrant an article of their own, and Scope has a lovely 2021 article titled
[How special characters and symbols affect screen reader accessibility](https://business.scope.org.uk/article/accessibility-screen-readers-special-characters-and-unicode-symbols).
The article shows how different special character "fonts", typically used to create italics or other visual
affects, are read by screen readers for those who use them.

The case is similar for emoji. While in the standard emoji set there is associated
text for a screen reader to read, like a thumbs up 👍, when reading the text for a
_custom_ emoji the only text available is the name that is supplied between the colons.

Importantly, this is why here on Hachyderm we favor emoji names like ":verified:" rather
than "\:v\:", even though the latter is shorter. When a screen reader encounters the text
"Jayne Cobb \:v\: :gh:" it will read "Jayne Cobb v g h". On the other hand when a screen
reader encounters "Jayne Cobb :verified: :github:" it will read "Jayne Cobb verified github".
One of these is significantly more accessible than the other.

Hashtags is the last heavily used "type" in the visual section. Many screen readers are aware of
and able to read hashtags, but only when they are CamelCase. For those unfamiliar, that means that
you should use the hashtag #SaturdayCaturday not #saturdaycaturday. To show the difference,
[Belong AU has an excellent 17 second clip showing how screen readers read hashtags](https://twitter.com/BelongAU/status/1450711235704492035).

#### Audio

Common sources of audio or audiovisual content on social media are:

* Podcasts, recorded messages, and so on.
* Audiovideo content like YouTube, TikTok, etc.

The asks for these:

* When the content is your own, please have a transcript or similar available
* When the content is not your own, please favor content that has a transcript for longer
  content as often as possible.
* In either case, when posting the content include a short summary (similar to the function of alt text).

##### The context <!-- omit from toc -->

Due to the sizes of audio files in posts, most audio content, or audio-visual content in the case
of video, is not hosted on Hachyderm. That can mean that the 
In general, most Hachydermians are posting links to common
sources like YouTube, TikTok, news pages with video embedded, and so on.

FIXME

#### Noise

"Noise" in this sense applies to:

* "Too much" audio and/or visual content
* "Too loud" audio and/or visual content

For an example of what might be generating audiovisual noise, try navigating the internet without
an adblocker or script blocker. Risk of malware aside, there are a lot of audio and/or visual
ads placed all over web pages and there are frequently pop-ups, notifications, and cookie
consent windows as well.

These situations are usually frustrating when you're trying to navigate the situation as-is, let alone
what happens when you're trying to convert the page to one particular sense (auditory or visual).

Most of these situations do _not_ apply on the fediverse directly. They appear when links to other
pages and content. To be clear, on Hachyderm we do not ask you to be responsible for the entrity
of the internet. That said, if you are posting content that might be "noisy", it might be worth
mentioning in your post that supplies a link.

### Interpretive

Interpretive accessibilty is about how our minds understand presented information. This is a very
broad set of topics as our minds use _a lot_ of data to process information. As an introduction,
some common areas to consider for making intrepretation more access are listed below.

Almost exclusively, the ask for assisting with accessible interpretation is:

* [Use well written content warnings](../content-warnings/).

Since the ask is almost always the same, unlike the above section this section will not have
a "common examples" and "direct asks" pattern.  As an introduction we're
calling out some of the most common barriers to interepretation, offering a suggestion to handle,
and remindng everyone that we do not request or require anyone to become experts. Our main ask
is that you continue to learn and grow in awareness.

#### Neurodiverse

Neurodiversity is the umbrella term for "the range of differences in individual brain function
and behavioral traits, regarded as part of the normal variation in the human population". (Oxford
Dictionary) A few common attributes that are part of neurodiversity are:

* ADHD
* Dyslexia, Dyscalculia
* Autism / Spectrum

There are more than these. The main underlying factors that define different aspects of neurodiversiy
are things like verbal / written skills, hyper/hypofocus, sensory interpretation (e.g. overwhelm when there's
too much sensory input), mental visualization, and so on.
[The Web Content Accessibility Guide article on Digital Accessibility and Neurodiversity](https://wcag.com/blog/digital-accessibility-and-neurodiversity/)
has some excellent tips on the software design level that can also help you build your mental model
while interacting with others.

Within the context of Mastodon, these will usually come up via links to shared content rather than
anything hosted on the platform itself. That means that what you can do is include the relevant information
when you are posting a link to other content. This can either be via a description in the post itself
or, where relevant, crafting a [content warning](../content-warning/) for the post.


#### Medical

One of the most common medical conditions that can cause issues with audiovisual content is seizures.
Photosensitive seizures can be triggered by strobing, flickering, and similar visual effects.
This would only come up if/when a user posted an animated image or video that contained effects similar to
these. If you would like to read about this in more depth, please take a look at
[Mozilla's Web accessibility for seizures and physical reactions page](https://developer.mozilla.org/en-US/docs/Web/Accessibility/Seizure_disorders).

The other two primary medical conditions that come up when interacting with social
media are eating disorders and addictions. The former can be triggered by images of food,
discussions of weight gain or loss, and so forth. The latter can be triggered by images
and discussion around any addictive substance, which includes but is not limited to:
food, alcohol, various recreational drugs, and gambling.

We do not ask that Hachydermians be medical experts in order to interact on the platform.
The main ask to be aware of situations like these and use content warnings when posting
content that might be triggering to these groups.

#### Traumas and phobias

Trauma is a very broad category and the nuance of what can trigger trauma varies between
individuals. That said, there are some common examples of posting patterns that can be
assumed to be generally traumatic:

* If posting about trauma to an individual member of a community, either via a news cycle
  or personal experience, in all likelihood the trauma for the collective group will be triggered.
* If posting about any sort of violence, it can be assumed to be trauamtic even to those
  who have never experienced that type of violence. This includes various forms of violent
  trauma humans can inflict on each other _as well as_ animal abuse and abuse to our environment.
* If posting about wealth and poverty, and the topics in-between, it can be assumed that
  this will trigger the trauma of the many who have had to interact with economic systems
  from a place of disadvantage.

There are many more traumas than these. There are also common phobias that humans have
where the response patterns in the mind and body very directly mirror what happens in
a traumatized person that has been triggered. Common categories of phobias include:

* Death
* Disease
* Enclosed spaces
* Heights

We do not ask that Hachydermians be experts in trauma and phobias in order to interact
on the platform. We do ask that users use content warnings when discussing heavy topics
like the above. This is because, while there is a lot to be gained from discussion, those
most impacted will see the same traumatic conversations over and over again. Especially if
it's the Topic Du Jour (or week) or something has happened in a recent news cycle to prompt
many simultaneous discussions.

#### Language accessibility and ease of translation

The main goal here is to ensure that both plain text and text descriptions of media
are copy/pastable so they can be translated into a different language than they were
composed in. This allows users that may not be fluent, or fluent enough, in the language
the text was written in to use translation tools for assistance.

For clarity: we do not expect any individual to be a hyperpolyglot. We do not expect Hachydermians
to post translations of their posts either. What we are asking is for you to be aware of the issue
and to be aware if you are posting something that cannot be copy/pasted into a third party
tool for translation assistance if someone needs to do so.

Some examples:

* Video content with captions in any language: can another language tool be used to translate
      the captions and/or does the video host support multiple languages for their captions?
* Video content with transcript: can that transcript be copy/pasted into a translation tool?
* Plain-text post: can the post be copy/pasted into a translation tool?
* Slang: most regional slang doesn't translate well when using tools. If you're making a post that
         you want others to be able to easily translate, minimize the use of slang.

### Economic

Within the context of Mastodon, this appears when posts are made that link to paywalled content.
The paywall may be a direct purchase for that specific piece of content or the content is hosted
by an entity that requires a subscription to access.

From an accessibility and equity mindset: while people should be paid for their work, it is important
to remmeber that not everyone can pay for the access to that work. They may be disadvantaged overall,
or may live outside the country or countries that are allowed to pay for access to it.

Another common pattern is for user data to be a type of payment. In this situation, someone must
typically supply their email and some demographic information for free (as in currency) access
to the content. Similar to the above, this can be an accessibility issue for those who have reason
to only share their information cautiously. This is especially in light of increasingly common
data breaches, where supplied data can be used to target individuals and groups.

Here on Hachyderm _we do not moderate_ you for posting paywalled content. Within the context of
accessibility, we ask _that you are aware_ (and call out) when you do and that you manage what
you choose to share with care.

## Summary

The length of this particular document should tell you that being accessible requires time and effort.
As only an intro guide, it should also tell you that there is a lot happening on our biodiverse sphere.
This is part of the reason that we _request_ [content warnings](../content-warnings/) as appropriate:
we are approaching these issues from a growth mindset for our userbase. The other reason we _request_ is
that we understand that occasionally different groups have genuinely different needs. One person may
post about weight gain/loss as part of recovery from a medical issue, it may trigger another person's
current eating disorder. One person may want to scream about how blatant transphobia hurts them and
another person may not want a reminder that that's still happening today. Another way to look at
situations like these: individuals and groups _can_ be in a state of conflict without anyone being
wrong.

Taking these into account, these are our asks:

* Be aware of the general asks of the above, and at a minimum:
  * Apply [content warnings](../content-warnings/) when posting and sharing content that is likely
    to impact the mental health and psychological safety of others, especially if and when those
    most impacted will be a traditionally marginalized group.
  * Add alt text to your images and summaries for your videos.
  * Use CamelCase for your hashtags.
  * Be mindful of how much paywalled content you're posting.
* Remember that others may not know what you know, and others may know things that you do not know. That means
  when it comes to the above help others, but [Don't Be A Dick](/docs/rule-explainer/). e.g.:
  * If someone forgot their alt text, or didn't realize they could edit a post to add it after the fact, help
    them don't shame them or sealion them.[^1]
  * If someone didn't put a content warning on a post that maybe should have it, help them don't shame them or sealion them.
  * If someone didn't realize that an article was paywalled, help them don't shame them or sealion them.
  * And so on.
* Be courteous and respectful with each other when different needs come into conflict.
* Report issues, users, and/or servers when you encounter a situation that requires moderator attention and/or action.
  * Make sure to include the details, even if they are obvious, as [outlined in our Reporting and Communication doc](/docs/moderation/reporting).

[^1]: An addendum (we try to minimize these):<br />
If someone forgets their alt text, **_part of_** "help them don't shame them or sealion them" means
not telling them it "only takes two seconds to write alt text". Yes, people should write alt text.
No, it doesn't take two seconds to write (useful) alt text - there are literally whole articles
about how to do this effectively. If you're going to help, please do so in a genuine way but if
not then please move on. 