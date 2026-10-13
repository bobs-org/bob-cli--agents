# Chat History - ace-run (research.11.cld)

- **TIMESTAMP:** 2026-10-13 08:45:27 EDT
- **MODEL:** claude/opus
- **AGENT:** research.11.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261013_081833.md`

## Prompt

%id(cld, clan=research.11)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.11.cdx`, `research.11.grk`, `research.11.mus`, `research.11.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Instead of automatically adding successor task links to the current / next pomodoro, I
would like to start prompting the user which unblocked tasks (if any) they would like to
pull in as successor task links when completing a task that blocks other tasks (via any
supported method).

- I'm not sure what the UX should look like for this but I was thinking that the user
  should be able to easily select one or more unblocked tasks from one or more new
  panels (we'll probably need a custom / separate solution for the bob-mac-capture app,
  but you should verify this is needed).
- I think we have a limit currently where we only pull in at most 5 successors. That
  limit should be gone now since the user can pick them explicitly.
- As a part of this change, when a task unblocks a project task that has open tasks, the
  new panel that pops up should include all open tasks that belong to that project
  (which should also been unblocked by closing the task the project depended on). I
  thought we did this already, but just tried this by closing the ^bar task in the
  ~/bob/sase.md file and it did not pull in the (non-project) tasks contained in the
  ~/bob/sase_foo.md project note as successors as I expected.
- This change should also apply to the project tasks / parent project tasks we pull in
  as successors when closing the last open task / sub-project for a project.

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
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Reading the governing decisions and glossary before I dig into the code.

Confirmed what happened in the vault: closing `^bar` brought `sase_foo`'s `^prj` and both residents back to `[ ]`, but linked nothing. Next I'm checking the day file and the code paths.

Surveys are back. Now I'm checking the capture grammar for a free selection syntax, the CLI rules memory, and the current vault numbers.

Confirmed the resident-recovery code: residents keep their predecessor but get no anchor, so they can never be linked. Now checking freshness stamping rules for linked tasks.

Found a live case: `^post-blog-prj` was closed this morning with 11 dependents, so the breaker linked none of them. Confirming in vault history.

Writing the report now.

Report written. Spot-checking two claims from the survey before registering it.

Both verified. Registering the artifact.

Registered. Now the final declaration.

My report is at `sase/repos/research/202610/successor_pull_in_picker__cld.md` and is registered as `research:202610/successor_pull_in_picker__cld.md`. My recommendation: build the picker. The vault history from this morning backs that up.

**Why your `^bar` test linked nothing.** This isn't a bug; it's what the spec says. Closing `^bar` did unblock `sase_foo`: the `^prj` and both tasks went from `[?]` to `[ ]` and lost `#prj_is_blocked`. But nothing was linked, for two reasons:
- The project's own tasks are only ever unblocked, never linked. That is the written rule (`docs/task-dependencies.md` §12.2), and the `unblocked-tasks-resurface-as-ticklers` decision record explicitly rejected linking them. So we never did this; changing it needs a new decision record.
- `sase_foo` still had open tasks, so its `^prj` didn't count as an emptied project and wasn't pulled in either.

**The 5 limit is all-or-nothing.** If more than 5 tasks qualify, it links none; it doesn't link the first 5. It already went off for real today: at 07:59 a close completed `^post-blog-prj`, which had 11 dependents, and nothing was linked. Within 3½ minutes you linked two of them by hand, one under JOB and one under SASE. So the picker needs to let you pick a few out of many, and to send a pick to a different Pomodoro than the closed task's.

**The Mac app needs its own panel, but not a separate mechanism.** The panel hides as soon as a capture succeeds, and nothing in the app can select more than one row. But `bob` already works out the unblocked tasks during the live preview, before you press Return. So:
- A multi-select picker can open on Return, write your choice into the draft (e.g. `!sase:bar>1,3`), and submit once.
- That keeps it to one atomic `bob capture` call and keeps the app a thin client.
- It reuses existing patterns: the task-ID prompt that blocks submit, and the numbered-row hint "Type ~2 to drop task 2".

**Recommended design:**
- **Unblocking stays automatic; only the link becomes a choice.** Tasks still go from Blocked to Ready, and the project tag is still removed. Dismissing the picker links nothing, which is safe because the next morning's review already brings every unblocked task back up.
- **What gets offered:**
  - direct dependents the close fully unblocked, as today;
  - every open, visible, unblocked task in a project the close unblocked (the `sase_foo` case);
  - the `^prj` pull-ins when a close empties a project.
- **The limit is deleted** in both Rust and the plugins.
- **In Obsidian**, the picker opens after the close has been written. It uses the same keys as the Depends on picker: ⇥ marks a row, ↵ links the marked rows (or just the highlighted one), Esc links nothing. During a `]s` walk it doesn't open; the walk's toast names a "Pull in unblocked tasks…" command that reopens it.
- **On the CLI and the Mac**, a new `>` suffix picks offers: `>` takes all, `>0` none, `>1,3` those rows, and `>2#job` sends row 2 to the JOB session.
- **A picked task is treated like a manual link** (Ctrl+Shift+Enter): it becomes Next, gets a block ID if it lacks one, and gets a `[fresh::]` stamp. Each pick can choose its own Pomodoro.

**Changes to your requirements I'm proposing:**
- **Sub-project tasks are left out of v1.** Closing doesn't unblock them until the next reconcile, and an existing decision rejected changing that.
- **Cancels still never offer anything.**
- **Closes of tasks not on today's plan also offer**, with the current or next Pomodoro as the destination.
- **The `plan.link_unblocked` setting becomes `ask` or `off`.** There's no "auto" mode in v1.

The report has a four-phase plan:
1. the docs contract;
2. Rust;
3. the plugins, which can run alongside phase 2;
4. the Mac app, once phase 2's output format is fixed.

It also lists open questions. The one that most needs your call is whether the one-to-one hand-offs should come pre-selected. I recommend not.

While researching I found some small bugs; the report lists them, and I didn't file task beads for them:
- The Mac app shows the raw text "project_member" instead of proper wording.
- The Mac app ignores the `trigger` field that marks project pull-in rows.
- Two spots in the docs have drifted from the code.
