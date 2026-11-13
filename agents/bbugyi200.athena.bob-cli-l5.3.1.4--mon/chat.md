# Chat History - ace-run (bob-cli-l5.3.1.4--mon)

- **TIMESTAMP:** 2026-11-13 01:14:24 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-l5.3.1.4--mon

## Prompt

sase monitor start --command 'cargo test --test gcal_ack --test gcal_cli --test gcal_note_cli --test gcal_notes --test gcal_list --test gcal_sync --test gcal_lifecycle --test gcal_diagnostics --test gcal_auth && cargo test --lib native::gcal && just all' --reason 'Run the Google Calendar ack acceptance suites and project gate'

## Response

sase tool run a2f2637f452b26543e3e5e25fad16a9d
   Compiling bob-obsidian v0.5.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2.44s
     Running tests/gcal_ack.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_ack-6d603da56e50d5ab)

running 29 tests
test ack_help_sorts_options_and_documents_mode_boundaries ... ok
test ack_off_leaves_the_queue_empty ... ok
test ack_window_uses_contiguous_timezone_boundaries_across_dst ... ok
test list_json_has_task_and_waiting_lanes_without_writing ... ok
test non_tty_walk_refuses_but_bare_ack_lists_with_hint ... ok
test session_quit_reports_nothing_saved ... ok
test json_preview_is_redacted_and_does_not_append ... ok
test ack_selector_keeps_literal_note_query_and_scope_format_are_choices ... ok
test session_recurring_ack_defaults_to_all_events ... ok
test session_recurring_scope_eof_quits_cleanly ... ok
test session_adopt_answers_from_google_description ... ok
test session_burst_repeats_answer_only_once ... ok
test session_note_line_saves_and_answers ... ok
test session_recurring_ack_event_scope_keeps_sibling ... ok
test session_editor_failure_stays_on_card ... ok
test session_adopt_unavailable_stays_on_card ... ok
test session_editor_appends_valid_text ... ok
test session_return_is_inert_and_eof_quits ... ok
test session_empty_note_returns_to_card ... ok
test one_shot_ack_and_clear_preserve_historical_note_evidence ... ok
test session_skip_returns_next_run ... ok
test session_ack_then_quit_saves_first_answer ... ok
test session_ctrl_c_byte_exits_130_after_saving ... ok
test ack_list_surfaces_moved_receipts_that_left_the_window ... ok
test session_write_failure_keeps_earlier_answers ... ok
test session_invalid_note_offer_decline_stays ... ok
test session_timed_presses_answer_each_card ... ok
test session_invalid_note_decline_keeps_no_record ... ok
test session_help_and_open_preserve_state ... ok

test result: ok. 29 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.86s

     Running tests/gcal_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_auth-f82e170d88f9fac9)

running 65 tests
test doctor_reports_gog_missing ... ok
test doctor_keeps_the_ack_check_visible_when_config_setup_fails ... ok
test config_error_names_the_key_and_exits_2 ... ok
test login_rejects_account_without_at ... ok
test doctor_reports_too_old_gog ... ok
test logout_without_force_on_a_pipe_exits_2 ... ok
test logout_explicit_account_still_requires_confirmation ... ok
test login_downloads_q_cancels_and_junk_reprompts ... ok
test common_flags_precede_the_subcommand ... ok
test login_prints_the_guided_checklist_without_a_client ... ok
test logout_force_removes_the_grant_and_prints_revoke_url ... ok
test logout_explicit_account_is_passed_through_without_login_validation ... ok
test login_skips_keyring_held_client ... ok
test login_dash_c_rejects_web_client ... ok
test login_paste_without_tty_is_needs_tty ... ok
test calendars_prefers_the_sole_bob_account_over_multiple_gog_accounts ... ok
test login_keyring_failure_is_classified ... ok
test logout_case_insensitive_duplicate_emails_count_as_one ... ok
test doctor_reports_no_client ... ok
test doctor_maps_invalid_grant ... ok
test login_already_connected_human_transcript_includes_step_two_and_summary ... ok
test doctor_reports_not_logged_in ... ok
test doctor_maps_api_disabled_on_token_refresh ... ok
test doctor_fails_invalid_default_root ... ok
test calendars_table_and_json ... ok
test login_existing_client_is_already_connected ... ok
test gog_receives_bobs_default_and_explicit_config_roots ... ok
test login_api_disabled_without_tty_returns_project_url ... ok
test doctor_shows_the_stored_client_project ... ok
test login_check_accepts_primary_calendar_real_id ... ok
test configured_gog_is_used_and_relative_gog_is_a_config_error ... ok
test doctor_fails_missing_journal_rules ... ok
test doctor_json_healthy_setup ... ok
test login_paste_access_denied_then_q_is_cancelled ... ok
test doctor_fails_foreign_writer ... ok
test doctor_notes_lookup_errors_count_as_not_checked ... ok
test doctor_notes_ok_counts_a_live_note ... ok
test login_dash_c_replaces_existing_client ... ok
test login_retries_calendar_api_activation_on_a_tty ... ok
test login_browser_access_denied ... ok
test login_account_flag_overrides_config ... ok
test login_paste_flow_never_runs_interactive_auth_add ... ok
test login_browser_opener_spawn_fail_prints_fallback_and_accepts_callback ... ok
test login_paste_retry_exhaustion_is_stale_link ... ok
test login_paste_junk_then_good_url_reprompts ... ok
test login_human_transcript_stays_on_stderr_and_mentions_remote_writer ... ok
test login_paste_stale_state_then_fresh_link ... ok
test login_ssh_auto_selects_paste ... ok
test login_minus_m_uses_paste_remote_flow ... ok
test login_paste_denied_then_enter_retries_with_a_fresh_state ... ok
test login_dash_c_stores_the_client ... ok
test login_discovers_a_downloaded_client ... ok
test login_dash_c_accepts_legacy_flat_file ... ok
test login_guides_pasted_client_json_and_adds_json_fields ... ok
test login_self_heals_a_stale_saved_grant ... ok
test login_reuses_legacy_default_client_without_prompt ... ok
test login_browser_end_to_end ... ok
test doctor_ack_check_reports_clears_orphans_foreign_malformed_and_stale ... ok
test login_account_picker_accepts_a_number ... ok
test login_browser_denied_then_retry_succeeds ... ok
test login_suggests_config_when_bob_accounts_remain_ambiguous ... ok
test doctor_notes_combined_remedies_all_survive_and_run ... ok
test doctor_notes_orphans_not_found_cancelled_declined_and_series ... ok
test doctor_ack_lookup_errors_and_cap_are_not_reported_as_orphans ... ok
test doctor_notes_unresolved_foreign_malformed_and_cap ... ok

test result: ok. 65 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 5.36s

     Running tests/gcal_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_cli-4c5f4880e5a3a47d)

running 6 tests
test list_help_has_sorted_short_options_and_day_examples ... ok
test unknown_subcommand_exits_2 ... ok
test login_help_lists_short_aliases_in_order ... ok
test top_help_pins_the_command_surface ... ok
test logout_and_doctor_help_carry_examples ... ok
test bare_gcal_lists_today_and_exits_0 ... ok

test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.29s

     Running tests/gcal_diagnostics.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_diagnostics-d1bb2459b14f9b8f)

running 4 tests
test inherited_drop_advice_needs_a_usable_off_clock_root ... ok
test canonical_input_reports_empty_arrays ... ok
test deprecated_aliases_warn_once_per_occurrence ... ok
test sync_deprecations_survive_all_reports_without_extra_writes ... ok

test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.15s

     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_lifecycle-e7b1fdcbab13e592)

running 45 tests
test description_off_keeps_buffer_without_reason_bullets ... ok
test crash_adoption_matching_bullets_does_not_duplicate ... ok
test preexisting_off_clock_title_migrates_both_spans_in_place ... ok
test preexisting_off_clock_badge_without_calendar_link_migrates_with_buffer ... ok
test description_off_leaves_existing_bullets_alone ... ok
test emptied_meet_entry_is_removed_with_the_cancel ... ok
test context_rows_still_never_get_description_bullets ... ok
test dry_run_diff_shows_the_root_change ... ok
test malformed_description_record_is_hands_off ... ok
test unedited_root_reroutes_when_google_colour_changes ... ok
test unedited_root_reroutes_when_google_adds_a_token ... ok
test google_clearing_description_removes_the_block ... ok
test preexisting_titled_badges_migrate_in_place ... ok
test tomato_in_description_does_not_count_as_worked ... ok
test explicit_on_tag_adds_and_removes_in_place_on_untouched_rows ... ok
test declined_event_nests_cancel_log_above_tab_indented_child ... ok
test failed_lookup_writes_nothing ... ok
test yes_maybe_leaves_the_row_and_reports_once ... ok
test deleted_description_block_is_never_re_added ... ok
test maybe_yes_upgrades_the_context_row_and_links ... ok
test maybe_upgrade_gains_buffer_field ... ok
test bob_reroute_does_not_teach_the_series ... ok
test off_clock_tag_flip_on_worked_row_is_kept_once ... ok
test off_clock_tag_flip_updates_untouched_row_in_place ... ok
test pre_feature_row_backfills_on_the_next_sync ... ok
test root_reroute_keeps_buffered_google_run ... ok
test off_to_on_tag_flip_on_worked_row_is_kept_once ... ok
test plain_bullet_migrates_to_reason_bullet ... ok
test moved_event_names_the_new_day ... ok
test google_description_edit_rewrites_untouched_bullets ... ok
test list_footer_surfaces_open_past_meetings ... ok
test deleted_event_lookup_uses_the_sole_bob_account ... ok
test google_reason_edit_rewrites_untouched_block_and_keeps_edits ... ok
test edited_description_is_kept_silently_then_reported_once ... ok
test buffer_reasons_lead_the_description_block ... ok
test declined_event_cancels_untouched_task ... ok
test cancelled_external_row_loses_its_warning_tag ... ok
test worked_task_is_never_cancelled ... ok
test kept_edit_reported_once ... ok
test span_updates_rewrite_clean_spans_and_reslot ... ok
test series_edit_teaches_and_reteaches_the_root ... ok
test deleted_event_lookup_cancels_and_reports_once ... ok
test deleted_past_row_is_left_alone_and_reported_once ... ok
test doctor_reports_malformed_journal_and_last_error ... ok
test buffer_change_updates_untouched_row_in_place_and_keeps_edits ... ok

test result: ok. 45 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.51s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_list-7140ec371acc99cd)

running 15 tests
test bare_gcal_explains_how_to_connect_before_login ... ok
test all_flag_adds_omitted_events_with_their_reason ... ok
test list_uses_the_configured_account_among_multiple_bob_grants ... ok
test explicit_on_directive_is_listed_on_clock_even_with_an_off_alias ... ok
test list_uses_the_sole_bob_account_among_multiple_gog_accounts ... ok
test a_page_failure_or_remaining_token_fails_the_whole_snapshot ... ok
test list_shows_buffer_reasons_in_time_and_event_columns ... ok
test bare_gcal_lists_today_and_json_keeps_only_public_normalized_fields ... ok
test listed_clock_uses_google_root_and_via_note ... ok
test list_marks_fragile_directives_only_for_guest_tasks_with_google_bob_lines ... ok
test list_marks_moved_event_receipts_stale_in_json_and_human_output ... ok
test list_shows_waiting_for_templater_on_an_unrendered_note ... ok
test list_reads_a_replaced_section_before_any_held_sync ... ok
test list_shows_ack_states_and_counts_unacked ... ok
test list_and_sync_agree_on_love_meets_with_type_filtered_clock_defaults ... ok

test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.17s

     Running tests/gcal_note_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_note_cli-877cb2c899cbe7fa)

running 41 tests
test edit_requires_a_tty_and_hints_to_pass_text ... ok
test note_help_pins_sorted_options_and_examples ... ok
test list_json_exposes_waiting_reply_and_maybe_events ... ok
test list_orphans_and_past_hiding ... ok
test lookup_outages_are_warnings_not_orphans ... ok
test declined_and_all_day_events_are_excluded ... ok
test invalid_routes_and_empty_notes_have_ranged_errors ... ok
test edit_uses_visual_over_editor_and_drops_the_scissors_block ... ok
test adopt_edit_prefills_the_editor_with_google_lines ... ok
test explicit_separator_after_text_keeps_dash_d_as_text ... ok
test write_json_reports_waiting_reply_and_maybe_statuses ... ok
test saved_note_never_acks_owned_or_config_off_events ... ok
test matching_requires_every_word_and_ranks_exact_first ... ok
test show_hides_foreign_account_notes_with_a_warning ... ok
test saved_note_show_and_preview_share_highlight_input ... ok
test orphans_check_gone_before_past ... ok
test writer_host_applies_note_and_preview_matches_sync ... ok
test event_id_lookup_and_calendar_pin_and_ambiguous_ids ... ok
test adopt_guard_uses_the_resolved_scope ... ok
test edit_unchanged_text_appends_nothing ... ok
test edit_again_yes_reopens_and_no_saves_nothing ... ok
test series_instances_group_and_scope_is_required_off_tty ... ok
test off_writer_and_sync_failure_keep_the_saved_note ... ok
test human_write_and_clear_show_plain_preview_output ... ok
test effective_buffer_reasons_follow_occurrence_series_and_google_precedence ... ok
test series_note_immediately_syncs_each_existing_occurrence_day ... ok
test edit_series_scope_is_resolved_once_and_carried ... ok
test url_eid_decodes_and_verify_and_fallback_works ... ok
test list_json_key_names_the_mode_not_the_rows ... ok
test adopt_refuses_an_existing_note_and_nothing_to_copy ... ok
test clear_live_series_by_master_off_writer_and_lookup_failure ... ok
test edit_dry_run_leaves_journal_and_daily_note_unchanged ... ok
test adopt_copies_bare_buffers_and_says_they_live_in_bob ... ok
test edit_empty_clears_or_reports_unchanged_when_there_is_no_note ... ok
test list_and_show_round_trip_with_notes ... ok
test tty_picker_and_scope_prompt_select_recurring ... ok
test saved_note_appends_acked_only_for_new_external_review ... ok
test edit_empty_series_reports_unchanged_and_keeps_event_note ... ok
test clear_live_series_by_master_id_syncs_rendered_days ... ok
test orphan_clear_commands_remove_the_note_by_key ... ok
test preview_save_unchanged_clear_and_invalid_json ... ok

test result: ok. 41 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 3.35s

     Running tests/gcal_notes.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_notes-b65bb26a93a5a28a)

running 21 tests
test incomplete_snapshot_writes_nothing ... ok
test aliased_title_token_is_stripped_when_note_route_wins ... ok
test occurrence_beats_series_beats_google_per_field ... ok
test awaiting_reply_note_waits_applies_on_yes_and_skips_declined ... ok
test foreign_account_note_is_ignored ... ok
test locked_guest_is_born_with_note_root_buffer_and_reasons ... ok
test provenance_record_shape ... ok
test kept_description_words_note_change ... ok
test no_hold_when_nothing_is_malformed ... ok
test note_after_birth_updates_untouched_row_and_refiles_meet ... ok
test other_host_journal_applies_and_last_writer_wins ... ok
test note_prose_is_exempt_from_the_cap_and_off_hides_bullets ... ok
test force_reset_keeps_and_reapplies_notes ... ok
test clearing_a_note_restores_google_on_an_untouched_row ... ok
test two_accounts_on_one_key_keep_separate_notes ... ok
test note_does_not_move_newest_or_count_as_malformed ... ok
test list_and_sync_json_carry_no_note_text ... ok
test note_fields_omit_invalid_root_and_off_bullets ... ok
test row_edited_root_is_kept_and_reported_once ... ok
test note_follows_an_event_moved_to_another_day ... ok
test hold_on_truncated_note_line_and_clear_restores ... ok

test result: ok. 21 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.62s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/gcal_sync-7959dfda48a2df2e)

running 95 tests
test invalid_repeated_day_fails_before_any_google_call_or_write ... ok
test force_reset_respects_the_configured_writer ... ok
test invalid_last_n_days_fails_before_any_google_call ... ok
test dry_run_diff_shows_the_bullets ... ok
test last_n_days_unions_with_explicit_days_in_one_sorted_run ... ok
test missing_note_waits_with_exit_zero ... ok
test context_rows_never_get_bullets ... ok
test incomplete_snapshot_writes_nothing ... ok
test dry_run_on_an_unrendered_note_prints_the_waiting_reason ... ok
test description_off_writes_no_bullets ... ok
test future_day_gets_placeholder_and_starred_rows ... ok
test long_description_caps_at_eight_with_an_overflow_line ... ok
test past_day_gets_closed_meet_entries ... ok
test multi_day_dry_run_prints_both_diffs_without_writing ... ok
test event_spanning_midnight_keeps_existing_start_day_classification ... ok
test multi_day_json_stops_on_day_error_with_completed_reports ... ok
test descriptions_become_bullets_in_every_phase ... ok
test new_row_lands_after_the_previous_rows_bullets ... ok
test dry_run_prints_diff_and_writes_nothing ... ok
test crash_recovery_adopts_unjournaled_rows ... ok
test dry_run_diff_shows_the_stamp_line ... ok
test noncontiguous_days_fetch_separate_runs_and_skip_the_gap ... ok
test existing_open_meet_is_reused ... ok
test agenda_reads_synced_rows_cleanly ... ok
test foreign_writer_refuses_but_dry_run_previews ... ok
test meet_placeholder_follows_the_last_open_entry ... ok
test first_sync_creates_events_meet_and_links ... ok
test quiet_prints_nothing_on_success ... ok
test account_guard_refuses_a_foreign_stamp ... ok
test context_only_stamp_deletion_restores_stamp_without_hold ... ok
test last_n_days_matches_repeated_days_in_output_notes_and_journal ... ok
test list_keeps_google_root_when_vault_root_differs ... ok
test closed_meet_session_attributes_body_in_stats ... ok
test current_meeting_reconcile_then_clock_close ... ok
test deleted_row_with_overflow_bullet_is_tombstoned_not_adopted ... ok
test hostile_titles_stay_data ... ok
test last_one_day_keeps_the_single_day_json_shape ... ok
test past_day_sync_keeps_a_edited_running_meet_open ... ok
test space_indented_note_gets_space_bullets ... ok
test reconcile_keeps_linked_rows ... ok
test sync_json_rows_carry_description_lines ... ok
test past_day_sync_closes_bob_shaped_running_meet_in_place ... ok
test sync_row_json_marks_a_moved_live_event_receipt_stale ... ok
test unrendered_note_reports_json_reason_and_line ... ok
test unrendered_note_waits_and_writes_nothing ... ok
test tomorrow_stamp_uses_the_dated_form ... ok
test off_clock_aliases_split_clusters_and_report ... ok
test list_reports_task_meet_for_a_past_row ... ok
test google_span_edits_do_not_blame_the_tag ... ok
test teams_only_description_writes_nothing ... ok
test edited_root_keeps_tag_without_blaming_badges ... ok
test sync_json_reports_rows_and_pomodoro ... ok
test waiting_json_reports_a_null_stamp ... ok
test waiting_day_does_not_block_the_next_selected_day ... ok
test explicit_ack_and_hand_close_lift_the_tag ... ok
test deleted_row_and_removed_link_are_never_readded ... ok
test moved_past_event_refiles_its_bob_written_closed_meet ... ok
test deleted_stamp_is_restored_without_row_churn ... ok
test force_reset_reapplies_span_edits_and_refiles_a_removed_link ... ok
test buffered_spans_drive_meet_phases_and_clusters ... ok
test past_day_sync_keeps_unlinked_open_rows_once ... ok
test json_lists_meet_entries_and_keeps_open_entry_keys ... ok
test emptied_section_that_keeps_its_stamp_tombstones ... ok
test second_run_with_bullets_is_a_no_op ... ok
test past_day_sync_closes_a_previously_synced_placeholder_row ... ok
test rendering_the_note_lets_the_same_snapshot_write ... ok
test force_reset_reuses_a_dangling_link_without_duplicate_filing ... ok
test repeated_days_batch_fetch_and_write_in_sorted_deduped_order ... ok
test past_completed_row_stays_syncable_and_reconcile_stable ... ok
test deleting_the_row_tombstones_without_an_inferred_ack ... ok
test deleting_the_tag_files_an_inferred_ack_once ... ok
test title_update_keeps_the_description_record ... ok
test upgrade_lands_bullets_above_existing_notes ... ok
test sync_row_json_carries_ack_evidence_and_counts ... ok
test second_run_is_byte_identical_and_appends_nothing ... ok
test skipped_rows_follow_change_rows_and_json_rows_carry_detail ... ok
test sync_tags_only_open_external_task_rows ... ok
test hand_closing_a_tagged_row_lifts_the_tag_as_closed ... ok
test past_day_close_lifts_the_tag_silently ... ok
test title_free_row_is_adopted_without_duplicate ... ok
test force_dry_run_and_waiting_do_not_write ... ok
test every_left_out_event_is_named_with_its_reason ... ok
test inherited_note_clock_stamps_meets_without_materializing_tags ... ok
test tombstoning_run_json_carries_the_removed_row_detail ... ok
test list_shares_the_skip_words_and_footer ... ok
test force_reset_restores_clobbered_rows_with_old_ids_and_then_noops ... ok
test typed_tags_are_left_alone_and_config_off_removes_only_bobs ... ok
test sync_restores_missing_blank_under_events_heading ... ok
test sync_sorts_event_task_links_and_reports_sort_only_runs ... ok
test replaced_events_section_holds_until_force_reset ... ok
test missing_paragraph_gap_is_repaired_without_journal_churn ... ok
test rerun_after_a_tombstone_is_unchanged_and_names_the_skip ... ok
test pasted_back_row_is_managed_again ... ok
test buffered_rows_render_update_and_report ... ok
test stamp_refreshes_every_run_without_row_churn ... ok

test result: ok. 95 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 4.92s

   Compiling bob-obsidian v0.5.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2m 22s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261112_204543/build/debug/deps/bob_cli-6f0b1c2b1cdd9132)

running 279 tests
test native::gcal::ack::session_tests::non_terminal_fd_stays_inactive ... ok
test native::gcal::ack::session_tests::guard_restores_exact_settings_on_drop ... ok
test native::gcal::ack::session_tests::guard_restores_after_panic_unwind ... ok
test native::gcal::bullet_block::tests::empty_window_on_a_childless_row_is_directly_under_it ... ok
test native::gcal::bullet_block::tests::a_wrong_hash_is_not_the_block ... ok
test native::gcal::bullet_block::tests::empty_window_is_the_insertion_point_after_managed ... ok
test native::gcal::bullet_block::tests::depends_on_above_does_not_hide ... ok
test native::gcal::bullet_block::tests::finds_a_one_line_block ... ok
test native::gcal::bullet_block::tests::first_matching_window_wins ... ok
test native::gcal::bullet_block::tests::hash_ignores_indent_characters ... ok
test native::gcal::bullet_block::tests::insertion_skips_a_cancel_log_subtree ... ok
test native::gcal::bullet_block::tests::nested_note_hides_the_block ... ok
test native::gcal::bullet_block::tests::nested_depth_two_stays_in_the_window ... ok
test native::gcal::bullet_block::tests::replace_window_swaps_or_removes ... ok
test native::gcal::bullet_block::tests::sibling_notes_above_or_below_do_not_hide ... ok
test native::gcal::bullet_block::tests::work_log_above_or_below_does_not_hide ... ok
test native::gcal::classify::tests::local_day_windows_are_23_and_25_hours_at_dst_changes ... ok
test native::gcal::classify::tests::day_aliases_and_explicit_dates_are_local_calendar_days ... ok
test native::gcal::config::tests::ack_key_resolves_to_external_by_default_or_off ... ok
test native::gcal::config::tests::defaults_when_block_is_missing ... ok
test native::gcal::cli::tests::calendars_format_defaults_to_table ... ok
test native::gcal::config::tests::description_keys_resolve_and_reject ... ok
test native::gcal::cli::tests::login_args_pin_options ... ok
test native::gcal::cli::tests::sync_args_accept_repeated_days ... ok
test native::gcal::cli::tests::sync_args_pin_options ... ok
test native::gcal::config::tests::rejects_account_without_at ... ok
test native::gcal::cli::tests::logout_and_doctor_args ... ok
test native::gcal::description::bullets::tests::hash_and_materialization_follow_depth_and_body ... ok
test native::gcal::description::bullets::tests::markdown_destination_encoding_covers_delimiters ... ok
test native::gcal::classify::tests::fixture_covers_inclusion_rsvp_day_ownership_and_foreign_offsets ... ok
test native::gcal::classify::tests::tentative_task_setting_promotes_only_eligible_busy_events ... ok
test native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none ... FAILED
test native::gcal::description::bullets::tests::note_prose_is_exempt_from_the_cap ... ok
test native::gcal::description::tests::looks_like_html_uses_known_tags_only ... ok
test native::gcal::description::tests::debug_prints_counts_only ... ok
test native::gcal::description::tests::no_vendor_content_writes_no_keep_bullet ... ok
test native::gcal::description::tests::on_directive_is_removed_but_tagged_prose_remains_a_bullet ... ok
test native::gcal::diagnostics::tests::canonical_conflict_warns_without_deprecation_records ... ok
test native::gcal::description::tests::parse_note_uses_plain_tokenizer_and_set_flags ... ok
test native::gcal::diagnostics::tests::inherited_advice_appends_drop_parenthetical ... ok
test native::gcal::description::tests::keep_bullet_labels_by_vendor ... ok
test native::gcal::diagnostics::tests::on_wins_copy_drops_the_redundant_alias ... ok
test native::gcal::diagnostics::tests::single_alias_warns_with_write_off ... ok
test native::gcal::gog::tests::calendar_primary_matches_configured_id ... ok
test native::gcal::journal::tests::ack_stale_compares_only_live_event_instants ... ok
test native::gcal::description::tests::description_directive_vectors ... ok
test native::gcal::clock::tests::listed_clock_resolves_the_synced_meet_type ... ok
test native::gcal::clock::tests::listed_clock_inherits_through_the_chosen_root_only ... ok
test native::gcal::lifecycle::tests::cancel_log_reuses_tab_child_indent_and_lands_first ... ok
test native::gcal::journal::tests::span_hash_is_stable_and_short ... ok
test native::gcal::description::tests::boilerplate_vectors ... ok
test native::gcal::lifecycle::tests::rendered_unacked_in_a_title_cannot_collide_with_the_marker ... ok
test native::gcal::lifecycle::tests::completion_fields_stay_in_the_vault_owned_suffix ... ok
test native::gcal::lifecycle::tests::splits_task_and_context_rows ... ok
test native::gcal::journal::tests::ack_scope_is_stable_by_identity_and_note_history_survives_clear ... ok
test native::gcal::lifecycle::tests::open_meet_links_after_a_closed_entry_stay_untouched ... ok
test native::gcal::lifecycle::tests::hashes_match_the_journal_spans ... ok
test native::gcal::lifecycle::tests::timed_meet_entries_survive_cleanup ... ok
test native::gcal::journal::tests::ack_fold_is_account_guarded_and_last_writer_wins_across_hosts ... ok
test native::gcal::journal::tests::gone_after_row_stays_gone_and_a_later_tombstone_restarts ... ok
test native::gcal::lifecycle::tests::trailing_clock_badges_split_with_or_without_calendar_link ... ok
test native::gcal::lifecycle::tests::unacked_tag_add_and_strip_round_trip ... ok
test native::gcal::lifecycle::tests::cancel_creates_the_log_when_missing ... ok
test native::gcal::journal::tests::notes_fold_last_writer_wins_and_clears ... ok
test native::gcal::lifecycle::tests::unacked_tag_splits_into_the_suffix_not_the_title ... ok
test native::gcal::lifecycle::tests::untimed_meet_entries_go_when_childless ... ok
test native::gcal::journal::tests::notes_fold_per_account_so_a_foreign_note_does_not_hide_this_one ... ok
test native::gcal::login::tests::api_url_prefers_message_then_client_project ... ok
test native::gcal::link_order::tests::each_entry_sorts_independently_and_cross_midnight_uses_start ... ok
test native::gcal::journal::tests::tombstone_keeps_its_first_time_and_reason ... ok
test native::gcal::link_order::tests::link_subtrees_move_around_other_child_blocks ... ok
test native::gcal::journal::tests::row_after_gone_revives_the_occurrence ... ok
test native::gcal::link_order::tests::sorts_two_links_and_leaves_sorted_input_byte_identical ... ok
test native::gcal::description::tests::outline_vectors ... ok
test native::gcal::description::bullets::tests::bullet_vectors ... ok
test native::gcal::link_order::tests::no_event_rows_or_no_pomodoros_returns_input_unchanged ... ok
test native::gcal::link_order::tests::ties_use_end_then_event_row_order_and_duplicate_links_stay_stable ... ok
test native::gcal::link_order::tests::non_event_children_keep_their_slots ... ok
test native::gcal::link_order::tests::sorts_closed_tomato_and_struck_links_but_not_mixed_or_deeper_links ... ok
test native::gcal::link_order::tests::ignores_other_notes_unknown_ids_and_ambiguous_event_ids ... ok
test native::gcal::note::prepass_tests::attached_short_values_never_consume_the_next_token ... ok
test native::gcal::note::prepass_tests::buffer_tokens_never_parse_as_options ... ok
test native::gcal::note::prepass_tests::clear_after_query_stays_an_option ... ok
test native::gcal::note::prepass_tests::directive_text_gets_a_separator ... ok
test native::gcal::login::tests::downloads_confirm_treats_q_as_cancel_and_junk_as_unknown ... ok
test native::gcal::note::prepass_tests::explicit_separator_after_implicit_text_stops_option_extraction ... ok
test native::gcal::note::prepass_tests::explicit_separator_keeps_text_verbatim ... ok
test native::gcal::note::prepass_tests::note_tail_still_rewrites_after_sibling_fix ... ok
test native::gcal::note::prepass_tests::options_after_directives_are_still_honored ... ok
test native::gcal::login::tests::flow_names_match_json ... ok
test native::gcal::note::prepass_tests::second_separator_after_delimiter_remains_text ... ok
test native::gcal::note::prepass_tests::sign_digit_non_buffers_start_text_instead_of_erroring ... ok
test native::gcal::note::prepass_tests::valued_options_are_pulled_out_of_text_runs ... ok
test native::gcal::model::tests::google_title_clock_matching_requires_a_whole_token ... ok
test native::gcal::model::tests::external_includes_missing_organizer_and_gmail_events ... ok
test native::gcal::model::tests::event_description_debug_redacts_text ... ok
test native::gcal::model::tests::description_aliases_and_buffers_combine_only_on_directive_lines ... ok
test native::gcal::note::write::tests::canonical_display_colors_each_span_kind ... ok
test native::gcal::note::prepass_tests::separator_after_text_keeps_options_on_either_side ... ok
test native::gcal::model::tests::google_clock_conflicts_are_order_independent_and_keep_alias_evidence ... ok
test native::gcal::note::write::tests::canonical_note_size_is_limited_to_2048_bytes ... ok
test native::gcal::plan::tests::bold_span_bullet_never_moves_the_insert_slot ... ok
test native::gcal::plan::tests::adopted_unended_row_still_gets_open_meet_link ... ok
test native::gcal::plan::tests::absent_empty_description_appends_no_record ... ok
test native::gcal::plan::tests::absent_matching_window_is_adopted_without_writing ... ok
test native::gcal::model::tests::google_title_clock_tokens_strip_before_route_parsing ... ok
test native::gcal::note::write::tests::reason_spans_are_half_open_utf8_offsets ... ok
test native::gcal::plan::tests::existing_canonical_stamp_is_unchanged ... ok
test native::gcal::note::prepass_tests::ack_sibling_never_enters_note_rewrite ... ok
test native::gcal::plan::tests::existing_ended_row_gets_no_closed_entry ... ok
test native::gcal::plan::tests::bryan_edit_is_kept_silently_then_reported_once ... ok
test native::gcal::plan::tests::kept_clock_notices_cover_every_explicit_transition ... ok
test native::gcal::plan::tests::first_missing_line_tombstones_with_its_time_and_title ... ok
test native::gcal::plan::tests::every_run_refreshes_an_older_stamp ... ok
test native::gcal::note::write::tests::every_validation_error_marks_its_offending_range ... ok
test native::gcal::plan::tests::google_edit_rewrites_the_block_in_place ... ok
test native::gcal::plan::tests::hands_off_journal_is_never_rewritten ... ok
test native::gcal::plan::tests::escaped_title_is_stable_on_the_next_plan ... ok
test native::gcal::plan::tests::explicit_off_beats_a_false_note ... ok
test native::gcal::plan::tests::missing_fresh_root_never_removes_an_existing_root ... ok
test native::gcal::plan::tests::kept_title_edit_still_reroutes ... ok
test native::gcal::plan::tests::missing_root_gains_one ... ok
test native::gcal::plan::tests::mixed_current_events_stamp_worked ... ok
test native::gcal::note::write::tests::normalization_shared_vectors ... ok
test native::gcal::plan::tests::abby_inherits_love_and_invalid_nearer_value_stays_worked ... ok
test native::gcal::plan::tests::inherited_untagged_row_never_reports_kept_off_clock ... ok
test native::gcal::plan::tests::canonical_stamp_directly_above_prose_gains_one_separator ... ok
test native::gcal::plan::tests::gap_only_repair_changes_contents_without_records ... ok
test native::gcal::plan::tests::future_stamp_is_rewritten ... ok
test native::gcal::plan::tests::closed_entry_lands_between_completed_sessions ... ok
test native::gcal::plan::tests::context_rows_record_absent_and_write_no_bullets ... ok
test native::gcal::plan::tests::crash_adoption_of_empty_render_is_tracked ... ok
test native::gcal::plan::tests::crash_adoption_without_matching_window_is_hands_off ... ok
test native::gcal::plan::tests::colour_calendar_and_default_reroute_unedited_roots ... ok
test native::gcal::plan::tests::crash_adoption_records_matching_bullets_without_writing ... ok
test native::gcal::plan::tests::cross_midnight_past_meeting_wraps_end ... ok
test native::gcal::journal::tests::malformed_ack_receipts_are_counted_and_warn_with_the_existing_budget ... ok
test native::gcal::plan::tests::context_upgrade_resolves_the_upgraded_line ... ok
test native::gcal::plan::tests::current_during_running_work_uses_placeholder_and_warns ... ok
test native::gcal::plan::tests::current_meeting_creates_or_reuses_running_meet ... ok
test native::gcal::plan::tests::depends_on_above_the_block_does_not_hide_it ... ok
test native::gcal::plan::tests::deleted_block_is_never_re_added ... ok
test native::gcal::plan::tests::edited_misplaced_and_duplicated_stamps_normalize ... ok
test native::gcal::plan::tests::done_row_still_reroutes ... ok
test native::gcal::plan::tests::handwritten_section_gains_a_stamp ... ok
test native::gcal::plan::tests::empty_bullet_block_tracks_zero_lines_and_stays_put ... ok
test native::gcal::plan::tests::google_clearing_the_description_removes_the_block ... ok
test native::gcal::plan::tests::edited_root_is_kept_and_reported_once ... ok
test native::gcal::plan::tests::nested_note_hands_the_block_to_bryan ... ok
test native::gcal::plan::tests::moved_future_meeting_keeps_its_planned_link ... ok
test native::gcal::plan::tests::nested_google_list_rewrites_in_place ... ok
test native::gcal::plan::tests::existing_type_survives_a_reroute ... ok
test native::gcal::plan::tests::edited_root_still_gets_a_time_update ... ok
test native::gcal::plan::tests::moved_meeting_under_a_running_entry_is_left_silently ... ok
test native::gcal::plan::tests::earlier_row_joins_a_well_formed_list_below_its_gap ... ok
test native::gcal::plan::tests::pomodoro_entry_line_shifts_when_stamp_is_inserted ... ok
test native::gcal::plan::tests::stamp_above_a_paragraph_gets_a_blank_line ... ok
test native::gcal::plan::tests::moved_bob_closed_meeting_to_future_reopens_the_row ... ok
test native::gcal::plan::tests::pasted_back_row_with_its_link_adopts_the_link_too ... ok
test native::gcal::plan::tests::new_earliest_row_lands_below_the_stamp ... ok
test native::gcal::plan::tests::stamp_blank_before_list_is_preserved_on_refresh ... ok
test native::gcal::plan::tests::stamp_only_refresh_leaves_meet_lines_below_events_unmoved ... ok
test native::gcal::plan::tests::sibling_notes_and_work_log_do_not_hide_the_block ... ok
test native::gcal::plan::tests::new_section_plan_is_idempotent ... ok
test native::gcal::plan::tests::stamp_separator_is_reused_across_forced_refreshes ... ok
test native::gcal::plan::tests::series_memory_never_rewrites_an_existing_root ... ok
test native::gcal::journal::tests::oversized_or_unknown_scope_note_is_malformed ... ok
test native::gcal::plan::tests::tombstoned_row_pasted_back_is_adopted_again ... ok
test native::gcal::plan::tests::title_and_description_change_share_one_updated_row ... ok
test native::gcal::plan::tests::replan_uses_changed_daily_note_bytes ... ok
test native::gcal::plan::tests::new_section_has_gap_below_heading_only ... ok
test native::gcal::plan::tests::unparseable_row_keeps_its_bullets_and_record ... ok
test native::gcal::plan::tests::no_section_and_no_events_gains_nothing ... ok
test native::gcal::plan::tests::moved_past_meeting_refiles_with_its_inherited_off_clock ... ok
test native::gcal::plan::tests::unedited_root_reroute_skips_type_when_not_needed ... ok
test native::gcal::plan::tests::trimmed_closed_meet_survives_later_sync ... ok
test native::gcal::plan::tests::untouched_mid_line_title_tags_rewrite_once ... ok
test native::gcal::plan::tests::unedited_root_reroutes_to_token_and_adds_meet_type ... ok
test native::gcal::plan::tests::unedited_root_reroutes_to_note_like_token ... ok
test native::gcal::plan::tests::new_earlier_event_sorts_before_a_previously_journaled_link ... ok
test native::gcal::plan::tests::new_task_row_carries_its_bullets_and_tracks_them ... ok
test native::gcal::plan::tests::moved_past_meeting_refiles_bob_closed_meet ... ok
test native::gcal::plan::tests::root_reroute_is_idempotent ... ok
test native::gcal::plan::tests::moved_member_splits_a_bob_closed_cluster_and_refiles_every_link ... ok
test native::gcal::plan::tests::replanning_output_with_journal_is_idempotent ... ok
test native::gcal::plan::tests::off_mode_leaves_existing_bullets_and_carries_the_record ... ok
test native::gcal::plan::tests::sort_only_plan_refreshes_stamp_and_is_idempotent ... ok
test native::gcal::plan::tests::past_clusters_touching_meetings_and_splits_on_a_gap ... ok
test native::gcal::plan::tests::one_open_never_leaves_two_open_meets ... ok
test native::gcal::plan::tests::tombstoned_row_with_a_missing_line_is_never_tombstoned_again ... ok
test native::gcal::plan::tests::stamp_below_pomodoros_does_not_shift_meet_line ... ok
test native::gcal::render::tests::badge_urls_encode_ascii_whitespace_and_controls ... ok
test native::gcal::render::tests::badges_render_title_free ... ok
test native::gcal::render::tests::buffer_sides_render_only_when_set ... ok
test native::gcal::plan::tests::overflow_url_bullet_is_never_adopted_as_a_row ... ok
test native::gcal::render::tests::context_row_qualifiers_and_badges ... ok
test native::gcal::render::tests::hostile_join_and_maps_locations_stay_on_one_row ... ok
test native::gcal::plan::tests::time_change_reslots_the_row_with_its_bullets ... ok
test native::gcal::render::tests::badge_urls_and_maps_links_are_encoded ... ok
test native::gcal::plan::tests::on_tag_keeps_a_love_event_worked ... ok
test native::gcal::render::tests::off_clock_task_rows_render_the_canonical_tag_before_root ... ok
test native::gcal::render::tests::hostile_titles_stay_data ... ok
test native::gcal::render::tests::row_metadata_inserts_root_before_completion_suffix ... ok
test native::gcal::render::tests::on_and_conflicting_tags_render_as_canonical_on ... ok
test native::gcal::journal::tests::unacked_row_flag_round_trips_and_defaults_to_false ... ok
test native::gcal::plan::tests::past_and_future_share_closed_then_placeholder ... ok
test native::gcal::render::tests::row_metadata_reroute_keeps_the_google_run_intact ... ok
test native::gcal::plan::tests::untagged_love_event_creates_an_off_clock_cluster_without_a_tag ... ok
test native::gcal::render::tests::task_row_field_order_and_status ... ok
test native::gcal::replaced::tests::a_missing_events_section_holds_even_for_url_less_context_rows ... ok
test native::gcal::journal::tests::notes_do_not_move_newest_or_count_as_malformed ... ok
test native::gcal::plan::tests::update_carries_the_description_record_forward ... ok
test native::gcal::plan::tests::pre_feature_row_backfills_once ... ok
test native::gcal::plan::tests::upgraded_ended_maybe_gets_closed_meet ... ok
test native::gcal::plan::tests::vault_edited_root_controls_the_filed_clock ... ok
test native::gcal::journal::tests::ack_status_reports_receipts_notes_and_unacked ... ok
test native::gcal::description::bullets::tests::oversize_input_keeps_reasons_above_the_fallback ... ok
test native::gcal::plan::tests::edited_closed_meet_is_kept_and_reported_once_when_google_moves_it ... ok
test native::gcal::snapshot::tests::timed_window_overlap_uses_strict_boundaries ... ok
test native::gcal::render::tests::buffered_row_renders_buffer_between_badges_and_root ... ok
test native::gcal::stamp::tests::account_guard_ignores_malformed_and_matching_stamps ... ok
test native::gcal::replaced::tests::a_task_present_by_url_with_a_changed_block_id_is_not_replaced ... ok
test native::gcal::stamp::tests::account_guard_refuses_a_different_account ... ok
test native::gcal::stamp::tests::malformed_recognized_line_does_not_parse ... ok
test native::gcal::replaced::tests::a_task_still_present_by_block_id_is_not_replaced ... ok
test native::gcal::replaced::tests::an_emptied_section_that_keeps_its_stamp_is_not_replaced ... ok
test native::gcal::replaced::tests::context_rows_still_present_by_url_with_the_stamp_deleted_are_not_replaced ... ok
test native::gcal::stamp::tests::misplaced_stamp_is_due ... ok
test native::gcal::stamp::tests::missing_duplicate_future_and_edit_are_due ... ok
test native::gcal::replaced::tests::every_row_gone_and_the_stamp_gone_is_replaced ... ok
test native::gcal::replaced::tests::no_journaled_rows_for_the_day_is_not_replaced ... ok
test native::gcal::stamp::tests::older_stamp_is_due ... ok
test native::gcal::stamp::tests::other_day_round_trip ... ok
test native::gcal::stamp::tests::same_day_round_trip ... ok
test native::gcal::replaced::tests::only_gone_rows_are_not_replaced ... ok
test native::gcal::stamp::tests::truncate_drops_seconds ... ok
test native::gcal::replaced::tests::rows_from_another_day_are_ignored ... ok
test native::gcal::plan::tests::upgrade_lands_bullets_above_existing_notes ... ok
test native::gcal::stamp::tests::underscore_emphasis_is_recognized ... ok
test native::gcal::replaced::tests::url_less_context_rows_with_the_stamp_deleted_are_not_replaced ... ok
test native::gcal::sync::resolve_days_tests::last_n_days_expands_and_unions_with_explicit_days ... ok
test native::gcal::sync::waiting_tests::locked_reread_guard_refuses_a_replaced_note ... ok
test native::gcal::sync::waiting_tests::missing_note_has_its_own_code ... ok
test native::gcal::sync::waiting_tests::rendered_note_with_pomodoros_is_ready ... ok
test native::gcal::sync::waiting_tests::rendered_note_without_pomodoros_waits_for_the_section ... ok
test native::gcal::root::tests::accepts_an_area_that_is_its_own_root ... ok
test native::gcal::root::tests::rejects_invalid_and_missing ... ok
test native::gcal::root::tests::invalid_color_falls_back_to_calendar_and_invalid_default_has_no_root ... ok
test native::gcal::root::tests::route_token_precedes_color_calendar_and_default ... ok
test native::gcal::description::bullets::tests::oversize_input_uses_one_calendar_fallback ... ok
test native::gcal::skip::tests::hint_renders_the_command_cyan_only_with_color ... ok
test native::gcal::skip::tests::lifecycle_tombstones_keep_googles_reason_text ... ok
test native::gcal::root::tests::note_route_strips_aliased_title_token ... ok
test native::gcal::journal::tests::row_link_gone_fold_in_writer_order ... ok
test native::gcal::root::tests::note_route_precedes_token_and_strips_title_route ... ok
test native::gcal::root::tests::unknown_title_route_stays_in_title_and_color_wins_next ... ok
test native::gcal::skip::tests::classifier_strings_without_a_dedicated_code_keep_their_words ... ok
test native::gcal::skip::tests::omissions_map_to_stable_codes_and_friendly_detail ... ok
test native::gcal::skip::tests::undated_removal_drops_the_time ... ok
test native::gcal::skip::tests::your_deletion_reads_with_its_time_and_the_restore_command ... ok
test native::gcal::snapshot::tests::all_day_window_uses_an_exclusive_end_date ... ok
test native::gcal::ui::tests::hue_dot_stays_plain_without_color ... ok
test native::gcal::ui::tests::type_swatch_uses_name_without_color ... ok
test native::gcal::replaced::tests::a_missing_events_section_is_replaced ... ok
test native::gcal::stamp::tests::recognize_skips_list_rows_fences_and_outside_events ... ok
test native::gcal::stamp::tests::escaped_account_round_trips ... ok
test native::gcal::sync::resolve_days_tests::invalid_last_n_days_has_structured_setup_error_and_hint ... ok
test native::gcal::tests::error_exit_codes ... ok
test native::gcal::sync::waiting_tests::unrendered_check_precedes_the_pomodoros_check ... ok
test native::gcal::ui::tests::glyphs_are_status_marks ... ok
test native::gcal::skip::tests::outside_day_names_the_owning_note_for_timed_events_only ... ok
test native::gcal::journal::tests::append_ack_round_trips_and_ack_survives_reset ... ok
test native::gcal::skip::tests::skipped_row_marks_actionable_skips_apart_from_by_design_ones ... ok
test native::gcal::render::tests::mid_line_title_hazards_stay_data ... ok
test native::gcal::render::tests::calendar_badges_never_parse_as_due_dates ... ok
test native::gcal::description::tests::oversized_flag_does_not_stop_parse ... ok
test native::gcal::description::bullets::tests::hostile_bullets_are_isolated_from_bob_scanners ... ok
test native::gcal::journal::tests::reset_clears_only_its_day_and_later_records_survive ... ok
test native::gcal::ack::session_tests::drain_drops_a_burst_but_keeps_timed_presses ... ok

failures:

---- native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none stdout ----

thread 'native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none' (480580) panicked at src/native/gcal/cli.rs:1032:9:
assertion `left == right` failed
  left: ["tomorrow"]
 right: ["today", "tomorrow"]


failures:
    native::gcal::cli::tests::sync_args_read_last_n_days_aliases_and_default_to_none

test result: FAILED. 278 passed; 1 failed; 0 ignored; 0 measured; 6588 filtered out; finished in 0.40s

error: test failed, to rerun pass `--lib`
failed  exit=101  duration=169832ms

