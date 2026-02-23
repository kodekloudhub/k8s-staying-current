# Every Channel You Need to Stay Current After Kubernetes Certification

> **KubeCon EU 2026 — Cloud Native Theatre**
> March 24, 2026 — Amsterdam
> Speakers: Mumshad Mannambeth & Michael Forrester ([KodeKloud](https://kodekloud.com))

You passed your CKA. Congratulations. Now what?

Kubernetes ships three releases a year. The version you studied for your certification goes end-of-life in 14 months. The newsletters you bookmarked are dead. The social media accounts you followed moved platforms. And the governance structure you barely understood just reorganized.

This repository is the companion resource for our KubeCon EU 2026 talk. It contains every link, tool, checklist, and reference we mentioned — verified, organized, and maintained. Whether you attended the talk or found this repo on your own, everything you need to stay current is here.

---

## Table of Contents

- [The Problem](#the-problem)
- [How Kubernetes Ships](#how-kubernetes-ships)
- [Who Runs Kubernetes](#who-runs-kubernetes)
- [The 2025 Landscape Shift](#the-2025-landscape-shift)
- [The Non-Negotiable Five](#the-non-negotiable-five)
- [The 30-Minute Weekly System](#the-30-minute-weekly-system)
- [Your First Contribution](#your-first-contribution)
- [Repository Contents](#repository-contents)
- [Contributing](#contributing)

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
| v1.32 | — | — | Feb 28, 2026 (EOL) |

**v1.36** code freeze: March 18, 2026. Target release: April 22, 2026.

Every release ships with a detailed blog post listing new features, deprecations, and removals. That blog post is worth more than any vendor webinar. Read it.

New features go through the **KEP (Kubernetes Enhancement Proposal)** process:
- **Alpha** — Off by default. Architects evaluating direction.
- **Beta** — On by default. Operators should plan for this.
- **Stable** — GA. Production-ready for everyone.

v1.35 shipped 60 enhancements: 17 Stable, 19 Beta, 22 Alpha. Track them at [github.com/kubernetes/enhancements](https://github.com/kubernetes/enhancements).

→ Full release calendar: [`reference/release-calendar.md`](reference/release-calendar.md)

---

## Who Runs Kubernetes

### 24 SIGs Own Everything

Kubernetes is organized into **24 Special Interest Groups (SIGs)**. Each SIG owns a specific area of the project — the code, the tests, the documentation, the roadmap. The newest is SIG etcd, established November 2023.

**CNCF is the landlord. Kubernetes arranges its own furniture.** The CNCF provides infrastructure (CI/CD, legal entity, conferences) but doesn't tell SIGs what code to write.

| SIG | Owns |
|-----|------|
| SIG Network | All networking code |
| SIG Node | The kubelet |
| SIG Auth | RBAC, authentication |
| SIG Apps | Workload APIs (Deployments, StatefulSets) |
| SIG Release | The release process |
| SIG Storage | PVs, CSI drivers |
| SIG CLI | kubectl |
| SIG etcd | etcd (newest SIG) |

→ Full list: [`reference/all-24-sigs.md`](reference/all-24-sigs.md)

### Governance

- **7-person Steering Committee** — 4 new members elected November 2025
- **11-person Technical Oversight Committee (TOC)** — handles CNCF project acceptance and maturity
- **5 CNCF TAGs** — advisory groups (not the same as SIGs!)
- **12 active Working Groups** — cross-cutting concerns

→ Details: [`reference/governance-quick-ref.md`](reference/governance-quick-ref.md)

### SIGs vs TAGs — They Are Not the Same

| | Kubernetes SIGs | CNCF TAGs |
|-|----------------|-----------|
| **Function** | Own code | Advisory only |
| **Count** | 24 groups | 5 groups (restructured May 2025) |
| **Report to** | Steering Committee | TOC |

The CNCF originally called their advisory groups "SIGs" too. They renamed them to TAGs to fix the confusion. In May 2025, they restructured from 8 TAGs down to 5. The current TAGs: **Developer Experience, Infrastructure, Operational Resilience, Security and Compliance, Workloads Foundation**.

→ Details: [`reference/cncf-tags.md`](reference/cncf-tags.md)

---

## The 2025 Landscape Shift

If you're following guides written before 2025, many of your bookmarks are broken.

### What Died
- **KubeWeekly newsletter** — Last issue #434, May 2025
- **"Ship It" podcast** — Rebranded to "Fork Around and Find Out"
- **Old CNCF TAG Slack channels** — Archived when 8 TAGs became 5 (June 2025)

### What Changed
- **Kubernetes Slack** — Salesforce threatened a downgrade in June 2025, then cancelled it. Still active. Future uncertain.
- **Social media** — Bluesky is the official primary channel. v1.35 release blog: "Follow us on Bluesky @kubernetes.io." X/Twitter is deprioritized.

### What's Current
- **Wisdom of the Cloud** — Replaced KubeWeekly. Monthly. [cncf.io/newsletter](https://cncf.io/newsletter)
- **LWKD** — Still the best weekly digest. [lwkd.info](https://lwkd.info)
- **Bluesky** — @kubernetes.io

→ Full breakdown: [`what-changed-2025/2025-landscape-changes.md`](what-changed-2025/2025-landscape-changes.md)

---

## The Non-Negotiable Five

These five subscriptions cover security, releases, and deprecations — the three things that will actually break your production clusters.

| # | Channel | What It Does | Link |
|---|---------|-------------|------|
| 1 | kubernetes-security-announce | Fires on CVEs only | [Google Group](https://groups.google.com/g/kubernetes-security-announce) |
| 2 | LWKD | Weekly dev digest | [lwkd.info](https://lwkd.info) |
| 3 | Kubernetes Blog RSS | Release announcements, deprecations, security | [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml) |
| 4 | GitHub "Releases Only" watch | Every patch and minor release | [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) |
| 5 | Official CVE JSON feed | Machine-readable vulnerability feed | [Official CVE Feed](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/) |

→ Details: [`channels/essential-five.md`](channels/essential-five.md)

---

## The 30-Minute Weekly System

| Cadence | Time | What to Do |
|---------|------|-----------|
| **Weekly** | 20 min | Read LWKD + scan 1–2 SIG Slack channels for your role |
| **Monthly** | 30 min | Wisdom of the Cloud + Kubernetes blog scan |
| **Quarterly** | 1 hr | Run pluto + kubent + review upcoming release KEPs |
| **Once** | 5 min | Subscribe to the Non-Negotiable Five |

### By Role

| Role | Follow These SIGs |
|------|------------------|
| **Developers** | SIG Apps, SIG API Machinery, SIG CLI |
| **Operators** | SIG Node, SIG Network, SIG Storage, SIG Auth |
| **Architects** | SIG Architecture, CNCF TOC notes, Alpha-stage KEPs |

→ Role checklists: [`checklists/`](checklists/)
→ Tool guides: [`tools/`](tools/)

---

## Your First Contribution

The path to contributing to Kubernetes is clear and well-supported.

1. **Join Slack** — [slack.k8s.io](https://slack.k8s.io)
   - `#kubernetes-contributors` | `#sig-contribex` | your SIG's channel

2. **SIG Meet & Greet** — Happens at every KubeCon
   - Lunch session in the Project Pavilion. Just walk up.

3. **Claim a good first issue** — [go.k8s.io/good-first-issue](https://go.k8s.io/good-first-issue)
   - Comment `/assign` and it's yours. Practice at [contributor-playground](https://github.com/kubernetes-sigs/contributor-playground).

4. **New Contributor Orientation** — 3rd Tuesday of every month
   - [kubernetes.dev/docs/orientation/](https://kubernetes.dev/docs/orientation/)
   - Self-paced course: [kubernetes.dev/docs/onboarding](https://kubernetes.dev/docs/onboarding)

5. **Structured programs**
   - Release Team Shadow — watch `#sig-release` on Slack
   - [LFX Mentorship](https://mentoring.cncf.io) — 187 successful projects in 2025
   - GSoC / Outreachy — annual Kubernetes projects

→ Full guides: [`contributing/`](contributing/)

---

## Repository Contents

```
├── checklists/
│   ├── developer-checklist.md      Role-specific subscription guide
│   ├── operator-checklist.md       Role-specific subscription guide
│   └── architect-checklist.md      Role-specific subscription guide
│
├── reference/
│   ├── all-24-sigs.md              Every SIG with Slack, meetings, leads
│   ├── cncf-tags.md                The 5 restructured TAGs
│   ├── governance-quick-ref.md     Steering, TOC, Governing Board
│   ├── working-groups.md           12 active Working Groups
│   └── release-calendar.md         v1.32–v1.36 dates and support matrix
│
├── tools/
│   ├── pluto-guide.md              Detect deprecated API versions in manifests
│   ├── kubent-guide.md             Detect deprecations in running clusters
│   └── rss-setup.md                RSS reader setup for Kubernetes feeds
│
├── channels/
│   ├── essential-five.md           The 5 must-have subscriptions
│   ├── newsletters.md              LWKD, Wisdom of the Cloud, and more
│   ├── podcasts.md                 Kubernetes Podcast, FAFO, and more
│   ├── social-media.md             Bluesky, X, LinkedIn official accounts
│   ├── slack-channels.md           Key Slack channels by role
│   └── mailing-lists.md            Google Groups and SIG mailing lists
│
├── contributing/
│   ├── first-contribution.md       Step-by-step path to your first PR
│   ├── sig-meet-and-greet.md       What to expect at KubeCon SIG sessions
│   ├── mentorship-programs.md      LFX, GSoC, Outreachy details
│   ├── new-contributor-orientation.md  Monthly sessions + self-paced course
│   └── josh-berkus-and-contribex.md    SIG ContribEx and community connectors
│
├── what-changed-2025/
│   └── 2025-landscape-changes.md   What died, what moved, what replaced it
│
├── slides/                         Presentation slides (uploaded post-talk)
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
