# The 2025 Landscape Shift

If you're following Kubernetes staying-current guides written before mid-2025, many of your bookmarks are broken. Here's what changed.

---

## What Died

### KubeWeekly Newsletter
- **Status:** Dead
- **Last issue:** #434, May 2025
- **Replacement:** [Wisdom of the Cloud](https://cncf.io/newsletter) (monthly, from CNCF)
- **Note:** Many guides still recommend KubeWeekly. It's gone.

### "Ship It" Podcast
- **Status:** Rebranded
- **New name:** "Fork Around and Find Out" (FAFO)
- **What happened:** The Changelog network rebranded the show with new hosts and format.

### Old CNCF TAG Slack Channels
- **Status:** Archived (June 2025)
- **What happened:** CNCF restructured from 8 TAGs to 5 in May 2025. The old Slack channels for TAG App Delivery, TAG Runtime, and TAG Environmental Sustainability were archived.
- **Replacement:** New channels for the 5 current TAGs. See [`../reference/cncf-tags.md`](../reference/cncf-tags.md).

---

## What Changed

### Kubernetes Slack
- **Status:** Active, but future uncertain
- **What happened:** In June 2025, Salesforce threatened to downgrade the Kubernetes Slack workspace (300,000+ members). The community mobilized, and the downgrade was cancelled. Slack remains the primary real-time communication channel.
- **Current risk:** The dependency on Salesforce's goodwill is a known concern. No migration has been announced, but the conversation is ongoing.

### Social Media — Bluesky Is Official
- **Status:** Bluesky is the primary official social channel
- **Evidence:** The v1.35 release blog post (December 2025) explicitly stated: "Follow us on Bluesky @kubernetes.io"
- **X/Twitter:** Deprioritized. The official account still exists but is no longer the primary channel.
- **Action:** Follow [@kubernetes.io on Bluesky](https://bsky.app/profile/kubernetes.io)

### Ingress NGINX
- **Status:** Being archived after March 2026
- **Replacement:** Gateway API
- **Action:** If you're running Ingress NGINX, plan your migration. See the Kubernetes blog for migration guidance.

---

## What's Still Current

### LWKD (Last Week in Kubernetes Development)
- **Status:** Active and reliable
- **URL:** [lwkd.info](https://lwkd.info)
- **Cadence:** Weekly
- **Why it matters:** Best signal-to-noise ratio for upstream Kubernetes development

### Wisdom of the Cloud
- **Status:** Active (CNCF's replacement for KubeWeekly)
- **URL:** [cncf.io/newsletter](https://cncf.io/newsletter)
- **Cadence:** Monthly
- **Scope:** Broader than KubeWeekly — covers the full CNCF landscape, not just Kubernetes

### Kubernetes Blog
- **Status:** The single most authoritative source
- **URL:** [kubernetes.io/blog](https://kubernetes.io/blog)
- **RSS:** [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml)

### Kubernetes Podcast (from Google)
- **Status:** Active but verify
- **URL:** [kubernetespodcast.com](https://kubernetespodcast.com)
- **Note:** Last confirmed episode December 22, 2025
<!-- VERIFY WEEK-OF: Check if new episodes have been published -->

---

## Summary: Update Your Bookmarks

| Old | New |
|-----|-----|
| KubeWeekly | Wisdom of the Cloud ([cncf.io/newsletter](https://cncf.io/newsletter)) |
| Ship It podcast | Fork Around and Find Out |
| Twitter @kuabornetesio | Bluesky @kubernetes.io |
| 8 CNCF TAGs | 5 CNCF TAGs (restructured May 2025) |
| TAG App Delivery Slack | Archived — use new TAG channels |
| TAG Runtime Slack | Archived — use new TAG channels |
