---
title: fat routes
date: 2026-03-16
status: draft
tags:
  - pattern
  - gap
---

# 🔁 Fat Routes

> One sentence — what problem does this pattern solve?
Keep all operations of  APIs requests handling within Express routes rather than different layers like service and control
---

## The Problem
<!-- What recurring situation demands this pattern? -->
creating simple logistic app with minor data modifications does not need over engineering with multiple layers architecture
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
- Express Router receives requests and send to handlers
- Route handlers validate requests and resolve responses
- Mongoose models keep the shape of entity by using certain schema
## When To Use It
<!-- ✅ Use when... -->
- Simple CRUD application with minimal business logic
- Solo developers or small teams (2-3 people)
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- Complex domain logic
- Application requiring comprehensive unit testing
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What        | Link                                                                                                                      |
| ----------- | ------------------------------------------------------------------------------------------------------------------------- |
| order route | https://github.com/stormkid2009/expressTeam/blob/26e97fff7dca692f6f66d229d71503af7b5499e3/server/routes/orders.js#L1-L101 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/express-team]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/centralization]]
- **Related technology:** [[technology/express-js]] [[technology/mongo-db]] [[technology/mongoose]]
- **Related decision:** [[decision/simple-and-ready-for-production]]

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
