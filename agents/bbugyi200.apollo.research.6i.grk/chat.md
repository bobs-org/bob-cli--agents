# Chat History - ace-run (research.6i.grk)

- **TIMESTAMP:** 2026-11-26 09:38:44 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** research.6i.grk
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_092221.md`

## Prompt

%id(grk, clan=research.6i)
%m:grok/grok-4.6@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher grk in a 5-researcher swarm.
The other researchers, `research.6i.cdx`, `research.6i.cld`, `research.6i.mus`, `research.6i.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__mus.md` and `__gem.md`. Your report will end in `__grk.md`.

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
`__grk` suffix, i.e. `<stem>__grk.md` (double underscore before the
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

I'll start by opening the research repo and reading the skills that govern this report, then investigate the article note type independently.

I'll record skill use, open the research checkout, and pull the memory that governs artifacts, glossary terms, and decisions.

Research checkout is ready. Next I’ll map the article note type, related glossary and decisions, and what’s already in `202611/`.

I’ll pull the article docs, type-detection code, and any decisions that already govern note types.

Task Split looks like the existing promotion path. I’ll read that plus project-from-task, reserved types, and how article children attach.

I’ll read the prior article-format research, sample live article notes, and inspect the plugin’s type gate.

I’ll draft the two diagrams, then write the report under `202611/` with a unique `__grk` filename.

Figures check out. Next I’ll copy them into the research checkout and write the report.

**Rename the file type to `prose`.** Treat prose as one capability at three scales (field, section, note), and ship bob-owned extract/fold before using it for project reversal.

Report: `research:202611/article_type_to_prose_and_section_extract__grk.md`  
Snapshot: `file:explicit:f98af8814fc78c72abdc9d4d`

### Name
`prose` is the right name. I tried `page`, `doc`, `essay`, `writeup`, `note`, `draft`, `zettel`, and keeping `article`. Nothing beat it. It already means “the words, as opposed to layout” in Bob (`never changes prose`, “prose field”). It composes as prose field / prose section / prose note. `article` was a first-use-case name for the blog draft. `doc` collides with the documentation site. Keep web-clip `kind: "article"`; that collision is a reason to rename the vault type.

### Critique
The rename is justified and cheap (one live note, `sase_blog_contents.md`). The product is extract/fold, not the string change.

“Sections implicitly use this type” must mean extract eligibility and heading identity, never running the article formatter on a project. Auto-numbering `## Tasks` neighbors would break the 202610 safety property.

Project reverse currently refuses **any** child file (`Project has N child notes; move them before converting`). Folding derived prose children is necessary and not sufficient: albums, refs, and subprojects still block. Do not inline a product note such as `sase_blog_contents.md` into a restored task.

Notebooks cannot hold this payload (`notebook_shape` stray paragraphs). Note Composer cannot write `type`/`parent` or repair numbered heading links.

### Adjustments
- `[[prose]]` canonical; `[[article]]` and `bob articles` stay forever as aliases (`cli_rules.md`). JSON schema 1 keeps `summary.articles`. Plugin id stays `bob-articles`.
- Extracted notes default `section_numbers: false`; root prose notes stay numbered.
- Derived notes record origin so fold is lossless; root prose reparents.
- Optional `## Prose` owner catalog, same engine as Notebooks/Albums.
- Glossary + decision record (article never got either).

### Ship order
1. Rename with aliases.  
2. `bob prose extract` / `fold` plus a thin keymap (sibling of Task Split).  
3. Conversion uses fold/reparent for prose children only.
