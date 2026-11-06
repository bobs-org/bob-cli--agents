# Chat History - ace-run (research.2u.cld)

- **TIMESTAMP:** 2026-10-29 17:34:58 EDT
- **MODEL:** claude/opus
- **AGENT:** research.2u.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261029_154356.md`

## Prompt

%id(cld, clan=research.2u)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.2u.cdx`, `research.2u.grk`, `research.2u.mus`, `research.2u.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to improve the way the `bob ref create` command renders tables in PDF files
somehow to make them work better with annotations made in the Highlights app (it can be
hard to highlight cell contents for some reason--I think the Highlights app tries to
select the table cell or something, but I'm not sure) and make them easier to read (or,
at the very least, don't decrease readability).

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I'll start by understanding how `bob ref create` renders PDFs today.

Status: tables appear in 201 of 274 preserved reference sources, so this matters. Next I'll check whether I can reach the Mac to probe PDFKit's selection behavior on table PDFs directly.

Highlights 2026.1.2 is built on PDFKit and also links Vision. I'll check its binary strings for table/area-selection behavior.

Web sources are thin, so I'll measure PDFKit directly. First, checking Bryan's real annotated library PDFs for highlights that land on table cells.

The Chrome-printed table above shows clean multi-line highlights inside one column. Now looking at how the LaTeX route lays out a typical table from Bryan's corpus.

Status: I wrote a Swift PDFKit probe that simulates Highlights' drag and character-index selections on each table cell. Running it on the Mac against the current-pipeline render.

Tables hold 16.5% of the text in annotated LaTeX PDFs but get only 4.9% of annotations (10 of 205), about 3.4× fewer than expected. Inspecting those 10 to see whether they show selection problems.

The app hangs inside PDFView's mouse-down tracking loop: the 240 s watchdog wrote the log. Adding timing instrumentation and a shorter watchdog to see where it blocks.

The mouse events work now, but my scroll positioning put the drag points outside the view. Fixing it by sizing the window to show a whole page at 1:1.

Prose drags come back clean through the real PDFView path, so the harness works. Table cells further down the page still fall outside the view, so I'll print the converted coordinates.

Replacing the Table with a raw block drops pandoc's automatic `longtable`/`booktabs` loading, so I'll load those packages explicitly in the prototype header.

My earlier rewrite of the header file never ran (the whole command was blocked), so the old two-line version was still in use. Rewriting it now.

Now the Chrome-printed variant using bob's reader.css table styles.

The area-of-interest flags don't separate failures from successes, so I'll drop that check. Only 1 of 3 multi-line prose targets was located, which is too few to compare. Checking why.

The stacked prototype reads fine (the italic header labels came out plain, a cosmetic prototype bug). The hanging variant failed on the unescaped `#` in "#now". Fixing the escaping.

The hanging layout reads well (a prototype spacing glitch appears when the label wraps). Testing whether PDFKit still classifies it as a table.

All assets copied (about 500 KB). The failing `du` was a shell alias, not a copy problem. Writing the assets README and then the report.

Report written. Registering it as a durable artifact.

Registration succeeded. Next I'll file the emoji-tofu bug I found as a task bead, after the required duplicate check.

Status: report written and registered. The emoji duplicate check found no match (bob-cli-85 covers web-clip word fragmentation, a different defect), so I'm filing the emoji bug bead now.

Bead filed and marked ready. The Mac is still offline, so its probe scratch files remain. Submitting the final declaration.

I've written and registered the report. The short answer: restyling bob's tables can't fix highlighting. The cause is in macOS 26 itself: Apple's PDF framework, which Highlights is built on, auto-detects tables and blocks normal text selection inside them.

**What's happening.** The framework analyzes each page in the background and spots anything that looks like a grid. After that, a drag inside a table selects the **whole cell** or **nothing** — never a phrase. That cell selection has no usable position data, so Highlights saves an invisible highlight. This matches your "it tries to select the table cell" impression.

**Evidence from your own PDFs:**
- **Your session today:** page 6 of `the_ai_native_sdlc_playbook.pdf` has 5 real highlights on its table and **20 invisible ones** (zero-size boxes), made between 04:59 and 05:30 UTC. The first few attempts worked; after that almost all failed, which fits the analysis finishing in the background.
- **Library-wide:** none of your 205 annotations in LaTeX-rendered PDFs that contain tables land in a table cell, though tables hold about 13% of the text in your chat reports.
- **Mac probe (a small test app on macOS 26.5):**
  - **Grids:** today's style, wider and better-sized columns, row spacing, row rules, a full grid, Chrome's bordered table and a borderless CSS layout were *all* treated as tables.
  - **Workarounds:** neither modifier keys nor the framework's public selection functions get around it.
  - **What works:** only a linear "record" layout (each row becomes a bold lead line followed by its cells) selected normally, 22/22 cells and every phrase. Turning the analysis off also fixed everything, but only Highlights' developer can do that, through a non-public setting.

**Changes to your requirements:**
- **Change the layout, not the style.** Styling only helps readability. Tables you'd annotate need a layout the detector doesn't see as a table; short data tables can stay grids.
- **Measure readability.** On five of your reports, the hybrid below is never longer than today (23→22, 12→10 pages), and better column widths alone save up to 4 pages.
- **Report it upstream too.** bob can't fix tables in PDFs it doesn't render, like arXiv papers. That needs Highlights' developer or Apple.
- **Make it reversible.** Apple may change this behavior, so add a global default, a frontmatter setting and a per-table override.

**Recommended solution:**
- **Table filter:** add one table-layout filter that runs first in the Markdown and note-snapshot routes.
- **Prose tables become records:** any table with a cell of 12+ words outside the first column. That's 68% of your 996 tables and 89% of table text.
- **Data tables stay grids:** with content-based column widths and light row rules. They're still not highlightable on macOS 26, but rarely need it; Highlights' rectangle tool is the stopgap.
- **Report to Highlights and Apple** now; the report has the specifics to send.
- **Web articles** come later as phase 2; I haven't tested that route.

**Housekeeping:**
- **Mac leftovers:** the Mac went offline during cleanup, so a scratch folder under its `/tmp` (`/tmp/tblprobe.*`) and a few probe crash logs (`Cells-*`, `Dump-*`, `TableProbe-*` in `~/Library/Logs/DiagnosticReports`) may remain.
- **Emoji bug:** I filed `bob-cli-e9`. Emoji like 🍅 print as missing boxes in Markdown-rendered PDFs (there's no emoji font fallback), which also breaks any highlight quote that includes them.
- **Assets:** the test-app source, prototype filters and three side-by-side comparison images (current, better grid, records) are in a folder next to the report.

Files are in `sase/repos/research/202610`:
- `ref_create_tables_vs_pdfkit_cell_selection__cld.md` (artifact `file:explicit:2e7b9ec53745754460cf531c`)
- `ref_create_tables_vs_pdfkit_cell_selection__cld_assets/`
