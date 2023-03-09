---
title: "Specialized Account Verification with Hachyderm"
linkTitle: "Verify with Hachyderm"
weight: 20
description: >
  How to become a verified, specialized, account with Hachyderm.
---

## Who should verify?

Currently, only a subset of our specialized accounts are _required_ to verify. That said, we recommend
that all specialized accounts (influencer accounts on a case-by-case basis) go through the verification
process so that Hachyderm users know that your account is officially recognized and that you've
agreed to the [Specialized Account Expectations](../covenant/).


### Required and optional verification

While we recommend all accounts that are not user accounts apply to be verified with us, only the following
are required to be verified:

* [Corporate accounts](../corporate-accounts/)
* [Bot accounts](../bot-accounts/)
* [Curated accounts](../curated-accounts/)

Accounts that will likely want to consider being verified:

* [Community Events](../open-source-accounts/)
* [Open Source Projects](../open-source-accounts/)
* Any account that may appear similar to a corporate account (but is not). This may include:
  * Some of the non-profits we've welcomed on our instance
* Some of our [Influencer Accounts](../influencer-accounts/) (though not all)
    * Note that verification is not open to general users at this time.
    * In general, this is only if your personal brand or posting style could be conflated
      with one of the recognized specialized account types. If
      you're using Hachyderm as a general user and happen to have
      a large following, you likely would not want to be verified
      at this time.

## When to verify?

This process was launched in February 2023. We ask existing accounts that need to be verified to
do so by the end of March 2023.

## What does a verified account look like?
All specialized accounts that have been verified by the Hachyderm moderation team will have a verified link pointing to [community.hachyderm.io/approved](https://community.hachyderm.io/approved) in their profile links. This link should be titled "Approved" on the account bio:

<img src="../approved.png" alt="Screenshot of the approved links section of a profiles.
      There are two verified links. One link is pointing to the companies website.
      The other link is pointing to https://community.hachyderm.io/approved"
    width="400px" />

## The Application Process

**Steps to getting approved**

This is only for the specialized accounts.
We are not accepting request for individual users at this time.

_Part 1: Get Pre-Approved_

To get started, we will create an issue to track the full process from the creation of your account to the completion of the approval process.

1. Read the [Specialized Account Expectations](../covenant/)
1. Open a "Specialized Account Approval" issue from our [Community Issue Tracker](https://github.com/hachyderm/community/issues/new?assignees=&labels=Specialized+Accounts&template=9.Specialized-Account-Approvals.yml&title=Specialized+Accounts%3A+YOUR_ACCOUNT_NAME)
1. Include your agreement to the Specialized Account Expectations in the GitHub issue 
1. Be patient (we are group of volunteer mods and will reach out as soon as we can)
1. We make a decision
   - If you are not approved, we will provide a reason and close the GitHub issue.
   - If you are approved, you can now create your account and then move on to _Part 2_ below
     - Note: you should leave the GitHub issue _open_.

Do not pre-emptively put the Approval URL in your profile metadata.
Due to the way that verification works, Mastodon will only try to verify you
_once_ per server when you add a URL. This means that Hachyderm's instance will
only verify the URL when you add it, prior to it being approved, and will not re-check.
You will be prompted to add the URL at the appropriate step below so the URL is live
when Hachyderm checks.

If you've pre-emptively added the field to the account profile, you'll need to re-save after the
approval URL is live with your account listed in Part 2 below.

_Part 2: Finishing account setup_

1. Ensure you're already [verified with your official domain](/docs/mastodon/user/verification/)
    - Do not remove the reference link. Moderators will be using this during their validation process.
1. We will add your verification tag under the appropriate header in the approved file. (Please be patient, we are a group of volunteers and will update as soon as we can.)
1. We will update the GitHub issue when this is done.
1.  Using the [verification steps](/docs/mastodon/user/verification/), add the following to your profile metadata
    - Label: APPROVED
    - Content: https://community.hachyderm.io/approved
1. Verify that you can see the appropriate field highlighted in green and the green check mark
1. Once you have added the above to your profile metadata and verification is successful, please update and close the GitHub issue.
   - Do not remove the approved link once you have completed the process. This field lets
     our users know you're an approved account and will prevent your account from being reported as an unapproved account.
2. _Optional, but recommened:_ Make sure to share that you're an approved account, and include that that means you've agreed to the [Specialized Account Expectations](../covenant/)!
