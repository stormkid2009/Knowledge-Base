---
title: exams platform
date: 2026-03-29
type: general
parent:
status: draft
tags:
  - experience
  - gap
repo: https://github.com/stormkid2009/exams-platform
---

# 🧪 Exams platform

> One sentence — what is this experience about?
 Building huge base for french language various questions with answers
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
building my personal question answer bank to reuse when I am planning to make test for my students
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
I built dashboard to create and store french questions using zod for type schema validation and zustand for auth state management
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
- data validation using zod
- manage auth state using zustand instead of props drilling

---

## Code Reference

| What                          | Link                                                                                                                                       |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| type safety with zod          | https://github.com/stormkid2009/exams-platform/blob/734faa5d4a52b13c5cf1bdc3d09683e6ecedad12/src/shared/schemas/grammaire.schema.ts#L1-L40 |
| state mangement using zustand | https://github.com/stormkid2009/exams-platform/blob/734faa5d4a52b13c5cf1bdc3d09683e6ecedad12/src/store/auth-store.ts#L1-L76                |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/type-safety]]
- [[concept/separation-of-concerns]]
- [[concept/state-management]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- 

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- [[experience/quiz-maker]]

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/mham]]

### Other Nodes
- **Pattern applied:** [[pattern/token-based-authentication]]
- **Decision made:** [[decision/adopting-zustand-state-management]]
- **Bug encountered:** 
- **Technology used:** [[technology/next-js]] [[technology/zod]] [[technology/zustand]] [[technology/mongo-db]] [[technology/mongoose]]
- **Architecture involved:** [[architecture/layer-based]]

---
<!-- Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
