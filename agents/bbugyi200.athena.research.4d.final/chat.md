# Chat History - ace-run (research.4d.final)

- **TIMESTAMP:** 2026-10-13 10:14:01 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4d.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261013_093556.md`

## Prompt

%clan(research.4d, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to start automatically adding a new sub-bullet to tasks that other tasks
depend on to indicate that the task blocks one or more other tasks.

- We already use a "Depends On" sub-bullet on the dependent tasks.
- This should happen automatically when dependencies are added to tasks (via the
  `<ctrl+shift+p>` keymap, for example).
- The `bob task reconcile` command should ensure the appropriate sub-bullets all exist
  and are consistent.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.4d.final %m:@xlarge
%wait:research.4d.cdx %wait:research.4d.cld %wait:research.4d.grk %wait:research.4d.mus %wait:research.4d.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to start automatically adding a new sub-bullet to tasks that other tasks
depend on to indicate that the task blocks one or more other tasks.

- We already use a "Depends On" sub-bullet on the dependent tasks.
- This should happen automatically when dependencies are added to tasks (via the
  `<ctrl+shift+p>` keymap, for example).
- The `bob task reconcile` command should ensure the appropriate sub-bullets all exist
  and are consistent.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.4d.cdx`, `research.4d.cld`, `research.4d.grk`, `research.4d.mus`, `research.4d.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.4d.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.4d.linker`, can find it:

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

I've read all five reports. Three recommend a stored reverse line and two recommend virtual-only. I'm now checking their disputed claims against the code and contract.

Checking the live vault's blocker counts to settle the researchers' differing numbers.

Checking a few remaining code anchors and the prior Depends-On research's note on a reverse "Blocks…" stage.

Verification is done. Every disputed fact is now settled against the code, contract, or live vault. Next I'll move the five reports into a new stem directory and write the consolidated report.

Moves are done. Now writing the consolidated report.

Now registering the consolidated report as a durable artifact.

Registration succeeded. Submitting the final declaration.

The consolidated report is written and registered as `research:202610/prerequisite_blocks_line/prerequisite_blocks_line__final.md` (ref `file:explicit:46a489d719c94351700aef7b`). The research repo commit is declared, and the host makes it after this turn ends.

**Recommendation:** build it as a **derived mirror**. Add one `🧱 **BLOCKS:**` line to each open task that has open dependents. `⛓️ DEPENDS ON` stays the only place dependencies are written. The new line is generated from those edges and never read back, the same way `bob projects sync` maintains the `🧩 Sub-projects:` line. Obsidian renders it as chips. A 🔑 marks dependents for which this task is the last thing in the way, and a summary reads "frees N of M".

**How I settled the researchers' disagreements:**
- **Stored line or chips only:** three researchers wanted a stored line and two wanted render-only chips. I sided with the stored line, because it stays readable in vim, git and by agents, and the cost is small. The live vault has 15 open blocking tasks, so that's 15 lines, plus 6 block ids to create on dependents that have none. That refutes the "thousands of lines" and "extreme churn" claims. The chips-only design is still used, as the rendering layer.
- **Glyph:** I picked `🧱` over `🚧` and `⛓️`. `🚧` already means a work-in-progress project in the navigation plugin. A distinct glyph also makes blocking tasks stand out while scrolling.
- **Closed prerequisites:** the line stays frozen as a record of what the task freed. Deleting it would break the existing rule that reconcile never touches closed tasks.
- **Order:** entries are sorted by link text. Reconcile regroups tasks every run, so document order would keep changing.
- **Block ids:** they have to be created for dependents that lack one. One report claimed they already exist, but 6 of the 20 open dependents have none.
- **Chips are the useful signal:** all 20 open dependents are `[?]`, so status colour on these chips carries no information. The 🔑 "last blocker" mark is what's actually new.

**Requirement adjustments I'm calling out (12 in total, all in the report):**
- **One line per blocking task,** not one sub-bullet per dependent.
- **The line is read-only:** hand edits never change dependencies, and reconcile restores it.
- **Open tasks only:** a dependent drops off when it closes. A closed blocking task keeps its line unchanged.
- **Removals too:** every dependency change, not just additions, updates the line.
- **One-step undo only for same-note pairs:** for cross-note pairs, the other note is updated after the change is saved, and reconcile repairs any miss.
- **No new CLI or Tasks field:** `bob query --tasks "(not done) AND (is blocking)"` already answers the question.
- **A `blocks_lines` kill switch** that removes the lines cleanly.
- **Guards first:** the parsers in every codebase must learn to ignore the new line before anything writes it. Today bob-cli's capture and Pomodoro link scanners would mistake it for a task link.
- **Editing from the blocking task's side** (removing a dependent from its chip, a "Blocks…" picker) moves to phase 2.

**Decisions for you:**
- `🧱` or `⛓️` for the glyph.
- Freeze or remove the line when the task closes.
- Whether v1 chips should only navigate, or also let you remove a dependent from there.
- `B` or `k` as the phase-2 Task Card key.

All five reports are now in `202610/prerequisite_blocks_line/` alongside the final report.
