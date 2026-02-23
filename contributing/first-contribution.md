# Your First Contribution to Kubernetes

A step-by-step path from zero to your first merged pull request.

---

## Step 1: Join Slack

**Do this right now.** Go to [slack.k8s.io](https://slack.k8s.io) and create an account.

Join these channels:
- `#kubernetes-contributors` — General contributor discussion
- `#sig-contribex` — SIG Contributor Experience, the group that helps new contributors
- Your SIG's channel — Pick the SIG closest to your interest (see [`../reference/all-24-sigs.md`](../reference/all-24-sigs.md))

Slack is where most real-time contributor coordination happens. Lurk for a week to get the rhythm, then start asking questions.

---

## Step 2: Practice the Mechanics

Before touching the real Kubernetes repo, practice the PR workflow in the contributor playground:

**Repository:** [github.com/kubernetes-sigs/contributor-playground](https://github.com/kubernetes-sigs/contributor-playground)

This repo exists specifically for new contributors to practice:
- Forking and cloning
- Creating branches
- Making changes
- Signing the CLA (Contributor License Agreement)
- Opening a pull request
- Responding to bot commands and labels

---

## Step 3: Find a Good First Issue

**URL:** [go.k8s.io/good-first-issue](https://go.k8s.io/good-first-issue)

These issues are curated by the SIGs specifically for newcomers. They are:
- Well-defined with clear scope
- Appropriately sized for a first contribution
- Often tagged with a mentor who can help

### How to claim an issue:
1. Find an issue that interests you
2. Read the description and any linked context
3. Comment `/assign` on the issue
4. The Kubernetes bot will assign it to you
5. If you can't complete it within a reasonable time, comment `/unassign` so someone else can pick it up

### Types of first contributions:
- **Documentation fixes** — Typos, outdated instructions, missing examples
- **Test improvements** — Adding test coverage, fixing flaky tests
- **Small code changes** — Bug fixes with clear reproduction steps
- **Label/triage help** — Helping SIGs triage issues (no code required)

---

## Step 4: Submit Your Pull Request

1. Fork the relevant repository
2. Create a feature branch
3. Make your changes
4. Ensure tests pass locally
5. Open a pull request with a clear description
6. Respond to reviewer feedback

### Kubernetes-specific PR mechanics:
- **CLA:** You must sign the Contributor License Agreement. The bot will prompt you on your first PR.
- **Labels:** Bots apply labels automatically. Reviewers use `/lgtm` and `/approve` commands.
- **CI:** Automated tests run on every PR. All tests must pass before merge.
- **Review:** SIG members review PRs. Be patient — reviewers are volunteers.

---

## Step 5: Attend New Contributor Orientation

**Schedule:** 3rd Tuesday of every month
**URL:** [kubernetes.dev/docs/orientation/](https://kubernetes.dev/docs/orientation/)

This is a live session where experienced contributors walk through:
- How the project is organized
- How to find work
- How the review process works
- Common pitfalls and how to avoid them

Can't make the live session? There's a self-paced course:
**URL:** [kubernetes.dev/docs/onboarding](https://kubernetes.dev/docs/onboarding)

---

## Beyond Your First PR

Once you've merged your first contribution, the path forward opens up:

- **Continue contributing to your SIG** — Regular contributors get recognized and gain trust
- **Join SIG meetings** — Every SIG has regular video calls. Attending shows commitment.
- **Apply for structured programs** — See [`mentorship-programs.md`](mentorship-programs.md)
- **Release Team Shadow** — Shadow an experienced release team member for a release cycle. Watch `#sig-release` on Slack.

---

## Getting Help

- **Slack:** `#kubernetes-contributors` and `#sig-contribex`
- **SIG ContribEx:** The SIG dedicated to improving the contributor experience. See [`josh-berkus-and-contribex.md`](josh-berkus-and-contribex.md)
- **Mailing list:** [kubernetes-dev@googlegroups.com](https://groups.google.com/g/kubernetes-dev)
