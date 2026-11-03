# Chat History - ace-run (17p.f0--mon)

- **TIMESTAMP:** 2026-11-03 16:05:53 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 17p.f0--mon

## Prompt

sase monitor start --command 'set -eu\ncargo check --all-targets --locked\ncargo fmt --all -- --check\ncargo test --lib native::capture\ninstall_root="$(mktemp -d)"\nRUSTC_WRAPPER= cargo install --path . --locked --profile local-install --root "$install_root"\n"$install_root/bin/bob" --help' --reason 'Run the approved restore_note_pull_initializer verification'

## Response

sase tool run 36db0edcb9e33654216beaf06ef2a2bc
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1m 06s
   Compiling typenum v1.20.1
   Compiling cfg-if v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling foldhash v0.2.0
   Compiling memchr v2.8.1
   Compiling litemap v0.8.3
   Compiling writeable v0.6.4
   Compiling utf8_iter v1.0.4
   Compiling simd-adler32 v0.3.9
   Compiling bitflags v2.12.1
   Compiling smallvec v1.15.2
   Compiling utf8parse v0.2.2
   Compiling adler2 v2.0.1
   Compiling rand_core v0.10.1
   Compiling anstyle-query v1.1.5
   Compiling cpufeatures v0.3.0
   Compiling tinyvec_macros v0.1.1
   Compiling colorchoice v1.0.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling anstyle v1.0.14
   Compiling cpufeatures v0.2.17
   Compiling siphasher v1.0.4
   Compiling strsim v0.11.1
   Compiling clap_lex v1.1.0
   Compiling weezl v0.1.12
   Compiling itoa v1.0.18
   Compiling quick-error v2.0.1
   Compiling zune-core v0.5.3
   Compiling regex-syntax v0.8.10
   Compiling unicode-properties v0.1.4
   Compiling iana-time-zone v0.1.65
   Compiling const-oid v0.10.2
   Compiling time-core v0.1.9
   Compiling bytecount v0.6.9
   Compiling percent-encoding v2.3.2
   Compiling pxfm v0.1.30
   Compiling deranged v0.5.8
   Compiling num-conv v0.2.2
   Compiling powerfmt v0.2.0
   Compiling unicode-bidi v0.3.18
   Compiling byteorder-lite v0.1.0
   Compiling linux-raw-sys v0.12.1
   Compiling color_quant v1.1.0
   Compiling bytemuck v1.25.2
   Compiling ttf-parser v0.25.1
   Compiling libc v0.2.186
   Compiling serde_core v1.0.228
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
   Compiling zmij v1.0.21
   Compiling once_cell v1.21.4
   Compiling is_executable v1.0.6
   Compiling fallible-streaming-iterator v0.1.9
   Compiling base64 v0.22.1
   Compiling fastrand v2.5.0
   Compiling rangemap v1.7.1
   Compiling fallible-iterator v0.3.0
   Compiling num-traits v0.2.19
   Compiling ryu v1.0.23
   Compiling zerofrom v0.1.8
   Compiling thiserror v2.0.18
   Compiling unsafe-libyaml v0.2.11
   Compiling log v0.4.30
   Compiling hex v0.4.3
   Compiling fdeflate v0.3.7
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26/crates/bob-obsidian-assets)
   Compiling similar v2.7.0
   Compiling tinyvec v1.11.0
   Compiling generic-array v0.14.7
   Compiling hybrid-array v0.4.12
   Compiling nom v8.0.0
   Compiling aho-corasick v1.1.4
   Compiling quick-xml v0.41.0
   Compiling cc v1.2.63
   Compiling crc32fast v1.5.0
   Compiling chacha20 v0.10.2
   Compiling encoding_rs v0.8.35
   Compiling miniz_oxide v0.8.9
   Compiling form_urlencoded v1.2.2
   Compiling rustix v1.1.5
   Compiling phf_shared v0.12.1
   Compiling gif v0.14.2
   Compiling anstyle-parse v1.0.0
   Compiling hashbrown v0.17.1
   Compiling zune-jpeg v0.5.15
   Compiling chrono v0.4.44
   Compiling time v0.3.53
   Compiling getrandom v0.4.2
   Compiling fs2 v0.4.3
   Compiling image-webp v0.2.4
   Compiling yoke v0.8.3
   Compiling serde v1.0.228
   Compiling serde_json v1.0.150
   Compiling moxcms v0.8.1
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling unicode-normalization v0.1.25
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling anstream v1.0.0
   Compiling flate2 v1.1.9
   Compiling phf v0.12.1
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
   Compiling rand v0.10.1
   Compiling indexmap v2.14.0
   Compiling hashlink v0.12.1
   Compiling regex-automata v0.4.14
   Compiling stringprep v0.1.5
   Compiling digest v0.11.3
   Compiling clap_builder v4.6.7
   Compiling digest v0.10.7
   Compiling inout v0.1.4
   Compiling chrono-tz v0.10.4
   Compiling png v0.18.1
   Compiling nom_locate v5.0.0
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling plist v1.10.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tempfile v3.27.0
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling sha2 v0.11.0
   Compiling cipher v0.4.4
   Compiling icu_collections v2.3.0
   Compiling icu_locale_core v2.3.0
   Compiling clap v4.6.7
   Compiling cbc v0.1.2
   Compiling aes v0.8.4
   Compiling ecb v0.1.2
   Compiling clap_complete v4.6.11
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling regex v1.12.3
   Compiling icu_provider v2.3.1
   Compiling image v0.25.10
   Compiling lopdf v0.40.0
   Compiling icu_normalizer v2.3.0
   Compiling icu_properties v2.3.0
   Compiling rquickjs v0.12.1
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2m 37s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261103_154512/build/debug/deps/bob_cli-edb465a55cecd3c2)

running 1483 tests
test native::capture::budget::tests::destination_roles_follow_the_contract ... ok
test native::capture::event_conflict::tests::messages_name_the_buffer_the_overlap_sits_in ... ok
test native::capture::dependencies::tests::new_prj_edges_check_implicit_resident_cycles ... ok
test native::capture::keep_moving_net::tests::row_project_falls_back_to_the_row_note ... ok
test native::capture::keep_moving_net::tests::gaps_compare_against_the_nearest_earlier_step ... ok
test native::capture::keep_moving_net::tests::later_effects_are_the_links_added_after_the_group_item ... ok
test native::capture::keep_moving_net::tests::explicit_relinks_count_even_when_the_live_set_is_unchanged ... ok
test native::capture::link_guard::tests::new_task_flip_blocks_open_lines_tags_blocked_and_skips_closed ... ok
test native::capture::meet_event_run::tests::unnamed_start_without_a_meet_keeps_the_first_future ... ok
test native::capture::event_conflict::tests::start_fit_is_largest_count_ending_at_the_event ... ok
test native::capture::event_conflict::tests::more_counts_later_crossings ... ok
test native::capture::meet_event_run::tests::dropped_numbers_keep_pre_image_numbering ... ok
test native::capture::event_conflict::tests::unbuffered_payloads_omit_the_buffer_keys ... ok
test native::capture::event_conflict::tests::untracked_events_warn_and_named_starts_keep_the_hash ... ok
test native::capture::event_conflict::tests::plus_and_shift_fits_and_no_fit_when_the_start_is_the_event ... ok
test native::capture::meet_event_run::tests::far_run_label_adds_the_span_and_buffer_only_when_buffered ... ok
test native::capture::meet_event_run::tests::unnamed_start_skips_ended_and_done_events ... ok
test native::capture::meet_event_run::tests::run_extends_over_touching_events_with_the_same_clock_classification ... ok
test native::capture::meet_event_run::tests::ended_done_cancelled_and_foreign_links_are_skipped ... ok
test native::capture::meet_event_run::tests::finalize_writes_the_calendar_span_and_clamps_late_joins ... ok
test native::capture::event_conflict::tests::meet_sessions_and_own_lineup_and_old_span_are_exempt ... ok
test native::capture::event_conflict::tests::mid_meeting_start_reports_event_in_progress_without_untracked ... ok
test native::capture::event_conflict::tests::buffered_fit_ends_at_the_buffered_start_and_only_before_it ... ok
test native::capture::meet_event_run::tests::untracked_run_breaks_at_a_contiguous_tracked_event ... ok
test native::capture::meet_event_run::tests::unnamed_start_picks_the_earliest_overlapping_meet ... ok
test native::capture::meet_event_run::tests::unnamed_start_picks_meet_when_the_start_block_overlaps_the_run ... ok
test native::capture::meet_event_run::tests::unnamed_start_uses_buffered_lead_in_and_lead_out ... ok
test native::capture::note_pull::tests::np22_unavailable_proof_folds_candidate_blocked ... ok
test native::capture::meet_event_run::tests::buffered_spans_drive_candidates_sort_and_clustering ... ok
test native::capture::output::tests::capture_destination_swatches_respect_no_color ... ok
test native::capture::output::tests::all_unblocked_includes_project_note_successors ... ok
test native::capture::output::tests::complete_effect_omitted_when_none ... ok
test native::capture::output::tests::create_project_note_omits_form_and_successors ... ok
test native::capture::output::tests::log_entry_details_omitted_when_empty ... ok
test native::capture::output::tests::all_unblocked_covers_nested_relation_summaries_in_order ... ok
test native::capture::output::tests::typed_entry_details_print_two_spaces_under_their_entry ... ok
test native::capture::output::tests::relation_completes_omits_already_closed_rows ... ok
test native::capture::output::tests::relation_completes_omitted_when_empty ... ok
test native::capture::output::tests::typed_work_log_details_align_with_entries_when_present ... ok
test native::capture::output::tests::project_created_offer_header_reads_new_project ... ok
test native::capture::output::tests::unblocked_vecs_mut_reaches_nested_rows ... ok
test native::capture::pomodoro_adjust::tests::format_adjusted_range_preserves_missing_duration ... ok
test native::capture::output::tests::typed_work_log_details_omitted_when_no_entry_has_details ... ok
test native::capture::pomodoro_adjust::tests::session_clock_classifies_worked_off_clock_conflict_and_placeholder ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_tab_children_and_interior_blanks ... ok
test native::capture::pomodoro_adjust::tests::set_ledger_clock_moves_the_recorded_duration_between_keys ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_fenced_child_lines_verbatim ... ok
test native::capture::pomodoro_blocks::tests::block_range_stops_at_section_end_and_covers_last_entry ... ok
test native::capture::pomodoro_blocks::tests::block_range_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::depth_continuation_lines_take_parent_depth_plus_one ... ok
test native::capture::pomodoro_blocks::tests::depth_counts_nested_list_items ... ok
test native::capture::pomodoro_blocks::tests::block_range_trims_trailing_blanks_and_stops_at_zero_indent ... ok
test native::capture::pomodoro_blocks::tests::depth_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::pairing_created_block_is_all_added ... ok
test native::capture::pomodoro_blocks::tests::pairing_pure_insert_is_added_and_pure_delete_is_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_replace_becomes_changed_with_before ... ok
test native::capture::pomodoro_blocks::tests::pairing_uneven_replace_splits_changed_added_removed ... ok
test native::capture::batch_move::tests::batch_replacement_order_writes_destinations_before_sources ... ok
test native::capture::pomodoro_blocks::tests::tracker_autodetects_an_unreported_child_insert ... ok
test native::capture::pomodoro_blocks::tests::resolution_rejects_a_non_entry_after - should panic ... ok
test native::capture::pomodoro_blocks::tests::forwarding_panics_when_a_tracked_headline_is_deleted - should panic ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_exactly_at_end ... ok
test native::capture::pomodoro_blocks::tests::tracker_resolves_created_before_and_reports_roles_once ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_mid_session ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_overnight_wrap_is_not_overdue ... ok
test native::capture::pomodoro_blocks::tests::vanished_entry_is_dropped_silently - should panic ... ok
test native::capture::pomodoro_blocks::tests::unreported_headline_rewrite_emits_unchanged_block - should panic ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_start_later_than_now ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_past_the_end ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_unparsable_range ... ok
test native::capture::pomodoro_blocks::tests::tracker_reports_one_cumulative_block_across_items ... ok
test native::capture::pomodoro_blocks::tests::tracker_forwards_a_tracked_block_across_an_insert_above ... ok
test native::capture::project_deps::tests::prj_gate_matches_only_recognised_projects ... ok
test native::capture::project_deps::tests::flatten_block_links_uses_plain_alias_or_target_text ... ok
test native::capture::project_deps::tests::descendant_notes_are_internal_prj_targets ... ok
test native::capture::project_deps::tests::resident_block_flips_tags_and_skips_prj_and_closed ... ok
test native::capture::project_deps::tests::strongest_lane_ignores_closed_and_outsiders ... ok
test native::capture::project_deps::tests::resident_block_edits_idless_rows_and_rechecks_shifted_fences ... ok
test native::capture::project_deps::tests::resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range ... ok
test native::capture::project_deps::tests::kept_notes_text_strips_tags_fields_and_ids ... ok
test native::capture::project_note::tests::create_omits_offer_fields_and_iterator_skips_them ... ok
test native::capture::project_deps::tests::removed_refs_and_consumed_lines_use_the_items_pre_state_coordinates ... ok
test native::capture::project_note::tests::offer_named_without_tasks_is_refused ... ok
test native::capture::blocked_tasks::tests::always_mints_when_blocks_lines_is_off ... ok
test native::capture::inbox_route::tests::ir_snapshot_binding_refuses_when_unstaged_dest_or_repair_changes ... ok
test native::capture::note_pull::tests::np10_empty_refusals_carry_fold_and_write_nothing ... ok
test native::capture::note_pull::tests::np11_scheduled_project_names_date_reason ... ok
test native::capture::note_pull::tests::np12_missing_source_refuses_pull_note_missing ... ok
test native::capture::note_pull::tests::np11_blocked_project_names_prj_reason ... ok
test native::capture::note_pull::tests::batch_later_missing_note_rolls_back_earlier_creation ... ok
test native::capture::link_guard::tests::unblocked_project_resident_skips_the_vault_graph ... ok
test native::capture::dependency_drop::tests::partial_drop_keeps_verbatim_history_and_unresolved_links_and_field_ids ... ok
test native::capture::project_deps::tests::consumption_resolves_alias_basename_path_case_and_local_links_by_identity ... ok
test native::capture::link_guard::tests::tagged_prj_forces_the_vault_graph ... ok
test native::capture::link_guard::tests::tagged_project_resident_forces_the_vault_graph ... ok
test native::capture::inbox_route::tests::ir_route_refusal_blames_the_failing_second_member ... ok
test native::capture::link_guard::tests::tagged_destination_blocks_a_new_task ... ok
test native::capture::inbox_route::tests::ir_nested_status_uses_root_and_idless_tasks_get_stable_keys ... ok
test native::capture::dependency_drop::tests::last_dependency_line_and_field_are_removed_with_crlf_and_final_newline_preserved ... ok
test native::capture::link_guard::tests::capture_into_unblocked_project_skips_the_vault_graph ... ok
test native::capture::relations_mentions::tests::vanished_occurrences_preserve_mirrors_when_postimage_is_uncertain ... ok
test native::capture::link_guard::tests::inherited_reason_blocks_pull_forward ... ok
test native::capture::relation_sources::tests::relation_snapshot_drops_links_notes_without_event_token ... ok
test native::capture::relation_sources::tests::cheap_gate_rejects_without_catalog_or_source_reads ... ok
test native::capture::relation_sources::tests::marker_negative_target_loads_through_planner_and_missing_is_unavailable ... ok
test native::capture::dependency_drop::tests::duplicate_or_malformed_managed_lines_refuse_without_staging ... ok
test native::capture::relation_sources::tests::source_snapshot_uses_shared_parser_resolver_and_narrow_target_reads ... ok
test native::capture::blocked_tasks::tests::nested_dependent_path_is_addressed_by_relative_and_block_id ... ok
test native::capture::note_pull::tests::np8_closed_statuses_ignored_uncounted ... ok
test native::capture::relation_sources::tests::unreadable_links_note_taints_when_event_token_does_not_match ... ok
test native::capture::note_pull::tests::np23_missing_day_uses_existing_error ... ok
test native::capture::tests::assembly::exact_name_literal_never_prefix_matches ... ok
test native::capture::inbox_route::tests::ir_identical_idless_roots_route_together_with_exact_landings ... ok
test native::capture::tests::assembly::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::tests::assembly::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::assembly::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::assembly::completed_multiword_reuse_keeps_spelling ... ok
test native::capture::tests::assembly::exact_name_literal_creates_exact_spelling ... ok
test native::capture::tests::assembly::formats_task_line ... ok
test native::capture::tests::assembly::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembly::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::assembly::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::tests::assembly::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::tests::assembly::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::assembly::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::tests::assembly::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::assembly::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::assembly::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::assembly::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::assembly::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::assembly::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::assembly::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::assembly::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::assembly::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::assembly::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::assembly::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::assembly::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::assembly::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::assembly::sub_bullet_insertion_keeps_dependency_lines_first ... ok
test native::capture::task_blocks::tests::block_range_maps_byte_end_to_line_range ... ok
test native::capture::relation_sources::tests::staged_overlay_adds_edits_and_deletions_and_masks_read_failures ... ok
test native::capture::task_blocks::tests::toggle_plus_subbullet_shows_the_task_line_as_changed ... ok
test native::capture::tests::grammar::clip_directives_claim_edges_and_leave_prose_alone ... ok
test native::capture::tests::commit::refuses_when_absent_target_appears_before_commit ... ok
test native::capture::tests::commit::complete_label_batch_stale_preimage_keeps_external_edit ... ok
test native::capture::tests::commit::keep_moving_pick_batch_stale_preimage_refuses_whole_batch ... ok
test native::capture::dependencies::tests::prefiltered_snapshot_matches_full_read ... ok
test native::capture::tests::commit::refuses_when_second_note_edited_externally ... ok
test native::capture::tests::commit::refuses_when_existing_target_deleted_before_commit ... ok
test native::capture::relation_sources::tests::relation_archive_rules_exclude_done_directories_but_keep_done_md ... ok
test native::capture::relation_sources::tests::either_consumer_order_walks_and_reads_the_catalog_once ... ok
test native::capture::relation_sources::tests::dependency_snapshot_does_not_surface_unconsulted_relation_warning ... ok
test native::capture::tests::grammar::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::relation_sources::tests::parked_only_event_selects_sources_and_loads_its_target ... ok
test native::capture::relation_sources::tests::a_fresh_context_observes_new_disk_edges_without_a_persistent_cache ... ok
test native::capture::tests::grammar::clipboard_notes_parse_as_sub_bullet_without_text ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_schedule_log ... ok
test native::capture::blocked_tasks::tests::relocate_by_id_after_id_stamp_and_lane_promotion ... ok
test native::capture::relation_sources::tests::zero_matching_sources_returns_empty_source_and_dependency_notes ... ok
test native::capture::task_blocks::tests::authored_children_and_schedule_log_are_added_in_order ... ok
test native::capture::link_guard::tests::ordinary_unblocked_target_skips_the_vault_graph ... ok
test native::capture::relation_sources::tests::matched_source_dependency_proof_skips_unrelated_id_notes ... ok
test native::capture::task_blocks::tests::locally_routed_batch_reports_one_block_with_two_added_rows ... ok
test native::capture::tests::grammar::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::grammar::extracts_escaped_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::grammar::extracts_retired_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::grammar::normalizes_whitespace ... ok
test native::capture::tests::grammar::parses_picker_task_refs_strictly ... ok
test native::capture::tests::grammar::parses_priority_tokens ... ok
test native::capture::tests::grammar::parses_retired_priority_tokens ... ok
test native::capture::tests::grammar::parses_schedule_tokens ... ok
test native::capture::tests::grammar::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::grammar::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::grammar::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::grammar::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::grammar::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::grammar::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::grammar::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::grammar::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::grammar::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::grammar::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::grammar::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::placement::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::placement::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::placement::article_exact_raw_title_match_precedes_earlier_identity_match ... ok
test native::capture::tests::placement::article_prefix_prefers_raw_number_in_document_order ... ok
test native::capture::tests::grammar::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::placement::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::placement::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::grammar::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::tests::placement::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::placement::bare_bullet_marker_skips_generated_status_group ... ok
test native::capture::tests::placement::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::grammar::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::placement::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::placement::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::placement::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::tests::placement::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::grammar::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::placement::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::placement::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::placement::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::placement::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::placement::forced_section_does_not_target_generated_blocked_group ... ok
test native::capture::tests::placement::exact_selector_never_slug_matches ... ok
test native::capture::tests::placement::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::placement::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::placement::formats_sub_bullet_line ... ok
test native::capture::tests::placement::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::placement::edge_hash_markers_are_task_types_not_legacy_bullet_selectors ... ok
test native::capture::tests::placement::heading_matches_bullet_selector_is_raw_or_identity ... ok
test native::capture::tests::placement::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::placement::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::placement::formats_scheduled_date_from_offset ... ok
test native::capture::tests::placement::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::placement::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::placement::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::placement::generated_group_prefix_without_authored_match_falls_back ... ok
test native::capture::tests::placement::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::placement::forced_route_accepts_terminal_type_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::placement::formats_bullet_line ... ok
test native::capture::tests::placement::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::placement::json_success_shape_is_stable ... ok
test native::capture::tests::placement::inserts_after_single_top_level_task ... ok
test native::capture::tests::placement::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::placement::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::placement::non_article_numbered_heading_keeps_raw_title_matching ... ok
test native::capture::tests::placement::article_exact_section_matches_de_numbered_identity ... ok
test native::capture::tests::placement::article_slug_matches_after_raw_and_identity ... ok
test native::capture::tests::placement::raw_prefix_beats_an_earlier_slug_match ... ok
test native::capture::tests::placement::article_exact_section_matches_plain_identity ... ok
test native::capture::tests::placement::article_prefix_matches_de_numbered_identity ... ok
test native::capture::tests::placement::article_exact_section_matches_stale_number ... ok
test native::capture::tests::placement::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::placement::slug_selector_falls_back_to_h1_when_no_non_h1_matches ... ok
test native::capture::tests::placement::slug_selector_reaches_spaced_heading ... ok
test native::capture::tests::placement::prefix_skips_generated_blocked_group_for_authored_match ... ok
test native::capture::tests::placement::section_completion_prefers_raw_then_slug_then_quoted ... ok
test native::capture::tests::placement::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::placement::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::placement::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::tests::placement::section_completion_omits_selectors_that_cannot_round_trip ... ok
test native::capture::tests::placement::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::placement::section_completion_slug_query_matches_spaced_title ... ok
test native::capture::tests::placement::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::started::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::placement::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::started::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started::non_tasks_section_headings_skip_generated_status_groups ... ok
test native::capture::tests::started::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::started::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::started::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::placement::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::placement::whole_slug_beats_an_earlier_slug_prefix ... ok
test native::capture::tests::started::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::started::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::tests::placement::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::started::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture::tests::placement::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::started::started_pomodoro_move_preserves_crlf ... ok
test native::capture::tests::type_marker::capture_parse_recognizes_hash_type_marker ... ok
test native::capture_block_ids::tests::block_id_calibration ... ignored, set BOB_ID_CALIBRATION_VAULT to a vault of Markdown notes
test native::capture_block_ids::tests::first_suggestion_prefers_three_words_within_twenty_bytes ... ok
test native::capture_block_ids::tests::suggestions_offer_code_span_phrase_and_honor_length_cap ... ok
test native::capture_block_ids::tests::suggestions_drop_filler_leadins_and_keep_content_verbs ... ok
test native::capture_block_ids::tests::used_covers_done_nontask_duplicates_and_document_order ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_block_ids::tests::successor_mints_follow_the_pinned_vectors ... ok
test native::capture_block_ids::tests::allowed_regex_agrees_with_validator_for_every_ascii_char ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_block_ids::tests::suggestions_follow_the_pinned_examples ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture::blocked_tasks::tests::prj_internal_same_note_and_descendant_refuse ... ok
test native::capture::task_blocks::tests::nested_parent_reports_depths_relative_to_its_line ... ok
test native::capture::task_blocks::tests::task_ref_parent_omits_block_id_but_reports_its_block ... ok
test native::capture_completable_tasks::tests::draft_selected_marks_only_other_items ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture::inbox_route::tests::ir_routed_batch_rolls_back_when_a_repaired_file_changes ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_active_tasks::tests::excludes_ready_tasks_even_with_now_text ... ok
test native::capture_completable_tasks::tests::empty_query_orders_today_first_then_status ... ok
test native::capture_completable_tasks::tests::guard_reasons_match_the_contract ... ok
test native::capture_complete::drawers::tests::ellipsize_keeps_short_text_and_trims_long_text ... ok
test native::capture_complete::drawers::tests::plural_copy_is_singular_only_for_one ... ok
test native::capture_complete::drawers::tests::quote_escape_protects_quotes_and_backslashes ... ok
test native::capture_complete::drawers::tests::age_phrase_buckets_follow_whole_days ... ok
test native::capture::tests::template::sa36_hello_and_plain_x_add_no_relation_snapshot_reads ... ok
test native::capture::tests::commit::cumulative_stages_into_one_note_commit ... ok
test native::capture::task_blocks::tests::interior_blank_lines_are_kept_in_the_block ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_rotten_log ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture::blocked_tasks::tests::existing_owner_is_uncapped_at_in_progress ... ok
test native::capture::task_blocks::tests::crlf_note_reports_verbatim_texts_without_terminators ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_completable_tasks::tests::missing_day_file_means_no_today_rows ... ok
test native::capture::task_blocks::tests::cross_note_first_touch_order_with_revisit_and_second_parent ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_completable_tasks::tests::open_tasks_list_with_locators_scheduled_and_suggestions ... ok
test native::capture_completable_tasks::tests::hidden_and_recurring_sink_within_their_section ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_completable_tasks::tests::recurring_today_rows_sink_below_visible_rows_in_the_same_entry ... ok
test native::capture::blocked_tasks::tests::a8_refusals_name_star_and_teach ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_excludes_ready_tasks ... ok
test native::capture_completable_tasks::tests::struck_fenced_and_depends_on_links_never_place ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_complete::tests::active_tasks::active_task_human_rows_name_the_queue ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture::note_pull::tests::np23_day_without_pomodoros_uses_existing_error ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_an_existing_task_offers_bare_titles_with_the_glued_copy ... ok
test native::capture::project_note::tests::offer_none_keeps_create_files_and_emits_unselected_rows ... ok
test native::capture::note_pull::tests::np1_no_pick_reports_lane_order_and_writes_nothing ... ok
test native::capture_complete::tests::blocked_tasks::blocked_task_shell_rows_use_the_blocked_tasks_group ... ok
test native::capture_complete::tests::drawers::bullet_menu_filters_by_the_typed_name_and_decodes_a_quoted_literal ... ok
test native::capture::note_pull::tests::np2_pick_all_links_statuses_mints_and_stamps ... ok
test native::capture::note_pull::tests::batch_repeated_source_second_pull_pruned_not_refused ... ok
test native::capture::task_blocks::tests::created_parent_reports_every_row_added ... ok
test native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_names_a_trailing_range_as_running ... ok
test native::capture::blocked_tasks::tests::next_cap_holds_in_progress_dependent_and_prj_resident ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_disables_when_two_open_timed_entries_mix_formats ... ok
test native::capture::task_blocks::tests::two_parents_forward_across_an_insert_above ... ok
test native::capture_completable_tasks::tests::nonempty_query_keeps_today_matches_on_top ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_describes_the_selected_session ... ok
test native::capture_complete::tests::directives::bare_percent_opens_ordered_directive_menu_with_no_initial_selection ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_new_project_note_creates_title_case_sections ... ok
test native::capture_complete::tests::directives::directive_query_filters_by_letter_and_never_reads_clipboard ... ok
test native::capture_complete::tests::directives::directive_containing_menu_does_not_preselect_a_row ... ok
test native::capture::note_pull::tests::np6_own_prj_never_offered_or_counted ... ok
test native::capture_complete::tests::drawers::shell_completion_never_reaches_a_bullet_start ... ok
test native::capture_complete::tests::drawers::empty_query_lists_task_then_recent_rows_and_opens_unselected ... ok
test native::capture::project_note::tests::offer_scratch_placement_does_not_commit_probe_ids ... ok
test native::capture_complete::tests::output::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::output::empty_json_context_is_null ... ok
test native::capture_complete::tests::output::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::output::json_shape_is_stable ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_new_task_offers_recent_and_new_rows_only ... ok
test native::capture::note_pull::tests::np20_two_pulls_keep_item_order_and_continue_numbers ... ok
test native::capture_complete::tests::output::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture::note_pull::tests::np17_same_draft_creation_offered_without_fresh_stamp ... ok
test native::capture_complete::tests::directives::listen_row_activates_when_configured ... ok
test native::capture::note_pull::tests::np15_none_selection_writes_nothing_and_mints_nothing ... ok
test native::capture_completable_tasks::tests::today_roles_precedence_sessions_and_pomodoro ... ok
test native::capture_complete::tests::drawers::a_task_without_drawers_lists_recent_and_new_only ... ok
test native::capture::note_pull::tests::np13_require_choice_without_picks_refuses ... ok
test native::capture_complete::tests::drawers::shell_drawer_rows_are_the_targets_own_unrefused_drawers ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_complete::tests::output::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_complete::tests::output::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::output::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture_complete::tests::pomodoros::bare_start_name_replacements_prefix_hash_when_the_slug_cannot_be_bare ... ok
test native::capture_complete::tests::pomodoros::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_candidates_omit_next_up ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_today_before_creation_and_utilities ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_suppresses_creation_only_for_exact_open_names ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_filters_and_creates_by_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_lists_start_again_and_name_it_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_human_labels_cover_every_row_kind ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_orders_repeated_completed_names_newest_first ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_puts_the_running_entry_last ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_rows_carry_no_budget_preview ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture::tests::commit::commits_matching_multi_file_preimage ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::capture::note_pull::tests::np3_live_link_folds_already_planned ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_prj_task_lists_sections_and_refuses_structural_ones ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_complete::tests::drawers::rows_rank_prefix_before_substring_in_document_order ... ok
test native::capture_complete::tests::drawers::task_rows_carry_counts_singular_plural_detail_and_consequences ... ok
test native::capture::note_pull::tests::np21_subset_pick_links_only_picked_row ... ok
test native::capture_complete::tests::drawers::replacement_is_a_slug_only_when_it_resolves_back_to_the_same_drawer ... ok
test native::capture::project_note::tests::offer_iterator_and_completion_count_see_project_rows ... ok
test native::capture_complete::tests::drawers::bullet_replacement_continues_with_a_nested_bullet_only_when_nothing_follows ... ok
test native::capture_complete::tests::drawers::typed_query_drops_the_unselected_open_and_filters_every_group ... ok
test native::capture_complete::tests::relations::cancel_new_owner_is_refused_with_relabel_hint ... ok
test native::capture_complete::tests::directives::url_directive_menu_offers_listen_with_config_status ... ok
test native::capture_complete::tests::directives::shell_completion_exposes_safe_directive_rows_under_directives_group ... ok
test native::capture_complete::tests::drawers::bullet_rows_refuse_with_the_exact_resolvers_reason ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture_completable_tasks::tests::bang_replacement_quotes_reserved_locators ... ok
test native::capture_complete::tests::drawers::bullet_starts_that_cannot_name_a_drawer_are_empty_successes ... ok
test native::capture_complete::tests::drawers::bullet_new_row_spells_a_typed_slug_as_the_title_the_shortcut_creates ... ok
test native::capture_complete::tests::output::close_items_and_suffixes_request_no_completion ... ok
test native::capture_complete::tests::routes_tasks::double_at_offers_only_destinations_never_a_template_candidate ... ok
test native::capture_complete::tests::parent_tasks::vault_catalog_excludes_non_capture_and_terminal_notes ... ok
test native::capture_complete::tests::parent_tasks::bare_plus_serves_vault_candidates_and_operator_hints ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_matches_pomodoro_name_warnings ... ok
test native::capture_complete::tests::relations::relation_label_leading_and_dependency_tail_keep_narrow_ranges ... ok
test native::capture_complete::tests::relations::cancel_from_direction_resolves_the_token_source ... ok
test native::capture_complete::tests::drawers::nested_bullet_hash_still_offers_task_types ... ok
test native::capture_complete::tests::drawers::unresolvable_targets_report_a_diagnostic_and_no_rows ... ok
test native::capture_complete::tests::routes_tasks::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::relations::cancel_inverse_query_teaches_the_flip ... ok
test native::capture_complete::tests::relations::cancel_overlay_marks_rows_and_reports_cancels_for_to_owner ... ok
test native::capture::note_pull::tests::np5_fold_precedence_and_today_scheduled_offered ... ok
test native::capture_complete::tests::relations::cancel_hidden_overlay_stays_out_but_typed_match_shows_state ... ok
test native::capture_complete::tests::drawers::replacement_covers_the_hash_and_the_name_and_reports_cursor_after ... ok
test native::capture_complete::tests::parent_tasks::leading_plus_query_refetch_keeps_token_range_and_full_catalog ... ok
test native::capture_complete::tests::relations::complete_and_cancel_cues_coexist_when_both_policies_are_configured ... ok
test native::capture_complete::tests::drawers::recent_rows_are_catalog_keys_the_task_lacks ... ok
test native::capture_complete::tests::relations::parent_picker_reports_typed_relation_direction_and_target_text ... ok
test native::capture_complete::tests::relations::complete_from_direction_hints_inverses_and_disables_refused_rows ... ok
test native::capture_complete::tests::routes_tasks::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::routes_tasks::route_completion_matches_aliases_with_canonical_replacement_after_prefix ... ok
test native::capture_complete::tests::routes_tasks::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::parent_tasks::plus_query_ranks_candidates_and_scoped_descriptors_keep_exact_ranges ... ok
test native::capture_complete::tests::relations::relation_pools_follow_directional_tiers_and_editability ... ok
test native::capture_complete::tests::routes_tasks::section_completion_partial_quoted_query_covers_the_literal ... ok
test native::capture_complete::tests::parent_tasks::scoped_missing_and_empty_notes_keep_picker_and_empty_catalog ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_list_header_with_bullets ... ok
test native::capture_complete::tests::drawers::new_row_hints_at_a_near_catalog_key ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_complete::tests::drawers::refused_rows_carry_the_commit_resolvers_reason ... ok
test native::capture_complete::tests::relations::cancel_closed_source_links_only_without_disabling ... ok
test native::capture_complete::tests::routes_tasks::section_completion_quote_leading_titles_use_exact_fallback ... ok
test native::capture_complete::tests::routes_tasks::shell_completion_preserves_quoted_section_replacement ... ok
test native::capture_complete::tests::relations::complete_project_and_closed_sources_only_report_link_effects ... ok
test native::capture_dependency_tasks::tests::hidden_tasks_detect_only_the_exact_tag ... ok
test native::capture_drawers::tests::catalog_search_ranks_prefix_tier_first_and_skips_excluded_keys ... ok
test native::capture_drawers::tests::build_cli_renders_without_panicking ... ok
test native::capture_drawers::tests::checkboxed_all_caps_children_are_not_drawers ... ok
test native::capture_drawers::tests::empty_drawer_bullet_still_qualifies ... ok
test native::capture_dependency_tasks::tests::quoted_locator_round_trips_through_replacement ... ok
test native::capture_drawers::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_drawers::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_drawers::tests::grandchild_is_not_a_direct_child_drawer ... ok
test native::capture_drawers::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_drawers::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_drawers::tests::last_entry_text_is_the_direct_entry_a_capture_lands_after ... ok
test native::capture_drawers::tests::query_matches_a_key_or_slug_by_prefix_before_substring ... ok
test native::capture_drawers::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_drawers::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_drawers::tests::reserved_refusals_name_the_reserved_key ... ok
test native::capture_drawers::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_drawers::tests::managed_logs_are_never_drawers_plain_titles_are ... ok
test native::capture_drawers::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_drawers::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_drawers::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_flag_guard::tests::declared_flags_values_and_text_pass_through ... ok
test native::capture_flag_guard::tests::equals_only_short_combined_with_declared_option_then_unknown_is_rejected ... ok
test native::capture_flag_guard::tests::mixed_short_cluster_then_unknown_long_is_rejected ... ok
test native::capture_drawers::tests::title_whitelist_edges ... ok
test native::capture_flag_guard::tests::short_format_json_with_unknown_flag_reports_json ... ok
test native::capture_flag_guard::tests::text_starting_with_a_flag_word_needs_the_delimiter ... ok
test native::capture_flag_guard::tests::undeclared_short_cluster_is_text ... ok
test native::capture_flag_guard::tests::guard_specs_match_clap_declarations ... ok
test native::capture_flag_guard::tests::unknown_long_flag_before_text_is_rejected ... ok
test native::capture_flag_guard::tests::value_taking_short_with_attached_cluster_rest_is_the_value ... ok
test native::capture_language::bare_name::tests::bare_name_len_matches_letter_led_non_close_shapes ... ok
test native::capture_language::bare_name::tests::can_spell_bare_rejects_digit_led_and_close_shapes ... ok
test native::capture_language::bare_name::tests::composed_tokens_keep_hash_when_the_name_cannot_be_bare ... ok
test native::capture_language::close_log::tests::assign_log_positions_follows_the_assignment_rule ... ok
test native::capture_language::close_log::tests::first_bullet_kind_detection_skips_placeholders ... ok
test native::capture_language::close_log::tests::default_log_index_covers_every_close_shape ... ok
test native::capture_language::close_log::tests::inline_entry_defaults_and_leading_numbers ... ok
test native::capture_language::close_log::tests::inline_entry_reports_dangling ... ok
test native::capture_language::close_log::tests::inline_entry_reports_diagnostics_in_order ... ok
test native::capture_language::close_log::tests::lexes_entries_and_details ... ok
test native::capture_language::close_log::tests::mixed_numbering_fails_both_orders ... ok
test native::capture_language::close_log::tests::log_entries_from_lex_marks_star_origin ... ok
test native::capture_language::close_log::tests::positional_entries_carry_their_typed_position ... ok
test native::capture_language::close_log::tests::rejects_bad_bullets ... ok
test native::capture_language::close_log::tests::reports_dangling ... ok
test native::capture_language::close_log::tests::star_bullets_are_recognized_and_stay_unexpanded ... ok
test native::capture_language::close_log::tests::star_bullets_carry_details_and_dangle ... ok
test native::capture_language::close_log::tests::star_bullets_report_selection_mode_failures ... ok
test native::capture_language::close_log::tests::star_bullets_mix_with_either_list_kind ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_report_lexical_failures ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_stay_unresolved_without_a_selection ... ok
test native::capture_language::close_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::close_selection::tests::lex_reports_drop_selections ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_positionally_in_selection_mode ... ok
test native::capture_language::close_selection::tests::lex_reports_park_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::close_selection::tests::lex_reports_trailing_at_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_valid_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_wildcard_groups ... ok
test native::capture_language::close_selection::tests::retired_whole_item_spellings_name_their_bare_rewrite ... ok
test native::capture_language::close_selection::tests::selection_shape_detection ... ok
test native::capture_complete::tests::routes_tasks::template_completion_still_completes_markers_in_the_definition ... ok
test native::capture_complete::tests::drawers::new_row_needs_a_typed_name_no_other_row_claims ... ok
test native::capture_complete::tests::parent_tasks::unicode_duplicates_and_queued_pomodoros_stay_in_catalog ... ok
test native::capture_complete::tests::relations::cancel_recurring_source_disables_cancel_rows ... ok
test native::capture_complete::tests::drawers::project_note_prj_target_lists_sections_and_creates_title_case_sections ... ok
test native::capture_dependency_tasks::tests::groups_follow_the_picker_sections ... ok
test native::capture_complete::tests::routes_tasks::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::capture_dependency_tasks::tests::catalog_covers_every_task_bearing_note_kind ... ok
test native::capture_complete::tests::relations::relation_target_replacement_stops_before_an_existing_label ... ok
test native::capture_complete::tests::relations::cancel_project_source_keeps_residents_open ... ok
test native::capture_dependency_tasks::tests::empty_query_orders_same_note_lanes_history ... ok
test native::capture_complete::tests::drawers::empty_query_recent_is_capped_at_eight_keys ... ok
test native::capture_language::dependencies::tests::bare_sigil_is_directive_only_at_the_ends ... ok
test native::capture_language::dependencies::tests::blocked_task_modifiers_have_separate_entries_and_spans ... ok
test native::capture_language::dependencies::tests::escape_consumes_only_its_backslash ... ok
test native::capture_complete::tests::task_links::task_link_completion_lists_worked_example_in_canonical_order ... ok
test native::capture_complete::tests::task_links::task_link_completion_keeps_candidates_when_the_day_file_is_missing ... ok
test native::capture_language::dependencies::tests::protected_spans_are_never_modifiers ... ok
test native::capture_language::dependencies::tests::escaped_star_unescapes_only_inside_a_modifier_run ... ok
test native::capture_language::dependencies::tests::mid_line_modifiers_stay_literal ... ok
test native::capture_language::dependencies::tests::quoted_note_with_spaces_stays_atomic ... ok
test native::capture_complete::tests::task_links::task_link_completion_pins_json_shape_and_omissions ... ok
test native::capture_language::dependencies::tests::trailing_complete_modifier_strips_and_spans ... ok
test native::capture_language::dependencies::tests::quoted_escapes_decode ... ok
test native::capture_complete::tests::relations::relation_label_double_pipe_keeps_pipes_and_reports_one_off ... ok
test native::capture_language::dependencies::tests::traversal_and_bad_ids_are_invalid ... ok
test native::capture_complete::tests::routes_tasks::section_completion_round_trips_slug_and_quoted_replacements ... ok
test native::capture_language::dependencies::tests::star_markdown_and_mid_line_tokens_stay_literal ... ok
test native::capture_language::dependencies::tests::unicode_offsets_stay_on_char_boundaries ... ok
test native::capture_language::pomodoro_literal::tests::expand_covers_spaced_literals ... ok
test native::capture_complete::tests::task_links::task_link_completion_scopes_to_the_batch_second_item ... ok
test native::capture_language::pomodoro_literal::tests::lex_decodes_only_quote_and_backslash_escapes ... ok
test native::capture_language::pomodoro_literal::tests::lex_rejects_non_quote_openers ... ok
test native::capture::note_pull::tests::np19_hand_off_owns_row_later_pull_omits ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_unterminated_as_incomplete ... ok
test native::capture_language::project_tasks::tests::lexer_accepts_the_boundary_set ... ok
test native::capture::note_pull::tests::np7_only_source_residents_offered ... ok
test native::capture_language::project_tasks::tests::reserved_name_matches_in_any_letter_case ... ok
test native::capture_language::project_tasks::tests::suffix_helpers_split_on_the_last_word ... ok
test native::capture_language::start_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::start_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::start_selection::tests::lex_reports_valid_drop_lists ... ok
test native::capture_language::tests::bare_close::bare_close_classifier_claims_only_the_documented_shapes ... ok
test native::capture_complete::tests::directives::bare_hash_type_menu_also_has_no_initial_selection ... ok
test native::capture_dependency_tasks::tests::unique_basename_resolves_before_ambiguous_paths ... ok
test native::capture_language::dependencies::tests::unterminated_quote_is_one_partial ... ok
test native::capture_drawers::tests::resolved_task_with_no_drawers_is_a_successful_empty_list ... ok
test native::capture_drawers::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_drawers::tests::lists_drawers_in_document_order_for_a_block_id ... ok
test native::capture_dependency_tasks::tests::ranking_shares_the_tiered_matcher_vectors ... ok
test native::capture_complete::tests::task_links::task_link_completion_queries_cover_the_sigil_and_rank ... ok
test native::capture_drawers::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_complete::tests::task_links::task_link_human_rows_name_queues_and_missing_ids ... ok
test native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_straight_and_curly_literals ... ok
test native::capture_language::tests::bare_close::bare_close_suppresses_marker_completion_in_work_log_text ... ok
test native::capture_language::tests::chain::chain_token_predicate_covers_the_documented_table ... ok
test native::capture_language::tests::chain::editor_reports_selection_spans_at_absolute_offsets_in_a_chain ... ok
test native::capture_language::tests::chain::draft_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::bare_close::bare_close_spans_cover_the_one_byte_x_and_each_list ... ok
test native::capture_language::tests::chain::draft_keeps_sequential_indices_across_crlf_with_a_chain ... ok
test native::capture_language::tests::chain::execution_carries_a_close_selection_through_a_chain ... ok
test native::capture_language::tests::chain::execution_distinguishes_spaced_start_adjust_from_offset_start ... ok
test native::capture_language::tests::chain::execution_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::completion_requests_nothing_anywhere_on_a_chain ... ok
test native::capture_language::tests::chain::bang_items_claim_each_blank_line_block_independently ... ok
test native::capture_language::tests::chain::chain_token_predicate_equals_claimed_for_single_tokens ... ok
test native::capture_language::tests::chain::draft_splits_a_two_token_chain_with_absolute_ranges ... ok
test native::capture_language::tests::chain::draft_splits_tabs_and_runs_of_spaces ... ok
test native::capture_language::tests::chain::editor_chain_items_do_not_inherit_a_global_declaration ... ok
test native::capture_language::tests::chain::editor_reports_a_broken_second_token_with_its_own_diagnostic ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_plus_adjustment_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_dangling_close_separator_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_chain_with_absolute_spans ... ok
test native::capture_language::tests::chain::draft_splits_retired_double_tokens_and_reports_their_own_ranges ... ok
test native::capture_language::tests::chain::editor_reports_an_incomplete_named_start_inside_a_chain ... ok
test native::capture_language::tests::chain::draft_chain_works_with_a_global_declaration ... ok
test native::capture_language::tests::bare_close::bare_close_heads_session_chains_and_inline_trails ... ok
test native::capture_language::tests::chain::bang_claim_beats_dependency_errors ... ok
test native::capture_language::tests::chain::execution_rejects_forced_destinations_on_the_first_chain_token ... ok
test native::capture_language::tests::chain::execution_runs_a_chain_left_to_right ... ok
test native::capture_language::tests::chain::editor_reports_two_items_with_absolute_spans_for_a_chain ... ok
test native::capture_language::tests::completion::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::chain::execution_reports_a_broken_second_token_on_its_own_range ... ok
test native::capture_language::tests::chain::execution_switches_sessions_with_close_then_start ... ok
test native::capture_language::tests::completion::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion::completion_on_global_declarations_only_completes_the_route ... ok
test native::capture_language::tests::chain::execution_leaves_non_chains_unchanged ... ok
test native::capture_language::tests::completion::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_language::tests::completion::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion::drawer_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::completion::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::completion::empty_selector_after_hash_is_a_one_byte_drawer_field ... ok
test native::capture_language::tests::completion::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::completion::caret_suffix_names_preserve_the_link_part_for_completion ... ok
test native::capture_language::tests::completion::free_standing_hash_fragments_request_task_type_completion ... ok
test native::capture_language::tests::completion::a_cursor_on_a_type_marker_requests_task_type_completion ... ok
test native::capture_language::tests::completion::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::completion::hash_after_a_bare_block_id_marker_completes_a_task_type ... ok
test native::capture_language::tests::bare_close::bare_close_selection_shapes_report_the_same_close_everywhere ... ok
test native::capture_language::tests::completion::hash_completion_is_lexical_even_when_the_subject_will_refuse_it ... ok
test native::capture_language::tests::completion::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::completion::hash_ends_the_block_id_and_opens_the_drawer_replacement ... ok
test native::capture_language::tests::bare_close::prose_and_uppercase_x_remain_tasks ... ok
test native::capture_language::tests::completion::list_header_completes_route_after_bullets ... ok
test native::capture_language::tests::completion::list_header_completes_partial_quoted_section_after_bullets ... ok
test native::capture_language::tests::completion::list_header_completes_section_after_bullets ... ok
test native::capture_language::tests::completion::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::completion::block_id_project_note_sigil_is_excluded_from_replacement ... ok
test native::capture_language::tests::completion::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion::empty_block_id_with_section_still_yields_a_drawer_field ... ok
test native::capture_language::tests::completion::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture::project_note::tests::offer_all_mints_ids_and_links_like_colon_bullets ... ok
test native::capture_complete::tests::routes_tasks::template_rows_and_placeholders_do_not_open_route_completion ... ok
test native::capture::note_pull::tests::np18_later_link_drops_earlier_pull_row ... ok
test native::capture_complete::tests::routes_tasks::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture::note_pull::tests::np9_ref_nested_recurring_offered ... ok
test native::capture_complete::tests::relations::relation_shell_groups_are_directional_and_skip_guarded_rows ... ok
test native::capture_language::tests::completion::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::completion::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_start_name_leaves_link_form_names_alone ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_per_token_inside_chains ... ok
test native::capture_language::tests::completion::list_header_completes_with_crlf_and_utf8_before_it ... ok
test native::capture_language::tests::completion::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_complete::tests::relations::complete_overlay_marks_rows_and_reports_source_consequence ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_a_bare_name_with_the_bare_flag ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_lone_colon ... ok
test native::capture_language::tests::completion::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::completion::pomodoro_start_name_context_reports_ledger_behavior ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_after_hash_on_a_named_start ... ok
test native::capture_language::tests::completion::nested_project_task_block_id_completes_for_its_owner ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_partial_id ... ok
test native::capture_language::tests::completion::project_task_id_before_a_child_line_route_marker_still_completes ... ok
test native::capture_language::tests::completion::query_and_caret_completion_survive_a_neighboring_marker ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_caret_id ... ok
test native::capture_language::tests::completion::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_on_nested_project_bullets_through_owner ... ok
test native::capture_complete::tests::relations::successor_labels_offer_and_explain_inverse_and_released_targets ... ok
test native::capture_language::tests::completion::parent_task_plus_completes_the_terminal_token_with_utf8_byte_ranges ... ok
test native::capture_language::tests::completion::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::parent_task_plus_is_shared_across_parent_and_authored_lines ... ok
test native::capture_language::tests::completion::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::completion::pomodoro_link_suffix_names_complete_without_replacing_the_link_start ... ok
test native::capture_language::tests::completion::parent_task_plus_preserves_operator_and_protected_text_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::draft::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::completion::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture_language::tests::completion::work_log_bullet_lines_request_no_marker_completion ... ok
test native::capture_language::tests::completion::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::completion::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::draft::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::completion::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::draft::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::draft::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::completion::quoted_drawer_literal_decodes_its_query_and_replaces_the_quotes ... ok
test native::capture_language::tests::completion::retired_doubled_start_has_no_name_completion_or_override_context ... ok
test native::capture_language::tests::completion::task_link_query_completes_the_sigil_inclusive_token ... ok
test native::capture_language::tests::draft::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::draft::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::completion::task_list_block_id_completes_on_bullet_and_nested_lines ... ok
test native::capture_language::tests::completion::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::completion::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::completion::quoted_section_literal_decodes_its_query_and_replaces_the_quotes ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::completion::task_block_id_route_and_authored_id_both_complete ... ok
test native::capture_language::tests::draft::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::draft::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::draft::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::draft::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::draft::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::draft::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::draft::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::draft::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::draft::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::draft::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::draft::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::completion::route_completion_beside_a_type_marker_keeps_original_ranges ... ok
test native::capture_language::tests::draft::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::draft::execution_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::draft::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::draft::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::draft::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::draft::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::draft::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::draft::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::drawer_bullet::leading_hash_on_a_first_level_bullet_is_a_drawer_shortcut ... ok
test native::capture_language::tests::draft::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::drawer_bullet::quoted_literal_digit_heading_and_escaped_hashes ... ok
test native::capture_language::tests::drawer_bullet::bullet_query_decodes_a_partial_and_a_closed_literal ... ok
test native::capture_language::tests::draft::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::drawer_bullet::leftover_text_on_a_shortcut_is_drawer_bullet_text ... ok
test native::capture_language::tests::drawer_bullet::nested_hash_still_types_and_first_level_does_not ... ok
test native::capture_language::tests::drawer_bullet::each_reserved_bullet_is_flagged_once_and_a_glued_drawer_stays_quiet ... ok
test native::capture_language::tests::drawer_bullet::nested_and_parent_line_hashes_still_complete_task_types ... ok
test native::capture_language::tests::draft::execution_refuses_retired_priority_markers ... ok
test native::capture_language::tests::drawer_bullet::childless_shortcut_and_escaped_literal_hash ... ok
test native::capture_language::tests::drawer_bullet::bullet_start_hash_claims_a_drawer_field_not_a_type_field ... ok
test native::capture_language::tests::drawer_bullet::bullet_cursor_must_follow_the_hash ... ok
test native::capture_language::tests::draft::execution_treats_bare_dollar_as_priority_level_one ... ok
test native::capture_language::tests::drawer_bullet::a_new_project_note_keeps_its_structural_sections ... ok
test native::capture_language::tests::drawer_bullet::reserved_childless_shortcut_keeps_its_drawer_notes_need ... ok
test native::capture_language::tests::editor_modes::editor_rejects_checkbox_only_project_task_ids_over_the_id_token ... ok
test native::capture_language::tests::drawer_bullet::reserved_ranges_are_utf8_byte_offsets ... ok
test native::capture_language::tests::drawer_bullet::reserved_diagnostic_message_matches_the_commit_resolver ... ok
test native::capture_language::tests::drawer_bullet::bullet_continuation_needs_a_token_ending_the_line_without_a_nested_bullet ... ok
test native::capture_language::tests::drawer_bullet::bullet_drawer_target_follows_the_item_shape ... ok
test native::capture_language::tests::editor_modes::editor_holds_unused_pomodoro_while_a_colon_id_is_unfinished ... ok
test native::capture_language::tests::editor_modes::caret_close_conflicts_agree_with_execution ... ok
test native::capture_language::tests::editor_modes::editor_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::drawer_bullet::legal_controls_and_vault_dependent_names_stay_unflagged ... ok
test native::capture_language::tests::drawer_bullet::bullet_starts_outside_an_under_task_position_open_nothing ... ok
test native::capture_language::tests::drawer_bullet::execution_files_a_shortcut_under_a_new_task ... ok
test native::capture_language::tests::editor_modes::editor_reports_named_pomodoro_start_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::drawer_bullet::editor_reports_drawer_needs_and_all_caps_spans ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_complete_modes_needs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_retired_doubled_start_forms_over_the_token ... ok
test native::capture_language::tests::editor_spans::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_start_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_hash_token_is_a_task_type_marker_now ... ok
test native::capture_language::tests::editor_modes::editor_reports_unused_project_note_pomodoro_over_the_name ... ok
test native::capture_language::tests::editor_spans::editor_reports_bare_dollar_as_a_priority_span ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_link_queries_as_incomplete ... ok
test native::capture_language::tests::editor_spans::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_spans::attached_task_type_after_block_id_is_not_a_project_note_error ... ok
test native::capture_language::tests::editor_spans::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_priority_markers ... ok
test native::capture_language::tests::editor_spans::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_spans::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_language::tests::editor_spans::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_modes::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::editor_spans::editor_spans_a_bare_named_start_without_a_hash_gap ... ok
test native::capture_language::tests::editor_spans::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_task_complete_tokens ... ok
test native::capture_language::tests::editor_spans::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::editor_spans::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_spans::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::exact_name::bare_name_spelling_never_takes_quotes ... ok
test native::capture_language::tests::exact_name::close_hash_teaches_with_decoded_name ... ok
test native::capture_language::tests::editor_spans::editor_spans_pomodoro_link_names_after_the_equal_suffix ... ok
test native::capture_language::tests::exact_name::invalid_literal_names_error ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::exact_name::exact_name_start_reports_canonical_name_and_literal_flag ... ok
test native::capture_language::tests::editor_spans::editor_link_suffix_incomplete_states_keep_timing_and_placeholders ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_spans::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::exact_name::partial_literal_completes_on_decoded_text ... ok
test native::capture_language::tests::exact_name::literal_spans_cover_the_quotes ... ok
test native::capture_language::tests::editor_spans::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::exact_name::exact_name_accepts_round_trip_fixtures ... ok
test native::capture_language::tests::editor_modes::editor_reports_project_task_ids_with_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::drawer_bullet::editor_flags_reserved_shortcuts_and_literals_under_a_task ... ok
test native::capture_language::tests::editor_spans::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::editor_spans::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_spans::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::editor_spans::editor_t_colon_is_ordinary_prose ... ok
test native::capture_language::tests::editor_spans::editor_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::exact_name::unterminated_literal_is_incomplete_never_a_mistake ... ok
test native::capture_language::tests::editor_spans::task_link_query_spans_the_whole_token_as_a_placeholder ... ok
test native::capture_language::tests::editor_spans::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::exact_name::exact_name_link_reports_canonical_name ... ok
test native::capture_language::tests::globals::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::globals::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::globals::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::globals::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::globals::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::grammar::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::globals::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::goto::goto_completion_field_reports_sigil_relative_queries ... ok
test native::capture_language::tests::grammar::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::editor_modes::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::grammar::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::grammar::colon_alias_owner_is_unchanged_beside_modifiers ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::globals::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::globals::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::grammar::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::grammar::double_pipe_grammar_vectors ... ok
test native::capture_language::tests::editor_spans::incomplete_sealed_offers_keep_offer_modifiers_and_byte_exact_spans ... ok
test native::capture_language::tests::grammar::execution_keeps_task_id_lookalikes_literal_outside_project_notes ... ok
test native::capture_language::tests::grammar::execution_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::editor_modes::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::globals::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::globals::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::globals::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::grammar::execution_evaluates_project_note_markers_parents_and_children_in_order ... ok
test native::capture_language::tests::grammar::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::globals::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::grammar::execution_route_less_sealed_guard_agrees_across_destination_paths ... ok
test native::capture_language::tests::grammar::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::globals::task_complete_items_skip_global_inheritance ... ok
test native::capture_language::tests::grammar::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::grammar::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_markers ... ok
test native::capture_language::tests::goto::goto_claim_leaves_prose_byte_identical ... ok
test native::capture_language::tests::grammar::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::grammar::caret_alias_owns_relationships_in_leading_and_trailing_position ... ok
test native::capture_language::tests::grammar::execution_claims_trailing_hash_types_but_leaves_midline_hash_text ... ok
test native::capture_language::tests::grammar::execution_teaches_bare_named_start_shape_in_the_typed_spelling ... ok
test native::capture_language::tests::goto::goto_claim_covers_every_table_query_row ... ok
test native::capture_language::tests::grammar::execution_accepts_project_task_ids_and_strips_them_from_bodies ... ok
test native::capture_language::tests::grammar::bang_claim_covers_the_contract_table ... ok
test native::capture_language::tests::grammar::execution_rejects_checkbox_only_project_task_ids ... ok
test native::capture_complete::tests::relations::relation_label_suggestions_count_links_and_put_typed_spelling_first ... ok
test native::capture_language::tests::editor_modes::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::grammar::execution_retires_claimed_doubled_start_family ... ok
test native::capture_language::tests::grammar::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_route_less_retired_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_parses_trailing_hash_slugs_as_task_types ... ok
test native::capture_language::tests::grammar::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::grammar::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::grammar::plus_parent_picker_does_not_claim_operators_or_work_log_text ... ok
test native::capture_language::tests::grammar::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::grammar::plus_parent_picker_is_incomplete_but_keeps_the_lone_adjustment ... ok
test native::capture_language::tests::grammar::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::grammar::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::grammar::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::grammar::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::grammar::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_shared_timing_validation_matches_standalone ... ok
test native::capture_language::tests::lists::editor_empty_list_needs_list_item ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffixes_teach_about_drops_duplicate_names_and_glued_timing ... ok
test native::capture_language::tests::lists::editor_bare_header_reports_header_marker ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_offer_markers ... ok
test native::capture_language::tests::lists::editor_item_at_header_with_bullets_resolves_to_first_item ... ok
test native::capture_language::tests::grammar::task_link_query_leaves_prose_byte_identical ... ok
test native::capture_language::tests::lists::editor_lone_at_still_needs_route ... ok
test native::capture_language::tests::grammar::execution_rejects_project_task_id_rule_violations_verbatim ... ok
test native::capture_language::tests::grammar::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::grammar::execution_parses_equals_family_starts_alongside_close ... ok
test native::capture_language::tests::lists::execution_bare_at_with_bullets_refuses_incomplete_route ... ok
test native::capture_language::tests::grammar::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::lists::editor_header_marker_points_at_the_stray_token ... ok
test native::capture_language::tests::lists::editor_list_nested_children_shift_up_one_level ... ok
test native::capture_language::tests::lists::editor_duplicate_ids_land_on_the_second_bullet ... ok
test native::capture_language::tests::lists::editor_lone_route_reports_note_pull ... ok
test native::capture_language::tests::lists::execution_consecutive_headers_split_note_pull_and_list ... ok
test native::capture_language::tests::lists::editor_task_list_reports_items_modes_and_spans ... ok
test native::capture_language::tests::lists::editor_misplaced_and_unfinished_id_states ... ok
test native::capture_language::tests::grammar::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::lists::split_header_starts_item_without_blank_line ... ok
test native::capture_language::tests::grammar::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::lists::execution_list_nested_children_shift_up_one_level ... ok
test native::capture_language::tests::lists::execution_section_list_bullet_kind ... ok
test native::capture_language::tests::lists::execution_lone_route_is_note_pull ... ok
test native::capture_language::tests::grammar::task_link_query_rejects_single_colon_tokens_with_teaching_errors ... ok
test native::capture_language::tests::lists::split_section_list_files_notes ... ok
test native::capture_language::tests::lists::split_quoted_headers_hold_utf8_and_crlf_offsets ... ok
test native::capture_language::tests::lists::split_quoted_headers_decode_and_preserve_exact ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_names_match_the_existing_hash_spelling ... ok
test native::capture_language::tests::grammar::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::lists::split_lone_header_is_an_empty_list ... ok
test native::capture_language::tests::pomodoro_merge::double_star_close_lookalike_stays_not_a_close ... ok
test native::capture_language::tests::lists::split_ignores_declarations_and_non_headers ... ok
test native::capture_language::tests::grammar::typed_existing_task_owner_keeps_dependency_behavior ... ok
test native::capture_language::tests::lists::execution_quoted_sections_carry_exact ... ok
test native::capture_language::tests::pomodoro_merge::dest_less_merge_with_extra_text_is_invalid ... ok
test native::capture_language::tests::grammar::plus_selector_beside_modifiers_needs_task_parent ... ok
test native::capture_language::tests::lists::execution_task_list_bullet_kinds_and_ids ... ok
test native::capture_language::tests::pomodoro_merge::dest_less_merge_is_complete ... ok
test native::capture_language::tests::pomodoro_merge::merge_into_current_omits_src ... ok
test native::capture_language::tests::pomodoro_merge::merge_completion_src_and_dest_fields ... ok
test native::capture_language::tests::grammar::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::pomodoro_merge::merge_token_parses_src_and_dests ... ok
test native::capture_language::tests::pomodoro_merge::extra_text_is_a_shape_error ... ok
test native::capture_language::tests::pomodoro_merge::trailing_hash_needs_dest_in_the_editor ... ok
test native::capture_language::tests::lists::execution_lone_header_markers_keep_previous_meaning ... ok
test native::capture_language::tests::pomodoro_merge::digit_and_marker_star_forms_stay_retired_closes ... ok
test native::capture_language::tests::grammar::relationship_only_owner_refuses_text_extras ... ok
test native::capture_language::tests::lists::execution_list_template_rows_never_split ... ok
test native::capture_language::tests::lists::execution_list_refusals_carry_stable_codes ... ok
test native::capture_language::tests::lists::split_task_list_yields_one_item_per_bullet ... ok
test native::capture_language::tests::pomodoro_merge::merge_editor_spans_cover_sigil_and_names ... ok
test native::capture_language::tests::ref_grammar::bare_url_claims_reference_item_when_routing_is_on ... ok
test native::capture_language::tests::ref_grammar::url_list_split_handles_crlf_with_exact_ranges ... ok
test native::capture_language::tests::ref_grammar::editor_ref_route_spans_use_byte_offsets_including_utf8 ... ok
test native::capture_language::tests::retired_close::retired_closes_with_an_inline_entry_name_the_whole_rewritten_line ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::ref_grammar::editor_url_list_items_each_report_ref ... ok
test native::capture_language::tests::ref_grammar::routing_off_keeps_bare_url_a_task ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::ref_grammar::url_list_requires_every_line ... ok
test native::capture_language::tests::lists::unterminated_section_literal_is_incomplete_never_a_mistake ... ok
test native::capture_language::tests::retired_close::retired_closes_inside_chains_fail_on_their_own_range ... ok
test native::capture_language::tests::ref_grammar::mixed_list_classifies_each_line_on_its_own ... ok
test native::capture_language::tests::retired_close::retired_closes_stay_distinct_from_prose_lookalikes ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_requires_a_cursor ... ok
test native::capture_language::tests::ref_grammar::excluded_hosts_stay_tasks ... ok
test native::capture_language::tests::rewrite::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::ref_grammar::url_list_block_splits_into_one_item_per_line ... ok
test native::capture_language::tests::ref_grammar::editor_reports_ref_mode_with_one_exact_span ... ok
test native::capture_language::tests::retired_close::double_equals_close_lookalikes_teach_the_bare_spelling ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::rewrite::rewrite_draft_does_not_start_templates_from_a_third_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_alternates ... ok
test native::capture_language::tests::ref_grammar::forced_destination_global_and_clip_keep_tasks ... ok
test native::capture_language::tests::rewrite::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::rewrite::rewrite_draft_caret_plus_switches_to_plus ... ok
test native::capture_language::tests::ref_grammar::ref_parent_sources_cover_explicit_global_and_default ... ok
test native::capture_language::tests::grammar::execution_treats_bare_named_starts_as_hash_equivalents ... ok
test native::capture_language::tests::grammar::task_link_claim_is_equivalent_across_execution_editor_and_completion ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_a_sub_bullet_local_marker_local ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_language::tests::ref_grammar::claim_off_cases_stay_tasks ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_template_drafts_untouched ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_back_to_colon_or_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_keeps_absorption_when_it_does_not_claim ... ok
test native::capture_language::tests::retired_close::retired_whole_item_closes_fail_with_the_bare_rewrite_in_both_parsers ... ok
test native::capture_complete::tests::relations::relation_label_completions_carry_relation_and_owner ... ok
test native::capture_language::tests::ref_grammar::percent_l_directive_requests_companion_audio ... ok
test native::capture_language::tests::retired_close::retired_link_close_aliases_fail_with_the_x_rewrite ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_exclusions ... ok
test native::capture_language::tests::grammar::execution_refuses_route_less_sealed_project_note_offers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_requires_a_cursor ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_leaves_type_markers_intact ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_supports_three_way_reverse_from_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_parses_as_the_switched_mode ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attaches_a_pipe_after_a_relation_token ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_exclusions ... ok
test native::capture_language::tests::grammar::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_caret_marker_to_colon ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_colon_marker_to_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_colon_marker_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_before_a_schedule_marker ... ok
test native::capture::tests::commit::complete_label_batch_failure_after_replace_rolls_back ... ok
test native::capture_language::tests::ref_grammar::claim_accepts_wrapper_case_and_hints ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_child_line_trailing_marker ... ok
test native::capture_language::tests::editor_modes::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_one_item_in_a_batch ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_beside_emoji_and_preserves_crlf ... ok
test native::capture_language::tests::template::definition_validation_ignores_rows_but_checks_placeholders_without_rows ... ok
test native::capture_language::tests::template::every_directive_placement_expands_to_the_same_text ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_in_editor_positions ... ok
test native::capture_language::tests::template::a_directive_after_markers_still_claims_the_template ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_with_unicode_crlf_and_schedule ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_uppercase_and_hyphenated_ids ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_solo_and_leading_markers ... ok
test native::capture_language::tests::template::a_repeated_directive_in_the_first_item_is_a_duplicate ... ok
test native::capture_language::tests::template::missing_template_or_rows_has_a_teaching_issue ... ok
test native::capture_language::tests::template::non_template_expansion_is_an_identity ... ok
test native::capture_language::tests::template::multi_placeholder_extra_values_still_report_arity ... ok
test native::capture_language::tests::template::a_template_needs_a_blank_separator_before_rows ... ok
test native::capture_language::tests::template::a_directive_in_a_later_item_is_misplaced ... ok
test native::capture_language::tests::template::placeholder_gaps_and_one_based_indices_are_explained ... ok
test native::capture_language::tests::template::missing_placeholder_is_suppressed_until_rows_exist ... ok
test native::capture_language::tests::template::placeholders_repeat_reorder_escape_and_expand_inside_markers ... ok
test native::capture_language::tests::template::one_placeholder_global_declaration_names_containing_row ... ok
test native::capture_language::tests::template::quote_errors_and_arity_errors_are_row_scoped ... ok
test native::capture_language::tests::template::row_global_declarations_use_row_scope ... ok
test native::capture_language::tests::template::mid_line_and_escaped_directives_leave_an_ordinary_draft ... ok
test native::capture_language::tests::template::placeholder_grammar_rejects_noncanonical_and_incomplete_braces ... ok
test native::capture_language::tests::template::one_placeholder_mixed_lines_number_left_to_right_then_top_to_bottom ... ok
test native::capture_language::tests::template::expansion_matches_the_plan_example_byte_for_byte ... ok
test native::capture_language::tests::template::row_values_cannot_inject_the_template_directive ... ok
test native::capture_language::tests::template::row_lexer_handles_quotes_escapes_and_plain_quotes ... ok
test native::capture_language::tests::template::rows_cannot_be_bullets_and_templates_cannot_use_other_globals ... ok
test native::capture_language::tests::template::one_placeholder_rows_share_line_with_per_value_ranges ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_sealed_project_note_separators ... ok
test native::capture_language::tests::template::one_placeholder_one_line_equals_three_line_expansion ... ok
test native::capture_language::tests::template::template_mask_hides_only_the_directive_token_wherever_it_sits ... ok
test native::capture_language::tests::template::one_field_rows_split_on_spaces_and_template_line_endings_normalize ... ok
test native::capture_language::tests::template::one_placeholder_tabs_and_repeated_spaces_split_cleanly ... ok
test native::capture_language::tests::template::one_placeholder_unterminated_quote_names_value_row_and_keeps_leading_row ... ok
test native::capture_language::tests::type_marker::attached_route_type_completion_keeps_the_marker_attached ... ok
test native::capture_language::tests::template::one_placeholder_templates_never_report_arity ... ok
test native::capture_language::tests::template::template_mask_preserves_byte_offsets_and_hides_directive_rows_and_braces ... ok
test native::capture_language::tests::template::template_directive_sits_at_either_edge_of_any_line_of_the_first_item ... ok
test native::capture_language::tests::type_marker::malformed_masked_operators_keep_their_existing_errors ... ok
test native::capture_language::tests::type_marker::marker_edge_transparency_includes_clip_directives ... ok
test native::capture_language::tests::type_marker_editor::exact_name_resolution_prefers_config_then_catalog ... ok
test native::capture_language::tests::type_marker::unicode_and_crlf_offsets_index_the_original_draft ... ok
test native::capture_language::tests::type_marker::marker_only_continuations_stay_with_the_original_item ... ok
test native::capture_language::tests::type_marker::template_rows_keep_type_metadata_and_template_local_offsets ... ok
test native::capture_language::tests::type_marker::slug_literal_and_marker_run_keep_original_byte_ranges ... ok
test native::capture_language::tests::type_marker_editor::attached_project_marker_stays_midline_only_when_route_is_not_at_an_edge ... ok
test native::capture_language::tests::type_marker_editor::duplicate_markers_share_the_execution_duplicate_diagnostic ... ok
test native::capture_language::tests::type_marker::digit_heading_dash_and_midline_hashes_stay_prose ... ok
test native::capture_language::tests::type_marker_editor::a_marker_alone_needs_a_task ... ok
test native::capture_language::tests::type_marker_editor::marker_only_continuation_lines_contribute_no_child_body ... ok
test native::capture_language::tests::type_marker::edge_clock_tags_stay_task_text_and_never_become_type_markers ... ok
test native::capture_link_tasks::tests::ranker_orders_by_tier_sum_then_canonical_order ... ok
test native::capture_language::tests::type_marker::url_lists_and_operator_chains_probe_the_masked_line ... ok
test native::capture_language::tests::type_marker_editor::global_task_route_inheritance_keeps_type_markers_on_new_tasks ... ok
test native::capture_language::tests::type_marker::only_task_subjects_accept_markers ... ok
test native::capture_language::tests::type_marker_editor::trailing_marker_keeps_the_task_body_and_adds_a_whole_token_span ... ok
test native::capture_language::tests::type_marker_editor::template_rows_keep_markers_out_of_the_body ... ok
test native::capture_language::tests::type_marker_editor::clipboard_notes_accept_type_markers_without_task_need ... ok
test native::capture_language::tests::type_marker::escaped_midline_uppercase_and_protected_tokens_remain_body_text ... ok
test native::capture_language::tests::type_marker_editor::leading_marker_and_child_line_markers_type_the_same_item ... ok
test native::capture_link_tasks::tests::ranker_passes_the_dependency_contract_dk_vectors ... ok
test native::capture_language::tests::type_marker_editor::incomplete_marker_needs_a_task_type_without_a_diagnostic ... ok
test native::capture_language::tests::type_marker_editor::marker_offsets_survive_unicode_and_escaped_text ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_language::tests::type_marker_editor::bodiless_forms_need_a_task_like_their_masked_parse ... ok
test native::capture_language::tests::template::one_placeholder_thousand_and_first_value_is_too_large ... ok
test native::capture_language::tests::type_marker::incomplete_invalid_and_duplicate_markers_have_teaching_errors ... ok
test native::capture_parse::tests::format_pomodoro_close_describes_wildcard_scope ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_parse::tests::format_pomodoro_close_reports_detail_counts ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_language::tests::type_marker_editor::invalid_markers_carry_the_shared_teaching_copy ... ok
test native::capture_language::tests::type_marker_editor::attached_literal_spans_touch_route_ids_and_incomplete_literals_need_type ... ok
test native::capture_language::tests::type_marker::fixture_vectors_preserve_the_task_body_and_attach_one_type ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_language::tests::type_marker_editor::execution_and_editor_agree_on_typed_task_bodies ... ok
test native::capture_language::tests::type_marker_editor::non_task_subjects_are_refused_with_the_shared_copy ... ok
test native::capture_language::tests::type_marker_editor::existing_subjects_accept_markers ... ok
test native::capture_pomodoro_close::ledger::managed_dependency_tests::dependency_lines_are_notes_not_close_targets ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_global_route_with_no_mode_or_block_id_fields ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::lone_route_reports_note_pull_mode ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_pomodoro_close::linked_tasks::clock_tests::only_canonical_daily_timed_entries_supply_a_close_clock ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_pomodoro_close::names::tests::labels_stay_and_untyped_or_drifted_work_leaves_the_name ... ok
test native::capture_pomodoro_close::names::tests::only_fix_worked_narrows_and_the_last_fix_done_sheds ... ok
test native::capture_parse::tests::json_reports_invalid_start_suffixes_as_diagnostics ... ok
test native::capture_pomodoro_close::names::tests::parked_and_dropped_links_are_not_carried ... ok
test native::capture_pomodoro_close::names::tests::shedding_every_type_keeps_the_base ... ok
test native::capture_pomodoro_close::names::tests::single_type_meet_and_unnamed_never_rename ... ok
test native::capture_pomodoro_close::selection_tests::conflicting_duplicates_fail_and_same_outcome_passes ... ok
test native::capture_pomodoro_close::selection_tests::apply_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::drop_removes_from_closed_session_without_carry ... ok
test native::capture_pomodoro_close::selection_tests::embedded_hash_alias_and_tomato ... ok
test native::capture_pomodoro_close::selection_tests::fenced_links_are_unnumbered ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_language::tests::type_marker_editor::masked_items_match_their_baseline_across_grammar_families ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_pomodoro_close::selection_tests::lexically_resolved_positional_entry_reports_nested_wording ... ok
test native::capture_parse::tests::json_reports_retired_doubled_starts_with_token_ranges ... ok
test native::capture_pomodoro_close::selection_tests::log_entries_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_appends_after_existing_descendants ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_child_indent_follows_first_child_or_link_indent ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_nest_one_level_under_the_entry ... ok
test native::capture_parse::tests::json_reports_named_pomodoro_starts ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_preserve_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_errors ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_text_that_numbers_a_link_fails_loudly ... ok
test native::capture_pomodoro_close::selection_tests::managed_dependency_lines_are_not_numbered_for_close_or_agenda ... ok
test native::capture_pomodoro_close::selection_tests::mixed_lines_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::nested_bare_links_are_numbered ... ok
test native::capture_pomodoro_close::selection_tests::numbers_the_worked_example ... ok
test native::capture_pomodoro_close::selection_tests::none_is_byte_identical_to_plan_ledger_close ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_messages ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_with_one_and_zero_links ... ok
test native::capture_pomodoro_close::selection_tests::outcome_table_covers_every_row ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_follow_drop_and_complete_outcomes ... ok
test native::capture_pomodoro_close::selection_tests::parked_links_record_work_but_are_not_carried ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_resolve_against_session_worked_links ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_share_a_single_worked_link ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_skip_nested_links ... ok
test native::capture_parse::tests::json_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_pomodoro_close::selection_tests::rewrite_keeps_prefix_and_drops_tomato ... ok
test native::capture_pomodoro_close::selection_tests::positional_resolution_reports_session_failures ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_dedup_duplicate_targets ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_follow_numbered_bullets_in_non_selection_mode ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_expand_in_typed_order ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_report_nothing_left_and_empty_w ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_use_lexical_w_in_selection_mode ... ok
test native::capture_pomodoro_close::selection_tests::star_entry_nested_wording_names_the_star_origin ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_accepts_an_empty_lineup_but_explicit_positive_indices_do_not ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_use_top_level_lineup_for_wildcards ... ok
test native::capture_pomodoro_close::tests::close_after_the_start_still_shortens_by_whole_units ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_outcomes_cover_remaining_numbered_links_and_keep_exceptions ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_positional_logs_wait_for_and_use_top_level_worked_lineup ... ok
test native::capture_pomodoro_close::tests::close_before_the_start_clamps_to_a_zero_length_session ... ok
test native::capture_pomodoro_close::tests::bare_close_stamps_the_legacy_off_clock_duration ... ok
test native::capture_pomodoro_close::tests::close_names::a_reused_later_entry_is_never_renamed_and_sheds_nothing ... ok
test native::capture_pomodoro_close::tests::close_names::narrowed_closed_line_and_shed_placeholder ... ok
test native::capture_pomodoro_close::tests::conflicting_close_keeps_worked_key_and_drops_off_clock_key ... ok
test native::capture_pomodoro_close::tests::close_names::without_names_both_sessions_keep_the_running_name ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::tests::keyed_off_clock_close_preserves_the_recorded_minutes ... ok
test native::capture_complete::tests::relations::relation_target_contexts_use_directional_markers_and_owner_links ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::an_open_placeholder_above_is_never_an_anchor ... ok
test native::capture_complete::tests::output::close_bullet_lines_suppress_wikilink_block_but_keep_note ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_follows_nested_children_and_interior_blanks ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_lands_before_a_hand_ordered_completed_entry ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::meet_close_carrying_a_link_moves_the_continuation_last ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::no_open_entry_below_keeps_todays_slot ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::deferred_and_dropped_lines_keep_the_reported_line_right ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::non_meet_close_keeps_todays_slot ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_last_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_link_tasks::tests::pulls_forward_only_for_a_single_future_scheduled_field ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_link_tasks::tests::suggestions_avoid_used_ids_including_non_task_anchors ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_link_tasks::tests::worked_example_lists_eight_rows_in_canonical_order ... ok
test native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_link_tasks::tests::ranker_matches_the_worked_example_queries ... ok
test native::capture_complete::tests::output::bare_edge_hash_requests_task_type_completion ... ok
test native::capture_link_tasks::tests::warns_when_the_day_file_is_missing_but_lists_tasks ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_link_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture::note_pull::tests::np4_struck_or_closed_links_stay_offered ... ok
test native::capture::project_note::tests::offer_subset_keys_and_mint_collisions ... ok
test native::capture_pomodoro_start::drop_tests::created_session_reports_the_new_session_variant ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_pomodoro_start::drop_tests::dropped_last_line_without_final_newline_leaves_none ... ok
test native::capture_pomodoro_start::drop_tests::dropped_middle_line_without_final_newline_keeps_structure ... ok
test native::capture_pomodoro_start::drop_tests::drops_nested_links_with_their_parent ... ok
test native::capture_pomodoro_start::drop_tests::drops_embedded_and_unresolved_rows_by_number ... ok
test native::capture_complete::tests::output::trailing_hash_fragment_requests_task_type_completion ... ok
test native::capture_pomodoro_start::drop_tests::empty_lineup_suggests_the_token_without_its_drop ... ok
test native::capture_pomodoro_start::drop_tests::duplicate_still_queued_warns ... ok
test native::capture_pomodoro_start::drop_tests::preserves_crlf ... ok
test native::capture_pomodoro_start::drop_tests::out_of_range_names_every_bad_number ... ok
test native::capture_pomodoro_start::drop_tests::three_bad_numbers_join_with_commas ... ok
test native::capture_pomodoro_start::drop_tests::empty_drop_is_byte_identical ... ok
test native::capture_pomodoro_start::lineup_tests::managed_dependency_lines_are_not_start_lineup_items ... ok
test native::capture_pomodoro_start::lineup_tests::lists_direct_children_in_ledger_order ... ok
test native::capture_pomodoro_start::drop_tests::drops_numbered_subtree_and_keeps_gaps ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_preserves_crlf_line_numbers ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_matches_wrapper_across_sessions ... ok
test native::capture_pomodoro_start::drop_tests::fenced_lines_are_not_numbered ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_pomodoro_start::lineup_tests::skips_deeper_descendants_embeds_and_struck_lines ... ok
test native::capture_pomodoro_start::lineup_tests::resolves_rows_through_the_staged_view ... ok
test native::capture_complete::tests::output::bare_start_name_completion_prefixes_hash_for_digit_led_matches ... ok
test native::capture_pomodoros::tests::completed_summary_prefers_recorded_duration ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoro_start::lineup_tests::skips_fenced_lines ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture::note_pull::tests::batch_duplicate_idless_second_row_selects_alone ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_pomodoros_agenda::tests::agenda_location_reads_title_then_maps_url ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_pomodoros_agenda::tests::logs_tag_subtrees_and_prose_is_untagged ... ok
test native::capture_complete::tests::output::override_running_carries_homes_only_for_unnamed_sessions ... ok
test native::capture_language::tests::template::both_template_bounds_are_checked_without_truncation ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_pomodoro_close::linked_task_tests::closing_a_dependent_leaves_depends_on_prerequisites_open ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::caret_task_keeps_its_authored_checkbox ... ok
test native::capture_project_note::tests::configured_cancelled_status_stays_closed_in_project_note ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::named_all_caps_bullet_with_children_stays_a_task ... ok
test native::capture_project_note::tests::named_task_keeps_an_existing_created_stamp_before_the_id ... ok
test native::capture_project_note::tests::named_tasks_render_ids_last_with_next_status_for_links ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::prj_task_is_never_linked ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::scheduled_date_lands_inline_on_prj_with_a_blocked_checkbox ... ok
test native::capture_project_note::tests::scheduled_project_renders_linked_tasks_as_blocked ... ok
test native::capture_project_note::tests::section_title_shape_rejects_mixed_case_and_banners ... ok
test native::capture_project_note::tests::task_rows_cover_unnamed_hidden_closed_and_placeholder ... ok
test native::capture_project_note::tests::task_rows_keep_source_identity_when_tasks_section_merges_after ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_project_note::tests::unconfigured_status_stays_authored_in_scheduled_project_note ... ok
test native::capture_pomodoros_agenda::tests::task_block_lines_have_clean_text_kinds_and_depths ... ok
test native::capture_pomodoro_close::linked_task_tests::mentioned_first_bare_link_gets_number_and_blocked_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::custom_in_progress_symbol_gets_no_listed_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::listed_duplicate_embedded_and_plain_warns_once_for_not_completed ... ok
test native::capture_pomodoro_close::linked_task_tests::same_task_numbered_twice_carries_lowest_number ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_related::tests::cosine_is_symmetric_on_identical_titles ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_listed_row_warns_exactly_once ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_typed_target_warns_and_stays_in_pomodoro ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_related::tests::same_title_normalization_strips_punctuation_and_tags ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_nest_undated_in_task_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_lands_in_task_work_log_as_typed_subset ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_complete_writes_done_task_with_completion_date ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_align_with_typed_entries ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_on_complete_target_land_in_completed_task ... ok
test native::capture_related::tests::ordering_prefers_band_then_open_then_status ... ok
test native::capture_pomodoros_agenda::tests::unreadable_notes_fail_soft ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_stamped_work_logs ... ok
test native::capture_related::tests::tokenizer_records_display_spans ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_related::tests::tokenizer_table_covers_bob_aware_cases ... ok
test native::capture_related::tests::stopwords_stay_sorted_for_binary_search ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_rewrite::tests::json_does_not_search_for_a_separator_toggle_without_a_cursor ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_rewrite::tests::json_reports_an_existing_task_destination_notice_without_changing_text ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_rewrite::tests::json_shape_switches_a_block_id_separator ... ok
test native::capture_rewrite::tests::json_shape_switches_a_colon_marker_to_plus ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::close_items_are_never_rewritten ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_rewrite::tests::json_shape_attaches_a_relation_label_pipe ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_after_existing_children ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_for_a_childless_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_rotten_log_only_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_work_log_only_task ... ok
test native::capture_schedule_log::tests::insertion_ignores_a_marker_nested_under_another_child ... ok
test native::capture_schedule_log::tests::insertion_prefers_the_schedule_marker_over_other_logs ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_legacy_marker ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_spaced_marker ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_tabbed_marker ... ok
test native::capture_schedule_log::tests::insertion_preserves_a_missing_final_newline ... ok
test native::capture_schedule_log::tests::insertion_preserves_crlf_endings ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_schedule_log::tests::randomize_reason_appends_the_until_base ... ok
test native::capture_schedule_log::tests::randomize_reason_keeps_a_fixed_window ... ok
test native::capture_schedule_log::tests::randomize_reason_names_the_tool_without_a_from_suffix ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x1_complete_2 ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x0_and_x1_2 ... ok
test native::capture_related::tests::numbers_that_differ_cap_duplicates_at_similar ... ok
test native::capture_task_toggle::tests::blocked_is_forced_to_next ... ok
test native::capture_task_toggle::tests::errors_on_multiple_open_timed_entries ... ok
test native::capture_task_toggle::tests::errors_when_no_eligible_open_entry ... ok
test native::capture_task_toggle::tests::errors_when_no_pomodoros_section ... ok
test native::capture_task_toggle::tests::idempotent_insertion_skips_when_already_linked ... ok
test native::capture_task_toggle::tests::implicit_insertion_falls_back_to_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::implicit_insertion_targets_single_open_timed_entry ... ok
test native::capture_task_toggle::tests::insertion_ignores_struck_history_and_adds_a_live_link ... ok
test native::capture_task_toggle::tests::insertion_removes_duplicate_from_later_open_entry ... ok
test native::capture_task_toggle::tests::invalid_pomodoro_name_is_rejected ... ok
test native::capture_task_toggle::tests::ledger_entry_completed_ref_is_pomodoro_closed ... ok
test native::capture_pomodoros_agenda::tests::nested_log_markers_keep_their_own_kind ... ok
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_multiline_source ... ok
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_source ... ok
test native::capture_pomodoros_agenda::tests::overnight_ranges_roll_the_end_date ... ok
test native::capture_task_toggle::tests::ledger_entry_stale_ref_is_stale_pomodoro ... ok
test native::capture_task_toggle::tests::ledger_entry_moves_q_to_the_named_ref ... ok
test native::capture_pomodoros_agenda::tests::pomodoro_markers_and_prose_mix_with_links ... ok
test native::capture_related::tests::scorer_pairs_from_research ... ok
test native::capture_pomodoros_agenda::tests::relation_lines_are_not_agenda_task_links ... ok
test native::capture_pomodoros::tests::task_link_count_reports_ten_or_more_links ... ok
test native::capture_task_toggle::tests::ledger_exact_name_reuses_a_whole_slug_open_entry ... ok
test native::capture_task_toggle::tests::ledger_exact_name_creates_when_only_a_prefix_matches ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_parse::tests::incomplete_type_markers_attach_no_theme_ref ... ok
test native::capture::note_pull::tests::np16_inbox_ready_pick_routes_next_pick_does_not ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_pomodoros_agenda::tests::open_entries_can_link_done_tasks ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_pomodoros_agenda::tests::crlf_and_missing_final_newline_resolve ... ok
test native::capture_pomodoros_agenda::tests::resolved_items_carry_ledger_notes ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_pomodoros_agenda::tests::resolutions_cover_every_failure_mode ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_pomodoros_agenda::tests::long_task_blocks_truncate_at_150_lines ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_task_toggle::tests::typed_selection_creates_a_placeholder_past_the_ledger ... ok
test native::capture_task_toggle::tests::typed_selection_creates_past_the_old_cap ... ok
test native::capture_task_toggle::tests::typed_relocation_moves_the_queue_to_the_placed_entry ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_task_toggle::tests::typed_selection_prefers_the_running_exact_entry ... ok
test native::capture_task_toggle::tests::removal_preserves_struck_links_and_removes_only_live_occurrences ... ok
test native::capture_task_toggle::tests::typed_insertion_creates_one_shared_placeholder ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_task_toggle::tests::typed_selection_keeps_timed_ambiguity_without_an_exact_match ... ok
test native::capture_task_wikilinks::tests::inside_wikilink_is_protected ... ok
test native::capture_task_wikilinks::tests::at_sigil_in_query_stays_wikilink_task ... ok
test native::capture_task_wikilinks::tests::triple_paren_never_triggers ... ok
test native::capture_task_wikilinks::tests::mid_word_caret_does_not_swallow_following_text ... ok
test native::capture_task_wikilinks::tests::opener_at_line_start ... ok
test native::capture_task_wikilinks::tests::crlf_draft_keeps_byte_offsets ... ok
test native::capture_task_wikilinks::tests::mid_word_never_triggers ... ok
test native::capture_task_wikilinks::tests::closed_token_covers_closer ... ok
test native::capture_task_wikilinks::tests::forbidden_query_chars_reject_the_field ... ok
test native::capture_task_wikilinks::tests::multibyte_prefix_uses_byte_offsets ... ok
test native::capture_task_wikilinks::tests::whole_item_actions_request_no_field ... ok
test native::capture_task_wikilinks::tests::opener_after_space ... ok
test native::capture_task_wikilinks::tests::work_log_child_is_not_a_field ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_templates::command::tests::relative_time_uses_the_bob_clock_value ... ok
test native::capture_templates::command::tests::selectors_use_one_or_two_digits_for_one_based_indices ... ok
test native::capture_task_wikilinks::tests::closed_token_covers_caret_through_end_of_closer ... ok
test native::capture_templates::store::tests::a_draft_without_the_directive_has_no_canonical_text ... ok
test native::capture_templates::store::tests::canonical_text_strips_trailing_space_and_keeps_layout ... ok
test native::capture_task_wikilinks::tests::unclosed_token_stops_before_punctuation_and_preserves_suffix ... ok
test native::capture_templates::store::tests::canonical_text_handles_crlf_unicode_escapes_and_header_gap ... ok
test native::capture_templates::store::tests::origin_validation_accepts_only_short_alphanumerics ... ok
test native::capture_templates::store::tests::one_row_and_many_rows_save_the_same_entry ... ok
test native::capture_templates::store::tests::template_ids_are_stable_and_content_addressed ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_templates::store::tests::the_directive_never_changes_the_content_id ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_work_log::tests::creates_work_log_after_rotten_log_and_leaves_rotten_untouched ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::capture_work_log::tests::work_log_stamp_uses_iso_minute_precision ... ok
test native::capture_pomodoros_agenda::tests::current_numbers_match_number_task_links_walk ... ok
test native::capture_pomodoros_agenda::tests::each_note_reads_once_per_filter_mode ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::capture_parse::tests::task_type_spans_carry_one_ref_over_the_name_content ... ok
test native::capture_pomodoros_agenda::tests::roles_numbers_and_retired_counts ... ok
test native::capture_pomodoros_agenda::tests::rotten_log_markers_serialize_as_rotten ... ok
test native::capture_pomodoros_agenda::tests::september_shaped_vault_finishes_fast ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_targets::tests::scan_warns_on_shadowed_alias ... ok
test native::capture_targets::tests::scan_reads_aliases_and_warns_on_conflicts ... ok
test native::capture_link_tasks::tests::excludes_closed_unknown_terminal_untyped_and_unroutable ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_in_progress_and_complete_updates_both_tasks ... ok
test native::capture_pomodoro_close::selection_tests::full_close_reports_numbered_lineup_with_none ... ok
test native::capture_related::tests::excludes_gtd_checklist_and_closed_recurring_rows ... ok
test native::capture_pomodoro_close::selection_tests::listed_blocked_and_done_warnings ... ok
test native::capture_related::tests::band_edges_and_short_query_rules ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x2 ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_on_complete_target_lands_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x_complete ... ok
test native::capture_related::tests::closed_window_includes_30_days_and_excludes_31 ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::capture_templates::store::tests::newer_schema_refuses_writes_and_keeps_bytes ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::capture_pomodoros::tests::tasks_human_output_has_agenda_rows ... ok
test native::capture_pomodoros::tests::tasks_json_includes_derived_homes ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_parse::tests::theme_name_spans_report_components_with_source_offsets ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_with_multiple_open_timed_entries ... ok
test native::capture_related::tests::archive_closed_window_respects_mtime ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::capture_pomodoros::tests::task_link_count_numbers_only_numbered_links ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_for_completed_entries ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_without_a_current_session ... ok
test native::capture::note_pull::tests::np14_numeric_key_and_out_of_range_picks ... ok
test native::capture_complete::tests::output::named_start_completion_omits_context_without_a_single_runner ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... ok
test native::capture_task_wikilinks::tests::task_spans_cover_exactly_the_completion_fields ... ok
test native::capture_task_wikilinks::vectors_tests::vectors_match_candidates_and_link_targets ... ok
test native::capture_templates::store::tests::lock_timeout_reports_busy ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::capture_templates::store::tests::shelf_files_use_restricted_permissions ... ok
test native::capture_templates::store::tests::unknown_fields_survive_a_rewrite ... ok
test native::capture_templates::store::tests::origin_replace_keeps_unknown_fields ... ok
test native::capture_templates::store::tests::corrupt_file_is_quarantined_on_write ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::capture_complete::tests::output::named_start_completion_carries_keeps_ledger_and_running ... ok
test native::capture::tests::template::planning_each_template_matches_planning_its_expansion ... ok
test native::capture_templates::store::tests::origin_replace_swaps_in_one_write_and_keeps_history ... ok
test native::capture_templates::store::tests::repeated_captures_dedupe_and_bump ... ok
test native::capture_templates::store::tests::eviction_drops_least_recently_used_and_lowered_cap_trims ... ok
test native::capture_templates::store::tests::origin_cases_cover_same_missing_and_existing_target ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::capture_related::tests::synthetic_vault_query_is_under_250ms ... ok
test native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms ... ok

test result: ok. 1482 passed; 0 failed; 1 ignored; 0 measured; 3281 filtered out; finished in 1.73s

  Installing bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26)
    Updating crates.io index
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
   Compiling typenum v1.20.1
   Compiling version_check v0.9.5
   Compiling stable_deref_trait v1.2.1
   Compiling cfg-if v1.0.4
   Compiling autocfg v1.5.1
   Compiling memchr v2.8.1
   Compiling litemap v0.8.3
   Compiling writeable v0.6.4
   Compiling foldhash v0.2.0
   Compiling find-msvc-tools v0.1.9
   Compiling crc32fast v1.5.0
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
   Compiling utf8_iter v1.0.4
   Compiling equivalent v1.0.2
   Compiling libc v0.2.186
   Compiling allocator-api2 v0.2.21
   Compiling shlex v2.0.1
   Compiling simd-adler32 v0.3.9
   Compiling serde_core v1.0.228
   Compiling adler2 v2.0.1
   Compiling utf8parse v0.2.2
   Compiling colorchoice v1.0.5
   Compiling anstyle-query v1.1.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling anstyle v1.0.14
   Compiling smallvec v1.15.2
   Compiling getrandom v0.4.2
   Compiling tinyvec_macros v0.1.1
   Compiling rand_core v0.10.1
   Compiling cpufeatures v0.3.0
   Compiling bitflags v2.12.1
   Compiling strsim v0.11.1
   Compiling serde v1.0.228
   Compiling siphasher v1.0.4
   Compiling weezl v0.1.12
   Compiling zmij v1.0.21
   Compiling cpufeatures v0.2.17
   Compiling clap_lex v1.1.0
   Compiling thiserror v2.0.18
   Compiling itoa v1.0.18
   Compiling const-oid v0.10.2
   Compiling quick-error v2.0.1
   Compiling regex-syntax v0.8.10
   Compiling iana-time-zone v0.1.65
   Compiling unicode-properties v0.1.4
   Compiling zune-core v0.5.3
   Compiling percent-encoding v2.3.2
   Compiling pxfm v0.1.30
   Compiling chrono-tz v0.10.4
   Compiling unicode-bidi v0.3.18
   Compiling serde_json v1.0.150
   Compiling color_quant v1.1.0
   Compiling byteorder-lite v0.1.0
   Compiling bytecount v0.6.9
   Compiling ttf-parser v0.25.1
   Compiling is_executable v1.0.6
   Compiling rangemap v1.7.1
   Compiling bytemuck v1.25.2
   Compiling ryu v1.0.23
   Compiling unsafe-libyaml v0.2.11
   Compiling log v0.4.30
   Compiling encoding_rs v0.8.35
   Compiling tinyvec v1.11.0
   Compiling hex v0.4.3
   Compiling similar v2.7.0
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26/crates/bob-obsidian-assets)
   Compiling fdeflate v0.3.7
   Compiling anstyle-parse v1.0.0
   Compiling miniz_oxide v0.8.9
   Compiling form_urlencoded v1.2.2
   Compiling cc v1.2.63
   Compiling phf_shared v0.12.1
   Compiling gif v0.14.2
   Compiling nom v8.0.0
   Compiling aho-corasick v1.1.4
   Compiling chacha20 v0.10.2
   Compiling image-webp v0.2.4
   Compiling zune-jpeg v0.5.15
   Compiling phf v0.12.1
   Compiling hashbrown v0.17.1
   Compiling generic-array v0.14.7
   Compiling num-traits v0.2.19
   Compiling unicode-normalization v0.1.25
   Compiling anstream v1.0.0
   Compiling hybrid-array v0.4.12
   Compiling flate2 v1.1.9
   Compiling clap_builder v4.6.7
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling rquickjs-sys v0.12.1
   Compiling stringprep v0.1.5
   Compiling block-buffer v0.12.0
   Compiling crypto-common v0.2.2
   Compiling indexmap v2.14.0
   Compiling fs2 v0.4.3
   Compiling png v0.18.1
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling rand v0.10.1
   Compiling chrono v0.4.44
   Compiling digest v0.10.7
   Compiling inout v0.1.4
   Compiling digest v0.11.3
   Compiling regex-automata v0.4.14
   Compiling cipher v0.4.4
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling sha2 v0.11.0
   Compiling ecb v0.1.2
   Compiling cbc v0.1.2
   Compiling aes v0.8.4
   Compiling moxcms v0.8.1
   Compiling thiserror-impl v2.0.18
   Compiling serde_derive v1.0.228
   Compiling synstructure v0.14.0
   Compiling clap v4.6.7
   Compiling clap_complete v4.6.11
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling nom_locate v5.0.0
   Compiling lopdf v0.40.0
   Compiling zerofrom v0.1.8
   Compiling yoke v0.8.3
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling regex v1.12.3
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_collections v2.3.0
   Compiling icu_locale_core v2.3.0
   Compiling image v0.25.10
   Compiling icu_provider v2.3.1
   Compiling icu_normalizer v2.3.0
   Compiling icu_properties v2.3.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26)
    Finished `local-install` profile [optimized] target(s) in 2m 15s
  Installing /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261103_154512/tmp.LsDNatKGcl/bin/bob
  Installing /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261103_154512/tmp.LsDNatKGcl/bin/bob_notify
  Installing /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261103_154512/tmp.LsDNatKGcl/bin/bob_pomodoro
  Installing /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261103_154512/tmp.LsDNatKGcl/bin/tmux_bob_pomodoro
   Installed package `bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_26)` (executables `bob`, `bob_notify`, `bob_pomodoro`, `tmux_bob_pomodoro`)
warning: be sure to add `/home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws0-261103_154512/tmp.LsDNatKGcl/bin` to your PATH to be able to run the installed binaries
Bob tracks a daily Pomodoro ledger inside an Obsidian vault and keeps that
vault synced through Git. Commands follow the daily workflow: capture, review
(plan, freshness, ready), stats, run Pomodoros, reconcile tasks, and nightly
maintenance. Pass `--help` to any command, or run `bob help <command>`, for
its own options.

Usage: bob <COMMAND>

Daily workflow:
  capture     Capture tasks, bullets, and Pomodoro commands into the vault
  freshness   Walk the tiered freshness review queue
  plan        Show today's plan budget, Today's tasks, and NEXT/PENDING lanes
  pomodoro    Show Pomodoro status, print the tmux line, or notify on completion
  ready       Show each area/project note's Ready lane against the per-note cap
  stats       Show derived daily metrics as a glance, detail chart, or catalog
  types       Manage task types and explain task suggestions

Tasks and projects:
  projects    List and sync project notes via their ^prj tasks
  relations   List, hide, unhide, and rename relation labels
  task        Vault-wide task maintenance: archive, move, reconcile, reroll

Vault:
  articles    Format and inspect article notes with bob-owned section numbers
  nightly     Run nightly maintenance: vault-sync, task archive, articles,
              period notes, vault-sync
  periods     Manage period notes: weeks, quarters, years, and all time
  query       Run Dataview or Tasks queries against the vault
  ref         Find, list, read, rename, and plan references for today; sync
              Highlights PDFs into them
  vault-sync  Reconcile the vault through Git (default: run) or show status

Integrations:
  gcal        Project Google Calendar events onto today's daily note
  gkeep       Drain the Google Keep inbox into Obsidian tasks

Setup:
  completion  Install and inspect shell completion for bob
  plugins     List and deploy Bob's custom Obsidian plugins

Capture protocol:
  capture-complete       Complete the capture marker at the cursor
  capture-drawers        List the ALL-CAPS child drawers of a capture task
  capture-parse          Explain what in-progress capture text currently means
  capture-pomodoro-name  Write a name onto an open unnamed Pomodoro
  capture-pomodoros      List today's Pomodoro ledger entries
  capture-related        List existing tasks that a new capture may duplicate
  capture-rewrite        Apply the capture grammar's automatic draft rewrites
  capture-sections       List the non-Tasks sections of a capture note
  capture-targets        List inbox, area, and active project capture routes
  capture-task-id        Write a block ID onto an open capture task
  capture-tasks          List the open tasks of a capture note
  capture-templates      List, save, show, and manage saved capture templates

Options:
  -h, --help
          Print help (see a summary with '-h')

  -V, --version
          Print version

Examples:
  bob capture buy milk @groceries   Capture a task into groceries.md
  bob capture '='                   Start the queued Pomodoro
  bob plan                          Show today's plan budget and lanes
  bob freshness                     List the review queue
  bob ready                         Show Ready lanes against the per-note cap
  bob stats                         Glance at derived daily metrics
  bob types                         List recently used task types
  bob task reconcile --dry-run      Preview task status reconciliation
  bob query --source '#project'     Print matching note paths
  bob vault-sync status --json      Print the last vault Git sync status

Run 'bob <command> --help' or 'bob help <command>' for more on a command.
succeeded  exit=0  duration=370116ms

