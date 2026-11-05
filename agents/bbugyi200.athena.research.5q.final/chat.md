# Chat History - ace-run (research.5q.final)

- **TIMESTAMP:** 2026-11-05 09:31:00 EST
- **MODEL:** claude/opus
- **AGENT:** research.5q.final
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_083757.md`

## Prompt

%clan(research.5q, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] Obsidian tasks should always have a type (either implicitly or explicitly) that matches
one of the task types of a pomodoro that contains a task link pointing to that task, but
we don't seem to do a good job of enforcing this currently. I would like to change that.

- The `bob task reconcile` command should be used as a fallback mechanism to ensure this
  is always the case (by removing or adding types to pomodoro lines as necessary).
- With that said, we should try to make sure that any keymaps that can currently break
  this constraint are fixed, so the `bob task reconcile` command is rarely needed to
  perform this cleanup.
- I think that the exception to this rule should maybe be custom pomodoro names, but I
  don't use these much so don't let them constrain the design too much (but don't break
  anything).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.5q.final %m:@xlarge
%wait:research.5q.cdx %wait:research.5q.cld %wait:research.5q.grk %wait:research.5q.mus %wait:research.5q.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

Obsidian tasks should always have a type (either implicitly or explicitly) that matches
one of the task types of a pomodoro that contains a task link pointing to that task, but
we don't seem to do a good job of enforcing this currently. I would like to change that.

- The `bob task reconcile` command should be used as a fallback mechanism to ensure this
  is always the case (by removing or adding types to pomodoro lines as necessary).
- With that said, we should try to make sure that any keymaps that can currently break
  this constraint are fixed, so the `bob task reconcile` command is rarely needed to
  perform this cleanup.
- I think that the exception to this rule should maybe be custom pomodoro names, but I
  don't use these much so don't let them constrain the design too much (but don't break
  anything).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

When you author or carry over Mermaid diagrams, load `/mermaid_diagrams` before
drafting, even when no image or diagrams companion runs. The skill has the shared
figure-selection, styling, and PDF-render review rules. If the provider skill is not
deployed, verify the edited plugin's guide with `sase macro show skill/mermaid_diagrams --format raw` (or
`sase macro show /mermaid_diagrams --format raw`) and use the form this host supports.
This guidance does not enable a companion diagrams agent.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.5q.cdx`, `research.5q.cld`, `research.5q.grk`, `research.5q.mus`, `research.5q.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Open the research repo with `/sase_repo`, then read each report through its canonical
   research reference (or the `ref` field's `file:<id>` reference if the original has
   moved) using `sase artifact read`. Do not read predecessor chat transcripts. If the
   records above do not identify exactly one report per expected suffix, stop and report
   the missing or ambiguous input instead of guessing.
2. Research the request yourself, prioritizing gaps, weak evidence, and disagreements
   between the reports.
3. Pick a descriptive stem `<name>` that collides with nothing in the month directory
   (do NOT end the name with `_consolidated` or `_<YYYYmmdd>` or anything similar unless
   it relates to the research topic), create `<month-dir>/<name>/`, and move each report
   inside it as `<name>__<suffix>.md`, preserving its existing suffix. Each report's
   `source_path` is provenance for where it lives in your own opened research checkout;
   resolve its canonical repo-relative path there before moving it. Never modify the
   other agents' checkouts or the stored snapshot recorded at `ref` — only the copy in
   your own checkout moves. Preserve every file and never overwrite: on any collision,
   pick a different stem first.
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest findings
   from every report above and your own research, resolve conflicts, cut duplication,
   and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker
   agent `research.5q.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.5q.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails,
   report that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```

## Response

I've opened the research repo and confirmed all five reports exist (cdx, cld, grk, mus, gem). Next I'll read each one through `sase artifact read`.

The figure renders at 82% fit and reads correctly. I'll make one small label tweak to fix the awkward wrap, then re-render.

The figure is legible and fits, so it's done. Next I'll create the report directory and move the five reports in, keeping grk's assets beside its report so the image links still resolve.

I'm not authorized to edit memory this turn, so the report will only recommend the decision record and glossary changes. Before writing, I'll confirm the date range my vault scan covered.

Now writing the consolidated report.

Report written. Two small accuracy fixes before registering: split also removes types, and there are five open entries now, not six.

Now registering the consolidated report as an artifact.

Registration worked (`file:explicit:df9d3913517ab531eedbcc93`). The research repo now has the moves and the new report to commit, so I'll finish through `/sase_final`.

My recommendation: go ahead, with one change. Make the rule "open Pomodoro names follow their tasks' types," and have reconcile both add and remove types. Removal needs guards, because the main problem today is leftover types on names, not missing ones.

The consolidated report merges the five researchers' reports and my own checks against the code and your vault. It is registered as an artifact for the linker agent, and the host will commit the research repo after this turn.

**Is it a good idea?** Yes, but it reverses current policy. Bob already defines this rule ("agreement" in `docs/task-types.md`), but the docs and glossary say drift is "flagged and never silently repaired." You need a new decision record, not just new code. All five researchers agree on the direction: reconcile edits only the name on today's open Pomodoros. It never writes `[type::]` fields and never moves links.

**Where the reports disagreed, and what the code and vault showed:**
- **Removal is the main job, and three of the five reports wanted to avoid it.** Since Nov 2, types missing from a name are rare; names keeping types that no link has are the common leak. Your own note `^task-reconcile-removes-types` asks for removal. Their worry was deleting "planned" types, but that barely applies:
  - reconcile already deletes every childless Pomodoro;
  - only 4 of 586 recent ledger entries had more than one type;
  - the leftovers come from Obsidian keymaps that reconcile never sees, so "remove only when this run removed the link" would never fire.
- **Renaming a Pomodoro in Obsidian stopped retyping its tasks on Nov 2.** Commit `71ae1cb` changed what the rename passes, so it now merges and the result is thrown away. grk and mus thought it still worked.
- **The Task Card type edit skips relocating the link for any task that already had a session today.** The lookup also searches closed sessions, sees two matches, and says "no live link · ledger unchanged". Today's ledger has this exact shape.
- **Refuted claims:**
  - mus: named capture (`#NAME`, `=name`) does not retype tasks. It came from a stale docs sentence.
  - gem: moving a task does not abort relocation when the destination note has no `task_type:`, because your global default `CHORE` applies.
  - gem: naming unnamed placeholders isn't needed; none exist in recent daily notes.

**Requirement adjustments I'm calling out:**
1. Only today's open Pomodoros are touched; closed ones are history.
2. Remove a type only when no live or struck link carries it, and only when every child line is a resolved, typed task link. Any prose or unresolved child protects the name, which gives you a simple way to keep a planned type.
3. Your custom-name exception already exists: a name with no configured types is never touched. You haven't used one since Oct 19.
4. MEET Pomodoros are never renamed; mismatches there stay a warning.
5. Closing a Pomodoro should also set its name to the types actually worked, since Stats freezes at close.
6. A name you type by hand isn't authoritative: reconcile will undo it, so the rename keymap is how you retype tasks.
7. Typing a type name for a brand-new Pomodoro should retype the task rather than produce a two-type name.

**Recommended rollout:**
1. Fix the rename regression and the Task Card lookup in bob-plugins.
2. Add one shared rule (Rust and JS, with shared test vectors) and a reconcile pass. Run it report-only for a day or two, then let it write.
3. Apply the same rule in the shared helpers that remove links, so keymaps leave nothing for reconcile to fix.
4. Make the close follow the rule, and handle new-Pomodoro names.
5. Fix the stale docs, and make the Obsidian mismatch mark cover inherited types.

**Questions for you:**
- Is it OK that a name you type over by hand reverts within about 15 minutes?
- Should typing a name for a brand-new Pomodoro retype the task?
- May a one-type session rename at close if only other types were worked?
- Should an Event Task linked under a work Pomodoro add MEET to its name?
- Is "add a prose child to keep a planned type" acceptable?

All five reports and grk's figure folder are now in `202611/pomodoro_names_follow_task_types/`. I didn't edit any memory notes; the report lists the decision record and glossary changes for the implementing plan.

Files are in `sase/repos/research/202611/pomodoro_names_follow_task_types/`:
- pomodoro_names_follow_task_types__final.md
