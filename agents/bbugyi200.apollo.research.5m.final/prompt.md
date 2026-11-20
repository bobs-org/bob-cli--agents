%clan(research.5m, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to add a new `<ctrl+j>` keymap to the successor panel shown in Obsidian and
in the capture panel.

- This keymap should be able to be used to mark a successor that should be jumped to
  after completing the task (this should override the `<cmd+enter>` keymap in the
  capture panel--if it was used to submit the capture).
- We should be able to mark only a single task as the "jump successor" and that task may
  have any other state (i.e. it can be left open and not be pulled in, be pulled in, be
  closed, or be canceled).
- After the user completes the task close that triggered the successor panel, we should
  jump to the appropriate file in Obsidian and focus the selected jump successor task.
- This is often desirable when we don't want to pull a task in (so we can prioritize it,
  for example) or when we want to pull a task in that needs some changes made to it.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.5m.final %m:claude-fable-5
%wait:research.5m.cdx %wait:research.5m.cld %wait:research.5m.grk %wait:research.5m.mus %wait:research.5m.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to add a new `<ctrl+j>` keymap to the successor panel shown in Obsidian and
in the capture panel.

- This keymap should be able to be used to mark a successor that should be jumped to
  after completing the task (this should override the `<cmd+enter>` keymap in the
  capture panel--if it was used to submit the capture).
- We should be able to mark only a single task as the "jump successor" and that task may
  have any other state (i.e. it can be left open and not be pulled in, be pulled in, be
  closed, or be canceled).
- After the user completes the task close that triggered the successor panel, we should
  jump to the appropriate file in Obsidian and focus the selected jump successor task.
- This is often desirable when we don't want to pull a task in (so we can prioritize it,
  for example) or when we want to pull a task in that needs some changes made to it.
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

First run `sase repo open research -r "Write the swarm research reports"` and use
the path it prints as `<research checkout>`. The month directory is
`<research checkout>/202611`; create it if missing.

Steps:

1. From the registered reports above, identify exactly one report per expected suffix
   in cdx, cld, grk, mus, gem, belonging to this
   dispatch's `research.5m.cdx`, `research.5m.cld`, `research.5m.grk`, `research.5m.mus`, `research.5m.gem` dependencies, matching by `wait_name` and the canonical research
   label's existing `__<suffix>.md` suffix. Never reassign suffixes from list order.
   Read each report through its canonical research reference (or the `ref` field's
   `file:<id>` reference if the original has
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
   agent `research.5m.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.5m.linker`, can find it:

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