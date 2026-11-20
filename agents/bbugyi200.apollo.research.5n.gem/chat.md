# Chat History - ace-run (research.5n.gem)

- **TIMESTAMP:** 2026-11-20 16:31:25 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.5n.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261120_160058.md`

## Prompt

%id(gem, clan=research.5n)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5n.cdx`, `research.5n.cld`, `research.5n.grk`, `research.5n.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add much better (and explicit) support for "micro tasks".

- A "micro task" is a sub-bullet on an Obsidian task that would be converted to a task
  in the new project file if its parent task were converted to a project (e.g. via the
  `<ctrl+shift+alt+n>` keymap).
- We currently consider any sub-bullet that does not belong to a drawer to be a micro
  task (though we don't use this term yet).
  - We should instead start treating these bullets as if they were placed in a "NOTES"
    drawer and require that micro tasks be marked as such explicitly.
  - Any notes added to a task via captures (using the `@foo+bar` capture syntax, for
    example) should be added to the NOTES drawer by default unless another drawer is
    explicitly specified or a micro task marker is specified in the capture.
- I was thinking that we could either use a `TASK:` or `#task` prefix for these
  sub-bullets to mark them as micro tasks, but this is just my first thought. Think hard
  about the best way to mark these.
- We should support nested micro tasks (i.e. micro tasks with micro task parents).
- Regardless of how we decide to mark micro tasks, the mark should be rendered in a
  consistent and concise way. I was thinking we could render 2 or more `#` characters
  (depending on the micro task nesting level) for this micro task marker.
- It needs to be very easy to specify micro tasks in the capture panel. I was thinking
  that we could use `..` as a capture alias for the micro task marker (so `- ..` would
  be converted to `- #task `, for example) and add a new `<ctrl+g>t` keymap that toggles
  the micro task prefix for the current bullet.
- Top-level (i.e. `##`) micro tasks should show up as successors, which are closed by
  default, when their parent task is closed.
  - The user can decide to open these tasks using the `<ctrl+x>` keymap on the successor
    panel, in which case a new Obsidian task should be created for that micro task. The
    micro task bullet in the original task should be crossed out and an appropriate note
    should be placed next to it that links to the original parent task.
  - After opening a micro task successor, the user can also check it (e.g. using the
    `<space>` or `<tab>` keymaps), in which case the new task that is created should
    have a task link added to today's daily file (i.e. it should be pulled in).
  - The user can also canel a micro task successor using the `<ctrl+shift+x>` keymap, in
    which case the micro task sub-bullet should be striked out after closing the parent
    task (to indicate that it was not complete).
  - All non-top-level micro tasks (e.g. `###`, `####`, etc...) should still show up on
    the successor panel but should not be actionable since their status will be
    deteremined by whatever status we decide to give their parent micro task.
- When we merge a task into another task using one of the configured `merge_labels`, we
  should start creating a new micro task in the target task that represents the source
  task. I think this should just involve adding the microtask marker but there might be
  more work involved.
- As a part of this change, we should add an excellent new glossary term for "micro
  task".
- The Goals of this Change
  - Micro task successors will help me make sure that I've really completed all of the
    work that a task commits to before closing it.
  - I would like to soon make it possible to convert any project (regardless of how
    complex) into an equivalent task. This is out of scope for this research report but
    is a motivating factor, since this change will make it possible to convert
    sub-projects into equivalent micro tasks.
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

Completed independent research and wrote the design report to [explicit_micro_tasks_design__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202611/explicit_micro_tasks_design__gem.md), registered as snapshot `research:202611/explicit_micro_tasks_design__gem.md` (`id: explicit:8403637a96abdd181015de09`), and declared via `sase final submit`.

### Summary of Recommendations & Critiques

1. **Canonical Marker (`- TASK: <text>` over `- #task <text>`)**
   - **`- #task` conflicts with existing invariants**: Leading `- #` on a first-level capture child is reserved exclusively for drawer shortcuts ([drawer_bullet.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture_language/drawer_bullet.rs)), [note_tasks.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/note_tasks.rs) and [plan.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/task_split/plan.rs) treat `#task` as the Tasks global filter, [docs/task-tag-marks.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/task-tag-marks.md) uses raw `#task` pills on non-task lines to indicate Tasks ignores them, and Obsidian indexes `#task` across non-task bullets.
   - **Recommended syntax**: Use **`- TASK: <text>`** canonically while excluding empty `TASK` and `TASK:` in `is_drawer_title` ([capture_drawers.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture_drawers.rs)) and `isTaskSplitDrawerTitle` ([256-task-split-plan.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/256-task-split-plan.js)).

2. **Depth-Invariant Text + Dynamic Visual Multiplicity (`##`, `###`, ...)**
   - Store `- TASK:` at every nesting depth in raw Markdown and compute the rendered hash count (`d + 1` stacked `--bob-task-tag-glyph` hashes) dynamically in [138-task-tag-marks.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/138-task-tag-marks.js) and [264-plugin-task-tag-marks.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/264-plugin-task-tag-marks.js) from list depth beneath the enclosing `#task`. This keeps indent/outdent, task split, task merge, and future `project <-> task` conversions free of descendant text rewrites.

3. **`NOTES` Drawer & Capture Ergonomics**
   - Default unmarked `@foo+bar` captures into `NOTES` (or `## Notes` on `^prj`) via `ensure_drawer` ([plan.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture/plan.rs)), while inserting `TASK:` bullets directly beneath the task above drawers and refusing `TASK:` inside glued `#drawer` captures.
   - On forward promotion (`<ctrl+shift+alt+n>` in [110-project-seed.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/110-project-seed.js)), promote top-level `TASK:` bullets to `## Tasks` and preserve legacy unmarked non-drawer direct child bullets by folding them into `## Notes`.
   - `- ..` -> `- TASK: ` in [rewrite.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture_language/rewrite.rs) has no collision with existing `.` -> `@` / `&` fast double-tap escapes ([CapturePanelModel.swift](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CapturePanelModel.swift)); `<ctrl+g>t` extends `editorLeaderBindings` alongside `"u": .toggleLineCase` in [CaptureKeyCommandRouter.swift](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-mac-capture/Sources/BobMacCapture/CaptureKeyCommandRouter.swift) and registers `toggle-micro-task` in `bob-navigation-hotkeys`.

4. **Micro-Task Successors on Parent Close**
   - Always surface top-level (`##`) micro tasks as **closed-by-default** offers (`OfferGroup::MicroTask`) when closing a parent Done, with nested `###+` micro tasks displayed beneath them as non-selectable child rows whose status mirrors their parent micro task.
   - **Keymap critique**: Because `<ctrl+x>` already stages **Done** on dependent rows in [206c-successor-picker-verdicts.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/206c-successor-picker-verdicts.js) and `pullInChoiceCommand` in `CaptureKeyCommandRouter.swift`, recommend keeping `<ctrl+x>` = **Done / Re-close**, using **`<ctrl+o>`** / **`<ctrl+shift+t>`** to **Split Out (Open)**, **`<space>` / `<tab>`** for **Auto-Open + Pull-In**, and **`<ctrl+shift+x>`** to **Cancel** (`~~TASK: ...~~`).
   - On Split Out, strike out the micro-task bullet in the closed parent with a link to the newly created task (`- ~~TASK: Foo~~ → [[#^id|Foo]]`), move nested children onto the new task, place it via `choose_placement`, and attach `LINKED FROM` pointing back to the original parent task.

5. **`merge_labels` & Task Merge (`payload.rs`)**
   - Update `build_payloads` in [payload.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/task_merge/payload.rs) for `MergeContainer::Task` uniformly across `merge_labels`, `>`, `<`, and `bob task merge` (while keeping `MergeContainer::Drawer` free of `TASK:` bullets), preserving source drawers and child micro tasks nested beneath the merged micro task.

6. **Diagrams & Verification**
   - Both Mermaid figures in the report were rendered via `@mermaid-js/mermaid-cli@12.0.0`, measured above the 75% PDF box threshold (`91.1%` for `fig1`, `85.8%` for `fig2`), and visually inspected from rendered PNGs.
