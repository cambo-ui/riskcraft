---
title: "ISO 27005 in Practice: A Worked Example"
date: 2026-10-17
description: "ISO 27005 is the risk engine inside an ISO 27001 ISMS. Here's the process, the vocabulary, and a full worked example from context to treatment — so you can actually run it."
categories: ["Frameworks & Standards"]
tags: ["iso 27005", "iso 27001", "isms", "risk assessment", "worked example"]
level: 3
weight: 5
---

**ISO 27005** is the information security risk management standard in the ISO 27000 family. It does not sit alone — it is the risk engine that drives **ISO 27001**, the certifiable management standard. If you are building or maintaining an ISMS, 27005 is the process you actually run.

This is the standard explained as a procedure, with a worked example.

## Where it fits

| Standard | Role |
| --- | --- |
| **ISO 27001** | The management system: policies, roles, improvement cycle, certification |
| **ISO 27002** | A catalogue of controls (guidance) |
| **ISO 27005** | The **risk management process** that feeds 27001 |

27001 tells you to manage risk; 27005 tells you how.

## The process, step by step

1. **Establish context** — scope, assets, objectives, criteria.
2. **Risk identification** — assets, threats, vulnerabilities, existing controls, consequences.
3. **Risk analysis** — assess likelihood and impact; determine risk level.
4. **Risk evaluation** — compare against criteria; is it acceptable?
5. **Risk treatment** — avoid, modify, share, or retain.
6. **Acceptance** — risk owners formally accept residual risk.
7. **Communication and consultation** — throughout, not at the end.
8. **Monitoring and review** — ongoing.

Note the treatment vocabulary: ISO says **modify** where practitioners say *mitigate*, and **retain** where we say *accept*. Same idea, different words.

## A worked example

**Context.** A mid-sized company runs a **Customer Records System (CRS)** holding personal data and payment references. Scope: the CRS and its supporting infrastructure. Criteria: risks exceeding "Moderate" must be treated.

### Step 1–2: Identify

Start from the *information asset*, per 27005's asset-centric view.

| ID | Asset | Threat | Vulnerability | Consequence |
| --- | --- | --- | --- | --- |
| R1 | Customer PII | External attacker | No MFA on admin accounts | Breach, fines, trust loss |
| R2 | CRS application | Insider error | No change control on prod DB | Data corruption, outage |
| R3 | CRS availability | Ransomware | Backups untested | Extended outage |

Notice every row has **asset + threat + vulnerability + consequence** — 27005's canonical shape. Weak rows are missing one of these.

### Step 3: Analyse

Score likelihood and impact against defined criteria (see [scoring matrices](/posts/designing-a-risk-scoring-matrix/)).

| ID | Likelihood | Impact | Risk level |
| --- | --- | --- | --- |
| R1 | 4 | 5 | **Critical** |
| R2 | 3 | 3 | Medium |
| R3 | 4 | 5 | **Critical** |

Analyse both **inherent** and **residual** — the gap is your control environment.

### Step 4: Evaluate

Compare to criteria. R1 and R3 exceed "Moderate" → must be treated. R2 is borderline → treat if cheap, otherwise retain with justification.

### Step 5: Treat

ISO's four options, applied:

| ID | Treatment | Action |
| --- | --- | --- |
| R1 | **Modify** | Enforce MFA + privileged access review |
| R2 | **Modify** | Introduce change control on prod DB |
| R3 | **Modify + Share** | Tested backups + cyber-insurance for residual |
| — | **Avoid** | Decommission an unused legacy export feed (removes its risk) |
| — | **Retain** | Accept residual after MFA + backup testing |

### Step 6: Accept and link to 27001

Risk owners sign off the residual level. Then the treatments become **controls selected in the Statement of Applicability (SoA)** — the document 27001 auditors examine. This is the crucial join: **27005 output → 27001 controls → SoA → audit evidence.**

## Common pitfalls

- **Skipping context.** No scope or criteria means every risk is scored against vibes.
- **Asset-less risks.** 27005 is asset-centric; risks without an identifiable asset are hard to treat.
- **Treating 27005 as a one-off.** It is a cycle; re-run it, don't laminate it.
- **Ignoring the SoA link.** Risk work that never reaches the SoA is invisible to certification and audit.
- **Copying criteria from another company.** Criteria reflect *your* context and appetite.

## Key takeaways

- **ISO 27005 is the risk process inside ISO 27001**; 27002 supplies the controls.
- Its shape is **asset + threat + vulnerability + consequence**, scored to a risk level.
- Treatment is **avoid / modify / share / retain** — same four options, ISO's words.
- The output must reach the **Statement of Applicability**, or it does not count.
- Run it as a **cycle**, against criteria tied to your own context.

Next: [NIST RMF vs. ISO 27005 — which one, and when](/posts/nist-rmf-vs-iso-27005/).
