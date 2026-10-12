# Chat History - ace-run (research.0u.linker)

- **TIMESTAMP:** 2026-10-11 06:21:20 EDT
- **MODEL:** claude/opus
- **AGENT:** research.0u.linker
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261011_052055.md`

## Prompt

%id(linker, clan=research.0u) %m:@xlarge
%wait:research.0u.final %wait:research.0u.image %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the linker agent for a research swarm. The lead researcher,
`research.0u.final`, has written a consolidated report on the request below. Your job
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

I
want to start tracking my daily habits/stats somehow.

- Each of the stats I would like to track (ATM at least) boils down to a single integer
  per day:
  - The total number of morning GTD review tasks I completed each day (by iterating over
    and processing each one using the `]s` keymap).
  - The total number of pomodoro hours and minutes worked each day. Note that I already
    show this via an inline query in the "Pomodoro" section of each daily file.
  - The total number of tasks that I complete each day.
  - The total number of tasks that I create each day.
  - Think hard about what other metrics I should consider tracking in this v1
    implementation.
- It also needs to be easy to start tracking new daily metrics like these that I think
  of later.
- I'm not sure what the UX should look like for this, but it should make it easy to
  visualize my progress for a given metric over a given time period (which I should be
  able to adjust).
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
   with `wait_name` `research.0u.final` whose label has the form
   `research:<YYYYMM>/<name>/<name>__final.md`. If there is not exactly one such entry,
   stop and report the missing or ambiguous input instead of guessing. Open the research
   repo with `/sase_repo`, then read the report through its canonical research reference
   (or the `ref` field's `file:<id>` reference if the original has moved) using
   `sase artifact read`. Take `<YYYYMM>/<name>/` from the label, never from the current
   date. Do not read predecessor chat transcripts. Never modify, move, or delete
   `<name>__final.md` or the drafts.

2. **Inventory what must survive.** Before writing, list every finding, recommendation,
   caveat, open question, confidence statement, number, date, version, code block,
   table, and link in the lead's report.
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
├── <name>__mus.md
├── <name>__gem.md
├── <name>__final.md
├── <name>_infographic.png
└── <name>.md
```

## Response

Reading the lead's report now (it matches the file on disk); next I'll inventory it and restructure it into the canonical `bob_daily_stats.md`.

Now checking the external links and confirming the report has no frontmatter.

The research query runs to four sentences, over the three-sentence limit. Tightening it.

Now validating anchors with pandoc, URL coverage, and a word-level diff against the lead's report to catch anything dropped.

Registered. Confirming the research repo only gained the new file and the drafts are untouched.

I published the lead's report as `202610/bob_daily_stats/bob_daily_stats.md` in the research repo and registered it as a snapshot (`research:202610/bob_daily_stats/bob_daily_stats.md`, ref `file:explicit:126ebffaacff8ee28b16fb11`). The commit is declared and will happen after this turn ends. The lead's report and the drafts are untouched.

**How the file opens:** the title, then a two-sentence research query, then the infographic, then `## Bottom line`. The infographic was already in the directory beside the report.

**What I changed:**
- **Headings:** removed the hand numbering. Where a heading held code or a label in brackets (`src/native/stats/`, `cli_rules`, `bob stats`, "(v1)", "(the one new writer)"), I moved that text to the section's first line.
- **Section order:** kept the lead's order, which ends with the recommended solution. The opening "Lead researcher consolidation · 2026-10-11 · Inputs…" line is now an "About this report" section just before Sources. The UX section links to it for the "all mockup values are illustrative" note.
- **Cross-references:** every `§` reference is now a link to the right section. I added a few more links from the bottom line, the cheaper-fallback paragraph, the requirement table and the recommended solution. Every link target exists when converted with pandoc, and no anchor is used twice.

**Checks:**
- A word-level diff against the lead's report shows only the edits above. No claims, numbers, tables, the six code blocks or the 11 sources were dropped.
- All 11 external URLs are still in the file. Ten returned 200 with no redirects.
- The flowingdata.com "Graphical perception" link returned 403, so it is unverified rather than broken; I kept it.
- No links needed repair.
