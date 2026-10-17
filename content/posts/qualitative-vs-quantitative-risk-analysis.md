---
title: "Qualitative vs. Quantitative Risk Analysis: When to Use Each"
date: 2026-10-05
description: "High/medium/low is fast but fuzzy. FAIR and Monte Carlo are defensible but slow. The skill is knowing which one the decision deserves."
categories: ["Risk Assessment"]
tags: ["qualitative", "quantitative", "FAIR", "monte carlo", "scoring matrix"]
level: 2
weight: 3
---

There is a tired argument in risk circles: qualitative vs. quantitative analysis, as if one is correct and the other is malpractice. In reality they are tools for different jobs, and a competent practitioner uses both — often on the same risk.

## Qualitative analysis: fast, cheap, subjective

Qualitative analysis ranks risks using words or a small scale — Low / Medium / High, or a 1–5 likelihood × 1–5 impact matrix.

**Good for:**
- Screening a long list of risks to find the ones that matter.
- Environments where data does not exist.
- Fast, frequent conversations where speed beats precision.

**Weak at:**
- Comparing very different risks ("is the HR system risk worse than the data-centre risk?").
- Justifying spend. "High" does not unlock a budget.
- Withstanding scrutiny. Two experts can land on different scores for the same risk.

The failure mode of qualitative analysis is **false precision disguised as simplicity** — a matrix with no defined scoring criteria, where "High" means whatever the loudest person in the room wants it to mean.

## Quantitative analysis: slower, more defensible

Quantitative analysis expresses risk as a **distribution of possible losses in money** (and sometimes time). The best-known method in IT/cyber is **FAIR** (Factor Analysis of Information Risk). You estimate:

- **Frequency** — how often the event happens (times per year).
- **Loss magnitude** — what each occurrence costs.

Instead of a single number, you get a range — e.g. *"annualised loss: 80% likely between $200k and $1.4M, most likely $600k."* Run it enough times (Monte Carlo) and you get a distribution you can reason about.

**Good for:**
- Big, expensive, or contentious decisions.
- Justifying (or refusing) a security investment.
- Comparing risks in a common currency: money.
- Talking to finance, the board, and insurers.

**Weak at:**
- Speed. It takes real effort per risk.
- Inputs. Garbage estimates produce confident-looking garbage.
- Culture. Many organisations are not ready to hear "we accept $600k of expected annual loss."

## The hybrid approach most teams should use

You rarely need to pick one for the whole programme. Use them in layers:

1. **Screen everything qualitatively.** Cheap triage across the full register.
2. **Quantify the top handful.** The 3–10 risks where a real decision and real money are at stake.
3. **Feed the results back.** The quantified loss for a top risk often recalibrates how you label the others.

This is the "qualitative to triage, quantitative to decide" pattern, and it is where most mature programmes settle.

## A worked contrast

Take a risk: *"Ransomware encrypts a core system."*

**Qualitative:** Likelihood 4, Impact 5 → Critical. Prioritise. Everyone agrees it is bad. Nobody knows if the fix is worth its price.

**Quantitative (FAIR, toy numbers):** Frequency 0.3/yr. Loss per event: $400k–$3M. Annualised loss, 90th percentile ≈ $1.5M. Now compare against the $250k/yr cost of the mitigation. The conversation just got much easier — and much shorter.

## Calibrating your estimates

Quantitative analysis lives or dies on estimates. Two habits keep them honest:

- **Use ranges, never single points.** "Between 2 and 10 days of downtime" beats "5 days".
- **Calibrate people.** Ask "how often do events like this happen?" across credible sources and eat your own dog food — did last year's estimate hold up?

No estimate is perfect. A calibrated rough range still beats an unaccountable "High".

## Key takeaways

- **Qualitative** triages; **quantitative** decides.
- Publish **written scoring criteria** so qualitative scores mean the same thing to everyone.
- Use **ranges and distributions**, not single numbers, when you quantify.
- Quantify the **few risks where real money and real decisions** are at stake — not the whole register.

Next: [the IT risk frameworks you'll meet — and when each one earns its keep](/posts/it-risk-frameworks-explained/).
