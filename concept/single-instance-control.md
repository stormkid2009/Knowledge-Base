---
title: single instance control
date: 2026-03-05
reviewed: 04/03/2026
status: solid
tags:
  - concept
---

# 🔷 Single Instance Control

> One sentence — what is this concept in plain language?
 Ensure one instance of an object exists in memory and provide a single point of access to it
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
prevent filling the memory with many instances of the same object
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
We have in school only one notice board, so all teachers use this board no new instances of the board.the risk here free access can make many problems!
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- exporting singleton instance gives us the control of object behavior
- testing this kind of object will be difficult
- sometimes we gonna need dependency injection
- stateless object is preferred case to avoid global side effects
- safer examples like logger , immutable config , database pool manager and dependency container
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
Single instance pattern is always good for shared resources but it can make hidden dependencies so it can be difficult in testing and can cause unexpected state sharing

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/mham-api]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
[[experience/restooo]]
- **Expressed by pattern:** [[pattern/module-singleton]]
- **Implemented by technology:** [[technology/typescript]] [[technology/express-js]] [[technology/prisma]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
