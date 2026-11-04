# Chat History - ace-run (185--mon)

- **TIMESTAMP:** 2026-11-04 14:44:53 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 185--mon

## Prompt

sase monitor start --command 'just lint && just test && cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/sase/repos/linked/bob-mac-capture && just portable-check' --reason 'Run Rust lint and test gates plus the portable Swift check for the capture sigil alias changes'

## Response

sase tool run a611a27475a7be026857ca857ebdfb2c

🔍  LINT
────────────────────────────────────────────────
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking typenum v1.20.1
    Checking cfg-if v1.0.4
    Checking stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
    Checking equivalent v1.0.2
    Checking foldhash v0.2.0
    Checking memchr v2.8.1
    Checking allocator-api2 v0.2.21
    Checking writeable v0.6.4
    Checking litemap v0.8.3
    Checking utf8_iter v1.0.4
    Checking bitflags v2.12.1
    Checking simd-adler32 v0.3.9
    Checking utf8parse v0.2.2
    Checking rand_core v0.10.1
    Checking adler2 v2.0.1
    Checking smallvec v1.15.2
    Checking colorchoice v1.0.5
    Checking cpufeatures v0.3.0
    Checking anstyle v1.0.14
    Checking anstyle-query v1.1.5
    Checking is_terminal_polyfill v1.70.2
    Checking tinyvec_macros v0.1.1
    Checking cpufeatures v0.2.17
    Checking itoa v1.0.18
    Checking clap_lex v1.1.0
    Checking weezl v0.1.12
    Checking siphasher v1.0.4
    Checking strsim v0.11.1
    Checking color_quant v1.1.0
    Checking iana-time-zone v0.1.65
    Checking byteorder-lite v0.1.0
    Checking unicode-bidi v0.3.18
    Checking bytecount v0.6.9
    Checking pxfm v0.1.30
    Checking quick-error v2.0.1
    Checking const-oid v0.10.2
    Checking percent-encoding v2.3.2
    Checking regex-syntax v0.8.10
    Checking unicode-properties v0.1.4
    Checking zune-core v0.5.3
    Checking unsafe-libyaml v0.2.11
    Checking ttf-parser v0.25.1
    Checking log v0.4.30
    Checking bytemuck v1.25.2
    Checking ryu v1.0.23
    Checking rangemap v1.7.1
    Checking is_executable v1.0.6
    Checking libc v0.2.186
    Checking serde_core v1.0.228
    Checking icu_properties_data v2.3.0
    Checking icu_normalizer_data v2.3.0
    Checking zmij v1.0.21
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_22/crates/bob-obsidian-assets)
    Checking similar v2.7.0
    Checking hex v0.4.3
    Checking num-conv v0.2.2
    Checking num-traits v0.2.19
    Checking linux-raw-sys v0.12.1
    Checking powerfmt v0.2.0
    Checking zerofrom v0.1.8
    Checking deranged v0.5.8
    Checking thiserror v2.0.18
    Checking time-core v0.1.9
    Checking base64 v0.22.1
    Checking fallible-streaming-iterator v0.1.9
    Checking anstyle-parse v1.0.0
    Checking crc32fast v1.5.0
    Checking encoding_rs v0.8.35
    Checking once_cell v1.21.4
    Checking fastrand v2.5.0
    Checking fallible-iterator v0.3.0
   Compiling cc v1.2.63
    Checking miniz_oxide v0.8.9
    Checking fdeflate v0.3.7
    Checking hashbrown v0.17.1
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking quick-xml v0.41.0
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
sccache: error: failed to execute compile
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `fdeflate` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name fdeflate --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/fdeflate-0.3.7/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --allow=unexpected_cfgs --check-cfg 'cfg(fuzzing)' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values())' -C metadata=9b3fa12779010c7f -C extra-filename=-e74183f4c172b24d --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern simd_adler32=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libsimd_adler32-e6f2dc3bb2fa1ca8.rmeta --cap-lints allow` (exit status: 2)
warning: build failed, waiting for other jobs to finish...
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
error: could not compile `cc` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name cc --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/cc-1.2.63/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata,link -C embed-bitcode=no --allow=unexpected_cfgs --check-cfg 'cfg(disable_clang_cl_tests)' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("jobserver", "parallel"))' -C metadata=fcb0cc509b305233 -C extra-filename=-1c35974f1d47186c --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern find_msvc_tools=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libfind_msvc_tools-c67de4483d55f240.rmeta --extern shlex=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libshlex-a28547581f7e2e70.rmeta --cap-lints allow` (exit status: 2)
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `hashbrown` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name hashbrown --edition=2024 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/hashbrown-0.17.1/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --warn=unused_extern_crates --warn=unsafe_op_in_unsafe_fn --warn=unreachable_pub '--warn=clippy::str_to_string' '--warn=clippy::semicolon_if_nothing_returned' '--warn=clippy::ref_as_ptr' '--warn=clippy::redundant_else' '--warn=clippy::ptr_cast_constness' '--warn=clippy::ptr_as_ptr' '--allow=clippy::option_if_let_else' '--warn=clippy::needless_continue' '--allow=clippy::must_use_candidate' '--allow=clippy::module_name_repetitions' '--allow=clippy::missing_safety_doc' '--allow=clippy::missing_errors_doc' --warn=missing_docs '--allow=clippy::manual_map' '--warn=clippy::manual_let_else' --warn=explicit_outlives_requirements --warn=ellipsis_inclusive_range_patterns --warn=elided_lifetimes_in_paths '--allow=clippy::doc_markdown' '--warn=clippy::borrow_as_ptr' --warn=bare_trait_objects --cfg 'feature="allocator-api2"' --cfg 'feature="default"' --cfg 'feature="default-hasher"' --cfg 'feature="equivalent"' --cfg 'feature="inline-more"' --cfg 'feature="raw-entry"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "allocator-api2", "core", "default", "default-hasher", "equivalent", "inline-more", "nightly", "raw-entry", "rayon", "rustc-dep-of-std", "rustc-internal-api", "serde"))' -C metadata=810d895633b0ebca -C extra-filename=-7ba5608fa201e238 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern allocator_api2=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/liballocator_api2-b23a0b8d68a77616.rmeta --extern equivalent=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libequivalent-d6d8772c9e982907.rmeta --extern foldhash=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libfoldhash-d5b4f74569272821.rmeta --cap-lints allow` (exit status: 2)
error: could not compile `fallible-streaming-iterator` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name fallible_streaming_iterator --edition=2015 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/fallible-streaming-iterator-0.1.9/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("std"))' -C metadata=b519fa008706adc4 -C extra-filename=-93774e0ee77715dc --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --cap-lints allow` (exit status: 2)
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
error: could not compile `crc32fast` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name crc32fast --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/crc32fast-1.5.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="default"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("default", "nightly", "std"))' -C metadata=f1120a299ede56b8 -C extra-filename=-acc258ee2ec160d6 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern cfg_if=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libcfg_if-f40e48be2bfa8956.rmeta --cap-lints allow --cfg stable_arm_crc32_intrinsics --check-cfg 'cfg(stable_arm_crc32_intrinsics)'` (exit status: 2)
error: could not compile `fastrand` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name fastrand --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/fastrand-2.5.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "default", "getrandom", "js", "std"))' -C metadata=ba0fb2255efb01b2 -C extra-filename=-cb590ed6f5e99e2c --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --cap-lints allow` (exit status: 2)
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: warning: The server looks like it shut down unexpectedly, compiling locally instead
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: Connection reset by peer (os error 104)
error: could not compile `aho-corasick` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name aho_corasick --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/aho-corasick-1.1.4/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="perf-literal"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("default", "logging", "perf-literal", "std"))' -C metadata=470a24a8094159b4 -C extra-filename=-5d8e5db8ee47be79 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
error: could not compile `fallible-iterator` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name fallible_iterator --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/fallible-iterator-0.3.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "default", "std"))' -C metadata=59497228b7c20c39 -C extra-filename=-6f3aa564d6c52fe7 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --cap-lints allow` (exit status: 2)
sccache: error: failed to execute compile
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `base64` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name base64 --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/base64-0.22.1/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "default", "std"))' -C metadata=249d2406be746ebb -C extra-filename=-15993057dadfeb3d --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --cap-lints allow` (exit status: 2)
sccache: error: failed to execute compile
error: could not compile `miniz_oxide` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name miniz_oxide --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/miniz_oxide-0.8.9/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --warn=unexpected_cfgs --check-cfg 'cfg(fuzzing)' --cfg 'feature="default"' --cfg 'feature="simd"' --cfg 'feature="simd-adler32"' --cfg 'feature="with-alloc"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "block-boundary", "core", "default", "rustc-dep-of-std", "serde", "simd", "simd-adler32", "std", "with-alloc"))' -C metadata=73a7db74151eb19e -C extra-filename=-9f259bf4192e031f --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern adler2=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libadler2-0b7e9f993fb5c394.rmeta --extern simd_adler32=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libsimd_adler32-e6f2dc3bb2fa1ca8.rmeta --cap-lints allow` (exit status: 2)
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: Connection reset by peer (os error 104)
error: could not compile `anstyle-parse` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name anstyle_parse --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/anstyle-parse-1.0.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --warn=rust_2018_idioms '--warn=clippy::zero_sized_map_values' '--warn=clippy::wildcard_imports' '--warn=clippy::verbose_file_reads' --warn=unused_qualifications --warn=unused_macro_rules --warn=unused_lifetimes --warn=unsafe_op_in_unsafe_fn --warn=unreachable_pub --warn=unnameable_types '--warn=clippy::uninlined_format_args' '--warn=clippy::trait_duplication_in_bounds' '--warn=clippy::todo' '--warn=clippy::string_lit_as_bytes' '--warn=clippy::string_add_assign' '--warn=clippy::string_add' '--warn=clippy::str_to_string' '--warn=clippy::semicolon_if_nothing_returned' '--warn=clippy::self_named_module_files' '--warn=clippy::same_functions_in_if_condition' '--allow=clippy::result_large_err' '--warn=clippy::rest_pat_in_fully_bound_structs' '--warn=clippy::ref_option_ref' '--warn=clippy::redundant_feature_names' '--warn=clippy::rc_mutex' '--warn=clippy::ptr_as_ptr' '--warn=clippy::path_buf_push_overwrite' '--warn=clippy::negative_feature_names' '--warn=clippy::needless_for_each' '--allow=clippy::needless_continue' '--warn=clippy::mutex_integer' '--warn=clippy::mem_forget' '--warn=clippy::macro_use_imports' '--warn=clippy::lossy_float_literal' '--warn=clippy::linkedlist' '--allow=clippy::let_and_return' '--warn=clippy::large_types_passed_by_value' '--warn=clippy::large_stack_arrays' '--warn=clippy::large_digit_groups' '--warn=clippy::invalid_upcast_comparisons' '--warn=clippy::infinite_loop' '--warn=clippy::inefficient_to_string' '--warn=clippy::inconsistent_struct_constructor' '--warn=clippy::imprecise_flops' '--warn=clippy::implicit_clone' '--allow=clippy::if_same_then_else' '--warn=clippy::from_iter_instead_of_collect' '--warn=clippy::fn_params_excessive_bools' '--warn=clippy::float_cmp_const' '--warn=clippy::flat_map_option' '--warn=clippy::filter_map_next' '--warn=clippy::fallible_impl_from' '--warn=clippy::explicit_into_iter_loop' '--warn=clippy::explicit_deref_methods' '--warn=clippy::expl_impl_clone_on_copy' '--warn=clippy::enum_glob_use' '--warn=clippy::empty_enums' '--warn=clippy::doc_markdown' '--warn=clippy::debug_assert_with_mut_call' '--warn=clippy::dbg_macro' '--warn=clippy::create_dir' '--allow=clippy::collapsible_else_if' '--warn=clippy::checked_conversions' '--allow=clippy::branches_sharing_code' '--allow=clippy::bool_assert_comparison' --cfg 'feature="default"' --cfg 'feature="utf8"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("core", "default", "utf8"))' -C metadata=e23291b87ee22676 -C extra-filename=-96d67ace568d2357 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern utf8parse=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libutf8parse-67b3e3636a607846.rmeta --cap-lints allow` (exit status: 2)
error: could not compile `once_cell` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name once_cell --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/once_cell-1.21.4/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="race"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "atomic-polyfill", "critical-section", "default", "parking_lot", "portable-atomic", "race", "std", "unstable"))' -C metadata=b6c113139d0745d7 -C extra-filename=-e57a1acb3e2c999b --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --cap-lints allow` (exit status: 2)
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: failed to fill whole buffer
error: could not compile `encoding_rs` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name encoding_rs --edition=2018 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/encoding_rs-0.8.35/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "any_all_workaround", "default", "fast-big5-hanzi-encode", "fast-gb-hanzi-encode", "fast-hangul-encode", "fast-hanja-encode", "fast-kanji-encode", "fast-legacy-encode", "less-slow-big5-hanzi-encode", "less-slow-gb-hanzi-encode", "less-slow-kanji-encode", "serde", "simd-accel"))' -C metadata=2ceb833893dfee19 -C extra-filename=-37fc075231f72329 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern cfg_if=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libcfg_if-f40e48be2bfa8956.rmeta --cap-lints allow` (exit status: 2)
error: could not compile `quick-xml` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name quick_xml --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/quick-xml-0.41.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="default"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("arbitrary", "async-tokio", "default", "document-features", "encoding", "encoding_rs", "escape-html", "overlapped-lists", "serde", "serde-types", "serialize", "tokio"))' -C metadata=d08edec9d8f1da21 -C extra-filename=-bd40c0c31a051189 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
sccache: error: failed to execute compile
sccache: caused by: Failed to send data to or receive data from server
sccache: caused by: Failed to read response header
sccache: caused by: Connection reset by peer (os error 104)
error: could not compile `nom` (lib)

Caused by:
  process didn't exit successfully: `/home/bryan/bin/sase-rustc-wrapper /home/bryan/.rustup/toolchains/1.95.0-x86_64-unknown-linux-gnu/bin/rustc --crate-name nom --edition=2021 /home/bryan/.cargo/registry/src/index.crates.io-1949cf8c6b5b557f/nom-8.0.0/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --crate-type lib --emit=dep-info,metadata -C embed-bitcode=no -C debuginfo=line-tables-only --cfg 'feature="alloc"' --cfg 'feature="default"' --cfg 'feature="std"' --check-cfg 'cfg(docsrs,test)' --check-cfg 'cfg(feature, values("alloc", "default", "docsrs", "std"))' -C metadata=02d9e29d60f3c9f6 -C extra-filename=-b9a2d65d06592291 --out-dir /home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps -L dependency=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps --extern memchr=/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws22-261104_140359/build/debug/deps/libmemchr-e95b930020db7c4f.rmeta --cap-lints allow` (exit status: 2)
error: recipe `lint` failed on line 70 with exit code 101
failed  exit=101  duration=7603ms

