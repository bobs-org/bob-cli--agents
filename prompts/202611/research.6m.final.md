- **AGENTS:**
  - [bbugyi200.apollo.research.6m.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6m.final/README.md)

%clan(research.6m, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like
to start rendering child areas, sub-projects, notebooks, albums, and records as
collapsable sections, which we will name "cabinets", at the bottom of the property card
for the given file instead of in H2 sections.

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi,
  bob-cli-qj, bob-cli-qm, and bob-cli-qp epic beads.
- These cabinets should contain the same data that the corresponding H2 section used to
  contain.
- Our first cabinet already exists, it is just not named as such. The "property cabinet"
  can be expanded/collapsed via the `-` keymap.
- The collapsible "Schema" widget found on album cards and the bank card should also be
  migrated to a new cabinet (above the property cabinet). I think the only change that
  needs to be made is that the collapsible "Schema" and "Properties" widgets should use
  the same styling.
- The `_` keymap, which already serves to expand/collapse the schema section, should
  continue to serve this purpose, but should have a special behavior when more than one
  cabinet exists above the property cabinet.
  - Namely, the footer should change in Obsidian to show hints for numbers, starting at
    1, that are associated with the cabinets above the property cabinet starting from
    the bottom non-property cabinet (i.e. the one right above the property cabinet,
    which should always be the bottom cabinet).
  - If the user presses one of these numbers (they should also be able to use `<esc>` or
    `<ctrl+[>` to abort), then that cabinet should be expanded/collapsed.
- As a part of this change we should add an excellent new glossary term for "cabinet".
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.6m.final %m:claude-fable-5 %wait:research.6m.cdx %wait:research.6m.cld
%wait:research.6m.grk %wait:research.6m.mus %wait:research.6m.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to start rendering child areas, sub-projects, notebooks, albums, and
records as collapsable sections, which we will name "cabinets", at the bottom of the
property card for the given file instead of in H2 sections.

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi,
  bob-cli-qj, bob-cli-qm, and bob-cli-qp epic beads.
- These cabinets should contain the same data that the corresponding H2 section used to
  contain.
- Our first cabinet already exists, it is just not named as such. The "property cabinet"
  can be expanded/collapsed via the `-` keymap.
- The collapsible "Schema" widget found on album cards and the bank card should also be
  migrated to a new cabinet (above the property cabinet). I think the only change that
  needs to be made is that the collapsible "Schema" and "Properties" widgets should use
  the same styling.
- The `_` keymap, which already serves to expand/collapse the schema section, should
  continue to serve this purpose, but should have a special behavior when more than one
  cabinet exists above the property cabinet.
  - Namely, the footer should change in Obsidian to show hints for numbers, starting at
    1, that are associated with the cabinets above the property cabinet starting from
    the bottom non-property cabinet (i.e. the one right above the property cabinet,
    which should always be the bottom cabinet).
  - If the user presses one of these numbers (they should also be able to use `<esc>` or
    `<ctrl+[>` to abort), then that cabinet should be expanded/collapsed.
- As a part of this change we should add an excellent new glossary term for "cabinet".
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
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.6m.cdx`,
   `research.6m.cld`, `research.6m.grk`, `research.6m.mus`, `research.6m.gem`
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
   `research.6m.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.6m.linker`, can find it:

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
