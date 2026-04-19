---
title: order service
date: 2026-04-19
type: sub
parent: "[[restooo]]"
status: draft
tags:
  - experience
repo: https://github.com/stormkid2009/restooo
---

# 🧪 Order Service

> One sentence — what is this experience about?
creating orders for customers in small restaurant and reserve tables for dine in 
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
- creating orders for customers
- update tables status
- keep track of order status until completed or cancelled in previous phase
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
- I used [[pattern/transaction]] via prisma interactive transaction as a wrapper for steps of creating the order to ensure all are success or roll back 
- with this approach we avoid risks like table status occupied forever or two customers share the same table
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
doing series of dependent actions which all shall be success or fail
## What Surprised Me
<!-- Optional but valuable. What didn't go as expected? -->
the case table can be permanently occupied and two customers share the same table risks

---

## Code Reference

| What                           | Link                                                                                                                               |
| ------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| prisma interactive transaction | https://github.com/stormkid2009/restooo/blob/b4d1919d43759c6d0d26e8f13d4d560ee6c38cc0/src/modules/order/order.service.ts#L162-L211 |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/race-condition]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- [[concept/atomicity]]

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- 

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/concurrency-study]]

### Other Nodes
- **Pattern applied:** [[pattern/transaction]]
- **Decision made:** 
- **Bug encountered:** 
- **Technology used:** [[technology/prisma]]
- **Architecture involved:** 

---
<!-- Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
