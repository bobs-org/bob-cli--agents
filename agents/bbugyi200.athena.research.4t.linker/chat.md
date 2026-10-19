# Chat History - ace-run (research.4t.linker)

- **TIMESTAMP:** 2026-10-18 16:10:15 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4t.linker
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261018_150547.md`

## Prompt

%id(linker, clan=research.4t) %m:@xlarge
%wait:research.4t.final %wait:research.4t.image %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the linker agent for a research swarm. The lead researcher,
`research.4t.final`, has written a consolidated report on the request below. Your job
is to publish that report as the canonical `<name>.md`: the file readers open, and the
one SASE renders into a Highlights PDF. You are an editor, not a researcher. The new
file must carry exactly the lead's meaning and intent. Do not do research of your own:
add no new claims or sources, settle no open questions, and neither soften nor
strengthen the conclusions or the recommendation. If the lead seems wrong, leave it as
written. The only prose you write yourself is the short research-query summary of the
request that opens the file (step 3).

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request (context only; do not research it, but summarize it as the file's
research query in step 3):

We currently label every pomodoro with a theme and use these themes to aggregate
statistics in the ~/bob/dash_stats.md file. I would like to start automatically labeling
pomodoros by the corresponding projects and/or areas of the task links contained in
them.

- As a part of this change, we should start aggregating the stats shown in the
  ~/bob/dash_stats.md file by area and project when possible.
- We will need the ability to exclude sub-projects of some projects from being
  aggregated and/or used to label pomodoros directly. Instead, task links to tasks in
  these sub-projects should be treated as if (when labeling pomodoro and aggregating
  stats) they pointed to tasks in the parent project that configured this. We should
  configure the ~/bob/sase.md project note to use this functionality.
- I'm not sure how/when/what to label pomodoros, so you should think hard about this.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.

The lead researcher's registered report:

{% for a in wait.artifacts if a.kind == "markdown" and a.label and a.label.startswith("research:") %}
- wait_name={{ a.wait_name }} label={{ a.label }} source_path={{ a.source_path }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}

The image agent's registered images:

{% for a in wait.artifacts if a.kind == "image" %}
- wait_name={{ a.wait_name }} label={{ a.label }} vcs_relpath={{ a.vcs_relpath }} path={{ a.path }} ref={{ a.ref }}
{% endfor %}


Steps:

1. **Identify the source.** From the registered reports above, find exactly one entry
   with `wait_name` `research.4t.final` whose label has the form
   `research:<YYYYMM>/<name>/<name>__final.md`. If there is not exactly one such entry,
   stop and report the missing or ambiguous input instead of guessing. Open the research
   repo with `/sase_repo`, then read the report through its canonical research reference
   (or the `ref` field's `file:<id>` reference if the original has moved) using
   `sase artifact read`. Take `<YYYYMM>/<name>/` from the label, never from the current
   date. Do not read predecessor chat transcripts. Never modify, move, or delete
   `<name>__final.md` or the drafts.

2. **Inventory what must survive.** Before writing, list every finding, recommendation,
   caveat, open question, confidence statement, number, date, version, code block,
   table (record its cells; step 3 converts each one into a list), and link in the
   lead's report.
3. **Restructure** the lead's report into a well-thought-out organization:
   - Keep the frontmatter, updating `updated_time` if present.
   - **Open the file in this exact order**, with nothing else between these parts: the frontmatter (if any), one `#` title, the research query, the infographic, and then the bottom-line section.
   - **Research query.** Directly below the title, add one blockquote that summarizes
     the research request above in one to three sentences, for example
     `> **Research query:** <summary>`. Phrase it as the question or task being
     answered, in the requester's own terms: keep the questions, named subjects, and
     explicit scope or constraints; drop instructions aimed at agents, such as output
     paths, macro or directive syntax, and formatting requests. Summarize what was
     asked, not material the request quotes or attaches. Use a request that is already
     one short sentence verbatim. Never fold findings, answers, or scope the request
     does not state into it. It is not a heading, so it gets no section number and no
     TOC entry.
   - **Embed the infographic** exactly once, directly above the bottom-line section:
     after the research query and before that section's `##` heading, never further
     down. Use a relative link with descriptive alt text, for example
     `![<alt text>](<name>_infographic.png)`. Locate it by the
     `<name>_infographic.png` convention or the image entries above. Embed only a file
     you have confirmed exists beside the report in your research checkout. If the
     image agent completed without producing one, publish without it (the research query then sits directly above the bottom-line section) and say so in the final
     response.
   - **Bottom-line section.** The first `##` section is `## Bottom line` (or
     `## Overview` when the report surveys options rather than giving one answer) and
     gives the answer first.
   - Below it, `##` and `###` sections ordered by the questions a reader will ask, with
     duplicated passages merged.
   - **Never number headings.** The PDF renderer runs pandoc with `--number-sections`,
     so hand-numbered headings render doubly numbered.
   - **No table of contents and no block of jump links.** The PDF already gets a TOC.
   - **No tables.** The PDF renderer (pandoc → XeLaTeX) prints tables with equal-width
     columns, cramped wrapped cells, and rows that jump pages. Convert every table in the
     lead's report (pipe, grid, simple, multiline, or HTML) into a list with one item per
     row, keeping every cell's content:
     - Two columns: `- **<first cell>:** <second cell>`.
     - Three or more columns: a bullet whose first line is the row's identifying cell in
       bold (merge an ID column into it, e.g. `- **A1. Restart exactly once**`), then one
       nested bullet per remaining non-empty cell, `- *<Column header>:* <cell>`, in column
       order. Labels go in italics so bold inside a value stays distinct.
     - Ordered rows (phases, steps, ranks, tiers): the same shapes as a numbered list,
       keeping the original numbers.
     - Grouped rows (a blank first cell continues the group above): nest them under one
       bullet for the group.
     - Rows whose cells are all a few words: one line,
       `- **<row>:** <header> <value> · <header> <value> · …`.
     - Numbers: keep units, periods, denominators, and the difference between zero,
       unknown, and not applicable.
     - Long code in a cell: a fenced code block inside the list item.
     - Only when the rows are about six or fewer major named options the report discusses
       at length: one `###` section per option holding the same italic-labelled bullets.
       Never turn a row into a `####` heading. Turn a table caption into a one-line lead-in
       sentence. Put a blank line before every list (pandoc otherwise merges it into the
       paragraph above). Indent nested bullets 2 spaces under `- ` and
       3 spaces under `1. `. Write URLs as `[text](url)` or `<url>`, never bare. Do not
       substitute a definition list (`Term` then `: definition`), an HTML table, a grid
       or simple table, a table in a code block, a callout or `:::` div, raw LaTeX, or
       an image. Never drop a cell, merge two rows, or add totals, rankings, or
       conclusions the table did not state.
   - Keep the lead's wording where it works. Never drop a claim, caveat, or source to
     save space. If the lead's report restates the question or lists its inputs, keep
     those details in a later section; the research query summarizes the request but
     does not replace them.
4. **Validate every link carried over.**
   - Relative links resolve from `<YYYYMM>/<name>/`, and in-document anchors resolve
     against the final headings. Both are hard requirements.
   - Check external URLs with `curl -fsSL -o /dev/null --max-time 20 <url>`, retrying
     a transient failure once. Treat 401, 403, 429, and timeouts as _unverified_ and
     keep those links.
   - Verify repository-file links through a `/sase_repo` checkout, not by fetching
     github.com.
   - Repair a link only when the right target is certain: a followed redirect, a moved
     file, an obvious typo, or a renamed heading. For an unrepairable link, keep its
     text, drop the dead URL, and list it in the final response. **Never search for a
     replacement source.**

5. **Add in-document links** so readers can jump between parts of the file. Add them
   inline and sparingly: from summary points to the sections that back them, from "see
   above" or "see below" phrases, and from mentions of a named option, phase, or
   finding to where it is discussed. Do not link every mention.
   - Every heading used as a link target must start with a letter, contain only
     letters, digits, spaces, and hyphens, and be unique. Its anchor is then the
     lowercased heading with spaces replaced by hyphens, for example
     `[the bottom line](#bottom-line)`. pandoc (the PDF) and GitHub then agree.
   - Move emoji, version numbers, and code out of such headings, into the section's
     first line.
   - When `pandoc` is available, confirm anchors with `pandoc <file> -t html`.

6. **Re-check against the step-2 inventory** and restore anything missing or changed.
   Every URL in `<name>__final.md` must appear in the new file unless it was listed as
   unrepairable. Then confirm the file opens in the step-3 order: title, research query, infographic, bottom-line section.
   Confirm every cell of every table in the lead's report appears in the new file. When
   `pandoc` is available, confirm no table survives:
   `pandoc <file> -f markdown -t json | grep -o -i -E '"t":"Table"|"t":"RawBlock","c":\["html","<table' | wc -l`
   prints `0`.

7. **Write** `<YYYYMM>/<name>/<name>.md` without overwrite. On a collision, stop and
   report it.

8. **Register** it as a durable snapshot:

   sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

   Use the report's actual absolute path and its path relative to the research repo
   root, for example `research:202609/<name>/<name>.md`. Use no `--move`. If
   registration fails, report it and do not claim full completion.

Final layout:

```text
<month-dir>/<name>/
├── <name>__cdx.md
├── <name>__cld.md
├── <name>__grk.md
├── <name>__gem.md
├── <name>__final.md
├── <name>_infographic.png
└── <name>.md
```

## Response

I've opened the research repo and read the lead's final report. Next I'll go through its contents before restructuring it.

Checking one earlier published report for house style, then I'll write the restructured file.

Writing the restructured report now; every table becomes a list and the § references become in-document links.

Validating anchors, tables, and the opening order with pandoc.

No tables remain, every anchor resolves, and the infographic exists. Next, an automated inventory check that compares code spans, numbers, and words against the lead's report.

Only heading numbers are missing, and one bold lead became a `###` heading. Restoring "called out" in the adjustments lead-in:

Lists parse correctly and the only remaining `§` points to a section in an external doc, so it stays. Registering the report:

Registered. Now the final declaration, which covers the new file in the research repo.

I published the lead's report as the canonical file `202610/pomodoro_area_project_attribution/pomodoro_area_project_attribution.md` in the research repo and registered it as a durable snapshot (`file:explicit:8e99f203ae2079b1f901b3da`). The host will commit it to the research repo once this turn ends.

**How it opens:** the title, then a two-sentence research query, then the infographic (`pomodoro_area_project_attribution_infographic.png`, which exists beside the report), then `## Bottom line`.

**What changed from the lead's draft:**
- **Headings:** they are no longer numbered, and none contain code or punctuation that would break their link anchors.
- **Section order:** critique → requirement adjustments (A1–A9) → verified evidence → the model → labels → stats and the dashboard → where the reports disagreed → rejected alternatives → implementation plan → risks → open questions → recommended solution → sources.
- **Opening line moved:** the lead's "Lead synthesis · 2026-10-18…" line, which names the commits it checked against, is now the first paragraph of Sources so nothing sits between the title and the bottom line.
- **Tables:** all nine are now lists with every cell kept, including the empty "other effects" cell, "n/a", and "—". pandoc confirms 0 tables remain.
- **Section references:** each "§4.6", "§10 Q5" and similar is now a link to the named section, since the PDF's automatic numbering would differ from the lead's. I also added a few links from the bottom-line rules to the sections that back them. The one remaining `§Pomodoro Marker` stays because it points into `docs/task-status-hooks.md`, not this report.
- **Wording I added:** only the research query and short one-line lead-ins where tables or headings used to be.

**Checks:**
- **Inventory:** all 5 code blocks and every code span carried over. The only numbers missing are the old heading and § numbers.
- **Links:** the lead's report had no external URLs, so none needed checking and none were unrepairable. Every in-document anchor resolves in pandoc's HTML output, and the only relative link (the infographic) resolves.
