# Chat History - ace-run (bob-cli-q4.land--code)

- **TIMESTAMP:** 2026-11-26 07:00:03 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-q4.land--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_q4_land__plan-261125_085301.md`
- **2. --code** — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_q4_land__code-261125_085301.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202611/q4_land_settle_drift.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved `q4_land_settle_drift` plan and closed epic `bob-cli-q4`.

**What changed**
- Forwarded every capture line coordinate through the settle line map with block-ID fallback, plus inbox-route move forwarding for pulled/completed rows ([plan.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture/plan.rs)). Fixes `moved.line`, `new_line`, `project_note` moved/successor lines, offer closes, type agreement, and day-file link lines. `open_notes` and jump now land post-settle.
- Settled `bob ref today` like capture ([existing_task_link.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/capture/existing_task_link.rs)); dry-run reports settled bytes.
- Removed stale `allow(dead_code)` on `SettleContext` ([task_settle.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/src/native/task_settle.rs)).
- Rebased stale expectations: [task_theme_writes.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/cli/capture/task_theme_writes.rs), [sync.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/cli/task_status_hooks/sync.rs) (badge already `2 open`, reconcile plans nothing for `alpha.md`), [project_note.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/cli/capture/project_note.rs) (settled order + badge), [project_note_offer.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/cli/capture/project_note_offer.rs) (distinct lines, not order), note-pull fixtures via `generate.py` ([preview/picked/routed/stdout](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/fixtures/note_pull/)).
- Added `ref_today_leaves_nothing_note_local` to [settle_acceptance.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/tests/cli/settle_acceptance.rs).
- Docs: settle section in [capture.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/capture.md), writer list in [task-status-hooks.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/task-status-hooks.md), settle note in [ref.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/docs/ref.md). `just docs-gen` and `just docs-check` pass (447 passed).

**Verification observed**
- Targeted 17: `cargo test --test cli -- capture::inbox_route capture::note_pull capture::project_note capture::project_note_offer capture::task_theme_writes ref_library::today task_status_hooks::sync` → 169 passed, 0 failed.
- Broader: `settle_acceptance ref_library capture` → 2363 passed, 33 failed (all drawer/complete-drawer, pre-existing).
- Full CLI: 4215 passed, 38 failed — all drawer/completion/`task_drawer_rename`, none in the 17 areas. The 17 settle-drift nodes are gone.
- `cargo fmt --check` clean, `just lint` clean, `task_settle` lib tests pass (4/4).

**Closeout**
- `sase bead epic-symbols bob-cli-q4`: none.
- Closed `bob-cli-q4` with verification note; set `status: done` in `202611/better_o_gesture_settle.md` (plans sidecar).
- `just symvision`: no such recipe in the justfile.
- Submitted via `/sase_final`: primary `fix(capture)!` with `BREAKING CHANGE` footer covering settled writers and post-settle JSON lines plus `LINKED FROM`; plans sidecar chore commit. Host commits after turn end.
