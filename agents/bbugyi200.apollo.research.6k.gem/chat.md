# Chat History - ace-run (research.6k.gem)

- **TIMESTAMP:** 2026-11-26 11:39:33 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6k.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_111415.md`

## Prompt

%id(gem, clan=research.6k)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6k.cdx`, `research.6k.cld`, `research.6k.grk`, `research.6k.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering property cards at the top of prose (fka article) notes
and notebooks.

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi and
  bob-cli-qj epic beads.
- These property cards should act like other property cards (e.g. the native Obsidian
  "Properties" should be hidden in these note files).
- Prose notes and notebooks do not currently support many custom frontmatter properties
  (just a summary?), but we should include rich, useful data related to the prose note /
  notebook in these cards. Think hard about what data would be most useful for us to
  show on these cards.
- As a part of this change, we should add excellent new glossary terms for "prose card"
  and "notebook card".
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

Research complete. The full design, critique, parallel execution plan, and draft glossary strands have been written and registered as a durable SASE artifact.

### Report & Artifact
- **Report:** [prose_and_notebook_property_cards__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/prose_and_notebook_property_cards__gem.md)
- **Registered Artifact:** `explicit:e5208330f81462870811d8ee` (`research:202611/prose_and_notebook_property_cards__gem.md`)
- **Mermaid Diagrams Verified (`mmdc` v12.0.0):** Figure 1 (passive-rendering & ownership flow, 87.8% PDF fit) and Figure 2 (parallel execution with `bob-cli-qi` & `bob-cli-qj`, 84.1% PDF fit), both visually inspected with zero crossings or overlaps.

### Headline Verdict & Critique
- **Strong yes for Notebook Card immediately:** Auditing all 39 live notebooks in `~/bob` shows **25/39 (64%)** carry 7 Zorg-importer derived frontmatter keys, **39/39** have a matching H1 + `parent` + `summary`, and `bob-ledger-tools` currently mounts a separate `.bob-notebook-header` underneath the H1. Replacing both with one `spine`-tile (`notebook-tabs`) **Notebook Card** cleans up the top of nearly two-thirds of notebooks while adding `@stem` one-click capture-route copy, child-notebook chips, and clickable `##` section jump chips.
- **Qualified yes for Prose Card — kept editorial and folded by default:** Only 1 live note (`sase_blog_contents.md`) uses `[[article]]` today, but `bob-cli-qj` + `qj.5` (`bob prose extract`) will multiply prose notes with provenance metadata. Using a quiet `folio`-tile (`feather`) card with 3% area wash (0% when unparented), hiding **`.inline-title` ONLY** (never body H1s, which prose notes may use as depth-1 sections), and folding `Outline ▸` by default preserves `.bob-article`'s `40rem` editorial reading feel while surfacing word count, reading time, section/stub counts, backlinks, clickable findings, `§ numbered` / `§ off` toggle, and a scrollable interactive mini-TOC on `_`.

### Key Adjustments Called Out in the Report (A1–A7)
1. **Zero `bob-cli` Rust changes in v1 (`A1`):** Gate both cards on `props_v1` (already returned by `bob props show` for both notebooks and prose notes, matching Album/Record/Day/Period/Bank) and keep `==` unregistered to preserve Vim reindent (`+`, `-`, `_`, and direct controls handle everything).
2. **Host both cards in `bob-ledger-tools` (`A2`):** Keeps all Property Card Kit internals unexported, delivers 0 ms local-first paint even if `bob-articles` is off, and pairs with a ~25-line read-only `bob-articles.api.prose` seam for zero extra `bob` subprocesses.
3. **Supersede `.bob-notebook-header` on desktop title-slot scopes (`A3`)** to avoid duplicate breadcrumbs/chips (keeping it only as mobile/embed/fail-open fallback), and **fix the `298z` missing-key routing gap** so `+ Add summary` works cleanly on `props_v1`-only notes lacking `summary:`.
4. **Prose Card `.inline-title`-only ownership & folded default (`A4`)** plus **silent missing `created` (`240m`) & content-gated sparse fields (`A5`)** (72% of live notebooks omit `created:` and 97% lack `last_note`).
5. **Staged parallelism bypassing `bob-cli-qj.5` (`A6`):** ~80% (`P1` kit/models, `P2` Notebook Card, `P3` local-first Prose Card with dual `[[prose]]`/`[[article]]` detection in new `249g*`/`249h*` fragments) starts immediately without touching `~/bob` or running `bob plugins sync`. Only `P4` (25-line `bob-articles` bridge) waits on `bob-cli-qj.4`, and `P5` (takeover/passive E2E, docs, glossary strands, serialized `bob plugins sync`) waits on `bob-cli-qi.6` and `bob-cli-qj.4` — explicitly bypassing `qj.5`.
6. **Glossary updates (`A7`):** Drafted full `glossary:notebook-card` and `glossary:prose-card` strands plus the required coordinated update to `glossary:property-card` to land via `/sase_memory_write` in `P5`.
