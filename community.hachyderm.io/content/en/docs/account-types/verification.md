---
title: "Specialized Account Verification with Hachyderm"
linkTitle: "Verify with Hachyderm"
weight: 20
description: >
  How to become a verified, specialized, account with Hachyderm.
---

## Who should verify?

Currently only a subset of our specialized accounts are _required_ to verify. That said we recommend
that all specialized accounts (including some, but not all, influencer accounts) go through the verification
process so that Hachyderm users know that your account is officially recognized and that you've
agreed to [the covenant](../covenant/).


### Required and optional verification

We recommend all accounts that are not user accounts apply to be verified with us, only the following
are required to be verified:

* [Corporate accounts](../corporate-accounts/)
* [Bot accounts](../bot-accounts/)
* [Curated accounts](FIXME)

Accounts that will likely want to consider being verified:

* [Events](../open-source-accounts/)
* [Open Source Projects](../open-source-accounts/)
* Any account that may appear similar to a corporate account (but is not). This may include:
  * Some of the non-profits we've welcomed on our instance
  * Some of our [Influencer Accounts](../influencer-accounts/) (though not all)
    * Note that verification is not open to general users at this time.

## When to verify?

This process was launched in February of 2023. We ask existing accounts that need to be verified to
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

1. Read [the Covenant](../covenant/)
1. Open a "Specialized Account Approval" issue from our [Community Docs Github Repo](https://github.com/hachyderm/community/issues/new/choose)
1. Include your agreement to the covenant in the GitHub issue 
1. Be patient (we are group of volunteer mods and will reach out as soon as we can)
1. We make a decision
  - If you are not approved, we will provide a reason and close and the PR
  - If you are approved, you can now create your account and then move on to _Part 2_ below

_Part 2: Finishing account setup_

1. Ensure you're already [verified with your official domain](https://github.com/hachyderm/community/blob/main/verification.md)
    - Do not remove the reference link. Moderators will be using this during their validation process.
1. Fork this branch
1. Add your verification tag under the appropriate header in the [approved](https://github.com/hachyderm/community/blob/main/community.hachyderm.io/content/en/approved/_index.md) file.
1. Create a pull request using the [specialized account](FIXME) template.
1. Complete all tasks in the tasks list
1. Submit the pull request
1. Be patient (we are group of volunteer mods and will reach out as soon as we can)
1. Validate your code has been merged, and your account is now visible on [https://community.hachyderm.io/approved](https://community.hachyderm.io/approved)
1. Using the [verification steps](https://github.com/hachyderm/community/blob/main/verification.md), add the following to your profile metadata
    - Label: APPROVED
    - Content: https://community.hachyderm.io/approved
1. Make sure to share that you're an approved account, and include that that means you've agreed to [the covenant](../covenant/)!
