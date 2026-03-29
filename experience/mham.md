---
title: mham
date: 2026-03-28
type: general
parent:
status: draft
tags:
  - experience
  - gap
repo: https://github.com/stormkid2009/MHAM
---

# 🧪 MHAM

> One sentence — what is this experience about?
apply real estate domain model to serve real estate agency
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
next js app with tailwind css and mongodb for back end
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
- build front end reusable components like layout footer and navbar
- adding  lib for mongoDB native driver
- back end logic lives in pages/api
- adding util folder for domain constants
- use tailwind css for efficient and simple style
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
instead of using more dependencies to write simple back end logic we can use next api route to do the job as minimum viable product

---

## Code Reference

| What         | Link                                                                                                             |
| ------------ | ---------------------------------------------------------------------------------------------------------------- |
| add new unit | https://github.com/stormkid2009/MHAM/blob/bf0825aaa1439711a0f724a9bb1ff48fa5db899c/pages/api/units/add.js#L1-L48 |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/separation-of-concerns]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- [[concept/auth]]

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- [[experience/next-auth]] 

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/express-team]]

### Other Nodes
- **Pattern applied:** 
- **Decision made:** [[decision/adopting-mvp-structure]]
- **Bug encountered:** 
- **Technology used:** [[technology/next-js]] [[technology/mongo-db]]
- **Architecture involved:** [[architecture/monolith]]
---

<!--  Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
