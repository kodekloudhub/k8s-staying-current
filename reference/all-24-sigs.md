# All 24 Kubernetes Special Interest Groups (SIGs)

Every SIG, with Slack channels, mailing lists, meeting schedules, and current chairs. Data sourced from [kubernetes/community sig-list.md](https://github.com/kubernetes/community/blob/master/sig-list.md).

---

## Quick Reference

| # | SIG | Slack | Primary Meeting | Chairs |
|---|-----|-------|----------------|--------|
| 1 | API Machinery | `#sig-api-machinery` | Wed 11:00 PT, biweekly | David Eads (Red Hat), Federico Bongiovanni (Google) |
| 2 | Apps | `#sig-apps` | Mon 9:00 PT, biweekly | Janet Kuo (Google), Kenneth Owens (Snowflake), Maciej Szulik (Defense Unicorns) |
| 3 | Architecture | `#sig-architecture` | Thu 11:00 PT, biweekly | Derek Carr (Red Hat), Davanum Srinivas (NVIDIA), John Belamaric (Google) |
| 4 | Auth | `#sig-auth` | Wed 11:00 PT, biweekly | Anish Ramasekar (Microsoft), Micah Hausler (Amazon), Rita Zhang (Microsoft) |
| 5 | Autoscaling | `#sig-autoscaling` | Thu 17:00 Poland, weekly | Guy Templeton (Skyscanner), Kuba Tuznik (Google) |
| 6 | CLI | `#sig-cli` | Wed 09:00 PT, biweekly | Arda Guclu (Red Hat), Marly Salazar (Independent) |
| 7 | Cloud Provider | `#sig-cloud-provider` | Wed 9:00 PT, biweekly | Bridget Kromhout (Microsoft), Michael McCune (Red Hat) |
| 8 | Cluster Lifecycle | `#sig-cluster-lifecycle` | Tue 09:00 PT, biweekly | Justin Santa Barbara (Google), Lubomir Ivanov (Independent), Vince Prignano (Red Hat) |
| 9 | Contributor Experience | `#sig-contribex` | Wed 10:00 PT, biweekly | Kaslin Fields (Google), Mario Fahlandt (Kubermatic), Nabarun Pal (Broadcom) |
| 10 | Docs | `#sig-docs` | Tue 17:30 UTC, biweekly | Divya Mohan (SUSE), Natali Vlatko (Cisco), Rey Lejano (Red Hat) |
| 11 | etcd | `#sig-etcd` | Thu 11:00 PT, biweekly | Ivan Valdes (Inmar Intelligence), James Blair (Red Hat), Siyuan Zhang (Google) |
| 12 | Instrumentation | `#sig-instrumentation` | Fri 8:30 PT, biweekly | Pranshu Srivastava (Red Hat), Richa Banker (Google) |
| 13 | K8s Infra | `#sig-k8s-infra` | Wed 17:00 UTC, biweekly | Dylan-Daniel Page (Lambda AI), Arnaud Meukam (Independent), Ciprian Hacman (Microsoft) |
| 14 | Multicluster | `#sig-multicluster` | Tue 9:30 PT, weekly | Jeremy Olmsted-Thompson (Google), Stephen Kitt (Red Hat) |
| 15 | Network | `#sig-network` | Thu 09:00 PT, biweekly | Bowei Du (Google), Michael Zappa (Microsoft), Shane Utt (Red Hat) |
| 16 | Node | `#sig-node` | Tue 10:00 PT, weekly | Sergey Kanzhelev (Google), Peter Hunt (Red Hat), Mrunal Patel (Red Hat) |
| 17 | Release | `#sig-release` | Thu 14:30 UTC, biweekly | Jeremy Rickard (Microsoft), Stephen Augustus (Bloomberg), Sascha Grunert (Red Hat) |
| 18 | Scalability | `#sig-scalability` | Thu 10:30 PT, biweekly | Marcel Zieba (Isovalent), David (Mengqi) Yu (Amazon) |
| 19 | Scheduling | `#sig-scheduling` | Thu 10:00 PT, biweekly | Maciej Skoczen (Google), Kensei Nakada (Independent) |
| 20 | Security | `#sig-security` | Fri 8:00 PT, biweekly | Ian Coldwater (Independent), Cailyn Edwards (Okta), Tabitha Sable (Datadog) |
| 21 | Storage | `#sig-storage` | Thu 9:00 PT, biweekly | Saad Ali (Google), Xing Yang (VMware) |
| 22 | Testing | `#sig-testing` | Tue 10:00 PT, biweekly | Brady Pratt (Red Hat), Michelle Shepardson (Google), Brian McQueen (LinkedIn) |
| 23 | UI | `#sig-ui` | No regular meetings listed | Sebastian Florek (Plural), Joaquim Rocha (Amutable), Shu Muto (NEC) |
| 24 | Windows | `#sig-windows` | Tue 12:30 ET, weekly | Aravindh Puthiyaparambil (Softdrive Technologies), Mark Rossetti (Microsoft) |

---

## Mailing Lists

All SIGs have Google Group mailing lists. The naming pattern varies:

| SIG | Mailing List |
|-----|-------------|
| API Machinery | [kubernetes-sig-api-machinery](https://groups.google.com/forum/#!forum/kubernetes-sig-api-machinery) |
| Apps | [sig-apps@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-apps) |
| Architecture | [sig-architecture@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-architecture) |
| Auth | [kubernetes-sig-auth](https://groups.google.com/forum/#!forum/kubernetes-sig-auth) |
| Autoscaling | [kubernetes-sig-autoscaling](https://groups.google.com/forum/#!forum/kubernetes-sig-autoscaling) |
| CLI | [sig-cli@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-cli) |
| Cloud Provider | [kubernetes-sig-cloud-provider](https://groups.google.com/forum/#!forum/kubernetes-sig-cloud-provider) |
| Cluster Lifecycle | [sig-cluster-lifecycle@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-cluster-lifecycle) |
| Contributor Experience | [kubernetes-sig-contribex](https://groups.google.com/forum/#!forum/kubernetes-sig-contribex) |
| Docs | [kubernetes-sig-docs](https://groups.google.com/forum/#!forum/kubernetes-sig-docs) |
| etcd | [etcd-dev](https://groups.google.com/g/etcd-dev) |
| Instrumentation | [kubernetes-sig-instrumentation](https://groups.google.com/forum/#!forum/kubernetes-sig-instrumentation) |
| K8s Infra | [sig-k8s-infra@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-k8s-infra) |
| Multicluster | [kubernetes-sig-multicluster](https://groups.google.com/forum/#!forum/kubernetes-sig-multicluster) |
| Network | [sig-network@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-network) |
| Node | [sig-node@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-node) |
| Release | [kubernetes-sig-release](https://groups.google.com/forum/#!forum/kubernetes-sig-release) |
| Scalability | [kubernetes-sig-scale](https://groups.google.com/forum/#!forum/kubernetes-sig-scale) |
| Scheduling | [sig-scheduling@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-scheduling) |
| Security | [kubernetes-sig-security](https://groups.google.com/forum/#!forum/kubernetes-sig-security) |
| Storage | [sig-storage@kubernetes.io](https://groups.google.com/a/kubernetes.io/g/sig-storage) |
| Testing | [kubernetes-sig-testing](https://groups.google.com/forum/#!forum/kubernetes-sig-testing) |
| UI | [kubernetes-sig-ui](https://groups.google.com/forum/#!forum/kubernetes-sig-ui) |
| Windows | [kubernetes-sig-windows](https://groups.google.com/forum/#!forum/kubernetes-sig-windows) |

---

## By Role

### Developers
- **SIG Apps** — Workload APIs (Deployments, StatefulSets, Jobs)
- **SIG API Machinery** — API server, client libraries, API conventions
- **SIG CLI** — kubectl

### Operators
- **SIG Node** — Kubelet, container runtime, node-level changes
- **SIG Network** — Services, DNS, NetworkPolicy, Gateway API
- **SIG Storage** — PVs, CSI drivers, volume management
- **SIG Auth** — RBAC, authentication, authorization
- **SIG Cluster Lifecycle** — kubeadm, Cluster API, upgrades

### Architects
- **SIG Architecture** — API conventions, conformance, cross-cutting decisions
- **SIG Release** — Release process and timeline

### Contributors
- **SIG Contributor Experience** — Onboarding, community health
- **SIG Docs** — Documentation

---

## Notes

- **SIG etcd** is the newest SIG, established November 2023 (bringing total from 23 to 24).
- **SIG etcd** uses the `etcd-dev` mailing list rather than a `kubernetes-sig-*` group, reflecting its CNCF project heritage.
- **SIG Scalability** uses the mailing list name `kubernetes-sig-scale` (not `kubernetes-sig-scalability`).
- **SIG Contributor Experience** uses the abbreviated Slack channel `#sig-contribex`.
- **SIG UI** has no regular meetings listed in the community repo.
- All Slack channels are on `kubernetes.slack.com`. Join at [slack.k8s.io](https://slack.k8s.io).
- Most SIGs have additional subproject and triage meetings beyond the primary meeting listed here. Check each SIG's charter in the [kubernetes/community](https://github.com/kubernetes/community) repo for full schedules.
