- **AGENTS:**
  - [bbugyi200.athena.research.4t.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.athena.research.4t.final/README.md)

%clan(research.4t, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] We currently
label every pomodoro with a theme and use these themes to aggregate statistics in the
~/bob/dash_stats.md file. I would like to start automatically labeling pomodoros by the
corresponding projects and/or areas of the task links contained in them.

- As a part of this change, we should start aggregating the stats shown in the
  ~/bob/dash_stats.md file by area and project when possible.
- We will need the ability to exclude sub-projects of some projects from being
  aggregated and/or used to label pomodoros directly. Instead, task links to tasks in
  these sub-projects should be treated as if (when labeling pomodoro and aggregating
  stats) they pointed to tasks in the parent project that configured this. We should
  configure the ~/bob/sase.md project note to use this functionality.
- I'm not sure how/when/what to label pomodoros, so you should think hard about this.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.4t.final %m:@xlarge %wait:research.4t.cdx %wait:research.4t.cld
%wait:research.4t.grk %wait:research.4t.gem %q(1.5x, w=0.25) #gh:gh_bobs-org__bob-cli
You are the lead researcher: 4 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

We currently label every pomodoro with a theme and use these themes to aggregate
statistics in the ~/bob/dash_stats.md file. I would like to start automatically labeling
pomodoros by the corresponding projects and/or areas of the task links contained in
them.

- As a part of this change, we should start aggregating the stats shown in the
  ~/bob/dash_stats.md file by area and project when possible.
- We will need the ability to exclude sub-projects of some projects from being
  aggregated and/or used to label pomodoros directly. Instead, task links to tasks in
  these sub-projects should be treated as if (when labeling pomodoro and aggregating
  stats) they pointed to tasks in the parent project that configured this. We should
  configure the ~/bob/sase.md project note to use this functionality.
- I'm not sure how/when/what to label pomodoros, so you should think hard about this.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}

- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }}
  path={{ a.path }} ref={{ a.ref }} {% endfor %}

Month directory (create it if missing):

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix in
   cdx, cld, grk, gem, belonging to this dispatch's `research.4t.cdx`,
   `research.4t.cld`, `research.4t.grk`, `research.4t.gem` dependencies, matching by
   `wait_name` and the canonical research label's existing `__<suffix>.md` suffix. Never
   reassign suffixes from list order. Open the research repo with `/sase_repo`, then
   read each report through its canonical research reference (or the `ref` field's
   `file:<id>` reference if the original has moved) using `sase artifact read`. Do not
   read predecessor chat transcripts. If the records above do not identify exactly one
   report per expected suffix, stop and report the missing or ambiguous input instead of
   guessing.
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
4. Write the consolidated report to `<name>/<name>__final.md`: merge the strongest
   findings from every report above and your own research, resolve conflicts, cut
   duplication, and add missing critical context without unnecessary length.

   Do not create `<name>/<name>.md`, not even as a placeholder, because the linker agent
   `research.4t.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.4t.linker`, can find it:

   sase artifact create -p "<absolute-report-path>" -l
   "research:<repo-relative-report-path>"

   Use the consolidated report's actual absolute path and its path relative to the
   research repo root, for example `research:202609/<name>/<name>__final.md`. Register
   only the consolidated report, and do not pass `--move`. If registration fails, report
   that failure; do not report the task as fully complete.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__gem.md
└── <name>__final.md
```
