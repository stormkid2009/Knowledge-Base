---
title: next auth
date: 2026-03-28
type: sub
parent: "[[experience/mham]]"
status: draft
tags:
  - experience
  - gap
repo: https://github.com/stormkid2009/MHAM
---

# 🧪 Next Auth

> One sentence — what is this experience about?
apply authentication for users
---

## What I Was Building
<!-- The context. What was the goal? What problem were you solving? -->
add next auth using google provider
## What I Did
<!-- Your approach. Key decisions made. No need for full detail — link to the code. -->
configured next-auth with google provider, setup the API route and session handling
## What I Learned
<!-- The honest takeaway. What shifted in your understanding? -->
- OAuth delegates authentication responsibility to google
- I don't have to check password manually or hash them
- keep minimal dependencies

---

## Code Reference

| What                      | Link                                                                                                                          |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| auth with google provider | https://github.com/stormkid2009/MHAM/blob/bf0825aaa1439711a0f724a9bb1ff48fa5db899c/pages/api/auth/%5B...nextauth%5D.js#L1-L20 |

---

## Connections

### Concepts I Applied
<!-- Concepts you already knew and deliberately used -->
- [[concept/separation-of-concerns]]

### Concepts I Discovered
<!-- New or fuzzy concepts this experience surfaced → create a draft concept note for each one -->
- [[concept/auth]]

### Leads To
<!-- Direct links to experiences this one unlocked or made possible -->
- [[experience/cakes-shop]]

### Came From
<!-- Direct links to experiences that preceded and enabled this one -->
- [[experience/mham]]

### Other Nodes
- **Pattern applied:** 
- **Decision made:** 
- **Bug encountered:** 
- **Technology used:** [[technology/next-js]]
- **Architecture involved:** 

---
<!-- Habit check before closing:
  1. What did this come from? → fill Came From + Parent
  2. What does this point to? → fill Leads To
  3. Where does the code live? → fill Code Reference
  4. Did this surface any fuzzy concepts? → fill Concepts I Discovered + create draft concept notes
-->
