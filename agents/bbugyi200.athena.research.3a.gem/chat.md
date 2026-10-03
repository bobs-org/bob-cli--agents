# Chat History - ace-run (research.3a.gem)

- **TIMESTAMP:** 2026-10-01 17:27:19 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3a.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_171714.md`

## Prompt

%id(gem, clan=research.3a)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3a.cdx`, `research.3a.cld`, `research.3a.grk`, `research.3a.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We
recently seeded the `fresh` property for all ready Obsidian tasks with fake freshness
dates in order to chunk these up a bit so I am not overwhelmed. I don't think we'll need
to do that anymore if we refine my morning GTD review process a bit more.

- Namely, the `[s` / `]s` and `<ctrl+alt+j/k>` keymaps should always walk through new
  tasks first, then pending tasks, then next tasks, and then ready tasks in order based
  on which ready tasks have the lowest refresh interval and then (if refresh intervals
  are equal) based on which was refreshed earlier (i.e. is more overdue) and then (if
  they have the same `refresh` property value) based on which was created later. For
  example, we should review a task with a 1d refresh interval before we review a task
  with a 7d refresh interval that is 1d overdue but we should review a task with a 7d
  interval that is 3d overdue before that one and we should review a task with a 7d
  interval that is 3d overdue but was created a few days later even sooner .
- We should also change the way refresh intervals are determined by adding new
  configuration fields that control the refresh interval used for pending/next tasks.
  Also, any task that has a `scheduled` property should have a default refresh interval
  that is configurable as well. All of these should default to 1 (i.e. they need to be
  refreshed every day--in the case of scheduled tasks, this just means they need to be
  refreshed on the day they are due).
- This should have the effect of me always reviewing my new tasks, pending tasks, next
  tasks, due scheduled tasks, and other ready tasks in that order.
- Once that is done, we should remove all of the artificial `refresh` properties that we
  added previously.

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

The independent research report has been completed and registered as a durable artifact.

### Executive Overview & Critique of the Plan

#### 1. Is this a good idea?
* **The Goal is Outstanding:** Unifying the morning GTD review sequence into a single seamless keyboard walkthrough (`[s` / `]s` and `<Ctrl+Alt+J/K>`) traversing **NEW $\to$ PENDING $\to$ NEXT $\to$ DUE SCHEDULED $\to$ OTHER READY** matches the visual structure of your dashboard (`dash.md`) and the GTD review ritual. Today, you are forced to use `]s` for NEW/ROTTEN tasks but manually switch context to visually scan PENDING and NEXT.
* **The Proposed Mechanism is Problematic:** Attempting to force this sequence by assigning an artificial refresh interval of $1\text{d}$ to PENDING, NEXT, and SCHEDULED tasks conflates **Kanban execution lanes** with **backlog freshness hygiene**. Doing so would permanently pollute whole-vault metrics: the status bar and the dashboard `ROTTEN` chip would scream with dozens of "rotten" tasks every morning, even though they represent active, healthy WIP.
* **Scheduled Tasks Already Have Native "Due Today" Semantics:** Tasks with a `scheduled` date automatically transition to `RESURFACED` as soon as their date arrives. Under existing semantics, `RESURFACED` tasks are *already* due immediately on the arrival date. If you assign them a $1\text{d}$ refresh interval, then once confirmed on their due date, they will become ROTTEN *every single day thereafter* until completed, inducing severe review fatigue.
* **The Sorting Contradiction in Ready Tasks:**
  There is a direct mathematical contradiction between your stated sorting rule and your accompanying example:
  * *Stated Rule:* Sort by lowest refresh interval first, then earlier fresh date, then created later (`interval ASC, fresh ASC, created DESC`).
  * *Accompanying Example:* A $7\text{d}$ task that is $3\text{d}$ overdue must come *before* a $1\text{d}$ task, but a $1\text{d}$ task must come *before* a $7\text{d}$ task that is only $1\text{d}$ overdue.
  * Under the stated rule (`interval ASC`), a $1\text{d}$ task *always* comes before a $7\text{d}$ task regardless of overdue days. Your example demonstrates that your actual intuition prioritizes **overdue urgency** over raw interval length.

---

### Key Adjustments to the Requirements

1. **Decouple Morning Review Navigation from the Freshness Bucket Contract:**
   Implement an explicit **5-Stage Morning Review Queue** in `bob-ledger-tools` and `bob-navigation-hotkeys`:
   * **Stage 1 (NEW):** Inbox captures without stamps (process to zero).
   * **Stage 2 (PENDING):** Active WIP (`[/]`) — review active work, link to today's Pomodoro, or release (`Alt+N`).
   * **Stage 3 (NEXT):** Committed pool (`[*]`) — pull into today's ledger (`Ctrl+Shift+Enter`) or release (`Alt+N`).
   * **Stage 4 (DUE SCHEDULED):** Resurfaced tasks due today or earlier (`scheduled <= today`).
   * **Stage 5 (ROTTEN READY):** Aging Ready backlog tasks (`[ ]`).
   * *Benefit:* Delivers 100% of your desired walk order without corrupting `counts.rotten`, the `ROTTEN` dashboard chip, or `rotten.md`.
2. **Preserve `RESURFACED` Semantics for Scheduled Tasks:**
   Keep scheduled tasks in their native `RESURFACED` state and place them in Stage 4. This guarantees they are reviewed before general Ready backlog tasks on the day they are due, without turning them into daily recurring chores.
3. **Reconcile Ready Backlog Sorting with a Tiered Escalation Sort:**
   In Stage 5 (Rotten Ready), partition tasks into:
   * **Escalated Overdue:** Tasks overdue by $\ge 3\text{d}$ (or $\ge 50\%$ of interval).
   * **Standard Rotten:** Tasks overdue by $< 3\text{d}$.
   Within each sub-tier, apply your rule: `(interval ASC, fresh ASC, created DESC)`. This faithfully produces your exact narrative example (`7d 3d overdue` $\to$ `1d` $\to$ `7d 1d overdue`).
4. **Decommission Artificial `refresh` Properties:**
   Provide a safe, automated dry-run cleanup tool (`bob task cleanup-refresh --dry-run`) to canonically strip artificial `[refresh:: N]` properties from Ready tasks while preserving intentional human overrides (e.g. `[refresh:: 30]`).

---

### Durable Snapshot Registration

* **Report File:** [`morning_review_walk_order_and_freshness_refinement__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/morning_review_walk_order_and_freshness_refinement__gem.md)
* **Artifact Ref:** `file:explicit:78f3de39af83fc7e51052b51`
* **Artifact Label:** `research:202610/morning_review_walk_order_and_freshness_refinement__gem.md`

The SASE finalizer declaration has been successfully submitted for the required commit payload covering `202610/morning_review_walk_order_and_freshness_refinement__gem.md`.
