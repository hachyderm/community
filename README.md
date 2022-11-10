# Community

Hachyderm Community Resources, including

* How to get help when you need it (at the top)
* Mastodon 101
* Hachyderm 101 - Things to know about the Hachyderm instance in particular

# Troubleshooting, Support, and Issues

The most critical thing you can do to help us help you (even more so than a donation) is to **reduce noise**. 

The best way for you to help reduce noise is to leverage our issue tracker instead of independent one-off requests for help. It is a full time job sifting through requests and making sense of them. If you want to help, leverage the issue tracker and [create a new issue](https://github.com/hachyderm/community/issues/new) or better yet find one that already exists.

### Do Not

 - Please do not reach out on Twitter.
 - Please do not join the Discord just to report an issue, bug, or feature request.
 - Please do not send us emails (we get too many emails).
 
### Do
 
  - File an issue in this repository

  
# Mastodon 101

Hello Hachydermians! Some of you are new to Mastodon, so here are some notes to help you get started. Since a fair few of you are coming from Twitter, there will be comparisions to the Twitter model for social media.

## How do I sign up?

If you're looking to sign up with us here at Hachyderm, you can sign up on [hachyderm.io](https://hachyderm.io). The only criteria for signing up is abiding by our [Hachyderm Terms of Service](https://hachyderm.io/about/more), a copy of which is in our repo. If you're looking at other Mastodon instances, then the sign up process is likely similar but with their own domain.

## How do I access (public) toots?

There are a few different ways:

* The web browser, so in our case [hachyderm.io](https://hachyderm.io)
* A client app, usually for mobile devices:
  * iOS: [Toot!](https://apps.apple.com/us/app/toot/id1229021451) (cost: $3 USD)
  * Android: [Tusky](https://play.google.com/store/apps/details?id=com.keylesspalace.tusky&hl=en_US&gl=US&pli=1) (cost: free)

For a complete comparison of 8 iOS apps: Fedi, Mast, Mastodon (official), Mercury, Metatext, tooot, Toot!, and Tootle, please take a look at [Transpondering's Blog](https://transponderings.blog/2022/05/21/eight-mastodon-apps-for-iphone/) on the topic. The deep dive is very deep, going into various UI features, commenting about how intuitive the different apps are or aren't, which are more or less compatible with screenreaders and VoiceOver, and so on.

## What does being on a specific Mastodon instance mean

If you're here you've likley signed up on "the Hachyderm instance of Mastodon", but you may have signed up for any instance here referred to algebriacially by "X".


## Toots and Messages

### Who can see my stuff / Whose stuff can I see?

This diagram has been making rounds on Twitter, Mastdon, et al. It is from a GitHub issue on the Mastodon project:

![Flow chart showing that a public toot by USER is visible only if you are: following that user, the user is on the same instance as you, or someone on your instanced follows and interacted with the toot](assets/mastodon-toot-visibility-flowchart.jpg)

This is the case of _public_ toots only. When you are a private account, the people you allow to follow you are the people who can see your toots.

### Who can see DMs? It depends.

Direct messages are similar (in intention) the way that you are able to communicate directly with one or more other users. This is similar to what you've likely experienced on many other platform, with a notable exception:

* ⚠️ **_When you bring someone into a DM conversation they are able to see the whole DM history._**

On the one hand this solves the problem of Slack, Twitter, etc. where when you look to add someone to a conversation you need to summarize everything relevant to that point to bring the new person / people up to speed. That said, if you aren't expecting it, it can expose conversations to third parties that needed to be private.

The other person / people who can see DMs are mods. 

* **_Note: Yes, mods_ can _see your DMs._**

Similar to the above, this is a double edged sword. On the one hand it makes it easy for mods to read DMs when they receive a report of harassing behavior. On the other hand it might also make private conversations visible that you wished were kept private even in those circumstances.

As a transparent statement: Hachyderm mods do _not_ casually read user DMs. We would only look at a specific DM in the event of a report from a user (e.g. due to harassment, platform errors, etc.).


#### DM user experience in the various interfaces

The UI experience of DMs is not as clearly separated as other apps like Twitter, Slack/Discord, et al. In the web UI, for example, DMs do not look significantly different than a private account tooting. Some of the mobile apps, like Toot!, have a better visual separation. Basically: depending on where you prefer to toot, you'll have vastly different experiences (for now).

### Content Warnings

Content Warnings are implemented differently in Mastodon than Twitter. CW'ed toots look like this:

![](assets/mastodon-content-warning.png)

In this case the toot has both text and associated graphic. You would need to click to display each separately in each case. When a toot has a CW, all toots in the conversation carry that same CW.

Content Warnings have a few uses:

* If discussing topics that can cause distress or trigger PTSD, like a great many political situations
* Discussing topics that will spoil a book / movie / show

**_Because of how well CWs are implemented on the platform, we recommend that people make use of them._** It is far easier on the mental health of other users to opt into a discussion about Whatever than to skim past it.

Also! Make sure that your CWs are _specific_ so users know whether they want to opt in or not. e.g. are you hiding a toot / image that depicts violence or hints at it? Are you hiding the season finale to a show? How users socialize their use of CWs is what makes them useful. Making heavy, unclear, use of CWs adds confusion.s