# Chat History - ace-run (research.5x.cld)

- **TIMESTAMP:** 2026-11-22 16:31:22 EST
- **MODEL:** claude/opus
- **AGENT:** research.5x.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261122_160554.md`

## Prompt

%id(cld, clan=research.5x)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.5x.cdx`, `research.5x.grk`, `research.5x.mus`, `research.5x.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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

Reading the task-requirements epic plan (bob-cli-on) now, then I'll survey the drawer code, capture grammar, and rendering.

Surveying the drawer code in bob-cli: the drawer recognizer, capture grammar, and notebook section targeting.

Still surveying: now the drawer-bullet capture grammar and the notebook `- #Section` logic it should share.

Reading the user-facing capture docs for drawers and notebook sections next.

Checking whether the epic's `^prj` NOTES-home bug is already fixed, then the promotion/demotion casing code.

Inventory done. Now building a visual mock of the proposed drawer rendering before writing the report.

Confirmed in a scratch vault: today a hand-typed `**Future Work**` header is ignored, and capture creates a duplicate `FUTURE WORK` drawer. Checking one more case, then writing the report.

Writing the report now.

I recommend making the change, using the marker you already sketched: a drawer is a bullet whose whole text is one bold span, like `- **Future Work**`, directly under a task. The report is written and registered as `research:202611/drawers_without_all_caps__cld.md`, with a mock image of the proposed rendering.

**Is it a good idea?** Yes. ALL-CAPS makes letter case carry structure, and I reproduced three problems with `bob 0.6.0` in a scratch vault:
- A note like `- AWS` with detail under it silently becomes a drawer.
- `#api-design` creates `API DESIGN`.
- A hand-typed `**Future Work**` header is ignored, so capturing into "Future Work" creates a second, shouting `FUTURE WORK` drawer.

Promotion is also lossy both ways. `API DESIGN` becomes `## Api Design`, and demoting `## C++ Notes` or `## Q1: Goals` is refused outright.

**Tags:** yes, they're ruled out, and the main reason is stronger than marking the task. Tags can't hold spaces or most punctuation, so they can't store "Future Work" at all. They also appear in Obsidian's vault-wide tag list, and `#` already means two things in capture.

**Why bold:** I compared eight markers. Bold is the only one that keeps true case, still reads as a header in plain Markdown, collides with nothing in capture, and maps one-to-one onto `## Title` in a project note. Only 3 task sub-bullets in the vault are entirely bold today, and one (`**ROADMAP**`) was already being used as a drawer.

**Changes I'm proposing to the requirements (each flagged in the report):**
- **Empty drawers stay valid.** 53 of the 109 non-structural `##` sections in your project notes are empty (mostly `## Notes` and `## Future Work`). A round trip only works if an empty `## Notes` maps to an empty `- **Notes**`. Capture still never creates an empty drawer.
- **No re-casing anywhere.** Promotion and demotion copy the title exactly, which is the real lossless step toward converting projects to tasks and back.
- **Imported text must never become a drawer.** Today the Google Calendar importer wraps ALL-CAPS lines in `**…**` to keep them from being drawers. After this change that same wrapping would create drawers, so it has to switch to `__…__`, which looks the same.
- **The `*` → `**|**` typing shortcut fires only where a drawer would be created.** Enter at the end of the title opens the first note inside the drawer.
- **Change all four places where ALL-CAPS means "section".** That's task drawers, project-note capture, new-notebook bodies, and record capture.

**Capture:** I'd reuse the notebook logic by merging the drawer and notebook-section lookup into one resolver, not by copying rules. The two lexers are already near-duplicates. New names keep the capitals you type and title-case the rest, quoted names are kept exactly, and task drawers still prefer the vault's most common spelling. `- #api-design` stays the shortcut, and picking a menu row writes `- **API Design**`.

**Rendering:** In Obsidian a drawer gets a small "drawer front" glyph in the task's colour, with the title in semibold and its true case. A folded drawer shows a note count, and an empty one is dashed. On the Mac the `**` should be dimmed rather than hidden, so the caret never moves invisibly.

**bob-cli-on epic:** nothing in its behaviour conflicts, because a checkbox under a note or under a drawer is never a requirement either way. The conflict is shared files, so the work should start only after phases `.11`, `.12`, `.15` and `.17` land:
- `.12` is rewriting the same promotion code and currently specifies "Title Case" sections.
- `.17` rewrites the Task Drawer glossary entry.
- The epic's open bug about `^prj` notes (repeated `## NOTES` headings) is in the same function and should be fixed once.

I'd send `.12` one instruction now: keep its drawer check and section casing behind one helper each.

**Rollout:** first a release that reads both styles and writes bold, then a reviewed migration of the vault's 7 ALL-CAPS drawers, then removal of the old rule.

**Side findings:**
- The `bob-ledger-tools` drawer regex has a character-range bug: it accepts `NOTE: X` and `KEY:: VALUE`.
- The epic plan's claim that this would be "one change in one place" understates it. The drawer check is copied in four places across the plugins, and the casing logic appears in several more.

I made no memory edits. The report lists the memory decisions a future plan should carry.

Files are in `202611/` of the research repo:
- drawers_without_all_caps__cld.md
- drawers_without_all_caps__cld_assets/drawer_marker_mock.png
