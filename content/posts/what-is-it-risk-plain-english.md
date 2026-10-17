---
title: "What Is IT Risk? A Plain-English Primer"
date: 2026-10-01
description: "Risk, threat, vulnerability, likelihood, impact — the vocabulary everyone nods along to and almost nobody defines the same way. Here it is, in plain English."
categories: ["Foundations"]
tags: ["risk basics", "definitions", "inherent risk", "residual risk"]
level: 0
weight: 1
---

Ask five people in a meeting what "risk" means and you will get five answers. That is the single biggest reason risk conversations go nowhere. So let us fix the vocabulary first.

## Risk is about objectives, not events

The most useful definition, and the one behind ISO 31000, is:

> **Risk is the effect of uncertainty on objectives.**

Read that again, because the important word is **objectives**. A risk is not "we might get hacked". A risk is "*this could stop us achieving something we care about*". No objective, no risk — just an interesting fact.

That reframing changes the conversation. Instead of arguing about whether a threat is scary, you ask: *which goal does this put at risk, and how badly?*

## The building blocks

| Term | What it really means |
| --- | --- |
| **Asset** | Anything of value: data, systems, people, reputation. |
| **Threat** | Something that could cause harm — a ransomware gang, an insider, a flood, a resigning admin. |
| **Vulnerability** | A weakness the threat can use — an unpatched server, missing MFA, a process nobody owns. |
| **Likelihood** | How probable the event is, given current conditions. |
| **Impact** | How bad it is for the business when it happens. |
| **Risk** | The combination: *what could happen, how likely, how bad, to which objective.* |

A clean way to hold it together: **Risk = Threat × Vulnerability × Impact**, all moderated by what controls you already have.

## Inherent vs. residual risk

Two terms that trip up almost everyone:

- **Inherent risk** — the risk *before* you apply controls. This is your starting exposure.
- **Residual risk** — the risk *left over after* controls. **This is the only one you can meaningfully accept, treat, or report.**

If someone says "we have a critical risk but we fixed it", the honest question is: *what is the residual risk now, and who accepted it?*

## Why IT risk is a business language

Security people like to talk about CVEs, misconfigurations, and control gaps. The business talks about revenue, downtime, fines, and trust. IT risk is the translation layer between the two.

You are not the person who lists every possible thing that could go wrong. You are the person who helps the organisation **make a deliberate decision** about which risks to take, which to reduce, and which to refuse.

That is the whole game. Everything else — frameworks, registers, KRIs — are tools in service of that decision.

## Key takeaways

- **Risk is the effect of uncertainty on objectives.** No objective, no risk.
- Threat, vulnerability, likelihood, and impact are inputs. Risk is the synthesis.
- **Residual risk is what you manage.** Inherent risk tells you how much work there is to do.
- IT risk is a **business conversation with technical inputs**, not a technical conversation with business consequences.

Next: [how to capture all this in a risk register people actually use](/posts/building-a-risk-register-people-use/).
