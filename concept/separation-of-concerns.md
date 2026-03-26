---
title: separation of concerns
date: 2026-03-05
reviewed: 03/25/2026
status: solid
tags:
  - concept
---

# 🔷 Separation of concerns

> One sentence — what is this concept in plain language?
Each component in project has clear and specific role to do 
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
to prevent potential bugs caused by shared responsibilities between different components
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
Car has various components like engine battery ...etc and each one does its clear job
to make the car go and transport us from place to other
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- determine principal role for every component
- divide huge and fat components into subordinates to distribute roles
- principal component role is to orchestrate the integration between subs
- discover bugs and maintenance will be much easier
- we have the ability to reuse the code or create instances of our components
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
I gave wrong role for certain component like register new user for user component instead of authentication component

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/api-template]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
- [[experience/mham-api]]
- [[experience/quiz-maker]]
- [[experience/restooo]]
- **Expressed by pattern:** [[pattern/modular-monolith]]
- **Implemented by technology:** [[technology/express-js]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
