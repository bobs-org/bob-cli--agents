# Chat History - ace-run (research.06.gem)

- **TIMESTAMP:** 2026-10-04 05:47:55 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.06.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261004_054029.md`

## Prompt

%id(gem, clan=research.06)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.06.cdx`, `research.06.cld`, `research.06.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I think that the `bob` command could organize its sub-commands more effectively to make
them easier / more intuitive to understand, but I'm not sure which sub-commands (if any)
deserve to be grouped together under one sub-command. For example, maybe we should
consider grouping some of bob's current sub-commands under a new `bob task` sub-command?

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution and
a recommended re-organization of the `bob` command's sub-commands. 
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

# Research Summary: `bob` CLI Subcommand Reorganization and Domain Grouping

- **Report Path:** [`bob_cli_subcommand_reorganization__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/repos/research/202610/bob_cli_subcommand_reorganization__gem.md)
- **Artifact Ref:** `file:explicit:2c11285699de23daf90da0b8` (`research:202610/bob_cli_subcommand_reorganization__gem.md`)
- **Researcher:** `research.06.gem`

---

## 1. Executive Summary & Critique of the `bob task` Plan

### Is grouping sub-commands under a new `bob task` sub-command a good idea?
**Partially yes, but an aggressive or broad `bob task` command is an anti-pattern.**

1. **The "Domain Currency Fallacy" (Why Maximalist Grouping Fails):**
   In `bob`, **tasks are the fundamental currency of the entire program**, not a peripheral feature. If we group all task-related commands (`plan`, `ready`, `freshness`, `randomize`, `capture`, `task-status-hooks`, `move-done-tasks`) under `bob task`:
   - **Ergonomics degradation:** High-frequency daily commands that Bryan runs multiple times every hour (`bob plan`, `bob ready`, `bob freshness`) become `bob task plan`, `bob task ready`, etc., imposing an unnecessary typing tax and breaking muscle memory.
   - **Conceptual mismatch:** `bob plan` is fundamentally about the **daily Pomodoro budget** (16-pomodoro ceiling, theme caps) and ledger capacity—not just tasks. `bob capture` captures notes, headings, and Pomodoro session adjustments, not just tasks.
   - **Deep hierarchy:** `bob freshness` already has subcommands (`list`, `seed`). Moving it under `task` creates triple-level nesting: `bob task freshness list`.

2. **Where `bob task` DOES Make Sense (Targeted Lifecycle Maintenance):**
   Creating a focused `bob task` command for task **maintenance and reconciliation** is a major win:
   - `bob task sync` (or `bob task hooks`): Replaces the clunky hyphenated `task-status-hooks`.
   - `bob task archive` (or `bob task move-done`): Replaces the awkward `move-done-tasks`.
   - Optional discoverability aliases: `bob task ready` and `bob task freshness` can point to `bob ready` and `bob freshness` for users exploring the `bob task` hierarchy, without stripping them from their fast top-level porcelain spots.

3. **The Real Culprit (The 10 Capture Endpoints):**
   The primary reason `bob` feels cluttered is not task commands, but the fact that **11 out of 28 subcommands start with `capture`** (39% of the CLI). Ten of these (`capture-parse`, `capture-complete`, `capture-targets`, `capture-tasks`, etc.) are machine-to-machine RPC plumbing for the Bob Mac Capture menu-bar frontend. They dwarf user-facing commands in `bob --help`.
   - *Crucial note:* These cannot simply become subcommands of `bob capture` (e.g. `bob capture complete`), because `bob capture` takes arbitrary free-text prose as trailing arguments; naming subcommands `complete` or `tasks` creates severe token collision hazards with task titles (e.g. `bob capture complete the Q3 taxes`).
   - *Solution:* Group the 10 capture endpoints into a designated `Plumbing / Capture Protocol` section in `--help` (or hide them behind `--full-help`), while keeping their command names intact for Bob Mac Capture Swift IPC.

---

## 2. Recommended Re-Organization of the `bob` Subcommands

We recommend a clean 3-tier structure that adheres to [`cli_rules.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/sase/memory/cli_rules.md) (alphabetical within categories, clear `-h|--help`, short aliases):

```text
bob
├── Daily Workflow (Top-Level Porcelain - High Frequency)
│   ├── capture                 Capture a task, bullet, or Pomodoro session
│   ├── freshness               Walk tiered freshness review queue (list, seed)
│   ├── plan                    Show daily Pomodoro budget & active task lanes
│   ├── randomize               Re-roll due prioritized tasks within windows
│   └── ready                   Show per-note Ready lanes against note cap
│
├── Domain Management (Noun -> Verbs)
│   ├── gkeep                   Google Keep inbox drain (list, pull, doctor, login)
│   ├── highlights              PDF annotation sync and intake (clip, create, scan, sync)
│   ├── plugins                 Manage Bob custom Obsidian plugins (list, sync)
│   ├── pomodoro                Inspect Pomodoro timer status and integrations
│   │   ├── [status]            (default) Show current Pomodoro status
│   │   ├── tmux                Format Pomodoro status & plan meter for tmux
│   │   └── notify              Send desktop notification on session completion
│   ├── projects                Manage project notes via their ^prj tasks (list, sync)
│   ├── task                    Task lifecycle, maintenance, and reconciliation
│   │   ├── sync                Reconcile active task dependencies and statuses
│   │   ├── archive             Archive completed and canceled tasks to done/
│   │   ├── ready               (alias -> bob ready)
│   │   └── freshness           (alias -> bob freshness)
│   └── vault                   Obsidian vault Git synchronization and health
│       ├── sync                Pull, commit, and push vault Git changes
│       └── nightly             (alias -> bob nightly) Run nightly maintenance
│
├── System & Inspection
│   ├── completion              Install and inspect shell completion (install, status)
│   ├── nightly                 Run full nightly sync and maintenance workflow
│   └── query                   Run headless Dataview and Tasks queries
│
└── Capture Protocol (Plumbing - Hidden or Grouped under --full-help)
    ├── capture-complete        RPC: Complete marker/wikilink at cursor
    ├── capture-parse           RPC: Explain in-progress capture text
    ├── capture-pomodoro-name   RPC: Name an open unnamed Pomodoro
    ├── capture-pomodoros       RPC: List today's Pomodoro ledger entries
    ├── capture-rewrite         RPC: Apply automatic draft rewrites
    ├── capture-sections        RPC: List non-Tasks sections in note
    ├── capture-targets         RPC: List capture routes
    ├── capture-task-id         RPC: Assign block ID to open task
    ├── capture-task-sections   RPC: List child sections of task
    └── capture-tasks           RPC: List open tasks in note
```

---

## 3. Mapping and Backward-Compatibility Guarantees

Every existing command remains executable through compatibility aliases, guaranteeing **zero disruption** to external systems:

| Current Command | Proposed Primary Form | Compatibility Status | Callers Protected |
| :--- | :--- | :--- | :--- |
| `bob task-status-hooks` | `bob task sync` | Retained as alias | Git hooks, `bob-plugins` docs |
| `bob move-done-tasks` | `bob task archive` | Retained as alias | `bob nightly`, maintenance scripts |
| `bob tmux-pomodoro` | `bob pomodoro tmux` | Retained as alias | `tmux.conf` status line |
| `bob notify` | `bob pomodoro notify` | Retained as alias | `~/bin/executable_bob_notify` |
| `bob vault-sync` | `bob vault sync` | Retained as alias | `~/bin/executable_bob_vault_sync_watch` |
| `bob capture-*` (10 endpoints) | Unchanged name; grouped as Plumbing in help | Retained as primary endpoints | `bob-mac-capture` Swift IPC |
| `bob plan`, `ready`, `freshness` | Unchanged | Unchanged | Human morning review routines |

---

## 4. Proposed Implementation Roadmap

1. **Phase 1: Clap Help Facelift (Immediate visual win, 0% risk):**
   - Add categorized help headings (`Daily Workflow`, `Domain Management`, `Inspection & System`, `Plumbing / Capture Protocol`) in `src/runner.rs`.
   - Keep all subcommands alphabetical within their headings.
   - This cuts top-level help visual clutter by ~50% immediately without renaming a single command.
2. **Phase 2: Introduce `bob task`, `bob pomodoro`, and `bob vault`:**
   - Implement `bob task sync` (wrapping `task_status_hooks`) and `bob task archive` (wrapping `collect_done`).
   - Implement `bob pomodoro tmux` and `bob pomodoro notify`.
   - Implement `bob vault sync`.
   - Register old command names in `HIDDEN_SUBCOMMAND_ALIASES` in `src/runner.rs`.
3. **Phase 3: Update Shell Completion & Script Wrappers:**
   - Mount new subcommands in `src/native/completion/tree.rs`.
   - Update `chezmoi` wrappers (`tmux.conf`, `executable_bob_notify`) to use new canonical paths over time.

The finalizer declaration for the completed research report has been published and accepted (`commit` authorized for `sdd:research`).
