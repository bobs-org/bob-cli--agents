- **AGENTS:**
  - [bbugyi200.apollo.research.5f.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5f.final/README.md)

%clan(research.5f, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] We already
support a headline in daily files, intentions in weekly period notes, outcomes in
quarterly period notes, and themes in yearly period notes. I would like to unify this
concept into a single term, "intentions", that describes the same structure, which
should have a period associated with it, including daily (e.g. "daily intentions",
"weekly intentions", etc...).

- Instead of H2 sections or the **Headline** bullet used in daily files, we should start
  supporting new `intentions` (user-set list of strings), `summary` (agent-set string),
  and `reflection` (user-set string) frontmatter fields to daily files and period notes.
- We should hide these frontmatter properties in Obsidian. Instead, we should generalize
  the code (if possible--at least the UX should be shared) used for the
  album/record/bank cards that are rendered at the top of album notes, record notes, and
  the ~/bob/bank.md file.
  - This new "intentions card" (this and "album/record/bank cards" should be considered
    types of "property cards") will only be shown when the `intentions` frontmatter
    property is set.
  - It should be very easy for the user to modify the current intentions and/or
    reflection using a property card editor that is triggered by the `==` keymap.
- As a part of this change, you should add two new `#periods` daily GTD tasks to the
  ~/bob/gtd_daily.md file that (1: a `#pre` task) ask me to launch an agent to review
  all of the work that I did the previous day and add a `summary` field to that day's
  daily file and (2: a `#post` task) ask me to manually (by typing something like
  `[n==r` from today's current daily file, for example) set the `reflection` field on
  yesterday's daily file.
  - We should add excellent agent instructions to a file somewhere that describes how
    this summary should be generated and point to that file using some kind of sentinal
    value for the `summary` field maybe? This is just my first thought on
    implementation. The goal is to make sure that agents always find these instructions
    when asked to summarize a daily file without ever having to show these instructions
    to the user when they have daily files open in Obsidian (think hard about the best
    way to implement this).
- We should add excellent new glossary terms for "intention", "property card",
  "intention card", "album card". "record card", and "bank card".
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.5f.final %m:claude-fable-5 %wait:research.5f.cdx %wait:research.5f.cld
%wait:research.5f.grk %wait:research.5f.mus %wait:research.5f.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

We already support a headline in daily files, intentions in weekly period notes,
outcomes in quarterly period notes, and themes in yearly period notes. I would like to
unify this concept into a single term, "intentions", that describes the same structure,
which should have a period associated with it, including daily (e.g. "daily intentions",
"weekly intentions", etc...).

- Instead of H2 sections or the **Headline** bullet used in daily files, we should start
  supporting new `intentions` (user-set list of strings), `summary` (agent-set string),
  and `reflection` (user-set string) frontmatter fields to daily files and period notes.
- We should hide these frontmatter properties in Obsidian. Instead, we should generalize
  the code (if possible--at least the UX should be shared) used for the
  album/record/bank cards that are rendered at the top of album notes, record notes, and
  the ~/bob/bank.md file.
  - This new "intentions card" (this and "album/record/bank cards" should be considered
    types of "property cards") will only be shown when the `intentions` frontmatter
    property is set.
  - It should be very easy for the user to modify the current intentions and/or
    reflection using a property card editor that is triggered by the `==` keymap.
- As a part of this change, you should add two new `#periods` daily GTD tasks to the
  ~/bob/gtd_daily.md file that (1: a `#pre` task) ask me to launch an agent to review
  all of the work that I did the previous day and add a `summary` field to that day's
  daily file and (2: a `#post` task) ask me to manually (by typing something like
  `[n==r` from today's current daily file, for example) set the `reflection` field on
  yesterday's daily file.
  - We should add excellent agent instructions to a file somewhere that describes how
    this summary should be generated and point to that file using some kind of sentinal
    value for the `summary` field maybe? This is just my first thought on
    implementation. The goal is to make sure that agents always find these instructions
    when asked to summarize a daily file without ever having to show these instructions
    to the user when they have daily files open in Obsidian (think hard about the best
    way to implement this).
- We should add excellent new glossary terms for "intention", "property card",
  "intention card", "album card". "record card", and "bank card".
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
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.5f.cdx`,
   `research.5f.cld`, `research.5f.grk`, `research.5f.mus`, `research.5f.gem`
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
   `research.5f.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.5f.linker`, can find it:

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
