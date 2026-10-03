# Chat History - ace-run (research.v.gem)

- **TIMESTAMP:** 2026-09-30 18:19:40 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.v.gem
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(gem, clan=research.v)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.v.cdx`, `research.v.cld`, `research.v.grk`, `research.v.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I'm
currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for context),
but there is still one major requirement that is unmet.

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).

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

I have completed the independent research and analysis for researcher `gem`.

The complete report has been written to:
[`task_freshness_review__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202609/task_freshness_review__gem.md)

And registered as a durable SASE artifact:
- **Ref:** `file:explicit:4492d053f5c53e32c0d33e4a`
- **Label:** `research:202609/task_freshness_review__gem.md`

Below is an executive summary of the research findings, critique, technical gotchas, requirement adjustments, and recommended solution.

---

### 1. In One Breath

> **The Diagnosis:** You are attempting to solve two fundamentally distinct problems with a single mechanism:
> 1. **Daily In-Basket Triage:** Glancing at tasks captured in the last 24–48 hours (such as a Google Keep voice note while speed-walking with your wife asking to pick up your daughter) so urgent commitments are never dropped.
> 2. **Rolling Backlog Grooming:** Keeping 186+ project tasks from rotting in a dormant `READY` backlog because you do not do a weekly review.
>
> **The Trap:** If you treat newly captured inbox tasks simply as "unfresh" tasks and pool them into a generic 7-day freshness review, you will face **~25 to 30 tasks to review every morning**. If you attempt to cope by capping that review to $N$ tasks per day (e.g. $N = 10$), **you will inevitably miss your daughter's pickup** whenever that note is sorted past item 10.
>
> **The Technical Landmine:** Obsidian Tasks' parser evaluates Dataview inline fields strictly from right to left against a hardcoded whitelist. Appending `[fresh:: YYYY-MM-DD]` at the end of a task line causes the parser to abort, hiding every `[scheduled:: ...]`, `[priority:: ...]`, `[id:: ...]`, and `[dependsOn:: ...]` field to its left from Obsidian Tasks, `bob query`, and the dash.
>
> **The Recommendation:** Decouple the workflow into two strict tiers:
> - **Tier 1: Daily Inbox (Zero-Tolerance, Uncapped, ~30 Seconds):** A dedicated `INBOX` section at the top of [`dash.md`](file:///home/bryan/bob/dash.md) isolating [`gkeep_inbox.md`](file:///home/bryan/bob/gkeep_inbox.md) and unfiled captures.
> - **Tier 2: Rolling Task Freshness (Anti-Rot, Paced, Capped):** Implement `[fresh:: YYYY-MM-DD]` placed *immediately after the task description* (before trailing Tasks metadata), with a 14-day default interval, project frontmatter and task-level overrides, automatic updates via supported keymaps (`Alt+N`, `Ctrl+Shift+P`, `Ctrl+Shift+]`, `Alt+[`/`]`), dedicated navigation/refresh keymaps (`Alt+F`), and a paced daily queue on [`dash.md`](file:///home/bryan/bob/dash.md) (capped at 10 items) to smoothly amortize weekly review work without morning fatigue.

---

### 2. Critique of the Proposed Plan

1. **The "Daily Cap Fatal Flaw" (Conflating Inbox with Backlog):**
   - **Inbox Triage** requires 100% review completeness every morning. Zero items can be dropped, because an inbox item might be a time-sensitive commitment for today.
   - **Backlog Review** has 186+ items, low urgency, and can be reviewed on a rolling basis.
   - If newly captured inbox items are simply treated as "unfresh" tasks and thrown into an out-of-date queue capped at $N=10$, an urgent Keep note ("Pick up daughter") sorted at position 12 will be truncated by the cap and completely missed.
2. **Morning Review Bloat & "Refresh Theatre":**
   - In a vault with 186 ready tasks and a 7-day refresh interval, steady-state expirations will produce $\approx 27$ tasks expiring every day, plus 2–5 new Keep captures.
   - Reviewing ~30 tasks every morning breaks the $\le 5$ minute morning review budget established in epic `bob-cli-2y`.
   - Faced with 30 tasks every morning, human nature leads to "refresh theatre" (rapidly mashing the refresh keymap without actually reading or evaluating the tasks).
3. **Metadata Clutter & Git Worktree Noise:**
   - 186 tasks refreshed every 7 days generates $\approx 800$ line modifications per month across 15+ project notes, cluttering vault Git sync history with date bumps.
4. **The Obsidian Tasks Parser Hazard:**
   - In [`src/native/dataview/tasks/task.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/src/native/dataview/tasks/task.rs) (and Obsidian Tasks plugin):
     The Dataview field parser evaluates trailing fields right-to-left and only recognizes a fixed whitelist (`priority`, `start`, `created`, `scheduled`, `due`, `completion`, `cancelled`, `repeat`, `onCompletion`, `id`, `dependsOn`).
   - If `[fresh:: YYYY-MM-DD]` is placed at the end of the line, the parser aborts on `fresh`. Every Tasks signifier to its left (like `[scheduled:: 2026-10-05]`) is ignored as a task attribute and dumped into description text. Scheduled tasks would immediately appear in `READY`!

---

### 3. Key Requirement Adjustments

| Initial Requirement | Recommended Adjustment | Rationale |
|---|---|---|
| **Inbox tasks treated as unfresh tasks in the general review queue** | **Decouple into Tier 1 (Inbox) and Tier 2 (Backlog Freshness)** | Guarantees that urgent new captures are never buried under 25 project backlog tasks or truncated by a daily review cap. |
| **Default 7-day freshness interval for all ready tasks** | **Increase default to 14 days for projects; 7 days for Areas; 3 days for Inbox** | A 7-day interval across 186 tasks forces ~27 tasks/day. A 14-day default halves the daily load to ~13 tasks/day, keeping morning review sustainable. |
| **Field placement unspecified (implicit trailing field)** | **Strict Field Ordering: place `[fresh:: ...]` immediately after description text, before Tasks trailing signifiers** | Prevents breaking Obsidian Tasks' right-to-left whitelist parser. |
| **Pacing as an optional fallback ("if it becomes a problem")** | **Pacing designed directly into the dashboard query ($N=10$ cap for Tier 2)** | Prevents review overwhelm from day one while keeping Tier 1 (Inbox) completely uncapped. |
| **Cold-start unspecified** | **Cold-start seed / staggered initialization** | Prevents Day 1 from confronting you with 186 out-of-date tasks simultaneously. |

---

### 4. Recommended Architecture

#### 4.1 Field Syntax & Placement
```markdown
- [ ] #task Pick up daughter [fresh:: 2026-09-30] [priority:: high] [created:: 2026-09-30] [scheduled:: 2026-10-01] ^block-id
```
- Placed immediately after body description text, before Tasks trailing signifiers.
- Tasks strips trailing fields (`scheduled`, `created`, `priority`), stops at `fresh`, leaving `[fresh:: ...]` cleanly inside `task.description`.
- Dataview scans the entire line and accesses `task.fresh` directly.
- Task override: `[fresh_interval:: 21d]`.
- Project override: Frontmatter `refresh_interval: 21` in `<project>.md`.

#### 4.2 Two-Tier Dashboard Structure in [`dash.md`](file:///home/bryan/bob/dash.md)
1. **Tier 1: `### INBOX Tasks` (Uncapped, Top of Dash):**
   ```tasks
   ### INBOX Tasks
   not done
   path includes gkeep_inbox
   filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) !== true
   sort by created reverse
   ```
   *Glance at this in 30 seconds. If Keep pulled something yesterday, you see it instantly.*
2. **Tier 2: `### FRESHNESS REVIEW Tasks` (Paced, Capped at 10):**
   ```tasks
   ### FRESHNESS REVIEW Tasks
   status.type is TODO
   path does not include gkeep_inbox
   filter by function globalThis.app?.plugins?.plugins?.["bob-ledger-tools"]?.api?.isToday?.(task) !== true
   filter by function {
     const desc = task.description;
     const match = desc.match(/\[fresh::\s*(\d{4}-\d{2}-\d{2})\]/);
     const freshDate = match ? moment(match[1], "YYYY-MM-DD") : null;
     const taskOverride = desc.match(/\[fresh_interval::\s*(\d+)d?\]/);
     let interval = taskOverride ? parseInt(taskOverride[1], 10) : null;
     if (interval === null) {
       const projProp = task.file.property("refresh_interval");
       interval = (typeof projProp === "number") ? projProp : 14;
     }
     if (!freshDate) return true;
     return moment().diff(freshDate, "days") >= interval;
   }
   sort by function {
     const match = task.description.match(/\[fresh::\s*(\d{4}-\d{2}-\d{2})\]/);
     return match ? match[1] : "1970-01-01";
   }
   limit 10
   ```
3. **Chip Widget:**
   - Add `INBOX` chip (colored dot/warning when > 0).
   - Add `FRESH` chip showing: `FRESH: 8 stale (4 refreshed)`.

#### 4.3 Obsidian Hotkeys (`bob-plugins`)
- In `bob-navigation-hotkeys`:
  - `refresh-task` (`Alt+F`): Updates or inserts `[fresh:: <today>]` at the description boundary on the current task line. Supports Vim counts (e.g. `3 Alt+F` to refresh 3 lines).
  - `jump-to-next-unfresh-task` / `jump-to-prev-unfresh-task` (`Alt+Shift+J` / `Alt+Shift+K`): Navigates through unfresh tasks in the active note.
  - Automatic updates hooked into `toggleTaskLane` (`Alt+N`) and `setBulletProperty` (`Ctrl+Shift+P`).
- In `task-status-cycler`:
  - Automatic updates on bullet-to-task promotions (`Ctrl+Shift+]`) and unblocking (`Alt+[` / `Alt+]`).

#### 4.4 SASE Memory Strand: `glossary:task_freshness`
Define `task freshness` as the property of an open ready task indicating when a human being last reviewed and affirmed it, specifying the 14-day default, override hierarchy, and auto-touch semantics.

---

### 5. Rollout Plan
1. **Day 0:** Add the `### INBOX Tasks` block to [`dash.md`](file:///home/bryan/bob/dash.md) immediately. This gives immediate relief for the Google Keep speed-walking scenario without requiring new code.
2. **Day 1:** Run a cold-start seeding script across existing project tasks that staggers initial freshness dates across the past 14 days, avoiding an immediate 186-task avalanche.
3. **Day 2:** Deploy the `bob-plugins` keymaps (`Alt+F`, auto-touch hooks) and the `FRESH` chip widget on [`dash.md`](file:///home/bryan/bob/dash.md).
4. **Day 3–14:** Two-week trial measuring that Tier 1 (Inbox) takes $\le 1$ min and Tier 2 (Freshness) takes $\le 3$ min, keeping the total morning review comfortably within $\le 5$ minutes.
