%clan(research.59, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to move the day strip to above the badges instead of below them, which
makes sense I think since the working time bar (see below) can act as a natural
separator.

- See the bob-cli-bz epic bead for context on day strips.
- Also, I liked the old look better. You were just supposed to fix the overlap.
- I think you just needed to change the way / where the working time bar, which shows
  which areas were worked on, is rendered.
- As a part of this change, let's also change that working time bar so we prefer to
  aggregate by the "top-level project" (i.e. the project in a task's ancestry--ancestry
  refers to walking the `parent` frontmatter fields--associated with a prj note that has
  an area note as its parent, not another project). We should aggregate by area iff the
  task lives in an area note. We will call this top-level project / area note the "root
  parent" for a task. In other words, the working time bar should aggregate by root
  parent.
- Make sure that the ~/bob/dash_stats.md file (the "stats dash") also allows for a good
  view that aggregates by root parent. We already have a button that supports
  aggregating by theme, so I was thinking we could just add a third button for this? Or
  maybe we should just always aggregate by the root parent (unless the theme button is
  used)? I'll let you decide this one.
- We should add new glossary memory web strands for:
  - "top-level project" (aka "top project")
  - "root parent"
  - "day strip"
  - "stats dash" (an easy way to refer to the ~/bob/dash_stats.md file)
- Finally, this change should allow us to obsolete a few things:
  - We should stop aggregating the total working time for the day in the "Pomodoros" H2
    section title in daily files, since this now duplicates data that can be found in
    the day strip.
  - We should remove support for the frontmatter field that allows projects to specify
    that aggregation should ignore sub-children (root parent aggregation makes this a
    lot less useful).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.59.final %m:@xlarge
%wait:research.59.cdx %wait:research.59.cld %wait:research.59.grk %wait:research.59.mus %wait:research.59.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to move the day strip to above the badges instead of below them, which
makes sense I think since the working time bar (see below) can act as a natural
separator.

- See the bob-cli-bz epic bead for context on day strips.
- Also, I liked the old look better. You were just supposed to fix the overlap.
- I think you just needed to change the way / where the working time bar, which shows
  which areas were worked on, is rendered.
- As a part of this change, let's also change that working time bar so we prefer to
  aggregate by the "top-level project" (i.e. the project in a task's ancestry--ancestry
  refers to walking the `parent` frontmatter fields--associated with a prj note that has
  an area note as its parent, not another project). We should aggregate by area iff the
  task lives in an area note. We will call this top-level project / area note the "root
  parent" for a task. In other words, the working time bar should aggregate by root
  parent.
- Make sure that the ~/bob/dash_stats.md file (the "stats dash") also allows for a good
  view that aggregates by root parent. We already have a button that supports
  aggregating by theme, so I was thinking we could just add a third button for this? Or
  maybe we should just always aggregate by the root parent (unless the theme button is
  used)? I'll let you decide this one.
- We should add new glossary memory web strands for:
  - "top-level project" (aka "top project")
  - "root parent"
  - "day strip"
  - "stats dash" (an easy way to refer to the ~/bob/dash_stats.md file)
- Finally, this change should allow us to obsolete a few things:
  - We should stop aggregating the total working time for the day in the "Pomodoros" H2
    section title in daily files, since this now duplicates data that can be found in
    the day strip.
  - We should remove support for the frontmatter field that allows projects to specify
    that aggregation should ignore sub-children (root parent aggregation makes this a
    lot less useful).
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
   dispatch's `research.59.cdx`, `research.59.cld`, `research.59.grk`, `research.59.mus`, `research.59.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.59.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.59.linker`, can find it:

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