# Chat History - ace-run (research.29.gem)

- **TIMESTAMP:** 2026-10-21 08:49:23 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.29.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261021_083251.md`

## Prompt

%id(gem, clan=research.29)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.29.cdx`, `research.29.cld`, `research.29.grk`, `research.29.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We recently added support for link relations, which are currently always directed. I
would like to start making any relation that does not have a description an undirected
relation instead.

- I was thinking we should just show `links` instead of `links to` and `links from` for
  these.
- Any relation with a description would then become a directed relation (update the
  glossary term and add new ones for "directed" and "undirected" relations).
- Linking another note to the current note (using the `~~` syntax, for example) then
  only makes sense if a relation description is provided (otherwise, it is the same as
  linking to a task directly using `~`, for example).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: Undirected Task Relations and Directional Symmetry

**Researcher:** `research.29.gem` (Swarm Gem)  
**Date:** October 2026  
**Artifact Reference:** `file:explicit:0f487e76d810e0ba31385b68`  
**Report Path:** [`undirected_task_relations__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/undirected_task_relations__gem.md)  
**Artifact Label:** `research:202610/undirected_task_relations__gem.md`

---

## Executive Summary & Assessment

You proposed transitioning any task relation without a description into an **undirected relation**, displaying `links` instead of `links to` / `links from` for these, reserving directed relations for labelled links, and re-evaluating the role of the `~~` draft syntax.

### Is this a good idea?
**Yes, it is an outstanding ergonomic and conceptual improvement.** 

In personal knowledge management and GTD workflows, general association between two tasks ("Task A touches the same subsystem as Task B") is inherently symmetric. Forcing an arbitrary direction on unlabelled relations introduces decision friction during capture ("Should I link A to B, or B to A?") and visual fragmentation on task displays (arbitrarily splitting related tasks across `🪢 links to →` and `🪢 linked from` rows based solely on which note was authored first).

However, to make this feature **intuitive, reliable, and beautiful**, several key requirements need careful refinement:

1. **Syntax Refinement for `~~`:** An unlabelled `~~` relation is semantically identical to an unlabelled `~` relation, but mechanically worse because it mutates a remote existing note rather than the draft task. We recommend **strict rejection in CLI capture** (`~~ requires a relation label; use ~ for undirected links`), coupled with **smart guidance in Bob Mac Capture** (auto-focusing the label prompt when `~~` is typed and gracefully falling back to `~` if left empty).
2. **Storage Invariant (Single Source of Truth):** "Undirected" must remain a **semantic and presentation abstraction**, rather than dual-authored storage on disk. Both ends writing `- 🪢 **LINKS:**` would cause distributed merge conflicts and fail on read-only notes (`done/` archives). Retaining the single-authored `LINKS:` line with an automated `LINKED FROM:` projection ensures zero-conflict, idempotent reconciliation.
3. **Visual Beauty (The Single-Row Merge):** For unlabelled relations, omit all directional arrows (`→`). If a task has multiple unlabelled connections (regardless of which note physically hosts the `LINKS:` line), **merge them into a single, cohesive row: `🪢 links (○ Task B) (○ Task C)`**.

---

## 1. Critique of the Proposal & Requirement Adjustments

### 1.1 The Semantic Distinction: Undirected vs. Directed

| Dimension | Undirected Relation (Unlabelled) | Directed Relation (Labelled) |
| :--- | :--- | :--- |
| **Concept** | Associative, mutual relevance, peer context | Asymmetric, causal, chronological, hierarchical |
| **Examples** | General relation, shared subsystem | `follow-up of`, `superseded by`, `split from` |
| **Mental Model** | "Tasks A and B are linked." | "Task A is a follow-up of Task B." |
| **Visual Header** | `🪢 links` (no arrow) | `🪢 links to` / `🪢 linked from` (with arrows/inverse) |
| **Edge Identity** | Unordered set $\{u, v\}$ | Ordered triple $(u, v, \text{label})$ |

Under the current directed model, if Task A links to B without a label, and Task C links to A without a label, Task A renders:
```text
🪢 links to → (○ Task B)
🪢 linked from (○ Task C)
```
To a human, both B and C are simply "related tasks." Fragmenting them across two lines with an arrow on one and no arrow on the other is distracting clutter. With undirected relations, they merge cleanly into:
```text
🪢 links  (○ Task B)  (○ Task C)
```

### 1.2 Syntax Critique: The Role of `~~`

Your observation is completely accurate:
> *"Linking another note to the current note (using the `~~` syntax, for example) then only makes sense if a relation description is provided (otherwise, it is the same as linking to a task directly using `~`, for example)."*

If an edge is undirected, linking $A \sim B$ produces the exact same mutual link as $B \sim A$. However:
- `~target` writes the link directly to the newly drafted task's `LINKS:` line (local mutation).
- `~~target` writes to the existing target note's `LINKS:` line (remote mutation).

Allowing `~~` without a description invites accidental remote note edits for no semantic reason.

#### Recommended Requirement Adjustments:
1. **In CLI (`bob capture`): Refuse unlabelled `~~` with a teaching error:**
   ```text
   error: `~~` creates a directed incoming relation and requires a label (e.g. `~~note:id|"label"`).
   For an undirected link, use `~note:id`.
   ```
2. **In Mac Capture (Interactive Panel): Auto-focus label prompt:**
   - Typing `~` enters undirected link mode.
   - Typing `~~` immediately opens the Relation Card with the label field focused.
   - If the user leaves the label blank and presses Enter, Mac Capture automatically coerces the draft back to `~` (undirected link).

---

## 2. Storage Architecture & Invariants

We evaluated whether to change the underlying Markdown storage format (e.g. introducing a new `🪢 **RELATED:**` line or writing `LINKS:` on both notes). 

**Conclusion: Retain Model C (Single-Source Storage with Symmetric Projection).**

```text
Task S (Source Note):      - 🪢 **LINKS:** [[T#^t]]
Task T (Target Note):      - 🪢 **LINKED FROM:** [[S#^s]]
```

- **Why?** Reconcile Guarantee 1 (`docs/task-relations.md` LR11) requires single-source determinism: deleting all `LINKED FROM:` lines and running reconcile must recreate byte-identical files. If both sides authored `LINKS:`, deleting an edge from one note would cause reconcile to resurrect it from the other. Furthermore, targets in read-only notes (`done/` archives) cannot be authored.
- **How it works:** On disk, `LINKS:` and `LINKED FROM:` remain. In memory and in UI rendering, any relation entry where `label.is_none()` is recognized as an **undirected relation**, rendered symmetrically on both ends under `🪢 links`.
- **Symmetric Deletion:** Clicking `×` on either task's chip resolves the underlying edge to $S$'s `LINKS:` line and removes it cleanly.

---

## 3. UI & Interaction Design: Making It Beautiful

### 3.1 Obsidian Relation Chips (`bob-ledger-tools`)

The relation chip rendering logic is restructured into three clean tiers:

1. **Row 1: Undirected Relations (`🪢 links`)**
   - **Prefix:** `🪢 links` (bold knot glyph `🪢`, bold lowercase `links`).
   - **No Arrow:** Omits `→`. The absence of an arrow immediately communicates symmetry.
   - **Aggregated:** Merges all unlabelled links (both authored on this task and mirrored from other tasks) into one row.
   - **Display:**
     ```text
     🪢 links  (○ Task B)  (○ Task C)
     ```
2. **Row 2: Outgoing Directed Relations (`🪢 links to`)**
   - **Prefix:** `🪢 links to`
   - **Display:** `‹label pill› → (○ Target Task)`
3. **Row 3: Incoming Directed Relations (`🪢 linked from`)**
   - **Prefix:** `🪢 linked from`
   - **Display:** `‹inverse label pill› (○ Source Task)` or `(○ Source Task) · ‹label pill› → this`

### 3.2 Obsidian Task Card (`bob-navigation-hotkeys`)

On the Task Card (`Ctrl+Shift+P`):
- **Key `l` becomes `Links` (The Primary Associative Action):**
  - Pressing `l` opens the task picker.
  - Pressing `Enter`: creates an **undirected relation** (one keystroke, handles 90% of connections).
  - Pressing `Shift+Enter`: prompts for a label to create an **outgoing directed relation**.
- **Key `⇧L` becomes `Linked from (directed)`:**
  - Dedicated exclusively to creating incoming directed relations.
  - Prompts immediately for a label. Empty labels are rejected with an inline notice: `Directed relations require a label · use 'l' for undirected links.`
- **Clearing Relations (`Ctrl+D`):**
  - Pressing `Ctrl+D` on the `Links` row clears all undirected relations for the task, regardless of which task physically hosts the `LINKS:` line on disk.

---

## 4. Glossary Specifications

The SASE Memory strand and documentation terms should be updated as follows:

### 4.1 Updated: `Task Relation`
```markdown
# Task Relation
aka relation, LINKS line, LINKED FROM line

An inert link between two tasks, either **undirected** (an unlabelled association
asserting mutual relevance) or **directed** (a labelled relationship describing a
specific semantic connection). It is authored on a task's 🪢 **LINKS:** line and
mirrored on the counterpart task's generated 🪢 **LINKED FROM:** line. Add one
with Capture `~` / `~~` or the Task Card `l` / `⇧L` gestures. A relation is
distinct from a Pomodoro [[task-link]]: it never blocks a task, counts as a
Pomodoro Task Link, or changes its status, schedule, priority, or freshness.
```

### 4.2 New: `Undirected Relation`
```markdown
# Undirected Relation
aka undirected task relation, unlabelled relation, links

A symmetric, unlabelled [[task-relation]] between two tasks asserting mutual
relevance without hierarchy or direction. It is authored using Capture `~note:id`
or the Task Card `l` gesture without a label. In the UI (chips and task cards), an
undirected relation is displayed symmetrically on both tasks under 🪢 **links**
without directional arrows, unifying all unlabelled connections into a single
row. Deleting or clearing the relation from either task removes the edge.
```

### 4.3 New: `Directed Relation`
```markdown
# Directed Relation
aka directed task relation, labelled relation, links to, linked from

An asymmetric [[task-relation]] qualified by an authored label describing the
connection from the source task to the target task (such as `follow-up of`,
`superseded by`, or `split from`). It is authored using Capture `~note:id|"label"`
(outgoing) or `~~note:id|"label"` (incoming), or via Task Card `Shift+Enter`. In
the UI, it is displayed on the source task as 🪢 **links to** (`label → (target)`)
and on the target task as 🪢 **linked from** (`inverse (source)`). A directed
relation requires a non-empty label of 1–40 characters; unlabelled relations are
always [[undirected-relation]]s.
```

---

## 5. Conformance Test Vectors to Add to `docs/task-relations.md`

- **LP19:** `Fix bug ~~work:foo` $\to$ Refused: `~~ requires a relation label; use ~ for undirected links`
- **LP20:** `Fix bug ~~work:foo|"parent"` $\to$ Accepted: `direction: from`, `label: "parent"`
- **LC15:** Task A has `[[B]]` (unlabelled) $\to$ Renders `🪢 links (○ B)` on Task A and `🪢 links (○ A)` on Task B (no arrows).
- **LC16:** Task A has `[[B]]` (unlabelled) and mirror `[[C]]` (unlabelled) $\to$ Renders single row `🪢 links (○ B) (○ C)`.
- **LR25:** Task A has `[[B]]` on `LINKS:`, Task B has `[[A]]` on `LINKS:` $\to$ Reconcile deduplicates into one undirected edge and emits a deduplication notice.

---

## Artifact Registration Verification

The report was created and registered in the durable artifact store:
- **Snapshot Path:** `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261021083257/undirected_task_relations__gem-3667b32750bc.md`
- **Artifact ID:** `explicit:0f487e76d810e0ba31385b68`
- **Artifact Reference:** `file:explicit:0f487e76d810e0ba31385b68`
- **Git Finalization:** Declaration submitted via `sase final submit`.
