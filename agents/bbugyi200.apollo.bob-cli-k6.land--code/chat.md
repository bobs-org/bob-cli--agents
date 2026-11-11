# Chat History - ace-run (bob-cli-k6.land--code)

- **TIMESTAMP:** 2026-11-11 10:52:17 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-k6.land--code

## Linked Chats

- 1. --plan — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_k6_land__plan-261111_075501.md`
- **2. --code** — `~/.sase/chats/202611/gh_bobs_org__bob_cli-ace_run-bob_cli_k6_land__code-261111_075501.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli
@plan:202611/svg_image_landing_repairs.md

The above plan has been reviewed and approved. Implement it now.


## Response

Implemented the approved `202611/svg_image_landing_repairs.md` tale and landed `bob-cli-k6`.

Changed:
- [diagrams.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/highlights_ref/diagrams.rs): replaced fragile `] (` / `]:` / `src=` prescan with permissive case-insensitive `.svg` marker scan; added `prescan_covers_all_pandoc_svg_image_forms`, `prepare_reaches_adapter_for_all_pandoc_svg_forms` (angle-space, plain, reference with real space filename, adapter request contains source bytes + `"kind":"svg"`), `collect_preserves_document_order_across_kinds` (Mermaid-first, SVG-first, alternating nested lists/quotes), `collect_budget_keeps_document_order_not_type_order` (200 Mermaids + late SVG).
- [diagrams_collect.lua](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/highlights_ref/diagrams_collect.lua): added `traverse = "topdown"` for document order.
- [diagram_render.py](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/scripts/web_clip/diagram_render.py): sanitize `[root, ...querySelectorAll('*')]`, reject root `<script>`.
- [web_clip_adapter.py](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/scripts/web_clip/web_clip_adapter.py): browser-backed SVG sanitization regression inspects inserted root before print (root/down `on*`, `script` removed, mouseover cannot set sentinel), verifies PDF, foreignObject `VectorLabel`, no network routes.
- [create.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/src/native/highlights_ref/create.rs): `overwrite_markdown` and `-M` plain `overwrite_vault_note` now emit `image_guard` + `diagram_pass` exactly once after successful commit; snapshot path unchanged.
- [overwrite_local.rs](/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/tests/cli/highlights/overwrite_local.rs): new CLI `markdown_overwrite_reports_svg_{vector_success,sibling_fallback,placeholder_warning}` with source-directory resolution assertions.
- Plans sidecar `202611/ref_create_svg_images.md`: `status: wip` → `done`.

Verified:
- `cargo test --lib -- native::highlights_ref::diagrams::tests`: 22 passed.
- `cargo test --test cli -- highlights::overwrite_local::markdown_overwrite_reports_svg`: 3 passed; existing `vault_note_same_day_overwrite_plain_markdown`, 4 markdown overwrite, 3 SVG ordinary-create tests pass.
- `just check-web-clip-adapter`: `ok` (includes new SVG sanitization checks).
- `just docs-check`: fails only on the 5 known budgets (6036, 6177, 6060, 6186, 6149), independent of epic.
- `just check`: blocked by pre-existing `records/context.rs` clippy `needless_borrow` in unrelated `f7332f58`; reproduces on clean tree, no SVG integration needed.
- `sase bead epic-symbols bob-cli-k6`: empty; `git log 7eb82440..HEAD`: only `f7332f58` records work; no `symvision` recipe; epic closed via `sase bead close bob-cli-k6`.
