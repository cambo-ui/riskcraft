---
title: "FAIR in 15 Minutes: Quantitative Risk for Busy People"
date: 2026-10-17
description: "You don't need a data science team to put a number on risk. FAIR in plain terms: frequency, loss magnitude, ranges, and a worked example you can run in a spreadsheet."
categories: ["Risk Assessment"]
tags: ["fair", "quantitative", "monte carlo", "loss magnitude", "risk assessment"]
level: 2
weight: 5
---

"High risk" cannot approve a budget. "We expect to lose about $1.2M a year, with a 1-in-10 chance of exceeding $4M" can. That is what **FAIR** (Factor Analysis of Information Risk) gives you — a way to express cyber and IT risk in money, using ranges rather than false precision.

Here is the whole method, stripped to what a busy practitioner actually needs.

## The model is two questions

FAIR reduces risk to two factors:

```
Risk  =  Frequency (how often)  ×  Loss Magnitude (how bad each time)
```

That's it. Everything else in FAIR is decomposing those two — but the core is refreshingly simple, and you can get value without the full taxonomy.

- **Frequency** → expressed as *events per year* (e.g. 0.3, meaning roughly once every 3 years).
- **Loss Magnitude** → the total cost *per event*, including response, downtime, fines, and lost business.

Risk = frequency × loss = **expected annual loss**. That is a number finance understands.

## Use ranges, not points

The single most important habit: estimate **ranges**, never single numbers. You do not know the loss is exactly $500k; you know it is *probably between $200k and $1.5M*.

The common shape is a **PERT** (or triangular) distribution — three numbers per factor:

| Estimate | Meaning |
| --- | --- |
| **Minimum** | Best case (still plausible) |
| **Most likely** | Your single best guess |
| **Maximum** | Worst case (still plausible) |

Example frequency: min 0.1, most likely 0.3, max 1.0 events/year.
Example loss: min $150k, most likely $400k, max $2M.

## Run it (Monte Carlo, no maths degree required)

A Monte Carlo simulation just samples those ranges thousands of times and multiplies. In plain terms:

1. Pick a random frequency from the frequency range.
2. Pick a random loss from the loss range.
3. Multiply → one simulated year of loss.
4. Repeat 10,000 times.
5. Look at the distribution of results.

A spreadsheet, a short script, or a FAIR tool does this instantly. The output looks like:

| Statistic | Annualised loss |
| --- | --- |
| 10th percentile | $45k |
| **Most likely (median)** | **$310k** |
| 90th percentile | $1.4M |
| Mean | $520k |

Now you have a sentence: *"Expected annual loss around $310k, but a 1-in-10 chance it exceeds $1.4M."*

## The decision this unlocks

Suppose a control costs **$150k/year** and would cut both frequency and loss by roughly half.

- Current expected loss (mean): ~$520k
- Expected loss after control: ~$260k
- **Annual saving: ~$260k for a $150k cost → worthwhile.**

That is a risk decision in dollars, not adjectives. It also works in reverse: if the control cost $800k, you now have a defensible reason to *decline* it — and leadership will believe you, because the maths is visible.

## Where the value really comes from

Counter-intuitively, the benefit is less about *precision* and more about **decomposition and conversation**:

- **It makes assumptions explicit.** "Frequency 0.3 and loss $400k" is arguable; "High risk" is not.
- **It separates frequency from magnitude.** Teams often conflate them; FAIR forces them apart, which changes which control matters.
- **It surfaces disagreement usefully.** When two experts disagree, you can see *where* — on frequency or on loss.
- **It ranks across unlike risks.** Money is the common denominator a payroll system risk and a website risk share.

## Common objections, answered

- *"We don't have data."* Perfect estimates are not required. Calibrated ranges from people who know the system beat a matrix of undefined words. And you only quantify the handful of risks that matter.
- *"It's too slow."* With practice, a single FAIR analysis takes 30–60 minutes. You will not do it for 200 risks — you will do it for the 5–10 that involve real money.
- *"The numbers will be wrong."* They will be *ranges*, and they will be far closer to reality than "High". A rough calibrated estimate beats an unaccountable label.

## How to start

1. Pick your **top three** risks from the register.
2. For each, write min / most-likely / max for **frequency** and **loss**.
3. Run the simulation (spreadsheet or tool).
4. Compare the results to the qualitative ranking. Do they agree? Where they disagree, you have learned something.
5. Use the output the next time a budget decision comes up.

## Key takeaways

- **FAIR = frequency × loss magnitude**, expressed as expected annual loss in money.
- Always estimate **ranges**, never single points; output a distribution, not one number.
- **Monte Carlo** just samples the ranges and multiplies — no maths degree needed.
- The real win is **explicit assumptions and better conversations**, not precision.
- Quantify the **few risks** where real money and real decisions are at stake.

Next: [control types — preventive, detective, corrective, deterrent](/posts/control-types/).
