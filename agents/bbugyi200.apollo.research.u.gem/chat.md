# Chat History - ace-run (research.u.gem)

- **TIMESTAMP:** 2026-09-30 15:19:21 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.u.gem
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_150848.md`

## Prompt

%id(gem, clan=research.u)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.u.cdx`, `research.u.cld`, `research.u.grk`, `research.u.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
think we may have made a mistake adding the `#now` tag.

- Part of the reason it was deemed necessary is because we were preserving the behavior
  of the `bob task-status-hooks` command that keeps WIP/Next Obsidian task statuses in
  sync with whether or not the task has a task link in the current pomodoro.
- We can remove that, but that would leave one unfilled need: I need a way to query for
  all tasks associated with task links in today's daily file.
- We can fill this need, however, using either a file path filter in the query or by
  using some kind of `#today` tag that the `bob task-status-hooks` command starts
  managing instead of WIP/Next statuses.
- We would then replace the Now/WIP/Next section queries in the ~/bob/dash.md file with
  Today/Pending/Next queries that must be mutually exclusive (i.e. a task can only be
  shown in one of these sections).
- Then, as a part of my daily morning GTD review, I can review all Pending/Next tasks
  first to pull in tasks for today and then, if I don't have enough work for the day,
  pull from the Ready section's tasks.
- This means that what was tracked using `#now` would now start being tracked by the
  Next status. The only thing I think I lose here is the ability to have a task link
  that is not tagged with `#now` (since every task link is either WIP/Pending or--by
  default--Next). That's fine though since I don't really need that I don't think.
- It's important that Pending/WIP tasks not have their statuses wiped by the
  `bob task-status-hooks` command either since that will allow me to remove the
  corresponding task link when I have a task that is in-progress, likely to be done the
  next time I look at it, but I won't be able to look at it for a while (because a swarm
  of agents will take a few hours to implement it, for example--this way I won't forget
  to review this work, since it will be in the Pending section of the ~/bob/dash.md
  file, but it also won't be in my face for the time being, since I can remove it from
  my daily file).

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

# Research Report: Retiring `#now` and Adopting a `Today / Pending / Next / Ready` Task Taxonomy

- **Researcher:** `gem` (5-researcher swarm)
- **Artifact Reference:** `research:202609/now_tag_retirement_today_pending_next_taxonomy__gem.md`
- **Artifact ID:** `explicit:094f20f79c92fa76a020da6e`
- **Report Path:** [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202609/now_tag_retirement_today_pending_next_taxonomy__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202609/now_tag_retirement_today_pending_next_taxonomy__gem.md)

---

## Executive Summary & Verdict

Your intuition is **spot-on**: adding `#now` was an emergency band-aid to escape the *status-lock trap*, but it ended up inverting standard GTD semantics, cluttering the dashboard, and creating friction with modern asynchronous agent swarms.

Your proposed direction—retiring `#now`, letting `[*]` Next represent your weekly horizon/GTD Next Actions pool, letting `[/]` In Progress represent in-flight/delegated work without aggressive decay, and maintaining mutually exclusive dashboard sections—is **an excellent, high-leverage architectural improvement**.

However, our research reveals **three critical technical and systemic adjustments** that must be made to your plan:

1. **A query-based "file path filter" is technically impossible; a machine-managed `#today` tag is mandatory.**
   Because task definitions live in domain notes (`sase.md`, `dev.md`) while Pomodoro links live in daily notes (`YYYY/YYYYMMDD.md`), Obsidian Tasks queries cannot filter tasks by incoming block links or backlinks. Tasks has no graph-traversal capability, and `bob-cli`'s native Rust Tasks engine operates in an isolated JavaScript sandbox. Therefore, `bob task-status-hooks` must manage a `#today` tag on the task lines themselves.
2. **Preventing Status Inflation requires explicit Caps and Lints for `NEXT` and `PENDING`.**
   Automatic decay was originally built because unmanaged statuses explode (reaching 50 `[/]` and 25 `[*]` tasks in September 2026). If `task-status-hooks` stops demoting `[*]` and `[/]`, human discipline alone will not prevent backlog rot. We must repurpose the plan budget engine:
   - Cap `NEXT` at 15 (inheriting `plan.max_now`, renamed `plan.max_next`).
   - Cap `PENDING` at 5 (WIP limit for in-flight/delegated work).
   - Display active counters on `dash.md` chips that turn red when caps are exceeded, backed by `bob plan` lints.
3. **Mutual Exclusivity on `dash.md` must be enforced via Boolean Tag/Status Query Filters.**
   Using `#today` and standard Tasks filters, the four sections become cleanly and mathematically mutually exclusive:
   - `TODAY`: `tags include #today`
   - `PENDING`: `status.type is IN_PROGRESS` AND `tags do not include #today`
   - `NEXT`: `status.name includes Next` AND `tags do not include #today`
   - `READY`: `status.type is TODO` AND `status.name does not include Next` AND `tags do not include #today`

---

## Detailed Critique of the Proposed Plan

### 1. What Makes This Plan Great
* **Restores Natural GTD Semantics:** Standard GTD has "Next Actions" (your committed horizon) and "Calendar/Daily Focus" (today). In Bob, `[*]` was hijacked to mean "in today's Pomodoro ledger", which forced `#now` to be invented to fill the true Next Actions role. Calling the weekly inventory `Next` (`[*]`) and today's execution `Today` (`#today`) restores natural ergonomics.
* **Empowers Asynchronous Agent Swarms:** When launching a 3-hour SASE agent swarm, you want the task off today's immediate Pomodoro ledger so it is not in your face. Under the old rules, unlinking it caused `task-status-hooks` to demote it to `[ ]` Ready after 24 hours, burying it in the backlog. Under the new model, unlinking it simply strips `#today`, causing it to drop safely and visibly into `dash.md#PENDING Tasks`.
* **Eliminates Dashboard Duplication:** With strict mutual exclusivity, a task exists in exactly one section on `dash.md`. When pulled into today's ledger, it automatically moves from `NEXT` to `TODAY`.
* **Zero-Overhead Capture:** You no longer need to type `#now` or use Alt+N hotkeys during capture. Capturing with `@route^id` creates or links a task that is naturally `[*]` and tagged `#today`.

### 2. Why the "File Path Filter" Fails (and Why `#today` Works)
In Obsidian Tasks and `bob query --tasks`:
* The query expression `path includes ...` or `filter by function task.file.path ...` inspects the path where the task is **defined**, not where it is **referenced**.
* For a task `- [*] #task Ship feature ^ship` in `dev.md`, `task.file.path` is `"dev.md"`, even if linked inside `2026/20260930.md`.
* Obsidian Tasks has no concept of backlinks or incoming block links.
* Consequently, **the task line itself must carry an explicit marker**.
* A machine-managed `#today` tag placed right after `#task` (`- [*] #task #today ...`) provides 100% reliable filtering across Obsidian Tasks and `bob query --tasks` without corrupting trailing Dataview fields or block IDs.

### 3. Mitigating the Risk of Status Inflation (The 50 WIP Trap)
The original reason `task-status-hooks` implemented aggressive decay was that unmanaged checkbox statuses suffered from Little's Law queue explosion. If `task-status-hooks` stops demoting `[*]` and `[/]`, we must prevent status inflation through **visibility and budgeting rather than silent decay**:
1. **Caps on `dash.md` Chips:**
   - `NEXT n/15`: Turns bright red when `n > 15`.
   - `PENDING n/5`: Turns bright red when `n > 5` (WIP limit).
2. **`bob plan` Lints:**
   - Emits `next_cap_exceeded` and `pending_cap_exceeded` warnings.
3. **Stale Age Visibility:**
   - In `dash.md#PENDING Tasks`, sort tasks by modification date so tasks lingering in `PENDING` for > 3 days are immediately flagged during the morning review.

---

## The New `dash.md` Architecture

### Mutually Exclusive State Matrix

| Section | Checkbox Status | `#today` Tag | Criteria & Mutual Exclusivity |
| :--- | :--- | :--- | :--- |
| **`## TODAY Tasks`** | `[*]` or `[/]` | **Yes** | Active in today's Pomodoro ledger |
| **`## PENDING Tasks`** | `[/]` (In Progress) | **No** | In-flight / delegated to agents / paused |
| **`## NEXT Tasks`** | `[*]` (Next) | **No** | Weekly commitment horizon / GTD Next Actions |
| **`## READY Tasks`** | `[ ]` (Todo) | **No** | Backlog (unblocked, unscheduled) |

*(Blocked tasks `[?]` and future schedules remain excluded from all four sections by `is not blocked` in `TQ_extra_instructions`.)*

### Exact Tasks Code Blocks for `dash.md`

```markdown
### TODAY Tasks

```tasks
not done
tags include #today
sort by status
sort by priority
```

### PENDING Tasks

```tasks
not done
status.type is IN_PROGRESS
tags do not include #today
sort by priority
```

### NEXT Tasks

```tasks
not done
status.name includes Next
tags do not include #today
sort by priority
```

### READY Tasks

```tasks
not done
status.type is TODO
status.name does not include Next
tags do not include #today
sort by priority
```
```

---

## Daily GTD Review & Execution Workflow

1. **Morning Review (`dash.md`):**
   - **Step 1: Triage `PENDING Tasks`.** Review work that was in-flight or delegated to agents overnight. If completed, mark `[x]`. If ongoing, leave in `PENDING` or pull into `TODAY`.
   - **Step 2: Pull from `NEXT Tasks`.** Select 3–5 focus tasks for today and link them under an open Pomodoro in `YYYYMMDD.md`. `task-status-hooks` immediately adds `#today`, which automatically moves them from `NEXT` into `TODAY`.
   - **Step 3: Review `READY Tasks` (Backlog).** Only if daily capacity remains, promote candidate tasks to `[*]` (or link directly into the ledger).
2. **Daily Execution:**
   - Work strictly from `TODAY Tasks` and the daily Pomodoro ledger.
   - When delegating a task to an agent swarm: remove the block link from today's ledger. `task-status-hooks` strips `#today`, and the task automatically transitions to `PENDING Tasks`. It stays off your immediate focus while remaining safely tracked for tomorrow's review.

---

## Implementation & Migration Roadmap

1. **`bob-cli` Core (`src/native/task_status_hooks/`):**
   - Manage `#today` on tasks linked under today's open Pomodoros and their transcluded dependencies.
   - Strip `#today` from tasks no longer in today's open Pomodoros or on day rollover.
   - Make `[*]` and `[/]` sticky: stop demoting to `[ ]` on unlink.
   - Ensure unstarted tasks pulled from `[ ]` into today's ledger are promoted to `[*]`.
2. **`bob-cli` Budget Engine (`src/native/plan_budget/`):**
   - Deprecate `max_now` in favor of `max_next` (default 15) and add `max_pending` (default 5).
   - Add `next_cap_exceeded` and `pending_cap_exceeded` lints.
3. **`bob-plugins`:**
   - Update `bob-ledger-tools` API to compute `nextBudget()` and `pendingBudget()`.
   - Update `bob-navigation-hotkeys`: change `Alt+N` to toggle `[*]` Next instead of `#now`.
4. **Vault Migration & `dash.md`:**
   - Run a one-time migration: convert `- [ ] #task ... #now` to `- [*] #task ...`, and strip `#now` from existing tasks.
   - Update `dash.md` Tasks queries and DataviewJS header chips.
5. **Memory & SASE Documentation:**
   - Supersede `decisions/now-tag-is-user-owned`.
   - Amend `decisions/task-status-is-derived`.

---

The full research report has been committed and registered as:
- **Path:** [`sase/repos/research/202609/now_tag_retirement_today_pending_next_taxonomy__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202609/now_tag_retirement_today_pending_next_taxonomy__gem.md)
- **Artifact:** `research:202609/now_tag_retirement_today_pending_next_taxonomy__gem.md` (`explicit:094f20f79c92fa76a020da6e`)
