---
title: "Control Types: Preventive, Detective, Corrective, Deterrent"
date: 2026-10-17
description: "Most control environments are a wall of preventive measures and almost no detection. Learn the four types, how they map to the timeline of an event, and why you need all of them."
categories: ["Treatment & Controls"]
tags: ["controls", "preventive", "detective", "corrective", "deterrent"]
level: 2
weight: 6
---

When you decide to **mitigate** a risk, you are choosing controls. But "controls" is not one thing. Classifying them reveals gaps fast — and the most common gap is an organisation that has built a fortress and installed no alarms.

## The four types, on a timeline

Controls act at different points relative to an event:

```
        before                     during                 after
   ┌──────────────┐          ┌──────────────┐       ┌──────────────┐
   │  Preventive  │          │  Detective   │       │  Corrective  │
   │  stop it     │          │  notice it   │       │  recover     │
   └──────────────┘          └──────────────┘       └──────────────┘
        ▲
   ┌──────────────┐
   │  Deterrent   │  discourage the attempt
   └──────────────┘
```

| Type | Goal | Fails silently when |
| --- | --- | --- |
| **Preventive** | Stop the event happening | It is bypassed and nobody knows |
| **Detective** | Notice the event (or attempt) | Nobody acts on the alert |
| **Corrective** | Recover after the event | Untested; does not work when needed |
| **Deterrent** | Discourage the attempt | Perceived risk is low |

## Preventive controls

Stop something before it happens. This is where most security budgets go — for good reason.

- MFA, network segmentation, least privilege.
- Patching, hardening, input validation.
- Change control, segregation of duties.

**Strength:** if it works, nothing happens. **Weakness:** preventive controls fail *silently*. When MFA is bypassed via a legacy protocol, the control has not "worked"; it has an invisible hole. This is why prevention alone is not a strategy.

## Detective controls

Discover that an event is happening or has happened. Detection cannot undo an event, but it limits how long it goes unnoticed — and duration drives cost.

- Logging, monitoring, and alerting.
- Anomaly detection, integrity checks.
- Access reviews, reconciliation, audits.

**Strength:** detects the bypasses prevention missed. **Weakness:** a detective control that nobody responds to is theatre. Detection without a response process just produces ignored alerts — and alert fatigue is its own risk.

## Corrective controls

Restore normal operation after an event. Corrective controls determine how bad an incident actually gets.

- Backups and tested restores.
- Incident response, failover, disaster recovery.
- Patches, rebuilds, config rollback.

**Strength:** limits impact when prevention fails (it will). **Weakness:** corrective controls are worthless if untested. An untested backup is a belief, not a control. Test restores on a cadence and record the result.

## Deterrent controls

Discourage an attempt in the first place by raising perceived risk to the attacker.

- Warning banners, visible cameras, clear policies.
- Threat of legal action, monitoring disclosures.

**Strength:** cheap, shapes behaviour. **Weakness:** effectiveness depends on the adversary's perception, so it is hard to measure and trivially defeated against a motivated attacker. Treat deterrence as a bonus, never as your primary control.

## The pairing that matters most

Prevention and detection are complementary, and the highest-value pairing is **detective + corrective**:

> You cannot prevent every event. What you *can* do is **detect it quickly and recover quickly**, which shrinks the loss.

A useful design question for every material risk:

1. What stops it? (preventive)
2. How would we know? (detective)
3. How do we recover? (corrective)

If any answer is "nothing", you have a gap to document — and probably to fund.

## A second axis: how controls are delivered

The four types describe *when* a control acts. A second axis describes *how*:

| Category | Examples |
| --- | --- |
| **Administrative** | Policies, procedures, training, reviews |
| **Technical** | Firewalls, MFA, encryption, monitoring |
| **Physical** | Locks, guards, CCTV, access cards |

A mature control set uses all three. Engineers default to technical, but most real-world failures involve an **administrative** gap — a process nobody followed.

## Common mistakes

- **All prevention, no detection.** A wall with no alarm.
- **Detection with no response.** Alerts nobody owns or acts on.
- **Untested corrective controls.** Backups that have never been restored.
- **Confusing complementary with compensating.** *Complementary* controls work alongside a primary control; *compensating* controls replace one that cannot be applied. Different risk profiles — document which you mean.
- **Assuming a control works because it exists.** Score effectiveness with evidence, not presence.

## Key takeaways

- Four types: **preventive** (stop), **detective** (notice), **corrective** (recover), **deterrent** (discourage).
- The strongest pairing is **detect fast + recover fast** — since prevention will sometimes fail.
- Every material risk needs an answer to **stop, know, recover**.
- Controls are also **administrative, technical, or physical** — and administrative gaps cause many failures.
- Judge controls by **evidence of effectiveness**, not by their presence.

Next: [avoid, mitigate, transfer, accept — choosing a treatment](/posts/choosing-a-risk-treatment/).
