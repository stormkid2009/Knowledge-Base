---
title: adopting single instance control
date: 2026-04-02
status: draft
tags:
  - decision
  - gap
repo: https://github.com/stormkid2009/restooo
---

# 🗂️ Adopting Single Instance Control

> One sentence — what was the choice you had to make?
The choice between exporting new instance of class service or plain object containing service methods
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
AI generated the code with class new instance exporting so I searched about it and took the decision to use it
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option             | Pros            | Cons              |
| ------------------ | --------------- | ----------------- |
| Plain object       | light weight    | can't be extended |
| Class new instance | can be extended | more boilerplate  |

## What I Chose
<!-- State the decision clearly -->
Class new instance
## Why
<!-- The honest reasoning. What tipped the balance? -->
maybe my admire to object oriented programming benefits encourage me to stick to this pattern and most developers already adopted this pattern
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
- what problems are hidden behind the advantages of this pattern
- how far can I figure out more about this pattern through review the code and testing
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What                            | Link                                                                                                                                   |
| ------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| [[experience/customer-service]] | https://github.com/stormkid2009/restooo/blob/f95a0772394a6dde422a7e2828c015773acd34e2/src/modules/customer/customer.service.ts#L1-L326 |

---

## Connections

- **Made during experience:** [[experience/customer-service]]
- **Based on concept:** [[concept/single-instance-control]]
<!-- Was this decision made from a known concept or a fuzzy one? -->
- **Concept confidence at time of decision:** fuzzy
- **Related pattern:** [[pattern/modular-monolith]]
- **Related architecture:** [[architecture/monolith]]

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
