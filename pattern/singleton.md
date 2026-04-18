---
title: singleton
date: 2026-04-02
status: draft
tags:
  - pattern
  - theoretical
---

# 🔁 Singleton

> One sentence — what problem does this pattern solve?
Ensure that only one instance of the class is shared between resources
---

## The Problem
<!-- What recurring situation demands this pattern? -->
every time we need to use class we create new instance this will lead to big mess in the memory and affect the performance badly
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
static method "getInstance " is the shared point and class constructor control create only one instance which we can use within our app
## When To Use It
<!-- ✅ Use when... -->
when we have stateless shared resources or configurations 
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
 when shared state can be mutated and this side effect leads to wrong computations in another component using it.
---


---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->

- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->

- **Related concept:** [[concept/single-instance-control]]
- **Related technology:** 
- **Related decision:** 

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
