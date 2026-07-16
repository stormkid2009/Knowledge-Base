---
title: feature based architecture versus layer based
date: 2026-03-05
status: growing
tags:
  - decision
  - gap
repo: https://github.com/stormkid2009/restooo
---

# 🗂️ Feature based vs Layer based

> One sentence — what was the choice you had to make?
Feature based architecture or layer architecture ?
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
Jumping between directories like controllers to services is so disturbing especially if u watch out the flow of certain feature like authentication
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option        | Pros                                                | Cons                                                           |
| ------------- | --------------------------------------------------- | -------------------------------------------------------------- |
| feature based | not hard to watch integration of feature components |                                                                |
| layer based   | similar components stick together                   | feature components are distributed between various directories |

## What I Chose
<!-- State the decision clearly -->
Using feature based architecture
## Why
<!-- The honest reasoning. What tipped the balance? -->
For me It is much easier to isolate feature components and test it
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
the dependency between different features how much it will cause silent problems
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What    | Link                                                          |
| ------- | ------------------------------------------------------------- |
| modules | https://github.com/stormkid2009/restooo/tree/main/src/modules |

---

## Connections

- **Made during experience:** [[experience/restooo]]
- **Based on concept:** [[concept/separation-of-concerns]]
<!-- Was this decision made from a known concept or a fuzzy one? -->
- **Concept confidence at time of decision:** known
- **Related pattern:** 
- **Related architecture:** [[architecture/feature-based]]

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
