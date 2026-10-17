---
title: "How to Write a Risk Statement That Isn't Vague"
date: 2026-10-16
description: "A risk register full of 'cloud risk' and 'insider threat' is a list of feelings. The cause → event → impact formula turns each row into something you can actually decide about."
categories: ["Foundations"]
tags: ["risk statement", "risk register", "writing", "assessment"]
level: 1
weight: 4
---

The fastest way to tell whether an organisation *does* risk management or merely *has* a risk register is to read the rows. If they look like this, it is a list of feelings:

> ~~Cloud risk. Insider threat. Third-party risk. Budget. AI.~~

None of those tell you what to do. A **risk statement** is the fix, and it costs you one sentence per risk.

## The formula

> **Because of** *[cause]*, **there is a risk that** *[event]*, **which would result in** *[impact]*.

Three parts, in order:

| Part | What it captures | Fails when |
| --- | --- | --- |
| **Cause** | The condition creating exposure | Vague ("poor security") |
| **Event** | What happens if it lands | Missing or sensational |
| **Impact** | The business consequence | Unstated or purely technical |

Each part earns its place. The **cause** tells you what to change. The **event** tells you what you are worried about. The **impact** tells you why anyone else should care.

## Bad → better

**Bad:** *"Cloud risk."*

**Better:** *"Because our cloud workloads run without centralised logging, there is a risk that a compromise goes undetected for weeks, which would result in extended data exposure and regulatory notification costs."*

Now you know what to fix (logging), what the scenario is (undetected compromise), and what it costs (exposure + notification). A decision is possible.

Another:

**Bad:** *"Insider threat."*

**Better:** *"Because departing engineers retain production credentials for 30 days, there is a risk of unauthorised access after departure, which would result in data loss or sabotage."*

The cause is specific and fixable: offboarding. Offboarding risk, not "insider threat".

## Test every statement with three questions

1. **Could two different people read this and picture the same scenario?** If not, it is too vague.
2. **Does it name a cause you can act on?** If nothing can change, it is a complaint, not a risk.
3. **Is the impact in business terms** (money, downtime, trust, compliance), not just "security"?

If all three are yes, the statement is doing its job.

## Common traps

- **The topic trap.** Registering a category ("Cloud") instead of a risk. Topics belong in the category column; risks belong in the row.
- **The consequence-free risk.** Naming an event but never an impact. "Data breach" is not an impact; fines, downtime, churn, and trust are.
- **The control-in-disguise.** *"We lack MFA"* is a control gap, not a risk. The risk is what could happen because of it.
- **The sensational event.** Over-dramatising ("total collapse") destroys credibility. Be concrete and credible.
- **Multiple risks in one row.** If it has two causes and two impacts, it is two risks. Split it.

## Standardise so it scales

Once the formula is fixed, consistency does the heavy lifting. In a register of 200 rows, uniform statements let you:

- **Group and de-duplicate** similar risks.
- **Sort meaningfully** by impact and likelihood.
- **Hand rows to owners** and have them understand instantly.
- **Compare over time** without rewriting everything.

Write the formula into your template and your [Pages CMS](https://app.pagescms.org) or spreadsheet header. Make the good shape the path of least resistance.

## Key takeaways

- **Because of [cause], there is a risk that [event], which would result in [impact].**
- Each part is load-bearing: the cause points to the fix, the event to the scenario, the impact to the business.
- Test statements for **shared picture, actionable cause, business impact**.
- Avoid topics, control gaps, sensationalism, and multi-risk rows.
- **One formula, used everywhere**, is what makes a large register usable.

Next: [risk appetite vs. tolerance vs. capacity](/posts/risk-appetite-tolerance-capacity/).
