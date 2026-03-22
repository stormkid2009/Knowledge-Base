---
title: asynchronous
date: 2026-03-16
reviewed: 03/22/2026
status: solid
tags:
  - concept
---

# 🔷 Asynchronous

> One sentence — what is this concept in plain language?
initiating an operation and go on without waiting for it when it completed we take reaction
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
some operations need time to been resolved or rejected like API response
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
- we are getting ready to go outside when the pizza is ready
- async operation is like sub pipeline which merge back to the main when it completes
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- asynchronous operation will not block other operations
- asynchronous is really useful with one thread language like JavaScript
- asynchronous is good for operation which need time to be processed

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/express-team]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
[[experience/mham-api]] [[experience/customer-service]]
- **Expressed by pattern:** [[pattern/high-order-function]]
- **Implemented by technology:** [[technology/typescript]] [[technology/node-js]] 

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
