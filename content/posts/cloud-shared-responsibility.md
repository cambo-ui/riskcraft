---
title: "Cloud Shared Responsibility and What It Means for Your Risk"
date: 2026-10-17
description: "\"The cloud provider handles security\" is the most expensive misunderstanding in modern IT. What you actually own depends on the service model — and most cloud incidents land on your side of the line."
categories: ["Cloud & Cyber Risk"]
tags: ["cloud", "shared responsibility", "iaas", "paas", "saas", "misconfiguration"]
level: 4
weight: 8
---

"The provider is certified, so we're secure." If you have heard that sentence in a design meeting, you have found a risk that is not in the register yet. The **shared responsibility model** is the single most important mental model for assessing cloud risk — and it is routinely misread.

## The model

Cloud providers secure **the cloud**; you secure **what you put in it**. Where exactly the line falls depends on the **service model**:

| Layer | IaaS | PaaS | SaaS |
| --- | --- | --- | --- |
| Data & access | **You** | **You** | **You** |
| Identity & configuration | **You** | **You** | **You** / shared |
| Applications | **You** | Shared | Provider |
| Runtime / middleware | **You** | Provider | Provider |
| OS / virtualisation | **You** | Provider | Provider |
| Network / hosts / facilities | Provider | Provider | Provider |

The pattern: as you move from IaaS to SaaS, the provider takes on more — **but the top of the stack is always yours.**

## What you always own

Regardless of service model, these are on your side of the line:

- **Data** — classification, encryption, retention, and who may access it.
- **Identity and access** — your users, roles, keys, and MFA.
- **Configuration** — the settings that determine exposure.
- **The use of the service** — what you build and how you connect it.

Most cloud security failures are here. Not in the provider's infrastructure — **in the customer's configuration and identity**.

## The failure modes that actually happen

- **Public storage buckets / over-broad sharing.** Data exposed by a single misconfigured permission.
- **Leaked or over-privileged credentials.** Long-lived keys, no MFA, wildcard permissions.
- **Open management interfaces.** Databases or admin consoles reachable from the internet.
- **Logging disabled.** No detection, so a compromise runs for months.
- **Assumed encryption.** "It's encrypted" without knowing who holds the keys or whether it is on by default.

Every one of these is a **customer-side** responsibility. Providers build secure platforms; they cannot stop you from making them insecure.

## What this means for risk assessment

The shared responsibility model changes three things in your assessment:

### 1. The control boundary moves

Your "estate" now includes **your configuration and identity plane**, not just servers you run. If a control (e.g. encryption at rest) sits on the provider's side, you are relying on **their** assurance — which brings us to evidence.

### 2. Evidence shifts to provider assurance

You cannot test the provider's datacentre. You rely on:

- **Certifications and reports** — ISO 27001, SOC 2, and (for regulated sectors) regional schemes.
- **Scope statements** — a SOC 2 covers specific services and controls. Read the scope; it may not cover the service you actually use.
- **Your own configuration evidence** — config exports, coverage reports, posture tooling.

This is [vendor risk](/posts/third-party-supply-chain-risk/) applied to your cloud provider, and it feeds the same [evidence library](/posts/audit-readiness-evidence/).

### 3. Misconfiguration becomes a first-class risk

For cloud estates, the dominant risk is not "the provider is breached" — it is **"we misconfigured it"**. Score it accordingly: high likelihood, controllable, and therefore worth investing in preventive *and* detective controls (posture scanning, guardrails, drift detection).

## A responsibility matrix you can build

For each cloud service you use, write the line down explicitly:

| Component | Provider | Us |
| --- | --- | --- |
| Physical & network | ✅ | |
| Hypervisor / host OS (IaaS) | ✅ | |
| Guest OS & patching | | ✅ |
| Application & data | | ✅ |
| Identity & access | | ✅ |
| Encryption keys | shared | ✅ (customer-managed) |
| Backups | service | ✅ (test restores) |
| Logging & monitoring | service | ✅ (enable & alert) |
| Provider assurance | ✅ (SOC 2 / ISO) | ✅ (review scope) |

For a SaaS service the middle rows move to the provider — but data, identity, backups, and log consumption never do.

## Cloud exit and concentration

Two more risks the model exposes, both easy to miss:

- **Concentration.** Everything on one provider or region is a correlated failure. Document it and, for critical systems, plan for it.
- **Exit.** Can you export your data in a usable format, and have you tested it? Provider lock-in is [third-party exit risk](/posts/third-party-supply-chain-risk/) at platform scale.

## Common mistakes

- **Assuming the certificate covers you.** It covers the provider's side, for a defined scope.
- **Treating configuration as an implementation detail.** In cloud, configuration *is* the security control.
- **No posture monitoring.** Drift accumulates silently; detection is your safety net.
- **Forgetting data residency and keys.** Who holds the encryption keys matters, and where the data sits may be a regulatory requirement.
- **One region, no exit plan.** Concentration and lock-in are risks, not implementation trivia.

## Key takeaways

- **The provider secures the cloud; you secure what you put in it** — data, identity, and configuration are always yours.
- The boundary **moves with the service model** (IaaS → PaaS → SaaS); write it down per service.
- Most cloud incidents are **customer-side misconfiguration**, so treat it as a first-class risk.
- You rely on **provider certifications/reports** for their side — check the **scope**.
- Manage **concentration** and **exit** as real cloud risks.

Next: [putting risk into change, project, and vendor processes](/posts/embedding-risk-in-processes/).
