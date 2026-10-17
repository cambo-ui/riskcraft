---
title: "Risk Appetite Statements the Board Will Actually Approve"
date: 2026-10-17
description: "\"We have a low appetite for risk\" is not a statement, it's a shrug. How to write appetite that links to strategy, survives the boardroom, and turns into thresholds people can act on."
categories: ["Governance & Oversight"]
tags: ["risk appetite", "board", "governance", "reporting", "strategy"]
level: 4
weight: 6
---

Most risk appetite statements are written once, approved without much thought, and then ignored forever. They say things like *"we have a low appetite for risk"* or *"risk is managed in line with our values"* — sentences that cannot be tested, disagreed with, or acted on.

The test of a good appetite statement is simple: **can you hold a specific risk up against it and get a yes or no?** If not, it is decoration.

## Why appetite statements fail

- **Unmeasurable.** "Low" and "moderate" mean nothing without units.
- **Disconnected from strategy.** Appetite exists to *enable* strategy — to say how much risk you will take to win — not to be cautious for its own sake.
- **Written for the wrong reader.** Lawyers and risk teams draft them; operators have to use them. If operators cannot act, it is fiction.
- **No tolerances.** Appetite without thresholds produces no monitoring, no escalation, and no decisions.
- **Copy-paste from another company.** Someone else's appetite reflects *their* capital, objectives, and regulation.

## What the board actually needs

Boards are being asked to *govern* risk, not recite it. They need statements that are:

1. **Strategy-linked** — tied to the objectives the board already cares about.
2. **Quantified where possible** — hours, dollars, counts, percentages.
3. **Domain-specific** — one line per material risk area, not one vague umbrella.
4. **Operationalised** — each with a tolerance (threshold) and an owner.
5. **Reportable** — something you can show a position against, every quarter.

## A worked example

Here is what a usable statement set looks like. This is a template — tune it to your objectives.

| Domain | Appetite statement | Tolerance / threshold | Owner |
| --- | --- | --- | --- |
| **Availability** | We will accept no more than 4 hours of unplanned downtime per quarter for tier-1 systems. | Escalate at 3h; board brief at >4h | CTO |
| **Customer data confidentiality** | We have a **low** appetite: no known unauthorised access to customer data is acceptable. | Any confirmed access → immediate escalation | CISO |
| **Financial loss** | We will accept up to $500k annualised cyber loss before changing strategy. | Review at $300k; act at $500k | CFO |
| **Compliance** | We have a **zero** appetite for regulatory breaches and will invest to prevent them. | Any breach = material event | CCO |
| **Innovation / delivery** | We will accept **high** delivery risk on new products to move fast, within security baselines. | Post-incident review, no threshold | CPO |
| **Third party** | We accept third-party risk only where assurance and exit options exist. | No critical vendor without exit plan | CISO |

Two things make this work. First, the **units** — hours, dollars, "zero", "no critical vendor". Second, the **tolerances** — the "escalate at / act at" column, which is what turns appetite into monitoring and alarms.

Note also that appetite is not uniformly low. A mature statement deliberately accepts **high** risk somewhere (delivery, innovation) — that is appetite doing its job of enabling strategy.

## Linking appetite to strategy

The board thinks in strategy. So frame appetite in the same language:

> *"Our strategy requires us to launch two new digital products this year. To do that we accept elevated delivery and availability risk on new systems, but we will not accept elevated confidentiality risk to customer data or any compliance breach."*

Now the board is not approving a risk document — it is approving a **stance toward its own strategy**. That is a decision it can make, defend, and revisit.

## From appetite to action

Appetite becomes real through three mechanical steps:

1. **Tolerance → thresholds.** Every statement gets a threshold that monitoring can watch. No threshold, no control loop.
2. **Position vs. appetite reporting.** Each quarter, report *where you stand* against each domain. A gap is a visible decision.
3. **Named owners.** Someone — a human, not a committee — is accountable for each domain.

This is the same machinery as [appetite, tolerance and capacity](/posts/risk-appetite-tolerance-capacity/), now at board scale.

## Getting it approved

- **Draft with the executives who own the objectives**, not in isolation. Ownership up front prevents a rubber stamp.
- **Bring the trade-off.** Show the cost of a tighter appetite in money or speed. Boards approve choices, not absolutes.
- **Keep it short.** One page. If it needs an appendix to be understood, it will not be used.
- **Set a review cadence** (annually, or when strategy changes). Appetite is a living stance.

## Common mistakes

- **Writing appetite below capacity you actually have**, then watching the business bypass risk — which teaches everyone the rules are optional.
- **Setting appetite above capacity.** That is not ambition; it is negligence.
- **No tolerance.** Appetite without thresholds is a slogan.
- **Never reporting against it.** If the board never sees a position versus appetite, appetite does not exist.

## Key takeaways

- A good appetite statement is **measurable, strategy-linked, domain-specific, operationalised, and reportable**.
- **Tolerances turn appetite into thresholds** — without them there is no monitoring or escalation.
- Good appetite is **not uniformly low**; it deliberately accepts high risk where strategy needs it.
- The board approves a **stance toward its strategy**, with trade-offs shown.
- **Report position versus appetite** every cycle, or the statement is decoration.

Next: [third-party and supply-chain risk — a practical playbook](/posts/third-party-supply-chain-risk/).
