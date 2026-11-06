# Chat History - ace-run (research.3h.gem)

- **TIMESTAMP:** 2026-11-05 17:15:27 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3h.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_142246.md`

## Prompt

%id(gem, clan=research.3h)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3h.cdx`, `research.3h.cld`, `research.3h.grk`, `research.3h.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add a few new recurring tasks to the ~/bob/gtd_daily.md file and also
add support for prioritizing some of the tasks in the list of pre-GTD and/or post-GTD
task review groups higher than others (by showing them before tasks with a lower
priority in that review group when walking through my GTD morning review).

- The new recurring pre-GTD tasks I would like to add should trigger on the same day as
  the corresponding post-GTD review task for each period (i.e. to review one or more
  period notes).
  - These tasks should be prioritized above all other tasks in the pre-GTD group so I
    work them first.
  - These tasks are meant to remind me to run one or more agents to update the
    appropriate period notes (depending on which periods need review that day, if any).
- Below that, we should prioritize the "Clean up SASE agents" pre-GTD task.
- Below that, we should prioritize all pre-GTD tasks that require my internet browser
  (the tasks related to the weather, my email, and my calendar--this is just meant to
  make sure that I always do all of these tasks at once). All other pre-GTD tasks should
  be reviewed after these.
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

# Research Summary: Prioritized GTD Review Groups and Period Note Agent Workflows

**Researcher**: `gem` (5-Researcher Swarm)  
**Report File**: [`202611/pre_gtd_periodic_tasks_and_review_priority__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/sase/repos/research/202611/pre_gtd_periodic_tasks_and_review_priority__gem.md)  
**Durable Artifact Snapshot**: `file:explicit:1065ca5db21da91aead2a94e` (`research:202611/pre_gtd_periodic_tasks_and_review_priority__gem.md`)

---

## 1. Executive Summary & Design Overview

We investigated the requirements for:
1. Adding recurring pre-GTD reminder tasks to `~/bob/gtd_daily.md` to trigger autonomous background agent runs for period notes on review days.
2. Enabling intra-tier task prioritization within the GTD review checklist groups (`PRE` and `POST`) to support Bryan's morning review workflow hierarchy:
   - **Rank 1 (Top Priority)**: Period note agent launch tasks (so agents start immediately in the background).
   - **Rank 2**: Clean up SASE agents on athena and apollo.
   - **Rank 3**: Browser-dependent pre-GTD tasks (Google Calendar, Weather, Email) batched into a single web session.
   - **Rank 4 (Standard)**: Local chores and physical rituals (Teeth, Supplements, Morning stretches, Reconcile).

### The Technical Root Cause of Line Drift
Currently, both the Rust CLI (`src/native/freshness/state.rs`) and Obsidian plugins (`plugins/bob-ledger-tools/src/110-freshness-queue.js`) sort tasks within `Tier::Pre` and `Tier::Post` strictly by **file line order** (`path ↑, line ↑`).
Relying solely on physical line order in `~/bob/gtd_daily.md` is fragile:
- When a recurring task is completed via `Ctrl+Enter`, Obsidian Tasks rewrites the completed line (`- [x]`) and inserts the newly created recurrence (`- [?]`), causing line numbers to shift and drift over time.
- Tasks recurring on different schedules (daily vs. weekly vs. quarterly) interleave unpredictably when evaluated dynamically on different days.

### The Recommended Prioritization Architecture: Native Tasks Priority
Instead of introducing custom tags (`#p1`, `#browser`) or ad-hoc inline fields (`[order:: 1]`), intra-tier prioritization should leverage standard Obsidian Tasks `[priority:: <level>]` fields:
- **Rank 1**: `[priority:: highest]` (renders Bob's solid urgent `!` square mark).
- **Rank 2**: `[priority:: high]` (renders 4 signal bars, P1).
- **Rank 3**: `[priority:: medium]` (renders 3 signal bars, P2).
- **Rank 4**: *No priority field* (defaults cleanly to `normal` / P0, keeping markdown clean).

Both engines (`bob-cli` and `bob-plugins`) update their `PRE` and `POST` queue comparators to sort by:
$$\text{priority } \uparrow \quad (\text{highest} > \text{high} > \text{medium} > \text{normal} > \text{low} > \text{lowest}), \quad \text{then } \text{path } \uparrow, \quad \text{then } \text{line } \uparrow$$

---

## 2. Plan Critique & Important Workflow Discoveries

### Critique 1: The Ledger Reconcile Dependency (Data Integrity Hazard)
- **The Finding**: Period note agents use `bob periods brief <PERIOD>` and `bob periods draft <PERIOD>`, which perform a full `bob stats` computation across all constituent daily notes.
- **The Risk**: If Bryan launches period review agents in Rank 1 *before* running `Run task reconcile + gcal sync + gkeep pull` (currently placed in Rank 4), Sunday's unfiled Pomodoros or unsynced Google Calendar events may not yet be reconciled, leading the agent to generate draft reviews based on incomplete ledger data!
- **Adjustment**: Bryan must ensure Sunday closeout includes reconcile, or elevate `task reconcile` to run prior to or alongside the agent launch.

### Critique 2: SASE Environment Stability vs. Early Launch
- Launching new agents into remote SASE hosts (`athena` / `apollo`) *before* running `Clean up SASE agents on athena and apollo ... update SASE on all machines!` carries a minor operational risk if host daemons need restarts or binary updates.
- Bryan's desire for background concurrency is sound, provided the SASE host environment is healthy; if SASE updates or host restarts are required on Monday morning, cleanup should precede new agent launches.

### Critique 3: Fixing the POST-GTD Walk Inversion Bug
- In `~/bob/gtd_daily.md`, `Morning review` currently sits on line 15 with explicit instructions stating `Closeout · complete last`. However, `Weekly review` sits on line 24.
- Because `POST` currently sorts by `line ↑`, the morning review walk lands on `Morning review` **before** `Weekly review` on Mondays!
- Introducing priority sorting solves this bug immediately: assigning `[priority:: high]` to `Weekly review` ensures it is walked and completed *before* `Morning review` (`[priority:: lowest]` / normal) closes the session.

---

## 3. Proposed Task Specifications for `~/bob/gtd_daily.md`

In accordance with ISO 8601 and `bob periods`, periodic notes exist for **weeks**, **quarters**, and **years** (months are intentionally omitted from review rolls; see Section 3.4 of research note `period_note_tree_and_stats_strips__gem.md`).

### Proposed Task Block

```markdown
### Blocked

%% --- Rank 1: Pre-GTD Period Note Agent Launch (Trigger on Review Days) --- %%
- [?] #task #gtd #pre [priority:: highest] **Update weekly note**: Launch agent with "Update last week's note (YYYY/YYYY-Www.md)" via `bob periods brief` / `bob periods draft`  [repeat:: every week on Monday when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-09]
- [?] #task #gtd #pre [priority:: highest] **Update quarterly note**: Launch agent with "Update last quarter's note (YYYY/YYYY-Qn.md)" via `bob periods brief` / `bob periods draft`  [repeat:: every 3 months on the 1st Monday]  [created:: 2026-11-05]  [scheduled:: 2027-01-04]
- [?] #task #gtd #pre [priority:: highest] **Update yearly note**: Launch agent with "Update last year's note (YYYY.md)" via `bob periods brief` / `bob periods draft`  [repeat:: every January on the 2nd Monday]  [created:: 2026-11-05]  [scheduled:: 2027-01-11]

%% --- Rank 2: Pre-GTD SASE Environment Health --- %%
- [?] #task #gtd #pre [priority:: high] **Clean up SASE agents on athena and apollo**: Restart failed agents, dismiss agents from yesterday, review inboxes, update SASE on all machines!  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]

%% --- Rank 3: Pre-GTD Browser Batch (Calendar, Weather, Email) --- %%
- [?] #task #gtd #pre [priority:: medium] Review next week in Google Calendar  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
- [?] #task #gtd #pre [priority:: medium] Check [weather](https://google.com/search?q=weather)  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
- [?] #task #gtd #pre [priority:: medium] Read email  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]

%% --- Rank 4: Pre-GTD Local Maintenance & Physical Chores --- %%
- [?] #task #gtd #pre Run `task reconcile` + `gcal sync` + `gkeep pull`  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
- [?] #task #gtd #pre Brush teeth  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
- [?] #task #gtd #pre Take fish oil pills + Take L-tyrosine pills  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
- [?] #task #gtd #pre Do morning stretches [created:: 2026-07-06] [scheduled:: 2026-11-11]  [repeat:: every day when done]

%% --- POST-GTD Review Rituals (Prioritized over Morning Closeout) --- %%
- [?] #task #gtd #post [priority:: high] **Weekly review**: close last week — from today's note open the week link, then ‹; no Review yet? launch an agent with "Update YYYY/YYYY-Www.md", correct its draft, and write the Reflection · open this week's note, re-read the quarter's Outcomes (↑), and set ≤3 Intentions · prune: release [[dash#NEXT Tasks|NEXT]] to ≤15 and [[dash#PENDING Tasks|PENDING]] to ≤10 with Alt+N, promote from [[dash#READY Tasks|READY]], defer with P-levels, clear leftover [[rotten|ROTTEN]] or lengthen that note's task_refresh.  [repeat:: every week on Monday when done]  [created:: 2026-11-02]  [scheduled:: 2026-11-09]
- [?] #task #gtd [priority:: high] **Quarterly review**: close the quarter that just ended — every week reviewed? · launch an agent with "Update YYYY/YYYY-Qn.md", correct its draft, write the Reflection · prune [[projects]]: close, pause, or recommit each open ^prj · set ≤3 Outcomes in the new quarter's note.  [repeat:: every 3 months on the 1st Monday]  [created:: 2026-11-03]  [scheduled:: 2027-01-04]
- [?] #task #gtd [priority:: high] **Yearly review**: after the Q4 review — launch an agent with "Update YYYY.md", correct its draft, write the Reflection · revisit [[h3_goal]] and [[h4_vision]] · set the new year's Theme and ≤3 Outcomes.  [repeat:: every January on the 2nd Monday]  [created:: 2026-11-03]  [scheduled:: 2027-01-11]
- [?] #task #gtd #post [priority:: lowest] **Morning review**: PRE chores done or knowingly skipped · walked to Commitments done (NEW never capped or skipped; lanes: keep Alt+Shift+F, today Ctrl+Shift+Enter, release Alt+N; tickler not-now is a priority roll, not Alt+F; recurring: Ctrl+Enter done, Ctrl+Shift+Enter today, or reschedule — never Alt+F) · [[crowded|CROWDED]] at 0 (split, sequence, defer, drop) · highlight chosen (≤3 themes, highlight first) · [[rotten|ROTTEN]] upkeep until 0, budget, or you stop — then ]S and complete this.  [repeat:: every day when done]  [created:: 2026-11-05]  [scheduled:: 2026-11-06]
```

---

## 4. Implementation Summary & Next Steps

1. **`bob-cli` Core**:
   - Update [`RichTask`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/src/native/dataview/tasks/mod.rs#L106-L126), [`FreshnessRow`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/src/native/freshness/state.rs#L183-L204), and `QueueEntry` to carry `priority: Priority`.
   - Update `evaluate_freshness_queue` in [`src/native/freshness/state.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/src/native/freshness/state.rs#L927-L930) to sort `Tier::Pre` and `Tier::Post` by `priority.cmp()` then `path` and `line`.
   - Update [`docs/freshness.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/docs/freshness.md#L474-L487) §4 comparator specification.
2. **`bob-plugins` Parity**:
   - Extract `priority` in [`freshnessRowFromTask`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/160-widgets-and-row.js#L285-L340).
   - Implement `freshnessComparePriority` in [`freshnessQueue`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/110-freshness-queue.js#L65-L78).
3. **Artifact Registration & Finalizer**:
   - The full report is stored at [`sase/repos/research/202611/pre_gtd_periodic_tasks_and_review_priority__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_41/sase/repos/research/202611/pre_gtd_periodic_tasks_and_review_priority__gem.md).
   - Snapshot registered as `research:202611/pre_gtd_periodic_tasks_and_review_priority__gem.md` (id: `explicit:1065ca5db21da91aead2a94e`).
   - SASE finalizer declaration submitted and accepted for host commit.
