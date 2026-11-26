# Chat History - ace-run (research.6k.cld)

- **TIMESTAMP:** 2026-11-26 11:34:58 EST
- **MODEL:** claude/opus
- **AGENT:** research.6k.cld
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261126_111415.md`

## Prompt

%id(cld, clan=research.6k)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.6k.cdx`, `research.6k.grk`, `research.6k.mus`, `research.6k.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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

Status: reading the decisions roster and glossary is done. Next I'm opening the bob-plugins repo to study the card kit, and looking at how bob-cli handles props for notebooks and prose notes.

Status: found that notebooks already get a "notebook header" from bob-ledger-tools. Reading how it works now, since a notebook card would replace it.

Status: studying the card kit's species and tile system so I can design new Notebook and Prose species that fit in. Next: the area/project home-card host, then the prose engine data.

Now the home-card host and model (area/project), which is the most recent and closest analog.

Status: no existing beads cover these cards (the notebook header came from bob-cli-j8.6). Checking how the shared notebook report refreshes, then I'll start writing.

Status: I have enough evidence. Loading the Mermaid skill for the sequencing figure, then I'll write the report.

Status: research is done. Now drafting the sequencing figure, which shows which card phases wait on which qi/qj phases, and rendering it to check it fits.

Status: first render was too tall (65% fit) with tangled edges. Trimming it to the four gating phases and re-rendering.

Status: the figure now fits at 81% and reads cleanly. Checking the research repo layout, then writing the report.

Status: figure is done. Pulling the full outline of the live prose note so the card mockup uses real data.

Status: all evidence gathered. Writing the report now.

The report is written and registered. Finishing the turn through `/sase_final`.

I've written the report on cards for prose notes and notebooks and registered it as `research:202611/prose_and_notebook_cards__cld.md`. My recommendation is one new epic with four phases. Only the notebook card can start now; the rest wait on single phases of bob-cli-qi or bob-cli-qj.

**Is it a good idea?** Yes for notebooks, and yes but kept small for prose notes.
- **Notebooks benefit right away.** There are 39 in the vault. 25 carry seven leftover zorg migration keys each, which fill the native Properties block, and 28 have no `created` date. Notebooks also already have a separate "linked notebook header" (crumbs plus child-notebook chips) that the new card should replace, not sit beside.
- **Prose notes have only one example today** (`sase_blog_contents.md`). The card pays off later, once prose-section extraction (bob-cli-qj.5) starts creating many prose notes. It should look like a quiet title page, not a dashboard on top of an essay.

**Is coordination needed?** Very little. Neither card needs bob-cli code changes or a new JSON contract: both read reports that already exist (`bob notebooks list`, which the plugin already uses, and `bob articles list`, which takes about 0.1s). There are four ordering points, each one bead dependency:
1. The prose card's call to `bob prose` waits for bob-cli-qj.4's check that every machine runs the new bob.
2. Real-Obsidian acceptance waits until bob-cli-qi.4 passes, so two agents aren't editing the same test harness.
3. Glossary edits wait for bob-cli-qi.6, which is already editing the Property Card term.
4. Glossary edits also wait for bob-cli-qj.4, which creates the Prose Note term the new terms link to.

The report includes a diagram of this. Merge conflicts on the shared plugin files are mechanical: rebuild after rebasing, never hand-merge.

**Requirement changes I'm calling out:**
- The notebook card replaces the existing notebook header. Two things owning one note's top is how the bank-card problems started.
- The prose card never hides a body heading, because in a prose note every `#` heading is a numbered section.
- Add an optional one-line `summary:` to prose notes as a subtitle.
- Don't add a stored status or "published" field to prose notes; draft progress comes from bob's TODO sections.
- No new note kind in bob's properties output for prose, which follows qj.2's "add no new wire kind" rule.
- `==` opens the Property Editor on `summary` rather than a new editor.
- Both cards use the existing `props_v1` check that decides when native Properties can be hidden.

**Design highlights:**
- Both cards share one implementation (as area and project cards do), with one precedence order so a note never gets two cards. A test should check every two-type combination.
- **Notebook Card:** a binder-spine icon, crumbs back to the root area, the summary (or a prompt to add one), the note count, a clickable index of `##` sections, child notebooks, the `@stem` capture route you can copy, and bob's warnings at the bottom.
- **Prose Card:** a drop-cap icon showing the title's first letter, the title in the prose serif font, the summary below it, and a line like "306 words · ≈ 2 min · 14 sections". While any section is still a TODO, a "draft ribbon" shows one segment per section, filled once it has words. On the blog draft it reads "1 of 14 sections written", and it disappears once nothing is a TODO.
- Draft wording for the two new glossary terms, "Prose Card" and "Notebook Card", is in the report. "Notebook Card" needs an explicit "not the notebook catalog card" clause to avoid confusion with the existing catalog in area notes.

**Recommended epic:**
1. **Notebook card.** Starts now with no gate.
2. **Prose card.** Starts after bob-cli-qj.4.
3. **Acceptance in real Obsidian, with screenshots.** Starts after bob-cli-qi.4 passes.
4. **Docs, glossary and deploy.** Starts after bob-cli-qi.6 and bob-cli-qj.4.

Decisions to put to you in the plan:
- Retire the notebook header everywhere (I recommend yes).
- Add `summary:` to prose notes (I recommend yes).
- Compute reading time in the plugin, or have bob report it (I recommend the plugin).
- Show the draft ribbon only while TODO sections remain (I recommend yes).
- Approve each glossary edit individually (all default off).

I suggest passing a note to the bob-cli-qj.5 planner to fill the prose card's reserved "where this came from" slot, with an "Inline back" action. I didn't edit any beads.
