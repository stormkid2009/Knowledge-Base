---
title: mham api
date: 2026-03-18
type: general
parent:
status: draft
tags:
  - experience
  - gap
repo: https://github.com/stormkid2009/mham-api
---

# 🧪 MHAM API

> One sentence — what is this experience about?
evolving in building restful api and adopting typescript
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
full API for brokerage and real estate agency 
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
go out from comfort zone and try prisma orm with postegresql as database
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
- using relational database with orm
- apply unit testing with jest
- using middleware to keep dry
## What Surprised Me
<!-- Optional but valuable. What didn't go as expected? -->

---

## Code Reference

| What                         | Link                                                                                                                             |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| [[pattern/module-singleton]] | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/src/db/prisma.client.ts#L1-L6             |
| [[concept/testing]]          | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/src/controllers/unit.controller.ts#L1-L83 |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/type-safety]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- [[concept/testing]] 

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- [[experience/exams-platform]]

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/express-team]]
- [[experience/api-template]] 

### Other Nodes
- **Pattern applied:** [[pattern/module-singleton]]
- **Decision made:** [[decision/adopting-relational-db-with-prisma-orm]]
- **Bug encountered:** 
- **Technology used:** [[technology/typescript]] [[technology/prisma]] [[technology/express-js]] [[technology/postgresql]] [[technology/jest]] 
- **Architecture involved:** [[architecture/layer-based]] 

---
<!-- Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
