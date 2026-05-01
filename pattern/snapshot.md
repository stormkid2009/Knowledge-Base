---
title: snapshot
date: 2026-04-25
status: draft
tags:
  - pattern
---

# 🔁 Snapshot

> One sentence — what problem does this pattern solve?
 certain data we need to keep its value at this  current time because mutate it will give wrong computations
---

## The Problem
<!-- What recurring situation demands this pattern? -->
suppose we are updating product's price and the customer already ordered it  with old price 
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
- menu items prices represent data has been frozen
- employee or customer is the actor in this operation
- order transaction is the operation we froze the data within
## When To Use It
<!-- ✅ Use when... -->
- special case we need to freeze data and use it in certain operation 
- we need to make records for data analytics over time
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- when we need recent and updated data 
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What                         | Link                                                                                                                               |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| [[experience/order-service]] | https://github.com/stormkid2009/restooo/blob/cd1907570add33c5b2efb276d42cf6f4e9c41b8d/src/modules/order/order.service.ts#L113-L138 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/order-service]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/immutability]]
- **Related technology:** [[technology/typescript]]
- **Related decision:** 

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
