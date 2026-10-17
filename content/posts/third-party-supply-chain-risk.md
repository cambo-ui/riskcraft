---
title: "Third-Party and Supply-Chain Risk: A Practical Playbook"
date: 2026-10-17
description: "You inherit the risk of every vendor you depend on — and you can't audit your way out of a supply chain. A tiered, lifecycle approach you can actually run."
categories: ["Third-Party Risk"]
tags: ["third-party risk", "supply chain", "vendors", "tprm", "concentration risk"]
level: 4
weight: 7
---

Every vendor you depend on extends your risk surface — without extending your control. When you adopt a SaaS platform, you accept its outages, its breaches, its insolvency, and the risks of *its* suppliers. You cannot secure your way out of someone else's problem, but you can **manage the relationship deliberately**.

This is the playbook: tier, assess, contract, monitor, and exit.

## Why it deserves its own programme

- **Inherited risk.** A provider's incident is your incident — to your customers and your regulator.
- **Concentration.** Ten services running on one cloud region, or one identity provider for everything, is a single point of failure even if each is "approved".
- **Nth parties.** Your vendor's subcontractors are outside your visibility and inside your blast radius.
- **Regulatory pressure.** Rules increasingly hold you accountable for the resilience of your critical providers, not just your own systems.

## Step 1: Tier your vendors

Do not assess 800 vendors with the same intensity. **Tier by criticality** — the combination of impact and access.

| Tier | Criteria | Assessment depth |
| --- | --- | --- |
| **Tier 1 — Critical** | Business stops or data breaches if they fail; holds sensitive data; deep system access | Full assessment, on-site/evidence, annual review, exit plan required |
| **Tier 2 — Important** | Moderate disruption; limited data or access | Questionnaire + evidence, biennial review |
| **Tier 3 — Low** | Little impact; no sensitive data or access | Lightweight check, register only |

Tiering is the whole game. It is what makes the programme affordable enough to survive.

## Step 2: Assess before you sign

Due diligence happens **pre-contract**, while you still have leverage.

- **Security & privacy**: certifications (ISO 27001, SOC 2), pen-test summaries, incident history.
- **Resilience**: their availability record, DR/BCP, dependency on *their* vendors.
- **Concentration**: are you adding a fourth dependency on the same platform or region?
- **Financial & legal**: solvency, jurisdiction, sub-processor list.

Prefer **evidence over questionnaires** where it exists — a current SOC 2 report tells you more than a self-assessment. (This is [evidence reuse](/posts/audit-readiness-evidence/) applied to vendors.)

## Step 3: Put it in the contract

Risk that is not in the contract is a hope. Key clauses:

- **Security & privacy obligations** matched to your tier.
- **Breach notification** with a firm timeline (e.g. 24–72 hours).
- **Right to audit** or agreed third-party assurance.
- **Sub-processor** disclosure and change control.
- **Data return and deletion** on exit, in usable formats.
- **Availability SLAs** with remedies, and a **liability cap** you have reviewed.

## Step 4: Monitor continuously

Onboarding is a moment; risk is continuous.

- **Track posture drift** — certifications expiring, incidents, breaches, ownership changes.
- **Watch concentration** across the portfolio, not per vendor.
- **Review on a cadence** by tier (annual for Tier 1) and on triggers (an incident, an acquisition, a scope change).
- **Keep an owner per critical vendor** — one human accountable for the relationship and its risk.

## Step 5: Plan the exit before you need it

Exit risk is the most neglected and most painful. For every Tier 1 vendor, document:

- What leaving looks like and roughly how long it takes.
- Data **export** formats and whether you have ever tested one.
- The **alternate provider** or in-house fallback.

A vendor with no exit plan is a risk you cannot treat.

## The questionnaire that gets answered

Most third-party questionnaires are too long to complete honestly. Better:

- **Keep it tiered** — Tier 3 gets 10 questions, not 200.
- **Use certifications as shortcuts** — a valid ISO 27001 or SOC 2 scope covers many questions.
- **Ask about the specific risk**, not everything: "what happens to our data if you are acquired?" beats another 40 rows of generic controls.
- **Close the loop** — tell vendors what you found and what matters. Silence produces stale answers.

## Common mistakes

- **Assessing everyone equally.** Unsustainable, so it stops.
- **One-time diligence.** A clean SOC 2 two years ago says little about today.
- **Ignoring fourth parties.** Your vendor's sub-processors inherit into your risk.
- **No concentration view.** Individually approved vendors can collectively be one big bet.
- **"Vendor risk" owned by procurement alone.** Security, resilience, and legal each hold part of the picture.

## Key takeaways

- Third-party risk is **inherited risk you must manage deliberately**: **tier → assess → contract → monitor → exit**.
- **Tier by criticality** so effort goes where impact is — that is what makes it sustainable.
- Prefer **evidence (certifications, reports) over long questionnaires**, and tier the questions.
- Contract the risks: **notification, audit, sub-processors, SLAs, and exit**.
- Always know your **concentration** and your **exit path** for critical vendors.

Next: [cloud shared responsibility and what it means for your risk](/posts/cloud-shared-responsibility/).
