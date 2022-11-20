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
including username / handle. (Note GitHub has different instructions than
usual, more on that in a moment.)

# How to verify

## How to verify, in general

In general, when you verify you will do so by using the following HTML on the
page you are editing, like a personal site or blog:

```
<a rel="me" href="https://hachyderm.io/@username">Hachyderm</a>
```

If you would like to avoid using a visible link, like the above, you can
also put the following in the page headers:

```
<link rel="me" href="https://hachyderm.io/@username">
```

After doing either of the above, you will need to add the URL of the site
to your Hachyderm / Mastodon profile. You will do that by:

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

#### Updated with new information

There are **_two_** ways to verify your GitHub. Both of these differ from
the regular verification instructions above.

**First Option: Profile Bio Field**

Note that this method will not work if your Hachyderm username matches
your, or anyone's, Github username, beause Github will turn the username
into a link, breaking the verification process.

1. Add your full Hachyderm / Mastodon username to your GitHub bio.
   * Note: your full username includes the server, e.g. `@username@hachyderm.io`
2. Save changes.

It looks like this:

<img src="assets/mastodon-github-verify-bio-field.png"
     alt="Screenshot GitHub profile edit page with @username@hachyderm.io in
     in the bio field"
     width="250" />

**Second Option: Website in Profile[^SimonWillison]**

1. Add your Hachyderm / Mastodon URL to the website field of your GitHub
   profile, e.g. [https://hachyderm.io/@username](https://hachyderm.io/@username)
   * Note: You should not include "rel=me" for GitHub verification / use raw HTML
2. Save changes.

It looks like this:

<img src="assets/mastodon-github-verify-website-field.png"
     alt="Screenshot GitHub profile edit page with
     https://hachyderm.io/@username in the website field"
     width="250" />

Note: In order for this to work this MUST be sit in the profile web link
under your profile picture. This field will automatically add the required
`rel=me` tag to your URL, whereas the other locations will strip the tags
automatically. You cannot embed the URL in a README on your profile page.

Unfortunately you will not be able to post another URL in the website
location; even though hachyderm.io will continue to show you as verified,
other instances will do their own verification check when users on those
instances view your profile.

**On Hachyderm / Mastodon**

Whichever of the above you choose, after you have saved your changes go
to your Hachyderm / Mastodon account and:

1. Go to Edit Profile
2. In one of the four fields of Profile Metadata, add the URL to your
   GitHub account, e.g. [https://github.com/username](https://github.com/username)
3. Save changes.

Verification should appear almost instantaneously.

Please note that this only applies to _personal_ GitHub profiles.
Currently, there is no way to verify _organizational_ GitHub profiles as
the `rel=me` tag is not added here.

### Your GitHub.io Page

If you do not want to sacrifice your web page field on your GitHub profile,
then another way to verify is to verify your username.github.io page.
This is a workaround [documented by Simon Willison on his blog](https://til.simonwillison.net/mastodon/verifying-github-on-mastodon).[^SimonWillison]
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

[^JWildeboer]: Source for verifying GitHub <https://jan.wildeboer.net/2022/06/Quick-Fix-Verified-Mastodon-Github/#the-solution>

[^SimonWillison]: Second example, GitHub as well as GitHub.io <https://til.simonwillison.net/mastodon/verifying-github-on-mastodon>
