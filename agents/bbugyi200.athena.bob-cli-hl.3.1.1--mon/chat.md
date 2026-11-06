# Chat History - ace-run (bob-cli-hl.3.1.1--mon)

- **TIMESTAMP:** 2026-11-05 20:16:31 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-hl.3.1.1--mon

## Prompt

sase monitor start --command 'just check && just docs-check' --reason 'Run bob-cli phase gates before finalizing the assigned adapter phase'

## Response

sase tool run 0426d51ca9ed74f487a725890aad2762

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
    Checking foldhash v0.2.0
    Checking equivalent v1.0.2
    Checking writeable v0.6.4
    Checking litemap v0.8.3
    Checking simd-adler32 v0.3.9
    Checking bitflags v2.12.1
    Checking utf8_iter v1.0.4
    Checking smallvec v1.15.2
    Checking utf8parse v0.2.2
    Checking rand_core v0.10.1
    Checking adler2 v2.0.1
    Checking anstyle-query v1.1.5
    Checking is_terminal_polyfill v1.70.2
    Checking anstyle v1.0.14
    Checking colorchoice v1.0.5
    Checking tinyvec_macros v0.1.1
    Checking cpufeatures v0.3.0
    Checking siphasher v1.0.4
    Checking clap_lex v1.1.0
    Checking weezl v0.1.12
    Checking cpufeatures v0.2.17
    Checking strsim v0.11.1
    Checking itoa v1.0.18
    Checking const-oid v0.10.2
    Checking iana-time-zone v0.1.65
    Checking bytecount v0.6.9
    Checking quick-error v2.0.1
    Checking percent-encoding v2.3.2
    Checking byteorder-lite v0.1.0
    Checking color_quant v1.1.0
    Checking pxfm v0.1.30
    Checking unicode-properties v0.1.4
    Checking zune-core v0.5.3
    Checking unicode-bidi v0.3.18
    Checking regex-syntax v0.8.10
    Checking bytemuck v1.25.2
    Checking ryu v1.0.23
    Checking unsafe-libyaml v0.2.11
    Checking is_executable v1.0.6
    Checking ttf-parser v0.25.1
    Checking base64 v0.22.1
    Checking log v0.4.30
    Checking libc v0.2.186
    Checking serde_core v1.0.228
    Checking icu_properties_data v2.3.0
    Checking icu_normalizer_data v2.3.0
    Checking zmij v1.0.21
    Checking rangemap v1.7.1
    Checking hex v0.4.3
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_35/crates/bob-obsidian-assets)
    Checking similar v2.7.0
    Checking num-traits v0.2.19
    Checking deranged v0.5.8
    Checking num-conv v0.2.2
    Checking zerofrom v0.1.8
    Checking time-core v0.1.9
    Checking thiserror v2.0.18
    Checking powerfmt v0.2.0
    Checking tinyvec v1.11.0
    Checking linux-raw-sys v0.12.1
   Compiling cc v1.2.63
    Checking fallible-streaming-iterator v0.1.9
    Checking fastrand v2.5.0
    Checking fallible-iterator v0.3.0
    Checking once_cell v1.21.4
    Checking phf_shared v0.12.1
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking quick-xml v0.41.0
    Checking gif v0.14.2
    Checking anstyle-parse v1.0.0
    Checking crc32fast v1.5.0
    Checking chacha20 v0.10.2
    Checking encoding_rs v0.8.35
    Checking hashbrown v0.17.1
    Checking fdeflate v0.3.7
    Checking generic-array v0.14.7
    Checking hybrid-array v0.4.12
    Checking miniz_oxide v0.8.9
    Checking unicode-normalization v0.1.25
    Checking zune-jpeg v0.5.15
    Checking form_urlencoded v1.2.2
    Checking yoke v0.8.3
    Checking chrono v0.4.44
    Checking getrandom v0.4.2
    Checking fs2 v0.4.3
    Checking image-webp v0.2.4
    Checking serde v1.0.228
    Checking serde_json v1.0.150
    Checking time v0.3.53
    Checking rustix v1.1.5
    Checking anstream v1.0.0
    Checking moxcms v0.8.1
    Checking regex-automata v0.4.14
    Checking phf v0.12.1
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
    Checking indexmap v2.14.0
    Checking hashlink v0.12.1
    Checking stringprep v0.1.5
    Checking nom_locate v5.0.0
    Checking crypto-common v0.2.2
    Checking block-buffer v0.12.0
    Checking flate2 v1.1.9
    Checking rand v0.10.1
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking tempfile v3.27.0
    Checking clap_builder v4.6.7
    Checking inout v0.1.4
    Checking chrono-tz v0.10.4
    Checking digest v0.10.7
    Checking png v0.18.1
    Checking serde_yaml v0.9.34+deprecated
    Checking regex v1.12.3
    Checking plist v1.10.0
    Checking digest v0.11.3
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking cipher v0.4.4
    Checking md-5 v0.10.6
    Checking sha2 v0.10.9
    Checking sha2 v0.11.0
    Checking image v0.25.10
    Checking icu_locale_core v2.3.0
    Checking icu_collections v2.3.0
    Checking ecb v0.1.2
    Checking aes v0.8.4
    Checking cbc v0.1.2
    Checking clap v4.6.7
    Checking lopdf v0.40.0
    Checking clap_complete v4.6.11
    Checking rusqlite v0.40.1
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_35)
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
  --> src/native/capture/batch.rs:25:54
   |
25 |     pub(super) fn validate(&self, bob_dir: &Path) -> Result<(), CaptureError> {
   |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
   = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:83:10
   |
83 |     ) -> Result<(), CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:149:10
    |
149 |     ) -> Result<bool, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:157:10
    |
157 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:171:10
    |
171 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:186:10
    |
186 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:239:10
    |
239 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:258:10
    |
258 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:402:10
    |
402 |     ) -> Result<usize, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:427:10
    |
427 |     ) -> Result<Vec<StagedTextFile>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:464:6
    |
464 | ) -> Result<Vec<usize>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:516:6
    |
516 | ) -> Result<CaptureWritePlan, CaptureError> {
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
   --> src/native/capture/budget.rs:333:6
    |
333 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:862:10
    |
862 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:904:22
    |
904 |                   .map(|values| {
    |  ______________________^
905 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
906 | |                 })
    | |_________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:905:32
    |
905 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
    |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:912:26
    |
912 |                       .map(|vals| {
    |  __________________________^
913 | |                         vals.map(|raw| {
914 | |                             super::move_choice::parse_move_in_picks(raw)
915 | |                         })
916 | |                         .collect::<Result<Vec<_>, _>>()
917 | |                     })
    | |_____________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:913:34
    |
913 |                           vals.map(|raw| {
    |  __________________________________^
914 | |                             super::move_choice::parse_move_in_picks(raw)
915 | |                         })
    | |_________________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:926:22
    |
926 |                 .map(|raw| parse_pull_in_picks(raw))
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:945:6
    |
945 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:959:6
    |
959 | ) -> Result<PullInPicks, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:995:6
    |
995 | ) -> Result<InboxRoutePick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1024:6
     |
1024 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1035:14
     |
1035 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1042:6
     |
1042 | ) -> Result<SubBulletTarget, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1055:6
     |
1055 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1104:6
     |
1104 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1135:6
     |
1135 | ) -> Result<String, CaptureError> {
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
   --> src/native/capture/event_conflict.rs:290:1
    |
290 | / pub(super) fn detect_event_conflict(
291 | |     contents: &str,
292 | |     date: NaiveDate,
293 | |     session_name: Option<&str>,
...   |
298 | |     fit: &FitKind,
299 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/event_conflict.rs:314:1
    |
314 | / pub(super) fn detect_event_conflict_with<V: CloseVault + ?Sized>(
315 | |     contents: &str,
316 | |     date: NaiveDate,
317 | |     session_name: Option<&str>,
...   |
324 | |     day_relative: Option<&Path>,
325 | | ) -> Option<EventConflictJson> {
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
   --> src/native/capture/meet_event_run.rs:556:6
    |
556 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/meet_event_run.rs:547:1
    |
547 | / pub(super) fn restamp_session_clock(
548 | |     planner: &mut CaptureBatchPlanner,
549 | |     bob_dir: &Path,
550 | |     day_file: &Path,
...   |
555 | |     warnings: &mut Vec<CaptureWarning>,
556 | | ) -> Result<(), CaptureError> {
    | |_____________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:579:6
    |
579 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:625:6
    |
625 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:644:6
    |
644 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:851:6
    |
851 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
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

warning: this function has too many arguments (14/7)
   --> src/native/capture/output.rs:558:5
    |
558 | /     pub(super) fn from_items(
559 | |         items: Vec<CaptureItemResult>,
560 | |         global_destination: Option<GlobalDestinationSummary>,
561 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
572 | |         type_agreement: Vec<TypeAgreementJson>,
573 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture/output.rs:6980:5
     |
6980 | /     pub(super) fn pull_in_choice_required(
6981 | |         extra: serde_json::Map<String, serde_json::Value>,
6982 | |         human_unblocked: Vec<TaskCompleteUnblockedJson>,
6983 | |         human_keep_moving_folds: Vec<
...    |
6992 | |         human_note_pull_groups: Vec<PullInGroupJson>,
6993 | |     ) -> Self {
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:120:6
    |
120 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:128:6
    |
128 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1125:6
     |
1125 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1219:6
     |
1219 | ) -> Result<FanoutClipboardRead, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1312:6
     |
1312 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1521:6
     |
1521 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1629:6
     |
1629 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (14/7)
    --> src/native/capture/plan.rs:1614:1
     |
1614 | / pub(super) fn plan_capture_item(
1615 | |     request: &CaptureRequest,
1616 | |     parsed_item: ParsedCaptureItem,
1617 | |     now: chrono::NaiveDateTime,
...    |
1628 | |     project_moves: &[ProjectMoveLanding],
1629 | | ) -> Result<PlannedCaptureItem, CaptureError> {
     | |_____________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:2340:14
     |
2340 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:2525:11
     |
2525 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4077:6
     |
4077 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4191:6
     |
4191 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4220:6
     |
4220 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4306:6
     |
4306 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4347:6
     |
4347 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4567:6
     |
4567 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:5029:13
     |
5029 |             &String::new(),
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
   --> src/native/capture/pomodoro_adjust.rs:511:6
    |
511 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:593:6
    |
593 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:638:6
    |
638 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:823:6
    |
823 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1322:6
     |
1322 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1358:6
     |
1358 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1519:6
     |
1519 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1693:6
     |
1693 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1856:6
     |
1856 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2151:6
     |
2151 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2227:6
     |
2227 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2340:6
     |
2340 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2878:6
     |
2878 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/pomodoro_link.rs:986:6
    |
986 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1031:6
     |
1031 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1823:6
     |
1823 | ) -> Result<&str, CaptureError> {
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
    --> src/native/capture/pomodoro_past.rs:1279:6
     |
1279 | ) -> Result<(String, usize, usize), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the variable `idx` is used as a loop counter
    --> src/native/capture/pomodoro_past.rs:1327:5
     |
1327 |     for line in &block_lines {
     |     ^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (idx, line) in (insert_at..).zip(block_lines.iter())`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
     = note: `#[warn(clippy::explicit_counter_loop)]` on by default

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_past.rs:1360:6
     |
1360 | ) -> Result<super::plan::PlannedCaptureItem, CaptureError> {
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
  --> src/native/capture/pomodoro_start.rs:54:6
   |
54 |   ) -> Result<
   |  ______^
55 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
56 | |     CaptureError,
57 | | > {
   | |_^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:107:6
    |
107 |   ) -> Result<
    |  ______^
108 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
109 | |     CaptureError,
110 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:425:6
    |
425 |   ) -> Result<
    |  ______^
426 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
427 | |     CaptureError,
428 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:518:6
    |
518 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:570:6
    |
570 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:629:6
    |
629 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:648:6
    |
648 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:806:6
    |
806 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:818:6
    |
818 | ) -> Result<(String, Placement, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:863:6
    |
863 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:889:6
    |
889 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1190:6
     |
1190 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1451:6
     |
1451 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2093:6
     |
2093 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2196:6
     |
2196 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2261:6
     |
2261 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2431:6
     |
2431 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/project_note.rs:154:14
    |
154 |         .map(|offset| scheduled_date_string(today, offset))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2168:6
     |
2168 | ) -> Result<Vec<ResolvedProjectMove>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2333:6
     |
2333 | ) -> Result<ProjectMoveExecution, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/project_note.rs:2345:14
     |
2345 |           .map(|movement| {
     |  ______________^
2346 | |             slot_by_source.get(&movement.source_index).copied().ok_or_else(
2347 | |                 || {
2348 | |                     CaptureError::io(
...    |
2353 | |         })
     | |_________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2950:6
     |
2950 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
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
   --> src/native/capture/pull_in.rs:289:6
    |
289 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/relations_merge.rs:227:6
    |
227 | ) -> Result<TaskLocator, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:267:6
    |
267 | ) -> Result<VaultSnapshot, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:442:6
    |
442 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/task_complete.rs:172:6
    |
172 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:921:6
    |
921 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1188:6
     |
1188 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
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
   --> src/native/capture/transfer.rs:644:6
    |
644 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:670:6
    |
670 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:735:6
    |
735 |   ) -> Result<
    |  ______^
736 | |     (
737 | |         RelationMergeOutput,
738 | |         Vec<crate::native::task_move::transplant::RepairedFile>,
739 | |     ),
740 | |     CaptureError,
741 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:202:6
    |
202 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:375:44
    |
375 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
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
    --> src/native/capture_complete/candidates.rs:1081:1
     |
1081 | / fn relationship_disabled_reason(
1082 | |     bob_dir: &Path,
1083 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
1084 | |     graph: &HashMap<
...    |
1093 | |     blocked_tasks: &[ResolvedRelationshipEntry],
1094 | | ) -> Option<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1713:6
     |
1713 |   ) -> (
     |  ______^
1714 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1715 | |     Vec<String>,
1716 | |     Vec<(String, usize)>,
1717 | | ) {
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
   --> src/native/capture_language/close_log.rs:951:1
    |
951 | / pub(crate) fn lex_close_log_bullets_with_all(
952 | |     child_lines: &[ItemLine<'_>],
953 | |     close_token: &str,
954 | |     in_progress: Option<&[u32]>,
...   |
959 | |     complete_all: bool,
960 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: casting to the same type is unnecessary (`usize` -> `usize`)
    --> src/native/capture_language/completion.rs:1248:19
     |
1248 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast
     = note: `#[warn(clippy::unnecessary_cast)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:2232:6
     |
2232 |   ) -> Result<
     |  ______^
2233 | |     Vec<(
2234 | |         ParsedCaptureText,
2235 | |         Option<RefParentSource>,
...    |
2238 | |     TemplateCodedError,
2239 | | > {
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
   --> src/native/capture_language/editor_model.rs:786:1
    |
786 | / pub(super) enum TokenParse {
787 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
788 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 136 bytes
789 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
787 -     Marker(MarkerParse),
787 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:2436:1
     |
2436 | / fn empty_editor_item(
2437 | |     item: &CaptureItem<'_>,
2438 | |     mode: EditorMode,
2439 | |     route: Option<String>,
...    |
2444 | |     diagnostics: Vec<Diagnostic>,
2445 | | ) -> EditorItemParse {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:3292:1
     |
3292 | / fn attach_drawer_bullet_metadata(
3293 | |     item: &CaptureItem<'_>,
3294 | |     mode: &mut EditorMode,
3295 | |     parent_body: &str,
...    |
3300 | |     sub_bullets: &mut [AuthoredSubBullet],
3301 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:3891:35
     |
3891 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `#[warn(clippy::trim_split_whitespace)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:4547:5
     |
4547 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:4546:5
     |
4546 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:301:1
    |
301 | / pub(super) fn parse_editor_named_start_item<'a>(
302 | |     item: &CaptureItem<'a>,
303 | |     parent_trimmed: &str,
304 | |     suffix: String,
...   |
310 | |     spelling: NameSpelling,
311 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_pomodoro.rs:3273:1
     |
3273 | / fn editor_past_outcome<'a>(
3274 | |     item: &CaptureItem<'a>,
3275 | |     parent_trimmed: &str,
3276 | |     mode: EditorMode,
...    |
3281 | |     diagnostics: Vec<Diagnostic>,
3282 | | ) -> EditorItemOutcome<'a> {
     | |__________________________^
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
    --> src/native/capture_language/item.rs:1399:5
     |
1399 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1398:5
     |
1398 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/item.rs:1286:35
     |
1286 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:2099:1
     |
2099 | / fn parse_capture_item_masked<'a>(
2100 | |     item: &CaptureItem<'a>,
2101 | |     forced_route: Option<&str>,
2102 | |     forced_section: Option<&str>,
...    |
2107 | |     target_run: Option<&TargetRunContext>,
2108 | | ) -> Result<ParsedCaptureItemOutcome<'a>, String> {
     | |_________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:2422:5
     |
2422 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:2421:5
     |
2421 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:4250:1
     |
4250 | / pub(super) fn named_shape_error_with_drop(
4251 | |     token: &str,
4252 | |     suffix: &str,
4253 | |     name: &str,
...    |
4258 | |     is_literal: bool,
4259 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_language/past.rs:411:6
    |
137 |     Valid(PastEValid),
    |     ----------------- the largest variant contains at least 144 bytes
...
411 | ) -> Result<PastName, PastEOutcome> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_language::past::PastEOutcome`, for example by boxing large elements or replacing it with `Box<native::capture_language::past::PastEOutcome>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `idx` is used to index `members`
    --> src/native/capture_language/past.rs:1116:16
     |
1116 |     for idx in start..=end {
     |                ^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1116 -     for idx in start..=end {
1116 +     for (idx, <item>) in members.iter().enumerate().take(end + 1).skip(start) {
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
    --> src/native/capture_language/rewrite.rs:1137:8
     |
1137 |       if !raw_text[..run_start]
     |  ________^
1138 | |         .chars()
1139 | |         .next_back()
1140 | |         .is_some_and(|before| !before.is_whitespace())
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
1137 ~     if raw_text[..run_start]
1138 +         .chars()
1139 +         .next_back().is_none_or(|before| before.is_whitespace())
     |

warning: this function has too many arguments (9/7)
    --> src/native/capture_language/rewrite.rs:1206:1
     |
1206 | / fn candidate_selects_plain_marker(
1207 | |     candidate: &str,
1208 | |     start: usize,
1209 | |     end: usize,
...    |
1215 | |     id_part: &str,
1216 | | ) -> bool {
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
   --> src/native/capture_language/task_sources.rs:112:20
    |
112 |         let rest = &text[1..];
    |                    ^^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_language/task_sources.rs:111:5
    |
111 |     if text.starts_with('@') {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
    = note: `#[warn(clippy::manual_strip)]` on by default
help: try using the `strip_prefix` method
    |
111 ~     if let Some(rest) = text.strip_prefix('@') {
112 ~         if let Some(plus) = rest.find('+') {
    |

warning: redundant guard
    --> src/native/capture_language/tokens.rs:1406:43
     |
1406 |                 Some((after_x, x_len)) if after_x.is_empty() => {
     |                                           ^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
     |
1406 -                 Some((after_x, x_len)) if after_x.is_empty() => {
1406 +                 Some(("", x_len)) => {
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
    --> src/native/capture_parse.rs:2507:1
     |
2507 | / fn refusal_diagnostic(
2508 | |     spans: &[Span],
2509 | |     mode: EditorMode,
2510 | |     pomodoro_start: &Option<PomodoroStartSpec>,
...    |
2515 | |     source: &str,
2516 | | ) -> Option<Diagnostic> {
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

warning: this function has too many arguments (8/7)
   --> src/native/gcal/refile.rs:228:1
    |
228 | / fn classify_filing<C: ClockLookup + ?Sized>(
229 | |     input: &SyncPlanInput<'_>,
230 | |     contents: &str,
231 | |     events: &[EventNoteRow],
...   |
236 | |     clock: &mut Option<&mut C>,
237 | | ) -> Filing {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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
    --> src/native/gcal/sync.rs:1259:47
     |
1259 | fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
     |                                               ^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
1259 - fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
1259 + fn display_rel(vault: &std::path::Path, path: &Path) -> String {
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
    --> src/native/highlights_ref/create.rs:1982:1
     |
1982 | / pub(super) fn stamp_overwrite_source(
1983 | |     config: &Config,
1984 | |     plan: &OverwritePreflight,
1985 | |     options: &CreateOptions,
...    |
1990 | |     info: &PdfInfo,
1991 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2024:1
     |
2024 | / pub(super) fn stage_overwrite_audio(
2025 | |     options: &CreateOptions,
2026 | |     plan: &OverwritePreflight,
2027 | |     request: &OverwriteRequest,
...    |
2032 | |     title: &str,
2033 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2706:1
     |
2706 | / fn plan_target_for(
2707 | |     config: &Config,
2708 | |     stem: &str,
2709 | |     ref_type: &str,
...    |
2714 | |     source_display: &str,
2715 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3726:1
     |
3726 | / fn stage_overwrite_source_store(
3727 | |     _config: &Config,
3728 | |     plan: &OverwritePreflight,
3729 | |     scratch: &Path,
...    |
3736 | |     catalog: &super::code_catalog::CatalogOutcome,
3737 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4420:1
     |
4420 | / fn overwrite_pdf_url(
4421 | |     config: &Config,
4422 | |     url: super::clip_url::WebUrl,
4423 | |     downloaded: PathBuf,
...    |
4428 | |     selection: &OverwriteSelection,
4429 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4502:1
     |
4502 | / fn create_pdf_url_route(
4503 | |     config: &Config,
4504 | |     url: super::clip_url::WebUrl,
4505 | |     downloaded: PathBuf,
...    |
4510 | |     listen: Option<&super::listen::ListenCommand>,
4511 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5239:1
     |
5239 | / fn print_pdf_dry_run(
5240 | |     config: &Config,
5241 | |     styler: &Styler,
5242 | |     source_display: &str,
...    |
5250 | |     legacy: &[sources_mod::RecordedSource],
5251 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/create.rs:5480:1
     |
5480 | / fn compose_markdown_marker(
5481 | |     status: &str,
5482 | |     parent: &str,
5483 | |     title: &str,
...    |
5489 | |     return_links: bool,
5490 | | ) -> Result<String> {
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

warning: this function has too many arguments (16/7)
   --> src/native/plugins/sync.rs:238:1
    |
238 | / fn apply_plugin(
239 | |     options: &SyncOptions,
240 | |     id: &str,
241 | |     captured: &CapturedPlugin,
...   |
254 | |     issues: &mut Vec<String>,
255 | | ) -> PluginSync {
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
   --> src/native/pomodoro_homes/resolve.rs:540:25
    |
540 | /                         chain[nearest_home..end]
541 | |                             .iter()
542 | |                             .filter(|(_, facts)| {
543 | |                                 facts.kind == NoteKind::Project
544 | |                             })
545 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
545 -                             .last()
545 +                             .next_back()
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
    = note: `#[warn(clippy::manual_map)]` on by default
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
   --> src/native/task_merge/payload.rs:482:6
    |
482 | ) -> Result<(Vec<LineRange>, Vec<(String, String)>, usize), MergeError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/retirement.rs:213:15
    |
213 |     repoints: &[((PathBuf, String), (PathBuf, String))],
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
   --> src/native/task_move/plan.rs:342:22
    |
342 |           let parent = tasks
    |  ______________________^
343 | |             .iter()
344 | |             .filter(|candidate| {
345 | |                 candidate.line_index < task.line_index
...   |
348 | |             })
349 | |             .last();
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
349 -             .last();
349 +             .next_back();
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

warning: `bob-obsidian` (lib) generated 489 warnings (run `cargo clippy --fix --lib -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 35 suggestions)
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
   --> tests/gcal_lifecycle.rs:672:19
    |
672 |       let learned = journal
    |  ___________________^
673 | |         .iter()
674 | |         .filter(|line| line["kind"] == "gcal.series_root")
675 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
675 -         .last()
675 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> tests/gcal_lifecycle.rs:708:21
    |
708 |       let relearned = journal
    |  _____________________^
709 | |         .iter()
710 | |         .filter(|line| line["kind"] == "gcal.series_root")
711 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
711 -         .last()
711 +         .next_back()
    |

warning: useless use of `vec!`
    --> tests/gcal_lifecycle.rs:1405:19
     |
1405 |       let journal = vec![
     |  ___________________^
1406 | |         journal_entry(
1407 | |             "migrate",
1408 | |             "migrate",
...    |
1429 | |         ),
1430 | |     ];
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
     = note: `#[warn(clippy::useless_vec)]` on by default
help: you can use an array directly
     |
1405 ~     let journal = [journal_entry(
1406 +             "migrate",
1407 +             "migrate",
1408 +             migrate_html,
1409 +             "1830-1900",
1410 +             "Migrate",
1411 +             &migrate_legacy,
1412 +         ),
1413 +         journal_entry(
1414 +             "hand",
1415 +             "hand",
1416 +             hand_html,
1417 +             "1900-1930",
1418 +             "Hand",
1419 +             &hand_legacy,
1420 +         ),
1421 +         journal_entry(
1422 +             "done",
1423 +             "done",
1424 +             done_html,
1425 +             "2000-2030",
1426 +             "Done",
1427 +             &done_legacy,
1428 ~         )];
     |

warning: `bob-obsidian` (test "gcal_lifecycle") generated 4 warnings (run `cargo clippy --fix --test "gcal_lifecycle" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 4 suggestions)
warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:1776:5
     |
1776 | /     journal
1777 | |         .iter()
1778 | |         .filter(|line| {
1779 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == event_id
1780 | |         })
1781 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
     = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
     |
1781 -         .last()
1781 +         .next_back()
     |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:2519:18
     |
2519 |       let latest = journal
     |  __________________^
2520 | |         .iter()
2521 | |         .filter(|line| {
2522 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == "talk"
2523 | |         })
2524 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
     |
2524 -         .last()
2524 +         .next_back()
     |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
    --> tests/gcal_sync.rs:2631:18
     |
2631 |       let latest = journal
     |  __________________^
2632 | |         .iter()
2633 | |         .filter(|line| {
2634 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == "dentist"
2635 | |         })
2636 | |         .last()
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
     |
2636 -         .last()
2636 +         .next_back()
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
    --> src/native/capture/note_pull.rs:1632:39
     |
1632 |     fn plan(harness: &mut Harness) -> Result<PlannedCaptureItem, CaptureError> {
     |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3199:10
     |
3199 |     ) -> Result<PlannedCaptureItem, CaptureError> {
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
    --> src/native/capture_language/close_log.rs:1379:9
     |
1379 | /         match lex_bullets(close, draft).expect("valid bullets") {
1380 | |             CloseLogLexed { entries, dangling } => {
1381 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1382 | |                 entries
...    |
1387 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `#[warn(clippy::match_single_binding)]` on by default
help: consider using a `let` statement
     |
1379 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1380 +         {
1381 +             assert!(dangling.is_empty(), "unexpected dangling");
1382 +             entries
1383 +                 .into_iter()
1384 +                 .map(|entry| (entry.index, entry.text, entry.details))
1385 +                 .collect()
1386 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1485:9
     |
1485 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1486 | |             CloseLogLexed { entries, dangling } => {
1487 | |                 assert!(entries.is_empty());
1488 | |                 assert_eq!(dangling.len(), 1);
...    |
1491 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1485 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1486 +         {
1487 +             assert!(entries.is_empty());
1488 +             assert_eq!(dangling.len(), 1);
1489 +             assert_eq!(dangling[0].index, Some(1));
1490 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1560:9
     |
1560 | /         match lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing")
1561 | |         {
1562 | |             error => assert!(
1563 | |                 error.message.contains("- 1 wired"),
...    |
1566 | |             ),
1567 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1560 ~         let error = lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing");
1561 +         assert!(
1562 +             error.message.contains("- 1 wired"),
1563 +             "{}",
1564 +             error.message
1565 +         )
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2057:9
     |
2057 | /         match lex_bullets("x", "x\n- *").expect("dangling star") {
2058 | |             CloseLogLexed { entries, dangling } => {
2059 | |                 assert!(entries.is_empty());
2060 | |                 assert_eq!(dangling.len(), 1);
...    |
2063 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2057 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *").expect("dangling star");
2058 +         {
2059 +             assert!(entries.is_empty());
2060 +             assert_eq!(dangling.len(), 1);
2061 +             assert_eq!(dangling[0].index, None);
2062 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2064:9
     |
2064 | /         match lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details")
2065 | |         {
2066 | |             CloseLogLexed { entries, dangling } => {
2067 | |                 assert!(entries.is_empty());
...    |
2071 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2064 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details");
2065 +         {
2066 +             assert!(entries.is_empty());
2067 +             assert_eq!(dangling.len(), 1);
2068 +             assert_eq!(dangling[0].index, None);
2069 +         }
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
    --> src/native/capture_language/tests/grammar.rs:2416:35
     |
2416 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2453:48
     |
2453 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2462:22
     |
2462 |         execute(raw).expect(&format!("{raw} executes as prose"));
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

error: constant `TODAY` is never used
 --> tests/cli/capture/merge_in.rs:8:7
  |
8 | const TODAY: &str = "2026-11-05";
  |       ^^^^^
  |
  = note: `-D dead-code` implied by `-D unused`
  = help: to override `-D unused` add `#[expect(dead_code)]` or `#[allow(dead_code)]`

warning: very complex type used. Consider factoring parts into `type` definitions
   --> tests/cli/capture/parse.rs:940:16
    |
940 |     let cases: &[(&str, &[&str], &[(u64, u64, &str, &str)])] = &[
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
    = note: `#[warn(clippy::type_complexity)]` on by default

warning: this function has too many arguments (10/7)
   --> tests/cli/capture/pomodoro_clock.rs:364:1
    |
364 | / fn assert_landing_retype(
365 | |     vault: &Path,
366 | |     day_file: &Path,
367 | |     config: &Path,
...   |
374 | |     started: bool,
375 | | ) -> Value {
    | |__________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:479:14
    |
479 |         .arg("-2 x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#suspicious_command_arg_space
    = note: `#[warn(clippy::suspicious_command_arg_space)]` on by default
help: consider splitting the argument
    |
479 -         .arg("-2 x\n- 1 wired the lexer")
479 +         .args(["-2", "x\n- 1 wired the lexer"])
    |

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
    = note: `#[warn(clippy::single_range_in_vec_init)]` on by default
help: if you wanted a `Vec` that contains the entire range, try
    |
290 -         apply_emphasis(already_strong, &[strong_start..strong_end]),
290 +         apply_emphasis(already_strong, &(strong_start..strong_end).collect::<std::vec::Vec<usize>>()),
    |

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

warning: `bob-obsidian` (test "cli") generated 7 warnings
error: could not compile `bob-obsidian` (test "cli") due to 1 previous error; 7 warnings emitted
warning: build failed, waiting for other jobs to finish...
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

warning: `bob-obsidian` (lib test) generated 525 warnings (488 duplicates) (run `cargo clippy --fix --lib -p bob-obsidian --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 8 suggestions)
error: recipe `check` failed on line 79 with exit code 101
failed  exit=101  duration=137505ms

