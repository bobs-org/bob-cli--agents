# Chat History - ace-run (bob-cli-na.land--mon)

- **TIMESTAMP:** 2026-11-18 17:55:19 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-na.land--mon

## Prompt

sase monitor start --command 'cargo test --lib albums && cargo test --lib capture && just check' --reason 'Run the remaining record-walk library tests and just check before epic closeout'

## Response

sase: tool run not reserved (tool run store is busy: timed out waiting to enable WAL journal mode: database is locked); running wrapped
sase tool run 3076a19a599159fd36f323fb190897c3
   Compiling bob-obsidian v0.5.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3454:26
     |
3454 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 3m 55s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261118_110828/build/debug/deps/bob_cli-360fc3cff622e271)

running 145 tests
test native::albums::create::tests::default_title_humanizes_the_stem ... ok
test native::albums::create::tests::input_validation_refuses_and_warns ... ok
test native::albums::create::tests::renders_canonical_key_order_h1_intro_and_label ... ok
test native::albums::create::tests::album_schema_emitter_uses_indented_yaml_sequences ... ok
test native::albums::create::tests::stems_normalize_to_lowercase_routes ... ok
test native::albums::create::tests::plan_refuses_dangling_symlink_destinations ... ok
test native::albums::grouping::tests::default_facets_skip_group_field_and_keep_index_by ... ok
test native::albums::create::tests::plan_refuses_case_insensitive_non_file_destinations ... ok
test native::albums::catalog::tests::catalog_dependencies_notice_an_ordinary_note_becoming_an_album ... ok
test native::albums::create::tests::plans_the_album_base_and_owner_catalog_from_one_overlay ... ok
test native::albums::grouping::tests::explicit_facets_keep_author_order ... ok
test native::albums::create::tests::plan_refuses_existing_destinations_claims_parents_and_folders ... ok
test native::albums::catalog::tests::damaged_host_plans_are_not_current ... ok
test native::albums::catalog::tests::overlay_reparent_keeps_the_old_owner_as_a_removal_plan ... ok
test native::albums::catalog::tests::rows_sort_direct_albums_then_path_qualified_owner_groups ... ok
test native::albums::create::tests::stale_plan_notices_an_ordinary_note_becoming_a_claim ... ok
test native::albums::create::tests::verify_rejects_a_damaged_required_host ... ok
test native::albums::catalog::tests::catalog_dependencies_notice_a_nested_identity_change ... ok
test native::albums::create::tests::stale_plan_notices_a_collision_introduced_after_planning ... ok
test native::albums::grouping::tests::first_choices_field_wins_without_status ... ok
test native::albums::grouping::tests::no_choices_means_no_groups ... ok
test native::albums::grouping::tests::missing_unknown_and_invalid_shapes_count_as_needs_status ... ok
test native::albums::grouping::tests::status_choices_lead_and_empty_groups_are_omitted ... ok
test native::albums::grouping::tests::missing_index_by_values_sort_last_under_an_em_dash ... ok
test native::albums::grouping::tests::large_index_by_group_orders_peeks_by_folded_value_then_title ... ok
test native::albums::grouping::tests::thirteen_members_with_one_folded_value_stay_flat ... ok
test native::albums::grouping::tests::twelve_members_stay_flat_even_with_two_index_values ... ok
test native::albums::grouping::tests::subgroup_heading_prefers_plain_text_on_a_frequency_tie ... ok
test native::albums::index::tests::eat_shaped_index_is_byte_exact ... ok
test native::albums::create::tests::stale_plan_notices_a_nested_identity_and_host_preimage_change ... ok
test native::albums::index::tests::empty_album_renders_the_teaching_index ... ok
test native::albums::index::tests::group_is_large_threshold_matches_contract ... ok
test native::albums::index::tests::fences_bom_and_crlf_are_preserved ... ok
test native::albums::index::tests::hostile_title_and_facets_are_escaped ... ok
test native::albums::index::tests::first_insert_and_second_render_are_stable ... ok
test native::albums::index::tests::incomplete_folder_or_missing_text_is_damaged ... ok
test native::albums::index::tests::lists_and_links_and_empty_facets ... ok
test native::albums::index::tests::movies_shaped_flat_index_keeps_numeric_facets ... ok
test native::albums::index::tests::explicit_facets_keep_location_on_grouped_rows ... ok
test native::albums::index::tests::grouped_rows_drop_the_repeated_location_facet ... ok
test native::albums::index::tests::moved_callout_stays_put_and_duplicates_heal ... ok
test native::albums::index::tests::path_tie_breaks_equal_titles ... ok
test native::albums::index::tests::podcasts_shaped_index_uses_icon_free_labels ... ok
test native::albums::index::tests::malformed_member_keeps_filename_fallback_in_needs_status ... ok
test native::albums::index::tests::hostile_plural_and_choice_labels_stay_on_one_inert_line ... ok
test native::albums::index::tests::tally_text_uses_singular_for_one_and_plural_otherwise ... ok
test native::albums::registry::tests::record_recognition_uses_album_claims ... ok
test native::albums::registry::tests::broken_album_claim_does_not_hide_a_valid_album ... ok
test native::albums::registry::tests::malformed_album_schema_does_not_hide_valid_album ... ok
test native::albums::registry::tests::parent_scope_handles_unquoted_terminal_project_cycles_and_checkboxes ... ok
test native::albums::registry::tests::duplicate_nouns_and_property_storage_conflicts_mark_every_album ... ok
test native::albums::index::tests::tv_shaped_index_keeps_acronym_singular_and_plural ... ok
test native::albums::registry::tests::identical_album_stems_are_scoped_to_the_supplied_vault ... ok
test native::albums::registry::tests::route_head_refuses_traversal_absolute_and_reserved_stems ... ok
test native::albums::registry::tests::target_head_resolution_does_not_read_album_body_or_record_folders ... ok
test native::albums::registry::tests::broken_noun_recovery_preserves_album_claims ... ok
test native::albums::registry::tests::route_head_refuses_a_symlink_escape_and_foreign_known_registry ... ok
test native::albums::report::tests::album_schema_fingerprint_ignores_yaml_formatting ... ok
test native::albums::registry::tests::album_parent_validation_and_notebook_parent_regression ... ok
test native::albums::tests::invalid_field_options_have_physical_line_and_full_key_path ... ok
test native::albums::tests::album_type_spellings_match_existing_frontmatter_grammar ... ok
test native::albums::tests::block_and_flow_schema_preserve_field_and_choice_order ... ok
test native::albums::tests::all_existing_field_kinds_defaults_bounds_and_lists_are_reused ... ok
test native::albums::tests::invalid_schema_keeps_the_noun_claim ... ok
test native::albums::tests::malformed_flow_yaml_retains_a_recoverable_noun_claim ... ok
test native::albums::tests::album_nouns_stems_and_index_metadata_are_validated ... ok
test native::albums::tests::nested_repeated_key_lines_follow_the_full_path ... ok
test native::albums::tests::top_level_album_facts_do_not_read_nested_record_fields ... ok
test native::albums::tests::optional_fields_and_display_defaults_include_acronym_plural_rule ... ok
test native::albums::sync::tests::combined_plan_includes_the_owner_catalog_edit ... ok
test native::albums::update::ops::tests::envelope_examples_parse_for_the_span_phase ... ok
test native::albums::tests::noun_recovery_keeps_only_a_direct_record_noun ... ok
test native::albums::update::ops::tests::derived_key_collisions_reserved_and_invalid_refuse ... ok
test native::albums::sync::tests::record_frontmatter_is_guarded_but_its_body_is_not ... ok
test native::albums::registry::tests::stem_noun_and_case_insensitive_folder_collisions_invalidate_all_claims ... ok
test native::albums::report::tests::album_schema_fingerprint_tracks_order_and_semantic_changes ... ok
test native::albums::registry::tests::snapshot_retains_album_claims_and_reclassifies_overlays ... ok
test native::albums::sync::tests::walk_member_body_edit_after_planning_refuses_and_writes_nothing ... ok
test native::albums::update::ops::tests::atomic_last_choice_replacement_allows_empty_intermediate ... ok
test native::albums::update::ops::tests::field_remove_inverse_preserves_keys_and_absent_label ... ok
test native::albums::sync::tests::owner_preimage_and_new_album_membership_are_guarded ... ok
test native::albums::update::ops::tests::prohibited_kind_change_carries_target_and_count ... ok
test native::albums::update::ops::tests::every_operation_applies_and_reports ... ok
test native::albums::update::ops::tests::forbidden_edits_return_typed_refusals_with_counts ... ok
test native::albums::update::ops::tests::required_and_bound_changes_report_newly_invalid ... ok
test native::albums::update::ops::tests::kind_specific_defaults_validate_through_the_shared_validator ... ok
test native::albums::update::ops::tests::incomplete_scans_and_malformed_members_cannot_prove_unused ... ok
test native::albums::update::ops::tests::required_url_counts_newly_invalid ... ok
test native::albums::update::ops::tests::list_values_false_and_zero_count_as_filled ... ok
test native::albums::update::ops::tests::unset_is_distinct_from_false_zero_and_empty ... ok
test native::albums::update::ops::tests::semantic_inverses_restore_order_and_identity ... ok
test native::albums::update::ops::tests::missing_targets_and_position_edges_refuse ... ok
test native::albums::update::protocol::tests::empty_ops_are_a_valid_no_op ... ok
test native::albums::update::ops::tests::group_prefers_status_over_first_choices ... ok
test native::albums::update::protocol::tests::duplicate_keys_refuse_the_envelope ... ok
test native::albums::update::protocol::tests::stdin_convention_is_documented_for_the_command_layer ... ok
test native::albums::update::protocol::tests::unknown_versions_ops_and_keys_refuse ... ok
test native::albums::update::protocol::tests::restoration_metadata_is_typed_and_limited_to_schema_key_paths ... ok
test native::albums::update::protocol::tests::wrong_types_and_malformed_input_refuse ... ok
test native::albums::update::ops::tests::ordered_batches_use_stable_keys_from_earlier_ops ... ok
test native::albums::update::plan::tests::empty_operations_do_not_repair_a_missing_index ... ok
test native::albums::sync::tests::album_preimage_and_folder_membership_are_guarded ... ok
test native::albums::update::plan::tests::incomplete_record_scan_refuses_before_index_planning ... ok
test native::albums::update::spans::tests::duplicate_record_keys_refuse ... ok
test native::albums::update::spans::tests::aliases_inside_record_refuse_but_external_plain_comment_is_safe ... ok
test native::albums::update::spans::tests::quoted_punctuation_is_not_an_anchor_token ... ok
test native::albums::walk::tests::insert_uses_frontmatter_newline_and_preserves_bom ... ok
test native::albums::update::spans::tests::no_op_keeps_original_bytes_and_index_placement ... ok
test native::albums::walk::tests::insertion_without_a_frontmatter_newline_uses_lf_and_preserves_prose ... ok
test native::albums::update::spans::tests::net_semantic_noop_returns_original_bytes ... ok
test native::albums::create::tests::apply_refuses_a_stale_plan_without_writing ... ok
test native::albums::walk::tests::incomplete_frontmatter_is_damaged_and_never_written ... ok
test native::albums::walk::tests::moved_stale_walk_line_is_replaced_in_place_and_is_idempotent ... ok
test native::albums::walk::tests::parser_accepts_canonical_and_rejects_extra_text ... ok
test native::albums::walk::tests::singleton_blank_body_gets_one_trailing_newline ... ok
test native::albums::walk::tests::trim_arrow_edges_before_markdown_escaping ... ok
test native::albums::walk::tests::walk_matcher_mirror_keeps_the_hub_out_of_both_directions ... ok
test native::albums::write::tests::overlay_ignores_non_direct_members ... ok
test native::albums::walk::tests::shared_order_label_line_and_recognition_vectors ... ok
test native::albums::write::tests::overlay_replaces_by_path_without_appending ... ok
test native::albums::write::tests::album_guard_refuses_even_when_no_edit_was_needed ... ok
test native::albums::update::plan::tests::schema_change_composes_with_index_and_guards_record_inputs ... ok
test native::albums::write::tests::staged_record_matches_disk_decode ... ok
test native::capture::tests::placement::generated_albums_section_is_never_a_bullet_target ... ok
test native::albums::write::tests::plan_repairs_a_missing_index_without_touching_other_bytes ... ok
test native::host_catalog::region::tests::albums_duplicates_self_heal_to_first ... ok
test native::bank::subscriptions::projection::tests::missing_and_invalid_albums_force_null_false_projection ... ok
test native::host_catalog::region::tests::crlf_and_bom_survive_albums_edits ... ok
test native::capture::tests::placement::explicit_albums_selector_refuses_instead_of_falling_through ... ok
test native::host_catalog::region::tests::empty_subtree_deletes_albums_heading_and_keeps_notebooks ... ok
test native::capture::tests::placement::generated_albums_section_is_never_completed ... ok
test native::host_catalog::region::tests::fences_and_frontmatter_stay_inert_for_albums ... ok
test native::albums::update::spans::tests::field_value_edit_preserves_comments_and_inverse_restores_exact_quote_bytes ... ok
test native::albums::write::tests::damaged_folder_and_unreadable_member_are_damaged ... ok
test native::albums::write::tests::two_file_install_refuses_on_album_drift_and_rolls_back ... ok
test native::parent_notes::tests::broken_albums_refuse_without_inventing_owner_or_noun ... ok
test native::albums::update::spans::tests::tampered_restore_cannot_change_unrelated_fields ... ok
test native::parent_notes::tests::albums_refuse_as_task_parents_with_owner_guidance ... ok
test native::albums::update::spans::tests::inserted_defaults_use_indented_obsidian_sequence_items ... ok
test native::albums::update::spans::tests::field_and_choice_moves_carry_original_entry_slices ... ok
test native::albums::update::spans::tests::unlabeled_field_and_diverged_choices_round_trip_byte_identical ... ok
test native::albums::walk::tests::radius_in_an_unbackfilled_album_edits_only_new_record_and_changed_neighbours ... ok
test native::albums::create::tests::rollback_preserves_an_intervening_owner_edit ... ok
test native::albums::create::tests::verify_failure_rolls_back_album_base_and_owner ... ok
test native::albums::walk::tests::ring_is_a_cycle_and_matches_the_index_tally ... ok

test result: ok. 145 passed; 0 failed; 0 ignored; 0 measured; 7240 filtered out; finished in 0.95s

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3454:26
     |
3454 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 1 warning (run `cargo fix --lib -p bob-obsidian --tests` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.21s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261118_110828/build/debug/deps/bob_cli-360fc3cff622e271)

running 2148 tests
test native::capture::batch::move_order_tests::cyclic_move_order_refuses_before_returning_staged_files ... ok
test native::capture::batch::move_order_tests::replacement_order_is_stable_and_destinations_precede_sources ... ok
test native::capture::batch::move_order_tests::read_guard_rejects_metadata_drift_after_classification ... ok
test native::capture::budget::tests::destination_roles_follow_the_contract ... ok
test native::capture::batch_move::tests::batch_replacement_order_writes_destinations_before_sources ... ok
test native::capture::dependencies::tests::new_prj_edges_check_implicit_resident_cycles ... ok
test native::capture::event_conflict::tests::messages_name_the_buffer_the_overlap_sits_in ... ok
test native::capture::blocked_tasks::tests::always_mints_when_blocks_lines_is_off ... ok
test native::capture::event_conflict::tests::meet_sessions_and_own_lineup_and_old_span_are_exempt ... ok
test native::capture::event_conflict::tests::buffered_fit_ends_at_the_buffered_start_and_only_before_it ... ok
test native::capture::event_conflict::tests::mid_meeting_start_reports_event_in_progress_without_untracked ... ok
test native::capture::event_conflict::tests::more_counts_later_crossings ... ok
test native::capture::event_conflict::tests::plus_and_shift_fits_and_no_fit_when_the_start_is_the_event ... ok
test native::capture::event_conflict::tests::start_fit_drafts_keep_the_later_sign ... ok
test native::capture::event_conflict::tests::start_fit_is_largest_count_ending_at_the_event ... ok
test native::capture::event_conflict::tests::untracked_events_warn_and_named_starts_keep_the_hash ... ok
test native::capture::event_conflict::tests::unbuffered_payloads_omit_the_buffer_keys ... ok
test native::capture::dependency_drop::tests::partial_drop_keeps_verbatim_history_and_unresolved_links_and_field_ids ... ok
test native::capture::batch_move::tests::changed_repair_note_refuses_the_move_snapshot ... ok
test native::capture::budget::tests::no_grown_daily_component_skips_theme_catalog ... ok
test native::capture::dependencies::tests::prefiltered_snapshot_matches_full_read ... ok
test native::capture::keep_moving_net::tests::explicit_relinks_count_even_when_the_live_set_is_unchanged ... ok
test native::capture::keep_moving_net::tests::gaps_compare_against_the_nearest_earlier_step ... ok
test native::capture::keep_moving_net::tests::later_effects_are_the_links_added_after_the_group_item ... ok
test native::capture::inbox_route::tests::ir_snapshot_binding_refuses_when_unstaged_dest_or_repair_changes ... ok
test native::capture::blocked_tasks::tests::existing_owner_is_uncapped_at_in_progress ... ok
test native::capture::keep_moving_net::tests::row_project_falls_back_to_the_row_note ... ok
test native::capture::inbox_route::tests::ir_route_refusal_blames_the_failing_second_member ... ok
test native::capture::inbox_route::tests::ir_nested_status_uses_root_and_idless_tasks_get_stable_keys ... ok
test native::capture::link_guard::tests::new_task_flip_blocks_open_lines_tags_blocked_and_skips_closed ... ok
test native::capture::blocked_tasks::tests::relocate_by_id_after_id_stamp_and_lane_promotion ... ok
test native::capture::dependency_drop::tests::duplicate_or_malformed_managed_lines_refuse_without_staging ... ok
test native::capture::dependency_drop::tests::last_dependency_line_and_field_are_removed_with_crlf_and_final_newline_preserved ... ok
test native::capture::blocked_tasks::tests::nested_dependent_path_is_addressed_by_relative_and_block_id ... ok
test native::capture::meet_event_run::tests::dropped_numbers_keep_pre_image_numbering ... ok
test native::capture::link_guard::tests::ordinary_unblocked_target_skips_the_vault_graph ... ok
test native::capture::meet_event_run::tests::buffered_spans_drive_candidates_sort_and_clustering ... ok
test native::capture::meet_event_run::tests::later_offsets_round_forward_and_use_checked_arithmetic ... ok
test native::capture::meet_event_run::tests::far_run_label_adds_the_span_and_buffer_only_when_buffered ... ok
test native::capture::inbox_route::tests::ir_identical_idless_roots_route_together_with_exact_landings ... ok
test native::capture::link_guard::tests::tagged_prj_forces_the_vault_graph ... ok
test native::capture::meet_event_run::tests::ended_done_cancelled_and_foreign_links_are_skipped ... ok
test native::capture::meet_event_run::tests::finalize_writes_the_calendar_span_and_clamps_late_joins ... ok
test native::capture::meet_event_run::tests::run_extends_over_touching_events_with_the_same_clock_classification ... ok
test native::capture::meet_event_run::tests::unnamed_start_skips_ended_and_done_events ... ok
test native::capture::link_guard::tests::inherited_reason_blocks_pull_forward ... ok
test native::capture::link_guard::tests::unblocked_project_resident_skips_the_vault_graph ... ok
test native::capture::link_guard::tests::tagged_destination_blocks_a_new_task ... ok
test native::capture::link_guard::tests::tagged_project_resident_forces_the_vault_graph ... ok
test native::capture::meet_event_run::tests::unnamed_start_uses_buffered_lead_in_and_lead_out ... ok
test native::capture::meet_event_run::tests::unnamed_start_picks_the_earliest_overlapping_meet ... ok
test native::capture::meet_event_run::tests::unnamed_start_without_a_meet_keeps_the_first_future ... ok
test native::capture::meet_event_run::tests::untracked_run_breaks_at_a_contiguous_tracked_event ... ok
test native::capture::meet_event_run::tests::unnamed_start_picks_meet_when_the_start_block_overlaps_the_run ... ok
test native::capture::move_consequence::tests::actual_details_share_prediction_copy_and_preserve_followed_link_text ... ok
test native::capture::blocked_tasks::tests::prj_internal_same_note_and_descendant_refuse ... ok
test native::capture::link_guard::tests::capture_into_unblocked_project_skips_the_vault_graph ... ok
test native::capture::blocked_tasks::tests::next_cap_holds_in_progress_dependent_and_prj_resident ... ok
test native::capture::move_consequence::tests::predicts_dependency_drop_pull_forward_and_existing_link ... ok
test native::capture::move_consequence::tests::predicts_sticky_lanes_and_guarded_blocked_moves ... ok
test native::capture::move_consequence::tests::pull_forward_and_dependency_drop_keep_the_date ... ok
test native::capture::move_consequence::tests::unnamed_existing_link_uses_today_wording ... ok
test native::capture::note_pull::tests::np11_scheduled_project_names_date_reason ... ok
test native::capture::note_pull::tests::np10_empty_refusals_carry_fold_and_write_nothing ... ok
test native::capture::note_pull::tests::batch_later_missing_note_rolls_back_earlier_creation ... ok
test native::capture::note_pull::tests::np12_missing_source_refuses_pull_note_missing ... ok
test native::capture::note_pull::tests::blocked_project_counts_only_open_prerequisites ... ok
test native::capture::note_pull::tests::np11_blocked_project_names_prj_reason ... ok
test native::capture::inbox_route::tests::ir_routed_batch_rolls_back_when_a_repaired_file_changes ... ok
test native::capture::blocked_tasks::tests::a8_refusals_name_star_and_teach ... ok
test native::capture::note_pull::tests::batch_repeated_source_second_pull_pruned_not_refused ... ok
test native::capture::note_pull::tests::np15_none_selection_writes_nothing_and_mints_nothing ... ok
test native::capture::note_pull::tests::np13_require_choice_without_picks_refuses ... ok
test native::capture::note_pull::tests::np1_no_pick_reports_lane_order_and_writes_nothing ... ok
test native::capture::note_pull::tests::np22_unavailable_proof_folds_candidate_blocked ... ok
test native::capture::note_pull::tests::np19_hand_off_owns_row_later_pull_omits ... ok
test native::capture::note_pull::tests::np23_missing_day_uses_existing_error ... ok
test native::capture::note_pull::tests::np21_subset_pick_links_only_picked_row ... ok
test native::capture::note_pull::tests::np20_two_pulls_keep_item_order_and_continue_numbers ... ok
test native::capture::note_pull::tests::np23_day_without_pomodoros_uses_existing_error ... ok
test native::capture::note_pull::tests::np17_same_draft_creation_offered_without_fresh_stamp ... ok
test native::capture::note_pull::tests::batch_pull_then_transfer_move_follows_picked_row ... ok
test native::capture::note_pull::tests::np2_pick_all_links_statuses_mints_and_stamps ... ok
test native::capture::note_pull::tests::fold_gating_closed_prereq_keeps_later_filter ... ok
test native::capture::note_pull::tests::np8_closed_statuses_ignored_uncounted ... ok
test native::capture::note_pull::tests::batch_selected_handoff_owns_row_later_pull_omits ... ok
test native::capture::note_pull::tests::batch_pull_then_project_move_follows_picked_row ... ok
test native::capture::note_pull::tests::np3_live_link_folds_already_planned ... ok
test native::capture::offer_verdicts::verdict_copy_tests::tickler_lines_cover_only_stamped_rows ... ok
test native::capture::offer_verdicts::verdict_copy_tests::unblock_suffix_counts_recovered_rows ... ok
test native::capture::offer_verdicts::verdict_copy_tests::verdict_messages_use_would_forms_on_dry_runs ... ok
test native::capture::output::tests::all_unblocked_covers_nested_relation_summaries_in_order ... ok
test native::capture::output::tests::all_unblocked_includes_project_note_successors ... ok
test native::capture::output::tests::capture_destination_swatches_respect_no_color ... ok
test native::capture::output::tests::clip_file_confirmations_pad_verbs_and_append_sizes ... ok
test native::capture::output::tests::clipboard_history_summary_uses_provider_and_known_endpoint_ages ... ok
test native::capture::output::tests::complete_effect_omitted_when_none ... ok
test native::capture::output::tests::create_project_note_omits_form_and_successors ... ok
test native::capture::output::tests::log_entry_details_omitted_when_empty ... ok
test native::capture::output::tests::project_created_offer_header_reads_new_project ... ok
test native::capture::output::tests::relation_completes_omits_already_closed_rows ... ok
test native::capture::output::tests::relation_completes_omitted_when_empty ... ok
test native::capture::output::tests::typed_entry_details_print_two_spaces_under_their_entry ... ok
test native::capture::output::tests::typed_work_log_details_align_with_entries_when_present ... ok
test native::capture::output::tests::typed_work_log_details_omitted_when_no_entry_has_details ... ok
test native::capture::output::tests::unblocked_vecs_mut_reaches_nested_rows ... ok
test native::capture::pomodoro_adjust::tests::format_adjusted_range_preserves_missing_duration ... ok
test native::capture::pomodoro_adjust::tests::session_clock_classifies_worked_off_clock_conflict_and_placeholder ... ok
test native::capture::pomodoro_adjust::tests::set_ledger_clock_moves_the_recorded_duration_between_keys ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_fenced_child_lines_verbatim ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_tab_children_and_interior_blanks ... ok
test native::capture::pomodoro_blocks::tests::block_range_stops_at_section_end_and_covers_last_entry ... ok
test native::capture::pomodoro_blocks::tests::block_range_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::block_range_trims_trailing_blanks_and_stops_at_zero_indent ... ok
test native::capture::pomodoro_blocks::tests::depth_continuation_lines_take_parent_depth_plus_one ... ok
test native::capture::pomodoro_blocks::tests::depth_counts_nested_list_items ... ok
test native::capture::pomodoro_blocks::tests::depth_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::forwarding_panics_when_a_tracked_headline_is_deleted - should panic ... ok
test native::capture::pomodoro_blocks::tests::pairing_created_block_is_all_added ... ok
test native::capture::pomodoro_blocks::tests::pairing_pure_insert_is_added_and_pure_delete_is_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_replace_becomes_changed_with_before ... ok
test native::capture::pomodoro_blocks::tests::pairing_uneven_replace_splits_changed_added_removed ... ok
test native::capture::pomodoro_blocks::tests::resolution_rejects_a_non_entry_after - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_autodetects_an_unreported_child_insert ... ok
test native::capture::pomodoro_blocks::tests::tracker_forwards_a_tracked_block_across_an_insert_above ... ok
test native::capture::note_pull::tests::batch_duplicate_idless_second_row_selects_alone ... ok
test native::capture::pomodoro_blocks::tests::tracker_resolves_created_before_and_reports_roles_once ... ok
test native::capture::pomodoro_blocks::tests::tracker_reports_one_cumulative_block_across_items ... ok
test native::capture::pomodoro_blocks::tests::unreported_headline_rewrite_emits_unchanged_block - should panic ... ok
test native::capture::pomodoro_blocks::tests::vanished_entry_is_dropped_silently - should panic ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_exactly_at_end ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_mid_session ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_overnight_wrap_is_not_overdue ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_past_the_end ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_start_later_than_now ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_unparsable_range ... ok
test native::capture::pomodoro_timeline::tests::both_pins_layout_runs_in_typed_order ... ok
test native::capture::pomodoro_timeline::tests::empty_future_and_back_to_back_days_are_handled ... ok
test native::capture::pomodoro_timeline::tests::end_pins_check_now_midnight_and_empty_room ... ok
test native::capture::pomodoro_timeline::tests::equal_end_segments_sort_later_start_then_later_line_first ... ok
test native::capture::note_pull::tests::np5_fold_precedence_and_today_scheduled_offered ... ok
test native::capture::pomodoro_timeline::tests::every_layout_cut_and_limit_error_is_accounted_for ... ok
test native::capture::pomodoro_timeline::tests::errors_and_out_of_range_listing_are_structured ... ok
test native::capture::pomodoro_timeline::tests::example_catalog_numbers_segments_and_resolves_every_pin ... ok
test native::capture::pomodoro_timeline::tests::example_layouts_match_the_acceptance_windows ... ok
test native::capture::pomodoro_timeline::tests::off_clock_rows_are_timeline_rows_and_midnight_edges_stay_bounded ... ok
test native::capture::pomodoro_timeline::tests::tail_at_close_is_empty_and_stale_open_rows_do_not_make_gaps ... ok
test native::capture::pomodoro_timeline::tests::short_slivers_are_unnumbered_and_overlaps_keep_each_closed_row ... ok
test native::capture::pomodoro_timeline::tests::walls_bound_the_tail_and_start_pins ... ok
test native::capture::project_deps::tests::descendant_notes_are_internal_prj_targets ... ok
test native::capture::project_deps::tests::kept_notes_text_strips_tags_fields_and_ids ... ok
test native::capture::project_deps::tests::kept_notes_text_flattens_block_links ... ok
test native::capture::project_deps::tests::prj_gate_matches_only_recognised_projects ... ok
test native::capture::project_deps::tests::resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range ... ok
test native::capture::project_deps::tests::resident_block_edits_idless_rows_and_rechecks_shifted_fences ... ok
test native::capture::project_deps::tests::resident_block_flips_tags_and_skips_prj_and_closed ... ok
test native::capture::project_deps::tests::strongest_lane_ignores_closed_and_outsiders ... ok
test native::capture::project_deps::tests::removed_refs_and_consumed_lines_use_the_items_pre_state_coordinates ... ok
test native::capture::note_pull::tests::np7_only_source_residents_offered ... ok
test native::capture::project_deps::tests::consumption_resolves_alias_basename_path_case_and_local_links_by_identity ... ok
test native::capture::project_note::tests::offer_named_without_tasks_is_refused ... ok
test native::capture::project_note::tests::create_omits_offer_fields_and_iterator_skips_them ... ok
test native::capture::note_pull::tests::np6_own_prj_never_offered_or_counted ... ok
test native::capture::note_pull::tests::np9_ref_nested_recurring_offered ... ok
test native::capture::pull_in::offer_json_tests::merged_from_is_additive_and_absent_for_existing_offers ... ok
test native::capture::note_pull::tests::np18_later_link_drops_earlier_pull_row ... ok
test native::capture::note_pull::tests::batch_pull_move_pull_destination_dedups_and_source_omits ... ok
test native::capture::relation_sources::tests::a_fresh_context_observes_new_disk_edges_without_a_persistent_cache ... ok
test native::capture::note_pull::tests::offer_close_post_pass_reuses_one_dependency_snapshot ... ok
test native::capture::note_pull::tests::staged_closed_prerequisite_is_visible_to_note_pull_snapshot ... ok
test native::capture::note_pull::tests::np4_struck_or_closed_links_stay_offered ... ok
test native::capture::relation_sources::tests::dependency_snapshot_does_not_surface_unconsulted_relation_warning ... ok
test native::capture::relation_sources::tests::cheap_gate_rejects_without_catalog_or_source_reads ... ok
test native::capture::relation_sources::tests::marker_negative_target_loads_through_planner_and_missing_is_unavailable ... ok
test native::capture::relation_sources::tests::relation_archive_rules_exclude_done_directories_but_keep_done_md ... ok
test native::capture::relation_sources::tests::parked_only_event_selects_sources_and_loads_its_target ... ok
test native::capture::relation_sources::tests::relation_snapshot_drops_links_notes_without_event_token ... ok
test native::capture::relation_sources::tests::matched_source_dependency_proof_skips_unrelated_id_notes ... ok
test native::capture::relations_mentions::tests::vanished_occurrences_preserve_mirrors_when_postimage_is_uncertain ... ok
test native::capture::shell_guard::tests::at_prefixed_regular_files_trigger ... ok
test native::capture::relation_sources::tests::unreadable_links_note_taints_when_event_token_does_not_match ... ok
test native::capture::relation_sources::tests::either_consumer_order_walks_and_reads_the_catalog_once ... ok
test native::capture::shell_guard::tests::drafts_without_an_expanded_home_are_not_refused ... ok
test native::capture::shell_guard::tests::expanded_tildes_are_restored_in_place ... ok
test native::capture::shell_guard::tests::directories_and_missing_files_do_not_trigger ... ok
test native::capture::shell_guard::tests::pipes_do_not_trigger ... ok
test native::capture::task_blocks::tests::block_range_maps_byte_end_to_line_range ... ok
test native::capture::relation_sources::tests::source_snapshot_uses_shared_parser_resolver_and_narrow_target_reads ... ok
test native::capture::relation_sources::tests::staged_overlay_adds_edits_and_deletions_and_masks_read_failures ... ok
test native::capture::relation_sources::tests::zero_matching_sources_returns_empty_source_and_dependency_notes ... ok
test native::capture::project_note::tests::offer_scratch_placement_does_not_commit_probe_ids ... ok
test native::capture::project_note::tests::offer_iterator_and_completion_count_see_project_rows ... ok
test native::capture::project_note::tests::offer_none_keeps_create_files_and_emits_unselected_rows ... ok
test native::capture::task_blocks::tests::crlf_note_reports_verbatim_texts_without_terminators ... ok
test native::capture::task_blocks::tests::authored_children_and_schedule_log_are_added_in_order ... ok
test native::capture::task_blocks::tests::interior_blank_lines_are_kept_in_the_block ... ok
test native::capture::task_blocks::tests::created_parent_reports_every_row_added ... ok
test native::capture::task_blocks::tests::toggle_plus_subbullet_shows_the_task_line_as_changed ... ok
test native::capture::task_blocks::tests::locally_routed_batch_reports_one_block_with_two_added_rows ... ok
test native::capture::project_note::tests::offer_all_mints_ids_and_links_like_colon_bullets ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_schedule_log ... ok
test native::capture::task_blocks::tests::nested_parent_reports_depths_relative_to_its_line ... ok
test native::capture::task_blocks::tests::cross_note_first_touch_order_with_revisit_and_second_parent ... ok
test native::capture::task_blocks::tests::task_ref_parent_omits_block_id_but_reports_its_block ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_rotten_log ... ok
test native::capture::task_blocks::tests::two_parents_forward_across_an_insert_above ... ok
test native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two ... ok
test native::capture::tests::album_index::album_create_reads_only_its_slice_and_stages_one_edit ... ok
test native::capture::tests::album_index::album_batch_reuses_one_folder_scan_for_two_creates ... ok
test native::capture::tests::album_index::album_create_then_update_renders_final_fields ... ok
test native::capture::tests::album_index::album_edit_after_planning_refuses_and_writes_nothing ... ok
test native::capture::tests::assembly::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::assembly::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembly::completed_multiword_reuse_keeps_spelling ... ok
test native::capture::tests::album_index::ordinary_task_draft_loads_no_record_index ... ok
test native::capture::tests::assembly::exact_name_literal_creates_exact_spelling ... ok
test native::capture::tests::assembly::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::tests::assembly::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::assembly::formats_task_line ... ok
test native::capture::tests::assembly::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::assembly::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::tests::assembly::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::assembly::exact_name_literal_never_prefix_matches ... ok
test native::capture::tests::assembly::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::assembly::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::assembly::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::assembly::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::album_index::damaged_folder_refuses_batch_and_writes_nothing ... ok
test native::capture::tests::album_index::records_config_alone_resolves_no_record_route ... ok
test native::capture::tests::assembly::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::assembly::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::assembly::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::assembly::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::tests::assembly::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::assembly::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::assembly::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::assembly::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::assembly::sub_bullet_insertion_keeps_dependency_lines_first ... ok
test native::capture::tests::album_index::failing_second_item_writes_nothing ... ok
test native::capture::tests::assembly::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::commit::complete_label_batch_stale_preimage_keeps_external_edit ... ok
test native::capture::tests::commit::existing_record_update_race_preserves_foreign_bytes_and_rolls_back ... ok
test native::capture::tests::commit::hard_link_unsupported_classifies_fallback_kinds ... ok
test native::capture::tests::commit::keep_moving_pick_batch_stale_preimage_refuses_whole_batch ... ok
test native::capture::tests::album_index::walk_neighbour_edit_after_planning_refuses_and_writes_nothing ... ok
test native::capture::tests::album_index::net_zero_final_index_reports_nothing_but_keeps_its_guard ... ok
test native::capture::tests::album_index::missing_index_reports_original_preimage_and_state ... ok
test native::capture::tests::album_index::unreadable_member_refuses_while_malformed_member_allows_write ... ok
test native::capture::tests::commit::new_note_creates_missing_parent_directory ... ok
test native::capture::tests::commit::existing_note_edits_still_rename_when_hard_link_fallback_is_forced ... ok
test native::capture::tests::commit::cumulative_stages_into_one_note_commit ... ok
test native::capture::tests::commit::new_note_install_commits_missing_target ... ok
test native::capture::tests::commit::new_note_install_race_in_missing_parent_preserves_foreign_bytes ... ok
test native::capture::tests::commit::new_note_install_falls_back_when_hard_links_are_unsupported ... ok
test native::capture::tests::commit::move_destination_is_rolled_back_when_source_replace_fails ... ok
test native::capture::tests::commit::commits_matching_multi_file_preimage ... ok
test native::capture::tests::commit::refuses_when_existing_target_deleted_before_commit ... ok
test native::capture::tests::commit::refuses_when_absent_target_appears_before_commit ... ok
test native::capture::project_note::tests::offer_subset_keys_and_mint_collisions ... ok
test native::capture::tests::commit::refuses_when_second_note_edited_externally ... ok
test native::capture::tests::commit::new_note_fallback_refuses_when_file_lands_between_check_and_install ... ok
test native::capture::tests::album_index::album_replace_failure_rolls_back_the_staged_record ... ok
test native::capture::tests::grammar::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::tests::grammar::clip_directives_claim_edges_and_leave_prose_alone ... ok
test native::capture::tests::grammar::clipboard_notes_parse_as_sub_bullet_without_text ... ok
test native::capture::tests::grammar::extracts_escaped_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::grammar::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::grammar::extracts_retired_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::grammar::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::commit::record_update_then_create_plant_rolls_back_earlier_write ... ok
test native::capture::tests::commit::new_note_install_refuses_when_file_lands_between_check_and_install ... ok
test native::capture::tests::grammar::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::grammar::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::grammar::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::grammar::normalizes_whitespace ... ok
test native::capture::tests::grammar::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::grammar::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::grammar::parses_picker_task_refs_strictly ... ok
test native::capture::tests::grammar::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::grammar::parses_priority_tokens ... ok
test native::capture::tests::grammar::parses_retired_priority_tokens ... ok
test native::capture::tests::grammar::parses_schedule_tokens ... ok
test native::capture::tests::commit::complete_label_batch_failure_after_replace_rolls_back ... ok
test native::capture::tests::grammar::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::grammar::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::grammar::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::grammar::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::grammar::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::grammar::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::placement::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::grammar::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::tests::placement::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::placement::article_exact_raw_title_match_precedes_earlier_identity_match ... ok
test native::capture::tests::placement::article_prefix_prefers_raw_number_in_document_order ... ok
test native::capture::tests::placement::article_slug_matches_after_raw_and_identity ... ok
test native::capture::tests::placement::article_exact_section_matches_plain_identity ... ok
test native::capture::tests::placement::article_exact_section_matches_stale_number ... ok
test native::capture::tests::placement::article_exact_section_matches_de_numbered_identity ... ok
test native::capture::tests::placement::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::placement::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::placement::article_prefix_matches_de_numbered_identity ... ok
test native::capture::tests::placement::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::placement::bare_bullet_marker_skips_generated_status_group ... ok
test native::capture::tests::placement::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::placement::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::placement::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::placement::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::placement::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::placement::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::placement::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::tests::placement::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::placement::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::placement::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::placement::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::placement::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::placement::exact_selector_never_slug_matches ... ok
test native::capture::tests::placement::explicit_areas_selector_refuses_instead_of_falling_through ... ok
test native::capture::tests::placement::explicit_projects_selector_refuses_instead_of_falling_through ... ok
test native::capture::tests::placement::explicit_notebooks_selector_refuses_instead_of_falling_through ... ok
test native::capture::tests::placement::forced_section_does_not_target_generated_blocked_group ... ok
test native::capture::tests::placement::explicit_albums_selector_refuses_instead_of_falling_through ... ok
test native::capture::tests::placement::formats_bullet_line ... ok
test native::capture::tests::placement::edge_hash_markers_are_task_types_not_legacy_bullet_selectors ... ok
test native::capture::tests::placement::formats_scheduled_date_from_offset ... ok
test native::capture::tests::placement::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::placement::forced_route_accepts_terminal_type_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::placement::formats_sub_bullet_line ... ok
test native::capture::tests::placement::generated_albums_section_is_never_a_bullet_target ... ok
test native::capture::tests::placement::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::placement::generated_group_prefix_without_authored_match_falls_back ... ok
test native::capture::tests::placement::generated_notebooks_section_is_never_a_bullet_target ... ok
test native::capture::tests::commit::transfer_merge_same_note_stages_one_file ... ok
test native::capture::tests::placement::generated_areas_section_is_never_completed_or_a_bullet_target ... ok
test native::capture::tests::placement::heading_matches_bullet_selector_is_raw_or_identity ... ok
test native::capture::tests::placement::generated_albums_section_is_never_completed ... ok
test native::capture::tests::placement::generated_notebooks_section_is_never_completed ... ok
test native::capture::tests::placement::generated_projects_section_is_never_completed_or_a_bullet_target ... ok
test native::capture::tests::placement::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::placement::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::placement::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::placement::inserts_after_single_top_level_task ... ok
test native::capture::tests::placement::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::placement::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::placement::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::placement::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::placement::prefix_skips_generated_blocked_group_for_authored_match ... ok
test native::capture::tests::placement::non_article_numbered_heading_keeps_raw_title_matching ... ok
test native::capture::tests::placement::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::placement::raw_prefix_beats_an_earlier_slug_match ... ok
test native::capture::tests::placement::json_success_shape_is_stable ... ok
test native::capture::tests::placement::section_completion_slug_query_matches_spaced_title ... ok
test native::capture::tests::placement::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::placement::section_completion_prefers_raw_then_slug_then_quoted ... ok
test native::capture::tests::placement::slug_selector_falls_back_to_h1_when_no_non_h1_matches ... ok
test native::capture::tests::placement::slug_selector_reaches_spaced_heading ... ok
test native::capture::tests::placement::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::placement::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::placement::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::placement::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::tests::placement::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::placement::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::whole_slug_beats_an_earlier_slug_prefix ... ok
test native::capture::tests::placement::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::started::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::started::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::started::non_tasks_section_headings_skip_generated_status_groups ... ok
test native::capture::tests::placement::section_completion_omits_selectors_that_cannot_round_trip ... ok
test native::capture::tests::started::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::started::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started::started_pomodoro_move_preserves_crlf ... ok
test native::capture::tests::started::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::started::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::tests::started::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::started::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture::tests::type_marker::capture_parse_recognizes_hash_type_marker ... ok
test native::capture::tests::placement::parses_suffixed_route_token_as_bullet ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture_active_tasks::tests::excludes_ready_tasks_even_with_now_text ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_block_ids::tests::block_id_calibration ... ignored, set BOB_ID_CALIBRATION_VAULT to a vault of Markdown notes
test native::capture_block_ids::tests::allowed_regex_agrees_with_validator_for_every_ascii_char ... ok
test native::capture_block_ids::tests::first_suggestion_prefers_three_words_within_twenty_bytes ... ok
test native::capture_block_ids::tests::successor_mints_follow_the_pinned_vectors ... ok
test native::capture_block_ids::tests::suggestions_drop_filler_leadins_and_keep_content_verbs ... ok
test native::capture_block_ids::tests::suggestions_offer_code_span_phrase_and_honor_length_cap ... ok
test native::capture_block_ids::tests::suggestions_follow_the_pinned_examples ... ok
test native::capture_block_ids::tests::used_covers_done_nontask_duplicates_and_document_order ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_clip::history::tests::blank_env_falls_through_to_config ... ok
test native::capture_clip::history::tests::explicit_providers_are_mac_only ... ok
test native::capture_clip::history::tests::non_macos_auto_keeps_the_actionable_guidance ... ok
test native::capture_clip::history::tests::env_command_beats_everything ... ok
test native::capture_clip::history::tests::off_refuses_and_command_needs_argv ... ok
test native::capture_clip::model::tests::clipboard_history_ages_are_clamped_and_unknowns_stay_null ... ok
test native::capture_clip::history::tests::auto_prefers_alfred_then_clipy_and_skips_missing_stores ... ok
test native::capture::tests::template::sa36_hello_and_plain_x_add_no_relation_snapshot_reads ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_clip::persist::tests::create_new_fallback_copies_from_the_temporary_file ... ok
test native::capture_clip::tests::agreeing_history_must_be_complete_and_text ... ok
test native::capture_clip::persist::tests::source_change_after_planning_aborts_without_installing_files ... ok
test native::capture_clip::persist::tests::attachment_install_refuses_a_destination_planted_after_planning ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_clip::tests::auto_skips_a_permanent_provider_failure ... ok
test native::capture_clip::tests::attachment_plans_keep_only_a_path_and_dry_run_creates_nothing ... ok
test native::capture_clip::tests::busy_provider_is_retried_until_it_agrees ... ok
test native::capture_clip::tests::auto_uses_the_first_provider_that_agrees ... ok
test native::capture_clip::tests::clipboard_history_agrees_on_the_first_poll ... ok
test native::capture_clip::tests::clipboard_history_waits_for_a_lagging_provider_to_agree ... ok
test native::capture_clip::tests::classifies_angle_wrapped_paths_and_file_uris ... ok
test native::capture::tests::commit::transfer_merge_preserves_engine_order_and_rolls_back_failed_source ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_clip::tests::concealed_live_clip_refuses_with_the_likely_cause_hint ... ok
test native::capture_clip::tests::counted_history_carries_a_video_entry ... ok
test native::capture_clip::tests::deduped_secondary_source_is_validated_before_any_copy ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_clip::tests::fanout_plan_validates_a_deduped_source_from_a_later_item ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::attachment_size_limits_refuse_before_hashing_and_warn_below_limit ... ok
test native::capture_clip::tests::history_does_not_inspect_entries_beyond_the_requested_count ... ok
test native::capture::offer_verdicts::disk_guard_tests::concurrent_verdict_target_edit_aborts_the_whole_batch ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reuses_duplicate_snippets ... ok
test native::capture::tests::commit::move_choice_capture_rolls_back_every_file_when_source_replace_fails ... ok
test native::capture_clip::tests::ignored_guard_skips_non_git_vaults_and_missing_git ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::mixed_image_video_and_file_clipboard_keeps_all_kinds_in_order ... ok
test native::capture_clip::tests::gitignored_attachments_refuse_and_reincluded_paths_pass ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture_clip::tests::reused_attachment_source_is_still_validated_after_planning ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::capture_clip::tests::slow_agreeing_provider_is_trusted_past_the_deadline ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture::tests::commit::transfer_merge_rerun_has_no_staged_writes ... ok
test native::capture_clip::tests::source_change_after_planning_aborts_and_leaves_no_attachment ... ok
test native::capture_clip::tests::stale_clipboard_history_refuses_after_the_shared_deadline ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_clip::tests::video_catalog_covers_expected_extensions_only ... ok
test native::capture_clip::tests::video_paths_accept_wrappers_cases_and_unicode_names ... ok
test native::capture_completable_tasks::tests::bang_replacement_quotes_reserved_locators ... ok
test native::capture_clip::tests::video_clipboard_paths_embed_from_vid_at_400px ... ok
test native::capture_completable_tasks::tests::draft_selected_marks_only_other_items ... ok
test native::capture_completable_tasks::tests::guard_reasons_match_the_contract ... ok
test native::capture_completable_tasks::tests::empty_query_orders_today_first_then_status ... ok
test native::capture_completable_tasks::tests::hidden_and_recurring_sink_within_their_section ... ok
test native::capture_completable_tasks::tests::missing_day_file_means_no_today_rows ... ok
test native::capture::tests::commit::transfer_merge_guards_unchanged_reads_membership_and_missing_day ... ok
test native::capture_completable_tasks::tests::recurring_today_rows_sink_below_visible_rows_in_the_same_entry ... ok
test native::capture_completable_tasks::tests::open_tasks_list_with_locators_scheduled_and_suggestions ... ok
test native::capture_clip::tests::vid_copies_reuse_identical_files_and_suffix_clashes ... ok
test native::capture_completable_tasks::tests::nonempty_query_keeps_today_matches_on_top ... ok
test native::capture_complete::candidates::closed_goto_tests::dated_rows_come_before_undated_newest_first ... ok
test native::capture_complete::candidates::closed_goto_tests::ties_break_by_note_path_then_line ... ok
test native::capture::note_pull::tests::batch_pull_then_project_move_no_pick_keeps_offer ... ok
test native::capture_complete::drawers::tests::age_phrase_buckets_follow_whole_days ... ok
test native::capture_complete::drawers::tests::ellipsize_keeps_short_text_and_trims_long_text ... ok
test native::capture_complete::drawers::tests::plural_copy_is_singular_only_for_one ... ok
test native::capture_complete::drawers::tests::quote_escape_protects_quotes_and_backslashes ... ok
test native::capture_completable_tasks::tests::struck_fenced_and_depends_on_links_never_place ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_completable_tasks::tests::today_roles_precedence_sessions_and_pomodoro ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_excludes_ready_tasks ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture_complete::tests::active_tasks::active_task_human_rows_name_the_queue ... ok
test native::capture_complete::tests::blocked_tasks::blocked_task_shell_rows_use_the_blocked_tasks_group ... ok
test native::capture_complete::tests::directives::bare_percent_opens_ordered_directive_menu_with_no_initial_selection ... ok
test native::capture_complete::tests::directives::directive_query_filters_by_letter_and_never_reads_clipboard ... ok
test native::capture::note_pull::tests::np16_inbox_ready_pick_routes_next_pick_does_not ... ok
test native::capture_complete::tests::directives::listen_row_activates_when_configured ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_describes_the_selected_session ... ok
test native::capture_complete::tests::directives::directive_containing_menu_does_not_preselect_a_row ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_names_a_trailing_range_as_running ... ok
test native::capture_complete::tests::directives::pomodoro_note_row_disables_when_two_open_timed_entries_mix_formats ... ok
test native::capture_complete::tests::directives::shell_completion_exposes_safe_directive_rows_under_directives_group ... ok
test native::capture::note_pull::tests::np14_numeric_key_and_out_of_range_picks ... ok
test native::capture_complete::tests::directives::url_directive_menu_offers_listen_with_config_status ... ok
test native::capture_clip::tests::clipy_reports_binary_only_rows_as_not_text ... ok
test native::capture_complete::tests::drawers::a_task_without_drawers_lists_recent_and_new_only ... ok
test native::capture_complete::tests::drawers::bullet_menu_filters_by_the_typed_name_and_decodes_a_quoted_literal ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_new_project_note_creates_title_case_sections ... ok
test native::capture::tests::commit::merge_in_new_target_rolls_back_real_staged_files_on_source_replace_failure ... ok
test native::capture_complete::tests::directives::bare_hash_type_menu_also_has_no_initial_selection ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_prj_task_lists_sections_and_refuses_structural_ones ... ok
test native::capture_complete::tests::directives::notebook_creation_directive_enables_without_pomodoro ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_an_existing_task_offers_bare_titles_with_the_glued_copy ... ok
test native::capture_complete::tests::drawers::bullet_menu_on_a_new_task_offers_recent_and_new_rows_only ... ok
test native::capture_clip::tests::clipy_decodes_one_canonical_flavor_per_entry ... ok
test native::capture_complete::tests::drawers::new_row_hints_at_a_near_catalog_key ... ok
test native::capture_complete::tests::drawers::empty_query_lists_task_then_recent_rows_and_opens_unselected ... ok
test native::capture_complete::tests::drawers::bullet_new_row_spells_a_typed_slug_as_the_title_the_shortcut_creates ... ok
test native::capture_complete::tests::drawers::bullet_starts_that_cannot_name_a_drawer_are_empty_successes ... ok
test native::capture_complete::tests::drawers::empty_query_recent_is_capped_at_eight_keys ... ok
test native::capture_clip::tests::reads_alfred_history_newest_first_with_cocoa_epoch ... ok
test native::capture_complete::tests::drawers::bullet_rows_refuse_with_the_exact_resolvers_reason ... ok
test native::capture_complete::tests::drawers::recent_rows_are_catalog_keys_the_task_lacks ... ok
test native::capture_complete::tests::drawers::nested_bullet_hash_still_offers_task_types ... ok
test native::capture_complete::tests::drawers::shell_completion_never_reaches_a_bullet_start ... ok
test native::capture_complete::tests::drawers::shell_drawer_rows_are_the_targets_own_unrefused_drawers ... ok
test native::capture_complete::tests::drawers::project_note_prj_target_lists_sections_and_creates_title_case_sections ... ok
test native::capture_complete::tests::drawers::punctuated_drawer_lists_under_task_with_exact_slug_reach ... ok
test native::capture_complete::tests::drawers::replacement_covers_the_hash_and_the_name_and_reports_cursor_after ... ok
test native::capture_complete::tests::drawers::bullet_replacement_continues_with_a_nested_bullet_only_when_nothing_follows ... ok
test native::capture_complete::tests::drawers::new_row_needs_a_typed_name_no_other_row_claims ... ok
test native::capture_complete::tests::merge_in::transfer_source_picker_keeps_idless_rows_for_add_block_id ... ok
test native::capture_complete::tests::drawers::refused_rows_carry_the_commit_resolvers_reason ... ok
test native::capture_complete::tests::output::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::drawers::task_rows_carry_counts_singular_plural_detail_and_consequences ... ok
test native::capture_complete::tests::drawers::replacement_is_a_slug_only_when_it_resolves_back_to_the_same_drawer ... ok
test native::capture_complete::tests::output::empty_json_context_is_null ... ok
test native::capture_complete::tests::merge_in::merge_in_excludes_typed_sources_through_project_aliases ... ok
test native::capture_complete::tests::output::json_shape_is_stable ... ok
test native::capture_complete::tests::drawers::typed_query_drops_the_unselected_open_and_filters_every_group ... ok
test native::capture_complete::tests::output::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture_complete::tests::output::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::drawers::rows_rank_prefix_before_substring_in_document_order ... ok
test native::capture_complete::tests::merge_in::merge_in_note_and_vault_pickers_keep_only_mergeable_rows ... ok
test native::capture_complete::tests::output::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::output::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_complete::tests::output::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_complete::tests::output::close_items_and_suffixes_request_no_completion ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_complete::tests::drawers::unresolvable_targets_report_a_diagnostic_and_no_rows ... ok
test native::capture_complete::tests::parent_tasks::bare_plus_serves_vault_candidates_and_operator_hints ... ok
test native::capture_complete::tests::parent_tasks::leading_plus_query_refetch_keeps_token_range_and_full_catalog ... ok
test native::capture_complete::tests::parent_tasks::scoped_missing_and_empty_notes_keep_picker_and_empty_catalog ... ok
test native::capture_complete::tests::parent_tasks::vault_catalog_excludes_non_capture_and_terminal_notes ... ok
test native::capture_complete::tests::parent_tasks::plus_query_ranks_candidates_and_scoped_descriptors_keep_exact_ranges ... ok
test native::capture_complete::tests::parent_tasks::unicode_duplicates_and_queued_pomodoros_stay_in_catalog ... ok
test native::capture_complete::tests::pomodoros::bare_start_name_replacements_prefix_hash_when_the_slug_cannot_be_bare ... ok
test native::capture_complete::tests::pomodoros::bare_start_name_replacements_fold_trailing_glued_timing ... ok
test native::capture_complete::tests::pomodoros::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_candidates_omit_next_up ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_today_before_creation_and_utilities ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_suppresses_creation_only_for_exact_open_names ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::parent_tasks::parent_task_continuation_is_advertised_only_when_comma_extends_the_row ... ok
test native::capture_complete::tests::pomodoros::pomodoro_past_name_fields_preserve_suffixes_and_chain_siblings ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_filters_and_creates_by_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_human_labels_cover_every_row_kind ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_lists_start_again_and_name_it_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_matches_pomodoro_name_warnings ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_orders_repeated_completed_names_newest_first ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_puts_the_running_entry_last ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_rows_carry_no_budget_preview ... ok
test native::capture_clip::tests::rejects_missing_locked_and_mismatched_alfred_databases ... ok
test native::capture_complete::tests::records::broken_album_stays_diagnosed_and_does_not_hide_a_healthy_route ... ok
test native::capture_complete::tests::records::album_route_and_field_completion_follow_the_explicit_vault ... ok
test native::capture_complete::tests::records::crlf_next_missing_inserts_crlf_bullets ... ok
test native::capture_complete::tests::output::bare_edge_hash_requests_task_type_completion ... ok
test native::capture_complete::tests::output::bare_start_name_completion_prefixes_hash_for_digit_led_matches ... ok
test native::capture_complete::tests::records::caret_and_next_missing_advertise_assist_version_without_edit ... ok
test native::capture_complete::tests::records::date_menu_offers_today_then_yesterday ... ok
test native::capture_complete::tests::records::empty_section_query_prepends_record_create_and_expands_the_token ... ok
test native::capture_complete::tests::records::empty_url_value_has_one_candidate_and_no_continuation ... ok
test native::capture_complete::tests::records::field_menu_after_a_field_excludes_the_typed_key ... ok
test native::capture_complete::tests::records::empty_remaining_keys_leave_note_bullets_alone ... ok
test native::capture_complete::tests::records::field_menu_lists_required_keys_first_on_a_fresh_dash ... ok
test native::capture_complete::tests::records::global_destination_section_menu_has_no_create_row ... ok
test native::capture_complete::tests::records::list_member_completion_replaces_only_the_member_at_the_caret ... ok
test native::capture_complete::tests::records::named_field_does_not_fall_into_task_completion ... ok
test native::capture_complete::tests::records::human_output_names_record_field_and_value_rows ... ok
test native::capture_complete::tests::records::named_field_crlf_inserts_crlf_bullets ... ok
test native::capture_complete::tests::records::named_field_empty_suggested_text_folder_still_has_edit ... ok
test native::capture_complete::tests::output::trailing_hash_fragment_requests_task_type_completion ... ok
test native::capture_complete::tests::records::named_field_edit_materializes_the_default_spelling ... ok
test native::capture_complete::tests::output::close_bullet_lines_suppress_wikilink_block_but_keep_note ... ok
test native::capture_complete::tests::records::named_field_on_a_non_record_is_empty_success ... ok
test native::capture_complete::tests::records::named_field_ignores_legacy_records_config ... ok
test native::capture_complete::tests::records::named_field_edit_authors_an_empty_optional_bullet ... ok
test native::capture_complete::tests::records::mixed_draft_scopes_route_errors_to_the_cursor_item ... ok
test native::capture_complete::tests::records::named_field_missing_title_still_addresses_the_field ... ok
test native::capture_complete::tests::records::named_field_opens_an_unfiltered_value_menu_without_a_bullet ... ok
test native::capture_complete::tests::records::named_field_unicode_prefix_keeps_byte_offsets ... ok
test native::capture_complete::tests::records::named_field_preserves_an_explicit_empty ... ok
test native::capture_complete::tests::records::named_field_on_an_invalid_value_is_unfiltered ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_complete::tests::records::named_field_list_uses_caret_member_else_the_final_member ... ok
test native::capture_complete::tests::records::named_field_unknown_is_read_only ... ok
test native::capture_complete::tests::records::ordinary_draft_does_not_open_the_record_catalog ... ok
test native::capture_complete::tests::records::near_value_hint_warns_without_rewriting_cheeseteaks ... ok
test native::capture_complete::tests::records::named_field_targets_the_record_item_containing_the_cursor ... ok
test native::capture_complete::tests::records::opaque_field_values_do_not_open_the_type_picker ... ok
test native::capture_complete::tests::records::record_target_menu_skips_spaced_stems ... ok
test native::capture_complete::tests::records::template_argument_rows_are_not_record_items ... ok
test native::capture_complete::tests::records::route_menu_offers_eat_with_new_label_and_continuation ... ok
test native::capture_complete::tests::records::next_missing_walks_status_then_category_then_location ... ok
test native::capture_complete::tests::records::record_target_menu_ranks_matches_and_shows_stored_values ... ok
test native::capture_complete::tests::records::status_value_menu_offers_schema_choices ... ok
test native::capture_complete::tests::records::record_link_values_keep_the_living_stem_on_dedup ... ok
test native::capture_complete::tests::records::shell_record_route_strips_the_trailing_space ... ok
test native::capture_complete::tests::records::typed_section_query_keeps_headings_and_omits_the_create_row ... ok
test native::capture_complete::tests::records::westfield_and_wikilink_alias_collapse_to_the_majority_spelling ... ok
test native::capture_complete::tests::records::update_field_assistance_uses_current_values_without_legacy_prompts ... ok
test native::capture_clip::tests::clipy_skips_concealed_and_transient_rows_without_counting_them ... ok
test native::capture_complete::tests::output::override_running_carries_homes_only_for_unnamed_sessions ... ok
test native::capture_complete::tests::relations::cancel_from_direction_resolves_the_token_source ... ok
test native::capture_complete::tests::relations::cancel_inverse_query_teaches_the_flip ... ok
test native::capture_complete::tests::relations::cancel_closed_source_links_only_without_disabling ... ok
test native::capture_complete::tests::relations::cancel_hidden_overlay_stays_out_but_typed_match_shows_state ... ok
test native::capture_complete::tests::relations::cancel_overlay_marks_rows_and_reports_cancels_for_to_owner ... ok
test native::capture_complete::tests::records::trailing_sigils_inside_record_values_stay_record_values ... ok
test native::capture_complete::tests::relations::cancel_new_owner_is_refused_with_relabel_hint ... ok
test native::capture_complete::tests::relations::parent_picker_reports_typed_relation_direction_and_target_text ... ok
test native::capture_complete::tests::relations::complete_and_cancel_cues_coexist_when_both_policies_are_configured ... ok
test native::capture_complete::tests::relations::cancel_project_source_keeps_residents_open ... ok
test native::capture_complete::tests::relations::complete_project_and_closed_sources_only_report_link_effects ... ok
test native::capture_complete::tests::relations::cancel_recurring_source_disables_cancel_rows ... ok
test native::capture_complete::tests::relations::relation_shell_groups_are_directional_and_skip_guarded_rows ... ok
test native::capture_complete::tests::relations::relation_pools_follow_directional_tiers_and_editability ... ok
test native::capture_complete::tests::relations::complete_from_direction_hints_inverses_and_disables_refused_rows ... ok
test native::capture_complete::tests::routes_tasks::double_at_offers_only_destinations_never_a_template_candidate ... ok
test native::capture_complete::tests::relations::relation_target_replacement_stops_before_an_existing_label ... ok
test native::capture_complete::tests::routes_tasks::notebook_create_row_keeps_typed_capitals ... ok
test native::capture_complete::tests::routes_tasks::notebook_block_ids_mark_notebook_kind_and_avoid_all_ids ... ok
test native::capture_complete::tests::routes_tasks::notebook_duplicate_headings_are_refused_rows ... ok
test native::capture_complete::tests::routes_tasks::notebook_note_duplicate_ids_are_disabled ... ok
test native::capture_complete::tests::pomodoros::pomodoro_past_name_menu_excludes_running_targets_without_override ... ok
test native::capture_complete::tests::routes_tasks::notebook_section_completion_keeps_block_id_suffix_range ... ok
test native::capture_complete::tests::routes_tasks::notebook_note_bullets_offer_idd_first_then_idless ... ok
test native::capture_complete::tests::relations::relation_target_contexts_use_directional_markers_and_owner_links ... ok
test native::capture_complete::tests::routes_tasks::notebook_sections_list_h2_only_in_document_order ... ok
test native::capture_complete::tests::routes_tasks::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::routes_tasks::route_completion_offers_notebook_rows_after_projects_with_breadcrumb ... ok
test native::capture_complete::tests::routes_tasks::route_completion_matches_aliases_with_canonical_replacement_after_prefix ... ok
test native::capture_complete::tests::routes_tasks::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::routes_tasks::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_complete::tests::routes_tasks::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_list_header_with_bullets ... ok
test native::capture_complete::tests::routes_tasks::notebook_section_create_row_for_unrelated_slug_and_near_miss ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_complete::tests::routes_tasks::section_completion_partial_quoted_query_covers_the_literal ... ok
test native::capture_complete::tests::routes_tasks::shell_completion_preserves_quoted_section_replacement ... ok
test native::capture_complete::tests::routes_tasks::section_completion_round_trips_slug_and_quoted_replacements ... ok
test native::capture_complete::tests::routes_tasks::section_completion_quote_leading_titles_use_exact_fallback ... ok
test native::capture_complete::tests::routes_tasks::template_completion_still_completes_markers_in_the_definition ... ok
test native::capture_complete::tests::routes_tasks::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_complete::tests::relations::relation_label_leading_and_dependency_tail_keep_narrow_ranges ... ok
test native::capture_complete::tests::task_links::task_link_completion_keeps_candidates_when_the_day_file_is_missing ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::capture_complete::tests::task_links::task_link_completion_lists_worked_example_in_canonical_order ... ok
test native::capture_complete::tests::routes_tasks::template_rows_and_placeholders_do_not_open_route_completion ... ok
test native::capture_complete::tests::task_links::task_link_completion_pins_json_shape_and_omissions ... ok
test native::capture_complete::tests::task_links::task_link_human_rows_name_queues_and_missing_ids ... ok
test native::capture_dependency_tasks::tests::closed_on_prefers_completion_for_done_and_cancelled_otherwise ... ok
test native::capture_complete::tests::relations::complete_overlay_marks_rows_and_reports_source_consequence ... ok
test native::capture_complete::tests::task_links::task_link_completion_queries_cover_the_sigil_and_rank ... ok
test native::capture_complete::tests::task_links::task_link_completion_scopes_to_the_batch_second_item ... ok
test native::capture_dependency_tasks::tests::catalog_covers_every_task_bearing_note_kind ... ok
test native::capture_dependency_tasks::tests::hidden_tasks_detect_only_the_exact_tag ... ok
test native::capture_dependency_tasks::tests::quoted_locator_round_trips_through_replacement ... ok
test native::capture_drawers::tests::build_cli_renders_without_panicking ... ok
test native::capture_dependency_tasks::tests::interleaved_names_walk_in_sorted_order ... ok
test native::capture_drawers::tests::catalog_search_ranks_prefix_tier_first_and_skips_excluded_keys ... ok
test native::capture_drawers::tests::checkboxed_all_caps_children_are_not_drawers ... ok
test native::capture_drawers::tests::empty_drawer_bullet_still_qualifies ... ok
test native::capture_dependency_tasks::tests::unique_basename_resolves_before_ambiguous_paths ... ok
test native::capture_drawers::tests::ensure_drawer_creates_task_drawer_then_rescans_it ... ok
test native::capture_drawers::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_drawers::tests::ensure_drawer_creates_project_h2_sibling_and_rescans_it ... ok
test native::capture_drawers::tests::grandchild_is_not_a_direct_child_drawer ... ok
test native::capture_drawers::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_drawers::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_drawers::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_dependency_tasks::tests::groups_follow_the_picker_sections ... ok
test native::capture_drawers::tests::last_entry_text_is_the_direct_entry_a_capture_lands_after ... ok
test native::capture_dependency_tasks::tests::ranking_shares_the_tiered_matcher_vectors ... ok
test native::capture_drawers::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_drawers::tests::near_duplicate_suggests_quoted_title_when_slug_is_invalid ... ok
test native::capture_drawers::tests::query_matches_a_key_or_slug_by_prefix_before_substring ... ok
test native::capture_drawers::tests::reserved_refusals_name_the_reserved_key ... ok
test native::capture_drawers::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_drawers::tests::managed_logs_are_never_drawers_plain_titles_are ... ok
test native::capture_dependency_tasks::tests::empty_query_orders_same_note_lanes_history ... ok
test native::capture_drawers::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_drawers::tests::sentence_punctuation_drawer_titles_qualify ... ok
test native::capture_drawers::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_drawers::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_drawers::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_drawers::tests::title_whitelist_edges ... ok
test native::capture_drawers::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_flag_guard::tests::command_specific_known_shorts_are_kept_and_unknown_shorts_refused ... ok
test native::capture_flag_guard::tests::equals_only_short_combined_with_declared_option_then_unknown_is_rejected ... ok
test native::capture_flag_guard::tests::declared_flags_values_and_text_pass_through ... ok
test native::capture_complete::tests::relations::relation_label_double_pipe_keeps_pipes_and_reports_one_off ... ok
test native::capture_flag_guard::tests::guard_specs_match_clap_declarations ... ok
test native::capture_flag_guard::tests::mixed_short_cluster_then_unknown_long_is_rejected ... ok
test native::capture_flag_guard::tests::short_format_json_with_unknown_flag_reports_json ... ok
test native::capture_flag_guard::tests::text_starting_with_a_flag_word_needs_the_delimiter ... ok
test native::capture_flag_guard::tests::unknown_first_short_in_cluster_is_rejected_before_later_known_short ... ok
test native::capture_flag_guard::tests::unknown_long_flag_before_text_is_rejected ... ok
test native::capture_flag_guard::tests::unknown_short_flag_before_text_is_rejected ... ok
test native::capture_flag_guard::tests::unknown_short_in_mixed_known_cluster_is_rejected ... ok
test native::capture_complete::tests::relations::relation_label_completions_carry_relation_and_owner ... ok
test native::capture_flag_guard::tests::value_taking_short_with_attached_cluster_rest_is_the_value ... ok
test native::capture_language::bare_name::tests::bare_name_len_matches_letter_led_non_close_shapes ... ok
test native::capture_language::bare_name::tests::can_spell_bare_rejects_digit_led_and_close_shapes ... ok
test native::capture_language::bare_name::tests::composed_tokens_keep_hash_when_the_name_cannot_be_bare ... ok
test native::capture_language::close_log::tests::assign_log_positions_follows_the_assignment_rule ... ok
test native::capture_language::close_log::tests::default_log_index_covers_every_close_shape ... ok
test native::capture_language::close_log::tests::first_bullet_kind_detection_skips_placeholders ... ok
test native::capture_language::close_log::tests::inline_entry_defaults_and_leading_numbers ... ok
test native::capture_language::close_log::tests::inline_entry_reports_dangling ... ok
test native::capture_language::close_log::tests::inline_entry_reports_diagnostics_in_order ... ok
test native::capture_language::close_log::tests::lexes_entries_and_details ... ok
test native::capture_language::close_log::tests::log_entries_from_lex_marks_star_origin ... ok
test native::capture_language::close_log::tests::mixed_numbering_fails_both_orders ... ok
test native::capture_language::close_log::tests::not_worked_suggestions_keep_complete_and_drop_lists ... ok
test native::capture_language::close_log::tests::reports_dangling ... ok
test native::capture_language::close_log::tests::positional_entries_carry_their_typed_position ... ok
test native::capture_language::close_log::tests::rejects_bad_bullets ... ok
test native::capture_language::close_log::tests::star_bullets_are_recognized_and_stay_unexpanded ... ok
test native::capture_language::close_log::tests::star_bullets_carry_details_and_dangle ... ok
test native::capture_language::close_log::tests::star_bullets_report_selection_mode_failures ... ok
test native::capture_language::close_log::tests::star_bullets_mix_with_either_list_kind ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_report_lexical_failures ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_for_explicit_lists ... ok
test native::capture_language::close_selection::tests::close_marker_may_follow_accepts_viable_prefixes ... ok
test native::capture_language::close_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_positionally_in_selection_mode ... ok
test native::capture_language::close_selection::tests::lex_reports_park_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_drop_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::close_selection::tests::lex_reports_trailing_at_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_valid_selections ... ok
test native::capture_language::close_selection::tests::retired_whole_item_spellings_name_their_bare_rewrite ... ok
test native::capture_language::close_selection::tests::lex_reports_wildcard_groups ... ok
test native::capture_language::close_selection::tests::selection_shape_detection ... ok
test native::capture_language::dependencies::tests::bare_sigil_is_directive_only_at_the_ends ... ok
test native::capture_language::dependencies::tests::escape_consumes_only_its_backslash ... ok
test native::capture_language::dependencies::tests::blocked_task_modifiers_have_separate_entries_and_spans ... ok
test native::capture_language::dependencies::tests::escaped_star_unescapes_only_inside_a_modifier_run ... ok
test native::capture_language::dependencies::tests::protected_spans_are_never_modifiers ... ok
test native::capture_language::dependencies::tests::mid_line_modifiers_stay_literal ... ok
test native::capture_language::dependencies::tests::quoted_escapes_decode ... ok
test native::capture_language::dependencies::tests::quoted_note_with_spaces_stays_atomic ... ok
test native::capture_language::dependencies::tests::traversal_and_bad_ids_are_invalid ... ok
test native::capture_language::dependencies::tests::trailing_complete_modifier_strips_and_spans ... ok
test native::capture_language::dependencies::tests::unicode_offsets_stay_on_char_boundaries ... ok
test native::capture_language::dependencies::tests::star_markdown_and_mid_line_tokens_stay_literal ... ok
test native::capture_language::dependencies::tests::unterminated_quote_is_one_partial ... ok
test native::capture_language::notebook::tests::candidates_are_deduplicated_and_include_global_routes ... ok
test native::capture_language::notebook::tests::unsupported_suffix_is_a_fail_closed_editor_diagnostic ... ok
test native::capture_language::notebook::tests::editor_spans_use_utf8_byte_offsets_for_trailing_markers ... ok
test native::capture_language::notebook::tests::route_scan_recognizes_the_four_individual_forms ... ok
test native::capture_language::pomodoro_literal::tests::expand_covers_spaced_literals ... ok
test native::capture_language::pomodoro_literal::tests::lex_decodes_only_quote_and_backslash_escapes ... ok
test native::capture_language::pomodoro_literal::tests::lex_rejects_non_quote_openers ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_straight_and_curly_literals ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_unterminated_as_incomplete ... ok
test native::capture_language::project_tasks::tests::lexer_accepts_the_boundary_set ... ok
test native::capture_language::project_tasks::tests::reserved_name_matches_in_any_letter_case ... ok
test native::capture_language::project_tasks::tests::suffix_helpers_split_on_the_last_word ... ok
test native::capture_language::start_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::notebook::tests::classification_keeps_body_details_opaque_and_emits_spans ... ok
test native::capture_language::start_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::start_selection::tests::lex_reports_valid_drop_lists ... ok
test native::capture_language::tests::alias_tip::alias_id_codes_are_unique_snake_case_wire_spellings ... ok
test native::capture_language::notebook::tests::strict_parser_claims_individual_notebook_note_forms ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_keeps_only_the_keys_the_forward_rewrite_accepts ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_only_looks_at_the_sigil_ending_at_the_cursor ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_reports_utf8_byte_offsets ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_stays_silent_for_an_album_hash ... ok
test native::capture_complete::tests::relations::successor_labels_offer_and_explain_inverse_and_released_targets ... ok
test native::capture_language::tests::alias_tip::the_tipped_classification_matches_the_v1_lessons ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_uses_the_forward_pipeline_for_a_spaced_next_parent ... ok
test native::capture_language::tests::bare_close::bare_close_classifier_claims_only_the_documented_shapes ... ok
test native::capture_complete::tests::output::named_start_completion_omits_context_without_a_single_runner ... ok
test native::capture_language::tests::bare_close::bare_close_spans_cover_the_one_byte_x_and_each_list ... ok
test native::capture_language::tests::bare_close::bare_close_suppresses_marker_completion_in_work_log_text ... ok
test native::capture_language::tests::bare_close::past_bare_token_is_not_a_close ... ok
test native::capture_language::tests::bare_close::bare_close_heads_session_chains_and_inline_trails ... ok
test native::capture_language::tests::chain::bang_claim_beats_dependency_errors ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_proves_each_positive_row ... ok
test native::capture_language::tests::chain::chain_token_predicate_covers_the_documented_table ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_agrees_with_the_forward_rewrite_for_every_prefix ... ok
test native::capture_language::tests::bare_close::bare_close_selection_shapes_report_the_same_close_everywhere ... ok
test native::capture_language::tests::chain::draft_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::bang_items_claim_each_blank_line_block_independently ... ok
test native::capture_language::tests::chain::draft_chain_works_with_a_global_declaration ... ok
test native::capture_language::tests::chain::completion_requests_nothing_anywhere_on_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_a_two_token_chain_with_absolute_ranges ... ok
test native::capture_language::tests::chain::draft_keeps_sequential_indices_across_crlf_with_a_chain ... ok
test native::capture_language::tests::bare_close::prose_and_uppercase_x_remain_tasks ... ok
test native::capture_language::tests::chain::chain_token_predicate_equals_claimed_for_single_tokens ... ok
test native::capture_language::tests::chain::draft_splits_tabs_and_runs_of_spaces ... ok
test native::capture_language::tests::alias_tip::sigil_alias_tip_stays_silent_for_the_negative_corpus ... ok
test native::capture_language::tests::chain::editor_reports_a_broken_second_token_with_its_own_diagnostic ... ok
test native::capture_language::tests::chain::editor_chain_items_do_not_inherit_a_global_declaration ... ok
test native::capture_language::tests::chain::editor_reports_a_dangling_close_separator_inside_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_retired_double_tokens_and_reports_their_own_ranges ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_plus_adjustment_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_chain_with_absolute_spans ... ok
test native::capture_language::tests::chain::editor_reports_an_incomplete_named_start_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_selection_spans_at_absolute_offsets_in_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_two_items_with_absolute_spans_for_a_chain ... ok
test native::capture_language::tests::chain::execution_carries_a_close_selection_through_a_chain ... ok
test native::capture_language::tests::chain::execution_distinguishes_spaced_start_adjust_from_offset_start ... ok
test native::capture_language::tests::chain::execution_rejects_forced_destinations_on_the_first_chain_token ... ok
test native::capture_language::tests::chain::execution_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::execution_reports_a_broken_second_token_on_its_own_range ... ok
test native::capture_language::tests::chain::execution_runs_a_chain_left_to_right ... ok
test native::capture_language::tests::chain::execution_switches_sessions_with_close_then_start ... ok
test native::capture_language::tests::chain::execution_leaves_non_chains_unchanged ... ok
test native::capture_language::tests::chain::past_chains_split_and_stack ... ok
test native::capture_language::tests::completion::a_cursor_on_a_type_marker_requests_task_type_completion ... ok
test native::capture_language::tests::completion::bare_at_completes_an_empty_route ... ok
test native::capture_drawers::tests::resolved_task_with_no_drawers_is_a_successful_empty_list ... ok
test native::capture_drawers::tests::lists_drawers_in_document_order_for_a_block_id ... ok
test native::capture_language::tests::completion::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_drawers::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_language::tests::alias_tip::every_alias_id_has_a_stamped_forward_fixture ... ok
test native::capture_language::tests::completion::block_id_project_note_sigil_is_excluded_from_replacement ... ok
test native::capture_language::tests::completion::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion::completion_on_global_declarations_only_completes_the_route ... ok
test native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_language::tests::completion::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion::caret_suffix_names_preserve_the_link_part_for_completion ... ok
test native::capture_language::tests::completion::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::drawer_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::completion::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::completion::empty_block_id_with_section_still_yields_a_drawer_field ... ok
test native::capture_language::tests::completion::empty_selector_after_hash_is_a_one_byte_drawer_field ... ok
test native::capture_language::tests::completion::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::hash_completion_is_lexical_even_when_the_subject_will_refuse_it ... ok
test native::capture_language::tests::completion::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::completion::free_standing_hash_fragments_request_task_type_completion ... ok
test native::capture_language::tests::completion::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::completion::hash_ends_the_block_id_and_opens_the_drawer_replacement ... ok
test native::capture_language::tests::completion::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::completion::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::completion::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::completion::hash_after_a_bare_block_id_marker_completes_a_task_type ... ok
test native::capture_language::tests::completion::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::completion::list_header_completes_partial_quoted_section_after_bullets ... ok
test native::capture_language::tests::completion::list_header_completes_route_after_bullets ... ok
test native::capture_language::tests::completion::list_header_completes_section_after_bullets ... ok
test native::capture_language::tests::completion::list_header_completes_with_crlf_and_utf8_before_it ... ok
test native::capture_language::tests::completion::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion::merge_in_arrow_and_gaps_do_not_fall_through_to_target_runs ... ok
test native::capture_language::tests::completion::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::merge_in_source_slots_reuse_route_task_and_parent_contexts ... ok
test native::capture_language::tests::completion::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::completion::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_complete::tests::relations::relation_label_suggestions_count_links_and_put_typed_spelling_first ... ok
test native::capture_language::tests::completion::move_bullet_completion_opens_under_both_seals ... ok
test native::capture_language::tests::completion::parent_task_plus_completes_the_terminal_token_with_utf8_byte_ranges ... ok
test native::capture_language::tests::completion::parent_task_plus_is_shared_across_parent_and_authored_lines ... ok
test native::capture_language::tests::completion::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::past_segment_suffix_field_ranges_and_queries ... ok
test native::capture_language::tests::completion::parent_task_plus_preserves_operator_and_protected_text_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture::note_pull::tests::batch_repeated_source_selected_ownership_prunes ... ok
test native::capture_language::tests::completion::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::completion::pomodoro_link_suffix_names_complete_without_replacing_the_link_start ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_per_token_inside_chains ... ok
test native::capture_language::tests::completion::nested_project_task_block_id_completes_for_its_owner ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_after_hash_on_a_named_start ... ok
test native::capture_language::tests::completion::pomodoro_start_name_leaves_link_form_names_alone ... ok
test native::capture_language::tests::completion::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_language::tests::completion::pomodoro_start_name_context_reports_ledger_behavior ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_lone_colon ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_to_bare_or_hashed_spellings ... ok
test native::capture_language::tests::completion::query_and_caret_completion_survive_a_neighboring_marker ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_partial_id ... ok
test native::capture_language::tests::completion::quoted_section_literal_decodes_its_query_and_replaces_the_quotes ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_caret_id ... ok
test native::capture_language::tests::completion::quoted_drawer_literal_decodes_its_query_and_replaces_the_quotes ... ok
test native::capture_language::tests::completion::project_task_id_before_a_child_line_route_marker_still_completes ... ok
test native::capture_language::tests::completion::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::retired_doubled_start_has_no_name_completion_or_override_context ... ok
test native::capture_language::tests::completion::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_on_nested_project_bullets_through_owner ... ok
test native::capture_language::tests::completion::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::task_block_id_route_and_authored_id_both_complete ... ok
test native::capture_language::tests::completion::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::completion::transfer_plus_picker_uses_vault_merge_target_role ... ok
test native::capture_language::tests::completion::work_log_bullet_lines_request_no_marker_completion ... ok
test native::capture_language::tests::completion::transfer_sources_complete_routes_and_tasks ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::completion::target_run_members_and_inner_edge_fragments_complete ... ok
test native::capture_language::tests::completion::transfer_merge_targets_drawers_and_sections_complete ... ok
test native::capture_language::tests::completion::transfer_arrow_and_gaps_offer_no_completion ... ok
test native::capture_language::tests::completion::route_completion_beside_a_type_marker_keeps_original_ranges ... ok
test native::capture_language::tests::completion::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::completion::transfer_destination_routes_complete_after_the_arrow ... ok
test native::capture_language::tests::completion::task_link_query_completes_the_sigil_inclusive_token ... ok
test native::capture_language::tests::draft::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::draft::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::draft::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::completion::task_list_block_id_completes_on_bullet_and_nested_lines ... ok
test native::capture_language::tests::draft::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::draft::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::draft::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::draft::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::draft::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::draft::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::draft::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::completion::target_run_completion_crosses_transparent_markers_with_source_offsets ... ok
test native::capture_language::tests::draft::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::draft::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::draft::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::draft::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::draft::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::draft::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::draft::execution_refuses_retired_priority_markers ... ok
test native::capture_language::tests::draft::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::draft::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::draft::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::draft::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::draft::execution_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::draft::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::draft::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::draft::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::draft::execution_treats_bare_dollar_as_priority_level_one ... ok
test native::capture_language::tests::drawer_bullet::bullet_cursor_must_follow_the_hash ... ok
test native::capture_language::tests::drawer_bullet::bullet_start_hash_claims_a_drawer_field_not_a_type_field ... ok
test native::capture_language::tests::drawer_bullet::each_reserved_bullet_is_flagged_once_and_a_glued_drawer_stays_quiet ... ok
test native::capture_language::tests::drawer_bullet::a_new_project_note_keeps_its_structural_sections ... ok
test native::capture_language::tests::drawer_bullet::execution_files_a_shortcut_under_a_new_task ... ok
test native::capture_language::tests::drawer_bullet::bullet_drawer_target_follows_the_item_shape ... ok
test native::capture_language::tests::drawer_bullet::leading_hash_on_a_first_level_bullet_is_a_drawer_shortcut ... ok
test native::capture_language::tests::drawer_bullet::nested_hash_still_types_and_first_level_does_not ... ok
test native::capture_language::tests::drawer_bullet::leftover_text_on_a_shortcut_is_drawer_bullet_text ... ok
test native::capture_language::tests::drawer_bullet::childless_shortcut_and_escaped_literal_hash ... ok
test native::capture_language::tests::drawer_bullet::nested_and_parent_line_hashes_still_complete_task_types ... ok
test native::capture_language::tests::drawer_bullet::bullet_continuation_needs_a_token_ending_the_line_without_a_nested_bullet ... ok
test native::capture_language::tests::drawer_bullet::quoted_literal_digit_heading_and_escaped_hashes ... ok
test native::capture_language::tests::drawer_bullet::bullet_query_decodes_a_partial_and_a_closed_literal ... ok
test native::capture_language::tests::drawer_bullet::punctuated_drawer_reports_a_drawer_bullet_span ... ok
test native::capture_language::tests::drawer_bullet::editor_reports_drawer_needs_and_all_caps_spans ... ok
test native::capture_language::tests::drawer_bullet::reserved_diagnostic_message_matches_the_commit_resolver ... ok
test native::capture_language::tests::drawer_bullet::reserved_childless_shortcut_keeps_its_drawer_notes_need ... ok
test native::capture_language::tests::drawer_bullet::reserved_ranges_are_utf8_byte_offsets ... ok
test native::capture_language::tests::drawer_bullet::legal_controls_and_vault_dependent_names_stay_unflagged ... ok
test native::capture_language::tests::drawer_bullet::notebook_note_bullet_hash_is_empty_success_with_policy ... ok
test native::capture_language::tests::editor_modes::editor_holds_unused_pomodoro_while_a_colon_id_is_unfinished ... ok
test native::capture_language::tests::editor_modes::editor_rejects_checkbox_only_project_task_ids_over_the_id_token ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_past_mode ... ok
test native::capture_language::tests::editor_modes::editor_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::editor_modes::caret_close_conflicts_agree_with_execution ... ok
test native::capture_language::tests::drawer_bullet::bullet_starts_outside_an_under_task_position_open_nothing ... ok
test native::capture_language::tests::drawer_bullet::editor_flags_reserved_shortcuts_and_literals_under_a_task ... ok
test native::capture_language::tests::editor_modes::editor_reports_unused_project_note_pomodoro_over_the_name ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_link_queries_as_incomplete ... ok
test native::capture_language::tests::editor_spans::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::editor_modes::editor_reports_named_pomodoro_start_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::attached_task_type_after_block_id_is_not_a_project_note_error ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_start_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_retired_doubled_start_forms_over_the_token ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_complete_modes_needs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_hash_token_is_a_task_type_marker_now ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::editor_spans::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_spans::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_language::tests::editor_spans::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_spans::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_spans::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_modes::editor_reports_project_task_ids_with_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_link_suffix_incomplete_states_keep_timing_and_placeholders ... ok
test native::capture_language::tests::editor_spans::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::editor_spans::editor_reports_bare_dollar_as_a_priority_span ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_priority_markers ... ok
test native::capture_language::tests::editor_spans::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_spans::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::editor_spans::editor_spans_a_bare_named_start_without_a_hash_gap ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_task_complete_tokens ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_past_tokens ... ok
test native::capture_language::tests::editor_spans::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_signed_start_timing_and_name_bytes ... ok
test native::capture_language::tests::editor_spans::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::editor_spans::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::editor_spans::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::editor_spans::editor_spans_pomodoro_link_names_after_the_equal_suffix ... ok
test native::capture_language::tests::exact_name::bare_name_spelling_never_takes_quotes ... ok
test native::capture_language::tests::editor_spans::task_link_query_spans_the_whole_token_as_a_placeholder ... ok
test native::capture_language::tests::editor_spans::editor_t_colon_is_ordinary_prose ... ok
test native::capture_language::tests::editor_spans::editor_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::exact_name::close_hash_teaches_with_decoded_name ... ok
test native::capture_language::tests::exact_name::exact_name_accepts_round_trip_fixtures ... ok
test native::capture_language::tests::editor_spans::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::exact_name::exact_name_start_reports_canonical_name_and_literal_flag ... ok
test native::capture_language::tests::editor_spans::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::exact_name::literal_spans_cover_the_quotes ... ok
test native::capture_language::tests::exact_name::exact_name_link_reports_canonical_name ... ok
test native::capture_language::tests::exact_name::invalid_literal_names_error ... ok
test native::capture_language::tests::editor_modes::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::exact_name::partial_literal_completes_on_decoded_text ... ok
test native::capture_language::tests::exact_name::unterminated_literal_is_incomplete_never_a_mistake ... ok
test native::capture_language::tests::editor_modes::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::editor_modes::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::globals::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::globals::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::globals::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::globals::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::editor_spans::incomplete_sealed_offers_keep_offer_modifiers_and_byte_exact_spans ... ok
test native::capture_language::tests::editor_spans::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::globals::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::globals::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::globals::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::globals::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::globals::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::globals::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::task_complete_items_skip_global_inheritance ... ok
test native::capture_language::tests::globals::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::grammar::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::globals::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::goto::goto_completion_field_reports_sigil_relative_queries ... ok
test native::capture_language::tests::goto::goto_claim_covers_every_table_query_row ... ok
test native::capture_language::tests::grammar::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::grammar::double_pipe_grammar_vectors ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::grammar::caret_alias_owns_relationships_in_leading_and_trailing_position ... ok
test native::capture_language::tests::goto::goto_claim_leaves_prose_byte_identical ... ok
test native::capture_language::tests::grammar::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::grammar::colon_alias_owner_is_unchanged_beside_modifiers ... ok
test native::capture_language::tests::grammar::bang_claim_covers_the_contract_table ... ok
test native::capture_language::tests::grammar::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::grammar::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::grammar::execution_keeps_task_id_lookalikes_literal_outside_project_notes ... ok
test native::capture_language::tests::grammar::execution_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::grammar::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::grammar::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::grammar::execution_evaluates_project_note_markers_parents_and_children_in_order ... ok
test native::capture_language::tests::grammar::execution_accepts_project_task_ids_and_strips_them_from_bodies ... ok
test native::capture_language::tests::grammar::execution_claims_trailing_hash_types_but_leaves_midline_hash_text ... ok
test native::capture_language::tests::grammar::execution_parses_trailing_hash_slugs_as_task_types ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_route_less_sealed_guard_agrees_across_destination_paths ... ok
test native::capture_language::tests::grammar::execution_rejects_checkbox_only_project_task_ids ... ok
test native::capture_language::tests::grammar::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::grammar::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_route_less_retired_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::grammar::execution_teaches_bare_named_start_shape_in_the_typed_spelling ... ok
test native::capture_language::tests::grammar::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::grammar::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::grammar::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::grammar::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::grammar::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_offer_markers ... ok
test native::capture_language::tests::grammar::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::grammar::execution_retires_claimed_doubled_start_family ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::grammar::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::grammar::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::grammar::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::grammar::execution_rejects_project_task_id_rule_violations_verbatim ... ok
test native::capture_language::tests::grammar::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::grammar::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::grammar::execution_treats_leading_and_trailing_timing_as_equivalent ... ok
test native::capture_language::tests::grammar::execution_refuses_route_less_sealed_project_note_offers ... ok
test native::capture_language::tests::grammar::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::grammar::plus_parent_picker_does_not_claim_operators_or_work_log_text ... ok
test native::capture_language::tests::grammar::plus_parent_picker_is_incomplete_but_keeps_the_lone_adjustment ... ok
test native::capture_language::tests::grammar::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::grammar::named_signed_start_refusals_keep_typed_names_and_timing_ranges ... ok
test native::capture_language::tests::grammar::plus_selector_beside_modifiers_needs_task_parent ... ok
test native::capture_language::tests::grammar::execution_parses_equals_family_starts_alongside_close ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffixes_teach_about_drops_duplicate_names_and_glued_timing ... ok
test native::capture_language::tests::grammar::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::grammar::task_link_query_leaves_prose_byte_identical ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_shared_timing_validation_matches_standalone ... ok
test native::capture_language::tests::grammar::pomodoro_link_operator_body_folds_only_unambiguous_unsigned_shifts ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_names_match_standalone_start_grammar ... ok
test native::capture_language::tests::grammar::task_link_query_rejects_single_colon_tokens_with_teaching_errors ... ok
test native::capture_language::tests::lists::editor_item_at_header_with_bullets_resolves_to_first_item ... ok
test native::capture_language::tests::grammar::signed_start_forms_share_the_lexer_editor_and_link_contract ... ok
test native::capture_language::tests::lists::editor_bare_header_reports_header_marker ... ok
test native::capture_language::tests::lists::editor_list_nested_children_shift_up_one_level ... ok
test native::capture_language::tests::editor_modes::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::lists::editor_lone_at_still_needs_route ... ok
test native::capture_language::tests::grammar::relationship_only_owner_refuses_text_extras ... ok
test native::capture_language::tests::lists::editor_task_list_reports_items_modes_and_spans ... ok
test native::capture_language::tests::lists::editor_duplicate_ids_land_on_the_second_bullet ... ok
test native::capture_language::tests::lists::editor_empty_list_needs_list_item ... ok
test native::capture_language::tests::lists::execution_list_nested_children_shift_up_one_level ... ok
test native::capture_language::tests::lists::editor_lone_route_reports_note_pull ... ok
test native::capture_language::tests::grammar::signed_start_refusals_are_teaching_errors_and_prose_stays_prose ... ok
test native::capture_language::tests::lists::execution_bare_at_with_bullets_refuses_incomplete_route ... ok
test native::capture_language::tests::lists::execution_consecutive_headers_split_note_pull_and_list ... ok
test native::capture_language::tests::lists::execution_section_list_bullet_kind ... ok
test native::capture_language::tests::lists::editor_misplaced_and_unfinished_id_states ... ok
test native::capture_language::tests::lists::execution_task_list_bullet_kinds_and_ids ... ok
test native::capture_language::tests::lists::split_ignores_declarations_and_non_headers ... ok
test native::capture_language::tests::lists::execution_lone_route_is_note_pull ... ok
test native::capture_language::tests::lists::editor_header_marker_points_at_the_stray_token ... ok
test native::capture_language::tests::lists::execution_list_template_rows_never_split ... ok
test native::capture_language::tests::lists::split_lone_header_is_an_empty_list ... ok
test native::capture_language::tests::lists::split_section_list_files_notes ... ok
test native::capture_language::tests::lists::split_task_list_yields_one_item_per_bullet ... ok
test native::capture_language::tests::merge_in::duplicate_sources_refuse ... ok
test native::capture_language::tests::merge_in::bare_route_and_plus_are_incomplete ... ok
test native::capture_language::tests::grammar::typed_existing_task_owner_keeps_dependency_behavior ... ok
test native::capture_language::tests::lists::split_quoted_headers_decode_and_preserve_exact ... ok
test native::capture_language::tests::lists::split_quoted_headers_hold_utf8_and_crlf_offsets ... ok
test native::capture_language::tests::lists::execution_lone_header_markers_keep_previous_meaning ... ok
test native::capture_language::tests::merge_in::editor_valid_keeps_task_mode_with_spans_and_model ... ok
test native::capture_language::tests::lists::split_header_starts_item_without_blank_line ... ok
test native::capture_language::tests::merge_in::escape_keeps_tail_literal ... ok
test native::capture_language::tests::merge_in::execution_needs_new_task_for_empty_left ... ok
test native::capture_language::tests::merge_in::execution_incomplete_uses_approved_code ... ok
test native::capture_language::tests::lists::execution_quoted_sections_carry_exact ... ok
test native::capture_language::tests::merge_in::editor_needs_new_task_carries_use_rewrite ... ok
test native::capture_language::tests::merge_in::execution_case_folds_routes_for_also_marked ... ok
test native::capture_language::tests::merge_in::editor_pending_has_need_and_placeholder_without_diagnostic ... ok
test native::capture_language::tests::merge_in::execution_attaches_clause_to_single_new_task ... ok
test native::capture_language::tests::lists::unterminated_section_literal_is_incomplete_never_a_mistake ... ok
test native::capture_language::tests::lists::execution_list_refusals_carry_stable_codes ... ok
test native::capture_language::tests::merge_in::extra_text_has_move_before_rewrite ... ok
test native::capture_language::tests::merge_in::glued_non_sources_stay_prose ... ok
test native::capture_language::tests::merge_in::glued_arrows_claim_spacing_error ... ok
test native::capture_language::tests::merge_in::execution_source_also_marked_refuses ... ok
test native::capture_language::tests::grammar::task_link_claim_is_equivalent_across_execution_editor_and_completion ... ok
test native::capture_language::tests::merge_in::nested_source_routes_reject_empty_and_dot_path_components ... ok
test native::capture_language::tests::merge_in::later_real_clause_claims_after_prose_arrow ... ok
test native::capture_language::tests::merge_in::prose_comparisons_stay_unclaimed ... ok
test native::capture_language::tests::merge_in::nested_note_paths_are_valid_source_routes ... ok
test native::capture_language::tests::merge_in::protected_markup_does_not_claim ... ok
test native::capture_language::tests::merge_in::second_arrow_is_extra_text ... ok
test native::capture_language::tests::merge_in::source_marker_and_suffix_reuse_transfer_codes ... ok
test native::capture_language::tests::merge_in::terminal_arrow_is_incomplete ... ok
test native::capture_language::tests::merge_in::valid_merge_in_claims_two_sources_in_order ... ok
test native::capture_language::tests::move_bullet::bad_charset_uses_the_existing_charset_error ... ok
test native::capture_language::tests::move_bullet::checkbox_before_the_token_is_a_teaching_error ... ok
test native::capture_language::tests::merge_in::execution_needs_new_task_for_existing_destination ... ok
test native::capture_language::tests::grammar::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_language::tests::merge_in::task_list_bullets_claim_per_bullet ... ok
test native::capture_language::tests::move_bullet::choice_lexer_claims_exact_shape_before_alphanumeric_check ... ok
test native::capture_language::tests::move_bullet::complete_move_bullet_claims_sigil_and_id_with_spans ... ok
test native::capture_language::tests::move_bullet::cross_note_shapes_point_at_another_note ... ok
test native::capture_language::tests::move_bullet::lone_sigil_followed_by_words_stays_prose ... ok
test native::capture_language::tests::move_bullet::escapes_and_protected_markup_keep_prose ... ok
test native::capture_language::tests::move_bullet::non_sigil_bodies_stay_prose ... ok
test native::capture_language::tests::move_bullet::reserved_prj_never_moves ... ok
test native::capture_language::tests::move_bullet::words_after_the_token_are_a_teaching_error ... ok
test native::capture_language::tests::note_goto::note_goto_and_task_goto_claims_are_disjoint ... ok
test native::capture_language::tests::merge_in::utf8_and_bulk_offsets_are_absolute ... ok
test native::capture_language::tests::move_bullet::markers_after_the_token_name_the_marker ... ok
test native::capture_language::tests::move_bullet::accepted_moves_record_empty_bodies_with_spans_in_both_parsers ... ok
test native::capture_language::tests::move_bullet::colon_moves_count_as_links_for_the_unused_name_rule ... ok
test native::capture_language::tests::move_bullet::choice_complete_parse_has_no_needs_and_spans_both_carets ... ok
test native::capture_language::tests::move_bullet::choice_foreign_shapes_keep_todays_meaning ... ok
test native::capture_language::tests::notebook::clip_directive_is_recorded_on_the_note ... ok
test native::capture_language::tests::move_bullet::lone_sigil_is_an_unfinished_move ... ok
test native::capture_language::tests::note_goto::note_goto_completion_field_reports_sigil_relative_queries ... ok
test native::capture_language::tests::move_bullet::choice_duplicate_names_first_line_across_parsers ... ok
test native::capture_language::tests::notebook::clipboard_marker_keeps_text_on_both_sides_of_route ... ok
test native::capture_language::tests::move_bullet::unfinished_moves_agree_on_the_need_without_a_diagnostic ... ok
test native::capture_language::tests::note_goto::note_goto_claim_covers_every_table_query_row ... ok
test native::capture_language::tests::notebook::complete_caret_seal_plus_note_creates_a_notebook ... ok
test native::capture_language::tests::notebook::empty_notebook_notes_list_is_empty_list ... ok
test native::capture_language::tests::notebook::empty_notebook_hash_header_needs_a_section ... ok
test native::capture_language::tests::notebook::create_does_not_absorb_into_a_global_declaration ... ok
test native::capture_language::tests::notebook::editor_reports_notebook_section_ambiguous ... ok
test native::capture_language::tests::notebook::empty_summary_stays_notebook_create_with_a_diagnostic ... ok
test native::capture_language::tests::notebook::empty_unsectioned_notebook_list_holds_no_tasks ... ok
test native::capture_language::tests::notebook::forced_route_claims_notebook_and_keeps_at_tokens_literal ... ok
test native::capture_language::tests::notebook::grammar_revision_is_twenty_eight ... ok
test native::capture_language::tests::notebook::global_destination_inherits_until_a_local_marker ... ok
test native::capture_language::tests::move_bullet::nested_and_foreign_lines_keep_todays_meaning ... ok
test native::capture_language::tests::notebook::global_notebook_route_refuses_bullet_led_items ... ok
test native::capture_language::tests::notebook::global_place_suffixes_are_invalid_destinations ... ok
test native::capture_language::tests::notebook::incomplete_or_colon_seals_keep_the_pomodoro_note_conflict ... ok
test native::capture_language::tests::note_goto::note_goto_claim_leaves_prose_byte_identical ... ok
test native::capture_language::tests::move_bullet::choice_teaching_errors_agree_across_parsers ... ok
test native::capture_language::tests::notebook::global_notebook_route_skips_capture_operations ... ok
test native::capture_language::tests::notebook::later_create_is_used_before_created ... ok
test native::capture_language::tests::notebook::notebook_section_list_inherits_the_header_section ... ok
test native::capture_language::tests::notebook::resolve_notebook_section_follows_precedence_and_typed_capitals ... ok
test native::capture_language::tests::notebook::named_section_header_is_not_a_list ... ok
test native::capture_language::tests::notebook::create_refusals_name_the_unsupported_marker ... ok
test native::capture_language::tests::notebook::notebook_list_files_notes_and_strips_bullet_prefixes ... ok
test native::capture_language::tests::notebook::individual_forms_claim_notes_and_sub_notes ... ok
test native::capture_language::tests::notebook::incomplete_section_and_id_refuse_instead_of_falling_back ... ok
test native::capture_language::tests::notebook::plus_id_with_bullets_fans_out_sub_notes ... ok
test native::capture_language::tests::notebook::notebook_capture_refuses_authored_checkbox_rows ... ok
test native::capture_language::tests::notebook::ordinary_named_bullet_keeps_block_id_without_a_notebook_policy ... ok
test native::capture_language::tests::notebook::notebook_section_near_miss_has_editor_diagnostics ... ok
test native::capture_language::tests::notebook::template_expansion_sees_instance_notebook_routes ... ok
test native::capture_language::tests::notebook::staged_sections_surface_percent_n_seeds_to_a_later_glued_selector ... ok
test native::capture_language::tests::notebook::unicode_and_crlf_offsets_stay_on_char_boundaries ... ok
test native::capture_language::tests::notebook::section_plus_id_splits_unquoted_and_quoted_carets ... ok
test native::capture_language::tests::notebook::staged_sections_include_earlier_creates_and_skip_later_and_failed ... ok
test native::capture_language::tests::notebook::url_on_a_notebook_is_a_plain_note ... ok
test native::capture_language::tests::past::past_both_spellings_produce_equal_specs ... ok
test native::capture_language::tests::notebook::unknown_notebook_routes_stay_on_the_established_path ... ok
test native::capture_language::tests::notebook::ordinary_plus_list_does_not_fan_out ... ok
test native::capture_language::tests::past::past_names_stop_at_operators_and_literals_hold_them ... ok
test native::capture_language::tests::past::numeric_past_later_offsets_teach_the_start_spelling ... ok
test native::capture_language::tests::past::named_past_later_offsets_teach_the_hash_spelling ... ok
test native::capture_language::tests::past::past_prose_guards_stay_prose ... ok
test native::capture_language::tests::past::past_chain_ownership_and_stacks ... ok
test native::capture_language::tests::move_bullet::execution_and_editor_agree_on_every_lexical_refusal ... ok
test native::capture_language::tests::past::past_compatibility_breaks_parse_as_chains ... ok
test native::capture_language::tests::pomodoro_merge::double_star_close_lookalike_stays_not_a_close ... ok
test native::capture_language::tests::past::past_run_pins_and_diagnostics ... ok
test native::capture_language::tests::pomodoro_merge::extra_text_is_a_shape_error ... ok
test native::capture_language::tests::pomodoro_merge::merge_completion_src_and_dest_fields ... ok
test native::capture_language::tests::pomodoro_merge::merge_into_current_omits_src ... ok
test native::capture_language::tests::past::past_names_follow_start_name_rules ... ok
test native::capture_language::tests::pomodoro_merge::merge_editor_spans_cover_sigil_and_names ... ok
test native::capture_language::tests::pomodoro_merge::trailing_hash_needs_dest_in_the_editor ... ok
test native::capture_language::tests::record::configured_type_id_as_folder_names_its_directory ... ok
test native::capture_language::tests::pomodoro_merge::digit_and_marker_star_forms_stay_retired_closes ... ok
test native::capture_language::tests::notebook::teaching_refusals_name_the_marker ... ok
test native::capture_language::tests::record::bare_route_is_a_title_need ... ok
test native::capture_language::tests::past::past_segment_suffix_valid_shapes ... ok
test native::capture_language::tests::record::editor_empty_values_need_record_value ... ok
test native::capture_language::tests::pomodoro_merge::merge_token_parses_src_and_dests ... ok
test native::capture_language::tests::past::past_unfinished_uses_existing_needs ... ok
test native::capture_language::tests::record::draft_policy_resolves_album_routes_from_the_vault ... ok
test native::capture_language::tests::pomodoro_merge::dest_less_merge_is_complete ... ok
test native::capture_language::tests::record::existing_non_record_folder_refuses ... ok
test native::capture_language::tests::record::escaped_type_text_decodes_in_title_but_keeps_original_range ... ok
test native::capture_language::tests::pomodoro_merge::dest_less_merge_with_extra_text_is_invalid ... ok
test native::capture_language::tests::record::editor_spans_cover_route_stem_and_fields ... ok
test native::capture_language::tests::record::explicit_stem_claims_both_positions ... ok
test native::capture_language::tests::record::invalid_child_lines_stay_in_the_record_path ... ok
test native::capture_language::tests::record::list_bullets_can_claim_records ... ok
test native::capture_language::tests::record::field_values_do_not_claim_template_directives_or_hide_placeholders ... ok
test native::capture_language::tests::record::legacy_records_config_does_not_claim_capture_routes ... ok
test native::capture_language::tests::record::forced_destination_keeps_record_text_literal ... ok
test native::capture_language::tests::record::field_values_stay_opaque ... ok
test native::capture_language::tests::record::fields_parse_notes_stay_notes ... ok
test native::capture_language::tests::record::nested_bullets_under_fields_refuse ... ok
test native::capture_language::tests::record::middle_route_tokens_stay_literal ... ok
test native::capture_language::tests::record::local_record_route_overrides_global_declaration ... ok
test native::capture_language::tests::record::malformed_stems_stay_in_the_record_path ... ok
test native::capture_language::tests::past::past_segment_suffix_lexical_teaching_rows ... ok
test native::capture_language::tests::record::editor_keyless_bullets_need_record_field ... ok
test native::capture_language::tests::record::record_claim_is_shared_between_paths ... ok
test native::capture_language::tests::record::record_claims_before_transfer ... ok
test native::capture_language::tests::past::past_token_table_reports_expected_specs ... ok
test native::capture_language::tests::record::unicode_ranges_survive ... ok
test native::capture_language::tests::record::sections_group_and_nested_notes_attach ... ok
test native::capture_language::tests::record::route_first_and_title_first_claim_creation ... ok
test native::capture_language::tests::ref_grammar::bare_url_claims_reference_item_when_routing_is_on ... ok
test native::capture_language::tests::record::route_only_update_has_no_title_need_and_parses_authored_notes ... ok
test native::capture_language::tests::record::task_modifier_utf8_ranges_point_to_original_bytes ... ok
test native::capture_language::tests::record::unknown_folders_stay_literal_task_text ... ok
test native::capture_language::tests::record::prose_punctuation_stays_literal ... ok
test native::capture_language::tests::ref_grammar::editor_ref_route_spans_use_byte_offsets_including_utf8 ... ok
test native::capture_language::tests::record::update_spelling_claims_both_positions_and_keeps_existing_stems ... ok
test native::capture_language::tests::ref_grammar::excluded_hosts_stay_tasks ... ok
test native::capture_language::tests::ref_grammar::mixed_list_classifies_each_line_on_its_own ... ok
test native::capture_language::tests::ref_grammar::editor_reports_ref_mode_with_one_exact_span ... ok
test native::capture_language::tests::record::unrelated_nested_task_routes_keep_task_meaning ... ok
test native::capture_language::tests::ref_grammar::editor_url_list_items_each_report_ref ... ok
test native::capture_language::tests::ref_grammar::forced_destination_global_and_clip_keep_tasks ... ok
test native::capture_language::tests::ref_grammar::claim_off_cases_stay_tasks ... ok
test native::capture_language::tests::ref_grammar::routing_off_keeps_bare_url_a_task ... ok
test native::capture_language::tests::ref_grammar::url_list_split_handles_crlf_with_exact_ranges ... ok
test native::capture_language::tests::ref_grammar::ref_parent_sources_cover_explicit_global_and_default ... ok
test native::capture_language::tests::ref_grammar::url_list_requires_every_line ... ok
test native::capture_language::tests::ref_grammar::url_list_block_splits_into_one_item_per_line ... ok
test native::capture_language::tests::retired_close::retired_closes_with_an_inline_entry_name_the_whole_rewritten_line ... ok
test native::capture_language::tests::record::marker_families_refuse_outside_field_values ... ok
test native::capture_language::tests::retired_close::retired_closes_stay_distinct_from_prose_lookalikes ... ok
test native::capture_language::tests::retired_close::double_equals_close_lookalikes_teach_the_bare_spelling ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::retired_close::retired_closes_inside_chains_fail_on_their_own_range ... ok
test native::capture_language::tests::ref_grammar::claim_accepts_wrapper_case_and_hints ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_requires_a_cursor ... ok
test native::capture_language::tests::rewrite::rewrite_draft_close_outcome_alias_leaves_templates ... ok
test native::capture_language::tests::rewrite::rewrite_draft_close_outcome_alias_requires_cursor ... ok
test native::capture_language::tests::past::past_teaching_errors_name_token_and_rewrite ... ok
test native::capture_language::tests::rewrite::rewrite_draft_close_outcome_alias_utf8_and_crlf ... ok
test native::capture_language::tests::ref_grammar::percent_l_directive_requests_companion_audio ... ok
test native::capture_language::tests::retired_close::retired_whole_item_closes_fail_with_the_bare_rewrite_in_both_parsers ... ok
test native::capture_language::tests::retired_close::retired_link_close_aliases_fail_with_the_x_rewrite ... ok
test native::capture_language::tests::rewrite::rewrite_draft_caret_plus_switches_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_comma_matches_plus_in_transfer_merge_and_run_slots ... ok
test native::capture_language::tests::rewrite::rewrite_draft_does_not_start_templates_from_a_third_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_collapses_glued_trigger_after_complete_global_route ... ok
test native::capture_language::tests::rewrite::rewrite_draft_close_outcome_aliases_stay_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_exclusions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_comma_switches_block_id_separators_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_comma_does_not_switch_in_ineligible_block_id_positions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attaches_a_pipe_after_a_relation_token ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_switches_plus_markers_to_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_toggles_task_bullet_ids ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_toggles_block_id_separators ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_after_plus_matches_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_backslash_directive_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_route_alias_stays_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_item_start_dot_route_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_past_segment_dash_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_comma_to_parent_task_picker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_keeps_route_alias_when_item_is_not_routed_or_and_cannot_open ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_does_not_toggle_ineligible_block_id_spots ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_relation_reverse_flip_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_a_sub_bullet_local_marker_local ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_close_outcome_aliases ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_relation_equals_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_complete::tests::pomodoros::accepting_a_start_name_keeps_trailing_glued_timing ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_sigil_aliases_in_route_picker_positions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_dot_route_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_dot_dependency_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_backslash_literal_where_slash_stays_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_slash_literal_after_an_album_route ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_note_goto_and_task_goto_slashes_literal ... ok
test native::capture_language::tests::record::task_markers_at_both_route_edges_refuse_as_record_modifiers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_template_drafts_untouched ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_move_bullet_sigil_aliases ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_comma_literal_outside_parent_task_picker_positions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_move_choice_dot_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_relation_flip_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_transfer_plus_triggers_for_other_marks_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_past_segment_dash_stays_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_a_run_for_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_transfer_for_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_semicolon_blocked_task_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_record_field_values_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_alternates ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_keeps_absorption_when_it_does_not_claim ... ok
test native::capture_language::tests::rewrite::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_leaves_type_markers_intact ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_requires_a_cursor ... ok
test native::capture_language::tests::rewrite::rewrite_draft_relation_direction_toggle_exclusions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_parses_as_the_switched_mode ... ok
test native::capture_language::tests::rewrite::rewrite_draft_still_collapses_global_album_slash ... ok
test native::capture_language::tests::rewrite::rewrite_draft_dot_prefers_dependency_once_item_is_routed ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_backslash_directive_alias_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_child_line_trailing_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_modifier_aliases_keep_existing_alias_precedence ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_supports_three_way_reverse_from_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_caret_marker_to_colon ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_colon_marker_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_colon_marker_to_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_before_a_schedule_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_one_item_in_a_batch ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_beside_emoji_and_preserves_crlf ... ok
test native::capture_language::tests::rewrite::rewrite_draft_relation_equals_alias_stays_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_token_that_becomes_a_run_member ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_non_move_bullet_dots_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_and_continues_merge_in_sources ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_exclusions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_sigil_aliases_exclude_other_contexts ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_back_to_colon_or_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_still_aliases_slash_without_an_album_claim ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_in_editor_positions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_transfer_destination_caret_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_transfer_source_colon_to_plus ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_uppercase_and_hyphenated_ids ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_sealed_project_note_separators ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_solo_and_leading_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_relation_flip_alias_stays_literal ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_plus_markers_with_unicode_crlf_and_schedule ... ok
test native::capture_language::tests::rewrite::slash_alias_notebook_preflight_only_fires_at_first_level_bullets ... ok
test native::capture_language::tests::rewrite::rewrite_draft_modifier_aliases_stay_literal ... ok
test native::capture_language::tests::rewrite::slash_route_album_preflight_only_fires_on_glued_single_at_routes ... ok
test native::capture_language::tests::section_bullet::caret_inside_quotes_is_title_and_outside_is_leftover ... ok
test native::capture_language::tests::section_bullet::create_seed_plan_puts_plain_siblings_first ... ok
test native::capture_language::tests::section_bullet::drawer_position_without_notebook_policy_is_unchanged ... ok
test native::capture_language::tests::section_bullet::all_caps_in_a_list_stays_a_plain_note ... ok
test native::capture_language::tests::section_bullet::create_all_caps_and_hash_merge ... ok
test native::capture_language::tests::section_bullet::editor_keeps_one_item_per_section_bullet ... ok
test native::capture_language::tests::section_bullet::editor_create_section_notes_need ... ok
test native::capture_language::tests::section_bullet::list_item_plan_ignores_all_caps ... ok
test native::capture_language::tests::section_bullet::create_plan_puts_siblings_between_and_after_sections_on_top ... ok
test native::capture_language::tests::section_bullet::editor_bare_hash_and_empty_notes_are_incomplete ... ok
test native::capture_language::tests::section_bullet::hash_under_a_single_notebook_note_stays_opaque ... ok
test native::capture_language::tests::section_bullet::list_near_miss_and_create_near_miss_refuse ... ok
test native::capture_language::tests::section_bullet::escaped_hash_stays_a_top_note ... ok
test native::capture_language::tests::rewrite::rewrite_draft_expands_slash_hash_alias ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_slash_hash_alias_literal ... ok
test native::capture_language::tests::section_bullet::header_section_plus_section_bullet_is_position_error ... ok
test native::capture_language::tests::section_bullet::scanner_hits_and_opener_exceptions ... ok
test native::capture_language::tests::section_bullet::staged_percent_n_hash_is_visible_to_a_later_glued_selector ... ok
test native::capture_language::tests::section_bullet::staged_create_sees_earlier_hash_bullets_before_the_caret ... ok
test native::capture_language::tests::section_bullet::utf8_byte_ranges_follow_the_source ... ok
test native::capture_language::tests::sized_close::sized_completion_needs_sit_after_the_prefix ... ok
test native::capture_language::tests::section_bullet::route_only_list_fans_out_nested_notes ... ok
test native::capture_language::tests::sized_close::unsized_neighbours_keep_their_meanings ... ok
test native::capture_language::tests::target_runs::all_target_line_is_not_split ... ok
test native::capture_language::tests::target_runs::between_prose_words_stays_literal ... ok
test native::capture_language::tests::sized_close::sized_operator_spans_cover_digits_and_x ... ok
test native::capture_language::tests::target_runs::child_trailing_run_needs_body_before_it ... ok
test native::capture_language::tests::section_bullet::refusals_match_the_contract_table ... ok
test native::capture_language::tests::target_runs::duplicate_message_uses_repeated_token_and_block_id ... ok
test native::capture_language::tests::sized_close::sized_incomplete_keeps_size_and_execution_refuses ... ok
test native::capture_language::tests::sized_close::sized_link_and_task_suffixes_carry_size ... ok
test native::capture_language::tests::sized_close::sized_closes_parse_in_both_parsers ... ok
test native::capture_language::tests::target_runs::duplicate_identity_ignores_case_drawer_and_toggle ... ok
test native::capture_language::tests::target_runs::editor_mixed_toggle_and_drawer_spans_are_all_kept ... ok
test native::capture_language::tests::target_runs::editor_leading_run_combines_into_one_item_with_targets ... ok
test native::capture_language::tests::target_runs::editor_separate_route_lines_still_refuse_duplicates ... ok
test native::capture_language::tests::sized_close::sized_teaching_errors_match_in_both_parsers ... ok
test native::capture_language::tests::target_runs::editor_duplicate_and_split_diagnostics_share_strict_evidence ... ok
test native::capture_language::tests::target_runs::child_line_runs_and_dependency_ownership_are_member_local ... ok
test native::capture_language::tests::sized_close::rewrite_draft_sized_close_aliases_stay_literal ... ok
test native::capture_language::tests::sized_close::sized_close_logs_and_front_chains_keep_the_size ... ok
test native::capture_language::tests::target_runs::editor_partial_members_union_needs_without_prose ... ok
test native::capture_language::tests::rewrite::rewrite_draft_toggles_complete_relation_direction ... ok
test native::capture_language::tests::target_runs::editor_trailing_and_whole_line_runs_keep_body_and_offsets ... ok
test native::capture_language::tests::sized_close::sized_looking_prose_stays_text ... ok
test native::capture_language::tests::target_runs::leading_run_selects_two_members ... ok
test native::capture_language::tests::target_runs::forced_destinations_keep_targets_literal ... ok
test native::capture_language::tests::target_runs::editor_second_item_offsets_and_unicode_stay_absolute ... ok
test native::capture_language::tests::sized_close::rewrite_draft_expands_sized_close_outcome_aliases ... ok
test native::capture_language::tests::target_runs::fanout_keeps_coded_refusals_for_later_members_and_templates ... ok
test native::capture_language::tests::target_runs::editor_terminal_extraction_matches_execution_across_the_run ... ok
test native::capture_language::tests::target_runs::list_bullets_keep_list_marker ... ok
test native::capture_language::tests::target_runs::malformed_later_member_keeps_its_existing_strict_error ... ok
test native::capture_language::tests::target_runs::partial_and_malformed_members_are_selected ... ok
test native::capture_language::tests::target_runs::non_target_tokens_end_the_run ... ok
test native::capture_language::tests::target_runs::member_views_match_singleton_equivalence ... ok
test native::capture_language::tests::target_runs::public_execution_fans_out_runs_and_reports_refusal_codes ... ok
test native::capture_language::tests::target_runs::ordinary_draft_fans_out_in_typed_order_with_shared_source_identity ... ok
test native::capture_language::tests::target_runs::expanded_members_share_one_inline_global_declaration ... ok
test native::capture_language::tests::target_runs::split_edges_refuse_with_trailing_range ... ok
test native::capture_language::tests::target_runs::trailing_run_selects_two_members ... ok
test native::capture_language::tests::target_runs::three_members_with_mixed_suffixes ... ok
test native::capture_language::tests::target_runs::unicode_offsets_are_preserved ... ok
test native::capture_language::tests::target_runs::whole_line_selects_all_members ... ok
test native::capture_language::tests::target_runs::trailing_plain_route_stays_literal ... ok
test native::capture_language::tests::target_runs::template_clipboard_refusal_keeps_its_coded_error ... ok
test native::capture_language::tests::target_runs::template_fanout_applies_cross_run_schedule_to_each_member ... ok
test native::capture_language::tests::target_runs::template_row_fans_out_without_changing_row_identity ... ok
test native::capture_language::tests::target_runs::split_refusal_precedes_duplicate_identity_across_edges ... ok
test native::capture_language::tests::target_runs::retired_priority_probe_preserves_singleton_and_selected_run_boundaries ... ok
test native::capture_language::tests::target_runs::terminal_extraction_crosses_the_run ... ok
test native::capture_language::tests::target_runs::toggle_member_keeps_relationship_refusal ... ok
test native::capture_language::tests::template::a_repeated_directive_in_the_first_item_is_a_duplicate ... ok
test native::capture_language::tests::target_runs::type_marker_spans_remain_at_original_draft_offsets_for_each_member ... ok
test native::capture_language::tests::template::a_template_needs_a_blank_separator_before_rows ... ok
test native::capture_language::tests::template::a_directive_after_markers_still_claims_the_template ... ok
test native::capture_language::tests::template::missing_placeholder_is_suppressed_until_rows_exist ... ok
test native::capture_language::tests::template::a_directive_in_a_later_item_is_misplaced ... ok
test native::capture_language::tests::template::missing_template_or_rows_has_a_teaching_issue ... ok
test native::capture_language::tests::template::definition_validation_ignores_rows_but_checks_placeholders_without_rows ... ok
test native::capture_language::tests::template::expansion_matches_the_plan_example_byte_for_byte ... ok
test native::capture_language::tests::template::mid_line_and_escaped_directives_leave_an_ordinary_draft ... ok
test native::capture_language::tests::template::non_template_expansion_is_an_identity ... ok
test native::capture_language::tests::template::multi_placeholder_extra_values_still_report_arity ... ok
test native::capture_language::tests::template::one_placeholder_global_declaration_names_containing_row ... ok
test native::capture_language::tests::template::one_placeholder_one_line_equals_three_line_expansion ... ok
test native::capture_language::tests::template::one_placeholder_mixed_lines_number_left_to_right_then_top_to_bottom ... ok
test native::capture_language::tests::template::every_directive_placement_expands_to_the_same_text ... ok
test native::capture_language::tests::template::one_placeholder_rows_share_line_with_per_value_ranges ... ok
test native::capture_language::tests::template::one_placeholder_tabs_and_repeated_spaces_split_cleanly ... ok
test native::capture_language::tests::template::one_placeholder_templates_never_report_arity ... ok
test native::capture_language::tests::template::placeholder_gaps_and_one_based_indices_are_explained ... ok
test native::capture_language::tests::template::quote_errors_and_arity_errors_are_row_scoped ... ok
test native::capture_language::tests::template::one_field_rows_split_on_spaces_and_template_line_endings_normalize ... ok
test native::capture_language::tests::template::row_global_declarations_use_row_scope ... ok
test native::capture_language::tests::template::row_values_cannot_inject_the_template_directive ... ok
test native::capture_language::tests::template::placeholder_grammar_rejects_noncanonical_and_incomplete_braces ... ok
test native::capture_language::tests::target_runs::refusal_detection_checks_only_the_selected_run ... ok
test native::capture_language::tests::target_runs::leading_run_terminals_reach_each_member_with_original_editor_spans ... ok
test native::capture_language::tests::template::placeholders_repeat_reorder_escape_and_expand_inside_markers ... ok
test native::capture_language::tests::template::row_lexer_handles_quotes_escapes_and_plain_quotes ... ok
test native::capture_language::tests::template::one_placeholder_unterminated_quote_names_value_row_and_keeps_leading_row ... ok
test native::capture_language::tests::template::template_mask_preserves_byte_offsets_and_hides_directive_rows_and_braces ... ok
test native::capture_language::tests::transfer::all_four_destinations_parse ... ok
test native::capture_language::tests::template::rows_cannot_be_bullets_and_templates_cannot_use_other_globals ... ok
test native::capture_language::tests::transfer::children_make_a_transfer_invalid ... ok
test native::capture_language::tests::template::template_mask_hides_only_the_directive_token_wherever_it_sits ... ok
test native::capture_language::tests::transfer::bad_destinations_name_the_four_shapes ... ok
test native::capture_language::tests::transfer::escaped_arrow_keeps_literal_and_drops_backslash ... ok
test native::capture_language::tests::transfer::destination_is_source_when_it_names_a_source_task ... ok
test native::capture_language::tests::transfer::execution_resolver_claims_transfer_before_target_run_fanout ... ok
test native::capture_language::tests::template::template_directive_sits_at_either_edge_of_any_line_of_the_first_item ... ok
test native::capture_language::tests::transfer::editor_transfer_contract_has_modes_spans_and_destination_fields ... ok
test native::capture_language::tests::transfer::glued_arrows_need_spaces ... ok
test native::capture_language::tests::transfer::extra_text_after_destination_is_refused ... ok
test native::capture_language::tests::template::one_placeholder_thousand_and_first_value_is_too_large ... ok
test native::capture_language::tests::transfer::lexical_duplicates_use_parent_identity ... ok
test native::capture_language::tests::transfer::many_sources_keep_typed_order_and_spans ... ok
test native::capture_language::tests::transfer::plus_transfer_destinations_only_open_the_picker_for_selector_tokens ... ok
test native::capture_language::tests::transfer::incomplete_transfer_is_never_reinterpreted_as_capture_text ... ok
test native::capture_language::tests::transfer::escaped_arrow_drops_only_its_escape_and_skips_transfer_claiming ... ok
test native::capture_language::tests::transfer::source_markers_teach_plus_ids ... ok
test native::capture_language::tests::transfer::transfer_needs_use_editor_labels ... ok
test native::capture_language::tests::transfer::source_suffixes_name_the_drawer_or_toggle ... ok
test native::capture_language::tests::transfer::single_source_note_destination_is_valid ... ok
test native::capture_language::tests::transfer::partial_right_hand_sides_report_needs ... ok
test native::capture_language::tests::transfer::prose_code_and_blockquotes_stay_unclaimed ... ok
test native::capture_language::tests::transfer::utf8_and_crlf_offsets_stay_on_char_boundaries ... ok
test native::capture_language::tests::transfer::quoted_selectors_preserve_intent ... ok
test native::capture_language::tests::type_marker::attached_route_type_completion_keeps_the_marker_attached ... ok
test native::capture_language::tests::transfer::transfer_plus_selector_is_an_incomplete_task_picker ... ok
test native::capture_language::tests::target_runs::each_member_reuses_singleton_semantics_for_toggles_drawers_and_schedule ... ok
test native::capture_language::tests::type_marker::malformed_masked_operators_keep_their_existing_errors ... ok
test native::capture_language::tests::type_marker::marker_edge_transparency_includes_clip_directives ... ok
test native::capture_language::tests::type_marker::template_rows_keep_type_metadata_and_template_local_offsets ... ok
test native::capture_language::tests::type_marker::marker_only_continuations_stay_with_the_original_item ... ok
test native::capture_language::tests::type_marker::escaped_midline_uppercase_and_protected_tokens_remain_body_text ... ok
test native::capture_language::tests::type_marker::digit_heading_dash_and_midline_hashes_stay_prose ... ok
test native::capture_language::tests::type_marker::url_lists_and_operator_chains_probe_the_masked_line ... ok
test native::capture_language::tests::type_marker::unicode_and_crlf_offsets_index_the_original_draft ... ok
test native::capture_language::tests::type_marker::only_task_subjects_accept_markers ... ok
test native::capture_language::tests::type_marker::incomplete_invalid_and_duplicate_markers_have_teaching_errors ... ok
test native::capture_language::tests::type_marker::edge_clock_tags_stay_task_text_and_never_become_type_markers ... ok
test native::capture_language::tests::type_marker::slug_literal_and_marker_run_keep_original_byte_ranges ... ok
test native::capture_language::tests::type_marker::fixture_vectors_preserve_the_task_body_and_attach_one_type ... ok
test native::capture_language::tests::type_marker_editor::exact_name_resolution_prefers_config_then_catalog ... ok
test native::capture_language::tests::type_marker_editor::a_marker_alone_needs_a_task ... ok
test native::capture_language::tests::type_marker_editor::attached_project_marker_stays_midline_only_when_route_is_not_at_an_edge ... ok
test native::capture_language::tests::type_marker_editor::duplicate_markers_share_the_execution_duplicate_diagnostic ... ok
test native::capture_language::tests::type_marker_editor::leading_marker_and_child_line_markers_type_the_same_item ... ok
test native::capture_language::tests::type_marker_editor::bodiless_forms_need_a_task_like_their_masked_parse ... ok
test native::capture_language::tests::type_marker_editor::incomplete_marker_needs_a_task_type_without_a_diagnostic ... ok
test native::capture_language::tests::type_marker_editor::clipboard_notes_accept_type_markers_without_task_need ... ok
test native::capture_language::tests::type_marker_editor::invalid_markers_carry_the_shared_teaching_copy ... ok
test native::capture_language::tests::type_marker_editor::global_task_route_inheritance_keeps_type_markers_on_new_tasks ... ok
test native::capture_language::tests::type_marker_editor::marker_only_continuation_lines_contribute_no_child_body ... ok
test native::capture_language::tests::type_marker_editor::trailing_marker_keeps_the_task_body_and_adds_a_whole_token_span ... ok
test native::capture_link_tasks::tests::ranker_orders_by_tier_sum_then_canonical_order ... ok
test native::capture_link_tasks::tests::ranker_passes_the_dependency_contract_dk_vectors ... ok
test native::capture_link_tasks::tests::pulls_forward_only_for_a_single_future_scheduled_field ... ok
test native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_language::tests::type_marker_editor::template_rows_keep_markers_out_of_the_body ... ok
test native::capture_language::tests::type_marker_editor::attached_literal_spans_touch_route_ids_and_incomplete_literals_need_type ... ok
test native::capture_language::tests::type_marker_editor::existing_subjects_accept_markers ... ok
test native::capture_language::tests::type_marker_editor::marker_offsets_survive_unicode_and_escaped_text ... ok
test native::capture_language::tests::type_marker_editor::non_task_subjects_are_refused_with_the_shared_copy ... ok
test native::capture_language::tests::type_marker_editor::execution_and_editor_agree_on_typed_task_bodies ... ok
test native::capture_link_tasks::tests::warns_when_the_day_file_is_missing_but_lists_tasks ... ok
test native::capture_link_tasks::tests::ranker_matches_the_worked_example_queries ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_link_tasks::tests::suggestions_avoid_used_ids_including_non_task_anchors ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_link_tasks::tests::excludes_closed_unknown_terminal_untyped_and_unroutable ... ok
test native::capture_links::tests::vault_wide_link_suggestions_rank_daily_ahead_of_satellites ... ok
test native::capture_links::tests::vault_wide_link_suggestions_partition_living_archive_and_hidden ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_links::tests::archived_notes_remain_resolvable_and_target_scoped ... ok
test native::capture_links::tests::vault_wide_link_suggestions_rank_library_sidecars_after_living ... ok
test native::capture_notebooks::tests::forced_destination_is_indexed_without_reading_draft_routes ... ok
test native::capture_link_tasks::tests::worked_example_lists_eight_rows_in_canonical_order ... ok
test native::capture_links::tests::empty_vault_wide_link_query_partitions_living_archive_and_hidden ... ok
test native::capture_notebooks::tests::every_notebook_frontmatter_type_shape_is_recognized ... ok
test native::capture_notebooks::tests::ordinary_routes_are_not_claimed_as_notebooks ... ok
test native::capture_notebooks::tests::route_metadata_uses_notebook_title_owner_and_breadcrumb ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_links::tests::matching_note_inserts_keep_living_ahead_of_archive_twins ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_parse::tests::format_pomodoro_close_reports_detail_counts ... ok
test native::capture_parse::tests::format_pomodoro_close_describes_wildcard_scope ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_links::tests::vault_wide_link_suggestions_truncate_to_living_before_archive ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_parse::tests::bare_album_without_owner_reports_problem_and_omits_rewrite ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::bare_album_task_home_refuses_with_owner_and_rewrite ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_link_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_notebooks::tests::unrouted_draft_reads_no_files_and_repeated_candidates_read_once ... ok
test native::capture_language::tests::type_marker_editor::masked_items_match_their_baseline_across_grammar_families ... ok
test native::capture_parse::tests::json_reports_merge_in_pending_need_without_diagnostic ... ok
test native::capture_parse::tests::json_reports_global_route_with_no_mode_or_block_id_fields ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::json_reports_merge_in_wire_shape_and_grammar_27 ... ok
test native::capture_parse::tests::json_reports_glued_start_suffix_names ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_parse::tests::json_reports_merge_in_rewrite_and_reparses ... ok
test native::capture_parse::tests::album_routes_carry_source_metadata_through_parse ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_targets_for_public_runs ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_parse::tests::lone_route_reports_note_pull_mode ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::record_parse_ignores_legacy_records_configuration ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_parse::tests::json_reports_named_pomodoro_starts ... ok
test native::capture_pomodoro_close::ledger::managed_dependency_tests::dependency_lines_are_notes_not_close_targets ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_parse::tests::json_reports_retired_doubled_starts_with_token_ranges ... ok
test native::capture_pomodoro_close::linked_task_tests::custom_in_progress_symbol_gets_no_listed_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::closing_a_dependent_leaves_depends_on_prerequisites_open ... ok
test native::capture_parse::tests::record_parse_keeps_repeated_field_ranges_disjoint_from_notes ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::listed_duplicate_embedded_and_plain_warns_once_for_not_completed ... ok
test native::capture_pomodoro_close::linked_task_tests::mentioned_first_bare_link_gets_number_and_blocked_warning ... ok
test native::capture_parse::tests::record_parse_projects_engine_fields_defaults_and_source_ranges ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_pomodoro_close::linked_task_tests::same_task_numbered_twice_carries_lowest_number ... ok
test native::capture_parse::tests::record_parse_reports_per_item_and_same_draft_collisions ... ok
test native::capture_language::tests::template::both_template_bounds_are_checked_without_truncation ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_complete_writes_done_task_with_completion_date ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_align_with_typed_entries ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_nest_undated_in_task_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_in_progress_and_complete_updates_both_tasks ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_listed_row_warns_exactly_once ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_lands_in_task_work_log_as_typed_subset ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_on_complete_target_land_in_completed_task ... ok
test native::capture_pomodoro_close::linked_tasks::clock_tests::only_canonical_daily_timed_entries_supply_a_close_clock ... ok
test native::capture_pomodoro_close::names::tests::deferring_everything_keeps_both_names ... ok
test native::capture_pomodoro_close::names::tests::carried_drift_retypes_the_continuation ... ok
test native::capture_pomodoro_close::names::tests::drifted_work_settles_both_sessions ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_typed_target_warns_and_stays_in_pomodoro ... ok
test native::capture_pomodoro_close::names::tests::parked_and_dropped_links_are_not_carried ... ok
test native::capture_pomodoro_close::names::tests::only_fix_worked_narrows_and_the_last_fix_done_sheds ... ok
test native::capture_parse::tests::json_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_pomodoro_close::names::tests::single_type_close_settles_to_the_worked_type ... ok
test native::capture_pomodoro_close::names::tests::shedding_every_type_keeps_the_base ... ok
test native::capture_pomodoro_close::names::tests::untyped_worked_links_keep_the_name ... ok
test native::capture_parse::tests::record_parse_keeps_schema_for_incomplete_titles_and_unknown_fields ... ok
test native::capture_pomodoro_close::names::tests::single_type_meet_and_unnamed_never_rename ... ok
test native::capture_pomodoro_close::selection_tests::conflicting_duplicates_fail_and_same_outcome_passes ... ok
test native::capture_pomodoro_close::selection_tests::embedded_hash_alias_and_tomato ... ok
test native::capture_pomodoro_close::selection_tests::complete_only_selection_keeps_unlisted_event_clock_outcomes ... ok
test native::capture_pomodoro_close::selection_tests::any_numbered_list_defers_unlisted_links_and_preserves_authored_markers ... ok
test native::capture_pomodoro_close::selection_tests::drop_removes_from_closed_session_without_carry ... ok
test native::capture_pomodoro_close::selection_tests::fenced_links_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::apply_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::lexically_resolved_positional_entry_reports_nested_wording ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_on_complete_target_lands_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::log_entries_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_stamped_work_logs ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_appends_after_existing_descendants ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_child_indent_follows_first_child_or_link_indent ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_preserve_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::full_close_reports_numbered_lineup_with_none ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_nest_one_level_under_the_entry ... ok
test native::capture_pomodoro_close::selection_tests::listed_blocked_and_done_warnings ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_text_that_numbers_a_link_fails_loudly ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::managed_dependency_lines_are_not_numbered_for_close_or_agenda ... ok
test native::capture_pomodoro_close::selection_tests::nested_bare_links_are_numbered ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_errors ... ok
test native::capture_pomodoro_close::selection_tests::mixed_lines_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x2 ... ok
test native::capture_pomodoro_close::selection_tests::numbers_the_worked_example ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_with_one_and_zero_links ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_messages ... ok
test native::capture_pomodoro_close::selection_tests::outcome_table_covers_every_row ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x_complete ... ok
test native::capture_pomodoro_close::selection_tests::none_is_byte_identical_to_plan_ledger_close ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_resolve_against_session_worked_links ... ok
test native::capture_pomodoro_close::selection_tests::parked_links_record_work_but_are_not_carried ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_share_a_single_worked_link ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_skip_nested_links ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_follow_drop_and_complete_outcomes ... ok
test native::capture_pomodoro_close::selection_tests::rewrite_keeps_prefix_and_drops_tomato ... ok
test native::capture_pomodoro_close::selection_tests::positional_resolution_reports_session_failures ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_dedup_duplicate_targets ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_expand_in_typed_order ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_accepts_an_empty_lineup_but_explicit_positive_indices_do_not ... ok
test native::capture_pomodoro_close::selection_tests::star_entry_nested_wording_names_the_star_origin ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_follow_numbered_bullets_in_non_selection_mode ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_report_nothing_left_and_empty_w ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_use_lexical_w_in_selection_mode ... ok
test native::capture_pomodoro_close::tests::bare_close_stamps_the_legacy_off_clock_duration ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_positional_logs_wait_for_and_use_top_level_worked_lineup ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_outcomes_cover_remaining_numbered_links_and_keep_exceptions ... ok
test native::capture_pomodoro_close::tests::close_after_the_start_still_shortens_by_whole_units ... ok
test native::capture_pomodoro_close::tests::close_before_the_start_clamps_to_a_zero_length_session ... ok
test native::capture_pomodoro_close::selection_tests::star_entries_use_top_level_lineup_for_wildcards ... ok
test native::capture_pomodoro_close::tests::close_names::without_names_both_sessions_keep_the_running_name ... ok
test native::capture_pomodoro_close::tests::conflicting_close_keeps_worked_key_and_drops_off_clock_key ... ok
test native::capture_pomodoro_close::tests::close_names::a_reused_later_entry_is_never_renamed_and_sheds_nothing ... ok
test native::capture_pomodoro_close::tests::close_names::narrowed_closed_line_and_shed_placeholder ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::tests::keyed_off_clock_close_preserves_the_recorded_minutes ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::an_open_placeholder_above_is_never_an_anchor ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_lands_before_a_hand_ordered_completed_entry ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_last_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::no_open_entry_below_keeps_todays_slot ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::meet_close_carrying_a_link_moves_the_continuation_last ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::non_meet_close_keeps_todays_slot ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::deferred_and_dropped_lines_keep_the_reported_line_right ... ok
test native::capture_pomodoro_close::tests::meet_continuation_last::continuation_follows_nested_children_and_interior_blanks ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x0_and_x1_2 ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x1_complete_2 ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture_pomodoro_start::drop_tests::created_session_reports_the_new_session_variant ... ok
test native::capture_pomodoro_start::drop_tests::dropped_last_line_without_final_newline_leaves_none ... ok
test native::capture_pomodoro_start::drop_tests::dropped_middle_line_without_final_newline_keeps_structure ... ok
test native::capture_pomodoro_start::drop_tests::drops_embedded_and_unresolved_rows_by_number ... ok
test native::capture_pomodoro_start::drop_tests::drops_nested_links_with_their_parent ... ok
test native::capture_pomodoro_start::drop_tests::drops_numbered_subtree_and_keeps_gaps ... ok
test native::capture_pomodoro_start::drop_tests::empty_drop_is_byte_identical ... ok
test native::capture_pomodoro_start::drop_tests::duplicate_still_queued_warns ... ok
test native::capture_pomodoro_start::drop_tests::empty_lineup_suggests_the_token_without_its_drop ... ok
test native::capture_pomodoro_start::drop_tests::fenced_lines_are_not_numbered ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_pomodoro_start::drop_tests::preserves_crlf ... ok
test native::capture_pomodoro_start::drop_tests::out_of_range_names_every_bad_number ... ok
test native::capture_pomodoro_start::drop_tests::three_bad_numbers_join_with_commas ... ok
test native::capture_pomodoro_start::lineup_tests::lists_direct_children_in_ledger_order ... ok
test native::capture_pomodoro_start::lineup_tests::managed_dependency_lines_are_not_start_lineup_items ... ok
test native::capture_pomodoro_start::lineup_tests::resolves_rows_through_the_staged_view ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_preserves_crlf_line_numbers ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_matches_wrapper_across_sessions ... ok
test native::capture_pomodoro_start::lineup_tests::skips_fenced_lines ... ok
test native::capture_pomodoro_start::lineup_tests::skips_deeper_descendants_embeds_and_struck_lines ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoros::tests::completed_summary_prefers_recorded_duration ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_parse::tests::record_parse_retains_empty_missing_and_invalid_field_states ... ok
test native::capture_complete::tests::output::named_start_completion_carries_keeps_ledger_and_running ... ok
test native::capture_parse::tests::incomplete_type_markers_attach_no_theme_ref ... ok
test native::capture_parse::tests::record_parse_maps_explicit_stems_single_colon_and_collection_fix ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... ok
test native::capture_pomodoros::tests::max_task_link_count_includes_running_and_placeholder_entries ... ok
test native::capture_pomodoros::tests::max_task_link_count_reports_twelve_for_an_open_placeholder ... ok
test native::capture_parse::tests::theme_name_spans_report_components_with_source_offsets ... ok
test native::capture_pomodoros::tests::max_task_link_count_is_zero_without_open_entries ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_parse::tests::task_type_spans_carry_one_ref_over_the_name_content ... ok
test native::capture_pomodoros_agenda::tests::agenda_location_reads_title_then_maps_url ... ok
test native::capture_pomodoros_agenda::tests::crlf_and_missing_final_newline_resolve ... ok
test native::capture_pomodoros_agenda::tests::current_numbers_match_number_task_links_walk ... ok
test native::capture_pomodoros_agenda::tests::each_note_reads_once_per_filter_mode ... ok
test native::capture_pomodoros_agenda::tests::logs_tag_subtrees_and_prose_is_untagged ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::capture_pomodoros_agenda::tests::long_task_blocks_truncate_at_150_lines ... ok
test native::capture_pomodoros_agenda::tests::open_entries_can_link_done_tasks ... ok
test native::capture_pomodoros_agenda::tests::nested_log_markers_keep_their_own_kind ... ok
test native::capture_pomodoros_agenda::tests::overnight_ranges_roll_the_end_date ... ok
test native::capture_pomodoros_agenda::tests::pomodoro_markers_and_prose_mix_with_links ... ok
test native::capture_pomodoros_agenda::tests::relation_lines_are_not_agenda_task_links ... ok
test native::capture_pomodoros_agenda::tests::resolved_items_carry_ledger_notes ... ok
test native::capture_pomodoros_agenda::tests::resolutions_cover_every_failure_mode ... ok
test native::capture_pomodoros_agenda::tests::rotten_log_markers_serialize_as_rotten ... ok
test native::capture_pomodoros_agenda::tests::roles_numbers_and_retired_counts ... ok
test native::capture_pomodoros_agenda::tests::task_block_lines_have_clean_text_kinds_and_depths ... ok
test native::capture_pomodoros_agenda::tests::unreadable_notes_fail_soft ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::captured_timestamp_is_minute_precision_with_matching_offset ... ok
test native::capture_project_note::tests::captured_timestamp_uses_shared_format_helper ... ok
test native::capture_project_note::tests::caret_task_keeps_its_authored_checkbox ... ok
test native::capture_project_note::tests::configured_cancelled_status_stays_closed_in_project_note ... ok
test native::capture_project_note::tests::configured_zone_controls_created_offset_on_utc_clock_hosts ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::named_all_caps_bullet_with_children_stays_a_task ... ok
test native::capture_project_note::tests::named_task_keeps_an_existing_created_stamp_before_the_id ... ok
test native::capture_project_note::tests::named_tasks_render_ids_last_with_next_status_for_links ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::prj_task_is_never_linked ... ok
test native::capture_project_note::tests::render_stamps_created_in_the_configured_zone ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::scheduled_date_lands_inline_on_prj_with_a_blocked_checkbox ... ok
test native::capture_project_note::tests::scheduled_project_renders_linked_tasks_as_blocked ... ok
test native::capture_project_note::tests::section_title_shape_allows_sentence_punctuation ... ok
test native::capture_project_note::tests::task_rows_cover_unnamed_hidden_closed_and_placeholder ... ok
test native::capture_project_note::tests::task_rows_keep_source_identity_when_tasks_section_merges_after ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_project_note::tests::unconfigured_status_stays_authored_in_scheduled_project_note ... ok
test native::capture_record::tests::album_create_carries_source_metadata_and_canonical_storage ... ok
test native::capture_pomodoros_agenda::tests::september_shaped_vault_finishes_fast ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_record::tests::create_to_update_rewrite_is_item_scoped_for_both_route_positions ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_for_completed_entries ... ok
test native::capture_pomodoros::tests::max_task_link_count_uses_the_largest_placeholder_lineup ... ok
test native::capture_record::tests::ordinary_drafts_do_no_album_or_folder_reads ... ok
test native::capture_record::tests::invocation_context_reuses_schema_and_folder_index ... ok
test native::capture_record::tests::bad_byte_album_head_is_explicit_discovery_incomplete ... ok
test native::capture_record::tests::legacy_config_never_resurrects_a_record_route ... ok
test native::capture_record::tests::broken_album_never_falls_back_to_config ... ok
test native::capture_record::tests::healthy_album_stays_usable_despite_unrelated_bad_file ... ok
test native::capture_related::tests::cosine_is_symmetric_on_identical_titles ... ok
test native::capture_record::tests::staged_create_then_update_shares_one_batch_overlay ... ok
test native::capture_related::tests::excludes_gtd_checklist_and_closed_recurring_rows ... ok
test native::capture_related::tests::merge_in_sources_are_linked_and_relate_actions_anchor_before_the_arrow ... ok
test native::capture_related::tests::band_edges_and_short_query_rules ... ok
test native::capture_related::tests::closed_window_includes_30_days_and_excludes_31 ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_without_a_current_session ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_with_multiple_open_timed_entries ... ok
test native::capture_related::tests::notebook_notes_have_no_similar_band_while_mixed_drafts_keep_task_rows ... ok
test native::capture_related::tests::ordering_prefers_band_then_open_then_status ... ok
test native::capture_related::tests::same_title_normalization_strips_punctuation_and_tags ... ok
test native::capture_related::tests::stopwords_stay_sorted_for_binary_search ... ok
test native::capture_related::tests::record_near_title_match_carries_scope_and_add_to ... ok
test native::capture_related::tests::record_update_items_have_no_rows ... ok
test native::capture_related::tests::tokenizer_records_display_spans ... ok
test native::capture_related::tests::record_number_guard_never_reports_duplicate ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_related::tests::tokenizer_table_covers_bob_aware_cases ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_related::tests::record_unrelated_title_has_no_rows ... ok
test native::capture_rewrite::tests::json_does_not_search_for_a_separator_toggle_without_a_cursor ... ok
test native::capture_rewrite::tests::close_items_are_never_rewritten ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_rewrite::tests::json_reports_an_existing_task_destination_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_rewrite::tests::json_shape_attaches_a_relation_label_pipe ... ok
test native::capture_rewrite::tests::json_shape_expands_a_whole_item_task_link_alias ... ok
test native::capture_rewrite::tests::json_shape_expands_a_route_sigil_alias ... ok
test native::capture_rewrite::tests::json_shape_expands_a_glued_target_comma_to_parent_continuation ... ok
test native::capture_rewrite::tests::json_shape_expands_comma_to_parent_task_picker ... ok
test native::capture_rewrite::tests::json_shape_switches_a_block_id_separator ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_after_existing_children ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_for_a_childless_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_rotten_log_only_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_work_log_only_task ... ok
test native::capture_schedule_log::tests::insertion_ignores_a_marker_nested_under_another_child ... ok
test native::capture_schedule_log::tests::insertion_prefers_the_schedule_marker_over_other_logs ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_legacy_marker ... ok
test native::capture_rewrite::tests::json_shape_switches_a_colon_marker_to_plus ... ok
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
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_targets::tests::legacy_records_config_does_not_add_capture_routes ... ok
test native::capture_targets::tests::broken_album_is_reported_without_hiding_healthy_or_config_routes ... ok
test native::capture_targets::tests::base_scan_hides_notebooks_while_opt_in_lists_them_after_projects ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::partial_registry_hides_every_record_capture_target ... ok
test native::capture_related::tests::scorer_pairs_from_research ... ok
test native::capture_targets::tests::scan_reads_aliases_and_warns_on_conflicts ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_targets::tests::scan_warns_on_shadowed_alias ... ok
test native::capture_targets::tests::scan_uses_album_registry_and_enriches_record_target_metadata ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_targets::tests::scan_appends_indexed_record_folders_after_note_targets ... ok
test native::capture_related::tests::numbers_that_differ_cap_duplicates_at_similar ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_related::tests::archive_candidates_follow_resolved_source_after_rename ... ok
test native::capture_task_id::tests::notebook_assignment_rejects_non_note_and_duplicate_ids ... ok
test native::capture_related::tests::archive_closed_window_respects_mtime ... ok
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
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_multiline_source ... ok
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_source ... ok
test native::capture_task_toggle::tests::ledger_entry_moves_q_to_the_named_ref ... ok
test native::capture_task_toggle::tests::ledger_entry_stale_ref_is_stale_pomodoro ... ok
test native::capture_task_toggle::tests::ledger_exact_name_creates_when_only_a_prefix_matches ... ok
test native::capture_task_toggle::tests::ledger_exact_name_reuses_a_whole_slug_open_entry ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_preserves_struck_links_and_removes_only_live_occurrences ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_task_toggle::tests::typed_insertion_creates_one_shared_placeholder ... ok
test native::capture_task_toggle::tests::typed_relocation_moves_the_queue_to_the_placed_entry ... ok
test native::capture_task_toggle::tests::typed_selection_creates_a_placeholder_past_the_ledger ... ok
test native::capture_task_toggle::tests::typed_selection_creates_past_the_old_cap ... ok
test native::capture_task_toggle::tests::typed_selection_keeps_timed_ambiguity_without_an_exact_match ... ok
test native::capture_task_toggle::tests::typed_selection_prefers_the_running_exact_entry ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_task_wikilinks::tests::at_sigil_in_query_stays_wikilink_task ... ok
test native::capture_task_wikilinks::tests::closed_token_covers_caret_through_end_of_closer ... ok
test native::capture_task_wikilinks::tests::closed_token_covers_closer ... ok
test native::capture_task_wikilinks::tests::crlf_draft_keeps_byte_offsets ... ok
test native::capture_task_wikilinks::tests::forbidden_query_chars_reject_the_field ... ok
test native::capture_task_wikilinks::tests::inside_wikilink_is_protected ... ok
test native::capture_task_wikilinks::tests::mid_word_caret_does_not_swallow_following_text ... ok
test native::capture_task_wikilinks::tests::mid_word_never_triggers ... ok
test native::capture_task_wikilinks::tests::multibyte_prefix_uses_byte_offsets ... ok
test native::capture_task_wikilinks::tests::opener_after_space ... ok
test native::capture_task_wikilinks::tests::opener_at_line_start ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::capture_task_id::tests::notebook_assignment_writes_and_returns_parent_replacement ... ok
test native::capture_task_wikilinks::tests::triple_paren_never_triggers ... ok
test native::capture_task_wikilinks::tests::whole_item_actions_request_no_field ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_task_wikilinks::tests::work_log_child_is_not_a_field ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_pomodoros::tests::task_link_count_numbers_only_numbered_links ... ok
test native::capture_pomodoros::tests::max_task_link_count_ignores_completed_entries_with_or_without_all ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::capture_pomodoros::tests::task_link_count_reports_ten_or_more_links ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_templates::command::tests::relative_time_uses_the_bob_clock_value ... ok
test native::capture_templates::command::tests::selectors_use_one_or_two_digits_for_one_based_indices ... ok
test native::capture_templates::store::tests::a_draft_without_the_directive_has_no_canonical_text ... ok
test native::capture_templates::store::tests::canonical_text_handles_crlf_unicode_escapes_and_header_gap ... ok
test native::capture_task_wikilinks::tests::unclosed_token_stops_before_punctuation_and_preserves_suffix ... ok
test native::capture_templates::store::tests::canonical_text_strips_trailing_space_and_keeps_layout ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_templates::store::tests::one_row_and_many_rows_save_the_same_entry ... ok
test native::capture_templates::store::tests::newer_schema_refuses_writes_and_keeps_bytes ... ok
test native::capture_pomodoros::tests::tasks_human_output_has_agenda_rows ... ok
test native::capture_templates::store::tests::origin_validation_accepts_only_short_alphanumerics ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::capture_pomodoros::tests::tasks_json_includes_derived_homes ... ok
test native::capture_templates::store::tests::template_ids_are_stable_and_content_addressed ... ok
test native::capture_templates::store::tests::the_directive_never_changes_the_content_id ... ok
test native::capture_templates::store::tests::corrupt_file_is_quarantined_on_write ... ok
test native::capture_templates::store::tests::origin_replace_keeps_unknown_fields ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_work_log::tests::creates_work_log_after_rotten_log_and_leaves_rotten_untouched ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_work_log::tests::work_log_stamp_uses_iso_minute_precision ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::config::capture::tests::accepts_zero_through_cap ... ok
test native::collect_done::tests::health::capture_failure_reports_incomplete_diagnostics ... ok
test native::config::capture::tests::clipboard_command_list_is_ignored_under_other_values ... ok
test native::config::capture::tests::clipboard_history_accepts_every_setting ... ok
test native::config::capture::tests::clipboard_history_defaults_to_auto ... ok
test native::config::capture::tests::clipboard_history_command_requires_a_nonempty_argv_list ... ok
test native::config::capture::tests::clipboard_keys_load_independently_of_max_saved_templates ... ok
test native::config::capture::tests::clipboard_history_rejects_invalid_scalars ... ok
test native::config::capture::tests::missing_capture_block_uses_default ... ok
test native::gkeep::render::tests::capture_grammar_lookalikes_stay_literal ... ok
test native::config::capture::tests::rejects_out_of_range_and_non_integer ... ok
test native::gmail::sync::file::tests::missing_inbox_template_keeps_the_capture_parent_and_ready_cap ... ok
test native::highlights_ref::clip_adapter::tests::capture_request_omits_out_pdf_when_render_is_false ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_defaults_new_render_paths ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_preserves_gist_metadata_and_provenance ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_reads_article_json ... ok
test native::highlights_ref::clip_adapter::tests::single_capture_request_json_is_byte_identical ... ok
test native::highlights_ref::collection::tests::encoded_twin_spelling_overlaps_the_recorded_capture ... ok
test native::highlights_ref::create::tests::markdown_marker_carries_minute_captured_in_extra_order ... ok
test native::highlights_ref::create::tests::pdf_marker_carries_minute_captured_in_extra_order ... ok
test native::highlights_ref::duplicate::tests::captured_compare_orders_by_date_then_full_value ... ok
test native::highlights_ref::duplicate::tests::captured_refusal_renders_date_part_only ... ok
test native::highlights_ref::duplicate::tests::single_captured_copy_renders_detail_and_hints ... ok
test native::highlights_ref::recapture::tests::allocation_skips_occupied_and_refuses_at_cap ... ok
test native::capture_templates::store::tests::shelf_files_use_restricted_permissions ... ok
test native::capture_templates::store::tests::unknown_fields_survive_a_rewrite ... ok
test native::capture_templates::store::tests::lock_timeout_reports_busy ... ok
test native::gmail::sync::archive_scan::tests::saved_ids_and_fingerprints_are_captured_and_stable ... ok
test native::capture_templates::store::tests::origin_replace_swaps_in_one_write_and_keeps_history ... ok
test native::capture_templates::store::tests::repeated_captures_dedupe_and_bump ... ok
test native::capture_task_id::tests::notebook_assignment_handles_stale_shifted_and_format_edges ... ok
test native::highlights_ref::recapture::tests::defaults_come_from_the_newest_located_task ... ok
test native::capture_task_wikilinks::vectors_tests::vectors_match_candidates_and_link_targets ... ok
test native::capture_task_wikilinks::tests::task_spans_cover_exactly_the_completion_fields ... ok
test native::highlights_ref::recapture::tests::exact_family_wins_over_a_larger_overlapping_collection ... ok
test native::highlights_ref::recapture::tests::legacy_only_hits_are_not_family_roots ... ok
test native::highlights_ref::recapture::tests::occupancy_covers_sidecars_audio_assets_and_ids ... ok
test native::highlights_ref::recapture::tests::attach_hit_follows_the_family_to_its_newest_reading ... ok
test native::highlights_ref::recapture::tests::free_title_stem_is_an_ordinary_capture ... ok
test native::highlights_ref::recapture::tests::deleted_family_root_is_recovered_from_the_oldest_lineage_entry ... ok
test native::highlights_ref::recapture::tests::output_on_a_captured_reread_names_the_allocated_stem ... ok
test native::highlights_ref::recapture::tests::dangling_middle_member_keeps_max_reading ... ok
test native::highlights_ref::recapture::tests::report_line_covers_every_detail_row ... ok
test native::highlights_ref::recapture::tests::exact_set_multi_reading_family_counts_as_one ... ok
test native::highlights_ref::recapture::tests::family_of_three_orders_newest_first ... ok
test native::capture_pomodoros::tests::tasks_headline_is_display_null_or_omitted ... ok
test native::capture::tests::template::planning_each_template_matches_planning_its_expansion ... ok
test native::highlights_ref::sources::tests::reserved_at_sign_off_medium_is_a_distinct_capture ... ok
test native::highlights_ref::sources::tests::twin_path_spelling_refuses_as_already_captured ... ok
test native::highlights_ref::stamp::tests::marker_return_links_key_orders_after_captured_and_round_trips ... ok
test native::highlights_ref::recapture::tests::partial_overlap_count_is_distinct_urls_not_families ... ok
test native::highlights_ref::tests::sidecar::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::recapture::tests::name_outside_the_family_refuses_with_expected_pattern ... ok
test native::highlights_ref::recapture::tests::one_url_into_a_collection_is_a_partial_overlap ... ok
test native::pomodoro_themes::agree_apply::tests::capture_unlink_drops_last_fix_type ... ok
test native::highlights_ref::recapture::tests::real_later_reading_rereads_beside_its_root ... ok
test native::note_tasks::tests::lightweight_capture_lookup_matches_full_index_task_rules ... ok
test native::highlights_ref::recapture::tests::natural_version_root_keeps_its_full_stem ... ok
test native::highlights_ref::tests::tasks::highlights_ref_capture_dates_follow_bob_clock ... ok
test native::highlights_ref::recapture::tests::queued_only_matches_stay_queued ... ok
test native::ref_library::tests::added_uses_captured_date_part_with_stamp_fallback ... ok
test native::task_move::tests::capture_move_refuses_destination_block_id_collisions ... ok
test native::task_status_hooks::tests::structure::capture_consumption_keeps_link_only_notes_as_clean_task_text ... ok
test native::task_status_hooks::tests::structure::capture_only_removes_pomodoros_emptied_by_this_consumption ... ok
test native::task_status_hooks_write::tests::planned_remove_requires_a_captured_present_file ... ok
test native::task_status_hooks_write::tests::unplanned_note_after_capture_invalidates_a_removal ... ok
test native::task_move::tests::capture_slots_place_moves_in_draft_order_and_report_exact_landings ... ok
test native::highlights_ref::recapture::tests::no_force_output_keeps_the_normal_family_refusal ... ok
test native::highlights_ref::recapture::tests::same_stem_across_types_stays_ambiguous ... ok
test native::capture_templates::store::tests::origin_cases_cover_same_missing_and_existing_target ... ok
test native::capture_templates::store::tests::eviction_drops_least_recently_used_and_lowered_cap_trims ... ok
test native::ref_jobs::fallback::tests::fallback_creates_missing_target_like_capture ... ok
test native::highlights_ref::recapture::tests::single_url_selects_a_family_of_one ... ok
test native::highlights_ref::recapture::tests::v2_v4_occupancy_yields_v5 ... ok
test native::highlights_ref::recapture::tests::unrelated_same_identity_families_are_ambiguous ... ok
test native::highlights_ref::tests::marker_write::restored_capture_is_held_at_execution_and_after_coordinated_save ... ok
test native::ref_library::tests::legacy_unread_is_superseded_by_the_pdf_capture ... ok
test native::capture_related::tests::synthetic_vault_query_is_under_250ms ... ok
test native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms ... ok

test result: ok. 2147 passed; 0 failed; 1 ignored; 0 measured; 5237 filtered out; finished in 5.20s


✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13/crates/bob-obsidian-assets)
    Checking bob-obsidian v0.5.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
warning: redundant field names in struct initialization
    --> src/native/bank/config_update/ops.rs:2350:13
     |
2350 |             op_index: op_index,
     |             ^^^^^^^^^^^^^^^^^^ help: replace it with: `op_index`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_field_names
     = note: `#[warn(clippy::redundant_field_names)]` on by default

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

warning: this function has too many arguments (9/7)
   --> src/native/albums/index.rs:115:1
    |
115 | / pub(crate) fn plan_index(
116 | |     path: &str,
117 | |     contents: Option<&str>,
118 | |     album_stem: &str,
...   |
124 | |     folder_complete: bool,
125 | | ) -> IndexPlan {
    | |______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: this boolean expression can be simplified
   --> src/native/albums/sync.rs:378:21
    |
378 | /                     !(is_record_path(&existing.path)
379 | |                         && !is_record_path(&edit.path)
380 | |                         || !is_record_path(&existing.path)
381 | |                             && is_record_path(&edit.path)),
    | |__________________________________________________________^ help: try: `(!is_record_path(&edit.path) || is_record_path(&existing.path)) && (is_record_path(&edit.path) || !is_record_path(&existing.path))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
    = note: `#[warn(clippy::nonminimal_bool)]` on by default

error: this `if` statement can be collapsed
   --> src/native/albums/sync.rs:466:5
    |
466 | /     if let Some(error) = snapshot.io_errors.first() {
467 | |         if !only_known_album_member_read_errors(&snapshot.io_errors, &registry)
468 | |         {
469 | |             return Err(error.clone());
470 | |         }
471 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
    = note: requested on the command line with `-D clippy::collapsible-if`
help: collapse nested if block
    |
466 ~     if let Some(error) = snapshot.io_errors.first()
467 ~         && !only_known_album_member_read_errors(&snapshot.io_errors, &registry)
468 |         {
469 |             return Err(error.clone());
470 ~         }
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:165:6
    |
165 | ) -> Result<OpOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:218:6
    |
218 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:294:6
    |
294 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:497:6
    |
497 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:797:6
    |
797 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1102:6
     |
1102 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1191:6
     |
1191 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1369:6
     |
1369 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/albums/update/ops.rs:1360:1
     |
1360 | / fn apply_choice_add(
1361 | |     field: &str,
1362 | |     label: &str,
1363 | |     emoji: Option<&str>,
...    |
1368 | |     inputs: &ApplyInputs<'_>,
1369 | | ) -> Result<OpResult, OpError> {
     | |______________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1481:6
     |
1481 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1623:6
     |
1623 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1708:6
     |
1708 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1808:6
     |
1808 | ) -> Result<(RecordType, Option<String>), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1852:6
     |
1852 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2299:6
     |
2299 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2387:6
     |
2387 | ) -> Result<String, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2409:6
     |
2409 | ) -> Result<bool, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2431:6
     |
2431 | ) -> Result<f64, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:240:6
    |
240 | ) -> Result<String, UpdateFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:257:20
    |
257 | fn read_stdin() -> Result<String, UpdateFailure> {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:271:6
    |
271 | ) -> Result<(VaultSnapshot, AlbumRegistry), UpdateFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:699:10
    |
699 |     ) -> Result<UpdatePlan, UpdatePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 208 bytes
    |
    = help: try reducing the size of `native::albums::update::plan::UpdatePlanError`, for example by boxing large elements or replacing it with `Box<native::albums::update::plan::UpdatePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: iterating on a map's keys
   --> src/native/areas/graph.rs:213:29
    |
213 |           let mut top_level = nodes
    |  _____________________________^
214 | |             .iter()
215 | |             .filter_map(|(path, _node)| {
216 | |                 (edges.get(path).and_then(|edge| edge.parent.as_ref())
217 | |                     == Some(root_path))
218 | |                 .then_some(path.clone())
219 | |             })
    | |______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#iter_kv_map
    = note: `#[warn(clippy::iter_kv_map)]` on by default
help: try
    |
213 ~         let mut top_level = nodes.keys().filter_map(|path| {
214 +                 (edges.get(path).and_then(|edge| edge.parent.as_ref())
215 +                     == Some(root_path))
216 +                 .then_some(path.clone())
217 +             })
    |

warning: this function has too many arguments (10/7)
   --> src/native/areas/graph.rs:281:1
    |
281 | / fn resolve_edge(
282 | |     current: &Path,
283 | |     header: &str,
284 | |     raw: &Option<String>,
...   |
291 | |     issues: &mut Vec<AreaIssue>,
292 | | ) -> ParentEdge {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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

warning: the `Err`-variant returned from this closure is very large
    --> src/native/bank/cli.rs:1135:13
     |
1135 |             || Ok(()),
     |             ^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/bank/cli.rs:1353:13
     |
1353 |             || Ok(()),
     |             ^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: used `expect()` on `Some` value
   --> src/native/bank/config.rs:408:22
    |
408 |         let config = config.expect("parsed bank config is present");
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
help: remove the `Some` and `expect()`
   --> src/native/bank/config.rs:399:18
    |
399 |       let config = Some(BankConfig {
    |  __________________^
400 | |         accounts,
401 | |         categories,
402 | |         rules,
...   |
405 | |         stale_after_line: line_by_path.get("bank.stale_after").copied(),
406 | |     });
    | |______^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_literal_unwrap
    = note: `#[warn(clippy::unnecessary_literal_unwrap)]` on by default

warning: the loop variable `index` is used to index `lines`
   --> src/native/bank/config_spans.rs:996:18
    |
996 |     for index in (key_line + 1)..stop_before.min(lines.len()) {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
    = note: `#[warn(clippy::needless_range_loop)]` on by default
help: consider using an iterator and enumerate()
    |
996 -     for index in (key_line + 1)..stop_before.min(lines.len()) {
996 +     for (index, <item>) in lines.iter().enumerate().take(stop_before.min(lines.len())).skip((key_line + 1)) {
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:237:6
    |
237 | ) -> Result<(String, Vec<OpResult>, Vec<InverseOp>), OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:265:6
    |
265 | ) -> Result<OneOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:458:6
    |
458 | ) -> Result<(), OpError> {
    |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:581:6
    |
581 | ) -> Result<OneOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:691:6
    |
691 | ) -> Result<String, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:790:6
    |
790 | ) -> Result<(), OpError> {
    |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:853:6
    |
853 | ) -> Result<Option<Anchor>, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:879:6
    |
879 | ) -> Result<(), OpError> {
    |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/ops.rs:909:6
    |
909 | ) -> Result<OneOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1081:6
     |
1081 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1163:6
     |
1163 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1247:6
     |
1247 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1311:6
     |
1311 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1340:6
     |
1340 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1404:6
     |
1404 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1559:6
     |
1559 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1589:6
     |
1589 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1669:6
     |
1669 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (10/7)
    --> src/native/bank/config_update/ops.rs:1658:1
     |
1658 | / fn set_account(
1659 | |     markdown: &str,
1660 | |     config: &BankConfig,
1661 | |     usage: &UsageIndex,
...    |
1668 | |     index: usize,
1669 | | ) -> Result<OneOutcome, OpError> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1805:6
     |
1805 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1844:6
     |
1844 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:1888:6
     |
1888 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2024:6
     |
2024 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2100:6
     |
2100 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/bank/config_update/ops.rs:2091:1
     |
2091 | / fn add_rule(
2092 | |     markdown: &str,
2093 | |     config: &BankConfig,
2094 | |     match_text: &str,
...    |
2099 | |     index: usize,
2100 | | ) -> Result<OneOutcome, OpError> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2167:6
     |
2167 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (10/7)
    --> src/native/bank/config_update/ops.rs:2156:1
     |
2156 | / fn set_rule(
2157 | |     markdown: &str,
2158 | |     config: &BankConfig,
2159 | |     index_in_rules: usize,
...    |
2166 | |     op_index: usize,
2167 | | ) -> Result<OneOutcome, OpError> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2285:6
     |
2285 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2343:6
     |
2343 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2381:6
     |
2381 | ) -> Result<&'a Rule, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2417:6
     |
2417 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2488:6
     |
2488 | ) -> Result<OneOutcome, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2529:32
     |
2529 | fn parse_ok(markdown: &str) -> Result<BankConfig, OpError> {
     |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/bank/config_update/ops.rs:2910:45
     |
2910 | pub(crate) fn parse_live(markdown: &str) -> Result<BankConfig, OpError> {
     |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
     |
     = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/bank/config_update/plan.rs:55:53
   |
55 | pub(crate) fn load_scan(vault: &std::path::Path) -> Result<BankScan, OpError> {
   |                                                     ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
   |
   = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/bank/config_update/plan.rs:76:6
   |
76 | ) -> Result<UpdatePlan, OpError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
   |
   = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/bank/config_update/protocol.rs:883:6
    |
883 |   ) -> Result<
    |  ______^
884 | |     (Option<String>, Option<String>, Option<char>, Option<bool>),
885 | |     ProtocolError,
886 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
    = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/bank/config_update/protocol.rs:1094:6
     |
1094 |   ) -> Result<
     |  ______^
1095 | |     (
1096 | |         Option<String>,
1097 | |         Option<String>,
...    |
1101 | |     ProtocolError,
1102 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/bank/config_update/protocol.rs:1307:6
     |
1307 |   ) -> Result<
     |  ______^
1308 | |     (
1309 | |         Option<String>,
1310 | |         Option<String>,
...    |
1314 | |     ProtocolError,
1315 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/run.rs:181:6
    |
181 | ) -> Result<String, UpdateFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 152 bytes
    |
    = help: try reducing the size of `native::bank::config_update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/run.rs:201:20
    |
201 | fn read_stdin() -> Result<String, UpdateFailure> {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 152 bytes
    |
    = help: try reducing the size of `native::bank::config_update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/bank/import_run.rs:330:6
    |
330 |   ) -> Result<
    |  ______^
331 | |     (
332 | |         BatchPlan,
333 | |         BankConfig,
...   |
340 | |     TxnFailure,
341 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the loop variable `index` is used to index `logical`
   --> src/native/bank/month.rs:321:18
    |
321 |     for index in day.heading_line..logical.len() {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
321 -     for index in day.heading_line..logical.len() {
321 +     for (index, <item>) in logical.iter().enumerate().skip(day.heading_line) {
    |

warning: this loop could be written as a `while let` loop
   --> src/native/bank/subscriptions/cadence.rs:96:5
    |
 96 | /     loop {
 97 | |         let Some(prev) = n.checked_sub(1) else {
 98 | |             break;
 99 | |         };
...   |
106 | |         n = prev;
107 | |     }
    | |_____^ help: try: `while let Some(prev) = n.checked_sub(1) { .. }`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#while_let_loop
    = note: `#[warn(clippy::while_let_loop)]` on by default

warning: casting to the same type is unnecessary (`i32` -> `i32`)
   --> src/native/bank/subscriptions/ledger.rs:452:45
    |
452 |         let Some(n) = current_n.checked_add(offset as i32 - 11) else {
    |                                             ^^^^^^^^^^^^^ help: try: `offset`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast
    = note: `#[warn(clippy::unnecessary_cast)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/bank/subscriptions/loader.rs:150:6
    |
150 | ) -> Result<Vec<(PathBuf, Option<Vec<u8>>)>, TxnFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/bank/subscriptions/loader.rs:287:6
    |
287 |   ) -> Result<
    |  ______^
288 | |     (
289 | |         Vec<RestaurantEntry>,
290 | |         Vec<ReadDep>,
...   |
294 | |     TxnFailure,
295 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/bank/subscriptions/loader.rs:400:6
    |
400 |   ) -> Result<
    |  ______^
401 | |     (
402 | |         SubscriptionRegistry,
403 | |         Vec<ReadDep>,
...   |
408 | |     TxnFailure,
409 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: `format!` in `format!` args
   --> src/native/bank/subscriptions_report.rs:600:19
    |
600 |       out.push_str(&format!(
    |  ___________________^
601 | |         "   {} a month · {}\n",
602 | |         format!("≈ {}", display_money(report.monthly_cents)),
603 | |         yearly
604 | |     ));
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:27:54
   |
27 |     pub(super) fn validate(&self, bob_dir: &Path) -> Result<(), CaptureError> {
   |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:85:10
   |
85 |     ) -> Result<(), CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:151:10
    |
151 |     ) -> Result<bool, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:159:10
    |
159 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:173:10
    |
173 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:188:10
    |
188 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:228:10
    |
228 |     ) -> Result<VaultSnapshot, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:275:10
    |
275 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:294:10
    |
294 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:438:10
    |
438 |     ) -> Result<usize, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:463:10
    |
463 |     ) -> Result<Vec<StagedTextFile>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:500:6
    |
500 | ) -> Result<Vec<usize>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:552:6
    |
552 | ) -> Result<CaptureWritePlan, CaptureError> {
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
   --> src/native/capture/blocked_tasks.rs:227:6
    |
227 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:254:6
    |
254 | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/blocked_tasks.rs:245:1
    |
245 | / pub(super) fn plan_blocked_task_writes(
246 | |     ctx: &mut DependencyContext,
247 | |     planner: &mut CaptureBatchPlanner,
248 | |     bob_dir: &Path,
...   |
253 | |     options: ExistingDependencyOptions,
254 | | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
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
   --> src/native/capture/budget.rs:333:6
    |
333 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:927:10
    |
927 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:969:22
    |
969 |                   .map(|values| {
    |  ______________________^
970 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
971 | |                 })
    | |_________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:970:32
    |
970 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
    |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:977:26
    |
977 |                       .map(|vals| {
    |  __________________________^
978 | |                         vals.map(|raw| {
979 | |                             super::move_choice::parse_move_in_picks(raw)
980 | |                         })
981 | |                         .collect::<Result<Vec<_>, _>>()
982 | |                     })
    | |_____________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:978:34
    |
978 |                           vals.map(|raw| {
    |  __________________________________^
979 | |                             super::move_choice::parse_move_in_picks(raw)
980 | |                         })
    | |_________________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:991:22
    |
991 |                 .map(|raw| parse_pull_in_picks(raw))
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1019:6
     |
1019 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1033:6
     |
1033 | ) -> Result<PullInPicks, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1069:6
     |
1069 | ) -> Result<InboxRoutePick, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1098:6
     |
1098 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1109:14
     |
1109 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1116:6
     |
1116 | ) -> Result<SubBulletTarget, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1129:6
     |
1129 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1178:6
     |
1178 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1209:6
     |
1209 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
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

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:60:6
   |
60 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
  --> src/native/capture/commit.rs:75:55
   |
75 |           write_staged_files_guarded(&batch.text_files, || {
   |  _______________________________________________________^
76 | |             batch.read_guards.validate(bob_dir)
77 | |         })
   | |_________^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:148:6
    |
148 | ) -> Result<Vec<PathBuf>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:193:6
    |
193 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:250:6
    |
250 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:251:39
    |
251 |     write_staged_files_guarded(files, || Ok(()))
    |                                       ^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:261:6
    |
261 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:308:35
    |
308 |         validate_reads().and_then(|()| validate_disk_preimages(files))
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:371:6
    |
371 | ) -> Result<Vec<PathBuf>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:465:6
    |
465 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:485:6
    |
485 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:512:6
    |
512 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:598:6
    |
598 | ) -> Result<PathBuf, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:667:45
    |
667 | pub(super) fn read_target(target: &Path) -> Result<String, CaptureError> {
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
    --> src/native/capture/dependencies.rs:1028:6
     |
1028 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1194:6
     |
1194 | ) -> Result<PathBuf, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1311:6
     |
1311 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1363:6
     |
1363 | ) -> Result<(String, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1474:6
     |
1474 | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:1465:1
     |
1465 | / fn resolve_prerequisites(
1466 | |     ctx: &DependencyContext,
1467 | |     planner: &mut CaptureBatchPlanner,
1468 | |     bob_dir: &Path,
...    |
1473 | |     dependent_desc: &str,
1474 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1564:10
     |
1564 |     ) -> Result<Self, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1807:24
     |
1807 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1896:6
     |
1896 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2037:6
     |
2037 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2058:6
     |
2058 | ) -> Result<Vec<TaskBlockRef>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2071:6
     |
2071 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2110:6
     |
2110 | ) -> Result<Vec<TargetTouch>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2210:6
     |
2210 | ) -> Result<Option<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2390:6
     |
2390 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2390:6
     |
2390 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2599:6
     |
2599 | ) -> Result<PlannedDependencyUpdate, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3101:6
     |
3101 | ) -> Result<(AugmentedNewTask, PlannedDependencyUpdateParts), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3359:6
     |
3359 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3417:6
     |
3417 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/event_conflict.rs:289:1
    |
289 | / pub(super) fn detect_event_conflict(
290 | |     contents: &str,
291 | |     date: NaiveDate,
292 | |     session_name: Option<&str>,
...   |
297 | |     fit: &FitKind,
298 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/event_conflict.rs:313:1
    |
313 | / pub(super) fn detect_event_conflict_with<V: CloseVault + ?Sized>(
314 | |     contents: &str,
315 | |     date: NaiveDate,
316 | |     session_name: Option<&str>,
...   |
323 | |     day_relative: Option<&Path>,
324 | | ) -> Option<EventConflictJson> {
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
   --> src/native/capture/meet_event_run.rs:568:6
    |
568 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/meet_event_run.rs:559:1
    |
559 | / pub(super) fn restamp_session_clock(
560 | |     planner: &mut CaptureBatchPlanner,
561 | |     bob_dir: &Path,
562 | |     day_file: &Path,
...   |
567 | |     warnings: &mut Vec<CaptureWarning>,
568 | | ) -> Result<(), CaptureError> {
    | |_____________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:591:6
    |
591 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:638:6
    |
638 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:657:6
    |
657 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:867:6
    |
867 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/merge_in.rs:37:6
   |
37 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/merge_in.rs:107:6
    |
107 | ) -> Result<MergeInExecution, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/merge_in.rs:191:6
    |
191 | ) -> Result<Vec<(lexer::TransferSource, PathBuf)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/merge_in.rs:195:14
    |
195 |           .map(|source| {
    |  ______________^
196 | |             let transfer_source = source_as_transfer(source);
197 | |             let path = transfer::resolve_transfer_note(snapshot, &source.route)
198 | |                 .map_err(|error| {
...   |
202 | |             Ok((transfer_source, path))
203 | |         })
    | |_________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/move_choice.rs:40:6
   |
40 | ) -> Result<MoveInPicks, super::output::CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/move_choice.rs:367:6
    |
367 | ) -> Result<Option<MoveChoiceSlot>, super::output::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/move_choice.rs:462:14
    |
462 |         .map(|off| super::plan::scheduled_date_string(today, off))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/move_choice.rs:951:6
    |
951 | ) -> Result<Vec<Option<char>>, super::output::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1162:6
     |
1162 | ) -> Result<MoveChoiceReport, super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1378:6
     |
1378 | ) -> Result<MoveChoiceReport, super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1560:6
     |
1560 | ) -> Result<(), super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/note_pull.rs:58:6
   |
58 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/notebook_create.rs:23:6
   |
23 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
  --> src/native/capture/notebook_create.rs:14:1
   |
14 | / pub(super) fn plan_notebook_create_item(
15 | |     request: &CaptureRequest,
16 | |     parsed_item: ParsedCaptureItem,
17 | |     now: chrono::NaiveDateTime,
...  |
22 | |     warnings: &mut Vec<CaptureWarning>,
23 | | ) -> Result<PlannedCaptureItem, CaptureError> {
   | |_____________________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/notebook_note.rs:161:6
    |
161 | ) -> Result<(usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/notebook_note.rs:391:6
    |
391 | ) -> Result<Option<capture_clip::ClipPlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/notebook_note.rs:456:6
    |
456 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/notebook_note.rs:564:6
    |
564 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/notebook_note.rs:788:6
    |
788 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (10/7)
   --> src/native/capture/notebook_note.rs:914:1
    |
914 | / pub(super) fn notebook_item_result(
915 | |     request: &CaptureRequest,
916 | |     route: &str,
917 | |     relative_str: &str,
...   |
924 | |     kind: &'static str,
925 | | ) -> crate::native::capture::output::CaptureItemResult {
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/offer_verdicts.rs:40:6
   |
40 | ) -> Result<Vec<String>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/offer_verdicts.rs:60:6
   |
60 | ) -> Result<Vec<(String, String)>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/offer_verdicts.rs:123:6
    |
123 | ) -> Result<Vec<OfferVerdictRequest>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/offer_verdicts.rs:301:6
    |
301 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/offer_verdicts.rs:313:6
    |
313 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:321:17
    |
321 |                 &[verdict.key.clone()],
    |                 ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs
    = note: `#[warn(clippy::cloned_ref_to_slice_refs)]` on by default

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:362:21
    |
362 |                     &[verdict.key.clone()],
    |                     ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/offer_verdicts.rs:377:6
    |
377 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/offer_verdicts.rs:461:6
    |
461 | ) -> Result<Vec<super::output::OfferCloseJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:502:17
    |
502 |                 &[verdict.key.clone()],
    |                 ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:512:17
    |
512 |                 &[verdict.key.clone()],
    |                 ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:568:29
    |
568 | ...                   &[verdict.key.clone()],
    |                       ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: the loop variable `position` is used to index `attributed`
   --> src/native/capture/offer_verdicts.rs:694:25
    |
694 |         for position in 0..verdicts.len() {
    |                         ^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
694 -         for position in 0..verdicts.len() {
694 +         for (position, <item>) in attributed.iter_mut().enumerate().take(verdicts.len()) {
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/capture/offer_verdicts.rs:755:17
    |
755 |                 &[verdict.key.clone()],
    |                 ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&verdict.key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

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

warning: this function has too many arguments (17/7)
   --> src/native/capture/output.rs:590:5
    |
590 | /     pub(super) fn from_items(
591 | |         items: Vec<CaptureItemResult>,
592 | |         global_destination: Option<GlobalDestinationSummary>,
593 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
607 | |         walk_files: Vec<WalkFileJson>,
608 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `to_string` applied to a type that implements `Display` in `print!` args
   --> src/native/capture/output.rs:681:22
    |
681 |                       )
    |  ______________________^
682 | |                     .to_string()
    | |________________________________^ help: remove this
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args
    = note: `#[warn(clippy::to_string_in_format_args)]` on by default

warning: `to_string` applied to a type that implements `Display` in `print!` args
   --> src/native/capture/output.rs:709:22
    |
709 |                       )
    |  ______________________^
710 | |                     .to_string()
    | |________________________________^ help: remove this
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: this function has too many arguments (8/7)
    --> src/native/capture/output.rs:7783:5
     |
7783 | /     pub(super) fn pull_in_choice_required(
7784 | |         extra: serde_json::Map<String, serde_json::Value>,
7785 | |         human_unblocked: Vec<TaskCompleteUnblockedJson>,
7786 | |         human_keep_moving_folds: Vec<
...    |
7795 | |         human_note_pull_groups: Vec<PullInGroupJson>,
7796 | |     ) -> Self {
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:158:6
    |
158 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:166:6
    |
166 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1545:6
     |
1545 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1639:6
     |
1639 | ) -> Result<FanoutClipboardRead, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1732:6
     |
1732 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1944:6
     |
1944 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2054:6
     |
2054 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (16/7)
    --> src/native/capture/plan.rs:2037:1
     |
2037 | / pub(super) fn plan_capture_item(
2038 | |     request: &CaptureRequest,
2039 | |     parsed_item: ParsedCaptureItem,
2040 | |     now: chrono::NaiveDateTime,
...    |
2053 | |     project_moves: &[ProjectMoveLanding],
2054 | | ) -> Result<PlannedCaptureItem, CaptureError> {
     | |_____________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:2827:14
     |
2827 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:3036:11
     |
3036 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4636:6
     |
4636 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4755:6
     |
4755 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4784:6
     |
4784 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4870:6
     |
4870 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4911:6
     |
4911 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5131:6
     |
5131 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:5593:13
     |
5593 |             &String::new(),
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
   --> src/native/capture/pomodoro_adjust.rs:507:6
    |
507 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:607:6
    |
607 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:652:6
    |
652 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:837:6
    |
837 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1336:6
     |
1336 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1372:6
     |
1372 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1536:6
     |
1536 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1713:6
     |
1713 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2026:6
     |
2026 | ) -> Result<Option<SizedCloseStaging>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2115:6
     |
2115 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2622:6
     |
2622 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2698:6
     |
2698 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2811:6
     |
2811 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:3408:6
     |
3408 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/pomodoro_link.rs:231:6
    |
231 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:287:6
    |
287 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:710:6
    |
710 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:807:6
    |
807 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:989:6
    |
989 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1034:6
     |
1034 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1830:6
     |
1830 | ) -> Result<&str, CaptureError> {
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
   --> src/native/capture/pomodoro_past.rs:102:6
    |
102 | ) -> Result<PastPreflight, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: manual `!RangeInclusive::contains` implementation
   --> src/native/capture/pomodoro_past.rs:186:24
    |
186 |         if t > 1440 || end > 1440 || end < 0 {
    |                        ^^^^^^^^^^^^^^^^^^^^^ help: use: `!(0..=1440).contains(&end)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains
    = note: `#[warn(clippy::manual_range_contains)]` on by default

warning: this function has too many arguments (11/7)
   --> src/native/capture/pomodoro_past.rs:211:1
    |
211 | / fn make_member_window(
212 | |     idx: usize,
213 | |     spec: &PomodoroPastSpec,
214 | |     blocks: u32,
...   |
222 | |     now_min: i64,
223 | | ) -> MemberWindow {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:552:6
    |
552 | ) -> Result<PastPreflight, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:784:6
    |
784 | ) -> Result<Vec<TrimPlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1072:6
     |
1072 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1105:6
     |
1105 | ) -> Result<(usize, String, PastTargetSource, Option<String>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1241:6
     |
1241 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1285:6
     |
1285 | ) -> Result<(String, usize, usize, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the variable `idx` is used as a loop counter
    --> src/native/capture/pomodoro_past.rs:1333:5
     |
1333 |     for line in &block_lines {
     |     ^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (idx, line) in (insert_at..).zip(block_lines.iter())`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
     = note: `#[warn(clippy::explicit_counter_loop)]` on by default

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1385:6
     |
1385 | ) -> Result<super::plan::PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

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
  --> src/native/capture/pomodoro_start.rs:19:6
   |
19 | ) -> Result<(String, String, u64, String), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:103:6
    |
103 |   ) -> Result<
    |  ______^
104 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
105 | |     CaptureError,
106 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:156:6
    |
156 |   ) -> Result<
    |  ______^
157 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
158 | |     CaptureError,
159 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:481:6
    |
481 |   ) -> Result<
    |  ______^
482 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
483 | |     CaptureError,
484 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:576:6
    |
576 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:628:6
    |
628 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:687:6
    |
687 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:706:6
    |
706 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:864:6
    |
864 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:876:6
    |
876 | ) -> Result<(String, Placement, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:921:6
    |
921 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:947:6
    |
947 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1252:6
     |
1252 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1517:6
     |
1517 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2169:6
     |
2169 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2272:6
     |
2272 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2337:6
     |
2337 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2507:6
     |
2507 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/project_deps.rs:537:6
    |
537 | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/project_deps.rs:528:1
    |
528 | / pub(super) fn restamp_retyped_timed_entries(
529 | |     planner: &mut CaptureBatchPlanner,
530 | |     bob_dir: &Path,
531 | |     day_file: &Path,
...   |
536 | |     warnings: &mut Vec<CaptureWarning>,
537 | | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    | |________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:561:6
    |
561 | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/project_deps.rs:551:1
    |
551 | / fn restamp_changed_or_retyped_timed_entries(
552 | |     planner: &mut CaptureBatchPlanner,
553 | |     bob_dir: &Path,
554 | |     day_file: &Path,
...   |
560 | |     include_renamed_or_moved: bool,
561 | | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    | |________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:20:6
   |
20 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:38:6
   |
38 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:78:6
   |
78 | ) -> Result<Option<ProjectNoteParentCatalogJson>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_note.rs:141:6
    |
141 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/project_note.rs:216:14
    |
216 |         .map(|offset| scheduled_date_string(today, offset))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2256:6
     |
2256 | ) -> Result<Vec<ResolvedProjectMove>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2421:6
     |
2421 | ) -> Result<ProjectMoveExecution, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/project_note.rs:2433:14
     |
2433 |           .map(|movement| {
     |  ______________^
2434 | |             slot_by_source.get(&movement.source_index).copied().ok_or_else(
2435 | |                 || {
2436 | |                     CaptureError::io(
...    |
2441 | |         })
     | |_________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3040:6
     |
3040 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
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
  --> src/native/capture/pull_in.rs:96:6
   |
96 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:382:6
    |
382 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/record_note.rs:28:6
   |
28 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/record_note.rs:61:6
   |
61 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: unneeded late initialization
  --> src/native/capture/record_note.rs:79:5
   |
79 |       let synthetic;
   |       ^^^^^^^^^^^^^^ created here
80 | /     synthetic = records::RecordsConfig {
81 | |         types: vec![record_type.clone()],
82 | |     };
   | |_____^ initialised here
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_late_init
   = note: `#[warn(clippy::needless_late_init)]` on by default
help: move the declaration `synthetic` here
   |
79 ~     
80 ~     let synthetic = records::RecordsConfig {
   |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/record_note.rs:196:6
    |
196 | ) -> Result<Vec<super::output::WalkFileJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/record_note.rs:347:6
    |
347 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/record_note.rs:574:6
    |
574 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/relations_close.rs:233:6
    |
233 | ) -> Result<ItemRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations_close.rs:224:1
    |
224 | / pub(super) fn plan_item_relations(
225 | |     ctx: &mut DependencyContext,
226 | |     planner: &mut CaptureBatchPlanner,
227 | |     request: &CaptureRequest,
...   |
232 | |     warnings: &mut Vec<CaptureWarning>,
233 | | ) -> Result<ItemRelationReports, CaptureError> {
    | |______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:271:6
    |
271 | ) -> Result<RelationCloseReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:470:6
    |
470 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this boolean expression can be simplified
   --> src/native/capture/relations_close.rs:494:14
    |
494 |         if !(cancel && complete || cancel && merge || complete && merge) {
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
494 -         if !(cancel && complete || cancel && merge || complete && merge) {
494 +         if !(!(!cancel || !complete && !merge) || complete && merge) {
    |
494 -         if !(cancel && complete || cancel && merge || complete && merge) {
494 +         if !((merge || complete) && cancel || complete && merge) {
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
  --> src/native/capture/relations_merge.rs:45:6
   |
45 | ) -> Result<RelationMergeReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:253:6
    |
253 | ) -> Result<TaskLocator, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:293:6
    |
293 | ) -> Result<VaultSnapshot, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:544:6
    |
544 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/sections.rs:579:6
    |
579 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
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
   --> src/native/capture/task_complete.rs:175:6
    |
175 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:924:6
    |
924 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1191:6
     |
1191 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:163:10
    |
163 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:205:10
    |
205 |     ) -> Result<AppliedTaskTheme, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:311:10
    |
311 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:328:10
    |
328 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:361:10
    |
361 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:502:10
    |
502 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:626:10
    |
626 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:671:10
    |
671 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:818:10
    |
818 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/task_theme.rs:809:5
    |
809 | /     fn apply_theme_change(
810 | |         &self,
811 | |         planner: &mut CaptureBatchPlanner,
812 | |         target: &Path,
...   |
817 | |         started: bool,
818 | |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    | |_____________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:865:10
    |
865 |     ) -> Result<Option<super::meet_event_run::MeetFinish>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture/task_theme.rs:880:27
    |
880 |           let Some(entry) = scan
    |  ___________________________^
881 | |             .entries
882 | |             .iter()
883 | |             .filter(|entry| entry.line <= link_one_based)
884 | |             .last()
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
884 -             .last()
884 +             .next_back()
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:917:10
    |
917 |     ) -> Result<Option<usize>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:974:10
    |
974 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1224:10
     |
1224 |     ) -> Result<Option<AppliedMerge>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1289:10
     |
1289 |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
    --> src/native/capture/task_theme.rs:1279:5
     |
1279 | /     pub(super) fn relocate_for_retype(
1280 | |         &mut self,
1281 | |         planner: &mut CaptureBatchPlanner,
1282 | |         task_path: &Path,
...    |
1288 | |         warnings: &mut Vec<CaptureWarning>,
1289 | |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
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
  --> src/native/capture/transfer.rs:67:6
   |
67 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:649:6
    |
649 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:675:6
    |
675 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:740:6
    |
740 |   ) -> Result<
    |  ______^
741 | |     (
742 | |         RelationMergeOutput,
743 | |         Vec<crate::native::task_move::transplant::RepairedFile>,
744 | |     ),
745 | |     CaptureError,
746 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:213:6
    |
213 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:411:44
    |
411 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
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

warning: this function has too many arguments (8/7)
   --> src/native/capture_clip/clipboard.rs:374:1
    |
374 | / pub(super) fn read_agreed_history<R, N, S, P>(
375 | |     current: String,
376 | |     candidates: &[HistoryProvider],
377 | |     source: &SelectionSource,
...   |
390 | |     S: FnMut(Duration),
391 | |     P: FnMut(&HistoryProvider) -> Option<bool>,
    | |_______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/capture_complete/candidates.rs:2060:1
     |
2060 | / fn relationship_disabled_reason(
2061 | |     bob_dir: &Path,
2062 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
2063 | |     graph: &HashMap<
...    |
2072 | |     blocked_tasks: &[ResolvedRelationshipEntry],
2073 | | ) -> Option<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:2694:6
     |
2694 |   ) -> (
     |  ______^
2695 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
2696 | |     Vec<String>,
2697 | |     Vec<(String, usize)>,
2698 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/capture_complete/records.rs:1208:9
     |
1208 |         &[spelling.clone()],
     |         ^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&spelling)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

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
    --> src/native/capture_drawers.rs:1557:5
     |
1557 | /     direct_child_list_indexes(&lines, drawer.line_index(), drawer.block_end)
1558 | |         .into_iter()
1559 | |         .filter(|&index| line_start(&lines, index) < insertion.offset)
1560 | |         .filter(|&index| {
1561 | |             parse_managed_task_log_marker(lines[index].text).is_none()
1562 | |         })
1563 | |         .next_back()
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_next
     = note: `#[warn(clippy::filter_next)]` on by default

warning: redundant guard
   --> src/native/capture_language/close_log.rs:222:23
    |
222 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
    = note: `#[warn(clippy::redundant_guards)]` on by default
help: try
    |
222 -         Some(list) if list.is_empty() => {
222 +         Some([]) => {
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/close_log.rs:544:1
    |
544 | / fn check_index_loggable(
545 | |     index: u32,
546 | |     index_range: (usize, usize),
547 | |     close_token: &str,
...   |
553 | |     complete_all: bool,
554 | | ) -> Result<(), CloseLogError> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:713:1
    |
713 | / pub(crate) fn lex_close_inline_entry_with_all(
714 | |     entry_tokens: &[Token<'_>],
715 | |     close_token: &str,
716 | |     in_progress: Option<&[u32]>,
...   |
721 | |     complete_all: bool,
722 | | ) -> Result<CloseInlineLex, CloseLogError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:955:1
    |
955 | / pub(crate) fn lex_close_log_bullets_with_all(
956 | |     child_lines: &[ItemLine<'_>],
957 | |     close_token: &str,
958 | |     in_progress: Option<&[u32]>,
...   |
963 | |     complete_all: bool,
964 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: casting to the same type is unnecessary (`usize` -> `usize`)
    --> src/native/capture_language/completion.rs:1304:19
     |
1304 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast

warning: the following explicit lifetimes could be elided: 'i
    --> src/native/capture_language/completion.rs:1676:29
     |
1676 | fn merge_in_completion_slot<'i, 's>(
     |                             ^^
1677 |     item: &'i CaptureItem<'s>,
     |            ^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
     |
1676 ~ fn merge_in_completion_slot<'s>(
1677 ~     item: &CaptureItem<'s>,
     |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:2141:22
     |
2141 |       let mut targets: Vec<(
     |  ______________________^
2142 | |         String,
2143 | |         String,
2144 | |         &'static str,
2145 | |         Option<(usize, usize)>,
2146 | |     )> = Vec::new();
     | |______^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:2412:6
     |
2412 |   ) -> Result<
     |  ______^
2413 | |     Vec<(
2414 | |         ParsedCaptureText,
2415 | |         Option<RefParentSource>,
...    |
2418 | |     TemplateCodedError,
2419 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:384:12
    |
384 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
384 -     spans: &mut Vec<Span>,
384 +     spans: &mut [Span],
    |

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:442:12
    |
442 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
442 -     spans: &mut Vec<Span>,
442 +     spans: &mut [Span],
    |

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:870:1
    |
870 | / pub(super) enum TokenParse {
871 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 520 bytes
872 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 136 bytes
873 | | }
    | |_^ the entire enum is at least 520 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
871 -     Marker(MarkerParse),
871 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:2707:1
     |
2707 | / fn empty_editor_item(
2708 | |     item: &CaptureItem<'_>,
2709 | |     mode: EditorMode,
2710 | |     route: Option<String>,
...    |
2715 | |     diagnostics: Vec<Diagnostic>,
2716 | | ) -> EditorItemParse {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:3565:1
     |
3565 | / fn attach_drawer_bullet_metadata(
3566 | |     item: &CaptureItem<'_>,
3567 | |     mode: &mut EditorMode,
3568 | |     parent_body: &str,
...    |
3573 | |     sub_bullets: &mut [AuthoredSubBullet],
3574 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:4168:35
     |
4168 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `#[warn(clippy::trim_split_whitespace)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:4849:5
     |
4849 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:4848:5
     |
4848 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:302:1
    |
302 | / pub(super) fn parse_editor_named_start_item<'a>(
303 | |     item: &CaptureItem<'a>,
304 | |     parent_trimmed: &str,
305 | |     suffix: String,
...   |
311 | |     spelling: NameSpelling,
312 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_pomodoro.rs:3322:1
     |
3322 | / fn editor_past_outcome<'a>(
3323 | |     item: &CaptureItem<'a>,
3324 | |     parent_trimmed: &str,
3325 | |     mode: EditorMode,
...    |
3330 | |     diagnostics: Vec<Diagnostic>,
3331 | | ) -> EditorItemOutcome<'a> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:125:6
    |
125 |   ) -> Option<
    |  ______^
126 | |     Result<
127 | |         (
128 | |             LineOutcome<'a>,
...   |
133 | |     >,
134 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:218:6
    |
218 |   ) -> Option<
    |  ______^
219 | |     Result<
220 | |         (
221 | |             LineOutcome<'a>,
...   |
226 | |     >,
227 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:1439:5
     |
1439 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1438:5
     |
1438 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/item.rs:1326:35
     |
1326 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:2145:1
     |
2145 | / fn parse_capture_item_masked<'a>(
2146 | |     item: &CaptureItem<'a>,
2147 | |     forced_route: Option<&str>,
2148 | |     forced_section: Option<&str>,
...    |
2153 | |     target_run: Option<&TargetRunContext>,
2154 | | ) -> Result<ParsedCaptureItemOutcome<'a>, String> {
     | |_________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:2488:5
     |
2488 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:2487:5
     |
2487 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:4868:1
     |
4868 | / pub(super) fn named_shape_error_with_drop(
4869 | |     token: &str,
4870 | |     suffix: &str,
4871 | |     name: &str,
...    |
4876 | |     is_literal: bool,
4877 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: stripping a prefix manually
    --> src/native/capture_language/notebook.rs:1057:63
     |
1057 |         let parsed = super::tokens::parse_hash_section_and_id(&suffix[1..]);
     |                                                               ^^^^^^^^^^^^
     |
note: the prefix was tested here
    --> src/native/capture_language/notebook.rs:1056:5
     |
1056 |     if suffix.starts_with('#') {
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
     = note: `#[warn(clippy::manual_strip)]` on by default
help: try using the `strip_prefix` method
     |
1056 ~     if let Some(<stripped>) = suffix.strip_prefix('#') {
1057 ~         let parsed = super::tokens::parse_hash_section_and_id(<stripped>);
     |

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_language/notebook.rs:1424:6
     |
 989 |     Supported(RouteMarker),
     |     ---------------------- the largest variant contains at least 160 bytes
...
1424 | ) -> Result<Option<NotebookRouteInfo>, RouteScan> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_language::notebook::RouteScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::notebook::RouteScan>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_language/notebook.rs:1446:6
     |
 989 |     Supported(RouteMarker),
     |     ---------------------- the largest variant contains at least 160 bytes
...
1446 | ) -> Result<Option<NotebookClaim>, RouteScan> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_language::notebook::RouteScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::notebook::RouteScan>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_language/past.rs:424:6
    |
137 |     Valid(PastEValid),
    |     ----------------- the largest variant contains at least 144 bytes
...
424 | ) -> Result<PastName, PastEOutcome> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_language::past::PastEOutcome`, for example by boxing large elements or replacing it with `Box<native::capture_language::past::PastEOutcome>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `idx` is used to index `members`
    --> src/native/capture_language/past.rs:1233:16
     |
1233 |     for idx in start..=end {
     |                ^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1233 -     for idx in start..=end {
1233 +     for (idx, <item>) in members.iter().enumerate().take(end + 1).skip(start) {
     |

warning: large size difference between variants
  --> src/native/capture_language/record.rs:85:1
   |
85 | /   pub(crate) enum PerRouteDecision {
86 | | /     AlbumValid {
87 | | |         record_type: RecordType,
88 | | |         album: AlbumRouteMeta,
89 | | |     },
   | | |_____- the largest variant contains at least 272 bytes
90 | | /     AlbumInvalid {
91 | | |         paths: Vec<String>,
92 | | |         findings: Vec<AlbumFinding>,
93 | | |     },
   | | |_____- the second-largest variant contains at least 48 bytes
...  |
97 | |       },
98 | |   }
   | |___^ the entire enum is at least 272 bytes
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
   |
87 -         record_type: RecordType,
87 +         record_type: Box<RecordType>,
   |

warning: large size difference between variants
   --> src/native/capture_language/record.rs:669:1
    |
669 | / enum RouteResolution {
670 | |     /// A configured folder: claim creation.
671 | |     Configured,
    | |     ---------- the second-largest variant carries no data at all
672 | |     /// A teaching refusal (type id or existing
673 | |     /// non-record folder).
674 | |     Refused(RecordClaim),
    | |     -------------------- the largest variant contains at least 216 bytes
675 | |     /// An unknown folder: stay literal task text.
676 | |     Literal,
677 | | }
    | |_^ the entire enum is at least 216 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
674 -     Refused(RecordClaim),
674 +     Refused(Box<RecordClaim>),
    |

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
    --> src/native/capture_language/rewrite.rs:2312:8
     |
2312 |       if !raw_text[..run_start]
     |  ________^
2313 | |         .chars()
2314 | |         .next_back()
2315 | |         .is_some_and(|before| !before.is_whitespace())
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
2312 ~     if raw_text[..run_start]
2313 +         .chars()
2314 +         .next_back().is_none_or(|before| before.is_whitespace())
     |

warning: this function has too many arguments (9/7)
    --> src/native/capture_language/rewrite.rs:2527:1
     |
2527 | / fn candidate_selects_plain_marker(
2528 | |     candidate: &str,
2529 | |     start: usize,
2530 | |     end: usize,
...    |
2536 | |     id_part: &str,
2537 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` has identical blocks
   --> src/native/capture_language/target_runs.rs:458:51
    |
458 |           } else if is_escaped_priority_token(text) {
    |  ___________________________________________________^
459 | |             break;
460 | |         } else {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/target_runs.rs:460:16
    |
460 |           } else {
    |  ________________^
461 | |             break;
462 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else
    = note: `#[warn(clippy::if_same_then_else)]` on by default

warning: stripping a prefix manually
   --> src/native/capture_language/task_sources.rs:119:20
    |
119 |         let rest = &text[1..];
    |                    ^^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_language/task_sources.rs:118:5
    |
118 |     if text.starts_with('@') {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_prefix` method
    |
118 ~     if let Some(rest) = text.strip_prefix('@') {
119 ~         if let Some(plus) = rest.find('+') {
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_language/transfer.rs:467:6
    |
107 | /     Valid {
108 | |         sources: Vec<TransferSource>,
109 | |         arrow: TransferArrow,
110 | |         destination: TransferDestination,
111 | |     },
    | |_____- the largest variant contains at least 184 bytes
...
467 |   ) -> Result<TransferSource, TransferScan> {
    |        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_language::transfer::TransferScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::transfer::TransferScan>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: redundant pattern matching, consider using `is_ok()`
   --> src/native/capture_language/transfer.rs:797:5
    |
797 |     matches!(parse_destination_token(&token), Ok(_))
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `parse_destination_token(&token).is_ok()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_pattern_matching
    = note: `#[warn(clippy::redundant_pattern_matching)]` on by default

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

warning: this function has too many arguments (8/7)
    --> src/native/capture_parse.rs:2930:1
     |
2930 | / fn refusal_diagnostic(
2931 | |     spans: &[Span],
2932 | |     mode: EditorMode,
2933 | |     pomodoro_start: &Option<PomodoroStartSpec>,
...    |
2938 | |     source: &str,
2939 | | ) -> Option<Diagnostic> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_pomodoro_close/ledger.rs:808:24
    |
808 |       let Some(anchor) = scan
    |  ________________________^
809 | |         .entries
810 | |         .iter()
811 | |         .filter(|entry| {
...   |
814 | |         })
815 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
815 -         .last()
815 +         .next_back()
    |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:155:1
    |
155 | / pub(crate) enum PomodoroCloseOutcome {
156 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 688 bytes
157 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
158 | | }
    | |_^ the entire enum is at least 688 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
156 -     Close(PomodoroClosePlan),
156 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:319:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
319 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:366:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
366 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:554:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
554 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:571:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
571 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:591:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
591 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:614:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
614 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:677:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
677 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:750:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
750 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:904:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
904 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:982:6
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
982 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1007:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1007 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1036:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1036 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1027:1
     |
1027 | / pub(crate) fn plan_pomodoro_close_for_entry<V: CloseVault>(
1028 | |     day_path: &Path,
1029 | |     day_contents: &str,
1030 | |     entry: &RunningPomodoro,
...    |
1035 | |     policy: LedgerClosePolicy,
1036 | | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1324:1
     |
1324 | / fn resolve_close_clock_fact<V: CloseVault, S: HomeSource>(
1325 | |     vault: &V,
1326 | |     resolver: &mut HomeResolver<S>,
1327 | |     events: &[EventNoteRow],
...    |
1333 | |     all_settings: &NoteTaskSettings,
1334 | | ) -> CloseClockFact {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1739:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1739 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture_pomodoro_start.rs:409:1
    |
409 | / fn resolve_clock_fact<V: CloseVault + ?Sized, S: HomeSource>(
410 | |     vault: Option<&V>,
411 | |     resolver: Option<&mut HomeResolver<S>>,
412 | |     events: &[EventNoteRow],
...   |
417 | |     all_settings: &note_tasks::NoteTaskSettings,
418 | | ) -> CountedLinkFact {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: unneeded late initialization
   --> src/native/capture_record.rs:405:9
    |
405 |           let synthetic;
    |           ^^^^^^^^^^^^^^ created here
406 | /         synthetic = records::RecordsConfig {
407 | |             types: vec![record_type.clone()],
408 | |         };
    | |_________^ initialised here
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_late_init
help: move the declaration `synthetic` here
    |
405 ~         
406 ~         let synthetic = records::RecordsConfig {
    |

warning: this function has too many arguments (13/7)
   --> src/native/capture_related/corpus.rs:170:1
    |
170 | / fn collect_from_note(
171 | |     _bob_dir: &Path,
172 | |     relative: &str,
173 | |     absolute: &Path,
...   |
183 | |     _warnings: &mut Vec<String>,
184 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/corpus.rs:263:1
    |
263 | / fn collect_from_archives(
264 | |     bob_dir: &Path,
265 | |     settings: &note_tasks::NoteTaskSettings,
266 | |     today: NaiveDate,
...   |
271 | |     warnings: &mut Vec<String>,
272 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:498:1
    |
498 | / fn draft_match(
499 | |     ranked: bands::RankedMatch<'_>,
500 | |     item: &EditorItemParse,
501 | |     draft: &str,
...   |
506 | |     index: &NoteIndex,
507 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:635:1
    |
635 | / fn verify_link_action(
636 | |     action: &str,
637 | |     item: &EditorItemParse,
638 | |     draft: &str,
...   |
643 | |     options: &EditorParseOptions<'_>,
644 | | ) -> bool {
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

warning: manual implementation of `Option::map`
   --> src/native/capture_rewrite.rs:448:28
    |
448 |           let record_store = match cursor.and_then(|position| {
    |  ____________________________^
449 | |             capture_language::slash_route_may_need_album_policy(
450 | |                 &input, position,
...   |
459 | |             None => None,
460 | |         };
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
    = note: `#[warn(clippy::manual_map)]` on by default
help: try
    |
448 ~         let record_store = cursor.and_then(|position| {
449 +             capture_language::slash_route_may_need_album_policy(
450 +                 &input, position,
451 +             )
452 +         }).map(|route| super::capture_record::record_policy_for_draft(
453 +                     &bob_env::bob_dir(),
454 +                     &format!("@{route}/"),
455 ~                 ));
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

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/link_repair.rs:873:6
    |
873 | ) -> io::Result<Option<(String, BTreeSet<String>, BTreeSet<String>)>> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:615:10
    |
615 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:627:10
    |
627 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:644:10
    |
644 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1202:21
     |
1202 |                     &[archive.clone()],
     |                     ^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(archive)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1230:21
     |
1230 |                     &[source.clone()],
     |                     ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(source)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1252:21
     |
1252 |                     &[archive.clone()],
     |                     ^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(archive)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1268:21
     |
1268 |                     &[source.clone()],
     |                     ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(source)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this function has too many arguments (8/7)
    --> src/native/gcal/ack.rs:1076:1
     |
1076 | / fn select_candidate(
1077 | |     args: &AckArgs,
1078 | |     config: &GcalConfig,
1079 | |     vault: &Path,
...    |
1084 | |     warnings: &mut Vec<String>,
1085 | | ) -> Result<NoteCandidate, GcalError> {
     | |_____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/gcal/ack.rs:1381:1
     |
1381 | / fn print_selected_result(
1382 | |     args: &AckArgs,
1383 | |     config: &GcalConfig,
1384 | |     candidate: &NoteCandidate,
...    |
1389 | |     warnings: &[String],
1390 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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
    = note: `#[warn(clippy::match_like_matches_macro)]` on by default
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
   = note: `#[warn(clippy::wrong_self_convention)]` on by default

warning: this function has too many arguments (8/7)
   --> src/native/gcal/note/write.rs:93:1
    |
 93 | / pub(super) fn write_one<S: HomeSource>(
 94 | |     args: &NoteArgs,
 95 | |     config: &GcalConfig,
 96 | |     vault: &std::path::Path,
...   |
101 | |     related_days: Vec<NaiveDate>,
102 | | ) -> Result<WriteOutcome, GcalError> {
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/gcal/note/write.rs:361:1
    |
361 | / pub(crate) fn save_session_note<S: HomeSource>(
362 | |     candidate: &NoteCandidate,
363 | |     vault: &std::path::Path,
364 | |     config: &GcalConfig,
...   |
369 | |     related_days: &[chrono::NaiveDate],
370 | | ) -> Result<SessionNoteSave, GcalError> {
    | |_______________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/gcal/note/write.rs:656:1
    |
656 | / pub(crate) fn rebuild_candidate<S: HomeSource>(
657 | |     original: &NoteCandidate,
658 | |     config: &GcalConfig,
659 | |     vault: &std::path::Path,
...   |
664 | |     replacement: Option<&str>,
665 | | ) -> Result<NoteCandidate, GcalError> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the loop variable `index` is used to index `tokens`
    --> src/native/gcal/note/write.rs:1253:22
     |
1253 |         for index in cursor..tokens.len() {
     |                      ^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1253 -         for index in cursor..tokens.len() {
1253 +         for (index, <item>) in tokens.iter().enumerate().skip(cursor) {
     |

warning: `format!` in `format!` args
    --> src/native/gcal/note/write.rs:1353:17
     |
1353 | /                 format!(
1354 | |                     "{} and {} set different {} buffer values",
1355 | |                     format!("{}{}", side.sign(), previous.minutes),
1356 | |                     format!("{}{}", side.sign(), minutes),
1357 | |                     side.name()
1358 | |                 ),
     | |_________________^
     |
     = help: combine the `format!(..)` arguments with the outer `format!(..)` call
     = help: or consider changing `format!` to `format_args!`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: this function has too many arguments (13/7)
    --> src/native/gcal/note/write.rs:1652:1
     |
1652 | / fn print_result(
1653 | |     args: &NoteArgs,
1654 | |     candidate: &NoteCandidate,
1655 | |     scope: NoteScope,
...    |
1665 | |     newly_acked: bool,
1666 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/gcal/note.rs:589:1
    |
589 | / pub(crate) fn fetch_candidates<S: HomeSource>(
590 | |     config: &GcalConfig,
591 | |     vault: &std::path::Path,
592 | |     resolver: &mut HomeResolver<S>,
...   |
598 | |     day_filter: Option<NaiveDate>,
599 | | ) -> Result<(Vec<NoteCandidate>, Vec<String>), GcalError> {
    | |_________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/gcal/note.rs:804:1
    |
804 | / pub(crate) fn lookup_exact<S: HomeSource>(
805 | |     config: &GcalConfig,
806 | |     vault: &std::path::Path,
807 | |     resolver: &mut HomeResolver<S>,
...   |
812 | |     pinned: Option<&str>,
813 | | ) -> Result<(Option<NoteCandidate>, Vec<String>), GcalError> {
    | |____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this expression can be written more simply using `.retain()`
    --> src/native/gcal/note.rs:1077:9
     |
1077 | /         listed = listed
1078 | |             .into_iter()
1079 | |             .filter(|candidate| {
1080 | |                 matches_query(&candidate.event.title, &args.query)
1081 | |             })
1082 | |             .collect();
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_retain
     = note: `#[warn(clippy::manual_retain)]` on by default
help: consider calling `.retain()` instead
     |
1077 ~         listed.retain(|candidate| {
1078 +                 matches_query(&candidate.event.title, &args.query)
1079 ~             });
     |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/gcal/note.rs:1117:6
     |
1117 | ) -> Result<(Vec<NoteCandidate>, Vec<Orphan>, Vec<String>), GcalError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/gcal/note.rs:1108:1
     |
1108 | / fn lookup_orphans<S: HomeSource>(
1109 | |     _config: &GcalConfig,
1110 | |     vault: &std::path::Path,
1111 | |     _resolver: &mut HomeResolver<S>,
...    |
1116 | |     _day_filter: Option<NaiveDate>,
1117 | | ) -> Result<(Vec<NoteCandidate>, Vec<Orphan>, Vec<String>), GcalError> {
     | |______________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/gcal/note.rs:1400:1
     |
1400 | / fn run_show<S: HomeSource>(
1401 | |     args: &NoteArgs,
1402 | |     config: &GcalConfig,
1403 | |     vault: &std::path::Path,
...    |
1408 | |     url_event: Option<String>,
1409 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/gcal/note.rs:1525:1
     |
1525 | / fn clear_live_series_by_master<S: HomeSource>(
1526 | |     args: &NoteArgs,
1527 | |     config: &GcalConfig,
1528 | |     vault: &std::path::Path,
...    |
1535 | |     day_filter: Option<NaiveDate>,
1536 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/gcal/note.rs:1870:1
     |
1870 | / fn show_from_query<S: HomeSource>(
1871 | |     args: &NoteArgs,
1872 | |     config: &GcalConfig,
1873 | |     vault: &std::path::Path,
...    |
1878 | |     day_filter: Option<NaiveDate>,
1879 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/gcal/note.rs:2231:1
     |
2231 | / fn present_candidate<S: HomeSource>(
2232 | |     args: &NoteArgs,
2233 | |     config: &GcalConfig,
2234 | |     vault: &std::path::Path,
...    |
2239 | |     related_days: Vec<NaiveDate>,
2240 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/gcal/note.rs:2749:1
     |
2749 | / fn print_list_json(
2750 | |     all: bool,
2751 | |     window_from: &NaiveDate,
2752 | |     window_to: &NaiveDate,
...    |
2757 | |     warnings: &[String],
2758 | | ) -> Result<(), GcalError> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
    --> src/native/gcal/note.rs:2825:15
     |
2825 |     warnings: &mut Vec<String>,
     |               ^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
2825 -     warnings: &mut Vec<String>,
2825 +     warnings: &mut [String],
     |

warning: this `if` has identical blocks
   --> src/native/gcal/description.rs:509:45
    |
509 |       let first_ok = if first.is_alphabetic() {
    |  _____________________________________________^
510 | |         true
511 | |     } else if !first.is_ascii()
    | |_____^
    |
note: same as this
   --> src/native/gcal/description.rs:513:5
    |
513 | /     {
514 | |         true
515 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: this if-then-else expression returns a bool literal
   --> src/native/gcal/description.rs:511:12
    |
511 |       } else if !first.is_ascii()
    |  ____________^
512 | |         && !matches!(first, '\u{2010}'..='\u{2015}' | '\u{2212}')
513 | |     {
514 | |         true
515 | |     } else {
516 | |         false
517 | |     };
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
   --> src/native/gcal/journal.rs:637:6
    |
637 |   ) -> std::io::Result<(
    |  ______^
638 | |     BTreeMap<(String, String), OccurrenceState>,
639 | |     Vec<String>,
640 | |     Option<(DateTime<FixedOffset>, String)>,
641 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: large size difference between variants
   --> src/native/gcal/journal.rs:703:1
    |
703 | / enum Update {
704 | |     Row(RowRecord),
    | |     -------------- the largest variant contains at least 320 bytes
705 | |     Link,
706 | |     Gone(Option<String>),
    | |     -------------------- the second-largest variant contains at least 24 bytes
707 | |     Flag(String),
708 | | }
    | |_^ the entire enum is at least 320 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
704 -     Row(RowRecord),
704 +     Row(Box<RowRecord>),
    |

warning: enclosing `Some` and `?` operator are unneeded
   --> src/native/gcal/lifecycle.rs:332:5
    |
332 |     Some(text.get(..open)?)
    |     ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_question_mark
    = note: `#[warn(clippy::needless_question_mark)]` on by default
help: remove the enclosing `Some` and `?` operator
    |
332 -     Some(text.get(..open)?)
332 +     text.get(..open)
    |

warning: this function has too many arguments (8/7)
   --> src/native/gcal/refile.rs:230:1
    |
230 | / fn classify_filing<C: ClockLookup + ?Sized>(
231 | |     input: &SyncPlanInput<'_>,
232 | |     contents: &str,
233 | |     events: &[EventNoteRow],
...   |
238 | |     clock: &mut Option<&mut C>,
239 | | ) -> Filing {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `.as_mut().map(|clock| &mut **clock)` on an `Option` value
   --> src/native/gcal/refile.rs:338:9
    |
338 |         clock.as_mut().map(|clock| &mut **clock),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using as_deref_mut: `clock.as_deref_mut()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#option_as_ref_deref
    = note: `#[warn(clippy::option_as_ref_deref)]` on by default

warning: this function has too many arguments (8/7)
    --> src/native/gcal/refile.rs:1081:1
     |
1081 | / fn wanted_for_event<C: ClockLookup + ?Sized>(
1082 | |     input: &SyncPlanInput<'_>,
1083 | |     contents: &str,
1084 | |     event: &EventNoteRow,
...    |
1089 | |     clock: &mut Option<&mut C>,
1090 | | ) -> Option<WantedLink> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: replacing a value of type `T` with `T::default()` is better expressed using `std::mem::take`
  --> src/native/gcal/render.rs:97:22
   |
97 |     let mut suffix = std::mem::replace(&mut spans.suffix, String::new());
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `std::mem::take(&mut spans.suffix)`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#mem_replace_with_default
   = note: `#[warn(clippy::mem_replace_with_default)]` on by default

warning: this boolean expression can be simplified
   --> src/native/gcal/render.rs:265:5
    |
265 | /     !result
266 | |         .suggestion
267 | |         .is_some_and(|suggestion| suggestion.theme.name == "MEET")
    | |__________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
265 ~     result
266 +         .suggestion.is_none_or(|suggestion| suggestion.theme.name != "MEET")
    |

warning: this function has too many arguments (8/7)
   --> src/native/gcal/root.rs:94:1
    |
 94 | / pub(crate) fn choose_event_root<S: HomeSource>(
 95 | |     resolver: &mut HomeResolver<S>,
 96 | |     vault: &Path,
 97 | |     daily_rel: &Path,
...   |
102 | |     note: Option<&NoteRootCandidate>,
103 | | ) -> EventRoot {
    | |______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/gcal/sync.rs:986:1
    |
986 | / pub(super) fn build_occurrences<S: HomeSource>(
987 | |     snapshot: &snapshot::DaySnapshot,
988 | |     config: &GcalConfig,
989 | |     vault: &std::path::Path,
...   |
995 | |     resolver: &mut HomeResolver<S>,
996 | | ) -> Vec<(PlannedOccurrence, Option<String>)> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
    --> src/native/gcal/sync.rs:2350:47
     |
2350 | fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
     |                                               ^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
2350 - fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
2350 + fn display_rel(vault: &std::path::Path, path: &Path) -> String {
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
     = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
     |
1952 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1952 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.start));
     |

warning: this function has too many arguments (8/7)
   --> src/native/gmail/compose/draft.rs:785:1
    |
785 | / fn persist_after_remote(
786 | |     vault: &Path,
787 | |     relative: &Path,
788 | |     note: &str,
...   |
793 | |     recovery_operation: Option<&str>,
794 | | ) -> Result<bool, GmailError> {
    | |_____________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/gmail/compose/draft.rs:875:1
    |
875 | / fn recover_create(
876 | |     vault: &Path,
877 | |     relative: &Path,
878 | |     note: &str,
...   |
884 | |     config: &GmailConfig,
885 | | ) -> Result<PreparedDraft, GmailError> {
    | |______________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/gmail/compose/draft.rs:967:1
    |
967 | / fn readback(
968 | |     gog: &Gog,
969 | |     account: &str,
970 | |     expected_draft_id: &str,
...   |
975 | |     verify_local: bool,
976 | | ) -> Result<Readback, GmailError> {
    | |_________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the following explicit lifetimes could be elided: 'a
    --> src/native/gmail/compose/draft.rs:1203:16
     |
1203 | fn unique_body<'a>(
     |                ^^
1204 |     candidates: &'a [body::BodyCandidate],
     |                  ^^
1205 |     kind: CandidateKind,
1206 | ) -> Result<&'a str, GmailError> {
     |              ^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
     |
1203 ~ fn unique_body(
1204 ~     candidates: &[body::BodyCandidate],
1205 |     kind: CandidateKind,
1206 ~ ) -> Result<&str, GmailError> {
     |

warning: large size difference between variants
  --> src/native/gmail/compose/send.rs:28:1
   |
28 | /  enum SendResponse {
29 | |      Preview(super::draft::PreparedDraft),
   | |      ------------------------------------ the largest variant contains at least 664 bytes
30 | |/     State {
31 | ||         status: &'static str,
32 | ||         note: String,
33 | ||         draft_id: Option<String>,
34 | ||         thread_id: Option<String>,
35 | ||         sent_message_id: Option<String>,
36 | ||     },
   | ||_____- the second-largest variant contains at least 112 bytes
37 | |  }
   | |__^ the entire enum is at least 664 bytes
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
   |
29 -     Preview(super::draft::PreparedDraft),
29 +     Preview(Box<super::draft::PreparedDraft>),
   |

warning: a `Vec` of `Range` that is only one element
   --> src/native/gmail/compose/source.rs:271:19
    |
271 |     let regions = vec![start..end];
    |                   ^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
    = note: `#[warn(clippy::single_range_in_vec_init)]` on by default
help: if you wanted a `Vec` that contains the entire range, try
    |
271 -     let regions = vec![start..end];
271 +     let regions = (start..end).collect::<std::vec::Vec<usize>>();
    |

warning: a `Vec` of `Range` that is only one element
    --> src/native/gmail/compose/source.rs:1019:16
     |
1019 |         return vec![start..end];
     |                ^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1019 -         return vec![start..end];
1019 +         return (start..end).collect::<std::vec::Vec<usize>>();
     |

warning: this function has too many arguments (8/7)
    --> src/native/gmail/compose/source.rs:1061:1
     |
1061 | / fn source_fingerprint(
1062 | |     kind: &ComposeKind,
1063 | |     to: &[String],
1064 | |     cc: &[String],
...    |
1069 | |     target: Option<&ReplyTarget>,
1070 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this boolean expression can be simplified
   --> src/native/gmail/doctor.rs:424:20
    |
424 |                   && !scopes
    |  ____________________^
425 | |                     .iter()
426 | |                     .any(|scope| {
427 | |                         scope == super::config::MODIFY_SCOPE
...   |
430 | |                     .then_some(acct)
431 | |                     .is_some()
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
424 ~                 && scopes
425 +                     .iter()
426 +                     .any(|scope| {
427 +                         scope == super::config::MODIFY_SCOPE
428 +                             || scope.contains("gmail.modify")
429 +                     })
430 +                     .then_some(acct).is_none()
    |

warning: this function has too many arguments (8/7)
   --> src/native/gmail/link.rs:374:1
    |
374 | / fn resolve_url(
375 | |     gog: &Gog,
376 | |     account: &str,
377 | |     vault: &Path,
...   |
382 | |     url: &str,
383 | | ) -> Result<PreparedSave, GmailError> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/gmail/link.rs:655:6
    |
655 |   ) -> Result<
    |  ______^
656 | |     (
657 | |         Vec<StagedTextFile>,
658 | |         Vec<AppliedSwap>,
...   |
662 | |     GmailError,
663 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/gmail/link.rs:1198:1
     |
1198 | / fn commit_and_journal(
1199 | |     vault: &Path,
1200 | |     host: &str,
1201 | |     child_env: &ob::ChildEnv,
...    |
1206 | |     outcome: &mut LinkOutcome,
1207 | | ) -> Result<(), GmailError> {
     | |___________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the loop variable `index` is only used to index `masked`
   --> src/native/gmail/list.rs:436:22
    |
436 |         for index in cursor..end {
    |                      ^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
436 -         for index in cursor..end {
436 +         for <item> in masked.iter_mut().take(end).skip(cursor) {
    |

warning: this function has too many arguments (9/7)
   --> src/native/gmail/note/layout.rs:255:1
    |
255 | / fn render_card(
256 | |     message: &GmailMessage,
257 | |     id: &str,
258 | |     body: &RenderedBody,
...   |
264 | |     attachment_number: &mut u32,
265 | | ) -> RenderedCard {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: consider using `sort_by_key`
   --> src/native/gmail/note/merge.rs:105:5
    |
105 |     replacements.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
105 -     replacements.sort_by(|left, right| right.0.start.cmp(&left.0.start));
105 +     replacements.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

warning: this loop could be written as a `while let` loop
  --> src/native/gmail/note/text.rs:13:5
   |
13 | /     loop {
14 | |         let Some((prefix, rest)) = subject.split_once(':') else {
15 | |             break;
16 | |         };
...  |
23 | |         subject = rest.trim_start();
24 | |     }
   | |_____^ help: try: `while let Some((prefix, rest)) = subject.split_once(':') { .. }`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#while_let_loop

warning: this function has too many arguments (9/7)
   --> src/native/gmail/save.rs:506:1
    |
506 | / pub(crate) fn plan_prepared_saves(
507 | |     vault: &Path,
508 | |     folder: &Path,
509 | |     link_template: &str,
...   |
515 | |     timezone: chrono_tz::Tz,
516 | | ) -> Result<Vec<StagedSaveNote>, GmailError> {
    | |____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/gmail/save.rs:535:1
    |
535 | / pub(crate) fn plan_prepared_saves_with_parent_links(
536 | |     vault: &Path,
537 | |     folder: &Path,
538 | |     link_template: &str,
...   |
545 | |     timezone: chrono_tz::Tz,
546 | | ) -> Result<Vec<StagedSaveNote>, GmailError> {
    | |____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/gmail/sync/archive_preview.rs:454:1
    |
454 | / pub(crate) fn remote_verdict_for_saved_ids<R: GmailRead>(
455 | |     reader: &R,
456 | |     account: &str,
457 | |     evidence: &ArchiveThreadEvidence,
...   |
462 | |     policy: &NeverSavePolicy,
463 | | ) -> Result<RemoteVerdict, GmailError> {
    | |______________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: enclosing `Some` and `?` operator are unneeded
    --> src/native/gmail/sync/archive_state.rs:1262:17
     |
1262 | /                 Some(ThreadKey::new(
1263 | |                     value.get("account")?.as_str()?,
1264 | |                     value.get("thread_id")?.as_str()?,
1265 | |                 )?)
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_question_mark
help: remove the enclosing `Some` and `?` operator
     |
1262 ~                 ThreadKey::new(
1263 |                     value.get("account")?.as_str()?,
1264 |                     value.get("thread_id")?.as_str()?,
1265 ~                 )
     |

warning: this function has too many arguments (23/7)
    --> src/native/gmail/sync/file.rs:1038:1
     |
1038 | / fn build_attempt(
1039 | |     vault: &Path,
1040 | |     mail_folder: &Path,
1041 | |     link_template: &str,
...    |
1061 | |     pending_reopen: &[RecoveryReopen],
1062 | | ) -> Result<AttemptPlan, GmailError> {
     | |____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `map(f)` on an `Option` value where `f` is a closure that returns the unit type `()`
    --> src/native/gmail/sync/file.rs:1218:25
     |
1218 | /                         reopen_activity.as_mut().map(|(state, _)| {
1219 | |                             state.retry_thread_ids.remove(key.thread_id());
1220 | |                         });
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#option_map_unit_fn
     = note: `#[warn(clippy::option_map_unit_fn)]` on by default
help: use `if let` instead
     |
1218 -                         reopen_activity.as_mut().map(|(state, _)| {
1219 -                             state.retry_thread_ids.remove(key.thread_id());
1220 -                         });
1218 +                         if let Some((state, _)) = reopen_activity.as_mut() { state.retry_thread_ids.remove(key.thread_id()); }
     |

warning: this function has too many arguments (9/7)
    --> src/native/gmail/sync/file.rs:1859:1
     |
1859 | / fn apply_reopen_plan(
1860 | |     vault: &Path,
1861 | |     timezone: chrono_tz::Tz,
1862 | |     saves: &[StagedSaveNote],
...    |
1868 | |     outcome: &mut FilingOutcome,
1869 | | ) -> Vec<RecoveryReopen> {
     | |________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this boolean expression can be simplified
    --> src/native/gmail/sync/file.rs:2135:12
     |
2135 |           if !file
     |  ____________^
2136 | |             .target
2137 | |             .extension()
2138 | |             .is_some_and(|extension| extension == "md")
     | |_______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
2135 ~         if file
2136 +             .target
2137 +             .extension().is_none_or(|extension| extension != "md")
     |

warning: this boolean expression can be simplified
    --> src/native/gmail/sync/file.rs:2187:12
     |
2187 |           if !file
     |  ____________^
2188 | |             .target
2189 | |             .extension()
2190 | |             .is_some_and(|extension| extension == "md")
     | |_______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
2187 ~         if file
2188 +             .target
2189 +             .extension().is_none_or(|extension| extension != "md")
     |

warning: this function has too many arguments (9/7)
    --> src/native/gmail/sync/file.rs:2210:1
     |
2210 | / fn apply_born_held(
2211 | |     vault: &Path,
2212 | |     timezone: chrono_tz::Tz,
2213 | |     reply_wait_days: u32,
...    |
2219 | |     works: &BTreeMap<(String, String), PreparedSave>,
2220 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
    --> src/native/gmail/sync/file.rs:2216:13
     |
2216 |     staged: &mut Vec<StagedTextFile>,
     |             ^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
2216 -     staged: &mut Vec<StagedTextFile>,
2216 +     staged: &mut [StagedTextFile],
     |

warning: this function has too many arguments (13/7)
    --> src/native/gmail/sync/file.rs:2300:1
     |
2300 | / fn apply_health_edits(
2301 | |     vault: &Path,
2302 | |     inbox: &str,
2303 | |     enrollment: &EnrollmentFold,
...    |
2313 | |     health_events: &mut Vec<HealthEvent>,
2314 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/gmail/sync/file.rs:2902:6
     |
2902 | ) -> Result<FilingOutcome, (GmailError, AttemptPlan)> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 800 bytes
     |
     = help: try reducing the size of `(native::google::error::GoogleError, native::gmail::sync::file::AttemptPlan)`, for example by boxing large elements or replacing it with `Box<(native::google::error::GoogleError, native::gmail::sync::file::AttemptPlan)>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this `.filter_map(..)` can be written more simply using `.map(..)`
    --> src/native/gmail/sync/file.rs:3063:51
     |
3063 |                       .chain(plan.watch_gone.iter().filter_map(|key| {
     |  ___________________________________________________^
3064 | |                         Some(RecoveryWatch {
3065 | |                             account: key.account().to_string(),
3066 | |                             thread_id: key.thread_id().to_string(),
...    |
3076 | |                         })
3077 | |                     })),
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_filter_map
     = note: `#[warn(clippy::unnecessary_filter_map)]` on by default

warning: this function has too many arguments (8/7)
   --> src/native/gmail/sync/health.rs:567:1
    |
567 | / pub(crate) fn plan(
568 | |     vault: &Path,
569 | |     inbox: &str,
570 | |     enrollment: &super::enroll::EnrollmentFold,
...   |
575 | |     already_conflicted: &BTreeSet<ThreadKey>,
576 | | ) -> Vec<HealthIntent> {
    | |______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` has identical blocks
   --> src/native/gmail/sync/health.rs:828:40
    |
828 |       } else if physical.ends_with('\n') {
    |  ________________________________________^
829 | |         "\n"
830 | |     } else {
    | |_____^
    |
note: same as this
   --> src/native/gmail/sync/health.rs:830:12
    |
830 |       } else {
    |  ____________^
831 | |         "\n"
832 | |     }
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: large size difference between variants
   --> src/native/gmail/sync/reopen.rs:470:1
    |
470 | / enum PreparedOne {
471 | |     Candidate(PreparedReopenCandidate),
    | |     ---------------------------------- the largest variant contains at least 624 bytes
472 | |     NoChange,
473 | |     Gone,
474 | |     Failure(ReopenFailure, bool),
    | |     ---------------------------- the second-largest variant contains at least 97 bytes
475 | |     AuthAbort(ReopenFailure),
476 | | }
    | |_^ the entire enum is at least 624 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
471 -     Candidate(PreparedReopenCandidate),
471 +     Candidate(Box<PreparedReopenCandidate>),
    |

warning: this function has too many arguments (9/7)
   --> src/native/gmail/sync/watch_apply.rs:891:1
    |
891 | / pub(crate) fn plan_for_send(
892 | |     vault: &Path,
893 | |     timezone: chrono_tz::Tz,
894 | |     reply_wait_days: u32,
...   |
900 | |     pending: &[RecoveryWatch],
901 | | ) -> WatchPlan {
    | |______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `format!` in `println!` args
   --> src/native/gmail/unarchive.rs:918:9
    |
918 | /         println!(
919 | |             "{} {}{}{}",
920 | |             action_mark(row.action),
921 | |             row.action,
...   |
927 | |             format!("{label}{message}")
928 | |         );
    | |_________^
    |
    = help: combine the `format!(..)` arguments with the outer `println!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: consider using `sort_by_key`
   --> src/native/google/client_setup.rs:301:5
    |
301 |     paths.sort_by(|a, b| b.0.cmp(&a.0));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
301 -     paths.sort_by(|a, b| b.0.cmp(&a.0));
301 +     paths.sort_by_key(|b| std::cmp::Reverse(b.0));
    |

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1985:1
     |
1985 | / pub(super) fn stamp_overwrite_source(
1986 | |     config: &Config,
1987 | |     plan: &OverwritePreflight,
1988 | |     options: &CreateOptions,
...    |
1993 | |     info: &PdfInfo,
1994 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2027:1
     |
2027 | / pub(super) fn stage_overwrite_audio(
2028 | |     options: &CreateOptions,
2029 | |     plan: &OverwritePreflight,
2030 | |     request: &OverwriteRequest,
...    |
2035 | |     title: &str,
2036 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2746:1
     |
2746 | / fn plan_target_for(
2747 | |     config: &Config,
2748 | |     stem: &str,
2749 | |     ref_type: &str,
...    |
2754 | |     source_display: &str,
2755 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3779:1
     |
3779 | / fn stage_overwrite_source_store(
3780 | |     _config: &Config,
3781 | |     plan: &OverwritePreflight,
3782 | |     scratch: &Path,
...    |
3789 | |     catalog: &super::code_catalog::CatalogOutcome,
3790 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4475:1
     |
4475 | / fn overwrite_pdf_url(
4476 | |     config: &Config,
4477 | |     url: super::clip_url::WebUrl,
4478 | |     downloaded: PathBuf,
...    |
4483 | |     selection: &OverwriteSelection,
4484 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4557:1
     |
4557 | / fn create_pdf_url_route(
4558 | |     config: &Config,
4559 | |     url: super::clip_url::WebUrl,
4560 | |     downloaded: PathBuf,
...    |
4565 | |     listen: Option<&super::listen::ListenCommand>,
4566 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5294:1
     |
5294 | / fn print_pdf_dry_run(
5295 | |     config: &Config,
5296 | |     styler: &Styler,
5297 | |     source_display: &str,
...    |
5305 | |     legacy: &[sources_mod::RecordedSource],
5306 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/create.rs:5535:1
     |
5535 | / fn compose_markdown_marker(
5536 | |     status: &str,
5537 | |     parent: &str,
5538 | |     title: &str,
...    |
5544 | |     return_links: bool,
5545 | | ) -> Result<String> {
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
   --> src/native/highlights_ref/clip_adapter.rs:780:5
    |
780 | /     DIAGRAM_TIMEOUT_BASE_SECS
781 | |         .saturating_add(
782 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
785 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
780 ~     DIAGRAM_TIMEOUT_BASE_SECS
781 +         .saturating_add(
782 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
783 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
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
    --> src/native/highlights_ref/note_snapshot/bob.rs:1258:1
     |
1258 | / fn push_schedule_group(
1259 | |     blocks: &mut Vec<Block>,
1260 | |     source: &SourceIdentity,
1261 | |     level: HeadingLevel,
...    |
1266 | |     used_ids: &mut BTreeSet<String>,
1267 | | ) {
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

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:133:1
    |
133 | / pub(super) fn plan_pdf_url(
134 | |     url: &WebUrl,
135 | |     downloaded: &Path,
136 | |     name_override: Option<&str>,
...   |
142 | |     progress: Option<&dyn Fn(&str)>,
143 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:220:1
    |
220 | / pub(super) fn plan_arxiv(
221 | |     paper: &ArxivPaper,
222 | |     name_override: Option<&str>,
223 | |     title_override: Option<&str>,
...   |
229 | |     progress: Option<&dyn Fn(&str)>,
230 | | ) -> Result<PdfPlan> {
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

warning: the `Err`-variant returned from this function is very large
  --> src/native/highlights_ref/scan_apply.rs:92:6
   |
92 | ) -> std::result::Result<AppliedFullScan, ApplyError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 160 bytes
   |
   = help: try reducing the size of `native::highlights_ref::scan_apply::ApplyError`, for example by boxing large elements or replacing it with `Box<native::highlights_ref::scan_apply::ApplyError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/highlights_ref/scan_apply.rs:160:6
    |
160 | ) -> std::result::Result<(), ApplyError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 160 bytes
    |
    = help: try reducing the size of `native::highlights_ref::scan_apply::ApplyError`, for example by boxing large elements or replacing it with `Box<native::highlights_ref::scan_apply::ApplyError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: field assignment outside of initializer for an instance created with Default::default()
   --> src/native/highlights_ref/scan_apply.rs:206:5
    |
206 |     counts.unchanged = pdfs.len();
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
note: consider initializing the variable with `native::highlights_ref::report::ScanCounts { unchanged: pdfs.len(), ..Default::default() }` and removing relevant reassignments
   --> src/native/highlights_ref/scan_apply.rs:205:5
    |
205 |     let mut counts = ScanCounts::default();
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: the `Err`-variant returned from this function is very large
   --> src/native/highlights_ref/scan_apply.rs:243:6
    |
243 | ) -> std::result::Result<AppliedFullScan, ApplyError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 160 bytes
    |
    = help: try reducing the size of `native::highlights_ref::scan_apply::ApplyError`, for example by boxing large elements or replacing it with `Box<native::highlights_ref::scan_apply::ApplyError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `contains_key` followed by `insert` on a `BTreeMap`
  --> src/native/highlights_ref/scan_plan.rs:78:5
   |
78 | /     if !file_states.contains_key(&path) {
79 | |         let state = fingerprint_file(&path)?;
80 | |         file_states.insert(path, state);
81 | |     }
   | |_____^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_entry
   = note: `#[warn(clippy::map_entry)]` on by default
help: try
   |
78 ~     if let std::collections::btree_map::Entry::Vacant(e) = file_states.entry(path) {
79 +         let state = fingerprint_file(&path)?;
80 +         e.insert(state);
81 +     }
   |

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

warning: the `Err`-variant returned from this function is very large
   --> src/native/host_catalog/txn.rs:131:52
    |
131 |     pub(crate) fn validate(&self, vault: &Path) -> Result<(), CaptureError> {
    |                                                    ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/host_catalog/txn.rs:225:26
    |
225 |                       .map(|entry| {
    |  __________________________^
226 | |                         entry.map_err(|error| {
227 | |                             read_failed(format!(
228 | |                                 "read directory {}: {error}",
...   |
231 | |                         })
232 | |                     })
    | |_____________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/host_catalog/txn.rs:269:6
    |
269 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/host_catalog/txn.rs:308:6
    |
308 | ) -> Result<Option<Vec<PathBuf>>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/host_catalog/txn.rs:800:48
    |
800 |             write_staged_files_guarded(&files, || deps.validate(vault))
    |                                                ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this boolean expression can be simplified
   --> src/native/note_catalog/tiers.rs:102:8
    |
102 |       if !relative
    |  ________^
103 | |         .extension()
104 | |         .is_some_and(|extension| extension == "md")
    | |___________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
102 ~     if relative
103 +         .extension().is_none_or(|extension| extension != "md")
    |

warning: this boolean expression can be simplified
  --> src/native/notebooks/rules.rs:96:9
   |
96 |         !frontmatter_end.is_some_and(|end| index <= end)
   |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `frontmatter_end.is_none_or(|end| index > end)`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/notebooks/scan.rs:907:6
    |
907 |   ) -> (
    |  ______^
908 | |     usize,
909 | |     Vec<(String, usize)>,
910 | |     Option<usize>,
911 | |     Option<usize>,
912 | |     Vec<usize>,
913 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: manual `RangeInclusive::contains` implementation
   --> src/native/notify.rs:255:12
    |
255 |           && seconds >= 0.0
    |  ____________^
256 | |         && seconds <= MAX_SLEEP_SECONDS
    | |_______________________________________^ help: use: `(0.0..=MAX_SLEEP_SECONDS).contains(&seconds)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains

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
   --> src/native/periods/note.rs:424:57
    |
424 |               if !name.is_empty() && !name.contains("  ") {
    |  _________________________________________________________^
425 | |                 current = Some(name);
426 | |             } else if !name.is_empty() {
    | |_____________^
    |
note: same as this
   --> src/native/periods/note.rs:426:40
    |
426 |               } else if !name.is_empty() {
    |  ________________________________________^
427 | |                 current = Some(name);
428 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/periods/report.rs:1149:6
     |
1149 | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/periods/report.rs:1140:1
     |
1140 | / fn build_parts(
1141 | |     vault: &Path,
1142 | |     id: PeriodId,
1143 | |     span: Span,
...    |
1148 | |     period_charts: &charts::Charts,
1149 | | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     | |____________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/plugins/sync.rs:172:1
    |
172 | / fn sync_one_plugin(
173 | |     options: &SyncOptions,
174 | |     id: &str,
175 | |     repo_plugin_dir: &Path,
...   |
181 | |     issues: &mut Vec<String>,
182 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (17/7)
   --> src/native/plugins/sync.rs:276:1
    |
276 | / fn apply_plugin(
277 | |     options: &SyncOptions,
278 | |     id: &str,
279 | |     captured: &CapturedPlugin,
...   |
293 | |     issues: &mut Vec<String>,
294 | | ) -> PluginSync {
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
   --> src/native/pomodoro_homes/resolve.rs:555:25
    |
555 | /                         chain[nearest_home..end]
556 | |                             .iter()
557 | |                             .filter(|(_, facts)| {
558 | |                                 facts.kind == NoteKind::Project
559 | |                             })
560 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
560 -                             .last()
560 +                             .next_back()
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
   --> src/native/pomodoro_themes/relocation_apply.rs:147:13
    |
147 | /             match rename_entry(day_contents, entry.line, &new_name) {
148 | |                 Some(updated) => Some((
149 | |                     updated,
150 | |                     TypeRelocation {
...   |
160 | |                 None => None,
161 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
147 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
148 +                     updated,
149 +                     TypeRelocation {
150 +                         outcome: "rename_entry",
151 +                         from,
152 +                         to: new_name,
153 +                         source_before: line,
154 +                         dest_before: Some(line),
155 +                         dest_after: line,
156 +                         dest_created: false,
157 +                     },
158 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:167:13
    |
167 | /             match rename_entry(day_contents, entry.line, &new_name) {
168 | |                 Some(updated) => Some((
169 | |                     updated,
170 | |                     TypeRelocation {
...   |
180 | |                 None => None,
181 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
167 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
168 +                     updated,
169 +                     TypeRelocation {
170 +                         outcome: "rename_placeholder",
171 +                         from,
172 +                         to: new_name,
173 +                         source_before: line,
174 +                         dest_before: Some(line),
175 +                         dest_after: line,
176 +                         dest_created: false,
177 +                     },
178 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:187:13
    |
187 | /             match rename_entry(day_contents, entry.line, &new_name) {
188 | |                 Some(updated) => Some((
189 | |                     updated,
190 | |                     TypeRelocation {
...   |
200 | |                 None => None,
201 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
187 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
188 +                     updated,
189 +                     TypeRelocation {
190 +                         outcome: "append_component",
191 +                         from,
192 +                         to: new_name,
193 +                         source_before: line,
194 +                         dest_before: Some(line),
195 +                         dest_after: line,
196 +                         dest_created: false,
197 +                     },
198 +                 ))
    |

warning: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:252:13
    |
252 | /             match create_below_and_move(
253 | |                 day_contents,
254 | |                 source_entry.line,
255 | |                 link.line_index,
...   |
271 | |                 None => None,
272 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
252 ~             create_below_and_move(
253 +                 day_contents,
254 +                 source_entry.line,
255 +                 link.line_index,
256 +                 link.subtree_end,
257 +                 &name,
258 +             ).map(|updated| (
259 +                     updated,
260 +                     TypeRelocation {
261 +                         outcome: "create_below",
262 +                         from: from_name,
263 +                         to: name,
264 +                         source_before: source_index,
265 +                         dest_before: None,
266 +                         dest_after,
267 +                         dest_created: true,
268 +                     },
269 +                 ))
    |

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/cli.rs:734:45
    |
734 |         write_staged_files_guarded(&staged, || deps.validate(&vault))
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/cli.rs:960:45
    |
960 |         write_staged_files_guarded(&staged, || deps.validate(&vault))
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/records/cli.rs:1364:45
     |
1364 |         write_staged_files_guarded(&staged, || deps.validate(vault))
     |                                             ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: `to_string` applied to a type that implements `Display` in `print!` args
    --> src/native/records/cli.rs:2505:64
     |
2505 |               .header(&format!("a/{path}"), &format!("b/{path}"))
     |  ________________________________________________________________^
2506 | |             .to_string()
     | |________________________^ help: remove this
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: large size difference between variants
    --> src/native/records/cli.rs:2764:1
     |
2764 | / enum Collection {
2765 | |     Usable(ResolvedRecordKind),
     | |     -------------------------- the second-largest variant contains at least 344 bytes
2766 | |     InvalidAlbum(AlbumEntry),
     | |     ------------------------ the largest variant contains at least 1152 bytes
2767 | | }
     | |_^ the entire enum is at least 1152 bytes
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
     |
2766 -     InvalidAlbum(AlbumEntry),
2766 +     InvalidAlbum(Box<AlbumEntry>),
     |

warning: large size difference between variants
   --> src/native/records/context.rs:104:1
    |
104 | /   pub(crate) enum RecordKindResolution {
105 | | /     Valid {
106 | | |         kind: ResolvedRecordKind,
107 | | |         warnings: Vec<AlbumFinding>,
108 | | |         health: DiscoveryHealth,
109 | | |     },
    | | |_____- the largest variant contains at least 392 bytes
110 | | /     Invalid {
111 | | |         paths: Vec<String>,
112 | | |         findings: Vec<AlbumFinding>,
113 | | |         health: DiscoveryHealth,
114 | | |     },
    | | |_____- the second-largest variant contains at least 72 bytes
...   |
120 | |       },
121 | |   }
    | |___^ the entire enum is at least 392 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
106 -         kind: ResolvedRecordKind,
106 +         kind: Box<ResolvedRecordKind>,
    |

warning: stripping a suffix manually
  --> src/native/records/notes_section.rs:23:18
   |
23 |                 (raw[..raw.len() - 2].to_owned(), "\r\n".to_owned())
   |                  ^^^^^^^^^^^^^^^^^^^^
   |
note: the suffix was tested here
  --> src/native/records/notes_section.rs:22:37
   |
22 |             let (content, ending) = if raw.ends_with("\r\n") {
   |                                     ^^^^^^^^^^^^^^^^^^^^^^^^^
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_suffix` method
   |
22 ~             let (content, ending) = if let Some(<stripped>) = raw.strip_suffix("\r\n") {
23 ~                 (<stripped>.to_owned(), "\r\n".to_owned())
   |

warning: the `Err`-variant returned from this function is very large
   --> src/native/records/plan.rs:398:6
    |
398 | ) -> Result<FieldInputState, RecordDiagnostic> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: manual `Range::contains` implementation
   --> src/native/records/render.rs:423:25
    |
423 |         if index < 4 || (index >= 5 && index < 7) || (index >= 8 && index < 10)
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `(5..7).contains(&index)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains

warning: manual `Range::contains` implementation
   --> src/native/records/render.rs:423:54
    |
423 |         if index < 4 || (index >= 5 && index < 7) || (index >= 8 && index < 10)
    |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `(8..10).contains(&index)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains

warning: stripping a suffix manually
   --> src/native/records/render.rs:464:18
    |
464 |                 (raw[..raw.len() - 2].to_owned(), "\r\n".to_owned())
    |                  ^^^^^^^^^^^^^^^^^^^^
    |
note: the suffix was tested here
   --> src/native/records/render.rs:463:37
    |
463 |             let (content, ending) = if raw.ends_with("\r\n") {
    |                                     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_suffix` method
    |
463 ~             let (content, ending) = if let Some(<stripped>) = raw.strip_suffix("\r\n") {
464 ~                 (<stripped>.to_owned(), "\r\n".to_owned())
    |

warning: the variable `offset` is used as a loop counter
    --> src/native/records/render.rs:1596:9
     |
1596 |         for line in block {
     |         ^^^^^^^^^^^^^^^^^ help: consider using: `for (offset, line) in block.into_iter().enumerate()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop

warning: the `Err`-variant returned from this function is very large
   --> src/native/records/schema.rs:674:6
    |
674 | ) -> Result<ValidatedFieldInput, RecordDiagnostic> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/records/schema.rs:696:6
    |
696 | ) -> Result<RecordValue, RecordDiagnostic> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/schema.rs:717:14
    |
717 |         .map(|member| validate_scalar(field, member, today))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/records/schema.rs:726:6
    |
726 | ) -> Result<RecordValue, RecordDiagnostic> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/schema.rs:766:14
    |
766 |         .map(|member| validate_scalar(field, member, today))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/records/schema.rs:1049:18
     |
1049 |       let result = (|| {
     |  __________________^
1050 | |         reject_unknown_keys(mapping, ALBUM_RECORD_KEYS, &source, "record")?;
1051 | |
1052 | |         let noun = mapping_get(mapping, "noun")
...    |
1135 | |         })
1136 | |     })();
     | |______^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1160:6
     |
1160 | ) -> Result<Option<String>, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1231:6
     |
1231 | ) -> Result<RecordField, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1299:6
     |
1299 | ) -> Result<FieldKind, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1369:6
     |
1369 | ) -> Result<RecordValue, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/records/schema.rs:1382:18
     |
1382 |             .map(|item| default_scalar(item, field, source))
     |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1399:6
     |
1399 | ) -> Result<RecordScalar, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1453:6
     |
1453 | ) -> Result<RecordScalar, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1592:6
     |
1592 | ) -> Result<f64, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1742:6
     |
1742 | ) -> Result<Vec<String>, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/records/schema.rs:1757:14
     |
1757 |           .map(|pattern| {
     |  ______________^
1758 | |             pattern
1759 | |                 .as_str()
1760 | |                 .filter(|pattern| !pattern.is_empty())
...    |
1767 | |                 })
1768 | |         })
     | |_________^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1779:6
     |
1779 | ) -> Result<&'a Mapping, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1800:6
     |
1800 | ) -> Result<String, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1840:6
     |
1840 | ) -> Result<Option<String>, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1875:6
     |
1875 | ) -> Result<bool, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1895:6
     |
1895 | ) -> Result<(), RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1937:6
     |
1937 | ) -> Result<bool, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1953:6
     |
1953 | ) -> Result<Option<String>, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:1979:6
     |
1979 | ) -> Result<Option<f64>, RecordDiagnostic> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: consider using `sort`
    --> src/native/records/schema.rs:2006:5
     |
2006 |     candidates.sort_by(|left, right| left.cmp(right));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
     |
2006 -     candidates.sort_by(|left, right| left.cmp(right));
2006 +     candidates.sort();
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
    --> src/native/ref_library/migrate_tasks/plan.rs:1042:20
     |
1042 |               return format!(
     |  ____________________^
1043 | |                 "{}{}",
1044 | |                 &line[..caret + 1],
1045 | |                 format!("{new_id}{}", &line[trimmed_end..])
1046 | |             );
     | |_____________^
     |
     = help: combine the `format!(..)` arguments with the outer `format!(..)` call
     = help: or consider changing `format!` to `format_args!`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: doc list item without indentation
   --> src/native/ref_library/mod.rs:933:5
    |
933 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
933 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
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
   --> src/native/relation_labels/rename.rs:841:5
    |
841 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
841 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
841 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
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

warning: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/tick/catalog.rs:38:15
   |
38 |     pub gate: fn(&StepContext<'_>) -> Option<(GateInfo, Option<GateResult>)>,
   |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/tick/catalog.rs:102:11
    |
102 |     gate: fn(&StepContext<'_>) -> Option<(GateInfo, Option<GateResult>)>,
    |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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

warning: this boolean expression can be simplified
   --> src/native/task_complete/offer_close.rs:518:8
    |
518 |     if !ordinal.is_some_and(|ordinal| ordinal > 0)
    |        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `ordinal.is_none_or(|ordinal| ordinal <= 0)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool

warning: this function has too many arguments (9/7)
   --> src/native/task_complete/project_pull_in.rs:934:1
    |
934 | / fn emit_keep_moving_recover(
935 | |     plan: &mut SuccessorPlan,
936 | |     completed: &[CompletedTask],
937 | |     day_task_lines: &BTreeMap<String, usize>,
...   |
943 | |     reason: &'static str,
944 | | ) {
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
   --> src/native/task_complete/successors.rs:873:1
    |
873 | / fn effective_relation_state_map(
874 | |     verdicts: &[DependentVerdict],
875 | |     files: &[FileScan],
876 | |     states: &BTreeMap<
...   |
885 | |     source_paths: &BTreeSet<&Path>,
886 | | ) -> BTreeMap<String, SourceRecovery> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1143:1
     |
1143 | / fn relation_offer_placement(
1144 | |     group: &RelationOfferGroup,
1145 | |     completed: &[CompletedTask],
1146 | |     baseline_day: &DayView,
...    |
1151 | |     implicit: Option<&ImplicitDest>,
1152 | | ) -> Option<RelationOfferPlacement> {
     | |___________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2555:1
     |
2555 | / fn attach_offer(
2556 | |     verdict: &mut DependentVerdict,
2557 | |     files: &[FileScan],
2558 | |     day: &DayView,
...    |
2563 | |     project: Option<PathBuf>,
2564 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:2656:1
     |
2656 | / fn apply_project_member_classes(
2657 | |     verdicts: &mut Vec<DependentVerdict>,
2658 | |     folds: &mut Vec<ProjectFold>,
2659 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
2668 | |     _note_settings: &NoteTaskSettings,
2669 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
    --> src/native/task_complete/successors.rs:3252:1
     |
3252 | / fn apply_verdicts(
3253 | |     input: SuccessorInput,
3254 | |     files: Vec<FileScan>,
3255 | |     verdicts: Vec<DependentVerdict>,
...    |
3265 | |     relation_target_reads: usize,
3266 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/payload.rs:464:6
    |
464 | ) -> Result<(Vec<LineRange>, Vec<(String, String)>, usize), MergeError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/retirement.rs:215:15
    |
215 |     repoints: &[((PathBuf, String), (PathBuf, String))],
    |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
   --> src/native/task_merge/types.rs:176:41
    |
176 | pub(crate) fn format_merge_origin(path: &PathBuf, block_id: &str) -> String {
    |                                         ^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
176 - pub(crate) fn format_merge_origin(path: &PathBuf, block_id: &str) -> String {
176 + pub(crate) fn format_merge_origin(path: &Path, block_id: &str) -> String {
    |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/command.rs:1105:6
     |
1105 | ) -> Result<(Option<(PathBuf, String)>, Vec<RelocatedInfo>), String> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/task_move/plan.rs:359:22
    |
359 |           let parent = tasks
    |  ______________________^
360 | |             .iter()
361 | |             .filter(|candidate| {
362 | |                 candidate.line_index < task.line_index
...   |
365 | |             })
366 | |             .last();
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
366 -             .last();
366 +             .next_back();
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
   --> src/native/task_status_hooks/sync.rs:584:5
    |
584 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:372:9
    |
372 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1405:1
     |
1405 | / fn consume_blocked_links_after_compose(
1406 | |     compose: &mut ComposeResult,
1407 | |     files: &[FileScan],
1408 | |     daily_path: &Path,
...    |
1419 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1420 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: match can be simplified with `.unwrap_or_default()`
    --> src/native/task_status_hooks/sync.rs:1584:9
     |
1584 | /         match bob_config::load_plan_config(&bob_config::config_path()) {
1585 | |             Ok(config) => config,
1586 | |             Err(_) => crate::native::config::PlanConfig::default(),
1587 | |         };
     | |_________^ help: replace it with: `bob_config::load_plan_config(&bob_config::config_path()).unwrap_or_default()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_unwrap_or_default
     = note: `#[warn(clippy::manual_unwrap_or_default)]` on by default

warning: redundant redefinition of a binding `current_signatures`
   --> src/native/vault_task_loss.rs:258:5
    |
258 |     let mut current_signatures = current_signatures;
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
help: `current_signatures` is initially defined here
   --> src/native/vault_task_loss.rs:187:9
    |
187 |     let mut current_signatures = BTreeSet::new();
    |         ^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

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

warning: `bob-obsidian` (lib) generated 743 warnings
error: could not compile `bob-obsidian` (lib) due to 1 previous error; 743 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/sync.rs:989:13
    |
989 |             || txn.deps.validate(&vault),
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:165:6
    |
165 | ) -> Result<OpOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/write.rs:356:57
    |
356 |         let error = write_staged_files_guarded(&staged, || deps.validate(root))
    |                                                         ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/write.rs:444:53
    |
444 |         let error = write_staged_files_guarded(&[], || deps.validate(root))
    |                                                     ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

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
   --> src/native/bank/config_update/tests.rs:261:6
    |
261 | ) -> Result<(String, Vec<ops::OpResult>, Vec<InverseOp>), ops::OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/bank/config_update/tests.rs:269:6
    |
269 | ) -> Result<(String, Vec<ops::OpResult>, Vec<InverseOp>), ops::OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::bank::config_update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::bank::config_update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: field assignment outside of initializer for an instance created with Default::default()
   --> src/native/bank/status.rs:623:9
    |
623 | /         journal.imports =
624 | |             vec![import(1, 5, 5, 10_000, 6), import(8, 12, 12, 10_000, 12)];
    | |____________________________________________________________________________^
    |
note: consider initializing the variable with `native::bank::journal::JournalSnapshot { imports: vec![import(1, 5, 5, 10_000, 6), import(8, 12, 12, 10_000, 12)], ..Default::default() }` and removing relevant reassignments
   --> src/native/bank/status.rs:622:9
    |
622 |         let mut journal = JournalSnapshot::default();
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
    = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
   --> src/native/bank/status.rs:650:9
    |
650 | /         journal.imports =
651 | |             vec![import(1, 5, 5, 10_000, 5), import(1, 5, 5, 10_250, 5)];
    | |_________________________________________________________________________^
    |
note: consider initializing the variable with `native::bank::journal::JournalSnapshot { imports: vec![import(1, 5, 5, 10_000, 5), import(1, 5, 5, 10_250, 5)], ..Default::default() }` and removing relevant reassignments
   --> src/native/bank/status.rs:649:9
    |
649 |         let mut journal = JournalSnapshot::default();
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
   --> src/native/bank/subscriptions/coverage.rs:152:9
    |
152 | /         journal.imports = vec![
153 | |             import("checking", date(2026, 1, 1), date(2026, 1, 31)),
154 | |             import("savings", date(2026, 2, 1), date(2026, 2, 28)),
155 | |         ];
    | |__________^
    |
note: consider initializing the variable with `native::bank::journal::JournalSnapshot { imports: vec![
                  import("checking", date(2026, 1, 1), date(2026, 1, 31)),
                  import("savings", date(2026, 2, 1), date(2026, 2, 28)),
              ], ..Default::default() }` and removing relevant reassignments
   --> src/native/bank/subscriptions/coverage.rs:151:9
    |
151 |         let mut journal = JournalSnapshot::default();
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: this function has too many arguments (8/7)
   --> src/native/bank/subscriptions/ledger.rs:566:5
    |
566 | /     fn row(
567 | |         account: &str,
568 | |         day: NaiveDate,
569 | |         cents: i64,
...   |
574 | |         line: usize,
575 | |     ) -> BankRow {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/bank/tests.rs:1462:9
     |
1462 |         || Ok(()),
     |         ^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:366:10
    |
366 |     ) -> Result<PlannedDependencyUpdate, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:630:10
    |
630 |     ) -> Result<DependentRef, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/note_pull.rs:1655:39
     |
1655 |     fn plan(harness: &mut Harness) -> Result<PlannedCaptureItem, CaptureError> {
     |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3292:10
     |
3292 |     ) -> Result<PlannedCaptureItem, CaptureError> {
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
    --> src/native/capture_language/close_log.rs:1383:9
     |
1383 | /         match lex_bullets(close, draft).expect("valid bullets") {
1384 | |             CloseLogLexed { entries, dangling } => {
1385 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1386 | |                 entries
...    |
1391 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `#[warn(clippy::match_single_binding)]` on by default
help: consider using a `let` statement
     |
1383 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1384 +         {
1385 +             assert!(dangling.is_empty(), "unexpected dangling");
1386 +             entries
1387 +                 .into_iter()
1388 +                 .map(|entry| (entry.index, entry.text, entry.details))
1389 +                 .collect()
1390 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1489:9
     |
1489 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1490 | |             CloseLogLexed { entries, dangling } => {
1491 | |                 assert!(entries.is_empty());
1492 | |                 assert_eq!(dangling.len(), 1);
...    |
1495 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1489 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1490 +         {
1491 +             assert!(entries.is_empty());
1492 +             assert_eq!(dangling.len(), 1);
1493 +             assert_eq!(dangling[0].index, Some(1));
1494 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1564:9
     |
1564 | /         match lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing")
1565 | |         {
1566 | |             error => assert!(
1567 | |                 error.message.contains("- 1 wired"),
...    |
1570 | |             ),
1571 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1564 ~         let error = lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing");
1565 +         assert!(
1566 +             error.message.contains("- 1 wired"),
1567 +             "{}",
1568 +             error.message
1569 +         )
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2061:9
     |
2061 | /         match lex_bullets("x", "x\n- *").expect("dangling star") {
2062 | |             CloseLogLexed { entries, dangling } => {
2063 | |                 assert!(entries.is_empty());
2064 | |                 assert_eq!(dangling.len(), 1);
...    |
2067 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2061 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *").expect("dangling star");
2062 +         {
2063 +             assert!(entries.is_empty());
2064 +             assert_eq!(dangling.len(), 1);
2065 +             assert_eq!(dangling[0].index, None);
2066 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2068:9
     |
2068 | /         match lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details")
2069 | |         {
2070 | |             CloseLogLexed { entries, dangling } => {
2071 | |                 assert!(entries.is_empty());
...    |
2075 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2068 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details");
2069 +         {
2070 +             assert!(entries.is_empty());
2071 +             assert_eq!(dangling.len(), 1);
2072 +             assert_eq!(dangling[0].index, None);
2073 +         }
     |

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:4849:5
     |
4849 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:4848:5
     |
4848 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

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
   --> src/native/capture_language/tests/goto.rs:103:22
    |
103 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:116:35
    |
116 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: called `filter(..).next_back()` on an `DoubleEndedIterator`. This is more succinctly expressed by calling `.rfind(..)` instead
    --> src/native/capture_language/tests/grammar.rs:1368:29
     |
1368 |           let last_operator = raw
     |  _____________________________^
1369 | |             .split_whitespace()
1370 | |             .filter(|token| token.starts_with('+') || token.starts_with('-'))
1371 | |             .next_back()
     | |________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_next
help: try
     |
1368 ~         let last_operator = raw
1369 +             .split_whitespace().rfind(|token| token.starts_with('+') || token.starts_with('-'))
     |

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2699:35
     |
2699 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2736:48
     |
2736 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2745:22
     |
2745 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
  --> src/native/capture_language/tests/note_goto.rs:55:42
   |
55 |         let completion = field(raw, end).expect(&format!("{raw:?} completes"));
   |                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw:?} completes"))`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/note_goto.rs:128:22
    |
128 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/note_goto.rs:144:35
    |
144 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: `to_string` applied to a type that implements `Display` in `format!` args
    --> src/native/capture_parse.rs:4860:13
     |
4860 |             "Blaze @eat"[..start].to_string(),
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use this: `&"Blaze @eat"[..start]`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: `to_string` applied to a type that implements `Display` in `format!` args
    --> src/native/capture_parse.rs:4862:13
     |
4862 |             "Blaze @eat"[end..].to_string(),
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use this: `&"Blaze @eat"[end..]`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

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

warning: struct pattern is not needed for a unit variant
    --> src/native/capture_record.rs:1398:61
     |
1398 | ...                   Some(PerRouteDecision::Unclaimed { .. })
     |                                                       ^^^^^^^ help: remove the struct pattern
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unneeded_struct_pattern
     = note: `#[warn(clippy::unneeded_struct_pattern)]` on by default

warning: struct pattern is not needed for a unit variant
    --> src/native/capture_record.rs:1419:45
     |
1419 |             Some(PerRouteDecision::Unclaimed { .. }) | None
     |                                             ^^^^^^^ help: remove the struct pattern
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unneeded_struct_pattern

warning: this assertion has a constant value
   --> src/native/file_coordination.rs:225:9
    |
225 |         assert!(!IS_COORDINATED);
    |         ^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: consider moving this into a const block: `const { assert!(..) }`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants
    = note: `#[warn(clippy::assertions_on_constants)]` on by default

warning: unnecessary use of `get(&(
                         occurrence_key("primary", "deerwood"),
                         "2026-10-30".to_string()
                     ))
                     .is_none()`
    --> src/native/gcal/journal.rs:2121:14
     |
2121 |               .get(&(
     |  ______________^
2122 | |                 occurrence_key("primary", "deerwood"),
2123 | |                 "2026-10-30".to_string()
2124 | |             ))
2125 | |             .is_none());
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
help: replace it with
     |
2120 ~         assert!(!state.contains_key(&(
2121 +                 occurrence_key("primary", "deerwood"),
2122 +                 "2026-10-30".to_string()
2123 ~             )));
     |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/gmail/compose/draft.rs:1732:24
     |
1732 |         let mutations: Vec<(&str, fn(&mut Preview))> = vec![
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: called `.err().expect()` on a `Result` value
    --> src/native/gmail/gog.rs:1378:10
     |
1378 |           .err()
     |  __________^
1379 | |         .expect("size mismatch must fail");
     | |_______________^ help: try: `expect_err`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#err_expect
     = note: `#[warn(clippy::err_expect)]` on by default

warning: called `.err().expect()` on a `Result` value
    --> src/native/gmail/gog.rs:1387:60
     |
1387 |             let error = parse_attachment_response(&stdout).err().expect("fail");
     |                                                            ^^^^^^^^^^^^ help: try: `expect_err`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#err_expect

warning: called `.err().expect()` on a `Result` value
    --> src/native/gmail/gog.rs:1553:56
     |
1553 |             let error = normalize_threads_list(stdout).err().expect("fail");
     |                                                        ^^^^^^^^^^^^ help: try: `expect_err`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#err_expect

warning: called `.err().expect()` on a `Result` value
    --> src/native/gmail/gog.rs:1640:50
     |
1640 |             let error = parse_sent_receipt(&bad).err().expect("fail");
     |                                                  ^^^^^^^^^^^^ help: try: `expect_err`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#err_expect

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/archive_preview.rs:2045:30
     |
2045 |         let forward = digest(&[duplicates.clone()]);
     |                              ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&duplicates)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: unnecessary use of `get(&("other@example.com".to_string(), THREAD.to_string()))
                         .is_none()`
    --> src/native/gmail/sync/archive_state.rs:2952:18
     |
2951 | /              listed
2952 | |                  .get(&("other@example.com".to_string(), THREAD.to_string()))
     | | __________________^
2953 | ||                 .is_none(),
     | ||__________________________^ help: replace it with: `!listed.contains_key(&("other@example.com".to_string(), THREAD.to_string()))`
     |  |__________________________|
     |
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: this assertion has a constant value
   --> src/native/gmail/sync/discover.rs:885:9
    |
885 |         assert!(DEFAULT_LIMIT <= MAX_LIMIT);
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: consider moving this into a const block: `const { assert!(..) }`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/report.rs:1389:46
     |
1389 |         let first = ArchiveRow::from_reviews(&[review.clone()], &empty);
     |                                              ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&review)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:1937:9
     |
1937 |         outcome.failed = true;
     |         ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { failed: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:1936:9
     |
1936 |         let mut outcome = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:1959:9
     |
1959 |         outcome.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, watch_snapshot: WatchScan::default(), ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:1958:9
     |
1958 |         let mut outcome = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2008:9
     |
2008 |         live.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2007:9
     |
2007 |         let mut live = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2011:9
     |
2011 |         dry.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2010:9
     |
2010 |         let mut dry = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1313:13
     |
1313 |             &[thread.clone()],
     |             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1352:58
     |
1352 |         let mut watching = task(dir.path(), "job.md", 1, &[thread.clone()]);
     |                                                          ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1396:13
     |
1396 |             &[thread.clone()],
     |             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1430:13
     |
1430 |             &[thread.clone()],
     |             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1469:43
     |
1469 |             task(dir.path(), "job.md", 1, &[held_thread.clone()]),
     |                                           ^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&held_thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1470:44
     |
1470 |             task(dir.path(), "body.md", 1, &[fresh_thread.clone()]),
     |                                            ^^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&fresh_thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1580:45
     |
1580 |             ..task(dir.path(), "job.md", 1, &[thread.clone()])
     |                                             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1588:45
     |
1588 |             ..task(dir.path(), "job.md", 2, &[thread.clone()])
     |                                             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1641:13
     |
1641 |             &[old_thread.clone()],
     |             ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&old_thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1706:13
     |
1706 |             &[thread.clone()],
     |             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1756:13
     |
1756 |             &[thread.clone()],
     |             ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1816:17
     |
1816 |                 &[thread.clone()],
     |                 ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/gmail/sync/watch_apply.rs:1877:58
     |
1877 |         let mut watching = task(dir.path(), "job.md", 1, &[thread.clone()]);
     |                                                          ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&thread)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/gmail/worker.rs:275:17
    |
275 |                 assert_eq!(job.notes, [canonical_note.clone()]);
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

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
help: if you wanted a `Vec` that contains the entire range, try
    |
290 -         apply_emphasis(already_strong, &[strong_start..strong_end]),
290 +         apply_emphasis(already_strong, &(strong_start..strong_end).collect::<std::vec::Vec<usize>>()),
    |

warning: unnecessary use of `get(Path::new("orphan.md"))
                 .is_none()`
   --> src/native/notebooks/tests.rs:311:10
    |
311 |           .get(Path::new("orphan.md"))
    |  __________^
312 | |         .is_none());
    | |__________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
help: replace it with
    |
308 ~     assert!(!analysis
309 +         .graph
310 ~         .notebooks.contains_key(Path::new("orphan.md")));
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/ob.rs:538:58
    |
538 |             commit_paths(&vault, &env, "bracket change", &[bracketed.clone()])
    |                                                          ^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&bracketed)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

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
    --> src/native/pomodoro.rs:1010:51
     |
1010 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
     |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1754:51
     |
1754 |         assert_eq!(companions.source_ranges, Some(vec![20..35]));
     |                                                   ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1754 -         assert_eq!(companions.source_ranges, Some(vec![20..35]));
1754 +         assert_eq!(companions.source_ranges, Some((20..35).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 35, try
     |
1754 -         assert_eq!(companions.source_ranges, Some(vec![20..35]));
1754 +         assert_eq!(companions.source_ranges, Some(vec![20; 35]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1792:61
     |
1792 |         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
     |                                                             ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1792 -         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
1792 +         assert_eq!(result.properties[3].source_ranges, Some((40..43).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 43, try
     |
1792 -         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
1792 +         assert_eq!(result.properties[3].source_ranges, Some(vec![40; 43]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1853:58
     |
1853 |         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
     |                                                          ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1853 -         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
1853 +         assert_eq!(result.invalid[0].source_ranges, Some((12..20).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 20, try
     |
1853 -         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
1853 +         assert_eq!(result.invalid[0].source_ranges, Some(vec![12; 20]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1854:61
     |
1854 |         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
     |                                                             ^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1854 -         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
1854 +         assert_eq!(result.properties[2].source_ranges, Some((3..11).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 11, try
     |
1854 -         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
1854 +         assert_eq!(result.properties[2].source_ranges, Some(vec![3; 11]));
     |

warning: the `Err`-variant returned from this function is very large
   --> src/native/records/schema.rs:777:6
    |
777 | ) -> Result<RecordsConfig, RecordDiagnostic> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
    |
    = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/records/schema.rs:2127:29
     |
2127 |     fn parse(text: &str) -> Result<RecordsConfig, super::RecordDiagnostic> {
     |                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 240 bytes
     |
     = help: try reducing the size of `native::records::schema::RecordDiagnostic`, for example by boxing large elements or replacing it with `Box<native::records::schema::RecordDiagnostic>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this function has too many arguments (9/7)
  --> src/native/task_complete/tests/offer_close_tests.rs:21:1
   |
21 | / fn input<'a>(
22 | |     key: &'a str,
23 | |     path: &'a Path,
24 | |     line_index: usize,
...  |
30 | |     index: &'a crate::native::vault_links::NoteIndex,
31 | | ) -> OfferCloseInput<'a> {
   | |________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/task_complete/tests/offer_close_tests.rs:398:1
    |
398 | / fn fixture_input<'a>(
399 | |     key: &'a str,
400 | |     path: &'a Path,
401 | |     line_index: usize,
...   |
407 | |     index: &'a crate::native::vault_links::NoteIndex,
408 | | ) -> OfferCloseInput<'a> {
    | |________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:584:5
    |
584 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:372:9
    |
372 |     let mut files = Vec::with_capacity(markdown_files.len());
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

warning: call to `.clone()` on a reference in this situation does nothing
    --> src/native/records/render.rs:3454:26
     |
3454 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 836 warnings (740 duplicates)
error: could not compile `bob-obsidian` (lib test) due to 1 previous error; 836 warnings emitted
error: Recipe `check` failed on line 79 with exit code 101
failed  exit=101  duration=480079ms

