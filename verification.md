# Verification

Verification on Mastodon works less like Twitter and more like an identity
service. That is, you do not need to prove your association with your own
brand or to pay a fee, you are only showing that you are the owner of one
(or more) accounts on separate services to substantiate your digital
identity.

Here's what it looks like when a profile has verified via their GitHub
identity:

<img src="assets/mastodon-verification-profile-quintessence.png"
     alt="Screenshot of profile for user quintessence, showing avatar, header
          and relevantly the verified GitHub URL field which is highlighted in
          green and has a green checkmark next to the URL." />

GitHub shows as verified with a green checkmark and complete URL,
including username / handle. (Since GitHub has special instructions, more on
that in a moment.

# How to verify

## How to verify, in general

GitHub has separated instructions because, as far as we know, they're one of
the only providers that adds the "rel=me" attribute. In general, when you
verify you will need to add the the URL with this attribute called out like
so:

```
<a rel="me" href="https://hachyderm.io/@username">Hachyderm</a>
```

You can also put the following in the page headers of your personal site, if
you would like to avoid having a visible link:

```
<link rel="me" href="https://hachyderm.io/@username">
```

Then on Mastodon / Hachyderm:

1. Go to Edit Profile
2. In one of the four fields of Profile Metadata, add the URL of the
   destination you are verifying
3. Save changes

Here is an example profile with two separate sources of identity
verification:

<img src="assets/mastodon-verification-profile-matt-stratton.png"
     alt="Screenshot of profile for user Matty Stratton, used with permission,
          showing two sources of URL verification. One is his own website,
          mattstratton.com and the other is his Keyoxide account. Both are
          highlighted in green with green checkmarks next to the URL to show
          they are verified." />

## GitHub - Workarounds

### Your GitHub Profile

1. Add your Hachyderm / Mastodon URL to the website field of your GitHub
   profile, e.g. [https://hachyderm.io/@username](https://hachyderm.io/@username)
   * Note: You should not include "rel=me" for GitHub verification / use raw HTML
2. Save changes.
3. Then on Hachyderm / your Mastodon account, go to Edit Profile
4. In one of the four fields of Profile Metadata, add the URL to your
   GitHub account, e.g. [https://github.com/username](https://github.com/username)
5. Save changes.

The verification should appear almost instantaneously.

Note: In order for this to work this MUST be sit in the profile web link under your profile picture. This field will automatically add the required `rel=me` tag to your URL, whereas the other locations will strip the tags automatically. You cannot embed the URL in a README on your profile page. Unfortunately you will not be able to post another URL in the location.

### Your GitHub.io Page

If you do not want to sacrifice your web page field on your GitHub profile,
then another way to verify is to verify your username.github.io page.
This is a workaround [documented by Simon Willison on his blog](https://til.simonwillison.net/mastodon/verifying-github-on-mastodon).
In this case, you supply the regular link with the `rel="me"` attribute,
again either using a regular link or placing it in the header information.
As an example, [Simon Willison's code for his GitHub.io page is here](https://github.com/simonw/simonw.github.com/blob/main/index.html).

The result is this:

<img src="assets/mastodon-verification-profile-simon-willison.png"
     alt="Screenshot of profile for user Simon Willison, showing that
          he has verified his Blog and GitHub.io pages. Note he is a
          Mastodon, but not a Hachyderm, user." 
     width="400" />

Note: 

* This image is only the metadata information that he also included in his
blog post.
* He is running his own self-hosted Mastodon instance.

          
## How long does verification persist?

Verification is checked upon saving your profile. Thus, as long as you
don't change anything, your verified identities will persist and you're
free to change back the website on your GitHub profile[^JWildeboer]. 
Please keep in mind to change the website on your GitHub profile if
you intend to do any changes to your Mastodon profile.

## Alternatives

If you would like to verify your identity with more services than the
metadata allows, you might want to consider using a service like
Keyoxide or Keybase for the majority of your identity verification, and
then verify Hachyderm / Mastodon with that identity management service.

# Who should verify

We do not have a policy for regular users to verify or not - that is up to
you! If you have a special account type, for example a corporate or open
source project account, please see the instructions for those accounts
for what verification we'd need.

---
[^JWildeboer]: See <https://jan.wildeboer.net/2022/06/Quick-Fix-Verified-Mastodon-Github/#the-solution>
