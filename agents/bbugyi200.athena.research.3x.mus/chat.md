# Chat History - ace-run (research.3x.mus)

- **TIMESTAMP:** 2026-10-07 10:15:09 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.3x.mus
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261007_100736.md`

## Prompt

%id(mus, clan=research.3x)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.3x.cdx`, `research.3x.cld`, `research.3x.grk`, `research.3x.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

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
would like to improve the way that the `bob ref create` command renders PDFs from
markdown files.

- Namely, I would like to add support for backlinks that make it very easy for the user
  reading the PDF to use local links to jump to a part of a document and then jump back
  to where they were originally.
- I think we can accomplish this by searching for any local links in the markdown,
  figuring out which part of the document they link to, adding a unique alphanumeric ID
  to the rendered local link text, and then adding a new local link at the original
  link's target destination that uses that same alphanumeric ID as rendered link text
  but links back to the original link.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research complete and registered.

Report: `sase/repos/research/202610/pdf_backlinks__mus.md` (snapshot id `explicit:190190aef4e6204ef73035ea`).

Key findings:

- The idea is worth building with adjustments. Pandoc already renders every `#anchor` link as a working forward jump (`\hyperref`, verified live with pandoc 3.1.11.1) — only the way back is missing, which matters most in annotation readers like Highlights that lack history-back.
- I verified with a working prototype Lua filter that true position-accurate return is achievable AST-only: wrapping each outbound link in an identified `Span` emits `\phantomsection\label{…}` (a real return anchor) with no LaTeX preamble changes.
- Main critique: raw alphanumeric IDs in body text should not ship — use small superscript `↩n` markers in link color plus a capped, right-aligned return cluster at the destination. Also required: anchor creation at the link site (the proposal assumes it), trailing rather than heading-adjacent placement, a dangling-target policy (warn, no marker), and exclusions for TOC/headings/listen cards.
- Recommended solution: ~60 lines of Lua in the existing `PANDOC_CODE_BREAK_FILTER`, no CLI or preamble changes, with `--to=latex` assertion tests in the current style plus a real-PDF spot check including the lopdf stamp round-trip.

Declaration submitted — research report commit authorized.
