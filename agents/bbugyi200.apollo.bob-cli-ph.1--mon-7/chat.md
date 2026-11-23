# Chat History - ace-run (bob-cli-ph.1--mon-7)

- **TIMESTAMP:** 2026-11-23 10:28:04 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-ph.1--mon-7

## Prompt

sase monitor start --command 'set -e; cargo test --lib capture_drawers; cargo test --lib task_block_layout; cargo test --lib task_split; cargo test --lib task_text_escape; cargo test --lib gcal::description::bullets; cargo test --lib gmail::body::inert; cargo test --test cli drawer; cargo test --test cli req; cargo test --test cli clip; cargo test --test cli docs_reference; uv run --project tools/docs pytest tools/docs/tests/test_contracts.py; just check; just docs-check' --reason 'Run the full drawer-contract regression and repository gates after correcting stale clipboard and help expectations'

## Response

sase tool run 9f02531858dacf876f1f1f88448cde29
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
   Compiling cfg-if v1.0.4
   Compiling siphasher v1.0.4
   Compiling typenum v1.20.1
   Compiling libc v0.2.186
   Compiling stable_deref_trait v1.2.1
   Compiling version_check v0.9.5
   Compiling smallvec v1.15.2
   Compiling fastrand v2.5.0
   Compiling memchr v2.8.1
   Compiling bitflags v2.12.1
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling foldhash v0.2.0
   Compiling autocfg v1.5.1
   Compiling rand_core v0.10.1
   Compiling serde_core v1.0.228
   Compiling phf_shared v0.14.0
   Compiling parking_lot_core v0.9.12
   Compiling writeable v0.6.4
   Compiling litemap v0.8.3
   Compiling cc v1.2.63
   Compiling new_debug_unreachable v1.0.6
   Compiling getrandom v0.4.2
   Compiling scopeguard v1.2.0
   Compiling generic-array v0.14.7
   Compiling icu_normalizer_data v2.3.0
   Compiling lock_api v0.4.14
   Compiling itoa v1.0.18
   Compiling hashbrown v0.17.1
   Compiling simd-adler32 v0.3.9
   Compiling phf_generator v0.14.0
   Compiling num-traits v0.2.19
   Compiling crc32fast v1.5.0
   Compiling utf8_iter v1.0.4
   Compiling icu_properties_data v2.3.0
   Compiling precomputed-hash v0.1.1
   Compiling phf_codegen v0.14.0
   Compiling serde v1.0.228
   Compiling utf8parse v0.2.2
   Compiling log v0.4.30
   Compiling adler2 v2.0.1
   Compiling rustix v1.1.5
   Compiling cpufeatures v0.3.0
   Compiling anstyle-parse v1.0.0
   Compiling miniz_oxide v0.8.9
   Compiling anstyle v1.0.14
   Compiling tinyvec_macros v0.1.1
   Compiling linux-raw-sys v0.12.1
   Compiling is_terminal_polyfill v1.70.2
   Compiling colorchoice v1.0.5
   Compiling vcpkg v0.2.15
   Compiling anstyle-query v1.1.5
   Compiling dtoa v1.0.11
   Compiling pkg-config v0.3.33
   Compiling anstream v1.0.0
   Compiling tinyvec v1.11.0
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling string_cache_codegen v0.11.2
   Compiling hybrid-array v0.4.12
   Compiling indexmap v2.14.0
   Compiling flate2 v1.1.9
   Compiling dtoa-short v0.3.5
   Compiling chacha20 v0.10.2
   Compiling tendril v0.5.1
   Compiling regex-syntax v0.8.10
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling thiserror v2.0.18
   Compiling inout v0.1.4
   Compiling digest v0.10.7
   Compiling unicode-width v0.2.3
   Compiling cpufeatures v0.2.17
   Compiling web_atoms v0.3.0
   Compiling rquickjs-sys v0.12.1
   Compiling parking_lot v0.12.5
   Compiling libsqlite3-sys v0.38.1
   Compiling cipher v0.4.4
   Compiling zmij v1.0.21
   Compiling once_cell v1.21.4
   Compiling clap_lex v1.1.0
   Compiling strsim v0.11.1
   Compiling string_cache v0.11.0
   Compiling weezl v0.1.12
   Compiling clap_builder v4.6.7
   Compiling getopts v0.2.24
   Compiling rand v0.10.1
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling wait-timeout v0.2.1
   Compiling unicode-normalization v0.1.25
   Compiling aho-corasick v1.1.4
   Compiling nom v8.0.0
   Compiling fdeflate v0.3.7
   Compiling phf_shared v0.12.1
   Compiling servo_arc v0.5.0
   Compiling bit-vec v0.10.2
   Compiling iana-time-zone v0.1.65
   Compiling powerfmt v0.2.0
   Compiling pxfm v0.1.30
   Compiling fnv v1.0.7
   Compiling quick-error v1.2.3
   Compiling zune-core v0.5.3
   Compiling tempfile v3.27.0
   Compiling time-core v0.1.9
   Compiling unicode-properties v0.1.4
   Compiling byteorder-lite v0.1.0
   Compiling unicode-bidi v0.3.18
   Compiling const-oid v0.10.2
   Compiling deranged v0.5.8
   Compiling chrono-tz v0.10.4
   Compiling quick-error v2.0.1
   Compiling percent-encoding v2.3.2
   Compiling bytecount v0.6.9
   Compiling pulldown-cmark v0.13.6
   Compiling num-conv v0.2.2
   Compiling rustc-hash v2.1.3
   Compiling color_quant v1.1.0
   Compiling serde_json v1.0.150
   Compiling stringprep v0.1.5
   Compiling form_urlencoded v1.2.2
   Compiling gif v0.14.2
   Compiling digest v0.11.3
   Compiling image-webp v0.2.4
   Compiling regex-automata v0.4.14
   Compiling zune-jpeg v0.5.15
   Compiling rusty-fork v0.3.1
   Compiling clap v4.6.7
   Compiling bit-set v0.11.1
   Compiling png v0.18.1
   Compiling phf v0.12.1
   Compiling aes v0.8.4
   Compiling cbc v0.1.2
   Compiling ecb v0.1.2
   Compiling synstructure v0.14.0
   Compiling time v0.3.53
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling hashlink v0.12.1
   Compiling quick-xml v0.41.0
   Compiling rand_xorshift v0.5.0
   Compiling encoding_rs v0.8.35
   Compiling rangemap v1.7.1
   Compiling base64 v0.22.1
   Compiling fallible-streaming-iterator v0.1.9
   Compiling unarray v0.1.4
   Compiling ttf-parser v0.25.1
   Compiling unicase v2.10.0
   Compiling unsafe-libyaml v0.2.11
   Compiling core_detect v1.0.0
   Compiling is_executable v1.0.6
   Compiling nom_locate v5.0.0
   Compiling bytemuck v1.25.2
   Compiling pulldown-cmark-escape v0.11.0
   Compiling ego-tree v0.11.1
   Compiling ryu v1.0.23
   Compiling moxcms v0.8.1
   Compiling fallible-iterator v0.3.0
   Compiling clap_complete v4.6.11
   Compiling proptest v1.12.0
   Compiling regex v1.12.3
   Compiling sha2 v0.11.0
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling phf_macros v0.14.0
   Compiling serde_derive v1.0.228
   Compiling derive_more-impl v2.1.1
   Compiling cssparser-macros v0.7.1
   Compiling thiserror-impl v2.0.18
   Compiling fs2 v0.4.3
   Compiling roxmltree v0.21.2
   Compiling similar v2.7.0
   Compiling glob v0.3.4
   Compiling zerofrom v0.1.8
   Compiling hex v0.4.3
   Compiling phf v0.14.0
   Compiling yoke v0.8.3
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/crates/bob-obsidian-assets)
   Compiling cssparser v0.38.0
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling derive_more v2.1.1
   Compiling selectors v0.41.0
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_collections v2.3.0
   Compiling icu_locale_core v2.3.0
   Compiling lopdf v0.40.0
   Compiling markup5ever v0.40.0
   Compiling html5ever v0.40.1
   Compiling image v0.25.10
   Compiling scraper v0.29.0
   Compiling icu_provider v2.3.1
   Compiling chrono v0.4.44
   Compiling plist v1.10.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 4m 52s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 33 tests
test native::capture_drawers::tests::bold_drawer_titles_keep_authored_bytes_and_unicode_keys ... ok
test native::capture_drawers::tests::build_cli_renders_without_panicking ... ok
test native::capture_drawers::tests::catalog_search_ranks_prefix_tier_first_and_skips_excluded_keys ... ok
test native::capture_drawers::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_drawers::tests::drawer_heading_mapping_is_lossless_and_creation_stays_nonempty ... ok
test native::capture_drawers::tests::checkboxed_all_caps_children_are_not_drawers ... ok
test native::capture_drawers::tests::grandchild_is_not_a_direct_child_drawer ... ok
test native::capture_drawers::tests::near_duplicate_suggests_quoted_title_when_slug_is_invalid ... ok
test native::capture_drawers::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_drawers::tests::ensure_drawer_creates_project_h2_sibling_and_rescans_it ... ok
test native::capture_drawers::tests::last_entry_text_is_the_direct_entry_a_capture_lands_after ... ok
test native::capture_drawers::tests::ensure_drawer_creates_task_drawer_then_rescans_it ... ok
test native::capture_drawers::tests::query_matches_a_key_or_slug_by_prefix_before_substring ... ok
test native::capture_drawers::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_drawers::tests::reserved_refusals_name_the_reserved_key ... ok
test native::capture_drawers::tests::contextual_reader_filters_false_drawers_and_reports_byte_ranges ... ok
test native::capture_drawers::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_drawers::tests::sentence_punctuation_drawer_titles_qualify ... ok
test native::capture_drawers::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_drawers::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_drawers::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_drawers::tests::empty_drawer_bullet_still_qualifies ... ok
test native::capture_drawers::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_drawers::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_drawers::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_drawers::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_drawers::tests::managed_logs_are_never_drawers_plain_titles_are ... ok
test native::capture_drawers::tests::title_whitelist_edges ... ok
test native::capture_drawers::tests::drawer_conformance_vectors_match_reader_and_mapping ... ok
test native::capture_drawers::tests::catalog_v3_rebuilds_v2_and_keeps_marker_provenance_per_spelling ... ok
test native::capture_drawers::tests::resolved_task_with_no_drawers_is_a_successful_empty_list ... ok
test native::capture_drawers::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_drawers::tests::lists_drawers_in_document_order_for_a_block_id ... ok

test result: ok. 33 passed; 0 failed; 0 ignored; 0 measured; 7957 filtered out; finished in 0.02s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.25s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 15 tests
test native::task_block_layout::tests::zones_name_every_task_child_kind ... ok
test native::task_block_layout::tests::canonicalize_new_req_block_leaves_zero_req_and_closed_blocks ... ok
test native::task_block_layout::tests::a_note_without_a_final_newline_keeps_that_state ... ok
test native::task_block_layout::tests::a_created_notes_drawer_lands_first_among_the_drawers ... ok
test native::task_block_layout::tests::log_and_cancel_log_writers_land_in_their_zones ... ok
test native::task_block_layout::tests::managed_link_writers_land_inside_the_managed_zone ... ok
test native::task_block_layout::tests::notes_home_matches_bold_notes_by_key_and_tidy_reuses_its_header ... ok
test native::task_block_layout::tests::vector_ids_are_unique_and_sequenced ... ok
test native::task_block_layout::tests::layout_note_homes_match_vectors ... ok
test native::task_block_layout::tests::layout_violations_match_vectors ... ok
test native::task_block_layout::tests::canonicalize_new_req_block_files_notes_and_keeps_req_subtrees ... ok
test native::task_block_layout::tests::layout_slots_match_vectors ... ok
test native::task_block_layout::tests::layout_tidy_matches_vectors ... ok
test native::task_block_layout::tests::a_tidied_block_has_no_violations_and_tidies_to_none ... ok
test native::task_block_layout::tests::req_writers_match_vectors ... ok

test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 7975 filtered out; finished in 0.05s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.22s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::task_split::tests::req_candidates_list_every_depth_with_their_state ... ok
test native::task_split::tests::split_same_note_fabricates_no_retargets ... ok
test native::task_split::tests::split_minted_anchor_still_qualifies_pathless_stayed_anchor_links ... ok
test native::task_split::tests::split_repairs_whole_payload_with_multiline_fence_and_comment_context ... ok
test native::task_split::tests::carry_req_by_row_key_moves_the_branch_and_maps_descendants ... ok
test native::task_split::tests::split_repairs_cross_note_anchors_in_owned_fields_and_payload ... ok
test native::task_split::tests::carry_req_by_line_digest_and_its_refusals ... ok
test native::task_split::tests::split_conformance_vectors_match_byte_for_byte ... ok

test result: ok. 8 passed; 0 failed; 0 ignored; 0 measured; 7982 filtered out; finished in 0.56s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.22s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::task_text_escape::tests::escape_task_text_leaves_intended_markup_alone ... ok
test native::task_text_escape::tests::note_inline_disarms_organizer_escapes_first ... ok
test native::task_text_escape::tests::note_inline_neutralizes_code_spans_queries_and_math ... ok
test native::task_text_escape::tests::note_inline_neutralizes_refs_tags_and_fields ... ok
test native::task_text_escape::tests::note_escapers_leave_ordinary_prose_alone ... ok
test native::task_text_escape::tests::note_text_adds_line_start_guards ... ok
test native::task_text_escape::tests::child_text_escapes_a_bullet_start_checkbox ... ok
test native::task_text_escape::tests::child_text_defuses_legacy_and_bold_drawer_headers_idempotently ... ok

test result: ok. 8 passed; 0 failed; 0 ignored; 0 measured; 7982 filtered out; finished in 0.01s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.21s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::gcal::description::bullets::tests::markdown_destination_encoding_covers_delimiters ... ok
test native::gcal::description::bullets::tests::hash_and_materialization_follow_depth_and_body ... ok
test native::gcal::description::bullets::tests::punctuated_drawer_shaped_lines_are_defused ... ok
test native::gcal::description::bullets::tests::note_prose_is_exempt_from_the_cap ... ok
test native::gcal::description::bullets::tests::bullet_vectors ... ok
test native::gcal::description::bullets::tests::oversize_input_keeps_reasons_above_the_fallback ... ok
test native::gcal::description::bullets::tests::oversize_input_uses_one_calendar_fallback ... ok
test native::gcal::description::bullets::tests::hostile_bullets_are_isolated_from_bob_scanners ... ok

test result: ok. 8 passed; 0 failed; 0 ignored; 0 measured; 7982 filtered out; finished in 0.08s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.21s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/bob_cli-133a49cac731dd3a)

running 19 tests
test native::gmail::body::inert::tests::checkbox_fragments_never_survive_as_requirements ... ok
test native::gmail::body::inert::tests::verified_embed_accepts_only_writer_paths ... ok
test native::gmail::body::inert::tests::verified_wikilink_mints_exact_resized_embed_for_writer_paths_only ... ok
test native::gmail::body::inert::tests::whole_bold_and_legacy_list_items_are_defused_as_imported_children ... ok
test native::gmail::body::inert::tests::structured_inline_text_keeps_spaces_around_renderer_formatting ... ok
test native::gmail::body::inert::tests::safe_url_refuses_wikilinks_but_keeps_usable_urls ... ok
test native::gmail::body::inert::tests::remote_images_never_become_image_syntax ... ok
test native::gmail::body::inert::tests::fenced_code_keeps_text_info_and_sizes_delimiters ... ok
test native::gmail::body::inert::tests::inline_queries_are_broken ... ok
test native::gmail::body::inert::tests::bang_before_trusted_link_never_forms_remote_image ... ok
test native::gmail::body::inert::tests::split_colon_runs_cannot_reform_bare_or_bracketed_fields ... ok
test native::gmail::body::inert::tests::readable_text_survives_untouched ... ok
test native::gmail::body::inert::tests::simulated_card_holds_no_sender_structure ... ok
test native::gmail::body::inert::tests::split_percent_math_and_backslash_edges_stay_inert ... ok
test native::gmail::body::inert::tests::link_policy_allows_only_http_mailto ... ok
test native::gmail::body::inert::tests::hidden_node_boundaries_cannot_rejoin_hazards ... ok
test native::gmail::body::inert::tests::yaml_values_survive_serialization_without_active_syntax ... ok
test native::gmail::body::inert::tests::helpers_neutralize_hostile_fragments ... ok
test native::gmail::body::inert::tests::adversarial_corpus_stays_inert_and_readable ... ok

test result: ok. 19 passed; 0 failed; 0 ignored; 0 measured; 7971 filtered out; finished in 0.49s

   Compiling bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 3m 56s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/cli-1555ea48c466b133)

running 82 tests
test capture::complete_drawers::bullet_menu_human_output_shows_the_title_line_only ... ok
test capture::complete_drawers::bullet_menu_json_pins_the_target_the_bare_titles_and_the_continuation ... ok
test capture::complete_drawers::notebook_note_bullet_hash_opens_no_drawer_menu ... ok
test capture::complete_drawers::empty_drawer_menu_json_pins_groups_fields_and_the_unselected_open ... ok
test capture::complete_drawers::drawer_menu_human_output_lists_bobs_detail_and_refusals ... ok
test capture::complete_drawers::bullet_menu_continuation_depends_on_what_follows_the_token ... ok
test capture::complete_drawers::quoted_drawer_literals_decode_the_query_and_cover_the_quotes ... ok
test capture::complete_drawers::refused_rows_name_the_commits_reason ... ok
test capture::complete_transfer::transfer_drawer_destination_lists_task_drawers ... ok
test capture::complete_drawers::run_members_complete_and_bullet_menu_keeps_first_members_drawers ... ok
test capture::complete_drawers::target_run_completion_crosses_schedule_and_clipboard_tokens ... ok
test capture::complete_drawers::typed_drawer_menu_filters_groups_and_drops_the_unselected_open ... ok
test capture::complete_notebook_sections::place_menu_covers_drawer_glued_and_bullet_menus ... ok
test capture::drawer_bullets::childless_all_caps_stays_a_plain_bullet ... ok
test capture::drawer_bullets::catalog_spelling_wins_for_a_slug ... ok
test capture::complete_drawers::bullet_menu_on_new_tasks_and_project_notes_carries_the_new_target ... ok
test capture::complete_drawers::bullet_starts_that_cannot_name_a_drawer_are_empty_successes ... ok
test capture::drawer_bullets::new_task_shortcut_renders_the_all_caps_drawer ... ok
test capture::drawer_bullets::project_note_shortcut_becomes_a_section ... ok
test capture::drawer_bullets::repeated_keys_merge_in_draft_order ... ok
test capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks ... ok
test capture::complete_drawers::unresolvable_drawer_targets_return_a_diagnostic_and_no_rows ... ok
test capture::clip_notes::clip_notes_drawers_and_prj_sections ... ok
test capture::drawer_bullets::reserved_childless_and_text_refusals ... ok
test capture::drawer_bullets::same_line_note_is_not_under_task ... ok
test capture::authored::capture_drawer_authored_children_and_composition ... ok
test capture::drawer_bullets::reserved_diagnostic_copy_matches_the_refusal ... ok
test capture::note_bullets::same_line_shortcut_reports_drawer_position ... ok
test capture::note_bullets::childless_literal_matching_existing_drawer_is_refused ... ok
test capture::note_bullets::reserved_drawer_is_refused ... ok
test capture::complete_editor::capture_complete_drawer_json_covers_components_and_warnings ... ok
test capture::multi_target::a_glued_drawer_suffix_stays_local_to_its_target ... ok
test capture::multi_target::note_less_bullets_and_drawers_are_filed_to_each_member ... ok
test capture::note_bullets::glued_drawer_files_every_bullet_inside ... ok
test capture::drawer_bullets::punctuated_drawer_merges_into_the_existing_drawer ... ok
test capture::note_bullets::two_bullets_naming_one_missing_drawer_merge ... ok
test capture::prj_drawers::capture_drawers_lists_h2_sections_for_prj_parent ... ok
test capture::prj_drawers::capture_complete_prj_drawer_menu_lists_h2_sections ... ok
test capture::prj_drawers::capture_prj_drawer_promotion_round_trip ... ok
test capture::prj_drawers::capture_prj_drawer_authored_children_and_clip_nest_under_entry ... ok
test capture::note_bullets::worked_example_files_notes_drawers_json_and_human ... ok
test capture::drawer_bullets::new_project_note_structural_sections_stay_legal_everywhere ... ok
test capture::lists::capture_list_checkbox_and_drawer_positions_are_refused ... ok
test capture::reqs_new::an_authored_notes_drawer_merges_scooped_notes ... ok
test capture::prj_drawers::capture_prj_drawer_creates_missing_h2_in_title_case ... ok
test capture::reqs_new::interleaved_notes_reqs_and_drawers_canonicalize ... ok
test capture::parse::capture_parse_json_reports_drawer_and_incomplete_needs ... ok
test capture::prj_drawers::capture_prj_drawer_appends_after_section_content ... ok
test capture::reqs_existing::req_only_capture_keeps_notes_drawer_nonempty_and_existing_reqs_append ... ok
test capture::prj_drawers::capture_prj_drawer_ambiguous_and_guard_refuse_but_literal_wins ... ok
test capture::reqs_existing::implicit_notes_on_a_req_owner_reports_the_drawer ... ok
test capture::prj_drawers::capture_prj_drawer_separate_type_and_plain_child_still_work ... ok
test capture::sections::capture_drawer_managed_log_geometry ... ok
test capture::sections::capture_forced_drawer_option_errors ... ok
test capture::task_id::capture_drawers_json_and_human_list_sections ... ok
test capture::merge_in::merge_in_equivalence_covers_same_note_drawers_and_configured_labels ... ok
test capture::drawer_bullets::legal_drawer_controls_agree_across_parse_preview_and_commit ... ok
test capture::sections::capture_forced_drawer_matches_title_exactly ... ok
test capture::sections::capture_drawer_inserts_into_first_middle_and_last_sections ... ok
test completion::capture_text::drawers_complete_after_id_hash ... ok
test capture::sections::capture_drawer_prefix_vs_whole_slug_and_multiword ... ok
test help::capture_drawers_help_is_native_only ... ok
test help_options::capture_drawers_help_lists_options_alphabetically ... ok
test completion::vault::drawers_offer_exact_titles ... ok
test capture::drawer_bullets::reserved_new_task_drafts_agree_across_parse_preview_and_commit ... ok
test capture::task_id::capture_drawers_empty_and_error_paths ... ok
test capture::retype_closeout::idless_task_ref_retype_plain_and_drawer ... ok
test capture::prj_drawers::capture_prj_drawer_structural_and_reserved_refuse ... ok
test capture::transfer::transfer_merge_origins_cover_renamed_anchors_and_drawers ... ok
test capture::sections::capture_drawer_indent_units_crlf_and_dry_run ... ok
test capture::complete_drawers::accepting_a_row_makes_the_commit_agree_with_the_menu ... ok
test task_drawer_rename::bare_run_is_a_dry_run_with_an_inventory ... ok
test capture::sections::capture_drawer_errors_leave_the_note_unchanged ... ok
test task_drawer_rename::no_match_is_a_clean_report ... ok
test task_drawer_rename::invalid_requests_exit_2_before_reading_the_vault ... ok
test capture::transfer::transfer_merge_drawers_and_sections_preserve_selector_intent ... ok
test task_drawer_rename::apply_prints_a_summary_per_note ... ok
test task_drawer_rename::apply_commits_once_and_a_rerun_reports_nothing ... ok
test task_merge::merge_into_created_drawer ... ok
test task_merge::merge_into_prj_h2_drawer ... ok
test task_merge::merge_into_drawer_uses_existing_drawer ... ok
test capture::complete_drawers::accepting_a_bullet_row_makes_the_commit_agree_with_the_menu ... ok

test result: ok. 82 passed; 0 failed; 0 ignored; 0 measured; 3989 filtered out; finished in 3.30s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.53s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/cli-1555ea48c466b133)

running 125 tests
test capture::complete_links_only::source_note_requires_links_only ... ok
test capture::parse_reqs::every_problem_is_reported_not_only_the_first ... ok
test capture::parse_reqs::nested_requirements_report_req_marker_spans_with_depths ... ok
test capture::parse_reqs::human_output_lists_req_marker_spans ... ok
test capture::parse_reqs::sealed_project_notes_mark_requirements_under_task_rows_only ... ok
test capture::complete_links_only_tasks::task_links_requires_links_only ... ok
test capture::parse_reqs::ineligible_items_keep_checkboxes_as_text ... ok
test capture::parse_dependency::capture_new_task_does_not_promote_a_closed_prerequisite ... ok
test capture::parse_reqs::the_depth_bound_and_the_empty_placeholder ... ok
test capture::parse_reqs::task_lists_count_levels_after_the_shift ... ok
test capture::parse_reqs::the_same_line_form_marks_the_item_line ... ok
test capture::note_pull::np13_required_choice_matches_refusal_fixture_without_writes ... ok
test capture::record::update_required_empty_still_needs_record_value ... ok
test capture::complete_records::capture_complete_next_missing_walks_required_fields ... ok
test capture::note_bullets::notes_on_a_req_owning_task_file_into_notes ... ok
test capture::blocked_tasks::ampersand_same_note_prerequisite_below_dependent_relocates ... ok
test capture::prj_notes::first_req_scoops_a_loose_prj_note_into_notes ... ok
test capture::parse_reqs::each_refusal_reports_its_code_on_the_bullets_whole_line ... ok
test capture::req_annotations::completing_a_task_meets_its_requirements ... ok
test capture::req_annotations::existing_block_annotates_dropped_carried_excluded_and_notes ... ok
test capture::req_annotations::new_task_preview_annotates_requirement_depths ... ok
test capture::relate_existing::rx16_new_task_prints_per_prerequisite_row ... ok
test capture::record::capture_required_default_none_and_list_semantics ... ok
test capture::record::capture_update_replaces_lists_in_request_order ... ok
test capture::keep_moving::km30_require_choice_refuses_write_free ... ok
test capture::req_annotations::idle_agenda_annotates_requirement_rows ... ok
test capture::record::capture_update_empty_required_and_historical_warning ... ok
test capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks ... ok
test capture::project_note::capture_project_note_colon_move_drops_local_prerequisite_and_links ... ok
test capture::req_close::carry_plus_pull_in_on_same_req_conflicts_write_free ... ok
test capture::req_close::dual_gate_pending_reqs_demand_acknowledgement ... ok
test capture::req_close::default_met_closes_owner_and_leaves_req_bytes ... ok
test capture::req_close::human_preview_prints_requirements_first ... ok
test capture::relations_cancel::cancel_dependent_with_other_prereq_stays_blocked ... ok
test capture::req_close::dual_gate_jump_alone_is_not_acknowledgement ... ok
test capture::req_close::dry_run_uses_would_forms_and_writes_nothing ... ok
test capture::req_close::multi_owner_done_reports_each_forest ... ok
test capture::req_close::carry_creates_own_task_without_pulling_in ... ok
test capture::req_close::no_req_task_advertises_zero_pending ... ok
test capture::req_close::drop_rewrites_req_and_optional_cancel_log ... ok
test capture::relation_successors::refusal_and_require_choice_include_relation_rows ... ok
test capture::req_close::explicit_met_acknowledges_pending_reqs ... ok
test capture::req_close::later_item_still_places_a_pomodoro_close_carry ... ok
test capture::reqs_existing::failed_note_planning_rolls_back_the_req_insert_and_scoop ... ok
test capture::req_close::mixed_card_numbers_requirements_first ... ok
test capture::req_close::relation_complete_audits_source_reqs ... ok
test capture::parse_dependency::capture_does_not_promote_closed_done_or_cancelled_prerequisites ... ok
test capture::req_close::pomodoro_close_audits_linked_task_reqs ... ok
test capture::req_close::mark_all_never_selects_requirement_rows ... ok
test capture::reqs_existing::forced_task_and_task_ref_targets_write_same_line_requirements ... ok
test capture::reqs_existing::project_root_task_accepts_existing_requirement_groups ... ok
test capture::reqs_existing::first_req_scoops_only_preexisting_notes_before_planning_new_notes ... ok
test capture::reqs_existing::nested_requirements_count_at_every_depth_like_new_blocks ... ok
test capture::req_close::overlap_across_hand_ticked_intermediate_refuses_both_orders ... ok
test capture::req_close::dual_gate_none_or_explicit_verdict_acknowledges ... ok
test capture::req_close::pomodoro_close_pull_in_uses_the_closing_continuation ... ok
test capture::req_close::legacy_client_keeps_offer_numbering_and_met_default ... ok
test capture::reqs_existing::implicit_notes_on_a_req_owner_reports_the_drawer ... ok
test capture::reqs_lexical::a_deep_marker_only_row_in_a_notes_list_is_still_refused ... ok
test capture::req_close::stale_keyed_replay_in_a_second_process_refuses ... ok
test capture::reqs_existing::same_line_req_and_its_children_insert_as_one_block ... ok
test capture::reqs_existing::req_only_capture_keeps_notes_drawer_nonempty_and_existing_reqs_append ... ok
test capture::reqs_existing::task_links_to_requirement_anchors_refuse_with_owner_copy ... ok
test capture::reqs_lexical::parse_needs_agree_with_completion_on_deep_requirement_lines ... ok
test capture::reqs_lexical::deep_requirement_lines_take_the_typing_aliases ... ok
test capture::req_close::offer_close_keeps_ordinary_numbering_when_owner_has_no_reqs ... ok
test capture::req_close::pomodoro_close_pulls_several_carries_into_one_continuation ... ok
test capture::req_close::pull_in_on_req_is_carry_pulled ... ok
test capture::reqs_lexical::a_deep_requirement_prerequisite_writes_like_level_two ... ok
test capture::reqs_new::a_project_note_row_files_its_loose_note_into_notes ... ok
test capture::reqs_new::a_task_list_canonicalizes_each_owner_and_leaves_zero_req_rows ... ok
test capture::req_close::keyed_and_numbered_flags_select_the_same_row ... ok
test capture::reqs_new::a_single_requirement_uses_singular_copy ... ok
test capture::reqs_new::a_zero_req_new_task_stays_byte_identical_and_omits_requirements ... ok
test capture::reqs_refusals::a_third_level_note_keeps_invalid_child_line_with_the_requirement_hint ... ok
test capture::reqs_new::a_new_task_files_notes_into_notes_and_reports_the_write ... ok
test capture::reqs_refusals::a_new_task_writes_requirements_past_two_levels_at_their_depth ... ok
test capture::reqs_new::interleaved_notes_reqs_and_drawers_canonicalize ... ok
test capture::reqs_refusals::a_placeholder_requirement_writes_nothing ... ok
test capture::reqs_new::an_authored_notes_drawer_merges_scooped_notes ... ok
test capture::reqs_refusals::a_project_note_row_writes_its_requirements_at_depth ... ok
test capture::reqs_new::clip_notes_with_reqs_file_into_notes ... ok
test capture::rewrite::capture_rewrite_json_expands_an_admitted_requirement_marker ... ok
test capture::rewrite::capture_rewrite_keeps_requirement_marker_literal_at_an_ineligible_position ... ok
test capture::rewrite::capture_rewrite_keeps_requirement_marker_literal_in_a_notebook_list ... ok
test capture::reqs_new::a_named_new_task_and_a_linked_pomodoro_task_write_the_same_layout ... ok
test capture::sections::capture_forced_section_requires_route ... ok
test capture::reqs_refusals::a_multi_note_existing_task_writes_requirements_at_their_depth ... ok
test completion::protocol::malformed_request_exits_two ... ok
test completion::zsh_adapter::adapter_source_has_required_properties ... ok
test capture::rewrite::capture_rewrite_keeps_requirement_marker_literal_in_a_record_note ... ok
test capture::reqs_lexical::refused_deep_lines_stay_inert ... ok
test capture::reqs_refusals::forced_targets_re_decide_requirement_positions ... ok
test capture::reqs_refusals::the_depth_bound_admits_sixteen_and_refuses_seventeen ... ok
test capture::reqs_refusals::the_same_line_form_writes_its_requirement_chain_at_depth ... ok
test completion::zsh_adapter::request_argv_unquotes_escaped_hash_prefix ... ok
test completion::zsh_adapter::request_argv_unquotes_words_and_passes_suffix ... ok
test completion::vault::missing_prerequisites_name_the_flag ... ok
test capture::reqs_refusals::refusals_report_the_shared_codes_and_copy ... ok
test capture::successor_jump::jump_does_not_satisfy_required_pull_in_choice ... ok
test highlights::create::highlights_create_closed_and_plain_require_one_vault_note ... ok
test capture::successor_offers::so27_require_choice_refuses_when_offers_exist ... ok
test capture::successor_integration::restart_and_reset_never_complete_prerequisites ... ok
test capture::retype_closeout::near_duplicate_teaches_requested_override_and_creates_it ... ok
test highlights::podcast_create::enrich_off_makes_no_itunes_request ... ok
test highlights::jobs::ref_jobs_stale_running_once_is_requeued_and_clipped ... ok
test capture::reqs_lexical::deep_requirement_lines_open_the_same_pickers_as_level_two ... ok
test capture::successor_verdicts::pulled_in_inbox_row_remains_required_and_is_renumbered ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test relations_rename::relations_rename_applies_case_only_and_requires_merge_for_existing_key ... ok
test highlights::tasks::highlights_ref_task_cancelled_dry_run_requires_and_writes_pdf_marker ... ok
test plugins::plugins_sync_git_vault_requires_ignored_stamp ... ok
test capture::note_pull::np_move_groups_follow_requested_sources_in_cli_fixtures ... ok
test task_status_hooks::subprojects::blocked_subproject_links_are_consumed_and_promote_ancestor_prerequisites ... ok
test highlights::tasks::highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker ... ok
test task_drawer_rename::invalid_requests_exit_2_before_reading_the_vault ... ok
test capture::reqs_refusals::dry_run_and_capture_parse_agree_on_codes_and_depths ... ok
test pomodoro::pomodoro_stale_cutoff_is_empty_unless_requested ... ok
test task_tidy::a_req_owning_prj_files_loose_notes_under_the_notes_section ... ok
test task_status_hooks::blocked::reconcile_terminal_project_prerequisite_does_not_block_residents ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test notebooks_catalog::create_summary_rules_quote_warn_and_require ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test task_status_hooks::consume::consumption_promoted_daily_note_prerequisite_may_clear_next_run ... ok
test highlights::create::highlights_create_output_renders_pdf_at_requested_path_when_available ... ok

test result: ok. 125 passed; 0 failed; 0 ignored; 0 measured; 3946 filtered out; finished in 10.39s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.28s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/cli-1555ea48c466b133)

running 69 tests
test capture::clip::capture_clip_json_always_emits_collection_fields ... ok
test capture::clip::capture_flat_clipboard_list_routes_normalized_children ... ok
test capture::clip::capture_history_dry_run_plans_colliding_files_without_writes ... ok
test capture::clip::capture_clipboard_reads_once_per_invocation ... ok
test capture::clip::capture_history_human_output_reports_provider_and_unknown_ages ... ok
test capture::clip::capture_history_without_a_provider_has_actionable_guidance ... ok
test capture::clip::capture_percent_c1_is_an_exact_single_clip_alias ... ok
test capture::clip::capture_clip_failures_leave_vault_untouched ... ok
test attachments::attachments_capture_clip_records_origins_and_keeps_json_stable ... ok
test capture::clip::capture_bare_terminal_marker_clipboard_marker_writes_children_beneath_note ... ok
test capture::clip::capture_sub_bullet_task_ref_recovers_shift_and_nests_clipboard ... ok
test capture::clip::capture_oversized_clipboard_refuses_without_writing ... ok
test attachments::attachments_import_classifies_like_clipboard_lines ... ok
test capture::clip::capture_clip_uses_each_target_notes_indent_and_tabs_for_a_fresh_note ... ok
test capture::clip::capture_clipboard_history_config_selects_the_provider ... ok
test capture::clip_notes::clip_notes_keep_relationship_refusal ... ok
test capture::clip_notes::clip_notes_flatten_history_in_order ... ok
test capture::clip::capture_headerless_clip_marker_renders_under_tasks_and_pomodoros ... ok
test capture::clip::capture_clip_saves_attachments_snippets_and_reports_dry_run ... ok
test capture::clip::capture_clip_options_force_read_or_never_read ... ok
test capture::clip::capture_clip_marker_composes_with_schedule_routes_bullets_and_pomodoro ... ok
test capture::clip_notes::clip_notes_attachments_and_snippets_are_direct_children ... ok
test capture::clip::capture_history_is_headerless_structured_and_composes_with_routes ... ok
test capture::parse::capture_parse_never_touches_the_vault_or_clipboard ... ok
test capture::clip_notes::clip_notes_dry_run_no_clip_atomicity ... ok
test capture::complete_drawers::target_run_completion_crosses_schedule_and_clipboard_tokens ... ok
test capture::multi_target::clipboard_runs_share_each_read_and_reuse_one_snippet_file ... ok
test capture::multi_target::counted_clipboard_reads_share_live_and_history_values_within_the_run ... ok
test capture::clip::capture_history_provider_failures_leave_the_vault_untouched ... ok
test capture::notebook_notes::test_notebook_checkbox_guard_covers_generated_authored_and_clip_rows ... ok
test capture::priority::capture_priority_with_clip_orders_clip_children_before_schedule_log ... ok
test capture::r#ref::capture_spool_hit_is_clipping ... ok
test capture::parse_template::template_clipboard_follows_expanded_instances ... ok
test capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks ... ok
test capture::r#ref::capture_with_kick_returns_before_the_clip_finishes ... ok
test capture::clip_notes::clip_notes_drawers_and_prj_sections ... ok
test capture::prj_drawers::capture_prj_drawer_authored_children_and_clip_nest_under_entry ... ok
test capture::clip_notes::clip_notes_are_direct_children_in_order_before_managed_logs ... ok
test capture::record::forced_clip_refuses_record_before_running_clipboard_command ... ok
test capture::template::template_clipboard_markers_refuse_even_with_no_clip ... ok
test clipboard_status::off_selection_refuses_with_stable_code ... ok
test capture::template::template_url_listen_marker_is_not_clipboard_capture ... ok
test capture::rewrite::capture_rewrite_never_touches_the_vault_or_clipboard ... ok
test capture::reqs_new::clip_notes_with_reqs_file_into_notes ... ok
test clipboard_status::help_and_usage_are_listed_under_integrations ... ok
test help_options::highlights_clip_alias_help_matches_create_help ... ok
test clipboard_status::healthy_command_provider_reports_only_metadata ... ok
test highlights::create::highlights_create_clip_alias_is_byte_identical_on_error_path ... ok
test capture::r#ref::capture_end_to_end_clips_through_the_worker ... ok
test capture::r#ref::explicit_url_clip_forms_keep_the_clipboard_path ... ok
test highlights::fake_clip::fake_adapter_answers_render_like_compose ... ok
test highlights::jobs::ref_jobs_old_created_records_still_render_as_clipped ... ok
test highlights::create::highlights_create_article_maps_options_to_clip ... ok
test capture::clip_notes::clip_notes_retype_forced_clip_json_and_human ... ok
test capture::template::template_clip_flag_and_session_operators_have_stable_codes ... ok
test highlights::create::highlights_create_clip_alias_matches_create_for_force ... ok
test highlights::jobs::ref_jobs_stale_running_twice_falls_back_without_clipping ... ok
test highlights::create::highlights_create_clip_alias_rereads_filed_url ... ok
test highlights::create::highlights_create_and_clip_attach_listen_to_the_newest_reading ... ok
test highlights::jobs::ref_jobs_stuck_fallback_is_retried_without_clipping ... ok
test capture::r#ref::percent_listen_reference_never_reads_clipboard_and_queues_listen_job ... ok
test highlights::jobs::ref_jobs_run_clips_a_seeded_article ... ok
test highlights::create::highlights_create_article_routes_through_clip_engine ... ok
test highlights::jobs::ref_jobs_stale_running_once_is_requeued_and_clipped ... ok
test highlights::create::highlights_create_folded_doctor_reports_web_clip_rows ... ok
test capture::clip::stale_counted_clipboard_history_refuses_without_writing ... ok
test clipboard_status::stale_command_provider_refuses_with_stable_code_and_redacts_content ... ok
test capture::clip::capture_hung_history_command_refuses_near_the_deadline ... ok
test highlights::jobs::ref_jobs_slow_clip_still_drains_a_late_job ... ok

test result: ok. 69 passed; 0 failed; 0 ignored; 0 measured; 4002 filtered out; finished in 6.88s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.21s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_101408/build/debug/deps/cli-1555ea48c466b133)

running 1 test
test docs_reference::cli_reference_is_current ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 4070 filtered out; finished in 1.98s

============================= test session starts ==============================
platform linux -- Python 3.14.4, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/tools/docs
configfile: pyproject.toml
plugins: platformdirs-4.13.5
collected 8 items

tools/docs/tests/test_contracts.py FFF.....                              [100%]

=================================== FAILURES ===================================
_______ test_current_registry_and_generated_nav_are_complete_and_unique ________

    def test_current_registry_and_generated_nav_are_complete_and_unique() -> None:
        registry = load_contract_registry(ROOT)
>       assert len(registry.entries) == 56
E       AssertionError: assert 57 == 56
E        +  where 57 = len((Contract(stem='articles', summary='`bob articles` formatting, list, outline, adopt, and ArticlePlan JSON', order=1, r...ar-label display contract for canonical task dates and recurrence rules', order=6, reader=None, historical=False), ...))
E        +    where (Contract(stem='articles', summary='`bob articles` formatting, list, outline, adopt, and ArticlePlan JSON', order=1, r...ar-label display contract for canonical task dates and recurrence rules', order=6, reader=None, historical=False), ...) = ContractRegistry(groups=(ContractGroup(title='Capture and integrations', entries=(Contract(stem='articles', summary='`...ry, ownership roles, guarded `bob props show` / `update`, undo, and JSON', order=56, reader=None, historical=False))))).entries

tools/docs/tests/test_contracts.py:36: AssertionError
_________ test_llmstxt_contracts_section_lists_exactly_registry_stems __________

    def test_llmstxt_contracts_section_lists_exactly_registry_stems() -> None:
        registry = load_contract_registry(ROOT)
        expected = sorted(f"{entry.stem}.md" for entry in registry.entries)
        config = load_yaml(ROOT / "mkdocs.yml")
        llmstxt = next(
            plugin["llmstxt"] for plugin in config["plugins"] if isinstance(plugin, dict) and "llmstxt" in plugin
        )
        actual = sorted(llmstxt["sections"]["Contracts (optional)"])
>       assert actual == expected
E       AssertionError: assert ['areas.md', ...ture.md', ...] == ['areas.md', ...ture.md', ...]
E         
E         At index 43 diff: 'task-link-marks.md' != 'task-drawers.md'
E         Right contains one more item: 'walks.md'
E         Use -v to get more diff

tools/docs/tests/test_contracts.py:56: AssertionError
__________ test_readme_table_matches_original_contract_index_snapshot __________

    def test_readme_table_matches_original_contract_index_snapshot() -> None:
        table = _generated_region(
            (ROOT / "docs/README.md").read_text(encoding="utf-8"), "contract table"
        )
>       assert hashlib.sha256(table.encode()).hexdigest() == README_TABLE_SHA256
E       AssertionError: assert '17180faf3a68...171641f9e757a' == 'b89c442651a8...adbe30df6ecfa'
E         
E         - b89c442651a84055cc27115e495c23fbb0fc5d3352050652e14adbe30df6ecfa
E         + 17180faf3a681a022b9e0f60ffb3912e10976d36b4afad97320171641f9e757a

tools/docs/tests/test_contracts.py:63: AssertionError
=========================== short test summary info ============================
FAILED tools/docs/tests/test_contracts.py::test_current_registry_and_generated_nav_are_complete_and_unique
FAILED tools/docs/tests/test_contracts.py::test_llmstxt_contracts_section_lists_exactly_registry_stems
FAILED tools/docs/tests/test_contracts.py::test_readme_table_matches_original_contract_index_snapshot
========================= 3 failed, 5 passed in 0.83s ==========================
failed  exit=1  duration=557525ms

