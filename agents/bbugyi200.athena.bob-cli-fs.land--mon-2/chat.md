# Chat History - ace-run (bob-cli-fs.land--mon-2)

- **TIMESTAMP:** 2026-11-03 00:25:44 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-fs.land--mon-2

## Prompt

sase monitor start --command 'just check' --reason 'Re-run just check after SA27 unreadability taint fix'

## Response

sase tool run b686f23bb4763974c99f0d338927b3bb

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking typenum v1.20.1
    Checking cfg-if v1.0.4
    Checking stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
    Checking allocator-api2 v0.2.21
    Checking memchr v2.8.1
    Checking equivalent v1.0.2
    Checking foldhash v0.2.0
    Checking litemap v0.8.3
    Checking writeable v0.6.4
    Checking bitflags v2.12.1
    Checking utf8_iter v1.0.4
    Checking simd-adler32 v0.3.9
    Checking utf8parse v0.2.2
    Checking rand_core v0.10.1
    Checking adler2 v2.0.1
    Checking smallvec v1.15.2
    Checking anstyle v1.0.14
    Checking tinyvec_macros v0.1.1
    Checking cpufeatures v0.3.0
    Checking is_terminal_polyfill v1.70.2
    Checking anstyle-query v1.1.5
    Checking colorchoice v1.0.5
    Checking clap_lex v1.1.0
    Checking weezl v0.1.12
    Checking cpufeatures v0.2.17
    Checking siphasher v1.0.4
    Checking strsim v0.11.1
    Checking itoa v1.0.18
    Checking const-oid v0.10.2
    Checking percent-encoding v2.3.2
    Checking iana-time-zone v0.1.65
    Checking pxfm v0.1.30
    Checking unicode-properties v0.1.4
    Checking bytecount v0.6.9
    Checking quick-error v2.0.1
    Checking unicode-bidi v0.3.18
    Checking color_quant v1.1.0
    Checking regex-syntax v0.8.10
    Checking byteorder-lite v0.1.0
    Checking zune-core v0.5.3
    Checking ryu v1.0.23
    Checking rangemap v1.7.1
    Checking is_executable v1.0.6
    Checking ttf-parser v0.25.1
    Checking bytemuck v1.25.2
    Checking log v0.4.30
    Checking unsafe-libyaml v0.2.11
    Checking libc v0.2.186
    Checking icu_properties_data v2.3.0
    Checking serde_core v1.0.228
    Checking icu_normalizer_data v2.3.0
    Checking zmij v1.0.21
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12/crates/bob-obsidian-assets)
    Checking hex v0.4.3
    Checking similar v2.7.0
    Checking powerfmt v0.2.0
    Checking num-traits v0.2.19
    Checking linux-raw-sys v0.12.1
    Checking num-conv v0.2.2
    Checking zerofrom v0.1.8
    Checking deranged v0.5.8
    Checking thiserror v2.0.18
    Building [====>                     ] 49/233: siphasher, quick-error, zun…    Checking time-core v0.1.9
    Building [====>                     ] 50/233: siphasher, quick-error, zun…    Checking base64 v0.22.1
    Building [====>                     ] 51/233: siphasher, quick-error, zun…    Checking fallible-streaming-iterator v0.1.9
    Building [====>                     ] 52/233: siphasher, quick-error, zun…   Compiling cc v1.2.63
    Building [====>                     ] 53/233: siphasher, quick-error, zun…    Checking fallible-iterator v0.3.0
    Building [=====>                    ] 54/233: siphasher, quick-error, zun…    Checking once_cell v1.21.4
    Checking anstyle-parse v1.0.0
    Checking tinyvec v1.11.0
    Checking fastrand v2.5.0
    Building [=====>                    ] 62/233: siphasher, quick-error, zun…    Checking crc32fast v1.5.0
    Checking encoding_rs v0.8.35
    Building [======>                   ] 63/233: siphasher, quick-error, zun…    Checking hashbrown v0.17.1
    Building [======>                   ] 64/233: hashbrown, siphasher, quick…    Building [======>                   ] 65/233: hashbrown, siphasher, quick…    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking quick-xml v0.41.0
    Building [======>                   ] 66/233: hashbrown, siphasher, quick…    Building [======>                   ] 67/233: hashbrown, siphasher, quick…    Building [======>                   ] 68/233: hashbrown, siphasher, quick…    Checking generic-array v0.14.7
    Checking hybrid-array v0.4.12
    Building [======>                   ] 69/233: hashbrown, siphasher, quick…sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `cc` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name cc --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/cc-1.2.63/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata,link -C embed-bitcode=no --allow=unexpected_cfgs --check-cfg 'cfg(disable_clang_cl_tests)' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("jobserver", "parallel"))' -C metadata=fcb0cc509b305233 -C extra-filename=-1c35974f1d47186c --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern find_msvc_tools=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libfind_msvc_tools-c67de4483d55f240.rmeta --extern shlex=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libshlex-a28547581f7e2e70.rmeta --cap-lints allow` (exit status: 2)
warning: build failed, waiting for other jobs to finish...
    Building [======>                   ] 70/233: hashbrown, siphasher, quick…sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `hybrid-array` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name hybrid_array --edition=2024 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/hybrid-array-0.4.12/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only '--warn=clippy::unwrap_used' '--warn=clippy::unwrap_in_result' --warn=unused_qualifications --warn=unused_lifetimes '--warn=clippy::trivially_copy_pass_by_ref' --warn=trivial_numeric_casts --warn=trivial_casts '--warn=clippy::std_instead_of_core' '--warn=clippy::std_instead_of_alloc' '--warn=clippy::semicolon_if_nothing_returned' '--warn=clippy::return_self_not_must_use' '--warn=clippy::ref_as_ptr' '--warn=clippy::redundant_closure_for_method_calls' '--warn=clippy::ptr_as_ptr' '--warn=clippy::panic_in_result_fn' '--warn=clippy::panic' '--warn=clippy::must_use_candidate' '--warn=clippy::mod_module_files' '--warn=clippy::missing_panics_doc' '--warn=clippy::missing_errors_doc' --warn=missing_docs --warn=missing_debug_implementations --warn=missing_copy_implementations '--warn=clippy::map_unwrap_or' '--warn=clippy::manual_assert' '--warn=clippy::implicit_saturating_sub' '--warn=clippy::from_iter_instead_of_collect' '--warn=clippy::doc_markdown' '--warn=clippy::checked_conversions' '--warn=clippy::cast_sign_loss' '--warn=clippy::cast_precision_loss' '--warn=clippy::cast_possible_wrap' '--warn=clippy::cast_possible_truncation' '--warn=clippy::cast_lossless' '--warn=clippy::borrow_as_ptr' '--warn=clippy::arithmetic_side_effects' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "arbitrary", "bytemuck", "ctutils", "extra-sizes", "serde", "subtle", "zerocopy", "zeroize"))' -C metadata=00727f9056c1c6aa -C extra-filename=-ead9e57856844274 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern typenum=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libtypenum-c2da7f26060c43a4.rmeta --cap-lints allow` (exit status: 2)
    Building [======>                   ] 71/233: hashbrown, siphasher, quick…sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `generic-array` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name generic_array --edition=2015 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/generic-array-0.14.7/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="more_lengths"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("more_lengths", "serde", "zeroize"))' -C metadata=2679f7fe18d85ab3 -C extra-filename=-1f3a9a5d3829382d --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern typenum=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libtypenum-c2da7f26060c43a4.rmeta --cap-lints allow --cfg relaxed_coherence` (exit status: 2)
    Building [=======>                  ] 72/233: hashbrown, siphasher, quick…error: could not compile `nom` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name nom --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/nom-8.0.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "default", "docsrs", "std"))' -C metadata=02d9e29d60f3c9f6 -C extra-filename=-b9a2d65d06592291 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
    Building [=======>                  ] 73/233: hashbrown, siphasher, quick…sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
error: could not compile `quick-xml` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name quick_xml --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/quick-xml-0.41.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="default"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("arbitrary", "async-tokio", "default", "document-features", "encoding", "encoding_rs", "escape-html", "overlapped-lists", "serde", "serde-types", "serialize", "tokio"))' -C metadata=d08edec9d8f1da21 -C extra-filename=-bd40c0c31a051189 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `tinyvec` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name tinyvec --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/tinyvec-1.11.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --cfg 'feature="tinyvec_macros"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "arbitrary", "borsh", "debugger_visualizer", "default", "defmt", "experimental_write_impl", "generic-array", "grab_spare_slice", "latest_stable_rust", "nightly_slice_partition_dedup", "real_blackbox", "rustc_1_40", "rustc_1_55", "rustc_1_57", "rustc_1_61", "serde", "std", "tinyvec_macros"))' -C metadata=896640ee640ce5c8 -C extra-filename=-267b77b58665f1d8 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern tinyvec_macros=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libtinyvec_macros-b9684d0dbad6de10.rmeta --cap-lints allow` (exit status: 2)
    Building [=======>                  ] 75/233: hashbrown, siphasher, quick…error: could not compile `hashbrown` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name hashbrown --edition=2024 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/hashbrown-0.17.1/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --warn=unused_extern_crates --warn=unsafe_op_in_unsafe_fn --warn=unreachable_pub '--warn=clippy::str_to_string' '--warn=clippy::semicolon_if_nothing_returned' '--warn=clippy::ref_as_ptr' '--warn=clippy::redundant_else' '--warn=clippy::ptr_cast_constness' '--warn=clippy::ptr_as_ptr' '--allow=clippy::option_if_let_else' '--warn=clippy::needless_continue' '--allow=clippy::must_use_candidate' '--allow=clippy::module_name_repetitions' '--allow=clippy::missing_safety_doc' '--allow=clippy::missing_errors_doc' --warn=missing_docs '--allow=clippy::manual_map' '--warn=clippy::manual_let_else' --warn=explicit_outlives_requirements --warn=ellipsis_inclusive_range_patterns --warn=elided_lifetimes_in_paths '--allow=clippy::doc_markdown' '--warn=clippy::borrow_as_ptr' --warn=bare_trait_objects --cfg 'feature="allocator-api2"' --cfg 'feature="default"' --cfg 'feature="default-hasher"' --cfg 'feature="equivalent"' --cfg 'feature="inline-more"' --cfg 'feature="raw-entry"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "allocator-api2", "core", "default", "default-hasher", "equivalent", "inline-more", "nightly", "raw-entry", "rayon", "rustc-dep-of-std", "rustc-internal-api", "serde"))' -C metadata=810d895633b0ebca -C extra-filename=-7ba5608fa201e238 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern allocator_api2=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/liballocator_api2-b23a0b8d68a77616.rmeta --extern equivalent=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libequivalent-d6d8772c9e982907.rmeta --extern foldhash=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libfoldhash-d5b4f74569272821.rmeta --cap-lints allow` (exit status: 2)
    Building [=======>                  ] 76/233: siphasher, quick-error, zun…sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `aho-corasick` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name aho_corasick --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/aho-corasick-1.1.4/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="perf-literal"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("default", "logging", "perf-literal", "std"))' -C metadata=470a24a8094159b4 -C extra-filename=-5d8e5db8ee47be79 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws12-261103_001256/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
    Building [=======>                  ] 77/233: siphasher, quick-error, zun…    Building [=======>                  ] 78/233: siphasher, quick-error, zun…    Building [=======>                  ] 79/233: siphasher, quick-error, zun…    Building [========>                 ] 81/233: siphasher, quick-error, zun…    Building [========>                 ] 82/233: siphasher, quick-error, zun…    Building [========>                 ] 83/233: siphasher, quick-error, zun…    Building [========>                 ] 84/233: siphasher, quick-error, zun…    Building [========>                 ] 85/233: siphasher, quick-error, zun…    Building [========>                 ] 86/233: siphasher, zune-core, hex, …    Building [========>                 ] 87/233: siphasher, zune-core, hex, …    Building [========>                 ] 88/233: siphasher, zune-core, hex, …    Building [========>                 ] 89/233: siphasher, zune-core, hex, …    Building [=========>                ] 90/233: siphasher, zune-core, hex, …    Building [=========>                ] 91/233: siphasher, zune-core, hex, …    Building [=========>                ] 92/233: siphasher, zune-core, hex, …    Building [=========>                ] 93/233: siphasher, zune-core, hex, …    Building [=========>                ] 94/233: siphasher, zune-core, hex, …    Building [=========>                ] 95/233: siphasher, zune-core, hex, …    Building [=========>                ] 96/233: siphasher, zune-core, hex, …    Building [=========>                ] 97/233: siphasher, zune-core, hex, …    Building [=========>                ] 98/233: siphasher, zune-core, hex, …    Building [==========>               ] 99/233: siphasher, zune-core, hex, …    Building [=========>               ] 101/233: siphasher, zune-core, hex, …    Building [=========>               ] 102/233: zune-core, hex, powerfmt, w…    Building [==========>              ] 103/233: zune-core, hex, powerfmt, w…    Building [==========>              ] 104/233: zune-core, hex, powerfmt, w…    Building [==========>              ] 105/233: zune-core, hex, powerfmt, w…    Building [==========>              ] 106/233: zune-core, hex, weezl, enco…    Building [==========>              ] 107/233: zune-core, hex, weezl, enco…    Building [==========>              ] 108/233: zune-core, hex, weezl, enco…    Building [==========>              ] 109/233: hex, weezl, encoding_rs, re…    Building [==========>              ] 110/233: weezl, encoding_rs, regex-s…    Building [==========>              ] 111/233: weezl, encoding_rs, regex-s…    Building [===========>             ] 112/233: weezl, encoding_rs, regex-s…    Building [===========>             ] 113/233: weezl, encoding_rs, regex-s…    Building [===========>             ] 114/233: weezl, encoding_rs, regex-s…    Building [===========>             ] 115/233: weezl, encoding_rs, regex-s…    Building [===========>             ] 116/233: encoding_rs, regex-syntax, …    Building [===========>             ] 117/233: encoding_rs, regex-syntax, …    Building [===========>             ] 118/233: encoding_rs, regex-syntax, …    Building [===========>             ] 119/233: encoding_rs, regex-syntax, …    Building [===========>             ] 120/233: encoding_rs, regex-syntax, …    Building [===========>             ] 121/233: encoding_rs, regex-syntax, …    Building [============>            ] 122/233: encoding_rs, regex-syntax, …    Building [============>            ] 123/233: encoding_rs, regex-syntax, …    Building [============>            ] 124/233: encoding_rs, regex-syntax, …    Building [============>            ] 125/233: regex-syntax, libc, pxfm, s…    Building [============>            ] 126/233: regex-syntax, pxfm, serde_c…    Building [============>            ] 127/233: regex-syntax, pxfm, serde_c…    Building [============>            ] 128/233: pxfm, serde_core, ttf-parser    Building [============>            ] 129/233: pxfm, serde_core                Building [============>            ] 130/233: pxfm                        error: recipe `check` failed on line 79 with exit code 101
failed  exit=101  duration=14236ms
verdict: undetermined; exit 101

