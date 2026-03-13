# 🧠 Knowledge-Base

> A personal knowledge system that lives in Obsidian and connects to all my GitHub repos.  
> Not a collection of notes — a network of understanding built from real code, real decision, and real experience.

---

## What This Is

This vault is the **thinking layer** on top of all my projects.

When I write code in any repo, I learn something — a concept clicks, a pattern emerges, a bug corrects my mental model, a decision gets made. That knowledge used to live nowhere. Now it lives here, linked directly back to the exact file, line, or commit where it was born.

Every note in this vault points outward to real code on GitHub.  
Every piece of real code on GitHub can be traced back to a note here.

---

## The Structure

**Experience is the center.** Everything else radiates from it.

```
              🔷 concept/
                   ▲
        validates  │  discovers
                   │
🔁 pattern/ ◄──── 🧪 experience/ ────► 🗂️ decision/
                   │
         ┌─────────┼──────────┐
         ▼         ▼          ▼
      ⚙️ tech/  🏛️ arch/   🐛 debug/
```

An experience is where things actually happen. Every other node exists to capture what that experience taught, revealed, or produced.

---

## The 8 Nodes

| Node                | The Question It Answers                       |
| ------------------- | --------------------------------------------- |
| 🧪 `experience/`    | *What happened when I actually built it?*     |
| 🔷 `concept/`       | *Why does this exist? What is the core idea?* |
| 🔁 `pattern/`       | *How do I solve this class of problem?*       |
| ⚙️ `technology/`    | *What tool does this? How does it behave?*    |
| 🐛 `debugging/`     | *What broke, why, and what did it teach me?*  |
| 🏛️ `architecture/` | *How does it all fit together at scale?*      |
| 🗂️ `decision/`     | *Why did I choose this over that?*            |
| 🗺️ `map/`          | *How do all the notes connect to each other?* |

---

## Two Kinds of Concepts

Not all concepts are equal. Every experience touches concepts in two different ways:

**Concepts I applied** — things I already understood and deliberately used.  
**Concepts I discovered** — things the experience revealed, or ideas I only partially understood that need deeper work.

Discovered concepts become `draft` concept notes. They are **gaps in my knowledge** — tracked with `#gap` tag until they become `solid`.

This means the concept node has a lifecycle:
- `draft` — surfaced by one experience, not yet owned
- `growing` — appearing across multiple experiences, understanding deepening
- `solid` — I can explain it, apply it, and recognize it anywhere

---

## Experiences Connect Directly To Each Other

Not everything flows through a concept. Sometimes one experience directly unlocks another:

> *"I built X, which gave me the foundation to attempt Y"*  
> *"I built X, then the next logical step in the project was Y"*

These direct chains are the **narrative of how I grew as a developer**. They live in the `Leads To` and `Came From` fields of every experience note.

---

## How It Connects to GitHub

Notes don't contain code — they **link to it**.

| Link Type | Points To | Used For |
|---|---|---|
| File link | A specific file in a repo | Technology, pattern references |
| Line link | A specific line in a file | Debugging, precise code moments |
| Commit link | A permanent snapshot in time | Decisions, bug fixes — never changes |

---

## How To Use This Vault

**After a coding session — ask these questions:**

1. Did I apply or discover a concept? → `concept/`
2. Did I use a pattern knowingly, or find one by accident? → `pattern/`
3. Did something break and teach me something? → `debugging/`
4. Did I make a real choice between two genuine alternatives? → `decision/`
5. Did I ship or build something? → `experience/`

**Before starting something new:**
- Planning a system or feature? → Start in `architecture/` or `decision/`
- Come back after and link to what you actually built

**The non-negotiable habits:**
- Every note links to at least one other note
- Every note links to at least one GitHub URL
- Every bug creates or updates a concept note
- Every discovered concept starts as `draft` with tag `#gap`
- A note with no links is an island — it is not part of the system yet

---

## Repos Connected to This Vault

| Repo | What It Contains |
|---|---|
| [restooo](https://github.com/stormkid2009/restooo) | Restaurant app — customer service, business logic |
| [Coding-Notes](https://github.com/stormkid2009/Coding-Notes) | Earlier notes — may be referenced here |
| *(add repos as you connect them)* | |

---

## Meta

- This vault is itself a repo — decisions about how the system works are tracked in `decision/`
- The `map/` folder contains indexes and knowledge threads
- Start exploring: [`map/`](map/)
