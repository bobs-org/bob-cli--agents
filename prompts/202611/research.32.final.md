- **AGENTS:**
  - [bbugyi200.apollo.research.32.final](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.32.final/README.md)

%clan(research.32, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I want to
make some improvements to the way we handle freshness updates using the `<alt+f>` and
`<ctrl+alt+f>` keymaps.

- I want to generalize and unify the "task decay" supported by bob currently. We should
  add a new glossary term for "task decay" that does a good job of explaining this new /
  improved policy.
- We should add one more more appropriate config field to make this functionality
  flexible (I was thinking just allowed rolls for each task status, but I'll let you
  decide) and add them to my bob/config.yml file in my chezmoi repo (with good, but
  concise, comments).
- I would like my bob to allow 2 keeps in each status/priority before defaulting to
  rolling to the next status/priority. We already support this for priorities I believe,
  but it should be configured explicitly.
- We already support a way to decay ready tasks (after 3 keeps currently--this should be
  changed to 2).
  - There seems to be a problem with ready task decay right now though that you should
    look into.
  - Namely, it says that no priority ladder is configured (I think we should just always
    use P1, right?).
  - We should fix this issue as a part of this change.
  - See the ~/tmp/screenshots/20261102_134505.png screenshot for context.
- WIP tasks should decay to next tasks by default when their keep limit has been
  reached.
- Next tasks should decay to ready tasks by default when their keep limit has been
  reached.
- The user should have an option to keep the status the same for all of these
  transitions / prompts, which should reset the keep count for that task.
- Make sure the rotten log entries reflect all of these transitions appropriately.
- Let's stop prompting for a work log entry when marking WIP tasks as fresh in Obsidian.
  These WIP tasks should be considered rotten, which means that we should prompt for a
  rotten log entry instead.
- We should continue to prompt for a rotten log entry for next tasks (like we do now),
  but a rotten log entry should always be added (either explicitly or using a default).
- If the user does not give a rotten log entry, then a default one should be added which
  specifies the status that was kept (make sure it is clear how many times each task was
  kept in each status). We already do something like this for ready tasks I believe, but
  we might want to unify the process a bit (I'll let you decide on this one).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]])
%id:research.32.final %m:@xlarge %wait:research.32.cdx %wait:research.32.cld
%wait:research.32.grk %wait:research.32.mus %wait:research.32.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are the lead researcher: 5 independent researchers have
reported on the request below, and you will add your own research and merge every
perspective into one consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I want to make some improvements to the way we handle freshness updates using the
`<alt+f>` and `<ctrl+alt+f>` keymaps.

- I want to generalize and unify the "task decay" supported by bob currently. We should
  add a new glossary term for "task decay" that does a good job of explaining this new /
  improved policy.
- We should add one more more appropriate config field to make this functionality
  flexible (I was thinking just allowed rolls for each task status, but I'll let you
  decide) and add them to my bob/config.yml file in my chezmoi repo (with good, but
  concise, comments).
- I would like my bob to allow 2 keeps in each status/priority before defaulting to
  rolling to the next status/priority. We already support this for priorities I believe,
  but it should be configured explicitly.
- We already support a way to decay ready tasks (after 3 keeps currently--this should be
  changed to 2).
  - There seems to be a problem with ready task decay right now though that you should
    look into.
  - Namely, it says that no priority ladder is configured (I think we should just always
    use P1, right?).
  - We should fix this issue as a part of this change.
  - See the ~/tmp/screenshots/20261102_134505.png screenshot for context.
- WIP tasks should decay to next tasks by default when their keep limit has been
  reached.
- Next tasks should decay to ready tasks by default when their keep limit has been
  reached.
- The user should have an option to keep the status the same for all of these
  transitions / prompts, which should reset the keep count for that task.
- Make sure the rotten log entries reflect all of these transitions appropriately.
- Let's stop prompting for a work log entry when marking WIP tasks as fresh in Obsidian.
  These WIP tasks should be considered rotten, which means that we should prompt for a
  rotten log entry instead.
- We should continue to prompt for a rotten log entry for next tasks (like we do now),
  but a rotten log entry should always be added (either explicitly or using a default).
- If the user does not give a rotten log entry, then a default one should be added which
  specifies the status that was kept (make sure it is clear how many times each task was
  kept in each status). We already do something like this for ready tasks I believe, but
  we might want to unify the process a bit (I'll let you decide on this one).
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

$(sase repo path research --ensure)/$(date +%Y%m)

Steps:

1. From the registered reports above, identify exactly one report per expected suffix in
   cdx, cld, grk, mus, gem, belonging to this dispatch's `research.32.cdx`,
   `research.32.cld`, `research.32.grk`, `research.32.mus`, `research.32.gem`
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
   `research.32.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.32.linker`, can find it:

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
