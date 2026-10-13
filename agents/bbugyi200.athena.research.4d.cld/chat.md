# Chat History - ace-run (research.4d.cld)

- **TIMESTAMP:** 2026-10-13 09:58:11 EDT
- **MODEL:** claude/opus
- **AGENT:** research.4d.cld
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261013_093556.md`

## Prompt

%id(cld, clan=research.4d)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.4d.cdx`, `research.4d.grk`, `research.4d.mus`, `research.4d.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

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
would like to start automatically adding a new sub-bullet to tasks that other tasks
depend on to indicate that the task blocks one or more other tasks.

- We already use a "Depends On" sub-bullet on the dependent tasks.
- This should happen automatically when dependencies are added to tasks (via the
  `<ctrl+shift+p>` keymap, for example).
- The `bob task reconcile` command should ensure the appropriate sub-bullets all exist
  and are consistent.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

I'm reading the dependency contract docs and the Depends-On writers in bob-cli and bob-plugins before drafting the design.

Still researching: I found that the `🧩 Sub-projects` line is an existing machine-owned reverse-index line, which is a close precedent. Next I'm measuring real dependency edges in the vault.

I'm now sending two read-only code-exploration helpers through the plugin and Rust writers while I check outside precedents (Tasks plugin, Linear, GitHub).

Both code maps are back. I'm now measuring how many open dependents lack block IDs, since BLOCKS links need IDs on those tasks.

I'm verifying the most serious compatibility hazard the plugin map flagged: block-id-prompt's Task Link gesture deleting links.

The design is settled; writing the report now.

Report written. Registering it as a durable artifact.

Registration succeeded. Now submitting the final declaration.

I've written the report and registered it as an artifact. The research repo commits after this turn ends. My recommendation is to build the BLOCKS line, but only as a copy that is generated from your existing `⛓️ DEPENDS ON` lines and never read back as data. It works like the existing `🧩 Sub-projects` line. If it became a second editable copy of the dependency graph, the two copies would drift and could break each other.

**How big it is today:** your vault has 57 dependency links, but only 21 run between two open tasks. That means about **15 BLOCKS lines** and **6 dependent tasks needing new block IDs** (a link needs one). Most lines would hold a single task from the same note. The real value is in links between notes and in tasks with several dependents, such as `cash#^unemployment`, which has 4.

**Recommended design:**
- **Format:** `- 🧱 **BLOCKS:** [[#^a]] • [[note#^b]]`, placed right after the Depends-On line. On `^prj` it comes before `🧩 Sub-projects`.
  - It uses the same link rules as Depends-On, sorted alphabetically by link text. Reconcile moves task blocks between sections on every run, so document order isn't stable.
  - I chose 🧱 because the alternatives are taken: 🚧 is already nav's WIP glyph, ⛔ is the Tasks plugin's "depends on" emoji, and 🔓 and ⏳ are in use.
- **Who gets a line:** open tasks with at least one open dependent, the same rule as the Tasks plugin's `is blocking`. Once a task closes, its line is never touched again and stays as history.
- **`bob task reconcile` is in charge.** A new pass after the dependency step creates, rewrites, de-duplicates and deletes lines, and adds block IDs where needed. A config switch, `dependencies.blocks_lines: false`, removes every line with nothing lost.
- **Immediate updates:** every gesture that adds *or removes* a dependency updates the line at once.
  - If both tasks are in the same note, one Ctrl+Z undoes both changes.
  - If they're in different notes, the second write is best-effort and reconcile fixes any miss within one run.
  - Closing a dependent is left to reconcile.
- **The line is read-only.** Hand edits are put back with a notice. You change it through the chip `×`, and later through a "Blocks…" picker on the Task Card (key `B`, the reverse of `b`) that writes the dependent's Depends-On line.
- **Chips:** they show the live state, so the display is right even before reconcile catches up. 🔑 marks a dependent for which this task is the *last* thing in the way, and the summary reads "frees N of M".

**Changes to your requirements, called out in the report:**
- Only open tasks and their open dependents are listed, not every dependent ever.
- Removing a dependency must update the line too, not just adding one.
- Dependents without a block ID get one generated.
- Blocking that a task inherits from its project is not copied onto lines.
- The off switch deletes all lines.
- Every plugin and the Rust code learn to ignore the new line before anything writes it.

That last point matters because I found three places that would misread the line today:
- **block-id-prompt:** Ctrl+Shift+Enter on a BLOCKS link would run the Task Link flow on it, because only Depends-On lines are guarded.
- **Capture:** it would count a BLOCKS line in today's daily note as a Task Link sighting.
- **Pomodoro scanning:** it would treat the line's links as Task Links if the task sits inside the Pomodoros section. Depends-On lines already have this latent bug.

The report also covers alternatives I rejected, draft test cases for a new section of `docs/task-dependencies.md`, a six-phase rollout, and five questions for you (label, the `B` key, and which task the reverse picker marks as fresh).

Files are in `sase/repos/research/202610/`:
- blocks_line_reverse_dependency_mirror__cld.md (artifact `file:explicit:46098c92b2089986292d458e`)
