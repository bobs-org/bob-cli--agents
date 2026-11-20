- **AGENTS:**
  - [bbugyi200.apollo.research.5l.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5l.final/README.md)

%clan(research.5l, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] Once I've
completed the work described by the property_card_title_block.md file in the research
sidecar repo, I want to add the new `[N` and `]N` keymaps, which should be immediately
useful for daily files, period notes, and record notes.

- These should be configurable in any Obsidian note somehow. I was thinking we could
  look for links that start with `<<` or `>>`, respectively, but that's just my first
  thought. Think hard about the best way to implement this.
- For daily files, the << link should point to the first day of the previous week and
  the >> link should point to the first day of the next week.
- For period notes, the << link should point to the first period note of the same level
  (ex: weekly period note if inside a weekly period note currently) in the previous
  period of a level one higher. The >> link should point to the first period note of the
  same level in the next period of a level one higher.
  - For example, this means the ~/bob/2026/2026-W30.md file should have a << link that
    points to the ~/bob/2026/2026-W14.md file and a >> link that points to the
    ~/bob/2026/2026-W40.md file.
  - This also means that yearly period notes should not support this functionality (i.e.
    should not have << or >> links).
  - Make sure that we make it clear (in a visually appealing way) when one of these
    files does not yet exist somehow.
- Album notes should be able to configure a field that its record notes should be
  grouped by in order to support these new keymaps.
  - The `[n` and `]n` keymaps should then start walking through all record notes with
    that field set to the same value in sequence before moving on to the prev/next
    record group (i.e. group of record notes with this field all set to the same value).
  - The `[N` and `]N` keymaps should jump to the first record note of the previous/next,
    respectively, record group.
  - As our first use-cases, I would like to configure the ~/bob/sase_blog_zettel.md
    album note to start using its `section` field to group this walk. Think hard about
    whether or not the other albums in my vault would benefit from configuring a
    grouping field as well (configure the appropriate field for these if so).
- Make sure that the `[{` and `]}` keymaps work properly with these keymaps.
- We should make sure these links render nicely at the bottom of property cards (see the
  bob-cli-nh epic bead for context).
- We should also make sure to add support for appropriate hints to the walker footer for
  these new links.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.5l.final %m:claude-fable-5 %wait:research.5l.cdx %wait:research.5l.cld
%wait:research.5l.grk %wait:research.5l.mus %wait:research.5l.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

Once I've completed the work described by the property_card_title_block.md file in the
research sidecar repo, I want to add the new `[N` and `]N` keymaps, which should be
immediately useful for daily files, period notes, and record notes.

- These should be configurable in any Obsidian note somehow. I was thinking we could
  look for links that start with `<<` or `>>`, respectively, but that's just my first
  thought. Think hard about the best way to implement this.
- For daily files, the << link should point to the first day of the previous week and
  the >> link should point to the first day of the next week.
- For period notes, the << link should point to the first period note of the same level
  (ex: weekly period note if inside a weekly period note currently) in the previous
  period of a level one higher. The >> link should point to the first period note of the
  same level in the next period of a level one higher.
  - For example, this means the ~/bob/2026/2026-W30.md file should have a << link that
    points to the ~/bob/2026/2026-W14.md file and a >> link that points to the
    ~/bob/2026/2026-W40.md file.
  - This also means that yearly period notes should not support this functionality (i.e.
    should not have << or >> links).
  - Make sure that we make it clear (in a visually appealing way) when one of these
    files does not yet exist somehow.
- Album notes should be able to configure a field that its record notes should be
  grouped by in order to support these new keymaps.
  - The `[n` and `]n` keymaps should then start walking through all record notes with
    that field set to the same value in sequence before moving on to the prev/next
    record group (i.e. group of record notes with this field all set to the same value).
  - The `[N` and `]N` keymaps should jump to the first record note of the previous/next,
    respectively, record group.
  - As our first use-cases, I would like to configure the ~/bob/sase_blog_zettel.md
    album note to start using its `section` field to group this walk. Think hard about
    whether or not the other albums in my vault would benefit from configuring a
    grouping field as well (configure the appropriate field for these if so).
- Make sure that the `[{` and `]}` keymaps work properly with these keymaps.
- We should make sure these links render nicely at the bottom of property cards (see the
  bob-cli-nh epic bead for context).
- We should also make sure to add support for appropriate hints to the walker footer for
  these new links.
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
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.5l.cdx`,
   `research.5l.cld`, `research.5l.grk`, `research.5l.mus`, `research.5l.gem`
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
   `research.5l.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.5l.linker`, can find it:

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
