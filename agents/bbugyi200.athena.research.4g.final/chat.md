# Chat History - ace-run (research.4g.final)

- **TIMESTAMP:** 2026-10-14 10:46:15 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4g.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261014_100238.md`

## Prompt

%clan(research.4g, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I
would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax.

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.4g.final %m:@xlarge
%wait:research.4g.cdx %wait:research.4g.cld %wait:research.4g.grk %wait:research.4g.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 4 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I
would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax.

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).

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
   in cdx, cld, grk, gem, belonging to this
   dispatch's `research.4g.cdx`, `research.4g.cld`, `research.4g.grk`, `research.4g.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.4g.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.4g.linker`, can find it:

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
├── <name>__gem.md
└── <name>__final.md
```

## Response

I've read the cdx report, and the canonical files match the latest registered snapshots, so each suffix maps to exactly one report. Next I'm reading the cld, grk, and gem reports.

I have all four reports. Now I'm checking the main disputed points against the source, starting with how much the existing Pomodoro cleanup helpers delete.

All research is done. I'm moving the four reports into `202610/capture_star_blocks_modifier/` and then writing the consolidated report.

Registration succeeded. Now submitting the final declaration.

I merged the four reports with my own checks into one report, and it's registered for the linker as `research:202610/capture_star_blocks_modifier/capture_star_blocks_modifier__final.md`. The four original reports moved into the same folder, keeping their suffixes. The research-repo commit runs after this turn ends.

For cdx and cld, two snapshots each were registered under one file path; the file in the research repo matches the later snapshot, so each suffix resolved to exactly one report. I ran no new capture tests; the behavior tests cited come from cdx and cld.

**Is it a good idea? Yes, build it.** `N *note:id` is just `&` with the roles swapped: it adds N to the other task's Depends-On line. That needs no new data model. Today the same result takes two capture items, a block ID you make up yourself, and it can't reach tasks in nested notes at all.

**Your third requirement already exists.** A Blocked task already loses its Task Links under today's open Pomodoros, and capture `&` and `bob task reconcile` already enforce it. `*` should reuse that code path, but four problems in it need fixing first, because `*` makes it the common case:
1. **It deletes your notes.** When a link has notes indented under it, the link and its notes are removed together. I scanned your last 90 daily notes: 212 of 1,613 Pomodoro Task Links (13%) have notes under them, on 57 of the 90 days. That's exactly the "I was working on T and hit a blocker" case.
2. **It deletes silently.** Removed links and deleted Pomodoros, even the running session, show up only as a one-line warning. This is already filed as `bob-cli-7l`.
3. **It deletes more than you asked.** It removes every childless Pomodoro in today's file, not just the one it emptied. Reconcile does the same on every run, so this isn't data loss, but it makes "iff it becomes empty" untrue in the preview.
4. **It matches links by exact text.** Tasks in nested notes, which `*` makes reachable for the first time, would be missed.

**Disagreements between the reports, and how I settled them:**
- **Notes under a removed link:** keep them under a plain-text bullet. cdx wanted this; cld and grk wanted to keep the current deletion rule. This changes an accepted rule (PDL7), so it needs your approval.
- **The new task's status:** it takes over the blocked task's commitment (Next or Pending), capped at Next. Otherwise blocking a Next task leaves neither task committed. grk wanted no takeover; cdx wanted it to become Pending (`[/]`) when the blocked task was.
- **Blocking with an existing task** (`*T @route+id`): allow it. It's the exact mirror of what `&` already supports.
- **When a lone `*` opens the picker:** only after other text on the same line. The Mac app already treats a `*` at the start of a line as a bullet.
- **JSON field names:** use `blocked_task*`. `task_blocks`, which grk and gem proposed, is already a capture output field.
- **gem's "take its slot" example was invalid,** because `=` starts a Pomodoro session command. The working form is `N @inbox:id *T`. That links N into the session before T's link is removed, so the session survives.

**Recommended changes to your requirements** (the full table is §4 of the report):
- Only live links under today's open Pomodoros are removed. Closed sessions, history, and other days are untouched.
- "Pomodoro" means the session entry, not the `## Pomodoros` heading. "Empty" means it has no child lines at all.
- The new task always gets a block ID automatically.
- Blocked tasks must be open. Blocking a project's `^prj` task is allowed, but the preview must show how many tasks that blocks.
- Lone `*` that's really Markdown (`*italic*`, `**bold**`, `* bullet`, `5 * 3`) stays literal text.
- The new task is never linked into the freed slot automatically; you opt in by linking it yourself.

**Recommended plan:**
1. Write the contract docs and a decision record.
2. Fix the four problems above. This also improves `&` today.
3. Add the bob-cli parsing and picker support (and fix `bob-cli-7m`, a parsing bug `*` would inherit).
4. Add the bob-cli write path.
5. Update the Mac picker and preview.

Rough size: medium for bob-cli, small to medium for the Mac app.

**Decisions for you:**
1. Cap the new task at Next, or let it become Pending when the blocked task was Pending?
2. Approve keeping notes when a link is removed?
3. Keep `*`, or use `?`, which matches the blocked task's `[?]` and needs no Markdown guards?
4. Include existing-task blockers in the first version?
