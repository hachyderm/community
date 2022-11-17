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
including username / handle.

# How to verify

## GitHub

1. Add your Hachyderm / Mastodon URL to the website field of your GitHub
   profile, e.g. [https://hachyderm.io/@username](https://hachyderm.io/@username)
   * Note: You should not include "rel=me" for GitHub verification / use raw HTML
2. Save changes.
3. Then on Hachyderm / your Mastodon account, go to Edit Profile
4. In one of the four fields of Profile Metadata, add the URL to your
   GitHub account, e.g. [https://github.com/username](https://github.com/username)
5. Save changes.

The verification should appear almost instantaneously.

## Other sources

GitHub has separated instructions because, as far as we know, they're one of
the only providers that adds the "rel=me" attribute. In general, when you
verify you will need to add the the URL with this attribute called out like
so:

```
<a rel="me" href="https://hachyderm.io/@username">Hachyderm</a>
```

Similar to above, on Mastodon / Hachyderm:

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
          
## How long does verification persist?

Verification persists only as long as the check link is there. This is
important to note as for some services, like the GitHub example above,
you cannot have multiple URLs as your "website". This means if you remove
your Hachyderm / Mastodon URL from the relevant field that the verification
check will break and the green "verified" next to that URL will disappear.

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
