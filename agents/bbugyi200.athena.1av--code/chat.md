# Chat History - ace-run (1av--code)

- **TIMESTAMP:** 2026-11-10 08:38:04 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 1av--code

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202611/dot_alias_prefers_dependency_once_routed.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- routed_scope = any_route (planner default: any_route). Implement the "routed_scope = any_route" branch; ignore "routed_scope = block_id". Context: "Should a bare `@route` or `@route#section` also make a spaced `.` prefer `&`, not just `@route:id`/`^id`/`+id`?".
- memory_glossary_capture_alias = yes 🧠. Memory edits are authorized for glossary:capture-alias only. Context: "Should the glossary capture-alias strand be updated for the new spaced `.` precedence?".
No other memory note may be edited.
Implement only the branches selected above.
%macros_enabled:true


## Response

Implemented the approved routed-dot plan (`any_route` branch; glossary `capture-alias` memory update only).

What changed:
- [rewrite.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_language/rewrite.rs): added `alias_item_is_routed` (pre-key draft minus the typed `.`, item lookup by `start`, `local_destination_markers` non-empty). Spaced `.` now tries `&` first once the item is routed, falling back to `@`; otherwise `@` first. Block-ID `^` stays first. Doc comments updated.
- Tests: new `rewrite_draft_dot_prefers_dependency_once_item_is_routed` and `rewrite_draft_dot_keeps_route_alias_when_item_is_not_routed_or_and_cannot_open` in [tests/rewrite.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_language/tests/rewrite.rs); new `Buy milk @foo:bar &` positive row and `Buy milk @foo:bar @` negative row in [tests/alias_tip.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_language/tests/alias_tip.rs); new `capture_rewrite_json_dot_prefers_dependency_once_routed` plus tip-table row in [tests/cli/capture/rewrite.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/tests/cli/capture/rewrite.rs).
- Help/docs: [capture_rewrite.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/capture_rewrite.rs) help and [docs/capture.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/docs/capture.md) gained the routed-first rule with the `Buy milk @foo:bar .` example; `just docs-gen` regenerated [capture-rewrite.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/docs/reference/cli/capture-rewrite.md) and [glossary.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/docs/reference/glossary.md) (diff is only the new sentences, nothing hand-edited).
- Memory: [glossary/capture-alias.md](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/memory/glossary/capture-alias.md) spaced-`.` bullets rewritten; `sase memory init` run (commit deferred to host finalizer).
- Mac Capture docs-only: `relationship-pickers.md`, `keyboard.md`, `capture-panel.md` corrected; no Swift changes.

Verification observed:
- `cargo test --lib` rewrite + alias-tip suites green; full `just test` (workspace) exit 0; `just fmt` and `just lint` exit 0.
- Probes: `Buy milk @foo:bar .` → `&` (dependency), `Buy milk @foo .` → `&`, `Buy milk .` → `@`, `@a+x > .` → `@`, `Create task < @cash:line .` → `@`, `@errands.` → `^`, blank-line-separated second item → `@`, tip for `Buy milk @foo:bar &` is `dependency`/`once routed` and `Buy milk @foo:bar @` gives no tip.
- `just docs-check` fails identically on the untouched base (5 pre-existing word-budget errors in `json-outputs.md` and `mac-capture/*` reference pages; verified via stash on both repos), so not a regression.
