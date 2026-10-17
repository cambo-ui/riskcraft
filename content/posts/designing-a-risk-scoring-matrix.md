---
title: "Designing a Risk Scoring Matrix That Isn't Arbitrary"
date: 2026-10-17
description: "A 5x5 grid is not a methodology. Define your scales with real anchors, avoid the classic mistakes, and your scores will survive scrutiny instead of collapsing into 'whatever the loudest person says'."
categories: ["Risk Assessment"]
tags: ["scoring matrix", "likelihood", "impact", "qualitative", "risk assessment"]
level: 2
weight: 4
---

Almost every organisation has a risk matrix. Few have one that means anything. Done badly, a 5×5 grid is a machine for laundering opinion into numbers that look objective. Done well, it is a fast, consistent, defensible way to rank risks.

The difference is entirely in **how you define the scales**.

## Two dimensions, not one

A risk score combines two judgements:

- **Likelihood** — how probable is the event, given current conditions?
- **Impact** — how bad is it for the business if it happens?

The score is a **combination** (usually likelihood × impact, or a lookup in a matrix), never a single gut feeling. Keep the two dimensions visible; a risk that is certain-but-trivial is not the same as one that is rare-but-catastrophic, and collapsing them into one number hides that.

## The cardinal sin: undefined words

Here is a matrix nobody can use:

| | Low | Medium | High |
| --- | --- | --- | --- |
| **Low** | Low | Low | Medium |
| **Medium** | Low | Medium | High |
| **High** | Medium | High | High |

What does "High impact" mean? $10k? $10M? A day of downtime? Without defined anchors, two analysts scoring the same risk will disagree — and both will be "right".

## Define each level with anchors

Write down what every number means. This is the entire job.

**Likelihood scale**

| Score | Label | Anchor (per year) |
| --- | --- | --- |
| 1 | Rare | Less than once in 10 years |
| 2 | Unlikely | Once every 3–10 years |
| 3 | Possible | Once every 1–3 years |
| 4 | Likely | More than once a year |
| 5 | Almost certain | Multiple times a year |

**Impact scale**

| Score | Label | Anchor |
| --- | --- | --- |
| 1 | Insignificant | < $10k, no downtime, no data |
| 2 | Minor | $10k–$100k, < 4h downtime |
| 3 | Moderate | $100k–$500k, 4–24h downtime |
| 4 | Major | $500k–$2M, 1–3 days, limited data loss |
| 5 | Severe | > $2M, multi-day outage, or reportable data breach |

Your anchors will differ — the point is not these numbers, it is that **yours are written down and agreed** before anyone scores anything.

## Build the matrix

Combine the two scales. A common approach is multiplication with bands:

| | | **Impact →** | | | |
| --- | --- | --- | --- | --- | --- |
| | | 1 | 2 | 3 | 4 | 5 |
| **Likelihood ↓** | 5 | 5 | 10 | 15 | 20 | **25** |
| | 4 | 4 | 8 | 12 | **16** | **20** |
| | 3 | 3 | 6 | 9 | 12 | **15** |
| | 2 | 2 | 4 | 6 | 8 | 10 |
| | 1 | 1 | 2 | 3 | 4 | 5 |

Bands: **1–4 Low · 5–9 Medium · 10–14 High · 15–25 Critical.** Tune the bands to your tolerance — if a score of 10 triggers action, say so.

## The classic mistakes

- **Multiplying ranks.** Likelihood 4 × Impact 5 = 20 is not "twice as bad" as 10. Ordinal scales are not ratios. Use the number to *rank and band*, never to compute cost. For that, you need [quantitative analysis](/posts/fair-in-15-minutes/).
- **Different scores for inherent and residual, with no controls listed.** If residual doesn't reference the controls, it is fiction.
- **No calibration.** Two people scoring the same risk differently is expected; do it in a workshop and reconcile. A short calibration exercise makes scores converge remarkably fast.
- **Rank reversal.** With some matrix shapes, a slightly worse likelihood can rank a risk *lower*. Test your matrix with edge cases before you ship it.
- **Treating the score as the answer.** The score ranks; the decision still belongs to a human with a criterion (your appetite and tolerance).

## When to go beyond the matrix

A scoring matrix is a triage tool. It is fast and good enough for most risks. But when you must justify or refuse a **six- or seven-figure** decision, "Critical" will not carry the argument. That is the moment to quantify — which is exactly the next post.

## Key takeaways

- A risk score is **likelihood × impact**, kept as two visible dimensions.
- **Write anchors for every level.** Undefined words make the matrix arbitrary.
- Use the score to **rank and band**, never to compute money — ordinal ≠ ratio.
- **List controls and re-score** for residual; calibrate people in a workshop.
- The matrix **triages**; quantification decides the few expensive cases.

Next: [FAIR in 15 minutes — quantitative risk for busy people](/posts/fair-in-15-minutes/).
