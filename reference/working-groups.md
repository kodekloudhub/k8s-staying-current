# Kubernetes Working Groups

Working Groups (WGs) are time-bounded, cross-cutting groups that address issues spanning multiple SIGs. They don't own code or long-term artifacts — they produce recommendations and designs that SIGs then implement.

**Current count:** 11 active Working Groups.

---

## Active Working Groups

### WG AI Conformance
- **Focus:** Define standardized capabilities, APIs, and configurations for Kubernetes clusters to reliably run AI/ML workloads. Establish conformance criteria.
- **Sponsoring SIGs:** Architecture, Testing
- **Slack:** `#wg-ai-conformance`
- **Meetings:** Thursdays 10:00 PT, biweekly

### WG AI Gateway
- **Focus:** Extending load-balancer, gateway, and proxy technologies to manage and route traffic for AI inference workloads.
- **Sponsoring SIGs:** Multicluster, Network
- **Slack:** `#wg-ai-gateway`
- **Meetings:** Thursdays 2:00 PM EST, weekly

### WG AI Integration
- **Focus:** Enable seamless integration of AI/ML control planes with Kubernetes. Standardize patterns for deploying and operating AI applications at scale.
- **Sponsoring SIGs:** API Machinery, Apps, Architecture, Auth, CLI
- **Slack:** `#wg-ai-integration`
- **Meetings:** Wednesdays 10:00 PT, biweekly

### WG Batch
- **Focus:** Enhance support for batch workloads (HPC, AI/ML, data analytics, CI) in core Kubernetes. Unify batch deployment patterns across providers.
- **Sponsoring SIGs:** Apps, Autoscaling, Node, Scheduling
- **Slack:** `#wg-batch`
- **Meetings:** Thursdays 3:00 PM CET, monthly

### WG Checkpoint Restore
- **Focus:** Integrate container checkpoint/restore functionality into Kubernetes — pause execution state and resume later.
- **Sponsoring SIGs:** Apps, Auth, Node, Scheduling
- **Slack:** `#wg-checkpoint-restore`
- **Meetings:** Thursdays 17:00 UTC, weekly

### WG Data Protection
- **Focus:** Promote data protection support in Kubernetes — backup, restore, and data protection workflows.
- **Sponsoring SIGs:** Apps, Storage
- **Slack:** `#wg-data-protection`
- **Meetings:** Wednesdays 9:00 PT, biweekly

### WG Device Management
- **Focus:** Enable simple and efficient configuration, sharing, and allocation of accelerators (GPUs, TPUs) and other specialized hardware.
- **Sponsoring SIGs:** Architecture, Autoscaling, Network, Node, Scheduling
- **Slack:** `#wg-device-management`
- **Meetings:** Biweekly (multiple sessions)

### WG etcd Operator
- **Focus:** Automatic and efficient operation of etcd clusters in Kubernetes using an etcd-operator. Manages application-level etcd (not the control plane etcd).
- **Sponsoring SIGs:** Cluster Lifecycle, etcd
- **Slack:** `#wg-etcd-operator`
- **Meetings:** Tuesdays 11:00 PT, biweekly

### WG LTS (Long Term Support)
- **Focus:** Investigate what "Long Term Support" means for Kubernetes. Assess feasibility, benefits, costs, and prerequisites of extending support windows.
- **Sponsoring SIGs:** Architecture, Cluster Lifecycle, K8s Infra, Release, Security, Testing
- **Slack:** `#wg-lts`
- **Meetings:** Tuesdays 07:00 PT, biweekly

### WG Node Lifecycle
- **Focus:** Improve node and pod lifecycle management — node drain/maintenance, pod disruption/termination, autoscaling, migration, and cloud provider integrations.
- **Sponsoring SIGs:** Apps, Autoscaling, CLI, Cloud Provider, Cluster Lifecycle, Network, Node, Scheduling, Storage
- **Slack:** `#wg-node-lifecycle`
- **Meetings:** Mondays 8:00 PT, weekly

### WG Structured Logging
- **Focus:** Modernize logging in Kubernetes core components — enable efficient consumption, processing, storage, and analysis of log information.
- **Sponsoring SIGs:** API Machinery, Architecture, Cloud Provider, Instrumentation, Network, Node, Scheduling, Storage
- **Slack:** `#wg-structured-logging`
- **Meetings:** Schedule varies

---

## How Working Groups Differ from SIGs

| | SIGs | Working Groups |
|-|------|---------------|
| **Duration** | Permanent | Time-bounded |
| **Own code** | Yes | No |
| **Governance** | Report to Steering | Report through sponsoring SIGs |
| **Output** | Code, tests, docs | Recommendations, designs, KEPs |

---

## Notes

- All Slack channels are on [Kubernetes Slack](https://slack.k8s.io).
- The AI-focused WGs (AI Conformance, AI Gateway, AI Integration) reflect the significant investment in AI/ML workload support in the Kubernetes community.
- WG LTS is investigating whether Kubernetes should offer longer support windows beyond the current 14-month lifecycle.
- Source: [kubernetes/community sig-list.md](https://github.com/kubernetes/community/blob/master/sig-list.md)
