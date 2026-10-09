%clan(research.0q, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to re-imagine the way that we track ref tasks.

- I have been treating ref tasks as normal Obsidian tasks in practice, but our
  implementation does not support this well or encourage it.
- Namely, the fact that we store ref tasks inside of ref notes is not intuitive or
  consistent with how we treat other tasks, which all live in either area notes or
  project notes.
- I would like to fix this by requiring that all future and currently open ref notes
  have a project note or area note listed as their parent.
- We should then be able to define the ref task for each ref associated with an
  area/project in the "Tasks" section of the corresponding note file like we do for all
  other Obsidian tasks.
- You should migrate any existing ref notes that are associated with open ref tasks to
  use this new policy and move their ref tasks to the appropriate area/project note
  file.
- This complicates syncing the ref note status with the ref task a bit since we need to
  account for the possibility that the ref task gets moved to a "done" note file in the
  ~/bob/done/ directory at some point.
- Also, I think there is a lot of logic that currently treats ref tasks as special /
  something to filter out. We don't show them when pressing `^` to show today's /
  pending / next tasks in the bob-mac-capture app, for example. Just about all (probably
  all, but think hard about this so we don't break any invariants that I currently rely
  on) of this logic should be removed so we start treating ref tasks like any other
  task.
- This change will also require that we start prompting the user for a project / area
  note file when capturing new ref URLs (via the bob-mac-capture app or the
  `bob gkeep pull` command, for example) so we know which project / area note file to
  use.
- This project / area name should then be passed to the `bob ref create` command's new,
  required `-p|--parent` option.
- I currently use a sase (a GitHub project in the sase-org organization) file hook that
  uses this `bob ref create` command. We will need to start passing in the project name
  (e.g. "sase", "bob-cli") to the `-p|--parent` option.
  - I'm not sure that sase injects the project name into this file hook command string
    right now, so you might need to add support for that.
  - Also note that it is not guaranteed that the project name that gets passed in will
    exactly match the project note's name. For example, the "bob-cli" project name
    should actually map to the ~/bob/bob.md file. To work around this, we should add
    support for a new `project_name_aliases` frontmatter field to project notes that
    allows them to specify alternative names that will be matched by the `bob` command
    when searching for a project by name. We should set this field to `["bob-cli"]` for
    the ~/bob/bob.md project note.
- We will need to start giving ref tasks a different block ID since `^ref` will no
  longer be guaranteed to be unique. In order to make ref tasks stand out a bit more, we
  should also start rendering an appropriate icon/symbol instead of `#ref` when these
  tasks are rendered in Obsidian.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.0q.final %m:@xlarge
%wait:research.0q.cdx %wait:research.0q.cld %wait:research.0q.grk %wait:research.0q.mus %wait:research.0q.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to re-imagine the way that we track ref tasks.

- I have been treating ref tasks as normal Obsidian tasks in practice, but our
  implementation does not support this well or encourage it.
- Namely, the fact that we store ref tasks inside of ref notes is not intuitive or
  consistent with how we treat other tasks, which all live in either area notes or
  project notes.
- I would like to fix this by requiring that all future and currently open ref notes
  have a project note or area note listed as their parent.
- We should then be able to define the ref task for each ref associated with an
  area/project in the "Tasks" section of the corresponding note file like we do for all
  other Obsidian tasks.
- You should migrate any existing ref notes that are associated with open ref tasks to
  use this new policy and move their ref tasks to the appropriate area/project note
  file.
- This complicates syncing the ref note status with the ref task a bit since we need to
  account for the possibility that the ref task gets moved to a "done" note file in the
  ~/bob/done/ directory at some point.
- Also, I think there is a lot of logic that currently treats ref tasks as special /
  something to filter out. We don't show them when pressing `^` to show today's /
  pending / next tasks in the bob-mac-capture app, for example. Just about all (probably
  all, but think hard about this so we don't break any invariants that I currently rely
  on) of this logic should be removed so we start treating ref tasks like any other
  task.
- This change will also require that we start prompting the user for a project / area
  note file when capturing new ref URLs (via the bob-mac-capture app or the
  `bob gkeep pull` command, for example) so we know which project / area note file to
  use.
- This project / area name should then be passed to the `bob ref create` command's new,
  required `-p|--parent` option.
- I currently use a sase (a GitHub project in the sase-org organization) file hook that
  uses this `bob ref create` command. We will need to start passing in the project name
  (e.g. "sase", "bob-cli") to the `-p|--parent` option.
  - I'm not sure that sase injects the project name into this file hook command string
    right now, so you might need to add support for that.
  - Also note that it is not guaranteed that the project name that gets passed in will
    exactly match the project note's name. For example, the "bob-cli" project name
    should actually map to the ~/bob/bob.md file. To work around this, we should add
    support for a new `project_name_aliases` frontmatter field to project notes that
    allows them to specify alternative names that will be matched by the `bob` command
    when searching for a project by name. We should set this field to `["bob-cli"]` for
    the ~/bob/bob.md project note.
- We will need to start giving ref tasks a different block ID since `^ref` will no
  longer be guaranteed to be unique. In order to make ref tasks stand out a bit more, we
  should also start rendering an appropriate icon/symbol instead of `#ref` when these
  tasks are rendered in Obsidian.
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
   dispatch's `research.0q.cdx`, `research.0q.cld`, `research.0q.grk`, `research.0q.mus`, `research.0q.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.0q.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.0q.linker`, can find it:

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