# Chat History - ace-run (research.5n.gem)

- **TIMESTAMP:** 2026-11-01 18:52:23 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.5n.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261101_183856.md`

## Prompt

%id(gem, clan=research.5n)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5n.cdx`, `research.5n.cld`, `research.5n.grk`, `research.5n.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to start making it much clearer (in a visually appealing way) why a task is
blocked in Obsidian.

- I think the best way to do this is probably to start rendering `[1]`, `[2]`, `[3]`,
  and `[4]` for tasks that have a `priority` property using distinct colors for each
  priority.
- This means that we should probably stop rendering the priority icon I'm thinking,
  right?
- We could also start rendering `[&]` for tasks that are blocked by other tasks (i.e.
  have open task dependencies).
- Note that `[1]`, `[2]`, `[3]`, `[4]`, and `[&]` are only suggestions (ones that I have
  low confidence in). Think hard about the best way to achieve my goal here.
- This way the only tasks that look like they use `[?]` in Obsidian are tasks that were
  explicitly scheduled using the `scheduled` task property.
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

# Research Report: Visual Distinction of Blocked Tasks & Priority Semantics

The independent research report has been completed and registered as a durable snapshot:
- **File:** [`blocked_task_visual_distinctions__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202611/blocked_task_visual_distinctions__gem.md)
- **Artifact:** `research:202611/blocked_task_visual_distinctions__gem.md` (`explicit:ebdd3f18710d2ae45dd276ec`)

---

## Executive Summary & Direct Critique

### 1. Critique of Rendering `[1]`, `[2]`, `[3]`, `[4]` in the Checkbox for Priority
**Verdict: Reject (Architectural Flaw — Dimensional Collapse).**

* **Lifecycle State vs. Priority Orthogonality:**
  The Markdown checkbox `- [c]` is a 1-character slot dedicated to **Lifecycle Workflow State** (`Ready [ ]`, `Next [*]`, `In Progress [/]`, `Blocked [?]`, `Done [x]`, `Cancelled [-]`). Priority (`P1`–`P4` / `high`–`lowest`) is an orthogonal dimension indicating urgency/importance.
* **Combinatorial Collisions:**
  A task can be P1 and Ready, P1 and In Progress, P1 and Blocked, or P1 and Done. If the checkbox renders `[1]`, its workflow state becomes invisible (you cannot tell if it is actionable, in-flight, blocked, or finished). If a P1 task has open dependencies, a fatal collision occurs: should the checkbox show `[1]` or `[&]`?
* **Aesthetic Degradation ("Carnival of Numbers"):**
  Rendering distinct bright colors for 1, 2, 3, and 4 in the checkbox gutter violates Bob's core visual design law (`docs/projects.md` § "Priority marks"): *"Shape carries meaning; color whispers."* It turns the left visual margin into distracting visual noise.

### 2. Critique of Dropping the Priority Icon
**Verdict: Reject (Preserve the Signal-Bar Mark).**

* The existing signal-bar mark ([`bob-priority-mark`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/135-priority-marks.js)) is exceptionally well-engineered:
  - It visually communicates P1–P4 via 4/3/2/1 staircase bars and urgent via a knocked-out `!` icon.
  - It uses quiet monochrome ink at rest (`--text-muted`).
  - It automatically folds the raw `[priority:: high]` metadata in Live Preview and reading view.
  - It cleanly integrates with Obsidian Tasks queries via CSS masks.
* Removing this mark would leave priority homeless while providing zero visual benefit.

### 3. Critique of Rendering `[&]` for Dependency-Blocked Tasks
**Verdict: Support the Goal, Reject `[&]` and Storage Mutation.**

* **Typographic Semantics:**
  The character `&` (ampersand) means "and" (conjunction), not "blocked by" or "waiting on". In monospace/interface fonts, it appears as dense punctuation.
* **The Trap of Storage Mutation:**
  Writing `- [&]` to Markdown files requires modifying `bob task reconcile` (Rust), Obsidian Tasks custom statuses, `task-status-cycler` (TypeScript), and Bob Mac Capture (Swift), while breaking hundreds of existing vault Dataview queries (`WHERE status = "?"`).
* **The Dual-Blocker Problem:**
  A task can have open dependencies *and* a future scheduled date. A single character on disk cannot represent both.

---

## The Real UX Problem Discovered

1. **The Left-Gutter Scan Path:**
   When scanning 30 tasks in a note, the eye moves vertically down the checkbox column. Because every non-actionable task displays the identical `?` glyph, the user must read across the line and down to child lines to discern *why* each item is blocked.
2. **The Tasks Query Blind Spot (The Primary Pain Point):**
   In aggregated **Obsidian Tasks query results**, child lines (`⛓️ **DEPENDS ON:**`) are completely stripped by the Tasks plugin. A dependency-blocked task has **zero visual indication** that prerequisites exist; it appears identical to an ordinary task.

---

## Recommended Solution: Render-Time Multi-Channel Blocker Decoration

Keep the stored Markdown status strictly canonical (`- [?]`). Implement multi-channel visual decoration inside [`bob-ledger-tools`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/):

### 1. Distinct Gutter Checkbox Glyphs (Live Preview & Reading View)
Style `[data-task="?"]` checkboxes dynamically based on the task's blocker classification:
* **Calendar-Deferred (Scheduled):**
  - **Glyph:** Subtle Clock / Calendar icon (Lucide `calendar-clock` / `⏳`).
  - **Tone:** Soft warm amber (`var(--color-yellow)` mixed with `--text-muted` at 25%).
  - **Tooltip:** `"Scheduled for Nov 6, 2026 (in 5 days)"`.
* **Prerequisite-Blocked (Dependencies):**
  - **Glyph:** Interlinked Chain icon (Lucide `link-2` / `⛓️`).
  - **Tone:** Technical slate-blue (`var(--color-blue)` mixed with `--text-muted` at 25%).
  - **Tooltip:** `"Waiting on 1 open prerequisite: [[Note#^id]]"`.
* **Project-Blocked (`#prj_is_blocked`):**
  - **Glyph:** Project Barrier / Lock icon (Lucide `folder-lock` / `🧱`).
  - **Tone:** Muted brick stone (`var(--text-faint)`).
  - **Tooltip:** `"Blocked by parent project [[Project Note]]"`.
* **Dual-Blocked (Scheduled + Prerequisite):**
  - **Glyph:** Interlinked Chain icon with an amber indicator pip in the top corner.
  - **Tooltip:** `"Waiting on open prerequisites AND scheduled for Nov 6, 2026"`.

### 2. Tasks Query Inline Blocker Chip
For Tasks query results (`.plugin-tasks-list-item[data-task="?"]`) where child lines are stripped:
* Inject a compact inline chip: `[⛓️ 1 dep]`.
* Clicking the chip navigates directly to the open prerequisite task.

### 3. Preserved Priority Architecture
* Retain the signal-bar staircase mark ([`bob-priority-mark`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/docs/projects.md#priority-marks)) on the task line for P1–P4 and urgent.

---

## Key Benefits of This Architecture
* **Zero Vault Migration:** Every existing Markdown file remains valid.
* **Zero CLI / Query Breakage:** `bob task reconcile`, `bob-mac-capture`, and Dataview `WHERE status = "?"` continue working without modification.
* **Instant Gutter Glanceability:** The eye scanning down the checkbox column immediately differentiates time-gated tasks from prerequisite-gated tasks.
* **Solves the Tasks Query Blind Spot:** Prerequisite information is restored to flat query views.
