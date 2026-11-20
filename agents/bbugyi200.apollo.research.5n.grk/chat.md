# Chat History - ace-run (research.5n.grk)

- **TIMESTAMP:** 2026-11-20 16:36:47 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** research.5n.grk
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261120_160058.md`

## Prompt

%id(grk, clan=research.5n)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.5n.cdx`, `research.5n.cld`, `research.5n.mus`, `research.5n.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

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
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll start by opening the research repo and loading the skills and memory this report depends on, then investigate the current task/drawer/successor design independently.

I'll record the skills, open the research checkout, and load glossary plus artifact memory before reading the codebase.

The research repo open is still running; I'll wait on it while loading glossary, decisions, and artifact memory.

The glossary selector was too broad; I'll retry with unique aliases and keep waiting on the research-repo open.

Research checkout is open. Next I’ll inspect existing 202611 reports and the current drawer, successor, capture, and merge implementations.

`#task` is already the Tasks global filter, so I’ll map drawers, promotion, successors, and merge before choosing a marker.

`..` already escapes a literal `.` in capture, so I’ll check that collision and the plugin keymaps before locking a marker.

I have enough to design the figures and write the report. Next I’ll render the diagrams, then draft the `__grk` markdown.

The close diagram is too wide; I’ll restack its verdicts and check the other two figures visually.

I'll restack the close verdicts vertically and simplify the round-trip figure so the mapping reads left to right.

I'll write the full research report now, then register it as an artifact.

I'll register the report as an artifact, then submit the SASE final declaration. First I need the artifact skill and to confirm the report is on disk.

The report is on disk. I'll record the artifact skill, confirm the create flags, then register it with the exact path and label you specified.

CLI uses `-l` and copies by default, matching the request. I'll register the report, then check that it ends with a recommended solution.

Artifact is registered. Next I’ll pull the finalizer context and submit the turn declaration.

I'll commit the research repo with the report and figures, then submit the finalizer.

Build it. Explicit marking is the right cut. Store and render two or more `#` characters whose count matches nesting depth. Do not store `#task` or `TASK:`. Treat opening a micro task as a split.

The independent report is at `202611/micro_task_hash_marker_and_successor_audit__grk.md` in the research checkout. Artifact:

- id: `explicit:c945631ca970227c9301281b`
- label: `research:202611/micro_task_hash_marker_and_successor_audit__grk.md`
- ref: `file:explicit:c945631ca970227c9301281b`

The source file stayed in the research repo (no `--move`).

### Recommended encoding

```markdown
- [ ] #task Prepare the launch review [created:: 2026-11-20] ^launch
	- ## Confirm the rollout owner
		- ### Send the owner the final date
	- ## Attach the final checklist
	- NOTES
		- brand preference still TBD
```

- Two or more hashes, then a space, mark a micro task (`##` at depth 1, `###` at depth 2, capped at `######`).
- Capture types that mark with `- ..` at a bullet start. `Ctrl+G t` toggles it on the existing Mac `Ctrl+G` leader.
- Unmarked notes, including `@foo+bar` same-line notes, file in a `NOTES` drawer created on demand.
- Closing the parent offers top-level micro tasks on the existing successor card, Leave by default. `Ctrl+X` extracts as a Ready sibling. `Tab` / empty-filter `Space` extracts and pulls into today. `Ctrl+Shift+X` strikes as abandoned. Nested rows show muted and follow their parent.
- Merge writes `## <source description>` in the target.
- Opening reuses split: sibling `#task`, stub in the parent, LINKED FROM mention.

### Why the requested spellings fail

`#task` is the Tasks global filter and the definition of a Bob task. A prefix on a plain bullet either special-cases every “is this a task?” predicate or grows a nested checkbox later. `TASK:` is a legal drawer title (`:` only as a final character), and `TASKS` is already reserved. `##` is already carved out of the drawer shortcut (`##`, `#`+digit, `#-` stay prose), so hashes are the free, heading-shaped mark.

`..` at item start already types `.bashrc`. The alias belongs at a list-item start only. `Ctrl+X` on the successor card already means Done; keep the chord, change the consequence copy to “open” for this row type.

### Sixteen requirement adjustments

The largest product calls:

- **ADJ-1** Store `##` / `###`, never `#task` or `TASK:`.
- **ADJ-4** Successor `Ctrl+X` means open (extract Ready). Tab/Space means open and pull in in one step.
- **ADJ-5** Extract reuses split. Leave writes nothing. A link from the struck bullet back to the parent is a ring.
- **ADJ-7** Dual-read plus a doctor. No silent vault rewrite.
- **ADJ-10** No checkbox on stored micro tasks.
- **ADJ-12** Bump `GRAMMAR_REVISION` 28 → 29 (`!` capture contract).
- **ADJ-13** Cancelling the parent does not auto-strike micro tasks.

### Ship order

1. Grammar and writers in bob-cli (`TaskChildKind::MicroTask { depth }`, NOTES default, `..` rewrite, toggle).
2. Promotion and split strip hashes; unmarked children become `## Notes`.
3. Merge prefixes the title bullet with `## `.
4. Successor group `micro_task` first on the card.
5. Glossary strand, capture docs, hash-token CSS. Mac stays a thin client.

v1 non-goals: project→task reversal of arbitrary projects, checkboxes on micro tasks, auto-migration of the vault, inheriting type onto extracted tasks.

The outline a task *is* should look like the outline a project *will be*. One hash names a drawer. Two hashes name a commitment. Closing a parent shows those hashes on the card already used to decide what happens next.
