---
title: prisma helper
date: 2026-03-11
type: sub
parent: "[[experience/mham-api]]"
status: draft
tags:
  - experience
  - gap
repo: https://github.com/stormkid2009/mham-api
---

# 🧪 Prisma Helper

> One sentence — what is this experience about?
it is about reusable function I can share logic along my project
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
building middleware to handle prisma operations and HTTP request and response
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
I built an async wrapper function to handle any prisma CRUD operations and send responses centralized in one place
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
using generics here means this function any prisma operation regardless its return type

---

## Code Reference

| What            | Link                                                                                                                          |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| helper function | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/src/middleware/prisma.helper.ts#L1-L18 |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/generics]]
- [[concept/asynchronous]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- 

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- 

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/mham-api]]

### Other Nodes
- **Pattern applied:** [[pattern/high-order-function]]
- **Decision made:** 
- **Bug encountered:** 
- **Technology used:** [[technology/typescript]]
- **Architecture involved:** 

---
<!-- Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
