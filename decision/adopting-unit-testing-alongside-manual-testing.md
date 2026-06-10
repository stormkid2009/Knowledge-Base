---
title: adopting unit testing alongside manual testing
date: 2026-03-19
status: solid
tags:
  - decision
repo: https://github.com/stormkid2009/mham-api
---

# 🗂️ Adopting unit testing alongside manual testing

> One sentence — what was the choice you had to make?
Manual testing is enough or combine it with unit tests?
---

## The Context
<!-- What situation forced this decision? What were the constraints? -->
Manual testing with insomnia only can lead to inaccurate results
## The Real Options
<!-- Only create this note if there were genuine alternatives -->

| Option                      | Pros                                            | Cons                      |
| --------------------------- | ----------------------------------------------- | ------------------------- |
| testing with insomnia       | simple with no more config and boilerplate code | not accurate all the time |
| unit tests alongside manual | acceptable and accurate results                 | more configs and code     |

## What I Chose
<!-- State the decision clearly -->
second option the combination between unit tests and manual tests
## Why
<!-- The honest reasoning. What tipped the balance? -->
to be on the safe side is good instinct,sometimes as human can forget tiny details to check in manual testing and this leads to potential bugs in the future.
## What I Was Uncertain About
<!-- What did you not fully know at the time of deciding? -->
what technology to use for unit testing alongside insomnia as manual tool for testing
## How It Turned Out
<!-- Fill this in later — was it the right call? What would you change? -->
<!-- Leave blank at first, come back to it -->
- it makes me more confident about code accuracy
- it reduces the rate of potential issues
---

## Code Reference
<!-- Link to the commit or file where this decision lives in the code -->

| What                              | Link                                                                                                                                       |
| --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------ |
| handle pirsma operation test file | https://github.com/stormkid2009/mham-api/blob/10b12c91a550896166b82171c907669952d653dd/src/middleware/handlePrismaOperation.test.ts#L1-L49 |

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
