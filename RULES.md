# 📐 Knowledge-Base — Rules, Constraints & Evaluation Rubric

> **Purpose:** This document defines every rule and constraint a note in this vault must satisfy.  
> It is designed so an AI model can read any note, apply these criteria, and produce an accuracy score.

---

## HOW TO USE THIS DOCUMENT (for AI Evaluators)

1. Identify the **node type** of the note (experience / concept / pattern / technology / architecture / decision / debugging / thread).
2. Apply **Section 1** (Universal Rules) — these apply to ALL notes regardless of type.
3. Apply the **node-specific section** for that note type.
4. Compute a score using the **Scoring Rubric** in Section 9.
5. Flag any violation using the **Severity Levels** defined below.

### Severity Levels
| Level | Label | Meaning |
|---|---|---|
| CRITICAL | Note cannot be considered part of the system until fixed |
| MAJOR | Note exists but is significantly incomplete or misleading |
| MINOR | Note works but misses a useful detail |
| PASS | Rule fully satisfied |

---

## SECTION 1 — Universal Rules (All Notes)

These rules apply to **every single note** in the vault, regardless of type.

---

### U-01 [CRITICAL] Frontmatter Must Exist
**Rule:** The note must begin with a YAML frontmatter block delimited by `---`.

**Valid example:**
```yaml
---
title: separation of concerns
date: 2026-03-05
status: solid
tags: [concept]
---
```

**Violation:** No frontmatter block present, or frontmatter is malformed YAML.

---

### U-02 [CRITICAL] `title` Field Must Be Filled
**Rule:** `title` must be a non-empty string that describes the note in plain language.

**Violation:** `title:` is blank or missing.

---

### U-03 [CRITICAL] `date` Field Must Be Filled
**Rule:** `date` must be a valid date in `YYYY-MM-DD` format indicating when the note was created.

**Violation:** `date:` is blank, missing, or not a recognizable date format.

---

### U-04 [CRITICAL] `status` Field Must Be a Valid Enum Value
**Rule:** `status` must be exactly one of: `draft` | `growing` | `solid`

**Definitions:**
- `draft` — surfaced by one experience; understanding is shallow
- `growing` — appearing across multiple experiences; understanding deepening
- `solid` — can explain, apply, and recognize it anywhere; no significant gaps remain

**Violation:** `status` is blank, missing, or contains any other value.

---

### U-05 [CRITICAL] `tags` Must Include the Node-Type Tag
**Rule:** The `tags` array must contain the tag corresponding to the note's node type.

| Node Type | Required Tag |
|---|---|
| concept | `concept` |
| pattern | `pattern` |
| technology | `technology` |
| architecture | `architecture` |
| experience | `experience` |
| decision | `decision` |
| debugging | `debugging` |
| thread | `thread` |

**Violation:** No tag, or node-type tag is missing from the array.

---

### U-06 [CRITICAL] At Least One Internal Link Must Exist
**Rule:** Every note must contain at least one `[[wikilink]]` pointing to another note within the vault.

**Rationale:** A note with no links is an island — it is not part of the knowledge graph.

**Violation:** The note body contains zero `[[...]]` wikilinks.

---

### U-07 [CRITICAL] At Least One GitHub URL Must Exist
**Rule:** Every note must contain at least one external GitHub URL (`https://github.com/...`) pointing to real code (a file, a line range, a commit, or a repo).

**Violation:** No GitHub URL anywhere in the note body or frontmatter.
**Exception:** `map/` folder notes (threads and index) are exempt from this rule.

---

### U-08 [MAJOR] The One-Sentence Summary Must Be Filled
**Rule:** The callout block directly after the `# Heading` must contain a plain-language summary sentence. It must NOT contain only the template placeholder text.

**Template placeholder (violation):**
```
> One sentence — what is this concept in plain language?
```

**Valid example:**
```
> Each component in a project has a clear and specific role to do.
```

**Violation:** The callout is empty or still contains the template instruction verbatim.

---

### U-09 [MAJOR] `#gap` Tag Must Be Present When Gaps Exist
**Rule:** If the note's `status` is `draft` OR if the note contains a non-empty "Gaps I Still Have" section, the tag `gap` must be present in `tags`.

**Corollary:** If `status` is `solid`, the `gap` tag must NOT be present and the "Gaps I Still Have" section must be deleted.

**Violation:** `status: draft` but no `gap` tag, OR `status: solid` but `gap` tag still present.

---

### U-10 [MINOR] Template Placeholders Must Not Remain
**Rule:** HTML comment placeholders like `<!-- What challenge does this address... -->` are guides, not content. Sections may remain empty if genuinely not applicable, but template instruction text must not be mixed with real content in a confusing way.

**Violation:** A section contains BOTH the HTML comment instruction AND real content in a messy way, or the HTML comment is the only "content" where real content was expected.

---

### U-11 [MINOR] The `Connections` Section Must Be Filled
**Rule:** The `## Connections` section must have at least one populated field (not all blank).

**Violation:** Every field in Connections is empty (all blank lines after the field labels).

---

## SECTION 2 — Concept Notes (`concept/`)

In addition to all Universal Rules, concept notes must satisfy:

---

### C-01 [CRITICAL] `Surfaced by` Must Reference at Least One Experience
**Rule:** The `Surfaced by:` field must contain a `[[experience/...]]` wikilink — the first experience that revealed this concept.

**Violation:** `Surfaced by:` is blank or contains only the HTML comment placeholder.

---

### C-02 [MAJOR] `Core Idea` Section Must Be Filled
**Rule:** The `## Core Idea` section must explain the "why" — what problem this concept exists to solve. Must be at least one complete sentence.

**Violation:** Section is empty or contains only the HTML comment.

---

### C-03 [MAJOR] `Mental Model` Section Must Be Filled
**Rule:** Must contain a personal analogy or image that makes the concept click. Generic descriptions do not count — it must be a concrete real-world comparison.

**Violation:** Empty, or it only restates the Core Idea without providing a different lens.

---

### C-04 [MAJOR] `Key Properties` Must List 3 to 5 Items
**Rule:** Between 3 and 5 bullet points capturing essential properties of the concept.

**Violation:** Fewer than 3 bullets, or more than 5 without clear justification.

---

### C-05 [MAJOR] `Common Misconception` Must Be Filled
**Rule:** Must describe a specific, real misconception — either the developer's own past mistake or a widely held incorrect belief about this concept.

**Violation:** Empty, or it states a tautology ("this concept is not simple") rather than a real misconception.

---

### C-06 [MINOR] `Gaps I Still Have` Section Rule
- If `status: draft` or `status: growing`: Section must exist and contain at least one honest gap item.
- If `status: solid`: Section must be deleted entirely (not just left blank).

**Violation:** Draft note with empty Gaps section, or solid note that still has the section.

---

### C-07 [MINOR] `Expressed by pattern` Must Link to a Real Pattern Note
**Rule:** If filled, the value must be a `[[pattern/...]]` wikilink pointing to an existing file.

**Violation:** Link points to a non-existent note, or text is present but no wikilink syntax used.

---

### C-08 [MINOR] `Implemented by technology` Must Link to a Real Technology Note
**Rule:** If filled, the value must be a `[[technology/...]]` wikilink pointing to an existing file.

**Violation:** Same as C-07.

---

### C-09 [MINOR] `reviewed` Date Must Be Updated
**Rule:** Every time the note is revisited and deepened, the `reviewed:` frontmatter field must be updated to the most recent visit date.

**Violation:** `reviewed:` is blank on a note with `status: growing` or `status: solid`.

---

## SECTION 3 — Pattern Notes (`pattern/`)

---

### P-01 [CRITICAL] `Applied in experience` Must Reference at Least One Experience
**Rule:** The `Applied in experience:` field must contain a `[[experience/...]]` wikilink. Patterns with no real experience reference are theoretical — they should be tagged `theoretical` and flagged for verification.

**Violation:** Field is blank AND note is NOT tagged `theoretical`.

---

### P-02 [CRITICAL] `Code Reference` Table Must Have at Least One Link
**Rule:** The `## Code Reference` table must contain a GitHub URL pointing to real code where this pattern was applied.

**Violation:** Table is empty (no rows with content).

---

### P-03 [MAJOR] `The Problem` Section Must Be Filled
**Rule:** Must describe the recurring situation that demands this pattern. Must be specific — not generic.

**Violation:** Empty or contains only the HTML comment.

---

### P-04 [MAJOR] `The Solution` Section Must Be Filled
**Rule:** Must describe the structure of the pattern — who the participants are and what their roles are.

**Violation:** Empty or contains only the HTML comment.

---

### P-05 [MAJOR] `When To Use It` Must Be Filled
**Rule:** Must list at least one concrete condition under which this pattern is appropriate.

**Violation:** Empty.

---

### P-06 [MAJOR] `When To Avoid It` Must Be Filled
**Rule:** Must list at least one condition under which this pattern should NOT be used, and ideally name a simpler alternative.

**Violation:** Empty.

---

### P-07 [MINOR] `Was I applying it knowingly or did I discover it?` Must Be Answered
**Rule:** Must explicitly say either `knowingly` or `discovered`.

**Rationale:** This distinction tracks the difference between deliberate application of knowledge vs. accidental discovery — essential to the system's meta-learning.

**Violation:** Field is blank.

---

### P-08 [MINOR] `Related concept` Must Be Linked
**Rule:** Must reference the abstract concept this pattern expresses via `[[concept/...]]`.

**Violation:** Field is blank.

---

## SECTION 4 — Experience Notes (`experience/`)

---

### E-01 [CRITICAL] `type` Field Must Be Filled
**Rule:** `type` must be exactly one of: `general` | `sub`
- `general` — a top-level project or initiative
- `sub` — a specific feature, component, or sub-task within a parent experience

**Violation:** Field is blank or contains any other value.

---

### E-02 [CRITICAL] `parent` Must Be Set When `type: sub`
**Rule:** If `type: sub`, the `parent:` field must contain a `[[experience/...]]` wikilink to the parent experience.

**Violation:** `type: sub` but `parent:` is blank.

---

### E-03 [CRITICAL] `repo` Field Must Contain a GitHub Repo URL
**Rule:** The `repo:` frontmatter field must contain the full GitHub URL of the repository this experience belongs to.

**Violation:** Field is blank.

---

### E-04 [CRITICAL] `Code Reference` Table Must Have at Least One Entry
**Rule:** The `## Code Reference` table must contain at least one GitHub URL pointing to a specific file, line range, or commit in the repo.

**Violation:** Table has no rows with content.

---

### E-05 [MAJOR] `What I Was Building` Section Must Be Filled
**Rule:** Must describe the goal and problem being solved. At minimum one complete sentence.

**Violation:** Empty or contains only the HTML comment.

---

### E-06 [MAJOR] `What I Did` Section Must Be Filled
**Rule:** Must describe the approach taken. Key decisions should be noted here (with links to decision notes). Full detail is not required — the code reference handles that.

**Violation:** Empty or contains only the HTML comment.

---

### E-07 [MAJOR] `What I Learned` Section Must Be Filled
**Rule:** Must state the honest takeaway — what shifted in understanding as a result of this experience.

**Violation:** Empty or contains only the HTML comment.

---

### E-08 [MAJOR] `Concepts I Applied` Must List Applied Concepts
**Rule:** Must name at least one concept that was deliberately applied in this experience, with a `[[concept/...]]` link.

**Violation:** Section is blank (every experience applies at least one concept).

---

### E-09 [MAJOR] `Leads To` or `Came From` Must Have At Least One Entry
**Rule:** An experience cannot exist in isolation. Either `Leads To` or `Came From` (or both) must contain a `[[experience/...]]` link showing where it sits in the narrative chain.

**Exception:** The very first experience in the chain may have `Came From` blank, but `Leads To` must be filled.

**Violation:** Both `Leads To` and `Came From` are blank.

---

### E-10 [MINOR] `Concepts I Discovered` Should List Discovered Concepts With Corresponding Notes
**Rule:** If the experience produced new or fuzzy understanding of any concept, those concepts must be listed here. Each listed concept must have a corresponding `draft` concept note with `#gap` tag.

**Violation:** Concepts are referenced here but no corresponding concept note exists in `concept/`.

---

### E-11 [MINOR] `Other Nodes — Technology Used` Must Be Linked
**Rule:** The `Technology used:` field must list all technologies actually used in the experience, each with a `[[technology/...]]` wikilink.

**Violation:** Technologies mentioned in prose but not formally linked in this field.

---

## SECTION 5 — Decision Notes (`decision/`)

---

### D-01 [CRITICAL] Two Real Options Must Exist in the Table
**Rule:** The `## The Real Options` table must contain exactly two or more rows with distinct, non-trivial alternatives. A decision note only justifies its existence if there were genuine competing choices.

**Violation:** Only one option in the table, or both options are trivially different (not real alternatives).

---

### D-02 [CRITICAL] `What I Chose` Must Be Stated Clearly
**Rule:** Must explicitly name the option selected. Must not be vague.

**Valid:** "I chose layer-based architecture (routes to controllers to services to DB)."
**Violation:** "I chose the better one" or blank.

---

### D-03 [CRITICAL] `Why` Section Must Give Honest Reasoning
**Rule:** Must explain what tipped the balance. Not generic ("it was better") — must name specific factors, constraints, or reasoning.

**Violation:** Generic reasoning or empty.

---

### D-04 [MAJOR] `What I Was Uncertain About` Must Be Filled
**Rule:** Must honestly state what was not fully known at the time of deciding. This is the most valuable field — it captures the epistemic state at decision time.

**Violation:** Empty or claims perfect certainty ("I was certain about everything").

---

### D-05 [MAJOR] `Code Reference` Must Link to the Decision in Code
**Rule:** Must contain a GitHub link to a commit, file, or directory where this decision is visible in the actual code.

**Violation:** Table is empty.

---

### D-06 [MAJOR] `Made during experience` Must Be Linked
**Rule:** Must reference the `[[experience/...]]` note where this decision was made.

**Violation:** Field is blank.

---

### D-07 [MINOR] `How It Turned Out` Should Be Filled Retrospectively
**Rule:** This field starts blank by design. Once sufficient time has passed and outcomes are observable, it must be filled.

**Evaluation signal:** If a decision note is `status: solid` but `How It Turned Out` is blank — this is a violation.

**Violation:** `status: solid` but `How It Turned Out` is not filled.

---

### D-08 [MINOR] `Concept confidence at time of decision` Must Be Set
**Rule:** Must be exactly `known` or `fuzzy`.
- `known` — the concept this decision was based on was well understood at the time
- `fuzzy` — the concept was partially or poorly understood at decision time

**Violation:** Field is blank or contains any other value.

---

## SECTION 6 — Architecture Notes (`architecture/`)

---

### A-01 [CRITICAL] `The Problem At This Scale` Must Be Filled
**Rule:** Must describe what challenge this architecture addresses that smaller solutions cannot. Must be specific.

**Violation:** Empty or still contains HTML comment placeholder only.

---

### A-02 [MAJOR] `The Structure` Must Be Filled
**Rule:** Must describe how the pieces are arranged — at minimum a list of layers or components, or a simple description.

**Violation:** Empty.

---

### A-03 [MAJOR] `Key Trade-offs` Table Must Have At Least One Row
**Rule:** The Gain/Cost table must have at least one populated row. Architecture is defined by its trade-offs.

**Violation:** Table is empty.

---

### A-04 [MAJOR] `When It Makes Sense` and `When It Doesn't` Must Both Be Filled
**Rule:** Both sections must have at least one concrete condition.

**Violation:** Either section is blank.

---

### A-05 [MAJOR] `Emerged from experience` Must Be Linked
**Rule:** Must reference a `[[experience/...]]` link. Purely theoretical architecture notes without real application are not accepted.

**Violation:** Field is blank.

---

### A-06 [MINOR] `Built on concept` Must Be Linked
**Rule:** Must reference the abstract concept this architecture expresses at scale via `[[concept/...]]`.

**Violation:** Field is blank.

---

### A-07 [MINOR] `Composed of patterns` Must Be Linked
**Rule:** Must reference at least one `[[pattern/...]]` link that composes this architecture.

**Violation:** Field is blank.

---

## SECTION 7 — Technology Notes (`technology/`)

---

### T-01 [CRITICAL] `since` Field Must Be Set
**Rule:** Must contain the year the developer first used this technology.

**Violation:** Blank.

---

### T-02 [MAJOR] `What It Is` Must Be Filled
**Rule:** Must describe the tool and what problem it solves. Must be from the developer's own understanding, not copy-paste from documentation.

**Violation:** Empty, or it reads like a marketing blurb without personal understanding.

---

### T-03 [MAJOR] `What Concept Does It Implement` Must Be Filled
**Rule:** Every tool implements an abstract concept. This field must link to `[[concept/...]]`.

**Rationale:** Tools are expressions of ideas — identifying the concept makes the tool portable across stacks.

**Violation:** Empty.

---

### T-04 [MAJOR] `How I Actually Used It` Must Be Filled
**Rule:** Must describe real usage — not what the docs say. What was actually done with this tool? This must differ from `What It Is`.

**Violation:** Empty, or it duplicates `What It Is`.

---

### T-05 [MAJOR] `Key Behaviours To Remember` Must Have At Least One Entry
**Rule:** Must list non-obvious behaviors — gotchas, quirks, or surprises that aren't in the happy-path docs.

**Violation:** Empty.

---

### T-06 [MAJOR] `Progress Timeline` Must Have At Least One Row
**Rule:** The timeline table tracks growth over time. Must have at least one row with: When, Experience (wikilink), What I Could Do, and Proof (GitHub link).

**Violation:** Table has no populated rows.

---

### T-07 [MINOR] `First used in experience` Must Be Linked
**Rule:** Must reference a `[[experience/...]]` wikilink for the first real use.

**Violation:** Blank.

---

### T-08 [MINOR] `What I Still Don't Fully Understand` Section Rule
- If `status: draft` or `status: growing`: Section must exist with at least one honest gap.
- If `status: solid`: Section must be deleted.

**Violation:** Solid note with the gaps section still present.

---

### T-09 [MINOR] `reviewed` Date Must Be Updated Regularly
**Rule:** The `reviewed:` frontmatter field must be updated every time the note is revisited and deepened.

**Violation:** Blank on a note with `status: growing` or `status: solid`.

---

## SECTION 8 — Debugging Notes (`debugging/`)

---

### B-01 [CRITICAL] `Root Cause` Must Be Specific
**Rule:** Must state exactly what was wrong — not "something with the types" but the precise technical cause.

**Violation:** Vague, generic, or empty.

---

### B-02 [CRITICAL] The Key Question Must Be Answered
**Rule:** One of these two checkboxes must be checked:
- `[x] A gap in a concept I thought I knew`
- `[x] A concept I didn't know existed at all`

**Rationale:** This distinction determines whether to deepen an existing concept note or create a new one.

**Violation:** Both boxes unchecked.

---

### B-03 [CRITICAL] `What To Do With This` Must Be Filled
**Rule:** Based on the answered checkbox, must either reference an existing concept note to update OR name a new concept note to create.

**Violation:** Empty.

---

### B-04 [MAJOR] `Symptoms` Must Be Filled
**Rule:** Must describe what the bug looked like from the outside — how it was noticed.

**Violation:** Empty.

---

### B-05 [MAJOR] `The Fix` Must Include a Commit Link
**Rule:** Must describe what was changed AND include a GitHub commit link showing the fix.

**Violation:** No commit link.

---

### B-06 [MAJOR] `Why It Was Hard To Find` Must Be Filled
**Rule:** Must explain what made the bug non-obvious — what red herrings or wrong assumptions made debugging harder.

**Violation:** Empty.

---

### B-07 [MINOR] `Happened during experience` Must Be Linked
**Rule:** Must reference the `[[experience/...]]` note where this bug occurred.

**Violation:** Blank.

---

## SECTION 9 — Scoring Rubric

Use this rubric to compute a quality score for any note.

### Step 1: Count Rule Violations by Severity

| Severity | Points Deducted per Violation |
|---|---|
| CRITICAL | -20 |
| MAJOR | -10 |
| MINOR | -5 |

### Step 2: Start at 100

```
Score = 100 - (CRITICAL_count x 20) - (MAJOR_count x 10) - (MINOR_count x 5)
```

Minimum score is 0.

### Step 3: Apply Status Consistency Check

| Declared Status | Expected Score Range |
|---|---|
| `draft` | 40–65 (gaps are expected and acceptable) |
| `growing` | 60–80 (most fields filled; some gaps remain) |
| `solid` | 80–100 (no critical or major violations; all gap sections deleted) |

If a note's computed score does not match its declared status range, add -10 (MAJOR — status mismatch).

### Step 4: Classify the Note

| Score | Classification |
|---|---|
| 90–100 | EXCELLENT — Ready for use; deeply connected |
| 70–89 | GOOD — Usable but needs one or two improvements |
| 50–69 | INCOMPLETE — Core content there but significant gaps |
| 30–49 | SKELETON — Structure exists, most content missing |
| 0–29 | ISLAND — Not yet part of the system; do not use for inference |

---

## SECTION 10 — Link Integrity Rules

These rules govern all wikilinks and GitHub URLs in any note.

---

### L-01 [CRITICAL] Wikilinks Must Point to Existing Notes
**Rule:** Every `[[wikilink]]` must correspond to an actual `.md` file in the vault. Broken links (pointing to notes that don't exist) are integrity violations.

**Evaluation method:** Resolve each `[[...]]` against the directory structure and verify the file exists.

---

### L-02 [CRITICAL] GitHub URLs Must Be Properly Formed
**Rule:** All GitHub URLs must:
- Begin with `https://github.com/`
- Reference an actual file, directory, line range, or commit (not just the profile)
- Use a permalink (commit SHA) when pointing to specific lines — not the branch reference which can change

**Violation:** URL is malformed, or it links to the repo root when a specific location is intended.

---

### L-03 [MAJOR] Line-Range Links Must Be Stable Using Commit SHA
**Rule:** Links to specific lines of code must use a commit SHA in the URL, not `blob/main/...` which will drift as the file changes.

**Valid:** `https://github.com/user/repo/blob/a1b2c3d4.../file.ts#L10-L20`
**Violation:** `https://github.com/user/repo/blob/main/file.ts#L10-L20`

---

### L-04 [MINOR] Connections Should Be Bidirectional Where Possible
**Rule:** If Note A links to Note B in its Connections section, Note B should ideally link back to Note A. Unidirectional links weaken the graph.

**Evaluation:** Check if the linked note contains a reciprocal link. Flag missing reciprocals as MINOR.

---

## SECTION 11 — Lifecycle Consistency Rules

---

### LC-01 [CRITICAL] `status: solid` Notes Must Have No Empty Mandatory Sections
**Rule:** A note marked `solid` must have ALL mandatory sections filled. If any mandatory section is empty, the note must be downgraded to `growing` or `draft`.

---

### LC-02 [MAJOR] `status: growing` Must Reference More Than One Experience
**Rule:** A concept or pattern marked `growing` should appear in the `Reinforced by` or `Applied in experience` fields of more than one experience note.

**Rationale:** "growing" means it is appearing across multiple experiences. If it only shows up in one, it should remain `draft`.

---

### LC-03 [MAJOR] `gap` Tag Must Be Consistent With Status and Content
**Rule:**
- `status: draft` → `gap` tag REQUIRED
- `status: growing` → `gap` tag REQUIRED if there are still knowledge gaps listed
- `status: solid` → `gap` tag FORBIDDEN

---

### LC-04 [MINOR] `Gaps I Still Have` Must Not Exist in `solid` Notes
**Rule:** This section must be completely removed (not just emptied) when the note reaches `solid` status.

**Violation:** Section header still present with blank or placeholder content in a `solid` note.

---

## SECTION 12 — Quick Checklist for Manual Review

Use this when reviewing a note before saving:

```
UNIVERSAL (all notes)
[ ] Frontmatter block exists and is valid YAML
[ ] title, date, status are all filled
[ ] status is one of: draft | growing | solid
[ ] tags includes the correct node-type tag
[ ] At least one [[wikilink]] exists
[ ] At least one https://github.com/... URL exists (except map/ notes)
[ ] One-sentence summary is filled (not template placeholder)
[ ] gap tag is present if status is draft or growing with gaps
[ ] gap tag is ABSENT if status is solid
[ ] Connections section has at least one populated field

CONTENT QUALITY
[ ] Every section required for this note type is filled
[ ] No section still contains ONLY the HTML comment instruction
[ ] Gaps I Still Have section deleted if status is solid
[ ] reviewed date is set if status is growing or solid

LINK INTEGRITY
[ ] All [[wikilinks]] resolve to existing files
[ ] All GitHub URLs are properly formed
[ ] Line-range GitHub links use commit SHA (not branch name)

LIFECYCLE
[ ] Declared status matches actual completeness level
[ ] growing notes appear in more than one experience
[ ] solid notes have zero empty mandatory sections
```

---

## SECTION 13 — Evaluation Output Format (for AI Models)

When evaluating a note, output the result in this exact structured format:

```
NOTE EVALUATION REPORT
======================
File: [path/to/note.md]
Node Type: [concept | pattern | experience | decision | architecture | technology | debugging | thread]
Declared Status: [draft | growing | solid]

VIOLATIONS FOUND:
  CRITICAL (-20 each):
    - [Rule ID] [Description of the specific violation found]
  MAJOR (-10 each):
    - [Rule ID] [Description of the specific violation found]
  MINOR (-5 each):
    - [Rule ID] [Description of the specific violation found]

STATUS CONSISTENCY: [MATCH | MISMATCH (-10)]
  Note: [explain why if MISMATCH]

COMPUTED SCORE: [0-100]
CLASSIFICATION: [EXCELLENT | GOOD | INCOMPLETE | SKELETON | ISLAND]

WHAT IS WORKING WELL:
  - [Specific strengths of this note]

TOP PRIORITY FIXES:
  1. [Most critical fix needed — specific and actionable]
  2. [Second most critical fix]
  3. [Third most critical fix]

MISSING LINKED NOTES (if any):
  - [[note/that/does/not/exist]] — referenced but file not found
```
