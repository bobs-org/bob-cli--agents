# Chat History - ace-run (bob-cli-df.2.1.4.1--mon-2)

- **TIMESTAMP:** 2026-10-28 03:03:09 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-df.2.1.4.1--mon-2

## Prompt

sase monitor start --command 'just test -p sase_core artifact_link && just test -p sase_core_py artifact_link_collision_bindings_round_trip && sase tool run check' --reason 'Verify artifact-link ordering repair and its binding after local lint fixes'

## Response

sase tool run 2143d55d156a961e975b436b12f1ccae
./scripts/check.sh test -p sase_core artifact_link
   Compiling libc v0.2.186
   Compiling cfg-if v1.0.4
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
   Compiling memchr v2.8.0
   Compiling zerocopy v0.8.48
   Compiling shlex v1.3.0
   Compiling find-msvc-tools v0.1.9
   Compiling regex-syntax v0.8.10
   Compiling crossbeam-utils v0.8.21
   Compiling serde_core v1.0.228
   Compiling version_check v0.9.5
   Compiling siphasher v1.0.4
   Compiling log v0.4.29
   Compiling serde v1.0.228
   Compiling autocfg v1.5.0
   Compiling once_cell v1.21.4
   Compiling bitflags v2.11.1
   Compiling crossbeam-epoch v0.9.21
   Compiling equivalent v1.0.2
   Compiling crossbeam-deque v0.8.8
   Compiling hashbrown v0.17.0
   Compiling zmij v1.0.21
   Compiling iana-time-zone v0.1.65
   Compiling ucd-trie v0.1.7
   Compiling itoa v1.0.18
   Compiling serde_json v1.0.149
   Compiling libm v0.2.16
   Compiling same-file v1.0.6
   Compiling smallvec v1.15.1
   Compiling lazy_static v1.5.0
   Compiling typenum v1.20.0
   Compiling pin-project-lite v0.2.17
   Compiling futures-core v0.3.32
   Compiling parking_lot_core v0.9.12
   Compiling deunicode v1.6.2
   Compiling futures-sink v0.3.32
   Compiling unicode-segmentation v1.13.3
   Compiling vcpkg v0.2.15
   Compiling bytes v1.11.1
   Compiling rayon-core v1.13.0
   Compiling thiserror v1.0.69
   Compiling either v1.19.0
   Compiling scopeguard v1.2.0
   Compiling anstyle v1.0.14
   Compiling heck v0.5.0
   Compiling clap_lex v1.1.1
   Compiling percent-encoding v2.3.2
   Compiling pkg-config v0.3.33
   Compiling winnow v1.0.4
   Compiling futures-io v0.3.32
   Compiling futures-task v0.3.32
   Compiling getrandom v0.4.2
   Compiling rustix v1.1.4
   Compiling slab v0.4.12
   Compiling toml_writer v1.1.3+spec-1.1.0
   Compiling tower-service v0.3.3
   Compiling home v0.5.12
   Compiling sync_wrapper v1.0.2
   Compiling winnow v0.7.15
   Compiling cpufeatures v0.2.17
   Compiling tower-layer v0.3.3
   Compiling linux-raw-sys v0.12.1
   Compiling fastrand v2.4.1
   Compiling fallible-iterator v0.3.0
   Compiling ryu v1.0.23
   Compiling unsafe-libyaml v0.2.11
   Compiling tinyvec v1.13.3
   Compiling fallible-streaming-iterator v0.1.9
   Compiling hex v0.4.3
   Compiling unicode-casefold v0.2.0
   Compiling semver v1.0.28
   Compiling unicode-width v0.2.2
   Compiling encoding_rs v0.8.35
   Compiling tracing-core v0.1.36
   Compiling aho-corasick v1.1.4
   Compiling bstr v1.13.1
   Compiling grep-matcher v0.1.9
   Compiling itertools v0.11.0
   Compiling num-traits v0.2.19
   Compiling generic-array v0.14.7
   Compiling ahash v0.8.12
   Compiling phf_shared v0.11.3
   Compiling cc v1.2.61
   Compiling toml_parser v1.1.5+spec-1.1.0
   Compiling futures-channel v0.3.32
   Compiling walkdir v2.5.0
   Compiling lock_api v0.4.14
   Compiling etcetera v0.8.0
   Compiling indexmap v2.14.0
   Compiling clap_builder v4.6.7
   Compiling slug v0.1.6
   Compiling colored v2.2.0
   Compiling crossbeam-channel v0.5.17
   Compiling unicode-normalization v0.1.25
   Compiling getrandom v0.2.17
   Compiling errno v0.3.14
   Compiling socket2 v0.6.3
   Compiling mio v1.2.0
   Compiling memmap2 v0.9.11
   Compiling term_size v0.3.2
   Compiling fs2 v0.4.3
   Compiling humansize v2.1.3
   Compiling toml_datetime v0.7.5+spec-1.1.0
   Compiling serde_spanned v1.1.2
   Compiling psm v0.1.24
   Compiling stacker v0.1.25
   Compiling libsqlite3-sys v0.30.1
   Compiling encoding_rs_io v0.1.8
   Compiling phf v0.11.3
   Compiling crypto-common v0.1.7
   Compiling block-buffer v0.10.4
   Compiling signal-hook-registry v1.4.8
   Compiling regex-automata v0.4.14
   Compiling tempfile v3.27.0
   Compiling rand_core v0.6.4
   Compiling parking_lot v0.12.5
   Compiling grep-searcher v0.1.17
   Compiling chrono v0.4.44
   Compiling toml v0.9.12+spec-1.1.0
   Compiling digest v0.10.7
   Compiling ppv-lite86 v0.2.21
   Compiling pest v2.9.4
   Compiling sha2 v0.10.9
   Compiling sha1 v0.10.7
   Compiling hashbrown v0.14.5
   Compiling rand_chacha v0.3.1
   Compiling rayon v1.12.0
   Compiling syn v2.0.117
   Compiling syn v3.0.9
   Compiling rand v0.8.6
   Compiling hashlink v0.9.1
   Compiling pest_meta v2.9.4
   Compiling regex v1.12.3
   Compiling globset v0.4.19
   Compiling phf_generator v0.11.3
   Compiling rusqlite v0.32.1
   Compiling parse-zoneinfo v0.3.1
   Compiling phf_codegen v0.11.3
   Compiling ignore v0.4.32
   Compiling chrono-tz-build v0.3.0
   Compiling chrono-tz v0.9.0
   Compiling pest_generator v2.9.4
   Compiling clap_derive v4.6.7
   Compiling derive_arbitrary v1.5.0
   Compiling globwalk v0.9.1
   Compiling arbitrary v1.5.0
   Compiling pest_derive v2.9.4
   Compiling serde_derive v1.0.228
   Compiling tokio-macros v2.7.0
   Compiling thiserror-impl v1.0.69
   Compiling tracing-attributes v0.1.31
   Compiling futures-macro v0.3.32
   Compiling clap v4.6.7
   Compiling tokio v1.52.2
   Compiling futures-util v0.3.32
   Compiling clap-cargo v0.18.3
   Compiling tracing v0.1.44
   Compiling table_formatter v0.6.1
   Compiling json5 v0.4.1
   Compiling dashmap v6.1.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tera v1.20.1
   Compiling sase_workspace_hack v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_workspace_hack)
   Compiling tower v0.5.3
   Compiling tokio-util v0.7.18
   Compiling tokei v15.0.0
   Compiling sase_core v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_core)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2m 48s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261028_024821/build/debug/deps/sase_core-c3182504540c81bb)

running 146 tests
test artifact_link::collision::tests::invalid_individual_events_still_error ... ok
test artifact_link::collision::tests::malformed_complete_history_timestamp_is_a_validation_error ... ok
test artifact_link::collision::tests::strict_reducer_still_rejects_operation_id_collisions ... ok
test artifact_link::collision::tests::exact_retries_collapse_without_quarantine ... ok
test artifact_link::collision::tests::durable_beats_pending_replay ... ok
test artifact_link::collision::tests::durable_beats_incoming_regardless_of_created_at ... ok
test artifact_link::collision::tests::admission_sequence_orders_local_only_objects ... ok
test artifact_link::collision::tests::distinct_operations_are_both_accepted ... ok
test artifact_link::collision::tests::historical_commit_time_orders_independent_histories ... ok
test artifact_link::collision::tests::historical_commit_time_compares_actual_instants_across_offsets ... ok
test artifact_link::collision::tests::established_evidence_beats_missing_evidence ... ok
test artifact_link::collision::tests::quarantine_record_path_validate_and_canonicalize ... ok
test artifact_link::collision::tests::missing_evidence_falls_back_to_digest_tie_break ... ok
test artifact_link::collision::tests::equivalent_timestamp_spellings_use_the_unordered_digest_tie_break ... ok
test artifact_link::collision::tests::historical_original_wins_with_identical_timestamps ... ok
test artifact_link::collision::tests::duplicate_root_ancestry_is_retained_for_complete_group_selection ... ok
test artifact_link::events::tests::alias_chains_resolve_edges_and_cycles_or_conflicts_fail ... ok
test artifact_link::events::tests::event_edge_identity_normalizes_directed_and_undirected_relations ... ok
test artifact_link::events::tests::bytes_validation_rejects_floats_and_path_mismatches ... ok
test artifact_link::collision::tests::three_payloads_produce_one_accepted_and_two_findings ... ok
test artifact_link::events::tests::edge_put_supersedes_named_versions_and_uses_lexical_tie_break ... ok
test artifact_link::cutover::tests::attestation_is_stable_and_head_sensitive ... ok
test artifact_link::events::tests::canonical_json_digest_and_path_are_byte_stable ... ok
test artifact_link::cutover::tests::marker_round_trips_with_canonical_json ... ok
test artifact_link::cutover::tests::import_identity_is_order_stable_and_head_sensitive ... ok
test artifact_link::cutover::tests::progress_walks_recovery_phases ... ok
test artifact_link::events::tests::predecessor_ids_known_on_other_edges_are_rejected ... ok
test artifact_link::cutover::tests::classifies_and_converts_legacy_outbox_lines ... ok
test artifact_link::events::tests::reduction_rejects_operation_id_collisions ... ok
test artifact_link::events::tests::reduction_deduplicates_exact_retries_but_counts_distinct_observations ... ok
test artifact_link::events::tests::stable_background_producer_contract_is_replay_stable ... ok
test artifact_link::collision::tests::identical_digest_copies_keep_the_earliest_history_across_roots ... ok
test artifact_link::events::tests::validation_rejects_bad_identifiers_payloads_and_edges ... ok
test artifact_link::events::tests::remove_before_add_removes_only_observed_versions ... ok
test artifact_link::collision::tests::rejected_put_cannot_supersede_accepted_observation ... ok
test artifact_link::events::tests::baseline_imports_preserve_counts_and_are_one_shot_by_import_id ... ok
test artifact_link::collision::tests::permutations_and_duplicate_roots_are_stable ... ok
test artifact_link::index::tests::empty_and_malformed_rows_do_not_reject_the_snapshot ... ok
test artifact_link::index::tests::colliding_agent_alias_resolves_to_earliest_row_in_row_order ... ok
test artifact_link::events::tests::reduction_is_stable_for_reordered_and_duplicated_deliveries ... ok
test artifact_link::collision::tests::rejected_kinds_cannot_affect_accepted_reduction ... ok
test artifact_link::inlet::tests::empty_list_is_entries ... ok
test artifact_link::inlet::tests::mapping_links_value_is_unrecognized ... ok
test artifact_link::cutover::tests::read_state_reports_four_states ... ok
test artifact_link::inlet::tests::matching_shape_is_entries ... ok
test artifact_link::inlet::tests::missing_key_is_absent ... ok
test artifact_link::index::tests::tolerant_duplicate_winner_uses_legacy_counts_and_edges_keep_first_row ... ok
test artifact_link::inlet::tests::no_frontmatter_is_absent ... ok
test artifact_link::inlet::tests::mkdocs_label_path_is_unrecognized ... ok
test artifact_link::collision::tests::complete_group_selection_eliminates_descendants_before_time_ordering ... ok
test artifact_link::index::tests::tolerant_string_fields_match_legacy_python_str ... ok
test artifact_link::merge::tests::accepts_one_sided_and_identical_deletes ... ok
test artifact_link::merge::tests::rejects_competing_same_key_edits_and_modify_delete ... ok
test artifact_link::ownership::tests::receipt_accepts_local_or_bead_durable_owners ... ok
test artifact_link::ownership::tests::receipt_rejects_schema_or_operation_mismatches ... ok
test artifact_link::merge::tests::validates_schema_artifact_ref_and_duplicates ... ok
test artifact_link::ownership::tests::receipt_classifies_per_endpoint_outcomes ... ok
test artifact_link::merge::tests::accepts_one_sided_and_identical_edits ... ok
test artifact_link::ownership::tests::receipt_requires_resolved_roots_and_durable_receipts ... ok
test artifact_link::ownership::tests::owner_requirements_partition_and_dedupe_event_refs ... ok
test artifact_link::path::tests::published_markdown_file_is_itself ... ok
test artifact_link::path::tests::goal_has_no_markdown_file ... ok
test artifact_link::path::tests::document_kind_is_itself ... ok
test artifact_link::ownership::tests::baseline_import_rows_contribute_document_owners ... ok
test artifact_link::merge::tests::unions_distinct_additions_in_deterministic_order_after_base_rows ... ok
test artifact_link::merge::tests::merge_is_idempotent ... ok
test artifact_link::path::tests::bead_page_uses_readme_for_lineage_root ... ok
test artifact_link::publication_retry::tests::due_policy_reports_retry_after_and_aging_warning ... ok
test artifact_link::publication_retry::tests::pending_registration_preserves_age_across_head_changes ... ok
test artifact_link::publication_retry::tests::failed_attempts_exponentially_back_off_at_six_hours ... ok
test artifact_link::path::tests::unpublished_file_uses_local_pages_dir ... ok
test artifact_link::relation::tests::every_builtin_documents_direction_and_examples ... ok
test artifact_link::relation::tests::builtins_cover_v1_table ... ok
test artifact_link::relation::tests::implements_settles_the_plan_bead_direction ... ok
test artifact_link::path::tests::companion_uses_stem_and_disambiguates_on_collision ... ok
test artifact_link::index::tests::empty_lookup_keys_yield_no_rows ... ok
test artifact_link::relation::tests::inverse_label_is_from_this_document ... ok
test artifact_link::index::tests::neighbor_target_uses_row_project_not_first_indexed_target ... ok
test artifact_link::index::tests::parity_fixture_alias_collision_does_not_shadow_canonical ... ok
test artifact_link::relation::tests::produced_by_and_launched_round_trip ... ok
test artifact_link::index::tests::native_build_and_selected_query_are_measurable ... ok
test artifact_link::index::tests::parity_fixture_first_wins_equal_uses_and_max_uses_unequal ... ok
test artifact_link::relation::tests::produced_by_covers_stitch_and_bead_sources ... ok
test artifact_link::publication_retry::tests::deferred_attempt_does_not_consume_failure_backoff ... ok
test artifact_link::relation::tests::reserved_slugs_point_at_bead_dep ... ok
test artifact_link::index::tests::parity_fixture_self_edge_and_projected_writability ... ok
test artifact_link::relation::tests::unknown_slug_lists_builtins ... ok
test artifact_link::row_resolution::tests::parse_link_ref_parts_strips_aliases_sigil_and_fragment ... ok
test artifact_link::relation::tests::awaits_is_a_projection_only_agent_to_bead_relation ... ok
test artifact_link::row_resolution::tests::project_hint_precedes_deterministic_fallback ... ok
test artifact_link::row_resolution::tests::guards_do_not_resolve_virtual_or_malformed_refs ... ok
test artifact_link::path::tests::stitch_has_no_markdown_file ... ok
test artifact_link::wire::tests::directed_same_pair_may_carry_several_relations ... ok
test artifact_link::row_resolution::tests::resolver_matches_key_probe_equivalence ... ok
test artifact_link::wire::tests::reserved_slugs_are_not_stored ... ok
test artifact_link::index::tests::missing_ref_is_absent_not_indexed_non_selectable ... ok
test artifact_link::index::tests::tolerant_uses_match_legacy_truthiness_truncation_and_strings ... ok
test artifact_link::wire::tests::prompt_ref_rewrite_increments_uses_and_keeps_created_at ... ok
test artifact_link::wire::tests::canonicalize_strips_sigil_and_rewrites_kind_aliases ... ok
test artifact_link_eligibility::policy::tests::a_real_change_makes_its_repo_qualify ... ok
test artifact_link_eligibility::policy::tests::bookkeeping_only_repos_are_ineligible ... ok
test artifact_link::wire::tests::undirected_related_dedups_either_direction ... ok
test artifact_link_eligibility::policy::tests::empty_repos_are_ineligible ... ok
test artifact_link_eligibility::policy::tests::rejects_blank_run_id ... ok
test artifact_link::index::tests::parity_fixture_skips_empty_refs_and_keeps_malformed_endpoints ... ok
test artifact_link_eligibility::policy::tests::rejects_unsupported_schema_version ... ok
test artifact_link_eligibility::policy::tests::release_evidence_rejects_a_different_agent_in_the_same_session ... ok
test artifact_link_eligibility::policy::tests::release_evidence_rejects_a_different_run_id ... ok
test artifact_link_eligibility::policy::tests::release_evidence_requires_eligible_decision ... ok
test artifact_link_eligibility::policy::tests::release_evidence_round_trips_and_validates_against_the_same_run ... ok
test artifact_link::wire::tests::validate_rejects_multiline_and_overlong_descriptions ... ok
test artifact_link_eligibility::policy::tests::serde_rejects_unknown_change_role ... ok
test artifact_link_eligibility::policy::tests::serde_rejects_unknown_fields ... ok
test artifact_link_eligibility::policy::tests::serde_round_trips_the_decision_wire ... ok
test artifact_link::wire::tests::validate_rejects_self_links_and_blank_descriptions ... ok
test plan::artifact_link::tests::bead_section_supports_linked_unlinked_and_prettier_wrapped_labels ... ok
test plan::artifact_link::tests::discontiguous_header_groups_before_body_content_are_invalid ... ok
test plan::artifact_link::tests::empty_list_section_is_omitted ... ok
test plan::artifact_link::tests::artifacts_is_compatible_with_either_counterpart_section ... ok
test plan::artifact_link::tests::bead_upsert_keeps_bead_frontmatter ... ok
test plan::artifact_link::tests::back_compat_single_legacy_and_mixed_cases ... ok
test plan::artifact_link::tests::artifacts_is_list_shaped_and_orders_between_agents_and_commits ... ok
test plan::artifact_link::tests::escapes_labels_and_trailing_text ... ok
test plan::artifact_link::tests::extra_leading_blank_line_is_recognized_as_noncanonical_layout ... ok
test plan::artifact_link::tests::known_header_labels_after_body_content_are_ordinary_bullets ... ok
test plan::artifact_link::tests::ordinary_bold_and_nested_body_bullets_are_not_header_sections ... ok
test plan::artifact_link::tests::fenced_header_example_is_not_a_live_document_header ... ok
test artifact_link::row_resolution::tests::resolves_class_a_row_identity_shapes ... ok
test plan::artifact_link::tests::multi_section_round_trip_uses_fixed_order ... ok
test plan::artifact_link::tests::parses_prettier_wrapped_commit_and_preserves_unchanged_bytes ... ok
test plan::artifact_link::tests::title_before_header_means_the_bullet_is_body_content ... ok
test plan::artifact_link::tests::list_cap_is_visible_and_round_trips_logically ... ok
test plan::artifact_link::tests::legacy_upsert_preserves_frontmatter_body_and_other_sections ... ok
test plan::artifact_link::tests::plan_and_prompt_sections_accept_absolute_cross_repo_targets ... ok
test plan::artifact_link::tests::parent_upsert_removes_only_legacy_top_level_parent ... ok
test plan::artifact_link::tests::rejects_malformed_duplicate_unknown_and_unterminated_documents ... ok
test plan::artifact_link::tests::remove_section_keeps_the_rest_and_canonical_layout ... ok
test artifact_link::managed_table::tests::links_skip_host_document_reference_labels ... ok
test artifact_link::managed_table::tests::links_render_sorts_and_emits_pointer ... ok
test artifact_link::managed_table::tests::empty_links_table_removes_the_block ... ok
test artifact_link::managed_table::tests::links_upsert_is_top_anchored_and_idempotent ... ok
test artifact_link::index::tests::frozen_handle_supports_concurrent_reads ... ok
test artifact_link::managed_table::tests::links_after_plan_header_does_not_trip_header_invalid ... ok
test artifact_link::index::tests::project_query_preserves_first_row_patch_edges ... ok
test artifact_link::index::tests::parity_fixture_pins_every_link_chip_and_target_field ... ok
test artifact_link::index::tests::rows_and_project_do_not_scan_unrelated_rows ... ok

test result: ok. 146 passed; 0 failed; 0 ignored; 0 measured; 5386 filtered out; finished in 0.02s

     Running tests/artifact_ref_commit_budget.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261028_024821/build/debug/deps/artifact_ref_commit_budget-1a6fa227cd0d0fc4)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s

     Running tests/hermetic_test_env.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261028_024821/build/debug/deps/hermetic_test_env-7cdce80175c84fb4)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s

     Running tests/integration/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261028_024821/build/debug/deps/integration-04c6d9b7d6498a92)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 405 filtered out; finished in 0.00s

./scripts/check.sh test -p sase_core_py artifact_link_collision_bindings_round_trip
   Compiling stable_deref_trait v1.2.1
   Compiling target-lexicon v0.12.16
   Compiling percent-encoding v2.3.2
   Compiling httparse v1.10.1
   Compiling writeable v0.6.3
   Compiling untrusted v0.9.0
   Compiling litemap v0.8.2
   Compiling icu_properties_data v2.2.0
   Compiling icu_normalizer_data v2.2.0
   Compiling utf8_iter v1.0.4
   Compiling fnv v1.0.7
   Compiling httpdate v1.0.3
   Compiling http v1.4.0
   Compiling rustls v0.21.12
   Compiling rustversion v1.0.22
   Compiling num-conv v0.2.1
   Compiling try-lock v0.2.5
   Compiling time-core v0.1.8
   Compiling powerfmt v0.2.0
   Compiling thiserror v2.0.18
   Compiling mime v0.3.17
   Compiling atomic-waker v1.1.2
   Compiling ring v0.17.14
   Compiling memoffset v0.9.1
   Compiling base64 v0.21.7
   Compiling base64 v0.22.1
   Compiling tracing-log v0.2.0
   Compiling thread_local v1.1.9
   Compiling sharded-slab v0.1.7
   Compiling ipnet v2.12.0
   Compiling webpki-roots v0.25.4
   Compiling sync_wrapper v0.1.2
   Compiling nu-ansi-term v0.50.3
   Compiling matchit v0.7.3
   Compiling socket2 v0.5.10
   Compiling matchers v0.2.0
   Compiling synstructure v0.13.2
   Compiling zerovec-derive v0.11.3
   Compiling displaydoc v0.2.5
   Compiling thiserror-impl v2.0.18
   Compiling num-integer v0.1.46
   Compiling async-trait v0.1.89
   Compiling async-stream-impl v0.3.6
   Compiling serde_path_to_error v0.1.20
   Compiling unindent v0.2.4
   Compiling indoc v2.0.7
   Compiling async-stream v0.3.6
   Compiling tera v1.20.1
   Compiling form_urlencoded v1.2.2
   Compiling want v0.3.1
   Compiling pyo3-build-config v0.22.6
   Compiling num-bigint v0.4.6
   Compiling pem v3.0.6
   Compiling zerofrom-derive v0.1.7
   Compiling yoke-derive v0.8.2
   Compiling time-macros v0.2.27
   Compiling deranged v0.5.8
   Compiling http-body v1.0.1
   Compiling tracing-subscriber v0.3.23
   Compiling http v0.2.12
   Compiling zerofrom v0.1.7
   Compiling rustls-pemfile v1.0.4
   Compiling serde_urlencoded v0.7.1
   Compiling http-body-util v0.1.3
   Compiling hyper v1.9.0
   Compiling yoke v0.8.2
   Compiling pyo3-macros-backend v0.22.6
   Compiling pyo3-ffi v0.22.6
   Compiling pyo3 v0.22.6
   Compiling rustls-webpki v0.101.7
   Compiling sct v0.7.1
   Compiling zerovec v0.11.6
   Compiling zerotrie v0.2.4
   Compiling axum-core v0.4.5
   Compiling tower-http v0.5.2
   Compiling http-body v0.4.6
   Compiling h2 v0.3.27
   Compiling time v0.3.47
   Compiling tokei v15.0.0
   Compiling hyper-util v0.1.20
   Compiling tinystr v0.8.3
   Compiling potential_utf v0.1.5
   Compiling icu_collections v2.2.0
   Compiling icu_locale_core v2.2.0
   Compiling simple_asn1 v0.6.4
   Compiling pyo3-macros v0.22.6
   Compiling axum v0.7.9
   Compiling jsonwebtoken v9.3.1
   Compiling icu_provider v2.2.0
   Compiling sase_core v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_core)
   Compiling tokio-rustls v0.24.1
   Compiling icu_properties v2.2.0
   Compiling icu_normalizer v2.2.0
   Compiling hyper v0.14.32
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling hyper-rustls v0.24.2
   Compiling reqwest v0.11.27
   Compiling sase_gateway v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_gateway)
   Compiling sase_core_py v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_core_py)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 2m 52s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261028_024821/build/debug/deps/sase_core_rs-18627314f8f139fe)

running 1 test
test artifact_links::tests::artifact_link_collision_bindings_round_trip ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 361 filtered out; finished in 0.02s

sase tool run 5edc9f0e00de975240b3ca3a494f4033
./scripts/check.sh all
    Checking cfg-if v1.0.4
   Compiling memchr v2.8.0
    Checking itoa v1.0.18
    Checking pin-project-lite v0.2.17
    Checking once_cell v1.21.4
    Checking bytes v1.11.1
    Checking log v0.4.29
    Checking futures-core v0.3.32
   Compiling regex-syntax v0.8.10
   Compiling siphasher v1.0.4
    Checking smallvec v1.15.1
    Checking futures-sink v0.3.32
    Checking equivalent v1.0.2
    Checking hashbrown v0.17.0
    Checking futures-io v0.3.32
    Checking futures-task v0.3.32
    Checking slab v0.4.12
    Checking tower-service v0.3.3
   Compiling iana-time-zone v0.1.65
   Compiling bitflags v2.11.1
   Compiling same-file v1.0.6
    Checking tower-layer v0.3.3
    Checking typenum v1.20.0
    Checking sync_wrapper v1.0.2
    Checking lazy_static v1.5.0
    Checking scopeguard v1.2.0
    Checking ryu v1.0.23
    Checking clap_lex v1.1.1
    Checking either v1.19.0
    Checking anstyle v1.0.14
    Checking libc v0.2.186
   Compiling zerocopy v0.8.48
    Checking serde_core v1.0.228
   Compiling crossbeam-utils v0.8.21
   Compiling zmij v1.0.21
    Checking winnow v1.0.4
   Compiling num-traits v0.2.19
    Checking thiserror v1.0.69
    Checking linux-raw-sys v0.12.1
    Checking home v0.5.12
    Checking winnow v0.7.15
    Checking cpufeatures v0.2.17
    Checking toml_writer v1.1.3+spec-1.1.0
    Checking arbitrary v1.5.0
    Checking zerofrom v0.1.7
    Checking libsqlite3-sys v0.30.1
    Checking tracing-core v0.1.36
    Checking encoding_rs v0.8.35
    Checking httparse v1.10.1
   Compiling phf_shared v0.11.3
    Checking fallible-iterator v0.3.0
    Checking unsafe-libyaml v0.2.11
    Checking stable_deref_trait v1.2.1
    Checking fastrand v2.4.1
    Checking tinyvec v1.13.3
   Compiling aho-corasick v1.1.4
   Compiling bstr v1.13.1
   Compiling crossbeam-epoch v0.9.21
    Checking fallible-streaming-iterator v0.1.9
    Checking unicode-casefold v0.2.0
    Checking semver v1.0.28
    Checking unicode-width v0.2.2
    Checking hex v0.4.3
    Checking thread_local v1.1.9
    Checking generic-array v0.14.7
    Checking writeable v0.6.3
    Checking nu-ansi-term v0.50.3
    Checking untrusted v0.9.0
    Checking indexmap v2.14.0
    Checking litemap v0.8.2
    Checking utf8_iter v1.0.4
    Checking fnv v1.0.7
    Checking httpdate v1.0.3
    Checking lock_api v0.4.14
    Checking clap_builder v4.6.7
    Checking grep-matcher v0.1.9
    Checking icu_normalizer_data v2.2.0
    Checking http v1.4.0
    Checking icu_properties_data v2.2.0
    Checking colored v2.2.0
    Checking sharded-slab v0.1.7
    Checking percent-encoding v2.3.2
    Checking try-lock v0.2.5
   Compiling serde v1.0.228
    Checking crossbeam-channel v0.5.17
    Checking toml_parser v1.1.5+spec-1.1.0
    Checking errno v0.3.14
    Checking socket2 v0.6.3
    Checking mio v1.2.0
    Checking getrandom v0.2.17
    Checking futures-channel v0.3.32
   Compiling chrono v0.4.44
   Compiling walkdir v2.5.0
    Checking parking_lot_core v0.9.12
    Checking ahash v0.8.12
    Checking ppv-lite86 v0.2.21
    Checking encoding_rs_io v0.1.8
    Checking toml_datetime v0.7.5+spec-1.1.0
    Checking tracing v0.1.44
    Checking itertools v0.11.0
    Checking serde_spanned v1.1.2
    Checking memmap2 v0.9.11
    Checking block-buffer v0.10.4
   Compiling regex-automata v0.4.14
    Checking crypto-common v0.1.7
    Checking rustix v1.1.4
    Checking etcetera v0.8.0
    Checking getrandom v0.4.2
    Checking term_size v0.3.2
    Checking unicode-normalization v0.1.25
    Checking fs2 v0.4.3
    Checking tracing-log v0.2.0
    Checking yoke v0.8.2
   Compiling stacker v0.1.25
    Checking http v0.2.12
   Compiling num-conv v0.2.1
    Checking powerfmt v0.2.0
   Compiling time-core v0.1.8
    Checking num-integer v0.1.46
    Checking socket2 v0.5.10
   Compiling crossbeam-deque v0.8.8
    Checking signal-hook-registry v1.4.8
    Checking mime v0.3.17
    Checking atomic-waker v1.1.2
    Checking clap v4.6.7
    Checking serde_json v1.0.149
   Compiling phf v0.11.3
    Checking want v0.3.1
    Checking form_urlencoded v1.2.2
    Checking thiserror v2.0.18
    Checking base64 v0.22.1
    Checking base64 v0.21.7
    Checking serde_path_to_error v0.1.20
    Checking ipnet v2.12.0
    Checking webpki-roots v0.25.4
    Checking hashbrown v0.14.5
    Checking sync_wrapper v0.1.2
    Checking matchit v0.7.3
    Checking async-stream v0.3.6
    Checking http-body v1.0.1
    Checking bitflags v1.3.2
   Compiling serde_repr v0.1.20
    Checking memoffset v0.9.1
    Checking unindent v0.2.4
    Checking serde_yaml v0.9.34+deprecated
    Checking futures-util v0.3.32
    Checking parking_lot v0.12.5
    Checking rand_core v0.6.4
    Checking ring v0.17.14
    Checking table_formatter v0.6.1
    Checking toml v0.9.12+spec-1.1.0
    Checking grep-searcher v0.1.17
   Compiling pest v2.9.4
    Checking tempfile v3.27.0
    Checking serde_urlencoded v0.7.1
    Checking num-bigint v0.4.6
    Checking tokio v1.52.2
    Checking digest v0.10.7
    Checking rayon-core v1.13.0
    Checking clap-cargo v0.18.3
    Checking deranged v0.5.8
   Compiling pyo3-build-config v0.22.6
    Checking zerovec v0.11.6
    Checking zerotrie v0.2.4
    Checking pem v3.0.6
    Checking rustls-pemfile v1.0.4
   Compiling time-macros v0.2.27
    Checking http-body v0.4.6
    Checking fluent-uri v0.1.4
    Checking dashmap v6.1.0
    Checking hashlink v0.9.1
    Checking http-body-util v0.1.3
    Checking rand_chacha v0.3.1
    Checking regex v1.12.3
    Checking globset v0.4.19
    Checking matchers v0.2.0
    Checking sct v0.7.1
    Checking rustls-webpki v0.101.7
    Checking rayon v1.12.0
    Checking sha1 v0.10.7
    Checking sha2 v0.10.9
    Checking futures v0.3.32
    Checking tinystr v0.8.3
    Checking potential_utf v0.1.5
   Compiling pest_meta v2.9.4
   Compiling pyo3-ffi v0.22.6
   Compiling pyo3-macros-backend v0.22.6
   Compiling pyo3 v0.22.6
    Checking rusqlite v0.32.1
    Checking rand v0.8.6
    Checking lsp-types v0.97.0
    Checking ignore v0.4.32
    Checking tracing-subscriber v0.3.23
    Checking axum-core v0.4.5
    Checking tower-http v0.5.2
    Checking time v0.3.47
    Checking rustls v0.21.12
   Compiling parse-zoneinfo v0.3.1
    Checking icu_locale_core v2.2.0
    Checking icu_collections v2.2.0
    Checking tokio-util v0.7.18
    Checking tower v0.5.3
    Checking hyper v1.9.0
   Compiling pest_generator v2.9.4
    Checking tokio-rustls v0.24.1
   Compiling globwalk v0.9.1
    Checking simple_asn1 v0.6.4
    Checking h2 v0.3.27
   Compiling phf_generator v0.11.3
    Checking icu_provider v2.2.0
    Checking hyper-util v0.1.20
   Compiling pest_derive v2.9.4
    Checking jsonwebtoken v9.3.1
   Compiling pyo3-macros v0.22.6
   Compiling json5 v0.4.1
   Compiling phf_codegen v0.11.3
    Checking icu_properties v2.2.0
    Checking icu_normalizer v2.2.0
    Checking axum v0.7.9
   Compiling chrono-tz-build v0.3.0
   Compiling chrono-tz v0.9.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking hyper v0.14.32
    Checking tower-lsp-server v0.21.1
   Compiling tera v1.20.1
   Compiling sase_workspace_hack v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_workspace_hack)
    Checking hyper-rustls v0.24.2
    Checking reqwest v0.11.27
   Compiling tokei v15.0.0
    Checking sase_core v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_core)
    Checking sase_gateway v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_gateway)
    Checking sase_macro_lsp v0.43.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/sase/repos/external/gh/sase-org/sase-core/crates/sase_macro_lsp)
error: use of a disallowed method `std::env::set_var`
  --> crates/sase_core/tests/artifact_ref_commit_budget.rs:36:5
   |
36 |     std::env::set_var(BUDGET_ENV, "0.2");
   |     ^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods
   = note: `-D clippy::disallowed-methods` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::disallowed_methods)]`

error: use of a disallowed method `std::env::set_var`
  --> crates/sase_core/tests/artifact_ref_commit_budget.rs:54:5
   |
54 |     std::env::set_var(BUDGET_ENV, "120");
   |     ^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
  --> crates/sase_core/tests/artifact_ref_commit_budget.rs:63:5
   |
63 |     std::env::set_var(BUDGET_ENV, "not-a-number");
   |     ^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
  --> crates/sase_core/tests/artifact_ref_commit_budget.rs:69:5
   |
69 |     std::env::remove_var(BUDGET_ENV);
   |     ^^^^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: could not compile `sase_core` (test "artifact_ref_commit_budget") due to 4 previous errors
warning: build failed, waiting for other jobs to finish...
error: use of a disallowed method `std::env::set_var`
  --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:28:9
   |
28 |         std::env::set_var("HOME", temp.path());
   |         ^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods
   = note: `-D clippy::disallowed-methods` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::disallowed_methods)]`

error: use of a disallowed method `std::env::remove_var`
  --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:43:13
   |
43 |             std::env::remove_var(key);
   |             ^^^^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
  --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:56:24
   |
56 |             Some(v) => std::env::set_var("HOME", v),
   |                        ^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
  --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:57:21
   |
57 |             None => std::env::remove_var("HOME"),
   |                     ^^^^^^^^^^^^^^^^^^^^
   |
   = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:160:9
    |
160 |         std::env::set_var(old_key, "/tmp/old-catalog.json");
    |         ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:161:9
    |
161 |         std::env::set_var(new_key, "/tmp/new-catalog.json");
    |         ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:183:9
    |
183 |         std::env::remove_var(new_key);
    |         ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:201:24
    |
201 |             Some(v) => std::env::set_var(old_key, v),
    |                        ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:202:21
    |
202 |             None => std::env::remove_var(old_key),
    |                     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:205:24
    |
205 |             Some(v) => std::env::set_var(new_key, v),
    |                        ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_macro_lsp/src/server/tests/macro_lsp.rs:206:21
    |
206 |             None => std::env::remove_var(new_key),
    |                     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_macro_lsp/src/server/tests/project_tags.rs:780:13
    |
780 |             std::env::remove_var("SASE_MACRO_VCS_PROJECT_CATALOG");
    |             ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_macro_lsp/src/server/tests/project_tags.rs:785:5
    |
785 |     std::env::set_var("SASE_MACRO_VCS_PROJECT_CATALOG", &catalog_path);
    |     ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: could not compile `sase_macro_lsp` (lib test) due to 13 previous errors
error: use of a disallowed method `std::env::set_var`
   --> crates/sase_gateway/src/push.rs:618:9
    |
618 |         std::env::set_var(env_name, "test-access-token");
    |         ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods
    = note: `-D clippy::disallowed-methods` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::disallowed_methods)]`

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_gateway/src/push.rs:660:9
    |
660 |         std::env::remove_var(env_name);
    |         ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: could not compile `sase_gateway` (lib test) due to 2 previous errors
error: use of a disallowed method `std::env::set_var`
    --> crates/sase_core/src/agent_hold.rs:2384:9
     |
2384 |         std::env::set_var(LOCK_TIMEOUT_ENV, "0.01");
     |         ^^^^^^^^^^^^^^^^^
     |
     = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods
     = note: `-D clippy::disallowed-methods` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::disallowed_methods)]`

error: use of a disallowed method `std::env::remove_var`
    --> crates/sase_core/src/agent_hold.rs:2390:9
     |
2390 |         std::env::remove_var(LOCK_TIMEOUT_ENV);
     |         ^^^^^^^^^^^^^^^^^^^^
     |
     = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:131:5
    |
131 |     std::env::remove_var("SASE_AGENT_NAME");
    |     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:132:5
    |
132 |     std::env::remove_var("SASE_AGENT");
    |     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:138:5
    |
138 |     std::env::set_var("SASE_AGENT", "1");
    |     ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:142:5
    |
142 |     std::env::set_var("SASE_AGENT", "worker");
    |     ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:144:5
    |
144 |     std::env::set_var("SASE_AGENT_NAME", "named-worker");
    |     ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:147:5
    |
147 |     std::env::remove_var("SASE_AGENT_NAME");
    |     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:148:5
    |
148 |     std::env::remove_var("SASE_AGENT");
    |     ^^^^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:150:9
    |
150 |         std::env::set_var("SASE_AGENT_NAME", value);
    |         ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/bead/cli/tests/parsing.rs:153:9
    |
153 |         std::env::set_var("SASE_AGENT", value);
    |         ^^^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
    --> crates/sase_core/src/bead/touch_index.rs:2653:9
     |
2653 |         std::env::set_var(LOCK_TIMEOUT_ENV, "0.05");
     |         ^^^^^^^^^^^^^^^^^
     |
     = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
    --> crates/sase_core/src/bead/touch_index.rs:2657:9
     |
2657 |         std::env::remove_var(LOCK_TIMEOUT_ENV);
     |         ^^^^^^^^^^^^^^^^^^^^
     |
     = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:113:5
    |
113 |     env::set_var(
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:124:5
    |
124 |     env::remove_var("SASE_MACRO_BUILTIN_DIR");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:137:5
    |
137 |     env::set_var(
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:141:5
    |
141 |     env::set_var(
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:148:5
    |
148 |     env::remove_var("SASE_MACRO_BUILTIN_DIR");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:149:5
    |
149 |     env::remove_var("SASE_XPROMPT_BUILTIN_DIR");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:156:5
    |
156 |     env::set_var(
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:160:5
    |
160 |     env::set_var(
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:167:5
    |
167 |     env::remove_var("SASE_MACRO_DEFAULT_DIR");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:168:5
    |
168 |     env::remove_var("SASE_XPROMPT_DEFAULT_DIR");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:185:5
    |
185 |     env::set_var("SASE_MACRO_PLUGIN_DIRS_JSON", &new_json);
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::set_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:186:5
    |
186 |     env::set_var("SASE_XPROMPT_PLUGIN_DIRS_JSON", &old_json);
    |     ^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:190:5
    |
190 |     env::remove_var("SASE_MACRO_PLUGIN_DIRS_JSON");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: use of a disallowed method `std::env::remove_var`
   --> crates/sase_core/src/macro_catalog/tests/catalog_sources.rs:191:5
    |
191 |     env::remove_var("SASE_XPROMPT_PLUGIN_DIRS_JSON");
    |     ^^^^^^^^^^^^^^^
    |
    = note: use crate::native::env::TestEnvGuard thread-local overrides in tests; never mutate process environment
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#disallowed_methods

error: could not compile `sase_core` (lib test) due to 27 previous errors
error: recipe `check` failed on line 10 with exit code 101
failed  exit=101  duration=188879ms
verdict: undetermined; exit 101
failed  exit=101  duration=534494ms

