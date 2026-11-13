# Chat History - ace-run (research.4j.gem)

- **TIMESTAMP:** 2026-11-13 09:26:00 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4j.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261113_091235.md`

## Prompt

%id(gem, clan=research.4j)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4j.cdx`, `research.4j.cld`, `research.4j.grk`, `research.4j.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering sub-projects in their own H2 section (with possible H3
sub-sections?) instead of as prj task sub-bullets.

- See how we already do this for record notes and notebooks for context and inspiration.
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

# Research Report: Rendering Sub-projects in Dedicated H2 Sections

**Author:** Researcher `gem` (5-researcher swarm)  
**File Location:** [`sase/repos/research/202611/subproject_h2_section_rendering__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/subproject_h2_section_rendering__gem.md)  
**Durable Artifact:** `research:202611/subproject_h2_section_rendering__gem.md` (`file:explicit:af1ebff380e5e5b04a7fad5a`)

---

## 1. Executive Summary & Verdict

Transitioning sub-project rendering from an indented sub-bullet under the `^prj` lifecycle task into a dedicated `## Sub-projects` H2 section with a machine-managed callout (`> [!subprojects]`) is **strongly recommended**.

### Why the current design fails:
1. **Conflates GTD Task vs. Entity Hierarchy:** The `^prj` task is an operational execution checkbox ("Ship project outcome!"). Sub-projects are full-fledged *project notes* with their own task backlogs, notebooks, and albums. Indenting major project notes beneath a single task checkbox misrepresents vault structure.
2. **Horizontal Overflow & Visual Clutter:** A parent project with dependencies (`⛓️ DEPENDS ON:`), blocks (`🧱 BLOCKS:`), cancellation logs (`❌ CANCEL LOG`), and 4+ sub-projects creates a messy block where sub-projects wrap awkwardly across multiple lines inside a single bullet.
3. **Information Starvation:** The sub-bullet format restricts display to bare file stems with emoji decorations (`🗓️`, `✅`, `❌`), omitting human display titles, descriptive summaries, schedules, or sub-sub-project hierarchy.
4. **Vault Inconsistency:** Bob has standardized on the pure, declarative `host_catalog` engine for `## Notebooks` (`> [!notebooks]`) and `## Albums` (`> [!albums]`). Sub-projects currently stand out as an ad-hoc legacy mechanism.

---

## 2. Critique of the Proposal & Key Adjustments

While the move to an H2 section is an outstanding idea, our investigation identified two critical hazards in a naive implementation that require adjustments to the requirements:

### Adjustment 1: Reject Physical Markdown H3 Headings; Adopt Callout-Internal Grouping (The Records Pattern)
* **The Hazard of Markdown H3 Headings:**  
  If Bob generates physical Markdown H3 headings (`### Active`, `### Scheduled`, `### Completed`) in the document body:
  - **Document Outline Pollution:** Markdown headings appear in Obsidian's Table of Contents / Outline pane. Machine status categories clutter the user's permanent document outline.
  - **Violation of `host_catalog` Ownership:** In Bob's architecture, *the user owns the document headings and structure; Bob owns only the callout block*. Generating headings outside the callout creates ambiguity over who owns surrounding text.
  - **Empty Section Churn:** When all sub-projects in a category finish, deleting or recreating H3 headings leads to fragile text surgery.
* **The Superior Alternative (The Records Pattern):**  
  Follow `src/native/albums/index.rs`: keep a single H2 heading `## Sub-projects` and perform all grouping *inside* the `> [!subprojects]` callout using bold list-item headers (e.g., `> - **Active** · 2`). If a project has only 1–3 sub-projects, render them flat without headers to avoid visual bureaucracy.

### Adjustment 2: Never Write Dynamic Task Counts into Markdown
* In `docs/notebooks.md` and `docs/records.md`, Bob adheres to a strict invariant: *counts, colors, and ages are drawn live by client plugins, never written to disk*.
* If Bob wrote "3 open tasks" into the parent note's catalog, checking off any task in a child sub-project would dirty the parent project file, creating cascading disk and git churn across the vault.
* Write only stable metadata: wikilink, display title, frontmatter summary, and schedule badge. Let `bob-plugins` inject live task counts and progress badges into the Obsidian DOM.

### Adjustment 3: Natural Extension to Area Notes (`## Projects`)
* Area notes (`work.md`, `dev.md`) parent top-level root projects, but currently have no project catalog.
* By building a unified project catalog engine, **Area Notes** naturally receive `## Projects` (`> [!projects]`), while **Project Notes** receive `## Sub-projects` (`> [!subprojects]`), completing the entire hierarchy of the vault.

---

## 3. Recommended Design: The Sub-projects Catalog

### Visual Appearance in Note

#### Flat Layout (1–3 Sub-projects)
```markdown
## Sub-projects

> [!subprojects] 2 sub-projects · 2 active
>
> - 🧩 **[[frontend_v2|Frontend Redesign]]** — Modern UI overhaul with design tokens.
> - 🧩 **[[api_v2|Backend API]]** — GraphQL server endpoints.
```

#### Grouped Layout ($>3$ Sub-projects or mixed statuses)
```markdown
## Sub-projects

> [!subprojects] 5 sub-projects · 2 active · 1 scheduled · 2 closed
>
> - **Active** · 2
>   - 🧩 **[[frontend_v2|Frontend Redesign]]** — Modern UI overhaul with design tokens.
>     - 🧩 **[[mobile_ui|Mobile Responsive Views]]** — Mobile viewport fixes.
>   - 🧩 **[[api_v2|Backend API]]** — GraphQL server endpoints.
> - **Scheduled** · 1
>   - 🗓️ **[[analytics_pipe|Analytics Pipeline]]** [scheduled:: 2026-12-01] — Event stream ingestion.
> - **Completed** · 2
>   - ~~[[auth_migration|Auth Migration]]~~ ✅ — Completed [closed:: 2026-11-01]
>   - ~~[[legacy_db|Database Decommission]]~~ ❌
```

---

## 4. Technical Architecture & Ecosystem Integration

### 4.1 Integration with `host_catalog`
Define `SUBPROJECTS` in `src/native/host_catalog/region.rs`:
```rust
pub(crate) const SUBPROJECTS: RegionSpec<'static> = RegionSpec {
    callout: "subprojects",
    heading: "Sub-projects",
    head_title: None, // Dynamic tally in callout head
    placement: Placement::BeforeFirstTasks,
    legacy: None,
    strict_bare: true,
};
```
- First write places `## Sub-projects` before `## Notebooks` and `## Tasks`.
- On later runs, Bob respects the author's placement if moved.
- Byte-span updates preserve line endings (CRLF/LF), UTF-8 BOM, and all surrounding text.

### 4.2 Preserving Gesture Performance in `surface.rs`
`project_surface` (`src/native/projects/surface.rs`) runs during latency-critical editor gestures (e.g. task completion, pull-in) and reads sub-projects from the staged note text to evaluate `EMPTY(N)`:
- **Primary Read Path:** Inspects `> [!subprojects]` in the staged file. Unstruck entries count as open; closing child stem is discounted.
- **Fallback Read Path:** Gracefully falls back to the legacy `- 🧩 **Sub-projects:**` sub-bullet under `^prj` if no callout is present.

### 4.3 Plugin Updates in `bob-plugins`
- `task-status-cycler`: Update `089-successor-project.js` to recognize open sub-projects inside `[!subprojects]` callouts.
- `bob-ledger-tools`: Update `145-relation-index-model.js` so that `[!subprojects]` callouts are treated as structural entity blocks (ignoring inner links during relation indexing).

---

## 5. Artifact & Report Registration

The full research report has been committed to the research sidecar repository and registered as a durable artifact:

```bash
sase artifact create \
  -p "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/subproject_h2_section_rendering__gem.md" \
  -l "research:202611/subproject_h2_section_rendering__gem.md"
```

* **Artifact ID:** `explicit:af1ebff380e5e5b04a7fad5a`
* **Artifact Reference:** `file:explicit:af1ebff380e5e5b04a7fad5a`
* **Local Workspace File:** [`subproject_h2_section_rendering__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_23/sase/repos/research/202611/subproject_h2_section_rendering__gem.md)
