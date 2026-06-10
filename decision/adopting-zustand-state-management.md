---
title: adopting zustand state management
date: 2026-03-30
status: growing
tags:
  - decision
repo: https://github.com/stormkid2009/exams-platform
---

# 🗂️ Adopting zustand state management

> One sentence — what was the choice you had to make?
Using Zustand or Props drilling to manage the state?
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
keep certain user's data available globally over the application.
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option         | Pros                           | Cons                                                                           |
| -------------- | ------------------------------ | ------------------------------------------------------------------------------ |
| zustand        | light state manager            | extra dependency with learning curve                                           |
| props drilling | no extra dependency to install | more code and complexity passing props down from parents componentes to childs |

## What I Chose
<!-- State the decision clearly -->
I went with using Zustand
## Why
<!-- The honest reasoning. What tipped the balance? -->
the data user I want to share is tiny and Zustand will do this perfectly than props drilling which can lead to potentials errors.
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
It was first time to use Zustand so I was not sure if it will do the job as expected
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What       | Link                                                                                                                        |
| ---------- | --------------------------------------------------------------------------------------------------------------------------- |
| auth-store | https://github.com/stormkid2009/exams-platform/blob/734faa5d4a52b13c5cf1bdc3d09683e6ecedad12/src/store/auth-store.ts#L1-L76 |

---

## Connections

- **Made during experience:** [[experience/exams-platform]]
- **Based on concept:** [[concept/state-management]]
<!-- Was this decision made from a known concept or a fuzzy one? -->
- **Concept confidence at time of decision:** known
- **Related pattern:** 
- **Related architecture:** 

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
