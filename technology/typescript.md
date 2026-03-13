---
title: typescript
date: 2026-03-05
since: "2022"
reviewed:
status: draft
tags:
  - technology
  - "#gap"
docs: https://www.typescriptlang.org/docs/
---

# ⚙️ TypeScript

> One sentence — what does this tool do?
It is super set of JavaScript with strict types check
---

## What It Is
<!-- The tool, library, or language. What problem does it solve? -->
It is a language over JavaScript to solve the problem of dynamic types
## What Concept Does It Implement
<!-- Every tool is an expression of an abstract concept -->
[[concept/type-safety]] [[concept/generics]]
## How I Actually Used It
<!-- Not the docs — your real usage. What did you do with it? -->
At the beginning I used it like JavaScript and sometimes use any type to avoid headache of types checker
## Key Behaviours To Remember
<!-- The things that aren't obvious. Gotchas, quirks, surprises. -->
- writing boilerplate is sometimes big headache especially when u come from JavaScript background
- reading typescript error message with long details to discover where is the error

## What I Still Don't Fully Understand
<!-- Honest gaps. Delete when status reaches solid. -->
- generics
- enums
- narrowing types

---

## Progress Timeline
<!-- One row per experience. The repo link is your proof. -->

| When | Experience                   | What I Could Do                    | Proof                                                                                                                            |
| ---- | ---------------------------- | ---------------------------------- | -------------------------------------------------------------------------------------------------------------------------------- |
| 2022 | [[experience/api-template]]  | explicit type annotation           | https://github.com/stormkid2009/api-template/blob/9995de1f563aedb4e5cd42631f87f5d9d98c62e2/src/v1/services/cardService.ts#L1-L64 |
| 2024 | [[experience/prisma-helper]] | using generics instead of any type | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/src/middleware/prisma.helper.ts#L1-L18    |
- - -



## Code Reference

| What         | Link                                                                                                                             |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------- |
| user service | https://github.com/stormkid2009/api-template/blob/9995de1f563aedb4e5cd42631f87f5d9d98c62e2/src/v1/services/userService.ts#L1-L65 |

---

## Connections

- **First used in experience:** [[experience/api-template]]
- **Implements concept:** [[concept/type-safety]] [[concept/generics]]
- **Enables pattern:** 
- **Caused bug:** 

---
<!-- Habit check before closing:
  1. What concept does this tool express? → fill Implements concept
  2. Where did I actually use this? → fill First used in experience + Code Reference
  3. What surprised me or caught me out? → fill Key Behaviours To Remember
  4. Update reviewed: date every time you revisit
-->
