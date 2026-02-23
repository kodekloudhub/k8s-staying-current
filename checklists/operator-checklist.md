# Operator Staying-Current Checklist

For platform engineers and cluster operators: the infrastructure-level changes that affect node management, networking, storage, and security.

---

## Subscribe Once (5 minutes)

- [ ] **kubernetes-security-announce** — [Google Group](https://groups.google.com/g/kubernetes-security-announce)
- [ ] **LWKD** — [lwkd.info](https://lwkd.info)
- [ ] **Kubernetes Blog RSS** — [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml)
- [ ] **GitHub Releases watch** — [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) → Watch → Custom → Releases
- [ ] **Official CVE JSON feed** — [kubernetes.io/docs/reference/issues-security/official-cve-feed/](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/)

---

## Your SIGs

These are the SIGs whose changes directly affect your infrastructure:

| SIG | Why It Matters to Operators |
|-----|------------------------------|
| **SIG Node** | Owns the kubelet — every node-level change, resource management, container runtime integration |
| **SIG Network** | Owns all networking code — Services, DNS, network policies, Gateway API, service mesh integration points |
| **SIG Storage** | Owns PersistentVolumes, CSI drivers, volume snapshots — everything about persistent data |
| **SIG Auth** | Owns RBAC, authentication, authorization — security boundaries and access control |

### Slack Channels to Join
- `#sig-node`
- `#sig-network`
- `#sig-storage`
- `#sig-auth`

---

## Weekly Routine (20 minutes)

- [ ] Read LWKD
- [ ] Scan `#sig-node` and `#sig-network` for breaking changes or deprecation discussions
- [ ] Check security-announce for any new CVEs

---

## Monthly Routine (30 minutes)

- [ ] Read Wisdom of the Cloud newsletter
- [ ] Scan the Kubernetes blog for security advisories, patch releases, and infrastructure changes
- [ ] Review any new patch releases — check if they contain security fixes requiring immediate upgrades

---

## Quarterly Routine (1 hour)

- [ ] Run `pluto detect-all-in-cluster` across all managed clusters
- [ ] Run `kubent` against all managed clusters
- [ ] Review KEPs for the upcoming release — focus on changes to:
  - Kubelet behavior and node management
  - Networking changes (especially Service and NetworkPolicy)
  - Storage driver changes and CSI updates
  - Auth and RBAC changes
- [ ] Verify your cluster versions against the [release calendar](../reference/release-calendar.md) — are any approaching EOL?
- [ ] Test upgrade path for next minor version in a staging environment

---

## What to Watch For

- **Node-level changes** — Kubelet flags get deprecated. CRI changes can affect container runtimes. Resource management behavior changes can impact scheduling.
- **Network policy changes** — New features in NetworkPolicy can change default behavior. Gateway API is replacing Ingress — plan migrations.
- **Storage deprecations** — In-tree storage plugins are migrating to CSI. Check if your storage provider's in-tree driver is being removed.
- **Security changes** — Auth changes can break existing RBAC configurations. Watch for changes to ServiceAccount token handling, Pod Security Standards enforcement, and admission control.
- **Ingress NGINX archival** — Being archived after March 2026. Migrate to Gateway API.

---

## Operator-Specific Tools

- **pluto** — Scans manifests and Helm releases for deprecated API versions. See [`../tools/pluto-guide.md`](../tools/pluto-guide.md)
- **kubent** — Checks running clusters for deprecated resources in real time. See [`../tools/kubent-guide.md`](../tools/kubent-guide.md)
- **kubeadm upgrade plan** — Shows available upgrades and required steps
- **kubectl get nodes** — Regularly verify node versions are consistent and supported
