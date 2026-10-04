# Chat History - ace-run (research.07.gem)

- **TIMESTAMP:** 2026-10-04 08:02:59 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.07.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261004_075520.md`

## Prompt

%id(gem, clan=research.07)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.07.cdx`, `research.07.cld`, `research.07.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I want to add two new review groups to the GTD morning review that I trigger with the
`]s` keymap in Obsidian: PRE and POST

- PRE should be reviewed before any other review group and POST should be reviewed after
  any other review group.
- The PRE review group should contain any ready task that has the `#gtd` and `#pre`
  tags. You should add these tags to all of the tasks in the ~/bob/gtd_daily.md file
  that recur daily except for the "Morning review" task.
- The POST review group should contain any ready task that has the `#gtd` and `#post`
  tags. You should add these tags to the "Morning review" task in the ~/bob/gtd_daily.md
  file.
- The idea is that we will close out each of these recurring GTD tasks as we get to them
  (the "Morning review" task is last so I can check off that I completed my morning
  review, which includes all of the items before it--unless there are some ROTTEN tasks
  I can't get to that day).

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

# Independent Research Report: Evaluating PRE and POST Review Groups for GTD Morning Review (`]s`)

**Researcher:** `gem` (Independent Evaluation · 4-Researcher Swarm)  
**Report Artifact:** `research:202610/gtd_pre_and_post_review_groups__gem.md`  
**Absolute Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/gtd_pre_and_post_review_groups__gem.md`  
**Artifact ID:** `explicit:539f7246829426583c0bfeff`

---

## Executive Summary & Findings

Your proposal aims to unify your morning routine into a single continuous keyboard flow via `]s`:
1. **`PRE`**: Reviewed *before* any other group, containing ready tasks tagged `#gtd #pre` (the daily recurring routine items in `~/bob/gtd_daily.md`, e.g., checking weather, brushing teeth, taking vitamins, stretches, and email).
2. **`POST`**: Reviewed *after* all other groups, containing ready tasks tagged `#gtd #post` (the `"Morning review"` task itself in `~/bob/gtd_daily.md`).
3. **Workflow Vision**: Close out each recurring GTD chore as you reach it, perform the commitment review, and check off `"Morning review"` at the end.

### Core Critique: Is this a good idea?

**The user experience intent is excellent, but the proposed sequencing contains a fatal trap:**

1. **The "ROTTEN Chasm" (Critical Usability Flaw)**:
   A live census of your vault on October 4, 2026 reveals **128 due review tasks**, including **51 commitment tasks** (4 new, 36 next, 1 returned, 10 references) and **77 ROTTEN tasks**.
   Under your established GTD practice (`docs/freshness.md` §6), ROTTEN upkeep is capped by a daily budget (5–10 tasks) and is designed to be stopped partway ("*fine to stop partway*").
   If `POST` is placed strictly after `ROTTEN`:
   $$\text{PRE [1..7]} \to \text{COMMITMENTS [8..58]} \to \text{ROTTEN [59..135]} \to \text{POST [136]}$$
   When you complete your commitments and finish your 5 daily rotten tasks, **72 rotten tasks remain**. Pressing `]s` will land on **Rotten task #6**, not `POST`. To reach `"Morning review"`, you would have to spam `]s` through **72 stale tasks** that you explicitly intended to defer! You would almost *never* reach `POST` during normal daily use.

2. **Category & Gesture Mismatch (Triage vs. Execution)**:
   - The `]s` review walk is an **analytical triage ritual** operated by `Alt+Shift+F` (keep/confirm & step) and `Alt+N` (release).
   - Habit tasks ("Brush teeth", "Take fish oil pills", "Morning stretches") are **physical execution tasks** operated by checkbox toggling (`- [ ]` $\to$ `- [x]`).
   - If you press `Alt+Shift+F` on a recurring task, Bob's placement engine **refuses to stamp** (`P13` refusal rule) because Obsidian Tasks plugin would duplicate `[fresh::]` into tomorrow's recurrence. You must use `Ctrl+Enter` to check off the task, then press `]s` to advance.
   - If you sit down at your desk to do your morning review before doing your morning stretches, stretches blocks your review queue until you skip past it.

3. **Core Invariant Breakdown (`¬recurring`)**:
   In both `bob-cli` (Rust) and `bob-ledger-tools` (JS), `walk_scope` strictly excludes `row.recurring`. Introducing `PRE` and `POST` requires carving out specific exceptions for `#gtd #pre` and `#gtd #post`. Crucially, these tasks must evaluate to `state: null` and `bucket: null` to prevent polluting your dashboard `NEW` / `READY` chips and the $B$ partition.

---

## Justified Requirements Adjustments

If proceeding with the in-engine `]s` implementation, the following three adjustments are strictly necessary:

### Adjustment 1: Reposition `POST` Immediately Before `ROTTEN`
Move `POST` to sit between the commitments walk (after `REFERENCES`) and `ROTTEN`:
$$\text{PRE} \to \text{NEW} \to \text{PROJECTS} \to \text{PENDING} \to \text{NEXT} \to \text{RETURNED} \to \text{REFERENCES} \to \mathbf{POST} \to \text{ROTTEN}$$

**Why:** In your own GTD definition (`gtd_daily.md` line 18), the non-negotiable morning review consists of clearing commitments ("*until Commitments done*"). Completing references *is* completing the core morning review. Checking off `"Morning review"` at this boundary signals completion of your review obligation, leaving ROTTEN upkeep as an optional, budget-bounded postscript.

### Adjustment 2: Dedicated "Checklist Tier" UI & Navigation Semantics
- In `bob-navigation-hotkeys`: When landing on a `PRE` or `POST` task, update the notice/footer to display: `[PRE 1/7] Check off to advance (Ctrl+Enter)` instead of `Alt+F to confirm`.
- If `Alt+Shift+F` is pressed on a `PRE` or `POST` task, map it directly to task completion (`toggleTaskDone`) rather than failing with a silent refusal.
- Ensure the walk anchor tracks checkbox completions so that checking off a recurring task cleanly advances `]s` to the next entry.

### Adjustment 3: Strict Ready-State Scoping
A recurring task in `gtd_daily.md` enters `PRE` / `POST` if and only if:
- It carries `#task`, `#gtd`, and `#pre` (or `#post`).
- Its status type is `TODO` (`- [ ]`).
- It has no future scheduled date (`scheduled <= today`).
- When checked off, Tasks plugin appends `[scheduled:: tomorrow]`, which immediately and cleanly excludes it from `PRE`/`POST` for the remainder of the day without extra code.

---

## Alternative Approaches Evaluated

| Approach | Description | Pros | Cons |
| :--- | :--- | :--- | :--- |
| **Approach 1: Refined In-Engine Tiers** *(Recommended if modifying `]s`)* | Add `pre` (tier 0) and `post` (tier 7, before rotten) to Rust and JS evaluators. | Unified single `]s` keymap across your whole morning. | Modifies shared evaluator, bumps JSON schema to 9, requires Rust/JS parity tests. |
| **Approach 2: "Morning Ritual" Orchestration Command** | A dedicated Obsidian command that opens `gtd_daily.md` for habits, launches `]s` for review, and auto-completes `"Morning review"` upon `Commitments done`. | **Zero engine changes**; completely avoids the ROTTEN trap; keeps habits separate from triage. | Requires a separate initial launcher command. |
| **Approach 3: Dashboard Embed** | Embed open `gtd_daily.md` tasks in a Dataview block at the top of `dash.md`. | Standard Obsidian setup; zero plugin code. | Retains current manual navigation friction. |

---

## Recommended Solution & Next Steps

**Proceed with Approach 1 under Adjustments 1, 2, and 3.**

This gives you exactly what you want—a single, continuous `]s` loop guiding your morning—while eliminating the 77-rotten-task trap.

### Decision Checklist Before Coding:
1. **Walk Order**: Confirm the adjusted sequence:
   $$\text{PRE} \to \text{NEW} \to \text{PROJECTS} \to \text{PENDING} \to \text{NEXT} \to \text{RETURNED} \to \text{REFERENCES} \to \mathbf{POST} \to \text{ROTTEN}$$
2. **Gesture for PRE/POST**: Confirm whether `Alt+Shift+F` on a PRE/POST task should automatically check off the task and advance, or whether you prefer pressing `Ctrl+Enter` followed by `]s`.
3. **Tagging**: Confirm that `#task #gtd #pre` and `#task #gtd #post` will be added to the active items in `/home/bryan/bob/gtd_daily.md`.

*Full architectural blueprints, Rust/JS diff specifications, and edge-case evaluations are preserved in the registered report at [`research:202610/gtd_pre_and_post_review_groups__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/gtd_pre_and_post_review_groups__gem.md).*
