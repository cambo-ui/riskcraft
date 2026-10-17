---
title: "The Risk Management Lifecycle, Step by Step"
date: 2026-10-15
description: "Identify, analyse, evaluate, treat, monitor, communicate. The core loop that turns risk from a one-off spreadsheet exercise into a repeatable, defensible process."
categories: ["Foundations"]
tags: ["risk lifecycle", "risk process", "iso 31000", "treatment"]
level: 1
weight: 3
---

Most organisations do risk as an event: a workshop, a spreadsheet, an audit. Then it stops. Risk management is not an event — it is a **loop you keep running**. This is the loop, and it is the same whether you follow ISO 31000, NIST, or your own method.

## The loop

```
        ┌──────────────────────────────────────────────┐
        │                                                │
   ┌────▼─────┐   ┌──────────┐   ┌──────────┐   ┌───────▼──┐
   │ Identify │──▶│ Analyse  │──▶│ Evaluate │──▶│  Treat   │
   └──────────┘   └──────────┘   └──────────┘   └────┬─────┘
        ▲                                             │
        │              ┌───────────┐                  │
        └──────────────│  Monitor  │◀─────────────────┘
                       └─────┬─────┘
                             │
                    ┌────────▼─────────┐
                    │ Communicate &    │  (runs through every step)
                    │ Consult          │
                    └──────────────────┘
```

Let's take each in turn.

## 1. Identify

Find and describe risks. Sources: risk workshops, incident history, threat intel, audit findings, architecture reviews, vendor assessments, near-misses.

The output is **risk statements** (cause → event → impact), not topics. "Cloud" is not a risk; "we cannot recover a deleted database within the SLA" is.

## 2. Analyse

Understand each risk: how likely, how bad, and what drives those numbers. This is where you use [qualitative or quantitative methods](/posts/qualitative-vs-quantitative-risk-analysis/) and consider existing controls to get from **inherent** to **residual** risk.

## 3. Evaluate

Compare the residual risk against your **criteria** — your appetite and tolerance. The question is not "is it bad?" but **"is it acceptable, or must we act?"** This step is where most registers fail: they list risks but never judge them against a standard.

## 4. Treat

Choose a response and assign an owner with a date. There are only four options:

| Treatment | Meaning |
| --- | --- |
| **Avoid** | Stop doing the activity that creates the risk |
| **Mitigate** | Add or improve controls to reduce likelihood or impact |
| **Transfer** | Shift it — insurance, contract, outsourcing |
| **Accept** | Deliberately carry it; document why |

"Accept" is a real option, not a failure. The sin is accepting *by accident*.

## 5. Monitor and review

Risks change. Threats evolve, controls decay, priorities shift. Review on a cadence, re-score when things change, and watch for **control drift** — the slow erosion of a control that was fine last year.

## 6. Communicate and consult

This is not a final step; it runs through everything. The right people — owners, leadership, the board — must know what matters and what is being done. A risk nobody is informed about is a risk nobody manages.

## The loop is the point

A one-off assessment tells you where you stood. A loop tells you where you are going. The value is in the *repeatability*: every risk gets the same treatment, every decision is documented, and the whole thing survives staff turnover.

Three habits make the loop real:

- **Cadence over intensity.** A quarterly light review beats an annual heroic one.
- **Owners, always.** Every risk has one accountable human.
- **Close the loop publicly.** Report what changed, including accepted risks — silence reads as "nobody cared".

## Key takeaways

- Risk management is a **loop**, not an event: identify → analyse → evaluate → treat → monitor.
- **Evaluate against a criterion** (appetite/tolerance) — listing risks is not evaluating them.
- There are exactly **four treatments**; "accept" is legitimate when it is deliberate and documented.
- **Communicate throughout**, not at the end.

Next: [how to write a risk statement that isn't vague](/posts/writing-a-risk-statement/).
