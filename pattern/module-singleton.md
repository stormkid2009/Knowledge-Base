---
title: module singleton
date: 2026-03-05
status: draft
tags:
  - pattern
  - "#gap"
---

# 🔁 Module Singleton

> Ensure that class has only one instance and provide global access to it
---

## The Problem
<!-- What recurring situation demands this pattern? -->
Creating many instances or objects which absorb resources
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
Export only one instance of class and module system make it works as node-js does caching module after first import load
## When To Use It
<!-- ✅ Use when... -->
when we need to manage resources
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- Testing because singletons are hard to mock
- Multiple config for the same class
- when instance holds state which varies per request
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What    | Link                                                                                                                                    |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| restooo | https://github.com/stormkid2009/restooo/blob/f95a0772394a6dde422a7e2828c015773acd34e2/src/modules/customer/customer.service.ts#L19-L325 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/customer-service]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/single-instance-control]]
- **Related technology:** [[technology/typescript]]
- **Related decision:** 

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
