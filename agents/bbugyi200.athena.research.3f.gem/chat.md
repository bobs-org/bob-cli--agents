# Chat History - ace-run (research.3f.gem)

- **TIMESTAMP:** 2026-10-02 14:55:35 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3f.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261002_144331.md`

## Prompt

%id(gem, clan=research.3f)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3f.cdx`, `research.3f.cld`, `research.3f.grk`, `research.3f.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to
improve the way that I track Obsidian task dependencies.

- I currently use transcluded links to tasks as sub-bullets on task A when I want to
  treat those tasks as dependencies of task A (i.e. those tasks need to be completed
  before task A is marked as unblocked).
- I want to stop using transcluded task links and instead just use normal task links for
  this. I also want to start listing all dependency task links on a single line in some
  visually appealing way.
- Finally, it needs to be very easy for users to add/remove dependency tasks, which can
  be located in any area/project note file in my Obsidian vault, to/from the currently
  selected task. I was thinking we could use the `<ctrl+shift+p>` keymap for this
  somehow, which already has support for our current dependency solution I think.
  Whatever solution you decide on, keep in mind that we need to support fuzzy searching
  for tasks across my entire Obsidian vault.
- We should add a new "task dependency link" (aka "task dep link") glossary memory web
  term to describe these dependency task links.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

I have completed the independent research investigation on improving Obsidian task dependency tracking and registered the research report as requested.

### Research Report Artifact
- **File:** [`single_line_task_dependency_links__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/research/202610/single_line_task_dependency_links__gem.md)
- **Durable Artifact Ref:** `research:202610/single_line_task_dependency_links__gem.md` (`file:explicit:43d5f7b7e408e6cb48bc75db`)

---

### Key Research Findings & Critique

#### 1. Critique of the Transition from Transclusions to Normal Task Links
- **Strongly Endorsed:** The July 2026 experiment with transcluded sub-bullets (`- ![[note#^id]]`) introduced severe layout degradation in Obsidian Live Preview. It created heavy card-like embeds with nested borders and padding, caused viewport/cursor jumping in Vim normal mode, and made strikethrough for completed dependencies (`~~![[...]]~~`) structurally broken.
- **Normal Wikilinks (`[[target#^id|alias]]`) Fix These Flaws:** Switching back to normal task links restores vertical rhythm, supports clean native strikethrough (`~~[[...]]~~`) on completion, enables standard hover previews via Obsidian's Page Preview core plugin, and eliminates Vim-mode DOM hopping.

#### 2. Visual & Syntactic Design for Single-Line Listing
To ensure the format is intuitive, reliable, and beautiful, we build directly upon Bob's established log grammar (`🗓️ **SCHEDULE LOG:**`, `⏱️ **WORK LOG:**`):
```markdown
- [?] #task Ship bob-cli v2.0 [dependsOn:: Apollo__api, ux-review] ^ship-cli
  - 🔗 **DEPENDS ON:** [[Projects/Apollo#^api|Deliver Backend API]] • [[#^ux-review|Conduct UX Review]]
```
- **Delimiters & Aliases:** Delimited by ` • ` (bullet dot with single spaces). Automatically populating link aliases (`|Clean Title`, truncated to 40 characters) is critical so links render as readable natural text rather than opaque technical slugs like `Projects/Apollo > ^api`.
- **Completion Strikethrough:** When a prerequisite is marked done, `task-status-cycler` wraps that link in strikethrough:
  ```markdown
  - 🔗 **DEPENDS ON:** ~~[[Projects/Apollo#^api|Deliver Backend API]]~~ • [[#^ux-review|Conduct UX Review]]
```

#### 3. Preserving Dual State: Machine Truth vs. Human Presentation
- **`[dependsOn:: ...]` on the task line must remain the semantic source of truth.** Obsidian Tasks and Dataview rely on this inline field for blocker queries and task state derivation.
- **The child bullet `- 🔗 **DEPENDS ON:** ...` serves as the human navigation and link-graph layer.** `bob task-status-hooks` reads this bullet to establish `dependency_edges` for Pomodoro Next promotions (`[*]`) and recent-activity recovery.
- `bob-navigation-hotkeys` maintains bidirectional synchronization between the two representations.

#### 4. Interaction Design in `<ctrl+shift+p>` with Vault-Wide Search
- Currently, `BulletPropertyPickerModal` for `dependsOn` only calls `getOpenLocalTasks()`, restricting search to the active note.
- **Vault-Wide Scoped Search:** When `dependsOn` is selected, the modal should query an in-memory index of tasks residing in all Area and Project notes (`type: [[area]]` or `type: [[project]]`).
- **Fuzzy Matching:** Matches against both the task description and the project/area note name (e.g. typing `apollo api` matches `Deliver Backend API` in `Projects/Apollo.md`).
- **Target Block-ID Handling:** If a selected target task lacks a trailing block ID, the modal prompts or generates an intuitive slug (e.g. `^deliver-backend-api`), updates the remote note via `app.vault.process`, and creates the link without requiring the user to open the target file.

---

### SASE Memory Web Strand: `Task Dependency Link`

A new strand has been drafted for `sase/memory/glossary/task_dependency_link.md`:
```markdown
# Task Dependency Link

*Requested · project*

aka task dep link, dependency task link

A normal (non-transcluded) block link to an Obsidian task (`[[note#^block-id]]` or `[[#^block-id]]`, formatted with an optional display alias `|alias`) used to record that the target task is a prerequisite dependency of the containing or parent task.

Task dependency links are listed together on a single managed child bullet formatted as `- 🔗 **DEPENDS ON:** [[...]] • [[...]]` beneath the dependent task, synchronized with the machine-readable `[dependsOn:: ...]` inline metadata on the parent task. Completed dependencies are formatted with strikethrough as `~~[[...]]~~`.

When a task is linked under today's open Pomodoros, `bob task-status-hooks` traverses its task dependency links to promote those prerequisites to Next (`[*]`). Removing all dependency links removes the child bullet and clears the `[dependsOn:: ...]` metadata.
```
*Note:* The existing `glossary:task-link` strand will be updated to retire its legacy mention of transcluded task links as sub-tasks.

---

### Recommended Implementation Roadmap
1. **`bob-plugins` (`bob-navigation-hotkeys`):**
   - Update `DEPENDENCY_NAVIGATION_BULLET_RE` and `formatDependencyNavigationBulletWithMarker` to generate the single `🔗 **DEPENDS ON:**` bullet with aliases.
   - Implement `VaultTaskIndex` to index open tasks in notes with `type: [[area]]` and `type: [[project]]`.
   - Update `BulletPropertyPickerModal` to support vault-wide fuzzy search and remote block-ID insertion.
2. **`bob-plugins` (`task-status-cycler`):**
   - Hook into task closure to strike through completed dependency links on parent bullets.
3. **`bob-cli` (`task-status-hooks`):**
   - Replace `sole_transcluded_block_reference` in `references.rs` with `dependency_bullet_references` that extracts non-struck wikilinks from `🔗 **DEPENDS ON:**` bullets and strips aliases.
4. **Vault Migration Script:**
   - Execute an idempotent migration script (`scripts/migrate-task-dependency-links.mjs`) to convert existing per-dependency transclusion bullets across `~/bob/` into the consolidated single-line format.
