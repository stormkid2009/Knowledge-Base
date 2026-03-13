---
title: generics
date: 2026-03-11
reviewed:
status: draft
tags:
  - concept
  - gap
---

# 🔷 Generics

> One sentence — what is this concept in plain language?
Simply put a placeholder for data shape we don't know
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
Write reusable code that works with different types while keeping type safety
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
It just a label on a box says what goes inside in build time the person who uses the box who decides the type will be persist forever(for this instance !)
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- the type is decided at call time not declaring time
- keep full type safety no need to use any type
- we can use same function to handle many types
- once a generic type is set for an instance it is locked
- that instance cannot change its type
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
- they think that typescript types exist at production but the fact after compiling there is no types  just plain JavaScript
## Gaps I Still Have
<!-- Honest list of what you don't fully understand yet about this concept -->
<!-- Delete this section when status reaches solid -->
- generics inside generics make me confused

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/prisma-helper]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->

- **Expressed by pattern:** [[pattern/discriminated-union]]
- **Implemented by technology:** [[technology/typescript]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
