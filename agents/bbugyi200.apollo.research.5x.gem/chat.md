# Chat History - ace-run (research.5x.gem)

- **TIMESTAMP:** 2026-11-22 16:29:57 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.5x.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261122_160554.md`

## Prompt

%id(gem, clan=research.5x)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5x.cdx`, `research.5x.cld`, `research.5x.grk`, `research.5x.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to make it so drawers no longer need to be capitalized.

- You should make sure that this work does not conflict with the (wip) bob-cli-on epic
  bead.
- We will need some other way to mark these sub-bullets as special without marking the
  task in the same way (I think this rules out `#foo` tags, right?).
  - Think hard about the best way to do this.
  - Regardless of what we store on disk, we should make sure to render these drawer
    sub-bullets in a distinct (and easily recognizable) way.
- I think we will need to fix the capture syntax we use for drawers to support this
  change. We already support targeting generic H2 sections when capturing to notebooks,
  so that logic should be re-used if possible/desirable.
- Goals of this Change
  - This change will allow us to represent the true/intended capitalization of the
    section name in drawers.
  - This task is a stepping stone towards the larger goal of giving every project note a
    distinct, lossless task representation (i.e. a way to convert it to/from a task
    without any data loss).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I completed the independent research report and registered it as a durable SASE artifact:

- **Report:** [drawer_casing_and_syntax_redesign__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/drawer_casing_and_syntax_redesign__gem.md)
- **Registered Artifact:** `research:202611/drawer_casing_and_syntax_redesign__gem.md` (`file:explicit:bfee1a02a5fbe212eaaaea6d`)

### Key Conclusions & Recommended Design

1. **Verdict & Timing:** Removing ALL-CAPS for drawers is the right call, and **immediately after `bob-cli-on` closes** is the cheapest moment to do it. A full read-only census of `~/bob` found only **7 ALL-CAPS task drawers** vault-wide (4 open, 1 closed active, 2 in `done/`), right before `bob-cli-on`'s automatic `NOTES` filing multiplies them.
2. **On-Disk Syntax (`- **Title**`):**
   - **Why `#foo` tags are ruled out:** Even though Obsidian Tasks parses tags per-line, any `#tag` on a child bullet still enters Obsidian's note-level `metadataCache.tags`, Tag Pane, Graph View, `tag:` search, and Dataview `file.tags`/`L.tags`, renders as a clickable search pill, and collides with capture's `#` sigils.
   - **Why whole-line bold `- **Title**` wins:** Out of **1,504** direct `#task` note children across `~/bob`, only **1** is an emphasized prose bullet (`0.066%` collision; `0%` with sub-children), it is pure CommonMark, cleanly distinct from emoji-prefixed managed logs and `bob-cli-on` checkboxes, and gets native Obsidian Live Preview `**` caret-reveal for free.
   - **Exact parser rules & safety catches:** Single whole-line `**Title**` span (no split bold, no `***`, no outer whitespace, contains alphanumeric, **no trailing `:`** so Google Calendar's `**Note:**` and prose lead-ins stay plain notes, not reserved). Decouple `is_pomodoro_name` from `is_drawer_title`, expand `reserved_drawer_keys()` to include structural project H2s (`PROJECTS`, `NOTEBOOKS`), and fix `src/native/gcal/description/bullets.rs:140` (which currently wraps ALL-CAPS in `**...**` and would otherwise *create* drawers from imported calendar descriptions!).
3. **Visual Rendering (`bob-ledger-tools` + `bob-mac-capture`):**
   - Mirror `bob-cli-on`'s **attribute-only** CM6 `Decoration.line` + Reading View post-processor pattern (zero DOM widgets, native folding and caret reveal intact).
   - Style drawers as a calm architectural **section-tab pill** (`var(--font-interface)`, **strictly preserved true capitalization**, monochrome `14×14` SVG tray CSS mask, subtle left accent bar, quiet tabular child-count whisper via `--bob-drawer-count`, dashed outline when empty, muted when owner is closed, and subtle child guide rail).
4. **Capture Syntax & Notebook H2 Reuse:**
   - Extract `capture_language/notebook.rs`'s glued `#selector` / `#"..."` parser, exact→slug→ambiguity resolver, and smart-casing creator into a shared module (`section_selector.rs`).
   - Keep drawer-specific policy layered on top: canonical first-level `- **Title**` bullets (mirroring on-disk Markdown without quotes for multi-word names), `- #selector` / `- #"..."` shorthand, vault drawer catalog spelling priority for all-lowercase slugs (`#api-design` → `API Design`), reserved-key refusal, `GRAMMAR_REVISION` 29 → 30, `DRAWER_CATALOG_VERSION` 2 → 3 (seeding real capitalization from the 102 project notes), and case-only retitling in `bob task rename-drawer`.
5. **Four Justified Requirement Adjustments Called Out:**
   - **Refine the `*` typing assist (from `bob.md`):** Bare `- *` breaks `*italic*` bullets (8 in vault) and fights Obsidian's default `autoPairMarkdown: true` (where `**` already yields `**<cursor>**`). Prefer native `**` + **Smart `Enter` inside `- **Title|**`** (hops past `**` and opens an indented child `- |`) + atomic `Backspace` on `- **|**` + optional `- *` + `Space` trigger + Toggle Drawer command.
   - **Clean cutover** via one previewed migration of the 7 drawers rather than permanent dual ALL-CAPS + bold recognition.
   - **Selective reuse** of notebook H2 resolution rather than replacing first-level capture bullets with quoted `- #"..."`.
   - **Honest scoping of lossless project-note ↔ task conversion:** Drawers eliminate section-header loss completely, while an audit of all 102 active project notes identifies 5 remaining gaps for `^task-to-project` (led by generated `### Done & Canceled` / `### Blocked` headings blocking reversal on 62/102 projects).
6. **`bob-cli-on` Non-Conflict & Coordination:** Zero semantic conflict; sequence implementation right after `bob-cli-on.12` and `.17` close, update all byte-identical JS twins (including the `257-task-split-apply.js:203-207` raw-body unwrapping trap), and fix the live `^prj` `note_home` duplicate-`## NOTES` bug together.
