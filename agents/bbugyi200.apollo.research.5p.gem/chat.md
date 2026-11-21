# Chat History - ace-run (research.5p.gem)

- **TIMESTAMP:** 2026-11-21 09:59:35 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.5p.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261121_093853.md`

## Prompt

%id(gem, clan=research.5p)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5p.cdx`, `research.5p.cld`, `research.5p.grk`, `research.5p.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to give bob support for sub-tasks.

- I was originally planning on calling these "micro tasks" and had launched the
  bob-cli-of epic bead for this work.
- I canceled the agent working this epic, however, since I think several of the
  requirements were not desirable / quite correct.
- See the ^micro-tasks-cleanup task in the ~/bob/bob.md file for some context on the
  improvements I would like to make to this design. Also, review the other tasks that
  the ^micro-tasks task in the ~/bob/bob.md file depends on and the tasks that those
  tasks depend on for an idea of the direction I am thinking of heading in with this
  feature.
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

I have completed the independent design research for Bob sub-tasks and written the report to:

- **Report:** [bob_subtasks_redesign__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/bob_subtasks_redesign__gem.md)
- **Registered artifact:** `file:explicit:f50da0993de6099b577c6da5` (`research:202611/bob_subtasks_redesign__gem.md`), stored at [bob_subtasks_redesign__gem-1c632a156a69.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261121093858/bob_subtasks_redesign__gem-1c632a156a69.md)

### Highlights & Recommended Solution

1. **Verdict — canceling `bob-cli-of` was the right call.** Keeping `- [ ]` (without `#task`) as the stored 1-byte state carrier is still the right foundation (verified **0** plain single-char checkboxes and **0** nested `#task` lines across all **776** open tasks in `~/bob/`), but dropping nesting, hiding the checkbox in favor of `⌗⌗`, enforcing four-zone anatomy (`Links < Sub-tasks < Drawers < Logs`) with an auto-`NOTES` drawer, and removing in-flight completion turns a task block into a true 1:1 structural twin of a Project Note — directly unlocking `^better-o`, `^no-all-caps-for-drawers`, `^tasks-parent-projects`, and `^task-to-project`.
2. **Eight justified adjustments called out in the report:**
   - **A1 (Name):** Use **Sub-task** (`sub-task` / `subtask`) rather than "task requirement" (`req`), which collides with the existing `REQUIREMENTS` drawer and jars on errands/merges.
   - **A2 (Unified pre-close audit):** Make `Esc` on a sub-task close card abort the close ("Not done yet", parent stays open, `]s` walk stays put) in **both** Obsidian and Mac Capture, eliminating `bob-cli-of`'s asymmetry where Obsidian wrote `[x]` before showing the card.
   - **A3 (0 → ≥1 loose-note sweep):** When a Bob writer adds the first sub-task to a task that already has loose notes, sweep those loose notes into `- NOTES` in the same undoable edit; keep readers tolerant and keep `bob task reconcile` to safe stable zone-sorting only.
   - **A4 (`CANCEL LOG` slot):** Keep `❌ **CANCEL LOG**` at slot 0 on cancelled tasks (preserving existing cancel/dependency contracts) so active tasks stay pure `Links < Sub-tasks < Drawers < Logs`.
   - **A5 (Checkbox-free visual craft & `[x]` retention):** Refuse early completion in gestures while retaining `[x]` in storage/readers (needed for closed parents, reopened parents, and future `^task-to-project`). Render via `Decoration.line` + CSS on `input.task-list-item-checkbox` (matching `bob-ledger-tools`'s Blocked Marks architecture): **`⌗⌗`** in owner ink for `[ ]`, muted **`⌗⌗`** + strike for `[x]`, quiet **`⊘`** + strike for `[-]` (explicitly overriding `task-statuses.css`'s grey row banner), and quiet **`→`** + clickable link for `[>]`.
   - **A6 (Single-level merge rule):** Allow nested plain notes under a sub-task; when merging a source task that has sub-tasks into a target task, fold its sub-tasks into plain notes under `- [ ] <source>` with a preview notice (alternative: strict refusal via `merge_source_open_subtasks`).
   - **A7 (Cross-surface authoring):** Replace `..` with **`- [<space>` → `- [ ] `** and atomic **`<Backspace>` → `- `** in both Mac Capture (prefiltered on `[` so ordinary spaces never spawn `bob`) and Obsidian CM6 (handling `autoPairBrackets`), plus `@route+id [<space>` and a dedicated Obsidian **`Ctrl+Shift+X`** obsolete/restore gesture with optional reason.
   - **A8 (`Ctrl+J` jump support on `api.successors` v6):** Keep `Ctrl+J` strictly navigation-only (`decisions:successor-jump-parks-the-walk`): landing on the **newly split `#task` line** when a sub-task is Kept Open / Pulled In, and on the sub-task's closed line (with a status reminder `⌃X to keep open as a task`) if pinned while Done/Not done.

### Key Open Decisions for Bryan

1. Confirm **Sub-task** vs. **Task requirement** (if retiring the `REQUIREMENTS` drawer convention).
2. On **Task Merge** when the source task has sub-tasks: fold into plain child notes under `- [ ] <source>` with a preview warning (recommended), or strictly refuse?
3. Confirm **pre-close `Esc` abort** in Obsidian when open sub-tasks are on the card (recommended) vs. legacy post-close `Esc` + a separate abort key.
4. Confirm keeping **`CANCEL LOG`** at slot 0 on cancelled tasks (recommended) vs. moving it to Zone 4.
