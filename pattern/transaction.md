---
title: transaction
date: 2026-04-19
status: draft
tags:
  - pattern
  - gap
---

# 🔁 Transaction

> One sentence — what problem does this pattern solve?
a wrapper of dependent actions to ensure the success of all or roll back if one failed
---

## The Problem
<!-- What recurring situation demands this pattern? -->
when multiple operations need to succeed together and partial success can be more harmful than total failure
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
- Caller : createOrder method 
- Mechanism: transaction wrapper (prisma interactive transaction)
- Operations: generate order id - lock table to be occupied - compute the total price including tax and tip
- Roll back if any operation failed
## When To Use It
<!-- ✅ Use when... -->
doing series of actions and wanna treat them as one unit if one fail means all failed too
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- independent operations
- simple operations
- negative effect on performance
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What                         | Link                                                                                                                               |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| [[experience/order-service]] | https://github.com/stormkid2009/restooo/blob/b4d1919d43759c6d0d26e8f13d4d560ee6c38cc0/src/modules/order/order.service.ts#L162-L211 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/order-service]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/atomicity]] [[concept/race-condition]]
- **Related technology:** [[technology/prisma]]
- **Related decision:** 

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
