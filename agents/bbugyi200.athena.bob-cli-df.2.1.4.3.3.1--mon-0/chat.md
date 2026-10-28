# Chat History - ace-run (bob-cli-df.2.1.4.3.3.1--mon-0)

- **TIMESTAMP:** 2026-10-28 07:34:28 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-df.2.1.4.3.3.1--mon-0

## Prompt

sase monitor start --command "sh -c 'just test -p sase_core artifact_link && just test -p sase_core_py artifact_link_collision_bindings_round_trip'" --reason 'Rerun the artifact-link collision and PyO3 binding regressions after fixing the ownership error'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
./scripts/check.sh test -p sase_core artifact_link
   Compiling libc v0.2.186
   Compiling cfg-if v1.0.4
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling memchr v2.8.0
   Compiling zerocopy v0.8.48
   Compiling find-msvc-tools v0.1.9
   Compiling shlex v1.3.0
   Compiling serde_core v1.0.228
   Compiling regex-syntax v0.8.10
   Compiling crossbeam-utils v0.8.21
   Compiling version_check v0.9.5
   Compiling siphasher v1.0.4
   Compiling log v0.4.29
   Compiling serde v1.0.228
   Compiling autocfg v1.5.0
   Compiling once_cell v1.21.4
   Compiling bitflags v2.11.1
   Compiling crossbeam-epoch v0.9.21
   Compiling equivalent v1.0.2
   Compiling hashbrown v0.17.0
   Compiling crossbeam-deque v0.8.8
   Compiling zmij v1.0.21
   Compiling ucd-trie v0.1.7
   Compiling itoa v1.0.18
   Compiling serde_json v1.0.149
   Compiling iana-time-zone v0.1.65
   Compiling same-file v1.0.6
   Compiling libm v0.2.16
   Compiling smallvec v1.15.1
   Compiling typenum v1.20.0
   Compiling pin-project-lite v0.2.17
   Compiling lazy_static v1.5.0
   Compiling deunicode v1.6.2
   Compiling futures-sink v0.3.32
   Compiling futures-core v0.3.32
   Compiling parking_lot_core v0.9.12
   Compiling anstyle v1.0.14
   Compiling scopeguard v1.2.0
   Compiling pkg-config v0.3.33
   Compiling heck v0.5.0
   Compiling percent-encoding v2.3.2
   Compiling vcpkg v0.2.15
   Compiling bytes v1.11.1
   Compiling thiserror v1.0.69
   Compiling unicode-segmentation v1.13.3
   Compiling rayon-core v1.13.0
   Compiling either v1.19.0
   Compiling clap_lex v1.1.1
   Compiling slab v0.4.12
   Compiling futures-io v0.3.32
   Compiling futures-task v0.3.32
   Compiling winnow v1.0.4
   Compiling getrandom v0.4.2
   Compiling rustix v1.1.4
   Compiling linux-raw-sys v0.12.1
   Compiling winnow v0.7.15
   Compiling tower-service v0.3.3
   Compiling toml_writer v1.1.3+spec-1.1.0
   Compiling home v0.5.12
   Compiling sync_wrapper v1.0.2
   Compiling cpufeatures v0.2.17
   Compiling tower-layer v0.3.3
   Compiling fallible-streaming-iterator v0.1.9
   Compiling tinyvec v1.13.3
   Compiling fastrand v2.4.1
   Compiling fallible-iterator v0.3.0
   Compiling ryu v1.0.23
   Compiling unsafe-libyaml v0.2.11
   Compiling unicode-width v0.2.2
   Compiling hex v0.4.3
   Compiling unicode-casefold v0.2.0
   Compiling semver v1.0.28
   Compiling tracing-core v0.1.36
   Compiling generic-array v0.14.7
   Compiling ahash v0.8.12
   Compiling phf_shared v0.11.3
   Compiling num-traits v0.2.19
   Compiling aho-corasick v1.1.4
   Compiling bstr v1.13.1
   Compiling grep-matcher v0.1.9
   Compiling walkdir v2.5.0
   Compiling encoding_rs v0.8.35
   Compiling cc v1.2.61
   Compiling colored v2.2.0
   Compiling etcetera v0.8.0
   Compiling slug v0.1.6
   Compiling futures-channel v0.3.32
   Compiling lock_api v0.4.14
   Compiling toml_parser v1.1.5+spec-1.1.0
   Compiling clap_builder v4.6.7
   Compiling indexmap v2.14.0
   Compiling itertools v0.11.0
   Compiling crossbeam-channel v0.5.17
   Compiling unicode-normalization v0.1.25
   Compiling phf v0.11.3
   Compiling humansize v2.1.3
   Compiling getrandom v0.2.17
   Compiling errno v0.3.14
   Compiling socket2 v0.6.3
   Compiling mio v1.2.0
   Compiling memmap2 v0.9.11
   Compiling term_size v0.3.2
   Compiling fs2 v0.4.3
   Compiling chrono v0.4.44
   Compiling regex-automata v0.4.14
   Compiling psm v0.1.24
   Compiling stacker v0.1.25
   Compiling libsqlite3-sys v0.30.1
   Compiling crypto-common v0.1.7
   Compiling block-buffer v0.10.4
   Compiling encoding_rs_io v0.1.8
   Compiling signal-hook-registry v1.4.8
   Compiling toml_datetime v0.7.5+spec-1.1.0
   Compiling serde_spanned v1.1.2
   Compiling rand_core v0.6.4
   Compiling parking_lot v0.12.5
   Compiling digest v0.10.7
   Compiling tempfile v3.27.0
   Compiling grep-searcher v0.1.17
   Compiling toml v0.9.12+spec-1.1.0
   Compiling sha1 v0.10.7
   Compiling sha2 v0.10.9
   Compiling ppv-lite86 v0.2.21
   Compiling pest v2.9.4
   Compiling syn v2.0.117
   Compiling syn v3.0.9
   Compiling rayon v1.12.0
   Compiling hashbrown v0.14.5
   Compiling rand_chacha v0.3.1
   Compiling rand v0.8.6
   Compiling hashlink v0.9.1
   Compiling pest_meta v2.9.4
   Compiling phf_generator v0.11.3
   Compiling regex v1.12.3
   Compiling globset v0.4.19
   Compiling phf_codegen v0.11.3
   Compiling parse-zoneinfo v0.3.1
   Compiling ignore v0.4.32
   Compiling chrono-tz-build v0.3.0
   Compiling pest_generator v2.9.4
   Compiling clap_derive v4.6.7
   Compiling derive_arbitrary v1.5.0
   Compiling chrono-tz v0.9.0
   Compiling globwalk v0.9.1
   Compiling arbitrary v1.5.0
   Compiling serde_derive v1.0.228
   Compiling tokio-macros v2.7.0
   Compiling thiserror-impl v1.0.69
   Compiling tracing-attributes v0.1.31
   Compiling futures-macro v0.3.32
   Compiling pest_derive v2.9.4
   Compiling tokio v1.52.2
   Compiling futures-util v0.3.32
   Compiling clap v4.6.7
   Compiling rusqlite v0.32.1
   Compiling tracing v0.1.44
   Compiling clap-cargo v0.18.3
   Compiling table_formatter v0.6.1
   Compiling json5 v0.4.1
   Compiling dashmap v6.1.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tera v1.20.1
   Compiling sase_workspace_hack v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/external/gh/sase-org/sase-core/crates/sase_workspace_hack)
   Compiling tower v0.5.3
   Compiling tokio-util v0.7.18
   Compiling tokei v15.0.0
   Compiling sase_core v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/sase/repos/external/gh/sase-org/sase-core/crates/sase_core)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2m 46s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws14-261028_072532/build/debug/deps/sase_core-c3182504540c81bb)

running 157 tests
test artifact_link::collision::tests::invalid_individual_events_still_error ... ok
test artifact_link::collision::tests::malformed_complete_history_timestamp_is_a_validation_error ... ok
test artifact_link::collision::tests::exact_retries_collapse_without_quarantine ... ok
test artifact_link::collision::tests::distinct_operations_are_both_accepted ... ok
test artifact_link::collision::tests::durable_beats_incoming_regardless_of_created_at ... ok
test artifact_link::collision::tests::durable_beats_pending_replay ... ok
test artifact_link::collision::tests::missing_evidence_falls_back_to_digest_tie_break ... ok
test artifact_link::collision::tests::established_evidence_beats_missing_evidence ... ok
test artifact_link::collision::tests::historical_commit_time_compares_actual_instants_across_offsets ... ok
test artifact_link::collision::tests::equal_instants_use_digest_tie_break ... ok
test artifact_link::collision::tests::historical_commit_time_orders_independent_histories ... ok
test artifact_link::collision::tests::equivalent_timestamp_spellings_use_the_unordered_digest_tie_break ... ok
test artifact_link::collision::tests::duplicate_root_ancestry_is_retained_for_complete_group_selection ... ok
test artifact_link::collision::tests::admission_sequence_orders_local_only_objects ... ok
test artifact_link::collision::tests::historical_original_wins_with_identical_timestamps ... ok
test artifact_link::collision::tests::same_commit_with_conflicting_instants_is_rejected ... ok
test artifact_link::collision::tests::strict_reducer_still_rejects_operation_id_collisions ... ok
test artifact_link::collision::tests::three_payloads_produce_one_accepted_and_two_findings ... ok
test artifact_link::collision::tests::same_payload_ancestor_evidence_still_rejects_a_competitor_descendant ... ok
test artifact_link::collision::tests::identical_digest_copies_keep_the_earliest_history_across_roots ... ok
test artifact_link::collision::tests::rejected_put_cannot_supersede_accepted_observation ... ok
test artifact_link::cutover::tests::attestation_is_stable_and_head_sensitive ... ok
test artifact_link::collision::tests::quarantine_record_path_validate_and_canonicalize ... ok
test artifact_link::collision::tests::multi_generation_identical_copies_do_not_outvote_their_earliest_history ... ok
test artifact_link::collision::tests::interleaved_duplicate_copies_do_not_change_copy_chronology_winner ... ok
test artifact_link::collision::tests::copy_chronology_with_three_distinct_payloads_selects_earliest_survivor ... ok
test artifact_link::events::tests::alias_chains_resolve_edges_and_cycles_or_conflicts_fail ... ok
test artifact_link::cutover::tests::import_identity_is_order_stable_and_head_sensitive ... ok
test artifact_link::collision::tests::same_commit_evidence_uses_digest_tie_break ... ok
test artifact_link::collision::tests::same_payload_descendant_uses_surviving_offset_instants_for_ties ... ok
test artifact_link::cutover::tests::marker_round_trips_with_canonical_json ... ok
test artifact_link::cutover::tests::classifies_and_converts_legacy_outbox_lines ... ok
test artifact_link::events::tests::bytes_validation_rejects_floats_and_path_mismatches ... ok
test artifact_link::cutover::tests::progress_walks_recovery_phases ... ok
test artifact_link::events::tests::baseline_imports_preserve_counts_and_are_one_shot_by_import_id ... ok
test artifact_link::events::tests::event_edge_identity_normalizes_directed_and_undirected_relations ... ok
test artifact_link::collision::tests::group_basis_uses_the_same_surviving_order_as_winner_selection ... FAILED
test artifact_link::events::tests::edge_put_supersedes_named_versions_and_uses_lexical_tie_break ... ok
test artifact_link::cutover::tests::read_state_reports_four_states ... ok
test artifact_link::events::tests::predecessor_ids_known_on_other_edges_are_rejected ... ok
test artifact_link::events::tests::reduction_rejects_operation_id_collisions ... ok
test artifact_link::events::tests::stable_background_producer_contract_is_replay_stable ... ok
test artifact_link::events::tests::reduction_deduplicates_exact_retries_but_counts_distinct_observations ... ok
test artifact_link::events::tests::validation_rejects_bad_identifiers_payloads_and_edges ... ok
test artifact_link::events::tests::remove_before_add_removes_only_observed_versions ... ok
test artifact_link::index::tests::empty_and_malformed_rows_do_not_reject_the_snapshot ... ok
test artifact_link::index::tests::colliding_agent_alias_resolves_to_earliest_row_in_row_order ... ok
test artifact_link::events::tests::canonical_json_digest_and_path_are_byte_stable ... ok
test artifact_link::collision::tests::permutations_and_duplicate_roots_are_stable ... ok
test artifact_link::collision::tests::same_payload_descendant_clock_does_not_replace_earliest_history ... FAILED
test artifact_link::events::tests::reduction_is_stable_for_reordered_and_duplicated_deliveries ... ok
test artifact_link::inlet::tests::mapping_links_value_is_unrecognized ... ok
test artifact_link::inlet::tests::no_frontmatter_is_absent ... ok
test artifact_link::inlet::tests::empty_list_is_entries ... ok
test artifact_link::inlet::tests::matching_shape_is_entries ... ok
test artifact_link::inlet::tests::mkdocs_label_path_is_unrecognized ... ok
test artifact_link::inlet::tests::missing_key_is_absent ... ok
test artifact_link::index::tests::tolerant_duplicate_winner_uses_legacy_counts_and_edges_keep_first_row ... ok
test artifact_link::collision::tests::rejected_kinds_cannot_affect_accepted_reduction ... ok
test artifact_link::collision::tests::complete_group_selection_eliminates_descendants_before_time_ordering ... ok
test artifact_link::collision::tests::later_identical_copy_descending_from_competitor_preserves_earliest_history ... ok
test artifact_link::ownership::tests::baseline_import_rows_contribute_document_owners ... ok
test artifact_link::ownership::tests::owner_requirements_partition_and_dedupe_event_refs ... ok
test artifact_link::index::tests::tolerant_string_fields_match_legacy_python_str ... ok
test artifact_link::merge::tests::validates_schema_artifact_ref_and_duplicates ... ok
test artifact_link::path::tests::bead_page_uses_readme_for_lineage_root ... ok
test artifact_link::ownership::tests::receipt_accepts_local_or_bead_durable_owners ... ok
test artifact_link::merge::tests::rejects_competing_same_key_edits_and_modify_delete ... ok
test artifact_link::merge::tests::accepts_one_sided_and_identical_deletes ... ok
test artifact_link::ownership::tests::receipt_requires_resolved_roots_and_durable_receipts ... ok
test artifact_link::merge::tests::accepts_one_sided_and_identical_edits ... ok
test artifact_link::path::tests::published_markdown_file_is_itself ... ok
test artifact_link::merge::tests::merge_is_idempotent ... ok
test artifact_link::path::tests::unpublished_file_uses_local_pages_dir ... ok
test artifact_link::publication_retry::tests::deferred_attempt_does_not_consume_failure_backoff ... ok
test artifact_link::publication_retry::tests::due_policy_reports_retry_after_and_aging_warning ... ok
test artifact_link::publication_retry::tests::failed_attempts_exponentially_back_off_at_six_hours ... ok
test artifact_link::ownership::tests::receipt_rejects_schema_or_operation_mismatches ... ok
test artifact_link::relation::tests::awaits_is_a_projection_only_agent_to_bead_relation ... ok
test artifact_link::merge::tests::unions_distinct_additions_in_deterministic_order_after_base_rows ... ok
test artifact_link::relation::tests::every_builtin_documents_direction_and_examples ... ok
test artifact_link::relation::tests::implements_settles_the_plan_bead_direction ... ok
test artifact_link::relation::tests::inverse_label_is_from_this_document ... ok
test artifact_link::relation::tests::produced_by_covers_stitch_and_bead_sources ... ok
test artifact_link::relation::tests::reserved_slugs_point_at_bead_dep ... ok
test artifact_link::relation::tests::unknown_slug_lists_builtins ... ok
test artifact_link::index::tests::empty_lookup_keys_yield_no_rows ... ok
test artifact_link::index::tests::missing_ref_is_absent_not_indexed_non_selectable ... ok
test artifact_link::ownership::tests::receipt_classifies_per_endpoint_outcomes ... ok
test artifact_link::row_resolution::tests::guards_do_not_resolve_virtual_or_malformed_refs ... ok
test artifact_link::wire::tests::canonicalize_strips_sigil_and_rewrites_kind_aliases ... ok
test artifact_link::path::tests::stitch_has_no_markdown_file ... ok
test artifact_link::index::tests::neighbor_target_uses_row_project_not_first_indexed_target ... ok
test artifact_link::publication_retry::tests::pending_registration_preserves_age_across_head_changes ... ok
test artifact_link::wire::tests::reserved_slugs_are_not_stored ... ok
test artifact_link::wire::tests::directed_same_pair_may_carry_several_relations ... ok
test artifact_link::wire::tests::prompt_ref_rewrite_increments_uses_and_keeps_created_at ... ok
test artifact_link::wire::tests::validate_rejects_multiline_and_overlong_descriptions ... ok
test artifact_link::wire::tests::validate_rejects_self_links_and_blank_descriptions ... ok
test artifact_link_eligibility::policy::tests::a_real_change_makes_its_repo_qualify ... ok
test artifact_link::wire::tests::undirected_related_dedups_either_direction ... ok
test artifact_link_eligibility::policy::tests::bookkeeping_only_repos_are_ineligible ... ok
test artifact_link_eligibility::policy::tests::empty_repos_are_ineligible ... ok
test artifact_link_eligibility::policy::tests::rejects_blank_run_id ... ok
test artifact_link::relation::tests::builtins_cover_v1_table ... ok
test artifact_link_eligibility::policy::tests::rejects_unsupported_schema_version ... ok
test artifact_link::row_resolution::tests::parse_link_ref_parts_strips_aliases_sigil_and_fragment ... ok
test artifact_link_eligibility::policy::tests::release_evidence_rejects_a_different_agent_in_the_same_session ... ok
test artifact_link::relation::tests::produced_by_and_launched_round_trip ... ok
test artifact_link::index::tests::parity_fixture_alias_collision_does_not_shadow_canonical ... ok
test artifact_link::index::tests::native_build_and_selected_query_are_measurable ... ok
test artifact_link::index::tests::parity_fixture_self_edge_and_projected_writability ... ok
test artifact_link::path::tests::companion_uses_stem_and_disambiguates_on_collision ... ok
test artifact_link::index::tests::tolerant_uses_match_legacy_truthiness_truncation_and_strings ... ok
test artifact_link::path::tests::document_kind_is_itself ... ok
test artifact_link::row_resolution::tests::resolver_matches_key_probe_equivalence ... ok
test plan::artifact_link::tests::bead_section_supports_linked_unlinked_and_prettier_wrapped_labels ... ok
test plan::artifact_link::tests::extra_leading_blank_line_is_recognized_as_noncanonical_layout ... ok
test plan::artifact_link::tests::known_header_labels_after_body_content_are_ordinary_bullets ... ok
test plan::artifact_link::tests::fenced_header_example_is_not_a_live_document_header ... ok
test plan::artifact_link::tests::escapes_labels_and_trailing_text ... ok
test artifact_link::path::tests::goal_has_no_markdown_file ... ok
test artifact_link::row_resolution::tests::project_hint_precedes_deterministic_fallback ... ok
test plan::artifact_link::tests::ordinary_bold_and_nested_body_bullets_are_not_header_sections ... ok
test artifact_link::index::tests::project_query_preserves_first_row_patch_edges ... ok
test artifact_link_eligibility::policy::tests::release_evidence_rejects_a_different_run_id ... ok
test plan::artifact_link::tests::parses_prettier_wrapped_commit_and_preserves_unchanged_bytes ... ok
test plan::artifact_link::tests::rejects_malformed_duplicate_unknown_and_unterminated_documents ... ok
test plan::artifact_link::tests::legacy_upsert_preserves_frontmatter_body_and_other_sections ... ok
test plan::artifact_link::tests::remove_section_keeps_the_rest_and_canonical_layout ... ok
test artifact_link_eligibility::policy::tests::release_evidence_requires_eligible_decision ... ok
test plan::artifact_link::tests::plan_and_prompt_sections_accept_absolute_cross_repo_targets ... ok
test artifact_link_eligibility::policy::tests::release_evidence_round_trips_and_validates_against_the_same_run ... ok
test artifact_link_eligibility::policy::tests::serde_rejects_unknown_change_role ... ok
test artifact_link_eligibility::policy::tests::serde_round_trips_the_decision_wire ... ok
test artifact_link_eligibility::policy::tests::serde_rejects_unknown_fields ... ok
test plan::artifact_link::tests::artifacts_is_compatible_with_either_counterpart_section ... ok
test plan::artifact_link::tests::artifacts_is_list_shaped_and_orders_between_agents_and_commits ... ok
test artifact_link::index::tests::parity_fixture_first_wins_equal_uses_and_max_uses_unequal ... ok
test plan::artifact_link::tests::back_compat_single_legacy_and_mixed_cases ... ok
test artifact_link::index::tests::parity_fixture_skips_empty_refs_and_keeps_malformed_endpoints ... ok
test plan::artifact_link::tests::empty_list_section_is_omitted ... ok
test plan::artifact_link::tests::discontiguous_header_groups_before_body_content_are_invalid ... ok
test plan::artifact_link::tests::multi_section_round_trip_uses_fixed_order ... ok
test plan::artifact_link::tests::bead_upsert_keeps_bead_frontmatter ... ok
test artifact_link::row_resolution::tests::resolves_class_a_row_identity_shapes ... ok
test plan::artifact_link::tests::list_cap_is_visible_and_round_trips_logically ... ok
test plan::artifact_link::tests::title_before_header_means_the_bullet_is_body_content ... ok
test plan::artifact_link::tests::parent_upsert_removes_only_legacy_top_level_parent ... ok
test artifact_link::index::tests::frozen_handle_supports_concurrent_reads ... ok
test artifact_link::managed_table::tests::links_skip_host_document_reference_labels ... ok
test artifact_link::managed_table::tests::links_render_sorts_and_emits_pointer ... ok
test artifact_link::managed_table::tests::links_upsert_is_top_anchored_and_idempotent ... ok
test artifact_link::managed_table::tests::empty_links_table_removes_the_block ... ok
test artifact_link::managed_table::tests::links_after_plan_header_does_not_trip_header_invalid ... ok
test artifact_link::index::tests::parity_fixture_pins_every_link_chip_and_target_field ... ok
test artifact_link::index::tests::rows_and_project_do_not_scan_unrelated_rows ... ok

failures:

---- artifact_link::collision::tests::group_basis_uses_the_same_surviving_order_as_winner_selection stdout ----

thread 'artifact_link::collision::tests::group_basis_uses_the_same_surviving_order_as_winner_selection' (3149056) panicked at crates/sase_core/src/artifact_link/collision/tests.rs:859:5:
assertion `left == right` failed
  left: "403640fb6141c2af29c18cd15116a4099c4f36d5bad46828d7348b6ceb655e65"
 right: "513001cd571b62d11f24864b4b101a00f8a018dafe62be06851ffb5e4dd58f4d"
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace

---- artifact_link::collision::tests::same_payload_descendant_clock_does_not_replace_earliest_history stdout ----

thread 'artifact_link::collision::tests::same_payload_descendant_clock_does_not_replace_earliest_history' (3149075) panicked at crates/sase_core/src/artifact_link/collision/tests.rs:641:5:
assertion `left == right` failed
  left: ArtifactLinkCollisionPartitionWire { schema_version: 1, accepted: [ArtifactLinkCollisionOutcomeWire { digest: "5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/competitor.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:relabeled-2") }], groups: [ArtifactLinkCollisionGroupWire { project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", accepted: ArtifactLinkCollisionOutcomeWire { digest: "5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/competitor.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:relabeled-2") }, rejected: [ArtifactLinkCollisionFindingWire { digest: "403640fb6141c2af29c18cd15116a4099c4f36d5bad46828d7348b6ceb655e65", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/repeated.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:relabeled-0"), basis: HistoricalCommitTimeWins, detail: "earlier first-add 5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd wins over 403640fb6141c2af29c18cd15116a4099c4f36d5bad46828d7348b6ceb655e65", ambiguity: [] }], basis: HistoricalCommitTimeWins, ambiguity: [], detail: "collision for gh_acme__widget:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa selects 5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd over 1 rejected payload(s) via historical_commit_time_wins" }] }
 right: ArtifactLinkCollisionPartitionWire { schema_version: 1, accepted: [ArtifactLinkCollisionOutcomeWire { digest: "5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/competitor.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:root-b0") }], groups: [ArtifactLinkCollisionGroupWire { project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", accepted: ArtifactLinkCollisionOutcomeWire { digest: "5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/competitor.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:root-b0") }, rejected: [ArtifactLinkCollisionFindingWire { digest: "403640fb6141c2af29c18cd15116a4099c4f36d5bad46828d7348b6ceb655e65", event: ArtifactLinkEventWire { schema_version: 1, project_key: "gh_acme__widget", operation_id: "aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa", created_by: "agent:reader", origin: Read, created_at: "2026-09-09T12:00:00Z", kind: Observation { edge: Directed { source_ref: "agent:reader", relation: "read", target_ref: "plan:202610/repeated.md" }, description: "read the artifact", occurrences: 1 } }, tier: Durable, source_locator: Some("durable:root-a0"), basis: HistoricalCommitTimeWins, detail: "earlier first-add 5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd wins over 403640fb6141c2af29c18cd15116a4099c4f36d5bad46828d7348b6ceb655e65", ambiguity: [] }], basis: HistoricalCommitTimeWins, ambiguity: [], detail: "collision for gh_acme__widget:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa selects 5e44fd06de423f081c92cd8f8f19cc0710d5cd0e9d05fb1d438fd315f3493ccd over 1 rejected payload(s) via historical_commit_time_wins" }] }


failures:
    artifact_link::collision::tests::group_basis_uses_the_same_surviving_order_as_winner_selection
    artifact_link::collision::tests::same_payload_descendant_clock_does_not_replace_earliest_history

test result: FAILED. 155 passed; 2 failed; 0 ignored; 0 measured; 5386 filtered out; finished in 0.02s

error: test failed, to rerun pass `-p sase_core --lib`
error: recipe `test` failed on line 23 with exit code 101

