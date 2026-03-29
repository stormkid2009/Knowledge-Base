---
title: auth
date: 2026-03-28
reviewed: 03/29/2026
status: growing
tags:
  - concept
  - gap
---

# 🔷 Auth

> One sentence — what is this concept in plain language?
verify the user and which domain he can access
---

## Core Idea
<!-- The "why". What problem does this concept exist to solve? -->
keep track of user activity and give access for protected routes
## Mental Model
<!-- An analogy or image that makes it click for you personally -->
in world of online games users can login and play but GM only has access to make events or ban player who abuse game's rules
## Key Properties
<!-- 3-5 bullet points. The essential things to know. -->
- authentication is to verify the identity of user
- authorization is to give access for certain domains 
- we can delegate auth to providers like google,x and facebook using OAuth
## Common Misconception
<!-- What do people (or you) get wrong about this? -->
well the mix comes here to think auth is only login or user verification but auth has also role of allow access for certain routes as example
## Gaps I Still Have
<!-- Honest list of what you don't fully understand yet about this concept -->
<!-- Delete this section when status reaches solid -->
- need to sharp understanding of jwt tokens and refresh tokens
- need to fully understand cookies
- need to sharpen session's fully understanding

---

## Connections

- **Surfaced by:** 
<!-- The first experience that revealed this concept to you -->
[[experience/next-auth]]
- **Reinforced by:** 
<!-- Other experiences that deepened your understanding over time -->
- [[experience/cakes-shop]]
- [[experience/exams-platform]]
- [[experience/restooo]]
- **Expressed by pattern:** [[pattern/oauth]]
- **Implemented by technology:** [[technology/next-js]] [[technology/express-js]]

---
<!-- Habit check before closing:
  1. Can I explain this in one sentence? → fill the callout at the top
  2. Where did I first encounter this? → fill Surfaced by
  3. What do I still not fully understand? → fill Gaps I Still Have
  4. Update reviewed: date every time you revisit and deepen this note
-->
