%clan(research.36, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to add better support for moving tasks from one note file to another and
add excellent (new) support for merging tasks to / creating new tasks from bullets of
other tasks.

- We should add support for a new `@a+aid @b+bid > @c` capture syntax where any number
  of notes can be on the left-hand side of the `>` character and `@c` can have a
  `#drawer` suffix to specify that the tasks should be converted to notes and moved to
  that drawer (this drawer should be created if it does not already exist).
- We should also be able to use a target of the form `@c+cid` after the `>`, in which
  case we should merge the source tasks into the `^cid` task in the ~/bob/c.md file. We
  should also be able to use the `@c+cid#drawer` syntax to target a specific drawer in
  the `^cid` task (this drawer should be created if it does not already exist).
- When merging one task into another, we should not delete the source tasks. Instead, we
  should add a new "merged into" task relation that points from the source tasks to the
  destination task (and auto-cancels the source task). This "merged into" task relation
  should be able to be used on its own (in Obsidian via the `<ctrl+shift+l>` keymap, for
  example) to perform the same operation (see how we associate other task relations with
  specific operations for inspiration--this "merged into" relation should be
  configurable if possible/desirable).
- We should add a new `<ctrl+shift+t>` keymap to Obsidian that makes it easy to split
  out one or more top-level bullets from a task into new tasks. When this is done, the
  bullets (and their child bullets) should be replaced by some concise and useful text
  containing inline links to the new tasks that were created from the old bullets (the
  old tasks should wind up being given "linked from" mentions which are triggered by
  these inline links).
- Make sure that we have good command-line support for all of this new functionality.
- FYI: I already am in the process of adding support for the `@file+id` capture syntax
  multiple times on the same line (see the capture_multi_target.md file in the plans
  sidecar repo for context).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.36.final %m:@xlarge
%wait:research.36.cdx %wait:research.36.cld %wait:research.36.grk %wait:research.36.mus %wait:research.36.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to add better support for moving tasks from one note file to another and
add excellent (new) support for merging tasks to / creating new tasks from bullets of
other tasks.

- We should add support for a new `@a+aid @b+bid > @c` capture syntax where any number
  of notes can be on the left-hand side of the `>` character and `@c` can have a
  `#drawer` suffix to specify that the tasks should be converted to notes and moved to
  that drawer (this drawer should be created if it does not already exist).
- We should also be able to use a target of the form `@c+cid` after the `>`, in which
  case we should merge the source tasks into the `^cid` task in the ~/bob/c.md file. We
  should also be able to use the `@c+cid#drawer` syntax to target a specific drawer in
  the `^cid` task (this drawer should be created if it does not already exist).
- When merging one task into another, we should not delete the source tasks. Instead, we
  should add a new "merged into" task relation that points from the source tasks to the
  destination task (and auto-cancels the source task). This "merged into" task relation
  should be able to be used on its own (in Obsidian via the `<ctrl+shift+l>` keymap, for
  example) to perform the same operation (see how we associate other task relations with
  specific operations for inspiration--this "merged into" relation should be
  configurable if possible/desirable).
- We should add a new `<ctrl+shift+t>` keymap to Obsidian that makes it easy to split
  out one or more top-level bullets from a task into new tasks. When this is done, the
  bullets (and their child bullets) should be replaced by some concise and useful text
  containing inline links to the new tasks that were created from the old bullets (the
  old tasks should wind up being given "linked from" mentions which are triggered by
  these inline links).
- Make sure that we have good command-line support for all of this new functionality.
- FYI: I already am in the process of adding support for the `@file+id` capture syntax
  multiple times on the same line (see the capture_multi_target.md file in the plans
  sidecar repo for context).
- #beau

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
   dispatch's `research.36.cdx`, `research.36.cld`, `research.36.grk`, `research.36.mus`, `research.36.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.36.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.36.linker`, can find it:

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