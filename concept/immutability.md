---
title: immutability
date: 2026-04-27
reviewed: 04/29/2026
status: growing
tags:
  - concept
---

# 🔷 Immutability

> One sentence — what is this concept in plain language?
Freeze data at certain time to keep its value with no changes
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
we need the current value of data in certain operation and any update will lead to wrong results
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
we have sale on some products and client ordered them before midnight and new day discount is vanished
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- immutability is good shape to prevent side effects
- it does not mean to keep stale data forever
- it creates predictability
- it trades memory for safety
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
immutable data has no probability to change and this is not true because we only keep the original data safe and make new copy with changes

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
we have rich area in JavaScript array methods like (map , filter ,reduce ...etc) which return new array instead of mutating the original one
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
[[experience/order-service]]
- **Expressed by pattern:** [[pattern/snapshot]]
- **Implemented by technology:** [[technology/typescript]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
