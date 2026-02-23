# Architect Staying-Current Checklist

For architects and technical leads: the strategic direction, governance decisions, and early-stage features that shape long-term platform decisions.

---

## Subscribe Once (5 minutes)

- [ ] **kubernetes-security-announce** — [Google Group](https://groups.google.com/g/kubernetes-security-announce)
- [ ] **LWKD** — [lwkd.info](https://lwkd.info)
- [ ] **Kubernetes Blog RSS** — [kubernetes.io/feed.xml](https://kubernetes.io/feed.xml)
- [ ] **GitHub Releases watch** — [kubernetes/kubernetes](https://github.com/kubernetes/kubernetes) → Watch → Custom → Releases
- [ ] **Official CVE JSON feed** — [kubernetes.io/docs/reference/issues-security/official-cve-feed/](https://kubernetes.io/docs/reference/issues-security/official-cve-feed/)

---

## Your SIGs

These are the SIGs whose changes shape strategic direction:

| SIG | Why It Matters to Architects |
|-----|-------------------------------|
| **SIG Architecture** | Owns API conventions, conformance testing, and cross-cutting architectural decisions — this is where the project's direction is set |
| **CNCF TOC** | Technical Oversight Committee — project acceptance, maturity ratings, and ecosystem-level decisions |
| **Alpha-stage KEPs** | Where the future lives — features in Alpha today are your production choices in 18 months |

### Slack Channels to Join
- `#sig-architecture`
- `#kubernetes-dev` (cross-SIG development discussions)
- `#sig-release` (release timeline awareness)

---

## Weekly Routine (20 minutes)

- [ ] Read LWKD — pay attention to KEP status changes and cross-SIG discussions
- [ ] Scan `#sig-architecture` for design proposals and architectural decisions
- [ ] Check for new Alpha-stage KEPs that could affect your platform roadmap

---

## Monthly Routine (30 minutes)

- [ ] Read Wisdom of the Cloud newsletter
- [ ] Review CNCF TOC meeting notes — [github.com/cncf/toc](https://github.com/cncf/toc)
- [ ] Scan the KEP board for features moving from Alpha to Beta — these are your planning signals
- [ ] Check CNCF project maturity changes — new Graduated projects may replace tools in your stack

---

## Quarterly Routine (1 hour)

- [ ] Run `pluto` and `kubent` across your fleet
- [ ] Deep-dive the upcoming release's KEP list — focus on:
  - Alpha features that signal future direction
  - Beta features that should enter your evaluation pipeline
  - Stable features that should enter your production pipeline
- [ ] Review the Steering Committee meeting notes for governance changes
- [ ] Evaluate your platform's alignment with the Kubernetes conformance profile
- [ ] Check the CNCF landscape for new projects entering Incubating or Graduated status

---

## What to Watch For

- **API convention changes** — SIG Architecture decisions about API design patterns affect every controller and operator you build or adopt.
- **Alpha-stage KEPs** — These take 2–4 releases (8–16 months) to reach Stable. If you're planning platform capabilities 12–18 months out, watch the Alpha pipeline.
- **Conformance changes** — What counts as "Kubernetes" evolves. Conformance test additions can affect managed Kubernetes provider evaluations.
- **CNCF project maturity** — When a project Graduates (e.g., moves from Sandbox to Incubating to Graduated), it signals ecosystem consensus. This should inform your build-vs-adopt decisions.
- **Governance shifts** — Steering Committee elections, TOC membership changes, and TAG restructuring all affect project direction. The May 2025 TAG restructuring from 8 to 5 TAGs is a recent example.

---

## Architect-Specific Resources

- **KEP tracking** — [github.com/kubernetes/enhancements](https://github.com/kubernetes/enhancements)
- **CNCF TOC** — [github.com/cncf/toc](https://github.com/cncf/toc)
- **CNCF Landscape** — [landscape.cncf.io](https://landscape.cncf.io)
- **Conformance dashboard** — [cncf.io/ck](https://cncf.io/ck)
- **SIG Architecture meetings** — Check [`../reference/all-24-sigs.md`](../reference/all-24-sigs.md) for schedule
