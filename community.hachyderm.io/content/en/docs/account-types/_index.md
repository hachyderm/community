---
title: "Account Types"
linkTitle: "Account Types"
weight: 20
---

We distinguish between 2 main types of accounts that we use to measure and
moderate here on Hachyderm: specialized accounts and user
accounts. (Specialized accounts are sometimes also referred to as
"novelty" accounts on other platforms.) User accounts are when
a single user is interacting with the platform as themselves and
not on behalf of a company (Company Inc.) or project (OSS project,
podcasts, etc.) and/or not posting with a singular purpose or
topic and/or bot accounts.

For specialty acounts: we recognize and have rules around some. If
an account is not a user account and not one of the recognized
account types below, then it is not a type permitted on this
server. This is to prevent automated / single post / corporate
account (etc.) posts from overtaking regular users. If you would
like to create a specialized account type that is not on this
list, please create a suggestion on [our Community Docs Github Repo](https://github.com/hachyderm/community/issues/new/choose) for a new type of specialized account. Unrecognized
specialized account types will be removed. Recognized account
types that do not follow the rules of their account types will be
moderated as needed.

Some specialized account types are invite only. Unapproved
specialized accounts that are invite only will be suspended. If
you are interested in creating a specialized account that is
invite only, you must first reach out to us at
[admin@hachyderm.io](mailto:admin@hachyderm.io).

For all other specialize accounts, please use the [account approval](#account-approvals) steps below to get formal approval for your account.

## User Accounts

User accounts are also referred to as General Accounts, which are
briefly described on our [General Accounts Page](/docs/account-types/general-accounts/).
In general:

- Follow server rules
- Don't create type confusion with a specialized account type

For the latter, if you are an individual user then you shouldn't
have a username or About page that might indicate that you are a
company, project, or other form of specialized account. As a
specific example, if you have an account name like MyUserCompany
or MyPodcast then you will be considered that specialized account
type based on name or About page and be bound by those rules.

**Influencer Accounts = Large Userbase Accounts**

Anyone who has more than 25k followers on an existing platform is
what we refer to as an [Influencer Account](/docs/account-types/influencer-accounts/). The only special rule here is
that we request that you reach out to us in advance at
[admin@hachyderm.io](mailto:admin@hachyderm.io) before migrating
as we will likely need to assist with the migration to prevent
follows getting "stuck", etc.

## Specialized Accounts

The common rules for all specialized account types are:

- Your username and display name must clearly indicate what you are<br />
This means for companies, OSS projects, podcasts, newsletters, etc.
then the username must match the company / project name. For most
other account types this means "describe what you are" via username,
e.g. "CuratedTechJobPosts".
- You must be verified with your company, project, etc. page<br />
If your company, project, newsletter, etc. has a web page then
that web page must be verified on your profile.

**Company and Project Account Types**

- [Corporate Accounts](/docs/account-types/corporate-accounts/)
- [Open Source Accounts](/docs/account-types/open-source-accounts/)


**Special / Focused Content Account Types**

These will have their own separate pages soon, but include:

- Newsletters
- Podcasts
- Streamers
- Curated Posting Accounts

**Automated Posting / Bot Account Types**

- [Bot Accounts](/docs/account-types/bot-accounts/)

### Account Approvals

All specialized accounts that have been approved by the Hachyderm moderation team will have a verified link pointing to [community.hachyderm.io/approved](https://community.hachyderm.io/approved) in their profile links. This link should be titled "Approved".

<img src="approved.png" alt="Screenshot of the approved links section of a profiles. There are two verified links. One link is pointing to the companies website. The other link is pointing to https://community.hachyderm.io/approved"/>

**Steps to getting approved**

This is only for the specialized accounts.
We are not accepting request for individual users at this time.

_Part 1: Get Pre-Approved_

To get started, we will create an issue to track the full process from creation of your account to completion of the approval process.

1. Open a "Specialized Account Approval" issue from our [Community Docs Github Repo](https://github.com/hachyderm/community/issues/new/choose)
1. Be patient (We are group of volunteer mods and will reach out as soon as we can)
1. We make a decision
  - If you are not approved, we will provide a reason and close and the PR
  - If you are approved, you can now create your account and then move on to _Part 2_ below

_Part 2: Finishing account setup_

1. Ensure you're already [verified with your official domain](https://github.com/hachyderm/community/blob/main/verification.md)
    - Do not remove the reference link. Moderators will be using this during their validation process.
1. Fork this branch
1. Add your verification tag under the appropriate header in the [approved](https://github.com/hachyderm/community/blob/main/community.hachyderm.io/content/en/approved/_index.md) file.
1. Create a pull request using the [specialize account]() template.
1. Complete all tasks in the tasks list
1. Submit the pull request
1. Be patient (We are group of volunteer mods and will reach out as soon as well can)
1. Validate your code has been merged, and your account is now visible on [https://community.hachyderm.io/approved](https://community.hachyderm.io/approved)
1. Using the [verification steps](https://github.com/hachyderm/community/blob/main/verification.md) add the following to your profile metadata
    - Label: APPROVED
    - Content: https://community.hachyderm.io/approved


## Frequently Asked Questions

Below are the FAQ for all Hachyderm accounts.

### Can I post about my company?

Yes. Posting about your company is different from a corporate account. Feel
free to say whatever you want about your company.

### Can I post about my project?

Yes. Posting about your project is different from an open source account. Feel
free to say whatever you want about your project.

### Can I create a bot account?

Not without working directly with the moderators.

### Can I create an anonymous account?

Yes. However, we do not want a single person to operate a high number of
accounts.

We understand the importance of being anonymous from a security, gender,
safety, and mental health perspective.

### Can I create multiple accounts?

Yes. Within reason. We expect you to use your best judgement in not flooding
our servers. We understand you might need more than one account. However, it is
not a free for all.  We understand security, gender, safety, and mental health,
and safe space from work are all reasons to create multiple and anonymous
accounts.

### Can I create accounts for pets, characters, or imaginary friends?

We prefer if you didn't. We are trying to build a curated network of
professionals on Hachyderm and would encourage you to move these accounts to
another instance.
