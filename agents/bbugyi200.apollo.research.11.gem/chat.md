# Chat History - ace-run (research.11.gem)

- **TIMESTAMP:** 2026-10-13 08:34:12 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.11.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261013_081833.md`

## Prompt

%id(gem, clan=research.11)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.11.cdx`, `research.11.cld`, `research.11.grk`, `research.11.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Instead of automatically adding successor task links to the current / next pomodoro, I
would like to start prompting the user which unblocked tasks (if any) they would like to
pull in as successor task links when completing a task that blocks other tasks (via any
supported method).

- I'm not sure what the UX should look like for this but I was thinking that the user
  should be able to easily select one or more unblocked tasks from one or more new
  panels (we'll probably need a custom / separate solution for the bob-mac-capture app,
  but you should verify this is needed).
- I think we have a limit currently where we only pull in at most 5 successors. That
  limit should be gone now since the user can pick them explicitly.
- As a part of this change, when a task unblocks a project task that has open tasks, the
  new panel that pops up should include all open tasks that belong to that project
  (which should also been unblocked by closing the task the project depended on). I
  thought we did this already, but just tried this by closing the ^bar task in the
  ~/bob/sase.md file and it did not pull in the (non-project) tasks contained in the
  ~/bob/sase_foo.md project note as successors as I expected.
- This change should also apply to the project tasks / parent project tasks we pull in
  as successors when closing the last open task / sub-project for a project.

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

# Research Report: Prompted Unblocked Successor Task Selection

**Researcher:** `research.11.gem`  
**Report File:** [`prompted_unblocked_successor_selection__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/prompted_unblocked_successor_selection__gem.md)  
**Registered Artifact:** `explicit:246218e12944768492162a57` (`research:202610/prompted_unblocked_successor_selection__gem.md`)

---

## 1. Executive Summary & Direct Answers

### 1.1 Why Closing `^bar` in `~/bob/sase.md` Did Not Pull In `~/bob/sase_foo.md`'s Tasks
In the current architecture, this behavior was intentional under vector **PDC2** ([`docs/task-dependencies.md` §13.16](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/docs/task-dependencies.md#L2064)) and [`decisions:unblocked-tasks-resurface-as-ticklers`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/memory/decisions/unblocked-tasks-resurface-as-ticklers.md):
- When a task completes and unblocks a project's `^prj` line, the rule in [`src/native/task_complete/successors.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/task_complete/successors.rs#L726) assigns `^prj` a verdict of `Recover("project_task")`, **never** `VerdictKind::Successor`.
- In cascade, [`recover_project_members`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/task_complete/project_close.rs#L224-L290) recovers open project residents from Blocked `[?]` to Ready `[ ]`, strips `#prj_is_blocked`, and writes `[unblocked:: today]`.
- Residents were categorized as **recover-only, never successor-linked** to prevent an unblocked project from flooding the daily Pomodoro ledger without user permission.
- **Under your new proposal**, because the user is explicitly selecting which tasks to link, this restriction is no longer needed. Unblocked project members can and should be presented in the selection panel.

### 1.2 Verification: Is a Separate Solution Needed for `bob-mac-capture`?
**Yes, absolutely.**  
Under [`decisions:mac-capture-is-a-thin-client`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/memory/decisions/mac-capture-is-a-thin-client.md), Bob Mac Capture is a stateless macOS AppKit menu bar popover that delegates syntax, preview, and mutation entirely to `bob`. Popping an interactive secondary modal after submission disrupts the menu-bar capture flow. Instead, Mac Capture should leverage its existing **Live Preview Card** (`bob capture --dry-run`), allowing inline candidate selection before submission, or provide an in-popover confirmation view.

### 1.3 Removing the 5-Successor Breaker Limit
The `MAX_SUCCESSORS_PER_GESTURE = 5` limit was a mechanical safeguard against runaway automatic ledger insertions. With explicit user confirmation, **this hard cutoff should be eliminated**. If the user explicitly selects 6 or 8 tasks, they are linked. The UI should merely provide a soft visual count indicator (e.g., `⚠️ 6 tasks selected for this Pomodoro session`).

### 1.4 Unifying Empty Project Pull-In (§12.10)
When closing the last open task in a project note empties the project, candidate `^prj` (or parent `^prj`) should be presented in the exact same selection panel with `trigger: "project_empty"`. If selected, it links to the Pomodoro as Next (`[*]`); if unselected, it surfaces to Ready (`[ ]`) without touching the day file.

---

## 2. Critique of the Plan: Is Prompting a Good Idea?

### 2.1 The Value
- **Ledger Intentionality:** Eliminates unexpected tasks injected into today's Pomodoro plan and eliminates manual `Alt+N` releases.
- **Unlocks Project Activation:** Solves the resident pull-in problem by allowing the user to select the first 1–2 steps of a newly unblocked project.
- **Unified Mental Model:** Unifies dependency successors, project member unblocking, and empty project completion (§12.10) into a single user choice.

### 2.2 The Dangers & Friction Points
- **Prompt Fatigue & Interruption:** Task completion is a frequent, low-friction gesture. Forcing a modal dialog on every close interrupts flow state.
- **Destruction of the GTD Review Walk (`]s` Walk):** In morning review, the user rapidly processes items with `Ctrl+Enter` and relies on auto-advancing (`decisions:answering-advances-the-walk`). Popping a modal on every review close breaks review walk rhythm.
- **Non-Interactive Breakage:** Headless CLI commands, git commit hooks, and scripts cannot block on interactive GUI modals.

---

## 3. Recommended Adjustments to the Specification

1. **GTD Morning Review Walk Carve-Out:**  
   When a task is completed via `completeTaskAtCursor` during the `]s` review walk, **never show a modal**. Unblocked tasks recover to Ready/Tickler silently or via a lightweight toast, allowing the review walk to advance uninterrupted.
2. **Smart Pre-Selection Defaults:**  
   - If **exactly 1 task** is unblocked: Pre-select it by default. Pressing `Enter` accepts and links immediately; `Esc` skips.
   - If **multiple tasks** or **project residents** are unblocked: Leave project residents **unselected by default** so an errant `Enter` does not accidentally pull in an entire project backlog.
3. **Frictionless Zero-Link Dismissal:**  
   Pressing `Esc` or `Enter` with 0 selected immediately completes the task with **zero links added**; unblocked tasks still recover to Ready with `[unblocked:: today]`.
4. **Non-Interactive CLI Default:**  
   In `bob capture`, if stdout is not a TTY and no `--successors` flag is passed, default to **recover-only** (`--successors none`) so scripts and agents never hang.

---

## 4. Multi-Surface UX Architecture

### 4.1 Obsidian UX (`bob-plugins`)
- **Component:** `SuccessorPickerModal` extending [`FilteredPickerModal`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/200-filtered-picker-modals.js#L1).
- **Layout:**
  - Group 1: **Direct Successors** (tasks depending directly on the closed task).
  - Group 2: **Unblocked Project Tasks** (residents of newly unblocked project notes having `open_count == 0` and `scheduled <= today`).
  - Group 3: **Emptied Projects** (`^prj` lines from projects whose last task was just closed).
- **Keybindings:** `↑`/`↓` navigate, `Space` toggles checkbox, `A` toggles all, `Enter` links selected, `Esc` dismisses with 0 links.

### 4.2 Bob Mac Capture UX (`bob-mac-capture`)
- **"In-Preview Selection":**  
  While the user types `!sase:bar` or `=x`, `bob capture --dry-run -f json` returns the candidate successors.
- The Swift AppKit preview card renders selectable checkbox pills directly within the **Unblocked** preview section.
- The user can toggle candidates with mouse clicks or `⌥1`, `⌥2` before pressing `Enter`.
- On submission, Mac Capture executes:
  ```bash
  bob capture -f json --successors "task-id-1,task-id-2" -- "!sase:bar"
  ```

### 4.3 CLI UX (`bob-cli`)
- **Interactive TTY:** Renders a terminal multi-select list.
- **Headless / Non-TTY:** Supported flags:
  - `--successors <ids...>`: Explicitly links specified tasks.
  - `--successors all`: Links all unblocked candidates.
  - `--successors none`: Default when non-interactive; completes and recovers without linking.

---

## 5. Artifact Details

- **Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/prompted_unblocked_successor_selection__gem.md`
- **Artifact ID:** `explicit:246218e12944768492162a57`
- **Artifact Label:** `research:202610/prompted_unblocked_successor_selection__gem.md`
- **Final Manifest Declaration:** Accepted and committed via `sase final submit`.
