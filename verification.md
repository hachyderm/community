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

```html
<a rel="me" href="https://hachyderm.io/@username">Hachyderm</a>
```

If you would like to avoid using a visible link, like the above, you can
also put the following in the page headers:

```html
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

## GitHub

*Update 2023-02-02: GitHub now allows to add up to four arbitrary social accounts, which drasticaly simplifies to verify GitHub profiles. See <https://github.blog/changelog/2023-02-02-add-more-social-links-to-your-user-profile/> for reference.*

**On GitHub**

Open the [settings of your GitHub account](https://github.com/settings/profile) you want to verify and:

1. Add the full URL of your Hachyderm / Mastodon profile to one of the four social accounts fields.
     - Note: your full username includes the server, e.g. @username@hachyderm.io
2. Save changes.

**On Hachyderm / Mastodon**

After you have saved your changes go to your Hachyderm / Mastodon account and:

1. Go to Edit Profile
2. In one of the four fields of Profile Metadata, add the URL to your
   GitHub account, e.g. [https://github.com/username](https://github.com/username)
3. Save changes.

Verification should appear almost instantaneously.

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
