# Developer Staying-Current Checklist

For developers building applications on Kubernetes: the APIs, tools, and workflows that matter to you.

---

## Subscribe Once (5 minutes)

- [ ] **kubernetes-security-announce** — [Google Group](https://groups.google.com/g/kubernetes-security-announce)
- [ ] **LWKD** — [lwkd.info](https://lwkd.info)
- [ ] **Kubernetes Blog RSS** — [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml)
- [ ] **GitHub Releases watch** — [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) → Watch → Custom → Releases
- [ ] **Official CVE JSON feed** — [kubernetes.io/docs/reference/issues-security/official-cve-feed/](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/)

---

## Your SIGs

These are the SIGs whose changes directly affect your work:

| SIG | Why It Matters to Developers |
|-----|------------------------------|
| **SIG Apps** | Owns Deployments, StatefulSets, DaemonSets, Jobs — the workload APIs you use daily |
| **SIG API Machinery** | Owns the API server, client libraries, API conventions — changes here affect how you interact with the cluster |
| **SIG CLI** | Owns kubectl — your primary interface |

### Slack Channels to Join
- `#sig-apps`
- `#sig-api-machinery`
- `#sig-cli`

---

## Weekly Routine (20 minutes)

- [ ] Read LWKD
- [ ] Scan `#sig-apps` and `#sig-cli` for discussions relevant to your workloads
- [ ] Check if any new kubectl plugins or changes affect your workflow

---

## Monthly Routine (30 minutes)

- [ ] Read Wisdom of the Cloud newsletter
- [ ] Scan the Kubernetes blog for any posts about API changes or new workload features
- [ ] Check [github.com/kubernetes/enhancements](https://github.com/kubernetes/enhancements) for KEPs in Beta or Stable that affect workload APIs

---

## Quarterly Routine (1 hour)

- [ ] Run `pluto detect-all-in-cluster` or `pluto detect-files -d <your-manifests>` — catch deprecated APIs in your manifests before they break
- [ ] Run `kubent` against your clusters to identify deprecated resources
- [ ] Review KEPs for the upcoming release — focus on changes to:
  - Workload APIs (Deployments, StatefulSets, Jobs)
  - API conventions and versioning
  - kubectl features and flags

---

## What to Watch For

- **API version deprecations** — When a beta API graduates to stable, the beta version gets a deprecation timeline. If your manifests use `apps/v1beta1`, you're already behind.
- **kubectl flag changes** — Flags get deprecated and removed. Check the release notes.
- **Client library updates** — If you use client-go, watch for breaking changes in new releases.
- **Gateway API evolution** — If you're still on Ingress, Gateway API is the future. Plan accordingly.

---

## Developer-Specific Tools

- **pluto** — Scans manifests for deprecated API versions. See [`../tools/pluto-guide.md`](../tools/pluto-guide.md)
- **kubent** — Checks running clusters for deprecated resources. See [`../tools/kubent-guide.md`](../tools/kubent-guide.md)
- **kubectl diff** — Compare local manifests against live cluster state before applying
