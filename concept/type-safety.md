---
title: type safety
date: 2026-03-05
reviewed: 03/30/2026
status: solid
tags:
  - concept
---

# 🔷 Type Safety

> One sentence — what is this concept in plain language?
 Ensure every value in the code base has known and constant type during development
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
 Solve the side effect of JavaScript dynamic types check
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
let's say we have multiple pets and each one needs different kind of treating food caring etc so if we give cat's treatment to turtle it will be not safe
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- type safety save time searching for non logical bugs
- discover bugs or typos in development phase
- save resources in memory allocation
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
The time's cost of writing more boilerplate is less than hunting dynamic type bugs later

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/api-template]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
- [[experience/mham]]
- [[experience/mham-api]]
- [[experience/exams-platform]]
- [[experience/quiz-maker]]
- [[experience/restooo]]
- **Expressed by pattern:** [[pattern/discriminated-union]]
- **Implemented by technology:** [[technology/typescript]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
