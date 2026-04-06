---
title: adopting layer based architecture
date: 2026-03-13
status: draft
tags:
  - decision
  - gap
repo: https://github.com/stormkid2009/api-template
---

# 🗂️ Adopting Layer Based Architecture

> One sentence — what was the choice you had to make?
 The question which structure should I use flat or layers?
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
Honestly I didn't know what is best choice to structure my app as beginner maybe u will go to flat structure
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option         | Pros                                    | Cons                                |
| -------------- | --------------------------------------- | ----------------------------------- |
| layer based    | good for large scale projects           | performance will be affected        |
| flat structure | good for tiny projects or simple script | if scaled it will be spaghetti code |

## What I Chose
<!-- State the decision clearly -->
I chose layer based routes - controllers - services - database
## Why
<!-- The honest reasoning. What tipped the balance? -->
I planned to make this api reusable in other projects so separation of concerns is a must here
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
- How exactly those layers interconnecting ? 
- What is behind the scene and can affect API performance?
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What                        | Link                                                          |
| --------------------------- | ------------------------------------------------------------- |
| [[experience/api-template]] | https://github.com/stormkid2009/api-template/tree/main/src/v1 |

---

## Connections

- **Made during experience:** [[experience/api-template]]
- **Based on concept:** [[concept/separation-of-concerns]]
<!-- Was this decision made from a known concept or a fuzzy one? -->
- **Concept confidence at time of decision:** fuzzy
- **Related pattern:** [[pattern/module-singleton]]
- **Related architecture:** [[architecture/layer-based]]

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
