---
title: "Putting Risk Into Change, Project, and Vendor Processes"
date: 2026-10-17
description: "If risk only lives in a register, it arrives too late to matter. Embed it in the workflows people already use — change management, projects, and procurement — with tiering so it never becomes a gatekeeping tax."
categories: ["Governance & Oversight"]
tags: ["risk integration", "change management", "project risk", "procurement", "grc"]
level: 4
weight: 9
---

A risk register that lives apart from how work gets done is a reporting artefact. By the time a risk reaches it, decisions have been made, money is spent, and systems are live. The fix is not a bigger register — it is **embedding risk into the processes your organisation already runs**.

The principle throughout: **integrate, don't add.** A parallel risk process is a tax people route around.

## Three places risk must live

1. **Change management** — every material change to a live environment.
2. **Projects** — from initiation through go-live.
3. **Procurement / vendor onboarding** — before commitments are signed.

Each already has a gate. Risk should ride along, not build its own.

## 1. Change management

Changes are where new risk enters production. Not all changes deserve a risk assessment — that is how you create a bottleneck nobody respects. **Tier by impact**:

| Change tier | Example | Risk treatment |
| --- | --- | --- |
| **Significant** | New internet-facing service, auth change, data migration | Full risk assessment before approval |
| **Moderate** | Config change to a core system, new integration | Lightweight checklist |
| **Routine** | Standard patch, minor UI fix | No extra step |

The goal: **significant changes get real scrutiny; routine changes get none.** Define the triggers explicitly so triage is objective, not political.

Useful rule: risk assessment here answers one question — *"does this change introduce or worsen any risk beyond our appetite, and if so what do we do before go-live?"*

## 2. Projects

Risk belongs at three points in a project, and each has a different purpose:

- **Initiation** — what risks could stop us achieving the project's objective? (Feeds the business case.)
- **Design** — have we designed out the foreseeable risks? (Architecture and control decisions.)
- **Go-live** — is the residual risk acceptable, and who accepts it? (The authorization moment.)

Folding risk into existing gates — business case, design review, go/no-go — avoids a separate process. The [NIST RMF authorization step](/posts/nist-rmf-vs-iso-27005/) is exactly this discipline: a **named person accepts residual risk**.

Cross-project patterns are a bonus: risks that recur across projects belong in the register and, often, in a **standard** or a **baseline control**.

## 3. Procurement and vendor onboarding

Never onboard a vendor without a risk view. This is where [third-party risk](/posts/third-party-supply-chain-risk/) meets process:

- **Tier the vendor** as part of the intake form.
- **Trigger assessment** from the tier, before contract signature.
- **Attach contract requirements** (notification, audit, exit) to the procurement record.
- **Create the register entry and owner** automatically on approval.

If the vendor risk check is a step in the procurement workflow, it happens. If it is a separate request to the risk team, it becomes optional.

## Make it lightweight, or it dies

The failure mode of embedded risk is **gatekeeping**: risk becomes the team that says no, and the business learns to avoid the gate. Counter it:

- **Tier everything.** Match effort to impact.
- **Default to yes with conditions.** "Approved if MFA is enforced" beats "rejected".
- **Timebox.** A significant-change assessment should take hours, not weeks.
- **Self-service first.** Templates and checklists let teams assess themselves; the risk function reviews exceptions, not everything.
- **Automate evidence.** Pull configs and tickets automatically where possible.

## Metrics worth watching

Embedding is measurable — and that is how you defend it:

- **% of significant changes with a completed risk assessment** before approval.
- **% of new vendors tiered and assessed** before contract.
- **Time to complete** a standard assessment (watch this one; if it grows, adoption will fall).
- **% of accepted risks with a named owner and date.**
- **Recurring risks across projects** — a signal to build a baseline control.

## Common mistakes

- **A separate risk process.** If it is not in the workflow, it will be skipped.
- **Assessing every change.** Unbounded effort guarantees a bottleneck.
- **No defined triggers.** Vague criteria make triage political.
- **Risk as "the department of no".** Removes the incentive to engage early.
- **No feedback loop.** Project risks that never reach the register teach nobody.
- **Manual evidence collection.** Automate it, or it will rot.

## Key takeaways

- **Integrate risk into existing gates** — change, projects, procurement — rather than adding a parallel process.
- **Tier by impact** everywhere; significant gets real scrutiny, routine gets none.
- In projects, use **initiation, design, and a named go-live acceptance**.
- In procurement, **tier and assess before signature**, and connect the result to the register.
- Keep it **lightweight and self-service**, and measure adoption — an embedded process that becomes a tax gets routed around.

---

That completes **Level 4 — Enterprise**. Next on the path is **Level 5 — Hero**: culture, metrics, and leadership, starting with KRIs that predict rather than report. See the [learning path](/learning-path/).
