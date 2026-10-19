# Chat History - ace-run (research.4y.final)

- **TIMESTAMP:** 2026-10-19 08:51:12 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4y.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261019_080823.md`

## Prompt

%clan(research.4y, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to start rendering some kind of marker on tasks that are in today's daily
file when I view those tasks in Obsidian.

- We already do something similar to this for task links (to show which tasks are
  in-progress and which were unblocked today).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.4y.final %m:@xlarge
%wait:research.4y.cdx %wait:research.4y.cld %wait:research.4y.grk %wait:research.4y.mus %wait:research.4y.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to start rendering some kind of marker on tasks that are in today's daily
file when I view those tasks in Obsidian.

- We already do something similar to this for task links (to show which tasks are
  in-progress and which were unblocked today).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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
   dispatch's `research.4y.cdx`, `research.4y.cld`, `research.4y.grk`, `research.4y.mus`, `research.4y.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.4y.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.4y.linker`, can find it:

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

## Response

Reading the five researcher reports now (the artifact lookup needs to run from the main workspace directory).

Three reports read; now reading the mus and gem reports.

Checking how existing reading-view marks map rendered rows back to source lines, which decides whether the marker can be reliable outside Live Preview.

Reading the Today cache rebuild code to check the refresh timing and stale-data concerns the reports raised.

Today's ledger has 14 links across 7 notes, 6 of them in `sase.md`. Now looking at how those task lines look in their home notes.

I'm checking which Tasks query blocks mix Today and non-Today tasks, then I'll render a visual comparison of the candidate glyphs.

Now writing the consolidated report.

The freshness scope rules (`docs/freshness.md:337,361`) exclude Today tasks, so that claim holds. Adding the citation, then registering the report.

The report is registered (`file:explicit:446ebb4d348f98024a7dbc21`). Submitting the final declaration.

I've written the consolidated report and registered it for the linker (`file:explicit:446ebb4d348f98024a7dbc21`). The five reports and the report itself sit in `202610/today_task_line_marks/`, and the research repo commit happens when this turn ends.

## Recommendation

**Build it.** It fills a real gap: since Next and In Progress stopped expiring, a `[*]` or `[/]` checkbox no longer tells you whether a task is on today's plan. Today the vault has 29 committed tasks and 13 on today's plan. In `sase.md`, 5 of the 8 Next/In Progress rows are linked under today's Pomodoros, and they look exactly like the other 3.

**The mark:** a 🍅 drawn just after the `#task` hash glyph, before the title, on open tasks that are on today's plan.
- Nothing is written to the vault; it's computed from the Today cache bob-ledger-tools already keeps.
- Hovering names the Pomodoro and whether it's running or queued.
- Plain click places the cursor; Cmd/Ctrl+click jumps to the task's link in today's daily note.
- A command toggles the marks off and on for the session.

I rendered every researcher's proposed glyph on real `bob.md` rows, in light and dark themes. The tomato was clearly the best: the sun reads as a brightness icon, the grey `TODAY` pill is tiny and lands next to the existing `+ today` date label, and the orange outline looks like a timer. Bob's task picker already uses 🍅 to mean "linked under today's Pomodoro", and putting it after the hash keeps that column lined up.

## Changes to your requirements

1. **"In today's daily file" becomes "on today's plan".** That means tasks with a link under one of today's still-open Pomodoros, the same set as dash's TODAY section. Every October daily note contains exactly one task line, the `^gtd` row, so marking tasks that live in the file would mark one task a day.
2. **No mark for tasks worked earlier** whose Pomodoro has since closed. "Did I touch this today?" is a different question.
3. **No marks inside daily notes**, since the daily note is the plan itself.
4. **No marks in Tasks query results.** I checked: every dash query already separates Today tasks from the rest, so a mark there would add nothing.
5. **The word "today" never appears on the line**, because the date and freshness marks already use it with other meanings.
6. **Ship in two phases:** Live Preview first, then the rest. All four of your open editor panes are in Live Preview.

## What could go wrong

- **Reading view is the one real unknown.** Reading view hides block IDs, and an existing plugin comment claims a full note in reading view gives no way to map rows back to source lines. That claim has no recorded evidence, and other renderers in the same plugin already do this mapping. This needs a quick check in live Obsidian before phase 2; until then those rows simply show no mark rather than a guessed one.
- **Three small gaps in the existing Today cache need fixing first:**
  - The cache doesn't check that a linked task is still open, so the mark has to check the line itself.
  - Starting or renaming a Pomodoro doesn't trigger a refresh, so tooltips would go stale.
  - Two overlapping reads of the daily note can finish out of order and overwrite the newer result.
- **Possible surprise:** a task you worked on this morning loses its tomato once that Pomodoro closes, even though it's still In Progress. That's correct for "on today's plan", and the tooltip wording makes it clear.

## Open questions for you

1. The 🍅 emoji, or a custom tomato icon? A CSS variable lets you swap later without code changes.
2. Should "running now" versus "later today" stay in the tooltip, or also get a visual tint (I'd defer the tint)?
3. Should a plain click jump to the daily note, or place the cursor (my recommendation)?
4. Do you ever want a faint mark for tasks you worked on earlier today?

Files are in `202610/today_task_line_marks/`:
- today_task_line_marks__final.md
- today_task_line_marks__final_assets/candidates.png
- today_task_line_marks__final_assets/recommended.png
