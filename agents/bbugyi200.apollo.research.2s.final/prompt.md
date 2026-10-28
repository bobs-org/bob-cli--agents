%clan(research.2s, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to start inferring which theme we should suggest for a task (by making it
the default choice in completion menus) based on the task.

- Project notes and area notes should be able to specify the default theme used by their
  tasks and/or sub-projects via a new `theme` frontmatter field. We should add
  `theme: BUILD` to the ~/bob/dev.md file, `theme: CHORE` to the ~/bob/love.md file, and
  `WRITE` to the ~/bob/job.md and ~/bob/sase_blog.md files as our first use-cases.
- Ref tasks should suggest the `READ` theme by default. This should override any
  area/project theme default.
- We should make it clear in completion menus why a particular theme is being suggested.
- We should also allow a theme to be overridden explicitly for a given task via a new
  `[theme::<theme]` property on the task.
  - Make sure this property is rendered in a concise and visually appealing way in
    Obsidian.
  - We should automatically set this property on a task when a theme other than the
    sugested theme is selected when adding a task link for a task (via the
    `<ctrl+enter>` keymap, for example). This way I don't need to re-override the theme
    again for that task the next day if it happens to roll over.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.2s.final %m:@xlarge
%wait:research.2s.cdx %wait:research.2s.cld %wait:research.2s.grk %wait:research.2s.mus %wait:research.2s.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to start inferring which theme we should suggest for a task (by making it
the default choice in completion menus) based on the task.

- Project notes and area notes should be able to specify the default theme used by their
  tasks and/or sub-projects via a new `theme` frontmatter field. We should add
  `theme: BUILD` to the ~/bob/dev.md file, `theme: CHORE` to the ~/bob/love.md file, and
  `WRITE` to the ~/bob/job.md and ~/bob/sase_blog.md files as our first use-cases.
- Ref tasks should suggest the `READ` theme by default. This should override any
  area/project theme default.
- We should make it clear in completion menus why a particular theme is being suggested.
- We should also allow a theme to be overridden explicitly for a given task via a new
  `[theme::<theme]` property on the task.
  - Make sure this property is rendered in a concise and visually appealing way in
    Obsidian.
  - We should automatically set this property on a task when a theme other than the
    sugested theme is selected when adding a task link for a task (via the
    `<ctrl+enter>` keymap, for example). This way I don't need to re-override the theme
    again for that task the next day if it happens to roll over.
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
   dispatch's `research.2s.cdx`, `research.2s.cld`, `research.2s.grk`, `research.2s.mus`, `research.2s.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.2s.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.2s.linker`, can find it:

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