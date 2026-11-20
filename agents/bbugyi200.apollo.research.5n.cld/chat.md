# Chat History - ace-run (research.5n.cld)

- **TIMESTAMP:** 2026-11-20 16:42:18 EST
- **MODEL:** claude/opus
- **AGENT:** research.5n.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261120_160058.md`

## Prompt

%id(cld, clan=research.5n)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.5n.cdx`, `research.5n.grk`, `research.5n.mus`, `research.5n.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add much better (and explicit) support for "micro tasks".

- A "micro task" is a sub-bullet on an Obsidian task that would be converted to a task
  in the new project file if its parent task were converted to a project (e.g. via the
  `<ctrl+shift+alt+n>` keymap).
- We currently consider any sub-bullet that does not belong to a drawer to be a micro
  task (though we don't use this term yet).
  - We should instead start treating these bullets as if they were placed in a "NOTES"
    drawer and require that micro tasks be marked as such explicitly.
  - Any notes added to a task via captures (using the `@foo+bar` capture syntax, for
    example) should be added to the NOTES drawer by default unless another drawer is
    explicitly specified or a micro task marker is specified in the capture.
- I was thinking that we could either use a `TASK:` or `#task` prefix for these
  sub-bullets to mark them as micro tasks, but this is just my first thought. Think hard
  about the best way to mark these.
- We should support nested micro tasks (i.e. micro tasks with micro task parents).
- Regardless of how we decide to mark micro tasks, the mark should be rendered in a
  consistent and concise way. I was thinking we could render 2 or more `#` characters
  (depending on the micro task nesting level) for this micro task marker.
- It needs to be very easy to specify micro tasks in the capture panel. I was thinking
  that we could use `..` as a capture alias for the micro task marker (so `- ..` would
  be converted to `- #task `, for example) and add a new `<ctrl+g>t` keymap that toggles
  the micro task prefix for the current bullet.
- Top-level (i.e. `##`) micro tasks should show up as successors, which are closed by
  default, when their parent task is closed.
  - The user can decide to open these tasks using the `<ctrl+x>` keymap on the successor
    panel, in which case a new Obsidian task should be created for that micro task. The
    micro task bullet in the original task should be crossed out and an appropriate note
    should be placed next to it that links to the original parent task.
  - After opening a micro task successor, the user can also check it (e.g. using the
    `<space>` or `<tab>` keymaps), in which case the new task that is created should
    have a task link added to today's daily file (i.e. it should be pulled in).
  - The user can also canel a micro task successor using the `<ctrl+shift+x>` keymap, in
    which case the micro task sub-bullet should be striked out after closing the parent
    task (to indicate that it was not complete).
  - All non-top-level micro tasks (e.g. `###`, `####`, etc...) should still show up on
    the successor panel but should not be actionable since their status will be
    deteremined by whatever status we decide to give their parent micro task.
- When we merge a task into another task using one of the configured `merge_labels`, we
  should start creating a new micro task in the target task that represents the source
  task. I think this should just involve adding the microtask marker but there might be
  more work involved.
- As a part of this change, we should add an excellent new glossary term for "micro
  task".
- The Goals of this Change
  - Micro task successors will help me make sure that I've really completed all of the
    work that a task commits to before closing it.
  - I would like to soon make it possible to convert any project (regardless of how
    complex) into an equivalent task. This is out of scope for this research report but
    is a motivating factor, since this change will make it possible to convert
    sub-projects into equivalent micro tasks.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Reading the glossary terms on drawers, successors, merges and captures before I dig into the code.

Now locating the task-to-project promotion code and the successor panel across bob-cli and bob-plugins.

Reading the promotion command's code to see how sub-bullets become project tasks today.

Promotion is in the bob-navigation-hotkeys plugin; reversal leaves nested `#task` checkboxes. Now checking the live vault for how sub-bullets are actually used today.

Most Rust task parsers gate on the `#task` filter, so plain checkboxes aren't tasks there. Next: capture note grammar, merge, split, and tag-mark rendering docs.

Split already treats an unchecked `- [ ] text` (no `#task`) as splittable into an open task. Now checking capture alias rules at bullet starts and the Mac panel's Ctrl+G keymaps.

Capture's same-line `@foo+bar` notes and authored bullets are clear now. Next I'm trying read-only `bob capture-parse` and dry runs to see how a `- [ ]` bullet behaves today.

The cycler treats any checkbox as a status-cyclable line (that's why a bank-row guard exists), so micro tasks will need the same kind of guard. Reading the offer reporting model next.

Promotion already maps a checkbox child to a task with its status preserved. Checking what bob-ledger-tools' existing "progress marks" are, since a micro progress chip could reuse them.

Checking prior art (Things checklists, org-mode checkboxes, Bullet Journal migration) to ground the marker choice.

Checking which short flags `bob capture` already uses, for the CLI side of micro-task verdicts.

Now quantifying what today's 243 loose sub-bullets actually are, to size the "everything is a micro task" error rate.

I have what I need from the code. Loading the diagram skill before adding a state figure to the report.

The lifecycle figure renders at 747×480 (87% fit) and reads cleanly. Writing the report now.

Report written. Verifying two claims: that `-t` is free on `capture-rewrite`, and that the files I cite exist.

All verified. Dropping the uncited Todoist source, then registering the artifact.

Artifact registered. Now the final declaration.

I wrote the report and registered it as `research:202611/micro_tasks_as_checkbox_steps__cld.md`. The host commits it to the research repo after this turn.

**Verdict:** the idea is sound and overdue. Of about 245 loose sub-bullets on 166 open tasks, at most 51 (about 21%) even start like a step. The rest are notes, images, Gmail links, questions and "Merged from:" lines. Today, promoting a task to a project turns every one of them into a `#task`, images included.

**Main recommendations:**

- **The marker should be a plain Markdown checkbox with no `#task`**, rather than a `TASK:` or `#task` prefix. Example: `- [ ] Write the parser`, as a child of a task or of another micro task.
  - The checkbox stores state: `[ ]` open, `[x]` done, `[-]` not done, `[>]` carried to its own task.
  - Neither prefix can store state, so neither could represent "done step under an open task". That case is exactly what converting a project back into a task needs.
  - `- #task` would collide with capture's `- #…` drawer shortcut (`tasks` is a reserved drawer name) and with every tag query. `TASK:` sits next to the drawer-title rule.
  - The checkbox is already safe: the Tasks plugin ignores it (the vault's global filter is `#task`), split already turns `- [ ] text` into a task, and promotion already keeps a checkbox's status.
- **Rendering:** draw `⌗⌗`, `⌗⌗⌗` after the checkbox. bob-ledger-tools already draws every `#task` as one teal `⌗`, so this extends that look. Depth comes from the nesting, so re-indenting a line updates it automatically.
- **Close card:** add a "Micro tasks" group at the top of the existing successor card. It already has Done (`Ctrl+X`) and Cancel (`Ctrl+Shift+X`).
  - Rows default to Done, and `Ctrl+X` flips a row between Done and **Keep open**.
  - Keep open runs Task Split at close time and leaves `[>] [[#^new|Text]]` under the closed task.
  - `Ctrl+Shift+X` marks a row not done (`[-]`, optional reason).
  - `Space`/`Tab` pulls a row in and switches it to Keep open.
  - Nested rows are shown but can't be selected.
- **Promotion:** micro tasks become `## Tasks` rows with their status kept; plain bullets go to `## Notes`.
- **Merge:** merging into a task writes the source as an open micro task, with the source's own micro tasks one level deeper.
- **Capture:** `- ..` becomes `- [ ] ` at bullet starts. Mac `Ctrl-G T` toggles the marker; bob decides where it's allowed, so the app stays a thin client.

**Requirement changes I'm proposing (the report lists all 13):**

- **No physical `NOTES` drawer by default.** Plain bullets already are the notes; writing a hidden drawer would break the accepted rule that a capture draft reads like the block it writes.
- **"Crossed out" means the `[-]`/`[>]` status, not `~~text~~`.** Obsidian already strikes those by default.
- **The verdict is called "Keep open" rather than "open"**, because "Open" already means "open the note".
- **Micro tasks can be ticked while working**, and ticked ones fold out of the card. A fully ticked task then closes with no card, which keeps the checkpoint meaningful.
- **Merges into a drawer or section stay notes**; only merging into the task itself makes a micro task.

**Please confirm one thing:** I read "a note that links to the original parent task" as wanting links in both directions. The `[>]` line in the parent links to the new task, and the new task gets the generated "linked from" mention back to the parent.

**Build order:**
1. Marker, rendering, authoring, and the merge change. None of these change what existing bullets mean.
2. A one-time review where you approve which existing bullets become micro tasks.
3. Switch promotion.
4. The close card. It's the expensive part: three card surfaces on top of the two close engines (Rust capture and the Obsidian cycler).

Prior art: [Things converts checklist items to to-dos on Convert to Project](https://culturedcode.com/things/support/articles/8491676/) ([guide](https://thesweetsetup.com/simple-guide-to-managing-tasks-in-things)); org-mode [checkboxes](https://orgmode.org/manual/Checkboxes.html) and [TODO dependencies](https://www.gnu.org/software/emacs/manual/html_node/org/TODO-dependencies.html); [Bullet Journal's `>` for migrated tasks](https://bulletjournal.com/pages/migration).
