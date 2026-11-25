- **AGENTS:**
  - [bbugyi200.apollo.research.69.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.69.final/README.md)

%clan(research.69, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I recently
did some research related to support for a new "snoozed task" functionaliity. I would
like to implement a modified (potentially--I haven't fully read it, so don't assume that
changes are needed) version of it.

- See the snoozed_task_links.md file in the research sidecar repo for context.
- Event tasks should never be treated as snoozed tasks. These work fine as is, so there
  is no need to change them.
- We need to make sure that we make it very clear which tasks are currently snoozed in
  today's daily file compared to which ones have active task links in the daily file
  when looking at a task's definition (maybe change the tomato icon to a clock with the
  snooze time next to it?).
- We should also make it very clear, when looking at a task link, to the user when a
  task link was snoozed but was awoken (i.e. is now ready). Make sure to show the wake
  time somewhere in the task link (or maybe we should show the snooze time? I'll let you
  decide on this one.)
- Snoozed tasks should NOT count against the `plan.max_links` limit.
- We should also make it very easy to snooze an existing task from its task link in the
  daily file (via a new keymap maybe?).
- When a snoozed task is woke, we should make sure to notify the user somehow, with the
  goal of making them aware that a new task that was planned for today is ready to be
  worked. Think hard about the best way to do this, so the user is very likely to see
  the notification (it should still go away on its own though).
- As a part of this change, we should add an excellent new glossary term for "snoozed
  task".
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.69.final %m:claude-fable-5 %wait:research.69.cdx %wait:research.69.cld
%wait:research.69.grk %wait:research.69.mus %wait:research.69.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I recently did some research related to support for a new "snoozed task" functionaliity.
I would like to implement a modified (potentially--I haven't fully read it, so don't
assume that changes are needed) version of it.

- See the snoozed_task_links.md file in the research sidecar repo for context.
- Event tasks should never be treated as snoozed tasks. These work fine as is, so there
  is no need to change them.
- We need to make sure that we make it very clear which tasks are currently snoozed in
  today's daily file compared to which ones have active task links in the daily file
  when looking at a task's definition (maybe change the tomato icon to a clock with the
  snooze time next to it?).
- We should also make it very clear, when looking at a task link, to the user when a
  task link was snoozed but was awoken (i.e. is now ready). Make sure to show the wake
  time somewhere in the task link (or maybe we should show the snooze time? I'll let you
  decide on this one.)
- Snoozed tasks should NOT count against the `plan.max_links` limit.
- We should also make it very easy to snooze an existing task from its task link in the
  daily file (via a new keymap maybe?).
- When a snoozed task is woke, we should make sure to notify the user somehow, with the
  goal of making them aware that a new task that was planned for today is ready to be
  worked. Think hard about the best way to do this, so the user is very likely to see
  the notification (it should still go away on its own though).
- As a part of this change, we should add an excellent new glossary term for "snoozed
  task".
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

When you author or carry over Mermaid diagrams, load `/mermaid_diagrams` before
drafting, even when no image or diagrams companion runs. The skill has the shared
figure-selection, styling, and PDF-render review rules. If the provider skill is not
deployed, verify the edited plugin's guide with
`sase macro show skill/mermaid_diagrams --format raw` (or
`sase macro show /mermaid_diagrams --format raw`) and use the form this host supports.
This guidance does not enable a companion diagrams agent.

The researchers' registered reports:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}

- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }}
  path={{ a.path }} ref={{ a.ref }} {% endfor %}

Month directory (create it if missing):

First run `sase repo open research -r "Write the swarm research reports"` and use the
path it prints as `<research checkout>`. The month directory is
`<research checkout>/202611`; create it if missing.

Steps:

1. From the registered reports above, identify exactly one report per expected suffix in
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.69.cdx`,
   `research.69.cld`, `research.69.grk`, `research.69.mus`, `research.69.gem`
   dependencies, matching by `wait_name` and the canonical research label's existing
   `__<suffix>.md` suffix. Never reassign suffixes from list order. Read each report
   through its canonical research reference (or the `ref` field's `file:<id>` reference
   if the original has moved) using `sase artifact read`. Do not read predecessor chat
   transcripts. If the records above do not identify exactly one report per expected
   suffix, stop and report the missing or ambiguous input instead of guessing.
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
   `research.69.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.69.linker`, can find it:

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
├── <name>__mus.md
├── <name>__gem.md
└── <name>__final.md
```
