- **AGENTS:**
  - [bbugyi200.apollo.research.31.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.31.final/README.md)

%clan(research.31, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I want to
make it so the `#off` tag is accepted in a Google Calendar event instead of `#offclock`
or `#untracked` (both of which should still work but should produce a deprecation
warning message by the `bob gcal sync` command).

- Let's start using `#off` instead of `#offclock` in Obsidian as well (to be
  consistent). Make sure to update all past event tasks that used the deprecated tags to
  now use `#off`.
- Also, as a part of this change, we should add support for a new `offclock: true`
  frontmatter field to area / project notes that specifies that tasks belonging to that
  area/project should always be treated as offclock.
- This new field should be respected for all child areas/projects of that area/project
  note, recursively, but children should be able to override this via their own
  `offclock: false` frontmatter field. Individual tasks should be able to override this
  via a new `#on` tag, which the `bob gcal sync` command should start looking for on
  Google Calendar events.
- As our first use-case I would like to set `offclock: true` in the ~/bob/love.md file
  so all "love" tasks (including event tasks) are treated as offclock.
- See the bob-cli-fl epic bead for context.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.31.final %m:@xlarge %wait:research.31.cdx %wait:research.31.cld
%wait:research.31.grk %wait:research.31.mus %wait:research.31.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I want to make it so the `#off` tag is accepted in a Google Calendar event instead of
`#offclock` or `#untracked` (both of which should still work but should produce a
deprecation warning message by the `bob gcal sync` command).

- Let's start using `#off` instead of `#offclock` in Obsidian as well (to be
  consistent). Make sure to update all past event tasks that used the deprecated tags to
  now use `#off`.
- Also, as a part of this change, we should add support for a new `offclock: true`
  frontmatter field to area / project notes that specifies that tasks belonging to that
  area/project should always be treated as offclock.
- This new field should be respected for all child areas/projects of that area/project
  note, recursively, but children should be able to override this via their own
  `offclock: false` frontmatter field. Individual tasks should be able to override this
  via a new `#on` tag, which the `bob gcal sync` command should start looking for on
  Google Calendar events.
- As our first use-case I would like to set `offclock: true` in the ~/bob/love.md file
  so all "love" tasks (including event tasks) are treated as offclock.
- See the bob-cli-fl epic bead for context.

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

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix in
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.31.cdx`,
   `research.31.cld`, `research.31.grk`, `research.31.mus`, `research.31.gem`
   dependencies, matching by `wait_name` and the canonical research label's existing
   `__<suffix>.md` suffix. Never reassign suffixes from list order. Open the research
   repo with `/sase_repo`, then read each report through its canonical research
   reference (or the `ref` field's `file:<id>` reference if the original has moved)
   using `sase artifact read`. Do not read predecessor chat transcripts. If the records
   above do not identify exactly one report per expected suffix, stop and report the
   missing or ambiguous input instead of guessing.
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
   `research.31.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.31.linker`, can find it:

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
