# Chat History - ace-run (bob-cli-q5.3.1.3--mon-1)

- **TIMESTAMP:** 2026-11-26 05:33:57 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-q5.3.1.3--mon-1

## Prompt

sase monitor start --command "bash -lc 'cargo test -p bob-obsidian snooze && just docs-check'" --reason 'Run snooze completion tests and docs gate for bob-cli-q5.3.1.3'

## Response

sase tool run a4372a7a30f0cfb9df0b5709dc9970d7
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling cfg-if v1.0.4
   Compiling siphasher v1.0.4
   Compiling typenum v1.20.1
   Compiling libc v0.2.186
   Compiling stable_deref_trait v1.2.1
   Compiling version_check v0.9.5
   Compiling smallvec v1.15.2
   Compiling memchr v2.8.1
   Compiling fastrand v2.5.0
   Compiling shlex v2.0.1
   Compiling bitflags v2.12.1
   Compiling find-msvc-tools v0.1.9
   Compiling equivalent v1.0.2
   Compiling foldhash v0.2.0
   Compiling allocator-api2 v0.2.21
   Compiling generic-array v0.14.7
   Compiling serde_core v1.0.228
   Compiling autocfg v1.5.1
   Compiling parking_lot_core v0.9.12
   Compiling phf_shared v0.14.0
   Compiling rand_core v0.10.1
   Compiling new_debug_unreachable v1.0.6
   Compiling litemap v0.8.3
   Compiling scopeguard v1.2.0
   Compiling getrandom v0.4.2
   Compiling writeable v0.6.4
   Compiling icu_properties_data v2.3.0
   Compiling precomputed-hash v0.1.1
   Compiling itoa v1.0.18
   Compiling cc v1.2.63
   Compiling icu_normalizer_data v2.3.0
   Compiling crc32fast v1.5.0
   Compiling simd-adler32 v0.3.9
   Compiling num-traits v0.2.19
   Compiling serde v1.0.228
   Compiling hashbrown v0.17.1
   Compiling lock_api v0.4.14
   Compiling utf8_iter v1.0.4
   Compiling adler2 v2.0.1
   Compiling cpufeatures v0.3.0
   Compiling log v0.4.30
   Compiling utf8parse v0.2.2
   Compiling rustix v1.1.5
   Compiling phf_generator v0.14.0
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling rquickjs-sys v0.12.1
   Compiling block-buffer v0.10.4
   Compiling anstyle-parse v1.0.0
   Compiling miniz_oxide v0.8.9
   Compiling phf_codegen v0.14.0
   Compiling hybrid-array v0.4.12
   Compiling is_terminal_polyfill v1.70.2
   Compiling anstyle-query v1.1.5
   Compiling anstyle v1.0.14
   Compiling colorchoice v1.0.5
   Compiling tinyvec_macros v0.1.1
   Compiling inout v0.1.4
   Compiling dtoa v1.0.11
   Compiling linux-raw-sys v0.12.1
   Compiling digest v0.10.7
   Compiling indexmap v2.14.0
   Compiling chacha20 v0.10.2
   Compiling tendril v0.5.1
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling string_cache_codegen v0.11.2
   Compiling parking_lot v0.12.5
   Compiling anstream v1.0.0
   Compiling flate2 v1.1.9
   Compiling dtoa-short v0.3.5
   Compiling strsim v0.11.1
   Compiling tinyvec v1.11.0
   Compiling cipher v0.4.4
   Compiling clap_lex v1.1.0
   Compiling thiserror v2.0.18
   Compiling once_cell v1.21.4
   Compiling unicode-width v0.2.3
   Compiling web_atoms v0.3.0
   Compiling zmij v1.0.21
   Compiling string_cache v0.11.0
   Compiling cpufeatures v0.2.17
   Compiling weezl v0.1.12
   Compiling regex-syntax v0.8.10
   Compiling rand v0.10.1
   Compiling unicode-normalization v0.1.25
   Compiling getopts v0.2.24
   Compiling clap_builder v4.6.7
   Compiling block-buffer v0.12.0
   Compiling crypto-common v0.2.2
   Compiling fdeflate v0.3.7
   Compiling nom v8.0.0
   Compiling aho-corasick v1.1.4
   Compiling phf_shared v0.12.1
   Compiling servo_arc v0.5.0
   Compiling serde_json v1.0.150
   Compiling unicode-bidi v0.3.18
   Compiling percent-encoding v2.3.2
   Compiling iana-time-zone v0.1.65
   Compiling tempfile v3.27.0
   Compiling chrono-tz v0.10.4
   Compiling quick-error v2.0.1
   Compiling phf_macros v0.14.0
   Compiling serde_derive v1.0.228
   Compiling derive_more-impl v2.1.1
   Compiling thiserror-impl v2.0.18
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling phf v0.14.0
   Compiling cssparser-macros v0.7.1
   Compiling unicode-properties v0.1.4
   Compiling bytecount v0.6.9
   Compiling byteorder-lite v0.1.0
   Compiling derive_more v2.1.1
   Compiling color_quant v1.1.0
   Compiling pulldown-cmark v0.13.6
   Compiling zune-core v0.5.3
   Compiling pxfm v0.1.30
   Compiling const-oid v0.10.2
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling rustc-hash v2.1.3
   Compiling cssparser v0.38.0
   Compiling regex-automata v0.4.14
   Compiling zerofrom v0.1.8
   Compiling gif v0.14.2
   Compiling digest v0.11.3
   Compiling stringprep v0.1.5
   Compiling image-webp v0.2.4
   Compiling zune-jpeg v0.5.15
   Compiling form_urlencoded v1.2.2
   Compiling nom_locate v5.0.0
   Compiling png v0.18.1
   Compiling yoke v0.8.3
   Compiling chrono v0.4.44
   Compiling phf v0.12.1
   Compiling aes v0.8.4
   Compiling markup5ever v0.40.0
   Compiling selectors v0.41.0
   Compiling sha2 v0.10.9
   Compiling clap v4.6.7
   Compiling cbc v0.1.2
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling ecb v0.1.2
   Compiling md-5 v0.10.6
   Compiling html5ever v0.40.1
   Compiling moxcms v0.8.1
   Compiling encoding_rs v0.8.35
   Compiling ryu v1.0.23
   Compiling base64 v0.22.1
   Compiling unsafe-libyaml v0.2.11
   Compiling rangemap v1.7.1
   Compiling bytemuck v1.25.2
   Compiling is_executable v1.0.6
   Compiling unicase v2.10.0
   Compiling ego-tree v0.11.1
   Compiling pulldown-cmark-escape v0.11.0
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling ttf-parser v0.25.1
   Compiling clap_complete v4.6.11
   Compiling regex v1.12.3
   Compiling sha2 v0.11.0
   Compiling fs2 v0.4.3
   Compiling serde_yaml v0.9.34+deprecated
   Compiling rquickjs-core v0.12.1
   Compiling roxmltree v0.21.2
   Compiling icu_locale_core v2.3.0
   Compiling icu_collections v2.3.0
   Compiling scraper v0.29.0
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/crates/bob-obsidian-assets)
   Compiling similar v2.7.0
   Compiling glob v0.3.4
   Compiling hex v0.4.3
   Compiling pkg-config v0.3.33
   Compiling vcpkg v0.2.15
   Compiling wait-timeout v0.2.1
   Compiling quick-error v1.2.3
   Compiling lopdf v0.40.0
   Compiling time-core v0.1.9
   Compiling powerfmt v0.2.0
   Compiling num-conv v0.2.2
   Compiling deranged v0.5.8
   Compiling icu_provider v2.3.1
   Compiling bit-vec v0.10.2
   Compiling fnv v1.0.7
   Compiling hashlink v0.12.1
   Compiling rand_xorshift v0.5.0
   Compiling libsqlite3-sys v0.38.1
   Compiling image v0.25.10
   Compiling quick-xml v0.41.0
   Compiling fallible-iterator v0.3.0
   Compiling rquickjs v0.12.1
   Compiling bit-set v0.11.1
   Compiling rusty-fork v0.3.1
   Compiling core_detect v1.0.0
   Compiling unarray v0.1.4
   Compiling fallible-streaming-iterator v0.1.9
   Compiling icu_normalizer v2.3.0
   Compiling icu_properties v2.3.0
   Compiling time v0.3.53
   Compiling proptest v1.12.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling plist v1.10.0
   Compiling bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12)
   Compiling rusqlite v0.40.1
warning: duplicated attribute
    --> src/native/capture_project_note.rs:1098:5
     |
1098 |     #[test]
     |     ^^^^^^^
     |
     = note: `#[warn(duplicate_macro_attributes)]` on by default

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3451:26
     |
3451 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 2 warnings (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 3m 14s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/bob_cli-82c271221a2c466a)

running 72 tests
test native::capture_language::snooze::tests::snooze_token_claims_only_lowercase ... ok
test native::capture_language::snooze::tests::drop_claims_only_the_narrow_spelling ... ok
test native::config::snooze::tests::defaults_when_missing ... ok
test native::freshness::placement::placement_tests::snoozed_planned_today_skips_unblocked_placement ... ok
test native::capture::relations_mentions::snoozed_mention_tests::snoozed_rows_create_no_mentions ... ok
test native::config::snooze::tests::rejects_unknown_notify_value ... ok
test native::config::snooze::tests::accepts_each_notify_mode ... ok
test native::capture_language::tests::snooze_completion::snooze_completion_uses_value_range_in_both_marker_orders ... ok
test native::capture_language::tests::snooze_completion::snooze_completion_keeps_utf8_offsets_and_accepts_an_empty_value ... ok
test native::capture_language::tests::grammar::snooze_duplicate_keeps_parsing_with_the_last_claim ... ok
test native::capture_language::tests::grammar::snooze_marks_unicode_offsets_in_bytes ... ok
test native::capture_language::tests::grammar::snooze_new_task_routes_cover_authored_and_minted_ids ... ok
test native::capture_drawers::tests::snoozed_is_structural_never_a_user_drawer ... ok
test native::capture_language::tests::grammar::snooze_admits_existing_task_markers_with_either_sigil ... ok
test native::snooze::notify::tests::single_and_batch_desktop_copy ... ok
test native::snooze::parse::tests::active_row_accepts_colon_and_embedded_aliased_links ... ok
test native::capture_language::tests::grammar::snooze_claims_terminal_z_in_either_marker_order ... ok
test native::snooze::parse::tests::consecutive_active_rows_all_parse ... ok
test native::capture_complete::tests::snooze::missing_daily_note_still_offers_valid_relative_times ... ok
test native::snooze::parse::tests::duplicate_sections_are_linted ... ok
test native::snooze::parse::tests::fenced_example_rows_never_execute ... ok
test native::capture_language::tests::snooze_completion::embedded_literals_and_child_prose_do_not_claim_snooze_completion ... ok
test native::snooze::parse::tests::frontmatter_and_fenced_headings_do_not_count ... ok
test native::snooze::parse::tests::history_row_parses_struck_tail ... ok
test native::snooze::parse::tests::indented_and_extra_link_rows_are_malformed ... ok
test native::snooze::parse::tests::section_bounds_stop_at_next_h2 ... ok
test native::snooze::plan::tests::first_child_insert_lands_above_existing_children ... ok
test native::capture_language::tests::grammar::snooze_stays_literal_outside_terminal_claims ... ok
test native::snooze::plan::tests::wake_refuses_when_no_pomodoros_section ... ok
test native::snooze::receipt::tests::empty_woken_builds_no_receipt ... ok
test native::freshness::state::state_tests::snoozed_linked_wins_preserves_today_checklist_exception ... ok
test native::snooze::plan::tests::wake_refuses_typed_destination_with_two_running_pomodoros ... ok
test native::capture_complete::tests::snooze::relative_suggestions_near_midnight_drop_overflow_and_nonfuture_rows ... ok
test native::collect_done::tests::unit::link_repair_rewrites_only_targets_inside_snoozed_rows ... ok
test native::snooze::shell::tests::lock_timeout_is_reported_as_deferred ... ok
test native::snooze::state::tests::asleep_due_blocked_and_ignored_states ... ok
test native::snooze::plan::tests::wake_untyped_with_two_running_pomodoros_lands_after_first ... ok
test native::capture_language::tests::grammar::snooze_drop_is_narrow_and_not_a_toggle ... ok
test native::snooze::state::tests::earliest_time_wins_ties_use_source_order ... ok
test native::snooze::state::tests::live_link_wins_and_event_emits_lint ... ok
test native::snooze::state::tests::live_targets_include_blocked_but_exclude_others ... ok
test native::snooze::state::tests::next_wake_at_ignores_blocked_and_previous_day ... ok
test native::capture_complete::tests::snooze::event_ends_then_relative_then_used_times_are_deduplicated_in_order ... ok
test native::snooze::shell::tests::changed_read_dependency_refuses_before_install ... ok
test native::snooze::shell::tests::second_preimage_drift_remains_unwritten_after_one_retry ... ok
test native::snooze::vectors::tests::unknown_group_is_an_error ... ok
test native::snooze::when::tests::absolute_forms_resolve ... ok
test native::snooze::when::tests::bare_digits_use_next_occurrence_today ... ok
test native::snooze::when::tests::relative_times_round_up_to_five_minutes ... ok
test native::capture_complete::tests::snooze::typed_prefix_filters_candidates_without_changing_their_group_order ... ok
test native::tick::adapters::tests::snooze_summaries_and_nonfailure_deferred_skipped ... ok
test native::snooze::when::tests::dst_gap_is_refused_and_fold_picks_first ... ok
test native::snooze::cli::tests::add_defers_when_the_day_rolls_over_before_write ... ok
test native::snooze::when::tests::past_and_midnight_overflow_refuse_with_teaching_copy ... ok
test native::freshness::state::state_tests::snoozed_planned_today_excludes_every_review_overlay ... ok
test native::snooze::vectors::tests::rows_vectors_match_parser ... ok
test native::snooze::vectors::tests::fixture_loads_with_six_groups ... ok
test native::snooze::vectors::tests::unknown_runner_is_an_error ... ok
test native::snooze::vectors::tests::live_vectors_match_classifier ... ok
test native::snooze::vectors::tests::when_vectors_match_grammar ... ok
test native::snooze::plan::tests::snooze_wake_cleanup_vectors ... ok
test native::capture_language::tests::grammar::snooze_bare_and_conflicts_agree_across_strict_and_editor ... ok
test native::snooze::cli::tests::add_defers_after_a_second_preimage_drift_without_partial_write ... ok
test native::snooze::notify::tests::darwin_failure_still_reports_wake_id_when_receipt_is_readable ... ok
test native::snooze::notify::tests::desktop_failure_reports_none_and_keeps_receipt ... ok
test native::snooze::notify::tests::auto_yields_to_live_claim_and_skips_desktop ... ok
test native::snooze::receipt::tests::write_is_readable_before_darwin_and_uses_0600 ... ok
test native::snooze::notify::tests::desktop_mode_ignores_live_claim_and_off_nudges_nothing ... ok
test native::snooze::cli::tests::add_refreshes_read_inputs_after_one_preimage_drift ... ok
test native::snooze::cli::tests::failed_second_file_install_rolls_back_the_daily_note ... ok
test native::snooze::notify::tests::corrupt_and_dead_claims_do_not_suppress_desktop ... ok
test native::capture::snooze::tests::snooze_batch_guards_task_daily_membership_and_eligibility_reads ... ok

test result: ok. 72 passed; 0 failed; 0 ignored; 0 measured; 8167 filtered out; finished in 2.14s

     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/bob-92104fb2086a6c9e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/bob_notify-df222187bc624122)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/bob_pomodoro-235ede3c6f0ff61a)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/tmux_bob_pomodoro-6e9f32d7b430687a)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/cli-5c417d1696cf4d24)

running 53 tests
test snooze::no_work_wake_leaves_vault_and_state_directory_unchanged ... ok
test snooze::bare_command_lists_read_only_with_stable_json ... ok
test snooze::invalid_notify_exits_two_before_mutating ... ok
test snooze::skipped_sweep_does_not_write_a_receipt ... ok
test snooze::wake_refuses_when_daily_note_has_no_pomodoros_section ... ok
test snooze_writer_audit::blocked_parks_and_ready_ignores ... ok
test capture::parse_snooze::capture_parse_reports_incomplete_and_duplicate_snooze ... ok
test capture::parse_snooze::capture_parse_reports_drop_span_and_keeps_the_toggle_distinct ... ok
test freshness::snoozed_seed_preserves_today_bucket_counters_and_idempotence ... ok
test snooze_writer_audit::capture_lineup_preserves_trailing_snoozed ... ok
test snooze::wake_refuses_typed_destination_with_two_running_pomodoros ... ok
test capture::snooze::time_refusals_use_same_day_and_dst_rules ... ok
test snooze::help_completion_and_catalog_expose_snooze_commands ... ok
test snooze::add_settles_a_promoted_task_into_its_status_group ... ok
test snooze::live_mac_claim_reports_mac_capture_without_desktop ... ok
test snooze::explicit_wake_works_when_automatic_writer_is_elsewhere ... ok
test snooze_writer_audit::over_cap_wake_succeeds_and_reports_over ... ok
test snooze::wake_moves_due_subtree_and_records_history ... ok
test snooze::dry_run_and_no_work_leave_the_prior_receipt_untouched ... ok
test walks::snoozed_lane_excess_drops_without_changing_whole_plan_lane ... ok
test capture::snooze::retime_dedupes_resolved_spellings_and_preserves_notes_and_history ... ok
test capture::snooze::link_now_uses_running_destination_and_transfers_nested_notes_once ... ok
test capture::snooze::same_note_target_and_daily_edits_coalesce ... ok
test capture::snooze::crlf_link_now_remaps_destination_after_an_earlier_snoozed_section ... ok
test capture::snooze::completion_candidate_is_literal_and_both_parse_and_capture_accept_it ... ok
test capture::parse_snooze::capture_parse_reports_snooze_spans_for_existing_and_new_tasks ... ok
test snooze_writer_audit::capture_record_preserves_trailing_snoozed ... ok
test capture::snooze::earlier_status_edit_is_visible_to_snooze_eligibility ... ok
test snooze::concurrent_wakes_move_one_row_in_one_successful_batch ... ok
test capture::snooze::full_link_budget_does_not_block_snooze_or_count_its_row ... ok
test capture::snooze::new_tasks_keep_children_and_mint_against_staged_and_non_task_ids ... ok
test snooze::notify_off_still_writes_receipt_and_desktop_failure_keeps_the_wake ... ok
test capture::snooze::sequential_same_task_operations_see_staged_rows_and_tasks ... ok
test snooze_writer_audit::wake_flow_noop_before_target_then_untimed_despite_running ... ok
test snooze::add_dry_run_and_drop_leave_expected_postimages ... ok
test capture::snooze::local_daily_link_aliases_retime_and_drop ... ok
test snooze_writer_audit::capture_start_preserves_trailing_snoozed ... ok
test capture::snooze::next_and_in_progress_task_bytes_do_not_change ... ok
test capture::snooze::ready_commits_next_and_dry_run_has_identical_plan ... ok
test capture::snooze::add_consumes_live_link_notes_and_keeps_recorded_time ... ok
test snooze_writer_audit::capture_link_preserves_trailing_snoozed_crlf ... ok
test snooze_writer_audit::capture_link_preserves_trailing_snoozed ... ok
test snooze_writer_audit::capture_close_preserves_trailing_snoozed ... ok
test capture::snooze::later_failure_rolls_back_earlier_snooze_and_new_task ... ok
test walks::snoozed_wake_returns_to_ordinary_today_without_freshness_mutation ... ok
test capture::parse_snooze::capture_dry_run_executes_recognized_snooze_intents_without_writing ... ok
test capture::snooze::drop_is_row_only_and_struck_history_is_not_active ... ok
test capture::snooze::inherited_project_block_and_event_clock_refuse ... ok
test capture::parse_snooze::capture_dry_run_and_parse_agree_on_snooze_refusals ... ok
test capture::snooze::blocked_and_closed_targets_refuse_without_dependency_or_schedule_changes ... ok
test tick::snooze_deferred_retries_without_consuming_cadence_and_skipped_is_ok ... ok
test walks::snoozed_planned_today_vectors_agree_across_freshness_walks_and_plan ... ok
test snooze_writer_audit::reconcile_leaves_snoozed_rows_byte_identical ... ok

test result: ok. 53 passed; 0 failed; 0 ignored; 0 measured; 4180 filtered out; finished in 2.10s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/dataview_parity-60b19327eb37e0e1)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 27 filtered out; finished in 0.00s

     Running tests/gcal_ack.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_ack-07a0da8715b97171)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 39 filtered out; finished in 0.00s

     Running tests/gcal_ack_tty.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_ack_tty-40bfbb490c9d1d79)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gcal_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_auth-09f5fb087b724d45)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 65 filtered out; finished in 0.00s

     Running tests/gcal_calendar_surfaces.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_calendar_surfaces-6cdf4b8c656c8780)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 2 filtered out; finished in 0.00s

     Running tests/gcal_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_cli-869a5a4776e67e9f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gcal_diagnostics.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_diagnostics-b6d22df90941583c)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 4 filtered out; finished in 0.00s

     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_lifecycle-cb20583c95cf35b7)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 45 filtered out; finished in 0.00s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_list-c85c4ba324261c68)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 16 filtered out; finished in 0.00s

     Running tests/gcal_note_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_note_cli-93505116d4190037)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 41 filtered out; finished in 0.00s

     Running tests/gcal_notes.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_notes-7f02d6a62454e101)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 21 filtered out; finished in 0.00s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gcal_sync-f7f14b3f510f7931)

running 1 test
test trailing_snoozed_section_survives_events_and_meet_filing ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 111 filtered out; finished in 0.33s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_adapter-60c726333455044d)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_auth-8c3352f073ea7d2a)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 14 filtered out; finished in 0.00s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_cli-bf430106f75f4a4e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_list-2e0ea76d94d03b87)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 23 filtered out; finished in 0.00s

     Running tests/gkeep_migrate.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_migrate-6f65609a26f10657)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_pull-eac8ca0cd3cf5cf9)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 52 filtered out; finished in 0.00s

     Running tests/gkeep_pull_recovery.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_pull_recovery-6243d7c4e43cc757)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gkeep_status.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gkeep_status-d6a4f58641ce0879)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 26 filtered out; finished in 0.00s

     Running tests/gmail_archive_apply.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_archive_apply-63031513bc708c10)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 61 filtered out; finished in 0.00s

     Running tests/gmail_archive_preview.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_archive_preview-1983b7b519508fc0)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 4 filtered out; finished in 0.00s

     Running tests/gmail_compose_contract.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_compose_contract-047a0e15c5064061)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 3 filtered out; finished in 0.00s

     Running tests/gmail_draft.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_draft-5953532e0aea243d)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 13 filtered out; finished in 0.00s

     Running tests/gmail_pull_attach.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_pull_attach-e41fa2c0624d44ba)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 2 filtered out; finished in 0.00s

     Running tests/gmail_search_peek.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_search_peek-8ae525807a153c77)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gmail_send.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_send-18004e95de486f02)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 11 filtered out; finished in 0.00s

     Running tests/gmail_shell.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_shell-bbd53df00c6c7ce2)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 71 filtered out; finished in 0.00s

     Running tests/gmail_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_sync-df303bbe70b43441)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 49 filtered out; finished in 0.00s

     Running tests/gmail_transport.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_transport-3dfda6b4d1a004ef)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 5 filtered out; finished in 0.00s

     Running tests/gmail_turns.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/gmail_turns-3947d831ab266a62)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 5 filtered out; finished in 0.00s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/randomize-cb8ae6a7298da374)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 15 filtered out; finished in 0.00s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/tasks_parity-d601f6aae5b4a068)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 33 filtered out; finished in 0.00s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261126_052122/build/debug/deps/tasks_real_vault_parity-613c6ebb8b8a6a5e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s


✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
Plugin documentation inventory is up to date.
generated contract content is up to date
docs-check: passed (generated drift)

docs-check: strict Zensical build
Build started
No issues found
Build finished in 13.21s
running: zensical build --strict --config-file /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/mkdocs.yml
built site: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site
docs-check: passed (strict Zensical build)

docs-check: published URLs
wrote /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/urls.txt (258 published pages)
urls: OK (258 pages, 983 mentions checked, 64 curated links)
docs-check: passed (published URLs)

docs-check: offline lychee with fragments
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/refs-browse-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/refs-browse-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/refs-browse.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/refs-browse.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/task-completion-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/task-completion-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/task-completion.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/task-completion.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/capture-agenda.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/reference/mac-capture/images/capture-agenda.png'
🔍 80138 Total (in 2s 236ms) 🔗 4445 Unique ✅ 78767 OK 🚫 0 Errors 👻 1371 Excluded

running: /home/bryan/.cache/bob-docs/bin/lychee --offline --no-progress --include-fragments --exclude-path (^|/)index[.]md$ --index-files index.html --root-dir /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site --remap https://bobs-org.github.io/ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/ /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site
links: OK (offline lychee with fragment checking)
docs-check: passed (offline lychee with fragments)

docs-check: edit links point at real sources
edit-links: OK (250 edit link(s) point at real source files)
docs-check: passed (edit links point at real sources)

docs-check: search smoke
search smoke: OK (136 cases; index /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/target/docs/site/search.json)
docs-check: passed (search smoke)

docs-check: executable first-day tutorial
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.46s

TUTORIAL_FENCE 5 docs/start/install.md:72
bob 0.6.0

TUTORIAL_FENCE 7 docs/start/first-bob-day.md:24
Using demo vault: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws12-261126_052122/bob-docs-sandbox-2gpkhkfb/tmp/bob-first-day.FRLCzs/vault

TUTORIAL_FENCE 8 docs/start/first-bob-day.md:46
✓ captured  mac_inbox.md
  - [ ] #task Sort the seed packets [created::2026-10-20] ^seed-packet

TUTORIAL_FENCE 9 docs/start/first-bob-day.md:61
✓ captured  garden.md
  - [ ] #task Water the seedlings [created::2026-10-20] ^seedlings

TUTORIAL_FENCE 10 docs/start/first-bob-day.md:76
bob plan - Tue 2026-10-20 - no daily note yet

  PLAN  0/10 links      TODAY 0 - PENDING 0/10 - NEXT 0/15


TUTORIAL_FENCE 11 docs/start/first-bob-day.md:92
Created daily note: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws12-261126_052122/bob-docs-sandbox-2gpkhkfb/tmp/bob-first-day.FRLCzs/vault/2026/20261020.md

TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117
✓ started  2026/20261020.md
  FOCUS 0905-0930 (25m) (created) at line 4
  - [ ] (**0905-0930** [t:: 25m]) — FOCUS
  nothing queued
plan 0/10 links

TUTORIAL_FENCE 13 docs/start/first-bob-day.md:128
✓ link  garden.md
  [ ] → [*]  Water the seedlings  ^seedlings
  Linked under FOCUS
plan 1/10 links
{"caps":{"max_links":10,"max_next":15,"max_pending":10,"max_ready":100},"daily_file":"2026/20261020.md","date":"2026-10-20","entries":[{"components":["FOCUS"],"exempt":false,"highlight":true,"homes":{"chip":"garden","hue":"magenta","kind":"work","label":"garden","parts":[{"area":"garden.md","area_label":"garden","hue":"magenta","key":"garden.md","kind":"area","label":"garden","share":100,"tasks":1}],"state":"forecast"},"line":4,"links":1,"name":"FOCUS","running":true,"themes":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"time_range":"0905-0930"}],"links":{"cap":10,"count":1,"off_clock":0,"over":false},"next":{"cap":15,"count":1,"over":false},"ok":true,"pending":{"cap":10,"count":0,"over":false},"schema_version":3,"status":"ok","theme_names":["FOCUS"],"theme_refs":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"today":{"count":1},"today_roots":[{"hue":"magenta","key":"garden.md","label":"garden","tasks":1}],"today_tasks":[{"block_id":"seedlings","entry_line":4,"entry_name":"FOCUS","ledger_line":5,"line":11,"path":"garden.md","status_name":"Next","status_symbol":"*","text":"Water the seedlings"}],"warnings":[]}

TUTORIAL_FENCE 14 docs/start/first-bob-day.md:141
bob capture: warning: FOCUS has not started: it starts at 0905, so closing now records a zero-length session; capture `x0` to reset it instead
✓ closed FOCUS 0905-0930 → 0905-0905 (0m, −25m) · 2026/20261020.md line 4
  1 [*] → [x] Water the seedlings garden.md ^seedlings
  next: FOCUS (created) at line 6 · carries 0 links
plan 0/10 links

TUTORIAL_FENCE 15 docs/start/first-bob-day.md:154
{"config":{"decay":{"enabled":true,"enter":null,"keeps":3,"limits":{"next":3,"pending":3,"ready":3}},"interval":7,"next_interval":1,"pending_interval":1,"post_stages":[],"pre_stages":[],"project_interval":null,"rotten_daily_budget":null},"counts":{"budget":null,"budget_met":false,"by_tier":{"new":1,"next":0,"pending":0,"post":0,"pre":0,"projects":1,"recurring":0,"rotten":0,"tickler":0},"decide":0,"due":2,"fresh":0,"new":2,"next_due":0,"pending_due":0,"post_due":0,"pre_due":0,"projects_due":1,"recurring_due":0,"refreshed_today":1,"resurfaced":0,"rotten":0,"upkeep_today":1,"walk":2},"date":"2026-10-20","ok":true,"queue":[{"block_id":"seed-packet","bucket":"new","created":"2026-10-20","days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":7,"path":"mac_inbox.md","rank":1,"returned_by":null,"scheduled":null,"stage":null,"stage_rank":null,"stage_total":null,"state":"new","status_symbol":" ","text":"Sort the seed packets ^seed-packet","tier":"new","unblocked_on":null},{"block_id":"prj","bucket":"new","created":null,"days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":11,"path":"Projects/seedlings.md","rank":2,"returned_by":null,"scheduled":null,"stage":null,"stage_rank":null,"stage_total":null,"state":"new","status_symbol":" ","text":"#prj Raise healthy seedlings for the garden ^prj","tier":"projects","unblocked_on":null}],"schema_version":16,"warnings":[]}
skipped: docs/start/install.md:16: network clone needs a remote and user credentials
skipped: docs/start/install.md:27: toolchain install changes the host and needs network
skipped: docs/start/install.md:42: install writes outside the tutorial sandbox
skipped: docs/start/install.md:66: PATH export edits the reader shell profile
skipped: docs/start/install.md:92: network install needs a remote and writes outside the sandbox
skipped: docs/start/obsidian.md:18: opening Obsidian needs the desktop app
skipped: docs/start/obsidian.md:28: Tasks install needs the Obsidian app and network
skipped: docs/start/obsidian.md:52: plugin clone needs network and a plugin source checkout
skipped: docs/start/obsidian.md:69: plugin sync needs a plugin source checkout and Obsidian
skipped: docs/start/mac-capture.md:19: Mac build needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:26: Mac bundle needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:33: Mac install needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:40: Mac launch needs the Mac app bundle
skipped: docs/start/mac-capture.md:54: panel setup needs the Mac app
skipped: docs/start/mac-capture.md:81: first Mac capture needs the Mac panel
tutorial: passed
docs-check: passed (executable first-day tutorial)

docs-check: CLI media determinism
media: check passed (regeneration is byte-stable)
docs-check: passed (CLI media determinism)

docs-check: documentation unit tests
============================= test session starts ==============================
platform linux -- Python 3.14.7, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/tools/docs
configfile: pyproject.toml
plugins: platformdirs-4.13.5
collected 448 items

tools/docs/tests/test_assemble.py ....                                   [  0%]
tools/docs/tests/test_assets.py .....s.                                  [  2%]
tools/docs/tests/test_capture_token_coverage.py ..                       [  2%]
tools/docs/tests/test_check.py ....                                      [  3%]
tools/docs/tests/test_compatibility.py ......                            [  5%]
tools/docs/tests/test_contracts.py ........                              [  6%]
tools/docs/tests/test_demo_tasks.py ..                                   [  7%]
tools/docs/tests/test_edit_links.py ....                                 [  8%]
tools/docs/tests/test_environment.py ........                            [ 10%]
tools/docs/tests/test_fences.py .......                                  [ 11%]
tools/docs/tests/test_gen_components.py ....                             [ 12%]
tools/docs/tests/test_gen_plugins.py ...........                         [ 14%]
tools/docs/tests/test_gen_reference.py ........                          [ 16%]
tools/docs/tests/test_generated.py .....                                 [ 17%]
tools/docs/tests/test_host.py ..................                         [ 21%]
tools/docs/tests/test_host_workflow.py .........                         [ 23%]
tools/docs/tests/test_links.py ...........                               [ 26%]
tools/docs/tests/test_links_online.py ......                             [ 27%]
tools/docs/tests/test_lint.py .......................................... [ 37%]
................                                                         [ 40%]
tools/docs/tests/test_media.py .........                                 [ 42%]
tools/docs/tests/test_mounts.py ........................................ [ 51%]
....................................                                     [ 59%]
tools/docs/tests/test_publish_drill.py ..........                        [ 61%]
tools/docs/tests/test_publish_issue.py .............                     [ 64%]
tools/docs/tests/test_publish_plan.py ........................           [ 70%]
tools/docs/tests/test_publish_record.py ..............                   [ 73%]
tools/docs/tests/test_publish_verify.py ...........                      [ 75%]
tools/docs/tests/test_publish_workflow.py .........................      [ 81%]
tools/docs/tests/test_search_smoke.py ........                           [ 83%]
tools/docs/tests/test_templates.py .....                                 [ 84%]
tools/docs/tests/test_tutorial.py ..................                     [ 88%]
tools/docs/tests/test_urls.py .........................                  [ 93%]
tools/docs/tests/test_weekly_issue.py ......                             [ 95%]
tools/docs/tests/test_weekly_workflow.py ....................            [ 99%]
tools/docs/tests/test_yaml_tools.py ..                                   [100%]

=========================== short test summary info ============================
SKIPPED [1] tools/docs/tests/test_assets.py:75: generation dependencies are absent (run with --group fonts)
======================= 447 passed, 1 skipped in 45.26s ========================
running: uv run --project tools/docs --group material pytest tools/docs/tests
docs-check: passed (documentation unit tests)

docs-check: follow-on gates
skipped: CLI reference golden is a cargo test, not a docs-check gate

docs-check: all implemented gates passed
succeeded  exit=0  duration=291277ms

