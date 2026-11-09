# Chat History - ace-run (research.3w.gem)

- **TIMESTAMP:** 2026-11-09 09:41:39 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3w.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_092439.md`

## Prompt

%id(gem, clan=research.3w)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3w.cdx`, `research.3w.cld`, `research.3w.grk`, `research.3w.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to improve the way that we handle done notes with the goal of fixing any
existing bugs, making their management more reliable and intuitive, and making other
improvements where possible and desirable (think hard about what improvements we could
make that I would most likely find useful). I think we use `done/<name>_done.md` files
currently, which works OK I guess. I'm just curious how other systems handle this and
whether there is a better way to approach this problem.

Can you do some research with the goal of helping me with this? End your analysis with a
recommended set of changes that you think I should consider making (or recommend no
changes). 
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

# Research Report: Architecture, Comparative Analysis, and Redesign Proposals for Bob Done Notes

The independent research report has been written, verified, and registered as a durable artifact snapshot.

- **Report Path:** [`done_notes_architecture_and_redesign__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202611/done_notes_architecture_and_redesign__gem.md)
- **Artifact Ref:** `file:explicit:29c264e1646542edbe7d0892`
- **Artifact Label:** `research:202611/done_notes_architecture_and_redesign__gem.md`

---

## Executive Summary of Findings

In the Bob ecosystem, completed tasks are moved from active notes into paired archive notes under `done/<name>_done.md` (e.g., `sase.md` $\rightarrow$ `done/sase_done.md`) via [`bob task archive`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/mod.rs#L79-L109) (formerly `collect-done`), executed during nightly maintenance ([`bob nightly`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/nightly.rs#L145-L177)).

While this offloading mechanism prevents active notes from ballooning, an audit of the `bob-cli` codebase, `bob-plugins`, and the live `~/bob` vault identified **critical correctness bugs, architectural fragilities, and workflow friction points**:

### 1. Concrete Bugs & Failure Modes Identified in `bob-cli`
1. **The Zombie Task Bug ([`task_block_end`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/transform.rs#L228-L260)):**
   When extracting a completed parent task (`- [x] Parent #task`), the block scanner treats *all* indented sub-bullets as part of the parent's payload. If an active, uncompleted task (`- [ ] Child #task`) is nested underneath, it is stripped from the active note and moved to `done/`. Because review walks ([`bob review`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/runner.rs)) and agenda views skip `done/`, open child tasks become invisible "zombie" tasks.
2. **Note Rename & Move Desynchronization ([`source_relative_path_from_archive`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/link_repair.rs#L412-L426)):**
   Archive pairing relies on naive path string-stripping (`strip_prefix("done")` and `strip_suffix("_done")`). When a user renames `projects/Alpha.md` to `projects/Bravo.md` in Obsidian, the `parent:` frontmatter in `done/projects/Alpha_done.md` updates to `[[projects/Bravo]]`, but the archive file itself is not renamed. The archive planner detects a mismatch with the filename-derived path, silently skips link repairs, and subsequently spawns a duplicate, disconnected archive file (`done/projects/Bravo_done.md`).
3. **Sub-Threshold Stagnation in Finite Projects ([`build_collection_plan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/plan.rs#L229-L277)):**
   The hardcoded threshold of 10 tasks (`--threshold 10`) works for high-frequency area hubs (`gtd_daily.md`, `sase.md`, `bob.md`), but fails small GTD projects. A completed 4-task project note is never archived during `bob nightly` because $4 < 10$. Its finished tasks linger in `projects/` indefinitely unless manually flushed via `bob task archive -t 1`.
4. **Strict One-Way Valve with No Restore Path ([`task_move::plan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/task_move/plan.rs#L500-L506)):**
   [`bob task move`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/task_move/mod.rs) hard-refuses any operation where the source or destination is under `done/` (`ArchivePath` error). If a task was archived by accident, there is no CLI command to restore it.
5. **Loss of Hierarchy & Chronology in Archives ([`archive.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/archive.rs#L263-L275)):**
   Archived tasks are concatenated at the end of `_done.md` as an undifferentiated list. Section provenance (e.g., milestones, drawers) is erased, and tasks without `[completion:: ...]` fields lose all temporal context.
6. **Double Identity & Link Churn Toll:**
   Rewriting links from `[[note#^id]]` to `[[done/note_done#^id]]` creates substantial Git churn. As documented in bead `bob-cli-gs`, downstream tools (such as [`bob periods brief`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/periods/brief.rs)) previously suffered attribution bugs when trying to reconcile time against active versus archived identities.

---

## Comparative System Insights

- **Emacs Org-Mode (`org-archive`):** Supports archiving to in-file subtrees (`* Archive :ARCHIVE:`), preserving link anchors without rewriting file paths. Org-mode appends origin metadata properties (`:ARCHIVE_TIME:`, `:ARCHIVE_FILE:`, `:ARCHIVE_CATEGORY:`).
- **Obsidian Community (Task Archiver):** Favors in-place archiving beneath an `## Archive` section at EOF. Eliminates link breakage, halves vault note count, and avoids Obsidian unpathed wikilink ambiguity warnings.
- **Things 3:** Distinguishes **Areas** (permanent containers that log tasks to a date-grouped Logbook) from **Projects** (finite initiatives that move to the Logbook as whole completed containers).
- **PARA Framework:** When a project completes, the entire container note moves to `archive/projects/<name>.md`. Projects are never shredded into active husks and separate archive notes.

---

## Recommended Set of Changes

### Phase 1: High-Priority Safety & Correctness (Immediate)
1. **Guard [`task_block_end`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/transform.rs#L228-L260):** Do not extract indented sub-bullets that contain open checklists (`- [ ]`, `- [/]`, `- [?]`), preventing active tasks from being swept into `done/`.
2. **Frontmatter-Aware Archive Resolution:** Enhance [`archived_block_targets`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/link_repair.rs#L289-L352) to resolve pairs via `parent:` and `done_tasks:` frontmatter rather than string manipulation, ensuring resilience across note renames.
3. **Terminal Project Auto-Flushing:** In [`build_collection_plan`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/plan.rs#L229-L277), check if a note is a terminal project ([`TargetProjectStatus::Done`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/projects/model.rs#L190-L203)); if so, lower the archive threshold to `0` during `bob nightly`.
4. **Implement `bob task restore`:** Allow [`bob task move`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/task_move/mod.rs) to accept sources in `done/` when moving to an active note, automating reverse link repair.
5. **Auto-Reconcile Status Chips Post-Archive:** Ensure [`task_status_groups`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/task_status_groups/mod.rs) chips (`🟢 N done/canceled`) are recomputed immediately after a manual run of `bob task archive`.

### Phase 2: Structural & Ergonomic Improvements (Short-to-Medium Term)
1. **Date-Partitioned Append Headers:** In [`append_archive_blocks`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/archive.rs#L263-L275), insert a `## Archived YYYY-MM-DD` heading before each batch of moved tasks to preserve chronological structure in `_done.md` notes.
2. **First-Class Project Archiving (`bob project archive`):** Add a command that moves the entire project file (`projects/X.md` $\rightarrow$ `archive/projects/X.md`), merging any existing `_done.md` tasks into an in-file `## Archive` section.
3. **Per-Note Threshold Overrides:** Allow notes to declare `archive_threshold: N` in YAML frontmatter to accommodate both high-volume inboxes and small milestone trackers.

### Phase 3: Architectural Consolidation (Strategic)
1. **Canonical Link Target Aliasing:** Teach vault link resolvers ([`NoteIndex`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/collect_done/link_repair.rs#L28-L94) and [`vault_links`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/src/native/vault_links.rs)) to treat `[[note#^id]]` and `[[done/note_done#^id]]` as identical locators, eliminating downstream link-repair fragility.
2. **Time-Partitioned Inbox Logbooks:** Route generic inbox completions (`mac_inbox.md`, `gkeep_inbox.md`) into shared monthly logs (`done/inbox/YYYY-MM_done.md`) to prevent monolithic, multi-thousand-line single files.
