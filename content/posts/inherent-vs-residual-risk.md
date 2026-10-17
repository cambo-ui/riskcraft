---
title: "Inherent vs. Residual Risk, Explained Simply"
date: 2026-10-12
description: "Miss this distinction and your risk register becomes fiction. Inherent risk shows how much work there is to do; residual risk is what you actually manage, report and accept."
categories: ["Foundations"]
tags: ["inherent risk", "residual risk", "controls", "risk register"]
level: 0
weight: 3
---

If there is one pair of terms that separates people who *do* risk from people who *talk about* risk, it is **inherent** and **residual**. Confuse them and your register quietly becomes fiction: risks scored as if no controls existed, or worse, as if every control worked perfectly.

## The two numbers

- **Inherent risk** — the exposure *before* you apply controls. Your raw starting position.
- **Residual risk** — the exposure *remaining after* controls. What is left once your defences have done their job.

Same risk, two viewpoints:

| | Likelihood | Impact |
| --- | --- | --- |
| **Inherent** | 4 (high — nothing stops it) | 5 (major outage) |
| **Controls** | MFA, patching, monitoring | Backups, IR plan, redundancy |
| **Residual** | 2 | 3 |

Inherent says *how much work exists*. Residual says *how much risk you are actually carrying* — and therefore how much you are asking someone to accept.

## Why you need both

**Inherent risk** tells you where the raw danger is, and how much control investment is justified. A risk with enormous inherent exposure and weak controls deserves attention even if it has never materialised.

**Residual risk** is the only number that supports a decision. It is what the owner accepts, what you report to the board, and what regulators and auditors care about. If you only track one, track residual — but track inherent too, or you cannot see the effect of your controls.

## The trap: assuming controls work

Residual risk is an **estimate of effectiveness**, and the most common failure is assuming controls are 100% effective just because they are documented.

- "We have backups" → do they restore? Have you tested in the last quarter?
- "We have MFA" → on every path, including the legacy VPN?
- "We have monitoring" → is anyone watching, and would they respond in time?

Documented control ≠ effective control. If you score residual as if everything works, you are managing a fantasy.

## How to score it honestly

1. **Score inherent first**, deliberately ignoring existing controls. This is your honest starting exposure.
2. **List the controls**, one line each.
3. **Judge effectiveness, not existence** — use evidence (tests, incidents, audit results), not optimism.
4. **Score residual** as a genuine view of what is left.
5. **Record who accepted it** and when.

Keep both scores in the register. The gap between them is, quite literally, the value of your control environment — and a board can see it.

## A worked example

*Risk: "Because the customer portal has no rate limiting, there is a risk of credential-stuffing, leading to account takeover and fraud."*

- **Inherent**: Likelihood 4, Impact 4 → High. Nothing stops it today.
- **Controls**: MFA on 80% of accounts, anomaly alerts on logins, no CAPTCHA.
- **Residual**: Likelihood 3, Impact 4 → still High, driven by the 20% without MFA.
- **Action**: enforce MFA for the remaining accounts by a date, then re-score.

Notice the inherent score motivates the work; the residual score tells you the risk is *still* not acceptable. Both matter.

## Key takeaways

- **Inherent = before controls. Residual = after controls.** They answer different questions.
- **Residual risk is what you accept, report, and manage.** Inherent tells you how much work exists.
- Judge controls by **effectiveness, backed by evidence**, not by their presence in a document.
- Always **record who accepted the residual risk** — that is the accountability trail.

Next: [the CIA triad and why it anchors everything](/posts/cia-triad/).
