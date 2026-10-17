---
title: "Designing KRIs That Predict, Not Just Report"
date: 2026-10-17
description: "Most risk metrics tell you what already went wrong. Key Risk Indicators should warn you before it does. How to pick drivers, set thresholds, and build a KRI catalogue that earns trust."
categories: ["Metrics & Reporting"]
tags: ["kri", "kpi", "metrics", "leading indicators", "thresholds", "reporting"]
level: 5
weight: 7
---

There is a moment when a risk programme grows up: it stops reporting incident counts and starts predicting them. That is the jump from **KPIs** to **KRIs**, and it is what separates a dashboard people glance at from one leaders act on.

## KRI vs. KPI, in one line

- A **KPI** measures **performance** — how well you are doing. *Number of incidents last quarter.*
- A **KRI** measures **risk** — how likely something is to go wrong. *Percentage of critical systems without MFA.*

KPIs look **backward** (results). KRIs should lean **forward** (exposure). The best KRIs are **leading indicators**: they move *before* the loss does.

| | Lagging | Leading |
| --- | --- | --- |
| Example | Breaches this quarter | Open critical vulnerabilities past SLA |
| Tells you | What happened | What is about to happen |
| Usefulness | Justifies the past | Enables a decision now |

Lagging metrics are not useless — they validate your model and reassure boards. But if *all* your metrics are lagging, you are managing risk through the rear-view mirror.

## What makes a KRI good

Five properties. Miss one and the metric drifts into noise:

1. **Predictive** — plausibly linked to a risk you care about.
2. **Measurable** — from data you can actually collect, reliably and cheaply.
3. **Owned** — one named human can move it.
4. **Thresholded** — it has green/amber/red bands, so it signals when to act.
5. **Actionable** — breaching it triggers a known response.

A metric without a **threshold** and an **owner** is trivia. It will sit on the dashboard forever, changing nothing.

## Build a KRI: the four-step loop

Work back from the risk:

```
1. Pick a risk        →  "Credential compromise leading to account takeover"
2. Name the driver    →  weak authentication, privileged access sprawl
3. Choose the metric  →  % of accounts with MFA; # of standing admin accounts
4. Set thresholds     →  green <2%, amber 2–5%, red >5%; owner; response
```

The driver is the crux. A KRI measures a **cause** of the risk, not the risk itself — because you cannot yet measure an event that has not happened.

## A starter KRI catalogue

| Domain | Example KRI | Threshold trigger | Owner |
| --- | --- | --- | --- |
| Identity | % of accounts with MFA enforced | <98% → escalate | IAM lead |
| Patching | % of critical vulns past SLA | >5% → escalate to CISO | Ops |
| Privileged access | # of standing (always-on) admin accounts | any increase → review | IAM lead |
| Backups | % of systems with tested restore in 90 days | <90% → infra review | Infra lead |
| Third party | # of critical vendors with expired assurance | >0 → procurement action | Vendor mgr |
| Change | % of significant changes without risk assessment | <95% → process review | Change mgr |
| Culture | Median days from risk raised to acknowledged response | >30 days → review | Risk lead |

Notice every row has **threshold, owner, and response**. That is the difference between a report and a control.

## Cascade from appetite

KRIs should not float free. They are the **operational expression of your appetite and tolerance**: if the board says "no more than 4 hours unplanned downtime per quarter", the KRI is "downtime hours to date vs. tolerance", with amber at 3 hours. This is the link that makes the board dashboard meaningful rather than decorative.

## Common mistakes

- **Vanity metrics.** Numbers that only ever look good. If a KRI can never be red, it is not measuring risk.
- **Too many.** Twenty KRIs means none are watched. Pick a handful per domain and defend them.
- **All lagging.** You learn of failure after the fact.
- **No thresholds.** A number without a band cannot trigger anything.
- **No owner.** Nobody can move it, so nothing happens.
- **Gameable metrics.** If "incidents reported" is punished, people stop reporting. Watch for metrics that incentivise hiding.
- **Metric without a decision.** If breaching it changes nothing, delete it.

## Reporting them honestly

- **Show trend, not just status.** A KRI at amber and rising is a different story from amber and falling.
- **Report against thresholds**, so red is unambiguous.
- **Keep it short.** Five to seven KRIs at board level; the rest live in operational reviews.
- **Close the loop.** When a KRI goes red, say what was done. Otherwise the dashboard teaches people that red means nothing.

## Key takeaways

- **KPIs measure performance; KRIs measure exposure.** Prefer **leading** indicators that move before the loss.
- A good KRI is **predictive, measurable, owned, thresholded, and actionable**.
- Build from the **driver** of the risk, since the event has not happened yet.
- **Thresholds + owners + responses** are what turn a metric into a control.
- **Cascade KRIs from appetite**, report **trend against thresholds**, and always **close the loop**.

Next: [five conversations that shift risk culture](/posts/five-conversations-that-shift-risk-culture/).
