# Chat History - ace-run (research.4d.gem)

- **TIMESTAMP:** 2026-10-13 09:49:38 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4d.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261013_093556.md`

## Prompt

%id(gem, clan=research.4d)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4d.cdx`, `research.4d.cld`, `research.4d.grk`, `research.4d.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
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

# Research Report: Reverse Dependency Sub-Bullets (`BLOCKS:`)

The complete research report has been written to:
[task_blocking_sub_bullet_dependencies__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/task_blocking_sub_bullet_dependencies__gem.md)

And registered as a durable artifact snapshot:
- **Ref:** `file:explicit:f422af0c2969f4d0b7920fcf`
- **Label:** `research:202610/task_blocking_sub_bullet_dependencies__gem.md`

---

## Executive Summary & Design Critique

### 1. Is this a good idea?
**The underlying intent is exceptionally high-value, but implementing it as a physical, bidirectional Markdown sub-bullet is an architectural trap.**

In GTD and daily task execution, knowing that completing Task A unblocks 3 other tasks is crucial prioritization context. Currently, the forward dependency line (`⛓️ **DEPENDS ON:**`) makes blocking status visible only on the *dependent* task, leaving the *prerequisite* unaware of its downstream impact.

However, writing physical `BLOCKS:` sub-bullets directly to Markdown files on disk introduces five severe hazards:

1. **Dual Source of Truth & Synchronization Hazards:**
   If both `DEPENDS ON:` and `BLOCKS:` exist in Markdown text, which is authoritative? If a user hand-edits or deletes a link from `BLOCKS:`, does `bob task reconcile` overwrite the user's edit, or modify the dependent's file? A dual-authoritative text model breaks the foundational rule codified in [`task-deps-are-depends-on-links`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/docs/task-dependencies.md).
2. **Extreme Write Amplification & Vault Churn:**
   Every time a dependent task is added, removed, or **completed** (`[x]`), the prerequisite's note must be modified. If foundational tasks retain completed blockers as history, lines grow unbounded; if completed blockers are pruned, closing tasks in daily notes will continuously dirty unrelated project files across the vault, causing constant Git diff noise and Obsidian sync events.
3. **Broken Atomic Undo in Obsidian (`<ctrl+shift+p>`):**
   CodeMirror editor transactions (`Ctrl+Z`) are strictly single-note. Modifying a cross-note prerequisite in the background via `app.vault.process()` cannot participate in the active editor's undo stack, creating immediate desynchronization if the user presses undo.
4. **Violation of Immutability Boundaries:**
   Bob strictly enforces that previous daily notes (`YYYYMMDD.md`) and archived tasks in `done/` are read-only (`docs/task-dependencies.md` §4.1). If a task in an immutable note blocks another task, a physical sub-bullet cannot be legally written, resulting in inconsistent state across the vault.
5. **Visual Clutter:**
   Tasks already carry metadata children (`DEPENDS ON`, `SCHEDULE LOG`, `CANCEL LOG`, Work Logs). Injecting a second dependency sub-bullet bloats task blocks, pushing actual tasks off-screen.

---

## Recommended Solution: Two-Tier Architecture

### Tier 1 (Recommended / Primary): Virtual "Blocks" Chips in `bob-ledger-tools`
Instead of dirtying Markdown on disk, compute reverse dependencies **in memory** using Obsidian's existing Tasks/Dataview index (`getTasks()`):
- **Live Preview & Reading View Decoration:** Tasks plugin already indexes `task.id` and `task.dependsOn`. `bob-ledger-tools` builds the in-memory inverted graph ($\text{PrerequisiteId} \to \text{Dependents}$) in sub-millisecond time.
- **The Visual Design:** Render an interactive, beautiful chip on the prerequisite task line:
  ```text
  [ ] Refactor payment processor gateway ^pay-gw   [ 🚧 blocks 3 ]
  ```
- **Interactive Popover:** Clicking or hovering the chip opens an interactive popover listing all blocked tasks, their live status icons (coloured checkboxes), parent note badges (`↗ note`), and direct jump navigation.
- **Key Advantages:** Zero disk writes, zero Git noise, zero sync conflicts, instant reactive updates upon task completion, and 100% compatibility with past daily notes and immutable archives.

### Tier 2 (Strict Fallback Spec): Asymmetric Physical Markdown Projection
If physical Markdown lines are strictly required for headless terminal / CLI editing, they must be implemented under a strict, bounded contract:
- **Asymmetric Authority:** `⛓️ **DEPENDS ON:**` remains the **sole source of truth**. `⛓️ **BLOCKS:**` is strictly a downstream, derived view (never an edit surface). Manual additions to `BLOCKS:` are ignored or warned.
- **Writer Form:**
  ```markdown
  - [ ] Implement user authentication backend ^auth-be
    - ⛓️ **DEPENDS ON:** [[db#^schema-v2]]
    - ⛓️ **BLOCKS:** [[ui#^login-page]] • [[api#^session-tokens]]
    - 🗓️ **SCHEDULE LOG**
  ```
- **Lifecycle & Dynamic Pruning:** Lists **only open, actively blocked dependents**. Completed tasks are pruned immediately. When all blocked tasks resolve, the `BLOCKS:` line is **completely deleted**.
- **Immutability Exemptions:** Daily notes prior to today and notes in `done/` are strictly exempt from receiving physical `BLOCKS:` lines.
- **Hotkey Decoupling:** `<ctrl+shift+p>` updates same-note targets in the editor transaction, but defers cross-note `BLOCKS:` generation to `bob task reconcile` to preserve atomic single-note undo and avoid background buffer conflicts.

---

## Summary of Requirement Adjustments

| Ref | Original Requirement / Assumption | Recommended Adjustment |
| :--- | :--- | :--- |
| **ADJ-1** | Add physical sub-bullet to Markdown | **Make Virtual Live Preview Chips (Tier 1) the primary experience.** |
| **ADJ-2** | Sub-bullet added on `<ctrl+shift+p>` | **Same-note targets update in-transaction; cross-note targets defer to `reconcile`.** |
| **ADJ-3** | Sub-bullet indicates blocked tasks | **`BLOCKS:` lines must list ONLY open, active dependents (no completed history).** |
| **ADJ-4** | Sub-bullet exists permanently | **Delete the `BLOCKS:` line completely when all blocked tasks resolve.** |
| **ADJ-5** | Bidirectional consistency | **`DEPENDS ON:` is the sole authority; `BLOCKS:` is strictly a read-only projection.** |
| **ADJ-6** | Universal vault participation | **Explicitly exempt past daily notes and `done/` archive notes.** |
| **ADJ-7** | Syntax & Formatting | **Use `- ⛓️ **BLOCKS:** [[...]] • [[...]]` joined by ` • `.** |
| **ADJ-8** | Child line hierarchy | **Position `BLOCKS:` immediately beneath `DEPENDS ON:` and above `SCHEDULE LOG`.** |

---

## Suggested Implementation Roadmap

1. **Phase 1 (Obsidian):** Implement Virtual "Blocks" Chips in `bob-plugins/plugins/bob-ledger-tools`. Provides instant, zero-churn visual clarity across the vault.
2. **Phase 2 (CLI):** Add a CLI inspection query `bob task blockers <block-id>` for terminal workflows.
3. **Phase 3 (Optional Physical Projection):** If raw file inspection remains necessary, implement the Tier 2 inverted graph generator in `bob task reconcile` (`src/native/task_status_hooks/reconcile.rs`).
