# Chat History - ace-run (research.4r.cld)

- **TIMESTAMP:** 2026-10-17 18:23:35 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4r.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261017_180407.md`

## Prompt

%id(cld, clan=research.4r)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.4r.cdx`, `research.4r.grk`, `research.4r.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

It seems like the `bob ref create` command does convert mermaid syntax well when
converting a markdown file to PDF.

- See the ~/tmp/screenshots/20261017_180121.png screenshot for context.
- I would love to add support if possible.

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

I've found the Markdown → pandoc → XeLaTeX render path. Next I'm reading `create.rs` and the note-snapshot route to see where Mermaid fences could be intercepted.

Still mapping the pipeline: both Markdown routes funnel through pandoc → XeLaTeX, and SVG images already degrade to a placeholder. Now checking which Mermaid renderers exist on this host.

I'm building the native Rust renderer (mmdr) in a scratch target dir so I can compare its output with official Mermaid on the same diagram.

Both engines rendered all five test diagrams. Now I'm comparing them side by side.

Now prototyping the "vendored mermaid.js in Bob's own headless Chrome" option, so I can compare it against `mmdc` and mmdr.

Still checking fonts: Chrome turns CFF/OTF and variable fonts into Type 3, so I'm trying the TTF DejaVu Sans that the Markdown route already uses.

DejaVu Sans TTF embeds properly (CID TrueType, extractable text). Now checking upstream versions: latest mermaid-cli and Mermaid releases.

Mermaid 12.2.0 still ships an IIFE `mermaid.min.js`, but it's 5.5 MB (1.2–1.6 MB compressed). Verifying it renders the same test set.

Sandbox mode isn't the difference. Checking whether Bob's Rust side rewrites TMPDIR before spawning the adapter.

All the evidence is in. Getting exact line numbers for the report's code references, then writing it.

Report written. Registering it as a durable artifact.

The report is written and registered as an artifact (`file:explicit:2c91cf89b5ce1fec7aacc731`). The research repo commit has been declared.

**Diagnosis:** your screenshot comes from the plain-Markdown route (pandoc → XeLaTeX). Pandoc treats a ` ```mermaid ` block as ordinary code, and nothing in bob handles Mermaid. So it's a missing feature, not a regression. Your vault has no Mermaid blocks at all; the demand comes from agent-written research reports.

**Is it a good idea?** Yes. Mermaid in those reports is meant to be a picture: GitHub and Obsidian both draw it, so the author never saw the source. Printed as source in Highlights, it's noise you can't usefully annotate.

**What I tested:**
- **Shelling out to `mmdc` (official Mermaid command-line tool, used by the pandoc-ext/diagram filter):** good output, but a poor long-term design.
  - It isn't installed on the Mac.
  - On athena it failed twice before working: its bundled browser library couldn't find the Chrome version it expected, then Chrome crashed under the long TMPDIR that SASE agents use.
  - It starts a new Chrome for every diagram (about 1.8 s each).
- **mmdr (pure-Rust renderer, no browser):** very fast, but not ready.
  - It laid your screenshot's flowchart out side by side at about 1,870 pt wide. On the page its text would print at about 3 pt.
  - It also drew a sequence diagram wrongly, putting a note inside the wrong frame.
- **Mermaid's own JavaScript, bundled into bob and run in bob's existing headless-Chrome tool (the one web-article capture already uses):** this worked end to end on athena and the Mac.
  - One browser launch rendered six diagrams in 1.6–2.5 s, and a broken diagram failed on its own without stopping the rest.
  - Diagrams come out as sharp vector graphics with selectable text.
  - bob's existing tool already avoids the TMPDIR crash that broke `mmdc`.

**Recommendation:**
- Bundle a fixed Mermaid version (12.2.0) into bob and add a diagram-rendering step to that existing browser tool.
- Render all of a document's diagrams once, then have a small pandoc filter swap each Mermaid block for its PDF in both Markdown routes.
- If anything fails, fall back to today's code block, with a visible note and a warning.

**Requirement changes I'm proposing:** all are listed in §6 of the report.
- Cover vault-note snapshots too, since both routes share the same filters.
- Never fail the import because of a diagram.
- Output vector PDFs, not PNG or SVG.
- Make the output identical on every host: fixed Mermaid version, font and theme. I suggest a grey theme, because Mermaid's default yellow notes clash with yellow highlights.
- No new command-line option in v1, just an environment-variable off switch.
- Keep `--dry-run` from launching a browser.

**Remaining risks:**
- **Wide diagrams print small.** Wide left-to-right flowcharts print at about 5–7 pt against 10 pt body text. They zoom cleanly because they're vector, but are small at 100%.
- **Binary size.** The bundled Mermaid file adds 5.5 MB to bob's 36 MB.
- **Untested in Highlights.** I haven't checked that diagram text can be highlighted there; that needs a manual look on the Mac.

**If you want a stopgap today:** run pandoc-ext/diagram by hand on athena with `mmdc`. It needs a config file pointing at `/opt/google/chrome/chrome` and `TMPDIR=/tmp`.

Report: `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202610/ref_create_mermaid_diagrams__cld.md`
