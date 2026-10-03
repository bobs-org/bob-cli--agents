# Chat History - ace-run (research.35.gem)

- **TIMESTAMP:** 2026-10-01 11:29:54 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.35.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_112023.md`

## Prompt

%id(gem, clan=research.35)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.35.cdx`, `research.35.cld`, `research.35.grk`, `research.35.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

The point of the
new `[fresh::<date>]` properties that we've added to ready Obsidian tasks is to make it
clearer which of those tasks are really ready.

- A new task or a rotten task (let's start using the term "rotten" instead of "stale")
  should not be shown in the "READY tasks" section of the ~/bob/dash.md file.
- Instead, we should show new tasks either in a new "NEW tasks" section, which should be
  shown above the "WIP tasks" section and show rotten tasks in a new ~/bob/rotten.md
  file (that the ~/bob/dash.md file links to with a new "ROTTEN" badge).
- We may need to preprocess these rotten tasks somehow in order to make this work. My
  first thought was that we could use the `bob task-status-hooks` command to add a
  `#rotten` tag to rotten tasks, but you should think hard about the best way to
  implement this.

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

# Research Report Summary: Ready Tasks Freshness, Rotten Separation, and Dashboard Architecture

The independent research report has been completed, written to disk, and registered as a durable artifact snapshot.

- **Report Path:** [`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/ready_tasks_rotten_and_new_dash_architecture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/ready_tasks_rotten_and_new_dash_architecture__gem.md)
- **Artifact Reference:** `file:explicit:ded9319dbf23cb3d720185a8` (`research:202610/ready_tasks_rotten_and_new_dash_architecture__gem.md`)
- **Finalizer Declaration:** Submitted and accepted for host commit (`commit`).

---

## Key Findings & Strategic Critique

### 1. Is the General Idea Good?
**Yes, conceptually it is a major operational upgrade.**
In Bryan's current vault, the `### READY Tasks` section displays ~180 tasks. Having un-triaged new captures (raw inbox items) and neglected decaying tasks sitting in the exact same list as genuinely actionable, validated tasks creates **backlog numbness** and destroys trust in the READY lane. 

Separating them into three distinct zones aligns with sound GTD / Kanban mechanics:
- **`NEW` (Triage Inbox):** Unprocessed, unconfirmed captures. The morning goal is to triage these to 0.
- **`READY` (Actionable Backlog):** Strictly fresh tasks confirmed within their review lease (e.g. 7 days). High confidence for pulling into Next / Today.
- **`ROTTEN` (Decaying Maintenance Queue):** Tasks whose review leases have expired, moved off `dash.md` into `rotten.md`.

---

### 2. Critique of Preprocessing with `bob task-status-hooks` to Add `#rotten` Tag
**Verdict: Strongly advised against. This is an architectural trap that reintroduces retired failure modes.**

Bryan considered using `bob task-status-hooks` to write a `#rotten` tag onto rotten task lines. While this seems intuitive from a naive Tasks filtering perspective, it has severe flaws:

1. **Repeats the `#now` Tag Failure:** Automated tag injection was trialed and decisively rejected in [`decisions:now-tag-is-user-owned`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/memory/decisions.md) and [`retire_now_sticky_lanes_ledger_today.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202609/retire_now_sticky_lanes_ledger_today/retire_now_sticky_lanes_ledger_today.md). A cron job modifying 10–30 notes weekly just because calendar days ticked over creates continuous git noise, dirty working trees, and merge conflicts with Obsidian Sync / iCloud.
2. **The Deletion Lifecycle Problem (Lag & Tool Explosion):** If `task-status-hooks` adds `#rotten`, who removes it?
   - When Bryan reviews a task in `rotten.md` and presses `Alt+F`, `Alt+F` stamps `[fresh:: 2026-10-01]`. If `Alt+F` does not strip `#rotten`, the task remains marked `#rotten` and stays visible in `rotten.md` until the next cron run (up to 15 minutes later), destroying the immediate tactile feedback of the morning review.
   - If `Alt+F` *does* strip it, then every single stamping surface (`bob-navigation-hotkeys`, `task-status-cycler`, `block-id-prompt`, `bob capture`, Vim bindings) must now contain tag-parsing and tag-deletion logic across multiple repositories.
3. **Mobile & Cross-Platform Incompatibility:** `task-status-hooks` runs as a cron job on desktop. It **does not run on iOS or iPadOS**. Tasks edited or viewed on mobile would not reflect updated `#rotten` tags until synced back to desktop.
4. **Violates SASE Architectural Invariants:** [`docs/freshness.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/docs/freshness.md) §4 explicitly states: *"Computed at read time, never stored."* Section 5 explicitly states that automation never touches freshness fields.
5. **Completely Unnecessary:** Obsidian Tasks already natively supports JavaScript predicates via `filter by function`. `bob-ledger-tools` is already loaded in Obsidian and memoizes freshness evaluation in sub-millisecond time.

---

### 3. The Recommended Alternative: Pure Read-Time Function Filtering

Instead of modifying note content on disk, leverage `bob-ledger-tools`' existing `api.freshness` namespace to expose clean, ergonomic helper predicates directly to Obsidian Tasks queries.

#### 1. In `bob-ledger-tools` (`plugins/bob-ledger-tools/main.js`):
Expose dedicated helper predicates under `api.freshness`:
- `isNew(task)`: `state(task) === "new"`
- `isRotten(task)`: `state(task) === "stale" || state(task) === "resurfaced"` (handling both rotten and unblocked deferrals)
- `isFresh(task)`: `state(task) === "fresh"`
- `isReady(task)`: `status.type === "TODO" && !isToday(task) && isFresh(task)`

#### 2. In `~/bob/dash.md`:
Update the section queries:
````markdown
### TODAY Tasks
```tasks
not done
filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) === true
sort by function (globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.todayRank?.(task) ?? 0)
```

### NEW Tasks
```tasks
status.type is TODO
filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.freshness?.isNew?.(task) === true
sort by created reverse
```

### PENDING Tasks
```tasks
status.type is IN_PROGRESS
filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) !== true
sort by created
```

### NEXT Tasks
```tasks
status.name includes Next
filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) !== true
sort by priority
```

### READY Tasks
```tasks
status.type is TODO
filter by function (globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.freshness?.isReady?.(task) ?? (globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) !== true))
```
````

#### 3. In `~/bob/rotten.md`:
Create `rotten.md` (or migrate `freshness.md`) with:
````markdown
```tasks
not done
filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.freshness?.isRotten?.(task) === true
sort by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.freshness?.rank?.(task) ?? 0
group by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.freshness?.tier?.(task) ?? "?"
```
````

**Benefits of this approach:**
- **Zero disk writes and zero git churn.**
- **Instant reactivity:** Pressing `Alt+F` in Obsidian immediately recalculates the task as `fresh`, causing it to instantly vanish from `NEW`/`ROTTEN` and appear in `READY`.
- **Identical behavior across Desktop and Mobile.**

---

### 4. Six Recommended Adjustments to Bryan's Requirements

1. **Adjustment 1 (Implementation Mechanism):** Do not use `task-status-hooks` or `#rotten` tags. Implement pure read-time filtering via `bob-ledger-tools` API helpers.
2. **Adjustment 2 (Account for `RESURFACED` Tasks):** Under [`docs/freshness.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/docs/freshness.md), deferred tasks whose scheduled date arrives today become `RESURFACED`. They are not fresh. If `rotten.md` only filters by stale tasks, resurfaced tasks become invisible orphans. `rotten.md` must encompass both `ROTTEN` (stale) and `RESURFACED` tasks.
3. **Adjustment 3 (Consolidate `freshness.md` and `rotten.md`):** Phase 31.9 recently created `~/bob/freshness.md`. Rather than maintaining two overlapping review notes, rename `freshness.md` to `rotten.md` (maintaining aliases `[Freshness review, Review]` so existing hotkeys and links continue to function).
4. **Adjustment 4 (Synchronize the `READY` Badge Budget):** In `bob-ledger-tools`, `readyCountFromTasks()` currently counts all 180 TODO tasks. If the section below only shows ~35 fresh tasks, the dashboard will look broken and contradictory. Update `readyCountFromTasks()` to count only fresh ready tasks.
5. **Adjustment 5 (Section Placement on `dash.md`):** Place `### NEW Tasks` directly between `### TODAY Tasks` and `### PENDING Tasks`. The natural Kanban flow becomes: `TODAY` (committed work) $\rightarrow$ `NEW` (unprocessed inbox) $\rightarrow$ `PENDING` (WIP) $\rightarrow$ `NEXT` (pull candidates) $\rightarrow$ `READY` (curated backlog).
6. **Adjustment 6 (Vocabulary Migration):** Adopt "rotten" immediately across all user-facing notes, chips, headings, and documentation, while retaining `"stale"` as an internal API alias so existing CLI JSON contracts (`bob freshness list -f json`) and unit tests do not break.

---

### 5. The Revised Morning Workflow

1. `bob gkeep pull` (brings in new captures).
2. Open `dash.md`: Triage `### NEW Tasks` directly on the dashboard using `Alt+Shift+F` (accept) or `Ctrl+Shift+P` (schedule/drop) until 0 new (takes ~2 minutes).
3. Check `ROTTEN` chip on `dash.md`: If count is high, click to open `rotten.md` and review decaying tasks. Tasks refreshed with `Alt+Shift+F` instantly vanish from `rotten.md` and enter `### READY Tasks` on `dash.md`.
4. Work `PENDING` $\rightarrow$ `NEXT`, pulling confident, validated tasks from `READY`.

For full implementation vectors, schema updates, and test plans, refer to the registered research report: [`ready_tasks_rotten_and_new_dash_architecture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/ready_tasks_rotten_and_new_dash_architecture__gem.md).
