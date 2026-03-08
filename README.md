# Every Channel You Need to Stay Current After Kubernetes Certification

[![KubeCon EU 2026](https://img.shields.io/badge/KubeCon_EU-Amsterdam_2026-326CE5?style=flat&logo=kubernetes&logoColor=white)](https://events.linuxfoundation.org/kubecon-cloudnativecon-europe/)
[![Last Verified](https://img.shields.io/badge/verified-March_2026-brightgreen?style=flat)]()
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

> **KubeCon EU 2026 — Cloud Native Theatre — March 24, Amsterdam**
> Speakers: Mumshad Mannambeth & Michael Forrester ([KodeKloud](https://kodekloud.com))

You passed your CKA. Congratulations. Now what?

Kubernetes ships three releases a year. The version you studied for goes end-of-life in 14 months. The newsletters you bookmarked are dead. The social media accounts you followed moved platforms. And the governance structure you barely understood just reorganized.

This repository is the companion resource for our KubeCon EU 2026 talk. Every link, tool, checklist, and reference we mentioned — verified, organized, and maintained.

---

> **Start here:** Just want the essentials?
> Jump to the [5 Must-Have Subscriptions](#the-non-negotiable-five) or grab your [role-based checklist](#by-role).

---

## Table of Contents

**Do something now**
- [The Non-Negotiable Five](#the-non-negotiable-five) — 5 subscriptions that cover security, releases, and deprecations
- [The 30-Minute Weekly System](#the-30-minute-weekly-system) — a low-effort habit that keeps you current
- [By Role](#by-role) — developer, operator, or architect checklists

**Understand the landscape**
- [The Problem](#the-problem) — why your cert goes stale
- [How Kubernetes Ships](#how-kubernetes-ships) — releases, KEPs, and the support window
- [Who Runs Kubernetes](#who-runs-kubernetes) — SIGs, TAGs, and governance
- [The 2025 Landscape Shift](#the-2025-landscape-shift) — what died, what moved, what replaced it

**Go deeper**
- [Your First Contribution](#your-first-contribution) — from zero to merged PR
- [All Channels & Tools](#all-channels--tools) — newsletters, podcasts, social, Slack, mailing lists, deprecation tools
- [Repository Map](#repository-map) — full directory listing

---

## The Non-Negotiable Five

These five subscriptions cover security, releases, and deprecations — the three things that will actually break your production clusters. Subscribe to all five. It takes five minutes.

| # | Channel | What It Does | Link |
|---|---------|-------------|------|
| 1 | kubernetes-security-announce | Fires on CVEs only | [Google Group](https://groups.google.com/g/kubernetes-security-announce) |
| 2 | LWKD | Weekly dev digest | [lwkd.info](https://lwkd.info) |
| 3 | Kubernetes Blog RSS | Release announcements, deprecations, security | [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml) |
| 4 | GitHub "Releases Only" watch | Every patch and minor release | [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) |
| 5 | Official CVE JSON feed | Machine-readable vulnerability feed | [Official CVE Feed](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/) |

> Details and setup instructions: [`channels/essential-five.md`](channels/essential-five.md)

---

## The 30-Minute Weekly System

| Cadence | Time | What to Do |
|---------|------|-----------|
| **Once** | 5 min | Subscribe to the Non-Negotiable Five (above) |
| **Weekly** | 20 min | Read LWKD + scan 1–2 SIG Slack channels for your role |
| **Monthly** | 30 min | Wisdom of the Cloud + Kubernetes blog scan |
| **Quarterly** | 1 hr | Run pluto + kubent + review upcoming release KEPs |

### By Role

| Role | Follow These SIGs | Checklist |
|------|-------------------|-----------|
| **Developers** | SIG Apps, SIG API Machinery, SIG CLI | [`developer-checklist.md`](checklists/developer-checklist.md) |
| **Operators** | SIG Node, SIG Network, SIG Storage, SIG Auth | [`operator-checklist.md`](checklists/operator-checklist.md) |
| **Architects** | SIG Architecture, CNCF TOC notes, Alpha-stage KEPs | [`architect-checklist.md`](checklists/architect-checklist.md) |

> Tool guides: [`pluto`](tools/pluto-guide.md) | [`kubent`](tools/kubent-guide.md) | [`RSS setup`](tools/rss-setup.md)

---

## The Problem

At KodeKloud, we've trained over a million students for Kubernetes certifications. The number one message we get after someone passes: *"I passed. Now what?"*

Your certification is a snapshot. It proves you understood Kubernetes at one point in time. But Kubernetes doesn't stop moving. v1.32 went end-of-life on February 28, 2026. v1.35 shipped December 17, 2025. v1.36 is targeting April 22, 2026. If you're not actively keeping up, you're falling behind — and the gap compounds.

The good news: you don't need to spend hours every week. You need a system, the right subscriptions, and a mental model for how the ecosystem is organized.

---

## How Kubernetes Ships

Kubernetes follows a predictable cadence: **3 releases per year**, each on roughly a **15-week cycle**, with **14 months of patch support** after release.

| Version | Name | Release Date | EOL |
|---------|------|-------------|-----|
| v1.35 | Timbernetes | Dec 17, 2025 | Feb 2027 |
| v1.34 | Of Wind & Will | Aug 2025 | Oct 2026 |
| v1.33 | Octarine | Apr 2025 | Jun 2026 |
| v1.32 | Penelope | Dec 2024 | **Feb 28, 2026 (EOL)** |

**v1.36** code freeze: March 18, 2026. Target release: April 22, 2026.

Every release ships with a detailed blog post listing new features, deprecations, and removals. That blog post is worth more than any vendor webinar. Read it.

New features go through the **KEP (Kubernetes Enhancement Proposal)** process — Alpha (off by default) → Beta (on by default) → Stable (GA). Track them at [kep.k8s.io](https://kubernetes.dev/resources/keps/) or filter release notes at [relnotes.k8s.io](https://relnotes.k8s.io).

> Full release calendar: [`reference/release-calendar.md`](reference/release-calendar.md)

---

## Who Runs Kubernetes

**Kubernetes is run by 24 Special Interest Groups (SIGs).** Each SIG owns a specific area — the code, the tests, the docs, the roadmap. The CNCF provides infrastructure (CI/CD, legal entity, conferences) but doesn't tell SIGs what to build.

| SIG | Owns | | SIG | Owns |
|-----|------|-|-----|------|
| SIG Network | All networking | | SIG Storage | PVs, CSI |
| SIG Node | The kubelet | | SIG CLI | kubectl |
| SIG Auth | RBAC, authn | | SIG Release | Release process |
| SIG Apps | Workload APIs | | SIG etcd | etcd (newest SIG) |

> Full list with Slack channels, meetings, and leads: [`reference/all-24-sigs.md`](reference/all-24-sigs.md)

**Governance at a glance:** 7-person Steering Committee · 11-person TOC · 5 CNCF TAGs · 12 Working Groups

> **SIGs vs TAGs:** SIGs own Kubernetes code and report to Steering. CNCF TAGs are advisory only and report to the TOC. They are not the same thing — the CNCF renamed theirs from "SIGs" to "TAGs" to fix the confusion.

> Details: [`reference/governance-quick-ref.md`](reference/governance-quick-ref.md) | [`reference/cncf-tags.md`](reference/cncf-tags.md) | [`reference/working-groups.md`](reference/working-groups.md)

---

## The 2025 Landscape Shift

If you're following guides written before 2025, many of your bookmarks are broken.

| Status | What | Details |
|--------|------|---------|
| Dead | **KubeWeekly** newsletter | Last issue #434, May 2025 |
| Dead | **"Ship It"** podcast | Rebranded to "Fork Around and Find Out" |
| Archived | Old CNCF TAG Slack channels | 8 TAGs became 5 (June 2025) |
| Uncertain | **Kubernetes Slack** | Salesforce threatened downgrade Jun 2025, then cancelled. Still active. |
| Moved | **Official social** | Bluesky is primary (@kubernetes.io). X/Twitter deprioritized. |
| New | **Wisdom of the Cloud** | Replaced KubeWeekly. Monthly. [cncf.io/newsletter](https://cncf.io/newsletter) |
| Current | **LWKD** | Still the best weekly digest. [lwkd.info](https://lwkd.info) |

> Full breakdown: [`what-changed-2025/2025-landscape-changes.md`](what-changed-2025/2025-landscape-changes.md)

---

## Your First Contribution

1. **Join Slack** — [slack.k8s.io](https://slack.k8s.io) → `#kubernetes-contributors` · `#sig-contribex` · your SIG's channel
2. **SIG Meet & Greet** — Lunch session in the Project Pavilion at every KubeCon. Just walk up.
3. **Claim a good first issue** — [go.k8s.io/good-first-issue](https://go.k8s.io/good-first-issue) → comment `/assign` and it's yours
4. **New Contributor Orientation** — 3rd Tuesday of every month at [kubernetes.dev/docs/orientation/](https://kubernetes.dev/docs/orientation/)
5. **Structured programs** — [LFX Mentorship](https://mentoring.cncf.io) (187 successful projects in 2025) · GSoC · Outreachy · Release Team Shadow

> Practice first: [contributor-playground](https://github.com/kubernetes-sigs/contributor-playground)
> Full guides: [`contributing/`](contributing/)

---

## All Channels & Tools

| Category | Guide | Highlights |
|----------|-------|------------|
| Must-have subscriptions | [`channels/essential-five.md`](channels/essential-five.md) | The 5 non-negotiable feeds |
| Newsletters | [`channels/newsletters.md`](channels/newsletters.md) | LWKD, Wisdom of the Cloud |
| Podcasts | [`channels/podcasts.md`](channels/podcasts.md) | Kubernetes Podcast, FAFO |
| Social media | [`channels/social-media.md`](channels/social-media.md) | Bluesky, X, LinkedIn, YouTube |
| Slack channels | [`channels/slack-channels.md`](channels/slack-channels.md) | Key channels by role |
| Mailing lists | [`channels/mailing-lists.md`](channels/mailing-lists.md) | Google Groups, SIG lists |
| Deprecation scanning | [`tools/pluto-guide.md`](tools/pluto-guide.md) | Detect deprecated APIs in manifests |
| Cluster scanning | [`tools/kubent-guide.md`](tools/kubent-guide.md) | Detect deprecations in live clusters |
| RSS setup | [`tools/rss-setup.md`](tools/rss-setup.md) | Feed readers and URLs |

---

## Repository Map

```
├── checklists/
│   ├── developer-checklist.md      Subscriptions and SIGs for developers
│   ├── operator-checklist.md       Subscriptions and SIGs for operators
│   └── architect-checklist.md      Subscriptions and SIGs for architects
│
├── reference/
│   ├── all-24-sigs.md              Every SIG: Slack, meetings, leads
│   ├── cncf-tags.md                The 5 restructured TAGs
│   ├── governance-quick-ref.md     Steering, TOC, Governing Board
│   ├── working-groups.md           Active Working Groups
│   └── release-calendar.md         v1.32–v1.36 dates and support matrix
│
├── tools/
│   ├── pluto-guide.md              Detect deprecated API versions
│   ├── kubent-guide.md             Detect deprecations in running clusters
│   └── rss-setup.md                RSS reader setup
│
├── channels/
│   ├── essential-five.md           The 5 must-have subscriptions
│   ├── newsletters.md              LWKD, Wisdom of the Cloud
│   ├── podcasts.md                 Kubernetes Podcast, FAFO
│   ├── social-media.md             Bluesky, X, LinkedIn
│   ├── slack-channels.md           Key Slack channels by role
│   └── mailing-lists.md            Google Groups and SIG mailing lists
│
├── contributing/
│   ├── first-contribution.md       Step-by-step path to your first PR
│   ├── sig-meet-and-greet.md       KubeCon SIG sessions
│   ├── mentorship-programs.md      LFX, GSoC, Outreachy
│   ├── new-contributor-orientation.md  Monthly sessions + self-paced course
│   └── josh-berkus-and-contribex.md    SIG ContribEx and community connectors
│
├── what-changed-2025/
│   └── 2025-landscape-changes.md   What died, what moved, what replaced it
│
├── slides/                         Presentation slides (added post-talk)
│
├── talk/
│   └── script.md                   Full talk script
│
├── CONTRIBUTING.md                 How to contribute to this repo
└── README.md                       This file
```

---

## Contributing

Found a broken link? Have a resource to add? See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## Five Things to Remember

1. **Your cert is a snapshot.** Kubernetes ships three times a year.
2. **SIGs own everything.** Follow the SIG, not the vendor blog.
3. **The information landscape changed in 2025.** Update your bookmarks.
4. **Thirty minutes a week.** That's all it takes.
5. **If you want to contribute, the path exists and it starts today.**

---

<sub>Last verified: March 2026. Content is reviewed before each KubeCon. Found something outdated? [Open an issue.](../../issues)</sub>
