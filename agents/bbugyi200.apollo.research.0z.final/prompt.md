%clan(research.0z, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to add full support to prj tasks for task dep links.

- You can add a dependency to a prj task now (using the `<ctrl+shift+p>` keymap, for
  example), but the result is not intuitive (see the ~/bob/job_apply_to_databricks.md
  file, which should be auto-fixed by the `bob task reconcile` command after this
  change, for an example).
- When a prj task is given a dep link, it should be added as a `depends_on` frontmatter
  field on that project note, not in a "Depends On" sub-subullet. Make sure to update
  the `<cmd+ctrl+shift+n>` Obsidian keymap to support this change so project notes are
  converted from tasks correctly.
- Most importantly, any task that lives in a blocked project should also be blocked (in
  this case, because the project has an unmet dependency, but whenever a project is
  blocked this rule applies).
- We will need to make sure to update the `<ctrl+shift+p>` keymap so this occurs
  automatically when I add a dependency to a prj task using that keymap.
- Keep in mind that blocked tasks should not have corresponding task links, so those
  should be removed (along with the pomodoro section they live in if it becomes empty)
  if they exist.
- We should also update the `bob task reconcile` command to check for any tasks that
  should be blocked and/or have their corresponding task links removed.
- The "task dep links" glossary memory web term should be updated accordingly.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.0z.final %m:@xlarge
%wait:research.0z.cdx %wait:research.0z.cld %wait:research.0z.grk %wait:research.0z.mus %wait:research.0z.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to add full support to prj tasks for task dep links.

- You can add a dependency to a prj task now (using the `<ctrl+shift+p>` keymap, for
  example), but the result is not intuitive (see the ~/bob/job_apply_to_databricks.md
  file, which should be auto-fixed by the `bob task reconcile` command after this
  change, for an example).
- When a prj task is given a dep link, it should be added as a `depends_on` frontmatter
  field on that project note, not in a "Depends On" sub-subullet. Make sure to update
  the `<cmd+ctrl+shift+n>` Obsidian keymap to support this change so project notes are
  converted from tasks correctly.
- Most importantly, any task that lives in a blocked project should also be blocked (in
  this case, because the project has an unmet dependency, but whenever a project is
  blocked this rule applies).
- We will need to make sure to update the `<ctrl+shift+p>` keymap so this occurs
  automatically when I add a dependency to a prj task using that keymap.
- Keep in mind that blocked tasks should not have corresponding task links, so those
  should be removed (along with the pomodoro section they live in if it becomes empty)
  if they exist.
- We should also update the `bob task reconcile` command to check for any tasks that
  should be blocked and/or have their corresponding task links removed.
- The "task dep links" glossary memory web term should be updated accordingly.

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
   dispatch's `research.0z.cdx`, `research.0z.cld`, `research.0z.grk`, `research.0z.mus`, `research.0z.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.0z.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.0z.linker`, can find it:

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