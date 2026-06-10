---
title: consistency vs variant responses
date: 2026-06-04
status: draft
tags:
  - decision
  - gap
repo: https://github.com/stormkid2009/restooo
---

# 🗂️ consistency vs variant responses

> One sentence — what was the choice you had to make?
hard code service responses or make template of response for each case
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
every time create response phrase for certain situation end up with a huge mess of variant responses sometimes for the similar cases
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option                | Pros             | Cons                               |
| --------------------- | ---------------- | ---------------------------------- |
| Template of responses | keep consistency | ignore special cases               |
| Hard code responses   | creative         | messy and huge number of responses |

## What I Chose
<!-- State the decision clearly -->
I went with Template option
## Why
<!-- The honest reasoning. What tipped the balance? -->
It helps so much in debug and easy to read
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
I did not know if special cases gonna make real problem later
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What            | Link                                                                                                             |
| --------------- | ---------------------------------------------------------------------------------------------------------------- |
| error responses | https://github.com/stormkid2009/restooo/blob/a8a4aefe0e878d8bcbdef8c04034ce836e24f651/src/utils/errors.ts#L1-L47 |

---

## Connections

- **Made during experience:** [[experience/restooo]]
- **Based on concept:** [[concept/consistency]]
<!-- Was this decision made from a known concept or a fuzzy one? -->
- **Concept confidence at time of decision:** known
- **Related pattern:** [[pattern/discriminated-union]]
- **Related architecture:** 

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
