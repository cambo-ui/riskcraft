---
title: "The CIA Triad and Why It Anchors Everything"
date: 2026-10-14
description: "Confidentiality, integrity, availability — three words that turn vague 'security risk' into something you can assess, prioritise, and link to a business objective."
categories: ["Foundations"]
tags: ["cia triad", "confidentiality", "integrity", "availability", "risk basics"]
level: 0
weight: 4
---

Ask a team "what's the risk?" and you will usually get a vague answer: *"security"*, *"the database"*, *"cyber"*. The **CIA triad** is the tool that turns that fog into three assessable dimensions — and it is the single most useful piece of structure in IT risk.

## The three properties

| Property | It is about | It fails when |
| --- | --- | --- |
| **Confidentiality** | Only the right people see the data | Breach, leak, over-broad access |
| **Integrity** | Data is accurate and unaltered | Corruption, tampering, bad syncs |
| **Availability** | Systems work when needed | Outage, ransomware, lost capacity |

Every IT risk you will ever assess damages at least one of these. Many damage two or three at once — ransomware hits **availability** (encryption) and possibly **confidentiality** (exfiltration).

## Why it beats "security"

"Security risk" is not actionable. It hides *what actually breaks*. The triad forces the question: **which property, for which asset, supporting which objective?**

That matters because the three properties have different costs, different owners, and different controls:

- **Confidentiality** → access control, encryption, classification, DLP.
- **Integrity** → input validation, checksums, change control, reconciliation.
- **Availability** → redundancy, backups, DR testing, capacity management.

A team that says "we need to improve security" cannot be funded or measured. A team that says "customer PII confidentiality is at risk because access reviews haven't run in a year" can.

## Prioritising across the triad

The triad also lets you weigh trade-offs honestly. The classic tension:

> Stronger **confidentiality** and **integrity** controls (MFA, approvals, encryption) can reduce **availability** or speed.

Sometimes that trade is right; sometimes it is not. A hospital's life-support monitoring prioritises **availability** first. A payment system prioritises **integrity**. A legal archive prioritises **confidentiality**. The triad gives you the vocabulary to have the argument explicitly rather than by accident.

## Mapping to business objectives

The final move is connecting each property to an objective, so the risk is a business statement, not a technical one:

| Asset | Property | Business objective it supports |
| --- | --- | --- |
| Customer database | Confidentiality | Trust, regulatory compliance (e.g. GDPR) |
| Trading ledger | Integrity | Financial accuracy, audit |
| Order platform | Availability | Revenue, customer satisfaction |

Now a risk maps cleanly:

> *"Because the customer database access reviews are stale, there is a risk that confidentiality is breached, resulting in regulatory fines and loss of customer trust."*

Business outcome. Ownable. Reportable.

## Common mistakes

- **Assuming availability is 'IT's problem'.** Availability is usually the most business-visible property; downtime costs money and reputation. Don't treat it as second class.
- **Ignoring integrity.** Integrity failures are often silent and expensive — bad data can persist for months before anyone notices.
- **Treating 'security' and confidentiality as synonyms.** Security is the umbrella; confidentiality is one property among three.

## Key takeaways

- **Confidentiality, integrity, availability** are the three properties that IT risk damages.
- The triad turns vague "security risk" into **specific, assessable, ownable** statements.
- Each property implies **different controls, costs, and owners** — and real trade-offs between them.
- Always connect the property to a **business objective** so the risk is a business statement.

Next on the path: [the risk management lifecycle, step by step](/posts/risk-management-lifecycle/).
