# Chat History - ace-run (research.v.cld)

- **TIMESTAMP:** 2026-09-30 18:36:03 EDT
- **MODEL:** claude/opus
- **AGENT:** research.v.cld
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(cld, clan=research.v)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.v.cdx`, `research.v.grk`, `research.v.mus`, `research.v.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

I'm reading the epic plan and its research report to ground the freshness design in the current lane model.

Now inspecting the vault's dash, task-line fields, project frontmatter, and where `bob gkeep pull` lands tasks.

Pulling stats on the 186 Ready tasks (per-project counts, capture rate, recurring tasks) to size the daily review load.

Next I'll check bob-cli's task-field helpers and the Tasks parser to see where a new inline field can sit on a task line, and open bob-plugins to inventory the keymaps.

I'm fanning out two read-only searches (bob-plugins keymaps and bob-cli task write paths) while I check the capture grammar and project-note frontmatter myself.

Both inventories are back. Checking the second inbox (`mac_inbox.md`), project-note frontmatter, and September capture rates to size the review load.

Stamping must be placed before `[created::]` (both Tasks and the hooks parse fields from the end of the line). Checking for keybinding conflicts and the CLI rules before I draft the recommendation.

Verifying a few load-bearing claims: the hooks parser's end-of-line behavior, the display-text stripping, and current lane counts.

I have what I need. Checking the output path is free, then writing the report.

Replacing the HTML lists in the "Where the code lives" table with plain Markdown for consistency.

Registering the report as a durable artifact.

Registration succeeded. Now the final declaration.

I wrote the report to `sase/repos/research/202609/task_freshness_rolling_review__cld.md` and registered it as `research:202609/task_freshness_rolling_review__cld.md` (artifact `explicit:fdb2184679171ab4647b33f4`). The research repo commit happens after this turn.

**Verdict: build it.** Walking Ready every morning meant about 186 glances a day. A 7-day freshness date cuts that to about 27 a day plus new arrivals, and every new capture is still guaranteed a glance. The design works because "never reviewed" is a state (no date yet), not a time window. A "created since yesterday" view wouldn't work: `bob gkeep pull` sets `created` to the date you wrote the Keep note, not the date you pulled it, so late pulls and skipped mornings would slip through.

**Adjustments I recommend (marked ADJ in the report):**
- **Where the field goes matters.** `[fresh:: …]` has to sit before `[created::]`. Tasks, bob-cli's own Tasks engine and `bob task-status-hooks` all read fields from the end of the line and stop at the first one they don't recognise. Every current writer adds new fields at the end, so written that way `fresh` would hide `scheduled` and `priority`, and Blocked would stop working. `bob highlights` already puts its `[h:: …]` field in the safe spot.
- **Only human gestures update the date; automation never does.** When a task leaves Blocked on its own (its scheduled date arrives or a dependency closes), it isn't marked fresh. Instead it simply counts as due that day, like a tickler file. The hooks keep making single-character status edits.
- **Two queues.** Never-reviewed tasks must be cleared every morning and are never capped. Your "only N a day" fallback may only limit the stale queue; otherwise it would quietly drop new captures.
- **Cover Next and Pending too, not just Ready.** Since the sticky-lanes change, nothing leaves those lanes on its own. The gestures that work a task keep its date current, so only neglected lane tasks come up. That makes it the weekly prune done in daily slices, and you could drop the weekly prune chore.
- **New tasks never start fresh, however they were captured.** That's what "glance at every task I captured yesterday" requires.
- **The first day needs setup.** About 250 tasks have no date yet. I'd backdate them across 7 days, grouped by note, so each morning brings a few whole projects due.
- **Review happens in the notes themselves.** New keys: `]s`/`[s` jump to the next/previous due task anywhere in the vault; Alt+F marks the current task fresh; Alt+Shift+F marks it fresh and makes it come back less often. A status bar item shows `⟳ 23 due · 3 new · ✓ 12 today`. All these keys and the vimrc slots are currently unbound.

**The main risk is daily load, not the mechanics.** About 250 tasks in scope, plus about 14 captures a day and 6–17 deferred tasks returning a day, comes to roughly 35–50 reviews a day at first. Reach for these before a daily cap:
1. Defer with P-levels during the review.
2. Use Alt+Shift+F, or set `task_refresh: 14d` in the frontmatter of big notes like `sase.md`.
3. Only then cap the stale queue.

**Recommended order, after the `bob-cli-2y` rollout:**
1. Define the rules in a new bob-cli doc (`docs/freshness.md`) with shared test cases, a `bob freshness` command, and counts in `bob plan`.
2. bob-ledger-tools and bob-navigation-hotkeys: the review keys, the status bar and a REVIEW section on the dash.
3. Backfill the dates, after a dry run you approve.
4. Make every keymap and `bob capture` gesture update the date. Until then a missed update only means reviewing a task one extra time.
5. Add the glossary term and a decision record.
6. Run a two-week trial.

Bob Mac Capture needs no changes.

I didn't edit memory: the glossary entry and decision record are drafted in the report, to add once you settle these questions:
- Should the review cover Next and Pending, or only Ready?
- Should desk captures start fresh?
- Should deferred tasks be due on the day they come back?
- Should the inbox notes get a shorter interval?
- Are the names `fresh`, `refresh` and `task_refresh` right?
