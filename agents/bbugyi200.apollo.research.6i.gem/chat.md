# Chat History - ace-run (research.6i.gem)

- **TIMESTAMP:** 2026-11-26 09:44:19 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6i.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_092221.md`

## Prompt

%id(gem, clan=research.6i)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6i.cdx`, `research.6i.cld`, `research.6i.grk`, `research.6i.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to rename the "article" Obsidian note file type to something more generic,
since I intend to use this type for any file that needs to contain prose.

- I was thinking of the name "prose" for this, but I'm not sure.
- You should think hard about other names and attempt to come up with a better one.
- The goal is to soon allow for sections ("prose sections"?) to implicitly use this type
  as well, which will allow us to use a keymap to convert that section into a full-blown
  "prose" note (or whatever we decide to call these).
- This functionality will be useful on its own, but will also be required in order to
  eventually make tasks and projects losslessly (or with minimal loss) reversible (since
  projects can have article notes as children).

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

I completed independent research across `bob-cli`, `bob-plugins`, `bob-mac-capture`, governing SASE decisions, and `~/bob`, and wrote the full report to [rename_article_type_and_prose_sections__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/rename_article_type_and_prose_sections__gem.md).

**Registered Artifact Snapshot**
- **ID / Ref:** `explicit:304ecc630f54d2b3b13f2d96` (`file:explicit:304ecc630f54d2b3b13f2d96`)
- **Label:** `research:202611/rename_article_type_and_prose_sections__gem.md`
- **Stored Path:** [rename_article_type_and_prose_sections__gem-df9dbb4dc076.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261126092226/rename_article_type_and_prose_sections__gem-df9dbb4dc076.md)

### Key Takeaways

- **Naming (`prose` wins; `page` is the strongest countable runner-up):** `~/bob` currently has only **1** `[[article]]` note (`sase_blog_contents.md`) versus 39 `[[notebook]]` and 213 `[[record]]` notes, and `"article"` collides with `bob ref` / `bob-mac-capture` web articles and `~/bob/articles.md`. Common countable candidates fail vault/CLI collision checks (`doc` collides with `~/bob/docs.md`, `lib/docs/`, and Bob Refs' `Doc` kind; `text`/`body`/`paper`/`sheet`/`leaf`/`draft` all collide). **`prose`** (`type: "[[prose]]"`, `bob prose` with permanent hidden `bob articles` alias, `prose.base`, `## Prose`, **Prose Note** / **prose section**) has zero user-facing collisions, matches Bob's `mail` mass-noun precedent and Glossary `<X> Note` pattern, and cleanly completes Bob's task-free content triad (`notebook` = bullets, `record`/`album` = schema fields, `prose` = continuous written prose).
- **Six justified requirement adjustments:**
  1. **Flip `section_numbers` default from `true` → `false`** (opt-in `section_numbers: true` + `Toggle section numbers` command) so casual prose notes and extracted sections don't get surprise `1.` / `1.1` numbering on save.
  2. **Keep "implicit prose sections" scoped to content-based classification, extraction, and reversal — not in-place auto-formatting inside live project notes.**
  3. **Make section conversion bidirectional (`bob prose extract` + `bob prose inline`) and own the engine in Rust**, keeping Obsidian (`Ctrl+Shift+E` bidirectional keymap) as a thin preview/trigger shell.
  4. **Add a generated `## Prose` (`> [!prose]`) host catalog** via `src/native/host_catalog` (matching `## Projects`, `## Notebooks`, `## Albums`) and register `prose` in `note_catalog` and the `<ctrl+=>` child note picker.
  5. **Bridge prose across Task ↔ Project via standalone prose notes:** task bullets cannot safely hold inline prose or act as YAML `parent:` targets, so Project → Task demotion auto-extracts inline prose sections and reparents child prose notes to the grandparent while linking them under `- **Notes**`; Task → Project promotion offers explicit opt-in adoption of linked direct-sibling prose notes.
  6. **Fix existing non-prose reversal blockers** uncovered in `bob-navigation-hotkeys`: `splitProjectNoteForReversal` currently fails on status-grouped `## Tasks` (`### Blocked`, `### Next & In Progress`, `### Done & Canceled`, chip bars) and only skips `> [!projects]` (not `> [!notebooks]`/`> [!albums]`), alongside req/subtask asymmetry and non-prose child notes.
