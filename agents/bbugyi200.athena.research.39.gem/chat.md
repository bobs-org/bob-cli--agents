# Chat History - ace-run (research.39.gem)

- **TIMESTAMP:** 2026-10-01 16:27:21 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.39.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_161410.md`

## Prompt

%id(gem, clan=research.39)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.39.cdx`, `research.39.cld`, `research.39.grk`, `research.39.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

One of my goals while reviewing my Obsidian tasks during my morning GTD is to make sure
that no area/project note file contains more than N ready tasks (this number should be
configurable, but should default to 5).

- The idea is that if I have more than N ready tasks in a area/project, then I should
  probably look into creating a new project from some of those tasks and/or
  de-prioritizing (using the `<ctrl+shift+p>` keymap, for example) some tasks in that
  area/project note file.
- I would like to make it clearer which project files have more ready tasks than they
  should.
- We should show some kind of notification / toast in Obsidian anytime we use any one of
  the Obsidian keymaps that would cause this constraint to be violated (for example,
  when moving a task to a project note file that already has >=N ready tasks).
- We should show a badge and/or diagnostics in the ~/bob/dash.md file and/or in project
  note files that makes it clear how many area/projects violate this contraint currently
  (and which ones).
- I should also have the ability to view this information from the command-line. Namely,
  I should have the ability to review the number of ready tasks in each area/project
  note file from the command-line and should be able to see (in some visually appealing
  way) when this constraint is being violated (and in which area/project note files).
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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research & Architecture Report: Area & Project Ready Task Limits

**Research ID:** `research.39.gem`  
**Durable Snapshot Ref:** `file:explicit:0183932a3d31d2e6c77cd501` (`research:202610/area_project_ready_task_limits__gem.md`)  
**Target Environments:** `bob-cli` (Rust), `bob-plugins` (CommonJS), Bob Vault (`~/bob/`)

---

## 1. Executive Summary & Critique: Is This a Good Idea?

### The Verdict
**Yes, but with crucial refinements.** Capping ready tasks at $N$ (default 5) per area and project note is a high-leverage GTD and Kanban practice. It attacks the single greatest source of clutter during morning GTD review: **unconstrained backlog hoarding**.

However, a naive, flat implementation will create friction and false alarms. Our analysis of Bryan's live vault (96 area and project notes) revealed specific architectural nuances that require adjustments to the initial design.

### Key Insights from Bryan's Live Vault Data
1. **80% of active projects already comply**: Out of 41 active projects, 33 currently have $\le 5$ ready tasks.
2. **The "Big Four" Backlog Hoarders**: Overload is concentrated in a handful of notes:
   - `sase.md`: **62 ready tasks** (total open: 262) — umbrella parent with 30 sub-projects.
   - `sase_remote.md`: **12 ready tasks** (total open: 15).
   - `sase_pager.md`: **8 ready tasks** (total open: 9).
   - `sase_usage.md`: **8 ready tasks** (total open: 8).
3. **The Inbox Trap**: `gkeep_inbox.md` holds **65 ready tasks** because it carries `type: [[area]]` in frontmatter. Applying a flat cap to all area notes would make inboxes permanently sound alarms.

---

## 2. Necessary Adjustments to the Requirements

| Proposed Requirement | Flaw / Risk | Recommended Adjustment |
| :--- | :--- | :--- |
| **Flat cap $N=5$ for both Areas and Projects** | Areas are continuous life maintenance horizons (e.g. `cash.md`, `body.md`); projects are finite outcomes. Areas naturally hold more non-blocking tasks. | **Differentiated Defaults & Note Overrides**: Default $5$ for projects, $7$ for areas. Support frontmatter override: `ready_cap: 10` or `ready_cap: exempt`. |
| **All `[[area]]` notes checked** | `gkeep_inbox.md`, `inbox.md`, and `mac_inbox.md` are capture hoppers, not backlogs. | **Explicit Inbox Exemption**: Automatically exempt capture inboxes (`inbox.md`, `*_inbox.md`, or `inbox: true`). |
| **Parent/Meta-Projects (`sase.md`)** | Umbrella projects with 30 sub-projects accumulate loose tasks. | **Strictly Enforce Cap on Parent Notes**: Do *not* grant higher caps to umbrella notes. The 5-task cap forces loose tasks into sub-projects (`Ctrl+Shift+M` or `Ctrl+Shift+Alt+N`). |
| **Post-Move Toast Only** | Toasting *after* `Ctrl+Shift+M` is reactive; the task has already moved. | **Proactive Picker Previews**: Show `[ready/cap]` tags on destination rows in `TaskMoveDestinationPickerModal` *before* selection, followed by an enriched Notice after. |
| **Constraint Enforcement** | Risk of hard-blocking operations. | **Keep Limits Soft**: Like Bob's lane caps (`max_next: 15`, `max_ready: 100`), limits trigger visual warnings, colored badges, and lints, but never lock keymaps. |

---

## 3. Recommended Multi-Layer Architecture

```
                  ┌──────────────────────────────────────────────┐
                  │      ~/.config/bob/config.yml                │
                  │  projects:                                   │
                  │    max_ready_tasks: 5                        │
                  │    max_area_ready: 7                         │
                  │    exempt: [inbox, gkeep_inbox, mac_inbox]   │
                  └──────────────────────┬───────────────────────┘
                                         │
                 ┌───────────────────────┴───────────────────────┐
                 ▼                                               ▼
   ┌───────────────────────────┐                   ┌───────────────────────────┐
   │     bob-cli (Rust Core)   │                   │  bob-plugins (Obsidian)   │
   ├───────────────────────────┤                   ├───────────────────────────┤
   │ • Status grouping badges: │                   │ • bob-navigation-hotkeys: │
   │   ⚪ 6/5 ready ⚠️         │                   │   - Picker count badges   │
   │ • CLI Commands:           │                   │   - Smart move toasts     │
   │   - bob projects list -o  │                   │ • bob-project-tasks:      │
   │   - bob backlog list      │                   │   - Materialize counts    │
   │ • Strict parity with JS   │                   │ • dash.md / ledger-tools: │
   │   definition of Ready     │                   │   - OVERCAP widget chip   │
   └───────────────────────────┘                   │   - Morning triage banner │
                                                   └───────────────────────────┘
```

### 3.1 Exact Definition of a "Ready Task"
A task is counted as **Ready** in note $N$ if:
1. $N$ has `type: "[[project]]"` or `type: "[[area]]"`, and is not exempt.
2. Checkbox status is `[ ]` (TODO). `[*]`, `[/]`, `[x]`, `[-]` are excluded.
3. No future inline schedule: absent or `[scheduled:: \le today]`.
4. No open Dataview dependency: `[dependsOn:: ...]` targets are resolved/closed.
5. No `#hide` tag and not in `_templates/` or `_conflicts/`.
6. Not linked under today's open Pomodoros (`isToday !== true`).
7. Resides in the canonical `## Tasks` intake pool.

---

## 4. UI & Interaction Design

### 4.1 Proactive Destination Picker & Move Toasts (`bob-navigation-hotkeys`)
1. **Picker Previews (`Ctrl+Shift+M`)**:
   In `TaskMoveDestinationPickerModal`, each item displays its live ready count:
   - `sase_better_config    [2/5 ready]` *(subtle muted tag)*
   - `sase_remote           [12/5 ready ⚠️]` *(high-contrast warning accent)*
2. **Move Notice**:
   If moving causes or compounds an overflow:
   `Moved 1 task to sase_remote (⚠️ 13/5 ready · +8 over cap)`

### 4.2 Upgraded Note Badges (`task_status_groups`)
The existing generated badge in `## Tasks` is upgraded from `⚪ 61 open` to show the fraction against the cap:
- **Healthy**: `[`⚪ 3/5 ready`](#Tasks)`
- **At Cap**: `[`⚪ 5/5 ready`](#Tasks)`
- **Over Cap**: `[`⚪ 12/5 ready ⚠️`](#Tasks)` *(linked to `#Tasks`, styled with warning CSS)*

### 4.3 Morning GTD Dashboard (`dash.md`)
1. **Header Chip Bar**:
   Adjacent to `READY 87/100`, render an `[OVERCAP 4 ↗]` chip (warning colored when $> 0$, neutral when $0$) that links directly to backlog diagnostics.
2. **Morning Backlog Triage Callout**:
   Directly above `### READY Tasks` in `dash.md`, render an interactive DataviewJS callout listing violating projects with their counts and actionable next steps (split into sub-project or roll priority via `Ctrl+Shift+P`).

---

## 5. Command-Line Interface (`bob-cli`)

Following `sase/memory/cli_rules.md`, CLI tools must be fast, beautiful, and complete:

### 5.1 Upgrading `bob projects list`
Add a colored `READY` column and filtering flags:
```text
$ bob projects list -o
Area & Project Backlog Health — 4 notes violating ready cap (>5)

  NOTE                              KIND     STATUS    READY   OPEN  TOTAL  ACTION
  sase                              project  wip       62/5 !   124    269  split sub-projects
  sase_remote                       project  wip       12/5 !    12     15  de-prioritize / roll
  sase_pager                        project  wip        8/5 !     8      9  de-prioritize / roll
  sase_usage                        project  wip        8/5 !     8      8  de-prioritize / roll
```

- `-a, --areas`: Include area notes alongside projects.
- `-c, --cap <N>`: Override threshold for ad-hoc inspection.
- `-o, --only-violations`: Show only over-cap notes.
- `-f, --format {human,json}`: Support automation and scripting.

### 5.2 Dedicated Morning GTD Triage Command
Introduce `bob backlog list` (or `bob projects audit`), designed specifically for morning review:
```bash
bob backlog list [-a] [-c <N>] [-k {all,area,project}] [-o] [-s {ready,name,total}]
```

---

## 6. Implementation Phasing

1. **Phase 1: Configuration & CLI Foundations (`bob-cli`)**
   - Add `projects:` block to `~/.config/bob/config.yml`.
   - Implement ready-task evaluation in Rust and upgrade `bob projects list` with colored `READY` column and `-o` filter.
2. **Phase 2: Note Badges & Frontmatter Materialization**
   - Upgrade Rust `task_status_groups` badge emitter to render `⚪ <ready>/<cap> ready`.
   - Update `bob-project-tasks` to materialize `ready_task_count` into note frontmatter.
3. **Phase 3: Interactive Obsidian Gestures (`bob-navigation-hotkeys`)**
   - Add destination picker count tags and post-move warning toasts for `Ctrl+Shift+M`.
   - Add boundary notifications to `Alt+N` (release) and `Ctrl+Shift+P` (un-scheduling).
4. **Phase 4: Dashboard & GTD Integration (`dash.md`, `bob-ledger-tools`)**
   - Add `OVERCAP` chip and triage diagnostic callout to `dash.md`.

---
*The full, unabridged research document and conformance specifications have been written to:*  
[`sase/repos/research/202610/area_project_ready_task_limits__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/area_project_ready_task_limits__gem.md)  
*Registered durable artifact:* `file:explicit:0183932a3d31d2e6c77cd501`
