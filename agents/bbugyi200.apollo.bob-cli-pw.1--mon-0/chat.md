# Chat History - ace-run (bob-cli-pw.1--mon-0)

- **TIMESTAMP:** 2026-11-24 11:34:57 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-pw.1--mon-0

## Prompt

sase monitor start --command 'just check' --reason 'Verify meeting notes implementation before host completion'

## Response

sase tool run b0b8390636142353d70673d800538d26

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking cfg-if v1.0.4
    Checking typenum v1.20.1
    Checking stable_deref_trait v1.2.1
   Compiling siphasher v1.0.4
    Checking smallvec v1.15.2
    Checking memchr v2.8.1
    Checking bitflags v2.12.1
   Compiling shlex v2.0.1
    Checking equivalent v1.0.2
    Checking allocator-api2 v0.2.21
    Checking foldhash v0.2.0
    Checking libc v0.2.186
    Checking rand_core v0.10.1
    Checking zerofrom v0.1.8
    Checking writeable v0.6.4
    Checking litemap v0.8.3
    Checking scopeguard v1.2.0
    Checking new_debug_unreachable v1.0.6
    Checking serde_core v1.0.228
    Checking lock_api v0.4.14
    Checking phf_shared v0.14.0
    Checking itoa v1.0.18
    Checking simd-adler32 v0.3.9
    Checking yoke v0.8.3
   Compiling cc v1.2.63
    Checking precomputed-hash v0.1.1
    Checking utf8_iter v1.0.4
    Checking num-traits v0.2.19
    Checking log v0.4.30
    Checking cpufeatures v0.3.0
    Checking adler2 v2.0.1
    Checking utf8parse v0.2.2
    Checking hashbrown v0.17.1
    Checking icu_properties_data v2.3.0
    Checking icu_normalizer_data v2.3.0
    Checking crc32fast v1.5.0
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking anstyle-parse v1.0.0
    Checking anstyle-query v1.1.5
    Checking miniz_oxide v0.8.9
    Checking is_terminal_polyfill v1.70.2
    Checking tinyvec_macros v0.1.1
    Checking colorchoice v1.0.5
    Checking linux-raw-sys v0.12.1
    Checking dtoa v1.0.11
    Checking anstyle v1.0.14
    Checking tinyvec v1.11.0
   Compiling phf_generator v0.14.0
    Checking chacha20 v0.10.2
    Checking dtoa-short v0.3.5
    Checking anstream v1.0.0
    Checking tendril v0.5.1
   Compiling phf_codegen v0.14.0
   Compiling string_cache_codegen v0.11.2
   Compiling phf_macros v0.14.0
    Checking strsim v0.11.1
    Checking flate2 v1.1.9
    Checking unicode-width v0.2.3
    Checking once_cell v1.21.4
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking indexmap v2.14.0
    Checking cpufeatures v0.2.17
    Checking weezl v0.1.12
    Checking rustix v1.1.5
    Checking regex-syntax v0.8.10
    Checking clap_lex v1.1.0
    Checking fastrand v2.5.0
    Checking generic-array v0.14.7
    Checking icu_collections v2.3.0
    Checking hybrid-array v0.4.12
    Checking clap_builder v4.6.7
    Checking icu_locale_core v2.3.0
    Checking getopts v0.2.24
    Checking parking_lot_core v0.9.12
   Compiling web_atoms v0.3.0
    Checking getrandom v0.4.2
    Checking unicode-normalization v0.1.25
    Checking derive_more v2.1.1
    Checking nom v8.0.0
    Checking parking_lot v0.12.5
    Checking rand v0.10.1
    Checking aho-corasick v1.1.4
    Checking fdeflate v0.3.7
    Checking phf v0.14.0
    Checking string_cache v0.11.0
    Checking cssparser v0.38.0
    Checking phf_shared v0.12.1
    Checking block-buffer v0.12.0
    Checking crypto-common v0.2.2
    Checking servo_arc v0.5.0
    Checking pxfm v0.1.30
    Checking iana-time-zone v0.1.65
    Checking const-oid v0.10.2
    Checking bytecount v0.6.9
    Checking percent-encoding v2.3.2
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking icu_provider v2.3.1
    Checking block-buffer v0.10.4
    Checking unicode-bidi v0.3.18
    Checking zune-core v0.5.3
    Checking inout v0.1.4
    Checking digest v0.10.7
    Checking color_quant v1.1.0
    Checking icu_properties v2.3.0
    Checking cipher v0.4.4
    Checking icu_normalizer v2.3.0
    Checking unicode-properties v0.1.4
    Checking quick-error v2.0.1
    Checking byteorder-lite v0.1.0
   Compiling rquickjs-sys v0.12.1
    Checking rustc-hash v2.1.3
    Checking aes v0.8.4
    Checking cbc v0.1.2
    Checking selectors v0.41.0
    Checking stringprep v0.1.5
    Checking image-webp v0.2.4
    Checking digest v0.11.3
    Checking ecb v0.1.2
    Checking sha2 v0.10.9
    Checking md-5 v0.10.6
    Checking zune-jpeg v0.5.15
    Checking gif v0.14.2
    Checking tempfile v3.27.0
    Checking form_urlencoded v1.2.2
    Checking regex-automata v0.4.14
    Checking thiserror v2.0.18
    Checking phf v0.12.1
    Checking serde v1.0.228
    Checking png v0.18.1
    Checking zmij v1.0.21
    Checking encoding_rs v0.8.35
    Checking ego-tree v0.11.1
    Checking is_executable v1.0.6
    Checking bytemuck v1.25.2
    Checking unsafe-libyaml v0.2.11
    Checking ttf-parser v0.25.1
    Checking ryu v1.0.23
    Checking idna_adapter v1.2.2
    Checking clap v4.6.7
    Checking pulldown-cmark-escape v0.11.0
    Checking unicase v2.10.0
    Checking idna v1.1.0
    Checking rangemap v1.7.1
    Checking base64 v0.22.1
    Checking serde_json v1.0.150
    Checking chrono v0.4.44
    Checking pulldown-cmark v0.13.6
    Checking clap_complete v4.6.11
    Checking sha2 v0.11.0
    Checking fs2 v0.4.3
    Checking url v2.5.8
    Checking roxmltree v0.21.2
    Checking markup5ever v0.40.0
    Checking similar v2.7.0
    Checking glob v0.3.4
    Checking html5ever v0.40.1
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/crates/bob-obsidian-assets)
    Checking hex v0.4.3
    Checking nom_locate v5.0.0
    Checking moxcms v0.8.1
   Compiling libsqlite3-sys v0.38.1
    Checking serde_yaml v0.9.34+deprecated
    Checking wait-timeout v0.2.1
    Checking num-conv v0.2.2
    Checking powerfmt v0.2.0
    Checking time-core v0.1.9
    Checking bit-vec v0.10.2
    Checking quick-error v1.2.3
    Checking fnv v1.0.7
    Checking deranged v0.5.8
    Checking chrono-tz v0.10.4
    Checking hashlink v0.12.1
    Checking quick-xml v0.41.0
    Checking rand_xorshift v0.5.0
    Checking rusty-fork v0.3.1
    Checking unarray v0.1.4
    Checking fallible-iterator v0.3.0
    Checking core_detect v1.0.0
    Checking regex v1.12.3
    Checking fallible-streaming-iterator v0.1.9
    Checking bit-set v0.11.1
    Checking proptest v1.12.0
    Checking scraper v0.29.0
    Checking lopdf v0.40.0
    Checking time v0.3.53
    Checking image v0.25.10
    Checking plist v1.10.0
    Checking rusqlite v0.40.1
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10)
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

error: unused imports: `DossierDocument`, `DossierError`, and `render_dossier`
  --> src/native/meetings/mod.rs:19:20
   |
19 |     parse_dossier, render_dossier, DossierDocument, DossierError,
   |                    ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^  ^^^^^^^^^^^^
   |
   = note: `-D unused-imports` implied by `-D unused`
   = help: to override `-D unused` add `#[allow(unused_imports)]`

error: unused imports: `MAX_NOTES_BYTES`, `NotesError`, `NotesInput`, `NotesSource`, and `read_notes`
  --> src/native/meetings/mod.rs:22:5
   |
22 |     read_notes, NotesError, NotesInput, NotesSource, MAX_NOTES_BYTES,
   |     ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^  ^^^^^^^^^^^^^^^

error: unused import: `normalize::normalize`
  --> src/native/meetings/mod.rs:24:16
   |
24 | pub(crate) use normalize::normalize;
   |                ^^^^^^^^^^^^^^^^^^^^

error: unused imports: `RecapState`, `ReplaceRecapError`, `recap_state`, `render_recap`, and `replace_recap`
  --> src/native/meetings/mod.rs:26:5
   |
26 |     recap_state, render_recap, replace_recap, RecapState, ReplaceRecapError,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^  ^^^^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^^^^^^^

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

error: unused imports: `DossierDocument` and `DossierError`
  --> src/native/meetings/mod.rs:19:36
   |
19 |     parse_dossier, render_dossier, DossierDocument, DossierError,
   |                                    ^^^^^^^^^^^^^^^  ^^^^^^^^^^^^
   |
   = note: `-D unused-imports` implied by `-D unused`
   = help: to override `-D unused` add `#[allow(unused_imports)]`

error: unused imports: `NotesError` and `NotesInput`
  --> src/native/meetings/mod.rs:22:17
   |
22 |     read_notes, NotesError, NotesInput, NotesSource, MAX_NOTES_BYTES,
   |                 ^^^^^^^^^^  ^^^^^^^^^^

error: unused import: `ReplaceRecapError`
  --> src/native/meetings/mod.rs:26:59
   |
26 |     recap_state, render_recap, replace_recap, RecapState, ReplaceRecapError,
   |                                                           ^^^^^^^^^^^^^^^^^

warning: this function has too many arguments (9/7)
   --> src/native/albums/index.rs:121:1
    |
121 | / pub(crate) fn plan_index(
122 | |     path: &str,
123 | |     contents: Option<&str>,
124 | |     album_stem: &str,
...   |
130 | |     folder_complete: bool,
131 | | ) -> IndexPlan {
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:179:6
    |
179 | ) -> Result<OpOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:260:6
    |
260 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:343:6
    |
343 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:535:6
    |
535 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:589:6
    |
589 | ) -> Result<(), OpError> {
    |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:632:6
    |
632 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:932:6
    |
932 | ) -> Result<OpResult, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1237:6
     |
1237 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1327:6
     |
1327 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1533:6
     |
1533 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/albums/update/ops.rs:1524:1
     |
1524 | / fn apply_choice_add(
1525 | |     field: &str,
1526 | |     label: &str,
1527 | |     emoji: Option<&str>,
...    |
1532 | |     inputs: &ApplyInputs<'_>,
1533 | | ) -> Result<OpResult, OpError> {
     | |______________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1645:6
     |
1645 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1787:6
     |
1787 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1872:6
     |
1872 | ) -> Result<OpResult, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:1972:6
     |
1972 | ) -> Result<(RecordType, Option<String>), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2016:6
     |
2016 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2466:6
     |
2466 | ) -> Result<(), OpError> {
     |      ^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2554:6
     |
2554 | ) -> Result<String, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2576:6
     |
2576 | ) -> Result<bool, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/albums/update/ops.rs:2598:6
     |
2598 | ) -> Result<f64, OpError> {
     |      ^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
     |
     = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:242:6
    |
242 | ) -> Result<String, UpdateFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:259:20
    |
259 | fn read_stdin() -> Result<String, UpdateFailure> {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:273:6
    |
273 | ) -> Result<(VaultSnapshot, AlbumRegistry), UpdateFailure> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 224 bytes
    |
    = help: try reducing the size of `native::albums::update::run::UpdateFailure`, for example by boxing large elements or replacing it with `Box<native::albums::update::run::UpdateFailure>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/run.rs:771:10
    |
771 |     ) -> Result<UpdatePlan, UpdatePlanError> {
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
    --> src/native/bank/cli.rs:1225:13
     |
1225 |             || Ok(()),
     |             ^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/bank/cli.rs:1443:13
     |
1443 |             || Ok(()),
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
   --> src/native/bank/import_run.rs:359:6
    |
359 |   ) -> Result<
    |  ______^
360 | |     (
361 | |         BatchPlan,
362 | |         BankConfig,
...   |
369 | |     TxnFailure,
370 | | > {
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
   --> src/native/capture/cli.rs:982:10
    |
982 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1024:22
     |
1024 |                   .map(|values| {
     |  ______________________^
1025 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
1026 | |                 })
     | |_________________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1025:32
     |
1025 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
     |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1032:26
     |
1032 |                       .map(|vals| {
     |  __________________________^
1033 | |                         vals.map(|raw| {
1034 | |                             super::move_choice::parse_move_in_picks(raw)
1035 | |                         })
1036 | |                         .collect::<Result<Vec<_>, _>>()
1037 | |                     })
     | |_____________________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1033:34
     |
1033 |                           vals.map(|raw| {
     |  __________________________________^
1034 | |                             super::move_choice::parse_move_in_picks(raw)
1035 | |                         })
     | |_________________________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1046:22
     |
1046 |                 .map(|raw| parse_pull_in_picks(raw))
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1081:6
     |
1081 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1095:6
     |
1095 | ) -> Result<PullInPicks, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1131:6
     |
1131 | ) -> Result<InboxRoutePick, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1160:6
     |
1160 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1171:14
     |
1171 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1178:6
     |
1178 | ) -> Result<SubBulletTarget, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1191:6
     |
1191 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1240:6
     |
1240 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1271:6
     |
1271 | ) -> Result<String, CaptureError> {
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
    --> src/native/capture/dependencies.rs:1026:6
     |
1026 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1204:6
     |
1204 | ) -> Result<PathBuf, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1321:6
     |
1321 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1373:6
     |
1373 | ) -> Result<(String, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1484:6
     |
1484 | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:1475:1
     |
1475 | / fn resolve_prerequisites(
1476 | |     ctx: &DependencyContext,
1477 | |     planner: &mut CaptureBatchPlanner,
1478 | |     bob_dir: &Path,
...    |
1483 | |     dependent_desc: &str,
1484 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1574:10
     |
1574 |     ) -> Result<Self, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1817:24
     |
1817 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1906:6
     |
1906 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2047:6
     |
2047 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2068:6
     |
2068 | ) -> Result<Vec<TaskBlockRef>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2081:6
     |
2081 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2120:6
     |
2120 | ) -> Result<Vec<TargetTouch>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2220:6
     |
2220 | ) -> Result<Option<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2400:6
     |
2400 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2400:6
     |
2400 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2609:6
     |
2609 | ) -> Result<PlannedDependencyUpdate, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3111:6
     |
3111 | ) -> Result<(AugmentedNewTask, PlannedDependencyUpdateParts), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3369:6
     |
3369 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3427:6
     |
3427 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
   --> src/native/capture/notebook_note.rs:790:6
    |
790 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (10/7)
   --> src/native/capture/notebook_note.rs:918:1
    |
918 | / pub(super) fn notebook_item_result(
919 | |     request: &CaptureRequest,
920 | |     route: &str,
921 | |     relative_str: &str,
...   |
928 | |     kind: &'static str,
929 | | ) -> crate::native::capture::output::CaptureItemResult {
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

warning: this function has too many arguments (19/7)
   --> src/native/capture/output.rs:598:5
    |
598 | /     pub(super) fn from_items(
599 | |         items: Vec<CaptureItemResult>,
600 | |         global_destination: Option<GlobalDestinationSummary>,
601 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
617 | |         walk_files: Vec<WalkFileJson>,
618 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `to_string` applied to a type that implements `Display` in `print!` args
   --> src/native/capture/output.rs:693:22
    |
693 |                       )
    |  ______________________^
694 | |                     .to_string()
    | |________________________________^ help: remove this
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args
    = note: `#[warn(clippy::to_string_in_format_args)]` on by default

warning: `to_string` applied to a type that implements `Display` in `print!` args
   --> src/native/capture/output.rs:721:22
    |
721 |                       )
    |  ______________________^
722 | |                     .to_string()
    | |________________________________^ help: remove this
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: this function has too many arguments (8/7)
    --> src/native/capture/output.rs:8057:5
     |
8057 | /     pub(super) fn pull_in_choice_required(
8058 | |         extra: serde_json::Map<String, serde_json::Value>,
8059 | |         human_unblocked: Vec<TaskCompleteUnblockedJson>,
8060 | |         human_keep_moving_folds: Vec<
...    |
8069 | |         human_note_pull_groups: Vec<PullInGroupJson>,
8070 | |     ) -> Self {
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:207:6
    |
207 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:215:6
    |
215 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1644:6
     |
1644 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1738:6
     |
1738 | ) -> Result<FanoutClipboardRead, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1831:6
     |
1831 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2058:6
     |
2058 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2168:6
     |
2168 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (16/7)
    --> src/native/capture/plan.rs:2151:1
     |
2151 | / pub(super) fn plan_capture_item(
2152 | |     request: &CaptureRequest,
2153 | |     parsed_item: ParsedCaptureItem,
2154 | |     now: chrono::NaiveDateTime,
...    |
2167 | |     project_moves: &[ProjectMoveLanding],
2168 | | ) -> Result<PlannedCaptureItem, CaptureError> {
     | |_____________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:2959:14
     |
2959 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:3168:11
     |
3168 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4882:6
     |
4882 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5080:6
     |
5080 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5109:6
     |
5109 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5195:6
     |
5195 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5236:6
     |
5236 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:5456:6
     |
5456 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:5957:13
     |
5957 |             &String::new(),
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
   --> src/native/capture/pomodoro_close.rs:608:6
    |
608 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:653:6
    |
653 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:846:6
    |
846 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1386:6
     |
1386 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1422:6
     |
1422 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1589:6
     |
1589 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1769:6
     |
1769 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2085:6
     |
2085 | ) -> Result<Option<SizedCloseStaging>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2174:6
     |
2174 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2687:6
     |
2687 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2763:6
     |
2763 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2876:6
     |
2876 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:3492:6
     |
3492 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
  --> src/native/capture/pomodoro_link.rs:19:6
   |
19 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:232:6
    |
232 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:288:6
    |
288 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:727:6
    |
727 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:824:6
    |
824 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1009:6
     |
1009 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1054:6
     |
1054 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1850:6
     |
1850 | ) -> Result<&str, CaptureError> {
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
    --> src/native/capture/pomodoro_start.rs:1255:6
     |
1255 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1523:6
     |
1523 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2178:6
     |
2178 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2281:6
     |
2281 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2346:6
     |
2346 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2516:6
     |
2516 | ) -> Result<PlannedCaptureItem, CaptureError> {
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
    --> src/native/capture/project_note.rs:2267:6
     |
2267 | ) -> Result<Vec<ResolvedProjectMove>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2432:6
     |
2432 | ) -> Result<ProjectMoveExecution, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/project_note.rs:2444:14
     |
2444 |           .map(|movement| {
     |  ______________^
2445 | |             slot_by_source.get(&movement.source_index).copied().ok_or_else(
2446 | |                 || {
2447 | |                     CaptureError::io(
...    |
2452 | |         })
     | |_________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3053:6
     |
3053 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
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

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/pull_in.rs:116:22
    |
116 |                   .map(|selector| {
    |  ______________________^
117 | |                     resolve_jump_offer(&probe.items, &selector, &probe_pull_in)
118 | |                 })
    | |_________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:164:6
    |
164 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:232:6
    |
232 | ) -> Result<PlannedCaptureBatch, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:243:6
    |
243 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:267:6
    |
267 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:295:6
    |
295 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:629:6
    |
629 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/record_note.rs:198:6
    |
198 | ) -> Result<Vec<super::output::WalkFileJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/record_note.rs:363:6
    |
363 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/record_note.rs:612:6
    |
612 | ) -> Result<(), CaptureError> {
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
   --> src/native/capture/relations_close.rs:235:6
    |
235 | ) -> Result<ItemRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations_close.rs:226:1
    |
226 | / pub(super) fn plan_item_relations(
227 | |     ctx: &mut DependencyContext,
228 | |     planner: &mut CaptureBatchPlanner,
229 | |     request: &CaptureRequest,
...   |
234 | |     warnings: &mut Vec<CaptureWarning>,
235 | | ) -> Result<ItemRelationReports, CaptureError> {
    | |______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:273:6
    |
273 | ) -> Result<RelationCloseReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:473:6
    |
473 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this boolean expression can be simplified
   --> src/native/capture/relations_close.rs:497:14
    |
497 |         if !(cancel && complete || cancel && merge || complete && merge) {
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
497 -         if !(cancel && complete || cancel && merge || complete && merge) {
497 +         if !(!(!cancel || !complete && !merge) || complete && merge) {
    |
497 -         if !(cancel && complete || cancel && merge || complete && merge) {
497 +         if !((merge || complete) && cancel || complete && merge) {
    |

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_complete.rs:40:6
   |
40 | ) -> Result<RelationCompleteReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:150:6
    |
150 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:186:6
    |
186 | ) -> Result<Option<PlannedSourceComplete>, CaptureError> {
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
   --> src/native/capture/req_choice.rs:128:6
    |
128 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/req_choice.rs:173:6
    |
173 | ) -> Result<CardPick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/req_choice.rs:211:6
    |
211 | ) -> Result<SplitCard, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/req_choice.rs:202:1
    |
202 | / pub(super) fn split_card_selection(
203 | |     owners: &[ReqCloseOwner],
204 | |     offer_keys: &[String],
205 | |     carry: &[String],
...   |
210 | |     req_aware: bool,
211 | | ) -> Result<SplitCard, CaptureError> {
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/req_choice.rs:442:6
    |
442 |   ) -> Result<
    |  ______^
443 | |     (Vec<ReqCloseOwner>, ReqWritePlan, Option<ReqCardTarget>),
444 | |     CaptureError,
445 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/req_close.rs:49:6
   |
49 | ) -> Result<ReqWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/req_placement.rs:93:6
   |
93 | ) -> Result<ReqLinkPlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/req_placement.rs:153:6
    |
153 | ) -> Result<Option<(CaptureJumpJson, ReqLanding)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/req_placement.rs:175:6
    |
175 | ) -> Result<Option<(CaptureJumpJson, ReqLanding)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
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
 --> src/native/capture/sub_bullet.rs:9:6
  |
9 | ) -> Result<CaptureWritePlan, CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sub_bullet.rs:51:6
   |
51 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
  --> src/native/capture/sub_bullet.rs:42:1
   |
42 | / pub(super) fn plan_sub_bullet_capture(
43 | |     planner: &mut CaptureBatchPlanner,
44 | |     bob_dir: &Path,
45 | |     target: &Path,
...  |
50 | |     warnings: &mut Vec<CaptureWarning>,
51 | | ) -> Result<CaptureWritePlan, CaptureError> {
   | |___________________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:227:6
    |
227 | ) -> Result<(CaptureWritePlan, RequirementWriteJson), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/sub_bullet.rs:218:1
    |
218 | / pub(super) fn plan_insert_reqs_capture(
219 | |     planner: &mut CaptureBatchPlanner,
220 | |     bob_dir: &Path,
221 | |     target: &Path,
...   |
226 | |     dry_run: bool,
227 | | ) -> Result<(CaptureWritePlan, RequirementWriteJson), CaptureError> {
    | |___________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:300:6
    |
300 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:372:6
    |
372 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:415:6
    |
415 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/sub_bullet.rs:405:1
    |
405 | / fn plan_prj_section_capture(
406 | |     planner: &mut CaptureBatchPlanner,
407 | |     bob_dir: &Path,
408 | |     target: &Path,
...   |
414 | |     warnings: &mut Vec<CaptureWarning>,
415 | | ) -> Result<CaptureWritePlan, CaptureError> {
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:662:6
    |
662 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_complete.rs:52:6
   |
52 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:181:6
    |
181 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:980:6
    |
980 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1247:6
     |
1247 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
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
   --> src/native/capture/transfer.rs:652:6
    |
652 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:678:6
    |
678 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:743:6
    |
743 |   ) -> Result<
    |  ______^
744 | |     (
745 | |         RelationMergeOutput,
746 | |         Vec<crate::native::task_move::transplant::RepairedFile>,
747 | |     ),
748 | |     CaptureError,
749 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:217:6
    |
217 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:415:44
    |
415 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
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
   --> src/native/capture_drawers.rs:730:16
    |
730 |     for idx in start_idx..end_idx.min(lines.len()) {
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
730 -     for idx in start_idx..end_idx.min(lines.len()) {
730 +     for (idx, <item>) in lines.iter().enumerate().take(end_idx.min(lines.len())).skip(start_idx) {
    |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_drawers.rs:959:35
    |
959 | pub(crate) fn rank_drawer_catalog<'a>(
    |                                   ^^
960 |     records: &'a BTreeMap<String, DrawerCatalogRecord>,
    |               ^^
961 | ) -> Vec<&'a DrawerCatalogRecord> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
959 ~ pub(crate) fn rank_drawer_catalog(
960 ~     records: &BTreeMap<String, DrawerCatalogRecord>,
961 ~ ) -> Vec<&DrawerCatalogRecord> {
    |

warning: called `filter(..).next_back()` on an `DoubleEndedIterator`. This is more succinctly expressed by calling `.rfind(..)` instead
    --> src/native/capture_drawers.rs:1628:5
     |
1628 | /     direct_child_list_indexes(&lines, drawer.line_index(), drawer.block_end)
1629 | |         .into_iter()
1630 | |         .filter(|&index| line_start(&lines, index) < insertion.offset)
1631 | |         .filter(|&index| {
1632 | |             parse_managed_task_log_marker(lines[index].text).is_none()
1633 | |         })
1634 | |         .next_back()
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
    --> src/native/capture_language/completion.rs:1306:19
     |
1306 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast

warning: the following explicit lifetimes could be elided: 'i
    --> src/native/capture_language/completion.rs:1678:29
     |
1678 | fn merge_in_completion_slot<'i, 's>(
     |                             ^^
1679 |     item: &'i CaptureItem<'s>,
     |            ^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
     |
1678 ~ fn merge_in_completion_slot<'s>(
1679 ~     item: &CaptureItem<'s>,
     |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:2174:22
     |
2174 |       let mut targets: Vec<(
     |  ______________________^
2175 | |         String,
2176 | |         String,
2177 | |         &'static str,
2178 | |         Option<(usize, usize)>,
2179 | |     )> = Vec::new();
     | |______^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:2445:6
     |
2445 |   ) -> Result<
     |  ______^
2446 | |     Vec<(
2447 | |         ParsedCaptureText,
2448 | |         Option<RefParentSource>,
...    |
2451 | |     TemplateCodedError,
2452 | | > {
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
   --> src/native/capture_language/editor_model.rs:888:1
    |
888 | / pub(super) enum TokenParse {
889 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 520 bytes
890 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 136 bytes
891 | | }
    | |_^ the entire enum is at least 520 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
889 -     Marker(MarkerParse),
889 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:2721:1
     |
2721 | / fn empty_editor_item(
2722 | |     item: &CaptureItem<'_>,
2723 | |     mode: EditorMode,
2724 | |     route: Option<String>,
...    |
2729 | |     diagnostics: Vec<Diagnostic>,
2730 | | ) -> EditorItemParse {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:3583:1
     |
3583 | / fn attach_drawer_bullet_metadata(
3584 | |     item: &CaptureItem<'_>,
3585 | |     mode: &mut EditorMode,
3586 | |     parent_body: &str,
...    |
3591 | |     sub_bullets: &mut [AuthoredSubBullet],
3592 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:4186:35
     |
4186 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `#[warn(clippy::trim_split_whitespace)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:4913:5
     |
4913 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:4912:5
     |
4912 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:305:1
    |
305 | / pub(super) fn parse_editor_named_start_item<'a>(
306 | |     item: &CaptureItem<'a>,
307 | |     parent_trimmed: &str,
308 | |     suffix: String,
...   |
314 | |     spelling: NameSpelling,
315 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_pomodoro.rs:3343:1
     |
3343 | / fn editor_past_outcome<'a>(
3344 | |     item: &CaptureItem<'a>,
3345 | |     parent_trimmed: &str,
3346 | |     mode: EditorMode,
...    |
3351 | |     diagnostics: Vec<Diagnostic>,
3352 | | ) -> EditorItemOutcome<'a> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:130:6
    |
130 |   ) -> Option<
    |  ______^
131 | |     Result<
132 | |         (
133 | |             LineOutcome<'a>,
...   |
138 | |     >,
139 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:223:6
    |
223 |   ) -> Option<
    |  ______^
224 | |     Result<
225 | |         (
226 | |             LineOutcome<'a>,
...   |
231 | |     >,
232 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:1435:5
     |
1435 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1434:5
     |
1434 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/item.rs:1322:35
     |
1322 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:2192:1
     |
2192 | / fn parse_capture_item_masked<'a>(
2193 | |     item: &CaptureItem<'a>,
2194 | |     forced_route: Option<&str>,
2195 | |     forced_section: Option<&str>,
...    |
2200 | |     target_run: Option<&TargetRunContext>,
2201 | | ) -> Result<ParsedCaptureItemOutcome<'a>, String> {
     | |_________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:2532:5
     |
2532 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:2531:5
     |
2531 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:5028:1
     |
5028 | / pub(super) fn named_shape_error_with_drop(
5029 | |     token: &str,
5030 | |     suffix: &str,
5031 | |     name: &str,
...    |
5036 | |     is_literal: bool,
5037 | | ) -> String {
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
    --> src/native/capture_language/notebook.rs:1428:6
     |
 989 |     Supported(RouteMarker),
     |     ---------------------- the largest variant contains at least 160 bytes
...
1428 | ) -> Result<Option<NotebookRouteInfo>, RouteScan> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_language::notebook::RouteScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::notebook::RouteScan>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_language/notebook.rs:1450:6
     |
 989 |     Supported(RouteMarker),
     |     ---------------------- the largest variant contains at least 160 bytes
...
1450 | ) -> Result<Option<NotebookClaim>, RouteScan> {
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
   --> src/native/capture_language/record.rs:87:1
    |
 87 | /   pub(crate) enum PerRouteDecision {
 88 | | /     AlbumValid {
 89 | | |         record_type: RecordType,
 90 | | |         album: AlbumRouteMeta,
 91 | | |     },
    | | |_____- the largest variant contains at least 272 bytes
 92 | | /     AlbumInvalid {
 93 | | |         paths: Vec<String>,
 94 | | |         findings: Vec<AlbumFinding>,
 95 | | |     },
    | | |_____- the second-largest variant contains at least 48 bytes
...   |
 99 | |       },
100 | |   }
    | |___^ the entire enum is at least 272 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
 89 -         record_type: RecordType,
 89 +         record_type: Box<RecordType>,
    |

warning: large size difference between variants
   --> src/native/capture_language/record.rs:671:1
    |
671 | / enum RouteResolution {
672 | |     /// A configured folder: claim creation.
673 | |     Configured,
    | |     ---------- the second-largest variant carries no data at all
674 | |     /// A teaching refusal (type id or existing
675 | |     /// non-record folder).
676 | |     Refused(RecordClaim),
    | |     -------------------- the largest variant contains at least 216 bytes
677 | |     /// An unknown folder: stay literal task text.
678 | |     Literal,
679 | | }
    | |_^ the entire enum is at least 216 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
676 -     Refused(RecordClaim),
676 +     Refused(Box<RecordClaim>),
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
    --> src/native/capture_language/rewrite.rs:2391:8
     |
2391 |       if !raw_text[..run_start]
     |  ________^
2392 | |         .chars()
2393 | |         .next_back()
2394 | |         .is_some_and(|before| !before.is_whitespace())
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
2391 ~     if raw_text[..run_start]
2392 +         .chars()
2393 +         .next_back().is_none_or(|before| before.is_whitespace())
     |

warning: this function has too many arguments (9/7)
    --> src/native/capture_language/rewrite.rs:2606:1
     |
2606 | / fn candidate_selects_plain_marker(
2607 | |     candidate: &str,
2608 | |     start: usize,
2609 | |     end: usize,
...    |
2615 | |     id_part: &str,
2616 | | ) -> bool {
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
   --> src/native/capture_language/type_marker.rs:461:45
    |
461 |           } else if lex.decoded.contains('+') {
    |  _____________________________________________^
462 | |             (
463 | |                 TypeMarkerOccurrence::Invalid {
464 | |                     span: start..raw_end,
...   |
469 | |         } else if marker_end != raw_end {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/type_marker.rs:469:41
    |
469 |           } else if marker_end != raw_end {
    |  _________________________________________^
470 | |             (
471 | |                 TypeMarkerOccurrence::Invalid {
472 | |                     span: start..raw_end,
...   |
477 | |         } else {
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: this function has too many arguments (8/7)
    --> src/native/capture_parse.rs:2965:1
     |
2965 | / fn refusal_diagnostic(
2966 | |     spans: &[Span],
2967 | |     mode: EditorMode,
2968 | |     pomodoro_start: &Option<PomodoroStartSpec>,
...    |
2973 | |     source: &str,
2974 | | ) -> Option<Diagnostic> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_pomodoro_close/ledger.rs:806:24
    |
806 |       let Some(anchor) = scan
    |  ________________________^
807 | |         .entries
808 | |         .iter()
809 | |         .filter(|entry| {
...   |
812 | |         })
813 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
813 -         .last()
813 +         .next_back()
    |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:158:1
    |
158 | / pub(crate) enum PomodoroCloseOutcome {
159 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 712 bytes
160 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
161 | | }
    | |_^ the entire enum is at least 712 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
159 -     Close(PomodoroClosePlan),
159 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:324:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
324 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:371:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
371 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:559:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
559 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:576:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
576 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:596:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
596 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:619:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
619 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:682:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
682 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:756:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
756 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:910:10
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
910 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:988:6
    |
153 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
988 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1013:6
     |
 153 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1013 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1042:6
     |
 153 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1042 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1033:1
     |
1033 | / pub(crate) fn plan_pomodoro_close_for_entry<V: CloseVault>(
1034 | |     day_path: &Path,
1035 | |     day_contents: &str,
1036 | |     entry: &RunningPomodoro,
...    |
1041 | |     policy: LedgerClosePolicy,
1042 | | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1331:1
     |
1331 | / fn resolve_close_clock_fact<V: CloseVault, S: HomeSource>(
1332 | |     vault: &V,
1333 | |     resolver: &mut HomeResolver<S>,
1334 | |     events: &[EventNoteRow],
...    |
1340 | |     all_settings: &NoteTaskSettings,
1341 | | ) -> CloseClockFact {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1746:6
     |
 153 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1746 | ) -> Result<(), PomodoroClosePlanError> {
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

warning: this function has too many arguments (8/7)
    --> src/native/capture_pomodoros_agenda.rs:1574:1
     |
1574 | / fn build_lines(
1575 | |     line_text: &[&str],
1576 | |     fenced: &BTreeSet<usize>,
1577 | |     depths: &[usize],
...    |
1582 | |     reqs: &BTreeMap<usize, super::task_reqs::ReqLineJson>,
1583 | | ) -> Vec<AgendaLine> {
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
   --> src/native/capture_rewrite.rs:481:13
    |
481 | /             match album_alias {
482 | |                 Some(route) => {
483 | |                     Some(super::capture_record::record_policy_for_draft(
484 | |                         &bob_env::bob_dir(),
...   |
488 | |                 None => None,
489 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
    = note: `#[warn(clippy::manual_map)]` on by default
help: try
    |
481 ~             album_alias.map(|route| super::capture_record::record_policy_for_draft(
482 +                         &bob_env::bob_dir(),
483 +                         &format!("@{route}/"),
484 +                     ))
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

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/link_repair.rs:988:6
    |
988 | ) -> io::Result<Option<(String, BTreeSet<String>, BTreeSet<String>)>> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/collect_done/link_repair.rs:1504:1
     |
1504 | / fn skip_repaired_span(
1505 | |     skip_code: bool,
1506 | |     line_index: usize,
1507 | |     line: &str,
...    |
1512 | |     protect_frontmatter: bool,
1513 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:613:10
    |
613 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:625:10
    |
625 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/collect_done/pair.rs:642:10
    |
642 |     ) -> io::Result<(Option<Self>, Vec<(PathBuf, String)>)>
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1200:21
     |
1200 |                     &[archive.clone()],
     |                     ^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(archive)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1228:21
     |
1228 |                     &[source.clone()],
     |                     ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(source)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1250:21
     |
1250 |                     &[archive.clone()],
     |                     ^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(archive)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/collect_done/pair.rs:1266:21
     |
1266 |                     &[source.clone()],
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
    --> src/native/highlights_ref/create.rs:2026:1
     |
2026 | / pub(super) fn stamp_overwrite_source(
2027 | |     config: &Config,
2028 | |     plan: &OverwritePreflight,
2029 | |     options: &CreateOptions,
...    |
2034 | |     info: &PdfInfo,
2035 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2068:1
     |
2068 | / pub(super) fn stage_overwrite_audio(
2069 | |     options: &CreateOptions,
2070 | |     plan: &OverwritePreflight,
2071 | |     request: &OverwriteRequest,
...    |
2076 | |     title: &str,
2077 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2788:1
     |
2788 | / fn plan_target_for(
2789 | |     config: &Config,
2790 | |     stem: &str,
2791 | |     ref_type: &str,
...    |
2796 | |     source_display: &str,
2797 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3820:1
     |
3820 | / fn stage_overwrite_source_store(
3821 | |     _config: &Config,
3822 | |     plan: &OverwritePreflight,
3823 | |     scratch: &Path,
...    |
3830 | |     catalog: &super::code_catalog::CatalogOutcome,
3831 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4516:1
     |
4516 | / fn overwrite_pdf_url(
4517 | |     config: &Config,
4518 | |     url: super::clip_url::WebUrl,
4519 | |     downloaded: PathBuf,
...    |
4524 | |     selection: &OverwriteSelection,
4525 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4598:1
     |
4598 | / fn create_pdf_url_route(
4599 | |     config: &Config,
4600 | |     url: super::clip_url::WebUrl,
4601 | |     downloaded: PathBuf,
...    |
4606 | |     listen: Option<&super::listen::ListenCommand>,
4607 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5335:1
     |
5335 | / fn print_pdf_dry_run(
5336 | |     config: &Config,
5337 | |     styler: &Styler,
5338 | |     source_display: &str,
...    |
5346 | |     legacy: &[sources_mod::RecordedSource],
5347 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
    --> src/native/highlights_ref/create.rs:5576:1
     |
5576 | / fn compose_markdown_marker(
5577 | |     status: &str,
5578 | |     parent: &str,
5579 | |     title: &str,
...    |
5585 | |     return_links: bool,
5586 | | ) -> Result<String> {
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
   --> src/native/highlights_ref/clip_adapter.rs:827:5
    |
827 | /     DIAGRAM_TIMEOUT_BASE_SECS
828 | |         .saturating_add(
829 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
832 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
827 ~     DIAGRAM_TIMEOUT_BASE_SECS
828 +         .saturating_add(
829 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
830 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:782:1
    |
782 | / pub(super) enum PdfSyncOutcome {
783 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
784 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
785 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
783 -     Written(SyncWriteReport),
783 +     Written(Box<SyncWriteReport>),
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:856:1
    |
856 | / pub(super) enum ScanWriteOutcome {
857 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
858 | |     Held(ScanHold),
859 | |     Failed(ScanFailure),
    | |     ------------------- the second-largest variant contains at least 168 bytes
860 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
857 -     Written(SyncWriteReport),
857 +     Written(Box<SyncWriteReport>),
    |

warning: this function has too many arguments (9/7)
  --> src/native/highlights_ref/note_snapshot/plan.rs:62:1
   |
62 | / pub(crate) fn plan_snapshot<L: SourceLoader>(
63 | |     store: &mut SourceStore<L>,
64 | |     note: ClassifiedNote,
65 | |     settings: &SnapshotSettings,
...  |
71 | |     parent_default_reason: Option<String>,
72 | | ) -> Result<SnapshotPlan, String> {
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
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:415:17
    |
415 |         blocks: &mut Vec<Block>,
    |                 ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
415 -         blocks: &mut Vec<Block>,
415 +         blocks: &mut [Block],
    |

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:606:21
    |
606 |                     *block = Box::new(expanded);
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace existing content with inner value instead: `**block = expanded`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box
    = note: `#[warn(clippy::replace_box)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:871:10
    |
871 |       ) -> (
    |  __________^
872 | |         BTreeMap<(AnchorIdentity, String), SnapshotAnchor>,
873 | |         BTreeMap<AnchorIdentity, String>,
874 | |         Vec<SnapshotAnchor>,
875 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1194:1
     |
1194 | / fn compose_bob_masthead<L: SourceLoader>(
1195 | |     masthead: &mut SnapshotMasthead,
1196 | |     source: &SourceIdentity,
1197 | |     kind: &NoteKind,
...    |
1204 | |     settings: &SnapshotSettings,
1205 | | ) {
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

warning: large size difference between variants
   --> src/native/highlights_ref/podcast/feed.rs:155:1
    |
155 | / pub(crate) enum FeedOutcome {
156 | |     /// Exactly one feed item agreed on at least two signals.
157 | |     Matched(FeedItem),
    | |     ----------------- the largest variant contains at least 248 bytes
158 | |     /// No usable feed: no iTunes candidate, or no candidate feed could be
159 | |     /// fetched and parsed.
160 | |     NoFeed(String),
    | |     -------------- the second-largest variant contains at least 24 bytes
...   |
167 | |     Off,
168 | | }
    | |_^ the entire enum is at least 248 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
157 -     Matched(FeedItem),
157 +     Matched(Box<FeedItem>),
    |

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
    --> src/native/highlights_ref/overwrite.rs:1474:1
     |
1474 | / fn frozen_body(
1475 | |     body: &str,
1476 | |     live_note: &str,
1477 | |     title: &str,
...    |
1482 | |     annotated_pdf: Option<&str>,
1483 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (14/7)
    --> src/native/highlights_ref/overwrite.rs:1567:1
     |
1567 | / fn plan_annotated_archive(
1568 | |     config: &Config,
1569 | |     live_note: &str,
1570 | |     ref_type: &str,
...    |
1581 | |     assets_relative: Option<&Path>,
1582 | | ) -> Result<AnnotatedArchivePlan, OverwriteRefusal> {
     | |___________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/highlights_ref/scan_apply.rs:92:6
   |
92 | ) -> std::result::Result<AppliedFullScan, ApplyError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 176 bytes
   |
   = help: try reducing the size of `native::highlights_ref::scan_apply::ApplyError`, for example by boxing large elements or replacing it with `Box<native::highlights_ref::scan_apply::ApplyError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/highlights_ref/scan_apply.rs:160:6
    |
160 | ) -> std::result::Result<(), ApplyError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 176 bytes
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
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 176 bytes
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

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/highlights_ref/scan_plan.rs:1717:6
     |
1717 |   ) -> Result<(
     |  ______^
1718 | |     Vec<PathBuf>,
1719 | |     Vec<PathBuf>,
1720 | |     Vec<PathBuf>,
1721 | |     BTreeSet<PathBuf>,
1722 | |     BTreeSet<PathBuf>,
1723 | | )> {
     | |__^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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
    --> src/native/highlights_ref/sidecar_render.rs:1274:1
     |
1274 | / fn append_resolved_image_notes(
1275 | |     config: &Config,
1276 | |     ref_note_path: &Path,
1277 | |     annotation_order: usize,
...    |
1283 | |     image_asset_writes_by_dest: &mut BTreeMap<PathBuf, ImageAssetWrite>,
1284 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/sidecar_render.rs:2489:1
     |
2489 | / pub(super) fn render_annotation_block(
2490 | |     config: &Config,
2491 | |     ref_note_path: &Path,
2492 | |     annotation: &SidecarAnnotation,
...    |
2497 | |     strip_return_links: bool,
2498 | | ) -> String {
     | |___________^
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
   --> src/native/log_history/cli.rs:179:13
    |
179 | /             pair[0] == "--format" && pair[1] == "json"
180 | |                 || pair[0] == "-f" && pair[1] == "json"
    | |_______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
179 -             pair[0] == "--format" && pair[1] == "json"
180 -                 || pair[0] == "-f" && pair[1] == "json"
179 +             !(pair[1] != "json" || pair[0] != "--format" && pair[0] != "-f")
    |
179 -             pair[0] == "--format" && pair[1] == "json"
180 -                 || pair[0] == "-f" && pair[1] == "json"
179 +             (pair[0] == "-f" || pair[0] == "--format") && pair[1] == "json"
    |

error: this `if` statement can be collapsed
   --> src/native/meetings/dossier.rs:241:9
    |
241 | /         if let Some((level, heading)) = atx_heading(line) {
242 | |             if (2..=3).contains(&level) {
243 | |                 if heading.eq_ignore_ascii_case("transcript") {
244 | |                     active = BodySection::Transcript;
...   |
265 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
    = note: requested on the command line with `-D clippy::collapsible-if`
help: collapse nested if block
    |
241 ~         if let Some((level, heading)) = atx_heading(line)
242 ~             && (2..=3).contains(&level) {
243 |                 if heading.eq_ignore_ascii_case("transcript") {
...
263 |                 continue;
264 ~             }
    |

warning: stripping a prefix manually
   --> src/native/meetings/dossier.rs:268:24
    |
268 |             let item = line[2..].to_string();
    |                        ^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/meetings/dossier.rs:267:9
    |
267 |         if line.starts_with("- ") {
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_prefix` method
    |
267 ~         if let Some(<stripped>) = line.strip_prefix("- ") {
268 ~             let item = <stripped>.to_string();
    |

error: this manual char comparison can be written more succinctly
   --> src/native/meetings/intake.rs:107:43
    |
107 |         .map(|line| line.trim_end_matches(|ch| ch == ' ' || ch == '\t'))
    |                                           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `[' ', '\t']`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_pattern_char_comparison
    = note: requested on the command line with `-D clippy::manual-pattern-char-comparison`

error: this manual char comparison can be written more succinctly
  --> src/native/meetings/normalize.rs:35:43
   |
35 |         .map(|line| line.trim_end_matches(|ch| ch == ' ' || ch == '\t'))
   |                                           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `[' ', '\t']`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_pattern_char_comparison

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

warning: unnecessary use of `get(&path).is_none()`
   --> src/native/periods/brief.rs:263:28
    |
263 |                 if buffers.get(&path).is_none() {
    |                    --------^^^^^^^^^^^^^^^^^^^^
    |                    |
    |                    help: replace it with: `!buffers.contains_key(&path)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
    = note: `#[warn(clippy::unnecessary_get_then_check)]` on by default

warning: consider using `sort_by_key`
    --> src/native/periods/brief.rs:1034:5
     |
1034 |     scored_roots.sort_by(|left, right| right.0.cmp(&left.0));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
     |
1034 -     scored_roots.sort_by(|left, right| right.0.cmp(&left.0));
1034 +     scored_roots.sort_by_key(|right| std::cmp::Reverse(right.0));
     |

warning: this `if` has identical blocks
   --> src/native/periods/draft.rs:549:54
    |
549 |       } else if matches!(subject, NoteSubject::Day(_)) {
    |  ______________________________________________________^
550 | |         "drafted".to_string()
551 | |     } else if draft.review.trim().is_empty() && !has_review_body {
    | |_____^
    |
note: same as this
   --> src/native/periods/draft.rs:551:66
    |
551 |       } else if draft.review.trim().is_empty() && !has_review_body {
    |  __________________________________________________________________^
552 | |         "drafted".to_string()
553 | |     } else if draft.review.trim().is_empty() {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: the loop variable `index` is used to index `lines`
   --> src/native/periods/draft.rs:946:18
    |
946 |     for index in heading + 1..limit {
    |                  ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
946 -     for index in heading + 1..limit {
946 +     for (index, <item>) in lines.iter().enumerate().take(limit).skip(heading + 1) {
    |

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:126:5
    |
126 |     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
126 -     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
126 +     rows.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: the loop variable `j` is used to index `lines`
   --> src/native/periods/migrate_intentions.rs:916:26
    |
916 |                 for j in index + 1..lines.len() {
    |                          ^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
916 -                 for j in index + 1..lines.len() {
916 +                 for (j, <item>) in lines.iter().enumerate().skip(index + 1) {
    |

warning: the loop variable `k` is only used to index `skip`
   --> src/native/periods/migrate_intentions.rs:925:26
    |
925 |                 for k in index..limit {
    |                          ^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
925 -                 for k in index..limit {
925 +                 for <item> in skip.iter_mut().take(limit).skip(index) {
    |

warning: the loop variable `i` is used to index `lines`
   --> src/native/periods/migrate_intentions.rs:962:14
    |
962 |     for i in heading + 1..limit {
    |              ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
962 -     for i in heading + 1..limit {
962 +     for (i, <item>) in lines.iter().enumerate().take(limit).skip(heading + 1) {
    |

warning: this `if` has identical blocks
   --> src/native/periods/migrate_intentions.rs:985:62
    |
985 |           if out.trim_end_matches('\n').ends_with("## Review") {
    |  ______________________________________________________________^
986 | |             out.push('\n');
987 | |         } else if !out.is_empty() {
    | |_________^
    |
note: same as this
   --> src/native/periods/migrate_intentions.rs:987:35
    |
987 |           } else if !out.is_empty() {
    |  ___________________________________^
988 | |             out.push('\n');
989 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: this `if` has identical blocks
   --> src/native/periods/note.rs:420:57
    |
420 |               if !name.is_empty() && !name.contains("  ") {
    |  _________________________________________________________^
421 | |                 current = Some(name);
422 | |             } else if !name.is_empty() {
    | |_____________^
    |
note: same as this
   --> src/native/periods/note.rs:422:40
    |
422 |               } else if !name.is_empty() {
    |  ________________________________________^
423 | |                 current = Some(name);
424 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/periods/report.rs:1298:6
     |
1298 | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
    --> src/native/periods/report.rs:1289:1
     |
1289 | / fn build_parts(
1290 | |     vault: &Path,
1291 | |     id: PeriodId,
1292 | |     span: Span,
...    |
1297 | |     period_charts: &charts::Charts,
1298 | | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/cli.rs:352:6
    |
352 | ) -> Result<(PathBuf, String), CliError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::props::cli::CliError`, for example by boxing large elements or replacing it with `Box<native::props::cli::CliError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/cli.rs:848:40
    |
848 | fn read_input(matches: &ArgMatches) -> Result<String, CliError> {
    |                                        ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 136 bytes
    |
    = help: try reducing the size of `native::props::cli::CliError`, for example by boxing large elements or replacing it with `Box<native::props::cli::CliError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/expand.rs:19:6
   |
19 | ) -> Result<Vec<Op>, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/expand.rs:91:6
   |
91 | ) -> Result<Vec<Op>, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/parent.rs:22:6
   |
22 | ) -> Result<&Context, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/parent.rs:43:6
   |
43 | ) -> Result<PathBuf, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/parent.rs:83:6
   |
83 | ) -> Result<String, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/contract/parent.rs:202:6
    |
202 | ) -> Result<(), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/validate.rs:50:6
   |
50 | ) -> Result<(Value, Vec<PropsError>), PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/contract/validate.rs:180:6
    |
180 | ) -> Result<(), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/contract/validate.rs:218:6
    |
218 | ) -> Result<(), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/contract/validate.rs:241:6
    |
241 | ) -> Result<Vec<PropsError>, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `index` is used to index `lines`
   --> src/native/props/document.rs:341:18
    |
341 |     for index in inner_start..inner_end.min(lines.len()) {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
341 -     for index in inner_start..inner_end.min(lines.len()) {
341 +     for (index, <item>) in lines.iter().enumerate().take(inner_end.min(lines.len())).skip(inner_start) {
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/props/document.rs:386:30
    |
386 |           let end_line_index = value_lines
    |  ______________________________^
387 | |             .iter()
388 | |             .enumerate()
389 | |             .filter(|(_, line)| !root_trivia(&line.text))
390 | |             .map(|(offset, _)| root.index + offset)
391 | |             .last()
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
391 -             .last()
391 +             .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/props/document.rs:413:31
    |
413 |           let last_value_line = value_lines
    |  _______________________________^
414 | |             .iter()
415 | |             .enumerate()
416 | |             .filter(|(_, line)| !root_trivia(&line.text))
417 | |             .map(|(offset, _)| root.index + offset)
418 | |             .last()
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
418 -             .last()
418 +             .next_back()
    |

warning: this function has too many arguments (14/7)
   --> src/native/props/document.rs:791:1
    |
791 | / fn build_entry(
792 | |     key: String,
793 | |     semantic_key: YamlValue,
794 | |     line: usize,
...   |
805 | |     inline_comment_range: Option<Range<usize>>,
806 | | ) -> PropertyEntry {
    | |__________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/emit.rs:65:6
   |
65 | ) -> Result<TypedValue, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/emit.rs:107:6
    |
107 | ) -> Result<YamlValue, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/emit.rs:181:6
    |
181 | ) -> Result<YamlValue, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/emit.rs:680:6
    |
680 | ) -> Result<YamlValue, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/emit.rs:707:6
    |
707 | ) -> Result<(), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/plan.rs:47:6
   |
47 | ) -> Result<PlanOutcome, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:154:6
    |
154 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:226:6
    |
226 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/props/plan.rs:217:1
    |
217 | / fn apply_set(
218 | |     contents: &str,
219 | |     document: &PropsDocument,
220 | |     context: &InspectContext,
...   |
225 | |     index: usize,
226 | | ) -> Result<(String, Vec<Op>), PropsError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:299:6
    |
299 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/props/plan.rs:290:1
    |
290 | / fn apply_set_yaml(
291 | |     contents: &str,
292 | |     document: &PropsDocument,
293 | |     context: &InspectContext,
...   |
298 | |     canonical_block: bool,
299 | | ) -> Result<(String, Vec<Op>), PropsError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:353:6
    |
353 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:372:6
    |
372 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:423:6
    |
423 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:449:6
    |
449 | ) -> Result<(String, Vec<Op>), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/props/plan.rs:440:1
    |
440 | / fn apply_restore(
441 | |     contents: &str,
442 | |     document: &PropsDocument,
443 | |     context: &InspectContext,
...   |
448 | |     index: usize,
449 | | ) -> Result<(String, Vec<Op>), PropsError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:640:6
    |
640 | ) -> Result<String, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:663:6
    |
663 | ) -> Result<String, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:681:6
    |
681 | ) -> Result<usize, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:911:56
    |
911 | fn validate_raw(raw: &str, key: &str, index: usize) -> Result<(), PropsError> {
    |                                                        ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/plan.rs:964:57
    |
964 | fn validate_framing(framing: &Framing, index: usize) -> Result<(), PropsError> {
    |                                                         ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1002:6
     |
1002 | ) -> Result<String, PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1070:6
     |
1070 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1102:6
     |
1102 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1165:6
     |
1165 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1250:6
     |
1250 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1295:6
     |
1295 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1311:6
     |
1311 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1482:6
     |
1482 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1507:6
     |
1507 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1560:6
     |
1560 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1582:6
     |
1582 | ) -> Result<(), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1602:45
     |
1602 | fn validate_key(key: &str, index: usize) -> Result<(), PropsError> {
     |                                             ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1631:6
     |
1631 | ) -> Result<(usize, &'a PropertyEntry), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1651:6
     |
1651 | ) -> Result<(usize, &'a PropertyEntry), PropsError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:209:45
    |
209 | pub(crate) fn parse_envelope(text: &str) -> Result<Envelope, PropsError> {
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:292:47
    |
292 | fn parse_op(raw: &JsonValue, index: usize) -> Result<Op, PropsError> {
    |                                               ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:327:6
    |
327 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:358:6
    |
358 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:381:6
    |
381 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:391:6
    |
391 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:401:6
    |
401 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:411:6
    |
411 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:430:6
    |
430 | ) -> Result<Op, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:468:6
    |
468 | ) -> Result<Option<Framing>, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:512:6
    |
512 | ) -> Result<Option<PropertyKind>, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:533:6
    |
533 | ) -> Result<String, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:541:6
    |
541 | ) -> Result<String, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:569:6
    |
569 | ) -> Result<Option<Position>, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:589:6
    |
589 | ) -> Result<Position, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:603:6
    |
603 | ) -> Result<String, PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/props/protocol.rs:625:6
    |
625 | ) -> Result<(), PropsError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
    |
    = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/cli.rs:736:45
    |
736 |         write_staged_files_guarded(&staged, || deps.validate(&vault))
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/records/cli.rs:980:45
    |
980 |         write_staged_files_guarded(&staged, || deps.validate(&vault))
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/records/cli.rs:1402:45
     |
1402 |         write_staged_files_guarded(&staged, || deps.validate(vault))
     |                                             ^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: `to_string` applied to a type that implements `Display` in `print!` args
    --> src/native/records/cli.rs:2556:64
     |
2556 |               .header(&format!("a/{path}"), &format!("b/{path}"))
     |  ________________________________________________________________^
2557 | |             .to_string()
     | |________________________^ help: remove this
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: large size difference between variants
    --> src/native/records/cli.rs:2954:1
     |
2954 | / enum Collection {
2955 | |     Usable(ResolvedRecordKind),
     | |     -------------------------- the second-largest variant contains at least 344 bytes
2956 | |     InvalidAlbum(AlbumEntry),
     | |     ------------------------ the largest variant contains at least 1232 bytes
2957 | | }
     | |_^ the entire enum is at least 1232 bytes
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
     |
2956 -     InvalidAlbum(AlbumEntry),
2956 +     InvalidAlbum(Box<AlbumEntry>),
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
   --> src/native/records/render.rs:381:25
    |
381 |         if index < 4 || (index >= 5 && index < 7) || (index >= 8 && index < 10)
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `(5..7).contains(&index)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains

warning: manual `Range::contains` implementation
   --> src/native/records/render.rs:381:54
    |
381 |         if index < 4 || (index >= 5 && index < 7) || (index >= 8 && index < 10)
    |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `(8..10).contains(&index)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains

warning: stripping a suffix manually
   --> src/native/records/render.rs:422:18
    |
422 |                 (raw[..raw.len() - 2].to_owned(), "\r\n".to_owned())
    |                  ^^^^^^^^^^^^^^^^^^^^
    |
note: the suffix was tested here
   --> src/native/records/render.rs:421:37
    |
421 |             let (content, ending) = if raw.ends_with("\r\n") {
    |                                     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_suffix` method
    |
421 ~             let (content, ending) = if let Some(<stripped>) = raw.strip_suffix("\r\n") {
422 ~                 (<stripped>.to_owned(), "\r\n".to_owned())
    |

warning: the variable `offset` is used as a loop counter
    --> src/native/records/render.rs:1549:9
     |
1549 |         for line in block {
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
   --> src/native/ref_jobs/worker.rs:456:5
    |
456 | /     fn record_done(
457 | |         &self,
458 | |         job: &JobFile,
459 | |         outcome: DoneOutcome,
...   |
464 | |         fallback_target: Option<String>,
465 | |     ) {
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

warning: this `if` has identical blocks
   --> src/native/tick/run.rs:584:25
    |
584 |           if !consecutive {
    |  _________________________^
585 | |             entry.waiting_since = row.started_at.or(Some(finished));
586 | |         } else if entry.waiting_since.is_none() {
    | |_________^
    |
note: same as this
   --> src/native/tick/run.rs:586:49
    |
586 |           } else if entry.waiting_since.is_none() {
    |  _________________________________________________^
587 | |             entry.waiting_since = row.started_at.or(Some(finished));
588 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

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
   --> src/native/task_complete/successors.rs:924:1
    |
924 | / fn effective_relation_state_map(
925 | |     verdicts: &[DependentVerdict],
926 | |     files: &[FileScan],
927 | |     states: &BTreeMap<
...   |
936 | |     source_paths: &BTreeSet<&Path>,
937 | | ) -> BTreeMap<String, SourceRecovery> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1194:1
     |
1194 | / fn relation_offer_placement(
1195 | |     group: &RelationOfferGroup,
1196 | |     completed: &[CompletedTask],
1197 | |     baseline_day: &DayView,
...    |
1202 | |     implicit: Option<&ImplicitDest>,
1203 | | ) -> Option<RelationOfferPlacement> {
     | |___________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2606:1
     |
2606 | / fn attach_offer(
2607 | |     verdict: &mut DependentVerdict,
2608 | |     files: &[FileScan],
2609 | |     day: &DayView,
...    |
2614 | |     project: Option<PathBuf>,
2615 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:2707:1
     |
2707 | / fn apply_project_member_classes(
2708 | |     verdicts: &mut Vec<DependentVerdict>,
2709 | |     folds: &mut Vec<ProjectFold>,
2710 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
2719 | |     _note_settings: &NoteTaskSettings,
2720 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
    --> src/native/task_complete/successors.rs:3419:1
     |
3419 | / fn apply_verdicts(
3420 | |     input: SuccessorInput,
3421 | |     files: Vec<FileScan>,
3422 | |     verdicts: Vec<DependentVerdict>,
...    |
3432 | |     relation_target_reads: usize,
3433 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/payload.rs:469:6
    |
469 | ) -> Result<(Vec<LineRange>, Vec<(String, String)>, usize), MergeError> {
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
   --> src/native/task_move/plan.rs:363:22
    |
363 |           let parent = tasks
    |  ______________________^
364 | |             .iter()
365 | |             .filter(|candidate| {
366 | |                 candidate.line_index < task.line_index
...   |
369 | |             })
370 | |             .last();
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
370 -             .last();
370 +             .next_back();
    |

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_move/transplant.rs:126:6
    |
126 |   ) -> Result<
    |  ______^
127 | |     (Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>),
128 | |     RenameError,
129 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the loop variable `index` is only used to index `nodes`
   --> src/native/task_reqs.rs:588:18
    |
588 |     for index in 0..nodes.len() {
    |                  ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
588 -     for index in 0..nodes.len() {
588 +     for <item> in &mut nodes {
    |

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_split/plan.rs:288:28
    |
288 |     let mut planned_moves: Vec<Option<(usize, Vec<(usize, usize)>)>> =
    |                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the loop variable `row` is only used to index `transformed_source`
   --> src/native/task_split/plan.rs:323:20
    |
323 |         for row in candidate.line + 1..=candidate.end {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
323 -         for row in candidate.line + 1..=candidate.end {
323 +         for <item> in transformed_source.iter_mut().take(candidate.end + 1).skip(candidate.line + 1) {
    |

warning: this `if` has identical blocks
    --> src/native/task_split/plan.rs:1306:55
     |
1306 |               if snapshot.notes.contains_key(&with_ext) {
     |  _______________________________________________________^
1307 | |                 Ok(with_ext)
1308 | |             } else {
     | |_____________^
     |
note: same as this
    --> src/native/task_split/plan.rs:1308:20
     |
1308 |               } else {
     |  ____________________^
1309 | |                 Ok(with_ext)
1310 | |             }
     | |_____________^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

warning: the loop variable `index` is used to index `lines`
    --> src/native/task_split/plan.rs:1495:18
     |
1495 |     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
     |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1495 -     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
1495 +     for (index, <item>) in lines.iter().enumerate().take(limit.min(lines.len().saturating_sub(1)) + 1).skip(start + 1) {
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
   --> src/native/periods/scaffold.rs:158:17
    |
158 |       let parts = vec![
    |  _________________^
159 | |         frontmatter_week(id),
160 | |         format!("# {title}"),
161 | |         week_nav(id),
...   |
166 | |         instructions::render(id),
167 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
    = note: `#[warn(clippy::useless_vec)]` on by default
help: you can use an array directly
    |
158 ~     let parts = [frontmatter_week(id),
159 +         format!("# {title}"),
160 +         week_nav(id),
161 +         week_day_links(id),
162 +         "```bob-stats-strip\n\n```".to_string(),
163 +         format!("## Days\n\n```bob-period-parts\n\n```"),
164 +         "## Review".to_string(),
165 ~         instructions::render(id)];
    |

warning: useless use of `vec!`
   --> src/native/periods/scaffold.rs:173:17
    |
173 |       let parts = vec![
    |  _________________^
174 | |         frontmatter_quarter(id),
175 | |         format!("# {title}"),
176 | |         quarter_nav(id),
...   |
181 | |         instructions::render(id),
182 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
help: you can use an array directly
    |
173 ~     let parts = [frontmatter_quarter(id),
174 +         format!("# {title}"),
175 +         quarter_nav(id),
176 +         quarter_child_links(id),
177 +         "```bob-stats-strip\n\n```".to_string(),
178 +         format!("## Weeks\n\n```bob-period-parts\n\n```"),
179 +         "## Review".to_string(),
180 ~         instructions::render(id)];
    |

warning: useless use of `vec!`
   --> src/native/periods/scaffold.rs:188:17
    |
188 |       let parts = vec![
    |  _________________^
189 | |         frontmatter_year(id),
190 | |         format!("# {title}"),
191 | |         year_nav(id),
...   |
196 | |         instructions::render(id),
197 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
help: you can use an array directly
    |
188 ~     let parts = [frontmatter_year(id),
189 +         format!("# {title}"),
190 +         year_nav(id),
191 +         year_child_links(id),
192 +         "```bob-stats-strip\n\n```".to_string(),
193 +         format!("## Quarters\n\n```bob-period-parts\n\n```"),
194 +         "## Review".to_string(),
195 ~         instructions::render(id)];
    |

warning: useless use of `vec!`
   --> src/native/periods/scaffold.rs:202:17
    |
202 |       let parts = vec![
    |  _________________^
203 | |         frontmatter_all_time(),
204 | |         "# All time".to_string(),
205 | |         "[[org|↑ org]]".to_string(),
...   |
209 | |         instructions::render(PeriodId::AllTime),
210 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
help: you can use an array directly
    |
202 ~     let parts = [frontmatter_all_time(),
203 +         "# All time".to_string(),
204 ~         "[[org|↑ org]]".to_string(),
205 +         "```bob-stats-strip\n\n```".to_string(),
206 +         "## Years\n\n```bob-period-parts\n\n```".to_string(),
207 +         "## Notes".to_string(),
208 ~         instructions::render(PeriodId::AllTime)];
    |

warning: `bob-obsidian` (lib) generated 846 warnings
error: could not compile `bob-obsidian` (lib) due to 7 previous errors; 846 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/sync.rs:988:13
    |
988 |             || txn.deps.validate(&vault),
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/albums/update/ops.rs:179:6
    |
179 | ) -> Result<OpOutcome, OpError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 168 bytes
    |
    = help: try reducing the size of `native::albums::update::ops::OpError`, for example by boxing large elements or replacing it with `Box<native::albums::update::ops::OpError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/write.rs:357:57
    |
357 |         let error = write_staged_files_guarded(&staged, || deps.validate(root))
    |                                                         ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/write.rs:443:57
    |
443 |         let error = write_staged_files_guarded(&staged, || deps.validate(root))
    |                                                         ^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/albums/write.rs:539:53
    |
539 |         let error = write_staged_files_guarded(&[], || deps.validate(root))
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
    --> src/native/bank/tests.rs:1465:9
     |
1465 |         || Ok(()),
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
    --> src/native/capture/note_pull.rs:1656:39
     |
1656 |     fn plan(harness: &mut Harness) -> Result<PlannedCaptureItem, CaptureError> {
     |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3311:10
     |
3311 |     ) -> Result<PlannedCaptureItem, CaptureError> {
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
    --> src/native/capture_language/close_log.rs:1384:9
     |
1384 | /         match lex_bullets(close, draft).expect("valid bullets") {
1385 | |             CloseLogLexed { entries, dangling } => {
1386 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1387 | |                 entries
...    |
1392 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `#[warn(clippy::match_single_binding)]` on by default
help: consider using a `let` statement
     |
1384 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1385 +         {
1386 +             assert!(dangling.is_empty(), "unexpected dangling");
1387 +             entries
1388 +                 .into_iter()
1389 +                 .map(|entry| (entry.index, entry.text, entry.details))
1390 +                 .collect()
1391 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1490:9
     |
1490 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1491 | |             CloseLogLexed { entries, dangling } => {
1492 | |                 assert!(entries.is_empty());
1493 | |                 assert_eq!(dangling.len(), 1);
...    |
1496 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1490 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1491 +         {
1492 +             assert!(entries.is_empty());
1493 +             assert_eq!(dangling.len(), 1);
1494 +             assert_eq!(dangling[0].index, Some(1));
1495 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1565:9
     |
1565 | /         match lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing")
1566 | |         {
1567 | |             error => assert!(
1568 | |                 error.message.contains("- 1 wired"),
...    |
1571 | |             ),
1572 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1565 ~         let error = lex_bullets("x1~2", "x1~2\n- 1 ok\n- wired").expect_err("missing");
1566 +         assert!(
1567 +             error.message.contains("- 1 wired"),
1568 +             "{}",
1569 +             error.message
1570 +         )
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2062:9
     |
2062 | /         match lex_bullets("x", "x\n- *").expect("dangling star") {
2063 | |             CloseLogLexed { entries, dangling } => {
2064 | |                 assert!(entries.is_empty());
2065 | |                 assert_eq!(dangling.len(), 1);
...    |
2068 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2062 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *").expect("dangling star");
2063 +         {
2064 +             assert!(entries.is_empty());
2065 +             assert_eq!(dangling.len(), 1);
2066 +             assert_eq!(dangling[0].index, None);
2067 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2069:9
     |
2069 | /         match lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details")
2070 | |         {
2071 | |             CloseLogLexed { entries, dangling } => {
2072 | |                 assert!(entries.is_empty());
...    |
2076 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2069 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details");
2070 +         {
2071 +             assert!(entries.is_empty());
2072 +             assert_eq!(dangling.len(), 1);
2073 +             assert_eq!(dangling[0].index, None);
2074 +         }
     |

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:4913:5
     |
4913 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:4912:5
     |
4912 |     let mut seen = SeenMarkers::default();
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
    --> src/native/capture_parse.rs:4895:13
     |
4895 |             "Blaze @eat"[..start].to_string(),
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use this: `&"Blaze @eat"[..start]`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#to_string_in_format_args

warning: `to_string` applied to a type that implements `Display` in `format!` args
    --> src/native/capture_parse.rs:4897:13
     |
4897 |             "Blaze @eat"[end..].to_string(),
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
    --> src/native/gmail/sync/report.rs:1563:46
     |
1563 |         let first = ArchiveRow::from_reviews(&[review.clone()], &empty);
     |                                              ^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&review)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2115:9
     |
2115 |         outcome.failed = true;
     |         ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { failed: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2114:9
     |
2114 |         let mut outcome = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2137:9
     |
2137 |         outcome.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, watch_snapshot: WatchScan::default(), ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2136:9
     |
2136 |         let mut outcome = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2218:9
     |
2218 |         outcome.failed = true;
     |         ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { failed: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2217:9
     |
2217 |         let mut outcome = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2303:9
     |
2303 |         live.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2302:9
     |
2302 |         let mut live = FilingOutcome::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/gmail/sync/report.rs:2306:9
     |
2306 |         dry.applied = true;
     |         ^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::gmail::sync::file::FilingOutcome { applied: true, ..Default::default() }` and removing relevant reassignments
    --> src/native/gmail/sync/report.rs:2305:9
     |
2305 |         let mut dry = FilingOutcome::default();
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
   --> src/native/ob.rs:544:58
    |
544 |             commit_paths(&vault, &env, "bracket change", &[bracketed.clone()])
    |                                                          ^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&bracketed)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: unnecessary use of `get(&path).is_none()`
   --> src/native/periods/brief.rs:263:28
    |
263 |                 if buffers.get(&path).is_none() {
    |                    --------^^^^^^^^^^^^^^^^^^^^
    |                    |
    |                    help: replace it with: `!buffers.contains_key(&path)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:383:9
    |
383 |         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
383 -         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
383 +         sorted.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/pomodoro.rs:1010:51
     |
1010 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
     |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: the `Err`-variant returned from this function is very large
  --> src/native/props/contract/tests.rs:77:6
   |
77 | ) -> Result<PlanOutcome, PropsError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
   |
   = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/props/plan.rs:1753:10
     |
1753 |     ) -> Result<PlanOutcome, PropsError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 128 bytes
     |
     = help: try reducing the size of `native::props::PropsError`, for example by boxing large elements or replacing it with `Box<native::props::PropsError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1756:51
     |
1756 |         assert_eq!(companions.source_ranges, Some(vec![20..35]));
     |                                                   ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1756 -         assert_eq!(companions.source_ranges, Some(vec![20..35]));
1756 +         assert_eq!(companions.source_ranges, Some((20..35).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 35, try
     |
1756 -         assert_eq!(companions.source_ranges, Some(vec![20..35]));
1756 +         assert_eq!(companions.source_ranges, Some(vec![20; 35]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1794:61
     |
1794 |         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
     |                                                             ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1794 -         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
1794 +         assert_eq!(result.properties[3].source_ranges, Some((40..43).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 43, try
     |
1794 -         assert_eq!(result.properties[3].source_ranges, Some(vec![40..43]));
1794 +         assert_eq!(result.properties[3].source_ranges, Some(vec![40; 43]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1855:58
     |
1855 |         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
     |                                                          ^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1855 -         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
1855 +         assert_eq!(result.invalid[0].source_ranges, Some((12..20).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 20, try
     |
1855 -         assert_eq!(result.invalid[0].source_ranges, Some(vec![12..20]));
1855 +         assert_eq!(result.invalid[0].source_ranges, Some(vec![12; 20]));
     |

warning: a `Vec` of `Range` that is only one element
    --> src/native/records/plan.rs:1856:61
     |
1856 |         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
     |                                                             ^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
help: if you wanted a `Vec` that contains the entire range, try
     |
1856 -         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
1856 +         assert_eq!(result.properties[2].source_ranges, Some((3..11).collect::<std::vec::Vec<usize>>()));
     |
help: if you wanted a `Vec` of len 11, try
     |
1856 -         assert_eq!(result.properties[2].source_ranges, Some(vec![3..11]));
1856 +         assert_eq!(result.properties[2].source_ranges, Some(vec![3; 11]));
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
    --> src/native/records/render.rs:3450:26
     |
3450 |         let empty = front.clone();
     |                          ^^^^^^^^ help: remove this redundant call
     |
     = note: the type `str` does not implement `Clone`, so calling `clone` on `&str` copies the reference, which does not do anything and can be removed
     = note: `#[warn(noop_method_call)]` on by default

warning: `bob-obsidian` (lib test) generated 943 warnings (842 duplicates)
error: could not compile `bob-obsidian` (lib test) due to 6 previous errors; 943 warnings emitted
error: Recipe `check` failed on line 83 with exit code 101
failed  exit=101  duration=320186ms
verdict: undetermined; exit 101

