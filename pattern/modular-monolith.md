---
title: modular monolith
date: 2026-03-25
status: growing
tags:
  - pattern
---

# 🔁 Modular Monolith

> One sentence — what problem does this pattern solve?
avoid writing the whole code in huge fat component
---

## The Problem
<!-- What recurring situation demands this pattern? -->
difficulty in maintain code base and high risk to break code with bugs
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
apply separation of concerns and divide the code base into various features or modules integrated to compose the whole app
## When To Use It
<!-- ✅ Use when... -->
- middle to big size projects
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
small project or simple script to implement determined task

---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What                      | Link                                                                |
| ------------------------- | ------------------------------------------------------------------- |
| [[experience/quiz-maker]] | https://github.com/stormkid2009/quiz-maker/tree/main/src/app/api/v1 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/quiz-maker]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
discovered
- **Related concept:** [[concept/separation-of-concerns]]
- **Related technology:** [[technology/next-js]]
- **Related decision:** [[decision/feature-based-vs-layer-based]]

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
