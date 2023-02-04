---
title: "Specialized Account Verification"
linkTitle: "Verification"
weight: 10
description: >
  How to be a verified, specialized account.
---

## Who should verify?

Currently, the only specialized account type that is _required_ to verify is the
[corporate account](../corporate-account/). That said, we recommend that all of our specialized accounts
go through the verification process so that Hachyderm users know that your account
is officially recognized and that you've agreed to [the Covenant](../covenant/).

## Which Accounts Should Apply

We recommend all accounts that are not user accounts apply to be verified with us, although only
invite-only account types are _required_ to be veriifed. Account types that will likely want to
consider being verified:

* [Corporate Accounts](../corporate-accounts/)
* [Events](../open-source-accounts/)
* [Open Source Projects](../open-source-accounts/)
* [Bots](../bot-accounts/)

### What Does an Approved Account look like?
All specialized accounts that have been approved by the Hachyderm moderation team will have a verified link pointing to [community.hachyderm.io/approved](https://community.hachyderm.io/approved) in their profile links. This link should be titled "Approved".

<img src="../approved.png" alt="Screenshot of the approved links section of a profiles.
      There are two verified links. One link is pointing to the companies website.
      The other link is pointing to https://community.hachyderm.io/approved"
    width="400px" />

## The Application Process

**Steps to getting approved**

This is only for the specialized accounts.
We are not accepting request for individual users at this time.

_Part 1: Get Pre-Approved_

To get started, we will create an issue to track the full process from creation of your account to completion of the approval process.

1. Read [the Covenant](../covenant/)
1. Open a "Specialized Account Approval" issue from our [Community Docs Github Repo](https://github.com/hachyderm/community/issues/new/choose)
1. Include your agreement to the covenant in the GitHub issue 
1. Be patient (We are group of volunteer mods and will reach out as soon as we can)
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
1. Be patient (We are group of volunteer mods and will reach out as soon as well can)
1. Validate your code has been merged, and your account is now visible on [https://community.hachyderm.io/approved](https://community.hachyderm.io/approved)
1. Using the [verification steps](https://github.com/hachyderm/community/blob/main/verification.md) add the following to your profile metadata
    - Label: APPROVED
    - Content: https://community.hachyderm.io/approved
1. Make sure to share that you're an approved account, and include that that means you've agreed to [the covenant](../covenant/)!