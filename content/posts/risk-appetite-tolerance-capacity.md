---
title: "Risk Appetite vs. Risk Tolerance vs. Risk Capacity"
date: 2026-10-17
description: "Three closely related ideas that decide whether a risk is acceptable. Get them straight and you can stop arguing about 'how much risk is too much' from scratch every time."
categories: ["Governance & Oversight"]
tags: ["risk appetite", "risk tolerance", "risk capacity", "governance"]
level: 1
weight: 5
---

Every risk conversation eventually reaches the same wall: *"Is this acceptable?"* Without a written answer, each debate starts from zero and is settled by whoever is most senior or most persistent. The three terms below are how mature organisations settle it in advance.

## The three ideas

| Term | Question | Who sets it |
| --- | --- | --- |
| **Risk capacity** | How much risk *could* we take before we are in serious trouble? | Objective reality |
| **Risk appetite** | How much risk do we *choose* to take to meet our objectives? | Board / executives |
| **Risk tolerance** | What range of variation around that is acceptable? | Management |

A useful shorthand: **capacity is what you can survive, appetite is what you choose, tolerance is the acceptable wobble.**

## Risk capacity: the hard limit

Capacity is the maximum risk an organisation can absorb before objectives, solvency, or existence are threatened. It is not a preference — it is a fact.

- How much downtime can we survive before contracts are breached?
- How large a fine can we absorb without material harm?
- How much capital can we lose and still operate?

You do not choose your capacity; you discover it. Appetite above capacity is not ambition — it is negligence.

## Risk appetite: the deliberate choice

Appetite is how much risk leadership is willing to take *on purpose* to pursue objectives. It is a choice, and it should be expressed in terms you can actually test.

Weak appetite: *"We have a low appetite for risk."* (Meaningless.)

Usable appetite:

> *"We will accept availability risk up to 4 hours of unplanned downtime per quarter for tier-2 systems, and near-zero for systems that process customer payments. We have a low appetite for confidentiality risk involving customer data and will not accept any known unauthorised access."*

Now you can evaluate a specific risk against it. That is the whole test.

## Risk tolerance: the acceptable range

Tolerance is the margin around appetite — how far you can drift before someone acts.

- **Appetite:** up to 4 hours of downtime per quarter.
- **Tolerance:** trigger a review at 3 hours; escalate to the CTO beyond 4.

Tolerance is what turns appetite into **thresholds** that monitoring can watch. Without tolerance, appetite is a slogan; with it, you get alerts and actions.

## How they fit together

```
   capacity   ────────────────  hard limit: beyond here, real trouble
        ▲
   appetite   ────────────────  where we choose to operate
        ▲
  tolerance   ─── range ──▶    trigger for review / escalation
        ▲
   current risk position
```

If current risk exceeds tolerance, you act or escalate. If it approaches capacity, you are in existential territory and appetite has failed.

## Making it real (the hard part)

Appetite statements are easy to write and easy to ignore. Four things make them bite:

1. **Express them in measurable units** — hours, dollars, count of incidents, % of systems. Not "low/medium/high".
2. **Tie them to objectives** — appetite exists to enable strategy, not to be cautious for its own sake.
3. **Define tolerances as thresholds** with owners and escalation paths.
4. **Report against them** — show leadership where you stand versus appetite and tolerance. A gap is a decision waiting to happen.

## Common mistakes

- **Setting appetite below capacity you actually have**, then wondering why the business bypasses risk. Too-tight appetite gets ignored, which teaches everyone that the rules are optional.
- **Copying another company's appetite.** It reflects *their* objectives, capital, and regulation, not yours.
- **Writing appetite nobody can measure.** If it cannot be tested against a real risk, it is decoration.
- **Confusing appetite with capacity.** One is a choice, the other a limit.

## Key takeaways

- **Capacity = what you can survive. Appetite = what you choose. Tolerance = the acceptable range.**
- Appetite must be **measurable** and tied to **objectives**, or it will be ignored.
- Tolerance converts appetite into **thresholds** for monitoring and escalation.
- Never set appetite **above capacity** — that is negligence dressed as ambition.

---

That completes **Level 1**. Next up on the path: **Level 2 — Practitioner**, where we get into assessment and treatment. See the [learning path](/learning-path/).
