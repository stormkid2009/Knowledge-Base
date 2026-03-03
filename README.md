# 🧠 Knowledge-Base

> A personal knowledge system that lives in Obsidian and connects to all my GitHub repos.  
> Not a collection of notes — a network of understanding built from real code, real decisions, and real experience.

---

## What This Is

This vault is the **thinking layer** on top of all my projects.

When I write code in any repo, I learn something — a concept clicks, a pattern emerges, a bug corrects my mental model, a decision gets made. That knowledge used to live nowhere. Now it lives here, linked directly back to the exact file, line, or commit where it was born.

Every note in this vault points outward to real code on GitHub.  
Every piece of real code on GitHub can be traced back to a note here.

---

## The 8 Nodes

| Node | The Question It Answers |
|---|---|
| 🔷 `concept/` | *Why does this exist? What is the core idea?* |
| ⚙️ `technology/` | *What tool does this? How does it behave?* |
| 🔁 `pattern/` | *How do I solve this class of problem?* |
| 🧪 `experience/` | *What happened when I actually built it?* |
| 🐛 `debugging/` | *What broke, why, and what did it teach me?* |
| 🏛️ `architecture/` | *How does it all fit together at scale?* |
| 🗂️ `decisions/` | *Why did I choose this over that?* |
| 🗺️ `map/` | *How do all the notes connect to each other?* |

---

## How It Connects to GitHub

Notes don't contain code — they **link to it**.

Three link types used throughout this vault:

- **File link** — points to a specific file in a repo
- **Line link** — points to a specific line where something interesting happens
- **Commit link** — points to a permanent snapshot in time (used for decisions and bugs)

This means the vault stays lightweight while the code stays where it belongs — in the repos.

---

## How To Use This Vault

**When you finish a coding session:**
- Did you learn a concept? → `concept/`
- Did you use a new tool in a real way? → `technology/`
- Did you apply a pattern? → `pattern/`
- Did you ship something? → `experience/`
- Did something break and teach you something? → `debugging/`
- Did you make a significant design choice? → `decisions/`

**When you're about to start something:**
- Planning a new feature or system? → Start in `architecture/` or `decisions/`
- Come back after and link to what you actually built

**The most important habit:**  
Every note should link to at least one other note and one GitHub URL.  
A note with no links is an island — it's not part of the system yet.

---

## Repos Connected to This Vault

| Repo | What It Contains |
|---|---|
| [Coding-Notes](https://github.com/stormkid2009/Coding-Notes) | Earlier notes — may be referenced here |
| *(add repos as you connect them)* | |

---

## Meta

- This vault is itself a repo — so decisions about *how the system works* are tracked in `decisions/`
- The `map/` folder contains indexes, knowledge threads, and the graph of connections
- Start exploring: [`map/`](map/)
