# Chat History - ace-run (research.4t.gem)

- **TIMESTAMP:** 2026-10-18 15:18:42 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4t.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261018_150547.md`

## Prompt

%id(gem, clan=research.4t)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.4t.cdx`, `research.4t.cld`, `research.4t.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We currently label every pomodoro with a theme and use these themes to aggregate
statistics in the ~/bob/dash_stats.md file. I would like to start automatically labeling
pomodoros by the corresponding projects and/or areas of the task links contained in
them.

- As a part of this change, we should start aggregating the stats shown in the
  ~/bob/dash_stats.md file by area and project when possible.
- We will need the ability to exclude sub-projects of some projects from being
  aggregated and/or used to label pomodoros directly. Instead, task links to tasks in
  these sub-projects should be treated as if (when labeling pomodoro and aggregating
  stats) they pointed to tasks in the parent project that configured this. We should
  configure the ~/bob/sase.md project note to use this functionality.
- I'm not sure how/when/what to label pomodoros, so you should think hard about this.
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

# Research Report: Automating Pomodoro Project/Area Labeling and Stats Aggregation

**Researcher:** `gem` (Independent Swarm Evaluation)  
**Report File:** [`pomodoro_project_area_labeling_and_stats__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/pomodoro_project_area_labeling_and_stats__gem.md)  
**Durable Snapshot:** `research:202610/pomodoro_project_area_labeling_and_stats__gem.md` (`file:explicit:2151b54103fe0f45f226ba54`)

---

## Executive Summary & Plan Critique

### 1. Is this a good idea?
**Yes, with one vital architectural pivot.**  
Replacing free-form themes with the vault’s canonical Project and Area hierarchy eliminates manual cognitive friction, aligns daily work with your GTD structure, and prevents artificial exhaustion of the daily plan budget (`plan.max_themes`).

However, **telemetry must not be tied solely to text labels written after the em-dash (`— `)**. If telemetry relied strictly on parsing markdown line labels:
- Multi-project pomodoros (which frequently occur in your daily logs, e.g., working on both `bob` and `sase` tasks in one session) would force arbitrary winner-take-all attribution.
- Historical daily notes would require destructive batch rewrites to yield project-level telemetry.

### 2. The Core Pivot: Dual-Plane Architecture
To make this feature intuitive, reliable, and beautiful, we decouple the **Telemetry Plane** from the **Ledger Plane**:
- **Telemetry Plane (`bob stats` / `dash_stats.md`):** Read-time derivation directly from child task links. Evaluators inspect each task link, resolve its residence note, walk the parent chain, apply subproject rollup, and attribute minutes proportionally. This guarantees mathematical precision and provides immediate retrospective stats over your entire vault history without editing a single past note.
- **Ledger Plane (`bob capture` / Daily Notes):** Operational ergonomics. `bob capture` and session start/close commands automatically format and stamp the pomodoro line (`— SASE`), while respecting manual user overrides.

---

## Sub-Project Rollup Design (`~/bob/sase.md`)

To prevent satellite notes (like `sase_blog.md`, `sase_memory.md`, `sase_art.md`, and `sase_pypi_releases.md`) from fracturing stats and consuming the daily plan budget, we introduce a scalar frontmatter property on the parent project note:

```yaml
---
parent: "[[dev]]"
type: "[[project]]"
status: wip
subproject_rollup: true
---
```

### Traversal & Rollup Rules
1. **Upward Chain Traversal:** When resolving any task link (e.g., `[[sase_blog#^intro-proposal]]`), the engine walks up `parent:` wikilinks: `sase_blog` $\rightarrow$ `sase` $\rightarrow$ `dev`.
2. **Absorption Boundary:** If any ancestor project in the chain configures `subproject_rollup: true`, the task is attributed to that parent project (`sase`) for both labeling and stats.
3. **Area Derivation:** The top-level Area note at the root of the chain (`dev`) becomes the attributed Area.
4. **Zero Maintenance:** Bryan never needs to maintain an explicit list of child notes in frontmatter; any new subproject created under `parent: "[[sase]]"` automatically inherits rollup.

---

## The "What, When, and How" of Pomodoro Labeling

### What to Label
- **Single Project:** Canonical uppercase project stem (e.g., `— SASE`, `— BOB`).
- **Area-Direct Task:** Canonical uppercase area name (e.g., `— DEV`, `— GTD`).
- **Multi-Project Session:** Composite label separated by ` + ` (e.g., `— BOB + SASE`), limited to two components (falling back to common Area if broader).
- **Manual Sovereignty:** If you explicitly author a custom theme (e.g., `— DEEP WORK` or `— INTERVIEW`), automation **never** overwrites it.

### When to Label (Lifecycle Triggers)
1. **Link Time:** When `bob capture` links a task to an unnamed placeholder (`- [ ] ()`), it immediately assigns `— <PROJECT>`.
2. **Start Time (`=`):** Starting an untimed placeholder that holds task links seals the label alongside timestamps (`- [ ] (**1410-1500** [t:: 50m]) — SASE`).
3. **Close Time (`=x`):** Closing an unnamed session ensures the completed entry is cleanly labeled.
4. **Read-Time Fallback:** If a session has task links but no label, `bob stats` still attributes its time to the correct project and area.

---

## Dashboard Presentation in `~/bob/dash_stats.md`

### 1. Schema-1 JSON Contract
In `bob stats -f json`, the `worked` metric extends `parts` and `parts_summary` with two new dimensions alongside `theme`:
- `parts["project"]` and `parts_summary["project"]`
- `parts["area"]` and `parts_summary["area"]`
*(This is 100% additive and backwards-compatible with existing schema-1 consumers.)*

### 2. Obsidian UI (`bob-stats` Code Block)
In `dash_stats.md`, the context panel below the main chart introduces a segmented pill switcher:

```text
┌────────────────────────────────────────────────────────────────────────┐
│  Worked breakdown                   [ Projects ]  ( Areas )  ( Themes ) │
│  Total: 137h 40m over last 4 weeks                                     │
├────────────────────────────────────────────────────────────────────────┤
│  sase       ████████████████████████████░░░░░░░░░░░  56h 45m  (41%)     │
│  bob        ██████████████░░░░░░░░░░░░░░░░░░░░░░░░░  22h 20m  (16%)     │
│  job_2026   ████████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░  13h 55m  (10%)     │
│  plex_hack  ████░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░░   7h 10m   (5%)     │
│  other      ██████████████████░░░░░░░░░░░░░░░░░░░░░  37h 30m  (28%)     │
└────────────────────────────────────────────────────────────────────────┘
```

- **Projects View (Default):** Shows focused execution across distinct projects (with `sase` subprojects cleanly rolled up).
- **Areas View:** Provides macro life balance metrics (`DEV`, `GTD`, `JOB`, `CASH`, `BODY`).
- **Themes View:** Preserves legacy/custom theme review.
- **Interactive Sync:** Panning or pinning a day/week bar on the focus chart dynamically scopes the breakdown to that specific bucket.

### 3. Terminal Glance (`bob stats show worked -c`)
```text
 normal   4h 10m – 5h 29m (p25–p75) - total 137h 40m over 28 days - 28 of 28 days with data
 project  SASE 56h 45m 41% - BOB 22h 20m 16% - JOB 13h 55m 10% - other 44h 40m 33%
 area     DEV 63h 55m 46% - GTD 32h 16m 23% - JOB 13h 55m 10% - other 27h 34m 21%
```

---

## Recommended Implementation Roadmap

1. **Phase 1: Subproject Rollup in `bob-cli`:** Parse `subproject_rollup` in project frontmatter and add ancestor chain resolution in [`src/native/projects/`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/projects/).
2. **Phase 2: Read-Time Stats Engine:** Parse child task links in `PomodoroSession` inside [`src/native/stats/index.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/stats/index.rs) and emit `project` and `area` parts in [`src/native/stats/metrics.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/stats/metrics.rs).
3. **Phase 3: Vault Configuration:** Add `subproject_rollup: true` to [`~/bob/sase.md`](file:///home/bryan/bob/sase.md).
4. **Phase 4: Auto-Labeling on Capture & Close:** Wire `derive_pomodoro_label` into `bob capture`, start (`=`), and close (`=x`), updating `plan_budget` to meter resolved projects.
5. **Phase 5: Obsidian UI Update:** Update `bob-ledger-tools` context panel with dimension pill toggles and ranked bar rendering.

The complete research report with architecture diagrams, data schemas, and edge case analyses is available in [`sase/repos/research/202610/pomodoro_project_area_labeling_and_stats__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/pomodoro_project_area_labeling_and_stats__gem.md).
