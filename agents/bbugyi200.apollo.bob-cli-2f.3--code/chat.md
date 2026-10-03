# Chat History - ace-run (bob-cli-2f.3--code)

- **TIMESTAMP:** 2026-09-28 18:05:10 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-2f.3--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202609/gh_bobs_org__bob_cli-ace_run-bob_cli_2f_3__plan-260928_164943.md`
- **2. --code** — `~/.sase/chats/202609/gh_bobs_org__bob_cli-ace_run-bob_cli_2f_3__code-260928_164943.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202609/split_capture_language.md

The above plan has been reviewed and approved. Implement it now.


## Response

Split `src/native/capture_language.rs` (11,615 lines, 163 tests) into focused modules, preserving behavior and `native::capture_language` paths.

New layout in [src/native/capture_language](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/src/native/capture_language):

- `mod.rs` (80 lines, root docs + re-exports, test-only gates)
- `model.rs`, `draft.rs`, `item.rs`, `line.rs`, `tokens.rs` (1,037), `markers.rs`, `editor_model.rs`, `editor_parse.rs` (1,008), `editor_pomodoro.rs`, `editor_classify.rs`, `completion.rs`, `rewrite.rs` — all ≤1,500
- `tests/mod.rs` (helpers) + `editor_spans.rs`, `editor_modes.rs` (1,037), `grammar.rs` (1,336), `completion.rs`, `draft.rs`, `globals.rs`, `rewrite.rs` — all ≤1,500

Used `git mv` to `mod.rs`, `pub(super)` for sibling-only items, root re-exports for existing `pub(crate)` caller paths. No logic or assertion edits, only moves + `cargo fmt`.

Verified:
- `cargo fmt --check` clean
- `cargo test --lib capture_language`: 163 passed (baseline 163)
- `cargo test` full: 1,139 lib + 515 cli + rest, all pass
- `cargo clippy --lib`: no new `capture_language` warnings
- `sase bead epic-symbols bob-cli-2f.3`: no remaining symbols

Note: `cargo clippy --all-targets` fails on unrelated clean-base `overly_complex_bool_expr` in `tests/cli/capture/pomodoro_name.rs:808`; recorded as `PROPOSED FOLLOW-UP` on `bob-cli-2f.3`.
