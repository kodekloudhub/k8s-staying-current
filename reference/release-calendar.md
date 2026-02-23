# Kubernetes Release Calendar

Kubernetes ships 3 releases per year on ~15-week cycles with 14 months of patch support per release.

---

## Release Timeline (v1.32 – v1.36)

| Version | Codename | Release Date | Active Support Ends | EOL (Maintenance) | Latest Patch |
|---------|----------|-------------|--------------------|--------------------|--------------|
| v1.32 | Penelope | Dec 11, 2024 | Dec 28, 2025 | **Feb 28, 2026** | 1.32.12 |
| v1.33 | Octarine | Apr 23, 2025 | Apr 28, 2026 | Jun 28, 2026 | 1.33.8 |
| v1.34 | Of Wind & Will | Aug 27, 2025 | Aug 27, 2026 | Oct 27, 2026 | 1.34.4 |
| v1.35 | Timbernetes | Dec 17, 2025 | Dec 28, 2026 | Feb 28, 2027 | 1.35.1 |
| v1.36 | TBD | **Apr 22, 2026** (target) | ~Apr 2027 | ~Jun 2027 | — |

<!-- VERIFY WEEK-OF: Check latest patch levels at kubernetes.io/releases/ -->

---

## Support Policy

Each release receives approximately **14 months** of total support:
- **~12 months active support** — Bug fixes and security patches
- **~2 months maintenance mode** — Only CVE fixes, dependency updates, and critical issues

Kubernetes maintains patches for the **3 most recent minor releases** (N, N-1, N-2).

### Current Support Window (as of February 2026)

| Version | Status |
|---------|--------|
| v1.35 | Active support (current) |
| v1.34 | Active support |
| v1.33 | Active support |
| v1.32 | Maintenance mode → **EOL Feb 28, 2026** |

When v1.36 ships (~April 22, 2026), v1.33 becomes the oldest supported version.

---

## v1.36 Release Schedule

| Milestone | Date | Week |
|-----------|------|------|
| Cycle begins | Jan 12, 2026 | 1 |
| Production Readiness Freeze | Feb 4–5, 2026 | 4 |
| Enhancements Freeze | Feb 11–12, 2026 | 5 |
| Feature Blog Freeze | Feb 26–27, 2026 | 7 |
| **Code Freeze / Test Freeze** | **Mar 18–19, 2026** | **10** |
| KubeCon EU 2026 (Amsterdam) | Mar 23–26, 2026 | 11 |
| Docs Freeze | Apr 8–9, 2026 | 13 |
| v1.36.0-rc.0 | Apr 8, 2026 | 13 |
| v1.36.0-rc.1 | Apr 14, 2026 | 14 |
| **v1.36.0 Release** | **Apr 22, 2026** | **15** |

All deadlines use "Anywhere on Earth" (AoE) time (UTC-12).

<!-- VERIFY WEEK-OF: Code freeze is Mar 18. Confirm no schedule slips at kubernetes.dev/resources/release/ -->

---

## Patch Release Cadence

- **Monthly:** Patch releases for all supported versions ship on the same day
- **Post-minor-release:** First patch 1–2 weeks after a new minor release
- **Emergency patches:** May ship outside normal cadence for critical security issues
- **Holiday avoidance:** Releases skip major holiday windows

### Upcoming Patch Releases

| Month | Cherry Pick Deadline | Patch Release |
|-------|---------------------|---------------|
| March 2026 | Mar 6, 2026 | Mar 10, 2026 |
| April 2026 | Apr 10, 2026 | Apr 14, 2026 |
| May 2026 | May 8, 2026 | May 12, 2026 |

---

## How to Check Current Versions

```bash
# Your cluster version
kubectl version

# Latest stable release
curl -s https://dl.k8s.io/release/stable.txt

# Latest patch for a specific minor version
curl -s https://dl.k8s.io/release/stable-1.35.txt
curl -s https://dl.k8s.io/release/stable-1.34.txt
curl -s https://dl.k8s.io/release/stable-1.33.txt
```

---

## Official Links

| Resource | URL |
|----------|-----|
| Release overview | [kubernetes.io/releases/](https://kubernetes.io/releases/) |
| Patch release schedule | [kubernetes.io/releases/patch-releases/](https://kubernetes.io/releases/patch-releases/) |
| v1.36 release info | [kubernetes.dev/resources/release/](https://www.kubernetes.dev/resources/release/) |
| v1.36 schedule (GitHub) | [sig-release/releases/release-1.36](https://github.com/kubernetes/sig-release/tree/master/releases/release-1.36) |
| All release notes | [github.com/kubernetes/kubernetes/releases](https://github.com/kubernetes/kubernetes/releases) |
| End-of-life tracker | [endoflife.date/kubernetes](https://endoflife.date/kubernetes) |
