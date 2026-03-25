---
title: versioning
date: 2026-03-17
status: draft
tags:
  - pattern
  - gap
---

# 🔁 Versioning

> One sentence — what problem does this pattern solve?
we don't want our app to be down for certain time until we finish update our code base
---

## The Problem
<!-- What recurring situation demands this pattern? -->
keep the old version up as users need it and make new version up too
## The Solution
<!-- The structure. Who are the participants and what are their roles? -->
make new version with same app so we have like v1 , v2 and both up
## When To Use It
<!-- ✅ Use when... -->
- when I want freedom to fix bugs and deploy updates without affecting current users
- when adding major breaking changes and existing users need time to migrate
## When To Avoid It
<!-- ❌ Avoid when... What simpler alternative exists? -->
- if old version is worthless to keep and upgrade is mandatory
- with small projects with no external consumers
---

## Code Reference
<!-- Link to where you actually applied this pattern in a real repo -->

| What                        | Link                                                          |
| --------------------------- | ------------------------------------------------------------- |
| [[experience/api-template]] | https://github.com/stormkid2009/api-template/tree/main/src/v1 |

---

## Connections

- **Applied in experience:** 
<!-- The experience where you first used or discovered this pattern -->
[[experience/api-template]]
- **Was I applying it knowingly or did I discover it?**
<!-- knowingly | discovered -->
knowingly
- **Related concept:** [[concept/backward-compatibility]]
- **Related technology:** [[technology/express-js]]
- **Related decision:** [[decision/maintenance-flexibility-vs-mandatory-upgrade]]

---
<!-- Habit check before closing:
  1. Where did I actually use this? → fill Applied in experience + Code Reference
  2. Did I know this pattern going in or did I discover it? → answer the question above
  3. What concept does this express? → fill Related concept
-->
