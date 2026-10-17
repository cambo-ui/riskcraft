---
title: "NIST RMF vs. ISO 27005: Which One, and When"
date: 2026-10-17
description: "Both manage security risk, but they optimise for different things. A side-by-side comparison, the decision criteria, and how to combine them without running two programmes."
categories: ["Frameworks & Standards"]
tags: ["nist rmf", "iso 27005", "nist 800-53", "framework", "comparison"]
level: 3
weight: 6
---

You have [the big picture of frameworks](/posts/it-risk-frameworks-explained/), and you have run [ISO 27005 in practice](/posts/iso-27005-in-practice/). Now the question that actually lands on your desk: **NIST RMF or ISO 27005?**

The honest answer is that they are not competitors so much as different centres of gravity. One is a **control-heavy lifecycle**; the other is a **risk process inside a management system**.

## Side by side

| | **NIST RMF** (SP 800-37) | **ISO 27005** |
| --- | --- | --- |
| Origin | US NIST (federal) | ISO/IEC international |
| Centre of gravity | System lifecycle + control catalogue | Risk process inside an ISMS |
| Companion catalogue | SP 800-53 controls | ISO 27002 controls |
| Output | Authorization to operate (ATO) | Risk treatment feeding the SoA |
| Stewardship model | Assess → Authorize → Monitor | Plan → Do → Check → Act (via 27001) |
| Certification | FedRAMP / agency ATO | ISO 27001 certification |

## The seven NIST RMF steps

NIST SP 800-37 Rev 2:

```
1. Prepare      scope, roles, priorities
2. Categorize   impact of the system (low/moderate/high, FIPS 199)
3. Select       controls from SP 800-53
4. Implement    put controls in place
5. Assess       test whether they work
6. Authorize    an official accepts the residual risk (ATO)
7. Monitor      continuous monitoring
```

The emphasis is on **systems, controls, and authorization**. It answers: *has this system been assessed, and will an accountable official accept the risk?*

## The ISO 27005 process

```
Context → Identify → Analyse → Evaluate → Treat → Accept → Monitor
                 (with communication throughout)
```

The emphasis is on **risk as a living process** inside a management system that improves over time. It answers: *are risks known, treated, and owned, and is the system improving?*

## How to choose

| If this is true… | Lean toward |
| --- | --- |
| You sell to US federal agencies / need FedRAMP | **NIST RMF** |
| You are or want to be **ISO 27001 certified** | **ISO 27005** |
| You need a control **catalogue** to select from | **NIST 800-53** |
| You need a **management system** and culture of improvement | **ISO 27001/27005** |
| You want board-level maturity mapping | NIST CSF 2.0 (either, as an overlay) |
| Your regulator names a framework explicitly | Whichever is named |

Most organisations outside US federal work **choose ISO** for certification and management, and borrow NIST's control catalogue where it is more granular.

## Do not run two programmes

The failure mode is running both in parallel: two registers, two control sets, two audits. The fix is to separate **process** from **catalogue**:

- Use **one risk process** — either RMF's lifecycle or ISO 27005's cycle — as your spine.
- Use **one control library**, then **map** it to both 800-53 and ISO 27002 labels.

Because controls are capabilities, not framework-specific objects, a single library can satisfy both. Access control is access control; NIST calls it AC-2/AC-3/AC-6, ISO calls it A.5.15–A.8.3. That mapping is the subject of the last post in this level.

## The pragmatic stack

A workable combination for most non-federal organisations:

1. **ISO 27001** for the management system and certification.
2. **ISO 27005** for the risk process (the cycle).
3. **NIST SP 800-53** as a richer control reference where ISO 27002 is too high-level.
4. **NIST CSF 2.0** to overlay a maturity profile for leadership.
5. **One crosswalk** linking your control library to all of the above.

## Common mistakes

- **Treating the framework as the goal.** Certification is not security; the risk decisions are.
- **Adopting NIST purely for prestige** without a federal driver, then drowning in control volume.
- **Ignoring the authorization step.** In RMF, residual risk acceptance is an explicit, named decision — a habit worth copying even in ISO shops.
- **Letting catalogues diverge.** Two control sets with no crosswalk means duplicated effort and audit chaos.

## Key takeaways

- **NIST RMF is a control-heavy system lifecycle ending in authorization; ISO 27005 is a risk process inside an ISMS.**
- Choose by **driver** (federal/FedRAMP → NIST; certification → ISO), not by preference.
- Keep **one risk process and one control library**, then map labels — never run two programmes.
- RMF's explicit **authorization** and ISO's **monitoring cycle** are both worth borrowing regardless.
- A single **crosswalk** is what lets one control set satisfy many standards.

Next: [audit readiness — evidence you can reuse](/posts/audit-readiness-evidence/).
