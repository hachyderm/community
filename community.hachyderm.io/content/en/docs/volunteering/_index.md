---
title: "Volunteering with Hachyderm"
linkTitle: "Volunteering"
weight: 2
description: >
  So you're interested in voluntering with Hachyderm?
---

{{% pageinfo %}}
<p align="center"><strong>[Please join us at our FOSDEM BOF!](https://fosdem.org/2026/schedule/event/3C3SX8-hachyderm-nivenly-bof/)</strong> 🎉</p>
{{% /pageinfo %}}

Hachyderm is looking for volunteers across four teams: Moderation, Infrastructure, and Security. Below you'll find what each team does and what we're looking for.

## Moderation

At Hachyderm, moderation is mission-critical infrastructure. Our moderators focus on community care, education, and de-escalation rather than reactive enforcement. The goal is about creating conditions where people have improved autonomy over their own experience, and with less hypervigilance, not to control what they see.

We have two tracks for moderation volunteers:

**Community Stewardship** Supporting Hachydermians in being their best selves and good Fediverse citizens. This includes growth-oriented interventions, conflict de-escalation, documentation, and programs like our Trusted Reporter Program.

**Threat Intelligence** Proactive, research-based moderation. Identifying harassment campaigns, scams, and abusive federation patterns before they reach our community.

Moderators in both tracks can also contribute to **abusability testing** the software. This is how we examine the ways that the platform's legitimate features can be gamed, misused, or exploited for harm. This is distinct from security vulnerability testing; it's about understanding how normal functionality can be weaponized (e.g. using report systems for targeted harassment, exploiting federation for coordinated attacks). Moderators are well-positioned for this work because they see how features get misused in practice.

Volunteers can contribute to either or both tracks.

**We're especially interested in:** For community stewardship, we're always interested in mental health professionals willing to volunteer as moderators or to assist with policy drafting and review. This helps us build trauma informed moderation practices. For threat intelligence, we're always interested in people with platform experience as well as experience testing software for human misuses.

## Infrastructure

Our infrastructure team keeps Hachyderm running. This means traditional server administration, incluidng: monitoring, maintenance, scaling, and incident response as well as documentation, automation, and building tooling alongside our moderation team to augment or patch existing tools. Functional patches may be pushed upstream.

**What infrastructure volunteers do:**

- **Operations** Monitoring system health, responding to incidents, managing backups and disaster recovery, and scaling resources as needed.
- **Automation & Configuration** Improving deployment processes, maintaining configuration management, and reducing manual toil.
- **Documentation** Creating and maintaining runbooks, architecture diagrams, and onboarding materials so knowledge isn't siloed.
- **Tooling** Collaborating with moderation to build tools that support community stewardship—bridging technical operations and community care.

**Technologies we work with / are interested in:** Linux (Debian, Arch), systemd, Docker, Grafana, Tailscale, and OAuth technologies like Keycloak. The Mastodon stack includes Ruby on Rails, PostgreSQL, Redis, Sidekiq, Node.js (streaming API), and S3-compatible object storage.

**We're especially interested in:** Current or aspiring contributors to [Mastodon](https://github.com/mastodon) (Ruby/Rails, React) and/or [Bonfire](https://github.com/bonfire-networks) (Elixir/Phoenix).

## Security

Hachyderm's security team works across two tracks: one technology focused, the other human focused. Both are essential to keeping our infrastructure resilient and our members safe.

**Infrastructure Security** Supporting the security of our servers and services. This includes hardening configurations, monitoring for vulnerabilities, incident response, and abuse testing (identifying technical vulnerabilities that could be exploited). Assisting with finding and patching security vulnerabilities or backlog items on [Mastodon](https://github.com/mastodon) or [Bonfire](https://github.com/bonfire-networks) is a plus.

**Moderation Security** R&D of tools that support our moderation team's threat intelligence and abusability testing work. This bridges technical security expertise with community protection—building capabilities to identify how platform features can be weaponized, and developing tools to detect and respond to harassment campaigns, coordinated attacks, and other threats before they reach our members.

Volunteers can contribute to either or both tracks.

**Technologies and skills:** Penetration testing, vulnerability assessment, Linux hardening, container security, OAuth/authentication systems, OSINT techniques, scripting (Python, Ruby, shell), and familiarity with ActivityPub or the Mastodon stack.

**We're especially interested in:** Security professionals with experience in application security, threat modeling, or building defensive tooling for online communities.

