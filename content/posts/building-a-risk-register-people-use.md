---
title: "Building a Risk Register People Actually Use"
date: 2026-10-03
description: "Most risk registers are graveyards: rows nobody reads, scores nobody trusts, owners who never agreed. Here's how to build one that drives decisions."
categories: ["Foundations", "Risk Assessment"]
tags: ["risk register", "risk assessment", "owners", "scoring"]
level: 1
weight: 2
---

Every organisation has a risk register. Almost none of them are *used*. They exist to satisfy an auditor, then rot.

A register is only worth building if it changes what people do. That is the design constraint. Here is how to build one that survives contact with reality.

## Start with the decision, not the spreadsheet

Before you open a spreadsheet, answer this: **who is going to make what decision from this register?**

- If it's the board: they need the top 10 risks, in business language, with trend and ownership.
- If it's a steering committee: they need risks tied to projects and budgets.
- If it's an engineering team: they need a work queue with clear actions.

One register trying to be all three serves none. Pick the primary consumer and design for them.

## The fields you actually need

A good register is small. Every extra column is a column that goes stale.

| Field | Why it exists |
| --- | --- |
| **ID** | So you can reference it forever. `RISK-0142`. |
| **Title** | One line, in business language. |
| **Description** | The risk *statement* (see below). |
| **Category** | For grouping and reporting. |
| **Owner** | A single named human who agreed to own it. Not a team. Not "IT". |
| **Inherent likelihood / impact** | Before controls. |
| **Controls in place** | What already reduces it. |
| **Residual likelihood / impact** | After controls. This drives priority. |
| **Treatment** | Avoid / mitigate / transfer / accept. |
| **Action & due date** | What happens next, and by when. |
| **Status / trend** | Open, mitigating, accepted, closed; is it getting better or worse? |

That is it. If you cannot fill a field for every row, the field does not belong.

## Write risk statements that aren't vague

The single best upgrade to any register is a consistent **risk statement**. Use this shape:

> **Because of** *[cause]*, **there is a risk that** *[event]*, **which would result in** *[impact]*.

Weak: *"Cloud risk."*

Strong: *"Because our backup restore process is untested, there is a risk we cannot recover a deleted production database within the SLA, which would result in extended outage and contractual penalties."*

The second version tells you what to fix. The first tells you nothing.

## Owners must truly own

A risk owner is not the person who knows the most about the risk. They are the person **with the authority and budget to do something about it**. If you assign a risk to someone who cannot act, you have assigned it to nobody.

Get explicit agreement. "I've put you down as owner" is not consent.

## Score honestly, and keep it boring

Pick a simple scale — say 1–5 for likelihood and impact — and **write down what each number means**. Otherwise two people scoring "4" mean different things and the whole register loses credibility.

A 5×5 matrix is plenty for most organisations. Save quantitative analysis for the handful of risks where the money actually matters.

## Make it a living thing

- **Review on a cadence**, not just before audits.
- **Report the top few** — a register of 300 risks is a data dump, not a report.
- **Track trend.** A risk that is stable at "high" tells a different story from one racing upward.
- **Retire risks loudly.** Closing a risk is a win; say so.

## Key takeaways

- Design the register for **one primary decision-maker**.
- Keep the fields **minimal and always filled**.
- Write every risk as a **cause → event → impact** statement.
- Owners need **authority**, not just knowledge.
- Define your **scoring scale in writing** and review on a cadence.

Next: [qualitative vs. quantitative risk analysis](/posts/qualitative-vs-quantitative-risk-analysis/).
