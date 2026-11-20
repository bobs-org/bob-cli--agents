# Chat History - ace-run (research.5n.cdx)

- **TIMESTAMP:** 2026-11-20 16:19:55 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** research.5n.cdx
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261120_160058.md`

## Prompt

#gh:gh_bobs-org__bob-cli
%id(cdx, clan=research.5n)
%m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.5n.cld`, `research.5n.grk`, `research.5n.mus`, `research.5n.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

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
`__cdx` suffix, i.e. `<stem>__cdx.md` (double underscore before the
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

I’ll investigate the existing task, capture, merge, and successor behavior independently, then write a design report with explicit tradeoffs and a recommended implementation. I’m using the SASE repo and artifact workflows to place and register the report.


I’m using the audited memory workflow to check the terminology and existing design decisions. I’ll also draft a glossary definition in the report; the live glossary can be updated when the design is implemented.


Two constraints matter already: capture uses a leading `#` for drawer shortcuts, and its authored bullets currently stop at two levels. Nested micro tasks therefore need a real grammar change. There is also an existing split operation that handles task creation, backlinks, daily-note placement, and stale edits; it looks useful for building reliable micro-task successors.


I’m leaning toward `TASK:` as the stored marker, rendered as your compact `##`, `###`, and deeper badges. It avoids the existing `#task` and drawer meanings. I also found a shortcut conflict: `..` already escapes some dot aliases, so the new alias needs a narrowly defined bullet-start context.


The main design risk is making parent completion look final before unfinished micro work has been preserved. I recommend staging the micro-task decisions before closing the parent, then committing closure, any new tasks, and selected daily links together. The report will distinguish “done with parent,” “keep open,” and “cancel,” since a crossed-out bullet alone cannot explain what happened.


The design is settled. I’m writing up the recommended behavior, the changes I would make to your requirements, and the source evidence. The report also covers migration: existing plain bullets mix notes and commitments, so automatically marking them all would preserve today’s ambiguity.


The report is written and checked. It recommends `TASK:` with depth badges, notes by default, and a micro-aware close that preserves unfinished work before completion. I’m waiting for durable snapshot registration to finish, then I’ll submit the SASE final declaration.


The durable snapshot registered successfully. I’m using `sase_final` to declare the completed report for the host’s commit finalizer.


Written and registered the [independent research report](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202611/explicit_micro_tasks_design__cdx.md).

Recommendation: store `TASK:`, render depth badges, default notes into NOTES, and settle micro-task outcomes together with parent closure. The report covers tradeoffs, requirement adjustments, migration, implementation seams, and a proposed glossary entry.

Durable snapshot: [explicit:fd444f4076052312a576268a](/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261120160058/explicit_micro_tasks_design__cdx-534b25eba2b6.md).
