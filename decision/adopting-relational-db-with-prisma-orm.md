---
title: adopting relational db with prisma orm
date: 2026-03-19
status: growing
tags:
  - decision
repo: https://github.com/stormkid2009/mham-api
---

# 🗂️ Adopting relational db with Prisma ORM

> One sentence — what was the choice you had to make?
Start using Prisma ORM with relational database PostgreSQL Or stick with MongoDB with mongoose
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
I wanted to jump out of my comfort zone (MongoDB with mongoose) and try PostgreSQL with Prisma
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option     | Pros                | Cons                                                 |
| ---------- | ------------------- | ---------------------------------------------------- |
| Prisma ORM | discover new things | new stack to learn                                   |
| Mongoose   | familiar technology | repeating same work like any other precedent project |

## What I Chose
<!-- State the decision clearly -->
I decided PostgreSQL with Prisma
## Why
<!-- The honest reasoning. What tipped the balance? -->
New Project with new challenge to extend my knowledge via trying new technology
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
I was not sure if I can really deal good with PostgreSQL and relational DB in general
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->

---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What               | Link                                                                                                               |
| ------------------ | ------------------------------------------------------------------------------------------------------------------ |
| prisma.schema file | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/prisma/schema.prisma#L7-L14 |

---

## Connections

- **Made during experience:** [[experience/mham-api]]
 

---
<!-- Habit check before closing:
  1. Were there genuinely two real options? If not — this isn't a decision note
  2. What was I uncertain about? → fill that section honestly
  3. Link to the commit where this decision is visible in the code
  4. Come back later and fill How It Turned Out
-->
