# Chat History - ace-run (research.4m.cld)

- **TIMESTAMP:** 2026-10-15 18:10:57 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4m.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_174319.md`

## Prompt

%id(cld, clan=research.4m)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.4m.cdx`, `research.4m.grk`, `research.4m.mus`, `research.4m.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to add much better support to the `bob ref create` command for creating
beautiful PDF files from area notes / project notes. See the
~/bob/lib/chat/sase_blog_v1.pdf file (this PDF file might not be available on this
machine, but should be available on my macbook) for an example of how these look now
(not great).

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

Reading the current `bob ref create` Markdown→PDF pipeline before forming a view.

Found the example PDF on athena; looking at how it currently renders.

Checking existing beads and prior research for related work.

Comparing against bob's existing HTML/Chrome web-clip template, which already looks much better.

Checking whether Highlights annotations from Chrome-rendered PDFs come back clean (key engine evidence).

Reading vault conventions memory and the relevant glossary terms.

Now prototyping: I'll build a quick Obsidian→clean-Markdown projection of `sase_blog.md` and render it through several engines to compare.

Bob already has task scanning, inline-field, and wikilink resolvers I can reuse. Checking `clean_description`.

Writing the projection prototype (Python, in a scratch dir) to normalize Obsidian/Bob syntax into clean pandoc Markdown.

Projection output looks clean. Now writing the render variants: improved xelatex note template, Typst, and HTML→Chrome.

Fixing Chrome's socket-path issue (long TMPDIR) and re-running the Typst and Chrome variants.

Found a bug in my spike filter (`table.unpack` truncation) and Typst label handling; fixing.

All five variants render. Rendering page images to compare visually.

Both C (xelatex) and D (Typst) look good. Now the decisive test: PDFKit text extraction on the Mac (Highlights uses PDFKit).

Kerning-off doesn't fix Chrome's fragmentation. Checking a few remaining facts (Obsidian plugins, font sizes, sase.md blocked composition).

Confirmed the current justified/hyphenated layout leaks splits like `correc-`/`tion` into real Highlights quotes. Testing generality on an area note and the huge `sase.md`.

Two instructive failures: `@BANK` (a capture route) became a pandoc citation, and raw TeX inside `\href` broke. Testing whether a CommonMark reader avoids these issues.

Projection alone (A1) already fixes most readability problems. Building a side-by-side comparison image for the report.

Confirmed a real trap: xelatex hard-fails on a struck-through link, and 20 of 101 area/project notes use `~~[[sub_project]]~~` syntax. Checking existing Rust dependencies.

I have enough evidence. Checking the output filename is free, then writing the report.

Writing the report now.

Verifying a couple of counts cited in the report.

Report written. Registering it as an artifact.

Artifact registered. Now filing the discovered web-clip PDFKit issue via the new-task skill.

No duplicate and no causally related epic found. Creating the bug bead.

Updating the report to cite the bead ID, then finalizing.

I wrote the report and registered it as an artifact. My recommendation: write a Rust step that rewrites the note into a clean, readable version before rendering, and keep pandoc + xelatex as the PDF engine with a new layout for notes.

**Report:** `sase/repos/research/202610/obsidian_note_pdf_snapshots__cld.md` (label `research:202610/obsidian_note_pdf_snapshots__cld.md`). It comes with figures and the throwaway test scripts.

**Why `sase_blog_v1.pdf` looks bad:** the problem is mostly what goes into the PDF, not the typesetting. `bob ref create` hands the note to pandoc as if it were plain Markdown, so all the Obsidian and Bob markup prints literally:
- wikilinks, image embeds, `[created:: …]` fields, `^ids`, `#task`, and the `[/] [?] [-]` statuses;
- emoji as empty boxes, the title as `sase_blog`, and sections numbered `0.1`;
- the "Requirements" heading is lost: it gets glued onto the line above it and is missing from the contents.

When I rewrote the note first (Python prototype), the same engine gave a clean document. The report has the before/after pages side by side.

**Engine findings:** I tested the rewritten note through xelatex, Typst and Chrome. On the MacBook I read each PDF back through PDFKit, which is what Highlights uses to pull quotes, and counted words that came back split:

| PDF | Split words |
| --- | --- |
| xelatex, new layout | 0% |
| Typst | 0% |
| Chrome, my test layout | 2.5% |
| Your real web clips from bob's Chrome template | 6.4% |

Your existing Highlights quotes from web clips show the same damage (`decisionsFor example`, `git pushor`). Turning kerning off in Chrome didn't help. So Chrome is out for anything you annotate. Typst is the runner-up: it looked as good and rendered in about 0.4 s versus 8 s. But it would be a second engine without the return-link pills you already have, and athena's pandoc 3.1.11 corrupted text when converting to it.

**Problems the implementation must handle:**
- **Struck-through links crash xelatex.** 20 of your 101 area/project notes use `~~[[sub_project]]~~ ✅` (61 times). Today that prints as raw text; once those become real links, every one of those renders would fail.
- **`@BANK` becomes a pandoc citation and `$` amounts can be read as math.** Switching pandoc to its CommonMark reader avoids both.
- **Justified, hyphenated text leaks into quotes.** 6 of your 395 existing quotes from research PDFs are split at a hyphen (`correc-`/`tion`). Today's layout does this for all Markdown refs, not just notes.

**Changes to your requirements that I'd make:**
- **Scope:** handle Obsidian markup for any vault note; add the task, log and header treatment only for area and project notes.
- **Content:** by default show open work and prose, leave out closed tasks (shown as a count), and shrink schedule and work logs. In `sase.md`, 211 of 214 Blocked tasks are only waiting on a future date.
- **Snapshots:** date-stamped names like `sase_blog_261015`, a `source_note` field on the ref note, a new `notes` ref type, and `-P` defaulting to the note itself.
- **No automation:** a new snapshot never closes an older one; it only prints a hint.

**Recommendation:** a Rust step inside `bob ref create` that detects area and project notes and rewrites them, reusing bob's existing task, field and link parsers. Render the result through a new xelatex layout for notes:
- bundled fonts and glyph fallback;
- status glyphs and a header block;
- no section numbers;
- left-aligned text without hyphenation.

Accept it only when all 101 notes render on both athena and the Mac, plus one real round trip in Highlights.

**Your decisions:**
- What a snapshot is for: reviewing the plan or triaging tasks. My defaults assume plan review.
- Ref type: a new `notes` folder or `chat`.
- Naming: date stems or `_vN` like your `sase_blog_v1`.
- Links: should wikilinks open Obsidian, and should ref tasks open the PDF in Highlights?
- Engine: xelatex now with Typst kept as a fallback, or a planned move of all Markdown refs to Typst.

I filed the web-clip split-word problem as bug bead **bob-cli-85** (marked ready). The report and its figures and scripts are declared for commit in the research repo; the host commits them after this turn.
