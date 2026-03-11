---
title: discriminated union
date: 2026-03-05
status: draft
tags:
  - pattern
---

# 🔁 Discriminated Union

> One sentence — what problem does this pattern solve?
Manage case of success and case of failure in API response with different types of data
---

## The Problem
<!-- What recurring situation demands this pattern? -->
API response maybe success with data or failed with error message and we don't know what type of data we will get
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
**The pattern idea:** A type that can be one of two distinct shapes, with a shared field that tells you which one you're dealing with at runtime. 

**The TypeScript implementation:** Use a discriminated union with generics — one shape for success with data, one shape for failure with an error message.
TypeScript narrows the type automatically when you check the discriminant field.
## When To Use It
<!-- ✅ Use when... -->
- When an operation can succeed or fail with different data shapes
- When we want to avoid use any type
- When caller needs to handle two cases explicitly
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- When we use plain JavaScript
- When the response holds same data shape regardless to success or failure
- When simplicity is the right decision over complexity
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What                  | Link                                                                                                                                   |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| service response type | https://github.com/stormkid2009/restooo/blob/f95a0772394a6dde422a7e2828c015773acd34e2/src/modules/customer/customer.service.ts#L12-L17 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/customer-service]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/type-safety]]
- **Related technology:** [[technology/typescript]]
- **Related decision:** [[decision/consistency-vs-variant-responses]]

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
