# Chat History - ace-run (research.v.linker)

- **TIMESTAMP:** 2026-09-30 19:06:12 EDT
- **MODEL:** claude/opus
- **AGENT:** research.v.linker
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260930_181054.md`

## Prompt

%id(linker, clan=research.v) %m:@xlarge
%wait:research.v.final %wait:research.v.image %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the linker agent for a research swarm. The lead researcher,
`research.v.final`, has written a consolidated report on the request below. Your job
is to publish that report as the canonical `<name>.md`: the file readers open, and the
one SASE renders into a Highlights PDF. You are an editor, not a researcher. The new
file must carry exactly the lead's meaning and intent. Do not do research of your own:
add no new claims or sources, settle no open questions, and neither soften nor
strengthen the conclusions or the recommendation. If the lead seems wrong, leave it as
written.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request (context only; do not research it):

I'm
currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for context),
but there is still one major requirement that is unmet.

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).

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
   with `wait_name` `research.v.final` whose label has the form
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

Publishing the lead's freshness report as the canonical file. I've read the final report through `sase artifact read`. Next I'll check its external links and the infographic.

The infographic is confirmed and all 10 external URLs return 200. Next I'll write the restructured report.

Now I'll check anchors with pandoc and compare the new file against the lead's report.

Only the hand-written section numbers and re-punctuated bold labels differ. Next I'll check that every line of the lead's text is still present.

Registration succeeded. Now the final declaration.

I've published the lead's report as `202609/ready_task_freshness_review/ready_task_freshness_review.md` and registered it as `file:explicit:de1637c0d03b01e6d94273ea` with the label `research:202609/ready_task_freshness_review/ready_task_freshness_review.md`. The host will commit it to the research repo after this turn ends. The `__final.md` file and the drafts are untouched.

**What changed in structure**
- **Opening:** the bottom line comes right after the title, followed by the infographic. It is embedded once with descriptive alt text, and I confirmed the file exists beside the report.
- **Section order:** Is this a good idea (what is right, what it doesn't solve, the daily load) → What was verified (V1–V12) → Adjusted requirements → Recommended design (nine subsections, from the glossary definition to where the code lives) → Where the researchers disagreed → Rejected alternatives → Risks → Open questions for Bryan → Recommended solution → About this report → Sources.
- **Recommended solution:** it stays as the last analysis section, because the original request asked to end with it.
- **Headings:** the hand-written numbers are gone. Headings with punctuation were renamed so they can be link targets; for example, "The load, honestly" became "The daily load". The lead's parenthetical wording moved into each section's first line.
- **The lead's header block:** the date, lead researcher, context and question moved to "About this report", because the bottom line now opens the report.
- **Links:** every `§5.x` / `§6` reference and the one "(below)" became anchor links. I also added a few sparing links from bottom-line and recommended-solution points to the sections that back them.

**Checks**
- **Content:** a word-level comparison against `__final.md` shows no content lost. The only removals are section numbers, "(consolidated)" from the title (the About section still says the report consolidates five swarm reports), and the words of renamed headings.
- **Carried-over items:** all code spans, tables (74 + 8 rows), numbers and URLs are present.
- **Anchors:** `pandoc -t html` shows all 14 internal link targets exist and every heading ID is unique.
- **External URLs:** all 10 returned 200. None were unverified or unrepairable, and none needed repair.
- **Relative links:** the only one is the infographic, and it resolves.
- **Frontmatter:** the lead's report has none, so there was no `updated_time` to update.
