# Kubernetes & CNCF Governance Quick Reference

A quick reference for the governance bodies that run Kubernetes and the CNCF.

---

## Kubernetes Steering Committee (7 seats)

The elected body that oversees the governance of the entire Kubernetes project. Members serve 2-year terms; 4 seats were elected in November 2025.

| Name | Affiliation | Term Ends | Notes |
|------|-------------|-----------|-------|
| Kat Cosgrove | Minimus | Oct 2027 | Elected Nov 2025 |
| Maciej Szulik | Defense Unicorns | Oct 2027 | Re-elected Nov 2025 |
| Paco Xu | DaoCloud | Oct 2027 | Re-elected Nov 2025 |
| Rita Zhang | Microsoft | Oct 2027 | Elected Nov 2025 |
| Antonio Ojea | Google | Oct 2026 | Continuing |
| Benjamin Elder | Google | Oct 2026 | Continuing |
| Sascha Grunert | Red Hat | Oct 2026 | Continuing |

**CNCF Governing Board Representative:** Christoph Blecker

**Meetings:**
- Open meeting: 1st Wednesday of each month, 8:00 AM PT (recorded)
- Closed meeting: 3rd Wednesday of each month, 8:00 AM PT

**GitHub:** [kubernetes/steering](https://github.com/kubernetes/steering)

---

## CNCF Technical Oversight Committee — TOC (11 seats)

The technical governing body of the CNCF. Handles project acceptance and maturity ratings. Does not tell Kubernetes what code to write.

| Name | Affiliation | Role | Term | Status |
|------|-------------|------|------|--------|
| Karena Angell | Red Hat | Chair | Mar 2025 – Mar 2027 | Active |
| Kevin Wang | Huawei | Vice Chair | Feb 2024 – Feb 2026 | **VERIFY WEEK-OF** |
| Alex Chircop | Google | Member | Mar 2025 – Mar 2027 | Active |
| Chad Beaudin | Boeing | Member | Mar 2025 – Mar 2027 | Active |
| Davanum Srinivas | NVIDIA | Member | Feb 2024 – Feb 2026 | **VERIFY WEEK-OF** |
| Emily Fox | Red Hat | Member | Feb 2024 – Mar 2026 | **VERIFY WEEK-OF** |
| Faseela K | Ericsson | Member | Mar 2025 – Mar 2027 | Active |
| Jeremy Rickard | Microsoft | Member | Mar 2025 – Mar 2027 | Active |
| Katie Gamanji | Apple | Member | Mar 2022 – Feb 2026 | **VERIFY WEEK-OF** |
| Lin Sun | Solo.io | Member | Feb 2024 – Feb 2026 | **VERIFY WEEK-OF** |
| Ricardo Rocha | CERN | Member | Feb 2024 – Feb 2026 | **VERIFY WEEK-OF** |

<!-- VERIFY WEEK-OF: 6 of 11 seats expire between Feb 4 and Mar 4, 2026. Check github.com/cncf/toc for updated membership. -->

**GitHub:** [cncf/toc](https://github.com/cncf/toc)

---

## CNCF Governing Board

Handles marketing, business oversight, and budget decisions for CNCF. Meets 3–5 times per year.

**Composition:**
- 17 Platinum Member Representatives (one per company)
- 3 Gold Member Representatives
- 3 Silver Member Representatives
- 1 End User TAB Chair
- 1 TOC Chair
- 2 Developer Seats

**GB Chair:** Christoph Blecker (Red Hat)

**Details:** [cncf.io/people/governing-board](https://www.cncf.io/people/governing-board/)

---

## 5 CNCF TAGs (Technical Advisory Groups)

Advisory groups that provide guidance on technical areas — they don't own code. Restructured from 8 to 5 in May 2025.

| TAG | Scope |
|-----|-------|
| Developer Experience | Databases, Microservices, Developer Frameworks |
| Infrastructure | Storage, Network, Compute, Service Mesh, Edge |
| Operational Resilience | Observability, Reliability, Cost, Chaos Engineering |
| Security and Compliance | Supply Chain Security, Policy, Auditing, Compliance |
| Workloads Foundation | Containers, Runtime, Serverless, Wasm, Batch, CI/CD |

Details: [`cncf-tags.md`](cncf-tags.md)

---

## 24 Kubernetes SIGs

SIGs own the code, tests, documentation, and roadmap for their area. They report to the Steering Committee.

Details: [`all-24-sigs.md`](all-24-sigs.md)

---

## Key Distinction

| | Kubernetes Governance | CNCF Governance |
|-|----------------------|-----------------|
| **Code authority** | Steering Committee → SIGs | None (advisory only) |
| **Technical oversight** | Steering Committee | TOC |
| **Budget/legal** | CNCF provides | Governing Board |
| **Advisory groups** | Working Groups | TAGs |

**Mental model:** CNCF is the landlord. Kubernetes arranges its own furniture. The CNCF provides infrastructure but doesn't tell SIGs what code to write.
