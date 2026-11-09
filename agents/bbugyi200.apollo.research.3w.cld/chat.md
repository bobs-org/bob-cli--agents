# Chat History - ace-run (research.3w.cld)

- **TIMESTAMP:** 2026-11-09 09:39:50 EST
- **MODEL:** claude/opus
- **AGENT:** research.3w.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_092439.md`

## Prompt

%id(cld, clan=research.3w)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.3w.cdx`, `research.3w.grk`, `research.3w.mus`, `research.3w.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to improve the way that we handle done notes with the goal of fixing any
existing bugs, making their management more reliable and intuitive, and making other
improvements where possible and desirable (think hard about what improvements we could
make that I would most likely find useful). I think we use `done/<name>_done.md` files
currently, which works OK I guess. I'm just curious how other systems handle this and
whether there is a better way to approach this problem.

Can you do some research with the goal of helping me with this? End your analysis with a
recommended set of changes that you think I should consider making (or recommend no
changes). 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

Reading the `bob task archive` (collect_done) module to map how done notes are produced today; next I'll check the planner, link repair, docs, and the live vault, then survey other systems.

Now the nightly integration and the places that read done notes elsewhere.

Found a real orphaned archive in the live vault (a renamed daily note left its `_done` file behind); checking how the source and archive point at each other now.

Confirmed two structural issues in the mover (open children ride along with a done parent; a done child is detached from its open parent). Checking the live archive for evidence of each.

Checking whether daily notes (which hold Event Tasks and the Pomodoro ledger) are eligible for archiving and how close they get to the threshold.

Next: the vault-sync loss detector and the Obsidian plugins' view of `done/`, then the external survey.

Surveying how the vault's own queries and dashboards treat `done/`, then the git history of archive runs.

Mapping how terminal projects are treated (55 finished project notes still sit at the vault root), then I'll do the external survey.

Codebase and live-vault mapping is mostly done. Moving to the external survey (org-mode, todo.txt, TaskPaper, Things, OmniFocus, Taskwarrior, Linear, Obsidian archiver plugins).

Survey is in hand. A few final live-vault checks (block-ID renames in archives, archive ordering by completion date, stale counts) before writing.

Writing the report next. One last look at the archiver's own fix history so I don't re-report already-fixed bugs.

Evidence gathering is complete. Writing the report now.

Report written. Registering it as a durable artifact now.

Registration succeeded. Finalizing the turn.

I recommend keeping the `done/<name>_done.md` layout and changing the rules around it. The report is saved and registered as an artifact.

**Why the layout is fine.** Org mode's default archive is the same kind of per-note sibling file; its manual's own example is `%s_done`. Bob identifies tasks by note path plus block ID, and every project note uses `^prj`. A single shared done log would make all those `^prj` IDs collide. About 20 readers (stats, period reviews, task dependencies, relations, link repair) also rely on each note mapping to exactly one archive.

**Bugs and sharp edges I found:**
- **Open subtasks get archived (not seen in the vault yet).** Closing a parent task leaves its open subtasks open on purpose, but the archiver then moves the whole block. The subtasks land in `done/`, which reconcile, plan and every lane skip, so they are never seen again.
- **Done children of open parents get detached (not seen in the vault yet).** The child is moved with its indentation intact, so in the archive it nests under whatever task was archived just before it.
- **Renaming a note orphans its archive (one real case).** The archiver pairs notes by filename, although the real link is in frontmatter (`done_tasks:` / `parent:`). `done/2026/20260528_day_done.md` was orphaned by the daily-note rename, and stats now credit its 21 tasks to a note that doesn't exist.
- **Daily notes can be archived (not seen recently).** Only the 10-task threshold protects them; recent days peak at 4 closed tasks. A day with 10 or more closed tasks, meetings included, would have its Events moved to `done/`. `bob gcal` would then tombstone those rows as "removed by you".
- **The count threshold behaves inconsistently.** `bob.md` is cleared every night. Meanwhile 104 quieter notes hold 469 closed tasks, 289 of them closed more than 30 days ago. Every other system I looked at archives by age or on demand, never by a per-file count.
- **No safety net.**
  - Running `bob task archive` by hand takes no lock.
  - There is no stale-file check, rollback or dry-run.
  - It writes the archive before the source note, so a failure in between can duplicate tasks.
  - About 26 separate checks of "is this path in `done/`?" follow at least four different rules.
  - A task reopened inside `done/` vanishes, and there is no way to restore it.

**Recommended changes, in order:**
1. Archive a task block only when no parent task is open and nothing under it is still open (Linear and Org use the same guard).
2. Archive only area, project and inbox notes, never daily, period, reference or mail notes.
3. One shared "is this in `done/`?" check for Rust and the plugins, with shared test cases. Fix the orphaned archive by hand.
4. Run the command through the existing `vault_rewrite` transaction (lock, stale check, rollback, one commit), and add `--dry-run` and `--format json`.
5. Replace the count threshold with an age rule: archive tasks closed 7 or more days ago. This changes behaviour, so it needs a decision record.
6. Pair notes through frontmatter and rename the archive when its source is renamed; group archive entries under month headings.
7. Later: an unarchive command, a source-side "archived" link, and possibly archiving finished projects as whole notes. That last one needs its own research first.

The report includes acceptance test cases DA1–DA12 and a table comparing Org, the Obsidian Archiver plugin, TaskPaper, todo.txt, Things/Nirvana, OmniFocus, Linear and Taskwarrior.

**Not verified:**
- Things 3's exact Logbook settings: their support site blocked access.
- The two subtask bugs come from reading the code and test fixtures; I didn't run the archiver on a test vault, and neither has happened in the live vault yet.
- That links break after restoring a task by hand is inferred from the code, not reproduced.

**Files:**
- Report: `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202611/done_notes_archive_lifecycle__cld.md`
- Artifact `explicit:f1dff67a04101e737d78751d`, label `research:202611/done_notes_archive_lifecycle__cld.md`. The research repo commit is declared and will land after this turn.
