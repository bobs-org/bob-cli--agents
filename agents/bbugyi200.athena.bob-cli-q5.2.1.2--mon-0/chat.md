# Chat History - ace-run (bob-cli-q5.2.1.2--mon-0)

- **TIMESTAMP:** 2026-11-26 04:13:15 EST
- **MODEL:** codex/gpt-6-astra
- **AGENT:** bob-cli-q5.2.1.2--mon-0

## Prompt

sase monitor start --command 'python3 /tmp/q5-review-compare.py' --reason 'Rebuild corrected planned-today conformance tests, run the full gate, and reproduce all unrelated failures on clean base 1c23bce7 before closing bob-cli-q5.2.1.2'

## Response

sase tool run ef46807f496a338f934940a1949e320b
Running current-check on bbcae8e03383b33cae1efc21856c00488fe68e16: ['just', 'check']
current-check exit 101
test result: FAILED. 8183 passed; 43 failed; 5 ignored; 0 measured; 0 filtered out; finished in 48.88s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: FAILED. 4160 passed; 55 failed; 0 ignored; 0 measured; 0 filtered out; finished in 136.74s
test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.34s
test result: ok. 39 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.07s
test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.02s
test result: ok. 65 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.72s
test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.54s
test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s
test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s
test result: ok. 45 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.99s
test result: ok. 16 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s
test result: ok. 41 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.71s
test result: ok. 21 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.83s
test result: ok. 112 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 3.89s
test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.21s
test result: ok. 14 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.08s
test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.07s
test result: ok. 23 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s
test result: ok. 9 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.20s
test result: ok. 52 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.47s
test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.26s
test result: ok. 26 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.17s
test result: ok. 61 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 14.76s
test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 4.88s
test result: ok. 3 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.26s
test result: ok. 13 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.95s
test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.63s
test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.35s
test result: ok. 11 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.81s
test result: ok. 71 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.15s
test result: ok. 49 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 9.32s
test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.15s
test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.58s
test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.41s
test result: ok. 33 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.19s
test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s
HEAD is now at 1c23bce7 feat(ties): PT12 CRLF vectors, missing LR31 skips, whole-JSON LR35
Running base-tests on 1c23bce7a8a0024e7874f0955bee104f4207870c: ['cargo', 'test', '--lib', '--test', 'cli', '--no-fail-fast']
base-tests exit 101
test result: FAILED. 8180 passed; 43 failed; 5 ignored; 0 measured; 0 filtered out; finished in 47.46s
test result: FAILED. 4156 passed; 55 failed; 0 ignored; 0 measured; 0 filtered out; finished in 140.65s
Previous HEAD position was 1c23bce7 feat(ties): PT12 CRLF vectors, missing LR31 skips, whole-JSON LR35
Switched to branch 'master'
Your branch is up to date with 'origin/master'.
{
  "base": "1c23bce7",
  "checks": [
    {
      "name": "current-check",
      "command": [
        "just",
        "check"
      ],
      "exit_code": 101,
      "log": "/tmp/q5-review-compare-current-check.log",
      "summaries": [
        "test result: FAILED. 8183 passed; 43 failed; 5 ignored; 0 measured; 0 filtered out; finished in 48.88s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: FAILED. 4160 passed; 55 failed; 0 ignored; 0 measured; 0 filtered out; finished in 136.74s",
        "test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.34s",
        "test result: ok. 39 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.07s",
        "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.02s",
        "test result: ok. 65 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.72s",
        "test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.54s",
        "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s",
        "test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s",
        "test result: ok. 45 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.99s",
        "test result: ok. 16 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s",
        "test result: ok. 41 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.71s",
        "test result: ok. 21 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.83s",
        "test result: ok. 112 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 3.89s",
        "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.21s",
        "test result: ok. 14 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.08s",
        "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.07s",
        "test result: ok. 23 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s",
        "test result: ok. 9 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.20s",
        "test result: ok. 52 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.47s",
        "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.26s",
        "test result: ok. 26 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.17s",
        "test result: ok. 61 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 14.76s",
        "test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 4.88s",
        "test result: ok. 3 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.26s",
        "test result: ok. 13 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.95s",
        "test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.63s",
        "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.35s",
        "test result: ok. 11 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.81s",
        "test result: ok. 71 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.15s",
        "test result: ok. 49 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 9.32s",
        "test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.15s",
        "test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.58s",
        "test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.41s",
        "test result: ok. 33 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.19s",
        "test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
        "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s"
      ]
    },
    {
      "name": "base-tests",
      "command": [
        "cargo",
        "test",
        "--lib",
        "--test",
        "cli",
        "--no-fail-fast"
      ],
      "exit_code": 101,
      "log": "/tmp/q5-review-compare-base-tests.log",
      "summaries": [
        "test result: FAILED. 8180 passed; 43 failed; 5 ignored; 0 measured; 0 filtered out; finished in 47.46s",
        "test result: FAILED. 4156 passed; 55 failed; 0 ignored; 0 measured; 0 filtered out; finished in 140.65s"
      ]
    }
  ],
  "implementation_head": "bbcae8e03383b33cae1efc21856c00488fe68e16",
  "restore_branch": "master",
  "verified_clean_base": "1c23bce7a8a0024e7874f0955bee104f4207870c",
  "restored_head": "bbcae8e03383b33cae1efc21856c00488fe68e16",
  "current_failure_count": 98,
  "base_failure_count": 98,
  "identical_failure_names": [
    "capture::authored::capture_drawer_authored_children_and_composition",
    "capture::clip::clipboard_drawer_lookalikes_stay_notes_on_new_and_req_owning_tasks",
    "capture::clip_notes::clip_notes_drawers_and_prj_sections",
    "capture::complete_drawers::bullet_menu_continuation_depends_on_what_follows_the_token",
    "capture::complete_drawers::bullet_menu_human_output_shows_the_title_line_only",
    "capture::complete_drawers::bullet_menu_json_pins_the_target_bold_titles_and_the_continuation",
    "capture::complete_drawers::bullet_menu_on_new_tasks_and_project_notes_carries_the_new_target",
    "capture::complete_drawers::drawer_menu_human_output_lists_bobs_detail_and_refusals",
    "capture::complete_drawers::empty_drawer_menu_json_pins_groups_fields_and_the_unselected_open",
    "capture::complete_drawers::quoted_drawer_literals_decode_the_query_and_cover_the_quotes",
    "capture::complete_drawers::refused_rows_name_the_commits_reason",
    "capture::complete_drawers::target_run_completion_crosses_schedule_and_clipboard_tokens",
    "capture::complete_drawers::typed_drawer_menu_filters_groups_and_drops_the_unselected_open",
    "capture::complete_editor::capture_complete_drawer_json_covers_components_and_warnings",
    "capture::complete_transfer::transfer_drawer_destination_lists_task_drawers",
    "capture::drawer_bullets::punctuated_drawer_merges_into_the_existing_drawer",
    "capture::drawer_bullets::uppercase_container_drafts_remain_ordinary_notes",
    "capture::inbox_route::ir_dependency_touch_follows_its_routed_task",
    "capture::inbox_route::ir_routed_link_moves_with_repair_stamp_follow_and_open_notes",
    "capture::multi_target::a_glued_drawer_suffix_stays_local_to_its_target",
    "capture::multi_target::note_less_bullets_and_drawers_are_filed_to_each_member",
    "capture::multi_target::repeated_near_catalog_warnings_are_reported_once_per_target_run",
    "capture::note_bullets::childless_literal_matching_existing_drawer_is_refused",
    "capture::note_bullets::worked_example_files_notes_drawers_json_and_human",
    "capture::note_pull::np16_inbox_choice_and_routed_pick_match_cli_fixtures",
    "capture::note_pull::np2_pick_all_matches_cli_json_and_human_fixtures",
    "capture::note_pull::np_move_groups_follow_requested_sources_in_cli_fixtures",
    "capture::project_note::capture_move_landing_repairs_moved_reports_after_child_edits",
    "capture::project_note::capture_project_note_choice_answers_match_authored_bullets",
    "capture::project_note::capture_project_note_task_links_write_the_worked_example",
    "capture::project_note_offer::offer_duplicate_picks_without_later_context_keep_every_offer",
    "capture::project_note_offer::offer_equal_descriptions_stay_distinct_from_an_authored_id_twin",
    "capture::project_note_offer::offer_picking_several_duplicates_keeps_the_rest_and_matches_authored",
    "capture::project_note_offer::offer_selected_pick_keeps_frozen_identity_across_line_shift",
    "capture::project_note_offer::offer_three_equal_descriptions_survive_picking_first_middle_or_last",
    "capture::project_note_offer::offer_two_equal_descriptions_survive_picking_the_first_or_last",
    "capture::reqs_existing::req_only_capture_keeps_notes_drawer_nonempty_and_existing_reqs_append",
    "capture::retype_closeout::near_duplicate_teaches_requested_override_and_creates_it",
    "capture::sections::capture_drawer_errors_leave_the_note_unchanged",
    "capture::sections::capture_drawer_indent_units_crlf_and_dry_run",
    "capture::sections::capture_drawer_inserts_into_first_middle_and_last_sections",
    "capture::sections::capture_drawer_managed_log_geometry",
    "capture::sections::capture_drawer_prefix_vs_whole_slug_and_multiword",
    "capture::sections::capture_forced_drawer_matches_title_exactly",
    "capture::task_theme_writes::new_named_task_reports_and_writes_the_resolved_theme_exception",
    "capture::transfer::transfer_merge_refusals_are_atomic_and_coded",
    "completion::bash::bash_keeps_spaces_in_one_argument",
    "completion::bash::bash_readline_inserts_what_bob_returned",
    "completion::capture_text::drawers_complete_after_id_hash",
    "completion::vault::drawers_offer_exact_titles",
    "help_options::capture_drawers_help_lists_options_alphabetically",
    "native::capture::block_diff::tests::annotate_drawer_lines_uses_after_snapshot_except_removed",
    "native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two",
    "native::capture_clip::tests::clipboard_items_that_look_like_drawers_are_escaped_after_rendering",
    "native::capture_complete::tests::drawers::a_task_without_drawers_lists_recent_and_new_only",
    "native::capture_complete::tests::drawers::bullet_menu_filters_by_the_typed_name_and_decodes_a_quoted_literal",
    "native::capture_complete::tests::drawers::bullet_menu_on_a_new_project_note_preserves_section_titles",
    "native::capture_complete::tests::drawers::bullet_menu_on_a_new_task_offers_recent_and_new_rows_only",
    "native::capture_complete::tests::drawers::bullet_menu_on_a_prj_task_lists_sections_and_refuses_structural_ones",
    "native::capture_complete::tests::drawers::bullet_menu_on_an_existing_task_offers_bold_titles_with_the_glued_copy",
    "native::capture_complete::tests::drawers::bullet_replacement_continues_with_a_nested_bullet_only_when_nothing_follows",
    "native::capture_complete::tests::drawers::bullet_rows_refuse_with_the_exact_resolvers_reason",
    "native::capture_complete::tests::drawers::empty_query_lists_task_then_recent_rows_and_opens_unselected",
    "native::capture_complete::tests::drawers::empty_query_recent_is_capped_at_eight_keys",
    "native::capture_complete::tests::drawers::menu_rows_agree_with_the_resolver_for_every_row_kind",
    "native::capture_complete::tests::drawers::new_row_hints_at_a_near_catalog_key",
    "native::capture_complete::tests::drawers::new_row_needs_a_typed_name_no_other_row_claims",
    "native::capture_complete::tests::drawers::project_note_prj_target_lists_sections_and_creates_title_case_sections",
    "native::capture_complete::tests::drawers::punctuated_drawer_lists_under_task_with_exact_slug_reach",
    "native::capture_complete::tests::drawers::recent_rows_are_catalog_keys_the_task_lacks",
    "native::capture_complete::tests::drawers::refused_rows_carry_the_commit_resolvers_reason",
    "native::capture_complete::tests::drawers::replacement_covers_the_hash_and_the_name_and_reports_cursor_after",
    "native::capture_complete::tests::drawers::replacement_is_a_slug_only_when_it_resolves_back_to_the_same_drawer",
    "native::capture_complete::tests::drawers::rows_rank_prefix_before_substring_in_document_order",
    "native::capture_complete::tests::drawers::shell_drawer_rows_are_the_targets_own_unrefused_drawers",
    "native::capture_complete::tests::drawers::task_rows_carry_counts_singular_plural_detail_and_consequences",
    "native::capture_complete::tests::drawers::typed_query_drops_the_unselected_open_and_filters_every_group",
    "native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts",
    "native::capture_drawers::tests::json_success_shape_and_key_order_are_stable",
    "native::gcal::description::bullets::tests::bullet_vectors",
    "native::gcal::description::bullets::tests::punctuated_drawer_shaped_lines_are_defused",
    "native::gkeep::render::tests::image_with_ocr_renders_attachment_line_and_grandchildren",
    "native::gmail::body::inert::tests::whole_bold_and_legacy_list_items_are_defused_as_imported_children",
    "native::meetings::profile::tests::wispr_summary_renders_one_or_two_pages_with_stable_words",
    "native::task_block_layout::tests::a_created_notes_drawer_lands_first_among_the_drawers",
    "native::task_block_layout::tests::canonicalize_new_req_block_files_notes_and_keeps_req_subtrees",
    "native::task_block_layout::tests::zones_name_every_task_child_kind",
    "native::task_children::tests::classifies_managed_links_logs_drawers_and_nested_tasks",
    "native::task_drawer_rename::tests::fences_quotes_and_stray_bullets_are_excluded",
    "native::task_drawer_rename::tests::nested_owners_report_their_original_lines",
    "native::task_merge::tests::task_drawers_and_project_h2_drawers_resolve_for_merge",
    "native::task_reqs::tests::child_kind_detects_requirements_before_authored",
    "native::task_tidy::tests::a_canonical_note_plans_nothing",
    "native::task_tidy::tests::legacy_notes_header_is_reused_and_never_respelled",
    "ref_library::today::today_matches_unnamed_capture_and_named_capture_remembers_theme",
    "task_drawer_rename::apply_commits_once_and_a_rerun_reports_nothing",
    "task_drawer_rename::bare_run_is_a_dry_run_with_an_inventory",
    "task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses"
  ],
  "changed_failure_names": [],
  "new_failure_names": [],
  "base_only_failure_names": [],
  "regression_passed": true,
  "current_test_summaries": [
    "test result: FAILED. 8183 passed; 43 failed; 5 ignored; 0 measured; 0 filtered out; finished in 48.88s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: FAILED. 4160 passed; 55 failed; 0 ignored; 0 measured; 0 filtered out; finished in 136.74s",
    "test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.34s",
    "test result: ok. 39 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.07s",
    "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.02s",
    "test result: ok. 65 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.72s",
    "test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.54s",
    "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s",
    "test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s",
    "test result: ok. 45 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.99s",
    "test result: ok. 16 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.86s",
    "test result: ok. 41 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.71s",
    "test result: ok. 21 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.83s",
    "test result: ok. 112 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 3.89s",
    "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.21s",
    "test result: ok. 14 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.08s",
    "test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.07s",
    "test result: ok. 23 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.12s",
    "test result: ok. 9 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.20s",
    "test result: ok. 52 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.47s",
    "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.26s",
    "test result: ok. 26 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.17s",
    "test result: ok. 61 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 14.76s",
    "test result: ok. 4 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 4.88s",
    "test result: ok. 3 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.26s",
    "test result: ok. 13 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.95s",
    "test result: ok. 2 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.63s",
    "test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.35s",
    "test result: ok. 11 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.81s",
    "test result: ok. 71 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.15s",
    "test result: ok. 49 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 9.32s",
    "test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.15s",
    "test result: ok. 5 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.58s",
    "test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.41s",
    "test result: ok. 33 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.19s",
    "test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s",
    "test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s"
  ],
  "comparison_passed": true
}
succeeded  exit=0  duration=665599ms

