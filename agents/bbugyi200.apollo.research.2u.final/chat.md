# Chat History - ace-run (research.2u.final)

- **TIMESTAMP:** 2026-10-29 18:53:39 EDT
- **MODEL:** claude/opus
- **AGENT:** research.2u.final
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261029_154356.md`

## Prompt

%clan(research.2u, tribe=research, summary=[[[bold]RESEARCH PROMPT:[/bold] I would like to improve the way the `bob ref create` command renders tables in PDF files
somehow to make them work better with annotations made in the Highlights app (it can be
hard to highlight cell contents for some reason--I think the Highlights app tries to
select the table cell or something, but I'm not sure) and make them easier to read (or,
at the very least, don't decrease readability).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.]]) %id:research.2u.final %m:@xlarge
%wait:research.2u.cdx %wait:research.2u.cld %wait:research.2u.grk %wait:research.2u.mus %wait:research.2u.gem %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are the lead researcher: 5 independent researchers have reported on the request
below, and you will add your own research and merge every perspective into one
consolidated report.

SASE derives your plan's links from the artifacts you read this turn; use
`sase artifact read` for context you actually used.

Research request:

I would like to improve the way the `bob ref create` command renders tables in PDF files
somehow to make them work better with annotations made in the Highlights app (it can be
hard to highlight cell contents for some reason--I think the Highlights app tries to
select the table cell or something, but I'm not sure) and make them easier to read (or,
at the very least, don't decrease readability).

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
   dispatch's `research.2u.cdx`, `research.2u.cld`, `research.2u.grk`, `research.2u.mus`, `research.2u.gem` dependencies, matching by `wait_name` and the canonical research
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
   agent `research.2u.linker` publishes it from your report.

5. After the write succeeds, register the consolidated report as a durable snapshot so
   the linker agent, `research.2u.linker`, can find it:

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

Now let me read the five reports through their canonical references.

I've read all five reports and am now checking the strongest claim (cld's zero-geometry highlights in your real PDF) against the vault copy here.

Still investigating: the Mac has CoreGraphics feature flags named `ModernSelection` and `LayoutWithCTLD` that may govern table-cell selection. One more check, then I'll move on to writing the report.

The Mac has gone offline (lid likely closed), so that lead stays unverified. Moving on to cross-checking the cited Apple threads and the bob-cli source claims.

Counting how many of your web-clip PDFs carry tables (my first pass's pattern missed them; fixing it now).

The decision-figure SVG renders cleanly (96% fit); the PNG export keeps hitting a browser connection error, so I'm trying another way to view it before writing the report.

Following the repo's precedent: moving each report (and the cld assets folder plus the cdx zip, under their original names) into a new `ref_create_table_layout_for_highlights/` directory.

Corpus checks done: about 1,000 tables in chat reports versus roughly 9 in 6 web-clip PDFs. Your observed failure, though, was on a web-clip table. Writing the consolidated report now.

The consolidated report is written and the layout is in place. Registering it as a durable artifact now.

A matching bug bead (`bob-cli-e9`) already exists, filed by cld. Before adding a +1, I'm measuring how widespread the problem is across your chat PDFs as independent evidence.

No in-progress epic is causally linked to the emoji bug, so the +1 is enough. Wrapping up with the final declaration.

The research is finished. On macOS 26 a table can't be both a visual grid and easy to highlight, so I recommend printing prose-heavy tables as single-column "row records" and keeping grids only for short-cell data tables.

**What's going on.** Your guess was close. The thing grabbing the cell is Apple's PDFKit, which Highlights is built on, not Highlights itself. PDFKit scans each page in the background and recognizes tables by how they look. After that, a drag inside a table selects the whole cell with no position data, or selects nothing.
- **It's in your own PDF.** Page 6 of `the_ai_native_sdlc_playbook.pdf` has 5 real table highlights from 04:51–04:57 UTC. The next 20 attempts (04:59–05:30) were saved as invisible annotations with all-zero positions. The early ones worked because the background scan hadn't finished yet.
- **Restyling can't fix it.** cld (one of the five researchers) tested on your Mac: booktabs, better widths, extra row spacing, row rules, a full grid, Chrome's bordered tagged table, and a table with no table tags. PDFKit detected every one. Only the row-record layout got normal selection back (22 of 22 cells).
- **No off-switch.** macOS 26.5's public PDFKit has no setting to turn this off; the switch exists only in Apple's private code. Apple forum threads report the same problem in Preview (119 and 463 votes) with no Apple response. Highlights probably can't offer a supported toggle, so Apple is the real fix for PDFs bob doesn't make.

**Critique of the plan.** It's worth doing. About 73% of your chat reports contain tables, and you've effectively never managed to annotate one. But "render tables better" is the wrong goal: the fix is to stop drawing prose as a grid. I disagreed with the researchers who wanted an opt-in marker, because agents write these reports and you'd never hand-mark tables. I also disagreed with flattening every table: pure data tables are 13% of tables and only 3% of table text.

**Requirement changes, called out in the report:**
- **Success test:** you can highlight a phrase inside a former cell and it imports correctly.
- **No promise for grids:** data tables stay hard to highlight on macOS 26. Use the rectangle tool or a per-table override.
- **Readability measured per document:** comparison tables you scan side by side lose that when they become records. That's the one real trade-off. On five real reports cld measured no added pages (15→15, 11→11, 12→10, 4→4, 23→22), because better grid widths elsewhere win the space back.
- **New PDFs only:** never re-render annotated PDFs automatically.
- **Lost feature:** Highlights' table-to-CSV export won't work on records. Do you ever use it? If so, that changes how easy the override should be.

**Recommended solution:**
- **The pass:** one shared table-layout step, run first in both Markdown render paths.
- **Records:** a table with a cell of 12 or more words outside the first column prints as records: a bold lead-in per row, then `Header: value` lines. Links, inline code, captions and numbering are preserved. At 12 words that's 68% of tables and 89% of table text, and the threshold is adjustable.
- **Grids:** all other tables keep a grid with smarter column widths and more row spacing.
- **Overrides:** a config default, a frontmatter key, and a per-table class. No new command-line flag.
- **Web clips** (phase 2): the same rule, applied only to the printed page. Your failure today was on a web clip, though they hold only about 1% of your tables.
- **Upstream:** report the PDFKit behavior to the Highlights developer and to Apple.

**Limits:**
- The Mac went offline partway through, so I couldn't check whether two system feature flags (`ModernSelection`, `LayoutWithCTLD`) control this. Changing them wouldn't be a supported workaround anyway.
- Nobody has yet tested records in a Chrome-printed (web-clip) PDF. That check is part of phase 2.
- The report's diagram rendered, but the image preview failed in this environment, so I checked its labels and size rather than looking at it.

**Bead:** cld had already filed `bob-cli-e9` for emoji printing as blank boxes in chat PDFs. I added a +1 showing 193 of 498 chat PDFs (39%) have those glyphs in their text.

The final report is registered as `research:202610/ref_create_table_layout_for_highlights/ref_create_table_layout_for_highlights__final.md`. The five researcher reports and their assets were moved into that folder, and the research-repo commit is declared to run when this turn ends.

Files are in `202610/ref_create_table_layout_for_highlights/`:
- ref_create_table_layout_for_highlights__final.md
- ref_create_table_layout_for_highlights__final_assets/
