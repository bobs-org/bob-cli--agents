# Chat History - ace-run (17z--mon-1)

- **TIMESTAMP:** 2026-11-04 11:58:24 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 17z--mon-1

## Prompt

sase monitor start --command 'cargo test gcal && cargo test --test gcal_sync --test gcal_lifecycle --test gcal_list && just lint && just docs-check' --reason 'Run the approved gcal verification after correcting the regression assertion'

## Response

sase tool run d215061572c0c0dcc4fdc79300302f08
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling typenum v1.20.1
   Compiling version_check v0.9.5
   Compiling cfg-if v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling memchr v2.8.1
   Compiling foldhash v0.2.0
   Compiling autocfg v1.5.1
   Compiling writeable v0.6.4
   Compiling libc v0.2.186
   Compiling litemap v0.8.3
   Compiling simd-adler32 v0.3.9
   Compiling crc32fast v1.5.0
   Compiling icu_normalizer_data v2.3.0
   Compiling bitflags v2.12.1
   Compiling icu_properties_data v2.3.0
   Compiling utf8_iter v1.0.4
   Compiling serde_core v1.0.228
   Compiling rand_core v0.10.1
   Compiling smallvec v1.15.2
   Compiling getrandom v0.4.2
   Compiling adler2 v2.0.1
   Compiling utf8parse v0.2.2
   Compiling anstyle v1.0.14
   Compiling colorchoice v1.0.5
   Compiling anstyle-query v1.1.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling serde v1.0.228
   Compiling tinyvec_macros v0.1.1
   Compiling cpufeatures v0.3.0
   Compiling itoa v1.0.18
   Compiling zmij v1.0.21
   Compiling strsim v0.11.1
   Compiling weezl v0.1.12
   Compiling siphasher v1.0.4
   Compiling clap_lex v1.1.0
   Compiling cpufeatures v0.2.17
   Compiling thiserror v2.0.18
   Compiling unicode-properties v0.1.4
   Compiling percent-encoding v2.3.2
   Compiling color_quant v1.1.0
   Compiling const-oid v0.10.2
   Compiling serde_json v1.0.150
   Compiling bytecount v0.6.9
   Compiling byteorder-lite v0.1.0
   Compiling pxfm v0.1.30
   Compiling regex-syntax v0.8.10
   Compiling unicode-bidi v0.3.18
   Compiling quick-error v2.0.1
   Compiling chrono-tz v0.10.4
   Compiling zune-core v0.5.3
   Compiling iana-time-zone v0.1.65
   Compiling unsafe-libyaml v0.2.11
   Compiling rangemap v1.7.1
   Compiling log v0.4.30
   Compiling bytemuck v1.25.2
   Compiling ttf-parser v0.25.1
   Compiling is_executable v1.0.6
   Compiling ryu v1.0.23
   Compiling hex v0.4.3
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/crates/bob-obsidian-assets)
   Compiling similar v2.7.0
   Compiling pkg-config v0.3.33
   Compiling vcpkg v0.2.15
   Compiling rustix v1.1.5
   Compiling powerfmt v0.2.0
   Compiling zune-jpeg v0.5.15
   Compiling num-conv v0.2.2
   Compiling deranged v0.5.8
   Compiling time-core v0.1.9
   Compiling linux-raw-sys v0.12.1
   Compiling cc v1.2.63
   Compiling fallible-streaming-iterator v0.1.9
   Compiling fallible-iterator v0.3.0
   Compiling generic-array v0.14.7
   Compiling hashbrown v0.17.1
   Compiling num-traits v0.2.19
   Compiling encoding_rs v0.8.35
   Compiling fastrand v2.5.0
   Compiling once_cell v1.21.4
   Compiling base64 v0.22.1
   Compiling aho-corasick v1.1.4
   Compiling nom v8.0.0
   Compiling anstyle-parse v1.0.0
   Compiling fdeflate v0.3.7
   Compiling quick-xml v0.41.0
   Compiling hybrid-array v0.4.12
   Compiling miniz_oxide v0.8.9
   Compiling chacha20 v0.10.2
   Compiling tinyvec v1.11.0
   Compiling gif v0.14.2
   Compiling image-webp v0.2.4
   Compiling form_urlencoded v1.2.2
   Compiling phf_shared v0.12.1
   Compiling fs2 v0.4.3
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
   Compiling indexmap v2.14.0
   Compiling hashlink v0.12.1
   Compiling time v0.3.53
   Compiling anstream v1.0.0
   Compiling phf v0.12.1
   Compiling flate2 v1.1.9
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling rand v0.10.1
   Compiling unicode-normalization v0.1.25
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling clap_builder v4.6.7
   Compiling inout v0.1.4
   Compiling png v0.18.1
   Compiling moxcms v0.8.1
   Compiling chrono v0.4.44
   Compiling regex-automata v0.4.14
   Compiling digest v0.10.7
   Compiling nom_locate v5.0.0
   Compiling stringprep v0.1.5
   Compiling cipher v0.4.4
   Compiling digest v0.11.3
   Compiling tempfile v3.27.0
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling aes v0.8.4
   Compiling ecb v0.1.2
   Compiling cbc v0.1.2
   Compiling sha2 v0.11.0
   Compiling clap v4.6.7
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling regex v1.12.3
   Compiling clap_complete v4.6.11
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling lopdf v0.40.0
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling image v0.25.10
   Compiling zerofrom v0.1.8
   Compiling yoke v0.8.3
   Compiling rusqlite v0.40.1
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling serde_yaml v0.9.34+deprecated
   Compiling plist v1.10.0
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_collections v2.3.0
   Compiling icu_locale_core v2.3.0
   Compiling icu_provider v2.3.1
   Compiling icu_normalizer v2.3.0
   Compiling icu_properties v2.3.0
   Compiling rquickjs-core v0.12.1
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 1m 55s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/bob_cli-edb465a55cecd3c2)

running 219 tests
test native::config::gcal::tests::calendars_accept_string_ids ... ok
test native::config::gcal::tests::missing_and_null_use_defaults ... ok
test native::config::gcal::tests::unknown_keys_are_ignored ... ok
test native::config::gcal::tests::description_keys_default_to_bullets_and_eight_lines ... ok
test native::gcal::account::tests::unique_emails_ignores_case_and_whitespace_duplicates ... ok
test native::config::gcal::tests::rejects_bad_description_values ... ok
test native::config::tests::mistyped_gcal_block_leaves_other_loaders_working ... ok
test native::config::gcal::tests::parses_full_block ... ok
test native::config::gcal::tests::rejects_wrong_types ... ok
test native::config::gcal::tests::validates_google_event_colour_names_and_ids ... ok
test native::gcal::bullet_block::tests::empty_window_on_a_childless_row_is_directly_under_it ... ok
test native::gcal::bullet_block::tests::a_wrong_hash_is_not_the_block ... ok
test native::gcal::bullet_block::tests::first_matching_window_wins ... ok
test native::gcal::bullet_block::tests::hash_ignores_indent_characters ... ok
test native::gcal::bullet_block::tests::finds_a_one_line_block ... ok
test native::gcal::bullet_block::tests::depends_on_above_does_not_hide ... ok
test native::gcal::bullet_block::tests::insertion_skips_a_cancel_log_subtree ... ok
test native::gcal::bullet_block::tests::nested_note_hides_the_block ... ok
test native::gcal::bullet_block::tests::nested_depth_two_stays_in_the_window ... ok
test native::gcal::bullet_block::tests::replace_window_swaps_or_removes ... ok
test native::gcal::bullet_block::tests::sibling_notes_above_or_below_do_not_hide ... ok
test native::gcal::bullet_block::tests::work_log_above_or_below_does_not_hide ... ok
test native::gcal::bullet_block::tests::empty_window_is_the_insertion_point_after_managed ... ok
test native::gcal::classify::tests::day_aliases_and_explicit_dates_are_local_calendar_days ... ok
test native::gcal::classify::tests::local_day_windows_are_23_and_25_hours_at_dst_changes ... ok
test native::gcal::classify::tests::tentative_task_setting_promotes_only_eligible_busy_events ... ok
test native::gcal::classify::tests::fixture_covers_inclusion_rsvp_day_ownership_and_foreign_offsets ... ok
test native::gcal::client::tests::authorized_user_is_rejected ... ok
test native::gcal::client::tests::bad_client_id_suffix_is_rejected ... ok
test native::gcal::cli::tests::calendars_format_defaults_to_table ... ok
test native::gcal::client::tests::empty_secret_is_rejected ... ok
test native::gcal::client::tests::installed_client_parses_with_project_id ... ok
test native::gcal::client::tests::legacy_flat_client_derives_numeric_prefix ... ok
test native::gcal::client::tests::missing_id_is_rejected ... ok
test native::gcal::client::tests::missing_secret_is_rejected ... ok
test native::gcal::cli::tests::sync_args_pin_options ... ok
test native::gcal::client::tests::non_json_is_rejected ... ok
test native::gcal::client::tests::peek_project_from_id_only_file ... ok
test native::gcal::cli::tests::logout_and_doctor_args ... ok
test native::gcal::cli::tests::login_args_pin_options ... ok
test native::gcal::client::tests::secret_never_appears_in_messages ... ok
test native::gcal::client::tests::service_account_is_rejected ... ok
test native::gcal::client::tests::web_client_is_rejected ... ok
test native::gcal::client::tests::to_gog_json_wraps_installed ... ok
test native::gcal::config::tests::defaults_when_block_is_missing ... ok
test native::gcal::config::tests::description_keys_resolve_and_reject ... ok
test native::gcal::config::tests::rejects_account_without_at ... ok
test native::gcal::description::bullets::tests::hash_and_materialization_follow_depth_and_body ... ok
test native::gcal::description::bullets::tests::markdown_destination_encoding_covers_delimiters ... ok
test native::gcal::description::tests::looks_like_html_uses_known_tags_only ... ok
test native::gcal::description::tests::on_directive_is_removed_but_tagged_prose_remains_a_bullet ... ok
test native::gcal::description::tests::debug_prints_counts_only ... ok
test native::gcal::description::tests::no_vendor_content_writes_no_keep_bullet ... ok
test native::gcal::diagnostics::tests::canonical_conflict_warns_without_deprecation_records ... ok
test native::gcal::diagnostics::tests::on_wins_copy_drops_the_redundant_alias ... ok
test native::gcal::description::tests::keep_bullet_labels_by_vendor ... ok
test native::gcal::gog::tests::calendar_primary_matches_configured_id ... ok
test native::gcal::diagnostics::tests::inherited_advice_appends_drop_parenthetical ... ok
test native::gcal::gog::tests::maps_keyring_invalid_client_and_redirect_mismatch ... ok
test native::gcal::gog::tests::maps_remote_step_failures ... ok
test native::gcal::diagnostics::tests::single_alias_warns_with_write_off ... ok
test native::gcal::gog::tests::semver_parse_and_compare ... ok
test native::gcal::gog::tests::state_from_auth_url_reads_query ... ok
test native::gcal::journal::tests::span_hash_is_stable_and_short ... ok
test native::gcal::description::tests::description_directive_vectors ... ok
test native::gcal::gog::tests::maps_api_disabled_and_invalid_grant ... ok
test native::gcal::lifecycle::tests::cancel_creates_the_log_when_missing ... ok
test native::gcal::lifecycle::tests::splits_task_and_context_rows ... ok
test native::gcal::lifecycle::tests::completion_fields_stay_in_the_vault_owned_suffix ... ok
test native::gcal::lifecycle::tests::trailing_clock_badges_split_with_or_without_calendar_link ... ok
test native::gcal::lifecycle::tests::timed_meet_entries_survive_cleanup ... ok
test native::gcal::lifecycle::tests::open_meet_links_after_a_closed_entry_stay_untouched ... ok
test native::gcal::lifecycle::tests::hashes_match_the_journal_spans ... ok
test native::gcal::lifecycle::tests::untimed_meet_entries_go_when_childless ... ok
test native::gcal::lifecycle::tests::cancel_log_reuses_tab_child_indent_and_lands_first ... ok
test native::gcal::login::tests::flow_names_match_json ... ok
test native::gcal::link_order::tests::no_event_rows_or_no_pomodoros_returns_input_unchanged ... ok
test native::gcal::login_ui::tests::step_prefix_pads_label_to_column_twenty ... ok
test native::gcal::login::tests::downloads_confirm_treats_q_as_cancel_and_junk_as_unknown ... ok
test native::gcal::login::tests::api_url_prefers_message_then_client_project ... ok
test native::gcal::link_order::tests::non_event_children_keep_their_slots ... ok
test native::gcal::link_order::tests::each_entry_sorts_independently_and_cross_midnight_uses_start ... ok
test native::gcal::model::tests::event_description_debug_redacts_text ... ok
test native::gcal::link_order::tests::ignores_other_notes_unknown_ids_and_ambiguous_event_ids ... ok
test native::gcal::clock::tests::listed_clock_inherits_through_the_chosen_root_only ... ok
test native::gcal::link_order::tests::link_subtrees_move_around_other_child_blocks ... ok
test native::gcal::description::tests::boilerplate_vectors ... ok
test native::gcal::link_order::tests::sorts_two_links_and_leaves_sorted_input_byte_identical ... ok
test native::gcal::link_order::tests::sorts_closed_tomato_and_struck_links_but_not_mixed_or_deeper_links ... ok
test native::gcal::link_order::tests::ties_use_end_then_event_row_order_and_duplicate_links_stay_stable ... ok
test native::gcal::model::tests::google_title_clock_matching_requires_a_whole_token ... ok
test native::gcal::model::tests::google_clock_conflicts_are_order_independent_and_keep_alias_evidence ... ok
test native::gcal::plan::tests::canonical_stamp_directly_above_prose_gains_one_separator ... ok
test native::gcal::plan::tests::bold_span_bullet_never_moves_the_insert_slot ... ok
test native::gcal::plan::tests::absent_empty_description_appends_no_record ... ok
test native::gcal::plan::tests::context_rows_record_absent_and_write_no_bullets ... ok
test native::gcal::plan::tests::absent_matching_window_is_adopted_without_writing ... ok
test native::gcal::plan::tests::adopted_unended_row_still_gets_open_meet_link ... ok
test native::gcal::plan::tests::closed_entry_lands_between_completed_sessions ... ok
test native::gcal::plan::tests::crash_adoption_of_empty_render_is_tracked ... ok
test native::gcal::plan::tests::crash_adoption_without_matching_window_is_hands_off ... ok
test native::gcal::plan::tests::colour_calendar_and_default_reroute_unedited_roots ... ok
test native::gcal::model::tests::description_aliases_and_buffers_combine_only_on_directive_lines ... ok
test native::gcal::plan::tests::current_meeting_creates_or_reuses_running_meet ... ok
test native::gcal::plan::tests::depends_on_above_the_block_does_not_hide_it ... ok
test native::gcal::plan::tests::crash_adoption_records_matching_bullets_without_writing ... ok
test native::gcal::plan::tests::cross_midnight_past_meeting_wraps_end ... ok
test native::gcal::plan::tests::every_run_refreshes_an_older_stamp ... ok
test native::gcal::plan::tests::handwritten_section_gains_a_stamp ... ok
test native::gcal::plan::tests::edited_misplaced_and_duplicated_stamps_normalize ... ok
test native::gcal::plan::tests::current_during_running_work_uses_placeholder_and_warns ... ok
test native::gcal::plan::tests::deleted_block_is_never_re_added ... ok
test native::gcal::plan::tests::bryan_edit_is_kept_silently_then_reported_once ... ok
test native::gcal::plan::tests::abby_inherits_love_and_invalid_nearer_value_stays_worked ... ok
test native::gcal::plan::tests::existing_ended_row_gets_no_closed_entry ... ok
test native::gcal::plan::tests::context_upgrade_resolves_the_upgraded_line ... ok
test native::gcal::plan::tests::done_row_still_reroutes ... ok
test native::gcal::plan::tests::existing_canonical_stamp_is_unchanged ... ok
test native::gcal::plan::tests::earlier_row_joins_a_well_formed_list_below_its_gap ... ok
test native::gcal::plan::tests::missing_root_gains_one ... ok
test native::gcal::plan::tests::empty_bullet_block_tracks_zero_lines_and_stays_put ... ok
test native::gcal::plan::tests::nested_note_hands_the_block_to_bryan ... ok
test native::gcal::plan::tests::missing_fresh_root_never_removes_an_existing_root ... ok
test native::gcal::plan::tests::kept_title_edit_still_reroutes ... ok
test native::gcal::plan::tests::mixed_current_events_stamp_worked ... ok
test native::gcal::model::tests::google_title_clock_tokens_strip_before_route_parsing ... ok
test native::gcal::plan::tests::inherited_untagged_row_never_reports_kept_off_clock ... ok
test native::gcal::plan::tests::kept_clock_notices_cover_every_explicit_transition ... ok
test native::gcal::plan::tests::new_earlier_event_sorts_before_a_previously_journaled_link ... ok
test native::gcal::plan::tests::gap_only_repair_changes_contents_without_records ... ok
test native::gcal::plan::tests::new_earliest_row_lands_below_the_stamp ... ok
test native::gcal::plan::tests::future_stamp_is_rewritten ... ok
test native::gcal::plan::tests::hands_off_journal_is_never_rewritten ... ok
test native::gcal::plan::tests::no_section_and_no_events_gains_nothing ... ok
test native::gcal::plan::tests::new_section_has_gap_below_heading_only ... ok
test native::gcal::plan::tests::new_task_row_carries_its_bullets_and_tracks_them ... ok
test native::gcal::plan::tests::stamp_above_a_paragraph_gets_a_blank_line ... ok
test native::gcal::plan::tests::nested_google_list_rewrites_in_place ... ok
test native::gcal::plan::tests::new_section_plan_is_idempotent ... ok
test native::gcal::plan::tests::stamp_only_refresh_leaves_meet_lines_below_events_unmoved ... ok
test native::gcal::plan::tests::stamp_below_pomodoros_does_not_shift_meet_line ... ok
test native::gcal::plan::tests::series_memory_never_rewrites_an_existing_root ... ok
test native::gcal::plan::tests::off_mode_leaves_existing_bullets_and_carries_the_record ... ok
test native::gcal::plan::tests::stamp_separator_is_reused_across_forced_refreshes ... ok
test native::gcal::plan::tests::sibling_notes_and_work_log_do_not_hide_the_block ... ok
test native::gcal::plan::tests::edited_root_is_kept_and_reported_once ... ok
test native::gcal::plan::tests::overflow_url_bullet_is_never_adopted_as_a_row ... ok
test native::gcal::plan::tests::explicit_off_beats_a_false_note ... ok
test native::gcal::plan::tests::google_edit_rewrites_the_block_in_place ... ok
test native::gcal::plan::tests::time_change_reslots_the_row_with_its_bullets ... ok
test native::gcal::plan::tests::edited_root_still_gets_a_time_update ... ok
test native::gcal::description::bullets::tests::bullet_vectors ... ok
test native::gcal::description::tests::outline_vectors ... ok
test native::gcal::plan::tests::unedited_root_reroute_skips_type_when_not_needed ... ok
test native::gcal::plan::tests::update_carries_the_description_record_forward ... ok
test native::gcal::plan::tests::untagged_love_event_creates_an_off_clock_cluster_without_a_tag ... ok
test native::gcal::plan::tests::upgrade_lands_bullets_above_existing_notes ... ok
test native::gcal::render::tests::badge_urls_and_maps_links_are_encoded ... ok
test native::gcal::plan::tests::existing_type_survives_a_reroute ... ok
test native::gcal::plan::tests::stamp_blank_before_list_is_preserved_on_refresh ... ok
test native::gcal::render::tests::badges_render_title_free ... ok
test native::gcal::render::tests::buffered_row_renders_buffer_between_badges_and_root ... ok
test native::gcal::render::tests::buffer_sides_render_only_when_set ... ok
test native::gcal::render::tests::context_row_qualifiers_and_badges ... ok
test native::gcal::render::tests::hostile_titles_stay_data ... ok
test native::gcal::render::tests::off_clock_task_rows_render_the_canonical_tag_before_root ... ok
test native::gcal::plan::tests::sort_only_plan_refreshes_stamp_and_is_idempotent ... ok
test native::gcal::render::tests::on_and_conflicting_tags_render_as_canonical_on ... ok
test native::gcal::render::tests::task_row_field_order_and_status ... ok
test native::gcal::render::tests::row_metadata_reroute_keeps_the_google_run_intact ... ok
test native::gcal::plan::tests::google_clearing_the_description_removes_the_block ... ok
test native::gcal::plan::tests::root_reroute_is_idempotent ... ok
test native::gcal::signin::tests::callback_from_request_keeps_port_and_query_bytes ... ok
test native::gcal::plan::tests::title_and_description_change_share_one_updated_row ... ok
test native::gcal::plan::tests::unparseable_row_keeps_its_bullets_and_record ... ok
test native::gcal::root::tests::rejects_invalid_and_missing ... ok
test native::gcal::plan::tests::upgraded_ended_maybe_gets_closed_meet ... ok
test native::gcal::root::tests::accepts_an_area_that_is_its_own_root ... ok
test native::gcal::plan::tests::vault_edited_root_controls_the_filed_clock ... ok
test native::gcal::plan::tests::unedited_root_reroutes_to_token_and_adds_meet_type ... ok
test native::gcal::plan::tests::on_tag_keeps_a_love_event_worked ... ok
test native::gcal::root::tests::invalid_color_falls_back_to_calendar_and_invalid_default_has_no_root ... ok
test native::gcal::plan::tests::replan_uses_changed_daily_note_bytes ... ok
test native::gcal::root::tests::unknown_title_route_stays_in_title_and_color_wins_next ... ok
test native::gcal::ui::tests::type_swatch_uses_name_without_color ... ok
test native::gcal::root::tests::route_token_precedes_color_calendar_and_default ... ok
test native::gcal::render::tests::row_metadata_inserts_root_before_completion_suffix ... ok
test native::gcal::signin::tests::choose_flow_matrix ... ok
test native::gcal::signin::tests::html_escape_and_page ... ok
test native::gcal::plan::tests::pomodoro_entry_line_shifts_when_stamp_is_inserted ... ok
test native::gcal::signin::tests::login_hint_preserves_state ... ok
test native::gcal::signin::tests::request_line_parsing ... ok
test native::gcal::stamp::tests::account_guard_ignores_malformed_and_matching_stamps ... ok
test native::gcal::stamp::tests::escaped_account_round_trips ... ok
test native::gcal::stamp::tests::malformed_recognized_line_does_not_parse ... ok
test native::gcal::stamp::tests::account_guard_refuses_a_different_account ... ok
test native::gcal::signin::tests::parse_redirect_cases ... ok
test native::gcal::stamp::tests::misplaced_stamp_is_due ... ok
test native::gcal::stamp::tests::missing_duplicate_future_and_edit_are_due ... ok
test native::gcal::stamp::tests::recognize_skips_list_rows_fences_and_outside_events ... ok
test native::gcal::stamp::tests::older_stamp_is_due ... ok
test native::gcal::stamp::tests::other_day_round_trip ... ok
test native::gcal::stamp::tests::truncate_drops_seconds ... ok
test native::gcal::stamp::tests::same_day_round_trip ... ok
test native::gcal::stamp::tests::underscore_emphasis_is_recognized ... ok
test native::gcal::tests::error_exit_codes ... ok
test native::gcal::ui::tests::glyphs_are_status_marks ... ok
test native::gcal::ui::tests::hue_dot_stays_plain_without_color ... ok
test native::gcal::plan::tests::one_open_never_leaves_two_open_meets ... ok
test native::gcal::plan::tests::pre_feature_row_backfills_once ... ok
test native::gcal::plan::tests::past_clusters_touching_meetings_and_splits_on_a_gap ... ok
test native::gcal::plan::tests::replanning_output_with_journal_is_idempotent ... ok
test native::gcal::plan::tests::past_and_future_share_closed_then_placeholder ... ok
test native::gcal::journal::tests::row_link_gone_fold_in_writer_order ... ok
test native::gcal::description::bullets::tests::oversize_input_uses_one_calendar_fallback ... ok
test native::gcal::description::bullets::tests::oversize_input_keeps_reasons_above_the_fallback ... ok
test native::gcal::render::tests::calendar_badges_never_parse_as_due_dates ... ok
test native::gcal::description::bullets::tests::hostile_bullets_are_isolated_from_bob_scanners ... ok
test native::gcal::description::tests::oversized_flag_does_not_stop_parse ... ok

test result: ok. 219 passed; 0 failed; 0 ignored; 0 measured; 4749 filtered out; finished in 0.04s

     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/bob-39abebeb4ad07360)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/bob_notify-f1a59fb8e3d29c43)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/bob_pomodoro-a1880c6eed04140e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/tmux_bob_pomodoro-5d65a532f2abf4a7)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/cli-862b59fffc4caf66)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 3085 filtered out; finished in 0.00s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/dataview_parity-045096bc8cc5f0cf)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 27 filtered out; finished in 0.00s

     Running tests/gcal_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_auth-5d44594e9efeed44)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 53 filtered out; finished in 0.00s

     Running tests/gcal_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_cli-4853c16bfec90355)

running 1 test
test bare_gcal_lists_today_and_exits_0 ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 5 filtered out; finished in 0.32s

     Running tests/gcal_diagnostics.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_diagnostics-3e6fd7d18ca75de6)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 4 filtered out; finished in 0.00s

     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_lifecycle-0c23bd6bd84e8a6f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 44 filtered out; finished in 0.00s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_list-95d8d3d0d1e7df7e)

running 2 tests
test bare_gcal_explains_how_to_connect_before_login ... ok
test bare_gcal_lists_today_and_json_keeps_only_public_normalized_fields ... ok

test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.61s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_sync-fd2f0701023233dc)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_adapter-a41834edd3018b24)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_auth-f4da0806ca5ba93e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 14 filtered out; finished in 0.00s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_cli-a204c8fbda174c45)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_list-36fbd230bb53870f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 23 filtered out; finished in 0.00s

     Running tests/gkeep_migrate.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_migrate-3f3c4b52e1837a47)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_pull-dd0da037d577b7d1)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_pull_recovery.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_pull_recovery-5e7761c13c11d64b)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gkeep_status.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gkeep_status-44b7313be29df440)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 26 filtered out; finished in 0.00s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/randomize-f69db91da68364ae)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 15 filtered out; finished in 0.00s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/tasks_parity-a579f56c8602ab2e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 33 filtered out; finished in 0.00s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/tasks_real_vault_parity-0d2dc2f594a35474)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.10s
     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_lifecycle-0c23bd6bd84e8a6f)

running 44 tests
test preexisting_off_clock_badge_without_calendar_link_migrates_with_buffer ... ok
test description_off_keeps_buffer_without_reason_bullets ... ok
test crash_adoption_matching_bullets_does_not_duplicate ... ok
test preexisting_off_clock_title_migrates_both_spans_in_place ... ok
test dry_run_diff_shows_the_root_change ... ok
test description_off_leaves_existing_bullets_alone ... ok
test malformed_description_record_is_hands_off ... ok
test preexisting_titled_badges_migrate_in_place ... ok
test context_rows_still_never_get_description_bullets ... ok
test unedited_root_reroutes_when_google_colour_changes ... ok
test unedited_root_reroutes_when_google_adds_a_token ... ok
test emptied_meet_entry_is_removed_with_the_cancel ... ok
test google_clearing_description_removes_the_block ... ok
test declined_event_nests_cancel_log_above_tab_indented_child ... ok
test tomato_in_description_does_not_count_as_worked ... ok
test failed_lookup_writes_nothing ... ok
test moved_event_names_the_new_day ... ok
test deleted_event_lookup_uses_the_sole_bob_account ... ok
test off_to_on_tag_flip_on_worked_row_is_kept_once ... ok
test yes_maybe_leaves_the_row_and_reports_once ... ok
test off_clock_tag_flip_on_worked_row_is_kept_once ... ok
test deleted_description_block_is_never_re_added ... ok
test list_footer_surfaces_open_past_meetings ... ok
test plain_bullet_migrates_to_reason_bullet ... ok
test kept_edit_reported_once ... ok
test maybe_yes_upgrades_the_context_row_and_links ... ok
test pre_feature_row_backfills_on_the_next_sync ... ok
test google_description_edit_rewrites_untouched_bullets ... ok
test explicit_on_tag_adds_and_removes_in_place_on_untouched_rows ... ok
test maybe_upgrade_gains_buffer_field ... ok
test off_clock_tag_flip_updates_untouched_row_in_place ... ok
test worked_task_is_never_cancelled ... ok
test bob_reroute_does_not_teach_the_series ... ok
test root_reroute_keeps_buffered_google_run ... ok
test declined_event_cancels_untouched_task ... ok
test span_updates_rewrite_clean_spans_and_reslot ... ok
test deleted_past_row_is_left_alone_and_reported_once ... ok
test deleted_event_lookup_cancels_and_reports_once ... ok
test buffer_reasons_lead_the_description_block ... ok
test edited_description_is_kept_silently_then_reported_once ... ok
test series_edit_teaches_and_reteaches_the_root ... ok
test google_reason_edit_rewrites_untouched_block_and_keeps_edits ... ok
test doctor_reports_malformed_journal_and_last_error ... ok
test buffer_change_updates_untouched_row_in_place_and_keeps_edits ... ok

test result: ok. 44 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.99s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_list-95d8d3d0d1e7df7e)

running 9 tests
test bare_gcal_explains_how_to_connect_before_login ... ok
test explicit_on_directive_is_listed_on_clock_even_with_an_off_alias ... ok
test list_uses_the_configured_account_among_multiple_bob_grants ... ok
test all_flag_adds_omitted_events_with_their_reason ... ok
test list_uses_the_sole_bob_account_among_multiple_gog_accounts ... ok
test list_shows_buffer_reasons_in_time_and_event_columns ... ok
test a_page_failure_or_remaining_token_fails_the_whole_snapshot ... ok
test listed_clock_uses_google_root_and_via_note ... ok
test bare_gcal_lists_today_and_json_keeps_only_public_normalized_fields ... ok

test result: ok. 9 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.64s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_114954/build/debug/deps/gcal_sync-fd2f0701023233dc)

running 50 tests
test dry_run_diff_shows_the_bullets ... ok
test dry_run_diff_shows_the_stamp_line ... ok
test dry_run_prints_diff_and_writes_nothing ... ok
test context_rows_never_get_bullets ... ok
test long_description_caps_at_eight_with_an_overflow_line ... ok
test description_off_writes_no_bullets ... ok
test descriptions_become_bullets_in_every_phase ... ok
test missing_note_waits_with_exit_zero ... ok
test crash_recovery_adopts_unjournaled_rows ... ok
test first_sync_creates_events_meet_and_links ... ok
test waiting_json_reports_a_null_stamp ... ok
test incomplete_snapshot_writes_nothing ... ok
test agenda_reads_synced_rows_cleanly ... ok
test foreign_writer_refuses_but_dry_run_previews ... ok
test tomorrow_stamp_uses_the_dated_form ... ok
test future_day_gets_placeholder_and_starred_rows ... ok
test hostile_titles_stay_data ... ok
test new_row_lands_after_the_previous_rows_bullets ... ok
test past_day_gets_closed_meet_entries ... ok
test space_indented_note_gets_space_bullets ... ok
test sync_json_rows_carry_description_lines ... ok
test teams_only_description_writes_nothing ... ok
test quiet_prints_nothing_on_success ... ok
test meet_placeholder_follows_the_last_open_entry ... ok
test existing_open_meet_is_reused ... ok
test sync_json_reports_rows_and_pomodoro ... ok
test current_meeting_reconcile_then_clock_close ... ok
test reconcile_keeps_linked_rows ... ok
test closed_meet_session_attributes_body_in_stats ... ok
test account_guard_refuses_a_foreign_stamp ... ok
test list_keeps_google_root_when_vault_root_differs ... ok
test second_run_with_bullets_is_a_no_op ... ok
test deleted_row_with_overflow_bullet_is_tombstoned_not_adopted ... ok
test deleted_row_and_removed_link_are_never_readded ... ok
test buffered_spans_drive_meet_phases_and_clusters ... ok
test json_lists_meet_entries_and_keeps_open_entry_keys ... ok
test second_run_is_byte_identical_and_appends_nothing ... ok
test deleted_stamp_is_restored_without_row_churn ... ok
test list_reports_task_meet_for_a_past_row ... ok
test off_clock_aliases_split_clusters_and_report ... ok
test title_free_row_is_adopted_without_duplicate ... ok
test upgrade_lands_bullets_above_existing_notes ... ok
test title_update_keeps_the_description_record ... ok
test inherited_note_clock_stamps_meets_without_materializing_tags ... ok
test sync_restores_missing_blank_under_events_heading ... ok
test past_completed_row_stays_syncable_and_reconcile_stable ... ok
test sync_sorts_event_task_links_and_reports_sort_only_runs ... ok
test missing_paragraph_gap_is_repaired_without_journal_churn ... ok
test stamp_refreshes_every_run_without_row_churn ... ok
test buffered_rows_render_update_and_report ... ok

test result: ok. 50 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.72s


🔍  LINT
────────────────────────────────────────────────
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking typenum v1.20.1
    Checking cfg-if v1.0.4
    Checking stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
    Checking allocator-api2 v0.2.21
    Checking equivalent v1.0.2
    Checking foldhash v0.2.0
    Checking memchr v2.8.1
    Checking litemap v0.8.3
    Checking writeable v0.6.4
    Checking simd-adler32 v0.3.9
    Checking bitflags v2.12.1
    Checking utf8_iter v1.0.4
    Checking smallvec v1.15.2
    Checking utf8parse v0.2.2
    Checking rand_core v0.10.1
    Checking adler2 v2.0.1
    Checking is_terminal_polyfill v1.70.2
    Checking tinyvec_macros v0.1.1
    Checking cpufeatures v0.3.0
    Checking anstyle v1.0.14
    Checking colorchoice v1.0.5
    Checking anstyle-query v1.1.5
    Checking cpufeatures v0.2.17
    Checking strsim v0.11.1
    Checking itoa v1.0.18
    Checking weezl v0.1.12
    Checking siphasher v1.0.4
    Checking clap_lex v1.1.0
    Checking color_quant v1.1.0
    Checking zune-core v0.5.3
    Checking quick-error v2.0.1
    Checking const-oid v0.10.2
    Checking bytecount v0.6.9
    Checking unicode-bidi v0.3.18
    Checking byteorder-lite v0.1.0
    Checking unicode-properties v0.1.4
    Checking regex-syntax v0.8.10
    Checking pxfm v0.1.30
    Checking iana-time-zone v0.1.65
    Checking percent-encoding v2.3.2
    Checking bytemuck v1.25.2
    Checking is_executable v1.0.6
    Checking ttf-parser v0.25.1
    Checking log v0.4.30
    Checking unsafe-libyaml v0.2.11
    Checking ryu v1.0.23
    Checking rangemap v1.7.1
    Checking libc v0.2.186
    Checking icu_properties_data v2.3.0
    Checking icu_normalizer_data v2.3.0
    Checking serde_core v1.0.228
    Checking zmij v1.0.21
    Checking similar v2.7.0
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/crates/bob-obsidian-assets)
    Checking hex v0.4.3
    Checking num-traits v0.2.19
    Checking deranged v0.5.8
    Checking num-conv v0.2.2
    Checking time-core v0.1.9
    Checking zerofrom v0.1.8
    Checking thiserror v2.0.18
    Checking linux-raw-sys v0.12.1
    Checking powerfmt v0.2.0
    Checking crc32fast v1.5.0
    Checking encoding_rs v0.8.35
    Checking fallible-iterator v0.3.0
    Checking fallible-streaming-iterator v0.1.9
   Compiling cc v1.2.63
    Checking fastrand v2.5.0
    Checking base64 v0.22.1
    Checking once_cell v1.21.4
    Checking phf_shared v0.12.1
    Checking image-webp v0.2.4
    Checking hashbrown v0.17.1
    Checking fs2 v0.4.3
    Checking anstyle-parse v1.0.0
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking quick-xml v0.41.0
    Checking getrandom v0.4.2
    Checking chacha20 v0.10.2
    Checking gif v0.14.2
    Checking zune-jpeg v0.5.15
    Checking generic-array v0.14.7
    Checking hybrid-array v0.4.12
    Checking miniz_oxide v0.8.9
    Checking fdeflate v0.3.7
    Checking tinyvec v1.11.0
    Checking form_urlencoded v1.2.2
    Checking rustix v1.1.5
    Checking yoke v0.8.3
    Checking chrono v0.4.44
    Checking time v0.3.53
    Checking serde v1.0.228
    Checking serde_json v1.0.150
    Checking phf v0.12.1
    Checking moxcms v0.8.1
    Checking indexmap v2.14.0
    Checking hashlink v0.12.1
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
    Checking anstream v1.0.0
    Checking regex-automata v0.4.14
    Checking rand v0.10.1
    Checking crypto-common v0.2.2
    Checking block-buffer v0.12.0
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking flate2 v1.1.9
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking unicode-normalization v0.1.25
    Checking nom_locate v5.0.0
    Checking serde_yaml v0.9.34+deprecated
    Checking chrono-tz v0.10.4
    Checking clap_builder v4.6.7
    Checking digest v0.10.7
    Checking inout v0.1.4
    Checking tempfile v3.27.0
    Checking plist v1.10.0
    Checking png v0.18.1
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking digest v0.11.3
    Checking stringprep v0.1.5
    Checking cipher v0.4.4
    Checking md-5 v0.10.6
    Checking sha2 v0.10.9
    Checking regex v1.12.3
    Checking icu_collections v2.3.0
    Checking aes v0.8.4
    Checking ecb v0.1.2
    Checking cbc v0.1.2
    Checking icu_locale_core v2.3.0
    Checking sha2 v0.11.0
    Checking image v0.25.10
    Checking clap v4.6.7
    Checking clap_complete v4.6.11
    Checking lopdf v0.40.0
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking rusqlite v0.40.1
    Checking url v2.5.8
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:563:12
    |
563 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:383:20
    |
383 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

warning: this `else` branch is empty
   --> src/native/task_cancel/prune.rs:119:15
    |
119 |               } else {
    |  _______________^
120 | |             }
    | |_____________^ help: you can remove it
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_else
    = note: `#[warn(clippy::needless_else)]` on by default

warning: `format!` in `println!` args
   --> src/native/articles/render.rs:170:5
    |
170 | /     println!(
171 | |         "{} {} {}",
172 | |         styler.cyan("Articles"),
173 | |         styler.separator(),
174 | |         format!("{total} · {}", display_root(root))
175 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `println!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args
    = note: `#[warn(clippy::format_in_format_args)]` on by default

warning: this function has too many arguments (8/7)
   --> src/native/attachments/journal.rs:108:1
    |
108 | / pub(crate) fn append_event(
109 | |     vault: &Path,
110 | |     host: &str,
111 | |     saved: &str,
...   |
116 | |     ts: DateTime<FixedOffset>,
117 | | ) -> io::Result<String> {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:23:54
   |
23 |     pub(super) fn validate(&self, bob_dir: &Path) -> Result<(), CaptureError> {
   |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
   = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:81:10
   |
81 |     ) -> Result<(), CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:147:10
    |
147 |     ) -> Result<bool, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:155:10
    |
155 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:169:10
    |
169 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:184:10
    |
184 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:237:10
    |
237 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:256:10
    |
256 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:370:10
    |
370 |     ) -> Result<usize, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:395:10
    |
395 |     ) -> Result<Vec<StagedTextFile>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:432:6
    |
432 | ) -> Result<Vec<usize>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:484:6
    |
484 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:25:6
   |
16 |     Capture(CaptureError),
   |     --------------------- the largest variant contains at least 248 bytes
...
25 | ) -> Result<MovePlan, BatchMoveError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: try reducing the size of `native::capture::batch_move::BatchMoveError`, for example by boxing large elements or replacing it with `Box<native::capture::batch_move::BatchMoveError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:40:6
   |
16 |     Capture(CaptureError),
   |     --------------------- the largest variant contains at least 248 bytes
...
40 | ) -> Result<MovePlan, BatchMoveError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: try reducing the size of `native::capture::batch_move::BatchMoveError`, for example by boxing large elements or replacing it with `Box<native::capture::batch_move::BatchMoveError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:70:6
   |
70 | ) -> Result<VaultSnapshot, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch_move.rs:110:6
    |
110 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch_move.rs:130:6
    |
130 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:38:6
   |
38 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:91:6
   |
91 | ) -> Result<DependentRef, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:226:6
    |
226 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:253:6
    |
253 | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/blocked_tasks.rs:244:1
    |
244 | / pub(super) fn plan_blocked_task_writes(
245 | |     ctx: &mut DependencyContext,
246 | |     planner: &mut CaptureBatchPlanner,
247 | |     bob_dir: &Path,
...   |
252 | |     options: ExistingDependencyOptions,
253 | | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    | |_______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocks_mirror.rs:52:6
   |
52 | ) -> Result<Option<(BlocksLineUpdateJson, TaskBlockRef)>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:237:6
    |
237 | ) -> Result<TaskBlockRef, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:266:6
    |
266 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:293:6
    |
293 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/budget.rs:325:6
    |
325 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:814:10
    |
814 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:856:22
    |
856 |                   .map(|values| {
    |  ______________________^
857 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
858 | |                 })
    | |_________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:857:32
    |
857 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
    |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:865:22
    |
865 |                 .map(|raw| parse_pull_in_picks(raw))
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:880:6
    |
880 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:894:6
    |
894 | ) -> Result<PullInPicks, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:930:6
    |
930 | ) -> Result<InboxRoutePick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:959:6
    |
959 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:970:14
    |
970 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:977:6
    |
977 | ) -> Result<SubBulletTarget, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:990:6
    |
990 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1039:6
     |
1039 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1070:6
     |
1070 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:28:6
   |
28 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:44:6
   |
44 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
  --> src/native/capture/commit.rs:59:55
   |
59 |           write_staged_files_guarded(&batch.text_files, || {
   |  _______________________________________________________^
60 | |             batch.read_guards.validate(bob_dir)
61 | |         })
   | |_________^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:132:6
    |
132 | ) -> Result<Vec<PathBuf>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:177:6
    |
177 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:222:6
    |
222 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:223:39
    |
223 |     write_staged_files_guarded(files, || Ok(()))
    |                                       ^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:229:6
    |
229 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:273:35
    |
273 |         validate_reads().and_then(|()| validate_disk_preimages(files))
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:408:6
    |
408 | ) -> Result<PathBuf, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:477:45
    |
477 | pub(super) fn read_target(target: &Path) -> Result<String, CaptureError> {
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/capture/dependencies.rs:65:19
   |
65 |       close_policy: OnceLock<(
   |  ___________________^
66 | |         Vec<config::relations::CancelLabel>,
67 | |         Vec<config::relations::CompleteLabel>,
68 | |         Vec<config::relations::CancelLabel>,
69 | |         Vec<config::relations::CancelLabel>,
70 | |         Option<String>,
71 | |     )>,
   | |______^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
   = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture/dependencies.rs:306:10
    |
306 |       ) -> &(
    |  __________^
307 | |         Vec<config::relations::CancelLabel>,
308 | |         Vec<config::relations::CompleteLabel>,
309 | |         Vec<config::relations::CancelLabel>,
310 | |         Vec<config::relations::CancelLabel>,
311 | |         Option<String>,
312 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1035:6
     |
1035 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1201:6
     |
1201 | ) -> Result<PathBuf, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1318:6
     |
1318 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1370:6
     |
1370 | ) -> Result<(String, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1481:6
     |
1481 | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:1472:1
     |
1472 | / fn resolve_prerequisites(
1473 | |     ctx: &DependencyContext,
1474 | |     planner: &mut CaptureBatchPlanner,
1475 | |     bob_dir: &Path,
...    |
1480 | |     dependent_desc: &str,
1481 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1571:10
     |
1571 |     ) -> Result<Self, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1814:24
     |
1814 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1903:6
     |
1903 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2044:6
     |
2044 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2065:6
     |
2065 | ) -> Result<Vec<TaskBlockRef>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2078:6
     |
2078 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2103:6
     |
2103 | ) -> Result<Vec<TargetTouch>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2193:6
     |
2193 | ) -> Result<Option<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2373:6
     |
2373 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2373:6
     |
2373 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2582:6
     |
2582 | ) -> Result<PlannedDependencyUpdate, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3088:6
     |
3088 | ) -> Result<(AugmentedNewTask, PlannedDependencyUpdateParts), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3352:6
     |
3352 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3410:6
     |
3410 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:42:6
   |
42 | ) -> Result<ResolvedLinkGuard, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:79:6
   |
79 | ) -> Result<DropAttempt, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/ensure_next.rs:23:6
   |
23 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/event_conflict.rs:287:1
    |
287 | / pub(super) fn detect_event_conflict(
288 | |     contents: &str,
289 | |     date: NaiveDate,
290 | |     session_name: Option<&str>,
...   |
295 | |     fit: &FitKind,
296 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/event_conflict.rs:311:1
    |
311 | / pub(super) fn detect_event_conflict_with<V: CloseVault + ?Sized>(
312 | |     contents: &str,
313 | |     date: NaiveDate,
314 | |     session_name: Option<&str>,
...   |
321 | |     day_relative: Option<&Path>,
322 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/existing_task_link.rs:57:6
   |
57 | ) -> Result<ExistingTaskLinkOutcome, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:144:6
    |
144 | ) -> Result<InboxRouteReport, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:345:6
    |
345 | ) -> Result<AppliedInboxRoutes, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:327:6
    |
327 | ) -> Result<LinkGuardVerdict, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:597:6
    |
597 | ) -> Result<Option<ConsumePlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:709:6
    |
709 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:203:6
    |
203 | ) -> Result<i64, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:533:6
    |
533 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:580:6
    |
580 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:599:6
    |
599 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:804:6
    |
804 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: methods called `as_*` usually take `self` by reference or `self` by mutable reference
   --> src/native/capture/move_consequence.rs:171:16
    |
171 |     fn as_text(self) -> String {
    |                ^^^^
    |
    = help: consider choosing a less ambiguous name
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention
    = note: `#[warn(clippy::wrong_self_convention)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/note_pull.rs:58:6
   |
58 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/open_notes.rs:138:1
    |
138 | / fn open_note_for_item(
139 | |     bob_dir: &Path,
140 | |     item: &CaptureItemResult,
141 | |     path: &Path,
...   |
146 | |     settings: &note_tasks::NoteTaskSettings,
147 | | ) -> OpenNoteJson {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
   --> src/native/capture/output.rs:442:5
    |
442 | /     pub(super) fn from_items(
443 | |         items: Vec<CaptureItemResult>,
444 | |         global_destination: Option<GlobalDestinationSummary>,
445 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
453 | |         inbox_route: InboxRouteReport,
454 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture/output.rs:6441:5
     |
6441 | /     pub(super) fn pull_in_choice_required(
6442 | |         extra: serde_json::Map<String, serde_json::Value>,
6443 | |         human_unblocked: Vec<TaskCompleteUnblockedJson>,
6444 | |         human_keep_moving_folds: Vec<
...    |
6453 | |         human_note_pull_groups: Vec<PullInGroupJson>,
6454 | |     ) -> Self {
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:64:6
   |
64 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:72:6
   |
72 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:492:6
    |
492 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:588:6
    |
588 | ) -> Result<FanoutClipboardRead, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:649:6
    |
649 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:857:6
    |
857 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:964:6
    |
964 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (14/7)
   --> src/native/capture/plan.rs:949:1
    |
949 | / pub(super) fn plan_capture_item(
950 | |     request: &CaptureRequest,
951 | |     parsed_item: ParsedCaptureItem,
952 | |     now: chrono::NaiveDateTime,
...   |
963 | |     project_moves: &[ProjectMoveLanding],
964 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:1633:14
     |
1633 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:1815:11
     |
1815 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3326:6
     |
3326 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3439:6
     |
3439 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3468:6
     |
3468 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3554:6
     |
3554 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3595:6
     |
3595 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3815:6
     |
3815 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:4276:13
     |
4276 |             &String::new(),
     |             ^^^^^^^^^^^^^^ help: try: `""`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_owned_empty_strings
     = note: `#[warn(clippy::unnecessary_owned_empty_strings)]` on by default

warning: the `Err`-variant returned from this function is very large
 --> src/native/capture/pomodoro_adjust.rs:8:6
  |
8 | ) -> Result<(), CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:24:6
   |
24 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:62:6
   |
62 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:131:6
    |
131 | ) -> Result<RunningSessionTarget, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:215:6
    |
215 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:271:6
    |
271 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:510:6
    |
510 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:582:6
    |
582 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:627:6
    |
627 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:810:6
    |
810 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1309:6
     |
1309 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1345:6
     |
1345 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1505:6
     |
1505 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1678:6
     |
1678 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1840:6
     |
1840 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2124:6
     |
2124 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2200:6
     |
2200 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2313:6
     |
2313 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2850:6
     |
2850 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_insert.rs:56:6
   |
56 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:127:6
    |
127 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:264:6
    |
264 | ) -> Result<DefaultPomodoroPick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:356:6
    |
356 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:468:6
    |
468 | ) -> Result<NamedPomodoroResolution<'a>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:499:6
    |
499 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/pomodoro_insert.rs:489:1
    |
489 | / pub(super) fn insert_named_pomodoro_child_block(
490 | |     contents: &str,
491 | |     block: &str,
492 | |     selector: &str,
...   |
498 | |     open: &[(usize, &str)],
499 | | ) -> Result<(String, Placement, usize, String), CaptureError> {
    | |_____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:572:6
    |
572 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_link.rs:18:6
   |
18 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:230:6
    |
230 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:286:6
    |
286 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:707:6
    |
707 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:792:6
    |
792 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:970:6
    |
970 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1015:6
     |
1015 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1807:6
     |
1807 | ) -> Result<&str, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_merge.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `index` is only used to index `lines`
  --> src/native/capture/pomodoro_merge.rs:94:18
   |
94 |     for index in (entry_index + 1)..=end {
   |                  ^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
   = note: `#[warn(clippy::needless_range_loop)]` on by default
help: consider using an iterator
   |
94 -     for index in (entry_index + 1)..=end {
94 +     for <item> in lines.iter().take(end + 1).skip((entry_index + 1)) {
   |

warning: the loop variable `index` is used to index `lines`
   --> src/native/capture/pomodoro_merge.rs:114:18
    |
114 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
114 -     for index in (entry_index + 1)..=end {
114 +     for (index, <item>) in lines.iter().enumerate().take(end + 1).skip((entry_index + 1)) {
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:250:6
    |
250 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:448:6
    |
448 | ) -> Result<ResolvedMerge, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:664:6
    |
664 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/pomodoro_merge.rs:655:1
    |
655 | / pub(super) fn plan_pomodoro_merge_item(
656 | |     request: &CaptureRequest,
657 | |     parsed: ParsedCaptureText,
658 | |     spec: PomodoroMergeSpec,
...   |
663 | |     warnings: &mut Vec<CaptureWarning>,
664 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_split.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `index` is only used to index `lines`
   --> src/native/capture/pomodoro_split.rs:194:18
    |
194 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
194 -     for index in (entry_index + 1)..=end {
194 +     for <item> in lines.iter().take(end + 1).skip((entry_index + 1)) {
    |

warning: the loop variable `index` is used to index `lines`
   --> src/native/capture/pomodoro_split.rs:214:18
    |
214 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
214 -     for index in (entry_index + 1)..=end {
214 +     for (index, <item>) in lines.iter().enumerate().take(end + 1).skip((entry_index + 1)) {
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_split.rs:295:6
    |
295 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/pomodoro_split.rs:286:1
    |
286 | / pub(super) fn plan_pomodoro_split_item(
287 | |     request: &CaptureRequest,
288 | |     parsed: ParsedCaptureText,
289 | |     spec: PomodoroSplitSpec,
...   |
294 | |     warnings: &mut Vec<CaptureWarning>,
295 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:17:6
   |
17 | ) -> Result<(String, String, u64, String), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:52:6
   |
52 |   ) -> Result<
   |  ______^
53 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
54 | |     CaptureError,
55 | | > {
   | |_^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:105:6
    |
105 |   ) -> Result<
    |  ______^
106 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
107 | |     CaptureError,
108 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:423:6
    |
423 |   ) -> Result<
    |  ______^
424 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
425 | |     CaptureError,
426 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:516:6
    |
516 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:568:6
    |
568 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:627:6
    |
627 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:646:6
    |
646 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:804:6
    |
804 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:816:6
    |
816 | ) -> Result<(String, Placement, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:861:6
    |
861 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:887:6
    |
887 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1187:6
     |
1187 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1447:6
     |
1447 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2088:6
     |
2088 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2191:6
     |
2191 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2256:6
     |
2256 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2426:6
     |
2426 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:105:6
    |
105 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:292:6
    |
292 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:311:6
    |
311 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:512:6
    |
512 | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/project_deps.rs:503:1
    |
503 | / pub(super) fn restamp_changed_timed_entries(
504 | |     planner: &mut CaptureBatchPlanner,
505 | |     bob_dir: &Path,
506 | |     day_file: &Path,
...   |
511 | |     warnings: &mut Vec<CaptureWarning>,
512 | | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    | |________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:18:6
   |
18 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:36:6
   |
36 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:79:6
   |
79 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/project_note.rs:164:14
    |
164 |         .map(|offset| scheduled_date_string(today, offset))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2099:6
     |
2099 | ) -> Result<Vec<ResolvedProjectMove>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2256:6
     |
2256 | ) -> Result<ProjectMoveExecution, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/project_note.rs:2268:14
     |
2268 |           .map(|movement| {
     |  ______________^
2269 | |             slot_by_source.get(&movement.source_index).copied().ok_or_else(
2270 | |                 || {
2271 | |                     CaptureError::io(
...    |
2276 | |         })
     | |_________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2864:6
     |
2864 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pull_in.rs:11:6
   |
11 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:282:6
    |
282 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relation_sources.rs:55:6
   |
55 | ) -> Result<Option<RelationSourceRead>, super::CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relation_sources.rs:364:6
    |
364 | ) -> Result<(), super::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:164:6
    |
164 | ) -> Result<PlannedRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:225:10
    |
225 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:254:6
    |
254 | ) -> Result<RelationOwner, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:314:6
    |
314 | ) -> Result<ResolvedRelation, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:391:6
    |
391 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:416:6
    |
416 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:460:6
    |
460 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:494:6
    |
494 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:570:6
    |
570 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:667:6
    |
667 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:716:6
    |
716 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:808:6
    |
808 | ) -> Result<(RelationAction, Option<String>, String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:916:1
    |
916 | / fn relation_update_json(
917 | |     direction: RelationDirection,
918 | |     source_relative: &Path,
919 | |     source_line: usize,
...   |
924 | |     previous_label: Option<String>,
925 | | ) -> RelationUpdateJson {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:961:6
    |
961 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_cancel.rs:36:6
   |
36 | ) -> Result<Vec<RelationCancelJson>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:112:6
    |
112 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:148:6
    |
148 | ) -> Result<Option<RelationCancelJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:383:6
    |
383 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:231:6
    |
231 | ) -> Result<ItemRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations_close.rs:222:1
    |
222 | / pub(super) fn plan_item_relations(
223 | |     ctx: &mut DependencyContext,
224 | |     planner: &mut CaptureBatchPlanner,
225 | |     request: &CaptureRequest,
...   |
230 | |     warnings: &mut Vec<CaptureWarning>,
231 | | ) -> Result<ItemRelationReports, CaptureError> {
    | |______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:269:6
    |
269 | ) -> Result<RelationCloseReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:465:6
    |
465 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this boolean expression can be simplified
   --> src/native/capture/relations_close.rs:489:14
    |
489 |         if !(cancel && complete || cancel && merge || complete && merge) {
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
    = note: `#[warn(clippy::nonminimal_bool)]` on by default
help: try
    |
489 -         if !(cancel && complete || cancel && merge || complete && merge) {
489 +         if !(!(!cancel || !complete && !merge) || complete && merge) {
    |
489 -         if !(cancel && complete || cancel && merge || complete && merge) {
489 +         if !((merge || complete) && cancel || complete && merge) {
    |

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_complete.rs:38:6
   |
38 | ) -> Result<RelationCompleteReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:144:6
    |
144 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:180:6
    |
180 | ) -> Result<Option<PlannedSourceComplete>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_mentions.rs:53:6
   |
53 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:460:6
    |
460 | ) -> Result<Option<(usize, String)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:507:6
    |
507 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:547:6
    |
547 | ) -> Result<Option<MirrorSkipReason>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:579:6
    |
579 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations_mentions.rs:570:1
    |
570 | / fn source_block_id(
571 | |     ctx: &mut DependencyContext,
572 | |     planner: &mut CaptureBatchPlanner,
573 | |     bob_dir: &Path,
...   |
578 | |     minted_sources: &mut BTreeMap<(PathBuf, usize), String>,
579 | | ) -> Result<Option<String>, CaptureError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:693:6
    |
693 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_merge.rs:43:6
   |
43 | ) -> Result<RelationMergeReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:222:6
    |
222 | ) -> Result<TaskLocator, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:262:6
    |
262 | ) -> Result<VaultSnapshot, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:436:6
    |
436 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/capture/relations_mirror.rs:54:38
   |
54 |   pub(super) fn load_close_policy() -> (
   |  ______________________________________^
55 | |     Vec<config::relations::CancelLabel>,
56 | |     Vec<config::relations::CompleteLabel>,
57 | |     Vec<config::relations::CancelLabel>,
58 | |     Vec<config::relations::CancelLabel>,
59 | |     Option<String>,
60 | | ) {
   | |_^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:159:6
    |
159 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:274:6
    |
274 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:411:6
    |
411 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:440:6
    |
440 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:46:6
   |
46 | ) -> Result<capture_language::ParsedCaptureDraft, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
 --> src/native/capture/sub_bullet.rs:8:6
  |
8 | ) -> Result<CaptureWritePlan, CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sub_bullet.rs:50:6
   |
50 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
  --> src/native/capture/sub_bullet.rs:41:1
   |
41 | / pub(super) fn plan_sub_bullet_capture(
42 | |     planner: &mut CaptureBatchPlanner,
43 | |     bob_dir: &Path,
44 | |     target: &Path,
...  |
49 | |     warnings: &mut Vec<CaptureWarning>,
50 | | ) -> Result<CaptureWritePlan, CaptureError> {
   | |___________________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:231:6
    |
231 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/sub_bullet.rs:221:1
    |
221 | / fn plan_prj_section_capture(
222 | |     planner: &mut CaptureBatchPlanner,
223 | |     bob_dir: &Path,
224 | |     target: &Path,
...   |
230 | |     warnings: &mut Vec<CaptureWarning>,
231 | | ) -> Result<CaptureWritePlan, CaptureError> {
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:507:6
    |
507 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_complete.rs:49:6
   |
49 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:171:6
    |
171 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:920:6
    |
920 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1187:6
     |
1187 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:147:10
    |
147 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/task_theme.rs:138:5
    |
138 | /     pub(super) fn apply_new_task(
139 | |         &mut self,
140 | |         planner: &mut CaptureBatchPlanner,
141 | |         target: &Path,
...   |
146 | |         warnings: &mut Vec<CaptureWarning>,
147 | |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    | |_____________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:187:10
    |
187 |     ) -> Result<AppliedTaskTheme, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:293:10
    |
293 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:307:10
    |
307 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/task_theme.rs:297:5
    |
297 | /     pub(super) fn apply_existing_task(
298 | |         &mut self,
299 | |         planner: &mut CaptureBatchPlanner,
300 | |         target: &Path,
...   |
306 | |         warnings: &mut Vec<CaptureWarning>,
307 | |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    | |_____________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:338:10
    |
338 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:478:10
    |
478 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:601:10
    |
601 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:644:10
    |
644 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:777:10
    |
777 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:824:10
    |
824 |     ) -> Result<Option<usize>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:881:10
    |
881 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1108:10
     |
1108 |     ) -> Result<Option<AppliedMerge>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1172:10
     |
1172 |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/task_theme.rs:1163:5
     |
1163 | /     pub(super) fn relocate_for_retype(
1164 | |         &mut self,
1165 | |         planner: &mut CaptureBatchPlanner,
1166 | |         block_id: &str,
...    |
1171 | |         warnings: &mut Vec<CaptureWarning>,
1172 | |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     | |________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_toggle.rs:19:6
   |
19 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_toggle.rs:447:6
    |
447 | ) -> Result<ToggleRelationPlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/transfer.rs:63:6
   |
63 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:415:6
    |
415 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:441:6
    |
441 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:507:6
    |
507 |   ) -> Result<
    |  ______^
508 | |     (
509 | |         RelationMergeOutput,
510 | |         Vec<crate::native::task_move::transplant::RepairedFile>,
511 | |     ),
512 | |     CaptureError,
513 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:323:44
    |
323 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
    |                                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_active_tasks.rs:331:12
    |
331 |     tasks: &mut Vec<ActiveTask>,
    |            ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
    = note: `#[warn(clippy::ptr_arg)]` on by default
help: change this to
    |
331 -     tasks: &mut Vec<ActiveTask>,
331 +     tasks: &mut [ActiveTask],
    |

warning: this function has too many arguments (9/7)
    --> src/native/capture_complete/candidates.rs:988:1
     |
 988 | / fn relationship_disabled_reason(
 989 | |     bob_dir: &Path,
 990 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
 991 | |     graph: &HashMap<
...    |
1000 | |     blocked_tasks: &[ResolvedRelationshipEntry],
1001 | | ) -> Option<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1620:6
     |
1620 |   ) -> (
     |  ______^
1621 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1622 | |     Vec<String>,
1623 | |     Vec<(String, usize)>,
1624 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
   --> src/native/capture_complete/theme_menu.rs:186:1
    |
186 | / pub(super) fn compose_task_aware(
187 | |     scan: &PomodoroScan,
188 | |     query: &str,
189 | |     catalog: Option<&Catalog>,
...   |
194 | |     next_up_line: Option<usize>,
195 | | ) -> Vec<PomodoroNameCandidate> {
    | |_______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this boolean expression can be simplified
   --> src/native/capture_complete/theme_menu.rs:261:16
    |
261 |               || !row
    |  ________________^
262 | |                 .name
263 | |                 .as_deref()
264 | |                 .is_some_and(|name| normalize_component(name) == key)
    | |_____________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
261 ~             || row
262 +                 .name
263 +                 .as_deref().is_none_or(|name| normalize_component(name) != key)
    |

warning: the loop variable `idx` is used to index `lines`
   --> src/native/capture_drawers.rs:666:16
    |
666 |     for idx in start_idx..end_idx.min(lines.len()) {
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
666 -     for idx in start_idx..end_idx.min(lines.len()) {
666 +     for (idx, <item>) in lines.iter().enumerate().take(end_idx.min(lines.len())).skip(start_idx) {
    |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_drawers.rs:899:35
    |
899 | pub(crate) fn rank_drawer_catalog<'a>(
    |                                   ^^
900 |     records: &'a BTreeMap<String, DrawerCatalogRecord>,
    |               ^^
901 | ) -> Vec<&'a DrawerCatalogRecord> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
899 ~ pub(crate) fn rank_drawer_catalog(
900 ~     records: &BTreeMap<String, DrawerCatalogRecord>,
901 ~ ) -> Vec<&DrawerCatalogRecord> {
    |

warning: called `filter(..).next_back()` on an `DoubleEndedIterator`. This is more succinctly expressed by calling `.rfind(..)` instead
    --> src/native/capture_drawers.rs:1548:5
     |
1548 | /     direct_child_list_indexes(&lines, drawer.line_index(), drawer.block_end)
1549 | |         .into_iter()
1550 | |         .filter(|&index| line_start(&lines, index) < insertion.offset)
1551 | |         .filter(|&index| {
1552 | |             parse_managed_task_log_marker(lines[index].text).is_none()
1553 | |         })
1554 | |         .next_back()
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_next
     = note: `#[warn(clippy::filter_next)]` on by default

warning: redundant guard
   --> src/native/capture_language/close_log.rs:213:23
    |
213 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
    = note: `#[warn(clippy::redundant_guards)]` on by default
help: try
    |
213 -         Some(list) if list.is_empty() => {
213 +         Some([]) => {
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/close_log.rs:511:1
    |
511 | / fn check_index_loggable(
512 | |     index: u32,
513 | |     index_range: (usize, usize),
514 | |     close_token: &str,
...   |
520 | |     complete_all: bool,
521 | | ) -> Result<(), CloseLogError> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:680:1
    |
680 | / pub(crate) fn lex_close_inline_entry_with_all(
681 | |     entry_tokens: &[Token<'_>],
682 | |     close_token: &str,
683 | |     in_progress: Option<&[u32]>,
...   |
688 | |     complete_all: bool,
689 | | ) -> Result<CloseInlineLex, CloseLogError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:918:1
    |
918 | / pub(crate) fn lex_close_log_bullets_with_all(
919 | |     child_lines: &[ItemLine<'_>],
920 | |     close_token: &str,
921 | |     in_progress: Option<&[u32]>,
...   |
926 | |     complete_all: bool,
927 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: casting to the same type is unnecessary (`usize` -> `usize`)
    --> src/native/capture_language/completion.rs:1002:19
     |
1002 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast
     = note: `#[warn(clippy::unnecessary_cast)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:1676:6
     |
1676 |   ) -> Result<
     |  ______^
1677 | |     Vec<(
1678 | |         ParsedCaptureText,
1679 | |         Option<RefParentSource>,
...    |
1682 | |     TemplateCodedError,
1683 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:382:12
    |
382 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
382 -     spans: &mut Vec<Span>,
382 +     spans: &mut [Span],
    |

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:439:12
    |
439 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
439 -     spans: &mut Vec<Span>,
439 +     spans: &mut [Span],
    |

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:722:1
    |
722 | / pub(super) enum TokenParse {
723 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
724 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
725 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
723 -     Marker(MarkerParse),
723 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:1746:1
     |
1746 | / fn empty_editor_item(
1747 | |     item: &CaptureItem<'_>,
1748 | |     mode: EditorMode,
1749 | |     route: Option<String>,
...    |
1754 | |     diagnostics: Vec<Diagnostic>,
1755 | | ) -> EditorItemParse {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:2580:1
     |
2580 | / fn attach_drawer_bullet_metadata(
2581 | |     item: &CaptureItem<'_>,
2582 | |     mode: &mut EditorMode,
2583 | |     parent_body: &str,
...    |
2588 | |     sub_bullets: &mut [AuthoredSubBullet],
2589 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:3171:35
     |
3171 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `#[warn(clippy::trim_split_whitespace)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:3816:5
     |
3816 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:3815:5
     |
3815 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:293:1
    |
293 | / pub(super) fn parse_editor_named_start_item<'a>(
294 | |     item: &CaptureItem<'a>,
295 | |     parent_trimmed: &str,
296 | |     suffix: String,
...   |
302 | |     spelling: NameSpelling,
303 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:105:6
    |
105 |   ) -> Option<
    |  ______^
106 | |     Result<
107 | |         (
108 | |             LineOutcome<'a>,
...   |
113 | |     >,
114 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:198:6
    |
198 |   ) -> Option<
    |  ______^
199 | |     Result<
200 | |         (
201 | |             LineOutcome<'a>,
...   |
206 | |     >,
207 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:1395:5
     |
1395 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1394:5
     |
1394 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/item.rs:1282:35
     |
1282 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:2090:1
     |
2090 | / fn parse_capture_item_masked<'a>(
2091 | |     item: &CaptureItem<'a>,
2092 | |     forced_route: Option<&str>,
2093 | |     forced_section: Option<&str>,
...    |
2098 | |     target_run: Option<&TargetRunContext>,
2099 | | ) -> Result<ParsedCaptureItemOutcome<'a>, String> {
     | |_________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:2412:5
     |
2412 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:2411:5
     |
2411 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: match expression looks like `matches!` macro
    --> src/native/capture_language/item.rs:3747:31
     |
3747 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
3748 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
3749 | |                 (false, '~', Some(b'@')) => true,
3750 | |                 _ => false,
3751 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
3747 -             let want_second = match (name.is_some(), first_sigil, second) {
3748 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
3749 -                 (false, '~', Some(b'@')) => true,
3750 -                 _ => false,
3751 -             };
3747 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:4068:1
     |
4068 | / pub(super) fn named_shape_error_with_drop(
4069 | |     token: &str,
4070 | |     suffix: &str,
4071 | |     name: &str,
...    |
4076 | |     is_literal: bool,
4077 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `expect` on `separator` after checking its variant with `is_some`
   --> src/native/capture_language/relations.rs:689:13
    |
687 |         block_end: if separator.is_some() {
    |                    ---------------------- help: try: `if let Some(<item>) = separator`
688 |             // Block ID ends where `|` starts.
689 |             separator.expect("separator").0
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap
    = note: `#[warn(clippy::unnecessary_unwrap)]` on by default

warning: this boolean expression can be simplified
   --> src/native/capture_language/rewrite.rs:553:8
    |
553 |       if !raw_text[..run_start]
    |  ________^
554 | |         .chars()
555 | |         .next_back()
556 | |         .is_some_and(|before| !before.is_whitespace())
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
553 ~     if raw_text[..run_start]
554 +         .chars()
555 +         .next_back().is_none_or(|before| before.is_whitespace())
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/rewrite.rs:622:1
    |
622 | / fn candidate_selects_plain_marker(
623 | |     candidate: &str,
624 | |     start: usize,
625 | |     end: usize,
...   |
631 | |     id_part: &str,
632 | | ) -> bool {
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` has identical blocks
   --> src/native/capture_language/target_runs.rs:457:51
    |
457 |           } else if is_escaped_priority_token(text) {
    |  ___________________________________________________^
458 | |             break;
459 | |         } else {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/target_runs.rs:459:16
    |
459 |           } else {
    |  ________________^
460 | |             break;
461 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else
    = note: `#[warn(clippy::if_same_then_else)]` on by default

warning: redundant guard
    --> src/native/capture_language/tokens.rs:1366:43
     |
1366 |                 Some((after_x, x_len)) if after_x.is_empty() => {
     |                                           ^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
     |
1366 -                 Some((after_x, x_len)) if after_x.is_empty() => {
1366 +                 Some(("", x_len)) => {
     |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_language/transfer.rs:467:6
    |
104 | /     Valid {
105 | |         sources: Vec<TransferSource>,
106 | |         arrow: TransferArrow,
107 | |         destination: TransferDestination,
108 | |     },
    | |_____- the largest variant contains at least 184 bytes
...
467 |   ) -> Result<TransferSource, TransferScan> {
    |        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_language::transfer::TransferScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::transfer::TransferScan>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: stripping a prefix manually
   --> src/native/capture_language/transfer.rs:474:20
    |
474 |         let rest = &text[1..];
    |                    ^^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_language/transfer.rs:473:5
    |
473 |     if text.starts_with('@') {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
    = note: `#[warn(clippy::manual_strip)]` on by default
help: try using the `strip_prefix` method
    |
473 ~     if let Some(rest) = text.strip_prefix('@') {
474 ~         if let Some(plus) = rest.find('+') {
    |

warning: this `if` has identical blocks
   --> src/native/capture_language/type_marker.rs:454:45
    |
454 |           } else if lex.decoded.contains('+') {
    |  _____________________________________________^
455 | |             (
456 | |                 TypeMarkerOccurrence::Invalid {
457 | |                     span: start..raw_end,
...   |
462 | |         } else if marker_end != raw_end {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/type_marker.rs:462:41
    |
462 |           } else if marker_end != raw_end {
    |  _________________________________________^
463 | |             (
464 | |                 TypeMarkerOccurrence::Invalid {
465 | |                     span: start..raw_end,
...   |
470 | |         } else {
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_pomodoro_close/ledger.rs:576:24
    |
576 |       let Some(anchor) = scan
    |  ________________________^
577 | |         .entries
578 | |         .iter()
579 | |         .filter(|entry| {
...   |
582 | |         })
583 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
583 -         .last()
583 +         .next_back()
    |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:154:1
    |
154 | / pub(crate) enum PomodoroCloseOutcome {
155 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 688 bytes
156 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
157 | | }
    | |_^ the entire enum is at least 688 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
155 -     Close(PomodoroClosePlan),
155 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:318:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
318 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:365:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
365 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:553:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
553 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:570:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
570 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:590:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
590 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:613:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
613 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:676:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
676 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:749:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
749 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:903:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
903 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:981:6
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
981 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1006:6
     |
 149 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1006 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1294:1
     |
1294 | / fn resolve_close_clock_fact<V: CloseVault, S: HomeSource>(
1295 | |     vault: &V,
1296 | |     resolver: &mut HomeResolver<S>,
1297 | |     events: &[EventNoteRow],
...    |
1303 | |     all_settings: &NoteTaskSettings,
1304 | | ) -> CloseClockFact {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1707:6
     |
 149 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1707 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture_pomodoro_start.rs:349:1
    |
349 | / fn resolve_clock_fact<V: CloseVault + ?Sized, S: HomeSource>(
350 | |     vault: Option<&V>,
351 | |     resolver: Option<&mut HomeResolver<S>>,
352 | |     events: &[EventNoteRow],
...   |
357 | |     all_settings: &note_tasks::NoteTaskSettings,
358 | | ) -> CountedLinkFact {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
   --> src/native/capture_related/corpus.rs:163:1
    |
163 | / fn collect_from_note(
164 | |     _bob_dir: &Path,
165 | |     relative: &str,
166 | |     absolute: &Path,
...   |
176 | |     _warnings: &mut Vec<String>,
177 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/corpus.rs:256:1
    |
256 | / fn collect_from_archives(
257 | |     bob_dir: &Path,
258 | |     settings: &note_tasks::NoteTaskSettings,
259 | |     today: NaiveDate,
...   |
264 | |     warnings: &mut Vec<String>,
265 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:449:1
    |
449 | / fn draft_match(
450 | |     ranked: bands::RankedMatch<'_>,
451 | |     item: &EditorItemParse,
452 | |     draft: &str,
...   |
457 | |     index: &NoteIndex,
458 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:580:1
    |
580 | / fn verify_link_action(
581 | |     action: &str,
582 | |     item: &EditorItemParse,
583 | |     draft: &str,
...   |
588 | |     options: &EditorParseOptions<'_>,
589 | | ) -> bool {
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` has identical blocks
   --> src/native/capture_related/tokenize.rs:260:54
    |
260 |           if prev.is_lowercase() && cur.is_uppercase() {
    |  ______________________________________________________^
261 | |             starts.push(chars[i].0);
262 | |         } else if prev.is_uppercase()
    | |_________^
    |
note: same as this
   --> src/native/capture_related/tokenize.rs:265:9
    |
265 | /         {
266 | |             starts.push(chars[i].0);
267 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: stripping a prefix manually
   --> src/native/capture_related/tokenize.rs:382:21
    |
382 |         let close = rest[2..].find("]]")?;
    |                     ^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_related/tokenize.rs:381:5
    |
381 |     if rest.starts_with("[[") {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_prefix` method
    |
381 ~     if let Some(<stripped>) = rest.strip_prefix("[[") {
382 ~         let close = <stripped>.find("]]")?;
    |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_task_toggle/ledger.rs:322:49
    |
322 | pub(crate) fn default_pomodoro_link_destination<'a>(
    |                                                 ^^
323 |     scan: &'a capture_pomodoros::PomodoroScan,
    |            ^^
324 |     queue_owner_line: Option<usize>,
325 | ) -> Option<&'a capture_pomodoros::PomodoroEntry> {
    |              ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
    |
322 ~ pub(crate) fn default_pomodoro_link_destination(
323 ~     scan: &capture_pomodoros::PomodoroScan,
324 |     queue_owner_line: Option<usize>,
325 ~ ) -> Option<&capture_pomodoros::PomodoroEntry> {
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_task_toggle/relocation.rs:523:18
    |
523 |       let anchor = scan
    |  __________________^
524 | |         .entries
525 | |         .iter()
526 | |         .filter(|entry| entry.state == PomodoroState::Open)
527 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
527 -         .last()
527 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
  --> src/native/capture_task_wikilinks.rs:79:5
   |
79 | /     wikilink_task_tokens(raw)
80 | |         .into_iter()
81 | |         .filter_map(|token| field_at_token(raw, token, cursor))
82 | |         .last()
   | |_______________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
   |
82 -         .last()
82 +         .next_back()
   |

warning: match expression looks like `matches!` macro
   --> src/native/gcal/bullet_block.rs:145:5
    |
145 | /     match structural_depth(spans, row_index, end) {
146 | |         Some(depth) if depth >= 2 => false,
147 | |         _ => true,
148 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
help: use `matches!` directly
    |
145 -     match structural_depth(spans, row_index, end) {
146 -         Some(depth) if depth >= 2 => false,
147 -         _ => true,
148 -     }
145 +     !matches!(structural_depth(spans, row_index, end), Some(depth) if depth >= 2)
    |

warning: the loop variable `index` is used to index `lines`
   --> src/native/gcal/bullet_block.rs:159:18
    |
159 |     for index in start..end {
    |                  ^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
159 -     for index in start..end {
159 +     for (index, <item>) in lines.iter().enumerate().take(end).skip(start) {
    |

warning: methods called `from_*` usually take no `self`
  --> src/native/gcal/classify.rs:50:32
   |
50 |     pub(crate) fn from_rfc3339(&self) -> String {
   |                                ^^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention

warning: this `if` has identical blocks
   --> src/native/gcal/description.rs:477:45
    |
477 |       let first_ok = if first.is_alphabetic() {
    |  _____________________________________________^
478 | |         true
479 | |     } else if !first.is_ascii()
    | |_____^
    |
note: same as this
   --> src/native/gcal/description.rs:481:5
    |
481 | /     {
482 | |         true
483 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: this if-then-else expression returns a bool literal
   --> src/native/gcal/description.rs:479:12
    |
479 |       } else if !first.is_ascii()
    |  ____________^
480 | |         && !matches!(first, '\u{2010}'..='\u{2015}' | '\u{2212}')
481 | |     {
482 | |         true
483 | |     } else {
484 | |         false
485 | |     };
    | |_____^ help: you can reduce it to: `{ !first.is_ascii() && !matches!(first, '\u{2010}'..='\u{2015}' | '\u{2212}') }`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_bool
    = note: `#[warn(clippy::needless_bool)]` on by default

warning: this `if` has identical blocks
   --> src/native/gcal/diagnostics.rs:98:55
    |
 98 |       let inherited_advice: Option<String> = if on_wins {
    |  _______________________________________________________^
 99 | |         None
100 | |     } else if !input.root_only_off_clock {
    | |_____^
    |
note: same as this
   --> src/native/gcal/diagnostics.rs:100:42
    |
100 |       } else if !input.root_only_off_clock {
    |  __________________________________________^
101 | |         None
102 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/gcal/journal.rs:130:6
    |
130 |   ) -> std::io::Result<(
    |  ______^
131 | |     BTreeMap<(String, String), OccurrenceState>,
132 | |     Vec<String>,
133 | |     Option<(DateTime<FixedOffset>, String)>,
134 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: large size difference between variants
   --> src/native/gcal/journal.rs:178:1
    |
178 | / enum Update {
179 | |     Row(RowRecord),
    | |     -------------- the largest variant contains at least 264 bytes
180 | |     Link,
181 | |     Gone,
182 | |     Flag(String),
    | |     ------------ the second-largest variant contains at least 24 bytes
183 | | }
    | |_^ the entire enum is at least 264 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
179 -     Row(RowRecord),
179 +     Row(Box<RowRecord>),
    |

warning: enclosing `Some` and `?` operator are unneeded
   --> src/native/gcal/lifecycle.rs:241:5
    |
241 |     Some(text.get(..open)?)
    |     ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_question_mark
    = note: `#[warn(clippy::needless_question_mark)]` on by default
help: remove the enclosing `Some` and `?` operator
    |
241 -     Some(text.get(..open)?)
241 +     text.get(..open)
    |

warning: consider using `sort_by_key`
   --> src/native/gcal/login.rs:638:5
    |
638 |     paths.sort_by(|a, b| b.0.cmp(&a.0));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
    = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
    |
638 -     paths.sort_by(|a, b| b.0.cmp(&a.0));
638 +     paths.sort_by_key(|b| std::cmp::Reverse(b.0));
    |

warning: replacing a value of type `T` with `T::default()` is better expressed using `std::mem::take`
  --> src/native/gcal/render.rs:83:22
   |
83 |     let mut suffix = std::mem::replace(&mut spans.suffix, String::new());
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `std::mem::take(&mut spans.suffix)`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#mem_replace_with_default
   = note: `#[warn(clippy::mem_replace_with_default)]` on by default

warning: this boolean expression can be simplified
   --> src/native/gcal/render.rs:190:5
    |
190 | /     !result
191 | |         .suggestion
192 | |         .is_some_and(|suggestion| suggestion.theme.name == "MEET")
    | |__________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
190 ~     result
191 +         .suggestion.is_none_or(|suggestion| suggestion.theme.name != "MEET")
    |

warning: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
    --> src/native/gcal/sync.rs:1248:47
     |
1248 | fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
     |                                               ^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
1248 - fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
1248 + fn display_rel(vault: &std::path::Path, path: &Path) -> String {
     |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/gkeep/imports.rs:422:26
    |
422 | pub(super) fn unfinished<'a>(
    |                          ^^
423 |     files: &'a [(PathBuf, TransactionFile)],
    |             ^^
424 | ) -> Vec<&'a (PathBuf, TransactionFile)> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
    |
422 ~ pub(super) fn unfinished(
423 ~     files: &[(PathBuf, TransactionFile)],
424 ~ ) -> Vec<&(PathBuf, TransactionFile)> {
    |

warning: consider using `sort_by_key`
    --> src/native/gkeep/migrate_tasks.rs:1952:5
     |
1952 |     ordered.sort_by(|left, right| right.start.cmp(&left.start));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
     |
1952 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1952 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.start));
     |

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1979:1
     |
1979 | / pub(super) fn stamp_overwrite_source(
1980 | |     config: &Config,
1981 | |     plan: &OverwritePreflight,
1982 | |     options: &CreateOptions,
...    |
1987 | |     info: &PdfInfo,
1988 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2021:1
     |
2021 | / pub(super) fn stage_overwrite_audio(
2022 | |     options: &CreateOptions,
2023 | |     plan: &OverwritePreflight,
2024 | |     request: &OverwriteRequest,
...    |
2029 | |     title: &str,
2030 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2703:1
     |
2703 | / fn plan_target_for(
2704 | |     config: &Config,
2705 | |     stem: &str,
2706 | |     ref_type: &str,
...    |
2711 | |     source_display: &str,
2712 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3711:1
     |
3711 | / fn stage_overwrite_source_store(
3712 | |     _config: &Config,
3713 | |     plan: &OverwritePreflight,
3714 | |     scratch: &Path,
...    |
3721 | |     catalog: &super::code_catalog::CatalogOutcome,
3722 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4392:1
     |
4392 | / fn overwrite_pdf_url(
4393 | |     config: &Config,
4394 | |     url: super::clip_url::WebUrl,
4395 | |     downloaded: PathBuf,
...    |
4400 | |     selection: &OverwriteSelection,
4401 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4473:1
     |
4473 | / fn create_pdf_url_route(
4474 | |     config: &Config,
4475 | |     url: super::clip_url::WebUrl,
4476 | |     downloaded: PathBuf,
...    |
4481 | |     listen: Option<&super::listen::ListenCommand>,
4482 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5207:1
     |
5207 | / fn print_pdf_dry_run(
5208 | |     config: &Config,
5209 | |     styler: &Styler,
5210 | |     source_display: &str,
...    |
5218 | |     legacy: &[sources_mod::RecordedSource],
5219 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:5443:1
     |
5443 | / fn compose_markdown_marker(
5444 | |     status: &str,
5445 | |     parent: &str,
5446 | |     title: &str,
...    |
5451 | |     return_links: bool,
5452 | | ) -> Result<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/attach.rs:332:1
    |
332 | / pub(super) fn run_attach(
333 | |     config: &Config,
334 | |     listen: &ListenCommand,
335 | |     attach: &AttachTarget,
...   |
340 | |     scratch: &mut super::ScratchDir,
341 | | ) -> Result<()> {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: clamp-like pattern without using clamp function
   --> src/native/highlights_ref/clip_adapter.rs:763:5
    |
763 | /     DIAGRAM_TIMEOUT_BASE_SECS
764 | |         .saturating_add(
765 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
768 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
763 ~     DIAGRAM_TIMEOUT_BASE_SECS
764 +         .saturating_add(
765 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
766 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:736:1
    |
736 | / pub(super) enum PdfSyncOutcome {
737 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
738 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
739 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
737 -     Written(SyncWriteReport),
737 +     Written(Box<SyncWriteReport>),
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:808:1
    |
808 | / pub(super) enum ScanWriteOutcome {
809 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
810 | |     Held(ScanHold),
811 | |     Failed(ScanFailure),
    | |     ------------------- the second-largest variant contains at least 144 bytes
812 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
809 -     Written(SyncWriteReport),
809 +     Written(Box<SyncWriteReport>),
    |

warning: this function has too many arguments (9/7)
  --> src/native/highlights_ref/note_snapshot/plan.rs:64:1
   |
64 | / pub(crate) fn plan_snapshot<L: SourceLoader>(
65 | |     store: &mut SourceStore<L>,
66 | |     note: ClassifiedNote,
67 | |     settings: &TasksSettings,
...  |
73 | |     parent_default_reason: Option<String>,
74 | | ) -> Result<SnapshotPlan, String> {
   | |_________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/note_snapshot/bob.rs:1121:1
     |
1121 | / fn push_schedule_group(
1122 | |     blocks: &mut Vec<Block>,
1123 | |     source: &SourceIdentity,
1124 | |     level: HeadingLevel,
...    |
1129 | |     used_ids: &mut BTreeSet<String>,
1130 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: methods called `as_*` usually take `self` by reference or `self` by mutable reference
  --> src/native/highlights_ref/note_snapshot/classify.rs:54:32
   |
54 |     pub(crate) const fn as_str(self) -> &'static str {
   |                                ^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention

warning: large size difference between variants
   --> src/native/highlights_ref/note_snapshot/serialize.rs:121:1
    |
121 | / enum InlineFlowPart {
122 | |     Inlines(Vec<Inline>),
    | |     -------------------- the second-largest variant contains at least 24 bytes
123 | |     Block(Block),
    | |     ------------ the largest variant contains at least 336 bytes
124 | | }
    | |_^ the entire enum is at least 336 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
123 -     Block(Block),
123 +     Block(Box<Block>),
    |

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:416:17
    |
416 |         blocks: &mut Vec<Block>,
    |                 ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
416 -         blocks: &mut Vec<Block>,
416 +         blocks: &mut [Block],
    |

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:607:21
    |
607 |                     *block = Box::new(expanded);
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace existing content with inner value instead: `**block = expanded`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box
    = note: `#[warn(clippy::replace_box)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:872:10
    |
872 |       ) -> (
    |  __________^
873 | |         BTreeMap<(AnchorIdentity, String), SnapshotAnchor>,
874 | |         BTreeMap<AnchorIdentity, String>,
875 | |         Vec<SnapshotAnchor>,
876 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1195:1
     |
1195 | / fn compose_bob_masthead<L: SourceLoader>(
1196 | |     masthead: &mut SnapshotMasthead,
1197 | |     source: &SourceIdentity,
1198 | |     kind: &NoteKind,
...    |
1205 | |     settings: &TasksSettings,
1206 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/visibility.rs:198:21
    |
198 | /                     *inner = Box::new(
199 | |                         nested.into_iter().next().expect("embedded block"),
200 | |                     );
    | |_____________________^ help: replace existing content with inner value instead: `**inner = nested.into_iter().next().expect("embedded block")`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/pdf_target.rs:128:1
    |
128 | / pub(super) fn plan_pdf_url(
129 | |     url: &WebUrl,
130 | |     downloaded: &Path,
131 | |     name_override: Option<&str>,
...   |
136 | |     progress: Option<&dyn Fn(&str)>,
137 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:213:1
    |
213 | / pub(super) fn plan_arxiv(
214 | |     paper: &ArxivPaper,
215 | |     name_override: Option<&str>,
216 | |     title_override: Option<&str>,
...   |
222 | |     progress: Option<&dyn Fn(&str)>,
223 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:757:1
    |
757 | / pub(super) fn preflight_for_url(
758 | |     config: &Config,
759 | |     rows: &[RefRow],
760 | |     recorded: &[RecordedSource],
...   |
765 | |     title_fallback: &str,
766 | | ) -> Result<Option<RereadPreflight>, CommandError> {
    | |__________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:804:1
    |
804 | / pub(super) fn preflight_for_url_outcome(
805 | |     config: &Config,
806 | |     rows: &[RefRow],
807 | |     recorded: &[RecordedSource],
...   |
812 | |     title_fallback: &str,
813 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this boolean expression can be simplified
   --> src/native/highlights_ref/recapture.rs:881:9
    |
881 | /         hit.dedupe_key == final_dedupe
882 | |             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 | |                 || !hit.is_ref_note)
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
881 -         hit.dedupe_key == final_dedupe
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
881 +         !(hit.dedupe_key != final_dedupe || hit.is_ref_note && hit.source_pdf.is_none())
    |
881 -         hit.dedupe_key == final_dedupe
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
881 +         (hit.source_pdf.is_some() || !hit.is_ref_note) && hit.dedupe_key == final_dedupe
    |

warning: this boolean expression can be simplified
   --> src/native/highlights_ref/recapture.rs:882:16
    |
882 |               && ((hit.is_ref_note && hit.source_pdf.is_some())
    |  ________________^
883 | |                 || !hit.is_ref_note)
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
882 +             && !(hit.is_ref_note && hit.source_pdf.is_none())
    |
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
882 +             && !hit.is_ref_note || hit.source_pdf.is_some()
    |

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:912:1
    |
912 | / pub(super) fn preflight_for_stem(
913 | |     config: &Config,
914 | |     rows: &[RefRow],
915 | |     stem: &str,
...   |
920 | |     identity: StemIdentity<'_>,
921 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/highlights_ref/recapture.rs:980:1
    |
980 | / fn url_selection_from_selection(
981 | |     config: &Config,
982 | |     family: SelectedFamily,
983 | |     name: Option<&str>,
...   |
990 | |     overwrite_enabled: bool,
991 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/recapture.rs:1006:1
     |
1006 | / fn url_reread_from_selection(
1007 | |     config: &Config,
1008 | |     family: SelectedFamily,
1009 | |     name: Option<&str>,
...    |
1015 | |     attach_available: bool,
1016 | | ) -> Result<Option<RereadPreflight>, CommandError> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/recapture.rs:1042:1
     |
1042 | / fn finish_selection(
1043 | |     config: &Config,
1044 | |     family: SelectedFamily,
1045 | |     name: Option<&str>,
...    |
1052 | |     overwrite_enabled: bool,
1053 | | ) -> Result<CaptureOutcome, CommandError> {
     | |_________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this boolean expression can be simplified
    --> src/native/highlights_ref/recapture.rs:1366:9
     |
1366 | /         hit.dedupe_key == final_dedupe
1367 | |             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 | |                 || !hit.is_ref_note)
     | |____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
1366 -         hit.dedupe_key == final_dedupe
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1366 +         !(hit.dedupe_key != final_dedupe || hit.is_ref_note && hit.source_pdf.is_none())
     |
1366 -         hit.dedupe_key == final_dedupe
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1366 +         (hit.source_pdf.is_some() || !hit.is_ref_note) && hit.dedupe_key == final_dedupe
     |

warning: this boolean expression can be simplified
    --> src/native/highlights_ref/recapture.rs:1367:16
     |
1367 |               && ((hit.is_ref_note && hit.source_pdf.is_some())
     |  ________________^
1368 | |                 || !hit.is_ref_note)
     | |____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1367 +             && !(hit.is_ref_note && hit.source_pdf.is_none())
     |
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1367 +             && !hit.is_ref_note || hit.source_pdf.is_some()
     |

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/overwrite/execute.rs:338:1
    |
338 | / fn overwrite_inside_accessor(
339 | |     config: &Config,
340 | |     locked: &OverwritePreflight,
341 | |     request: &OverwriteRequest,
...   |
347 | |     mut pdf_move: Option<&mut MoveContext<'_>>,
348 | | ) -> Result<OverwriteResult, CommandError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/overwrite/recovery.rs:1187:1
     |
1187 | / fn plan_endpoint_pair(
1188 | |     vault: &Path,
1189 | |     intent: &OverwriteIntent,
1190 | |     source: &Path,
...    |
1196 | |     plan: &mut ReversalPlan,
1197 | | ) -> std::result::Result<(), CommandError> {
     | |__________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/highlights_ref/overwrite/recovery.rs:1304:16
     |
1304 |     reversals: Vec<(PathBuf, PathBuf, Option<String>, Option<String>, bool)>,
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1178:1
     |
1178 | / pub(super) fn render_fresh_skeleton(
1179 | |     config: &Config,
1180 | |     note_rel: &str,
1181 | |     pdf: &Path,
...    |
1186 | |     audio_path: Option<&Path>,
1187 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1370:1
     |
1370 | / fn render_frozen_note(
1371 | |     old_contents: &str,
1372 | |     live_note: &str,
1373 | |     date: &str,
...    |
1378 | |     annotated: Option<FrozenAnnotated<'_>>,
1379 | | ) -> Result<String, String> {
     | |___________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1472:1
     |
1472 | / fn frozen_body(
1473 | |     body: &str,
1474 | |     live_note: &str,
1475 | |     title: &str,
...    |
1480 | |     annotated_pdf: Option<&str>,
1481 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (14/7)
    --> src/native/highlights_ref/overwrite.rs:1565:1
     |
1565 | / fn plan_annotated_archive(
1566 | |     config: &Config,
1567 | |     live_note: &str,
1568 | |     ref_type: &str,
...    |
1579 | |     assets_relative: Option<&Path>,
1580 | | ) -> Result<AnnotatedArchivePlan, OverwriteRefusal> {
     | |___________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/sidecar.rs:318:1
    |
318 | / pub(super) fn flush_sidecar_chunk(
319 | |     annotations: &mut Vec<SidecarAnnotation>,
320 | |     chunk: &mut Vec<String>,
321 | |     page_label: Option<&str>,
...   |
326 | |     page_ordinals: &mut BTreeMap<String, usize>,
327 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/sidecar_render.rs:308:29
    |
308 | ...                   &[member_text_key.clone()],
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&member_text_key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs
    = note: `#[warn(clippy::cloned_ref_to_slice_refs)]` on by default

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/sidecar_render.rs:1267:1
     |
1267 | / fn append_resolved_image_notes(
1268 | |     config: &Config,
1269 | |     ref_note_path: &Path,
1270 | |     annotation_order: usize,
...    |
1276 | |     image_asset_writes_by_dest: &mut BTreeMap<PathBuf, ImageAssetWrite>,
1277 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/sidecar_render.rs:2482:1
     |
2482 | / pub(super) fn render_annotation_block(
2483 | |     config: &Config,
2484 | |     ref_note_path: &Path,
2485 | |     annotation: &SidecarAnnotation,
...    |
2490 | |     strip_return_links: bool,
2491 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/source_store.rs:1129:1
     |
1129 | / pub(super) fn write_for_create(
1130 | |     config: &super::model::Config,
1131 | |     target_plan: &super::stamp::TargetPlan,
1132 | |     installed_pdf: &std::path::Path,
...    |
1138 | |     catalog: &CatalogOutcome,
1139 | | ) -> Option<StoreWriteOutcome> {
     | |______________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: all variants have the same postfix: `Host`
  --> src/native/highlights_ref/underline.rs:20:1
   |
20 | / pub(super) enum StandaloneUnderlineReason {
21 | |     NoHost,
22 | |     AmbiguousHost { hosts: usize },
23 | |     RepeatedInHost,
24 | | }
   | |_^
   |
   = help: remove the postfixes and use full paths to the variants instead of glob imports
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#enum_variant_names
   = note: `#[warn(clippy::enum_variant_names)]` on by default

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:125:5
    |
125 |     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
125 -     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
125 +     rows.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: this `if` has identical blocks
   --> src/native/periods/note.rs:317:57
    |
317 |               if !name.is_empty() && !name.contains("  ") {
    |  _________________________________________________________^
318 | |                 current = Some(name);
319 | |             } else if !name.is_empty() {
    | |_____________^
    |
note: same as this
   --> src/native/periods/note.rs:319:40
    |
319 |               } else if !name.is_empty() {
    |  ________________________________________^
320 | |                 current = Some(name);
321 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/periods/report.rs:1092:6
     |
1092 | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (9/7)
   --> src/native/plugins/sync.rs:140:1
    |
140 | / fn sync_one_plugin(
141 | |     options: &SyncOptions,
142 | |     id: &str,
143 | |     repo_plugin_dir: &Path,
...   |
149 | |     issues: &mut Vec<String>,
150 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (15/7)
   --> src/native/plugins/sync.rs:231:1
    |
231 | / fn apply_plugin(
232 | |     options: &SyncOptions,
233 | |     id: &str,
234 | |     captured: &CapturedPlugin,
...   |
246 | |     issues: &mut Vec<String>,
247 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: consider using `sort_by_key`
  --> src/native/pomodoro_homes/label.rs:21:5
   |
21 |     ranked.sort_by(|left, right| right.share.cmp(&left.share));
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
   |
21 -     ranked.sort_by(|left, right| right.share.cmp(&left.share));
21 +     ranked.sort_by_key(|right| std::cmp::Reverse(right.share));
   |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/pomodoro_homes/resolve.rs:467:25
    |
467 | /                         chain[nearest_home..end]
468 | |                             .iter()
469 | |                             .filter(|(_, facts)| {
470 | |                                 facts.kind == NoteKind::Project
471 | |                             })
472 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
472 -                             .last()
472 +                             .next_back()
    |

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/pomodoro_themes/cache.rs:217:6
    |
217 |   ) -> Option<(
    |  ______^
218 | |     BTreeMap<String, ThemeRecord>,
219 | |     BTreeMap<NaiveDate, BTreeSet<String>>,
220 | |     Vec<String>,
221 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
   --> src/native/pomodoro_themes/hints.rs:250:1
    |
250 | / fn suggested_hue(
251 | |     moved: &ThemeRecord,
252 | |     current: Hue,
253 | |     window_days: &[(&NaiveDate, &BTreeSet<String>)],
...   |
258 | |     themes: Option<&crate::native::config::ThemesConfig>,
259 | | ) -> Option<Hue> {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:100:13
    |
100 | /             match rename_entry(day_contents, entry.line, &new_name) {
101 | |                 Some(updated) => Some((
102 | |                     updated,
103 | |                     TypeRelocation {
...   |
113 | |                 None => None,
114 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
    = note: `#[warn(clippy::manual_map)]` on by default
help: try
    |
100 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
101 +                     updated,
102 +                     TypeRelocation {
103 +                         outcome: "rename_entry",
104 +                         from,
105 +                         to: new_name,
106 +                         source_before: line,
107 +                         dest_before: Some(line),
108 +                         dest_after: line,
109 +                         dest_created: false,
110 +                     },
111 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:120:13
    |
120 | /             match rename_entry(day_contents, entry.line, &new_name) {
121 | |                 Some(updated) => Some((
122 | |                     updated,
123 | |                     TypeRelocation {
...   |
133 | |                 None => None,
134 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
120 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
121 +                     updated,
122 +                     TypeRelocation {
123 +                         outcome: "rename_placeholder",
124 +                         from,
125 +                         to: new_name,
126 +                         source_before: line,
127 +                         dest_before: Some(line),
128 +                         dest_after: line,
129 +                         dest_created: false,
130 +                     },
131 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:140:13
    |
140 | /             match rename_entry(day_contents, entry.line, &new_name) {
141 | |                 Some(updated) => Some((
142 | |                     updated,
143 | |                     TypeRelocation {
...   |
153 | |                 None => None,
154 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
140 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
141 +                     updated,
142 +                     TypeRelocation {
143 +                         outcome: "append_component",
144 +                         from,
145 +                         to: new_name,
146 +                         source_before: line,
147 +                         dest_before: Some(line),
148 +                         dest_after: line,
149 +                         dest_created: false,
150 +                     },
151 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:205:13
    |
205 | /             match create_below_and_move(
206 | |                 day_contents,
207 | |                 source_entry.line,
208 | |                 link.line_index,
...   |
224 | |                 None => None,
225 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
205 ~             create_below_and_move(
206 +                 day_contents,
207 +                 source_entry.line,
208 +                 link.line_index,
209 +                 link.subtree_end,
210 +                 &name,
211 +             ).map(|updated| (
212 +                     updated,
213 +                     TypeRelocation {
214 +                         outcome: "create_below",
215 +                         from: from_name,
216 +                         to: name,
217 +                         source_before: source_index,
218 +                         dest_before: None,
219 +                         dest_after,
220 +                         dest_created: true,
221 +                     },
222 +                 ))
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/projects/sync.rs:914:28
    |
914 |       if let Some(depends) = sub_block
    |  ____________________________^
915 | |         .lines
916 | |         .iter()
917 | |         .filter(|line| is_direct_prj_dependency_line(sub_block, line))
918 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
918 -         .last()
918 +         .next_back()
    |

warning: this function has too many arguments (8/7)
   --> src/native/ref_jobs/worker.rs:455:5
    |
455 | /     fn record_done(
456 | |         &self,
457 | |         job: &JobFile,
458 | |         outcome: DoneOutcome,
...   |
463 | |         fallback_target: Option<String>,
464 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/ref_library/code.rs:236:1
    |
236 | / fn render_human(
237 | |     title: &str,
238 | |     path: &str,
239 | |     total_bytes: usize,
...   |
244 | |     hint_number: Option<u32>,
245 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `unwrap` on `page` after checking its variant with `is_some`
   --> src/native/ref_library/code.rs:587:47
    |
586 |     if blocks.is_empty() && page.is_some() {
    |                             -------------- the check is happening here
587 |         println!("no code blocks on page {}", page.unwrap());
    |                                               ^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

warning: the `Err`-variant returned from this function is very large
   --> src/native/ref_library/today.rs:351:6
    |
351 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/ref_library/today.rs:827:1
    |
827 | / fn fail(
828 | |     format: Format,
829 | |     dry_run: bool,
830 | |     code: &str,
...   |
835 | |     listing: &TodayListing,
836 | | ) -> i32 {
    | |________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `format!` in `format!` args
   --> src/native/ref_library/migrate_tasks/plan.rs:985:20
    |
985 |               return format!(
    |  ____________________^
986 | |                 "{}{}",
987 | |                 &line[..caret + 1],
988 | |                 format!("{new_id}{}", &line[trimmed_end..])
989 | |             );
    | |_____________^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: doc list item without indentation
   --> src/native/ref_library/mod.rs:919:5
    |
919 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
919 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
    |     ++

warning: the loop variable `index` is used to index `lines`
  --> src/native/ref_tasks/embed.rs:76:22
   |
76 |         for index in start..end.min(lines.len()) {
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
   |
76 -         for index in start..end.min(lines.len()) {
76 +         for (index, <item>) in lines.iter().enumerate().take(end.min(lines.len())).skip(start) {
   |

warning: the loop variable `index` is used to index `lines`
   --> src/native/ref_tasks/embed.rs:118:18
    |
118 |     for index in start..end.min(lines.len()) {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
118 -     for index in start..end.min(lines.len()) {
118 +     for (index, <item>) in lines.iter().enumerate().take(end.min(lines.len())).skip(start) {
    |

warning: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
    = note: `#[warn(clippy::explicit_counter_loop)]` on by default

warning: doc list item without indentation
   --> src/native/relation_labels/scan.rs:288:5
    |
288 | /// Every I/O failure is ignored: the sweep never fails a scan.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
help: indent this line
    |
288 | ///   Every I/O failure is ignored: the sweep never fails a scan.
    |     ++

warning: `format!` in `format!` args
   --> src/native/relation_labels/cli.rs:607:22
    |
607 |       let mut counts = format!(
    |  ______________________^
608 | |         "{} {} {} {} {} {}",
609 | |         report.counts.labels,
610 | |         label_word(report.counts.labels),
...   |
614 | |         format!("{} hidden", report.counts.hidden,),
615 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: consider using `sort_by_key`
   --> src/native/relation_labels/rename.rs:843:5
    |
843 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
843 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
843 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

warning: this function has too many arguments (9/7)
   --> src/native/stats/typical.rs:191:1
    |
191 | / pub(crate) fn period_typical_detail(
192 | |     kind: &str,
193 | |     display: Option<&str>,
194 | |     window: &str,
...   |
200 | |     in_progress: bool,
201 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: match expression looks like `matches!` macro
  --> src/native/style.rs:20:5
   |
20 | /     match bob_env::var_os("CLICOLOR_FORCE") {
21 | |         Some(value) if !value.is_empty() && value != "0" => true,
22 | |         _ => false,
23 | |     }
   | |_____^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
help: use `matches!` directly
   |
20 -     match bob_env::var_os("CLICOLOR_FORCE") {
21 -         Some(value) if !value.is_empty() && value != "0" => true,
22 -         _ => false,
23 -     }
20 +     matches!(bob_env::var_os("CLICOLOR_FORCE"), Some(value) if !value.is_empty() && value != "0")
   |

warning: consider using `sort_by_key`
   --> src/native/task_cancel/prune.rs:192:9
    |
192 |         edits.sort_by(|left, right| right.0.cmp(&left.0));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
192 -         edits.sort_by(|left, right| right.0.cmp(&left.0));
192 +         edits.sort_by_key(|right| std::cmp::Reverse(right.0));
    |

warning: this lifetime isn't used in the function definition
   --> src/native/task_cancel/prune.rs:271:22
    |
271 | fn is_dedicated_line<'a>(
    |                      ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extra_unused_lifetimes
    = note: `#[warn(clippy::extra_unused_lifetimes)]` on by default

warning: this boolean expression can be simplified
   --> src/native/task_complete/keep_moving.rs:604:9
    |
604 |         !task.scheduled.is_some_and(|date| date > today)
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `task.scheduled.is_none_or(|date| date <= today)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool

warning: this function has too many arguments (9/7)
   --> src/native/task_complete/project_pull_in.rs:932:1
    |
932 | / fn emit_keep_moving_recover(
933 | |     plan: &mut SuccessorPlan,
934 | |     completed: &[CompletedTask],
935 | |     day_task_lines: &BTreeMap<String, usize>,
...   |
941 | |     reason: &'static str,
942 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/task_complete/relation_successors/classify.rs:529:1
    |
529 | / fn resolve_edge<R: TargetNoteReader>(
530 | |     source_path: &Path,
531 | |     source: &TaskLine,
532 | |     entry: &RelationEntry,
...   |
537 | |     reader: &mut R,
538 | | ) -> Option<ResolvedEdge> {
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/task_complete/relation_successors/classify.rs:623:1
    |
623 | / fn classify_source<R: TargetNoteReader>(
624 | |     input: &RelationClassifyInput<'_>,
625 | |     source: &SourceHit,
626 | |     triggering: &[TriggeringEvent],
...   |
631 | |     baseline: Option<&DayView>,
632 | | ) -> SourceClass {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/task_complete/successors.rs:877:1
    |
877 | / fn effective_relation_state_map(
878 | |     verdicts: &[DependentVerdict],
879 | |     files: &[FileScan],
880 | |     states: &BTreeMap<
...   |
889 | |     source_paths: &BTreeSet<&Path>,
890 | | ) -> BTreeMap<String, SourceRecovery> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1147:1
     |
1147 | / fn relation_offer_placement(
1148 | |     group: &RelationOfferGroup,
1149 | |     completed: &[CompletedTask],
1150 | |     baseline_day: &DayView,
...    |
1155 | |     implicit: Option<&ImplicitDest>,
1156 | | ) -> Option<RelationOfferPlacement> {
     | |___________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2558:1
     |
2558 | / fn attach_offer(
2559 | |     verdict: &mut DependentVerdict,
2560 | |     files: &[FileScan],
2561 | |     day: &DayView,
...    |
2566 | |     project: Option<PathBuf>,
2567 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:2659:1
     |
2659 | / fn apply_project_member_classes(
2660 | |     verdicts: &mut Vec<DependentVerdict>,
2661 | |     folds: &mut Vec<ProjectFold>,
2662 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
2671 | |     _note_settings: &NoteTaskSettings,
2672 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
    --> src/native/task_complete/successors.rs:3254:1
     |
3254 | / fn apply_verdicts(
3255 | |     input: SuccessorInput,
3256 | |     files: Vec<FileScan>,
3257 | |     verdicts: Vec<DependentVerdict>,
...    |
3267 | |     relation_target_reads: usize,
3268 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/payload.rs:457:6
    |
457 | ) -> Result<(Vec<LineRange>, Vec<(String, String)>, usize), MergeError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/retirement.rs:212:15
    |
212 |     repoints: &[((PathBuf, String), (PathBuf, String))],
    |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/command.rs:1064:6
     |
1064 | ) -> Result<(Option<(PathBuf, String)>, Vec<RelocatedInfo>), String> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/task_move/plan.rs:340:22
    |
340 |           let parent = tasks
    |  ______________________^
341 | |             .iter()
342 | |             .filter(|candidate| {
343 | |                 candidate.line_index < task.line_index
...   |
346 | |             })
347 | |             .last();
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
347 -             .last();
347 +             .next_back();
    |

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_move/transplant.rs:121:6
    |
121 |   ) -> Result<
    |  ______^
122 | |     (Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>),
123 | |     RenameError,
124 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: called `unwrap` on `mention_id` after checking its variant with `is_some`
   --> src/native/task_split/plan.rs:298:33
    |
294 |             && mention_id.is_some()
    |                -------------------- the check is happening here
...
298 |                 format!("#^{}", mention_id.unwrap())
    |                                 ^^^^^^^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

warning: called `unwrap` on `mention_id` after checking its variant with `is_some`
   --> src/native/task_split/plan.rs:303:21
    |
294 |             && mention_id.is_some()
    |                -------------------- the check is happening here
...
303 |                     mention_id.unwrap()
    |                     ^^^^^^^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

warning: the loop variable `row` is only used to index `transformed_source`
   --> src/native/task_split/plan.rs:269:20
    |
269 |         for row in candidate.line + 1..=candidate.end {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
269 -         for row in candidate.line + 1..=candidate.end {
269 +         for <item> in transformed_source.iter_mut().take(candidate.end + 1).skip(candidate.line + 1) {
    |

warning: this `if` has identical blocks
   --> src/native/task_split/plan.rs:338:59
    |
338 |           let dest_after = if owner.kind == OwnerKind::Task {
    |  ___________________________________________________________^
339 | |             insert_tasks_section_string(&destination_before, &generated)?
340 | |         } else {
    | |_________^
    |
note: same as this
   --> src/native/task_split/plan.rs:340:16
    |
340 |           } else {
    |  ________________^
341 | |             insert_tasks_section_string(&destination_before, &generated)?
342 | |         };
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: this `if` has identical blocks
   --> src/native/task_split/plan.rs:936:55
    |
936 |               if snapshot.notes.contains_key(&with_ext) {
    |  _______________________________________________________^
937 | |                 Ok(with_ext)
938 | |             } else {
    | |_____________^
    |
note: same as this
   --> src/native/task_split/plan.rs:938:20
    |
938 |               } else {
    |  ____________________^
939 | |                 Ok(with_ext)
940 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: the loop variable `index` is used to index `lines`
    --> src/native/task_split/plan.rs:1089:18
     |
1089 |     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
     |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1089 -     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
1089 +     for (index, <item>) in lines.iter().enumerate().take(limit.min(lines.len().saturating_sub(1)) + 1).skip(start + 1) {
     |

warning: this function has too many arguments (8/7)
   --> src/native/task_status_groups/emit.rs:105:1
    |
105 | / pub(super) fn emit_grouped_body(
106 | |     node: &HeadingNode,
107 | |     contents: &str,
108 | |     classified: &ClassifiedChildren<'_>,
...   |
113 | |     heading_has_line_ending: bool,
114 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:556:5
    |
556 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:364:9
    |
364 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1358:1
     |
1358 | / fn consume_blocked_links_after_compose(
1359 | |     compose: &mut ComposeResult,
1360 | |     files: &[FileScan],
1361 | |     daily_path: &Path,
...    |
1372 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1373 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: useless use of `vec!`
   --> src/native/periods/scaffold.rs:209:17
    |
209 |       let parts = vec![
    |  _________________^
210 | |         frontmatter_all_time(),
211 | |         "# All time".to_string(),
212 | |         "[[org|↑ org]]".to_string(),
...   |
216 | |         instructions::render(PeriodId::AllTime),
217 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
    = note: `#[warn(clippy::useless_vec)]` on by default
help: you can use an array directly
    |
209 ~     let parts = [frontmatter_all_time(),
210 +         "# All time".to_string(),
211 ~         "[[org|↑ org]]".to_string(),
212 +         "```bob-stats-strip\n\n```".to_string(),
213 +         "## Years\n\n```bob-period-parts\n\n```".to_string(),
214 +         "## Notes".to_string(),
215 ~         instructions::render(PeriodId::AllTime)];
    |

warning: `bob-obsidian` (lib) generated 453 warnings (run `cargo clippy --fix --lib -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 31 suggestions)
warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
  --> tests/gcal_lifecycle.rs:62:5
   |
62 | /     journal
63 | |         .iter()
64 | |         .filter(|line| {
65 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == event_id
66 | |         })
67 | |         .last()
   | |_______________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
   = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
   |
67 -         .last()
67 +         .next_back()
   |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> tests/gcal_lifecycle.rs:671:19
    |
671 |       let learned = journal
    |  ___________________^
672 | |         .iter()
673 | |         .filter(|line| line["kind"] == "gcal.series_root")
674 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
674 -         .last()
674 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> tests/gcal_lifecycle.rs:707:21
    |
707 |       let relearned = journal
    |  _____________________^
708 | |         .iter()
709 | |         .filter(|line| line["kind"] == "gcal.series_root")
710 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
710 -         .last()
710 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:1694:5
     |
1694 | /     journal
1695 | |         .iter()
1696 | |         .filter(|line| {
1697 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == event_id
1698 | |         })
1699 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
     = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
     |
1699 -         .last()
1699 +         .next_back()
     |

warning: useless use of `vec!`
    --> tests/gcal_lifecycle.rs:1404:19
     |
1404 |       let journal = vec![
     |  ___________________^
1405 | |         journal_entry(
1406 | |             "migrate",
1407 | |             "migrate",
...    |
1428 | |         ),
1429 | |     ];
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
     = note: `#[warn(clippy::useless_vec)]` on by default
help: you can use an array directly
     |
1404 ~     let journal = [journal_entry(
1405 +             "migrate",
1406 +             "migrate",
1407 +             migrate_html,
1408 +             "1830-1900",
1409 +             "Migrate",
1410 +             &migrate_legacy,
1411 +         ),
1412 +         journal_entry(
1413 +             "hand",
1414 +             "hand",
1415 +             hand_html,
1416 +             "1900-1930",
1417 +             "Hand",
1418 +             &hand_legacy,
1419 +         ),
1420 +         journal_entry(
1421 +             "done",
1422 +             "done",
1423 +             done_html,
1424 +             "2000-2030",
1425 +             "Done",
1426 +             &done_legacy,
1427 ~         )];
     |

warning: `bob-obsidian` (test "gcal_lifecycle") generated 4 warnings (run `cargo clippy --fix --test "gcal_lifecycle" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 4 suggestions)
warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:2437:18
     |
2437 |       let latest = journal
     |  __________________^
2438 | |         .iter()
2439 | |         .filter(|line| {
2440 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == "talk"
2441 | |         })
2442 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
     |
2442 -         .last()
2442 +         .next_back()
     |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:2549:18
     |
2549 |       let latest = journal
     |  __________________^
2550 | |         .iter()
2551 | |         .filter(|line| {
2552 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == "dentist"
2553 | |         })
2554 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
     |
2554 -         .last()
2554 +         .next_back()
     |

warning: `bob-obsidian` (test "gcal_sync") generated 3 warnings (run `cargo clippy --fix --test "gcal_sync" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 3 suggestions)
warning: redundant redefinition of a binding `plans`
   --> src/native/articles/inbound.rs:485:9
    |
485 |         let mut plans = plans;
    |         ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `plans` is initially defined here
   --> src/native/articles/inbound.rs:479:13
    |
479 |         let mut plans =
    |             ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (8/7)
  --> src/native/attachments/tests.rs:38:1
   |
38 | / fn record(
39 | |     vault: &std::path::Path,
40 | |     host: &str,
41 | |     ts: &str,
...  |
46 | |     via: &str,
47 | | ) {
   | |_^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this method chain can be written more clearly with `if .. else ..`
   --> src/native/attachments/tests.rs:205:19
    |
205 |         let via = with_via.then_some(",\"via\":\"cli\"").unwrap_or("");
    |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `if with_via { ",\"via\":\"cli\"" } else { "" }`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#obfuscated_if_else
    = note: `#[warn(clippy::obfuscated_if_else)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:364:10
    |
364 |     ) -> Result<PlannedDependencyUpdate, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:628:10
    |
628 |     ) -> Result<DependentRef, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/note_pull.rs:1623:39
     |
1623 |     fn plan(harness: &mut Harness) -> Result<PlannedCaptureItem, CaptureError> {
     |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3108:10
     |
3108 |     ) -> Result<PlannedCaptureItem, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:14:6
   |
14 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:31:6
   |
31 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/tests/mod.rs:20:6
   |
20 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1345:9
     |
1345 | /         match lex_bullets(close, draft).expect("valid bullets") {
1346 | |             CloseLogLexed { entries, dangling } => {
1347 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1348 | |                 entries
...    |
1353 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `#[warn(clippy::match_single_binding)]` on by default
help: consider using a `let` statement
     |
1345 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1346 +         {
1347 +             assert!(dangling.is_empty(), "unexpected dangling");
1348 +             entries
1349 +                 .into_iter()
1350 +                 .map(|entry| (entry.index, entry.text, entry.details))
1351 +                 .collect()
1352 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1451:9
     |
1451 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1452 | |             CloseLogLexed { entries, dangling } => {
1453 | |                 assert!(entries.is_empty());
1454 | |                 assert_eq!(dangling.len(), 1);
...    |
1457 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1451 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1452 +         {
1453 +             assert!(entries.is_empty());
1454 +             assert_eq!(dangling.len(), 1);
1455 +             assert_eq!(dangling[0].index, Some(1));
1456 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1524:9
     |
1524 | /         match lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing") {
1525 | |             error => assert!(
1526 | |                 error.message.contains("- 2 wired"),
1527 | |                 "{}",
1528 | |                 error.message
1529 | |             ),
1530 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1524 ~         let error = lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing");
1525 +         assert!(
1526 +             error.message.contains("- 2 wired"),
1527 +             "{}",
1528 +             error.message
1529 +         )
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2002:9
     |
2002 | /         match lex_bullets("x", "x\n- *").expect("dangling star") {
2003 | |             CloseLogLexed { entries, dangling } => {
2004 | |                 assert!(entries.is_empty());
2005 | |                 assert_eq!(dangling.len(), 1);
...    |
2008 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2002 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *").expect("dangling star");
2003 +         {
2004 +             assert!(entries.is_empty());
2005 +             assert_eq!(dangling.len(), 1);
2006 +             assert_eq!(dangling[0].index, None);
2007 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2009:9
     |
2009 | /         match lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details")
2010 | |         {
2011 | |             CloseLogLexed { entries, dangling } => {
2012 | |                 assert!(entries.is_empty());
...    |
2016 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2009 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details");
2010 +         {
2011 +             assert!(entries.is_empty());
2012 +             assert_eq!(dangling.len(), 1);
2013 +             assert_eq!(dangling[0].index, None);
2014 +         }
     |

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/tests/editor_spans.rs:97:16
    |
 97 |       let cases: &[(
    |  ________________^
 98 | |         &str,
 99 | |         &[(usize, usize, SpanKind, Option<ProjectNoteForm>)],
100 | |         &[Need],
101 | |     )] = &[
    | |______^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: function call inside of `expect`
  --> src/native/capture_language/tests/goto.rs:54:42
   |
54 |         let completion = field(raw, end).expect(&format!("{raw:?} completes"));
   |                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw:?} completes"))`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call
   = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:102:22
    |
102 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:115:35
    |
115 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2420:35
     |
2420 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2457:48
     |
2457 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2466:22
     |
2466 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: unnecessary use of `get(Path::new("b.md")).is_none()`
   --> src/native/capture_pomodoro_close/linked_task_tests.rs:223:28
    |
223 |         plan.changed_files.get(Path::new("b.md")).is_none(),
    |         -------------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |         |
    |         help: replace it with: `!plan.changed_files.contains_key(Path::new("b.md"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
    = note: `#[warn(clippy::unnecessary_get_then_check)]` on by default

warning: this assertion has a constant value
   --> src/native/file_coordination.rs:225:9
    |
225 |         assert!(!IS_COORDINATED);
    |         ^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: consider moving this into a const block: `const { assert!(..) }`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants
    = note: `#[warn(clippy::assertions_on_constants)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> tests/cli/capture/parse.rs:940:16
    |
940 |     let cases: &[(&str, &[&str], &[(u64, u64, &str, &str)])] = &[
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
    = note: `#[warn(clippy::type_complexity)]` on by default

warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:453:14
    |
453 |         .arg("-2 x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#suspicious_command_arg_space
    = note: `#[warn(clippy::suspicious_command_arg_space)]` on by default
help: consider splitting the argument
    |
453 -         .arg("-2 x\n- 1 wired the lexer")
453 +         .args(["-2", "x\n- 1 wired the lexer"])
    |

warning: initializer for `thread_local` value can be made `const`
  --> src/native/highlights_ref/overwrite/execute.rs:62:58
   |
62 |     static FAILPOINT: Cell<Option<OverwriteFailpoint>> = Cell::new(None);
   |                                                          ^^^^^^^^^^^^^^^ help: replace with: `const { Cell::new(None) }`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#missing_const_for_thread_local
   = note: `#[warn(clippy::missing_const_for_thread_local)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/highlights_ref/overwrite/execute.rs:3069:9
     |
3069 |         request.explicit_title = Some("A Better Report".to_string());
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::highlights_ref::overwrite::OverwriteRequest { explicit_title: Some("A Better Report".to_string()), explicit_status: Some("next".to_string()), replacement_audio_path: Some("lib/papers/report.m4a".to_string()), ..Default::default() }` and removing relevant reassignments
    --> src/native/highlights_ref/overwrite/execute.rs:3068:9
     |
3068 |         let mut request = super::super::OverwriteRequest::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: the following explicit lifetimes could be elided: 'a
   --> tests/cli/capture/relation_presentation.rs:108:19
    |
108 | fn relation_group<'a>(json: &'a serde_json::Value) -> &'a serde_json::Value {
    |                   ^^         ^^                        ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
108 - fn relation_group<'a>(json: &'a serde_json::Value) -> &'a serde_json::Value {
108 + fn relation_group(json: &serde_json::Value) -> &serde_json::Value {
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/tests/continuations.rs:249:42
    |
249 |     let plan = super::plan_continuations(&[first.clone()]);
    |                                          ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&first)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: redundant redefinition of a binding `first`
   --> src/native/highlights_ref/tests/sections.rs:555:9
    |
555 |         let first = first;
    |         ^^^^^^^^^^^^^^^^^^
    |
help: `first` is initially defined here
   --> src/native/highlights_ref/tests/sections.rs:519:14
    |
519 |         let (first, second) = if first_sticky {
    |              ^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

warning: replacing text with itself
    --> src/native/highlights_ref/tests/sections_render.rs:1103:22
     |
1103 |       let at_sidecar = sidecar
     |  ______________________^
1104 | |         .replace("#what-is-it", "@what-is-it")
1105 | |         .replace("# what is it", "# what is it");
     | |________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#no_effect_replace
     = note: `#[warn(clippy::no_effect_replace)]` on by default

warning: an array of `Range` that is only one element
   --> src/native/highlights_ref/tests/underlines.rs:290:41
    |
290 |         apply_emphasis(already_strong, &[strong_start..strong_end]),
    |                                         ^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
    = note: `#[warn(clippy::single_range_in_vec_init)]` on by default
help: if you wanted a `Vec` that contains the entire range, try
    |
290 -         apply_emphasis(already_strong, &[strong_start..strong_end]),
290 +         apply_emphasis(already_strong, &(strong_start..strong_end).collect::<std::vec::Vec<usize>>()),
    |

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:377:9
    |
377 |         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
377 -         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
377 +         sorted.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/pomodoro.rs:1002:51
     |
1002 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
     |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this function has too many arguments (8/7)
  --> tests/cli/highlights/overwrite_recovery.rs:59:1
   |
59 | / pub(crate) fn write_intent_v2(
60 | |     state: &Path,
61 | |     vault: &Path,
62 | |     base: &str,
...  |
67 | |     writes: serde_json::Value,
68 | | ) {
   | |_^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
   = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: this function has too many arguments (9/7)
  --> tests/cli/ref_library/code.rs:62:1
   |
62 | / fn block_json(
63 | |     n: u32,
64 | |     kind: &str,
65 | |     lang: Option<&str>,
...  |
71 | |     attrs: &str,
72 | | ) -> String {
   | |___________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
  --> tests/cli/ref_library/links.rs:60:1
   |
60 | / fn link_json(
61 | |     n: u32,
62 | |     url: &str,
63 | |     text: &str,
...  |
69 | |     page: Option<u32>,
70 | | ) -> String {
   | |___________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: `bob-obsidian` (test "cli") generated 6 warnings (run `cargo clippy --fix --test "cli" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 1 suggestion)
warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:556:5
    |
556 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:364:9
    |
364 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:698:27
    |
698 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:709:27
    |
709 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:720:27
    |
720 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: `bob-obsidian` (lib test) generated 489 warnings (452 duplicates) (run `cargo clippy --fix --lib -p bob-obsidian --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 8 suggestions)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1m 49s

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
bob-docs: error: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/memory/glossary/task-merge.md: memory strand has no front matter
error: recipe `docs-check` failed on line 269 with exit code 2
failed  exit=2  duration=240245ms

