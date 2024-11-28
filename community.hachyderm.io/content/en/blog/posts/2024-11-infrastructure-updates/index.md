---
date: 2024-11-25
title: "Ensuring Hachyderm's Future: Improving Safety & Resilience through Strategic Placement of Infrastructure"
linkTitle: "Hachyderm Infrastructure Resilience Plan"
description: |
  Updates about Hachyderm infrastructure and security plans,
  risk assessments, etc. for the new year.
author: Hachyderm Infrastructure ([@Hachyderm](https://hachyderm.io/@Hachyderm))
---

FIXME - If not "Hachy Infra", change author to Esk
FIXME - Fix date to true date, not 25 Nov. This will need to be pre-publish, as the date is in the slug.

# Preamble/Disclaimer

This document has **not **been reviewed by a lawyer and **must not be considered legal advice**. Hachyderm and its volunteer staff will make a best effort to keep Hachyderm running and safe from government interference, but we cannot guarantee any particular legal outcomes.

***That being said, we are going to do our best to provide a service that is resilient, available, and safe to use.***

As a Fediverse user, we strongly encourage you to develop your own [operations security (opsec)](https://csrc.nist.gov/glossary/term/operations_security) plan and evaluate your personal risk profile. If you're not sure how to do this, we'll follow up with a post/blog with reading material so you can think through and improve your online defense posture.

Finally, you are welcome to share this document and engage others in the conversation; you don't have to have a Hachyderm account. As we begin executing on the plan, one key tenet is to share as much as we can so others can prepare their corners of the Fediverse.


## tl;dr

Hachyderm operates primarily out of the EU. We will reduce our exposure to US-based companies and continue to place key infrastructure in the EU.


# Introduction

Hachyderm has, over the last two years, established itself as a small corner of the Fediverse where approximately 54,000 users (10,000 monthly active users) have made their fedi-home. 


> Here we are trying to build a curated network of respectful
> professionals in the tech industry around the globe. We welcome
> anyone who follows the rules and needs a safe home or fresh
> start.
>
> We are hackers, professionals, enthusiasts, and are **passionate
> about life, respect, and digital freedom**. We believe in peace
> and balance.

With the outcome of the 2024 US elections, the United States electorate has signaled – confirmed? – a shift toward a strongly conservative government. Rightfully so, many people in the Hachyderm and Fediverse communities are anxious, worried, and fearful for the actions this new administration will pursue in the coming years.

It is not hard to envision a future in the US where new legislation, executive action, or court orders threaten the availability and even existence of Hachyderm and similar sites in the Fediverse.


## Resolution 

**Hachyderm _must_ continue to be a safe space for our community that is dependable, available, and secure.**

**Risk-model.** To this end, we will use a risk-based model to
reconsider the placement of our infrastructure components to
increase the safety and resilience of our platform. In particular,
we _must_ reduce our exposure to providers and services that could be compelled by the US government to disrupt our ability to serve the community.

**Diversified providers.** While we identify our future
configuration, we _must_ also continue to hold dear the value of diversifying across providers to avoid the risk of service suspension through a single provider. This was a core architecture principle in the current iteration of Hachyderm, and it will continue to be one in our future configuration.

**Always test first.** Although we want to act quickly, as a matter of good infrastructure stewardship, all changes we are proposing *must *be tested first against hachyderm.wtf (our dev instance) before they are applied to hachyderm.io. This may require us to improve our infrastructure delivery pipeline (using this phase very broadly).

**Share broadly.** Finally, we _must_ share our process, thinking,
and learnings openly so that the rest of the Fediverse community
can benefit. Where possible, we _should_ also open source our infrastructure and scripts as code – this will require additional effort to sanitize things like secrets or Hachyderm-specific configuration.


## Scope

While there are many other influencing factors that could affect Hachyderm, we are focused on the technical architecture and placement of infrastructure. For example, we care about where our media is stored, but we aren't addressing the fact that our bills are paid from a US-based credit card and bank account. We will address those other operational risks in a separate document.

For the moment, we are also not addressing German [political risks](https://www.reuters.com/world/europe/fearing-uncertainty-german-industry-calls-fast-snap-election-2024-11-07/) - we may expand the scope of this initiative based on the results of the [planned February 2025 snap election](https://www.cnn.com/2024/11/12/europe/germany-snap-election-february-intl/index.html).


# Sites

Hachyderm's infrastructure consists of several layers, designed to be modular, interchangeable, and replaceable with a reasonable amount of effort. Hachyderm operates two types of "sites": the core site, and our edge sites.


## Core Sites

The core site is where the Mastodon components, data and media are stored and processed. This includes components like the Mastodon software, our media storage system, and the Hachyderm database. Since this houses our data – multiple terabytes of information - the core site is harder to replace and would likely incur downtime if we had to create a new one.


## Edge Sites

Edge sites are "points of presence" we deploy across the globe that help speed up access to the core. For example, a user in Osaka, Japan would connect through the Tokyo, Japan edge site which then connects them to the core.

Edge sites will store temporary copies of assets like images and content to speed up access for other users connecting to that edge. It's a little slower for the first person to download the new viral catte.jpeg in a region, but then it's faster for everyone else. Edge sites are designed to be lightweight and replaceable; if we lose the Fremont, US site due to a technical issue, we don't lose any data. Users in the US are shortly – usually after about 30 seconds – routed to the next nearest site, in this case, Newark, US.


## Current State (November 2024)


FIXME - needs image and alt text
![alt_text](images/image1.png "image_tooltip") <br />
💜 = current edge site 💛 = possible future edge site <br />
🖼️ = media storage (images, videos) 
FIXME - needs image and alt text
![alt_text](images/image2.png "image_tooltip")
= Mastodon core services (web, queues, database)

Our [Core Site](#heading=h.762j9inad68r) is in Frankfurt, Germany and operated by Hetzner (a German provider). In 2022, we chose to deploy to Germany due to the protections offered by laws like the [General Data Protection Regulation (GDPR)](https://commission.europa.eu/law/law-topic/data-protection/data-protection-eu_en) that regulate how people's data is processed and handled by providers. Since it's harder for us to move or replace the Core Site – there's a lot of data! – we put this site in a location that offered the strongest legal protections for free speech and data privacy. In hindsight, we reaffirm this choice and commitment to keeping our data in the EU.

As you can see in the map above, our current [Edge Sites](#heading=h.ju6qeuabiwqz) are spread across the globe, with two of our four current sites in the United States. All of our Edge Sites are provided by Akamai (who recently purchased Linode, our original provider), a US-based company. Since Edge Sites are easier to replace, making a "wrong" decision is much less costly. If we find the location of an Edge Site is no longer desirable, we build a new one and shift traffic to it.

A more detailed analysis is available in [Appendix A: Infrastructure Component Locations & Providers](#heading=h.8pwfpq77ebcr).


# Component-by-component Analysis

The next level down from a Site is a Component. Each Component provides a distinct feature to our users, whether it's directly visible or not.

For each Component, we will assess:



* The impact should we do nothing and this component is affected,
* the likelihood of of the risk being realized, and
* a relative sizing of the effort to reduce the risk both in the short and long term.

We'll then provide a short-term and long-term recommendation for investigations, research, experiments, and actions we can take to mitigate our exposure.


## Service Discovery

FIXME - the table CSS from Google Docs needs to be adjusted
<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


Service discovery is the ability for our users to find Hachyderm in a predictable and human-accessible way. These are the mechanisms that let you type "hachyderm.io" and find Hachyderm. If you had to remember "https://74.207.251.5", you'd probably forget it pretty quickly. 

Externally, Hachyderm depends on DNS for service location via [https://hachyderm.io](https://hachyderm.io). Both our domain name registrar and DNS provider are Amazon Web Services, a US-based corporation. We use [Route 53 Geolocation Routing](https://docs.aws.amazon.com/Route53/latest/DeveloperGuide/routing-policy-geo.html) to direct users to the Edge Site nearest to where the user is accessing Hachyderm.

Furthermore, the .io domain suffix has an [uncertain future with the impending dissolution of the British Indian Ocean Territory](https://thenewstack.io/what-is-the-future-of-the-io-domain/).

Recommendations:



* Sooner
    * Migrate DNS services to a non-US provider, or self-host
    * Migrate hachyderm.io to a non-US registrar
    * Consider leveraging Anycast-based providers, as a comparable Geo DNS provider to Route 53 might be hard to find
    * Research implications of changing/adding new domain to a Mastodon instance (initial research indicates this is not feasible)
* Later
    * Use one of our alternate registered domains in an EU registrar, or register a new hachyderm.tld domain with a non-US registrar and TLD


## Edge Sites


FIXME - the table CSS from Google Docs needs to be adjusted
<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


We currently leverage Akamai (formerly known as Linode), a US-based company for our Edge Sites. Akamai has the advantages of being very affordable, established in many regions, and well-connected through their highly performant Internet backbone.

As previously mentioned, setting up a new Edge Site is a relatively quick operation.

Recommendations:



* Sooner
    * Consider establishing additional edge locations in the US in "blue" states (both current edge nodes in the US are in California and New Jersey)
    * Improve process to spin up CDN nodes & register them
    * Consider establishing process for CDN nodes outside of Linode
    * Adjust logging levels to retain for the minimum needed for day-to-day operations; ensure logs are shipped off-host to the EU for longer-term analysis
* Later
    * Experiment with presenting Hachy through Tor [https://docs.joinmastodon.org/admin/optional/tor/](https://docs.joinmastodon.org/admin/optional/tor/) 
    * Consider establishing additional edge locations (no particular order):
        * Johannesburg, ZA
        * Sao Paulo, BR
        * Mumbai, IN
        * Sydney, AU
        * Toronto, CA


## Media Storage


FIXME - the table CSS from Google Docs needs to be adjusted
<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


Media is stored in Germany in an S3-like service provided by Digital Ocean, a US-based company. Despite the media residing in Germany, because DO is a US company, we could be exposed to service suspensions, although we hypothesize the risk of this is low. Suspension of media would cause a significant impact to our services, as many posts include images, videos, and audio as the main component of their message. We would also lose access to older media, which would disrupt historical preservation of messages. 

We also store our weekly and incremental daily database backups with DO. Loss of our backups would make it difficult for us to restart service if we needed to rebuild the database from scratch.

Due to the size of the content (~23 TiB) and number of files, we consider this a hard-to-move component. We could, however, start storing media in a new location, or replicating to additional locations. Beyond this, we could consider a CDN-style delivery with multiple backing storage S3s. Fortunately, we "hide" the actual storage URL using our media.hachyderm.io domain, so assuming we did the work to move the media, storing media in a different location is a straightforward change.

Like the database, media storage is a bandwidth intensive application, and replicating to multiple providers could be costly due to costs increasing linearly with storage and egress bandwidth costs.

Recommendation:



* Sooner
    * Identify non US-based corporations with S3-compatible storage
    * Replicate database backups to an additional provider
    * Establish a media retention policy and periodically expire Very Old media to keep the total size of our media infrastructure to a somewhat predictable size (vs. growing infinitely)
* Later
    * Consider CDN-style delivery mechanism for media with write-through caching capability to store media in multiple backing stores across multiple providers


## Hachyderm Core (Web, Queues, Database)


FIXME - the table CSS from Google Docs needs to be adjusted
<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


The "core" Mastodon components – Mastodon web, sidekiq queues, redis, and database – are hosted in Hetzner in Frankfurt, Germany. In terms of exposure from the US, we classify this risk as significantly lower than our other providers.

We have recently established real-time replication from our primary database to a secondary read replica. In the event we lost our primary database, we could manually cut over to the replica with minimal disruption to service (est. &lt; 1 hour).

Similarly, each of our redis instances (persistent & cache) are singletons and co-located on servers that perform other tasks like sidekiq. We could establish redis replication for each to improve resilience, and this could be taken further by doing so across multiple providers.

Naturally, as both redis and the database are high-throughput, latency and bandwidth sensitive components in our architecture, homing across multiple providers may prove challenging and unreasonably costly due to egress bandwidth charges.

Recommendation:



* Sooner
    * Improve process to spin up mastodon web, sidekiq, and redis nodes in Hetzner
    * Build redundant mastodon-web and redis nodes
    * Research options for distributed postgresql, and identify potential additional providers that could provide near-local networking for establishing shards/hot spares
    * Research German law requirements for content scanning for adult content
* Later
    * Execute plan for hosting primary and secondary databases in different providers, if found to be necessary and reasonably cost-effective
    * Establish process to spin up mastodon core infra in providers other than Hetzner


## Internal Networking


FIXME - the table CSS from Google Docs needs to be adjusted
<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


Internally, we leverage [Tailscale](https://tailscale.com/), which is a Canada-based corporation. They provide control and data planes, which includes [API](https://tailscale.com/kb/1101/api), [PKI](https://tailscale.com/blog/tls-certs), and [DERP relay](https://tailscale.com/kb/1232/derp-servers) servers. It's possible they could be forced to suspend our service, which would break many internal communication paths. See their [Terms of Use](https://tailscale.com/terms), particularly:


> "4.4	Termination by Tailscale. We reserve the right to terminate these Terms and close your account upon notice to you in the event that we determine we are **required to do so by law**" (emphasis added)

and

> "4.5	Effect of termination. Upon termination of these Terms, Customer's right to access and use the Tailscale Solution will **immediately** end" (emphasis added)

We've asked Tailscale a hypothetical about the ToS [here](https://hachyderm.io/@esk/113438505581243141). Despite their response being somewhat tepid and noncommittal, this is balanced with the fact that Tailscale is a Canadian company, so a US court attempting to enforce an order in Canada would be challenging at best.

Given this context, we do not think there is significant risk from continuing to use Tailscale, and the benefits we get from them outweigh this small risk. In any case, we will research running our own control plane as a potential mitigation against this risk.

Recommendation:



* Short-term
    * Investigate running our own control plane, [like headscale](https://github.com/juanfont/headscale)

We also leverage Hetzner's [vSwitch capability](https://docs.hetzner.com/robot/dedicated-server/network/vswitch/) in our core network. Hetzner; however, is based in Germany and not as exposed to US legislation.


## Observability


<table>
  <tr>
   <td>Impact
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Likelihood
   </td>
   <td>
   </td>
  </tr>
  <tr>
   <td>Short-term effort
   </td>
   <td> 
   </td>
  </tr>
  <tr>
   <td>Long-term effort
   </td>
   <td>
   </td>
  </tr>
</table>


Our observability infrastructure (Prometheus, Grafana, Loki) is currently hosted on a single instance in Linode (esme.hachyderm.io) in their Frankfurt datacenter.

We also leverage Uptime Robot, based in Malta, to perform periodic synthetic checks that alert to our Discord.

Finally, we recently added honeycomb.io as a destination for OTel traces from Mastodon. We are currently storing tracing data in the US; however, Honeycomb offers the option of storing this data in the EU.

Recommendation:



* Short-term
    * Automate stand up of observability infrastructure
    * Move Honeycomb infrastructure to the EU
* Long-term
    * Split components into distinct hosts
    * Build redundancy into critical components


## Other Supporting Tools

There are many tools that aren't directly part of the above categories that help run Hachyderm. Most of these are SaaS solutions provided by US-based companies.



* 1Password
    * Canadian company.
    * Data stored in North Virginia, US.
    * Lower risk.
    * Stores both Nivenly and Hachyderm secrets.
    * Recommendations
        * Consider [moving our instance](https://support.1password.com/move-copy-items/) to 1password.eu, which is in Frankfurt, DE.
        * Consider an open source alternative like [https://github.com/bitwarden/server](https://github.com/bitwarden/server).
    * This would probably be a Nivenly project - not just Hachyderm, but we could act independently.
* Terraform Cloud
    * US company.
    * Lower risk since this isn't a critical component, primarily for convenience & speed.
    * Given Hashicorp's embrace of the BSL license, we should stop using Terraform Cloud.
    * Actions
        * Consider open source alternatives like Atlantis - [https://www.runatlantis.io/guide](https://www.runatlantis.io/guide). 
* Github
    * US company based in California; however, Microsoft ownership could complicate this.
    * Low-medium risk, primarily because Github is our main way to store infrastructure configuration.
    * Our infrastructure configuration is stored at [https://github.com/hachyderm/infrastructure](https://github.com/hachyderm/infrastructure). Today, **this also includes secrets**!
    * In some cases, we use Github Accounts as identity (like for Grafana)
    * Recommendations
        * Short-term, extract secrets from Git and perform full rotation of all secrets.
        * Evaluate [Github Enterprise Cloud](https://github.com/newsroom/press-releases/data-residency-in-the-eu) and its ability to store data in the EU. Would need to consider cost.
        * Consider self-hosted Git like Gitea [https://github.com/go-gitea/gitea](https://github.com/go-gitea/gitea) or Codeberg.
        * Once established, we must always fork projects and libraries we use from the open internet to our self-hosted Git.
* Let's Encrypt
    * ISRG non-profit based in California, US.
    * Low-medium risk.
    * [terms of service](https://community.letsencrypt.org/tos#2)
        * "or to further unlawful acts" → what happens if LGBTQIA+ content becomes "unlawful"?
        * "the Content is not pornographic, does not contain threats or incite violence, and does not violate the privacy or publicity rights of any third party;" —> definition of "pornographic" could change
    * Recommendations
        * Need to identify an EU-based alternative like [https://www.buypass.com/products/tls-ssl-certificates/go-ssl](https://www.buypass.com/products/tls-ssl-certificates/go-ssl) (Needs research!)
        * Could consider establishing our own Nivenly Intermediate CA that trusts up to a EU-based root. Could even consider a Nivenly Root CA based in the EU that we cross-sign this with. (high effort)
* Discord
    * Today, ops are coordinated in Discord, a closed-source, US-based solution.
    * Recommendations
        * Consider a self-hosted, open-source solution like [https://matrix.org/](https://matrix.org/).
    * This would likely be a Nivenly project given the scope (bigger than Hachy).
* Google GSuite
    * Today, Nivenly (and Hachyderm) use Google Workplace for e-mail, calendar, and group e-mails. Many of our notifications and accounts are configured to use Google-based e-mail accounts.
    * In some cases, we use Google Accounts for identity.
    * Recommendations
        * Consider a self-hosted, open-source solution like https://github.com/nextcloud. 
            * Unclear how Nextcloud App Store works re: open-source.
            * Unclear what all experiences/use cases are supported – needs research.
                * Talk - voice/video chat
                * Office - google docs based on libreoffice
                * Groupware - email, calendar, contacts
                * Files - drivers 
    * Not very excited about the notion of hosting/maintaining our own e-mail server.
    * This would likely be a Nivenly project given the scope (bigger than Hachy).
* SSH Access
    * Today, we directly expose 22/tcp to the internet to allow operators to SSH in with SSH keys (no passwords).
    * We also leverage Digital Ocean storage in Frankfurt as a staging place for our sshd public key file. Low risk.
    * Recommendations
        * Configure fail2ban in aggressive mode across all servers.
        * Consider putting SSH behind Tailscale or other SSH-type bastion/proxy.


# Appendix


## Appendix A. Infrastructure Component Locations & Providers

In this table, we make a distinction between assets and the provider itself. For example, for Media Storage, we run Digital Ocean's Spaces product in Frankfurt, Germany. Digital Ocean is a US-based company.

When determining our risk profile for a component, we are making the following broad assumptions:



* The safest posture is for both the asset and providers to be outside of the US.
* The next safest posture is for the asset to be outside the US but operated by a US-based provider.
* The least safe posture is for both the assets and provider to be in the US.

<table>
  <tr>
   <td>
<strong>Component</strong>
   </td>
   <td><strong>Asset Location(s)</strong>
   </td>
   <td><strong>Provider(s) & Country</strong>
   </td>
   <td><strong>Services Provided</strong>
   </td>
  </tr>
  <tr>
   <td>Edge CDN
   </td>
   <td>
<ul>

<li>US - California and New Jersey</li>

<li>DE - Frankfurt</li>

<li>JP - Tokyo</li>

<li>(further expansion planned soon)</li>
</ul>
   </td>
   <td>US - Akamai
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Web
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Sidekiq (Queues)
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Redis
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Streaming
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Postgresql (Database)
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Observability Metrics & System Logs
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>DE - Hetzner
   </td>
   <td>
<ul>

<li>Virtual Machines</li>

<li>Network Backbone</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Mastodon Media Storage
   </td>
   <td>
<ul>

<li>DE - Frankfurt</li>
</ul>
   </td>
   <td>US - DigitalOcean
   </td>
   <td>
<ul>

<li>S3-compatible Storage</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Observability Traces
   </td>
   <td>
<ul>

<li>US</li>
</ul>
   </td>
   <td>US - Honeycomb
   </td>
   <td>
<ul>

<li>Honeycomb OTel Ingestion</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Connectivity Mesh
   </td>
   <td>
<ul>

<li>Various - present on all Hachyderm VMs</li>
</ul>
   </td>
   <td>CA - Tailscale
   </td>
   <td>
<ul>

<li>Virtual Encrypted Network</li>

<li>Machine Identity & Tagging</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Code Version Control
   </td>
   <td>
<ul>

<li>US - Washington + Virginia</li>
</ul>
   </td>
   <td>US - Github/Microsoft
   </td>
   <td>
<ul>

<li>Git Source Control</li>
</ul>
   </td>
  </tr>
  <tr>
   <td>Secrets Management
   </td>
   <td>
<ul>

<li>US - North Virginia</li>
</ul>
   </td>
   <td>CA - 1Password
   </td>
   <td>
<ul>

<li>1Password Vault</li>
</ul>
   </td>
  </tr>
</table>



## Bandwidth Usage

### Hetzner

#### 2022

FIXME - needs image and alt text
![alt_text](images/image3.png "image_tooltip")

#### 2023

FIXME - needs image and alt text
![alt_text](images/image4.png "image_tooltip")

#### 2024

FIXME - needs image and alt text
![alt_text](images/image5.png "image_tooltip")

