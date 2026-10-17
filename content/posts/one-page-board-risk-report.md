---
title: "Writing a One-Page Board Risk Report"
date: 2026-10-17
description: "The board will not read a 40-page pack. How to give them the top risks, the trend, the position against appetite, and the decisions you need — on one page."
categories: ["Governance & Oversight", "Metrics & Reporting"]
tags: ["board reporting", "reporting", "governance", "executive", "risk report"]
level: 5
weight: 10
---

A risk report that nobody reads has zero value, no matter how accurate. Boards govern risk in **minutes, not hours** — so the report must be short, business-framed, and **decision-oriented**. One page is the discipline that forces it.

## What the board actually needs

Boards are accountable for oversight, not operations. They need to answer four questions:

1. **What are the material risks** right now?
2. **Are they getting better or worse?**
3. **Are we inside our appetite?**
4. **What decisions do you need from us?**

If your report does not answer all four, it is a status update, not a governance tool.

## The one-page structure

```
┌───────────────────────────────────────────────────────────────┐
│ 1. HEADLINE          3 bullets: the story in 15 seconds        │
├───────────────────────────────────────────────────────────────┤
│ 2. TOP RISKS         table: 5–7 risks, owner, trend, movement  │
├───────────────────────────────────────────────────────────────┤
│ 3. APPETITE          position vs. tolerance, by domain         │
├───────────────────────────────────────────────────────────────┤
│ 4. WHAT CHANGED      since last time: new, closed, escalated   │
├───────────────────────────────────────────────────────────────┤
│ 5. THE ASKS          decisions required, with a recommendation │
└───────────────────────────────────────────────────────────────┘
```

Every element earns its place. Let's take them in turn.

### 1. Headline — the 15-second version

Three bullets, in business language. A board member should understand the state of risk from these alone.

> - Two risks remain **above appetite**; both have funded remediation under way.
> - Overall risk exposure is **stable**; ransomware and third-party concentration are the top two.
> - **One decision requested:** approve a $180k control affecting two top risks.

### 2. Top risks — a table, not a document

Five to seven risks. More than that is a data dump. Each row: business description, owner, trend, and *what changed*.

| # | Risk (business language) | Owner | Rating | Trend | Change since last report |
| --- | --- | --- | --- | --- | --- |
| R1 | Ransomware disrupts order fulfilment | CISO | High | ▲ | Backup testing gaps found |
| R2 | Cloud provider outage stops trading | CTO | High | ▬ | Exit plan drafted |
| R3 | Customer data breach via portal | CISO | Medium | ▼ | MFA completed |
| R4 | Critical vendor failure | COO | Medium | ▲ | New dependency added |
| R5 | Regulatory breach (data residency) | CCO | Low | ▬ | No change |

Rules: **business language**, **one owner each**, **a trend arrow**, and a **"what changed"** column. The change column is what makes a report worth reading.

### 3. Appetite — position vs. tolerance

This is where the [appetite statements](/posts/risk-appetite-statements-for-the-board/) pay off. Show where you stand against each domain's tolerance.

| Domain | Tolerance | Position | Status |
| --- | --- | --- | --- |
| Availability | ≤ 4h/quarter | 3.5h | 🟡 Amber |
| Customer data confidentiality | zero known access | zero | 🟢 Green |
| Financial loss | ≤ $500k annualised | $380k | 🟡 Amber |
| Compliance | zero breaches | zero | 🟢 Green |

Amber and red here are the board's **early warning system** — and the reason the KRI work matters.

### 4. What changed

Three to five lines. New risks, closed risks, escalations, and anything that surprised you. A board that sees only a static list cannot tell whether management is on top of things.

### 5. The asks

End with **decisions**, not information. Every ask carries a recommendation.

> - **Approve** the $180k authentication control (recommended: yes — reduces R1/R3 below appetite).
> - **Accept** the residual risk on R5 pending the 2027 re-platform (recommended: accept).
> - **Note** the updated third-party concentration position.

## Principles that make it work

- **One page.** If it does not fit, you have not decided what matters. Put detail in an appendix; the board reads the page.
- **Business language.** "Order fulfilment stops" beats "availability of the OMS cluster". Define any term you must use.
- **Trend beats snapshot.** Arrows and "what changed" tell the story a static list hides.
- **Lead with the ask.** Put decisions where they are seen, with a clear recommendation.
- **Consistency.** Same structure every time; the board learns to read it in seconds.
- **Honesty.** If a risk is rising and unfunded, say so. A report that only reassures is worse than none.

## Common mistakes

- **The 40-page pack.** Nobody reads it; the message drowns.
- **Risk-speak.** A board cannot govern jargon it does not share.
- **A list with no trend.** A snapshot hides deterioration.
- **No owner.** A risk the board cannot attach to a person cannot be overseen.
- **No ask.** Information without a decision wastes the board's scarcest resource: attention.
- **Burying bad news.** Delayed bad news is four times as expensive when it arrives late.

## Putting it together

1. Pull the **top 5–7 risks** by residual rating, in business language.
2. Add **owner, trend, and what changed**.
3. Show **position vs. appetite** from your [KRIs](/posts/kris-that-predict/).
4. Write the **three-bullet headline** last, once the page exists.
5. End with **the asks and your recommendation**.
6. Keep it to **one page.** Always.

---

*You have reached the summit of the path.* Level 5 closes the loop: culture, metrics, leadership, and the artefact — the one-page report — that ties a risk programme to the people who govern it. From here, the work is depth, repetition, and judgement. See the [learning path](/learning-path/) or browse [topics](/categories/).
