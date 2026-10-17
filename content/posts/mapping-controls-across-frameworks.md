---
title: "Mapping Controls Across Frameworks: One Control, Many Standards"
date: 2026-10-17
description: "ISO 27001, NIST 800-53, SOC 2, PCI DSS all describe the same capabilities with different labels. A crosswalk lets one control set satisfy them all — without four parallel programmes."
categories: ["Compliance & Audit", "Frameworks & Standards"]
tags: ["crosswalk", "control mapping", "iso 27001", "nist 800-53", "soc 2", "pci dss"]
level: 3
weight: 8
---

By now you have met ISO 27001, NIST 800-53, SOC 2, and probably PCI DSS. Each has its own numbering, its own vocabulary, and its own auditor. The instinct is to run a programme per framework — which is how organisations end up with four control sets, four evidence hunts, and one exhausted team.

There is a better way: recognise that **frameworks are different views of the same underlying capabilities**, and build a **crosswalk**.

## Controls are capabilities; frameworks are labels

Access control is access control. What varies is the name:

| Capability | ISO 27001:2022 | NIST 800-53 | SOC 2 (TSC) | PCI DSS 4.0 |
| --- | --- | --- | --- | --- |
| Access control policy | A.5.15 | AC-3 | CC6.1 | Req 7 |
| Identity & authentication | A.5.16, A.8.5 | IA-2, IA-5 | CC6.1 | Req 8 |
| Access rights management | A.5.18 | AC-2 | CC6.2, CC6.3 | Req 7 |
| Privileged access | A.8.2 | AC-6 | CC6.1 | Req 7 |
| Malware protection | A.8.7 | SI-3 | CC6.8 | Req 5 |
| Backups | A.8.13 | CP-9 | A1.2 | Req 9 |
| Logging | A.8.15 | AU-2, AU-6 | CC7.2 | Req 10 |

Read that table once and the whole "framework fatigue" problem shrinks: you are implementing capability **once**, then labelling it four ways.

## Build the crosswalk

A crosswalk is a table mapping your **internal controls** to each framework's references.

### 1. Pick an anchor

Choose one framework as your **primary spine** — usually ISO 27001 (if you certify) or NIST 800-53 (if you are US-oriented or want the most granular catalogue). Everything else maps *to* the anchor. This keeps your control library from becoming a democratic mess.

### 2. Map in one direction first

Start with anchor → other frameworks, not the reverse. Mapping each new framework back to the anchor is additive and keeps the anchor authoritative.

### 3. Define your own internal control IDs

This is the key move. Do **not** use a framework's numbering as your primary key — numbering changes (ISO 27001:2022 renumbered the entire Annex A from 114 controls in 2013 to 93 in four themes). Give each capability a stable **internal ID** (e.g. `IAM-01 Access Control`) and map frameworks onto it. When a framework renumbers, you update the mapping, not your whole programme.

### 4. Verify, do not assume

Similar-looking controls are not always equivalent. Check scope and rigour:

- ISO A.8.13 (backup) and PCI Req 9 (backup) overlap, but PCI adds specific retention and testing expectations.
- SOC 2 describes **criteria**; you define the controls that meet them — there is no fixed control list to copy.

A green crosswalk cell means "relevant and likely sufficient", not "automatically compliant". Flag partial coverage explicitly.

## Structure the crosswalk

| Internal ID | Capability | ISO 27001:2022 | NIST 800-53 | SOC 2 | PCI 4.0 | Coverage |
| --- | --- | --- | --- | --- | --- | --- |
| IAM-01 | Access control | A.5.15 | AC-3 | CC6.1 | Req 7 | Full |
| IAM-02 | Privileged access | A.8.2 | AC-6 | CC6.1 | Req 7 | Full |
| IAM-03 | MFA | A.8.5 | IA-2 | CC6.1 | Req 8 | Partial (PCI scope) |
| BAK-01 | Backup & restore testing | A.8.13 | CP-9 | A1.2 | Req 9 | Full |
| LOG-01 | Centralised logging | A.8.15 | AU-6 | CC7.2 | Req 10 | Partial |

The **Coverage** column is the honest part — and the one auditors and managers actually need. It drives where extra work is required for a specific framework.

## The payoffs

- **Implement once, evidence once.** One control, one evidence artefact, many references — the direct link to [reusable audit evidence](/posts/audit-readiness-evidence/).
- **Map audits, not programmes.** When a new standard arrives, you add a column, not a project.
- **See real gaps.** "Full" vs "Partial" coverage shows where frameworks genuinely diverge.
- **Stable through version changes.** Internal IDs survive framework renumbering.
- **Clear reporting.** Leadership sees one control environment, not four.

## Common mistakes

- **Treating a map as compliance.** A crosswalk is a claim of relevance; only evidence and testing prove compliance.
- **Assuming one control always suffices.** Scope differs (e.g. PCI applies to the cardholder data environment, not the whole estate).
- **Mapping in both directions ad hoc.** Pick an anchor and map consistently toward it.
- **Using framework numbers as keys.** They change; your IDs should not.
- **Mapping once and forgetting.** Frameworks update (ISO 27001:2022, NIST 800-53 Rev 5, PCI DSS 4.0, CSF 2.0). Schedule a review.

## Key takeaways

- **Controls are capabilities; frameworks are labels.** Implement once, map many.
- Build a **crosswalk** with stable **internal control IDs** and framework references.
- Pick an **anchor framework** and map in one direction.
- Mark **coverage honestly** — full vs partial — because that is where the work is.
- A crosswalk is a **relevance claim, not proof**; evidence and testing still decide compliance.

---

That completes **Level 3 — Specialist**. Next on the path is **Level 4 — Enterprise**: governance and GRC at scale, starting with appetite statements the board will actually approve. See the [learning path](/learning-path/).
