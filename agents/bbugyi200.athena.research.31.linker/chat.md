# Chat History - ace-run (research.31.linker)

- **TIMESTAMP:** 2026-09-30 23:55:10 EDT
- **MODEL:** claude/opus
- **AGENT:** research.31.linker
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_225800.md`

## Prompt

%id(linker, clan=research.31) %m:@xlarge
%wait:research.31.final %wait:research.31.image %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the linker agent for a research swarm. The lead researcher,
`research.31.final`, has written a consolidated report on the request below. Your job
is to publish that report as the canonical `<name>.md`: the file readers open, and the
one SASE renders into a Highlights PDF. You are an editor, not a researcher. The new
file must carry exactly the lead's meaning and intent. Do not do research of your own:
add no new claims or sources, settle no open questions, and neither soften nor
strengthen the conclusions or the recommendation. If the lead seems wrong, leave it as
written.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request (context only; do not research it):

I am
in a position where I have near infinite tokens, but for the next 48 hours only. I'm
trying to think of some high value work that is also something I can run in a loop
(using the same or a similar prompt over and over again with /sase_handoff, for
example). Can you do some research with the goal of recommending some work that I should
consider that fits this pattern? End your analysis with a ranked list of recommendations
that you genuinely feel I should consider.

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
   with `wait_name` `research.31.final` whose label has the form
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

I've read the lead's report and confirmed the infographic exists. Next I'll look at the image so I can write accurate alt text, then do the inventory and restructure.

Writing alt text from the infographic now; next I'm checking the external URLs before drafting the restructured file.

Validating the anchors with pandoc, checking that every relative link and URL survived, and diffing the content against the lead's text.

All anchors and links resolve, and the URL sets match. Now a word-level check that no content from the lead was dropped.

Registration succeeded. Finishing with the final declaration.

I published the lead's report as `202609/token_window_48h_loop_portfolio/token_window_48h_loop_portfolio.md` in the research repo and registered it as a durable snapshot (`file:explicit:553a37c913f4a5586a3e0c1d`, label `research:202609/token_window_48h_loop_portfolio/token_window_48h_loop_portfolio.md`). The host commits it after this turn ends.

**Source:** there was exactly one `research.31.final` entry, which I read with `sase artifact read`. It had no frontmatter, so there was no `updated_time` to update. I left `__final.md` and the drafts untouched, and the new file didn't exist before, so nothing was overwritten.

**Structure:**
- The title, byline and question come first, then the bottom line, then the infographic (embedded once).
- After that come: the lead's checks (with "External evidence I re-checked" as its own subsection), where the reports disagreed, how loops run in SASE, what not to spend the window on, the 48-hour schedule, sources, and the ranked recommendations.
- I kept the lead's order so the ranked list stays last, because the request asked for the analysis to end with it.
- In "How loops run" I split the lead's single section into three subsections: loop primitives, iteration contract, and capacity. Each of the six disagreements also became its own subsection.

**Headings:**
- No heading is hand-numbered.
- The ranked items are titled "Lane 1 - …" through "Lane 9 - …", using the lead's own "lane N" naming. I added one line saying each lane's number is its rank. The lead only uses "lane" for items 1–7, so "Lane 8" and "Lane 9" are my extension of that wording.
- Punctuation, code and ↔ moved out of headings into each section's first line.

**Links:**
- Every `§N` cross-reference is now an anchor link.
- I added a few inline links: from the bottom line to the sections behind it, between lanes, and from "cld §7" to the cld draft.
- `pandoc -t html` confirmed that every in-document anchor resolves. All six relative links resolve (the five drafts and the infographic).
- All 10 external URLs returned 200, and the same URLs appear the same number of times as in `__final.md`. Nothing was unrepairable or dropped.

**Content check:** a word-and-number comparison against `__final.md` showed differences only in section numbers, horizontal rules and the disagreement-list numbering. Every finding, figure, caveat and source is still there, and I added no claims.

**Infographic:** the image agent produced it and it's embedded. Its timeline panel shows "H2–H44 Run and audit bounded loops", which is coarser than the report's schedule; I left the image as it is.
