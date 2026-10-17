---
title: "IT Risk Frameworks Explained: ISO 27005, NIST RMF, COBIT, COSO and FAIR"
date: 2026-10-08
description: "The alphabet soup of risk frameworks, decoded. What each one is actually for, how they fit together, and how to avoid drowning in compliance theatre."
categories: ["Frameworks & Standards"]
tags: ["ISO 27005", "NIST RMF", "COBIT", "COSO", "FAIR", "framework"]
level: 3
weight: 4
---

Sooner or later someone asks: *"Which framework do we follow?"* And someone else produces a 200-page standard that nobody reads. Let's cut through it.

The frameworks are not competitors. They operate at **different layers**, and a mature organisation usually uses several at once. Get the layering right and the alphabet soup becomes a stack.

## The four layers

```
Enterprise risk      →  COSO ERM, ISO 31000
IT governance        →  COBIT
Security risk mgmt   →  ISO 27005, NIST RMF, NIST CSF
Risk quantification  →  FAIR
```

You rarely *choose one*; you choose which layer you are solving for right now.

## ISO 31000 — the vocabulary layer

**What it is:** International principles and guidelines for any kind of risk management. Deliberately not IT-specific.

**Use it when:** You need a shared language and a defensible process across the whole organisation — and you want to avoid reinventing risk definitions per department.

**Do not expect:** Controls, or anything to implement. ISO 31000 tells you *how to think*, not *what to install*.

## ISO 27005 — infosec risk management

**What it is:** Information security risk management guidance, sitting under the ISO 27000 family and feeding ISO 27001.

**Use it when:** You run an ISMS and need to connect identified risks to your Statement of Applicability. It is the natural choice for security teams already living in ISO land.

**Key idea:** Risk is assessed in terms of the *information assets* and their confidentiality, integrity, and availability.

## NIST RMF — a repeatable lifecycle

**What it is:** NIST SP 800-37, the Risk Management Framework — six steps: **Prepare, Categorize, Select, Implement, Assess, Authorize, Monitor**.

**Use it when:** You want a rigorous, auditable lifecycle for systems, especially if you sell to or operate in US federal contexts.

**Strength:** It is prescriptive enough to actually run. **Weakness:** Heavier than many organisations need.

## NIST CSF — the maturity picture

**What it is:** The Cybersecurity Framework — five functions: **Identify, Protect, Detect, Respond, Recover** (with Govern added in CSF 2.0).

**Use it when:** You need a board-level view of cyber maturity and a common map across your controls. It is a *profile and gap* tool, not a deep risk methodology.

## COBIT — IT governance

**What it is:** A governance and management framework for enterprise IT, with detailed processes and practices.

**Use it when:** You must connect IT risk to enterprise governance, define who decides what, and audit IT processes. COBIT answers *"who governs IT, and how?"*

## COSO ERM — board-level, strategy-aligned

**What it is:** Enterprise Risk Management, framed around strategy and performance.

**Use it when:** You are building the executive/board risk programme and need risk to be seen as strategy, not compliance.

## FAIR — making it quantitative

**What it is:** A model for analysing and *measuring* risk in financial terms (frequency × loss magnitude).

**Use it when:** Qualitative "High" is not enough and you need to justify or refuse a spend. FAIR is a method, not a governance framework — it slots under any of the above.

## How they fit together in practice

A workable stack for a mid-to-large organisation:

1. **ISO 31000 / COSO** for the language and enterprise reporting standard.
2. **COBIT** to define IT governance and ownership.
3. **ISO 27005** (or **NIST RMF**) to run security risk assessments against systems.
4. **NIST CSF** to profile cyber maturity for leadership.
5. **FAIR** to quantify the handful of risks where money decides.

## Avoiding compliance theatre

The failure mode is treating a framework as the goal. You pass the audit and nothing gets safer.

- **Map, don't duplicate.** One control can satisfy many frameworks. Maintain a crosswalk, not five parallel programmes.
- **Start from decisions, not standards.** Ask what decision the framework is helping you make.
- **Reuse evidence.** Collect once, satisfy many.
- **Adapt.** Frameworks are menus, not checklists. Take what fits your risk, maturity, and regulation.

## Key takeaways

- Frameworks live in **layers** — enterprise, governance, security risk, quantification.
- **ISO 31000** gives language, **ISO 27005** secures information, **NIST RMF/CSF** give lifecycle and maturity, **COBIT** governs IT, **COSO** aligns to strategy, **FAIR** quantifies.
- The goal is **decisions**, not certification.
- **Map and reuse** to avoid running the same programme five times.

Next: [how the Three Lines Model turns all this into an operating model](/posts/three-lines-of-defense-explained/).
