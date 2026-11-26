# Chat History - ace-run (research.6i.cld)

- **TIMESTAMP:** 2026-11-26 09:34:21 EST
- **MODEL:** claude/opus
- **AGENT:** research.6i.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_092221.md`

## Prompt

%id(cld, clan=research.6i)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6i.cdx`, `research.6i.grk`, `research.6i.mus`, `research.6i.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
`__cld` suffix, i.e. `<stem>__cld.md` (double underscore before the
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

Status: research is done. I'm collecting exact line references, then writing the report.

I recommend renaming the type to **`prose`** now. But the rename alone won't make projects reversible. That needs a rule for how projects and tasks hold prose notes, which the report lays out.

The report is at `202611/prose_note_type_rename_and_sections__cld.md` in the research repo and is registered as `research:202611/prose_note_type_rename_and_sections__cld.md`.

**Why rename now**
- **Cheap:** the vault has exactly one real article note (`sase_blog_contents.md`), plus one template, one `.base` file and the type note. No hotkeys use the article plugin's commands.
- **Wrong word:** "article" already means web articles elsewhere in Bob. There's a `bob ref create` web-article capture, an `articles.md` reference collection in the vault root, and about 200 web-article uses in bob-cli's highlights code.

**Why `prose`**
- **Both roles:** of about 20 names I compared, it's the only one that works as a note type (`type: "[[prose]]"`, `bob prose`) and as the adjective your section idea needs ("prose section").
- **Clean contrast:** it pairs naturally with `notebook`, which holds only bullets.
- **Runner-up `doc`:** reads badly as "doc section", and the vault already has a `docs.md`.
- **Rules for "prose":** always write "prose note" or "prose section", never "a prose". Add glossary entries so the type isn't confused with the everyday use of "prose" (free text) in the docs.

**Changes I'd make to your requirements**
1. **Definition:** define the type by who owns the body, not by "contains prose". Area, project, ref and record notes all contain prose. A prose note is one whose body you own: bob only formats it, and it holds no tasks or anchors. The current refusals already enforce this.
2. **Prose sections:** a prose section should be something you can extract, not something bob formats in place. Formatting stays whole-note only, as it is today. Whether a `##` section counts as prose is worked out from its content and never stored. One gesture extracts it into a prose note and leaves `## Title` + `![[note]]` behind; the reverse gesture inlines it back. Extracting and then inlining an unedited note must give back the original section byte for byte.
3. **Reversal blockers:** the rename doesn't fix them. Reversing a project into a task currently refuses in three cases: the project has child notes, a section contains anything other than list items, or there's text outside the sections.
   - My fix: prose never moves into a task. Tasks and projects embed prose notes, and conversion moves the embed and updates the note's `parent:`.
   - Result: task → project → task loses nothing. Project → task → project only turns an inline prose section into an embedded note with identical text.
4. **Wider than prose:** the child-note refusal also fires for notebooks, albums and sub-projects. Do prose first, but build the rule so notebooks can reuse it.
5. **Old names:** keep `[[article]]` and `bob articles` as permanent aliases. Your CLI rules require the second. Keep JSON keys, refusal codes and the plugin id unchanged, and change only the wording users see.

**Rollout order** (because bob-cli ships through the daily release train):
1. bob-cli accepts both type names and adds `bob prose`.
2. The plugin gets renamed labels and accepts both types. It can keep calling `bob articles` safely.
3. The vault switches to `[[prose]]` once all three machines run the new bob.

If you want something today with no code, Obsidian's built-in Note Composer can extract a selection into a new note. Point its template at one with `parent: "[[{{fromTitle}}]]"` and `type: "[[prose]]"`, and set it to embed after extracting.

**Open questions for you**
- Should section numbering stay on by default? I lean yes.
- Should text above a project's first section be extracted as `## Overview`, or keep being refused?
- Should the extract/inline gesture reuse the existing task↔project conversion hotkey depending on where the cursor is, or get its own keys?
