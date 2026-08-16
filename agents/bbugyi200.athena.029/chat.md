# Chat History - ace-run (029)

- **TIMESTAMP:** 2026-08-15 09:51:07 EDT
- **MODEL:** agy/gemini-3.7-flash-high
- **AGENT:** 029

## Prompt

#gh:gh_bobs-org__bob-cli Describe this repo. %m:agy/gemini-3.7-flash-high

## Response

# Bob CLI (`bob-cli`)

[`bob-cli`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/README.md) is a high-performance command-line suite written in Rust (2024 edition) that powers the backend automation, task lifecycle management, note parsing, and Pomodoro workflow for Bryan's Bob Obsidian vault (`~/bob` or `$BOB_DIR`).

---

## Key Features & Subcommands

The primary CLI binary is [`bob`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/main.rs), which provides a rich set of subcommands:

### 1. Fast Capture Engine
* **[`bob capture`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture.rs)**: Captures tasks, plain Markdown bullets, and bounded sub-bullet hierarchies into target notes (`mac_inbox.md`, areas, projects) without needing desktop Obsidian open.
* **Routing, Scheduling, & Priorities**: Supports `@route` targets, relative scheduling (`s:<N>`), priority rolls (`p:1`–`p:4`) with automated `🗓️ SCHEDULE LOG` tracking, and clipboard attachments (`--clip`).
* **Editor Integration APIs**: Commands such as [`capture-parse`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_parse.rs), [`capture-complete`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_complete.rs), [`capture-sections`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_sections.rs), [`capture-targets`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_targets.rs), and [`capture-tasks`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/capture_tasks.rs) expose live syntax analysis and completions used by external frontends (e.g. `bob-mac-capture`).

### 2. Task Lifecycle & Maintenance
* **[`bob task-status-hooks`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/task_status_hooks.rs)**: Reconciles task block ranks, Pomodoro task links, and derived `Blocked` states across vault tasks.
* **[`bob move-done-tasks`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/collect_done.rs)**: Archives completed and canceled task blocks into monthly/yearly archive notes and repairs task block links.

### 3. Projects & Vault Querying
* **[`bob projects`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/projects.rs)**: Inspects project lifecycle states, validates frontmatter metadata, and syncs project task statuses with vault indices.
* **[`bob query`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/dataview.rs)**: Headless Dataview and Tasks query engine powered by an embedded JavaScript runtime (`rquickjs`).

### 4. PDF Annotation & Plugin Management
* **[`bob highlights`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/highlights_ref)**: Synchronizes Highlights app PDF annotations from macOS SQLite storage and `.plist` metadata into structured reference notes.
* **[`bob plugins`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/plugins.rs)**: Deploys and manages custom Obsidian plugins from the linked `bob-plugins` repository into the active vault.

### 5. Pomodoro, Status Lines, & Synchronization
* **[`bob pomodoro`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/pomodoro.rs)** & **[`bob tmux-pomodoro`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/bin/tmux_bob_pomodoro.rs)**: Manages Pomodoro cycle states and formats active status indicators for tmux status bars.
* **[`bob notify`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/notify.rs)**: Triggers desktop alerts when Pomodoros complete.
* **[`bob nightly`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/nightly.rs)** & **[`bob bulk-git-commit`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/src/native/sync.rs)**: Runs nightly automated maintenance passes, Obsidian sync, and automated Git commits/pushes.

---

## Tech Stack & Architecture

* **Language & Edition**: Rust 2024 Edition ([`Cargo.toml`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml))
* **Core Dependencies**:
  * [`clap`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L21): Command-line argument parsing and subcommand routing.
  * [`rquickjs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L26): QuickJS engine for headless evaluation of Obsidian Dataview JS queries.
  * [`fs2`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L22): Advisory file locking for concurrency-safe vault mutations.
  * [`rusqlite`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L35) & [`plist`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L34): macOS Highlights database and preference access.
  * [`lopdf`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/Cargo.toml#L24): PDF parsing.
* **Ecosystem Integration**: Coordinates with [`bob-mac-capture`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/AGENTS.md#L30) (native macOS menu-bar UI), [`bob-plugins`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/AGENTS.md#L24) (monorepo of custom Obsidian plugins), and tmux.
* **Development Workflow**: Managed with [`justfile`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/justfile) targets (`just fmt`, `just lint`, `just test`, `just install-smoke`).
