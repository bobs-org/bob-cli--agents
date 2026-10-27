# Chat History - ace-run (research.28.final)

- **TIMESTAMP:** 2026-10-21 08:08:11 EDT
- **MODEL:** claude/opus
- **AGENT:** research.28.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261021_072819.md`

## Prompt

%clan(research.28, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to start rendering nice appropriate icons in-place of `#gtd #pre` and
`#gtd #post` (i.e. the tags that specify which Obsidian tasks belong to our PRE and POST
GTD morning review groups, respectively).

- I would also like to start doing something about the `repeat` task property to make it
  look nicer and take up less space when rendered in Obsidian, but I'm not sure what (if
  anything) we should do for this one.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.28.final %m:@xlarge
%wait:research.28.cdx %wait:research.28.cld %wait:research.28.grk %wait:research.28.mus %wait:research.28.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to start rendering nice appropriate icons in-place of `#gtd #pre` and
`#gtd #post` (i.e. the tags that specify which Obsidian tasks belong to our PRE and POST
GTD morning review groups, respectively).

- I would also like to start doing something about the `repeat` task property to make it
  look nicer and take up less space when rendered in Obsidian, but I'm not sure what (if
  anything) we should do for this one.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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
   dispatch's `research.28.cdx`, `research.28.cld`, `research.28.grk`, `research.28.mus`, `research.28.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.28.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.28.linker`, can find it:

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

I've read the first of five researcher reports (cdx); reading the remaining four now, then I'll verify disagreements against the plugin source.

Census confirmed (cdx's numbers are right; gem's and mus's open-row counts are off). Next I'm checking which Tasks queries show recurring rows, and in what layout.

I'm now rendering a mockup to compare the remaining glyph and label options at actual size. It covers where the Today 🍅 lands, the `⧗ Mon` label collision, and the final recommended rows.

Both citations hold. Now I'm moving the five reports and cld's mockup into the new folder.

Confirmed. Writing the consolidated report now.

`fragments.json` is an explicit ordered list, and no fragment uses a letter suffix. I'll name free numeric slots instead of `138b`/`136b`/`266b`.

The report is in place. Registering it as a durable artifact for the linker.

Registered. Now submitting the final declaration.

The consolidated report is written and registered for the linker (`file:explicit:7475def815b11f2111ad7daf`). All five reports and cld's mockup now live in `202610/gtd_checklist_glyphs_and_recurrence_marks/`, and the host will commit the research repo when this turn ends.

**Verdict: build both. It's a good, cheap idea.** It only changes how things look, inside the existing "marks" in bob-ledger-tools (the teal `#task` hash, the 📖 book, the date marks). Nothing changes in storage, the evaluator, Tasks or Dataview. All five researchers agreed on that layer.

**Recommended design:**
- **PRE/POST:** one teal glyph replaces the whole `#task #gtd #pre` (or `#post`) run, sitting where the hash sits now. PRE is a **sunrise** and POST is a **flag**. This is my main change to your request: replace all three tags, not just `#gtd #pre`. It follows how `#task #ref` already became 📖, and it keeps the Today 🍅 right after the glyph with no code change. If the glyph sat after the hash instead, 🍅 would land between the two.
- **`repeat`:** a quiet loop glyph plus the cadence in plain words: `daily`, `Mondays`, `monthly · 1st`, `every 30 days`. The exact rule and its `when done` meaning go in the tooltip.
- **Reliability rule:** a glyph appears only when the display is certain. Conflicting tags, typos, rules Tasks can't read, and PRE/POST rows missing `when done` keep a raw pill, and that pill means "fix me."

**Where the reports split, and how I settled it** (checked against the code and vault):
- **POST glyph:** a sunset says evening, but POST closes the *morning* review. The flag is also the easiest shape to tell apart from the sunrise at 14 px, and `gtd_daily.md` has no PRE/POST headings to help.
- **Repeat glyph:** a circular arrow is already used twice, by the review footer's `⟳` and by the due-freshness mark. So the repeat glyph is a rectangular loop.
- **Weekly label:** `Mondays`, not `Mon`. Date marks already render *Weekly prune*'s date as `⧗ Mon`, so `Mon` would appear twice on that row.
- **Interval label:** `every 30 days`, not `30d`. The date marks already rejected that kind of abbreviation.
- **Two reports had wrong facts, now corrected:**
  - `dash.md`'s TODAY query is full mode, not short mode, so Tasks results need handling there.
  - The open-row counts were off. The actual census is 10 checklist rows (8 PRE, 2 POST) and 14 open repeat rows, with 98% of all 973 rules being `every day when done`.

My own contribution was a mockup of the final rows, rendered in light and dark at actual size. It's at `…__final_assets/mockup.png`, and `mockup.html` beside it holds the glyph paths to copy. The first sunrise drawing sat low and its rays floated, so I redrew it to fill the glyph box.

**Open questions for you:**
- Does the sunrise read well enough on the iPhone? If not, a small teal `PRE`/`POST` text chip is a one-line swap.
- Is `when done` in the tooltip enough? One researcher (cdx) wants it shown on the line.
- Do you want the 🌅/🏁 prefixes in task pickers later?

The plan also proposes one vault edit for you to approve: add `hide recurrence rule` to the RECURRING query in `blocked.md`. That query already groups by rule, so every row currently repeats its own heading.
