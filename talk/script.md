# Talk Script: Every Channel You Need to Stay Current After Kubernetes Certification

**Event:** KubeCon EU 2026 — Cloud Native Theatre
**Date:** March 24, 2026 — Amsterdam
**Duration:** 20 minutes
**Speakers:** Mumshad Mannambeth & Michael Forrester (KodeKloud)
**Format:** Role-play conversation

---

## Format Notes

- **Mumshad** plays a recently certified Kubernetes engineer — just passed CKA, excited but overwhelmed, doesn't know where to go next. He asks the questions the audience is already thinking.
- **Michael** plays the CNCF educator — experienced guide who's been in the ecosystem for years and cuts through the noise.
- **Minimal slides.** Slides are backdrops — a few key visuals, a couple of reference tables, the QR code. The conversation IS the talk. Everything detailed goes in the GitHub repo.

---

## Story Arc

| Act | Theme | Time |
|-----|-------|------|
| **Act 1** — "I Passed. Now What?" | Mumshad sets up the problem. Certified, proud, immediately lost. Michael explains why — the cert is a snapshot, not a subscription. | 5 min |
| **Act 2** — "Show Me How This Works" | Progressively deeper questions. How does K8s ship? Who decides what goes in? Where do I find what changed? Each answer builds the mental model. | 8 min |
| **Act 3** — "Make It Actionable" | Mumshad gets practical. What do I subscribe to? I don't have time. I want to contribute. Michael gives the system, tools, and specific next steps — including events at KubeCon this week. | 5 min |
| **Close + QR Code** | Both speakers summarize. Everything goes in the repo. Audience scans the code. | 2 min |

---

## Scene-by-Scene Script

### SCENE 1: The Setup
**Time: 1:30**
**SLIDE:** Title card — talk name, speakers, KodeKloud logo, Cloud Native University

**Mumshad:** *(to audience)* Hey everyone! So, at KodeKloud we've trained over a million students for Kubernetes certifications. And the number one message we get after someone passes is — *"I passed. Now what?"*

That's what we're going to answer today. And we're going to do it a little differently.

I'm going to pretend I just passed my CKA. I'm confused, I'm overwhelmed, and I'm going to ask Michael every question I know you're thinking.

Michael — you ready?

**Michael:** Let's do it.

---

### SCENE 2: "My Cert Is Already Expiring?"
**Time: 2:00**
**SLIDE:** Release timeline — v1.33 through v1.36 with dates, "3 releases/year," "14 months of patch support"

```
HOW KUBERNETES SHIPS

3 releases/year | ~15-week cycles | 14 months of patch support

  v1.35  Timbernetes    Dec 17, 2025     EOL Feb 2027
  v1.34  Of Wind & Will Aug 2025         EOL Oct 2026
  v1.33  Octarine       Apr 2025         EOL Jun 2026
  v1.32  ⚠ END OF LIFE  Feb 28, 2026

  v1.36 -> Code Freeze: Mar 18 | Target: Apr 22, 2026
```

**Mumshad:** So I studied for months, I passed my CKA, and you're telling me the version I studied is already old?

**Michael:** Kubernetes ships three releases a year. Each release has about a 15-week cycle, and once it ships, you get 14 months of patch support. After that, it's end of life — no more security fixes.

v1.32? That went end of life February 28th. Three weeks ago. If you studied on v1.32, the APIs you used are still there — but some of them are deprecated, and if you're running v1.32 in production, you're unpatched.

**Mumshad:** So my certification is like a snapshot?

**Michael:** Exactly. It proves you understood Kubernetes at one point in time. But Kubernetes doesn't stop. v1.35 shipped December 17th. v1.36 is targeting April 22nd — that's less than a month from now. And here's the thing nobody tells you: the release blog post is worth more than any vendor webinar. Every release ships with a detailed blog listing what's new, what's deprecated, and what was removed.

---

### SCENE 3: "Who Actually Runs Kubernetes?"
**Time: 2:30**
**SLIDE:** SIG structure diagram — "24 SIGs Own Everything" with examples

```
24 SIGs OWN EVERYTHING

SIG Network    → all networking code
SIG Node       → the kubelet
SIG Auth       → RBAC, authentication
SIG Apps       → workload APIs (Deployments, StatefulSets)
SIG Release    → the release process
SIG etcd       → newest SIG (est. Nov 2023)
SIG Storage    → PVs, CSI drivers
SIG CLI        → kubectl

CNCF is the landlord. Kubernetes arranges its own furniture.
```

**Mumshad:** OK so if Kubernetes moves this fast, who's actually driving? Is it Google? Is it the CNCF?

**Michael:** Neither. It's 24 Special Interest Groups — SIGs. Each SIG owns a specific area of the project. SIG Network owns all the networking code. SIG Node owns the kubelet. SIG Auth owns RBAC and authentication.

And here's the mental model that matters: **CNCF is the landlord. Kubernetes arranges its own furniture.** The CNCF provides the infrastructure — the CI/CD, the legal entity, the conference you're sitting in right now. But it doesn't tell the SIGs what code to write. That comes from within the community.

**Mumshad:** Wait, I thought there were 21 SIGs?

**Michael:** There were. Older docs are wrong. It's 24 now. The newest is SIG etcd, established November 2023. And these SIGs report to a 7-person Steering Committee — 4 new members were elected just last November. There's also an 11-person Technical Oversight Committee, or TOC, but the TOC handles project acceptance and maturity ratings — it doesn't tell Kubernetes what to build.

---

### SCENE 4: "But Wait — What About TAGs?"
**Time: 1:30**
**SLIDE:** SIGs vs TAGs comparison

```
KUBERNETES SIGs ≠ CNCF TAGs

     K8s SIGs                  CNCF TAGs
     Own code                  Advisory only
     24 groups                 5 groups (restructured May 2025)
     Report to Steering        Report to TOC

THE 5 CNCF TAGs:
  Developer Experience | Infrastructure | Operational Resilience
  Security and Compliance | Workloads Foundation
```

**Mumshad:** Hold on. I keep seeing "TAGs" and "SIGs" and I'm getting confused. Are they the same thing?

**Michael:** No, and this trips everyone up. The CNCF originally called their advisory groups "SIGs" too — same name, completely different thing. They renamed them to TAGs — Technical Advisory Groups — specifically to fix this confusion.

And in May 2025, they restructured from 8 TAGs down to 5. TAG App Delivery, TAG Runtime, TAG Environmental Sustainability — gone. The old Slack channels got archived in June 2025. So if you're following a guide that mentions those, it's outdated.

The five current TAGs are: Developer Experience, Infrastructure, Operational Resilience, Security and Compliance, and Workloads Foundation.

---

### SCENE 5: "How Do Features Actually Ship?"
**Time: 1:30**
**SLIDE:** KEP lifecycle — Alpha → Beta → Stable

```
HOW FEATURES SHIP: THE KEP PROCESS

Kubernetes Enhancement Proposal (KEP)
  Alpha  → Off by default. Architects evaluating direction.
  Beta   → On by default. Operators plan for this.
  Stable → GA. Everyone — it's production-ready.

v1.35 shipped 60 enhancements:
  17 Stable | 19 Beta | 22 Alpha

Track them: github.com/kubernetes/enhancements
```

**Mumshad:** OK, so SIGs own the code. But how do new features actually get in?

**Michael:** Through KEPs — Kubernetes Enhancement Proposals. A KEP starts as an idea, goes through Alpha where it's off by default, then Beta where it's on by default, then Stable which is GA — production-ready.

v1.35 shipped 60 enhancements: 17 went Stable, 19 went Beta, 22 new Alphas. In-Place Pod Resize — being able to change resource limits without restarting the pod — that went GA in v1.35. That's a big deal.

**Mumshad:** Where do I track these?

**Michael:** github.com/kubernetes/enhancements. Every KEP is there. And the release blog post summarizes all of them — that's why I keep saying, read the blog.

---

### SCENE 6: "Half My Bookmarks Are Broken"
**Time: 2:00**
**SLIDE:** "What Changed in 2025"

```
THE 2025 LANDSCAPE SHIFT

✗ KubeWeekly newsletter    → Dead. Last issue May 2025 (#434)
✗ Ship It podcast          → Dead. Now "Fork Around and Find Out"
✗ Old CNCF TAG Slack       → Archived. 8 TAGs became 5.

⚠ Kubernetes Slack         → Downgrade threatened, then CANCELLED
                              Still on Slack. Future uncertain.

✓ Bluesky                  → NOW the official social channel
                              v1.35 blog: "Follow us on Bluesky @kubernetes.io"
✓ Wisdom of the Cloud      → Replaced KubeWeekly (monthly, cncf.io/newsletter)
✓ LWKD                     → Still the best weekly digest (lwkd.info)
```

**Mumshad:** OK so I go to Google, I search "how to stay current with Kubernetes," and half the links I find recommend things that don't exist anymore.

**Michael:** Yeah, 2025 was a landscape shift. KubeWeekly — the newsletter everyone used to recommend — is dead. Last issue was number 434, May 2025. The replacement is "Wisdom of the Cloud," a monthly newsletter from CNCF.

"Ship It" — the podcast — rebranded to "Fork Around and Find Out." The old CNCF TAG Slack channels got archived when they restructured.

And then there was the Slack scare. In June 2025, Salesforce threatened to downgrade the Kubernetes Slack workspace — we're talking about 300,000+ members. The community mobilized, and the downgrade was cancelled. Slack is still the primary real-time channel. But the future is uncertain.

**Mumshad:** What about social media?

**Michael:** Bluesky. That's the official channel now. When v1.35 shipped, the release blog post said "Follow us on Bluesky @kubernetes.io." X is deprioritized. If you're following the Kubernetes account on Twitter and wondering why it's quiet — that's why.

---

### SCENE 7: "What Do I Actually Subscribe To?"
**Time: 1:30**
**SLIDE:** "The Non-Negotiable Five"

```
THE NON-NEGOTIABLE FIVE

1. kubernetes-security-announce    (Google Group — fires on CVEs only)
2. LWKD                           (lwkd.info — weekly dev digest)
3. Kubernetes Blog RSS             (kubernetes.io/feed.xml)
4. GitHub "Releases Only" watch    (kubernetes/kubernetes repo)
5. Official CVE JSON feed          (k8s.io/docs/reference/issues-security/
                                    official-cve-feed/)
```

**Mumshad:** OK Michael, just tell me — what do I actually subscribe to?

**Michael:** Five things. Non-negotiable.

One: kubernetes-security-announce. It's a Google Group. Low traffic — it only fires on CVEs. But when it fires, you need to know. Remember IngressNightmare? The CVE cluster that hit Ingress NGINX? If you were on this list, you knew before the blog posts started flying.

Two: LWKD — Last Week in Kubernetes Development. A weekly digest at lwkd.info. Best signal-to-noise ratio in the ecosystem.

Three: The Kubernetes Blog RSS feed. kubernetes.io/feed.xml. Release announcements, deprecation notices, security advisories — they all land here.

Four: GitHub "Releases Only" watch on the kubernetes/kubernetes repo. You'll get notified for every patch and minor release.

Five: The official CVE JSON feed. Machine-readable, automatable, and it's the source of truth for Kubernetes vulnerabilities.

These five cover security, releases, and deprecations — the three things that will actually break your production clusters.

---

### SCENE 8: "I Don't Have Time For This"
**Time: 1:30**
**SLIDE:** "30 Minutes/Week" system + role filters

```
THE 30-MINUTE WEEKLY SYSTEM

WEEKLY (20 min):  Read LWKD + scan 1-2 SIG Slack channels for your role
MONTHLY (30 min): Wisdom of the Cloud + Kubernetes blog scan
QUARTERLY (1 hr): Run pluto + kubent + review upcoming release KEPs

SUBSCRIBE ONCE:   security-announce, GitHub releases, CVE feed

BY ROLE:
  Developers  → SIG Apps, SIG API Machinery, SIG CLI
  Operators   → SIG Node, SIG Network, SIG Storage, SIG Auth
  Architects  → SIG Architecture, CNCF TOC notes, Alpha-stage KEPs
```

**Mumshad:** Five subscriptions, SIGs, TAGs, blogs, podcasts — Michael, I have a day job. I can't spend hours on this every week.

**Michael:** You don't need to. Here's the system.

Weekly: 20 minutes. Read LWKD and scan one or two SIG Slack channels relevant to your role.

Monthly: 30 minutes. Read Wisdom of the Cloud and do a quick scan of the Kubernetes blog.

Quarterly: One hour. Run pluto and kubent against your clusters — pluto checks your manifests for deprecated API versions, kubent checks your running cluster. Then review the KEPs for the upcoming release.

And the five subscriptions? Subscribe once. They come to you.

**Mumshad:** What about filtering by role?

**Michael:** If you're a developer — follow SIG Apps, SIG API Machinery, and SIG CLI. If you're an operator — SIG Node, SIG Network, SIG Storage, SIG Auth. If you're an architect — SIG Architecture, CNCF TOC meeting notes, and watch the Alpha-stage KEPs — that's where the future direction lives.

---

### SCENE 9: "I Want to Contribute. Where Do I Start?"
**Time: 2:30**
**SLIDE:** "Your First Contribution" — 5-step path

```
YOUR FIRST CONTRIBUTION

1. Join Slack NOW → slack.k8s.io
   #kubernetes-contributors | #sig-contribex | your SIG's channel

2. SIG Meet & Greet → happening THIS WEEK at KubeCon
   Lunch session, Project Pavilion — just walk up

3. Claim a good first issue → go.k8s.io/good-first-issue
   Comment /assign | Mentor included | Practice at
   github.com/kubernetes-sigs/contributor-playground

4. Monthly New Contributor Orientation → kubernetes.dev/docs/orientation/
   3rd Tuesday of every month

5. Structured programs:
   Release Team Shadow → watch #sig-release on Slack
   LFX Mentorship      → mentoring.cncf.io
   GSoC / Outreachy     → annual Kubernetes projects
```

**Mumshad:** *(genuinely interested)* What if I don't just want to follow along? What if I actually want to contribute?

**Michael:** Then the path exists and it's clear.

Step one: Join Slack. Right now. slack.k8s.io. Join #kubernetes-contributors, join #sig-contribex, and join the channel for whatever SIG interests you.

Step two: The SIG Meet & Greet. It happens at every KubeCon. It's a lunch session in the Project Pavilion. You just walk up, find the table for a SIG you're curious about, and talk to people. It's happening this week — check the schedule.

Step three: Claim a good first issue. Go to go.k8s.io/good-first-issue. These are curated by the SIGs specifically for newcomers. Comment `/assign` and it's yours. Many of them come with a named mentor. And if you want to practice the mechanics first — the PR process, the CLA, the labels — there's a contributor playground at github.com/kubernetes-sigs/contributor-playground.

Step four: Monthly New Contributor Orientation. Third Tuesday of every month. There's also a self-paced course at kubernetes.dev/docs/onboarding.

Step five: Structured programs. The Release Team Shadow program — watch #sig-release on Slack for the call. LFX Mentorship at mentoring.cncf.io — they ran 187 successful projects in 2025. And there's always GSoC and Outreachy.

**Mumshad:** Is there someone who helps newcomers navigate all this?

**Michael:** Josh Berkus. He's Red Hat's Kubernetes Community Architect and co-chairs SIG Contributor Experience — SIG ContribEx. They're the ones who build the onboarding infrastructure, run the orientations, and curate the good first issues. If you meet him on Slack, his username is jberkus.

---

### SCENE 10: "One More Thing — The Maintainer Summit"
**Time: 1:00**
*(No slide)*

**Mumshad:** One more thing — I keep hearing about a "Contributor Summit." What is that?

**Michael:** It's actually been renamed. It's the Maintainer Summit now. It happens the Sunday before co-located events. To attend, you need to be a CNCF project maintainer or a Kubernetes GitHub org member.

The conversations that happen there flow directly into SIG meetings and Slack channels for the rest of the cycle. If you contribute long enough, you'll get there. But even without attending, you can follow the outcomes.

---

### SCENE 11: Close + QR Code
**Time: 2:00**
**SLIDE:** QR code + repo URL + key takeaways

```
EVERYTHING IS IN THE REPO

[LARGE QR CODE]

github.com/kodekloud/k8s-staying-current

- All links from this talk, verified and maintained
- Role-based subscription checklists
- All 24 SIGs — names, Slack channels, meeting times
- Governance reference (Steering, TOC, 5 TAGs, 12 WGs)
- Tool guides (pluto, kubent, RSS setup)
- "What Changed in 2025" summary
- First contribution path with direct links
```

**Mumshad:** *(drops character, addresses audience directly)* Alright, let's land this.

Everything we just talked about — every link, every tool, every checklist — is in a GitHub repo that we're going to maintain. Scan that QR code or go to github.com/kodekloud/k8s-staying-current.

**Michael:** Five things to remember:

One: Your cert is a snapshot. Kubernetes ships three times a year.

Two: SIGs own everything. Follow the SIG, not the vendor blog.

Three: The information landscape changed in 2025. Update your bookmarks.

Four: Thirty minutes a week. That's all it takes.

Five: If you want to contribute, the path exists and it starts today.

**Mumshad:** Thank you all. Enjoy the rest of KubeCon.

---

## Timing Summary

| Scene | Topic | Time |
|-------|-------|------|
| 1 | Setup / Hook | 1:30 |
| 2 | Release cadence — "my cert is expiring?" | 2:00 |
| 3 | 24 SIGs — "who runs Kubernetes?" | 2:30 |
| 4 | TAGs vs SIGs | 1:30 |
| 5 | KEP process — "how features ship" | 1:30 |
| 6 | 2025 landscape shift — "half my bookmarks are broken" | 2:00 |
| 7 | The Non-Negotiable Five — "what do I subscribe to?" | 1:30 |
| 8 | 30 min/week system — "I don't have time" | 1:30 |
| 9 | First contribution path — "I want to contribute" | 2:30 |
| 10 | Maintainer Summit context | 1:00 |
| 11 | Close + QR code | 2:00 |
| | **TOTAL** | **19:30** |

**Buffer:** 30 seconds for audience reactions, laughter, Mumshad's timing adjustments.

---

## Handoff Mechanics

- No formal handoffs. Mumshad asks, Michael answers.
- **Scene 1 → 2:** Mumshad explicitly sets up the role-play.
- **Scene 9 → 11:** Mumshad drops character. "Alright, let's land this." Shifts to direct address.
- Michael stays in educator mode throughout.

---

## Speaker Prep Notes

### What Mumshad Needs to Prep
1. The 8 questions (internalized, not memorized)
2. Reactive energy — surprise, frustration, mirroring audience
3. The close — drops character, drives audience to QR code
4. Timing awareness — accelerate/decelerate by adjusting follow-ups

### What Michael Needs to Prep
1. Facts cold: 24 SIGs, 5 TAGs, 7 Steering, 11 TOC, v1.35 Dec 17, v1.36 Apr 22, KubeWeekly died May 2025, Bluesky official
2. Pivot lines that set up the next question
3. Josh Berkus reference (delivered casually)
4. SIG Meet & Greet — check kccnceu2026.sched.com morning-of for exact day/time/location

---

## Facts to Re-Verify Week-Of (March 23–26, 2026)

<!-- VERIFY WEEK-OF -->

| Fact | Why It Might Change | Where to Check |
|------|---------------------|----------------|
| SIG Meet & Greet day/time | Not yet on schedule | kccnceu2026.sched.com |
| CNCF TOC membership | 6 of 11 seats expired Feb–Mar 2026 | github.com/cncf/toc README |
| v1.36 release schedule | Code Freeze is Mar 18, can slip | kubernetes.dev/resources/release/ |
| v1.35 latest patch level | New patches ship monthly | kubernetes.io/releases/ |
| K8s Podcast status | Last episode Dec 22, 2025 | kubernetespodcast.com |
| v1.32 EOL | Should be dead by March — confirm | kubernetes.io/releases/patch-releases/ |
