# The Non-Negotiable Five

Five subscriptions that cover security, releases, and deprecations — the three things that will actually break your production clusters.

---

## 1. kubernetes-security-announce

**What:** Google Group that fires on CVE disclosures only.
**Why:** Low traffic, high signal. When a vulnerability drops (like the IngressNightmare CVE cluster that hit Ingress NGINX), subscribers know before the blog posts start flying.
**Subscribe:** [groups.google.com/g/kubernetes-security-announce](https://groups.google.com/g/kubernetes-security-announce)

---

## 2. LWKD — Last Week in Kubernetes Development

**What:** Weekly digest of Kubernetes development activity.
**Why:** Best signal-to-noise ratio in the ecosystem. Covers what changed in upstream Kubernetes each week — merges, KEP updates, SIG activity.
**Subscribe:** [lwkd.info](https://lwkd.info)

---

## 3. Kubernetes Blog RSS

**What:** The official Kubernetes blog feed.
**Why:** Release announcements, deprecation notices, and security advisories all land here first. The release blog post for each version is the single most valuable document in the ecosystem.
**Subscribe:** [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml)

**Tip:** Use any RSS reader — see [`../tools/rss-setup.md`](../tools/rss-setup.md) for setup instructions.

---

## 4. GitHub "Releases Only" Watch

**What:** GitHub notification for every patch and minor release of Kubernetes.
**Why:** You'll know the moment a new patch drops — including security patches that need immediate attention.
**How to set up:**
1. Go to [github.com/kubernetes/kubernetes](https://github.com/kubernetes/kubernetes)
2. Click **Watch** → **Custom** → check **Releases** only
3. Notifications go to your GitHub email

---

## 5. Official CVE JSON Feed

**What:** Machine-readable feed of Kubernetes vulnerabilities.
**Why:** Automatable — you can pipe this into your security tooling, dashboards, or alerting systems. It's the source of truth for Kubernetes CVEs.
**URL:** [kubernetes.io/docs/reference/issues-security/official-cve-feed/](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/)

---

## Why These Five?

These five sources cover the three categories that matter for production systems:

| Category | Covered By |
|----------|-----------|
| **Security** | kubernetes-security-announce, CVE JSON feed |
| **Releases** | GitHub Releases watch, Blog RSS |
| **Deprecations** | Blog RSS, LWKD |

Everything else — podcasts, newsletters, social media, SIG meetings — adds depth. These five are the foundation.
