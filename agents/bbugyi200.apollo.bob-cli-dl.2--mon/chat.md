# Chat History - ace-run (bob-cli-dl.2--mon)

- **TIMESTAMP:** 2026-10-28 09:58:26 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-dl.2--mon

## Prompt

sase monitor start --command 'just check' --reason 'Run the full bob-cli check before completing the approved cancellation engine phase'

## Response

sase tool run 85a9d70eec86831f81d770d3ac51f1d2

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14/crates/bob-obsidian-assets)
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_14)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:485:12
    |
485 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:144:20
    |
144 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

warning: this `else` branch is empty
  --> src/native/task_cancel/prune.rs:94:15
   |
94 |               } else {
   |  _______________^
95 | |             }
   | |_____________^ help: you can remove it
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_else
   = note: `#[warn(clippy::needless_else)]` on by default

error: methods `is_cancel_label` and `cancel_label_for_inverse` are never used
  --> src/native/config/relations.rs:35:19
   |
34 | impl RelationsConfig {
   | -------------------- methods in this implementation
35 |     pub(crate) fn is_cancel_label(&self, key: &str) -> bool {
   |                   ^^^^^^^^^^^^^^^
...
39 |     pub(crate) fn cancel_label_for_inverse(&self, key: &str) -> Option<&str> {
   |                   ^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = note: `-D dead-code` implied by `-D unused`
   = help: to override `-D unused` add `#[expect(dead_code)]` or `#[allow(dead_code)]`

error: enum `DailyReadState` is never used
  --> src/native/task_cancel/mod.rs:27:17
   |
27 | pub(crate) enum DailyReadState {
   |                 ^^^^^^^^^^^^^^

error: struct `TaskCancelInput` is never constructed
  --> src/native/task_cancel/mod.rs:33:19
   |
33 | pub(crate) struct TaskCancelInput<'a> {
   |                   ^^^^^^^^^^^^^^^

error: enum `TaskCancelError` is never used
  --> src/native/task_cancel/mod.rs:55:17
   |
55 | pub(crate) enum TaskCancelError {
   |                 ^^^^^^^^^^^^^^^

error: struct `TaskCancelPlan` is never constructed
  --> src/native/task_cancel/mod.rs:61:19
   |
61 | pub(crate) struct TaskCancelPlan {
   |                   ^^^^^^^^^^^^^^

error: function `plan_task_cancel` is never used
  --> src/native/task_cancel/mod.rs:80:15
   |
80 | pub(crate) fn plan_task_cancel(
   |               ^^^^^^^^^^^^^^^^

error: function `logical_line` is never used
   --> src/native/task_cancel/mod.rs:252:4
    |
252 | fn logical_line(segment: &str) -> &str {
    |    ^^^^^^^^^^^^

error: enum `CancelLogOutcome` is never used
  --> src/native/task_cancel/line.rs:14:17
   |
14 | pub(crate) enum CancelLogOutcome {
   |                 ^^^^^^^^^^^^^^^^

error: struct `SourceEdit` is never constructed
  --> src/native/task_cancel/line.rs:21:19
   |
21 | pub(crate) struct SourceEdit {
   |                   ^^^^^^^^^^

error: function `edit_source` is never used
  --> src/native/task_cancel/line.rs:26:15
   |
26 | pub(crate) fn edit_source(
   |               ^^^^^^^^^^^

error: function `upsert_cancelled_date` is never used
  --> src/native/task_cancel/line.rs:95:15
   |
95 | pub(crate) fn upsert_cancelled_date(line: &str, date: NaiveDate) -> String {
   |               ^^^^^^^^^^^^^^^^^^^^^

error: function `trailing_block_id_start` is never used
   --> src/native/task_cancel/line.rs:121:4
    |
121 | fn trailing_block_id_start(line: &str) -> Option<usize> {
    |    ^^^^^^^^^^^^^^^^^^^^^^^

error: function `insert_line_after` is never used
   --> src/native/task_cancel/line.rs:134:4
    |
134 | fn insert_line_after(
    |    ^^^^^^^^^^^^^^^^^

error: function `line_ending` is never used
   --> src/native/task_cancel/line.rs:157:4
    |
157 | fn line_ending(segment: &str) -> &str {
    |    ^^^^^^^^^^^

error: function `logical_line` is never used
   --> src/native/task_cancel/line.rs:167:4
    |
167 | fn logical_line(segment: &str) -> &str {
    |    ^^^^^^^^^^^^

error: function `predominant_line_ending` is never used
   --> src/native/task_cancel/line.rs:172:4
    |
172 | fn predominant_line_ending(content: &str) -> &'static str {
    |    ^^^^^^^^^^^^^^^^^^^^^^^

error: struct `TaskIdentity` is never constructed
  --> src/native/task_cancel/prune.rs:14:19
   |
14 | pub(crate) struct TaskIdentity {
   |                   ^^^^^^^^^^^^

error: struct `PruneResult` is never constructed
  --> src/native/task_cancel/prune.rs:20:19
   |
20 | pub(crate) struct PruneResult {
   |                   ^^^^^^^^^^^

error: struct `Match` is never constructed
  --> src/native/task_cancel/prune.rs:30:8
   |
30 | struct Match {
   |        ^^^^^

error: function `prune_daily` is never used
  --> src/native/task_cancel/prune.rs:38:15
   |
38 | pub(crate) fn prune_daily(
   |               ^^^^^^^^^^^

error: function `unchanged` is never used
   --> src/native/task_cancel/prune.rs:192:4
    |
192 | fn unchanged(content: &str) -> PruneResult {
    |    ^^^^^^^^^

error: function `is_dedicated_line` is never used
   --> src/native/task_cancel/prune.rs:203:4
    |
203 | fn is_dedicated_line<'a>(
    |    ^^^^^^^^^^^^^^^^^

error: function `remove_token_and_normalize_gap` is never used
   --> src/native/task_cancel/prune.rs:237:4
    |
237 | fn remove_token_and_normalize_gap(
    |    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

error: function `line_ending` is never used
   --> src/native/task_cancel/prune.rs:269:4
    |
269 | fn line_ending(segment: &str) -> &str {
    |    ^^^^^^^^^^^

error: function `logical_line` is never used
   --> src/native/task_cancel/prune.rs:279:4
    |
279 | fn logical_line(segment: &str) -> &str {
    |    ^^^^^^^^^^^^

error: struct `RecoveredTask` is never constructed
  --> src/native/task_cancel/recovery.rs:22:19
   |
22 | pub(crate) struct RecoveredTask {
   |                   ^^^^^^^^^^^^^

error: struct `RecoveryPlan` is never constructed
  --> src/native/task_cancel/recovery.rs:30:19
   |
30 | pub(crate) struct RecoveryPlan {
   |                   ^^^^^^^^^^^^

error: function `recover_cancelled_source` is never used
  --> src/native/task_cancel/recovery.rs:37:15
   |
37 | pub(crate) fn recover_cancelled_source(
   |               ^^^^^^^^^^^^^^^^^^^^^^^^

error: function `recovered_tasks` is never used
  --> src/native/task_cancel/recovery.rs:97:4
   |
97 | fn recovered_tasks(
   |    ^^^^^^^^^^^^^^^

error: enum `CancelSourceVerdict` is never used
  --> src/native/task_cancel/verdicts.rs:10:17
   |
10 | pub(crate) enum CancelSourceVerdict {
   |                 ^^^^^^^^^^^^^^^^^^^

error: method `is_cancelled` is never used
  --> src/native/task_cancel/verdicts.rs:23:19
   |
22 | impl CancelSourceVerdict {
   | ------------------------ method in this implementation
23 |     pub(crate) fn is_cancelled(self) -> bool {
   |                   ^^^^^^^^^^^^

error: function `cancel_verdict` is never used
  --> src/native/task_cancel/verdicts.rs:30:15
   |
30 | pub(crate) fn cancel_verdict(
   |               ^^^^^^^^^^^^^^

error: function `task_status` is never used
  --> src/native/task_cancel/verdicts.rs:55:4
   |
55 | fn task_status(line: &str) -> Option<char> {
   |    ^^^^^^^^^^^

error: function `source_block_id` is never used
  --> src/native/task_cancel/verdicts.rs:67:4
   |
67 | fn source_block_id(line: &str) -> Option<&str> {
   |    ^^^^^^^^^^^^^^^

error: enum `RelationAction` is never used
  --> src/native/task_cancel/verdicts.rs:82:17
   |
82 | pub(crate) enum RelationAction {
   |                 ^^^^^^^^^^^^^^

error: enum `RelationDirection` is never used
  --> src/native/task_cancel/verdicts.rs:89:17
   |
89 | pub(crate) enum RelationDirection {
   |                 ^^^^^^^^^^^^^^^^^

error: enum `RelationTrigger` is never used
  --> src/native/task_cancel/verdicts.rs:95:17
   |
95 | pub(crate) enum RelationTrigger {
   |                 ^^^^^^^^^^^^^^^

error: enum `ItemActionConflict` is never used
   --> src/native/task_cancel/verdicts.rs:109:17
    |
109 | pub(crate) enum ItemActionConflict {
    |                 ^^^^^^^^^^^^^^^^^^

error: associated function `from_modifier` is never used
   --> src/native/task_cancel/verdicts.rs:118:19
    |
117 | impl ItemActionConflict {
    | ----------------------- associated function in this implementation
118 |     pub(crate) fn from_modifier(modifier: &str) -> Option<Self> {
    |                   ^^^^^^^^^^^^^

error: enum `RelationPolicyVerdict` is never used
   --> src/native/task_cancel/verdicts.rs:131:17
    |
131 | pub(crate) enum RelationPolicyVerdict {
    |                 ^^^^^^^^^^^^^^^^^^^^^

error: methods `as_str` and `cancels` are never used
   --> src/native/task_cancel/verdicts.rs:141:19
    |
140 | impl RelationPolicyVerdict {
    | -------------------------- methods in this implementation
141 |     pub(crate) fn as_str(&self) -> &'static str {
    |                   ^^^^^^
...
152 |     pub(crate) fn cancels(&self) -> bool {
    |                   ^^^^^^^

error: struct `RelationPolicyInput` is never constructed
   --> src/native/task_cancel/verdicts.rs:157:19
    |
157 | pub(crate) struct RelationPolicyInput<'a> {
    |                   ^^^^^^^^^^^^^^^^^^^

error: function `relation_policy_verdict` is never used
   --> src/native/task_cancel/verdicts.rs:173:15
    |
173 | pub(crate) fn relation_policy_verdict(
    |               ^^^^^^^^^^^^^^^^^^^^^^^

error: function `plan_recovery_only` is never used
   --> src/native/task_complete/successors.rs:660:15
    |
660 | pub(crate) fn plan_recovery_only(
    |               ^^^^^^^^^^^^^^^^^^

error: variant `CancelRecovery` is never constructed
   --> src/native/task_complete/successors.rs:677:5
    |
675 | enum SuccessorMode {
    |      ------------- variant in this enum
676 |     Completion,
677 |     CancelRecovery {
    |     ^^^^^^^^^^^^^^
    |
    = note: `SuccessorMode` has derived impls for the traits `Clone` and `Debug`, but these are intentionally ignored during dead code analysis

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
    --> src/native/capture/dependencies.rs:1011:1
     |
1011 | / fn resolve_prerequisites(
1012 | |     ctx: &DependencyContext,
1013 | |     planner: &mut CaptureBatchPlanner,
1014 | |     bob_dir: &Path,
...    |
1019 | |     dependent_desc: &str,
1020 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
     = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1353:24
     |
1353 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
     = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1912:6
     |
1912 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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

warning: this function has too many arguments (11/7)
   --> src/native/capture/output.rs:358:5
    |
358 | /     pub(super) fn from_items(
359 | |         items: Vec<CaptureItemResult>,
360 | |         global_destination: Option<GlobalDestinationSummary>,
361 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
369 | |         inbox_route: InboxRouteReport,
370 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/plan.rs:550:1
    |
550 | / pub(super) fn plan_capture_item(
551 | |     request: &CaptureRequest,
552 | |     parsed_item: ParsedCaptureItem,
553 | |     now: chrono::NaiveDateTime,
...   |
560 | |     config_path: Option<&Path>,
561 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/capture/pomodoro_insert.rs:255:1
    |
255 | / pub(super) fn insert_named_pomodoro_child_block(
256 | |     contents: &str,
257 | |     block: &str,
258 | |     selector: &str,
...   |
264 | |     open: &[(usize, &str)],
265 | | ) -> Result<(String, Placement, usize, String), CaptureError> {
    | |_____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:905:1
    |
905 | / fn relation_update_json(
906 | |     direction: RelationDirection,
907 | |     source_relative: &Path,
908 | |     source_line: usize,
...   |
913 | |     previous_label: Option<String>,
914 | | ) -> RelationUpdateJson {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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

warning: this function has too many arguments (9/7)
   --> src/native/capture_complete/candidates.rs:774:1
    |
774 | / fn relationship_disabled_reason(
775 | |     bob_dir: &Path,
776 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
777 | |     graph: &HashMap<
...   |
786 | |     blocked_tasks: &[ResolvedRelationshipEntry],
787 | | ) -> Option<String> {
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1406:6
     |
1406 |   ) -> (
     |  ______^
1407 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1408 | |     Vec<String>,
1409 | |     Vec<(String, usize)>,
1410 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:551:1
    |
551 | / pub(super) enum TokenParse {
552 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
553 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
554 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
552 -     Marker(MarkerParse),
552 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:274:1
    |
274 | / pub(super) fn parse_editor_named_start_item<'a>(
275 | |     item: &CaptureItem<'a>,
276 | |     parent_trimmed: &str,
277 | |     suffix: String,
...   |
283 | |     spelling: NameSpelling,
284 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: match expression looks like `matches!` macro
    --> src/native/capture_language/item.rs:1391:31
     |
1391 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
1392 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1393 | |                 (false, '~', Some(b'@')) => true,
1394 | |                 _ => false,
1395 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
1391 -             let want_second = match (name.is_some(), first_sigil, second) {
1392 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1393 -                 (false, '~', Some(b'@')) => true,
1394 -                 _ => false,
1395 -             };
1391 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:1709:1
     |
1709 | / pub(super) fn named_shape_error_with_drop(
1710 | |     token: &str,
1711 | |     suffix: &str,
1712 | |     name: &str,
...    |
1717 | |     is_literal: bool,
1718 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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

warning: this `if` has identical blocks
   --> src/native/capture_language/rewrite.rs:110:38
    |
110 |       } else if rest.starts_with('\n') {
    |  ______________________________________^
111 | |         "\n"
112 | |     } else if rest.is_empty() {
    | |_____^
    |
note: same as this
   --> src/native/capture_language/rewrite.rs:112:31
    |
112 |       } else if rest.is_empty() {
    |  _______________________________^
113 | |         "\n"
114 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else
    = note: `#[warn(clippy::if_same_then_else)]` on by default

warning: this boolean expression can be simplified
   --> src/native/capture_language/rewrite.rs:322:8
    |
322 |       if !raw_text[..run_start]
    |  ________^
323 | |         .chars()
324 | |         .next_back()
325 | |         .is_some_and(|before| !before.is_whitespace())
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
    = note: `#[warn(clippy::nonminimal_bool)]` on by default
help: try
    |
322 ~     if raw_text[..run_start]
323 +         .chars()
324 +         .next_back().is_none_or(|before| before.is_whitespace())
    |

warning: redundant guard
   --> src/native/capture_language/tokens.rs:959:43
    |
959 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
    |
959 -                 Some((after_x, x_len)) if after_x.is_empty() => {
959 +                 Some(("", x_len)) => {
    |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:134:1
    |
134 | / pub(crate) enum PomodoroCloseOutcome {
135 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 536 bytes
136 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
137 | | }
    | |_^ the entire enum is at least 536 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
135 -     Close(PomodoroClosePlan),
135 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:241:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
241 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:288:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
288 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:476:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
476 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:493:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
493 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:513:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
513 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:536:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
536 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:599:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
599 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:672:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
672 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:826:10
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
826 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:903:6
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
903 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:927:6
    |
129 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
927 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1201:6
     |
 129 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1201 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

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
   --> src/native/capture_related/draft.rs:422:1
    |
422 | / fn draft_match(
423 | |     ranked: bands::RankedMatch<'_>,
424 | |     item: &EditorItemParse,
425 | |     draft: &str,
...   |
430 | |     index: &NoteIndex,
431 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:553:1
    |
553 | / fn verify_link_action(
554 | |     action: &str,
555 | |     item: &EditorItemParse,
556 | |     draft: &str,
...   |
561 | |     options: &EditorParseOptions<'_>,
562 | | ) -> bool {
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
    = note: `#[warn(clippy::manual_strip)]` on by default
help: try using the `strip_prefix` method
    |
381 ~     if let Some(<stripped>) = rest.strip_prefix("[[") {
382 ~         let close = <stripped>.find("]]")?;
    |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_task_toggle/ledger.rs:244:49
    |
244 | pub(crate) fn default_pomodoro_link_destination<'a>(
    |                                                 ^^
245 |     scan: &'a capture_pomodoros::PomodoroScan,
    |            ^^
246 |     queue_owner_line: Option<usize>,
247 | ) -> Option<&'a capture_pomodoros::PomodoroEntry> {
    |              ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
244 ~ pub(crate) fn default_pomodoro_link_destination(
245 ~     scan: &capture_pomodoros::PomodoroScan,
246 |     queue_owner_line: Option<usize>,
247 ~ ) -> Option<&capture_pomodoros::PomodoroEntry> {
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
    --> src/native/highlights_ref/create.rs:1947:1
     |
1947 | / pub(super) fn stamp_overwrite_source(
1948 | |     config: &Config,
1949 | |     plan: &OverwritePreflight,
1950 | |     options: &CreateOptions,
...    |
1955 | |     info: &PdfInfo,
1956 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1989:1
     |
1989 | / pub(super) fn stage_overwrite_audio(
1990 | |     options: &CreateOptions,
1991 | |     plan: &OverwritePreflight,
1992 | |     request: &OverwriteRequest,
...    |
1997 | |     title: &str,
1998 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2660:1
     |
2660 | / fn plan_target_for(
2661 | |     config: &Config,
2662 | |     stem: &str,
2663 | |     ref_type: &str,
...    |
2668 | |     source_display: &str,
2669 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3649:1
     |
3649 | / fn stage_overwrite_source_store(
3650 | |     _config: &Config,
3651 | |     plan: &OverwritePreflight,
3652 | |     scratch: &Path,
...    |
3659 | |     catalog: &super::code_catalog::CatalogOutcome,
3660 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4327:1
     |
4327 | / fn overwrite_pdf_url(
4328 | |     config: &Config,
4329 | |     url: super::clip_url::WebUrl,
4330 | |     downloaded: PathBuf,
...    |
4335 | |     selection: &OverwriteSelection,
4336 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4408:1
     |
4408 | / fn create_pdf_url_route(
4409 | |     config: &Config,
4410 | |     url: super::clip_url::WebUrl,
4411 | |     downloaded: PathBuf,
...    |
4416 | |     listen: Option<&super::listen::ListenCommand>,
4417 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5142:1
     |
5142 | / fn print_pdf_dry_run(
5143 | |     config: &Config,
5144 | |     styler: &Styler,
5145 | |     source_display: &str,
...    |
5153 | |     legacy: &[sources_mod::RecordedSource],
5154 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:5378:1
     |
5378 | / fn compose_markdown_marker(
5379 | |     status: &str,
5380 | |     parent: &str,
5381 | |     title: &str,
...    |
5386 | |     return_links: bool,
5387 | | ) -> Result<String> {
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
   --> src/native/highlights_ref/clip_adapter.rs:743:5
    |
743 | /     DIAGRAM_TIMEOUT_BASE_SECS
744 | |         .saturating_add(
745 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
748 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
743 ~     DIAGRAM_TIMEOUT_BASE_SECS
744 +         .saturating_add(
745 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
746 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:728:1
    |
728 | / pub(super) enum PdfSyncOutcome {
729 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
730 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
731 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
729 -     Written(SyncWriteReport),
729 +     Written(Box<SyncWriteReport>),
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:784:1
    |
784 | / pub(super) enum ScanWriteOutcome {
785 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
786 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
787 | |     Failed(ScanFailure),
788 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
785 -     Written(SyncWriteReport),
785 +     Written(Box<SyncWriteReport>),
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
   = note: `#[warn(clippy::wrong_self_convention)]` on by default

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

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/pdf_target.rs:128:1
    |
128 | / pub(super) fn plan_pdf_url(
129 | |     url: &WebUrl,
130 | |     downloaded: &Path,
131 | |     name_override: Option<&str>,
...   |
136 | |     progress: Option<&dyn Fn(&str)>,
137 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:213:1
    |
213 | / pub(super) fn plan_arxiv(
214 | |     paper: &ArxivPaper,
215 | |     name_override: Option<&str>,
216 | |     title_override: Option<&str>,
...   |
222 | |     progress: Option<&dyn Fn(&str)>,
223 | | ) -> Result<PdfPlan> {
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

warning: this function has too many arguments (15/7)
   --> src/native/plugins/sync.rs:231:1
    |
231 | / fn apply_plugin(
232 | |     options: &SyncOptions,
233 | |     id: &str,
234 | |     captured: &CapturedPlugin,
...   |
246 | |     issues: &mut Vec<String>,
247 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: consider using `sort_by_key`
  --> src/native/pomodoro_homes/label.rs:16:5
   |
16 |     ranked.sort_by(|left, right| right.share.cmp(&left.share));
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
   |
16 -     ranked.sort_by(|left, right| right.share.cmp(&left.share));
16 +     ranked.sort_by_key(|right| std::cmp::Reverse(right.share));
   |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/pomodoro_homes/resolve.rs:298:25
    |
298 | /                         chain[nearest_home..end]
299 | |                             .iter()
300 | |                             .filter(|(_, facts)| {
301 | |                                 facts.kind == NoteKind::Project
302 | |                             })
303 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
303 -                             .last()
303 +                             .next_back()
    |

warning: this function has too many arguments (8/7)
  --> src/native/pomodoro_homes/session.rs:81:1
   |
81 | / pub(crate) fn attribute_ledger_entry<S: HomeSource>(
82 | |     contents: &str,
83 | |     entry_line: usize,
84 | |     name: Option<&str>,
...  |
89 | |     resolver: &mut HomeResolver<S>,
90 | | ) -> SessionHomes {
   | |_________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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
   --> src/native/pomodoro_themes/hints.rs:155:1
    |
155 | / fn suggested_hue(
156 | |     moved: &ThemeRecord,
157 | |     current: Hue,
158 | |     window_days: &[(&NaiveDate, &BTreeSet<String>)],
...   |
163 | |     themes: Option<&crate::native::config::ThemesConfig>,
164 | | ) -> Option<Hue> {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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
   --> src/native/ref_library/today.rs:330:6
    |
330 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/ref_library/today.rs:676:1
    |
676 | / fn fail(
677 | |     format: Format,
678 | |     dry_run: bool,
679 | |     code: &str,
...   |
684 | |     pomodoros: &[TodayPomodoroRow],
685 | | ) -> i32 {
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
   --> src/native/ref_library/mod.rs:914:5
    |
914 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
914 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
    |     ++

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

warning: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
    = note: `#[warn(clippy::explicit_counter_loop)]` on by default

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
   --> src/native/relation_labels/cli.rs:312:18
    |
312 |       let counts = format!(
    |  __________________^
313 | |         "{} {} {} {} {} {}",
314 | |         report.counts.labels,
315 | |         label_word(report.counts.labels),
...   |
319 | |         format!("{} hidden", report.counts.hidden,),
320 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: consider using `sort_by_key`
   --> src/native/relation_labels/rename.rs:759:5
    |
759 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
759 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
759 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

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

error: this `if` statement can be collapsed
   --> src/native/task_cancel/line.rs:97:5
    |
 97 | /     if let Some(start) = line.find("[cancelled::") {
 98 | |         if let Some(end_offset) = line[start..].find(']') {
 99 | |             let end = start + end_offset + 1;
100 | |             let mut output = line.to_string();
...   |
104 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
    = note: requested on the command line with `-D clippy::collapsible-if`
help: collapse nested if block
    |
 97 ~     if let Some(start) = line.find("[cancelled::")
 98 ~         && let Some(end_offset) = line[start..].find(']') {
 99 |             let end = start + end_offset + 1;
...
102 |             return output;
103 ~         }
    |

warning: consider using `sort_by_key`
   --> src/native/task_cancel/prune.rs:167:9
    |
167 |         edits.sort_by(|left, right| right.0.cmp(&left.0));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
167 -         edits.sort_by(|left, right| right.0.cmp(&left.0));
167 +         edits.sort_by_key(|right| std::cmp::Reverse(right.0));
    |

warning: this lifetime isn't used in the function definition
   --> src/native/task_cancel/prune.rs:203:22
    |
203 | fn is_dedicated_line<'a>(
    |                      ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extra_unused_lifetimes
    = note: `#[warn(clippy::extra_unused_lifetimes)]` on by default

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1389:1
     |
1389 | / fn attach_offer(
1390 | |     verdict: &mut DependentVerdict,
1391 | |     files: &[FileScan],
1392 | |     day: &DayView,
...    |
1397 | |     project: Option<PathBuf>,
1398 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:1490:1
     |
1490 | / fn apply_project_member_classes(
1491 | |     verdicts: &mut Vec<DependentVerdict>,
1492 | |     folds: &mut Vec<ProjectFold>,
1493 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
1502 | |     _note_settings: &NoteTaskSettings,
1503 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1839:1
     |
1839 | / fn apply_verdicts(
1840 | |     input: SuccessorInput,
1841 | |     files: Vec<FileScan>,
1842 | |     verdicts: Vec<DependentVerdict>,
...    |
1847 | |     project_folds: Vec<ProjectFold>,
1848 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/plan.rs:1375:6
     |
1375 | ) -> Result<(Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>), PlanError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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
   --> src/native/task_status_hooks/sync.rs:471:5
    |
471 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:338:9
    |
338 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1255:1
     |
1255 | / fn consume_blocked_links_after_compose(
1256 | |     compose: &mut ComposeResult,
1257 | |     files: &[FileScan],
1258 | |     daily_path: &Path,
...    |
1269 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1270 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `bob-obsidian` (lib) generated 126 warnings
error: could not compile `bob-obsidian` (lib) due to 46 previous errors; 126 warnings emitted
warning: build failed, waiting for other jobs to finish...
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
    --> src/native/capture_language/close_log.rs:1353:9
     |
1353 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1354 | |             CloseLogLexed { entries, dangling } => {
1355 | |                 assert!(entries.is_empty());
1356 | |                 assert_eq!(dangling.len(), 1);
...    |
1359 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1353 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1354 +         {
1355 +             assert!(entries.is_empty());
1356 +             assert_eq!(dangling.len(), 1);
1357 +             assert_eq!(dangling[0].index, 1);
1358 +         }
     |

warning: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1426:9
     |
1426 | /         match lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing") {
1427 | |             error => assert!(
1428 | |                 error.message.contains("- 2 wired"),
1429 | |                 "{}",
1430 | |                 error.message
1431 | |             ),
1432 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1426 ~         let error = lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing");
1427 +         assert!(
1428 +             error.message.contains("- 2 wired"),
1429 +             "{}",
1430 +             error.message
1431 +         )
     |

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
    --> src/native/capture_language/tests/grammar.rs:2188:35
     |
2188 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2225:48
     |
2225 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2234:22
     |
2234 |         execute(raw).expect(&format!("{raw} executes as prose"));
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
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

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

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/pomodoro.rs:879:51
    |
879 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
    |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:471:5
    |
471 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:338:9
    |
338 |     let mut files = Vec::with_capacity(markdown_files.len());
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

warning: unnecessary use of `get(&edge("proj.md", "prj")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:814:27
    |
814 |     assert!(scanned.edges.get(&edge("proj.md", "prj")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("proj.md", "prj"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: `bob-obsidian` (lib test) generated 150 warnings (125 duplicates)
error: could not compile `bob-obsidian` (lib test) due to 1 previous error; 150 warnings emitted
error: Recipe `check` failed on line 79 with exit code 101
failed  exit=101  duration=124574ms
verdict: undetermined; exit 101

