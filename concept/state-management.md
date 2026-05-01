---
title: state management
date: 2026-03-30
reviewed: 04/24/2026
status: draft
tags:
  - concept
  - gap
---

# 🔷 State management

> One sentence — what is this concept in plain language?
it is data which can change over time and affect the application behavior
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
- synchronize application UI with potential updates (Reactivity) [[pattern/observer]]
- control transition between application special cases like reservation system (finite state machine)[[pattern/state]]
- store special data outside the component life cycle (persistence) [[pattern/observer]]  + [[pattern/singleton]]
- server should forget between requests (statelessness)
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
the weather gonna be cold today so I wear warm clothes or the opposite
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- state is dynamic and this afford flexibility to our project
- server side operations must be stateless
- choosing right approach to manage state depends on the scale of project
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
- the mix between state and props in react
- thinking there is no relation between state and component life cycle


---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/express-team]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
[[experience/mham]] [[experience/cakes-shop]] [[experience/exams-platform]]
- **Expressed by pattern:** [[pattern/observer]] [[pattern/state]] [[pattern/singleton]]
- **Implemented by technology:** [[technology/zustand]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
