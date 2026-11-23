# Chat History - ace-run (bob-cli-ph.1--mon-6)

- **TIMESTAMP:** 2026-11-23 10:13:52 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-ph.1--mon-6

## Prompt

sase monitor start --command 'set -e; cargo test --lib capture_drawers; cargo test --lib task_block_layout; cargo test --lib task_split; cargo test --lib task_text_escape; cargo test --lib gcal::description::bullets; cargo test --lib gmail::body::inert; cargo test --test cli drawer; cargo test --test cli req; cargo test --test cli clip; cargo test --test cli docs_reference; uv run --project tools/docs pytest tools/docs/tests/test_contracts.py; just check; just docs-check' --reason 'Run the full drawer-contract regression and repository gates after correcting stale Calendar drawer expectations'

## Response

sase tool run 7f1bd8d6bb0f2c9e22dcbe83fba517b5
warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.67s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 33 tests
test native::capture_drawers::tests::bold_drawer_titles_keep_authored_bytes_and_unicode_keys ... ok
test native::capture_drawers::tests::build_cli_renders_without_panicking ... ok
test native::capture_drawers::tests::drawer_heading_mapping_is_lossless_and_creation_stays_nonempty ... ok
test native::capture_drawers::tests::catalog_search_ranks_prefix_tier_first_and_skips_excluded_keys ... ok
test native::capture_drawers::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_drawers::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_drawers::tests::near_duplicate_suggests_quoted_title_when_slug_is_invalid ... ok
test native::capture_drawers::tests::query_matches_a_key_or_slug_by_prefix_before_substring ... ok
test native::capture_drawers::tests::ensure_drawer_creates_project_h2_sibling_and_rescans_it ... ok
test native::capture_drawers::tests::ensure_drawer_creates_task_drawer_then_rescans_it ... ok
test native::capture_drawers::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_drawers::tests::last_entry_text_is_the_direct_entry_a_capture_lands_after ... ok
test native::capture_drawers::tests::contextual_reader_filters_false_drawers_and_reports_byte_ranges ... ok
test native::capture_drawers::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_drawers::tests::reserved_refusals_name_the_reserved_key ... ok
test native::capture_drawers::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_drawers::tests::checkboxed_all_caps_children_are_not_drawers ... ok
test native::capture_drawers::tests::sentence_punctuation_drawer_titles_qualify ... ok
test native::capture_drawers::tests::grandchild_is_not_a_direct_child_drawer ... ok
test native::capture_drawers::tests::empty_drawer_bullet_still_qualifies ... ok
test native::capture_drawers::tests::managed_logs_are_never_drawers_plain_titles_are ... ok
test native::capture_drawers::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_drawers::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_drawers::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_drawers::tests::drawer_conformance_vectors_match_reader_and_mapping ... ok
test native::capture_drawers::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_drawers::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_drawers::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_drawers::tests::catalog_v3_rebuilds_v2_and_keeps_marker_provenance_per_spelling ... ok
test native::capture_drawers::tests::resolved_task_with_no_drawers_is_a_successful_empty_list ... ok
test native::capture_drawers::tests::lists_drawers_in_document_order_for_a_block_id ... ok
test native::capture_drawers::tests::title_whitelist_edges ... ok
test native::capture_drawers::tests::task_ref_resolves_a_task_without_a_block_id ... ok

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
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.22s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 15 tests
test native::task_block_layout::tests::zones_name_every_task_child_kind ... ok
test native::task_block_layout::tests::canonicalize_new_req_block_leaves_zero_req_and_closed_blocks ... ok
test native::task_block_layout::tests::a_note_without_a_final_newline_keeps_that_state ... ok
test native::task_block_layout::tests::a_created_notes_drawer_lands_first_among_the_drawers ... ok
test native::task_block_layout::tests::log_and_cancel_log_writers_land_in_their_zones ... ok
test native::task_block_layout::tests::notes_home_matches_bold_notes_by_key_and_tidy_reuses_its_header ... ok
test native::task_block_layout::tests::vector_ids_are_unique_and_sequenced ... ok
test native::task_block_layout::tests::managed_link_writers_land_inside_the_managed_zone ... ok
test native::task_block_layout::tests::layout_note_homes_match_vectors ... ok
test native::task_block_layout::tests::layout_violations_match_vectors ... ok
test native::task_block_layout::tests::canonicalize_new_req_block_files_notes_and_keeps_req_subtrees ... ok
test native::task_block_layout::tests::layout_slots_match_vectors ... ok
test native::task_block_layout::tests::layout_tidy_matches_vectors ... ok
test native::task_block_layout::tests::a_tidied_block_has_no_violations_and_tidies_to_none ... ok
test native::task_block_layout::tests::req_writers_match_vectors ... ok

test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 7975 filtered out; finished in 0.06s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.23s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::task_split::tests::req_candidates_list_every_depth_with_their_state ... ok
test native::task_split::tests::split_repairs_whole_payload_with_multiline_fence_and_comment_context ... ok
test native::task_split::tests::split_same_note_fabricates_no_retargets ... ok
test native::task_split::tests::carry_req_by_row_key_moves_the_branch_and_maps_descendants ... ok
test native::task_split::tests::split_minted_anchor_still_qualifies_pathless_stayed_anchor_links ... ok
test native::task_split::tests::split_repairs_cross_note_anchors_in_owned_fields_and_payload ... ok
test native::task_split::tests::carry_req_by_line_digest_and_its_refusals ... ok
test native::task_split::tests::split_conformance_vectors_match_byte_for_byte ... ok

test result: ok. 8 passed; 0 failed; 0 ignored; 0 measured; 7982 filtered out; finished in 0.46s

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
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::task_text_escape::tests::escape_task_text_leaves_intended_markup_alone ... ok
test native::task_text_escape::tests::note_inline_neutralizes_code_spans_queries_and_math ... ok
test native::task_text_escape::tests::note_inline_disarms_organizer_escapes_first ... ok
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
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.23s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 8 tests
test native::gcal::description::bullets::tests::markdown_destination_encoding_covers_delimiters ... ok
test native::gcal::description::bullets::tests::hash_and_materialization_follow_depth_and_body ... ok
test native::gcal::description::bullets::tests::punctuated_drawer_shaped_lines_are_defused ... ok
test native::gcal::description::bullets::tests::note_prose_is_exempt_from_the_cap ... ok
test native::gcal::description::bullets::tests::bullet_vectors ... ok
test native::gcal::description::bullets::tests::oversize_input_uses_one_calendar_fallback ... ok
test native::gcal::description::bullets::tests::oversize_input_keeps_reasons_above_the_fallback ... ok
test native::gcal::description::bullets::tests::hostile_bullets_are_isolated_from_bob_scanners ... ok

test result: ok. 8 passed; 0 failed; 0 ignored; 0 measured; 7982 filtered out; finished in 0.07s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.20s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/bob_cli-133a49cac731dd3a)

running 19 tests
test native::gmail::body::inert::tests::checkbox_fragments_never_survive_as_requirements ... ok
test native::gmail::body::inert::tests::verified_embed_accepts_only_writer_paths ... ok
test native::gmail::body::inert::tests::verified_wikilink_mints_exact_resized_embed_for_writer_paths_only ... ok
test native::gmail::body::inert::tests::whole_bold_and_legacy_list_items_are_defused_as_imported_children ... ok
test native::gmail::body::inert::tests::structured_inline_text_keeps_spaces_around_renderer_formatting ... ok
test native::gmail::body::inert::tests::hidden_node_boundaries_cannot_rejoin_hazards ... ok
test native::gmail::body::inert::tests::safe_url_refuses_wikilinks_but_keeps_usable_urls ... ok
test native::gmail::body::inert::tests::fenced_code_keeps_text_info_and_sizes_delimiters ... ok
test native::gmail::body::inert::tests::split_colon_runs_cannot_reform_bare_or_bracketed_fields ... ok
test native::gmail::body::inert::tests::simulated_card_holds_no_sender_structure ... ok
test native::gmail::body::inert::tests::remote_images_never_become_image_syntax ... ok
test native::gmail::body::inert::tests::inline_queries_are_broken ... ok
test native::gmail::body::inert::tests::bang_before_trusted_link_never_forms_remote_image ... ok
test native::gmail::body::inert::tests::readable_text_survives_untouched ... ok
test native::gmail::body::inert::tests::split_percent_math_and_backslash_edges_stay_inert ... ok
test native::gmail::body::inert::tests::link_policy_allows_only_http_mailto ... ok
test native::gmail::body::inert::tests::helpers_neutralize_hostile_fragments ... ok
test native::gmail::body::inert::tests::yaml_values_survive_serialization_without_active_syntax ... ok
test native::gmail::body::inert::tests::adversarial_corpus_stays_inert_and_readable ... ok

test result: ok. 19 passed; 0 failed; 0 ignored; 0 measured; 7971 filtered out; finished in 0.50s

   Compiling bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 4m 03s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws13-261123_100046/build/debug/deps/cli-1555ea48c466b133)

running 82 tests
test capture::complete_drawers::empty_drawer_menu_json_pins_groups_fields_and_the_unselected_open ... ok
test capture::complete_drawers::bullet_menu_json_pins_the_target_the_bare_titles_and_the_continuation ... ok
test capture::complete_drawers::bullet_menu_human_output_shows_the_title_line_only ... ok
test capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks ... FAILED
test capture::complete_drawers::drawer_menu_human_output_lists_bobs_detail_and_refusals ... ok
test capture::complete_drawers::bullet_menu_continuation_depends_on_what_follows_the_token ... ok
test capture::complete_drawers::quoted_drawer_literals_decode_the_query_and_cover_the_quotes ... ok
test capture::complete_drawers::notebook_note_bullet_hash_opens_no_drawer_menu ... ok
test capture::drawer_bullets::childless_all_caps_stays_a_plain_bullet ... ok
test capture::complete_transfer::transfer_drawer_destination_lists_task_drawers ... ok
test capture::complete_drawers::target_run_completion_crosses_schedule_and_clipboard_tokens ... ok
test capture::complete_drawers::run_members_complete_and_bullet_menu_keeps_first_members_drawers ... ok
test capture::drawer_bullets::catalog_spelling_wins_for_a_slug ... ok
test capture::complete_notebook_sections::place_menu_covers_drawer_glued_and_bullet_menus ... ok
test capture::complete_drawers::refused_rows_name_the_commits_reason ... ok
test capture::complete_drawers::typed_drawer_menu_filters_groups_and_drops_the_unselected_open ... ok
test capture::complete_drawers::bullet_menu_on_new_tasks_and_project_notes_carries_the_new_target ... ok
test capture::drawer_bullets::new_task_shortcut_renders_the_all_caps_drawer ... ok
test capture::drawer_bullets::repeated_keys_merge_in_draft_order ... ok
test capture::complete_drawers::unresolvable_drawer_targets_return_a_diagnostic_and_no_rows ... ok
test capture::drawer_bullets::project_note_shortcut_becomes_a_section ... ok
test capture::drawer_bullets::same_line_note_is_not_under_task ... ok
test capture::drawer_bullets::reserved_diagnostic_copy_matches_the_refusal ... ok
test capture::complete_drawers::bullet_starts_that_cannot_name_a_drawer_are_empty_successes ... ok
test capture::drawer_bullets::reserved_childless_and_text_refusals ... ok
test capture::clip_notes::clip_notes_drawers_and_prj_sections ... ok
test capture::authored::capture_drawer_authored_children_and_composition ... ok
test capture::note_bullets::childless_literal_matching_existing_drawer_is_refused ... ok
test capture::multi_target::a_glued_drawer_suffix_stays_local_to_its_target ... ok
test capture::note_bullets::same_line_shortcut_reports_drawer_position ... ok
test capture::multi_target::note_less_bullets_and_drawers_are_filed_to_each_member ... ok
test capture::note_bullets::glued_drawer_files_every_bullet_inside ... ok
test capture::note_bullets::reserved_drawer_is_refused ... ok
test capture::drawer_bullets::punctuated_drawer_merges_into_the_existing_drawer ... ok
test capture::complete_editor::capture_complete_drawer_json_covers_components_and_warnings ... ok
test capture::prj_drawers::capture_drawers_lists_h2_sections_for_prj_parent ... ok
test capture::note_bullets::two_bullets_naming_one_missing_drawer_merge ... ok
test capture::prj_drawers::capture_complete_prj_drawer_menu_lists_h2_sections ... ok
test capture::prj_drawers::capture_prj_drawer_authored_children_and_clip_nest_under_entry ... ok
test capture::prj_drawers::capture_prj_drawer_promotion_round_trip ... ok
test capture::drawer_bullets::new_project_note_structural_sections_stay_legal_everywhere ... ok
test capture::note_bullets::worked_example_files_notes_drawers_json_and_human ... ok
test capture::reqs_new::an_authored_notes_drawer_merges_scooped_notes ... ok
test capture::lists::capture_list_checkbox_and_drawer_positions_are_refused ... ok
test capture::reqs_new::interleaved_notes_reqs_and_drawers_canonicalize ... ok
test capture::prj_drawers::capture_prj_drawer_creates_missing_h2_in_title_case ... ok
test capture::parse::capture_parse_json_reports_drawer_and_incomplete_needs ... ok
test capture::prj_drawers::capture_prj_drawer_ambiguous_and_guard_refuse_but_literal_wins ... ok
test capture::prj_drawers::capture_prj_drawer_appends_after_section_content ... ok
test capture::reqs_existing::implicit_notes_on_a_req_owner_reports_the_drawer ... ok
test capture::reqs_existing::req_only_capture_keeps_notes_drawer_nonempty_and_existing_reqs_append ... ok
test capture::prj_drawers::capture_prj_drawer_separate_type_and_plain_child_still_work ... ok
test capture::sections::capture_forced_drawer_option_errors ... ok
test capture::sections::capture_drawer_managed_log_geometry ... ok
test capture::task_id::capture_drawers_json_and_human_list_sections ... ok
test capture::merge_in::merge_in_equivalence_covers_same_note_drawers_and_configured_labels ... ok
test capture::drawer_bullets::legal_drawer_controls_agree_across_parse_preview_and_commit ... ok
test capture::sections::capture_drawer_prefix_vs_whole_slug_and_multiword ... ok
test capture::sections::capture_drawer_inserts_into_first_middle_and_last_sections ... ok
test help::capture_drawers_help_is_native_only ... ok
test help_options::capture_drawers_help_lists_options_alphabetically ... FAILED
test capture::sections::capture_forced_drawer_matches_title_exactly ... ok
test completion::capture_text::drawers_complete_after_id_hash ... ok
test completion::vault::drawers_offer_exact_titles ... ok
test capture::retype_closeout::idless_task_ref_retype_plain_and_drawer ... ok
test capture::drawer_bullets::reserved_new_task_drafts_agree_across_parse_preview_and_commit ... ok
test capture::task_id::capture_drawers_empty_and_error_paths ... ok
test capture::transfer::transfer_merge_origins_cover_renamed_anchors_and_drawers ... ok
test capture::prj_drawers::capture_prj_drawer_structural_and_reserved_refuse ... ok
test capture::sections::capture_drawer_indent_units_crlf_and_dry_run ... ok
test task_drawer_rename::bare_run_is_a_dry_run_with_an_inventory ... ok
test task_drawer_rename::invalid_requests_exit_2_before_reading_the_vault ... ok
test task_drawer_rename::no_match_is_a_clean_report ... ok
test capture::complete_drawers::accepting_a_row_makes_the_commit_agree_with_the_menu ... ok
test capture::sections::capture_drawer_errors_leave_the_note_unchanged ... ok
test capture::transfer::transfer_merge_drawers_and_sections_preserve_selector_intent ... ok
test task_drawer_rename::apply_prints_a_summary_per_note ... ok
test task_drawer_rename::apply_commits_once_and_a_rerun_reports_nothing ... ok
test task_merge::merge_into_created_drawer ... ok
test task_merge::merge_into_prj_h2_drawer ... ok
test task_merge::merge_into_drawer_uses_existing_drawer ... ok
test capture::complete_drawers::accepting_a_bullet_row_makes_the_commit_agree_with_the_menu ... ok

failures:

---- capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks stdout ----

thread 'capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks' (44263) panicked at tests/cli/capture/clip.rs:140:5:
assertion `left == right` failed
  left: Array [String("  - __API Design__"), String("  - __AGENDA__")]
 right: Array [String("\t- __API Design__"), String("\t- __AGENDA__")]
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace

---- help_options::capture_drawers_help_lists_options_alphabetically stdout ----

thread 'help_options::capture_drawers_help_lists_options_alphabetically' (44648) panicked at tests/cli/help_options.rs:286:5:
expected capture-drawers long help:
List the direct-child drawer bullets of one task in a routed Bob note.

Task drawers include legacy ALL-CAPS headers and whole-bold titles.

The command is read-only and reports every qualifying drawer in document order with its original title, key, whitespace-free slug, marker, line, and entry count, plus recent catalog drawers absent from the task. When the parent is the project note's own `^prj` task, the note's eligible `##` sections are reported instead of task-child drawers. It uses the same parent-task lookup and error messages as `bob capture`: a missing, duplicated, or non-task block ID is an error, as is a stale or ambiguous --task-ref. A resolved task with no drawers returns a successful empty list so picker callers can skip the chooser.

Exactly one of -i/--block-id or -t/--task-ref is required. Use --block-id when the parent already has an ID, and --task-ref for the stale-safe picker ref from `bob capture-complete` or `bob capture-tasks`.

Usage: bob capture-drawers [OPTIONS]

Options:
  -i, --block-id <ID>
          Block ID of the parent task

  -b, --bob-dir <DIR>
          Bob vault root; defaults to BOB_DIR or ~/bob

  -f, --format <FORMAT>
          Output format: human or json
          
          [default: human]
          [possible values: human, json]

  -h, --help
          Show help

  -r, --route <NAME>
          Route/name of the note that contains the task

  -t, --task-ref <REF>
          Stale-safe task ref from capture-complete or capture-tasks

Examples:
  bob capture-drawers --route foo --block-id bar
  bob capture-drawers -r foo -i bar -f json
  bob capture-drawers -r cash -t 12:abcd1234
  bob capture-drawers -b ~/bob -r project-alpha -i goog-exit

Environment:
  BOB_DIR                    Bob vault root when --bob-dir is omitted



failures:
    capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks
    help_options::capture_drawers_help_lists_options_alphabetically

test result: FAILED. 80 passed; 2 failed; 0 ignored; 0 measured; 3989 filtered out; finished in 3.61s

error: test failed, to rerun pass `--test cli`
failed  exit=101  duration=250567ms

