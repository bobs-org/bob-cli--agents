# Chat History - ace-run (bob-cli-29.2--mon-0)

- **TIMESTAMP:** 2026-09-28 07:22:55 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-29.2--mon-0

## Prompt

sase monitor start --command 'cargo test && cargo clippy --all-targets --all-features' --reason 'Run the phase Rust tests and clippy after fixing compile failures'

## Response

sase tool run b9f52d2d2bd178a60c11797d996193ce
    Updating crates.io index
     Locking 5 packages to latest Rust 1.95.0 compatible versions
      Adding errno v0.3.14
      Adding fastrand v2.5.0
      Adding linux-raw-sys v0.12.1
      Adding rustix v1.1.5
      Adding tempfile v3.27.0
 Downloading crates ...
  Downloaded rustix v1.1.5
   Compiling typenum v1.20.1
   Compiling version_check v0.9.5
   Compiling cfg-if v1.0.4
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
   Compiling quote v1.0.45
   Compiling memchr v2.8.1
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling foldhash v0.2.0
   Compiling libc v0.2.186
   Compiling serde_core v1.0.228
   Compiling getrandom v0.4.2
   Compiling rand_core v0.10.1
   Compiling tinyvec_macros v0.1.1
   Compiling autocfg v1.5.1
   Compiling serde v1.0.228
   Compiling utf8parse v0.2.2
   Compiling cpufeatures v0.3.0
   Compiling bitflags v2.12.1
   Compiling crc32fast v1.5.0
   Compiling anstyle-parse v1.0.0
   Compiling tinyvec v1.11.0
   Compiling cc v1.2.63
   Compiling itoa v1.0.18
   Compiling is_terminal_polyfill v1.70.2
   Compiling generic-array v0.14.7
   Compiling hashbrown v0.17.1
   Compiling anstyle v1.0.14
   Compiling thiserror v2.0.18
   Compiling anstyle-query v1.1.5
   Compiling cpufeatures v0.2.17
   Compiling simd-adler32 v0.3.9
   Compiling colorchoice v1.0.5
   Compiling zmij v1.0.21
   Compiling adler2 v2.0.1
   Compiling chacha20 v0.10.0
   Compiling num-traits v0.2.19
   Compiling miniz_oxide v0.8.9
   Compiling anstream v1.0.0
   Compiling nom v8.0.0
   Compiling unicode-normalization v0.1.25
   Compiling aho-corasick v1.1.4
   Compiling const-oid v0.10.2
   Compiling strsim v0.11.1
   Compiling unicode-properties v0.1.4
   Compiling serde_json v1.0.150
   Compiling bytecount v0.6.9
   Compiling clap_lex v1.1.0
   Compiling indexmap v2.14.0
   Compiling regex-syntax v0.8.10
   Compiling unicode-bidi v0.3.18
   Compiling flate2 v1.1.9
   Compiling syn v2.0.117
   Compiling hybrid-array v0.4.12
   Compiling clap_builder v4.6.0
   Compiling encoding_rs v0.8.35
   Compiling stringprep v0.1.5
   Compiling ttf-parser v0.25.1
   Compiling rand v0.10.1
   Compiling unsafe-libyaml v0.2.11
   Compiling log v0.4.30
   Compiling crypto-common v0.2.2
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling inout v0.1.4
   Compiling block-buffer v0.10.4
   Compiling rquickjs-sys v0.12.1
   Compiling block-buffer v0.12.0
   Compiling digest v0.10.7
   Compiling cipher v0.4.4
   Compiling ryu v1.0.23
   Compiling rangemap v1.7.1
   Compiling md-5 v0.10.6
   Compiling sha2 v0.10.9
   Compiling aes v0.8.4
   Compiling cbc v0.1.2
   Compiling ecb v0.1.2
   Compiling iana-time-zone v0.1.65
   Compiling weezl v0.1.12
   Compiling fs2 v0.4.3
   Compiling digest v0.11.3
   Compiling chrono v0.4.44
   Compiling similar v2.7.0
   Compiling sha2 v0.11.0
   Compiling regex-automata v0.4.14
   Compiling hex v0.4.3
   Compiling vcpkg v0.2.15
   Compiling pkg-config v0.3.33
   Compiling clap v4.6.1
   Compiling rustix v1.1.5
   Compiling num-conv v0.2.2
   Compiling linux-raw-sys v0.12.1
   Compiling time-core v0.1.9
   Compiling powerfmt v0.2.0
   Compiling deranged v0.5.8
   Compiling hashlink v0.12.1
   Compiling quick-xml v0.41.0
   Compiling fallible-iterator v0.3.0
   Compiling libsqlite3-sys v0.38.1
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling nom_locate v5.0.0
   Compiling once_cell v1.21.4
   Compiling base64 v0.22.1
   Compiling smallvec v1.15.2
   Compiling fastrand v2.5.0
   Compiling fallible-streaming-iterator v0.1.9
   Compiling time v0.3.53
   Compiling lopdf v0.40.0
   Compiling regex v1.12.3
   Compiling tempfile v3.27.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling plist v1.10.0
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10)
warning: struct `VaultLinkResolver` is never constructed
   --> src/native/vault_links.rs:106:19
    |
106 | pub(crate) struct VaultLinkResolver {
    |                   ^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: associated items `new`, `root`, `resolve`, and `build_index` are never used
   --> src/native/vault_links.rs:114:19
    |
113 | impl VaultLinkResolver {
    | ---------------------- associated items in this implementation
114 |     pub(crate) fn new(root: impl Into<PathBuf>) -> Self {
    |                   ^^^
...
123 |     pub(crate) fn root(&self) -> &Path {
    |                   ^^^^
...
127 |     pub(crate) fn resolve(
    |                   ^^^^^^^
...
154 |     fn build_index(&self) -> NoteIndex {
    |        ^^^^^^^^^^^

warning: function `collect_markdown_paths` is never used
   --> src/native/vault_links.rs:164:4
    |
164 | fn collect_markdown_paths(
    |    ^^^^^^^^^^^^^^^^^^^^^^

warning: method `root` is never used
   --> src/native/vault_links.rs:123:19
    |
113 | impl VaultLinkResolver {
    | ---------------------- method in this implementation
...
123 |     pub(crate) fn root(&self) -> &Path {
    |                   ^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: `bob-cli` (lib) generated 3 warnings
warning: `bob-cli` (lib test) generated 1 warning
    Finished `test` profile [unoptimized + debuginfo] target(s) in 49.27s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws10-260928_071954/build/debug/deps/bob_cli-8509342c1f2f8320)

running 963 tests
test native::capture::tests::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::tests::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::tests::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::clip_markers_are_terminal_forgiving_and_can_be_disabled ... ok
test native::capture::tests::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::tests::forced_route_rejects_terminal_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::formats_bullet_line ... ok
test native::capture::tests::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::formats_scheduled_date_from_offset ... ok
test native::capture::tests::formats_sub_bullet_line ... ok
test native::capture::tests::formats_task_line ... ok
test native::capture::tests::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::inserts_after_single_top_level_task ... ok
test native::capture::tests::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::legacy_standalone_bullet_markers_are_rejected ... ok
test native::capture::tests::json_success_shape_is_stable ... ok
test native::capture::tests::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::tests::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::tests::parses_picker_task_refs_strictly ... ok
test native::capture::tests::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::normalizes_whitespace ... ok
test native::capture::tests::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::tests::parses_priority_tokens ... ok
test native::capture::tests::parses_schedule_tokens ... ok
test native::capture::tests::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::tests::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::tests::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started_pomodoro_move_preserves_crlf ... ok
test native::capture::tests::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::tests::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::tests::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture::tests::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture::tests::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_clip::tests::formats_headers ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_complete::tests::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture_complete::tests::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_complete::tests::all_tasks_does_not_change_pomodoro_completion ... ok
test native::capture_complete::tests::empty_json_context_is_null ... ok
test native::capture_complete::tests::default_task_completion_stays_identified_only ... ok
test native::capture_complete::tests::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::all_tasks_lists_identified_tasks_before_unidentified_tasks ... ok
test native::capture_complete::tests::json_shape_is_stable ... ok
test native::capture_complete::tests::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_complete::tests::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_complete::tests::all_tasks_search_keeps_identified_groups_ahead_of_unidentified ... ok
test native::capture_complete::tests::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture_complete::tests::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture_complete::tests::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture_complete::tests::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture_complete::tests::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_complete::tests::pomodoro_name_completion_offers_creation_before_substring_and_nameable_rows ... ok
test native::capture_complete::tests::pomodoro_name_completion_suppresses_creation_for_open_name_matches ... ok
test native::capture_complete::tests::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture_complete::tests::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_complete::tests::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_complete::tests::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::active_task_human_rows_name_the_queue ... ok
test native::capture_complete::tests::task_block_id_completion_offers_routes_but_not_authored_ids ... ok
test native::capture_complete::tests::task_section_completion_empty_block_id_is_an_empty_success ... ok
test native::capture_complete::tests::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_complete::tests::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_complete::tests::task_completion_before_an_explicit_toggle_bang_does_not_replace_the_bang ... ok
test native::capture_complete::tests::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_complete::tests::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_complete::tests::task_section_completion_lists_ranked_slugs_for_the_parent_task ... ok
test native::capture_complete::tests::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_complete::tests::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_language::tests::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_complete::tests::task_section_completion_warns_once_for_an_unresolvable_parent ... ok
test native::capture_language::tests::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion_on_a_global_declaration_excludes_both_sigils_and_plus ... ok
test native::capture_language::tests::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_complete::tests::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture_language::tests::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_complete::tests::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_language::tests::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_language::tests::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::editor_reports_legacy_bullet_markers_without_failing ... ok
test native::capture_language::tests::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::empty_block_id_with_section_still_yields_a_task_section_field ... ok
test native::capture_language::tests::empty_selector_after_hash_is_a_zero_length_task_section_field ... ok
test native::capture_language::tests::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::execution_inherits_a_global_sub_bullet_and_keeps_authored_children ... ok
test native::capture_language::tests::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::execution_parses_project_note_markers ... ok
test native::capture_language::tests::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::hash_separator_is_not_part_of_block_id_or_section_replacement ... ok
test native::capture_language::tests::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_language::tests::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture_language::tests::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_language::tests::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::rewrite_draft_absorbs_a_sub_bullet_local_marker ... ok
test native::capture_language::tests::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_language::tests::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_language::tests::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_language::tests::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::task_section_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::task_block_id_route_completes_but_authored_id_does_not ... ok
test native::capture_language::tests::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_a_global_sub_bullet_declaration_and_local_override ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_invalid_start_suffixes_as_diagnostics ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_dated_work_logs ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::pomodoro_link_uses_next_status_unless_scheduled ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::section_title_shape_rejects_mixed_case_and_banners ... ok
test native::capture_project_note::tests::scheduled_date_lands_in_frontmatter_with_a_blocked_checkbox ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_rewrite::tests::json_reports_a_task_toggle_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... FAILED
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_task_sections::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_sections::tests::checkboxed_all_caps_children_are_not_sections ... ok
test native::capture_task_sections::tests::empty_section_bullet_still_qualifies ... ok
test native::capture_task_sections::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_task_sections::tests::grandchild_is_not_a_direct_child_section ... ok
test native::capture_task_sections::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_task_sections::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_task_sections::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_task_sections::tests::lists_sections_in_document_order_for_a_block_id ... ok
test native::capture_task_sections::tests::managed_logs_are_never_sections_plain_titles_are ... ok
test native::capture_task_sections::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::capture_task_sections::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_task_sections::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_task_sections::tests::resolved_task_with_no_sections_is_a_successful_empty_list ... ok
test native::capture_task_sections::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_task_sections::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_task_sections::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_task_sections::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_task_sections::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_task_sections::tests::title_whitelist_edges ... ok
test native::capture_task_toggle::tests::errors_on_multiple_open_timed_entries ... ok
test native::capture_task_toggle::tests::errors_when_no_pomodoros_section ... ok
test native::capture_task_toggle::tests::errors_when_no_eligible_open_entry ... ok
test native::capture_task_toggle::tests::idempotent_insertion_skips_when_already_linked ... ok
test native::capture_task_toggle::tests::implicit_insertion_falls_back_to_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::implicit_insertion_targets_single_open_timed_entry ... ok
test native::capture_task_toggle::tests::insertion_removes_duplicate_from_later_open_entry ... ok
test native::capture_task_toggle::tests::invalid_pomodoro_name_is_rejected ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::blocked_is_forced_to_next ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_task_toggle::tests::plan_task_open_sets_ready_status_only ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::collect_done::tests::adds_archive_parent_to_existing_frontmatter ... ok
test native::collect_done::tests::adds_done_tasks_to_existing_source_frontmatter ... ok
test native::collect_done::tests::below_threshold_block_ids_do_not_trigger_link_repair ... ok
test native::collect_done::tests::block_id_deduplication_preserves_crlf_line_endings ... ok
test native::collect_done::tests::already_linked_source_with_existing_archive_is_not_planned ... ok
test native::collect_done::tests::block_ids_are_only_end_of_line_obsidian_anchors ... ok
test native::collect_done::tests::canceled_only_tasks_below_threshold_remain_in_source ... ok
test native::collect_done::tests::canceled_only_tasks_move_when_threshold_is_met ... ok
test native::collect_done::tests::collecting_tasks_adds_done_tasks_to_source ... ok
test native::collect_done::tests::completed_child_moves_without_collecting_active_parent ... ok
test native::collect_done::tests::creates_archive_frontmatter_for_new_archive_note ... ok
test native::collect_done::tests::creates_archive_frontmatter_with_nested_source_parent ... ok
test native::collect_done::tests::creates_source_frontmatter_for_done_tasks ... ok
test native::collect_done::tests::dependency_ids_preserve_path_case_and_qualify_nested_notes ... ok
test native::collect_done::tests::block_id_suffix_selection_preserves_distinct_moved_ids ... ok
test native::collect_done::tests::block_id_suffix_selection_skips_existing_candidates ... ok
test native::collect_done::tests::dependency_metadata_repair_rewrites_exact_tokens_only ... ok
test native::collect_done::tests::duplicate_moved_block_ids_are_ambiguous ... ok
test native::collect_done::tests::duplicate_moved_block_ids_become_unique_archive_ids ... ok
test native::collect_done::tests::duplicate_moved_block_ids_do_not_rewrite_links ... ok
test native::collect_done::tests::dependency_metadata_repair_supports_task_field_grammar_and_skips_code ... ok
test native::collect_done::tests::existing_archive_block_ids_reserve_original_ids ... ok
test native::collect_done::tests::existing_archive_creates_metadata_only_source_update ... ok
test native::collect_done::tests::extracts_block_ids_from_every_moved_task_block_line ... ok
test native::collect_done::tests::extracts_nested_blocks_and_continuations ... ok
test native::collect_done::tests::existing_archive_with_stale_metadata_creates_archive_only_plan ... ok
test native::collect_done::tests::includes_nested_path_note_when_it_meets_threshold ... ok
test native::collect_done::tests::generated_and_template_directories_are_not_collected_or_repaired ... ok
test native::collect_done::tests::inserts_missing_archive_type_frontmatter ... ok
test native::collect_done::tests::leaves_correct_archive_frontmatter_unchanged ... ok
test native::collect_done::tests::generated_tag_pages_do_not_make_source_basename_ambiguous ... ok
test native::collect_done::tests::leaves_ambiguous_basename_links_unchanged ... ok
test native::collect_done::tests::leaves_correct_done_tasks_frontmatter_unchanged ... ok
test native::collect_done::tests::maps_archive_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::maps_source_notes_to_archive_notes ... ok
test native::collect_done::tests::maps_source_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::link_repair_uses_renamed_unique_moved_block_id ... ok
test native::collect_done::tests::link_repair_scan_includes_done_notes ... ok
test native::collect_done::tests::markdown_repair_skips_wikilink_spans ... ok
test native::collect_done::tests::parses_attached_short_threshold_option ... ok
test native::collect_done::tests::parses_default_threshold ... ok
test native::collect_done::tests::missing_archive_without_threshold_tasks_is_not_planned ... ok
test native::collect_done::tests::parses_short_threshold_equals_option ... ok
test native::collect_done::tests::parses_short_threshold_option ... ok
test native::collect_done::tests::parses_threshold_option ... ok
test native::collect_done::tests::parses_threshold_equals_option ... ok
test native::collect_done::tests::prepends_archive_frontmatter_when_existing_note_has_none ... ok
test native::collect_done::tests::preserves_crlf_when_adding_done_tasks_frontmatter ... ok
test native::collect_done::tests::planned_source_and_archive_contents_are_link_repaired ... ok
test native::collect_done::tests::preserves_crlf_when_repairing_archive_frontmatter ... ok
test native::collect_done::tests::preserves_line_endings_in_source_and_archive ... ok
test native::collect_done::tests::recognizes_done_and_canceled_task_lines_only ... ok
test native::collect_done::tests::rejects_zero_threshold ... ok
test native::collect_done::tests::repairs_same_note_nested_and_unique_basename_links ... ok
test native::collect_done::tests::repairs_simple_markdown_inline_block_links ... ok
test native::collect_done::tests::repairs_wikilinks_embeds_and_aliases_to_moved_blocks ... ok
test native::collect_done::tests::replaces_stale_archive_type_frontmatter ... ok
test native::collect_done::tests::replaces_stale_done_tasks_frontmatter ... ok
test native::collect_done::tests::scans_markdown_files_with_exclusions_and_threshold ... ok
test native::collect_done::tests::self_heals_preexisting_block_links_to_archive ... ok
test native::collect_done::tests::source_block_id_keeps_links_pointing_at_source ... ok
test native::collect_done::tests::task_moving_plan_repairs_links_in_separate_notes ... ok
test native::collect_done::tests::task_moving_plan_writes_archive_with_nested_source_parent ... ok
test native::collect_done::tests::unqualifiable_paths_do_not_abort_identity_indexing ... ok
test native::collect_done::tests::updates_existing_archive_parent_frontmatter ... ok
test native::config::tests::blank_highlights_pre_scan_hook_disables_file_hook ... ok
test native::config::tests::parses_absent_highlights_config_as_none ... ok
test native::config::tests::parses_deployed_config ... ok
test native::config::tests::parses_highlights_pre_scan_hook ... ok
test native::config::tests::rejects_blank_label ... ok
test native::config::tests::rejects_blank_value ... ok
test native::config::tests::rejects_empty_levels ... ok
test native::config::tests::rejects_legacy_highlights_pre_scan_command ... ok
test native::config::tests::rejects_min_greater_than_max ... ok
test native::config::tests::rejects_missing_priority_property ... ok
test native::config::tests::rejects_missing_schedules ... ok
test native::config::tests::rejects_missing_value ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::config::tests::rejects_negative_min_days ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::config::tests::resolve_config_path_expands_tilde_in_xdg_config_home ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::config::tests::resolve_config_path_falls_back_to_home_dot_config ... ok
test native::collect_done::tests::self_healing_is_idempotent_after_links_are_repaired ... ok
test native::config::tests::resolve_config_path_falls_back_to_xdg_config_home ... ok
test native::config::tests::rejects_non_integer_min_days ... ok
test native::config::tests::rejects_wrong_schedules_target ... ok
test native::config::tests::rejects_value_containing_field_syntax ... ok
test native::config::tests::resolve_config_path_ignores_empty_env_values ... ok
test native::collect_done::tests::task_moves_repair_dependency_ids_in_archive_and_all_dependents ... ok
test native::config::tests::resolve_config_path_prefers_bob_config_file ... ok
test native::config::tests::roll_offset_p4_window_hits_both_extremes ... ok
test native::config::tests::roll_offset_returns_fixed_value_when_min_equals_max ... ok
test native::dataview::tasks::filter::tests::global_filter_removal_only_removes_the_first_occurrence ... ok
test native::dataview::tasks::filter::tests::absolute_ranges_are_inclusive_and_order_independent ... ok
test native::dataview::tasks::filter::tests::numbered_ranges_cover_year_month_quarter_and_iso_week ... ok
test native::dataview::tasks::filter::tests::relative_ranges_use_iso_weeks_and_calendar_boundaries ... ok
test native::config::tests::tolerates_unusual_sibling_properties ... ok
test native::dataview::tasks::filter::tests::weekday_and_offset_dates_are_pinned_to_now ... ok
test native::dataview::tasks::index::tests::heading_parser_supports_atx_and_setext_headings ... ok
test native::dataview::tasks::parse::tests::boolean_chains_use_tasks_precedence_and_allow_operand_apostrophes ... ok
test native::dataview::tasks::parse::tests::numbered_date_ranges_optional_priority_is_and_status_boundary_parse ... ok
test native::dataview::tasks::parse::tests::ignore_global_query_can_come_from_query_file_defaults ... ok
test native::dataview::tasks::parse::tests::parses_every_filter_family_and_boolean_combinations ... ok
test native::dataview::tasks::parse::tests::parses_every_v8_sort_group_and_layout_key ... ok
test native::dataview::tasks::parse::tests::rejects_malformed_filters_with_actionable_errors ... ok
test native::dataview::tasks::parse::tests::scanner_matches_tasks_line_continuation_rules ... ok
test native::dataview::tasks::result::tests::explanations_include_expanded_preset_statements ... ok
test native::dataview::tasks::result::tests::natural_collation_is_case_insensitive_and_numeric ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::dataview::tasks::settings::tests::unknown_task_format_falls_back_to_emoji ... ok
test native::dataview::tasks::parse::tests::composes_global_defaults_presets_and_placeholders_in_order ... ok
test native::dataview::tasks::filter::tests::regex_flags_match_javascript_filtering_behavior ... ok
test native::dataview::tasks::task::tests::file_context_matches_tasks_expose_properties ... ok
test native::dataview::tasks::task::tests::dataview_fields_honor_delimiters_whitespace_commas_and_case ... ok
test native::dataview::tasks::task::tests::dataview_parser_extracts_all_fields_and_cleans_description ... ok
test native::dataview::tasks::task::tests::invalid_dates_and_recurrences_match_tasks_semantics ... ok
test native::dataview::tasks::task::tests::removing_global_filter_preserves_spacing_and_only_removes_first_word ... ok
test native::dataview::tasks::task::tests::recurrence_rules_are_validated_and_standardized ... ok
test native::dataview::tasks::task::tests::metadata_must_be_trailing_but_tags_can_be_interleaved ... ok
test native::dataview::tasks::task::tests::task_line_parser_matches_tasks_markers_and_spacing ... ok
test native::dataview::tasks::task::tests::urgency_due_scheduled_and_start_boundaries_match_tasks_v8 ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_from_nested_blockquotes_and_callouts ... ok
test native::dataview::tasks::task::tests::urgency_matches_tasks_v8_coefficients ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_with_heading_context ... ok
test native::dataview::tests::dql_grouped_table_rows_warn_and_fail_when_strict ... ok
test native::dataview::tasks::task::tests::unknown_status_is_todo_and_remove_global_filter_is_display_only ... ok
test native::dataview::tests::dql_list_paths_use_list_pair_identity ... ok
test native::dataview::tests::dql_missing_table_identities_warn_per_row ... ok
test native::dataview::tests::dql_table_paths_use_first_identity_column ... ok
test native::dataview::tasks::index::tests::fixture_index_builds_hierarchy_and_ignores_fences_and_dot_directories ... ok
test native::dataview::tests::dql_task_paths_resolve_grouped_task_source_notes ... ok
test native::dataview::tests::native_dql_parser_reports_representative_invalid_queries ... ok
test native::dataview::tests::native_dql_parser_accepts_phase3_command_surface ... ok
test native::dataview::tests::native_source_parser_accepts_phase3_source_surface ... ok
test native::dataview::tests::source_paths_are_normalized_and_deduplicated ... ok
test native::highlights_ref::create::tests::exact_external_target_does_not_invent_library_destination ... ok
test native::highlights_ref::create::tests::exact_intake_refuses_mirrored_library_sidecar ... ok
test native::highlights_ref::create::tests::exact_intake_still_refuses_mirrored_library_pdf_with_force ... ok
test native::highlights_ref::create::tests::exact_library_target_requires_force_and_skips_mirrored_check ... ok
test native::highlights_ref::create::tests::exact_output_accepts_uppercase_pdf_extension ... ok
test native::highlights_ref::create::tests::exact_output_classifies_direct_library_target ... ok
test native::highlights_ref::create::tests::exact_output_keeps_nested_path_and_filename ... ok
test native::highlights_ref::create::tests::exact_output_does_not_treat_sibling_prefix_as_managed ... ok
test native::highlights_ref::create::tests::exact_output_refuses_same_stem_markdown_sidecar_even_with_force ... ok
test native::highlights_ref::create::tests::exact_output_resolves_relative_and_tilde_paths ... ok
test native::highlights_ref::create::tests::marker_rejects_wikilink_parent_and_unknown_status ... ok
test native::highlights_ref::create::tests::normalize_lexically_drops_dot_and_parent_components ... ok
test native::highlights_ref::create::tests::plan_derives_ref_type_output_and_valid_marker ... ok
test native::highlights_ref::create::tests::exact_output_rejects_non_pdf_paths ... ok
test native::highlights_ref::create::tests::plan_embeds_markdown_stem_id_when_opted_in ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_library_sidecar ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_library_pdf_even_with_force ... ok
test native::highlights_ref::create::tests::title_prefers_frontmatter_then_h1_then_stem ... ok
test native::highlights_ref::create::tests::plan_refuses_highlights_markdown_sidecar_even_with_force ... ok
test native::highlights_ref::create::tests::plan_refuses_existing_pdf_without_force ... ok
test native::highlights_ref::tests::annotation_block_id_is_stable_across_space_wrapping ... ok
test native::highlights_ref::tests::annotation_task_batches_append_in_insertion_order ... ok
test native::highlights_ref::tests::annotation_task_candidate_records_route_and_processed_id ... ok
test native::highlights_ref::tests::annotation_task_insertion_preserves_crlf_line_endings ... ok
test native::highlights_ref::tests::annotation_task_insertion_is_idempotent_and_preserves_existing_states ... ok
test native::highlights_ref::tests::annotation_task_candidates_extract_from_comments_and_notes ... ok
test native::highlights_ref::tests::annotation_task_route_suffix_is_strict_and_stripped_from_identity ... ok
test native::highlights_ref::tests::annotation_tasks_append_to_existing_tasks_section ... ok
test native::highlights_ref::tests::annotation_tasks_create_section_after_unterminated_ref_line ... ok
test native::highlights_ref::tests::annotation_tasks_fill_empty_tasks_section_with_blank_lines ... ok
test native::highlights_ref::tests::annotation_tasks_ignore_fenced_and_managed_tasks_headings ... ok
test native::highlights_ref::tests::beautify_annotation_text_preserves_list_structure ... ok
test native::highlights_ref::tests::annotation_tasks_reuse_h1_or_closed_atx_tasks_heading ... ok
test native::highlights_ref::tests::beautify_annotation_text_reflows_and_dehyphenates ... ok
test native::highlights_ref::tests::deprecated_statuses_normalize_for_synced_inputs ... ok
test native::highlights_ref::tests::frontmatter_projection_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::frontmatter_projection_uses_marker_fields_without_fallback_parent ... ok
test native::highlights_ref::tests::frontmatter_render_preserves_unmanaged_keys ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_conflicts_with_competing_edit ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_contributes_abandoned ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_maps_all_lifecycle_states ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_promotes_ready_and_back ... ok
test native::highlights_ref::tests::highlights_ref_pdf_task_status_signal_ready_reopens_terminal_to_ready ... ok
test native::highlights_ref::tests::highlights_ref_task_line_parser_recognizes_generated_pdf_task ... ok
test native::highlights_ref::tests::highlights_ref_task_checkbox_rewrite_and_dirty_allowance_are_narrow ... ok
test native::highlights_ref::tests::highlights_ref_task_line_parser_rejects_malformed_and_duplicate_tasks ... ok
test native::highlights_ref::tests::linked_sidecar_parser_keeps_wrapped_quotes_and_marker_mirror ... ok
test native::highlights_ref::tests::marker_content_decoder_preserves_pdfdoc_line_separators ... ok
test native::highlights_ref::tests::linked_sidecar_parser_strips_comment_bullet_markers ... ok
test native::highlights_ref::tests::image_block_id_is_stable_across_asset_renames ... ok
test native::highlights_ref::tests::marker_parser_accepts_yaml_subset_and_normalizes_keys ... ok
test native::highlights_ref::tests::marker_parser_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker_parser_rejects_linked_parent_targets ... ok
test native::highlights_ref::tests::marker_parser_rejects_missing_required_keys_type_and_duplicate_status ... ok
test native::highlights_ref::tests::marker_renderer_rejects_unrepresentable_parent_links ... ok
test native::highlights_ref::tests::marker_renderer_uses_stable_key_order ... ok
test native::highlights_ref::tests::missing_image_asset_error_points_at_textbundle_export ... ok
test native::highlights_ref::tests::parent_canonicalization_rejects_non_scalar_values ... ok
test native::highlights_ref::tests::pdf_path_metadata_derives_nested_reference_paths ... ok
test native::highlights_ref::tests::pdf_text_artifact_cleanup_normalizes_extraction_noise ... ok
test native::highlights_ref::tests::pipeline_fields_exclude_marker_user_projection ... ok
test native::highlights_ref::tests::processed_task_index_legacy_ht_backlink_blocks_edited_recreation ... ok
test native::highlights_ref::tests::plan_xlib_intake_maps_nested_paths_and_companions ... ok
test native::highlights_ref::tests::plan_xlib_intake_reports_every_destination_conflict ... ok
test native::highlights_ref::tests::processed_task_index_legacy_identity_blocks_recreation ... ok
test native::highlights_ref::tests::processed_task_index_scans_states_indents_and_done_notes ... ok
test native::highlights_ref::tests::projection_three_way_merge_handles_compatible_changes ... ok
test native::highlights_ref::tests::projection_snapshot_json_round_trips_compact_user_projection ... ok
test native::highlights_ref::tests::projection_three_way_merge_handles_deletes_and_conflicts ... ok
test native::config::tests::roll_offset_stays_within_bounds_for_many_seeds ... ok
test native::highlights_ref::tests::relative_config_paths_resolve_under_bob_dir ... ok
test native::highlights_ref::tests::sidecar_page_heading_extracts_linked_page_label ... ok
test native::highlights_ref::tests::render_sidecar_highlights_beautifies_callout_text ... ok
test native::highlights_ref::tests::rendered_annotation_blocks_do_not_include_source_task_anchors ... ok
test native::highlights_ref::tests::render_sidecar_highlights_renders_image_assets_and_tasks ... ok
test native::highlights_ref::tests::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::tests::simple_sidecar_unlabeled_text_after_quote_remains_comment ... ok
test native::highlights_ref::tests::sidecar_parser_extracts_image_annotations_and_leaves_non_images_as_notes ... ok
test native::highlights_ref::tests::status_validation_rejects_unsupported_and_non_scalar_values ... ok
test native::highlights_ref::tests::validate_library_layout_rejects_equal_and_nested_paths ... ok
test native::markdown::tests::blockquote_and_indented_code_detection ... ok
test native::markdown::tests::setext_underline_accepts_levels_and_indent ... ok
test native::markdown::tests::split_line_ending_preserves_crlf_lf_and_none ... ok
test native::markdown::tests::standalone_html_comment_reads_inner_text ... ok
test native::note_tasks::tests::block_id_lookup_distinguishes_found_non_task_duplicate_and_missing ... ok
test native::note_tasks::tests::ignores_frontmatter_and_fenced_code_tasks ... ok
test native::note_tasks::tests::computes_child_spans_for_mixed_indentation_blanks_and_eof ... ok
test native::note_tasks::tests::refs_resolve_exact_shifted_stale_and_ambiguous_tasks ... ok
test native::note_tasks::tests::gates_on_filter_and_cleans_descriptions_with_sections ... ok
test native::note_tasks::tests::suggests_case_matches_and_unique_nearby_block_ids_only ... ok
test native::note_tasks::tests::task_refs_parse_strictly_and_round_trip_scan_metadata ... ok
test native::note_tasks::tests::reads_real_statuses_and_missing_settings_fall_back_to_defaults ... ok
test native::plugins::tests::json_shape_is_stable ... ok
test native::plugins::tests::scan_reports_states_and_counts ... ok
test native::plugins::tests::backup_failure_aborts_overwrite ... ok
test native::plugins::tests::sync_dry_run_reports_without_writing ... ok
test native::plugins::tests::sync_only_filters_to_a_single_plugin ... ok
test native::dataview::tasks::task::tests::all_priorities_have_tasks_v8_names_numbers_and_scores ... ok
test native::dataview::tasks::index::tests::paragraphs_break_list_hierarchy ... ok
test native::plugins::tests::sync_reports_text_diff_for_changed_files ... ok
test native::plugins::tests::pull_repo_skips_non_git_directory ... ok
test native::plugins::tests::sync_summarizes_binary_and_minified_diffs ... ok
test native::plugins::tests::sync_state_detects_synced_drift_and_missing ... ok
test native::plugins::tests::sync_unknown_plugin_is_an_error ... ok
test native::plugins::tests::truncate_adds_ellipsis_only_when_needed ... ok
test native::plugins::tests::unreadable_repo_is_an_error ... ok
test native::dataview::tasks::index::tests::dependency_graph_matches_direct_tasks_v8_semantics ... ok
test native::plugins::tests::vault_state_reads_enabled_disabled_and_not_installed ... ok
test native::pomodoro::tests::completed_ledger_parser_only_accepts_x_checkbox_entries ... ok
test native::pomodoro::tests::open_ledger_parser_requires_an_open_checkbox ... ok
test native::plugins::tests::sync_creates_updates_and_leaves_unchanged ... ok
test native::pomodoro::tests::unclosed_frontmatter_delimiter_is_content ... ok
test native::projects::tests::non_project_notes_are_ignored ... ok
test native::projects::tests::project_changes_clean_duplicate_subproject_marker_lines ... ok
test native::projects::tests::project_changes_delete_subproject_line_for_stale_child ... ok
test native::projects::tests::project_changes_insert_subproject_line_above_user_bullets ... ok
test native::projects::tests::project_changes_insert_subproject_links_after_final_prj_line ... ok
test native::projects::tests::project_changes_insert_subproject_links_after_prj_with_tab_indent ... ok
test native::projects::tests::project_changes_preserve_crlf_for_subproject_link_insertions ... ok
test native::projects::tests::project_changes_mark_last_child_closed_and_keep_subproject_line ... ok
test native::projects::tests::project_changes_preserve_crlf_when_appending_status ... ok
test native::projects::tests::project_changes_remove_prj_hide_tag_with_crlf ... ok
test native::projects::tests::project_changes_remove_prj_fields_with_adjacent_whitespace ... ok
test native::projects::tests::frontmatter_keys_must_start_at_column_zero ... ok
test native::projects::tests::project_changes_rewrite_subproject_line_in_place ... ok
test native::projects::tests::project_changes_replace_status_append_missing_status_and_add_hide_tag ... ok
test native::projects::tests::project_parser_accepts_project_type_variants_and_counts_tasks ... ok
test native::projects::tests::project_parser_marks_unprioritized_prj_as_on_dash ... ok
test native::dataview::tasks::task::tests::emoji_parser_extracts_all_fields_and_variant_selectors ... ok
test native::dataview::tasks::index::tests::frontmatter_is_only_a_strictly_closed_column_zero_block ... ok
test native::projects::tests::project_parser_records_prj_sub_block_marker_lines ... ok
test native::projects::tests::project_parser_accepts_bare_project_type_and_prj_states ... ok
test native::projects::tests::project_parser_accepts_prj_tag_and_strips_it_from_description ... ok
test native::projects::tests::project_parser_reads_parent_wikilink_target ... ok
test native::plugins::tests::sync_preserves_runtime_data_json ... ok
test native::projects::tests::project_parser_records_scheduled_and_placeholder_prj ... ok
test native::highlights_ref::create::tests::code_break_filter_splits_long_inline_code_paths ... ok
test native::projects::tests::project_parser_splits_surfacing_and_dash_visibility_counts ... ok
test native::projects::tests::project_parser_stops_prj_sub_block_at_blank_line ... ok
test native::projects::tests::project_sync_plan_flips_status_without_prj_edits_after_effective_status ... ok
test native::projects::tests::project_parser_reports_malformed_and_multiple_prj_lines ... ok
test native::projects::tests::project_sync_plan_keeps_canonical_closed_subprojects_idempotent ... ok
test native::projects::tests::project_sync_plan_marks_tracked_closed_subprojects ... ok
test native::projects::tests::project_sync_plan_is_idempotent_when_prj_hide_tag_matches_dash_state ... ok
test native::projects::tests::project_sync_plan_matches_subproject_links_case_insensitively ... ok
test native::projects::tests::project_sync_plan_leaves_non_terminal_open_prj_status_untouched ... ok
test native::projects::tests::project_sync_plan_reconciles_subprojects_marker_line ... ok
test native::projects::tests::project_schedule_accepts_quoted_dates_and_rejects_bad_dates ... ok
test native::projects::tests::project_sync_plan_removes_stale_scheduled_field ... ok
test native::projects::tests::project_sync_plan_manages_prj_hide_tag_from_open_subprojects ... ok
test native::projects::tests::project_sync_plan_normalizes_subprojects_marker_drift ... ok
test native::projects::tests::render_subprojects_line_formats_closed_children_after_open_children ... ok
test native::projects::tests::schedule_only_issues_still_allow_subproject_aggregation ... ok
test native::projects::tests::project_sync_plan_reconciles_subproject_schedule_markers ... ok
test native::projects::tests::project_sync_plan_manages_prj_hide_tag_from_unhidden_count ... ok
test native::projects::tests::subproject_display_parser_scopes_schedule_and_lifecycle_markers ... ok
test native::projects::tests::project_sync_plan_treats_user_sub_bullets_as_user_owned ... ok
test native::projects::tests::scheduled_tasks_keep_subproject_ledger_planning ... ok
test native::projects::tests::task_schedule_edits_cover_contract_and_preserve_markdown ... ok
test native::projects::tests::project_sync_plan_reopens_terminal_project_from_open_prj ... ok
test native::projects::tests::project_sync_plan_warns_on_placeholder_while_reopening ... ok
test native::projects::tests::task_tag_matches_tasks_plugin_boundaries ... ok
test native::projects::tests::wikilink_target_extracts_normalized_note_names ... ok
test native::task_status_groups::tests::authored_heading_inside_a_managed_group_fails_closed ... ok
test native::projects::tests::scheduled_tasks_precede_prj_surfacing_at_local_date_boundary ... ok
test native::task_status_groups::tests::badge_anchors_percent_encode_the_obsidian_path_segments ... ok
test native::projects::tests::subproject_state_treats_terminal_open_prj_child_as_open ... ok
test native::task_status_groups::tests::authored_child_containers_get_independent_badges_and_anchors ... ok
test native::projects::tests::terminal_projects_do_not_reconcile_task_schedules ... ok
test native::task_status_groups::tests::badge_row_is_not_a_task_or_ambiguous_boundary ... ok
test native::task_status_groups::tests::badge_counts_refresh_when_membership_changes ... ok
test native::task_status_groups::tests::conservation_and_source_records ... ok
test native::task_status_groups::tests::authored_topics_receive_local_groups ... ok
test native::task_status_groups::tests::blockless_and_duplicate_ids_still_group ... ok
test native::task_status_groups::tests::badge_marker_in_intake_is_relocated_to_the_slot ... ok
test native::task_status_groups::tests::empty_global_filter_accepts_all_checkbox_tasks ... ok
test native::projects::tests::project_sync_plan_skips_subproject_links_without_open_prj_edits ... ok
test native::task_status_groups::tests::custom_terminal_statuses_and_registry_precedence ... ok
test native::task_status_groups::tests::crlf_mixed_endings_unicode_and_missing_final_newline ... ok
test native::task_status_groups::tests::h6_tasks_is_skipped_with_a_diagnostic ... ok
test native::task_status_groups::tests::global_filter_rejects_non_matching_lines ... ok
test native::task_status_groups::tests::heading_hash_in_ancestry_renders_unlinked_badges ... ok
test native::task_status_groups::tests::heading_only_first_setup_is_a_change ... ok
test native::task_status_groups::tests::lazy_continuation_skips_the_container ... ok
test native::task_status_groups::tests::excluded_markdown_contexts_are_not_task_roots_or_headings ... ok
test native::projects::tests::subproject_aggregation_marks_only_schedules_after_shared_today ... ok
test native::task_status_groups::tests::malformed_badge_markers_fail_closed ... ok
test native::task_status_groups::tests::empty_groups_are_retained_once_created ... ok
test native::task_status_groups::tests::malformed_and_duplicate_markers_fail_closed ... ok
test native::task_status_groups::tests::golden_layout_groups_every_status_bucket_and_keeps_ready_intake ... ok
test native::task_status_groups::tests::orphaned_badge_block_is_removed_without_creating_groups ... ok
test native::task_status_groups::tests::ordered_list_roots_and_nested_ordinary_items_are_reported ... ok
test native::task_status_groups::tests::nested_children_travel_with_parent_status ... ok
test native::task_status_groups::tests::ready_only_and_empty_sections_are_not_decorated ... ok
test native::task_status_groups::tests::nested_tasks_is_processed_once ... ok
test native::task_status_groups::tests::skip_codes_are_stable ... ok
test native::task_status_groups::tests::out_of_scope_spans_are_byte_identical ... ok
test native::task_status_groups::tests::prose_inside_managed_groups_is_preserved ... ok
test native::task_status_groups::tests::safe_legacy_adoption_completes_a_partial_set ... ok
test native::task_status_groups::tests::unmarked_group_title_with_prose_is_a_collision ... ok
test native::task_status_groups::tests::reopening_a_task_to_ready_appends_to_intake ... ok
test native::task_status_hooks::tests::allowed_transient_reasons_are_retried_without_applied_files ... ok
test native::task_status_groups::tests::multiple_tasks_headings_and_heading_syntax_variants ... ok
test native::task_status_hooks::tests::ambiguous_basename_does_not_resolve ... ok
test native::task_status_hooks::tests::any_error_listing_applied_files_is_never_retried ... ok
test native::task_status_groups::tests::standalone_prose_is_not_attached_to_a_task ... ok
test native::task_status_hooks::tests::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_groups::tests::tabs_internal_blanks_and_fences_stay_in_the_task_block ... ok
test native::task_status_hooks::tests::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::task_status_hooks::tests::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::tests::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::tests::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::task_status_hooks::tests::dependency_reference_requires_a_sole_transcluded_block_link ... ok
test native::task_status_hooks::tests::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::tests::direct_child_scan_counts_plain_children_but_ignores_fences ... ok
test native::task_status_hooks::tests::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::empty_pomodoro_deletion_removes_full_blocks_and_preserves_crlf_eof ... ok
test native::task_status_hooks::tests::empty_timed_entries_are_not_current_targets_or_ambiguity_inputs ... ok
test native::task_status_hooks::tests::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::extracts_only_block_links_under_open_pomodoros ... ok
test native::task_status_hooks::tests::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::entries_emptied_by_duplicate_cleanup_are_removed_in_same_pass ... ok
test native::task_status_hooks::tests::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::tests::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::task_status_hooks::tests::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::moving_last_child_removes_source_but_retains_destination ... ok
test native::task_status_hooks::tests::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::tests::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::random_unit_interval_varies_and_stays_in_unit_range ... ok
test native::task_status_hooks::tests::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::partial_apply_is_never_retried_even_with_no_applied_files ... ok
test native::task_status_hooks::tests::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::task_status_hooks::tests::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::task_status_hooks::tests::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::retry_ceiling_progression_caps_at_thirty_seconds ... ok
test native::task_status_hooks::tests::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::tests::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::task_status_hooks::tests::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::retry_delay_stays_within_upper_half_of_ceiling ... ok
test native::task_status_hooks::tests::retry_loop_stops_immediately_on_terminal_reason_without_noise ... ok
test native::task_status_hooks::tests::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::task_status_hooks::tests::rolling_reachability_is_cycle_safe_and_includes_dependencies ... ok
test native::task_status_hooks::tests::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::terminal_and_unknown_reasons_are_never_retried ... ok
test native::task_status_hooks::tests::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test native::task_status_hooks::tests::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
warning: You appear to have cloned an empty repository.
test native::task_status_hooks::tests::two_non_empty_timed_entries_still_match_the_ambiguity_guard ... ok
test native::task_status_hooks_write::tests::deletion_prevents_write ... ok
test native::task_status_hooks::tests::retry_loop_with_zero_budget_makes_one_attempt_and_never_sleeps ... ok
test native::task_status_hooks::tests::retry_decision_log_includes_run_attempt_reason_and_recovery_directory ... ok
test native::task_status_hooks::tests::retry_loop_clamps_sleep_to_remaining_budget ... ok
test native::task_status_hooks::tests::retry_loop_retries_lock_contention_then_succeeds ... ok
test native::projects::tests::subproject_parent_links_classify_open_and_terminal_prj_children ... ok
test native::task_status_hooks_write::tests::future_mtime_defers_without_sleeping ... ok
test native::task_status_hooks::tests::retry_loop_never_starts_another_attempt_once_budget_is_exhausted ... ok
test native::task_status_hooks_write::tests::live_rescan_sees_new_vault_file ... ok
test native::task_status_hooks_write::tests::multiply_linked_output_is_rejected ... ok
test native::task_status_hooks_write::tests::new_or_deleted_scan_candidate_invalidates_plan ... ok
test native::task_status_hooks_write::tests::noop_creates_no_recovery_or_staging ... ok
test native::task_status_hooks_write::tests::changed_tasks_settings_prevent_write ... ok
test native::task_status_hooks_write::tests::replacement_inode_prevents_write ... ok
test native::task_status_hooks_write::tests::changed_previous_daily_prevents_write ... ok
test native::task_status_hooks_write::tests::equal_length_change_with_restored_mtime_prevents_write ... ok
test native::task_status_hooks_write::tests::quiet_period_waits_once_then_defers_if_changed ... ok
test native::task_status_hooks_write::tests::symlink_substitution_prevents_write ... ok
test native::plugins::tests::sync_refuses_then_forces_a_dirty_vault_file ... ok
test native::vault_links::tests::basename_walk_skips_hidden_directories ... ok
test native::vault_links::tests::exact_root_note_does_not_build_the_vault_index ... ok
test native::vault_links::tests::resolves_exact_path_before_unique_case_insensitive_basename ... ok
test runner::tests::subcommands_are_sorted_alphabetically ... ok
test runner::tests::build_cli_renders_without_panicking ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::task_status_hooks_write::tests::edit_between_staging_and_revalidate_survives ... ok
test native::task_status_hooks_write::tests::staging_failure_preserves_notes_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::fresh_attempt_after_vault_changed_replans_from_intervening_edit ... ok
test native::task_status_hooks_write::tests::exclusive_temp_and_mode_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::retention_keeps_incomplete_and_prunes_old_completed ... ok
test native::task_status_hooks_write::tests::edit_before_later_replacement_reports_partial ... ok
test native::task_status_hooks_write::tests::unchanged_read_set_applies_and_records_recovery_bytes ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::task_status_hooks_write::tests::quiet_period_skips_wait_for_stable_files_and_status_only ... ok
test native::plugins::tests::pull_repo_fast_forwards_from_remote ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok

failures:

---- native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps stdout ----

thread 'native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps' (792587) panicked at src/native/capture_pomodoro_close.rs:2797:9:
assertion `left == right` failed
  left: Some("- [x] #task T25  [completion:: 2026-09-28] ^t25")
 right: Some("- [x] #task T25 [completion:: 2026-09-28] ^t25")
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace


failures:
    native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps

test result: FAILED. 962 passed; 1 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.64s

error: test failed, to rerun pass `--lib`
failed  exit=101  duration=49997ms

