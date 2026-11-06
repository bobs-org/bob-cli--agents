# Chat History - ace-run (bob-cli-e8.2--mon-3)

- **TIMESTAMP:** 2026-10-29 19:33:05 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-e8.2--mon-3

## Prompt

sase monitor start --command 'cargo test --test cli -- --nocapture' --reason 'Confirm the full-check CLI failures reproduce on clean base commit 53bf3dfa'

## Response

sase tool run 1648725a73fd75fade93fae90499540e
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
   Compiling typenum v1.20.1
   Compiling version_check v0.9.5
   Compiling cfg-if v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
   Compiling equivalent v1.0.2
   Compiling memchr v2.8.1
   Compiling allocator-api2 v0.2.21
   Compiling foldhash v0.2.0
   Compiling autocfg v1.5.1
   Compiling litemap v0.8.3
   Compiling libc v0.2.186
   Compiling writeable v0.6.4
   Compiling simd-adler32 v0.3.9
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
   Compiling cc v1.2.63
   Compiling bitflags v2.12.1
   Compiling serde_core v1.0.228
   Compiling utf8_iter v1.0.4
   Compiling crc32fast v1.5.0
   Compiling adler2 v2.0.1
   Compiling hashbrown v0.17.1
   Compiling getrandom v0.4.2
   Compiling rand_core v0.10.1
   Compiling smallvec v1.15.2
   Compiling utf8parse v0.2.2
   Compiling miniz_oxide v0.8.9
   Compiling anstyle-parse v1.0.0
   Compiling tinyvec_macros v0.1.1
   Compiling num-traits v0.2.19
   Compiling generic-array v0.14.7
   Compiling cpufeatures v0.3.0
   Compiling anstyle-query v1.1.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling serde v1.0.228
   Compiling colorchoice v1.0.5
   Compiling anstyle v1.0.14
   Compiling tinyvec v1.11.0
   Compiling strsim v0.11.1
   Compiling siphasher v1.0.4
   Compiling thiserror v2.0.18
   Compiling cpufeatures v0.2.17
   Compiling flate2 v1.1.9
   Compiling anstream v1.0.0
   Compiling weezl v0.1.12
   Compiling clap_lex v1.1.0
   Compiling zmij v1.0.21
   Compiling itoa v1.0.18
   Compiling unicode-normalization v0.1.25
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling clap_builder v4.6.7
   Compiling phf_shared v0.12.1
   Compiling aho-corasick v1.1.4
   Compiling nom v8.0.0
   Compiling chacha20 v0.10.2
   Compiling fdeflate v0.3.7
   Compiling bytecount v0.6.9
   Compiling indexmap v2.14.0
   Compiling hybrid-array v0.4.12
   Compiling pxfm v0.1.30
   Compiling color_quant v1.1.0
   Compiling byteorder-lite v0.1.0
   Compiling quick-error v2.0.1
   Compiling iana-time-zone v0.1.65
   Compiling unicode-bidi v0.3.18
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling serde_json v1.0.150
   Compiling rquickjs-sys v0.12.1
   Compiling inout v0.1.4
   Compiling digest v0.10.7
   Compiling chrono-tz v0.10.4
   Compiling cipher v0.4.4
   Compiling const-oid v0.10.2
   Compiling unicode-properties v0.1.4
   Compiling percent-encoding v2.3.2
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling regex-syntax v0.8.10
   Compiling zune-core v0.5.3
   Compiling stringprep v0.1.5
   Compiling form_urlencoded v1.2.2
   Compiling aes v0.8.4
   Compiling cbc v0.1.2
   Compiling zune-jpeg v0.5.15
   Compiling ecb v0.1.2
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling chrono v0.4.44
   Compiling image-webp v0.2.4
   Compiling png v0.18.1
   Compiling gif v0.14.2
   Compiling rand v0.10.1
   Compiling phf v0.12.1
   Compiling digest v0.11.3
   Compiling encoding_rs v0.8.35
   Compiling is_executable v1.0.6
   Compiling log v0.4.30
   Compiling unsafe-libyaml v0.2.11
   Compiling ryu v1.0.23
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling bytemuck v1.25.2
   Compiling ttf-parser v0.25.1
   Compiling rangemap v1.7.1
   Compiling synstructure v0.14.0
   Compiling regex-automata v0.4.14
   Compiling moxcms v0.8.1
   Compiling clap v4.6.7
   Compiling clap_complete v4.6.11
   Compiling sha2 v0.11.0
   Compiling fs2 v0.4.3
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/bob-cli-e8.2-cleanbase/crates/bob-obsidian-assets)
   Compiling nom_locate v5.0.0
   Compiling hex v0.4.3
   Compiling similar v2.7.0
   Compiling vcpkg v0.2.15
   Compiling pkg-config v0.3.33
   Compiling rustix v1.1.5
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling time-core v0.1.9
   Compiling num-conv v0.2.2
   Compiling deranged v0.5.8
   Compiling libsqlite3-sys v0.38.1
   Compiling powerfmt v0.2.0
   Compiling linux-raw-sys v0.12.1
   Compiling lopdf v0.40.0
   Compiling zerofrom v0.1.8
   Compiling hashlink v0.12.1
   Compiling quick-xml v0.41.0
   Compiling fallible-iterator v0.3.0
   Compiling regex v1.12.3
   Compiling yoke v0.8.3
   Compiling once_cell v1.21.4
   Compiling fastrand v2.5.0
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling base64 v0.22.1
   Compiling fallible-streaming-iterator v0.1.9
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_locale_core v2.3.0
   Compiling icu_collections v2.3.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling time v0.3.53
   Compiling tempfile v3.27.0
   Compiling icu_provider v2.3.1
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling image v0.25.10
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling plist v1.10.0
   Compiling url v2.5.8
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/target/bob-cli-e8.2-cleanbase)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 3m 24s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws17-261029_192443/build/debug/deps/cli-e2865b96c4cb0370)

running 2442 tests
test aliases::group_help_matches_snapshots_within_80_columns ... ok
test articles::adopt_help_lists_options_alphabetically ... ok
test articles::adopt_previews_without_writing_and_reports_replaced_numbers ... ok
test aliases::tmux_pomodoro_alias_matches_canonical_on_fixture ... ok
test articles::adopt_refuses_other_types_and_tasks ... ok
test aliases::randomize_alias_matches_canonical_dry_run_seed ... ok
test articles::adopt_stdin_json_returns_plan_without_writing ... ok
test articles::adopt_note_completion_is_a_vault_note ... ok
test aliases::notify_alias_matches_canonical_help_and_bad_arity ... ok
test articles::article_help_exposes_the_cli_contract ... ok
test articles::bare_articles_lists_only_marked_notes_and_honors_exclusions ... ok
test articles::adopt_write_inserts_type_and_adopting_twice_is_a_noop ... ok
test articles::all_formats_every_article_and_skips_untyped_notes ... ok
test articles::all_writes_good_articles_when_another_article_is_refused ... ok
test articles::article_note_completion_shows_section_count ... ok
test articles::dry_run_shows_inbound_diffs_without_writing ... ok
test articles::format_reports_unrepairable_inbound_and_resolves_duplicate_titles ... ok
test articles::format_rewrites_inbound_embeds ... ok
test articles::named_non_article_reports_refusal_in_json ... ok
test articles::format_rewrites_inbound_links_in_two_other_notes ... ok
test articles::list_json_keeps_report_fields_but_omits_edits ... ok
test aliases::capture_grammar_does_not_swallow_group_words ... ok
test articles::check_and_dry_run_report_changes_without_writing ... ok
test articles::format_writes_atomically_and_check_is_idempotent ... ok
test articles::outline_json_and_human_show_numbering_and_stubs ... ok
test capture::authored::capture_authored_bullet_marker_on_child_line_configures_whole_capture ... ok
test articles::non_utf8_markdown_does_not_break_list_or_format_all ... ok
test articles::stdin_json_fills_inbound_entries_without_writing ... ok
test capture::authored::capture_authored_bullets_accept_dash_star_and_plus_markers ... ok
test articles::stdin_json_returns_plan_without_writing ... ok
test capture::authored::capture_authored_bullets_duplicate_route_marker_across_lines_is_usage_error ... ok
test articles::unresolved_notes_show_nearby_and_ambiguous_candidates ... ok
test capture::authored::capture_authored_bullets_bullet_capture_uses_section_prefix_with_children ... ok
test aliases::completion_offers_group_members_status_flags_and_alias_options ... ok
test capture::authored::capture_authored_bullets_dry_run_reports_children_without_writing ... ok
test capture::authored::capture_authored_bullets_duplicate_schedule_marker_across_lines_is_usage_error ... ok
test capture::authored::capture_authored_bullets_reject_item_emptied_by_markers ... ok
test capture::authored::capture_authored_bullets_reject_orphaned_nested_lines ... ok
test capture::authored::capture_authored_bullets_preserve_inline_markdown_and_checkbox_text ... ok
test aliases::group_routing_and_help ... ok
test capture::authored::capture_authored_bullets_skip_placeholder_lines ... ok
test capture::authored::capture_authored_bullets_preserve_crlf_line_endings ... ok
test capture::authored::capture_authored_bullets_reject_indented_or_nonbullet_lines ... ok
test capture::authored::capture_authored_bullets_sub_bullet_nests_children_two_levels ... ok
test capture::authored::capture_authored_bullets_use_two_space_target_indentation ... ok
test capture::authored::capture_authored_nested_bullets_render_under_their_owners ... ok
test capture::authored::capture_authored_bullets_pomodoro_linked_capture_includes_children ... ok
test capture::authored::capture_bare_terminal_marker_authored_children_nest_one_level_deeper ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_land_under_the_same_pomodoro_in_order ... ok
test capture::authored::capture_authored_bullets_render_task_with_children_in_order ... ok
test capture::bare::capture_bare_terminal_marker_dry_run_reports_plan_and_writes_nothing ... ok
test capture::bare::capture_bare_terminal_marker_multiple_open_timed_pomodoros_is_io_error ... ok
test aliases::pomodoro_status_forms_match_with_and_without_show_stale ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_stack_under_the_same_completed_pomodoro ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_first_future_pomodoro ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_last_completed_pomodoro ... ok
test capture::batch::capture_batch_dry_run_reports_all_items_without_writing ... ok
test capture::bare::capture_bare_terminal_marker_selects_the_last_of_two_completed_pomodoros ... ok
test capture::bare::capture_bare_terminal_marker_human_output_shows_the_ledger_entry ... ok
test capture::bare::capture_bare_terminal_marker_keeps_crlf_line_endings ... ok
test capture::bare::capture_bare_terminal_marker_writes_pomodoro_note_under_current_pomodoro ... ok
test capture::batch::capture_global_batch_failure_leaves_every_fixture_unchanged ... ok
test capture::batch::capture_batch_duplicate_block_id_failure_leaves_no_partial_write ... ok
test capture::batch::capture_batch_human_output_numbers_items ... ok
test capture::batch::capture_global_destination_human_and_stdin_and_dry_run ... ok
test capture::bare::capture_bare_terminal_marker_preflight_failures_leave_daily_note_untouched ... ok
test capture::batch::capture_global_destination_can_be_declared_at_the_end_of_any_item ... ok
test capture::batch::capture_batch_json_is_ordered_and_keeps_legacy_top_level ... ok
test capture::batch::capture_global_destination_on_authored_child_line_applies_draft_wide ... ok
test capture::batch::capture_global_destination_routes_unmarked_items_and_keeps_overrides ... ok
test capture::batch::capture_global_destination_conflict_and_declaration_only_are_usage_errors ... ok
test capture::blocked_tasks::forced_target_rejections_name_the_typed_sigil ... ok
test capture::batch::capture_global_sub_bullet_inserts_ordered_siblings_and_keeps_authored_children ... ok
test capture::blocked_tasks::ampersand_same_note_prerequisite_below_dependent_relocates ... ok
test capture::authored::capture_task_section_authored_children_and_composition ... ok
test capture::blocked_tasks::close_with_ampersand_emits_dependency_updates_array ... ok
test capture::blocked_tasks::fenced_example_does_not_hide_real_task ... ok
test capture::blocked_tasks::st15_kill_switch_still_mints ... ok
test capture::blocked_tasks::st14_insert_between ... ok
test capture::blocked_tasks::human_dry_run_residents_and_kept_notes ... ok
test capture::blocked_tasks::st10_cycles_refuse ... ok
test capture::blocked_tasks::st12_already_present_noop ... ok
test capture::blocked_tasks::st16_later_link_drops_n ... ok
test capture::blocked_tasks::st11_a8_refusals ... ok
test capture::blocked_tasks::st1_new_blocker_ready_unlinked ... ok
test capture::blocked_tasks::same_note_task_blocks_relocate_by_block_id ... ok
test capture::blocked_tasks::st2_consume_link_keep_session ... ok
test capture::blocked_tasks::st3_delete_empty_running_entry ... ok
test capture::blocked_tasks::st13_multiple_and_duplicate ... ok
test capture::blocked_tasks::st4_notes_kept ... ok
test capture::blocks::capture_blocks_dry_run_reports_without_writing ... ok
test aliases::move_done_tasks_alias_matches_canonical_on_git_fixture ... ok
test capture::blocked_tasks::st5_nested_identity ... ok
test aliases::every_alias_matches_canonical_help_and_invalid_option ... ok
test capture::blocks::capture_blocks_kill_switch_writes_nothing ... ok
test capture::blocked_tasks::st6_link_then_consume ... ok
test capture::blocks::capture_new_task_with_explicit_id_stages_blocks_row ... ok
test capture::blocked_tasks::st7_unrelated_placeholder_untouched ... ok
test capture::clip::capture_bare_terminal_marker_clipboard_marker_writes_children_beneath_note ... ok
test capture::blocks::capture_new_task_without_id_mints_dependent_block_id ... ok
test capture::clip::capture_clip_json_always_emits_collection_fields ... ok
test capture::blocked_tasks::human_star_line_and_consumption ... ok
test capture::blocked_tasks::st9_prj_internal_refuse ... ok
test capture::blocks::capture_dependency_drop_removes_blocks_entry ... ok
test capture::blocked_tasks::st8_prj_blocks_residents ... ok
test capture::blocked_tasks::st17_two_item_equivalent ... ok
test capture::blocks::capture_dependency_only_add_stages_blocks_row ... ok
test capture::clip::capture_clip_failures_leave_vault_untouched ... ok
test capture::clip::capture_history_without_a_provider_has_actionable_guidance ... ok
test capture::clip::capture_flat_clipboard_list_routes_normalized_children ... ok
test capture::clip::capture_percent_one_is_an_exact_single_clip_alias ... ok
test capture::clip::capture_history_dry_run_plans_colliding_files_without_writes ... ok
test capture::complete_block_id::block_id_link_candidates_are_filtered_and_annotated ... ok
test capture::clip::capture_sub_bullet_task_ref_recovers_shift_and_nests_clipboard ... ok
test capture::complete_block_id::block_id_missing_note_is_not_an_error ... ok
test capture::clip::capture_headerless_clip_marker_renders_under_tasks_and_pomodoros ... ok
test capture::complete_block_id::block_id_suggestions_follow_body_examples ... ok
test capture::complete_block_id::block_id_used_covers_done_nontask_duplicates_and_order ... ok
test capture::complete_block_id::block_id_json_shape_and_human_line ... ok
test capture::complete_block_id::block_id_incomplete_close_list_still_links ... ok
test capture::complete_blocked_task::missing_day_file_is_empty_ledger_without_warning ... ok
test capture::complete_blocked_task::task_id_assignment_returns_star_replacement_with_quoted_locator ... ok
test aliases::script_fallback_uses_embedded_assets_for_canonical_and_old_spellings ... ok
test capture::clip::capture_clip_uses_each_target_notes_indent_and_tabs_for_a_fresh_note ... ok
test capture::complete_blocked_task::existing_owner_reports_self_existing_edges_and_typed_blocked_rows ... ok
test capture::clip::capture_clip_marker_composes_with_schedule_routes_bullets_and_pomodoro ... ok
test capture::complete_dependency::empty_query_orders_lanes_before_history_and_hides_last ... ok
test capture::complete_dependency::existing_owner_marks_self_and_already_added_rows ... ok
test capture::complete_blocked_task::disabled_rows_explain_duplicate_ids_cycles_and_internal_projects ... ok
test capture::clip::capture_history_is_headerless_structured_and_composes_with_routes ... ok
test capture::complete_dependency::note_path_assigns_nested_case_sensitive_notes ... ok
test capture::complete_block_id::project_task_block_id_reports_stem_body_used_and_suggestions ... ok
test capture::clip::capture_history_provider_failures_leave_the_vault_untouched ... ok
test capture::complete_dependency::note_path_preserves_quoting_and_case_in_the_replacement ... ok
test capture::complete_editor::capture_complete_bare_hash_marker_is_an_empty_success ... ok
test capture::complete_dependency::closed_tasks_need_the_opt_in_and_stay_closed ... ok
test capture::complete_blocked_task::partial_star_fields_rank_today_running_then_lanes_and_owner_note ... ok
test capture::complete_editor::capture_complete_cursor_in_body_text_is_an_empty_success ... ok
test capture::complete_dependency::previous_daily_snapshot_is_read_only ... ok
test capture::complete_dependency::rows_carry_exact_identities_and_id_flow_metadata ... ok
test capture::complete_editor::capture_complete_empty_text_defaults_to_an_empty_draft ... ok
test capture::clip::capture_clip_saves_attachments_snippets_and_reports_dry_run ... ok
test capture::complete_editor::capture_complete_never_creates_the_vault_directory ... ok
test capture::blocked_tasks::st19_existing_owner_and_forced_task ... ok
test capture::complete_editor::capture_complete_discovery_failure_reports_an_actionable_error ... ok
test capture::complete_editor::capture_complete_missing_note_behind_a_resolved_route_is_an_empty_success ... ok
test capture::complete_editor::capture_complete_human_output_is_plain_and_concise ... ok
test capture::clip::capture_clip_options_force_or_disable_marker_parsing ... ok
test capture::complete_dependency::protected_spans_never_open_the_dependency_picker ... ok
test capture::complete_dependency::refetch_at_replacement_start_returns_the_full_snapshot ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_human_labels_rows ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_outside_the_text ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_that_splits_a_multibyte_character ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_lists_named_and_nameable_rows ... ok
test capture::complete_editor::capture_complete_reports_utf8_byte_offsets ... ok
test capture::complete_dependency::traversal_and_ambiguous_paths_fail_without_writing ... ok
test capture::complete_editor::capture_complete_pomodoro_close_protocol ... ok
test capture::complete_editor::capture_complete_wikilink_note_json_returns_replacement_and_cursor_after ... ok
test capture::complete_dependency::query_ranks_matches_and_keeps_history_findable ... ok
test capture::complete_editor::capture_complete_relation_label_reports_cancel_cue ... ok
test capture::complete_editor::capture_complete_wikilink_same_note_heading_uses_capture_route ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_json_covers_empty_and_new_queries ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_child_line ... ok
test capture::complete_query::capture_complete_all_tasks_works_on_a_global_sub_bullet_declaration ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_nested_child_line ... ok
test capture::complete_query::capture_complete_all_tasks_uses_global_ranges_in_later_batch_item ... ok
test capture::complete_block_id::block_id_link_new_and_project_note_intents ... ok
test capture::complete_editor::capture_complete_pomodoro_ranges_preserve_start_suffix ... ok
test capture::complete_query::capture_complete_inherited_route_is_the_same_note_for_wikilinks ... ok
test capture::complete_query::capture_complete_route_json_ranks_prefix_before_substring ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_skips_create_when_ledger_cannot_place_it ... ok
test capture::complete_query::capture_complete_section_json_lists_headings_of_the_resolved_route ... ok
test capture::complete_query::capture_complete_task_json_only_offers_tasks_with_a_block_id ... ok
test capture::complete_query::capture_complete_all_tasks_is_opt_in_and_plus_context_only ... ok
test capture::complete_query::capture_complete_section_json_skips_generated_status_groups ... ok
test capture::complete_query::capture_complete_task_block_id_marker_completes_only_route_side ... ok
test capture::complete_query::capture_complete_scopes_to_later_batch_item_and_ignores_separator ... ok
test capture::complete_relationship_owner::capture_complete_help_documents_additive_owner_fields ... ok
test capture::complete_query::capture_complete_global_declaration_replaces_only_the_active_component ... ok
test capture::complete_ref_kind::ref_kind_appears_on_hat_picker ... ok
test capture::complete_ref_kind::ref_kind_appears_on_amp_and_bang_pickers ... ok
test capture::complete_editor::capture_complete_task_section_json_covers_components_and_warnings ... ok
test capture::complete_relationship_owner::caret_star_picker_disables_the_owner_task_itself ... ok
test capture::complete_editor::capture_complete_pomodoro_close_selection_protocol ... ok
test capture::complete_editor::capture_complete_pomodoro_start_drop_protocol ... ok
test capture::complete_task_complete::complete_padded_line_offers_no_picker ... ok
test capture::complete_task_complete::complete_bare_bang_lists_today_first_with_picker ... ok
test capture::complete_task_complete::complete_second_item_marks_already_selected ... ok
test capture::complete_task_complete::complete_id_less_and_recurring_rows_carry_guards ... ok
test capture::complete_ref_kind::ref_kind_appears_on_colon_and_plus_pickers ... ok
test capture::complete_parent_task::plus_picker_fixture_vault_catalog_and_entry_points ... ok
test capture::complete_relationship_owner::scoped_parent_picker_applies_the_same_relationship_guards ... ok
test capture::complete_relationship_owner::owner_metadata_resolves_existing_alias_and_new_task_text ... ok
test capture::complete_task_complete::shell_completion_serves_identified_enabled_bang_rows ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_offers_a_create_row ... ok
test capture::complete_task_complete::capture_task_id_reports_complete_replacement_in_both_modes ... ok
test capture::complete_task_complete::complete_partial_query_decodes_and_drops_continuation_keys ... ok
test capture::complete_themes::pomodoro_name_completion_adds_suggested_create_row_for_note_default ... ok
test capture::complete_task_link::complete_task_link_lists_the_worked_example_in_json_and_human ... ok
test capture::complete_themes::pomodoro_name_completion_preselects_the_existing_task_theme ... ok
test capture::complete_task_link::complete_parent_task_plus_serves_json_and_human_candidates ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_an_identified_task ... ok
test capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create ... ok
test capture::complete_editor::capture_complete_override_name_json_carries_keeps_ledger_and_running ... ok
test capture::complete_relationship_owner::project_cannot_depend_on_its_resident_and_unmodified_shape_is_frozen ... ok
test capture::complete_wikilink_task::all_tasks_does_not_change_the_pool ... ok
test capture::complete_wikilink_task::empty_query_orders_this_note_lanes_and_history ... ok
test capture::complete_relationship_owner::parent_picker_reports_resolved_relationships_and_guards_rows ... ok
test capture::complete_themes::theme_recent_shell_description_and_quoted_replacement ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_a_task_without_an_id ... ok
test capture::complete_wikilink_task::read_only_note_guards_id_less_rows_and_stays_untouched ... ok
test capture::complete_themes::accepting_hidden_theme_keeps_preferences_and_today_row ... ok
test capture::complete_task_link::complete_task_link_batch_accepts_two_queries ... ok
test capture::complete_wikilink_task::rows_carry_link_targets_groups_and_guards ... ok
test capture::complete_task_link::complete_task_link_pull_forward_agrees_with_the_scheduled_retire ... ok
test capture::complete_wikilink_task::query_ranks_open_matches_ahead_of_history ... ok
test capture::complete_wikilink_task::shell_completion_returns_nothing ... ok
test capture::complete_task_link::parent_picker_acceptance_round_trips_and_id_assignment_returns_replacement ... ok
test capture::flag_guard::capture_complete_unknown_long_flag_is_rejected_with_json ... ok
test capture::ensure_next::capture_ensure_next_on_project_blocked_resident_refuses_drop ... ok
test capture::complete_wikilink_task::capture_task_id_reports_wikilink_replacement_in_both_modes ... ok
test capture::flag_guard::capture_parse_unknown_long_flag_is_rejected_with_json ... ok
test capture::flag_guard::capture_mixed_short_cluster_unknown_long_is_rejected_with_json ... ok
test capture::flag_guard::capture_templates_save_guard_json_carries_a_stable_code ... ok
test capture::flag_guard::capture_templates_save_unknown_flag_leaves_the_shelf_unchanged ... ok
test capture::ensure_next::capture_ensure_next_drops_own_dependency_and_relocates ... ok
test capture::flag_guard::capture_rewrite_unknown_long_flag_is_rejected_with_json ... ok
test capture::flag_guard::capture_unknown_long_flag_human_error_writes_nothing ... ok
test capture::flag_guard::capture_unknown_long_flag_is_rejected_with_json_and_writes_nothing ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_keeps_in_progress ... ok
test capture::flag_guard::capture_delimiter_literal_and_trailing_flag_word_still_capture ... ok
test capture::complete_parent_task::plus_picker_accepts_insert_and_preserves_operators ... ok
test capture::freshness_stamps::capture_link_clears_keep_streak ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_moves_link_and_sets_next ... ok
test capture::freshness_stamps::capture_link_never_stamps_recurring_tasks ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_same_note_batch_and_rollback ... ok
test capture::freshness_stamps::capture_new_tasks_carry_no_fresh ... ok
test capture::freshness_stamps::capture_link_leaves_next_untouched_without_future_schedule ... ok
test capture::inbox_route::inbox_route_choice_guard_stays_hidden_from_help ... ok
test capture::inbox_route::ir_conflicting_duplicate_answers_are_usage_errors ... ok
test capture::freshness_stamps::capture_link_stamps_next_when_it_retires_future_schedule ... ok
test capture::inbox_route::ir_gkeep_inbox_child_is_classified_from_its_live_parent ... ok
test capture::freshness_stamps::capture_link_stamping_is_idempotent_same_day ... ok
test capture::inbox_route::ir_dependency_touch_follows_its_routed_task ... ok
test capture::inbox_route::ir_pull_in_choice_refusal_precedes_inbox_route_choice_refusal ... ok
test capture::freshness_stamps::capture_link_stamps_ready_and_blocked_to_next ... ok
test capture::freshness_stamps::capture_close_to_in_progress_stamps_but_complete_does_not ... ok
test capture::inbox_route::ir_pull_in_and_route_answers_combine_in_one_batch ... ok
test capture::inbox_route::ir_completed_task_routes_home_without_stamp ... ok
test capture::inbox_route::ir_block_id_collision_renames_on_route ... ok
test capture::inbox_route::ir_stale_route_key_lists_current_candidates ... ok
test capture::inbox_route::ir_route_refusals_name_the_destination_and_the_rule ... ok
test capture::inbox_route::ir_idless_recovered_dependent_moves_by_line ... ok
test capture::link_guard::capture_pomodoro_link_on_tagged_child_is_not_linked ... ok
test capture::link_guard::capture_toggle_on_tagged_child_prj_promotes_ancestor ... ok
test capture::complete_themes::theme_menu_vectors ... ok
test capture::inbox_route::ir_preview_report_matches_write_and_hidden_guard_refuses_write_free ... ok
test capture::link_guard::capture_new_task_into_tagged_project_is_unlinked ... ok
test capture::link_guard::capture_toggle_on_tagged_child_resident_promotes_ancestor ... ok
test capture::ensure_next::capture_task_toggle_named_ensure_next_moves_creates_and_noops ... ok
test capture::inbox_route::ir_two_candidates_move_to_two_destinations_in_one_bulk ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_covers_open_states_and_failures ... ok
test capture::link_guard::own_dependency_drop_is_refused_for_a_project_task ... ok
test capture::open_notes::open_notes_human_output_is_unchanged ... ok
test capture::link_guard::close_link_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::inbox_route::ir_keep_answers_keep_the_task_and_satisfy_the_guard ... ok
test capture::complete_wikilink_task::triggers_ranges_and_non_triggers ... ok
test capture::link_guard::pomodoro_link_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::link_guard::ensure_next_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::link_guard::link_toggle_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::link_guard::own_dependency_drop_is_refused_for_a_project_blocked_resident ... ok
test capture::inbox_route::ir_routed_bulk_with_one_off_relation_repairs_once_and_guards_write_nothing ... ok
test capture::open_notes::open_notes_ensure_next_toggle_opens_task_and_day ... ok
test capture::open_notes::open_notes_link_guard_lands_on_the_blocked_child ... ok
test capture::inbox_route::ir_routed_link_moves_with_repair_stamp_follow_and_open_notes ... ok
test capture::open_notes::open_notes_new_inbox_task ... ok
test capture::open_notes::open_notes_library_hit_has_no_line ... ok
test capture::open_notes::open_notes_pomodoro_reset ... ok
test capture::open_notes::open_notes_pomodoro_link_lands_on_the_resident ... ok
test capture::open_notes::open_notes_pomodoro_shift ... ok
test capture::open_notes::open_notes_pomodoro_adjust ... ok
test capture::open_notes::open_notes_routed_task ... ok
test capture::open_notes::open_notes_pomodoro_start ... ok
test capture::open_notes::open_notes_ampersand_and_star_open_the_owner_only ... ok
test capture::open_notes::open_notes_project_note_with_task_links ... ok
test capture::open_notes::open_notes_queued_link_is_empty ... ok
test capture::open_notes::open_notes_sub_bullet_lands_on_the_added_child_under_the_block ... ok
test capture::open_notes::open_notes_section_bullet ... ok
test capture::parse::capture_parse_human_output_is_plain_and_concise ... ok
test capture::parse::capture_parse_json_output_is_stable_and_parseable ... ok
test capture::parse::capture_parse_json_reports_batch_items_with_global_ranges ... ok
test capture::parse::capture_parse_human_reports_start_suffix ... ok
test capture::open_notes::open_notes_pomodoro_close_opens_only_the_day_file ... ok
test capture::parse::capture_parse_json_reports_retired_double_colon_as_migration_guidance ... ok
test capture::open_notes::open_notes_task_complete_with_ledger ... ok
test capture::open_notes::open_notes_template_draft ... ok
test capture::parse::capture_parse_json_reports_pomodoro_note_mode_and_span ... ok
test capture::complete_themes::theme_literal_vectors_round_trip_through_capture ... ok
test capture::parse::capture_parse_json_reports_explicit_toggle_span_and_plain_ensure_next ... ok
test capture::parse::capture_parse_and_capture_report_shadowed_global_destination_warnings ... ok
test capture::open_notes::open_notes_sub_bullet ... ok
test capture::parse::capture_parse_json_reports_wikilink_semantic_spans ... ok
test capture::parse::capture_parse_reports_diagnostics_without_failing ... ok
test capture::parse::capture_parse_named_pomodoro_reports_incomplete_need ... ok
test capture::parse::capture_parse_reads_one_stdin_line_when_text_is_omitted ... ok
test capture::parse::capture_parse_json_reports_task_block_id_marker_spans_and_needs ... ok
test capture::parse::capture_parse_missing_text_is_a_usage_error ... ok
test capture::parse::capture_parse_reports_nested_sub_bullets_and_depths ... ok
test capture::open_notes::open_notes_three_items_dedupe_and_keep_first_landing ... ok
test capture::open_notes::open_notes_relative_day_file_includes_day_and_matches_written_digest ... ok
test capture::open_notes::open_notes_task_dependency_lands_on_the_item_block_id ... ok
test capture::parse::capture_parse_reports_utf8_byte_offsets ... ok
test capture::parse::capture_parse_reports_global_destination_metadata ... ok
test capture::parse::capture_parse_reports_duplicate_global_destination_diagnostics ... ok
test capture::parse::capture_parse_reports_orphaned_nested_bullet_diagnostic ... ok
test capture::parse_blocked_task::bang_keeps_precedence_over_star ... ok
test capture::parse::capture_parse_reports_sub_bullets_for_a_multiline_draft ... ok
test capture::parse::capture_parse_never_touches_the_vault_or_clipboard ... ok
test capture::parse_blocked_task::blocked_task_parses_separately_with_directional_spans ... ok
test capture::parse_blocked_task::body_bearing_close_with_star_fails_capture ... ok
test capture::parse::capture_parse_json_reports_project_task_ids_spans_and_mode ... ok
test capture::parse_blocked_task::blocked_task_note_star_is_invalid ... ok
test capture::parse::capture_parse_json_reports_project_note_markers ... ok
test capture::parse::capture_parse_json_reports_sub_bullet_section_and_incomplete_needs ... ok
test capture::parse_dependency::block_id_intent_follows_dependency_ownership ... ok
test capture::parse_dependency::capture_consumption_keeps_authored_notes_under_plain_task_text ... ok
test capture::parse_dependency::capture_executes_new_task_dependencies ... ok
test capture::parse_blocked_task::both_directions_keep_independent_lists_and_blocked_task_order ... ok
test capture::parse_dependency::capture_dependency_consumes_links_when_newly_blocked ... ok
test capture::parse_dependency::capture_prj_dependency_refuses_descendant_targets ... ok
test capture::parse::capture_parse_reports_start_suffix_spans_and_batch_offsets ... ok
test capture::parse_dependency::capture_keeps_literal_ampersand_prose ... ok
test capture::parse_dependency::capture_consumption_reports_and_deletes_only_the_emptied_running_entry ... ok
test capture::parse_dependency::capture_prj_dependency_refuses_same_note_targets ... ok
test capture::parse_dependency::child_line_dependency_belongs_to_the_item ... ok
test capture::parse_dependency::capture_prj_dependency_deprojects_existing_descendant_links ... ok
test capture::parse_dependency::capture_prj_dependency_sees_implicit_resident_cycles ... ok
test capture::parse_dependency::dependency_new_task_reports_modifiers_and_target ... ok
test capture::parse_dependency::capture_dependency_failures_leave_the_vault_intact ... ok
test capture::parse_dependency::complete_reports_task_dependency_field ... ok
test capture::parse_dependency::dependency_only_plus_target_reports_task_dependency ... ok
test capture::parse_dependency::dependency_only_colon_alias_reports_existing_target ... ok
test capture::parse_blocked_task::blocked_task_parse_vectors_cover_leading_quoted_and_nested ... ok
test capture::parse_blocked_task::star_twins_of_ampersand_rejections_name_the_sigil ... ok
test capture::parse_dependency::caret_alias_reports_existing_task_owner ... ok
test capture::parse_dependency::escaped_ampersand_leaves_visible_token ... ok
test capture::parse_dependency::dependency_only_suffixed_colon_target_is_rejected ... ok
test capture::parse_dependency::ownerless_dependency_needs_its_target ... ok
test capture::parse_dependency::leading_dependency_run_skips_a_destination_marker ... ok
test capture::parse_dependency::capture_promotion_walks_through_prj_without_raising_it ... ok
test capture::parse_dependency::inherited_parent_selects_the_existing_dependent ... ok
test capture::parse_dependency::plus_selector_beside_modifiers_needs_task_parent ... ok
test capture::parse_dependency::rewrite_never_absorbs_ampersands_or_the_colon_alias ... ok
test capture::parse_dependency::malformed_modifiers_report_invalid_dependency ... ok
test capture::parse_dependency::section_bullet_with_dependency_is_rejected ... ok
test capture::parse_dependency::dependency_markers_interleave_with_destination_in_either_order ... ok
test capture::parse_dependency::quoted_note_reports_decoded_identity_and_offsets ... ok
test capture::parse_dependency::relationship_only_owner_reports_needs_text ... ok
test capture::parse_dependency::capture_prj_dependency_blocks_tags_and_unlinks_residents ... ok
test capture::parse_dependency::suffixed_plus_owner_keeps_must_be_bare ... ok
test capture::parse_dependency::human_consumption_line_replaces_the_legacy_warning ... ok
test capture::parse_dependency::literal_ampersands_stay_prose ... ok
test capture::parse_dependency::partial_queries_need_task_dependency ... ok
test capture::parse_dependency::capture_executes_dependency_only_updates_idempotently ... ok
test capture::complete_wikilink_task::spliced_identified_link_stays_valid_capture ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_chain_items ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_incomplete_needs_task ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_human_line ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_human_and_help ... ok
test capture::parse_relation::relation_after_close_is_refused ... ok
test capture::parse_relation::relation_clock_lookalike_needs_relation_target ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_diagnostics_match_execution ... ok
test capture::parse_blocked_task::blocked_task_picker_and_markdown_guards_are_distinct ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_valid_spec_and_spans ... ok
test capture::parse_relation::relation_code_and_wikilinks_stay_literal ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_human_and_help ... ok
test capture::parse_relation::relation_empty_double_pipe_needs_relation_label ... ok
test capture::parse_relation::relation_bare_and_partial_targets_need_relation_target ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_human_and_help ... ok
test capture::parse_relation::relation_escape_leaves_visible_tilde ... ok
test capture::parse_relation::relation_invalid_label_is_refused ... ok
test capture::parse_relation::relation_grammar_absent_without_tilde ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_protocol ... ok
test capture::parse_relation::relation_double_pipe_marks_label_hidden ... ok
test capture::parse_relation::relation_digit_and_slash_guards_stay_literal ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_drop_protocol ... ok
test capture::parse_relation::relation_only_existing_owner_reports_task_dependency ... ok
test capture::parse_relation::relation_mid_line_stays_prose ... ok
test capture::parse_relation::relation_ownerless_reuses_dependency_target ... ok
test capture::parse_relation::relation_label_spans_flag_configured_complete_labels ... ok
test capture::parse_relation::relation_complete_to_from_label_and_owner_reuse ... ok
test capture::parse_relation::relation_label_spans_flag_configured_cancel_labels ... ok
test capture::parse_relation::relation_partial_labels_need_relation_label ... ok
test capture::parse_relation::relation_interleaves_with_dependencies_in_either_order ... ok
test capture::parse_relation::relation_triple_tilde_is_invalid ... ok
test capture::parse_relation::relation_labels_after_pipe ... ok
test capture::parse_relation::relation_triple_pipe_is_teaching_error ... ok
test capture::parse_relation::relation_strike_guard_stays_literal ... ok
test capture::parse_relation::relation_single_pipe_omits_hidden ... ok
test capture::parse_template::human_output_adds_template_summary ... ok
test capture::parse_template::headerless_placeholder_suggests_template_without_changing_capture_items ... ok
test capture::parse_template::expanded_row_diagnostics_map_bad_ids_to_fields_and_dedupe_literals ... ok
test capture::parse_template::template_parse_one_line_values_share_line_with_per_value_ranges ... ok
test capture::parse_relation::relation_session_token_drops_are_unchanged ... ok
test capture::parse_template::template_parse_reports_typed_spans_items_and_summary ... ok
test capture::parse_template::template_clipboard_follows_expanded_instances ... ok
test capture::plan_budget::capture_complete_create_row_reports_plan_themes ... ok
test capture::plan_budget::capture_complete_start_name_new_row_reports_plan_themes ... ok
test capture::plan_budget::capture_complete_start_name_again_row_reports_plan_themes ... ok
test capture::parse_template::placeholders_suppress_per_row_picker_needs_but_constant_pickers_remain ... ok
test capture::plan_budget::capture_complete_create_row_omits_plan_themes_without_config ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_protocol ... ok
test capture::plan_budget::capture_invalid_config_without_ledger_change_has_no_warning ... ok
test capture::plan_budget::capture_parse_link_close_with_drop_reports_close ... ok
test capture::parse_pomodoro::capture_parse_named_pomodoro_start_protocol ... ok
test capture::parse_template::template_session_suffixes_are_refused_with_typed_ranges ... ok
test capture::parse_template::template_row_need_and_arity_diagnostic_use_typed_ranges ... ok
test capture::parse_template::template_placeholders_split_capture_spans_and_refusals_are_reported ... ok

thread 'capture::plan_budget::capture_strict_mode_refuses_new_theme_past_cap_atomically' (187929) panicked at tests/cli/capture/plan_budget.rs:419:5:
refusing capture: today's plan would grow to 4/3 types (adds NEWT); current types: GOALS, DECKS, BOB; queue it with ^ or defer with $<N>
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
test capture::plan_budget::capture_strict_mode_refuses_new_theme_past_cap_atomically ... FAILED
test capture::plan_budget::capture_strict_mode_never_refuses_named_starts ... ok

thread 'capture::plan_budget::capture_plan_budget_human_reports_meter_and_destination' (187902) panicked at tests/cli/capture/plan_budget.rs:118:5:
✓ captured  dev.md
  - [*] #task Ship the thing. [created::2026-07-10] ^newid
  → new Pomodoro NEWT
✓ linked   /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws17-261029_192443/bob-cli-capture-budget-human-185594-1793316673271028860-1565/vault/day.md
  - [[dev#^newid]]
plan 4/3 types · 4/10 links  (+1 type: NEWT)

test capture::plan_budget::capture_plan_budget_human_reports_meter_and_destination ... FAILED
test capture::plan_budget::capture_strict_mode_refuses_project_note_path ... ok
test capture::plan_budget::capture_destination_human_arrows_name_each_role ... ok
test capture::plan_budget::capture_plan_budget_stays_quiet_when_over_cap_does_not_grow ... ok
test capture::plan_budget::capture_plan_budget_warns_on_link_growth_past_cap ... ok
test capture::plan_budget::capture_plan_budget_invalid_config_skips_with_warning ... ok

thread 'capture::plan_budget::capture_plan_budget_warns_when_new_theme_grows_past_cap' (187917) panicked at tests/cli/capture/plan_budget.rs:82:5:
{"added_theme_refs":[{"hue":"red","hue_source":"hash","key":"newt","known":false,"name":"NEWT"}],"added_themes":["NEWT"],"links":{"before":3,"cap":10,"count":4,"over":false},"status":"over","themes":{"before":3,"cap":3,"count":4,"over":true},"warnings":[{"code":"plan_theme_cap_exceeded","message":"today's plan now has 4/3 types (adds NEWT); queue it with ^ or defer with $<N>"}]}
test capture::plan_budget::capture_plan_budget_warns_when_new_theme_grows_past_cap ... FAILED
test capture::plan_budget::capture_strict_mode_never_refuses_session_starts ... ok
test capture::plan_budget::capture_without_ledger_change_has_no_plan_budget ... ok
test capture::plan_budget::capture_plan_budget_dry_run_matches_real_run ... ok
test capture::plan_budget::capture_strict_mode_refuses_toggle_path ... ok
test capture::pomodoro_chain::chain_capture_parse_reports_per_token_items ... ok
test capture::pomodoro_chain::chain_capture_complete_returns_no_candidates ... ok
test capture::plan_budget::capture_trailing_now_tag_fails_like_any_other_tag ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_extends_and_reports_json ... ok
test capture::pomodoro_chain::chain_close_then_start_reports_next_started_block ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_reports_full_block ... ok
test capture::pomodoro_chain::chain_adjust_then_close_reports_one_cumulative_block ... ok
test capture::pomodoro_chain::chain_dry_run_writes_nothing ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_batch_atomicity_and_dry_run ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_protocol ... ok
test capture::pomodoro_chain::chain_failure_rolls_back_with_item_two_prefix ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_clamps_and_crosses_midnight ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_preserves_metadata_crlf_and_fallbacks ... ok
test capture::pomodoro_chain::chain_human_output_numbers_both_items ... ok
test capture::pomodoro_chain::chain_positional_args_form_works ... ok
test capture::plan_budget::capture_destination_roles_cover_current_next_up_named_created ... ok
test capture::pomodoro_chain::chain_bare_named_start_matches_hash_spelling ... ok
test capture::pomodoro_close::capture_pomodoro_close_maps_repeated_name_after_multiple_work_log_lines ... ok
test capture::pomodoro_chain::chain_matches_blank_line_batch_file_by_file ... ok
test capture::pomodoro_close::capture_pomodoro_close_maps_unnamed_session_after_day_file_work_log ... ok
test capture::pomodoro_chain::chain_switches_sessions_like_a_blank_line_batch ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_on_project_task_refuses_drop ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_moved_source_and_next ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_already_current ... ok
test capture::pomodoro_chain::chain_wildcard_close_matches_blank_line_batch ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_drops_own_dependency_and_closes ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_protocol ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_batch_rollback ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_full_blocks ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_unchanged_next_block ... ok
test capture::pomodoro_close::capture_pomodoro_close_tracks_blocks_past_day_file_work_log ... ok
test capture::pomodoro_close::capture_pomodoro_close_task_reports_closed_and_next ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_complete_target ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_parse ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_nested_wording ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_rejects_bad_grammar_and_targets ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_dry_run_and_blocks ... ok
test capture::pomodoro_close_retired::double_equals_close_teaches_the_bare_spelling ... ok
test capture::pomodoro_close_retired::capture_parse_reports_retired_closes_as_close_diagnostics ... ok
test capture::pomodoro_close_retired::retired_close_in_a_chain_rolls_the_whole_batch_back ... ok
test capture::pomodoro_close_log::capture_parse_pomodoro_close_log_protocol ... ok
test capture::pomodoro_close_retired::retired_link_aliases_name_the_x_spelling_and_write_nothing ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_execution_errors ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_retired_tail ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_plain_reports_numbered_lineup ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_runtime ... ok
test capture::pomodoro_close_retired::retired_whole_item_closes_name_the_bare_rewrite_and_write_nothing ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_complete_listed ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_acceptance ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_all ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_rest ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_wildcard_logs_resolve_once_against_staged_lineup ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_crlf_day_file ... ok
test capture::pomodoro_close::capture_pomodoro_close_worked_example ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_chains ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_human_output ... ok

thread 'capture::pomodoro_close_selection::capture_pomodoro_close_selection_human_output' (188377) panicked at tests/cli/capture/pomodoro_close_selection.rs:578:5:
assertion `left == right` failed
  left: ["✓ closed CAPTURE 0920-0950 → 0920-0940 (20m, −10m) · 2026/20260928.md line 5", "  1 [*] → [/] Add support for `x` syntax! bob.md ^capture-stop +2 Work Log", "      *2026-09-28* — Designed the `x` grammar", "      *2026-09-28* — Wrote the plan", "  2 [*] → [x] Add capture support for web URLs! bob.md ^web-capture", "    [x] Restart axe sase.md ^axe-restart +1 Work Log", "      *2026-09-28* — Restarted axe", "  next: CAPTURE (created) at line 14 · carries 1 link", "plan 2/3 types · 2/10 links"]
 right: ["✓ closed CAPTURE 0920-0950 → 0920-0940 (20m, −10m) · 2026/20260928.md line 5", "  1 [*] → [/] Add support for `x` syntax! bob.md ^capture-stop +2 Work Log", "      *2026-09-28* — Designed the `x` grammar", "      *2026-09-28* — Wrote the plan", "  2 [*] → [x] Add capture support for web URLs! bob.md ^web-capture", "    [x] Restart axe sase.md ^axe-restart +1 Work Log", "      *2026-09-28* — Restarted axe", "  next: CAPTURE (created) at line 14 · carries 1 link", "plan 2/3 themes · 2/10 links"]
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_in_progress_and_complete ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_human_output ... FAILED
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_selection_protocol ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_batches ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_dry_run_matches_real_run ... ok
test capture::pomodoro_close_successors::close_all_day_file_successor_composes_edits ... ok
test capture::pomodoro_close_successors::close_successor_human_rows_and_next_line ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_land_fixes ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_only_forms ... ok
test capture::pomodoro_close_successors::close_with_invalid_dependency_note_reports_unavailable ... ok
test capture::pomodoro_close_successors::close_successor_dry_run_matches_real ... ok
test capture::pomodoro_close_successors::close_without_identities_reports_no_successors ... ok
test capture::pomodoro_close_successors::close_then_start_opens_successor_continuation ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_park ... ok
test capture::pomodoro_close_successors::sl17_unpicked_offers_link_none_of_six_successors ... ok
test capture::pomodoro_close_successors::sl12_two_predecessors_link_shared_dependent_once ... ok
test capture::pomodoro_close_successors::pomodoro_close_pulls_in_parent_of_closed_subproject ... ok
test capture::pomodoro_close_successors::route_close_links_predecessor_then_closes_with_successor ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_and_new_task_wildcards ... ok
test capture::pomodoro_link::capture_malformed_pomodoro_marker_is_usage_error_without_writes ... ok
test capture::pomodoro_close_successors::sl24_successor_reuses_later_same_name_entry ... ok
test capture::pomodoro_close_successors::sl20_second_completion_drops_first_link_net ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_listed_matches_ledger ... ok
test capture::pomodoro_close_successors::sl27_dropped_link_is_not_relinked ... ok
test capture::pomodoro_link::capture_pomodoro_dry_run_validates_and_changes_neither_note ... ok
test capture::pomodoro_close_successors::sl7_close_all_creates_continuation_holding_only_successor ... ok
test capture::pomodoro_close_successors::sl8_embed_close_appends_successor_after_carried_links ... ok
test capture::pomodoro_link::capture_named_pomodoro_batch_reuses_new_placeholder ... ok
test capture::pomodoro_link::capture_named_pomodoro_updates_both_notes_and_skips_current ... ok
test capture::pomodoro_link::capture_pomodoro_link_uses_default_day_file_and_untimed_fallback ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_dependencies_when_already_linked ... ok
test capture::pomodoro_link::capture_pomodoro_missing_daily_note_does_not_create_target ... ok
test capture::pomodoro_link::capture_pomodoro_linked_task_updates_both_notes_and_reports_json ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_own_dependency_and_links_atomically ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_forms ... ok
test capture::pomodoro_link::bare_named_link_suffix_writes_the_same_result_as_hash_before_equals ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_created_named_destination ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_worked_table ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_move_destination_first ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_dependencies_without_existing_link ... ok
test capture::pomodoro_link::capture_pomodoro_task_with_open_dependency_is_created_unlinked ... ok
test capture::pomodoro_link::dependency_drop_keeps_closed_and_unresolved_links_verbatim ... ok
test capture::pomodoro_link::capture_named_pomodoro_dry_run_and_failures_leave_notes_untouched ... ok
test capture::pomodoro_link::failed_start_rolls_back_a_staged_dependency_drop_for_real_and_dry_runs ... ok
test capture::pomodoro_link::dependency_drop_supports_named_pomodoro_start ... ok
test capture::pomodoro_link::capture_pomodoro_preflight_failures_leave_both_notes_untouched ... ok
test capture::pomodoro_link::capture_pomodoro_task_reports_running_entry_block ... ok
test capture::pomodoro_link::dependency_drop_human_output_names_the_removed_link ... ok
test capture::pomodoro_link::dependency_drop_reasons_report_schedule_and_managed_line_refusals ... ok
test capture::pomodoro_name::capture_human_names_the_starting_pomodoro_and_its_time ... ok
test capture::pomodoro_link::link_form_reuses_completed_multiword_pomodoro_name ... ok
test capture::pomodoro_link::pomodoro_link_guard_consumes_an_aliased_live_link_by_identity ... ok
test capture::pomodoro_link::link_suffix_timing_errors_leave_notes_byte_identical ... ok
test capture::pomodoro_name::capture_pomodoro_name_warns_when_name_is_unconfigured ... ok
test capture::pomodoro_link::link_with_start_moves_queued_link_into_reused_completed_name ... ok
test capture::pomodoro_name::capture_pomodoros_human_output_is_plain_when_piped ... ok
test capture::pomodoro_link::link_with_start_creates_started_entry_from_completed_name ... ok
test capture::pomodoro_close::capture_pomodoro_close_diagnostics ... ok
test capture::pomodoro_name::capture_pomodoros_missing_note_and_section_warn_in_json ... ok
test capture::pomodoro_name::capture_pomodoros_json_lists_open_entries_with_stable_picker_shape ... ok
test capture::pomodoro_name::capture_pomodoro_name_plus_is_selectable_and_targetable ... ok
test capture::pomodoro_name::capture_pomodoro_name_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::pomodoro_name::capture_pomodoro_name_rejects_write_free_failures ... ok
test capture::pomodoro_override::override_restart_batch_rollback ... ok
test capture::pomodoro_override::override_restart_human_output ... ok
test capture::pomodoro_override::override_restart_refuses_multiple_running ... ok
test capture::pomodoro_override::eq_override_close_first_and_overdue ... ok
test capture::pomodoro_override::override_swap_batch_rollback ... ok
test capture::pomodoro_override::override_restart_keeps_note_bearing_session ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_diagnostics ... ok
test capture::pomodoro_override::override_restart_preserves_crlf_and_missing_newline ... ok
test capture::pomodoro_override::override_restart_dry_run_matches_real ... ok
test capture::pomodoro_name::capture_pomodoros_task_link_count_matches_dry_run_lineup ... ok
test capture::pomodoro_override::override_swap_did_you_mean_spells_override ... ok
test capture::pomodoro_override::override_swap_again_and_created_targets ... ok
test capture::pomodoro_override::override_swap_fresh_timing_worked_example ... ok
test capture::pomodoro_override::override_swap_human_output ... ok
test capture::pomodoro_override::override_restart_matches_reset_then_start_on_note_free ... ok
test capture::pomodoro_override::eq_override_human_warning_lines ... ok
test capture::pomodoro_override::override_swap_keeps_annotated_ledger_verbatim ... ok
test capture::pomodoro_override::override_swap_drops_target_lineup ... ok
test capture::pomodoro_override::override_swap_chains ... ok
test capture::pomodoro_override::override_swap_kept_ledger_worked_example ... ok
test capture::pomodoro_override::override_swap_naming_running_refuses ... ok
test capture::pomodoro_override::idle_start_omits_override_metadata_and_fallback_copy ... ok
test capture::pomodoro_override::override_swap_teaching_errors ... ok
test capture::pomodoro_override::override_swap_unnamed_running ... ok
test capture::pomodoro_override::override_swap_placeholder_above_stays_first_future ... ok
test capture::pomodoro_override::override_restart_worked_example_rows ... ok
test capture::pomodoro_override::override_swap_reports_notes ... ok
test capture::pomodoro_override::override_swap_dry_run_matches_real ... ok
test capture::pomodoro_override::override_swap_strict_never_refuses_created_target ... ok
test capture::pomodoro_reset::pomodoro_reset_clears_note_free_session ... ok
test capture::pomodoro_override::override_swap_preserves_crlf_and_missing_newline ... ok
test capture::pomodoro_reset::pomodoro_reset_moves_before_earlier_future ... ok
test capture::pomodoro_override::override_swap_named_restart_matches_plain_restart ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_reports_full_block ... ok
test capture::pomodoro_reset::pomodoro_reset_note_fallback_stays_close ... ok
test capture::pomodoro_override::retired_doubled_starts_teach_the_single_equals_rewrite ... ok
test capture::pomodoro_reset::pomodoro_reset_uppercase_and_modifiers ... ok
test capture::pomodoro_start::capture_pomodoro_start_active_and_ambiguous_fail_atomically ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_moves_and_reports_json ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_bare_defaults_and_midnight_wrap ... ok
test capture::pomodoro_override::override_swap_matches_reset_then_start ... ok
test capture::pomodoro_start::capture_pomodoro_start_batch_adjusts_moved_entry ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_preserves_metadata_and_matches_plugin ... ok
test capture::pomodoro_override::refuse_override_guard ... ok
test capture::pomodoro_start::capture_pomodoro_start_already_in_slot_keeps_blank_line ... ok
test capture::pomodoro_override::override_unnamed_running_session_carries_derived_homes ... ok
test capture::pomodoro_start::capture_pomodoro_start_dry_run_and_batch_rollback ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_batch_atomicity_and_dry_run ... ok
test capture::pomodoro_start::capture_pomodoro_start_crlf_no_final_newline_moves_up ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_named_destination_before_link_move ... ok
test capture::pomodoro_start::capture_pomodoro_start_rejects_invalid_and_conflicting_syntax ... ok
test capture::pomodoro_start_drop::start_drop_bare_removes_link_with_nested_note ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_moves_first ... ok
test capture::pomodoro_start::capture_pomodoro_start_creates_unnamed_when_no_placeholder ... ok
test capture::pomodoro_start::capture_pomodoro_start_midnight_wrap_and_bob_now ... ok
test capture::pomodoro_start_drop::start_drop_crlf_day_file ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_and_new ... ok
test capture::pomodoro_start_drop::start_drop_out_of_range_and_empty_lineup ... ok
test capture::pomodoro_start::capture_pomodoro_start_unnamed_moves_between_done_and_review ... ok
test capture::pomodoro_close::capture_pomodoro_close_links_batches_and_files ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_to_current_slot_screenshot_repro ... ok
test capture::pomodoro_start_drop::link_and_task_starts_stay_byte_stable ... ok
test capture::pomodoro_start_named::named_start_again_creates_from_completed_name ... ok
test capture::pomodoro_start_drop::start_lineup_numbered_human_and_json ... ok
test capture::pomodoro_start_drop::start_lineup_counted_and_named ... ok
test capture::pomodoro_start_named::named_start_bare_spelling_writes_the_same_as_hash ... ok
test capture::pomodoro_start::capture_pomodoro_start_new_entry_uses_first_open_placement ... ok
test capture::pomodoro_start_named::named_start_existing_reports_json_and_moves_to_current_slot ... ok
test capture::pomodoro_start_named::named_start_created_reports_added_block ... ok
test capture::pomodoro_start_named::named_start_human_created_dry_run_and_forced_flags ... ok
test capture::pomodoro_start_named::named_start_prefix_and_duration_forms ... ok
test capture::pomodoro_start_named::named_start_grammar_errors_are_precise ... ok
test capture::pomodoro_start_named::named_start_missing_creates_and_warns_on_near_miss ... ok
test capture::pomodoro_start::capture_pomodoro_start_default_and_explicit_durations ... ok
test aliases::reconcile_aliases_match_canonical_dry_run_json_and_live_write ... ok
test capture::pomodoros_agenda::agenda_all_lists_completed_with_empty_payloads ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_rejects_bad_grammar_and_targets ... ok
test capture::pomodoros_agenda::agenda_budget_includes_real_zero_for_empty_and_completed_only_ledgers ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_moved_block ... ok
test capture::pomodoros_agenda::agenda_budget_matches_plan_for_merged_exempt_alias_and_prose_links ... ok
test capture::pomodoro_start_named::named_start_running_guards_and_switch_chain ... ok
test capture::pomodoro_start_drop::start_drop_lexical_errors ... ok
test capture::pomodoros_agenda::agenda_empty_golden ... ok
test capture::pomodoros_agenda::agenda_budget_output_is_repeatable_and_read_only ... ok
test capture::pomodoros_agenda::agenda_budget_omits_missing_section_and_degrades_on_invalid_config ... ok
test capture::pomodoros_agenda::agenda_default_output_stays_byte_identical ... ok
test capture::pomodoros_agenda::agenda_current_golden ... ok
test capture::pomodoros_agenda::agenda_no_daily_note_golden ... ok
test capture::pomodoro_start_drop::start_drop_counted_offset_named_and_empty_session ... ok
test capture::pomodoros_agenda::agenda_nothing_running_golden ... ok
test capture::pomodoros_agenda::agenda_multiple_timed_golden ... ok
test capture::pomodoros_agenda::agenda_budget_uses_configured_caps_and_strict_over_comparison ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_selects_first_placeholder_and_moves ... ok
test capture::priority::capture_mid_line_dollar_amount_stays_task_text ... ok
test capture::pomodoro_start_drop::start_drop_batch_chain_and_rollback ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_queued_tasks ... ok
test capture::priority::capture_priority_dry_run_prints_schedule_log_without_writing ... ok
test capture::pomodoros_agenda::agenda_heavy_golden ... ok
test capture::priority::capture_priority_level_four_rolls_scheduled_date_in_window ... ok
test capture::priority::capture_bare_dollar_matches_priority_level_one ... ok
test capture::priority::capture_priority_level_one_rolls_scheduled_date_in_window ... ok
test capture::priority::capture_priority_missing_config_file_is_io_error_without_writes ... ok
test capture::priority::capture_parse_reports_priority_spans_and_retired_markers ... ok
test capture::priority::capture_priority_json_includes_priority_fields_only_when_set ... ok
test capture::priority::capture_priority_renders_before_scheduled_and_before_pomodoro_block_id ... ok
test capture::priority::capture_escaped_dollar_amount_stays_task_text ... ok
test capture::priority::capture_priority_schedule_log_uses_the_target_notes_indent_unit ... ok
test capture::priority::capture_without_priority_token_tolerates_missing_config_file ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_guards_fail_write_free ... ok
test capture::priority::capture_priority_sub_bullet_nests_schedule_log_under_the_child ... ok
test capture::priority::capture_priority_with_clip_orders_clip_children_before_schedule_log ... ok
test capture::priority::capture_priority_with_explicit_schedule_skips_roll ... ok
test capture::priority::capture_priority_out_of_range_is_usage_error_without_writes ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_batches_compose_and_roll_back ... ok
test capture::pomodoros_agenda::agenda_numbers_match_operator_lineups ... ok
test capture::project_note::capture_project_note_named_caret_form_rejects_the_unused_pomodoro ... ok
test capture::project_close::close_leaves_inherited_resident_blocked_naming_parent ... ok
test capture::project_close::close_leaves_resident_blocked_by_project ... ok
test capture::project_note::capture_project_note_retired_colon_forms_fail_with_teaching_errors ... ok
test capture::project_close::close_leaves_tagged_prj_blocked_without_recovery ... ok
test capture::project_note::capture_project_note_renders_authored_tasks_sections_and_tasks_merge ... ok
test capture::pomodoro_name::capture_pomodoro_link_solo_grammar_and_atomic_execution ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_json_and_human ... ok
test capture::project_note::capture_project_note_creates_plain_note_with_json_and_human_output ... ok
test capture::project_note::capture_project_note_schedule_and_priority_write_inline_date_and_log ... ok
test capture::priority::capture_retired_priority_marker_is_a_usage_error ... ok
test capture::project_close::close_recovers_prj_and_residents_with_unblocked ... ok
test capture::project_note::capture_project_note_reports_created_pomodoro_block ... ok
test capture::project_note::capture_project_note_dry_run_and_batch_parenting_and_rollback ... ok
test capture::project_note::capture_project_note_task_links_report_the_resolved_pomodoro_name ... ok
test capture::project_note::capture_project_note_task_links_use_the_implicit_pomodoro ... ok
test capture::project_note::capture_project_note_rejections_leave_no_partial_write ... ok
test capture::project_pull_in::already_planned_pull_in_raises_project_without_duplicate_link ... ok
test capture::project_note::capture_project_note_task_links_need_the_day_file_only_for_links ... ok
test capture::project_note::capture_project_note_task_links_write_the_worked_example ... ok
test capture::project_pull_in::pomodoro_close_pulls_in_project_at_continuation ... ok
test capture::project_pull_in::parent_pull_in_row_drops_when_parent_prj_also_closes ... ok
test capture::project_pull_in::stale_blocked_resident_stays_blocked ... ok
test capture::project_pull_in::due_project_schedule_applies_sync_hidden_task_recount ... ok
test capture::project_pull_in::still_blocked_project_row_has_trigger_and_context_before_reason ... ok
test capture::r#ref::capture_bracketed_url_queues_without_brackets ... ok
test capture::project_pull_in::external_blocker_pull_in_and_unplanned_ready_recovery ... ok
test capture::project_note::capture_project_note_task_links_dry_run_batch_and_rollback ... ok
test capture::project_pull_in::multi_item_project_pull_ins_obey_surface_and_net_pass ... ok
test capture::project_pull_in::disabled_pull_in_surfaces_and_in_progress_pull_in_stays_in_progress ... ok
test capture::project_pull_in::tagged_parent_prj_close_stays_blocked_naming_grandparent ... ok
test capture::project_pull_in::idless_last_task_close_pulls_in_and_sync_agrees ... ok
test capture::project_pull_in::punctuation_hide_pull_in_and_sync_agrees ... ok
test capture::r#ref::capture_dry_run_and_parse_never_touch_the_network_or_spool ... ok
test capture::project_pull_in::unplanned_pull_in_is_reported_as_surface_in_human_output ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_rejects_shape_and_forced_flags ... ok
test capture::r#ref::capture_config_off_and_invalid_config_keep_tasks ... ok
test capture::r#ref::capture_dry_run_routes_each_pdf_backed_list_source_to_library ... ok
test capture::r#ref::capture_excluded_and_corporate_hosts_stay_tasks ... ok
test capture::r#ref::capture_dry_run_matches_real_apart_from_dry_run_and_job ... ok
test capture::r#ref::capture_parse_reports_ref_mode_and_span ... ok
test capture::r#ref::capture_inline_global_blocks_ref_claim ... ok
test capture::r#ref::capture_spool_hit_is_clipping ... ok
test capture::r#ref::capture_repeat_in_draft_is_duplicate ... ok
test capture::r#ref::capture_lone_url_queues_a_ref_job ... ok
test capture::r#ref::capture_mixed_list_and_draft_plan_each_item ... ok
test capture::r#ref::capture_staged_write_failure_removes_jobs ... ok
test capture::r#ref::queued_job_ids_deduplicate_a_claim_overlap_and_keep_extra_jobs ... ok
test capture::r#ref::capture_with_kick_returns_before_the_clip_finishes ... ok
test capture::r#ref::capture_url_list_queues_one_item_per_line ... ok
test capture::ref_grammar::capture_lone_bare_url_stays_a_task_while_routing_is_off ... ok
test capture::project_pull_in::subproject_close_pulls_in_parent_and_sync_agrees ... ok
test capture::ref_grammar::capture_url_list_writes_one_task_per_line ... ok
test capture::relate_existing::rx11_cycle_path_starts_at_new_edge_source ... ok
test capture::r#ref::capture_library_hits_are_unchanged ... ok
test capture::relate_existing::rx10_child_bullets_need_text ... ok
test capture::r#ref::explicit_url_clip_forms_keep_the_clipboard_path ... ok
test capture::r#ref::capture_end_to_end_falls_back_on_blocked ... ok
test capture::r#ref::capture_unknown_library_queues_with_message ... ok
test capture::r#ref::capture_end_to_end_clips_through_the_worker ... ok
test capture::r#ref::capture_ref_parent_selection_reports_canonical_routes_and_hints ... ok
test capture::relate_existing::rx16_new_task_prints_per_prerequisite_row ... ok
test capture::r#ref::capture_url_with_markers_or_flags_stays_a_task ... ok
test capture::relate_existing::rx13_suffixed_owners_keep_must_be_bare ... ok
test capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance ... ok
test capture::r#ref::percent_listen_reference_never_reads_clipboard_and_queues_listen_job ... ok
test capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio ... ok
test capture::relate_existing::rx14_in_progress_owner_consumes_running_link ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_wildcard_forms ... ok
test capture::relate_existing::rx12_sub_bullet_prints_children_then_relationship ... ok
test capture::relate_existing::rx5_colon_alias_still_owns ... ok
test capture::relate_existing::rx2_existing_owner_star ... ok
test capture::relate_existing::rx3_existing_owner_both_directions ... ok
test capture::relate_existing::rx6_inherited_owner_writes_edge_only ... ok
test capture::related::bulk_draft_anchors_dedupe_linked_tasks_and_project_modes ... ok
test capture::relate_existing::rx8_unresolved_plus_selector_never_creates_a_task ... ok
test capture::related::draft_gates_short_titles_templates_and_noncreating_items_before_vault_io ... ok
test capture::relations::dry_run_human_says_would ... ok
test capture::related::linked_candidates_are_reported_and_excluded_and_closed_rows_use_split_defaults ... ok
test capture::relate_existing::rx7_closed_star_owner_is_refused ... ok
test capture::relations::ld_dry_run_previews_hides_without_writing ... ok
test capture::relate_existing::rx9_relationship_needs_text_in_parse_and_execute ... ok
test capture::related::idless_rows_offer_suggestions_and_atomic_code_spans_stay_distinct ... ok
test capture::relations::lx11_operator_relation_error ... ok
test capture::relations::ld_read_only_journal_still_captures_with_retry_warning ... ok
test capture::relations::lx10_malformed_linked_from_skips_mirror ... ok
test capture::relate_existing::rx1_existing_owner_ampersand_either_order ... ok
test capture::relations::ld_new_one_off_label_writes_plain_label_and_hides ... ok
test capture::relations::ld_mixed_pipes_and_repeated_keys_collapse_to_one_event ... ok
test capture::related::recapture_contract_golden_includes_actions_defaults_and_cross_note_matches ... ok
test capture::relations::lx13_relation_is_inert ... ok
test capture::relations::lx1_new_task_to_archived_skips_mirror_without_mint ... ok
test capture::relations::lx15_to_and_from_same_target_are_independent ... ok
test capture::related::calibration_excludes_self_before_closed_suppression_and_limits ... ok
test capture::relations::lx16_same_note_pair_composes ... ok
test capture::relations::ld_hidden_label_writes_no_event ... ok
test capture::relations::lx14_duplicate_noop_and_conflicting_labels_refuse ... ok
test capture::relations::ld_visible_existing_label_warns_and_hides ... ok
test capture::relations::lx9_malformed_links_refuses ... ok
test capture::relate_existing::rx4_caret_alias_executes_like_plus_owner ... ok
test capture::r#ref::capture_human_wording_for_every_case ... ok
test capture::relations::lx4_ampersand_blocks_and_relation_stays_inert ... ok
test capture::relations::lx2_from_relation_mints_new_task_and_writes_both_sides ... ok
test capture::relations::lx5_todays_daily_target_gets_mirror_and_mints_source ... ok
test capture::relations::previous_daily_target_skips_mirror ... ok
test capture::relations::lx8_self_non_task_and_missing_id_refuse ... ok
test capture::relations_cancel::cancel_dry_run_names_one_dependent ... ok
test capture::relations::lx7_from_target_path_refusals_leave_vault_untouched ... ok
test capture::relate_existing::rx15_repeat_is_already_present_noop ... ok
test capture::relations::lx6_kill_switch_skips_mirror_and_source_mint ... ok
test capture::relations_cancel::cancel_inert_without_config ... ok
test capture::relations_cancel::cancel_invalid_config_warns_and_cancels_nothing ... ok
test capture::relations_cancel::cancel_human_names_the_cancel_once ... ok
test capture::relations_cancel::cancel_prj_source_cancels_project_only ... ok
test capture::relations_cancel::cancel_prj_source_singular_open_task ... ok
test capture::relations::lx3_existing_owner_relabel_and_unchanged_rerun ... ok
test capture::relations_cancel::cancel_refusals_are_coded_and_write_nothing ... ok
test capture::relations_cancel::cancel_source_in_daily_note_stays_one_file ... ok
test capture::relations_cancel::cancel_forward_cancels_prunes_and_recovers ... ok
test capture::relations_cancel::cancel_reverse_retires_old_task ... ok
test capture::relations_cancel::cancel_two_edges_one_source_one_log_line ... ok
test capture::relations_cancel::cancel_cross_item_sees_staged_cancel ... ok
test capture::relations_cancel::cancel_with_mirror_kill_switch_still_cancels ... ok
test capture::relations_cancel::cancel_already_closed_links_only ... ok
test capture::relations_complete::complete_cross_item_mixed_effects_conflict ... ok
test capture::relations_cancel::cancel_midnight_dates_follow_bob_now ... ok
test capture::relations_cancel::cancel_two_recovered_dependents_uses_plural ... ok
test capture::relations_cancel::cancel_hidden_and_oneoff_labels_still_cancel ... ok
test capture::relations_cancel::cancel_dependent_with_other_prereq_stays_blocked ... ok
test capture::relations_cancel::cancel_without_daily_note_prunes_nothing ... ok
test capture::relations_complete::complete_embedded_subtasks_follow_bang ... ok
test capture::relations_cancel::cancel_unchanged_rerun_is_noop ... ok
test capture::relations_complete::complete_distinct_sources_mixed_cancel_and_complete ... ok
test capture::relations_complete::complete_human_names_the_complete_once ... ok
test capture::relations_cancel::cancel_relabel_into_and_away ... ok
test capture::relations_complete::complete_forward_completes_strikes_and_offers ... ok
test capture::relations_complete::complete_mixed_bang_pomodoro_relation_offers ... ok
test capture::relations_complete::complete_already_closed_links_only ... ok
test capture::relations_complete::complete_mixed_bang_and_relation_offers ... ok
test capture::relations_complete::complete_overlap_label_closes_nothing ... ok
test capture::relations_complete::complete_matches_bang_bytes ... ok
test capture::relations_complete::complete_mixed_direction_warnings_keep_their_targets ... ok
test capture::relations_complete::complete_prj_source_keeps_residents ... ok
test capture::relations_complete::complete_one_item_two_sources_with_offers ... ok
test capture::relations_complete::complete_inbox_routed_recovery ... ok
test capture::relations_complete::complete_same_note_shifted_source_groups_once ... ok
test capture::relations_complete::complete_reverse_completes_old_task ... ok
test capture::relations_complete::complete_relation_preserves_authored_theme ... ok
test capture::relations_complete::complete_refusals_are_coded_and_write_nothing ... ok
test capture::rewrite::capture_parse_does_not_apply_the_separator_toggle ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_adjustments ... ok
test capture::rewrite::capture_rewrite_human_output_is_plain_and_concise ... ok
test capture::rewrite::capture_rewrite_json_absorbs_a_local_marker ... ok
test capture::relations_complete::complete_no_config_and_cancel_only_compat ... ok
test capture::relations_complete::complete_two_edges_one_source_once ... ok
test capture::rewrite::capture_rewrite_json_reports_a_rule_a5_notice_without_changing_text ... ok
test capture::relations_complete::complete_bang_parity_ledger_crlf_midnight_ny ... ok
test capture::rewrite::capture_rewrite_json_starts_a_template ... ok
test capture::rewrite::capture_rewrite_json_reports_no_rewrite_without_a_bare_at_at ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_shifts ... ok
test capture::rewrite::capture_rewrite_json_switches_a_block_id_separator ... ok
test capture::rewrite::capture_rewrite_missing_text_is_a_usage_error ... ok
test capture::rewrite::capture_rewrite_reads_stdin_when_text_is_omitted ... ok
test capture::rewrite::capture_rewrite_rejects_a_cursor_off_a_char_boundary ... ok
test capture::rewrite::capture_rewrite_never_touches_the_vault_or_clipboard ... ok
test capture::routing::capture_bullet_json_reports_rendered_line ... ok
test capture::routing::capture_dry_run_reports_without_writing ... ok
test capture::routing::capture_empty_input_is_usage_error ... ok
test capture::routing::capture_json_failure_prints_error_object ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_starts ... ok
test capture::routing::capture_json_omits_sub_bullets_for_an_ordinary_single_line_capture ... ok
test capture::routing::capture_json_output_is_machine_readable ... ok
test capture::routing::capture_json_output_includes_scheduled_date ... ok
test capture::routing::capture_legacy_standalone_marker_form_is_usage_error ... ok
test capture::routing::capture_leading_route_bullet_inserts_into_section_by_prefix ... ok
test capture::routing::capture_bullet_marker_order_routes_equivalently ... ok
test capture::routing::capture_rejects_stdin_continuation_text_that_is_not_a_bullet ... ok
test capture::routing::capture_bullet_prefix_prefers_non_h1_and_ignores_prefix_case ... ok
test capture::routing::capture_route_override_keeps_at_tokens_literal ... ok
test capture::routing::capture_nonterminal_schedule_token_stays_literal ... ok
test capture::routing::capture_reads_the_complete_piped_stdin_stream_when_text_is_absent ... ok
test capture::routing::capture_routed_bullet_inserts_into_section_by_prefix ... ok
test capture::rewrite::capture_rewrite_pomodoro_close_protocol ... ok
test capture::routing::capture_schedule_only_is_usage_error ... ok
test capture::routing::capture_routed_task_into_blocked_project_lands_blocked_and_tagged ... ok
test capture::routing::capture_scheduled_offset_out_of_range_is_usage_error ... ok
test capture::routing::capture_scheduled_dry_run_reports_without_writing ... ok
test capture::routing::capture_routed_prefers_tasks_section_over_root_task ... ok
test capture::routing::capture_routed_prefix_inserts_and_suffix_creates_file ... ok
test capture::routing::capture_unrouted_appends_to_mac_inbox ... ok
test capture::routing::capture_scheduled_zero_uses_created_date ... ok
test capture::routing::capture_routed_task_into_tagged_project_lands_blocked_and_tagged ... ok
test capture::routing::capture_unrouted_scheduled_offset_appends_property ... ok
test capture::sections::capture_article_prefix_prefers_raw_number_in_document_order ... ok
test capture::sections::capture_article_exact_raw_title_precedes_earlier_identity_match ... ok
test capture::routing::capture_unrouted_prefers_tasks_section_in_existing_inbox ... ok
test capture::relations_complete::complete_ref_same_note_archived_cancelled_targets ... ok
test capture::relations_complete::complete_open_statuses_complete_and_custom_links_only ... ok
test capture::sections::capture_article_prefix_matches_de_numbered_identity ... ok
test capture::sections::capture_forced_section_requires_route ... ok
test capture::sections::capture_sections_json_lists_sections_in_order ... ok
test capture::sections::capture_sections_invalid_or_missing_route_errors_cleanly ... ok
test capture::routing::capture_scheduled_offset_routes_in_either_order ... ok
test capture::sections::capture_sections_json_skips_generated_status_groups ... ok
test capture::relations_complete::complete_locations_mirror_hidden_midnight_crlf ... ok
test capture::sections::capture_sections_missing_note_returns_empty_json ... ok
test capture::sections::capture_forced_section_inserts_exact_bullet ... ok
test capture::sections::capture_forced_task_section_option_errors ... ok
test capture::sections::capture_tasks_human_output_is_plain_when_piped ... ok
test capture::relations_complete::complete_relabel_unchanged_inverse ... ok
test capture::sections::capture_tasks_json_lists_open_tasks_with_stable_picker_shape ... ok
test capture::sections::capture_article_forced_section_matches_identity_and_stale_number ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_last_completed_entry_block ... ok
test capture::sections::capture_forced_task_section_matches_title_exactly ... ok
test capture::sections::capture_task_section_managed_log_geometry ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_running_entry_block ... ok
test capture::relations_complete::complete_offers_join_existing_pull_in ... ok
test capture::sections::capture_non_article_numbered_heading_keeps_raw_title_matching ... ok
test capture::sections::capture_task_section_prefix_vs_whole_slug_and_multiword ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_complete_subtree_before_parent_logs ... ok
test capture::sections::capture_task_section_inserts_into_first_middle_and_last_sections ... ok
test capture::sub_bullet::capture_sub_bullet_task_option_keeps_at_tokens_literal ... ok
test capture::relations_complete::complete_oneoff_hide_date_recurrence_new_target ... ok
test capture::sub_bullet::capture_sub_bullet_uses_dominant_indent_preserves_crlf_and_dry_run ... ok
test capture::successor_integration::close_successor_then_consume_net ... ok
test capture::successor_integration::ref_task_successor_links_like_an_ordinary_task ... ok
test capture::successor_integration::restart_and_reset_never_complete_prerequisites ... ok
test capture::successor_offers::no_successors_still_reports_pull_in ... ok
test capture::sub_bullet::capture_sub_bullet_selectors_and_batch_keep_order_above_logs ... ok
test capture::successor_offers::so14_unplanned_predecessor_implicit_destination ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_with_parent_indentation_and_reports_json ... ok
test capture::successor_offers::so16_two_open_timed_is_no_destination ... ok
test capture::successor_offers::so15_no_open_entry_is_no_destination ... ok
test capture::successor_offers::so17_emptied_project_unpicked ... ok
test capture::successor_offers::dry_run_parity_matches_pull_in_rows ... ok
test capture::successor_offers::so19_disabled_config_has_no_offers ... ok
test capture::sections::capture_task_section_indent_units_crlf_and_dry_run ... ok
test capture::targets::capture_targets_empty_vault_still_lists_inbox_default ... ok
test capture::successor_offers::so27_require_choice_refuses_when_offers_exist ... ok
test capture::targets::capture_targets_json_failure_prints_error_object ... ok
test capture::targets::capture_targets_human_groups_and_summarizes_without_ansi ... ok
test capture::successor_offers::so26_human_lists_offers_without_linking ... ok
test capture::targets::capture_targets_json_lists_picker_targets_in_order ... ok
test capture::successor_offers::so18_parent_project_unpicked_and_picked ... ok
test capture::targets::capture_targets_verbose_emits_skip_warnings ... ok
test capture::targets::capture_targets_json_reports_aliases_and_human_shows_aka ... ok
test capture::successor_offers::so1_project_offers_pick_one ... ok
test capture::task_blocks::capture_task_blocks_omitted_without_sub_bullets ... ok
test capture::task_blocks::capture_task_blocks_dry_run_reports_the_parent_block ... ok
test capture::task_blocks::capture_task_blocks_human_output_is_unchanged ... ok
test capture::task_blocks::capture_task_blocks_and_pomodoro_blocks_report_independently ... ok
test capture::sections::capture_task_section_errors_leave_the_note_unchanged ... ok
test capture::successor_offers::so6_bad_picks_are_usage_and_write_free ... ok
test capture::relations_complete::complete_offer_probe_rerun_keys_and_net_filter ... ok
test capture::task_complete::already_done_is_a_noop ... ok
test capture::task_blocks::capture_task_blocks_real_run_equals_dry_run_except_dry_run ... ok
test capture::task_complete::carried_link_dedupes_into_morning_entry_when_nothing_runs ... ok
test capture::task_complete::complete_without_id_skips_dependent_lookup ... ok
test capture::task_complete::ambiguous_and_duplicate_refusals_state_exit_code_and_leave_vault_untouched ... ok
test capture::task_complete::ambiguous_note_and_duplicate_id_and_forced_flags_fail ... ok
test capture::successor_offers::so2_so32_fan_out_offers_every_dependent ... ok
test capture::task_complete::close_completing_nothing_ignores_poisoned_note ... ok
test capture::successor_offers::so29_zero_offers_are_a_noop ... ok
test capture::successor_offers::so13_later_item_drops_stale_offers ... ok
test capture::task_complete::blocked_root_completes_and_dependent_unblocks ... ok
test capture::task_complete::embedded_subtasks_close_and_blocked_descendant_stays_open ... ok
test capture::task_complete::failure_in_item_two_rolls_item_one_back ... ok
test capture::task_complete::day_file_successor_composes_task_and_ledger_edits ... ok
test capture::task_complete::batch_of_two_completions_reports_already_done_for_repeats ... ok
test capture::task_complete::custom_global_filter_yields_clean_text_and_human_output ... ok
test capture::task_complete::hello_ignores_poisoned_note_only_discovery_would_touch ... ok
test capture::task_complete::day_file_successor_without_block_id_mints_in_place ... ok
test capture::task_complete::dry_run_json_matches_real ... ok

thread 'capture::task_complete::exact_human_output_for_strike_move_dedupe_and_done' (191483) panicked at tests/cli/capture/task_complete.rs:793:5:
assertion `left == right` failed
  left: "✓ completed [*] → [x] Fix flaky gkeep test  sase.md ^fix-flaky\n  ledger  Task Link struck in CAPTURE · 20261005.md\nplan 1/3 types · 0/10 links\n"
 right: "✓ completed [*] → [x] Fix flaky gkeep test  sase.md ^fix-flaky\n  ledger  Task Link struck in CAPTURE · 20261005.md\nplan 1/3 themes · 0/10 links\n"
test capture::task_complete::forced_flags_exit_2_with_exact_message_and_untouched_vault ... ok
test capture::task_complete::exact_human_output_for_strike_move_dedupe_and_done ... FAILED
test capture::successor_offers::so3_so4_so5_all_none_and_subset ... ok
test capture::task_complete::next_completes_with_running_session_strike ... ok
test capture::task_complete::invalid_dependency_note_reports_unavailable_and_skips_linking ... ok
test capture::task_complete::sl10_successor_block_id_is_minted ... ok
test capture::task_complete::sl16_gate_reports_checked_with_empty_rows ... ok
test capture::task_complete::placeholder_link_moves_to_running_entry_and_placeholder_is_removed ... ok
test capture::task_complete::sl19_reapplied_close_reports_nothing ... ok
test capture::task_complete::human_output_names_transition_ledger_and_unblocked ... ok
test capture::task_complete::sl18_disabled_config_recovers_without_link ... ok
test capture::sub_bullet::capture_sub_bullet_errors_are_actionable_in_human_and_json_modes ... ok
test capture::task_complete::exact_human_output_for_subtasks_and_unblocked ... ok
test capture::relations_complete::complete_reconcile_never_infers_and_batch_atomic ... ok
test capture::task_complete::sl14_ambiguous_basename_uses_dir_link ... ok
test capture::task_complete_parse::task_complete_padded_item_refuses_without_capturing ... ok
test capture::sub_bullet::capture_sub_bullet_lands_before_direct_managed_logs ... ok
test capture::task_complete::sl1_successor_links_into_vacated_slot ... ok
test capture::task_complete::sl2_successor_keeps_slot_retirement_moves_predecessor ... ok
test capture::task_complete::sl9_unplanned_predecessor_recovers_without_link ... ok
test capture::task_complete::task_living_in_todays_daily_note_completes_in_place ... ok
test capture::task_complete_parse::task_complete_padded_item_reports_invalid_task_complete ... ok
test capture::task_goto::capture_goto_query_fails_with_the_t3_teaching_error ... ok
test capture::task_complete_parse::task_complete_query_refuses_with_the_picker_teaching_error ... ok
test capture::task_complete_parse::task_complete_token_executes_now_that_execute_landed ... ok
test capture::task_complete::two_completions_plus_close_commit_as_one_batch ... ok
test capture::task_goto::capture_batch_with_a_slash_item_captures_both_items_as_usual ... ok
test capture::task_complete_parse::bang_prose_rows_still_capture_as_tasks ... ok
test capture::task_goto::capture_complete_goto_query_reports_task_goto_without_query_or_picker ... ok
test capture::task_complete_parse::bang_prose_rows_parse_as_editor_tasks_and_queries ... ok
test capture::task_complete_parse::task_complete_query_reports_incomplete_needing_task_complete ... ok
test capture::task_goto::complete_goto_candidates_carry_note_path_and_target_without_link_keys ... ok
test capture::task_goto::complete_goto_human_lines_show_note_path_and_line ... ok
test capture::task_complete_parse::single_item_task_complete_mirrors_top_level_object ... ok
test capture::task_complete::refusals_leave_the_vault_intact ... ok
test capture::task_complete::ledger_json_carries_text_struck_in_and_dropped ... ok
test capture::task_goto::shell_completion_serves_no_goto_rows ... ok
test capture::task_goto::capture_parse_goto_query_reports_incomplete_task_goto ... ok
test capture::task_link::capture_batch_with_a_colon_query_writes_nothing ... ok
test capture::related::draft_related_stays_under_the_debug_perf_gate ... ok
test capture::task_link::capture_colon_query_fails_with_the_picker_teaching_error ... ok
test capture::task_complete_parse::task_complete_token_reports_mode_spans_and_object ... ok
test capture::task_link::capture_colon_query_json_failure_reports_ok_false ... ok
test capture::task_link::capture_colon_query_teaches_the_at_spelling_for_links ... ok
test capture::task_marker::capture_retired_double_colon_marker_is_usage_error_without_writes ... ok
test capture::task_link::capture_complete_colon_query_reports_task_link_with_empty_candidates ... ok
test capture::task_id::capture_task_sections_json_and_human_list_sections ... ok
test capture::task_marker::capture_malformed_task_block_id_marker_is_usage_error_without_writes ... ok
test capture::task_link::capture_parse_colon_query_reports_incomplete_task_link ... ok
test capture::task_marker::capture_task_block_id_dry_run_and_duplicate_preflight_do_not_write ... ok
test capture::task_marker::capture_task_block_id_marker_creates_missing_routed_note ... ok
test capture::task_goto::capture_goto_refusals_cover_slash_forms_and_leave_the_vault_untouched ... ok
test capture::task_id::capture_task_id_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::task_goto::capture_parse_goto_prose_rows_keep_their_current_parse ... ok

thread 'capture::task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception' (191800) panicked at tests/cli/capture/task_theme_writes.rs:131:5:
{"block_id":"new-fix","block_link":"[[sase#^new-fix]]","created":"2026-10-28","creates_pomodoro":false,"day_file":"/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws17-261029_192443/bob-capture-task-theme-new-185594-1793316683156436884-4566/vault/2026/20261028.md","dry_run":true,"inbox_route":{"candidate_count":0,"candidates":[],"kept_count":0,"routed_count":0,"supported":true},"kind":"pomodoro_task","ok":true,"open_notes":[{"block_id":"new-fix","label":"sase.md","line":9,"path":"/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws17-261029_192443/bob-capture-task-theme-new-185594-1793316683156436884-4566/vault/sase.md","ref":"9:5f04489c","relative_path":"sase.md","role":"note"},{"label":"Today","line":2,"path":"/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws17-261029_192443/bob-capture-task-theme-new-185594-1793316683156436884-4566/vault/2026/20261028.md","ref":"2:ae8bb2f6","relative_path":"2026/20261028.md","role":"day"}],"placement":"appended","plan_budget":{"links":{"before":0,"cap":10,"count":1,"over":false},"status":"ok","themes":{"before":1,"cap":30,"count":1,"over":false}},"pomodoro_blocks":[{"created":false,"line":2,"lines":[{"change":"unchanged","depth":0,"text":"- [ ] () — FIX"},{"change":"added","depth":1,"text":"  - [[sase#^new-fix]]"}],"name":"FIX","relative_target":"2026/20261028.md","roles":["linked"],"status":"queued"}],"pomodoro_link_destination":{"line":2,"name":"FIX","role":"named"},"pomodoro_link_placement":"appended","pomodoro_name":"FIX","pull_in":{"choice":null,"offer_count":0,"picked_count":0,"supported":true},"relative_target":"sase.md","route":"sase","route_label":"sase.md","routed":true,"scheduled":null,"target":"/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws17-261029_192443/bob-capture-task-theme-new-185594-1793316683156436884-4566/vault/sase.md","task_line":"- [*] #task Draft a fix [type:: FIX] [created::2026-10-28] ^new-fix","task_theme":{"action":"set","inherited":{"from":{"chain":["sase.md"],"kind":"project","path":"sase.md","stem":"sase"},"label":"from sase","source":"note","theme":{"configured":true,"hue":"magenta","hue_source":"config","key":"write","name":"WRITE"}},"previous":null,"theme":{"configured":true,"hue":"blue","hue_source":"config","key":"fix","name":"FIX"}},"text":"Draft a fix"}
test capture::task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception ... FAILED
test capture::task_goto::complete_goto_route_ref_sequence_equals_task_link ... ok
test capture::task_complete::successor_dry_run_matches_real_with_human_rows ... ok
test capture::task_marker::capture_task_block_id_marker_writes_ordinary_task_and_ignores_daily_note ... ok

thread 'capture::task_theme_writes::ensure_next_named_relocation_sets_a_theme_after_freshness_edits' (191765) panicked at tests/cli/capture/task_theme_writes.rs:241:5:
- [*] #task Work [type:: FIX] [fresh:: 2026-10-28] ^work
test capture::task_theme_writes::ensure_next_named_relocation_sets_a_theme_after_freshness_edits ... FAILED

thread 'capture::task_theme_writes::active_existing_task_link_start_shorthand_uses_the_resolved_name' (191750) panicked at tests/cli/capture/task_theme_writes.rs:400:5:
the task line should carry the selected theme
test capture::task_theme_writes::active_existing_task_link_start_shorthand_uses_the_resolved_name ... FAILED
test capture::task_toggle::capture_task_toggle_can_edit_task_in_daily_note ... ok

thread 'capture::task_theme_writes::a_two_item_batch_stages_and_reports_both_task_theme_writes' (191743) panicked at tests/cli/capture/task_theme_writes.rs:209:5:
first task theme should be committed
test capture::task_theme_writes::a_two_item_batch_stages_and_reports_both_task_theme_writes ... FAILED
test capture::task_theme_writes::ref_today_named_selection_never_writes_task_theme ... ok
test capture::task_link::bare_caret_link_suffix_writes_the_same_result_as_hash_before_equals ... ok
test capture::task_toggle::capture_task_toggle_on_date_blocked_prj_is_refused ... ok
test capture::task_id::capture_task_id_recovers_a_shifted_line_and_rejects_write_free_failures ... ok
test capture::task_toggle::capture_task_toggle_on_project_scheduled_resident_reports_date ... ok
test capture::template::a_late_duplicate_id_refuses_the_whole_template_with_row_context ... ok
test capture::task_toggle::capture_task_toggle_on_project_blocked_resident_refuses_drop ... ok
test capture::task_id::capture_task_sections_empty_and_error_paths ... ok
test capture::template::bad_template_origin_is_a_usage_error ... ok
test capture::task_toggle::capture_task_toggle_batch_uses_staged_snapshots_and_rolls_back ... ok
test capture::template::expand_with_bad_template_origin_is_a_usage_error ... ok
test capture::template::duplicate_ids_across_template_rows_refuse_with_the_later_row ... ok
test capture::task_toggle::capture_task_toggle_drops_own_dependency_and_links ... ok
test capture::template::parser_diagnostics_keep_the_template_source_line ... ok
test capture::task_theme_writes::absent_suggestion_and_guarded_links_do_not_write_a_task_theme ... ok
test capture::task_toggle::capture_task_toggle_reports_unlink_removal_from_two_entries ... ok
test capture::task_toggle::promotion_walks_through_a_blocked_seed_without_raising_it ... ok
test capture::task_toggle::capture_task_toggle_reports_inserted_link_block ... ok
test capture::task_theme_writes::composite_exempt_and_unnamed_destinations_do_not_write_task_themes ... ok
test capture::task_toggle::capture_task_toggle_errors_are_actionable_without_writes ... ok
test capture::template::template_clipboard_markers_refuse_even_with_no_clip ... ok
test capture::template::template_execution_reports_first_issue_in_draft_order ... ok
test capture::template::non_saving_runs_leave_the_shelf_absent ... ok
test capture::template::template_human_summary_names_the_source_rows ... ok
test capture::task_toggle::capture_task_toggle_unlink_keeps_every_lane ... ok
test capture::task_toggle::capture_task_toggle_link_and_unlink_updates_notes_and_reports_json ... ok
test capture::template::plain_captures_stay_byte_identical_without_a_header ... ok
test capture::task_toggle::capture_task_toggle_reports_created_named_entry ... ok
test capture::template_expand::capture_expand_ignores_capture_options_and_never_needs_a_vault ... ok
test capture::template::template_human_output_reports_saved ... ok
test capture::template::template_executes_rows_and_adds_row_metadata ... ok
test capture::task_toggle::capture_task_toggle_named_creation_dry_run_and_pull_forward ... ok
test capture::template_expand::capture_expand_prints_template_text_and_json_summary ... ok
test capture::template::unwritable_shelf_keeps_exit_zero_with_not_saved ... ok
test capture::template::human_replaced_names_the_checked_out_origin ... ok
test capture::template::template_one_placeholder_one_line_dry_run_matches_three_lines ... ok
test capture::template::one_row_and_many_rows_save_the_same_shelf_entry ... ok
test capture::task_toggle::capture_task_toggle_links_unlinked_lanes_without_status_change ... ok
test capture::template_expand::capture_expand_reports_language_errors_as_usage_errors ... ok
test capture_templates::save_of_headerless_draft_is_not_a_template ... ok
test capture_templates::bare_delete_is_a_usage_error_and_leaves_the_store_absent ... ok
test capture::template::template_url_listen_marker_is_not_clipboard_capture ... ok
test capture::template_expand::capture_expand_is_identity_for_plain_drafts ... ok
test capture::template::template_session_suffixes_refuse_in_execution ... ok
test capture::theme_warnings::capture_deferred_priority_still_warns_when_theme_grows ... ok
test catalog::protocol_2_returns_json_error_and_exit_2 ... ok
test capture::template_expand::capture_expand_one_line_values_equal_three_line_rows ... ok
test capture::template::template_clip_flag_and_session_operators_have_stable_codes ... ok
test catalog::missing_protocol_exits_2_with_usage ... ok
bob __catalog --protocol 1 took 68ms
test catalog::catalog_is_fast ... ok

thread 'catalog::protocol_1_parses_with_schema_version_one' (192029) panicked at tests/cli/catalog.rs:43:5:
assertion failed: entries.iter().any(|entry|
        {
            entry["id"] == "themes-split" &&
                entry["path"] == serde_json::json!(["themes", "split"])
        })
test catalog::protocol_1_parses_with_schema_version_one ... FAILED
test catalog::catalog_is_read_only ... ok
test capture_templates::newer_schema_with_changed_field_type_stays_readable_and_refuses_writes ... ok
test capture_templates::clear_also_removes_the_corrupt_quarantine ... ok
test capture_templates::show_by_index_prints_the_insertable_draft ... ok
test completion::bash::bash_default_target_honors_env ... ok
test completion::bash::bash_counts_unicode_prefix_in_chars ... ok
test catalog::protocol_equals_form_matches_space_form ... ok
test capture_templates::human_list_covers_empty_populated_and_saving_off ... ok
test completion::bash::bash_completes_command_prefix ... ok
test completion::bash::bash_completes_attached_files_in_value ... ok
test completion::bash::bash_completes_attached_format_value ... ok
test capture_templates::definition_errors_and_newer_schema_have_stable_recovery_paths ... ok
test capture_templates::list_save_show_and_delete_follow_the_template_protocol ... ok
test completion::bash::bash_print_matches_installed_bytes ... ok
test completion::bash::bash_filters_create_target_by_extension ... ok
test completion::bash::bash_maps_dirs_directive ... ok
test completion::bash::bash_shell_selection ... ok
test capture::template::real_template_capture_saves_and_reports_statuses ... ok
test completion::bash::bash_keeps_spaces_in_one_argument ... ok
test completion::bash::bash_offers_nothing_once_text_starts ... ok
test capture::theme_warnings::capture_warns_on_unconfigured_start_again_and_name_field ... ok
test capture::theme_warnings::capture_skips_close_link_inventory_and_unconfigured_vocab ... ok
test completion::capture_text::body_bearing_route_colon_suggests_new_id ... ok
test completion::bash::bash_open_quote_completes_route ... ok
test completion::capture_text::bare_plus_shell_completion_returns_only_identified_parent_markers ... ok
test completion::bash::bash_install_status_uninstall_round_trip ... ok
test completion::capture_text::caret_completes_active_tasks ... ok
test completion::bash::bash_verify_reports_source_remedy ... ok
test completion::capture_text::partial_route_returns_full_set_for_shell_filtering ... ok
test completion::capture_text::newline_in_word_returns_nothing ... ok
test completion::capture_text::named_start_completes_after_hash ... ok
test completion::bash::bash_unquotes_single_quoted_word ... ok
test completion::capture_text::options_stay_hidden_once_text_starts ... ok
test completion::capture_text::named_start_after_inline_close_keeps_prefix ... ok
test completion::bash::bash_strips_every_wordbreak_not_just_colon ... ok
test completion::bash::bash_reassembles_colon_split_marker ... ok
test completion::capture_text::body_bearing_text_agrees_with_capture_complete_intent ... ok
test completion::capture_text::capture_parse_and_rewrite_share_the_text_slot ... ok
test completion::capture_text::suffix_returns_nothing ... ok
test completion::capture_text::routes_complete_at_end_of_text_word ... ok
test completion::lifecycle::dry_run_writes_nothing ... ok
test completion::capture_text::quoted_word_keeps_prefix_with_prefix_directive ... ok
test completion::capture_text::safe_rows_only_omit_missing_ids ... ok
test completion::capture_text::unicode_prefix_counts_chars_not_bytes ... ok
test completion::capture_text::task_sections_complete_after_id_hash ... ok
test completion::capture_text::solo_route_colon_lists_existing_tasks ... ok
test completion::capture_text::relation_labels_complete_after_double_pipe ... ok
test completion::capture_text::sections_complete_after_hash ... ok
test completion::lifecycle::path_shadow_warns ... ok
test completion::lifecycle::first_install_then_idempotent_unchanged ... ok
test completion::capture_text::close_shorthands_offer_nothing ... ok
test completion::lifecycle::home_default_fpath_line_prints_without_probe ... ok
test completion::lifecycle::plain_output_has_no_ansi_when_piped ... ok
test completion::lifecycle::not_installed_shell_never_probes_and_never_fails ... ok
test completion::lifecycle::fake_bash_never_reports_registered_when_missing ... ok
test completion::lifecycle::missing_manifest_entry_reports_missing ... ok
test completion::lifecycle::recorded_verification_survives_into_status ... ok
test completion::lifecycle::externally_managed_adapter_is_reported_never_adopted ... ok
test completion::lifecycle::previous_install_target_rule_and_reason ... ok
test completion::lifecycle::outdated_adapter_updates_without_force ... ok
test completion::lifecycle::install_without_shell_args_honors_shell_plus_owned ... ok
test completion::lifecycle::closers_tell_the_truth ... ok
test completion::lifecycle::status_without_verify_warns_on_recorded_unhealthy ... ok
test completion::lifecycle::status_json_shape_and_bare_forms ... ok
test completion::lifecycle::zsh_print_matches_installed_bytes ... ok
test completion::lifecycle::probe_without_controlling_terminal_via_zpty ... ok
test completion::protocol::attached_option_value_uses_prefix ... ok
test completion::protocol::conflicting_option_is_dropped ... ok
test completion::lifecycle::unrecorded_stamped_file_is_outdated_externally_managed ... ok
test completion::lifecycle::zsh_bound_to_function_reports ... ok
test completion::lifecycle::usage_errors_exit_2_and_shell_selection ... ok
test completion::lifecycle::target_move_removes_previous_adapter ... ok
test completion::protocol::double_dash_offers_long_forms_only ... ok
test completion::protocol::alias_completion_uses_canonical_path_and_freshness_seed_is_hidden ... ok
test completion::lifecycle::foreign_edited_and_symlink_refuse_without_force ... ok
test completion::protocol::empty_root_offers_commands_then_capture_protocol_without_options ... ok
test completion::protocol::lone_dash_offers_paired_forms ... ok
test completion::protocol::debug_log_writes_the_file_and_nothing_else ... ok
test completion::protocol::hidden_aliases_stay_hidden ... ok
test completion::protocol::format_values_carry_the_slot_group ... ok
test completion::protocol::file_and_dir_slots_emit_directives ... ok
test completion::protocol::malformed_request_exits_two ... ok
test completion::protocol::present_option_is_dropped ... ok
test completion::protocol::protocol_skew_reports_both_directions ... ok
test completion::lifecycle::uninstall_removes_only_bob_owned_files ... ok
test completion::protocol::freshness_short_option_value_completes ... ok
test completion::protocol::partial_command_word_yields_the_full_unfiltered_set ... ok
test completion::protocol::pull_in_value_is_free_text ... ok
test completion::protocol::nested_subcommands_complete ... ok
test completion::vault::locked_vault_fixture_is_removed_after_guard_and_tempdir_drop ... ok
test completion::lifecycle::install_glyphs_follow_registration ... ok
test completion::lifecycle::target_rules_pick_in_order ... ok
test completion::protocol::text_started_slot_offers_no_options ... ok
test completion::protocol::empty_cursor_at_positional_slot_offers_values_first ... ok
test completion::vault::levels_come_from_config_in_order ... ok
test completion::bash::bash_readline_inserts_what_bob_returned ... ok
test completion::protocol::task_move_is_discoverable_with_its_options ... ok
test completion::protocol::saved_template_group_and_format_complete_as_commands_and_static_choices ... ok
test completion::vault::pomodoro_refs_offer_open_entries ... ok
test completion::vault::plugins_come_from_the_repo_checkout ... ok
test completion::vault::missing_prerequisites_name_the_flag ... ok
test completion::protocol::ref_create_force_value_completes_both_modes ... ok
test completion::vault::routes_are_grouped_in_scan_order ... ok
test completion::vault::task_sections_offer_exact_titles ... ok
test completion::protocol::theme_suggest_is_discoverable_with_options_and_a_text_target ... ok
test completion::vault::relation_label_completion_notes_close_consequences ... ok
test completion::zsh_adapter::adapter_source_has_required_properties ... ok
test completion::vault::unknown_route_offers_nothing ... ok
test completion::vault::deadline_override_keeps_working ... ok
test completion::zsh_adapter::colon_escaping_empty_fields_and_defaults ... ok
test completion::zsh_adapter::candidate_groups_keep_order_and_nospace_flag ... ok
test completion::vault::relation_rename_arguments_complete_catalog_labels_including_hidden ... ok
test completion::zsh_adapter::default_styles_use_green_headers ... ok
test completion::vault::split_old_offers_themes_and_map_offers_files ... ok
test completion::vault::vault_notes_answer_files_in ... ok
test completion::zsh_adapter::empty_output_returns_one ... ok
test completion::zsh_adapter::no_color_uses_plain_header ... ok
test completion::vault::sections_follow_long_short_and_attached_route_forms ... ok
test completion::zsh_adapter::directives_map_to_native_widgets ... ok
test completion::zsh_adapter::request_argv_unquotes_words_and_passes_suffix ... ok
test completion::protocol::value_hints_beat_generic_kinds_entries ... ok
test completion::zsh_adapter::stderr_is_discarded ... ok
test dataview::dataview_native_table_json_projects_frontmatter_rows ... ok
test completion::zsh_adapter::user_descriptions_format_wins ... ok
test dataview::dataview_obsidian_dql_paths_extracts_and_deduplicates_note_paths ... ok
test dataview::dataview_obsidian_markdown_prints_rendered_markdown ... ok
test dataview::dataview_native_dql_paths_walks_parent_frontmatter_headlessly ... ok
test dataview::dataview_obsidian_dql_json_reads_query_file_and_forwards_env_vault ... ok
test dataview::dataview_native_table_paths_match_list_rows_headlessly ... ok
test completion::vault::tasks_offer_open_block_ids_with_text ... ok
test dataview::dataview_native_where_false_returns_no_rows ... ok
test dataview::dataview_obsidian_query_does_not_run_ob_command ... ok
test completion::lifecycle::verify_probe_classifications ... ok
test dataview::dataview_obsidian_source_uses_path_command_and_sentinel_protocol ... ok
test dataview::dataview_obsidian_dql_paths_warn_or_fail_for_missing_identities ... ok
test dataview::dataview_obsidian_reports_not_running_without_javascript_blob ... ok
test dataview::dataview_obsidian_reports_missing_command_without_query_blob ... ok
test dataview::dataview_rejects_removed_sync_option ... ok
test dataview::dataview_obsidian_reports_protocol_errors ... ok
test dataview::dataview_obsidian_reports_missing_and_malformed_sentinel ... ok
test dataview::dataview_rejects_unsafe_origin_and_missing_bob_dir ... ok
test dataview::dataview_rejects_invalid_argument_combinations ... ok
test epipe::closed_stderr_usage_error_exits_two_quietly ... ok
test epipe::closed_stdout_help_exits_zero_quietly ... ok
test dataview_oom::synthetic_list_census_counts_nested_children ... ok
test dataview::dataview_short_options_are_accepted ... ok
test completion::capture_text::wikilinks_return_nothing_quickly ... ok
test freshness::list_config_interval_and_budget ... ok
test freshness::list_budget_meter_uses_upkeep ... ok
test freshness::list_emoji_vault_is_refused_with_exit_2 ... ok
test dataview_oom::tasks_skips_dataview_index_under_address_space_cap ... ok
test freshness::list_canonical_budget_key_wins_and_warns ... ok
test freshness::list_excludes_today_and_daily_lane_tasks ... ok
test freshness::list_decay_off_and_zero_limit ... ok
test epipe::closed_stdout_pipe_exits_zero_with_empty_stderr ... ok
test completion::vault::theme_mutations_and_relation_hide_use_their_catalogs ... ok
test freshness::list_invalid_canonical_budget_exits_2 ... ok
test freshness::list_human_shows_reference_in_new_before_rotten_divider ... ok
test freshness::list_hidden_reference_stays_out_while_visible_walks ... ok
test freshness::list_invalid_config_exits_2 ... ok
test freshness::list_invalid_decay_exits_2 ... ok
test freshness::list_invalid_tracker_intervals_exit_2 ... ok
test freshness::list_excludes_today_tasks ... ok
test freshness::list_lane_rows_cover_pending_and_next ... ok
test freshness::list_json_reports_queue_counts_and_contract ... ok
warning: vault completion p50 is 69ms (> 30ms)
test completion::vault::vault_slots_stay_fast ... ok
test freshness::list_human_has_sections_and_no_ansi ... ok
test freshness::list_limit_truncates_rows_not_counts ... ok
dataview flatten RSS: tasks=1000 baseline=43.6 MiB census=45.6 MiB delta=2.0 MiB
test freshness::list_json_and_human_cover_recurring_tier ... ok
test freshness::list_json_and_human_cover_checklist_tiers ... ok
test freshness::list_legacy_budget_key_warns_once_and_still_counts ... ok
test dataview_oom::tasks_ignores_dataview_only_page_metadata ... ok
test freshness::list_reports_keeps_and_decide_per_schema_9 ... ok
test freshness::list_tracker_intervals_and_hide_gate ... ok
test freshness::list_walks_projects_after_new_with_decoupled_counts ... ok
test freshness::seed_dry_run_writes_nothing_and_reports_buckets ... ok
test freshness::seed_dry_run_lists_files_without_writing ... ok
test freshness::list_unblocked_tickler_reports_return_source ... ok
test freshness::seed_preserves_existing_keeps ... ok
test freshness::seed_invariance_abort_lists_the_line ... ok
test help::capture_complete_help_is_native_only ... ok
test help::capture_help_is_native_only ... ok
test freshness::seed_guard_refuses_and_force_overrides ... ok
test help::capture_pomodoro_name_help_is_native_only ... ok
test help::capture_parse_help_is_native_only ... ok
test help::capture_pomodoros_help_is_native_only ... ok
test freshness::seed_applies_stamps_and_rerun_is_noop ... ok
test help::capture_sections_help_is_native_only ... ok
test help::capture_targets_help_is_native_only ... ok
test help::capture_task_sections_help_is_native_only ... ok
test help::capture_task_id_help_is_native_only ... ok
test help::capture_tasks_help_is_native_only ... ok
test help::dataview_help_is_native_only ... ok
test help::capture_named_start_help_mentions_start_forms ... ok
test freshness::list_lane_intervals_false_null_and_invalid ... ok
test help::highlights_ref_help_is_native_only ... ok
test help::cache_extraction_writes_expected_files_and_modes ... ok
test help::help_routes_reject_non_command_paths_before_dispatch ... ok
test help::freshness_seed_stays_callable_but_hidden_from_help_and_completion ... ok
test help::move_done_tasks_help_is_native_only ... ok
test help::nightly_help_exits_before_operational_work ... ok
test help::legacy_binary_help_is_safe_and_plain ... ok
test help::ref_help_matches_grouped_snapshot ... ok
test help::projects_help_is_native_only ... ok
test freshness::list_decides_on_early_dates ... ok
test help::root_help_matches_sectioned_short_and_long_snapshots ... ok
test help_options::capture_complete_help_lists_options_alphabetically ... ok
test help::highlights_ref_subcommand_help_works ... ok
test completion::vault::completion_is_read_only ... ok
test help_options::capture_parse_help_lists_options_alphabetically ... ok
test help_options::capture_pomodoro_name_help_lists_options_alphabetically ... ok
test help_options::capture_related_help_lists_options_alphabetically ... ok
test help_options::capture_help_lists_options_alphabetically ... ok
test help::task_status_hooks_help_is_native_only ... ok
test help_options::capture_pomodoros_help_lists_options_alphabetically ... ok
test help_options::capture_rewrite_help_lists_options_alphabetically ... ok
test help_options::capture_sections_help_lists_options_alphabetically ... ok
test help_options::capture_task_sections_help_lists_options_alphabetically ... ok
test help_options::capture_targets_help_lists_options_alphabetically ... ok
test help_options::capture_task_id_help_lists_options_alphabetically ... ok
test help_options::capture_tasks_help_lists_options_alphabetically ... ok
test help_options::dataview_help_lists_options_alphabetically ... ok
test help_options::freshness_help_hides_the_seed_subcommand ... ok
test help_options::completion_help_lists_subcommands_and_options_alphabetically ... ok
test help_options::freshness_seed_help_lists_options_alphabetically ... ok
test help_options::freshness_list_help_lists_options_alphabetically ... ok
test help::pomodoro_help_documents_show_stale_option ... ok
test help_options::highlights_ref_scan_help_lists_options_alphabetically ... ok
test help_options::highlights_ref_help_lists_subcommands_alphabetically ... ok
test help_options::highlights_clip_alias_help_matches_create_help ... ok
test help_options::highlights_create_help_lists_options_alphabetically ... ok
test help_options::highlights_ref_scan_json_verbose_is_usage_error ... ok
test help_options::plugins_sync_help_lists_options_alphabetically ... ok
test help_options::default_subcommands_are_labeled_in_help ... ok
test help_options::highlights_ref_sync_help_lists_options_alphabetically ... ok
test help_options::plugins_help_lists_subcommand_and_options ... ok
test help_options::ref_attach_source_help_lists_options_alphabetically_and_explains_adoption ... ok
test help_options::ready_help_lists_options_alphabetically ... ok
test help_options::projects_help_lists_subcommands_and_options ... ok
test help_options::task_status_hooks_help_lists_options_alphabetically ... ok
test help_options::stats_help_lists_options_alphabetically ... ok
test dataview_oom::flatten_later_limit_does_not_hide_default_budget ... ok
test highlights::continuations::continuation_scan_reports_dangling_marker ... ok
test help::script_fallback_help_is_safe_and_plain ... ok
test highlights::create::highlights_create_and_clip_attach_listen_to_the_newest_reading ... ok
test highlights::create::highlights_create_article_binds_explicit_audio ... ok
test highlights::continuations::show_exposes_group_pieces_with_seams_and_omits_them_for_singles ... ok
test highlights::create::highlights_create_article_default_target_avoids_ids_in_other_types ... ok
test help::vault_sync_help_is_native_only_and_defaults_to_run ... ok
test highlights::create::highlights_create_article_dry_run_writes_nothing ... ok
test docs_reference::cli_reference_is_current ... ok
test highlights::create::highlights_create_arxiv_api_failure_falls_back_with_warning ... ok
test help::all_top_level_subcommand_help_is_safe_and_plain ... ok
test highlights::create::highlights_create_article_maps_options_to_clip ... ok
test highlights::continuations::continuation_scan_tucks_two_pages_and_is_idempotent ... ok
test highlights::create::highlights_create_article_routes_bot_wall_to_adapter ... ok
test highlights::create::highlights_create_arxiv_dry_run_shows_override_sources ... ok
test highlights::create::highlights_create_article_output_stem_becomes_marker_id ... ok
test highlights::create::highlights_create_clip_alias_is_byte_identical_on_error_path ... ok
dataview flatten RSS: tasks=2000 baseline=52.8 MiB census=57.4 MiB delta=4.6 MiB
test highlights::create::highlights_create_article_routes_through_clip_engine ... ok
test highlights::create::highlights_create_bare_force_fresh_url_dry_run_proceeds ... ok
test completion::zsh_adapter::real_zsh_first_tab_completes ... ok
test highlights::create::highlights_create_arxiv_captures_a_legacy_only_url_note_with_a_warning ... ok
test highlights::create::highlights_create_clip_alias_rereads_filed_url ... ok
test highlights::create::highlights_create_clip_alias_matches_create_for_force ... ok
test highlights::create::highlights_create_arxiv_uses_api_metadata_and_short_stem ... ok
test highlights::create::highlights_create_closed_and_plain_require_one_vault_note ... ok
test highlights::create::highlights_create_arxiv_rereads_from_original_source ... ok
test highlights::create::highlights_create_bare_force_filed_url_rereads ... ok
test highlights::create::highlights_create_collection_dry_run_skips_compose_and_writes ... ok
test highlights::create::highlights_create_collection_binds_explicit_audio ... ok
test highlights::create::highlights_create_collection_dry_run_validates_explicit_audio ... ok
test help::public_help_surfaces_do_not_list_long_only_options ... ok
test highlights::create::highlights_create_collection_failing_part_writes_nothing ... ok
test highlights::create::highlights_create_collection_listen_dry_run_prints_audio_and_would_run ... ok
test highlights::create::highlights_create_collection_overwrite_fresh_set_refuses_before_adapter ... ok
test highlights::create::highlights_create_collection_partial_overlap_with_listen_never_listens ... ok
test highlights::create::highlights_create_collection_listen_failure_leaves_vault_unchanged ... ok
test highlights::create::highlights_create_collection_listen_post_failure_hint_keeps_all_urls ... ok
test highlights::create::highlights_create_collection_listens_to_staged_pdf_before_install ... ok
test highlights::create::highlights_create_collection_partial_overlap_refuses_under_every_mode ... ok
test highlights::create::highlights_create_collection_installs_list_marker_and_scan_finds_each_part ... ok
test highlights::create::highlights_create_collection_rejects_invalid_target_lists_before_work ... ok
test highlights::create::highlights_create_collection_refuses_pdf_parts ... ok
test highlights::create::highlights_create_collection_collision_walk_and_exact_output ... ok
test highlights::create::highlights_create_collection_reread_failed_part_writes_nothing ... ok
test dataview_oom::synthetic_task_census_counts_are_exact ... ok
test help::help_routes_match_direct_help_for_root_and_nested_commands ... ok
test highlights::create::highlights_create_collection_three_parts_derives_title_and_authors ... ok
test highlights::create::highlights_create_collection_listen_attaches_to_same_set ... ok
test highlights::create::highlights_create_copies_audio_before_pdf_with_play_link ... ok
test highlights::create::highlights_create_dry_run_rejects_unknown_parent_with_hints ... ok
test highlights::create::highlights_create_dry_run_prints_plan_without_writes ... ok
dataview flatten RSS: tasks=2413 baseline=56.2 MiB census=62.4 MiB delta=6.1 MiB
test dataview_oom::synthetic_task_census_stays_under_address_space_cap ... ok
test highlights::create::highlights_create_collection_reread_guards ... ok
test dataview_oom::flatten_default_budget_fails_cli_json_and_markdown ... ok
test highlights::create::highlights_create_dry_run_resolves_parent_alias_to_canonical_route ... ok
test highlights::create::highlights_create_dry_run_reports_planned_audio_copy ... ok
test highlights::create::highlights_create_exact_output_refuses_an_existing_reference_id ... ok
test highlights::create::highlights_create_filed_url_refusal_names_next_reread ... ok
test highlights::create::highlights_create_folded_dry_run_writes_nothing ... ok
test highlights::create::highlights_create_collection_unrelated_families_ask_for_name ... ok
test highlights::create::highlights_create_diagram_doctor_warns_without_browser_and_reports_off ... ok
test highlights::create::highlights_create_collection_reread_listen_narrates_new_reading ... ok
test highlights::create::highlights_create_folded_direct_pdf_falls_back_to_slug_title ... ok
test highlights::create::highlights_create_collection_queued_only_replacement_both_modes ... ok
test highlights::corpus_gate::classifies_file_warnings_against_the_complete_gate ... ok
test highlights::create::highlights_create_folded_captures_a_legacy_only_url_note_with_a_warning ... ok
test highlights::create::highlights_create_folded_doctor_reports_web_clip_rows ... ok
test highlights::create::highlights_create_folded_force_overwrites_the_same_intake_target ... ok
test highlights::create::highlights_create_folded_library_without_url_suffixes ... ok
test highlights::create::highlights_create_folded_rejects_protocol_errors ... ok
test highlights::create::highlights_create_folded_refuses_library_and_dedupe_collisions_early ... ok
test highlights::create::highlights_create_folded_still_refuses_a_pdf_backed_url_note ... ok
test highlights::create::highlights_create_force_glued_short_is_output_path_error ... ok
test highlights::create::highlights_create_force_adopted_empty_target_matches_missing_target_usage ... ok
test highlights::create::highlights_create_force_invalid_equals_mode_is_clap_error ... ok
test highlights::create::highlights_create_force_stray_mode_guard_runs_no_adapter_and_writes_nothing ... ok
test highlights::create::highlights_create_force_repeated_flag_is_clap_usage_error ... ok
test highlights::create::highlights_create_folded_rejects_before_the_adapter_runs ... ok
test highlights::create::highlights_create_force_top_level_option_keeps_explicit_value ... ok
test highlights::create::highlights_create_collection_name_waterfall_is_local_and_options_parse_after_urls ... ok
test highlights::create::highlights_create_folded_reports_adapter_failures_with_hints ... ok
test highlights::create::highlights_create_diagram_doctor_warns_when_test_render_fails ... ok
test highlights::create::highlights_create_folded_success_writes_stamped_intake_pdf ... ok
test highlights::create::highlights_create_folded_forwards_overrides_and_html ... ok
test highlights::create::highlights_create_html_replay_rereads_without_fetch ... ok
test highlights::create::highlights_create_local_pdf_installs_and_stamps ... ok
test highlights::create::highlights_create_local_pdf_dry_run_writes_nothing_and_refuses_junk ... ok
test highlights::create::highlights_create_local_pdf_overrides_author_and_published ... ok
test highlights::create::highlights_create_collection_post_listen_recheck_keeps_narration ... ok
test highlights::create::highlights_create_local_pdf_inside_library_is_refused_with_listen_hint ... ok
test highlights::create::highlights_create_markdown_marker_carries_author_and_published ... ok
test highlights::create::highlights_create_library_pdf_as_target_refuses_reread_with_hint ... ok
test highlights::create::highlights_create_folded_round_trips_through_scan ... ok
test highlights::create::highlights_create_missing_parent_fails_before_any_work ... ok
test highlights::create::highlights_create_no_audio_skips_discovery ... ok
skipping markdown text-layer test: pandoc, xelatex, and pdftotext are required
test highlights::create::highlights_create_markdown_text_layer_avoids_hyphen_splits_and_ligatures ... ok
test highlights::create::highlights_create_local_pdf_reread_keeps_earlier_bundle_bytes ... ok
test highlights::create::highlights_create_output_dry_run_reports_direct_library_target ... ok
test highlights::create::highlights_create_output_dry_run_reports_intake_library_destination ... ok
test highlights::create::highlights_create_local_pdf_different_title_suffixes_with_id ... ok
test highlights::create::highlights_create_output_dry_run_prints_exact_path_without_writes ... ok
test highlights::create::highlights_create_output_existing_pdf_still_refuses_without_force ... ok
test highlights::create::highlights_create_markdown_renders_outside_xlib ... ok
test highlights::create::highlights_create_folded_supports_ref_type_output_and_name ... ok
test highlights::create::highlights_create_local_pdf_prepends_marker_and_snake_cases_stem ... ok
test highlights::create::highlights_create_local_pdf_title_override_and_name_type_output ... ok
test highlights::create::highlights_create_overwrite_fresh_url_refuses_before_fetch ... ok
test highlights::create::highlights_create_pdf_url_rejects_claimed_pdf_and_404 ... ok
test highlights::create::highlights_create_collection_reread_three_generations ... ok
test highlights::create::highlights_create_overwrite_filed_url_reaches_preflight ... ok
test highlights::create::highlights_create_refuses_different_audio_without_force ... ok
test highlights::create::highlights_create_pdf_url_binds_explicit_audio ... ok
test highlights::create::highlights_create_refuses_library_destination_audio ... ok
test highlights::create::highlights_create_rejects_conflicting_audio_flags ... ok
test highlights::create::highlights_create_pdf_url_colliding_slug_suffixes ... ok
test highlights::create::highlights_create_refuses_existing_library_pdf_with_or_without_force ... ok
test highlights::create::highlights_create_rejects_html_with_local_target_before_any_work ... ok
test highlights::create::highlights_create_refuses_mapped_private_literals_without_fetching ... ok
test highlights::create::highlights_create_rejects_output_combined_with_ref_type ... ok
test highlights::create::highlights_create_rejects_bad_audio_paths ... ok
test highlights::create::highlights_create_rejects_bad_published_before_any_work ... ok
test highlights::create::highlights_create_pdf_url_stamps_and_dedupes ... ok
test highlights::create::highlights_create_rejects_non_pdf_output ... ok
test highlights::create::highlights_create_refuses_each_url_in_pdf_backed_frontmatter_lists ... ok
test highlights::create::highlights_create_pdf_url_rereads_from_original_source ... ok
test highlights::create::highlights_create_rejects_non_utf8_include_id_before_writes ... ok
test highlights::create::highlights_create_plain_vault_note_keeps_snapshot_provenance ... ok
test highlights::create::highlights_create_reports_pandoc_failure_diagnostics ... ok
test highlights::create::highlights_create_reread_title_free_name_and_output_guards ... ok
test highlights::create::highlights_create_collection_rereads_exact_set_reversed ... ok
skipping vault-note real-render CLI test: missing TeX packages: titlesec.sty, lastpage.sty, xurl.sty
test highlights::create::highlights_create_renders_vault_note_snapshot_when_available ... ok
test highlights::create::highlights_create_reuses_identical_existing_companion ... ok
test highlights::create::highlights_create_local_pdf_recapture_rereads_after_scan ... ok
test highlights::create::highlights_create_reread_omits_parent_and_overrides_type_status ... ok
test highlights::create::highlights_create_reread_url_member_selection_and_rejection ... ok
test highlights::create::highlights_create_reread_listen_narrates_new_reading ... ok
test highlights::create::highlights_create_same_title_library_rereads_from_original_source ... ok
test highlights::create::highlights_create_queued_url_overwrite_replaces ... ok
test highlights::create::highlights_create_vault_note_dry_run_uses_title_parent_and_fixed_date ... ok
test highlights::create::highlights_create_same_stem_different_title_remains_a_new_capture ... ok
test highlights::create::highlights_create_reread_queued_then_scan_files_lineage ... ok
test highlights::create::highlights_create_stamps_rendered_pdf_through_shared_install ... ok
test highlights::create::landing_bare_library_pdf_renames ... ok
test highlights::create::landing_library_collision_hints_listen_attach ... ok
test highlights::create::highlights_create_url_reread_keeps_earlier_bundle_bytes ... ok
test highlights::create::landing_name_alone_does_not_embed_marker_id ... ok
test highlights::create::landing_companion_beside_source_is_copied ... ok
test highlights::create::highlights_create_vault_note_same_day_rereads ... ok
test highlights::create::route_guards_overwrite_markdown_exact_output_preparent_probe ... ok
test highlights::create::route_guards_overwrite_pdf_exact_output_tilde_preparent_probe ... ok
test highlights::create::landing_marked_pdf_outside_vault_is_refused ... ok
test highlights::create::highlights_create_warns_and_proceeds_for_legacy_list_note ... ok
test highlights::create::highlights_create_retries_without_force_never_mint_readings ... ok
test highlights::create::route_guards_overwrite_url_exact_output_replaces ... ok
test highlights::create::route_guards_library_pdf_reread_force_listen_refuses ... ok
test highlights::create::route_guards_overwrite_collection_exact_output_replaces ... ok
test highlights::diagrams::highlights_create_definition_list_dry_run_stays_browser_free ... ok
skipping mermaid degrade: pdftotext is required
test highlights::diagrams::highlights_create_mermaid_adapter_crash_invalid_and_timeout_degrade ... ok
skipping live Mermaid PDF test: missing pdftotext, pdffonts, pdfimages
test highlights::diagrams::highlights_create_live_mermaid_pdf_is_highlights_safe ... ok
test highlights::create::route_guards_redirect_guard_refuses_outside_family_via_curl ... ok
test highlights::create::ingest_characterizes_url_failure_modes ... ok
skipping mermaid kill switch: pdftotext is required
test highlights::diagrams::highlights_create_mermaid_kill_switch_skips_stub_and_prints_source ... ok
test highlights::create::route_guards_plain_reread_without_audio_has_no_narrated_hint ... ok
skipping mermaid partial: pdftotext is required
test highlights::diagrams::highlights_create_mermaid_partial_failure_keeps_note_and_exits_0 ... ok
test highlights::create::route_guards_vault_preflight_orders_before_parent ... ok
skipping definition-list Mermaid: pdftotext is required
test highlights::diagrams::highlights_create_recognizes_definition_list_mermaid_fences ... ok
skipping snapshot mermaid: pdftotext is required
skipping mermaid missing adapter: pdftotext is required
test highlights::diagrams::highlights_create_snapshot_mermaid_success_and_failure_shape ... ok
test highlights::diagrams::highlights_create_mermaid_missing_adapter_warns_and_exits_0 ... ok
skipping mermaid success: pdftotext is required
test highlights::diagrams::highlights_create_renders_mermaid_via_stub_adapter ... ok
test highlights::diagrams::highlights_create_mermaid_dry_run_counts_without_starting_tools ... ok
test highlights::create::route_guards_redirect_guard_refuses_outside_family_via_adapter ... ok
test highlights::doctor_library::doctor_coverage_warn_counts_unmirrored_zorg_records ... ok
test highlights::doctor_library::doctor_coverage_uses_provenance_mirroring ... ok
test highlights::doctor_library::doctor_annotations_warn_on_leaked_marker_mirror ... ok
test highlights::create::route_guards_plain_reread_names_narrated_reading_without_inheriting ... ok
test highlights::doctor_library::doctor_dangling_earlier_entry_warns ... ok
test highlights::doctor_library::doctor_identity_ok_reports_superseded_legacy_note ... ok
test highlights::doctor_library::doctor_identity_warn_on_identity_shared_by_two_pdfs ... ok
test highlights::doctor_library::doctor_intake_last_row_keeps_a_multiline_message_on_one_line ... ok
test highlights::doctor_library::doctor_family_identity_exempt_but_outsider_warns ... ok
test highlights::doctor_library::doctor_intake_last_row_reads_the_recorded_status ... ok
test highlights::doctor_library::doctor_library_diagnostics_warn_lists_codes_and_paths ... ok
test highlights::doctor_library::doctor_library_rows_report_ok_on_clean_vault ... ok
test highlights::doctor_library::doctor_reference_ids_allow_only_a_suffix_that_avoids_a_duplicate ... ok
test highlights::doctor_library::doctor_ref_sources_warns_on_dangling_mismatch_missing_and_orphan ... ok
test highlights::doctor_library::doctor_ref_sources_warns_on_ignored_catalog ... ok
test highlights::doctor_library::doctor_reference_ids_ok_when_ids_match_stems ... ok
test highlights::doctor_library::doctor_ref_sources_ok_counts_saved_code_blocks ... ok
test highlights::doctor_library::doctor_warns_when_a_queued_pdf_is_over_an_hour_old ... ok
test highlights::doctor_library::doctor_reference_ids_warn_on_mismatch_and_case_insensitive_duplicate ... ok
test highlights::doctor_library::doctor_xlib_row_shows_the_oldest_age_without_warning_when_fresh ... ok
test highlights::doctor_library::doctor_xlib_rows_stay_plain_when_nothing_is_queued ... ok
test highlights::create::highlights_create_collection_overwrites_exact_set_with_listen ... ok
test highlights::image_notes::image_notes_copy_embed_and_snapshot ... ok
test highlights::image_notes::image_notes_missing_source_warns_then_heals ... ok
test highlights::ingest::create_queues_for_non_git_and_other_vaults_without_touching_bob_dir ... ok
test highlights::create::highlights_create_lists_earlier_snapshots_and_hints_unread_ready ... ok
test highlights::ingest::create_rejects_an_invalid_ingest_on_create_env_before_any_write ... ok
test highlights::jobs::ref_jobs_bare_lists_empty_vault_state ... ok
test highlights::ingest::create_keeps_intake_for_flag_config_env_and_dry_run ... ok
test highlights::doctor_library::doctor_reference_ids_repair_through_rename_clears_the_row ... ok
test highlights::jobs::ref_jobs_group_flag_before_jobs_lists ... ok
test highlights::jobs::ref_jobs_list_shows_the_parent ... ok
test highlights::jobs::ref_jobs_fallback_bytes_match_capture_twin_vault ... ok
test highlights::jobs::ref_jobs_old_created_records_still_render_as_clipped ... ok
test highlights::jobs::ref_jobs_list_windows_and_json ... ok
test highlights::jobs::ref_jobs_doctor_row_tracks_pending_and_stuck ... ok
test highlights::jobs::ref_jobs_run_falls_back_on_blocked ... ok
test highlights::jobs::ref_jobs_run_falls_back_into_the_staged_parent ... ok
test highlights::jobs::ref_jobs_run_filed_family_never_mints_reread ... ok
test highlights::jobs::ref_jobs_run_clips_a_seeded_article ... ok
test highlights::jobs::ref_jobs_run_parentless_job_uses_the_source_inbox ... ok
test highlights::jobs::ref_jobs_run_uses_job_bob_dir_not_env ... ok
test highlights::jobs::ref_jobs_second_worker_exits_zero ... ok
test highlights::jobs::ref_jobs_run_rejects_an_invalid_ingest_on_create_env_before_xlib_write ... ok
test highlights::jobs::ref_jobs_run_queues_when_maintenance_lock_is_held ... ok
test highlights::ingest::create_rolls_back_pdf_when_birth_task_selection_refuses ... ok
test highlights::jobs::ref_jobs_stale_running_twice_falls_back_without_clipping ... ok
test highlights::jobs::ref_jobs_stuck_fallback_is_retried_without_clipping ... ok
test highlights::jobs::ref_jobs_unwritable_running_fails_promptly ... ok
test highlights::ingest::create_ingests_pdf_audio_note_and_parent_as_one_scoped_pushed_commit ... ok
test highlights::jobs::ref_jobs_stale_running_once_is_requeued_and_clipped ... ok
test highlights::listen::create_article_listen_uses_adapter_render ... ok
test highlights::listen::create_listen_captures_and_binds_episode ... ok
test highlights::listen::doctor_warns_for_queued_listen_feed_publish ... ok
test highlights::listen::listen_arxiv_offline_renders_via_sase ... ok
test highlights::create::highlights_create_vault_note_marker_survives_scan_and_sync ... ok
test highlights::listen::doctor_listen_rows_cover_unset_ok_and_invalid ... ok
test highlights::jobs::ref_jobs_run_ingests_into_a_synced_vault ... ok
test highlights::listen::listen_attach_refuses_when_audio_exists ... ok
test highlights::listen::listen_attaches_for_legacy_url_arxiv_note ... ok
test highlights::listen::listen_conflicts_with_audio_and_no_audio ... ok
test highlights::listen::listen_attaches_to_ref_note_capture ... ok
test highlights::listen::listen_dry_run_prints_would_run_without_invoking ... ok
test highlights::listen::listen_attaches_when_target_is_the_library_pdf ... ok
test highlights::listen::listen_attaches_to_queued_intake_pdf ... ok
test highlights::listen::listen_dry_run_uses_normalized_launcher ... ok
test highlights::listen::listen_invalid_template_is_an_error ... ok
test highlights::listen::listen_failure_writes_nothing ... ok
test highlights::listen::listen_has_no_fallback_when_sase_missing ... ok
test highlights::listen::listen_interrupted_exits_130 ... ok
test highlights::listen::listen_legacy_env_migrates_and_preserves_flags ... ok
test highlights::listen::listen_legacy_only_hit_captures_fresh_instead_of_attaching ... ok
test highlights::listen::listen_literal_values_arrive_intact ... ok
test highlights::listen::listen_markdown_binds_episode_and_play_uri ... ok
test highlights::listen::listen_pdf_url_streams_output_and_quotes_title ... ok
test highlights::listen::listen_post_listen_collision_keeps_scratch ... ok
test highlights::listen::listen_unconfigured_fails_before_fetch ... ok
test highlights::listen::listen_plugin_failure_has_no_fallback ... ok
test highlights::ingest::create_reread_files_inline_with_lineage_and_versioned_task ... ok
test highlights::listen::listen_queued_publish_warns_after_create_summary ... ok
test highlights::listen::listen_refusal_without_flag_points_at_listen ... ok
test highlights::marker::highlights_ref_comment_edit_keeps_stable_block_id ... ok
test highlights::listen::listen_without_audio_is_an_error ... ok
test highlights::listen::listen_attach_files_audio_for_a_library_capture ... ok
test highlights::marker::highlights_ref_deleted_highlight_is_tombstoned ... ok
test highlights::listen::listen_attach_files_queued_pdf_with_companion_audio ... ok
test highlights::listen::listen_wrappers_and_chains_fail_before_fetch ... ok
test highlights::marker::highlights_ref_doctor_no_hooks_reports_skipped ... ok
test highlights::marker::highlights_ref_conflicting_edits_fail_and_prefer_frontmatter_resolves ... ok
test highlights::marker::highlights_ref_doctor_checks_vault_git_without_writes ... ok
test highlights::marker::highlights_ref_doctor_reports_configured_pre_scan_executable ... ok
test highlights::marker::highlights_ref_doctor_warns_on_orphan_companion_audio ... ok
test highlights::marker::highlights_ref_frontmatter_missing_parent_fails_before_pdf_writeback ... ok
test highlights::marker::highlights_ref_doctor_warns_on_missing_latex_packages ... ok
test highlights::marker::highlights_ref_marker_uses_first_page_text_annotation ... ok
test highlights::marker::highlights_ref_deprecated_done_status_migrates_to_read_with_pdf_write ... ok
test highlights::marker::highlights_ref_frontmatter_unsupported_status_fails_before_pdf_writeback ... ok
test highlights::marker::highlights_ref_marker_edit_updates_frontmatter ... ok
test highlights::marker::highlights_ref_rejects_wikilink_marker_parent_before_writes ... ok
test highlights::marker::highlights_ref_short_options_are_accepted ... ok
test highlights::marker::highlights_ref_frontmatter_edit_updates_marker_when_pdf_writes_enabled ... ok
test highlights::marker_write::attended_scan_bypasses_the_reading_hold ... ok
test highlights::marker::highlights_ref_dry_run_and_inspection_do_not_modify_vault_files ... ok
test highlights::marker::highlights_ref_non_overlapping_edits_auto_merge_and_settle ... ok
test highlights::marker_write::json_unattended_scan_counts_a_hold_as_neither_note_nor_failure ... ok
test highlights::marker_write::key_off_scan_ignores_the_reading_probe_and_omits_coordination_header ... ok
test highlights::marker_write::unattended_scan_holds_editor_active_when_the_probe_says_reading ... ok
test highlights::marker_write::verbose_unattended_scan_names_the_reading_hold ... ok
test highlights::marker_write::ref_sync_bypasses_the_reading_hold ... ok
test highlights::overwrite::refusal_leaves_vault_and_intent_unchanged ... ok
test highlights::overwrite::writing_create_and_intake_scan_recover_crashed_overwrite ... ok
test highlights::overwrite::overwrite_preserves_task_children_relations_freshness_and_inbound_links ... ok
test highlights::create::highlights_create_vault_note_dry_run_reports_image_processing ... ok
test highlights::overwrite::unrelated_dirty_and_staged_files_survive_overwrite ... ok
test highlights::overwrite::frozen_archive_is_inert_across_list_find_doctor_and_create ... ok
test highlights::diagrams::highlights_create_without_mermaid_does_not_spawn_stub ... ok
test highlights::overwrite_annotated::coordination_key_on_still_refuses_annotated_overwrite_off_macos ... ok
test highlights::diagrams::highlights_create_mermaid_scale_warning_when_figure_is_wide ... ok
test highlights::overwrite_annotated::dirty_inbound_highlight_file_wins_over_annotated_gate ... ok
test highlights::overwrite_annotated::dry_run_previews_annotated_archive_and_writes_nothing ... ok
test highlights::overwrite::leftover_committed_intent_then_second_overwrite_of_same_stem ... ok
test highlights::overwrite_annotated::explicit_output_flag_still_wins_on_annotated_targets ... ok
test highlights::overwrite_annotated::exact_set_collection_refuses_annotated_target_before_adapter ... ok
test highlights::jobs::ref_jobs_slow_clip_still_drains_a_late_job ... ok
test highlights::overwrite_annotated::open_annotation_task_in_highlights_region_refuses_before_host_gate ... ok
test highlights::overwrite_local::free_name_on_title_route_is_still_fresh_for_overwrite ... ok
test highlights::overwrite_local::library_pdf_target_still_refuses_overwrite ... ok
test highlights::overwrite::no_prose_overwrite_removes_each_sidecar_shape_and_stays_stable ... ok
test highlights::overwrite_local::local_pdf_overwrite_dry_run_writes_nothing ... ok
test highlights::overwrite::two_same_day_prose_overwrites_keep_distinct_archives_and_family ... ok
test highlights::overwrite_local::bare_local_reread_hints_at_overwrite_on_real_and_dry_runs ... ok
test highlights::overwrite_local::local_pdf_overwrite_archives_authored_prose ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_failure_leaves_bytes_unchanged ... ok
test highlights::overwrite_local::local_pdf_overwrite_audio_extension_replaces_companion ... ok
test highlights::overwrite_local::local_pdf_overwrite_changes_title ... ok
test highlights::create::highlights_create_output_renders_pdf_at_requested_path_when_available ... ok
test highlights::create::highlights_create_renders_pdf_with_outline_and_marker_when_available ... ok
test highlights::create::highlights_create_reports_paired_links_and_dead_warnings_when_available ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_failure_after_narration_keeps_scratch ... ok
test highlights::overwrite_local::local_pdf_overwrite_marker_failure_after_narration_keeps_scratch ... ok
test highlights::overwrite_local::local_pdf_overwrite_keeps_archived_closed_task ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_replaces_companion ... ok
test highlights::overwrite_annotated::linux_refuses_each_annotation_kind_before_render_and_leaves_vault ... ok
test highlights::overwrite_local::local_pdf_overwrite_replaces_in_place_without_archive ... ok
test highlights::overwrite_local::local_pdf_overwrite_preserves_blocked_overlay ... ok
test highlights::overwrite_local::markdown_overwrite_ignored_catalog_warns_and_commits_source ... ok
test highlights::overwrite_local::no_force_overwrite_remedy_uses_the_selected_reading ... ok
test highlights::overwrite_local::overwrite_carries_aliases_topics_and_research ... ok
test highlights::overwrite_local::overwrite_refuses_disabled_ingest_and_unstampable_status_before_render ... ok
test highlights::overwrite_local::local_pdf_overwrite_selected_older_reading ... ok
test highlights::overwrite_local::markdown_overwrite_uses_fake_pandoc_and_skips_it_on_dry_run ... ok
test highlights::overwrite_local::overwrite_kept_closed_task_reports_reopen_hint_inline ... ok
test highlights::overwrite_local::overwrite_refuses_gitignored_sidecar_file_as_dirty_paths ... ok
test highlights::overwrite_local::overwrite_preserves_custom_task_alias ... ok
test highlights::overwrite_local::local_pdf_overwrite_preserves_wip_and_explicit_ready ... ok
test highlights::overwrite_recovery::overwrite_recovery_blocks_dry_run_create ... ok
test highlights::overwrite_recovery::overwrite_recovery_reports_pending_in_json_dry_run ... ok
test highlights::overwrite_recovery::overwrite_recovery_keeps_committed_overwrite_on_scan ... ok
test highlights::overwrite_recovery::overwrite_recovery_reverses_annotated_pdf_move_on_scan ... ok
test highlights::overwrite_recovery::overwrite_recovery_rolls_back_on_writing_scan ... ok
test highlights::overwrite_local::overwrite_reports_final_state_and_commit ... ok
test highlights::overwrite_recovery::task_move_refuses_while_overwrite_intent_is_pending ... ok
test highlights::overwrite_local::local_pdf_overwrite_keeps_and_replaces_audio ... ok
test highlights::overwrite_local::overwrite_refuses_incompatible_flags_without_writing ... ok
test highlights::overwrite_local::markdown_overwrite_repoints_and_reuses_unchanged_bytes ... ok
test highlights::overwrite_local::overwrite_without_title_change_keeps_task_file_byte_identical ... ok
test highlights::overwrite_recovery::vault_sync_recovers_a_planted_overwrite_intent ... ok
test highlights::overwrite_web::annotated_web_target_refuses_without_network ... ok
test highlights::overwrite_local::overwrite_root_without_title_change_adds_no_version_suffix ... ok
test highlights::overwrite_local::vault_note_same_day_overwrite_plain_markdown ... ok
test highlights::overwrite_local::pdf_overwrite_clears_source_markdown ... ok
test highlights::overwrite_web::article_overwrite_replaces_filed_reference ... ok
test highlights::overwrite_web::arxiv_overwrite_keeps_api_metadata ... ok
test highlights::overwrite_web::bare_web_reread_hints_at_dry_run ... ok
test highlights::overwrite_local::overwrite_refuses_all_remaining_preflight_codes_without_writing ... ok
test highlights::overwrite_local::overwrite_same_stem_source_selects_named_member ... ok
test highlights::overwrite_local::overwrite_title_change_keeps_old_version_suffix ... ok
test highlights::overwrite_web::pdf_url_overwrite_clears_source_markdown ... ok
test highlights::overwrite_web::web_overwrite_dry_run_writes_nothing_without_network ... ok
test highlights::overwrite_web::pdf_link_annotations_for_navigation_and_audio_do_not_refuse ... ok
test highlights::replaced_capture::explicit_sync_holds_in_human_and_dry_run_modes ... ok
test highlights::overwrite_web::pdf_url_overwrite_stamps_fetched_pdf ... ok
test highlights::overwrite_web::web_overwrite_refuses_disabled_ingest_before_dry_run_or_network ... ok
test highlights::overwrite_web::web_overwrite_redirect_to_other_family_refuses ... ok
test highlights::replaced_capture::human_scan_holds_v1_and_v2_before_import_and_continues_other_pdfs ... ok
test highlights::scan::highlights_ref_scan_allows_duplicate_basenames_in_different_ref_types ... ok
test highlights::scan::highlights_ref_scan_continues_after_write_failure ... ok
test highlights::scan::highlights_ref_scan_default_output_reports_inline_errors ... ok
test highlights::scan::highlights_ref_scan_detects_same_target_collision_before_writing ... ok
test highlights::scan::highlights_ref_scan_dry_run_previews_xlib_intake_without_writes ... ok
test highlights::scan::highlights_ref_scan_dry_run_reports_valid_and_invalid_pdfs ... ok
test highlights::replaced_capture::json_scan_checks_all_archives_and_keeps_dry_run_holds_as_previews ... ok
test highlights::scan::highlights_ref_scan_groups_routed_tasks_with_parallel_jobs ... ok
test highlights::scan::highlights_ref_scan_default_output_is_concise ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_pdf_and_writes_note_in_same_run ... ok
test highlights::scan::highlights_ref_scan_intakes_pdf_and_mp3_and_embeds_player ... ok
test highlights::overwrite_web::saved_html_overwrite_replays_without_fetch ... ok
test highlights::scan::highlights_ref_scan_refuses_audio_destination_conflict ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_sidecars_with_pdfs ... ok
test highlights::scan::highlights_ref_scan_refuses_xlib_intake_conflict_before_writes ... ok
test highlights::scan::highlights_ref_scan_recurses_dry_runs_and_writes_multiple_pdfs ... ok
test highlights::scan::highlights_ref_scan_late_pairs_audio_onto_existing_note ... ok
test highlights::scan::highlights_ref_scan_jobs_flag_matches_sequential_output ... ok
test highlights::scan::highlights_ref_scan_round_trips_provenance_marker_fields ... ok
test highlights::scan::highlights_ref_scan_treats_later_page_note_as_missing_marker ... ok
test highlights::scan::highlights_ref_scan_writes_valid_pdfs_despite_invalid_pdf ... ok
test highlights::scan::ref_scan_human_dry_run_ignores_maintenance_lock ... ok
test highlights::scan::ref_scan_human_lock_busy_when_maintenance_lock_held ... ok
test highlights::scan::ref_scan_holds_every_plan_rejecting_a_shared_dirty_route ... ok
test highlights::scan::ref_scan_human_scan_busy_when_writer_lock_held ... ok
test highlights::scan::ref_scan_human_hard_failure_writes_error_receipt ... ok
test highlights::scan::ref_scan_default_destination_exemption_is_not_shared_with_explicit_route ... ok
test highlights::scan::highlights_ref_scan_stamps_created_on_category_and_intake_notes ... ok
test highlights::scan::ref_scan_json_dry_run_ignores_maintenance_lock ... ok
test highlights::scan::ref_scan_human_scan_writes_equivalent_receipt ... ok
test highlights::scan::ref_scan_json_dry_run_ignores_writer_lock ... ok
test highlights::scan::ref_scan_json_dry_run_plans_intake_without_writing ... ok
test highlights::scan::ref_scan_json_hard_failure_writes_error_receipt ... ok
test highlights::scan::ref_scan_json_dry_run_writes_no_receipt ... ok
test highlights::scan::ref_scan_json_lock_busy_when_maintenance_lock_held ... ok
test highlights::scan::ref_scan_json_lock_busy_writes_no_receipt ... ok
test highlights::overwrite_local::markdown_overwrite_keeps_play_link_for_kept_audio ... ok
test highlights::overwrite_web::web_overwrite_rollback_removes_new_store ... ok
test highlights::scan::ref_scan_json_receipt_failure_only_warns ... ok
test highlights::scan::ref_scan_json_scan_busy_when_writer_lock_held ... ok
test highlights::scan::ref_scan_json_receipt_matches_stdout ... ok
test highlights::scan::ref_scan_json_intake_lists_pdf_only_when_audio_moves_alone ... ok
test highlights::scan::ref_scan_json_partial_failure_reports_pdf_stage_and_message ... ok
test highlights::scan::ref_scan_json_marker_write_direct_with_status_change ... ok
test highlights::overwrite_web::web_overwrite_listen_narrates_replacement ... ok
test highlights::scan::ref_scan_writes_when_maintenance_lock_is_free ... ok
test highlights::scan::ref_scan_json_holds_dirty_pdf_and_writes_clean_independent_pdf ... ok
test highlights::scan_hooks::highlights_ref_scan_dry_run_reports_env_pre_scan_without_executing ... ok
test highlights::scan_hooks::highlights_ref_scan_fails_when_pre_scan_hook_fails ... ok
test highlights::scan::ref_sync_writes_no_receipt ... ok
test highlights::overwrite_web::web_collection_overwrite_repoints_new_bytes ... ok
test highlights::scan_hooks::highlights_ref_scan_hook_child_sees_in_hook_marker ... ok
test highlights::scan_hooks::highlights_ref_scan_empty_env_disables_configured_pre_scan ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_before_subcommand_skips_configured_hook ... ok
test highlights::overwrite_web::every_annotation_source_refuses_with_the_contract_remedy ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_after_subcommand_skips_configured_hook ... ok
test highlights::scan::ref_scan_json_success_envelope_names_created_and_updated_notes ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_env ... ok
test highlights::scan::ref_scan_json_dirty_note_is_a_successful_hold ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_command_key ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_overrides_env_hook ... ok
test highlights::scan_hooks::ref_scan_json_hook_failure_error_envelope ... ok
test highlights::scan_hooks::ref_scan_json_hook_stdout_reaches_stderr_not_stdout ... ok
test highlights::scan_hooks::highlights_ref_scan_runs_configured_pre_scan_before_xlib_intake ... ok
test highlights::overwrite_web::web_overwrite_selects_older_member_with_name ... ok
test highlights::scan_intake::intake_only_empty_queue_writes_no_receipt ... ok
test highlights::scan_intake::intake_only_conflicts_with_write_pdfs ... ok
test highlights::scan_intake::full_scan_aborts_before_moving_any_queued_reread_with_an_occupant ... ok
test highlights::overwrite_web::web_overwrite_frozen_note_keeps_old_pointer ... ok
test highlights::scan_intake::full_scan_files_queued_reread_with_lineage ... ok
test highlights::scan_intake::intake_only_dry_run_previews_without_locks_or_writes ... ok
test highlights::overwrite_web::web_overwrite_without_source_view_clears_pointer ... ok
test highlights::scan_intake::intake_only_fails_with_lock_busy_when_work_waits_behind_the_lock ... ok
test highlights::scan_intake::intake_only_leaves_a_library_pdf_without_a_note_alone ... ok
test highlights::scan_intake::intake_only_hard_fails_when_pre_sync_cannot_pull ... ok
test highlights::scan_intake::intake_only_files_version_looking_pdf_without_predecessor_as_ordinary ... ok
test highlights::scan_intake::intake_only_json_dry_run_lists_would_queue_items_with_ok_true ... ok
test highlights::scan_intake::intake_only_drains_a_queued_pdf_into_one_pushed_commit ... ok
test highlights::scan_intake::intake_only_attaches_audio_to_an_existing_reread ... ok
test highlights::scan_intake::intake_only_files_queued_reread_with_lineage_and_stable_second_scan ... ok
test highlights::scan_intake::intake_only_human_drain_writes_receipt ... ok
test highlights::scan_intake::intake_only_files_each_queued_pdf_in_its_own_commit ... ok
test highlights::scan_intake::intake_only_attaches_late_audio_to_a_library_pdf ... ok
test highlights::scan_intake::intake_only_json_drain_writes_matching_receipt ... ok
test highlights::scan_intake::intake_only_preview_reports_a_queued_reread_occupant ... ok
test highlights::scan_integration::v2_adoption_reports_neither_created_nor_updated ... ok
test highlights::scan_integration::v2_alias_parent_resolves_to_canonical_residence ... ok
test highlights::scan_integration::v2_ambiguity_leaves_bytes_unchanged_with_pdf_writes ... ok
test highlights::scan_intake::intake_only_with_an_empty_queue_takes_no_lock_and_exits_zero ... ok
test highlights::scan_integration::v2_archive_reopen_inserts_fresh_task_with_suffixed_id ... ok
test highlights::scan_integration::v2_birth_honors_configured_ref_dir ... ok
test highlights::scan_integration::v2_archive_move_dedups_follow_up ... ok
test highlights::scan_integration::v2_birth_without_tasks_heading_creates_section ... ok
test highlights::scan_intake::intake_only_preserves_version_in_long_stem_task_ids ... ok
test highlights::scan_integration::v2_concise_scan_flags_open_v1_with_migrate_hint ... ok
test highlights::scan_integration::v2_destination_collision_suffixes_preview_id ... ok
test highlights::scan_integration::v2_dry_run_writes_nothing ... ok
test highlights::scan_integration::v2_deleted_managed_embed_heals_without_new_task ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_updates ... ok
test highlights::scan_intake::intake_status_records_a_writing_full_scan_but_not_a_dry_run ... ok
test highlights::scan_intake::intake_status_records_a_queued_drain_as_a_failure ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_creations ... ok
test highlights::scan_integration::v2_dirty_parent_accepts_default_follow_up ... ok
test highlights::scan_integration::v2_failed_pdf_does_not_consume_sibling_follow_up ... ok
test highlights::overwrite_web::web_overwrite_repoints_and_reuses_unchanged_bytes ... ok
test highlights::scan_integration::v2_fallback_parent_uses_inbox_with_warning ... ok
test highlights::scan_integration::v2_json_scan_reports_births_without_human_lines ... ok
test highlights::scan_integration::v2_orphan_recovery_adopts_existing_task ... ok
test highlights::scan_integration::v2_missing_task_never_gains_automatic_replacement ... ok
test highlights::scan_intake::intake_only_json_reports_filed_notes_and_queued_items ... ok
test highlights::scan_integration::v2_multiple_open_tasks_refuse_replacement ... ok
test highlights::scan_integration::v2_parallel_matches_sequential ... ok
test highlights::scan_integration::v2_moved_task_residence_heals_embed ... ok
test highlights::scan_integration::v2_ready_parent_accepts_default_follow_up ... ok
test highlights::scan_integration::v2_sidecar_free_birth_pins_created_date ... ok
test highlights::scan_integration::v2_same_stem_in_two_categories_stays_distinct ... ok
test highlights::scan_integration::v2_lifecycle_needs_opt_in_and_settles_on_rerun ... ok
test highlights::scan_integration::v2_parent_move_settles_without_pdf_opt_in ... ok
test highlights::scan_integration::v2_opt_in_refreshes_stale_marker_hint ... ok
test highlights::scan_integration::v2_single_pdf_report_names_performed_reading_write ... ok
test highlights::scan_integration::v2_two_births_share_one_parent_and_settle ... ok
test highlights::stale_save::dry_run_previews_the_stale_restore ... ok
test highlights::stale_save::no_write_pdfs_skips_restore_alone_without_refusal ... ok
test highlights::stale_save::replaced_hash_drops_on_a_note_write_that_observes_agreement ... ok
test highlights::stale_save::v1_stale_save_keeps_next_lane_and_restores_marker ... ok
test highlights::scan_integration::v2_scan_groups_copied_tasks_without_changing_json_shape_or_files ... ok
test highlights::stale_save::json_marker_write_restored_is_true_for_a_stale_save ... ok
test highlights::stale_save::missing_replaced_hash_disables_the_guard ... ok
test highlights::stale_save::genuine_marker_edit_is_still_adopted ... ok
test highlights::scan_intake::intake_only_queues_a_stem_taken_by_a_peer_and_exits_nonzero ... ok
test highlights::scan_intake::intake_only_queues_late_audio_when_the_marker_needs_a_pdf_write ... ok
test highlights::stale_save::v2_gesture_during_stale_save_applies_without_conflict ... ok
test highlights::scan_intake::intake_only_refuses_fabricated_reread_occupants_and_recovers ... ok
test highlights::scan_intake::intake_status_records_drain_success_and_doctor_shows_it ... ok
test highlights::stale_save::v2_stale_save_does_not_reopen_a_finished_task ... ok
test highlights::stale_save::v2_stale_save_keeps_next_lane_and_restores_marker ... ok
test highlights::sync::highlights_ref_sync_dry_run_reads_literal_marker_newlines ... ok
test highlights::store_gaps::store_dry_run_prints_planned_pointer_and_writes_nothing ... ok
test highlights::sync::highlights_ref_sync_maps_relative_pdf_paths_through_a_symlinked_vault ... ok
test highlights::sync::highlights_ref_sync_preserves_legacy_research_frontmatter ... ok
test highlights::store_gaps::store_output_outside_library_writes_no_store ... ok
test highlights::sync::highlights_ref_sync_creates_note_frontmatter_from_marker_pdf_note ... ok
test highlights::sync::highlights_ref_sync_allows_dirty_tracked_frontmatter_writeback ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_parent_without_note_write ... ok
test highlights::sync::highlights_ref_sync_refuses_dirty_target_note_before_writing ... ok
test highlights::sync::highlights_ref_sync_preserves_authored_created_and_rejects_marker_created ... ok
skipping snapshot route test: missing TeX packages: titlesec.sty, lastpage.sty, xurl.sty
test highlights::sync::highlights_ref_sync_rejects_unsupported_marker_status_without_note_write ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_status_without_note_write ... ok
test highlights::store_gaps::store_snapshot_create_records_note_snapshot_route ... ok
test highlights::sync::highlights_ref_sync_resolves_relative_library_pdf_paths_before_mapping ... ok
test highlights::sync::highlights_ref_sync_rejects_malformed_and_duplicate_marker_lists ... ok
test highlights::sync::highlights_ref_sync_stamps_cancellation_date_when_it_cancels_ref_task ... ok
test highlights::sync_tasks::highlights_ref_sync_beautifies_linked_sidecar_rendering ... ok
test highlights::sync::highlights_ref_sync_sets_created_timestamp_on_new_sidecar_free_note ... ok
test highlights::sync_tasks::highlights_ref_sync_creates_tasks_from_pdf_note_task_bullets ... ok
test highlights::sync_tasks::highlights_ref_sync_missing_routed_target_fails_before_writes ... ok
test highlights::sync_tasks::highlights_ref_sync_keeps_created_fixed_across_sidecar_updates ... ok
test highlights::sync_tasks::highlights_ref_sync_creates_annotation_tasks_for_open_statuses ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_sidecar_highlights_and_notes ... ok
test highlights::sync_tasks::highlights_ref_sync_drops_leaked_mirror_without_tombstone ... ok
test highlights::sync_tasks::highlights_ref_sync_preserves_manual_sections_and_rejects_missing_markers ... ok
test highlights::sync::highlights_ref_sync_stamps_completion_date_when_it_closes_ref_task ... ok
test highlights::sync_tasks::highlights_ref_sync_drops_color_grouped_mirror_without_tombstone ... ok
test highlights::sync_tasks::highlights_ref_sync_supports_linked_sidecar_style ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_vault_scan_when_no_annotation_candidates ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_legacy_highlight_task_property ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_textbundle_image_selections ... ok
test highlights::sync_tasks::highlights_ref_sync_routes_annotation_tasks_to_existing_root_note ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_annotation_tasks_for_terminal_statuses ... ok
test highlights::tasks::highlights_ref_task_cancelled_scan_write_pdfs_writes_pdf_marker ... ok
test highlights::tasks::highlights_ref_task_cancelled_competing_status_edits_fail ... ok
test highlights::store_gaps::store_rename_keeps_pointer_and_store_directory ... ok
test highlights::tasks::highlights_ref_status_abandoned_rewrites_generated_task_to_cancelled ... ok
test highlights::tasks::highlights_ref_blocked_task_syncs_as_status_neutral_overlay ... ok
test highlights::tasks::highlights_ref_task_checked_dirty_tracked_note_is_allowed ... ok
test highlights::store_gaps::store_plain_note_create_records_plain_route_with_source_note ... ok
test highlights::tasks::highlights_ref_task_cancelled_dry_run_requires_and_writes_pdf_marker ... ok
test highlights::tasks::highlights_ref_task_checked_competing_status_edits_fail ... ok
test highlights::store_gaps::store_write_failure_warns_and_files_without_pointer ... ok
test highlights::url_routing::url_routing_duplicate_refuses_before_missing_parent ... ok
test highlights::store_gaps::store_ignored_catalog_warns_but_files_reference ... ok
test highlights::url_routing::url_routing_doctor_prints_routing_row ... ok
test highlights::url_routing::url_routing_in_library_matches_create_refusal ... ok
test highlights::url_routing::url_routing_in_intake_matches_create_refusal ... ok
test highlights::underlines::standalone_underline_reason_appears_in_sync_and_scan_json ... ok
test highlights::url_routing::url_routing_legacy_matches_create_warning ... ok
test highlights::tasks::highlights_ref_task_checked_scan_creates_annotation_tasks_before_closing ... ok
test highlights::store_gaps::store_markdown_create_records_route_and_pointer ... ok
test highlights::tasks::highlights_ref_task_checked_sync_imports_ready_annotation_tasks_before_closing ... ok
test highlights::tasks::highlights_ref_task_checked_sync_creates_annotation_tasks_before_closing ... ok
test highlights::tasks::highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker ... ok
test highlights::underlines::underline_scan_merges_comment_and_stays_idempotent ... ok
test highlights::tasks::highlights_ref_task_ready_scan_reopens_read_ref_to_ready ... ok
test move_done::move_done_tasks_moves_canceled_tasks_in_non_repo_vault ... ok
test move_done::move_done_tasks_commits_link_repairs_with_collection_changes ... ok
test move_done::move_done_tasks_commits_and_pushes_collection_changes_only ... ok
test move_done::move_done_tasks_commits_metadata_only_archive_repairs ... ok
test move_done::move_done_tasks_commits_metadata_only_source_updates ... ok
test move_done::move_done_tasks_rewrites_stayed_pathless_links_in_archive ... ok
test move_done::move_done_tasks_warns_and_skips_git_for_non_repo_vault ... ok
test plan::plan_counts_only_visible_lane_tasks ... ok
test move_done::move_done_tasks_deduplicates_archive_block_ids_and_repairs_links ... ok
test move_done::move_done_tasks_rewrites_dirty_candidate_files ... ok
test plan::plan_help_lists_options_alphabetically ... ok
test move_done::move_done_tasks_rewrites_dirty_link_repair_files ... ok
test plan::plan_human_shows_derived_chip_for_unnamed_entry ... ok
test plan::plan_json_entries_include_derived_project_homes ... ok
test plan::plan_loads_a_config_that_still_has_max_now ... ok
test plan::plan_placeholder_only_section_shows_daily_file ... ok
test plan::plan_rejects_invalid_config_with_exit_2 ... ok
test plan::plan_reports_full_budget_as_json ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_archive ... ok

thread 'plan::plan_reports_human_budget_without_ansi_when_piped' (227349) panicked at tests/cli/plan.rs:301:5:
expected meters:
bob plan - Wed 2026-09-30 - 2026/20260930.md

  PLAN  3/3 types - 6/10 links      TODAY 6 - PENDING 2/10 - NEXT 1/15

  ★ GOALS  ▶ 0945-1015  3 links
    DECKS               2 links
    BOB                 2 links
    PLAN   exempt       0 links

  TODAY
    [*] sase.md#^fix-it        Fix it
    [/] bob.md#^capture-stop   Better capture stop
    [/] sase.md#^second        Second pass
    [ ] decks.md#^d-one        D one
    [?] decks.md#^d-two        D two
    [ ] 2026/20260930.md#^gtd  Gtd chore

  warning [[missing#^q]] does not resolve to a vault note (line 14)  today_link_unresolved

test plan::plan_reports_human_budget_without_ansi_when_piped ... FAILED
test plan::plan_reports_lane_over_cap_without_changing_status ... ok
test plan::plan_lints_unconfigured_theme_and_invalid_themes_block ... ok
test plan::plan_reports_over_cap_with_lints ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_source ... ok
test plan::plan_without_pomodoros_section_still_shows_lanes ... ok
test plan::plan_without_daily_note_still_shows_today_zero_and_lanes ... ok
test plugins::plugins_default_subcommand_runs_list ... ok
test plugins::plugins_list_json_is_machine_readable ... ok
test highlights::web_source_store::web_article_exact_output_saves_nothing ... ok
test plugins::plugins_list_renders_table_and_summary ... ok
test plugins::plugins_list_unreadable_repo_reports_error ... ok
test highlights::store_gaps::store_reread_gets_new_directory_and_pointer ... ok
test plugins::plugins_sync_backs_up_overwritten_file ... ok
test plugins::plugins_list_and_json_report_uncommitted_deployment ... ok
test plugins::plugins_sync_dry_run_json_writes_nothing ... ok
test highlights::web_source_store::web_article_create_without_source_view_files_without_pointer ... ok
test plugins::plugins_sync_bare_from_resolved_checkout_is_allowed ... ok
test highlights::create::highlights_create_stamps_return_links_marker_only_when_links_paired ... ok
test plugins::plugins_sync_dry_run_reports_without_writing ... ok
test plugins::plugins_sync_bare_from_unrelated_cwd_is_allowed ... ok
test plugins::plugins_list_no_pull_uses_existing_checkout ... ok
test plugins::plugins_sync_json_reports_errors_as_object ... ok
test plugins::plugins_list_pulls_repo_before_analysis ... ok
test plugins::plugins_sync_preserves_runtime_data_json ... ok
test plugins::plugins_list_json_stdout_stays_machine_readable_after_pull ... ok
test plugins::plugins_sync_json_reports_file_actions ... ok
test pomodoro::pomodoro_accepts_legacy_unbolded_inline_duration_field_in_time_range ... ok
test plugins::plugins_sync_single_plugin_copies_only_that_plugin ... ok
test pomodoro::pomodoro_formats_native_pomodoro_status ... ok
test pomodoro::pomodoro_missing_day_file_is_a_successful_noop ... ok
test pomodoro::pomodoro_named_session_skips_home_resolution ... ok
test pomodoro::pomodoro_prints_derived_chip_for_unnamed_linked_session ... ok
test pomodoro::pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test pomodoro::pomodoro_unnamed_unlinked_session_prints_range_only ... ok
test plugins::plugins_sync_explicit_repo_from_foreign_checkout_is_allowed ... ok
test plugins::plugins_sync_bare_from_foreign_checkout_refuses_before_pull_or_copy ... ok
test highlights::web_source_store::web_article_queued_create_birth_adopts_store ... ok
test plugins::plugins_sync_clean_landing_reconciles_then_updates ... ok
test plugins::plugins_sync_git_vault_requires_ignored_stamp ... ok
test pomodoro::tmux_pomodoro_appends_named_budget_meter ... ok
test pomodoro::tmux_pomodoro_formats_native_pomodoro_status ... ok
test pomodoro::tmux_pomodoro_omits_meter_without_pomodoros_section ... ok
test pomodoro::tmux_pomodoro_prints_derived_chip_for_unnamed_linked_session ... ok
test pomodoro::tmux_pomodoro_reverses_over_cap_meter ... ok
test projects::list::projects_list_ignores_leftover_rollup_key ... ok
test plugins::plugins_sync_refuses_dirty_vault_file_then_forces ... ok
test projects::list::projects_list_reports_invalid_and_duplicate_inline_prj_scheduled ... ok
test projects::list::projects_list_reports_prj_errors_without_aborting_scan ... ok
test highlights::web_source_store::web_article_create_saves_source_and_catalog ... ok
test pomodoro::pomodoro_show_stale_keeps_no_open_day_empty ... ok
test projects::list::projects_list_scans_project_notes_and_renders_counts ... ok
test projects::schedule::projects_schedule_errors_are_per_file_and_leave_invalid_file_untouched ... ok
test pomodoro::script_pomodoro_accepts_inline_duration_field_in_time_range ... ok
test projects::schedule::projects_sync_shows_sole_prj_task_when_schedule_is_due ... ok
test pomodoro::script_pomodoro_accepts_legacy_unbolded_time_range ... ok
test projects::schedule::projects_sync_surfaces_due_scheduled_project_with_only_closed_tasks ... ok
test projects::schedule::projects_sync_propagates_scheduled_task_properties_at_date_boundary ... ok
test projects::sync::projects_sync_does_not_hoist_without_open_prj ... ok
test projects::sync::projects_sync_marks_canceled_subproject_same_run ... ok
test projects::sync::projects_sync_normalizes_mangled_subprojects_line ... ok
test projects::sync::projects_sync_keeps_pruned_closed_entries_gone ... ok
test projects::sync::projects_sync_preserves_user_sub_bullets_and_inserts_subprojects_line ... ok
test pomodoro::script_pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test pomodoro::pomodoro_worked_reports_closed_ledger_total_only_when_status_is_empty ... ok
test plugins::plugins_sync_pulls_repo_before_copying ... ok
test projects::sync::projects_sync_reports_prj_errors_without_aborting_scan ... ok
test projects::sync::projects_sync_subproject_line_dry_run_reports_without_writing ... ok
test projects::sync::projects_sync_reopens_parent_ledger_when_child_prj_is_reopened_same_run ... ok
test projects::sync::projects_sync_treats_children_without_open_prj_as_childless ... ok
test projects::sync::projects_sync_orders_open_then_closed_subprojects_in_one_run ... ok
test projects::sync::projects_sync_hides_parent_projects_with_open_subprojects ... ok
test highlights::web_source_store::web_collection_create_saves_one_source_and_catalog ... ok
test projects::sync::projects_sync_reconciles_future_subproject_markers_at_date_boundary ... ok
test ready::overview_all_clear_reports_room ... ok
test projects::sync::projects_sync_unhides_parent_when_child_prj_is_checked_same_run ... ok
test ready::cap_preview_rejects_out_of_range_values ... ok
test ready::cap_preview_replaces_only_the_default ... ok
test ready::ready_help_documents_usage_options_and_environment ... ok
test ready::ready_rejects_invalid_config_with_exit_2 ... ok
test ready::overview_all_expands_room_empty_and_lints ... ok
test ready::overview_human_has_sections_order_and_no_ansi ... ok
test ready::overview_json_reports_totals_and_order ... ok
skipping adopt orphan dry run: pdftotext is required
test ref_library::attach::attach_adoption_dry_run_writes_nothing ... ok
test projects::sync::projects_sync_updates_status_prj_hide_tag_warns_and_is_idempotent ... ok
test plugins::plugins_sync_refuses_dirty_deploy_from_another_checkout ... ok
skipping adopt orphan saved source: pdftotext is required
test ref_library::attach::attach_adopts_an_orphan_without_search_and_preserves_catalog ... ok
test ready::worklist_json_carries_tasks_and_also ... ok
skipping real-render lost-glyph adoption: pdftotext is required
test ref_library::attach::attach_adopts_an_exact_render_with_one_lost_pdf_glyph ... ok
skipping ambiguous orphan saved sources: pdftotext is required
test ref_library::attach::attach_ambiguous_saved_sources_never_fall_through_to_search ... ok
skipping attach one-pass ambiguous stem: pdftotext is required
test ref_library::attach::attach_attaches_single_passing_ambiguous_candidate ... ok
skipping attach dry run: pdftotext is required
test ref_library::attach::attach_dry_run_verifies_but_writes_nothing ... ok
skipping attach explicit pair: pdftotext is required
test ref_library::attach::attach_explicit_pair_attaches_despite_title_mismatch ... ok
test ready::check_exits_3_when_crowded_and_0_when_clear ... ok
test ready::worklist_lists_file_order_with_also_here ... ok
skipping JSON saved-source fallback: pdftotext is required
test ref_library::attach::attach_json_reports_failed_saved_source_before_search_fallback ... ok
skipping JSON adoption write: pdftotext is required
skipping attach JSON verdicts: pdftotext is required
test ref_library::attach::attach_json_write_mode_keeps_adoption_stdout_parseable ... ok
test ref_library::attach::attach_json_names_every_candidate_verdict ... ok
skipping JSON attachment write: pdftotext is required
test ref_library::attach::attach_json_write_mode_keeps_search_attachment_stdout_parseable ... ok
skipping invalid store destination collision: pdftotext is required
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_catalog_is_invalid ... ok
skipping wrong-PDF store destination collision: pdftotext is required
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_store_has_wrong_pdf ... ok
skipping named reference without saved source: pdftotext is required
skipping claimed store destination collision: pdftotext is required
test ref_library::attach::attach_named_reference_without_search_reports_no_saved_source ... ok
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_store_is_claimed ... ok
skipping saved store referenced by another note: pdftotext is required
test ref_library::attach::attach_rejects_a_saved_store_claimed_by_another_note ... ok
skipping attach eligibility skips: pdftotext is required
test ref_library::attach::attach_reports_already_attached_and_snapshot_rows ... ok
skipping saved source with wrong PDF path: pdftotext is required
skipping unverified saved source fallback: pdftotext is required
skipping attach low-match skip: pdftotext is required
test ref_library::attach::attach_saved_source_with_wrong_pdf_path_falls_back_to_search ... ok
test ref_library::attach::attach_unverified_saved_source_reports_failure_then_uses_search ... ok
test ref_library::attach::attach_skips_an_edited_candidate_below_threshold ... ok
test ref_library::attach::attach_keeps_missing_search_path_as_a_usage_error ... ok
skipping attach zero-pass ambiguous stem: pdftotext is required
test ref_library::attach::attach_skips_ambiguous_stem_when_none_verify ... ok
skipping attach verifies a fixture source: pdftotext is required
skipping attach ambiguous skip: pdftotext is required
test ref_library::attach::attach_verifies_and_records_a_fixture_source ... ok
test ref_library::attach::attach_skips_ambiguous_and_title_mismatch_candidates ... ok
skipping search-free run without orphan stores: pdftotext is required
test ref_library::attach::attach_without_refs_and_search_stays_silent_without_orphans ... ok
test ref_library::code::code_human_output_groups_sections_and_hints_shortest_ref ... ok
test ready::overview_human_always_advertises_task_card_keys ... ok
test ref_library::code::code_raw_bytes_match_exact_block_text ... ok
test ref_library::code::code_fenced_uses_longer_fence_for_backtick_runs ... ok
test ref_library::code::code_json_golden_pins_envelope_and_block_fields ... ok
test ref_library::code::code_source_prints_exact_bytes_and_rejects_combinations ... ok
test pomodoro::pomodoro_stale_cutoff_is_empty_unless_requested ... ok
test ref_library::code::code_summaries_skip_noise_and_read_mermaid_frontmatter ... ok
test ref_library::code::code_page_filter_keeps_spanning_blocks ... ok
test ready::worklist_rejects_ambiguous_unknown_and_untyped_notes ... ok
test ref_library::find::find_family_plus_unrelated_duplicate_still_warns ... ok
test ready::worklist_resolves_paths_stems_and_case ... ok
test ref_library::find::find_doi_and_arxiv_doi_queries ... ok
test ref_library::find::find_go_link_keys_stay_opaque ... ok
test ref_library::find::find_batch_from_stdin_keeps_order_and_duplicates ... ok
test ref_library::find::find_human_blocks_carry_chips_and_footnotes ... ok
test ref_library::code::code_non_json_exits_cover_statuses_and_errors ... ok
test ref_library::find::find_conflict_and_unknown_states ... ok
test ref_library::find::find_intake_unavailable_without_intake_dir ... ok
test ref_library::find::find_intake_list_marker_indexes_each_url ... ok
test ref_library::find::find_markdown_table_and_coverage_line ... ok
test ref_library::find::find_intake_hit_with_marker_pdf ... ok
test ref_library::find::find_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::code::code_all_six_statuses_in_json ... ok
test ref_library::find::find_missing_ref_dir_fails_in_both_formats ... ok
test ref_library::find::find_intake_records_both_marker_url_fields ... ok
test ref_library::find::find_natural_versioned_stem_forms_no_family ... ok
test ref_library::find::find_medium_twins_are_one_identity ... ok
test ref_library::find::find_path_source_pdf_stem_and_id_queries ... ok
test ref_library::find::find_not_found_still_exits_zero ... ok
test ref_library::find::find_pending_sync_marks_status_with_footnote ... ok
test ref_library::find::find_rows_carry_blocked ... ok
test ref_library::find::find_ranks_the_newest_reading_first_with_reason_aware_also ... ok
test ref_library::links::links_json_golden_pins_envelope_and_computed_fields ... ok
test ref_library::links::links_human_output_groups_sections_and_hints_shortest_ref ... ok
test ref_library::find::find_title_exact_and_title_candidates ... ok
test ref_library::find::find_url_variants_share_one_identity ... ok
test ref_library::find::find_alias_matches_canonical ... ok
test ref_library::find::find_min_score_filters_title_candidates ... ok
test ref_library::links::links_raw_bytes_match_exact_url_without_newline ... ok
test ref_library::links::links_markdown_n_and_list_with_escaping ... ok
test ref_library::list::list_family_json_carries_reading_and_earlier ... ok
test ref_library::find::find_json_envelope_is_stable_and_honest ... ok
test ref_library::links::links_page_filter_keeps_exact_page ... ok
test ref_library::list::list_family_rows_wear_reading_chips ... ok
test ref_library::find::find_www_and_slash_variants_with_superseded_secondary ... ok
test ref_library::find::find_slug_fallback_for_url_miss ... ok
test ref_library::list::list_git_dates_without_git_warns_and_continues ... ok
test note_walkers::bob_dir_saved_sources_are_ignored_by_note_walkers ... ok
test ref_library::list::list_empty_views_say_so ... ok
test ref_library::find::find_leaves_the_vault_untouched ... ok
test ref_library::list::list_git_births_follow_renames_for_v1_and_v2_rows ... ok
test ref_library::list::list_human_rows_align_dated_and_undated_columns ... ok
test ref_library::list::list_git_dates_backfills_modern_notes_only ... ok
test ref_library::links::links_all_seven_statuses_in_json ... ok
test ref_library::list::list_json_always_exposes_added_at_without_git_dates ... ok
test ref_library::list::list_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::list::list_missing_ref_dir_fails_like_find ... ok
test ref_library::list::list_markdown_covers_dropped_rows ... ok
test ref_library::links::links_non_json_exits_cover_statuses_and_errors ... ok
test ref_library::list::list_default_view_is_the_queue_in_every_format ... ok
test ref_library::list::list_hides_superseded_notes_everywhere ... ok
test ref_library::list::list_legacy_collapse_versus_status_filter ... ok
test ref_library::list::list_rows_carry_always_present_blocked ... ok
test ref_library::migrate_tasks::help_lists_options_alphabetically ... ok
test ref_library::list::list_orders_states_era_status_dates_and_titles ... ok
test ref_library::migrate_tasks::ambiguous_bare_stem_left_unchanged ... ok
test ref_library::list::list_since_filters_by_row_date ... ok
test ref_library::list::list_limit_all_and_truncation ... ok
test ref_library::migrate_tasks::closed_and_legacy_notes_unchanged ... ok
test ref_library::migrate_tasks::crash_adoption_writes_embed_without_second_task ... ok
test ref_library::migrate_zorg::book_folds_lid_and_book_tied_chapters ... ok
test ref_library::list::list_unknown_and_conflict_states ... ok
test ref_library::migrate_zorg::book_without_chapters_stays_unknown_and_strays_skip ... ok
test ref_library::migrate_zorg::dry_run_plans_one_plain_record ... ok
test ref_library::migrate_tasks::depends_on_and_pomodoro_links_rewritten ... ok
test ref_library::migrate_zorg::invariant_note_chapter_skipped_equals_doctor_count ... ok
test ref_library::migrate_zorg::shared_block_pair_stays_distinct_under_provenance ... ok
test ref_library::migrate_zorg::stem_collisions_rename_against_vault_and_same_run ... ok
test ref_library::migrate_tasks::marks_preserve_fields_and_links ... ok
test ref_library::migrate_zorg::multi_url_and_unusable_url_records ... ok
test ref_library::migrate_tasks::tsv_round_trip_with_comments_and_extra_columns ... ok
test ref_library::list::list_leaves_the_vault_untouched ... ok
test ref_library::migrate_tasks::json_modes_and_commit_subject ... ok
test ref_library::migrate_zorg::write_refuses_non_git_vault ... ok
test ref_library::migrate_zorg::write_blocked_hub_dir_fails_clean_with_nothing_committed ... ok
test ref_library::migrate_zorg::write_refuses_dirty_zorg_with_nothing_written ... ok
test ref_library::list::list_filters_or_within_and_across_options ... ok
test ref_library::migrate_tasks::second_write_is_noop_and_non_git_fails ... ok
test ref_library::list::list_rows_carry_task_facts_blocked_by_and_human_reason ... ok
test ref_library::migrate_tasks::wrong_vault_refuses_before_syncing_or_migrating ... ok
test ref_library::migrate_zorg::write_revert_restores_tree_and_doctor_count ... ok
test ref_library::migrate_zorg::write_offline_writes_notes_and_commits_only_zorg ... ok
test ref_library::recatalog::recatalog_uses_snapshot_reader_for_snapshot_sources ... ok
test ref_library::rename::bundle_dry_run_includes_companions_done_daily_and_ambiguous_bare_links ... ok
test ref_library::migrate_tasks::unmapped_refuses_write_and_map_wins ... ok
test ref_library::migrate_zorg::wrong_vault_refuses_before_syncing_or_migrating ... ok
test ref_library::rename::dotted_stem_dry_run_preserves_the_full_stem ... ok
test ref_library::rename::gist_dry_run_reports_moves_links_and_id_rekey_without_writing ... ok
test ref_library::ref_doctor_and_scan_dry_run_match_aliases_on_fixture_vault ... ok
test ref_library::rename::annotated_same_stem_repair_succeeds_and_full_rename_still_refuses ... ok
test ref_library::recatalog::recatalog_dry_run_then_commits_only_additive_link_records ... ok
test ref_library::rename::colliding_reference_ids_receive_the_first_available_suffix ... ok
test ref_library::rename::rename_help_lists_options_alphabetically_with_short_aliases ... ok
test ref_library::rename::idless_reference_rename_keeps_idless_state_and_pdf_bytes ... ok
test ref_library::ref_error_paths_match_aliases_for_every_verb ... ok
test ref_library::ref_help_matches_aliases_for_every_verb ... ok
test ref_library::rename::family_member_rename_rewrites_later_reading_earlier_link ... ok
test ref_library::show::show_collapses_an_all_one_family_hit_set_to_the_newest ... ok
test ref_library::show::show_comments_only_without_comments_reports_empty ... ok
test ref_library::show::show_counts_preamble_blocks_as_excluded ... ok
test ref_library::show::show_dangling_middle_reading_keeps_numbers_and_warns ... ok
test ref_library::show::show_ambiguous_stem_never_picks_first ... ok
test ref_library::show::show_excludes_color_grouped_mirror_with_counts ... ok
test ref_library::rename::resolver_scope_name_collision_and_highlight_refusals_are_structured ... ok
test ref_library::show::show_family_json_carries_reading_earlier_and_later ... ok
test ref_library::migrate_zorg::write_sync_sandwich_merges_peer_and_pushes_scoped_commit ... ok
test ref_library::rename::same_stem_repair_updates_only_id_and_is_idempotent ... ok
test ref_library::rename::offline_write_verifies_identity_sync_and_already_renamed_reruns ... ok
test ref_library::rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test ref_library::show::show_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::rename::other_vault_preview_and_offline_rename_remain_available ... ok
test ref_library::show::show_excludes_mirrors_with_counts ... ok
test ref_library::show::show_missing_ref_dir_fails ... ok
test ref_library::rename::offline_write_moves_companions_and_refuses_dirty_or_stale_inputs ... ok
test ref_library::show::show_comments_only_and_no_annotations ... ok
test ref_library::show::show_natural_versioned_stem_has_no_chips_or_lineage ... ok
test ref_library::show::show_legacy_note_reports_absent_annotations ... ok
test ref_library::rename::listen_link_not_in_sync_dirty_and_live_mode_refusals ... ok
test ref_library::show::show_keeps_quotes_comments_images_and_tombstone_counts ... ok
test ref_library::show::show_resolves_id_doi_arxiv_and_source_pdf ... ok
test ref_library::show::show_resolves_before_printing_anything ... ok
test ref_library::show::show_resolves_every_exact_kind ... ok
test ref_library::show::show_unparsed_region_reports_raw ... ok
test ref_library::show::show_root_names_later_readings_and_wears_v1 ... ok
test ref_library::tasks::copied_reading_tasks_name_the_frontmatter_parent_in_diagnostics ... ok
test ref_library::show::show_markdown_digest_covers_research_and_sections ... ok
test ref_library::show::show_rows_carry_blocked ... ok
test ref_library::show::show_miss_suggests_title_hints ... ok
test ref_library::tasks::list_rows_carry_task_parent_status_and_diagnostics ... ok
test ref_library::tasks::git_dates_never_backfills_v2_finished ... ok
test ref_library::show::show_tasks_own_notes_and_multiline_comments ... ok
test ref_library::tasks::list_parent_resolution_matches_routes_aliases_and_literals ... ok
test ref_library::today::completed_pomodoro_ref_is_closed ... ok
test ref_library::show::show_separates_several_refs_in_order ... ok
test ref_library::today::help_lists_today_and_selectors ... ok
test ref_library::today::default_with_q_is_already_current ... ok
test ref_library::today::default_without_q_links_the_running_entry ... ok
test ref_library::tasks::doctor_reports_ref_tasks_and_parents_rows ... ok
test ref_library::show::show_superseded_url_picks_the_live_note_with_also ... ok
test ref_library::today::exact_name_creates_when_only_prefix_matches ... ok
test ref_library::today::exact_name_reuses_whole_slug ... ok
test ref_library::today::dry_run_capture_object_matches_write_apart_from_dry_run ... ok
test ref_library::today::moving_q_creates_the_named_destination ... ok
test ref_library::today::moving_to_duplicate_unnamed_entry_reports_its_post_move_line ... ok
test ref_library::tasks::show_human_and_json_carry_reading_tasks ... ok
test ref_library::show::show_sections_json_human_markdown_and_flags ... ok
test ref_library::today::named_prefix_selects_bugs ... ok
test ref_library::today::listing_flags_and_human_open_pomodoros ... ok
test ref_library::today::own_depends_on_is_dropped_and_linked ... ok
test ref_library::today::pomodoro_ref_targets_an_unnamed_entry ... ok
test ref_library::today::project_blocked_reading_task_is_link_guard ... ok
test ref_library::today::stale_pomodoro_ref_writes_nothing ... ok
test ref_library::today::today_listing_marks_the_task_theme_suggestion ... ok
test ref_library::today::next_and_in_progress_keep_their_lanes ... ok
test ref_library::today::ready_becomes_next_with_fresh_stamp ... ok
test ref_library::today::scheduled_blocked_task_is_pulled_forward ... ok
test ref_library::show::show_is_read_only ... ok
test ref_library::today::unnamed_rows_carry_derived_homes_and_label ... ok
test relations::relations_help_is_in_tasks_and_projects_and_lists_options ... ok
test relations::relations_list_warns_once_for_invalid_cancel_config ... ok
test relations::relations_lists_catalog_counts_on_scratch_vault ... ok
test relations::relations_list_marks_cancel_labels_and_overlays_zero_use_configured ... ok
test relations::relations_hide_refuses_unknown_and_invalid_labels ... ok
test relations::relations_hide_unhide_round_trip_folds_across_hosts ... ok
test relations_rename::relations_rename_refuses_malformed_matching_lines ... ok
test relations_rename::relations_rename_applies_case_only_and_requires_merge_for_existing_key ... ok
test relations_rename::relations_list_reports_a_label_used_again_after_rename ... ok
test relations::relations_concurrent_hides_both_survive ... ok
test ref_library::today::ledger_and_resolution_refusals ... ok
test relations_rename::relations_rename_into_and_out_of_cancel_labels_warns_and_never_cancels ... ok
test relations_rename::relations_rename_previews_rewrites_every_scope_and_reverts_as_one_commit ... ok
test relations_reverse::reverse_crlf_and_no_final_newline_preserved ... ok
test relations_rename::relations_rename_into_and_out_of_complete_labels_warns_without_completing ... ok
test ref_library::today::refusals_cover_task_and_ledger_codes ... ok
test relations_reverse::reverse_help_orders_flag_and_completion_inherits_it ... ok

thread 'ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme' (235071) panicked at tests/cli/ref_library/today.rs:269:5:
---
type: "[[area]]"
title: Sase
---
# Sase

## Tasks

- [*] #task #ref [[ref/papers/attention]] [type:: BUGS] [fresh:: 2026-10-16] ^ref-attention

test ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme ... FAILED
test relations_reverse::reverse_migration_fixture_matches_approved_counts ... ok
test relations_reverse::reverse_previous_daily_moves_with_existing_ids ... ok
test run_env::clicolor_force_emits_ansi_on_piped_stdout ... ok
test run_env::bob_progress_emits_a_line_on_piped_stderr ... ok
test run_env::clicolor_force_zero_emits_no_ansi_on_piped_stdout ... ok
test relations_rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test relations_reverse::reverse_never_closes_and_reports_stay_open ... ok
test relations_reverse::reverse_refuses_unresolved_ambiguous_and_self_targets ... ok
test run_env::no_color_wins_over_clicolor_force ... ok
test stats::help_names_docs_and_exit_codes ... ok
test run_env::unwritable_run_receipt_warns_and_keeps_the_exit_code ... ok
test stats::invalid_range_is_exit_two ... ok
test relations_reverse::reverse_with_mirrors_disabled_writes_no_mirrors_but_still_mints ... ok
test stats::missing_vault_is_exit_one ... ok
test stats::completion_includes_worked ... ok
test relations_reverse::reverse_merge_and_conflict_and_same_key ... ok
test stats::real_vault_parity_is_opt_in ... ok
test run_env::run_receipt_records_success_usage_and_failure ... ok
test relations_reverse::reverse_same_note_and_cross_note_moves ... ok
test stats::unknown_metric_is_exit_two_json_envelope ... ok
test support::note_profile_package_skip_tests::note_profile_package_skip_reports_missing_packages ... ok
test support::tempdir_drop_does_not_chmod_symlink_target ... ok
test support::tempdir_drop_removes_write_locked_tree ... ok
test stats::metrics_json_omits_points ... ok
test relations_reverse::reverse_mints_writable_sources_and_refuses_archived_ones ... ok
test relations_reverse::reverse_dry_run_writes_nothing_and_apply_reverts_as_one_commit ... ok
test stats::metrics_catalog_lists_worked ... ok
test stats::overview_csv_has_tidy_header ... ok
test stats::show_worked_json_includes_compare_points ... ok
test task_move::dry_run_reports_operational_plan_errors_as_json ... ok
test stats::overview_human_names_metrics ... ok
test task_move::help_lists_sorted_options_and_short_aliases ... ok
test task_move::live_zero_budget_refuses_a_held_lock_before_writing ... ok
test stats::overview_json_is_ok_schema_one ... ok
test task_move::dry_run_works_while_lock_is_held_and_writes_no_state_or_notes ... ok
test stats::show_all_json_lists_visible_metrics ... ok
test relations_reverse::reverse_reconcile_is_noop_after_apply ... ok
test task_move::identity_refusals_write_nothing ... ok
test task_status_hooks::blocked::reconcile_cascades_to_child_projects ... ok
test task_move::git_dry_run_changes_no_notes_or_git_state ... ok
test projects::schedule::projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test task_status_hooks::blocked::reconcile_derives_project_schedule_blocking ... ok
test task_move::pre_sync_failure_does_not_write_move_data ... ok
test task_status_hooks::blocked::reconcile_does_not_promote_same_note_ids_through_resident_edges ... ok
test task_status_hooks::blocked::reconcile_filters_project_internal_ids_by_id_field_only ... ok
test task_status_hooks::blocked::reconcile_does_not_warn_for_an_unfielded_internal_child_link ... ok
test task_status_hooks::blocked::reconcile_ignores_canonical_daily_note_projects ... ok
test task_status_hooks::blocked::reconcile_ignores_notes_with_two_open_prj_lines ... ok
test task_status_hooks::blocked::reconcile_ignores_terminal_projects ... ok
test task_status_hooks::blocked::reconcile_ignores_two_scheduled_prj_tasks ... ok
test projects::schedule::project_schedule_tasks_flip_between_dash_and_blocked_queries_when_due ... ok
test task_status_hooks::blocked::reconcile_keeps_field_only_internal_prj_ids_unprojected ... ok
test task_status_hooks::blocked::reconcile_keeps_prj_internal_links_unprojected ... ok
test task_status_hooks::blocked::reconcile_raises_directly_linked_prj ... ok
test task_status_hooks::blocked::reconcile_treats_uppercase_prj_anchor_as_an_ordinary_task ... ok
test task_status_hooks::blocked::reconcile_warns_inherited_resident_cycle ... ok
test task_status_hooks::blocked::task_status_hooks_blocked_status_guard_writes_nothing ... ok
test task_move::mixed_selectors_dedup_and_keep_source_order ... ok
test task_move::ordinary_commit_failure_keeps_the_write_without_post_sync ... ok
test task_move::non_git_live_move_writes_and_reports_null_git_stages ... ok
test relations::relations_hide_lock_busy_when_maintenance_lock_held ... ok
test task_move::offline_git_move_commits_only_repaired_paths_and_preserves_task_state ... ok
test task_move::post_sync_conflict_keeps_the_local_commit_and_reports_remote_wins ... ok
test task_status_hooks::blocked::reconcile_preserves_crlf_on_tag_rewrite ... ok
test task_status_hooks::blocks::br12_previous_daily_is_never_written_or_listed ... ok
test task_status_hooks::blocked::reconcile_pdf1_databricks_ref_residents ... ok
test task_status_hooks::blocked::reconcile_terminal_project_prerequisite_does_not_block_residents ... ok
test task_move::post_sync_failure_keeps_the_scoped_local_commit_and_reports_failure ... ok
test task_move::pre_sync_uses_the_peer_snapshot_and_commits_pending_local_edits ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test task_status_hooks::blocks::br18_unresolved_self_and_non_task_are_not_listed ... ok
test task_status_hooks::blocks::br17_malformed_dependent_is_kept_not_newly_added ... ok
test task_status_hooks::blocks::br20_internal_prj_target_is_not_listed ... ok
test task_move::co_move_then_reconcile_keeps_canonical_identities ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test task_status_hooks::blocked::task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test task_status_hooks::blocks::br10_closed_owner_is_frozen ... ok
test task_status_hooks::blocked::reconcile_derives_project_blocking_tag_and_unblocked ... ok
test task_status_hooks::blocked::task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test task_status_hooks::blocks::br25_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::blocks::br28_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::blocks::br13_hand_added_entry_without_edge_is_removed ... ok
test task_status_hooks::blocks::br14_canonicalizes_blocking_label ... ok
test task_status_hooks::blocks::br15_deduplicates_and_deletes_orphans ... ok
test task_status_hooks::blocks::br16_malformed_blocks_line_is_left_alone ... ok
test task_status_hooks::blocks::br19_prj_lists_only_the_project_task ... ok
test task_status_hooks::blocks::br1_same_note_insert ... ok
test task_status_hooks::blocks::br21_field_only_dependency_is_adopted_and_listed ... ok
test task_status_hooks::blocks::br22_cycle_each_lists_the_other ... ok
test task_status_hooks::blocks::br23_hide_ref_inbox_and_daily_are_listed ... ok
test task_status_hooks::blocks::br11_reopened_owner_is_reprojected ... ok
test task_status_hooks::blocks::br24_kill_switch_removes_open_lines_and_skips_mints ... ok
test task_status_hooks::blocks::br29_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::blocks::br27_second_run_is_idempotent ... ok
test task_status_hooks::consume::reconcile_keeps_a_link_when_the_block_clears_in_the_same_run ... ok
test task_status_hooks::blocks::br4_mints_idless_dependent_without_id_or_fresh_fields ... ok
test task_status_hooks::blocks::br2_unique_and_ambiguous_basename_links ... ok
test task_status_hooks::blocks::br3_one_line_sorted_across_notes ... ok
test task_status_hooks::blocks::br5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::blocks::br6_inserts_after_depends_on_subtree ... ok
test task_status_hooks::blocks::br7_inserts_second_after_cancel_log ... ok
test task_status_hooks::blocks::br8_prj_order_then_projects_sync_is_noop ... ok
test task_status_hooks::consume::consumption_promoted_daily_note_prerequisite_may_clear_next_run ... ok
test task_status_hooks::consume::reconcile_deletes_a_pomodoro_emptied_by_blocked_consumption ... ok
test task_status_hooks::blocks::br26_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::consume::reconcile_consumes_blocked_resident_links_and_keeps_the_entry ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw1_inserts_adopted_line_before_schedule_log ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw2_inserts_adopted_line_after_cancel_log ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw3_dw6_rewrite_keeps_link_order ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_with_adoptable_id_deletes_line_and_field ... ok
test task_status_hooks::dependency_line_writes::summary_reports_dependency_counts ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_deletes_line_and_field ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_unresolved_link_and_breadcrumbs ... ok
test task_status_hooks::dependency_lines::reconcile_never_writes_previous_daily_target ... ok
test task_status_hooks::dependency_lines::reconcile_projection_only_write_defers_in_quiet_interval ... ok
test task_status_hooks::dependency_lines::reconcile_adopts_field_ids_into_canonical_line ... ok
test task_status_hooks::dependency_lines::reconcile_canonicalizes_legacy_line_variants ... ok
test task_status_hooks::dependency_lines::reconcile_breadcrumb_heals_when_target_returns ... ok
test task_status_hooks::blocks::br9_last_dependent_close_removes_line ... ok
test task_status_hooks::dependency_lines::reconcile_daily_note_keeps_adoption_and_stamp ... ok
test task_status_hooks::dependency_lines::reconcile_dependency_chain_settles_in_one_run ... ok
test task_status_hooks::dependency_lines::reconcile_warns_dependency_cycle_and_keeps_members_blocked ... ok
test task_status_hooks::dependency_lines::reconcile_drops_stale_field_id ... ok
test task_status_hooks::dependency_lines::reconcile_does_not_read_child_links_as_dependencies ... ok
test task_status_hooks::dependency_lines::reconcile_field_writer_handles_trailing_tags ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_heals_moved_link ... ok
test task_status_hooks::dependency_lines::reconcile_skips_closed_dependents ... ok
test task_status_hooks::relations::configured_cancel_label_stays_inert_during_reconcile ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unadoptable_id_and_keeps_field ... ok
test task_status_hooks::dependency_lines::reconcile_ignores_archive_children_outside_the_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unencodable_target_without_projecting ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test task_status_hooks::relations::lr17_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::relations::lr12_malformed_linked_from_left_alone ... ok
test task_status_hooks::relations::lr14_unresolved_non_task_self_warned_and_omitted ... ok
test task_status_hooks::dependency_lines::reconcile_projects_line_into_field_and_stamps_target_id ... ok
test task_status_hooks::dependency_lines::reconcile_removes_empty_line_and_leaves_malformed_alone ... ok
test task_status_hooks::relations::lr21_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::relations::lr22_archived_source_keeps_done_form ... ok
test task_status_hooks::relations::lr23_duplicate_source_id_not_listed ... ok
test task_status_hooks::dependency_lines::reconcile_same_index_insert_does_not_clobber_replace ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test task_status_hooks::dependency_lines::reconcile_warns_non_task_and_self_links_without_projecting ... ok
test task_status_hooks::dependency_lines::reconcile_stamps_cross_note_target_id ... ok
test task_status_hooks::relations::lr10_noncanonical_line_is_canonicalized ... ok
test task_status_hooks::relations::lr13_malformed_links_never_newly_added ... ok
test task_status_hooks::relations::lr15_duplicate_linked_from_lines_deduplicated ... ok
test task_status_hooks::relations::lr19_symmetric_edges ... ok
test task_status_hooks::relations::lr7_done_and_previous_daily_targets_never_written ... ok
test task_status_hooks::relations::lr20_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::relations::lr_human_output_includes_knot_group ... ok
test task_status_hooks::relations::lr1_same_note_insert ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_terminal_failure_and_exit_status ... ok
test task_status_hooks::retry::task_status_hooks_defers_when_maintenance_lock_is_held ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_creates_no_lock_or_recovery ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_ignores_retry_timeout ... ok
test task_status_hooks::relations::lr24_prj_target_gets_the_mirror ... ok
test task_status_hooks::relations::lr2_labelled_edge ... ok
test task_status_hooks::retry::task_status_hooks_live_noop_may_lock_but_creates_no_recovery ... ok
test task_status_hooks::retry::task_status_hooks_rejects_invalid_retry_timeout ... ok
test task_status_hooks::structure::task_status_hooks_composes_daily_status_and_structural_edits ... ok
test task_status_hooks::structure::task_status_hooks_drops_carried_link_already_in_completed_fallback ... ok
test task_status_hooks::retry::task_status_hooks_exhausts_retry_budget_and_still_fails ... ok
test task_status_hooks::structure::task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks::structure::task_status_hooks_keeps_archive_out_of_active_dependency_sync ... ok
test task_status_hooks::retry::task_status_hooks_human_retry_progress_goes_to_stdout ... ok
test task_status_hooks::structure::task_status_hooks_normalizes_live_archive_terminal_references ... ok
test task_status_hooks::structure::task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test task_status_hooks::structure::task_status_hooks_removes_empty_pomodoros_and_reports_them ... ok
test task_status_hooks::relations::lr3_sorted_sources_include_done ... ok
test task_status_hooks::structure::task_status_hooks_resolves_archive_references_read_only ... ok
test task_status_hooks::relations::lr4_mints_source_id ... ok
test task_status_hooks::subprojects::descendant_project_targets_stay_unprojected_and_warn ... ok
test task_status_hooks::subprojects::blocked_subproject_links_are_consumed_and_promote_ancestor_prerequisites ... ok
test task_status_hooks::structure::task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test task_status_hooks::relations::lr6_closed_target_still_mirrored ... ok
test task_status_hooks::subprojects::projects_sync_ignores_cascade_tags_and_keeps_marker_state ... ok
test task_status_hooks::subprojects::project_parent_cycles_warn_once_and_only_inherit_other_projects_reasons ... ok
test task_status_hooks::subprojects::inherited_edges_participate_in_r7_cycle_detection ... ok
test task_status_hooks::relations::lr5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::structure::task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test task_status_hooks::sync::task_status_hooks_nulls_plan_budget_on_invalid_config ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_retry_and_final_result ... ok
test task_status_hooks::relations::lr11_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::subprojects::reconcile_cascades_reasons_and_tags_through_multiple_project_levels ... ok
test task_status_hooks::subprojects::reconciled_cascade_tree_has_no_second_run_changes ... ok
test task_status_hooks::relations::lr16_kill_switch_removes_writable_lines_and_skips_mints ... ok
test task_status_hooks::subprojects::reconcile_recovers_subprojects_and_keeps_nearest_remaining_reason ... ok
test task_status_hooks::sync::task_status_hooks_reports_grouping_warnings_without_noop_text ... ok
test task_status_hooks::relations::lr8_done_and_previous_daily_sources_are_listed ... ok
test task_status_hooks::retry::task_status_hooks_json_retry_progress_stays_off_stdout ... ok
test task_status_hooks::sync::reconcile_status_only_flips_skip_quiet_period_but_structural_edits_wait ... ok
test task_status_hooks::sync::task_status_hooks_reports_plan_budget_in_json_and_human ... ok
test task_status_hooks::relations::lr9_hand_added_and_deleted_entries ... ok
test themes::themes_bare_is_list ... ok
test themes::themes_alias_matches_types_for_list_and_bare_group ... ok
test themes::themes_default_cache_discovers_additions_through_a_vault_symlink ... ok
test themes::themes_default_cache_rechecks_same_size_edits_and_root_area_colors ... ok
test themes::themes_fresh_and_cached_json_agree ... ok
test themes::themes_default_cache_rebuilds_on_corruption_fresh_and_new_vaults ... ok
test themes::themes_hidden_filter_reads_journal ... ok
test themes::themes_help_is_in_daily_workflow_and_lists_options ... ok
test themes::themes_json_schema_and_query_ranks_fix_before_fixes ... ok
test task_status_hooks::sync::task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test themes::themes_list_does_not_invent_off_or_whitespace_unknown_hints ... ok
test themes::themes_concurrent_hides_both_survive ... ok
test themes::themes_list_emits_collision_hints ... ok
test themes::themes_hide_unhide_color_round_trip_folds_two_hosts ... ok
test themes::themes_lists_expected_hues_on_scratch_vault ... ok
test themes::themes_default_hints_track_edits_additions_deletions_types_and_knownness ... ok
test themes::themes_list_emits_not_configured_hints ... ok
test themes::themes_suggest_refuses_symlink_escape_and_tolerates_closed_stdout ... ok
test themes::themes_suggest_null_inheritance_repair_hidden_and_invalid_default_warnings ... ok
test themes::themes_default_cache_refreshes_large_vaults_and_propagates_read_errors ... ok
test themes::themes_write_refusals_are_json_on_nonzero_exit ... ok
test task_status_hooks::sync::task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test themes::themes_unknown_defaults_are_vault_wide_sorted_and_do_not_write ... ok
test themes::themes_suggest_explains_overrides_inheritance_and_new_tasks_without_writes ... ok
test themes::themes_suggest_reuses_capture_lookup_errors_and_rejects_unsafe_targets ... ok
test themes_rename::themes_alias_matches_types_for_rename_dry_run ... ok
test themes_rename::themes_rename_dry_run_previews_collapse_and_leaves_vault_untouched ... ok
test themes_rename::themes_rename_leaves_fenced_prose_and_tasks_untouched ... ok
test themes_rename::themes_rename_apply_verifies_commits_and_reappears ... ok
test themes_rename::themes_rename_later_hide_does_not_clear_reappearance ... ok
test themes_rename::themes_rename_later_color_or_unhide_clears_reappearance ... ok
test themes_rename::themes_rename_cycle_does_not_report_reappearance ... ok
test themes_rename::themes_rename_later_unhide_clears_reappearance ... ok
test themes_rename::themes_rename_merge_rewrites_task_fields_to_new ... ok
test themes_rename::themes_rename_preserves_trailing_whitespace_and_mixed_endings_offline ... ok
test themes_rename::themes_rename_refuses_reading_theme ... ok
test themes_rename::themes_rename_refuses_configured_old_and_warns_unconfigured_new ... ok
test themes_rename::themes_rename_refusals_are_json_on_nonzero_exit ... ok
test themes_split::themes_split_dry_run_reports_flags_and_leaves_vault_untouched ... ok
test themes_rename::themes_rename_rewrites_defaults_and_task_fields ... ok
test themes_split::themes_split_preserves_trailing_whitespace_and_mixed_endings_offline ... ok
test themes_split::themes_split_stdin_map_works ... ok
test themes_split::themes_split_template_lists_old_entries_and_round_trips_as_keep ... ok
test themes_rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test vault_sync::conflict_directory_is_skipped_by_vault_walkers ... ok
test themes_split::themes_split_write_commits_without_journal_and_invalidates_cache ... ok
test themes_split::themes_split_refusals_are_json_on_nonzero_exit ... ok
test themes_split::themes_split_warns_and_leaves_defaults_and_task_fields ... ok
test themes_split::wrong_vault_refuses_before_syncing_or_splitting ... ok
test vault_sync::renamed_old_top_level_commands_are_unknown ... ok
test vault_sync::executable_stubs_stay_executable_while_other_threads_fork ... ok
test vault_sync::nightly_articles_step_reports_without_writing_and_still_passes ... ok
test vault_sync::nightly_failed_step_still_runs_later_steps_and_exits_nonzero ... ok
test task_status_hooks::structure::task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test vault_sync::nightly_runs_vault_sync_move_done_tasks_vault_sync_in_order ... ok
test vault_sync::vault_sync_concurrent_invocation_exits_zero_silently ... ok
test vault_sync::vault_sync_both_added_file_quarantines_local_copy ... ok
test task_status_hooks::relations::lr18_inert_statuses_and_fields ... ok
test task_status_hooks::sync::task_status_hooks_un_decorates_legacy_groups_holding_only_ready ... ok
test vault_sync::vault_sync_binary_conflict_quarantines_uncorrupted_local_copy ... ok
test task_status_hooks::sync::task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test task_status_hooks::sync::task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test vault_sync::vault_sync_dry_run_reports_clobber_without_writing ... ok
test vault_sync::vault_sync_detects_clobber_when_shared_ids_sort_last ... ok
test vault_sync::vault_sync_local_only_change_commits_and_pushes ... ok
test vault_sync::vault_sync_no_change_cycle_writes_status_without_committing ... ok
test vault_sync::vault_sync_ignores_legitimate_rewrites ... ok
test vault_sync::vault_sync_delete_modify_conflict_keeps_the_file ... ok
test vault_sync::vault_sync_completes_fast_forward_left_by_head_lock ... ok
test vault_sync::vault_sync_refuses_95_mib_file_before_staging ... ok
test vault_sync::vault_sync_non_overlapping_edits_merge_cleanly ... ok
test vault_sync::vault_sync_conflict_copy_on_ignored_path_still_commits_merge ... ok
test vault_sync::vault_sync_remote_only_change_fast_forwards ... ok
test themes::themes_hide_lock_busy_when_maintenance_lock_held ... ok
test vault_sync::vault_sync_quarantines_incident_shaped_clobber ... ok
test vault_sync::vault_sync_quarantine_with_ignored_conflicts_dir_commits_and_pushes ... ok
test vault_sync::vault_sync_recovers_interrupted_merge_and_finishes_cycle ... ok
test vault_sync::vault_sync_push_race_retries_and_succeeds ... ok
test vault_sync::vault_sync_halts_on_repeated_interrupted_merge_of_same_remote ... ok
test vault_sync::vault_sync_same_line_edit_quarantines_local_copy_and_keeps_remote ... ok
test themes_rename::themes_rename_lock_busy_when_maintenance_lock_held ... ok
test vault_sync::vault_sync_retries_fast_forward_blocked_by_head_lock ... ok
test task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses ... ok
test highlights::ingest::create_queues_when_locks_or_pre_sync_prevent_inline_intake has been running for over 60 seconds
test highlights::ingest::create_queues_when_locks_or_pre_sync_prevent_inline_intake ... ok
test highlights::scan_intake::intake_status_records_create_outcomes_and_keeps_the_other_field has been running for over 60 seconds
test highlights::scan_intake::intake_status_records_create_outcomes_and_keeps_the_other_field ... ok

failures:

failures:
    capture::plan_budget::capture_plan_budget_human_reports_meter_and_destination
    capture::plan_budget::capture_plan_budget_warns_when_new_theme_grows_past_cap
    capture::plan_budget::capture_strict_mode_refuses_new_theme_past_cap_atomically
    capture::pomodoro_close_selection::capture_pomodoro_close_selection_human_output
    capture::task_complete::exact_human_output_for_strike_move_dedupe_and_done
    capture::task_theme_writes::a_two_item_batch_stages_and_reports_both_task_theme_writes
    capture::task_theme_writes::active_existing_task_link_start_shorthand_uses_the_resolved_name
    capture::task_theme_writes::ensure_next_named_relocation_sets_a_theme_after_freshness_edits
    capture::task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception
    catalog::protocol_1_parses_with_schema_version_one
    plan::plan_reports_human_budget_without_ansi_when_piped
    ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme

test result: FAILED. 2430 passed; 12 failed; 0 ignored; 0 measured; 0 filtered out; finished in 107.26s

error: test failed, to rerun pass `--test cli`
failed  exit=101  duration=312033ms

