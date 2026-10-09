%clan(research.48, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to start showing the current pomodoro (if any) and all future pomodoros in
the preview shown by the bob-mac-capture app when no input text has been typed.

- This preview should therefore load by default when the panel first pops up.
- Since we will load this preview so often, we should make sure to cache it somehow when
  the daily file's contents haven't changed at all. IMPORTANT: The bob-mac-capture app
  MUST be blazing fast.
- For each task associated with a task link in a current or future pomodoro in today's
  daily file, we should always show as much of each task's contents as possible without
  causing the user to need to scroll the preview pane.
- This means that, if it all fits in the preview pane without the user needing to scroll
  (we should expand the height of the window as neccessary), we shoould show the full
  task definition for each task including all of its sub-bullets.
- Otherwise, we should support two folded views, which we will use in this order of
  priority, if necessary, to decrease the size of the contents in the preview pane:
  1. A view of each task that does not show the work log or schedule log for that task,
     but shows all other sub-bullets.
  2. A single-line view of each task.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.48.final %m:@xlarge
%wait:research.48.cdx %wait:research.48.cld %wait:research.48.grk %wait:research.48.mus %wait:research.48.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to start showing the current pomodoro (if any) and all future pomodoros in
the preview shown by the bob-mac-capture app when no input text has been typed.

- This preview should therefore load by default when the panel first pops up.
- Since we will load this preview so often, we should make sure to cache it somehow when
  the daily file's contents haven't changed at all. IMPORTANT: The bob-mac-capture app
  MUST be blazing fast.
- For each task associated with a task link in a current or future pomodoro in today's
  daily file, we should always show as much of each task's contents as possible without
  causing the user to need to scroll the preview pane.
- This means that, if it all fits in the preview pane without the user needing to scroll
  (we should expand the height of the window as neccessary), we shoould show the full
  task definition for each task including all of its sub-bullets.
- Otherwise, we should support two folded views, which we will use in this order of
  priority, if necessary, to decrease the size of the contents in the preview pane:
  1. A view of each task that does not show the work log or schedule log for that task,
     but shows all other sub-bullets.
  2. A single-line view of each task.
- #beau

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
   dispatch's `research.48.cdx`, `research.48.cld`, `research.48.grk`, `research.48.mus`, `research.48.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.48.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.48.linker`, can find it:

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