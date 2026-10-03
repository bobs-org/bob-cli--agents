# Chat History - ace-run (research.32.linker)

- **TIMESTAMP:** 2026-10-01 01:28:15 EDT
- **MODEL:** claude/opus
- **AGENT:** research.32.linker
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261001_003004.md`

## Prompt

%id(linker, clan=research.32) %m:@xlarge
%wait:research.32.final %wait:research.32.image %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the linker agent for a research swarm. The lead researcher,
`research.32.final`, has written a consolidated report on the request below. Your job
is to publish that report as the canonical `<name>.md`: the file readers open, and the
one SASE renders into a Highlights PDF. You are an editor, not a researcher. The new
file must carry exactly the lead's meaning and intent. Do not do research of your own:
add no new claims or sources, settle no open questions, and neither soften nor
strengthen the conclusions or the recommendation. If the lead seems wrong, leave it as
written.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request (context only; do not research it):

I
have made a few major changes to my morning GTD and pomodoro practices today. Can you
review those changes with the goal of helping me improve my current practices further?
Namely, what am I getting wrong? Keep in mind that I haven't been doing my morning GTD
in the last month, so the data is a bit biased/unaccurate at the moment (there are a lot
of tasks I need to go back and mark as complete still, for example). End your analysis
with a ranked list of recommended improvements that you think I should consider making
to my process.

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
   with `wait_name` `research.32.final` whose label has the form
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
   - One `#` title, then the bottom line or answer first.
   - `##` and `###` sections ordered by the questions a reader will ask, with
     duplicated passages merged.
   - **Never number headings.** The PDF renderer runs pandoc with `--number-sections`,
     so hand-numbered headings render doubly numbered.
   - **No table of contents and no block of jump links.** The PDF already gets a TOC.
   - Keep the lead's wording where it works. Never drop a claim, caveat, or source to
     save space.
   
   - Embed the infographic exactly once, where it best supports the text (usually
     right after the bottom line). Use a relative link with descriptive alt text, for
     example `![<alt text>](<name>_infographic.png)`. Locate it by the
     `<name>_infographic.png` convention or the image entries above. Embed only a file
     you have confirmed exists beside the report in your research checkout. If the
     image agent completed without producing one, publish without it and say so in the
     final response.
   
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
   unrepairable.

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

Read the lead's report (532 lines). Next I'll check the raw file for frontmatter and verify the infographic and links.

Links all return 200; the report has no frontmatter. Now checking the infographic content for alt text.

Writing the restructured report now.

Validating anchors, relative links, URLs, and content preservation.

Anchors, files, and URLs all check out. Now a word-level diff against the lead's report to confirm nothing was dropped.

Registration worked. Last step is the final declaration.

I've published the report as `202610/gtd_morning_review_pomodoro_cutover/gtd_morning_review_pomodoro_cutover.md` and registered it as `file:explicit:33267a84976c7a860160b4af` under the label `research:202610/gtd_morning_review_pomodoro_cutover/gtd_morning_review_pomodoro_cutover.md`. The commit was declared and the host makes it after this turn ends. I didn't touch `__final.md` or the drafts.

**What changed from the lead's report**
- **Order:** the title is followed directly by the bottom line, with the infographic right after it. Then come What changed, What is working, the nine findings, the ten ranked recommendations, the morning script, how to judge the next 14 days, where the reports disagreed, scope and limitations, and sources.
- **Headings:** I removed the hand-numbering and the punctuation that breaks anchors. To keep the "finding N" and "recommendation 7" references and the ranking clear, each section now opens with a **Finding N.** or **Rank N.** label. Text that sat in parentheses in a heading (for example "2–4 blocks named CUTOVER, not GTD" and "≤25 minutes, in this order") moved to the section's first line.
- **Merged duplicate:** the report opened with your "data is biased" caveat, and its Limitations section repeated it as "Old data". These are now one bullet in the Scope and limitations section, with all of its points kept.
- **Links added:** each of the six bottom-line points links to its finding, and every "Why: finding N" links to that finding. I also linked "the script below", "the signals below", "recommendation 7" and "keep rule". The five researcher reports in Sources are now relative links.

**Checks**
- **Content:** a word-for-word comparison against `__final.md` found nothing missing apart from reworded heading words and the merged caveat. No claims, numbers or sources were added.
- **Links:** all 13 in-document anchors match the headings pandoc generates, and the infographic and five draft files exist beside the report. All five external URLs returned HTTP 200, so none was dropped or repaired.
- **Infographic:** embedded once, after the bottom line.

One thing I noticed but didn't change: the infographic says "about 30–55 due each morning, Oct 2–8". The report's bottom line says "39–55", though its own forecast table has 30 on Tue 10-06. Both come from upstream, so I left them as the lead and image agent produced them.
