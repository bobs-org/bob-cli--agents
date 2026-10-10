# Chat History - ace-run (65--mon)

- **TIMESTAMP:** 2026-10-10 06:49:05 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 65--mon

## Prompt

sase monitor start --command 'just check' --reason 'Run the final Rust verification before completing the approved freshness refactor'

## Response

sase tool run c169900537b8b6ba3814a089a468eced

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
cargo clippy --all-targets --all-features
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
    Checking typenum v1.20.1
   Compiling version_check v0.9.5
    Checking stable_deref_trait v1.2.1
    Checking cfg-if v1.0.4
   Compiling find-msvc-tools v0.1.9
   Compiling shlex v2.0.1
    Checking foldhash v0.2.0
    Checking memchr v2.8.1
    Checking allocator-api2 v0.2.21
    Checking equivalent v1.0.2
   Compiling libc v0.2.186
    Checking litemap v0.8.3
    Checking writeable v0.6.4
    Checking utf8_iter v1.0.4
   Compiling icu_properties_data v2.3.0
   Compiling serde_core v1.0.228
   Compiling icu_normalizer_data v2.3.0
    Checking rand_core v0.10.1
   Compiling cc v1.2.63
   Compiling getrandom v0.4.2
    Checking smallvec v1.15.2
    Checking utf8parse v0.2.2
    Checking is_terminal_polyfill v1.70.2
    Checking colorchoice v1.0.5
   Compiling crc32fast v1.5.0
    Checking anstyle-parse v1.0.0
   Compiling generic-array v0.14.7
    Checking bitflags v2.12.1
    Checking anstyle-query v1.1.5
   Compiling autocfg v1.5.1
    Checking tinyvec_macros v0.1.1
    Checking cpufeatures v0.3.0
   Compiling serde v1.0.228
    Checking anstyle v1.0.14
    Checking tinyvec v1.11.0
    Checking strsim v0.11.1
   Compiling thiserror v2.0.18
    Checking clap_lex v1.1.0
    Checking hashbrown v0.17.1
   Compiling zmij v1.0.21
    Checking adler2 v2.0.1
    Checking itoa v1.0.18
    Checking cpufeatures v0.2.17
    Checking simd-adler32 v0.3.9
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking anstream v1.0.0
    Checking chacha20 v0.10.0
    Checking miniz_oxide v0.8.9
    Checking regex-syntax v0.8.10
   Compiling num-traits v0.2.19
    Checking unicode-bidi v0.3.18
    Checking const-oid v0.10.2
    Checking unicode-normalization v0.1.25
    Checking clap_builder v4.6.7
    Checking unicode-properties v0.1.4
    Checking percent-encoding v2.3.2
    Checking hybrid-array v0.4.12
   Compiling serde_json v1.0.150
    Checking bytecount v0.6.9
    Checking flate2 v1.1.9
    Checking indexmap v2.14.0
   Compiling syn v3.0.6
   Compiling syn v2.0.117
    Checking stringprep v0.1.5
    Checking form_urlencoded v1.2.2
    Checking encoding_rs v0.8.35
    Checking weezl v0.1.12
    Checking rand v0.10.1
    Checking ryu v1.0.23
    Checking iana-time-zone v0.1.65
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking block-buffer v0.12.0
    Checking inout v0.1.4
    Checking crypto-common v0.2.2
    Checking is_executable v1.0.6
    Checking unsafe-libyaml v0.2.11
    Checking digest v0.10.7
    Checking log v0.4.30
   Compiling rquickjs-sys v0.12.1
    Checking rangemap v1.7.1
    Checking cipher v0.4.4
    Checking ttf-parser v0.25.1
    Checking sha2 v0.10.9
    Checking md-5 v0.10.6
    Checking chrono v0.4.44
    Checking fs2 v0.4.3
    Checking hex v0.4.3
    Checking similar v2.7.0
    Checking cbc v0.1.2
    Checking ecb v0.1.2
    Checking aes v0.8.4
   Compiling vcpkg v0.2.15
   Compiling pkg-config v0.3.33
    Checking clap v4.6.7
    Checking regex-automata v0.4.14
   Compiling rustix v1.1.5
    Checking digest v0.11.3
    Checking clap_complete v4.6.11
    Checking num-conv v0.2.2
    Checking deranged v0.5.8
    Checking sha2 v0.11.0
    Checking linux-raw-sys v0.12.1
    Checking powerfmt v0.2.0
    Checking time-core v0.1.9
    Checking hashlink v0.12.1
    Checking quick-xml v0.41.0
    Checking base64 v0.22.1
    Checking fallible-streaming-iterator v0.1.9
    Checking fallible-iterator v0.3.0
   Compiling libsqlite3-sys v0.38.1
    Checking once_cell v1.21.4
    Checking fastrand v2.5.0
    Checking nom_locate v5.0.0
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
    Checking time v0.3.53
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
    Checking regex v1.12.3
    Checking lopdf v0.40.0
    Checking tempfile v3.27.0
    Checking zerofrom v0.1.8
    Checking yoke v0.8.3
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking icu_collections v2.3.0
    Checking icu_locale_core v2.3.0
    Checking serde_yaml v0.9.34+deprecated
    Checking plist v1.10.0
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking rusqlite v0.40.1
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:297:12
    |
297 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:120:20
    |
120 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

warning: unused import: `RegionTask`
   --> src/native/highlights_ref/mod.rs:156:39
    |
156 |     split_note_body, RegionBlockKind, RegionTask,
    |                                       ^^^^^^^^^^
    |
    = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default

warning: unused import: `TrackerHit`
  --> src/native/ref_library/mod.rs:52:40
   |
52 | pub(crate) use status::{decide_status, TrackerHit};
   |                                        ^^^^^^^^^^

warning: unused import: `EditedReadingTask`
  --> src/native/ref_tasks/mod.rs:22:55
   |
22 |     edit_reading_task_checkbox, locate_original_line, EditedReadingTask,
   |                                                       ^^^^^^^^^^^^^^^^^

warning: unused import: `ManagedEmbed`
  --> src/native/ref_tasks/mod.rs:25:44
   |
25 | pub(crate) use embed::{find_managed_embed, ManagedEmbed};
   |                                            ^^^^^^^^^^^^

warning: unused import: `InsertedRefTask`
  --> src/native/ref_tasks/mod.rs:27:57
   |
27 |     insert_ref_task, insert_ref_task_with_preferred_id, InsertedRefTask,
   |                                                         ^^^^^^^^^^^^^^^

warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, `RefFollowUp`, and `stamp_close_date_any_id`
  --> src/native/ref_tasks/mod.rs:32:5
   |
32 |     stamp_close_date_any_id, strip_blockquote_prefix, task_mark, OrphanRefTask,
   |     ^^^^^^^^^^^^^^^^^^^^^^^                                      ^^^^^^^^^^^^^
33 |     RefFollowUp, REF_BLOCK_ID_MAX_LEN,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^

warning: unused import: `managed_region_line_range`
  --> src/native/ref_tasks/mod.rs:40:20
   |
40 |     find_trackers, managed_region_line_range, parse_tracker_line, TrackerHit,
   |                    ^^^^^^^^^^^^^^^^^^^^^^^^^

warning: unused imports: `find_trackers`, `managed_region_line_range`, and `parse_tracker_line`
   --> src/native/ref_library/status.rs:308:5
    |
308 |     find_trackers, managed_region_line_range, parse_tracker_line,
    |     ^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^

warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, and `RefFollowUp`
  --> src/native/ref_tasks/mod.rs:32:66
   |
32 |     stamp_close_date_any_id, strip_blockquote_prefix, task_mark, OrphanRefTask,
   |                                                                  ^^^^^^^^^^^^^
33 |     RefFollowUp, REF_BLOCK_ID_MAX_LEN,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^

warning: type `native::ref_library::find::FindSummary` is more private than the item `native::ref_library::output::print_find_json`
  --> src/native/ref_library/output.rs:61:1
   |
61 | / pub(crate) fn print_find_json(
62 | |     coverage: &Coverage,
63 | |     library: &LibraryCounts,
64 | |     summary: &FindSummary,
65 | |     results: &[FindResult],
66 | | ) {
   | |_^ function `native::ref_library::output::print_find_json` is reachable at visibility `pub(crate)`
   |
note: but type `native::ref_library::find::FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
  --> src/native/ref_library/find.rs:70:1
   |
70 | pub(super) struct FindSummary {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   = note: `#[warn(private_interfaces)]` on by default

warning: type `native::ref_library::find::FindResult` is more private than the item `native::ref_library::output::print_find_json`
  --> src/native/ref_library/output.rs:61:1
   |
61 | / pub(crate) fn print_find_json(
62 | |     coverage: &Coverage,
63 | |     library: &LibraryCounts,
64 | |     summary: &FindSummary,
65 | |     results: &[FindResult],
66 | | ) {
   | |_^ function `native::ref_library::output::print_find_json` is reachable at visibility `pub(crate)`
   |
note: but type `native::ref_library::find::FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
  --> src/native/ref_library/find.rs:57:1
   |
57 | pub(super) struct FindResult {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `native::ref_library::find::FindSummary` is more private than the item `native::ref_library::output::render_find_human`
   --> src/native/ref_library/output.rs:250:1
    |
250 | / pub(crate) fn render_find_human(
251 | |     coverage: &Coverage,
252 | |     summary: &FindSummary,
253 | |     results: &[FindResult],
...   |
256 | |     width: usize,
257 | | ) -> String {
    | |___________^ function `native::ref_library::output::render_find_human` is reachable at visibility `pub(crate)`
    |
note: but type `native::ref_library::find::FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:70:1
    |
 70 | pub(super) struct FindSummary {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `native::ref_library::find::FindResult` is more private than the item `native::ref_library::output::render_find_human`
   --> src/native/ref_library/output.rs:250:1
    |
250 | / pub(crate) fn render_find_human(
251 | |     coverage: &Coverage,
252 | |     summary: &FindSummary,
253 | |     results: &[FindResult],
...   |
256 | |     width: usize,
257 | | ) -> String {
    | |___________^ function `native::ref_library::output::render_find_human` is reachable at visibility `pub(crate)`
    |
note: but type `native::ref_library::find::FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:57:1
    |
 57 | pub(super) struct FindResult {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `native::ref_library::find::FindSummary` is more private than the item `native::ref_library::output::render_find_markdown`
   --> src/native/ref_library/output.rs:492:1
    |
492 | / pub(crate) fn render_find_markdown(
493 | |     summary: &FindSummary,
494 | |     results: &[FindResult],
495 | | ) -> String {
    | |___________^ function `native::ref_library::output::render_find_markdown` is reachable at visibility `pub(crate)`
    |
note: but type `native::ref_library::find::FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:70:1
    |
 70 | pub(super) struct FindSummary {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `native::ref_library::find::FindResult` is more private than the item `native::ref_library::output::render_find_markdown`
   --> src/native/ref_library/output.rs:492:1
    |
492 | / pub(crate) fn render_find_markdown(
493 | |     summary: &FindSummary,
494 | |     results: &[FindResult],
495 | | ) -> String {
    | |___________^ function `native::ref_library::output::render_find_markdown` is reachable at visibility `pub(crate)`
    |
note: but type `native::ref_library::find::FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:57:1
    |
 57 | pub(super) struct FindResult {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: method `ref_parent` is never used
   --> src/native/gkeep/ledger.rs:366:19
    |
249 | impl Journal {
    | ------------ method in this implementation
...
366 |     pub(super) fn ref_parent(&self, id: &str, fp: &str) -> Option<String> {
    |                   ^^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: field `refreshed` is never read
    --> src/native/highlights_ref/sync.rs:1705:5
     |
1703 | struct V2ReadingOutcome {
     |        ---------------- field in this struct
1704 |     execution: Option<ReadingTaskExecution>,
1705 |     refreshed: Option<ref_tasks_mod::LocatedRefTask>,
     |     ^^^^^^^^^

warning: fields `tracker_start` and `tracker_end` are never read
  --> src/native/ref_library/migrate_tasks/plan.rs:58:9
   |
44 | pub(crate) struct PlannedTask {
   |                   ----------- fields in this struct
...
58 |     pub tracker_start: usize,
   |         ^^^^^^^^^^^^^
59 |     pub tracker_end: usize,
   |         ^^^^^^^^^^^
   |
   = note: `PlannedTask` has derived impls for the traits `Clone` and `Debug`, but these are intentionally ignored during dead code analysis

warning: field `stem` is never read
  --> src/native/ref_library/migrate_tasks/plan.rs:70:9
   |
68 | pub(crate) struct UnmappedRow {
   |                   ----------- field in this struct
69 |     pub ref_note: String,
70 |     pub stem: String,
   |         ^^^^
   |
   = note: `UnmappedRow` has derived impls for the traits `Clone` and `Debug`, but these are intentionally ignored during dead code analysis

warning: method `is_empty` is never used
   --> src/native/ref_library/migrate_tasks/plan.rs:129:19
    |
128 | impl MigrationPlan {
    | ------------------ method in this implementation
129 |     pub(crate) fn is_empty(&self) -> bool {
    |                   ^^^^^^^^

warning: variant `V1` is never constructed
  --> src/native/ref_tasks/select.rs:34:5
   |
32 | pub(crate) enum Selected {
   |                 -------- variant in this enum
33 |     V2(LocatedRefTask),
34 |     V1(TrackerHit),
   |     ^^
   |
   = note: `Selected` has derived impls for the traits `Clone` and `Debug`, but these are intentionally ignored during dead code analysis

warning: field `warnings` is never read
  --> src/native/ref_tasks/walk.rs:40:5
   |
36 | pub(crate) struct RefTaskIndex {
   |                   ------------ field in this struct
...
40 |     warnings: Vec<String>,
   |     ^^^^^^^^
   |
   = note: `RefTaskIndex` has derived impls for the traits `Clone` and `Debug`, but these are intentionally ignored during dead code analysis

warning: method `warnings` is never used
   --> src/native/ref_tasks/walk.rs:501:19
    |
 50 | impl RefTaskIndex {
    | ----------------- method in this implementation
...
501 |     pub(crate) fn warnings(&self) -> &[String] {
    |                   ^^^^^^^^

warning: struct `RecoveredDependent` is never constructed
  --> src/native/task_complete/recovery.rs:25:19
   |
25 | pub(crate) struct RecoveredDependent {
   |                   ^^^^^^^^^^^^^^^^^^

warning: struct `DependentRecovery` is never constructed
  --> src/native/task_complete/recovery.rs:37:19
   |
37 | pub(crate) struct DependentRecovery {
   |                   ^^^^^^^^^^^^^^^^^

warning: function `recover_blocked_dependents` is never used
  --> src/native/task_complete/recovery.rs:51:15
   |
51 | pub(crate) fn recover_blocked_dependents<I>(
   |               ^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: function `line_start_offset` is never used
   --> src/native/task_complete/recovery.rs:137:4
    |
137 | fn line_start_offset(contents: &str, line_index: usize) -> usize {
    |    ^^^^^^^^^^^^^^^^^

warning: this function has too many arguments (8/7)
   --> src/native/capture/dependencies.rs:861:1
    |
861 | / fn resolve_prerequisites(
862 | |     ctx: &DependencyContext,
863 | |     planner: &mut CaptureBatchPlanner,
864 | |     bob_dir: &Path,
...   |
869 | |     dependent_desc: &str,
870 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
    | |_______________________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1079:24
     |
1079 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
     = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1590:6
     |
1590 |   ) -> Result<
     |  ______^
1591 | |     (
1592 | |         Vec<MergedMember>,
1593 | |         BTreeSet<(String, String)>,
...    |
1597 | |     CaptureError,
1598 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this `if` statement can be collapsed
   --> src/native/capture/output.rs:922:5
    |
922 | /     if result.kind == "pomodoro_start" {
923 | |         if let Some(start) = result.pomodoro_start.as_ref() {
924 | |             print_human_pomodoro_start_success(
925 | |                 result,
...   |
934 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
    = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
    |
922 ~     if result.kind == "pomodoro_start"
923 ~         && let Some(start) = result.pomodoro_start.as_ref() {
924 |             print_human_pomodoro_start_success(
...
932 |             return;
933 ~         }
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture/plan.rs:417:1
    |
417 | / pub(super) fn plan_capture_item(
418 | |     request: &CaptureRequest,
419 | |     parsed_item: ParsedCaptureItem,
420 | |     now: chrono::NaiveDateTime,
...   |
426 | |     dependency_ctx: &mut DependencyContext,
427 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:633:9
    |
633 | /         let Some(relative_close) = line[open..].find(')') else {
634 | |             return None;
635 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: manual `rem_euclid` implementation
   --> src/native/capture/pomodoro_adjust.rs:988:5
    |
988 |     (((value % 1440) + 1440) % 1440) as u64
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `value.rem_euclid(1440)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_rem_euclid
    = note: `#[warn(clippy::manual_rem_euclid)]` on by default

warning: this function has too many arguments (8/7)
   --> src/native/capture/pomodoro_insert.rs:245:1
    |
245 | / pub(super) fn insert_named_pomodoro_child_block(
246 | |     contents: &str,
247 | |     block: &str,
248 | |     selector: &str,
...   |
253 | |     open: &[(usize, &str)],
254 | | ) -> Result<(String, Placement, usize, String), CaptureError> {
    | |_____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `map_or` can be simplified
   --> src/native/capture/pomodoro_start.rs:419:20
    |
419 |                 && anchor.map_or(true, |anchor| *index > anchor)
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_map_or
    = note: `#[warn(clippy::unnecessary_map_or)]` on by default
help: use `is_none_or` instead
    |
419 -                 && anchor.map_or(true, |anchor| *index > anchor)
419 +                 && anchor.is_none_or(|anchor| *index > anchor)
    |

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_active_tasks.rs:321:12
    |
321 |     tasks: &mut Vec<ActiveTask>,
    |            ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
    = note: `#[warn(clippy::ptr_arg)]` on by default
help: change this to
    |
321 -     tasks: &mut Vec<ActiveTask>,
321 +     tasks: &mut [ActiveTask],
    |

warning: redundant guard
   --> src/native/capture_language/close_log.rs:206:23
    |
206 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
    = note: `#[warn(clippy::redundant_guards)]` on by default
help: try
    |
206 -         Some(list) if list.is_empty() => {
206 +         Some([]) => {
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/close_log.rs:493:1
    |
493 | / fn check_index_loggable(
494 | |     index: u32,
495 | |     index_range: (usize, usize),
496 | |     close_token: &str,
...   |
502 | |     complete_all: bool,
503 | | ) -> Result<(), CloseLogError> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:662:1
    |
662 | / pub(crate) fn lex_close_inline_entry_with_all(
663 | |     entry_tokens: &[Token<'_>],
664 | |     close_token: &str,
665 | |     in_progress: Option<&[u32]>,
...   |
670 | |     complete_all: bool,
671 | | ) -> Result<CloseInlineLex, CloseLogError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:900:1
    |
900 | / pub(crate) fn lex_close_log_bullets_with_all(
901 | |     child_lines: &[ItemLine<'_>],
902 | |     close_token: &str,
903 | |     in_progress: Option<&[u32]>,
...   |
908 | |     complete_all: bool,
909 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: unnecessary map of the identity function
   --> src/native/capture_language/editor_classify.rs:612:60
    |
612 |               let (after_x, x_len) = classify_link_close(raw)
    |  ____________________________________________________________^
613 | |                 .map(|(selection, x_len)| (selection, x_len))
    | |_____________________________________________________________^ help: remove the call to `map`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity
    = note: `#[warn(clippy::map_identity)]` on by default

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:450:1
    |
450 | / pub(super) enum TokenParse {
451 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 352 bytes
452 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
453 | | }
    | |_^ the entire enum is at least 352 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
451 -     Marker(MarkerParse),
451 +     Marker(Box<MarkerParse>),
    |

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture_language/editor_parse.rs:941:9
    |
941 | /         let Some(route) = route_parsed.route else {
942 | |             return None;
943 | |         };
    | |__________^ help: replace it with: `let route = route_parsed.route?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:1675:17
     |
1675 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture_language/item.rs:171:9
    |
171 | /         let Some(route) = route_parsed.route else {
172 | |             return None;
173 | |         };
    | |__________^ help: replace it with: `let route = route_parsed.route?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1684:31
     |
1684 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
1684 -                 Err(error) => return Err(error.message),
1684 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1692:21
     |
1692 | /                     return Err(close_inline_dangling_error(
1693 | |                         &head, index, plain,
1694 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1692 ~                     Err(close_inline_dangling_error(
1693 +                         &head, index, plain,
1694 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1730:21
     |
1730 | /                     return Ok(Some(parsed_capture_item_outcome(
1731 | |                         item,
1732 | |                         ParsedCaptureText {
1733 | |                             body,
...    |
1744 | |                         None,
1745 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1730 ~                     Ok(Some(parsed_capture_item_outcome(
1731 +                         item,
1732 +                         ParsedCaptureText {
1733 +                             body,
1734 +                             clip: None,
1735 +                             route: None,
1736 +                             kind: CaptureKind::PomodoroClose { spec },
1737 +                             scheduled_offset: None,
1738 +                             priority_level: None,
1739 +                             sub_bullets: Vec::new(),
1740 +                             dependencies: Vec::new(),
1741 +                             dependency_target: None,
1742 +                         },
1743 +                         Vec::new(),
1744 +                         None,
1745 ~                     )))
     |

warning: redundant guard
   --> src/native/capture_language/tokens.rs:667:43
    |
667 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
    |
667 -                 Some((after_x, x_len)) if after_x.is_empty() => {
667 +                 Some(("", x_len)) => {
    |

warning: unnecessary map of the identity function
    --> src/native/capture_language/tokens.rs:1112:59
     |
1112 |       let (after_x, x_len) = classify_link_close(raw_suffix)
     |  ___________________________________________________________^
1113 | |         .map(|(selection, x_len)| (selection, x_len))
     | |_____________________________________________________^ help: remove the call to `map`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1489:13
     |
1489 | /             return Ok(Some(parsed_capture_item_outcome(
1490 | |                 item,
1491 | |                 ParsedCaptureText {
1492 | |                     body: String::new(),
...    |
1509 | |                 Some(marker_text),
1510 | |             )));
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1489 ~             Ok(Some(parsed_capture_item_outcome(
1490 +                 item,
1491 +                 ParsedCaptureText {
1492 +                     body: String::new(),
1493 +                     clip: None,
1494 +                     route: Some(route),
1495 +                     kind: CaptureKind::PomodoroLink {
1496 +                         block_id: parts.block_id,
1497 +                         pomodoro_name: parts.pomodoro_name,
1498 +                         start: parts.start,
1499 +                         close: parts.close,
1500 +                         spelling: PomodoroLinkSpelling::Caret,
1501 +                     },
1502 +                     scheduled_offset: None,
1503 +                     priority_level: None,
1504 +                     sub_bullets: Vec::new(),
1505 +                     dependencies: Vec::new(),
1506 +                     dependency_target: None,
1507 +                 },
1508 +                 Vec::new(),
1509 +                 Some(marker_text),
1510 ~             )))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1571:13
     |
1571 |             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1571 -             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
1571 +             Err(POMODORO_LINK_SHAPE_ERROR.to_string())
     |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:130:1
    |
130 | / pub(crate) enum PomodoroCloseOutcome {
131 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 528 bytes
132 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
133 | | }
    | |_^ the entire enum is at least 528 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
131 -     Close(PomodoroClosePlan),
131 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:237:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
237 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:284:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
284 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:472:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
472 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:489:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
489 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:509:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
509 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:532:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
532 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:595:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
595 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:668:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
668 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:822:10
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
822 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:899:6
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
899 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:923:6
    |
125 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
923 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1184:6
     |
 125 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1184 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the borrowed expression implements the required traits
   --> src/native/env.rs:301:13
    |
301 |             &dir.join(file_name),
    |             ^^^^^^^^^^^^^^^^^^^^ help: change this to: `dir.join(file_name)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/gkeep/plan.rs:293:9
    |
293 | /         let Some(route) = parse_trailing_route(route_token) else {
294 | |             return None;
295 | |         };
    | |__________^ help: replace it with: `let route = parse_trailing_route(route_token)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/gkeep/plan.rs:296:9
    |
296 | /         let Some(intent) = classify_token(url_token) else {
297 | |             return None;
298 | |         };
    | |__________^ help: replace it with: `let intent = classify_token(url_token)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:384:5
    |
384 | /     if let Some(name) = matches.get_one::<String>("name") {
385 | |         if let Err(error) = super::clip_url::validate_name(name) {
386 | |             let styler = Styler::detect();
387 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
390 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
384 ~     if let Some(name) = matches.get_one::<String>("name")
385 ~         && let Err(error) = super::clip_url::validate_name(name) {
386 |             let styler = Styler::detect();
387 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
388 |             return 1;
389 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:392:5
    |
392 | /     if let Some(ref_type) = &ref_type {
393 | |         if let Err(error) = validate_ref_type(ref_type) {
394 | |             let styler = Styler::detect();
395 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
398 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
392 ~     if let Some(ref_type) = &ref_type
393 ~         && let Err(error) = validate_ref_type(ref_type) {
394 |             let styler = Styler::detect();
395 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
396 |             return 1;
397 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:399:5
    |
399 | /     if let Some(published) = matches.get_one::<String>("published") {
400 | |         if let Err(error) = super::clip_url::validate_published(published) {
401 | |             let styler = Styler::detect();
402 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
405 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
399 ~     if let Some(published) = matches.get_one::<String>("published")
400 ~         && let Err(error) = super::clip_url::validate_published(published) {
401 |             let styler = Styler::detect();
402 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
403 |             return 1;
404 ~         }
    |

warning: this `match` expression can be replaced with `?`
    --> src/native/highlights_ref/create.rs:1017:17
     |
1017 | /                 match companion_mod::copy_audio_for_install(plan.audio.as_ref())
1018 | |                 {
1019 | |                     Ok(created) => created,
1020 | |                     Err(error) => return Err(error),
1021 | |                 }
     | |_________________^ help: try instead: `companion_mod::copy_audio_for_install(plan.audio.as_ref())?`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:1760:1
     |
1760 | / fn print_pdf_dry_run(
1761 | |     config: &Config,
1762 | |     styler: &Styler,
1763 | |     source_display: &str,
...    |
1771 | |     legacy: &[sources_mod::RecordedSource],
1772 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:161:17
    |
161 | /                 if title.is_none() {
162 | |                     title = value;
163 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
    = note: `#[warn(clippy::collapsible_match)]` on by default
help: collapse nested if block
    |
160 ~             "title"
161 ~                 if title.is_none() => {
162 |                     title = value;
163 ~                 }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:166:17
    |
166 | /                 if value.is_some_and(|value| !value.is_empty()) {
167 | |                     has_audio = true;
168 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
165 ~             "audio"
166 ~                 if value.is_some_and(|value| !value.is_empty()) => {
167 |                     has_audio = true;
168 ~                 }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:244:21
    |
244 | /                     if source_pdf.is_none() {
245 | |                         source_pdf = entry.value.as_ref().and_then(|value| {
246 | |                             value.as_string().map(str::to_string)
247 | |                         });
248 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
243 ~                 "source_pdf"
244 ~                     if source_pdf.is_none() => {
245 |                         source_pdf = entry.value.as_ref().and_then(|value| {
246 |                             value.as_string().map(str::to_string)
247 |                         });
248 ~                     }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:251:21
    |
251 | /                     if entry.value.as_ref().is_some_and(|value| {
252 | |                         value.as_string().is_some_and(|value| !value.is_empty())
253 | |                     }) {
254 | |                         has_audio = true;
255 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
250 ~                 "audio"
251 |                     if entry.value.as_ref().is_some_and(|value| {
252 |                         value.as_string().is_some_and(|value| !value.is_empty())
253 ~                     }) => {
254 |                         has_audio = true;
255 ~                     }
    |

warning: you should use the `starts_with` method
   --> src/native/highlights_ref/listen.rs:407:23
    |
407 |     if length == 0 || rest[length..].chars().next() != Some('}') {
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: like this: `!rest[length..].starts_with('}')`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#chars_next_cmp
    = note: `#[warn(clippy::chars_next_cmp)]` on by default

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/pdf_target.rs:123:1
    |
123 | / pub(super) fn plan_pdf_url(
124 | |     url: &WebUrl,
125 | |     downloaded: &Path,
126 | |     name_override: Option<&str>,
...   |
131 | |     progress: Option<&dyn Fn(&str)>,
132 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:154:34
    |
154 |                         url.host.replace('.', "_").replace('-', "_"),
    |                                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '-'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace
    = note: `#[warn(clippy::collapsible_str_replace)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:208:1
    |
208 | / pub(super) fn plan_arxiv(
209 | |     paper: &ArxivPaper,
210 | |     name_override: Option<&str>,
211 | |     title_override: Option<&str>,
...   |
217 | |     progress: Option<&dyn Fn(&str)>,
218 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:310:33
    |
310 |     format!("arxiv_{}", full_id.replace('.', "_").replace('/', "_"))
    |                                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '/'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:811:9
    |
811 | /         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line) {
812 | |             if crate::native::ref_tasks::is_open_mark(hit.mark) {
813 | |                 tracker_idx = Some(i);
814 | |                 break;
815 | |             }
816 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
811 ~         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line)
812 ~             && crate::native::ref_tasks::is_open_mark(hit.mark) {
813 |                 tracker_idx = Some(i);
814 |                 break;
815 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:890:5
    |
890 | /     if has_hash && has_base {
891 | |         if let Some(updated) = recompute_parent_free_hash(&front_lines) {
892 | |             front_lines = updated;
893 | |         }
894 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
890 ~     if has_hash && has_base
891 ~         && let Some(updated) = recompute_parent_free_hash(&front_lines) {
892 |             front_lines = updated;
893 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:903:9
    |
903 | /         if let Some((k, v)) = line.split_once(':') {
904 | |             if k.trim() == "highlights_marker_base" {
905 | |                 let mut v = v.trim().to_string();
906 | |                 if (v.starts_with('\'') && v.ends_with('\'') && v.len() >= 2)
...   |
915 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
903 ~         if let Some((k, v)) = line.split_once(':')
904 ~             && k.trim() == "highlights_marker_base" {
905 |                 let mut v = v.trim().to_string();
...
913 |                 base_json = Some(v);
914 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:928:9
    |
928 | /         if let Some((k, _)) = line.split_once(':') {
929 | |             if k.trim() == "highlights_marker_hash" {
930 | |                 // Preserve quoting style: single-quoted string.
931 | |                 out.push(format!("highlights_marker_hash: '{hash}'"));
...   |
934 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
928 ~         if let Some((k, _)) = line.split_once(':')
929 ~             && k.trim() == "highlights_marker_hash" {
930 |                 // Preserve quoting style: single-quoted string.
931 |                 out.push(format!("highlights_marker_hash: '{hash}'"));
932 |                 continue;
933 ~             }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/sources.rs:146:21
    |
146 | /                     if source_pdf.is_none() {
147 | |                         source_pdf = value;
148 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
145 ~                 "source_pdf"
146 ~                     if source_pdf.is_none() => {
147 |                         source_pdf = value;
148 ~                     }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/stamp.rs:518:5
    |
518 | /     if let (Ok(child_c), Ok(parent_c)) =
519 | |         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
520 | |     {
521 | |         if let Some(rel) = relative_inside(&child_c, &parent_c) {
...   |
524 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
519 ~         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
520 ~         && let Some(rel) = relative_inside(&child_c, &parent_c) {
521 |             return Some(rel);
522 ~         }
    |

error: this boolean expression contains a logic bug
   --> src/native/highlights_ref/sync.rs:672:26
    |
672 |               let needed = semantic_needed
    |  __________________________^
673 | |                 || (options.write_pdf && hint_needed)
674 | |                 || (options.dry_run && hint_needed && semantic_needed);
    | |______________________________________________________________________^ help: it would look like the following: `semantic_needed || options.write_pdf && hint_needed`
    |
help: this expression can be optimized out by applying boolean operations to the outer expression
   --> src/native/highlights_ref/sync.rs:674:21
    |
674 |                 || (options.dry_run && hint_needed && semantic_needed);
    |                     ^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#overly_complex_bool_expr
    = note: `#[deny(clippy::overly_complex_bool_expr)]` on by default

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1053:9
     |
1053 | /         if trimmed.starts_with("done_tasks:") {
1054 | |             if let Some(start) = trimmed.find("[[") {
1055 | |                 if let Some(end) = trimmed[start..].find("]]") {
1056 | |                     let target = &trimmed[start + 2..start + end];
...    |
1064 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1053 ~         if trimmed.starts_with("done_tasks:")
1054 ~             && let Some(start) = trimmed.find("[[") {
1055 |                 if let Some(end) = trimmed[start..].find("]]") {
 ...
1062 |                 }
1063 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1054:13
     |
1054 | /             if let Some(start) = trimmed.find("[[") {
1055 | |                 if let Some(end) = trimmed[start..].find("]]") {
1056 | |                     let target = &trimmed[start + 2..start + end];
1057 | |                     let mut rel = target.trim().to_string();
...    |
1063 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1054 ~             if let Some(start) = trimmed.find("[[")
1055 ~                 && let Some(end) = trimmed[start..].find("]]") {
1056 |                     let target = &trimmed[start + 2..start + end];
 ...
1061 |                     return Some(rel);
1062 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1067:5
     |
1067 | /     if relative.components().count() == 1 {
1068 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1069 | |             return Some(format!("done/{stem}_done.md"));
1070 | |         }
1071 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1067 ~     if relative.components().count() == 1
1068 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1069 |             return Some(format!("done/{stem}_done.md"));
1070 ~         }
     |

warning: useless use of `format!`
   --> src/native/highlights_ref/target.rs:132:39
    |
132 |                   Err(CommandError::new(format!(
    |  _______________________________________^
133 | |                     "unsupported content type (missing): create accepts Markdown files, PDFs, PDF URLs, arXiv paper URLs, and web...
134 | |                 )))
    | |_________________^ help: consider using `.to_string()`: `"unsupported content type (missing): create accepts Markdown files, PDFs, PDF URLs, arXiv paper URLs, and web article URLs".to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format
    = note: `#[warn(clippy::useless_format)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/plugins/sync.rs:198:13
    |
198 | /             if let Some(parent) = backup_file.parent() {
199 | |                 if let Err(error) = fs::create_dir_all(parent) {
200 | |                     return Ok(FileOutcome {
201 | |                         action: FileAction::Failed,
...   |
210 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
198 ~             if let Some(parent) = backup_file.parent()
199 ~                 && let Err(error) = fs::create_dir_all(parent) {
200 |                     return Ok(FileOutcome {
...
208 |                     });
209 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/plugins/sync.rs:230:9
    |
230 | /         if let Some(parent) = vault_file.parent() {
231 | |             if let Err(error) = fs::create_dir_all(parent) {
232 | |                 return Ok(FileOutcome {
233 | |                     action: FileAction::Failed,
...   |
241 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
230 ~         if let Some(parent) = vault_file.parent()
231 ~             && let Err(error) = fs::create_dir_all(parent) {
232 |                 return Ok(FileOutcome {
...
239 |                 });
240 ~             }
    |

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/projects/scan.rs:216:5
    |
216 | /     let Some(&(line_number, raw_value)) = fields.first() else {
217 | |         return None;
218 | |     };
    | |______^ help: replace it with: `let &(line_number, raw_value) = fields.first()?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this `if` statement can be collapsed
   --> src/native/ref_jobs/spool.rs:399:9
    |
399 | /         if let Err(error) = fs::remove_file(path) {
400 | |             if error.kind() != std::io::ErrorKind::NotFound {
401 | |                 failures.push(format!(
402 | |                     "remove staged ref job {}: {error}",
...   |
406 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
399 ~         if let Err(error) = fs::remove_file(path)
400 ~             && error.kind() != std::io::ErrorKind::NotFound {
401 |                 failures.push(format!(
...
404 |                 ));
405 ~             }
    |

warning: this `if` statement can be collapsed
  --> src/native/ref_library/migrate_tasks/line.rs:81:9
   |
81 | /         if let Some(after) = line.strip_prefix(marker) {
82 | |             if after.starts_with('[') {
83 | |                 if let Some(close) = after.find(']') {
84 | |                     let mark_part = &after[..close + 1];
...  |
89 | |         }
   | |_________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
   |
81 ~         if let Some(after) = line.strip_prefix(marker)
82 ~             && after.starts_with('[') {
83 |                 if let Some(close) = after.find(']') {
...
87 |                 }
88 ~             }
   |

warning: this `if` statement can be collapsed
  --> src/native/ref_library/migrate_tasks/line.rs:82:13
   |
82 | /             if after.starts_with('[') {
83 | |                 if let Some(close) = after.find(']') {
84 | |                     let mark_part = &after[..close + 1];
85 | |                     let rest = after[close + 1..].trim_start().to_string();
...  |
88 | |             }
   | |_____________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
   |
82 ~             if after.starts_with('[')
83 ~                 && let Some(close) = after.find(']') {
84 |                     let mark_part = &after[..close + 1];
85 |                     let rest = after[close + 1..].trim_start().to_string();
86 |                     return (format!("{marker}{mark_part} "), rest);
87 ~                 }
   |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/line.rs:138:5
    |
138 | /     if let Some(last) = tokens.last() {
139 | |         if *last == "^ref" || last.starts_with("^ref-") {
140 | |             tokens.pop();
141 | |         }
142 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
138 ~     if let Some(last) = tokens.last()
139 ~         && (*last == "^ref" || last.starts_with("^ref-")) {
140 |             tokens.pop();
141 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:720:13
    |
720 | /             if let Some((key, value)) = raw.split_once(':') {
721 | |                 if key.trim().eq_ignore_ascii_case("title") {
722 | |                     let mut v = value.trim().to_string();
723 | |                     if (v.starts_with('"') && v.ends_with('"') && v.len() >= 2)
...   |
734 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
720 ~             if let Some((key, value)) = raw.split_once(':')
721 ~                 && key.trim().eq_ignore_ascii_case("title") {
722 |                     let mut v = value.trim().to_string();
...
732 |                     }
733 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:745:13
    |
745 | /             if let Some((key, value)) = raw.split_once(':') {
746 | |                 if key.trim().eq_ignore_ascii_case("created") {
747 | |                     let mut v = value.trim().to_string();
748 | |                     if (v.starts_with('"') && v.ends_with('"') && v.len() >= 2)
...   |
767 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
745 ~             if let Some((key, value)) = raw.split_once(':')
746 ~                 && key.trim().eq_ignore_ascii_case("created") {
747 |                     let mut v = value.trim().to_string();
...
765 |                     }
766 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:787:9
    |
787 | /         if let Some(archive_rel) = archive_rel_for(bob_dir, dest_abs, &contents)
788 | |         {
789 | |             if let Ok(archive) =
790 | |                 std::fs::read_to_string(bob_dir.join(&archive_rel))
...   |
798 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
787 ~         if let Some(archive_rel) = archive_rel_for(bob_dir, dest_abs, &contents)
788 ~             && let Ok(archive) =
789 |                 std::fs::read_to_string(bob_dir.join(&archive_rel))
...
795 |                 );
796 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:811:9
    |
811 | /         if trimmed.starts_with("done_tasks:") {
812 | |             if let Some(start) = trimmed.find("[[") {
813 | |                 if let Some(end) = trimmed[start..].find("]]") {
814 | |                     let target = &trimmed[start + 2..start + end];
...   |
822 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
811 ~         if trimmed.starts_with("done_tasks:")
812 ~             && let Some(start) = trimmed.find("[[") {
813 |                 if let Some(end) = trimmed[start..].find("]]") {
...
820 |                 }
821 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:812:13
    |
812 | /             if let Some(start) = trimmed.find("[[") {
813 | |                 if let Some(end) = trimmed[start..].find("]]") {
814 | |                     let target = &trimmed[start + 2..start + end];
815 | |                     let mut rel = target.trim().to_string();
...   |
821 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
812 ~             if let Some(start) = trimmed.find("[[")
813 ~                 && let Some(end) = trimmed[start..].find("]]") {
814 |                     let target = &trimmed[start + 2..start + end];
...
819 |                     return Some(rel);
820 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:825:5
    |
825 | /     if relative.components().count() == 1 {
826 | |         if let Some(stem) = dest_abs.file_stem().and_then(|s| s.to_str()) {
827 | |             return Some(format!("done/{stem}_done.md"));
828 | |         }
829 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
825 ~     if relative.components().count() == 1
826 ~         && let Some(stem) = dest_abs.file_stem().and_then(|s| s.to_str()) {
827 |             return Some(format!("done/{stem}_done.md"));
828 ~         }
    |

warning: `format!` in `format!` args
    --> src/native/ref_library/migrate_tasks/plan.rs:1004:20
     |
1004 |               return format!(
     |  ____________________^
1005 | |                 "{}{}",
1006 | |                 &line[..caret + 1],
1007 | |                 format!("{new_id}{}", &line[trimmed_end..])
1008 | |             );
     | |_____________^
     |
     = help: combine the `format!(..)` arguments with the outer `format!(..)` call
     = help: or consider changing `format!` to `format_args!`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args
     = note: `#[warn(clippy::format_in_format_args)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/rewrite.rs:452:21
    |
452 | /                     if frag == "^ref" {
453 | |                         if let LinkResolution::Migrated(ref_note) =
454 | |                             resolve_link_target(
455 | |                                 &tpart,
...   |
472 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
452 ~                     if frag == "^ref"
453 ~                         && let LinkResolution::Migrated(ref_note) =
454 |                             resolve_link_target(
...
470 |                             }
471 ~                         }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/rewrite.rs:453:25
    |
453 | /                         if let LinkResolution::Migrated(ref_note) =
454 | |                             resolve_link_target(
455 | |                                 &tpart,
456 | |                                 path_to_ref,
...   |
471 | |                         }
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
459 ~                             )
460 ~                             && let Some((route, new_id)) =
461 |                                 final_map.get(&ref_note)
...
468 |                                 ));
469 ~                             }
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/ref_library/migrate_tasks/write.rs:544:21
    |
544 |                     &task,
    |                     ^^^^^ help: change this to: `task`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
    = note: `#[warn(clippy::needless_borrow)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/write.rs:554:9
    |
554 | /         if let Some(old) = task.old_dep_id.clone() {
555 | |             if let Ok(new) = crate::native::task_dependencies::dependency_id(
556 | |                 Path::new(&task.parent_path),
557 | |                 &final_id,
...   |
561 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
554 ~         if let Some(old) = task.old_dep_id.clone()
555 ~             && let Ok(new) = crate::native::task_dependencies::dependency_id(
556 |                 Path::new(&task.parent_path),
...
559 |                 dep_final.insert(old, new);
560 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/write.rs:737:13
    |
737 | /             if path
738 | |                 .extension()
739 | |                 .and_then(|e| e.to_str())
740 | |                 .is_some_and(|e| e.eq_ignore_ascii_case("md"))
...   |
745 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
740 ~                 .is_some_and(|e| e.eq_ignore_ascii_case("md"))
741 ~                 && let Ok(rel) = path.strip_prefix(bob_dir) {
742 |                     ref_notes.push(rel.to_string_lossy().replace('\\', "/"));
743 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/write.rs:888:17
    |
888 | /                 if let Some((_, block_id)) =
889 | |                     crate::native::task_dependencies::parse_block_link_inside(
890 | |                         inside,
...   |
917 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
891 ~                     )
892 ~                     && block_id == "ref" {
893 |                         // Any remaining #^ref link whose target is a migrated
...
914 |                         }
915 ~                     }
    |

warning: the loop variable `index` is used to index `lines`
  --> src/native/ref_tasks/embed.rs:76:22
   |
76 |         for index in start..end.min(lines.len()) {
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
   = note: `#[warn(clippy::needless_range_loop)]` on by default
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

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:231:9
    |
231 | /         if trimmed.starts_with("done_tasks:") {
232 | |             if let Some(start) = trimmed.find("[[") {
233 | |                 if let Some(end) = trimmed[start..].find("]]") {
234 | |                     let target = &trimmed[start + 2..start + end];
...   |
242 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
231 ~         if trimmed.starts_with("done_tasks:")
232 ~             && let Some(start) = trimmed.find("[[") {
233 |                 if let Some(end) = trimmed[start..].find("]]") {
...
240 |                 }
241 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:232:13
    |
232 | /             if let Some(start) = trimmed.find("[[") {
233 | |                 if let Some(end) = trimmed[start..].find("]]") {
234 | |                     let target = &trimmed[start + 2..start + end];
235 | |                     let mut rel = target.trim().to_string();
...   |
241 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
232 ~             if let Some(start) = trimmed.find("[[")
233 ~                 && let Some(end) = trimmed[start..].find("]]") {
234 |                     let target = &trimmed[start + 2..start + end];
...
239 |                     return Some(rel);
240 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:249:5
    |
249 | /     if relative.components().count() == 1 {
250 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
251 | |             return Some(format!("done/{stem}_done.md"));
252 | |         }
253 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
249 ~     if relative.components().count() == 1
250 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
251 |             return Some(format!("done/{stem}_done.md"));
252 ~         }
    |

warning: this manual char comparison can be written more succinctly
  --> src/native/ref_tasks/line.rs:42:49
   |
42 |     let trimmed_start = line.trim_start_matches(|c| c == ' ' || c == '\t');
   |                                                 ^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `[' ', '\t']`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_pattern_char_comparison
   = note: `#[warn(clippy::manual_pattern_char_comparison)]` on by default

warning: this manual char comparison can be written more succinctly
  --> src/native/ref_tasks/line.rs:79:53
   |
79 |     let trimmed_start = stripped.trim_start_matches(|c| c == ' ' || c == '\t');
   |                                                     ^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `[' ', '\t']`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_pattern_char_comparison

warning: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
    = note: `#[warn(clippy::explicit_counter_loop)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/walk.rs:648:9
    |
648 | /         if b == b'#' || b == b'^' {
649 | |             if bytes[i + 1].eq_ignore_ascii_case(&b'r')
650 | |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
651 | |                 && bytes[i + 3].eq_ignore_ascii_case(&b'f')
...   |
655 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
648 ~         if (b == b'#' || b == b'^') {
649 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
650 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
653 |                 return true;
654 ~             }
    |

warning: this function has too many arguments (8/7)
   --> src/native/task_status_groups/emit.rs:118:1
    |
118 | / pub(super) fn emit_grouped_body(
119 | |     node: &HeadingNode,
120 | |     contents: &str,
121 | |     classified: &ClassifiedChildren<'_>,
...   |
126 | |     heading_has_line_ending: bool,
127 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
   --> src/native/task_status_hooks/references.rs:499:5
    |
499 | /     if let Some(Some(task_id)) =
500 | |         task_ids.get(&(target_path.to_path_buf(), block_id.to_string()))
501 | |     {
502 | |         if task
...   |
509 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
500 ~         task_ids.get(&(target_path.to_path_buf(), block_id.to_string()))
501 ~         && task
502 |             .depends_on
...
506 |             return true;
507 ~         }
    |

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:389:5
    |
389 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:256:9
    |
256 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this `impl` can be derived
   --> src/native/vault_sync.rs:164:1
    |
164 | / impl Default for RunOptions {
165 | |     fn default() -> Self {
166 | |         Self {
167 | |             dry_run: false,
...   |
172 | | }
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#derivable_impls
    = note: `#[warn(clippy::derivable_impls)]` on by default
help: replace the manual implementation with a derive attribute
    |
158 + #[derive(Default)]
159 | struct RunOptions {
    |

warning: `bob-cli` (lib) generated 126 warnings
error: could not compile `bob-cli` (lib) due to 1 previous error; 126 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: associated function `for_tests` is never used
   --> src/native/highlights_ref/model.rs:484:19
    |
472 | impl ScanContext {
    | ---------------- associated function in this implementation
...
484 |     pub(super) fn for_tests(
    |                   ^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1247:9
     |
1247 | /         match lex_bullets(close, draft).expect("valid bullets") {
1248 | |             CloseLogLexed { entries, dangling } => {
1249 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1250 | |                 entries
...    |
1255 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `#[warn(clippy::match_single_binding)]` on by default
help: consider using a `let` statement
     |
1247 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1248 +         {
1249 +             assert!(dangling.is_empty(), "unexpected dangling");
1250 +             entries
1251 +                 .into_iter()
1252 +                 .map(|entry| (entry.index, entry.text, entry.details))
1253 +                 .collect()
1254 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1354:9
     |
1354 | /         match lex_bullets("=x", "=x\n- 1").expect("dangling") {
1355 | |             CloseLogLexed { entries, dangling } => {
1356 | |                 assert!(entries.is_empty());
1357 | |                 assert_eq!(dangling.len(), 1);
...    |
1360 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1354 ~         let CloseLogLexed { entries, dangling } = lex_bullets("=x", "=x\n- 1").expect("dangling");
1355 +         {
1356 +             assert!(entries.is_empty());
1357 +             assert_eq!(dangling.len(), 1);
1358 +             assert_eq!(dangling[0].index, 1);
1359 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1427:9
     |
1427 | /         match lex_bullets("=x~1", "=x~1\n- 2 ok\n- wired").expect_err("missing")
1428 | |         {
1429 | |             error => assert!(
1430 | |                 error.message.contains("- 2 wired"),
...    |
1433 | |             ),
1434 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1427 ~         let error = lex_bullets("=x~1", "=x~1\n- 2 ok\n- wired").expect_err("missing");
1428 +         assert!(
1429 +             error.message.contains("- 2 wired"),
1430 +             "{}",
1431 +             error.message
1432 +         )
     |

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:1992:35
     |
1992 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call
     = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2029:48
     |
2029 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2038:22
     |
2038 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: you seem to be trying to use `match` for destructuring a single pattern. Consider using `if let`
  --> src/native/capture_language/tests/ref_grammar.rs:76:5
   |
76 | /     match execute_routing(raw, policy) {
77 | |         Ok(parsed) => assert!(
78 | |             !matches!(parsed.kind, CaptureKind::Ref(_)),
79 | |             "{raw}: must not claim a reference item, got {:?}",
...  |
82 | |         Err(_) => {}
83 | |     }
   | |_____^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_match
   = note: `#[warn(clippy::single_match)]` on by default
help: try
   |
76 ~     if let Ok(parsed) = execute_routing(raw, policy) { assert!(
77 +         !matches!(parsed.kind, CaptureKind::Ref(_)),
78 +         "{raw}: must not claim a reference item, got {:?}",
79 +         parsed.kind
80 +     ) }
   |

warning: for loop over a single element
    --> src/native/capture_parse.rs:1539:9
     |
1539 | /         for raw in ["Plan =x"] {
1540 | |             let prose = json(raw);
1541 | |             assert_eq!(prose["mode"], "task", "{raw}");
1542 | |             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1543 | |             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1544 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
     = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
     |
1539 ~         {
1540 +             let raw = "Plan =x";
1541 +             let prose = json(raw);
1542 +             assert_eq!(prose["mode"], "task", "{raw}");
1543 +             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1544 +             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1545 +         }
     |

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

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:764:9
    |
764 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:796:9
    |
796 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:711:27
    |
711 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:723:27
    |
723 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:735:27
    |
735 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: `bob-cli` (lib test) generated 134 warnings (117 duplicates)
error: could not compile `bob-cli` (lib test) due to 1 previous error; 134 warnings emitted
error: Recipe `check` failed on line 26 with exit code 101
failed  exit=101  duration=98550ms

