# Chat History - ace-run (research.39.cld)

- **TIMESTAMP:** 2026-10-01 16:49:29 EDT
- **MODEL:** claude/opus
- **AGENT:** research.39.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_161410.md`

## Prompt

%id(cld, clan=research.39)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.39.cdx`, `research.39.grk`, `research.39.mus`, `research.39.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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

I'm reading bob-cli's plan, projects, and freshness docs so I can see how READY is defined today. Next I'll look at the vault and the Obsidian plugins.

I've opened the plugins repo and the vault. Now I'm looking at the dash, the project/area notes, and how the READY badge is rendered.

Right now I'm pulling live per-file READY counts from the vault with `bob query`, so the design rests on real numbers.

Live data so far: 210 READY tasks across 29 files, and 7 files are over 5. Next I'm checking which Obsidian keymaps move tasks between notes, and how the ledger-tools READY badge and Notices work.

Both plugin surveys are back. Now I'm checking whether the move keymaps stamp freshness, how `bob capture` reports budgets, and whether `gkeep pull` rewrites frontmatter.

I'm checking earlier, unrelated research for any past discussion of per-project caps, reading it through the audited artifact reader.

I have what I need from the code. Last data step: modelling how many notes go over, and the total excess, at different caps.

One more thing before writing. The ledger-tools survey flagged two possible bugs in code this feature would build on. I'm checking both quickly so I report them accurately.

No duplicates or related epics turned up. I'm filing the two bugs now, then writing the report.

Beads `bob-cli-3d` and `bob-cli-3e` are filed. Now I'm writing the report.

Report written. Quick fact-check of a few numbers in the mocks (line numbers and parents) before registering it.

The label resolves. Now the final declaration.

I've written the report and registered it as `research:202610/per_note_ready_cap_crowded_notes__cld.md` (the label resolves).

**Is it a good idea?** Yes, as long as it limits *where* tasks pile up, not *how many* there are. Your global READY cap (100) already limits the total. A per-note cap points at the exact note that needs splitting or deferring. It matches Shape Up's rule that a list of more than "three to five" loose items means a new scope is needed, and it works like a Kanban per-lane limit.

**What the live vault shows today (N = 5):**
- **4 notes are over:** `sase` 60, `sase_remote` 11, `sase_pager` 7, `sase_usage` 7.
- **3 are exactly at the limit:** `bob`, `cash`, `sase_bug_bash`.
- **65 tasks are over the limit, and 55 of them are in `sase.md`.**
- `gkeep_inbox` (65) and `sase` (60) hold about 60% of all ~210 READY tasks.
- N = 3 would flag 9 notes; N = 7 would flag only 2. So 5 is a good default.

**Requirement changes I made:**
- **"Ready" means the dash's own READY**, grouped by the note that holds each task. A muted "+k in review" shows NEW/ROTTEN tasks in that note. Ctrl+Shift+M and Alt+N already stamp freshness, so a moved task counts the moment it lands.
- **Inbox notes are exempt** via a `ready_cap: off` property. Recurring tasks don't count.
- **Per-note override** with a `ready_cap:` frontmatter property; config key `plan.max_ready_per_note: 5`.
- **Three states:** crowded (over the cap), full (at it), room (under). "Full" is your "already has ≥ N" case, made visible before you move a task.
- **Soft limit everywhere:** nothing is refused, and toasts also say when a note gets back under its cap.
- **The move picker shows each note's count**, so you can avoid crowding a note in the first place.
- **The CLI needs a READY count in Rust.** `docs/plan.md` currently says there isn't one, so this needs a new decision record.

**Recommended solution:**
- **`bob ready`:** a new command with a colored bar chart grouped crowded / full / room. `bob ready <note>` lists that note's READY tasks.
- **`bob plan`:** adds `READY n/100 · CROWDED k` and one summary warning.
- **`dash.md`:** a CROWDED chip next to READY that opens a new `crowded.md` view listing which notes are over.
- **Each area/project note:** a live `READY 7/5` chip on its `## Tasks` heading.
- **Toasts:**
  - Ctrl+Shift+M and Alt+N show the destination's count.
  - Ctrl+Shift+P shows your progress ("↓1", "✓ back to 5/5").
  - A watcher in Bob Ledger Tools catches everything else in the note you're editing, especially confirming NEW tasks with Alt+F / Alt+Shift+F. That is where most tasks enter a note's READY count.
- **Before the trial:** spend one session splitting `sase.md`, or the CROWDED chip will stay red indefinitely.

**Open questions for you:**
- Do you want to clear `sase.md` in one triage session (my recommendation), or give it a temporary `ready_cap: 20`?
- Should areas use the same default of 5 as projects? I'd say yes.
- Are you happy with the name "CROWDED"?

While researching I found two bugs in the Bob Ledger Tools plugin and filed them:
- **`bob-cli-3d`:** the dash PENDING/NEXT badges lose their own color class and render in READY's blue.
- **`bob-cli-3e`:** the plugin reads `task_refresh` with the wrong lookup call, so note-level freshness intervals never apply in Obsidian. No note uses `task_refresh` yet, so nothing is visibly broken today.

I submitted the final declaration; the host commits the report after this turn.
