# Chat History - ace-run (bob-cli-do.3--mon)

- **TIMESTAMP:** 2026-10-28 11:22:38 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-do.3--mon

## Prompt

sase monitor start --command 'just check' --reason 'Verify before host completion'

## Response

sase tool run 76f26f1c00be2a84f73266e5f93db6c6

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
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
   --> src/native/pomodoro_themes/hints.rs:231:1
    |
231 | / fn suggested_hue(
232 | |     moved: &ThemeRecord,
233 | |     current: Hue,
234 | |     window_days: &[(&NaiveDate, &BTreeSet<String>)],
...   |
239 | |     themes: Option<&crate::native::config::ThemesConfig>,
240 | | ) -> Option<Hue> {
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
    --> src/native/task_complete/successors.rs:1391:1
     |
1391 | / fn attach_offer(
1392 | |     verdict: &mut DependentVerdict,
1393 | |     files: &[FileScan],
1394 | |     day: &DayView,
...    |
1399 | |     project: Option<PathBuf>,
1400 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:1492:1
     |
1492 | / fn apply_project_member_classes(
1493 | |     verdicts: &mut Vec<DependentVerdict>,
1494 | |     folds: &mut Vec<ProjectFold>,
1495 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
1504 | |     _note_settings: &NoteTaskSettings,
1505 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1841:1
     |
1841 | / fn apply_verdicts(
1842 | |     input: SuccessorInput,
1843 | |     files: Vec<FileScan>,
1844 | |     verdicts: Vec<DependentVerdict>,
...    |
1849 | |     project_folds: Vec<ProjectFold>,
1850 | | ) -> SuccessorPlan {
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

warning: `bob-obsidian` (lib) generated 126 warnings (run `cargo clippy --fix --lib -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 10 suggestions)
warning: `bob-obsidian` (lib test) generated 150 warnings (125 duplicates) (run `cargo clippy --fix --lib -p bob-obsidian --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 7 suggestions)
warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:451:14
    |
451 |         .arg("-2 x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#suspicious_command_arg_space
    = note: `#[warn(clippy::suspicious_command_arg_space)]` on by default
help: consider splitting the argument
    |
451 -         .arg("-2 x\n- 1 wired the lexer")
451 +         .args(["-2", "x\n- 1 wired the lexer"])
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
   = note: `#[warn(clippy::too_many_arguments)]` on by default

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

warning: `bob-obsidian` (test "cli") generated 4 warnings
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.81s
cargo test --workspace --no-fail-fast
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/crates/bob-obsidian-assets)
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15)
    Building [======================>  ] 211/228: gkeep_auth(test), randomize…    Building [======================>  ] 212/228: gkeep_auth(test), randomize…    Building [======================>  ] 213/228: gkeep_auth(test), randomize…    Building [======================>  ] 214/228: gkeep_auth(test), randomize…    Building [======================>  ] 215/228: gkeep_auth(test), randomize…    Building [======================>  ] 216/228: gkeep_auth(test), tasks_par…    Building [======================>  ] 217/228: tasks_parity(test), tasks_r…    Building [======================>  ] 218/228: tasks_real_vault_parity(tes…    Building [=======================> ] 219/228: tasks_real_vault_parity(tes…    Building [=======================> ] 220/228: tasks_real_vault_parity(tes…    Building [=======================> ] 221/228: tasks_real_vault_parity(tes…    Building [=======================> ] 222/228: bob_pomodoro(bin test), gke…    Building [=======================> ] 223/228: bob_pomodoro(bin test), bob…    Building [=======================> ] 224/228: bob(bin test), tmux_bob_pom…    Building [=======================> ] 225/228: bob(bin test), bob_notify(b…    Building [=======================> ] 226/228: bob_notify(bin test), bob_c…    Building [=======================> ] 227/228: bob_cli(test)                   Finished `test` profile [unoptimized + debuginfo] target(s) in 1m 16s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/bob_cli-edb465a55cecd3c2)

running 3819 tests
test native::articles::tests::corpus_no_panic_idempotent_and_words ... ignored, set BOB_ARTICLES_CORPUS to a vault of Markdown notes
test native::articles::tests::article_type_forms_are_detected ... ok
test native::articles::tests::adopt_already_article_is_noop_and_other_type_is_refused ... ok
test native::articles::tests::frontmatter_only_article_does_not_gain_an_extra_blank_line ... ok
test native::articles::tests::lazy_list_continuation_is_not_a_setext_heading ... ok
test native::articles::tests::pseudo_footnotes_only_exclude_url_like_destinations ... ok
test native::capture::budget::tests::destination_roles_follow_the_contract ... ok
test native::capture::budget::tests::theme_warning_names_added_themes_with_hint ... ok
test native::capture::dependencies::tests::new_prj_edges_check_implicit_resident_cycles ... ok
test native::articles::tests::layout_bom_and_final_newline ... ok
test native::articles::tests::layout_crlf_file ... ok
test native::articles::tests::adopt_inserts_type_after_parent_and_formats ... ok
test native::articles::tests::heading_links_leave_blocks_and_protected_code_alone ... ok
test native::articles::tests::outline_word_counts_skip_fences_math_and_comments ... ok
test native::articles::tests::report_only_findings_include_pseudo_footnote_broken_and_title ... ok
test native::articles::tests::bad_option_and_number_replaced_findings ... ok
test native::articles::tests::adopt_creates_frontmatter_when_missing_and_inserts_before_close ... ok
test native::articles::tests::invalid_section_numbers_finding_uses_the_option_line ... ok
test native::articles::tests::heading_embeds_refresh_and_preserve_aliases_and_blocks ... ok
test native::articles::tests::article_plan_json_matches_schema_v1_shape ... ok
test native::articles::inbound::tests::layout_only_format_skips_inbound_unless_forced ... ok
test native::capture::inbox_route::tests::ir_snapshot_binding_refuses_when_unstaged_dest_or_repair_changes ... ok
test native::articles::tests::refusals ... ok
test native::articles::inbound::tests::attach_rewrites_two_notes_and_reports_an_unrepairable_link ... ok
test native::articles::inbound::tests::write_skips_a_linking_note_whose_preimage_changed ... ok
test native::articles::tests::nested_heading_paths_rewrite_every_segment_and_numbers_off_removes_them ... ok
test native::articles::tests::fences_spacing_and_unclosed ... ok
test native::articles::tests::heading_spacing_surrounds_protected_blocks ... ok
test native::articles::tests::section_number_counts_and_notice_plurals_reflect_actual_changes ... ok
test native::articles::tests::strip_section_number_keeps_bare_numbers_and_escapes ... ok
test native::articles::tests::heading_links_follow_new_numbers_and_keep_aliases_and_encoding ... ok
test native::articles::vault::tests::write_refuses_a_changed_preimage_before_replacing_it ... ok
test native::articles::tests::setext_and_thematic_breaks ... ok
test native::articles::tests::numbers_off_and_round_trip ... ok
test native::articles::tests::heading_links_resolve_preformat_titles_before_ambiguous_identities ... ok
test native::articles::tests::protected_regions_leave_inner_headings ... ok
test native::articles::tests::indented_code_links_and_blank_runs_are_preserved ... ok
test native::articles::tests::layout_whitespace_crlf_and_bom ... ok
test native::articles::tests::heading_levels_and_depth ... ok
test native::articles::inbound::tests::duplicate_titles_use_preformat_text_and_report_ambiguous_identity ... ok
test native::articles::tests::ownership_tokens ... ok
test native::capture::link_guard::tests::new_task_flip_blocks_open_lines_tags_blocked_and_skips_closed ... ok
test native::articles::tests::blog_draft_matches_worked_example ... ok
test native::articles::tests::outline_counts_words_and_marks_stubs ... ok
test native::capture::output::tests::capture_destination_swatches_respect_no_color ... ok
test native::capture::output::tests::log_entry_details_omitted_when_empty ... ok
test native::capture::output::tests::typed_entry_details_print_two_spaces_under_their_entry ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_tab_children_and_interior_blanks ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_fenced_child_lines_verbatim ... ok
test native::capture::pomodoro_blocks::tests::block_range_stops_at_section_end_and_covers_last_entry ... ok
test native::capture::output::tests::typed_work_log_details_omitted_when_no_entry_has_details ... ok
test native::capture::output::tests::typed_work_log_details_align_with_entries_when_present ... ok
test native::capture::pomodoro_blocks::tests::block_range_trims_trailing_blanks_and_stops_at_zero_indent ... ok
test native::capture::pomodoro_blocks::tests::block_range_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::depth_continuation_lines_take_parent_depth_plus_one ... ok
test native::capture::pomodoro_blocks::tests::depth_counts_nested_list_items ... ok
test native::capture::pomodoro_blocks::tests::pairing_created_block_is_all_added ... ok
test native::capture::pomodoro_blocks::tests::depth_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::pairing_pure_insert_is_added_and_pure_delete_is_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_replace_becomes_changed_with_before ... ok
test native::capture::pomodoro_blocks::tests::pairing_uneven_replace_splits_changed_added_removed ... ok
test native::capture::pomodoro_blocks::tests::resolution_rejects_a_non_entry_after - should panic ... ok
test native::capture::pomodoro_blocks::tests::forwarding_panics_when_a_tracked_headline_is_deleted - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_forwards_a_tracked_block_across_an_insert_above ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_overnight_wrap_is_not_overdue ... ok
test native::capture::pomodoro_blocks::tests::vanished_entry_is_dropped_silently - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_resolves_created_before_and_reports_roles_once ... ok
test native::capture::blocked_tasks::tests::always_mints_when_blocks_lines_is_off ... ok
test native::capture::pomodoro_blocks::tests::unreported_headline_rewrite_emits_unchanged_block - should panic ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_start_later_than_now ... ok
test native::capture::pomodoro_blocks::tests::tracker_reports_one_cumulative_block_across_items ... ok
test native::capture::pomodoro_blocks::tests::tracker_autodetects_an_unreported_child_insert ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_exactly_at_end ... ok
test native::capture::project_deps::tests::flatten_block_links_uses_plain_alias_or_target_text ... ok
test native::capture::project_deps::tests::descendant_notes_are_internal_prj_targets ... ok
test native::capture::project_deps::tests::prj_gate_matches_only_recognised_projects ... ok
test native::capture::project_deps::tests::kept_notes_text_strips_tags_fields_and_ids ... ok
test native::capture::link_guard::tests::inherited_reason_blocks_pull_forward ... ok
test native::capture::inbox_route::tests::ir_nested_status_uses_root_and_idless_tasks_get_stable_keys ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_mid_session ... ok
test native::capture::project_deps::tests::resident_block_flips_tags_and_skips_prj_and_closed ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_past_the_end ... ok
test native::capture::pomodoro_start::tests::previous_session_overdue_unparsable_range ... ok
test native::capture::link_guard::tests::ordinary_unblocked_target_skips_the_vault_graph ... ok
test native::capture::project_deps::tests::resident_after_prj_before_fence_is_not_hidden_by_stale_fence_range ... ok
test native::capture::project_deps::tests::resident_block_edits_idless_rows_and_rechecks_shifted_fences ... ok
test native::capture::project_deps::tests::strongest_lane_ignores_closed_and_outsiders ... ok
test native::capture::tests::assembly::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::task_blocks::tests::block_range_maps_byte_end_to_line_range ... ok
test native::capture::tests::assembly::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::inbox_route::tests::ir_route_refusal_blames_the_failing_second_member ... ok
test native::capture::tests::assembly::completed_multiword_reuse_keeps_spelling ... ok
test native::capture::tests::assembly::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::assembly::exact_name_literal_never_prefix_matches ... ok
test native::capture::link_guard::tests::capture_into_unblocked_project_skips_the_vault_graph ... ok
test native::capture::link_guard::tests::tagged_destination_blocks_a_new_task ... ok
test native::capture::project_deps::tests::removed_refs_and_consumed_lines_use_the_items_pre_state_coordinates ... ok
test native::capture::tests::assembly::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::tests::assembly::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembly::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::task_blocks::tests::toggle_plus_subbullet_shows_the_task_line_as_changed ... ok
test native::capture::tests::assembly::formats_task_line ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::assembly::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::tests::assembly::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::link_guard::tests::unblocked_project_resident_skips_the_vault_graph ... ok
test native::capture::tests::assembly::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::assembly::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::assembly::exact_name_literal_creates_exact_spelling ... ok
test native::capture::tests::assembly::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::assembly::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::assembly::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::assembly::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::assembly::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::link_guard::tests::tagged_project_resident_forces_the_vault_graph ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::assembly::sub_bullet_insertion_keeps_dependency_lines_first ... ok
test native::capture::tests::assembly::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::dependency_drop::tests::duplicate_or_malformed_managed_lines_refuse_without_staging ... ok
test native::capture::tests::assembly::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::commit::refuses_when_absent_target_appears_before_commit ... ok
test native::capture::tests::commit::refuses_when_existing_target_deleted_before_commit ... ok
test native::capture::link_guard::tests::tagged_prj_forces_the_vault_graph ... ok
test native::capture::tests::assembly::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::assembly::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::grammar::extracts_escaped_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::assembly::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::assembly::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::grammar::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::grammar::extracts_retired_priority_tokens_from_the_terminal_region ... ok
test native::capture::tests::grammar::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::tests::grammar::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::assembly::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::grammar::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::grammar::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::grammar::normalizes_whitespace ... ok
test native::capture::tests::grammar::parses_priority_tokens ... ok
test native::capture::tests::grammar::parses_retired_priority_tokens ... ok
test native::capture::tests::grammar::parses_schedule_tokens ... ok
test native::capture::project_deps::tests::consumption_resolves_alias_basename_path_case_and_local_links_by_identity ... ok
test native::capture::tests::grammar::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::grammar::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::grammar::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::grammar::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::grammar::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::placement::article_prefix_prefers_raw_number_in_document_order ... ok
test native::capture::tests::placement::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::placement::article_exact_section_matches_stale_number ... ok
test native::capture::tests::placement::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::grammar::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::placement::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::grammar::parses_picker_task_refs_strictly ... ok
test native::capture::tests::placement::article_prefix_matches_de_numbered_identity ... ok
test native::capture::tests::placement::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::placement::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::tests::placement::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::placement::bare_bullet_marker_skips_generated_status_group ... ok
test native::capture::tests::placement::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::grammar::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::inbox_route::tests::ir_identical_idless_roots_route_together_with_exact_landings ... ok
test native::capture::tests::placement::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::grammar::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::grammar::clip_markers_are_terminal_forgiving_and_can_be_disabled ... ok
test native::capture::tests::grammar::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::dependencies::tests::prefiltered_snapshot_matches_full_read ... ok
test native::capture::tests::grammar::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::grammar::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::placement::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::placement::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::placement::article_exact_raw_title_match_precedes_earlier_identity_match ... ok
test native::capture::tests::placement::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::placement::article_exact_section_matches_plain_identity ... ok
test native::capture::tests::placement::article_exact_section_matches_de_numbered_identity ... ok
test native::capture::tests::placement::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::placement::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::placement::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::placement::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::placement::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::placement::formats_bullet_line ... ok
test native::capture::tests::placement::forced_route_rejects_terminal_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::placement::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::placement::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::placement::generated_group_prefix_without_authored_match_falls_back ... ok
test native::capture::tests::placement::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::placement::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::placement::inserts_after_single_top_level_task ... ok
test native::capture::dependency_drop::tests::partial_drop_keeps_verbatim_history_and_unresolved_links_and_field_ids ... ok
test native::capture::tests::placement::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::placement::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::forced_section_does_not_target_generated_blocked_group ... ok
test native::capture::tests::placement::formats_scheduled_date_from_offset ... ok
test native::capture::tests::placement::formats_sub_bullet_line ... ok
test native::capture::tests::placement::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::placement::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::placement::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::placement::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::placement::marker_only_bullet_input_is_usage_error ... ok
test native::capture::dependency_drop::tests::last_dependency_line_and_field_are_removed_with_crlf_and_final_newline_preserved ... ok
test native::capture::tests::placement::json_success_shape_is_stable ... ok
test native::capture::tests::placement::non_article_numbered_heading_keeps_raw_title_matching ... ok
test native::capture::tests::placement::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::placement::legacy_standalone_bullet_markers_are_rejected ... ok
test native::capture::blocked_tasks::tests::nested_dependent_path_is_addressed_by_relative_and_block_id ... ok
test native::capture::tests::placement::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::placement::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::placement::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::placement::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::placement::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::placement::prefix_skips_generated_blocked_group_for_authored_match ... ok
test native::capture::tests::placement::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::started::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::placement::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::started::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::placement::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::tests::started::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::started::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started::started_pomodoro_move_preserves_crlf ... ok
test native::capture::tests::started::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::blocked_tasks::tests::relocate_by_id_after_id_stamp_and_lane_promotion ... ok
test native::capture::tests::started::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::started::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::started::non_tasks_section_headings_skip_generated_status_groups ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture::tests::commit::refuses_when_second_note_edited_externally ... ok
test native::capture::tests::started::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_block_ids::tests::successor_mints_follow_the_pinned_vectors ... ok
test native::capture_completable_tasks::tests::guard_reasons_match_the_contract ... ok
test native::capture_block_ids::tests::suggestions_follow_the_pinned_examples ... ok
test native::capture_block_ids::tests::allowed_regex_agrees_with_validator_for_every_ascii_char ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_clip::tests::formats_headers ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_block_ids::tests::used_covers_done_nontask_duplicates_and_document_order ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture::task_blocks::tests::created_parent_reports_every_row_added ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture::blocked_tasks::tests::existing_owner_is_uncapped_at_in_progress ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_complete::tests::output::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::output::empty_json_context_is_null ... ok
test native::capture_complete::tests::output::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::output::json_shape_is_stable ... ok
test native::capture::task_blocks::tests::nested_parent_reports_depths_relative_to_its_line ... ok
test native::capture_complete::tests::output::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_rotten_log ... ok
test native::capture_complete::tests::output::trailing_hash_fragment_requests_no_completion ... ok
test native::capture_complete::tests::output::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_completable_tasks::tests::draft_selected_marks_only_other_items ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_completable_tasks::tests::recurring_today_rows_sink_below_visible_rows_in_the_same_entry ... ok
test native::capture_complete::tests::output::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::output::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_complete::tests::active_tasks::active_task_human_rows_name_the_queue ... ok
test native::capture::task_blocks::tests::global_batch_reports_one_block_with_two_added_rows ... ok
test native::capture_complete::tests::pomodoros::plan_themes_after_counts_only_fresh_non_exempt_components ... ok
test native::capture::task_blocks::tests::two_parents_forward_across_an_insert_above ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_candidates_omit_next_up ... ok
test native::capture_complete::tests::pomodoros::bare_start_name_replacements_prefix_hash_when_the_slug_cannot_be_bare ... ok
test native::capture_completable_tasks::tests::open_tasks_list_with_locators_scheduled_and_suggestions ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_complete::tests::output::close_items_and_suffixes_request_no_completion ... ok
test native::capture_complete::tests::pomodoros::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_excludes_ready_tasks ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_today_before_creation_and_utilities ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture::task_blocks::tests::authored_children_and_schedule_log_are_added_in_order ... ok
test native::capture_completable_tasks::tests::hidden_and_recurring_sink_within_their_section ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture::task_blocks::tests::cross_note_first_touch_order_with_revisit_and_second_parent ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_suppresses_creation_only_for_exact_open_names ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_completable_tasks::tests::struck_fenced_and_depends_on_links_never_place ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_orders_repeated_completed_names_newest_first ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_human_labels_cover_every_row_kind ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_matches_pomodoro_name_warnings ... ok
test native::capture_complete::tests::parent_tasks::scoped_missing_and_empty_notes_keep_picker_and_empty_catalog ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_filters_and_creates_by_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_lists_start_again_and_name_it_rows ... ok
test native::capture_complete::tests::blocked_tasks::blocked_task_shell_rows_use_the_blocked_tasks_group ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_puts_the_running_entry_last ... ok
test native::capture_completable_tasks::tests::empty_query_orders_today_first_then_status ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_again_rows_preview_plan_budget ... ok
test native::capture_completable_tasks::tests::missing_day_file_means_no_today_rows ... ok
test native::capture_complete::tests::parent_tasks::leading_plus_query_refetch_keeps_token_range_and_full_catalog ... ok
test native::capture_complete::tests::parent_tasks::bare_plus_serves_vault_candidates_and_operator_hints ... ok
test native::capture_complete::tests::parent_tasks::vault_catalog_excludes_non_capture_and_terminal_notes ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_completable_tasks::tests::today_roles_precedence_sessions_and_pomodoro ... ok
test native::capture_complete::tests::routes_tasks::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::routes_tasks::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::routes_tasks::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::routes_tasks::default_task_completion_stays_identified_only ... ok
test native::capture_complete::tests::routes_tasks::template_header_offered_only_on_first_nonblank_line ... ok
test native::capture_complete::tests::routes_tasks::template_completion_suppresses_header_rows_and_placeholders ... ok
test native::capture_complete::tests::routes_tasks::template_header_completion_is_offered_first_for_prefix_and_last_for_empty_query ... ok
test native::capture_complete::tests::parent_tasks::unicode_duplicates_and_queued_pomodoros_stay_in_catalog ... ok
test native::capture_complete::tests::task_links::task_link_completion_lists_worked_example_in_canonical_order ... ok
test native::capture_complete::tests::task_links::task_link_completion_keeps_candidates_when_the_day_file_is_missing ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_does_not_change_pomodoro_completion ... ok
test native::capture_dependency_tasks::tests::hidden_tasks_detect_only_the_exact_tag ... ok
test native::capture_complete::tests::task_links::task_link_completion_scopes_to_the_batch_second_item ... ok
test native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_dependency_tasks::tests::quoted_locator_round_trips_through_replacement ... ok
test native::capture_flag_guard::tests::declared_flags_values_and_text_pass_through ... ok
test native::capture_complete::tests::routes_tasks::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_complete::tests::task_links::task_link_completion_pins_json_shape_and_omissions ... ok
test native::capture_flag_guard::tests::equals_only_short_combined_with_declared_option_then_unknown_is_rejected ... ok
test native::capture_complete::tests::task_links::task_link_human_rows_name_queues_and_missing_ids ... ok
test native::capture_flag_guard::tests::mixed_short_cluster_then_unknown_long_is_rejected ... ok
test native::capture_flag_guard::tests::short_format_json_with_unknown_flag_reports_json ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_warns_once_for_an_unresolvable_parent ... ok
test native::capture_flag_guard::tests::guard_specs_match_clap_declarations ... ok
test native::capture_flag_guard::tests::undeclared_short_cluster_is_text ... ok
test native::capture_flag_guard::tests::text_starting_with_a_flag_word_needs_the_delimiter ... ok
test native::capture_flag_guard::tests::unknown_long_flag_before_text_is_rejected ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_lists_ranked_slugs_for_the_parent_task ... ok
test native::capture_complete::tests::relations::parent_picker_reports_typed_relation_direction_and_target_text ... ok
test native::capture_flag_guard::tests::value_taking_short_with_attached_cluster_rest_is_the_value ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_language::bare_name::tests::bare_name_len_matches_letter_led_non_close_shapes ... ok
test native::capture_language::bare_name::tests::can_spell_bare_rejects_digit_led_and_close_shapes ... ok
test native::capture_language::bare_name::tests::composed_tokens_keep_hash_when_the_name_cannot_be_bare ... ok
test native::capture_language::close_log::tests::first_bullet_kind_detection_skips_placeholders ... ok
test native::capture_language::close_log::tests::assign_log_positions_follows_the_assignment_rule ... ok
test native::capture_language::close_log::tests::inline_entry_defaults_and_leading_numbers ... ok
test native::capture_language::close_log::tests::inline_entry_reports_dangling ... ok
test native::capture_language::close_log::tests::default_log_index_covers_every_close_shape ... ok
test native::capture_language::close_log::tests::mixed_numbering_fails_both_orders ... ok
test native::capture_language::close_log::tests::inline_entry_reports_diagnostics_in_order ... ok
test native::capture_language::close_log::tests::lexes_entries_and_details ... ok
test native::capture_language::close_log::tests::positional_entries_carry_their_typed_position ... ok
test native::capture_language::close_log::tests::reports_dangling ... ok
test native::capture_complete::tests::task_links::task_link_completion_queries_cover_the_sigil_and_rank ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_report_lexical_failures ... ok
test native::capture_dependency_tasks::tests::unique_basename_resolves_before_ambiguous_paths ... ok
test native::capture_language::close_log::tests::rejects_bad_bullets ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_stay_unresolved_without_a_selection ... ok
test native::capture_dependency_tasks::tests::catalog_covers_every_task_bearing_note_kind ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_positionally_in_selection_mode ... ok
test native::capture_dependency_tasks::tests::groups_follow_the_picker_sections ... ok
test native::capture_language::close_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::close_selection::tests::lex_reports_park_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_drop_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_dependency_tasks::tests::ranking_shares_the_tiered_matcher_vectors ... ok
test native::capture_language::close_selection::tests::lex_reports_valid_selections ... ok
test native::capture_language::close_selection::tests::retired_whole_item_spellings_name_their_bare_rewrite ... ok
test native::capture_language::close_selection::tests::selection_shape_detection ... ok
test native::capture_language::close_selection::tests::lex_reports_trailing_at_selections ... ok
test native::capture_dependency_tasks::tests::empty_query_orders_same_note_lanes_history ... ok
test native::capture_language::dependencies::tests::bare_sigil_is_directive_only_at_the_ends ... ok
test native::capture_language::close_selection::tests::lex_reports_wildcard_groups ... ok
test native::capture_language::dependencies::tests::escape_consumes_only_its_backslash ... ok
test native::capture_language::dependencies::tests::protected_spans_are_never_modifiers ... ok
test native::capture_language::dependencies::tests::mid_line_modifiers_stay_literal ... ok
test native::capture_language::dependencies::tests::quoted_escapes_decode ... ok
test native::capture_language::dependencies::tests::blocked_task_modifiers_have_separate_entries_and_spans ... ok
test native::capture_language::dependencies::tests::escaped_star_unescapes_only_inside_a_modifier_run ... ok
test native::capture_language::dependencies::tests::star_markdown_and_mid_line_tokens_stay_literal ... ok
test native::capture_language::dependencies::tests::trailing_complete_modifier_strips_and_spans ... ok
test native::capture_language::dependencies::tests::traversal_and_bad_ids_are_invalid ... ok
test native::capture_language::dependencies::tests::quoted_note_with_spaces_stays_atomic ... ok
test native::capture_language::dependencies::tests::unicode_offsets_stay_on_char_boundaries ... ok
test native::capture_language::dependencies::tests::unterminated_quote_is_one_partial ... ok
test native::capture_language::pomodoro_literal::tests::lex_decodes_only_quote_and_backslash_escapes ... ok
test native::capture_language::pomodoro_literal::tests::expand_covers_spaced_literals ... ok
test native::capture_language::pomodoro_literal::tests::lex_rejects_non_quote_openers ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_straight_and_curly_literals ... ok
test native::capture_language::pomodoro_literal::tests::lex_reports_unterminated_as_incomplete ... ok
test native::capture_language::project_tasks::tests::lexer_accepts_the_boundary_set ... ok
test native::capture_language::project_tasks::tests::reserved_name_matches_in_any_letter_case ... ok
test native::capture_language::project_tasks::tests::suffix_helpers_split_on_the_last_word ... ok
test native::capture_language::start_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::start_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::start_selection::tests::lex_reports_valid_drop_lists ... ok
test native::capture_language::tests::bare_close::bare_close_classifier_claims_only_the_documented_shapes ... ok
test native::capture_language::tests::bare_close::bare_close_spans_cover_the_one_byte_x_and_each_list ... ok
test native::capture_language::tests::bare_close::bare_close_suppresses_marker_completion_in_work_log_text ... ok
test native::capture_language::tests::chain::chain_token_predicate_covers_the_documented_table ... ok
test native::capture_complete::tests::relations::relation_label_completions_carry_relation_and_owner ... ok
test native::capture_language::tests::chain::bang_claim_beats_dependency_errors ... ok
test native::capture_language::tests::chain::draft_chain_works_with_a_global_declaration ... ok
test native::capture_language::tests::chain::bang_items_claim_each_blank_line_block_independently ... ok
test native::capture_language::tests::chain::draft_keeps_sequential_indices_across_crlf_with_a_chain ... ok
test native::capture_language::tests::chain::draft_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::completion_requests_nothing_anywhere_on_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_a_two_token_chain_with_absolute_ranges ... ok
test native::capture_language::tests::chain::draft_splits_tabs_and_runs_of_spaces ... ok
test native::capture_language::tests::chain::chain_token_predicate_equals_claimed_for_single_tokens ... ok
test native::capture_language::tests::bare_close::bare_close_heads_session_chains_and_inline_trails ... ok
test native::capture_language::tests::chain::editor_chain_items_do_not_inherit_a_global_declaration ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_chain_with_absolute_spans ... ok
test native::capture_language::tests::chain::editor_reports_a_broken_second_token_with_its_own_diagnostic ... ok
test native::capture_language::tests::chain::editor_reports_a_dangling_close_separator_inside_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_retired_double_tokens_and_reports_their_own_ranges ... ok
test native::capture_language::tests::chain::editor_reports_an_incomplete_named_start_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_plus_adjustment_chain ... ok
test native::capture_language::tests::chain::editor_reports_selection_spans_at_absolute_offsets_in_a_chain ... ok
test native::capture_language::tests::bare_close::bare_close_selection_shapes_report_the_same_close_everywhere ... ok
test native::capture_language::tests::chain::execution_carries_a_close_selection_through_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_two_items_with_absolute_spans_for_a_chain ... ok
test native::capture_language::tests::bare_close::prose_and_uppercase_x_remain_tasks ... ok
test native::capture_language::tests::chain::execution_reports_a_broken_second_token_on_its_own_range ... ok
test native::capture_language::tests::chain::execution_runs_a_chain_left_to_right ... ok
test native::capture_language::tests::chain::execution_distinguishes_spaced_start_adjust_from_offset_start ... ok
test native::capture_language::tests::chain::execution_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::execution_leaves_non_chains_unchanged ... ok
test native::capture_language::tests::chain::execution_rejects_forced_destinations_on_the_first_chain_token ... ok
test native::capture_language::tests::chain::execution_switches_sessions_with_close_then_start ... ok
test native::capture_language::tests::completion::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion::caret_suffix_names_preserve_the_link_part_for_completion ... ok
test native::capture_language::tests::completion::completion_on_a_global_declaration_excludes_both_sigils_and_plus ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_language::tests::completion::block_id_project_note_sigil_is_excluded_from_replacement ... ok
test native::capture_language::tests::completion::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::completion::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::completion::empty_block_id_with_section_still_yields_a_task_section_field ... ok
test native::capture_language::tests::completion::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion::empty_selector_after_hash_is_a_zero_length_task_section_field ... ok
test native::capture_language::tests::completion::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::completion::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::completion::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_language::tests::completion::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::completion::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::completion::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::completion::hash_separator_is_not_part_of_block_id_or_section_replacement ... ok
test native::capture_language::tests::completion::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::completion::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::completion::parent_task_plus_is_shared_across_parent_and_authored_lines ... ok
test native::capture_language::tests::completion::operator_items_have_no_hash_completion ... ok
test native::capture_language::tests::completion::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::parent_task_plus_completes_the_terminal_token_with_utf8_byte_ranges ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_per_token_inside_chains ... ok
test native::capture_language::tests::completion::pomodoro_link_suffix_names_complete_without_replacing_the_link_start ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_a_bare_name_with_the_bare_flag ... ok
test native::capture_language::tests::completion::parent_task_plus_preserves_operator_and_protected_text_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_start_name_context_reports_ledger_behavior ... ok
test native::capture_language::tests::completion::pomodoro_start_name_leaves_link_form_names_alone ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_after_hash_on_a_named_start ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_lone_colon ... ok
test native::capture_language::tests::completion::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_caret_id ... ok
test native::capture_language::tests::completion::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::completion::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_language::tests::completion::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::retired_doubled_start_has_no_name_completion_or_override_context ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_partial_id ... ok
test native::capture_language::tests::completion::task_section_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::completion::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::completion::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_only_first_level_project_bullets ... ok
test native::capture_language::tests::completion::project_task_id_before_a_child_line_route_marker_still_completes ... ok
test native::capture_language::tests::completion::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::completion::work_log_bullet_lines_request_no_marker_completion ... ok
test native::capture_language::tests::completion::task_link_query_completes_the_sigil_inclusive_token ... ok
test native::capture_language::tests::draft::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::completion::task_block_id_route_and_authored_id_both_complete ... ok
test native::capture_language::tests::draft::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::completion::trailing_hash_fragments_have_no_completion ... ok
test native::capture_language::tests::completion::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_language::tests::draft::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::draft::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::draft::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::draft::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::draft::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::draft::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::draft::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::draft::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::draft::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::draft::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::draft::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::draft::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::draft::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::draft::execution_refuses_retired_priority_markers ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::draft::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::draft::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::draft::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::draft::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::draft::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture::tests::commit::cumulative_stages_into_one_note_commit ... ok
test native::capture_language::tests::draft::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::draft::execution_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::draft::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::draft::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::draft::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::editor_modes::editor_holds_unused_pomodoro_while_a_colon_id_is_unfinished ... ok
test native::capture_language::tests::editor_modes::editor_rejects_checkbox_only_project_task_ids_over_the_id_token ... ok
test native::capture_language::tests::editor_modes::editor_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::draft::execution_treats_bare_dollar_as_priority_level_one ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_complete_modes_needs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_start_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_retired_doubled_start_forms_over_the_token ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_link_queries_as_incomplete ... ok
test native::capture_language::tests::editor_modes::editor_reports_named_pomodoro_start_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_modes::editor_reports_unused_project_note_pomodoro_over_the_name ... ok
test native::capture_language::tests::editor_modes::caret_close_conflicts_agree_with_execution ... ok
test native::articles::tests::mutation_idempotent_and_words ... ok
test native::capture_language::tests::editor_spans::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::editor_spans::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_language::tests::editor_spans::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_modes::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::editor_spans::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_spans::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_partial_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::editor_modes::editor_reports_project_task_ids_with_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::editor_spans::editor_reports_bare_dollar_as_a_priority_span ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_now_tag_without_task_text ... ok
test native::capture_language::tests::editor_spans::editor_reports_legacy_bullet_markers_without_failing ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_priority_markers ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_modes::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::editor_spans::editor_link_suffix_incomplete_states_keep_timing_and_placeholders ... ok
test native::capture_language::tests::editor_spans::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_spans::editor_spans_a_bare_named_start_without_a_hash_gap ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_task_complete_tokens ... ok
test native::capture_language::tests::editor_spans::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::editor_spans::editor_unescapes_terminal_priority_dollar_amounts ... ok
test native::capture_language::tests::editor_spans::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::editor_spans::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::editor_spans::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::editor_modes::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::editor_spans::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::task_link_query_spans_the_whole_token_as_a_placeholder ... ok
test native::capture_language::tests::exact_name::bare_name_spelling_never_takes_quotes ... ok
test native::capture_language::tests::editor_spans::editor_spans_pomodoro_link_names_after_the_equal_suffix ... ok
test native::capture_language::tests::editor_spans::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_spans::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::exact_name::close_hash_teaches_with_decoded_name ... ok
test native::capture_language::tests::exact_name::invalid_literal_names_error ... ok
test native::capture_language::tests::exact_name::exact_name_start_reports_canonical_name_and_literal_flag ... ok
test native::capture_language::tests::exact_name::exact_name_accepts_round_trip_fixtures ... ok
test native::capture_language::tests::editor_modes::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::exact_name::exact_name_link_reports_canonical_name ... ok
test native::capture_language::tests::globals::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::editor_spans::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::globals::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::globals::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::exact_name::partial_literal_completes_on_decoded_text ... ok
test native::capture_language::tests::exact_name::unterminated_literal_is_incomplete_never_a_mistake ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::capture_language::tests::globals::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::globals::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::exact_name::literal_spans_cover_the_quotes ... ok
test native::capture_language::tests::globals::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_sub_bullet_and_keeps_authored_children ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::globals::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::globals::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::globals::task_complete_items_skip_global_inheritance ... ok
test native::capture_language::tests::goto::goto_completion_field_reports_sigil_relative_queries ... ok
test native::capture_language::tests::globals::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::goto::goto_claim_covers_every_table_query_row ... ok
test native::capture_language::tests::globals::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::globals::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::grammar::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::globals::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::grammar::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::goto::goto_claim_leaves_prose_byte_identical ... ok
test native::capture_language::tests::grammar::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::grammar::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::grammar::colon_alias_owner_is_unchanged_beside_modifiers ... ok
test native::capture_language::tests::grammar::double_pipe_grammar_vectors ... ok
test native::capture_language::tests::grammar::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::grammar::bang_claim_covers_the_contract_table ... ok
test native::capture_language::tests::grammar::caret_alias_owns_relationships_in_leading_and_trailing_position ... ok
test native::capture_language::tests::grammar::execution_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::grammar::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::grammar::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::grammar::execution_keeps_task_id_lookalikes_literal_outside_project_notes ... ok
test native::capture_language::tests::grammar::execution_evaluates_project_note_markers_parents_and_children_in_order ... ok
test native::capture_language::tests::grammar::execution_keeps_other_trailing_hash_tags_rejected ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_accepts_project_task_ids_and_strips_them_from_bodies ... ok
test native::capture_language::tests::grammar::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_checkbox_only_project_task_ids ... ok
test native::capture_language::tests::grammar::execution_rejects_route_less_retired_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_teaches_bare_named_start_shape_in_the_typed_spelling ... ok
test native::capture_language::tests::grammar::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::grammar::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::grammar::execution_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::grammar::execution_retires_claimed_doubled_start_family ... ok
test native::capture_language::tests::grammar::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::grammar::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::grammar::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::grammar::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::grammar::execution_parses_equals_family_starts_alongside_close ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::grammar::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::grammar::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::grammar::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::grammar::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::grammar::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::grammar::plus_parent_picker_does_not_claim_operators_or_work_log_text ... ok
test native::capture_language::tests::grammar::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::grammar::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::grammar::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::grammar::plus_parent_picker_is_incomplete_but_keeps_the_lone_adjustment ... ok
test native::capture_language::tests::grammar::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::grammar::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_complete::tests::relations::relation_target_contexts_use_directional_markers_and_owner_links ... ok
test native::capture_language::tests::grammar::execution_rejects_project_task_id_rule_violations_verbatim ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_shared_timing_validation_matches_standalone ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffixes_teach_about_drops_duplicate_names_and_glued_timing ... ok
test native::capture_language::tests::ref_grammar::bare_url_claims_reference_item_when_routing_is_on ... ok
test native::capture_language::tests::grammar::task_link_query_leaves_prose_byte_identical ... ok
test native::capture_language::tests::ref_grammar::editor_ref_route_spans_use_byte_offsets_including_utf8 ... ok
test native::capture_language::tests::grammar::task_link_query_rejects_single_colon_tokens_with_teaching_errors ... ok
test native::capture_language::tests::grammar::plus_selector_beside_modifiers_needs_task_parent ... ok
test native::capture_language::tests::grammar::suffixed_owners_keep_must_be_bare_refusals ... ok
test native::capture_language::tests::grammar::execution_treats_bare_named_starts_as_hash_equivalents ... ok
test native::capture_language::tests::ref_grammar::editor_url_list_items_each_report_ref ... ok
test native::capture_language::tests::ref_grammar::editor_reports_ref_mode_with_one_exact_span ... ok
test native::capture_language::tests::ref_grammar::routing_off_keeps_bare_url_a_task ... ok
test native::capture_language::tests::ref_grammar::mixed_list_classifies_each_line_on_its_own ... ok
test native::capture_language::tests::grammar::pomodoro_link_suffix_names_match_the_existing_hash_spelling ... ok
test native::capture_language::tests::grammar::relationship_only_owner_refuses_text_extras ... ok
test native::capture_language::tests::ref_grammar::excluded_hosts_stay_tasks ... ok
test native::capture_language::tests::ref_grammar::forced_destination_global_and_clip_keep_tasks ... ok
test native::capture_language::tests::ref_grammar::url_list_split_handles_crlf_with_exact_ranges ... ok
test native::capture_language::tests::ref_grammar::ref_parent_sources_cover_explicit_global_and_default ... ok
test native::capture_language::tests::ref_grammar::url_list_requires_every_line ... ok
test native::capture_language::tests::retired_close::double_equals_close_lookalikes_teach_the_bare_spelling ... ok
test native::capture_language::tests::retired_close::retired_closes_inside_chains_fail_on_their_own_range ... ok
test native::capture_language::tests::grammar::task_link_claim_is_equivalent_across_execution_editor_and_completion ... ok
test native::capture_language::tests::retired_close::retired_closes_with_an_inline_entry_name_the_whole_rewritten_line ... ok
test native::capture_language::tests::ref_grammar::url_list_block_splits_into_one_item_per_line ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::retired_close::retired_closes_stay_distinct_from_prose_lookalikes ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_requires_a_cursor ... ok
test native::capture_language::tests::ref_grammar::claim_off_cases_stay_tasks ... ok
test native::capture_language::tests::editor_modes::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::retired_close::retired_whole_item_closes_fail_with_the_bare_rewrite_in_both_parsers ... ok
test native::capture_language::tests::retired_close::retired_link_close_aliases_fail_with_the_x_rewrite ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_sub_bullet_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_leaves_template_drafts_untouched ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attach_relation_label_exclusions ... ok
test native::capture_language::tests::rewrite::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::rewrite::rewrite_draft_attaches_a_pipe_after_a_relation_token ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_child_line_trailing_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_alternates ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_keeps_absorption_when_it_does_not_claim ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_before_a_schedule_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_caret_marker_to_colon ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_a_trailing_colon_marker_to_caret ... ok
test native::capture_language::tests::rewrite::rewrite_draft_starts_a_template_at_the_first_line ... ok
test native::capture_language::tests::rewrite::rewrite_draft_starts_a_template_reusing_crlf ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_requires_a_cursor ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_beside_emoji_and_preserves_crlf ... ok
test native::capture_language::tests::ref_grammar::standalone_percent_and_at_listen_markers_request_companion_audio ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_one_item_in_a_batch ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_parses_as_the_switched_mode ... ok
test native::capture_language::tests::template::a_template_needs_a_blank_separator_before_rows ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_uppercase_and_hyphenated_ids ... ok
test native::capture_language::tests::rewrite::rewrite_draft_template_start_requires_the_exact_typing_gesture ... ok
test native::capture_language::tests::template::definition_validation_ignores_rows_but_checks_placeholders_without_rows ... ok
test native::capture_language::tests::template::missing_placeholder_is_suppressed_until_rows_exist ... ok
test native::capture_language::tests::template::expansion_matches_the_plan_example_byte_for_byte ... ok
test native::capture_language::tests::rewrite::rewrite_draft_separator_toggle_exclusions ... ok
test native::capture_language::tests::template::missing_template_or_rows_has_a_teaching_issue ... ok
test native::capture_language::tests::template::multi_placeholder_extra_values_still_report_arity ... ok
test native::capture_language::tests::template::non_template_expansion_is_an_identity ... ok
test native::capture_language::tests::rewrite::rewrite_draft_switches_solo_and_leading_markers ... ok
test native::capture_language::tests::template::one_placeholder_global_declaration_names_containing_row ... ok
test native::capture_language::tests::rewrite::rewrite_draft_template_start_is_idempotent ... ok
test native::capture_language::tests::template::one_placeholder_rows_share_line_with_per_value_ranges ... ok
test native::capture_language::tests::template::one_placeholder_mixed_lines_number_left_to_right_then_top_to_bottom ... ok
test native::capture_language::tests::template::one_placeholder_one_line_equals_three_line_expansion ... ok
test native::capture_language::tests::template::one_placeholder_tabs_and_repeated_spaces_split_cleanly ... ok
test native::capture_language::tests::template::one_field_rows_split_on_spaces_and_template_line_endings_normalize ... ok
test native::capture_language::tests::template::one_placeholder_templates_never_report_arity ... ok
test native::capture_language::tests::template::one_placeholder_unterminated_quote_names_value_row_and_keeps_leading_row ... ok
test native::capture_language::tests::template::placeholder_gaps_and_one_based_indices_are_explained ... ok
test native::capture_language::tests::template::placeholders_repeat_reorder_escape_and_expand_inside_markers ... ok
test native::capture_language::tests::template::quote_errors_and_arity_errors_are_row_scoped ... ok
test native::capture_language::tests::template::placeholder_grammar_rejects_noncanonical_and_incomplete_braces ... ok
test native::capture_language::tests::template::row_global_declarations_use_row_scope ... ok
test native::capture_language::tests::template::rows_cannot_be_bullets_and_templates_cannot_use_other_globals ... ok
test native::capture_language::tests::template::row_lexer_handles_quotes_escapes_and_plain_quotes ... ok
test native::capture_language::tests::template::template_header_accepts_case_and_ascii_padding_and_skips_blank_lines ... ok
test native::capture_language::tests::template::template_header_reports_misplaced_inline_repeated_and_option_like_forms ... ok
test native::capture_language::tests::grammar::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_link_tasks::tests::ranker_orders_by_tier_sum_then_canonical_order ... ok
test native::capture_language::tests::template::template_mask_preserves_byte_offsets_and_hides_header_rows_and_braces ... ok
test native::capture_link_tasks::tests::ranker_passes_the_dependency_contract_dk_vectors ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_link_tasks::tests::pulls_forward_only_for_a_single_future_scheduled_field ... ok
test native::capture_link_tasks::tests::suggestions_avoid_used_ids_including_non_task_anchors ... ok
test native::capture_link_tasks::tests::excludes_closed_unknown_terminal_untyped_and_unroutable ... ok
test native::capture_parse::tests::format_pomodoro_close_describes_wildcard_scope ... ok
test native::capture_link_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_link_tasks::tests::ranker_matches_the_worked_example_queries ... ok
test native::capture_link_tasks::tests::warns_when_the_day_file_is_missing_but_lists_tasks ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_language::tests::template::one_placeholder_thousand_and_first_value_is_too_large ... ok
test native::capture_language::tests::ref_grammar::claim_accepts_wrapper_case_and_hints ... ok
test native::capture::tests::commit::commits_matching_multi_file_preimage ... ok
test native::capture_link_tasks::tests::worked_example_lists_eight_rows_in_canonical_order ... ok
test native::capture_parse::tests::format_pomodoro_close_reports_detail_counts ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_parse::tests::json_reports_invalid_start_suffixes_as_diagnostics ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_a_global_sub_bullet_declaration_and_local_override ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_retired_doubled_starts_with_token_ranges ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_parse::tests::json_reports_named_pomodoro_starts ... ok
test native::capture_pomodoro_close::ledger::managed_dependency_tests::dependency_lines_are_notes_not_close_targets ... ok
test native::capture_parse::tests::json_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_pomodoro_close::linked_task_tests::custom_in_progress_symbol_gets_no_listed_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_pomodoro_close::linked_task_tests::listed_duplicate_embedded_and_plain_warns_once_for_not_completed ... ok
test native::capture_pomodoro_close::linked_task_tests::closing_a_dependent_leaves_depends_on_prerequisites_open ... ok
test native::capture_pomodoro_close::linked_task_tests::same_task_numbered_twice_carries_lowest_number ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_pomodoro_close::linked_task_tests::mentioned_first_bare_link_gets_number_and_blocked_warning ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_complete_writes_done_task_with_completion_date ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_in_progress_and_complete_updates_both_tasks ... ok
test native::capture_complete::tests::output::bare_start_name_completion_prefixes_hash_for_digit_led_matches ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_complete::tests::output::close_bullet_lines_suppress_wikilink_block_but_keep_note ... ok
test native::capture_pomodoro_close::selection_tests::conflicting_duplicates_fail_and_same_outcome_passes ... ok
test native::capture_pomodoro_close::selection_tests::fenced_links_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::embedded_hash_alias_and_tomato ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_listed_row_warns_exactly_once ... ok
test native::capture_pomodoro_close::selection_tests::drop_removes_from_closed_session_without_carry ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_typed_target_warns_and_stays_in_pomodoro ... ok
test native::capture_pomodoro_close::selection_tests::apply_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_pomodoro_close::selection_tests::log_entries_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::lexically_resolved_positional_entry_reports_nested_wording ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_appends_after_existing_descendants ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_child_indent_follows_first_child_or_link_indent ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_align_with_typed_entries ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_preserve_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_text_that_numbers_a_link_fails_loudly ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::managed_dependency_lines_are_not_numbered_for_close_or_agenda ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_errors ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_nest_one_level_under_the_entry ... ok
test native::capture_pomodoro_close::selection_tests::nested_bare_links_are_numbered ... ok
test native::capture_pomodoro_close::selection_tests::mixed_lines_are_unnumbered ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_on_complete_target_land_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::numbers_the_worked_example ... ok
test native::capture_pomodoro_close::selection_tests::listed_blocked_and_done_warnings ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_with_one_and_zero_links ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_dated_work_logs ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_nest_undated_in_task_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_on_complete_target_lands_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::outcome_table_covers_every_row ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_skip_nested_links ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_resolve_against_session_worked_links ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_share_a_single_worked_link ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_messages ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_lands_in_task_work_log_as_typed_subset ... ok
test native::capture_pomodoro_close::selection_tests::none_is_byte_identical_to_plan_ledger_close ... ok
test native::capture_pomodoro_close::selection_tests::rewrite_keeps_prefix_and_drops_tomato ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_follow_drop_and_complete_outcomes ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_accepts_an_empty_lineup_but_explicit_positive_indices_do_not ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_positional_logs_wait_for_and_use_top_level_worked_lineup ... ok
test native::capture_pomodoro_close::selection_tests::parked_links_record_work_but_are_not_carried ... ok
test native::capture_pomodoro_close::selection_tests::positional_resolution_reports_session_failures ... ok
test native::capture_pomodoro_close::selection_tests::full_close_reports_numbered_lineup_with_none ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_outcomes_cover_remaining_numbered_links_and_keep_exceptions ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x2 ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x_complete ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x1_complete_2 ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture_active_tasks::tests::excludes_ready_tasks_even_with_now_text ... ok
test native::capture_complete::tests::routes_tasks::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x0_and_x1_2 ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_pomodoro_start::drop_tests::drops_nested_links_with_their_parent ... ok
test native::capture_pomodoro_start::drop_tests::drops_numbered_subtree_and_keeps_gaps ... ok
test native::capture_pomodoro_start::drop_tests::created_session_reports_the_new_session_variant ... ok
test native::capture_complete::tests::parent_tasks::plus_query_ranks_candidates_and_scoped_descriptors_keep_exact_ranges ... ok
test native::capture_pomodoro_start::drop_tests::empty_drop_is_byte_identical ... ok
test native::capture_complete::tests::routes_tasks::route_completion_matches_aliases_with_canonical_replacement_after_prefix ... ok
test native::capture_pomodoro_start::drop_tests::dropped_last_line_without_final_newline_leaves_none ... ok
test native::capture_pomodoro_start::drop_tests::fenced_lines_are_not_numbered ... ok
test native::capture_pomodoro_start::drop_tests::duplicate_still_queued_warns ... ok
test native::capture_complete::tests::routes_tasks::task_completion_before_an_explicit_toggle_bang_does_not_replace_the_bang ... ok
test native::capture_complete::tests::routes_tasks::task_block_id_completion_offers_routes_but_not_authored_ids ... ok
test native::capture_pomodoro_start::drop_tests::preserves_crlf ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_lists_identified_tasks_before_unidentified_tasks ... ok
test native::capture_pomodoro_start::drop_tests::drops_embedded_and_unresolved_rows_by_number ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture::task_blocks::tests::task_ref_parent_omits_block_id_but_reports_its_block ... ok
test native::capture_pomodoro_start::drop_tests::empty_lineup_suggests_the_token_without_its_drop ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_pomodoro_start::drop_tests::out_of_range_names_every_bad_number ... ok
test native::capture_pomodoro_start::drop_tests::dropped_middle_line_without_final_newline_keeps_structure ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_pomodoro_start::drop_tests::three_bad_numbers_join_with_commas ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_complete::tests::relations::relation_label_leading_and_dependency_tail_keep_narrow_ranges ... ok
test native::capture_pomodoro_start::lineup_tests::lists_direct_children_in_ledger_order ... ok
test native::capture_completable_tasks::tests::bang_replacement_quotes_reserved_locators ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_empty_block_id_is_an_empty_success ... ok
test native::capture_pomodoro_start::lineup_tests::managed_dependency_lines_are_not_start_lineup_items ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_search_keeps_identified_groups_ahead_of_unidentified ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_matches_wrapper_across_sessions ... ok
test native::capture_pomodoro_start::lineup_tests::skips_deeper_descendants_embeds_and_struck_lines ... ok
test native::capture_pomodoro_start::lineup_tests::skips_fenced_lines ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoro_start::lineup_tests::resolves_rows_through_the_staged_view ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_pomodoro_start::lineup_tests::prepared_scan_preserves_crlf_line_numbers ... ok
test native::capture_pomodoros::tests::completed_summary_prefers_recorded_duration ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_complete::tests::routes_tasks::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_completable_tasks::tests::nonempty_query_keeps_today_matches_on_top ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_complete::tests::relations::relation_target_replacement_stops_before_an_existing_label ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_pomodoros_agenda::tests::crlf_and_missing_final_newline_resolve ... ok
test native::capture_pomodoros_agenda::tests::logs_tag_subtrees_and_prose_is_untagged ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture_complete::tests::relations::relation_label_double_pipe_keeps_pipes_and_reports_one_off ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_pomodoros_agenda::tests::current_numbers_match_number_task_links_walk ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_pomodoros_agenda::tests::unreadable_notes_fail_soft ... ok
test native::capture_pomodoros_agenda::tests::task_block_lines_have_clean_text_kinds_and_depths ... ok
test native::capture_pomodoros_agenda::tests::rotten_log_markers_serialize_as_rotten ... ok
test native::capture_pomodoros_agenda::tests::roles_numbers_and_retired_counts ... ok
test native::capture_pomodoros_agenda::tests::overnight_ranges_roll_the_end_date ... ok
test native::capture_pomodoros_agenda::tests::nested_log_markers_keep_their_own_kind ... ok
test native::capture_complete::tests::relations::relation_label_suggestions_count_links_and_put_typed_spelling_first ... ok
test native::capture_pomodoros_agenda::tests::open_entries_can_link_done_tasks ... ok
test native::capture_project_note::tests::section_title_shape_rejects_mixed_case_and_banners ... ok
test native::capture_pomodoros_agenda::tests::resolved_items_carry_ledger_notes ... ok
test native::capture_pomodoros_agenda::tests::pomodoro_markers_and_prose_mix_with_links ... ok
test native::capture_pomodoros_agenda::tests::each_note_reads_once_per_filter_mode ... ok
test native::capture_related::tests::cosine_is_symmetric_on_identical_titles ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::named_all_caps_bullet_with_children_stays_a_task ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::named_task_keeps_an_existing_created_stamp_before_the_id ... ok
test native::capture_project_note::tests::caret_task_keeps_its_authored_checkbox ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::scheduled_project_renders_linked_tasks_as_blocked ... ok
test native::capture_project_note::tests::configured_cancelled_status_stays_closed_in_project_note ... ok
test native::capture_project_note::tests::prj_task_is_never_linked ... ok
test native::capture_project_note::tests::named_tasks_render_ids_last_with_next_status_for_links ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_pomodoros_agenda::tests::relation_lines_are_not_agenda_task_links ... ok
test native::capture_project_note::tests::unconfigured_status_stays_authored_in_scheduled_project_note ... ok
test native::capture_project_note::tests::scheduled_date_lands_inline_on_prj_with_a_blocked_checkbox ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_schedule_log ... ok
test native::capture_related::tests::stopwords_stay_sorted_for_binary_search ... ok
test native::capture_complete::tests::relations::relation_shell_groups_are_directional_and_skip_guarded_rows ... ok
test native::capture_pomodoros_agenda::tests::resolutions_cover_every_failure_mode ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture::task_blocks::tests::crlf_note_reports_verbatim_texts_without_terminators ... ok
test native::capture::blocked_tasks::tests::prj_internal_same_note_and_descendant_refuse ... ok
test native::capture_related::tests::tokenizer_records_display_spans ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::relations::relation_pools_follow_directional_tiers_and_editability ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_rewrite::tests::json_shape_switches_a_block_id_separator ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::json_shape_attaches_a_relation_label_pipe ... ok
test native::capture_rewrite::tests::close_items_are_never_rewritten ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_rewrite::tests::json_reports_a_task_toggle_notice_without_changing_text ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_work_log_only_task ... ok
test native::capture_schedule_log::tests::insertion_ignores_a_marker_nested_under_another_child ... ok
test native::capture_schedule_log::tests::insertion_prefers_the_schedule_marker_over_other_logs ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_legacy_marker ... ok
test native::capture_rewrite::tests::json_does_not_search_for_a_separator_toggle_without_a_cursor ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_spaced_marker ... ok
test native::capture_schedule_log::tests::insertion_preserves_a_missing_final_newline ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_after_existing_children ... ok
test native::capture_schedule_log::tests::insertion_preserves_crlf_endings ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_for_a_childless_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_schedule_marker_beside_a_rotten_log_only_task ... ok
test native::capture_pomodoros_agenda::tests::long_task_blocks_truncate_at_150_lines ... ok
test native::capture::inbox_route::tests::ir_routed_batch_rolls_back_when_a_repaired_file_changes ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_tabbed_marker ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::randomize_reason_names_the_tool_without_a_from_suffix ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_schedule_log::tests::randomize_reason_appends_the_until_base ... ok
test native::capture::blocked_tasks::tests::a8_refusals_name_star_and_teach ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_schedule_log::tests::randomize_reason_keeps_a_fixed_window ... ok
test native::capture_related::tests::tokenizer_table_covers_bob_aware_cases ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_targets::tests::scan_warns_on_shadowed_alias ... ok
test native::capture_related::tests::same_title_normalization_strips_punctuation_and_tags ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_targets::tests::scan_reads_aliases_and_warns_on_conflicts ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture::task_blocks::tests::interior_blank_lines_are_kept_in_the_block ... ok
test native::capture_task_sections::tests::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::output::override_running_carries_homes_only_for_unnamed_sessions ... ok
test native::capture_task_sections::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_related::tests::ordering_prefers_band_then_open_then_status ... ok
test native::capture_task_sections::tests::checkboxed_all_caps_children_are_not_sections ... ok
test native::capture_task_sections::tests::empty_section_bullet_still_qualifies ... ok
test native::capture_task_sections::tests::grandchild_is_not_a_direct_child_section ... ok
test native::capture_task_sections::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_task_sections::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_task_sections::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_task_sections::tests::lists_sections_in_document_order_for_a_block_id ... ok
test native::capture_task_sections::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_task_sections::tests::title_whitelist_edges ... ok
test native::capture_task_sections::tests::managed_logs_are_never_sections_plain_titles_are ... ok
test native::capture_task_sections::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_task_sections::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_task_sections::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_task_toggle::tests::insertion_ignores_struck_history_and_adds_a_live_link ... ok
test native::capture_task_sections::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_related::tests::numbers_that_differ_cap_duplicates_at_similar ... ok
test native::capture_task_toggle::tests::insertion_removes_duplicate_from_later_open_entry ... ok
test native::capture_related::tests::band_edges_and_short_query_rules ... ok
test native::capture_related::tests::archive_closed_window_respects_mtime ... ok
test native::capture_task_toggle::tests::ledger_entry_completed_ref_is_pomodoro_closed ... ok
test native::capture_task_toggle::tests::blocked_is_forced_to_next ... ok
test native::capture_task_sections::tests::resolved_task_with_no_sections_is_a_successful_empty_list ... ok
test native::capture_task_sections::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_task_toggle::tests::errors_when_no_eligible_open_entry ... ok
test native::capture_task_toggle::tests::errors_on_multiple_open_timed_entries ... ok
test native::capture_task_toggle::tests::errors_when_no_pomodoros_section ... ok
test native::capture_task_sections::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_multiline_source ... ok
test native::capture_task_toggle::tests::ledger_entry_move_tracks_duplicate_unnamed_destination_after_source ... ok
test native::capture_task_toggle::tests::ledger_entry_stale_ref_is_stale_pomodoro ... ok
test native::capture_task_sections::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_task_toggle::tests::ledger_entry_moves_q_to_the_named_ref ... ok
test native::capture_task_toggle::tests::idempotent_insertion_skips_when_already_linked ... ok
test native::capture_related::tests::closed_window_includes_30_days_and_excludes_31 ... ok
test native::capture_task_toggle::tests::ledger_exact_name_reuses_a_whole_slug_open_entry ... ok
test native::capture_task_toggle::tests::implicit_insertion_falls_back_to_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::ledger_exact_name_creates_when_only_a_prefix_matches ... ok
test native::capture_task_toggle::tests::implicit_insertion_targets_single_open_timed_entry ... ok
test native::capture::blocked_tasks::tests::next_cap_holds_in_progress_dependent_and_prj_resident ... ok
test native::capture_task_toggle::tests::invalid_pomodoro_name_is_rejected ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_related::tests::excludes_gtd_checklist_and_closed_recurring_rows ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_related::tests::scorer_pairs_from_research ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_templates::command::tests::relative_time_uses_the_bob_clock_value ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_templates::command::tests::selectors_use_one_or_two_digits_for_one_based_indices ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_preserves_struck_links_and_removes_only_live_occurrences ... ok
test native::capture_templates::store::tests::canonical_text_handles_crlf_unicode_escapes_and_header_gap ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_templates::store::tests::canonical_text_strips_trailing_space_and_keeps_layout ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::capture_templates::store::tests::origin_validation_accepts_only_short_alphanumerics ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_work_log::tests::creates_work_log_after_rotten_log_and_leaves_rotten_untouched ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_templates::store::tests::one_row_and_many_rows_save_the_same_entry ... ok
test native::catalog::protocol::tests::parses_space_and_equals_forms ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::catalog::protocol::tests::rejects_malformed_requests ... ok
test native::catalog::protocol::tests::unsupported_covers_both_directions ... ok
test native::capture_templates::store::tests::newer_schema_refuses_writes_and_keeps_bytes ... ok
test native::catalog::tests::ids_are_unique_kebab_case_and_keywords_are_lowercase ... ok
test native::capture_pomodoros_agenda::tests::september_shaped_vault_finishes_fast ... ok
test native::capture_templates::store::tests::template_ids_are_stable_and_content_addressed ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_complete::tests::output::named_start_completion_omits_context_without_a_single_runner ... ok
test native::collect_done::tests::plan::existing_archive_with_stale_metadata_creates_archive_only_plan ... ok
test native::catalog::tests::slots_and_invalidates_are_known ... ok
test native::collect_done::tests::plan::includes_nested_path_note_when_it_meets_threshold ... ok
test native::collect_done::tests::plan::missing_archive_without_threshold_tasks_is_not_planned ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::collect_done::tests::plan::link_repair_scan_includes_done_notes ... ok
test native::collect_done::tests::plan::planned_source_and_archive_contents_are_link_repaired ... ok
test native::collect_done::tests::plan::generated_tag_pages_do_not_make_source_basename_ambiguous ... ok
test native::collect_done::tests::plan::canceled_only_tasks_below_threshold_remain_in_source ... ok
test native::collect_done::tests::plan::canceled_only_tasks_move_when_threshold_is_met ... ok
test native::collect_done::tests::plan::already_linked_source_with_existing_archive_is_not_planned ... ok
test native::collect_done::tests::plan::generated_and_template_directories_are_not_collected_or_repaired ... ok
test native::catalog::tests::policy_invariants ... ok
test native::collect_done::tests::plan::collecting_tasks_adds_done_tasks_to_source ... ok
test native::collect_done::tests::unit::adds_archive_parent_to_existing_frontmatter ... ok
test native::collect_done::tests::plan::scans_markdown_files_with_exclusions_and_threshold ... ok
test native::collect_done::tests::unit::adds_done_tasks_to_existing_source_frontmatter ... ok
test native::collect_done::tests::unit::archives_indented_gkeep_marker_with_its_task_and_not_its_neighbor ... ok
test native::collect_done::tests::unit::block_ids_are_only_end_of_line_obsidian_anchors ... ok
test native::collect_done::tests::plan::task_moving_plan_writes_archive_with_nested_source_parent ... ok
test native::collect_done::tests::unit::completed_child_moves_without_collecting_active_parent ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_for_new_archive_note ... ok
test native::collect_done::tests::plan::source_block_id_keeps_links_pointing_at_source ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_with_nested_source_parent ... ok
test native::collect_done::tests::unit::creates_source_frontmatter_for_done_tasks ... ok
test native::collect_done::tests::plan::task_moving_plan_repairs_links_in_separate_notes ... ok
test native::collect_done::tests::unit::dependency_ids_preserve_path_case_and_qualify_nested_notes ... ok
test native::collect_done::tests::plan::duplicate_moved_block_ids_do_not_rewrite_links ... ok
test native::collect_done::tests::unit::below_threshold_block_ids_do_not_trigger_link_repair ... ok
test native::collect_done::tests::unit::block_id_deduplication_preserves_crlf_line_endings ... ok
test native::collect_done::tests::plan::self_heals_preexisting_block_links_to_archive ... ok
test native::collect_done::tests::plan::existing_archive_creates_metadata_only_source_update ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_preserves_distinct_moved_ids ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_skips_existing_candidates ... ok
test native::collect_done::tests::unit::leaves_ambiguous_basename_links_unchanged ... ok
test native::collect_done::tests::unit::inserts_missing_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::leaves_correct_archive_frontmatter_unchanged ... ok
test native::collect_done::tests::unit::leaves_correct_done_tasks_frontmatter_unchanged ... ok
test native::collect_done::tests::unit::maps_archive_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::unit::maps_source_notes_to_archive_notes ... ok
test native::collect_done::tests::unit::maps_source_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::unit::link_repair_uses_renamed_unique_moved_block_id ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_are_ambiguous ... ok
test native::collect_done::tests::unit::extracts_nested_blocks_and_continuations ... ok
test native::collect_done::tests::unit::extracts_block_ids_from_every_moved_task_block_line ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_rewrites_exact_tokens_only ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_become_unique_archive_ids ... ok
test native::collect_done::tests::unit::markdown_repair_skips_wikilink_spans ... ok
test native::collect_done::tests::unit::parses_attached_short_threshold_option ... ok
test native::collect_done::tests::unit::parses_default_threshold ... ok
test native::collect_done::tests::unit::parses_short_threshold_equals_option ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_supports_task_field_grammar_and_skips_code ... ok
test native::collect_done::tests::unit::parses_short_threshold_option ... ok
test native::collect_done::tests::unit::existing_archive_block_ids_reserve_original_ids ... ok
test native::collect_done::tests::unit::parses_threshold_equals_option ... ok
test native::collect_done::tests::unit::parses_threshold_option ... ok
test native::collect_done::tests::unit::pathless_archive_links_gain_the_source_note_path ... ok
test native::collect_done::tests::unit::preserves_line_endings_in_source_and_archive ... ok
test native::collect_done::tests::unit::recognizes_done_and_canceled_task_lines_only ... ok
test native::collect_done::tests::unit::rejects_zero_threshold ... ok
test native::collect_done::tests::unit::repairs_same_note_nested_and_unique_basename_links ... ok
test native::collect_done::tests::unit::repairs_simple_markdown_inline_block_links ... ok
test native::collect_done::tests::unit::replaces_stale_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::repairs_wikilinks_embeds_and_aliases_to_moved_blocks ... ok
test native::collect_done::tests::unit::replaces_stale_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::updates_existing_archive_parent_frontmatter ... ok
test native::collect_done::tests::unit::prepends_archive_frontmatter_when_existing_note_has_none ... ok
test native::completion::adapters::tests::bash_stamp_matches_protocol ... ok
test native::completion::adapters::tests::zsh_stamp_matches_protocol ... ok
test native::collect_done::tests::unit::unqualifiable_paths_do_not_abort_identity_indexing ... ok
test native::collect_done::tests::unit::preserves_crlf_when_adding_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::preserves_crlf_when_repairing_archive_frontmatter ... ok
test native::completion::kinds::tests::path_specific_entries_win ... ok
test native::completion::protocol::tests::encoder_sanitizes_fields_and_drops_bad_values ... ok
test native::completion::protocol::tests::parses_attached_forms ... ok
test native::completion::protocol::tests::parses_full_request ... ok
test native::completion::protocol::tests::rejects_malformed_requests ... ok
test native::completion::protocol::tests::skew_messages_cover_both_directions ... ok
test native::completion::report::tests::tilde_collapses_home ... ok
test native::completion::tests::deadline_defaults_and_falls_back ... ok
test native::collect_done::tests::plan::self_healing_is_idempotent_after_links_are_repaired ... ok
test native::collect_done::tests::plan::task_moves_repair_dependency_ids_in_archive_and_all_dependents ... ok
test native::completion::context::tests::alias_words_rewrite_to_the_canonical_path ... ok
test native::completion::tree::tests::hand_descriptor_drift ... ok
test native::completion::verify::tests::timeout_override_falls_back ... ok
test native::config::capture::tests::accepts_zero_through_cap ... ok
test native::config::capture::tests::missing_capture_block_uses_default ... ok
test native::config::capture::tests::rejects_out_of_range_and_non_integer ... ok
test native::completion::tree::tests::descriptor_names_match_canonical_paths ... ok
test native::completion::tree::tests::hidden_aliases_and_help_are_absent ... ok
test native::completion::present::tests::attached_option_values_carry_prefix ... ok
test native::catalog::tests::public_leaves_are_entries_or_excluded ... ok
test native::completion::present::tests::double_dash_offers_long_forms_only ... ok
test native::config::day_timezone::tests::invalid_timezone_has_a_clear_config_error ... ok
test native::config::dependencies::tests::reports_invalid_blocks_lines_path_and_type ... ok
test native::config::dependencies::tests::rejects_invalid_dependencies_values ... ok
test native::config::day_timezone::tests::rejects_non_string_and_empty_timezone_values ... ok
test native::config::dependencies::tests::blocks_lines_defaults_true_and_parses_false ... ok
test native::config::freshness::tests::absent_freshness_block_loads_defaults ... ok
test native::config::day_timezone::tests::timezone_is_optional_and_null_means_unset ... ok
test native::capture::tests::template::planning_each_template_matches_planning_its_expansion ... ok
test native::config::freshness::tests::decay_defaults_when_absent_null_true_or_empty ... ok
test native::config::freshness::tests::canonical_budget_key_wins_over_legacy ... ok
test native::completion::tree::tests::mounted_names_match_subcommands_in_order ... ok
test native::catalog::tests::preview_and_fixed_options_exist_on_the_leaf ... ok
test native::completion::tree::tests::mounted_names_have_no_spaces ... ok
test native::completion::kinds::tests::every_value_arg_has_a_decision ... ok
test native::completion::present::tests::lone_dash_pairs_forms_with_identical_descriptions ... ok
test native::config::freshness::tests::missing_freshness_file_loads_defaults ... ok
test native::config::day_timezone::tests::parses_valid_iana_timezone_names ... ok
test native::config::freshness::tests::null_freshness_block_loads_defaults ... ok
test native::config::freshness::tests::null_values_fall_back_to_defaults ... ok
test native::config::freshness::tests::parses_freshness_overrides_and_ignores_unknown_keys ... ok
test native::config::freshness::tests::project_interval_defaults_absent_and_null ... ok
test native::config::freshness::tests::obsolete_reference_interval_is_ignored_regardless_of_value ... ok
test native::completion::context::tests::unknown_words_never_fail_the_parse ... ok
test native::config::freshness::tests::decay_false_counts_but_never_asks ... ok
test native::config::freshness::tests::lane_intervals_default_absent_and_null ... ok
test native::config::freshness::tests::decay_parses_zero_and_fixed_entry ... ok
test native::config::freshness::tests::legacy_budget_key_supplies_budget_with_deprecation_flag ... ok
test native::completion::kinds::tests::every_table_entry_matches_the_tree ... ok
test native::config::freshness::tests::legacy_budget_key_recovers_and_rejects_like_canonical ... ok
test native::config::freshness::tests::lane_intervals_parse_false_and_integers ... ok
test native::capture_language::tests::template::both_template_bounds_are_checked_without_truncation ... ok
test native::config::freshness::tests::mistyped_freshness_block_leaves_other_loaders_working ... ok
test native::config::freshness::tests::project_interval_parses_integers ... ok
test native::config::plan::tests::absent_plan_block_loads_defaults ... ok
test native::config::freshness::tests::rejects_invalid_decay_values ... ok
test native::config::freshness::tests::rejects_invalid_lane_intervals ... ok
test native::config::plan::tests::link_unblocked_defaults_true_and_parses_false ... ok
test native::config::plan::tests::absent_max_ready_per_note_falls_back_to_default ... ok
test native::config::freshness::tests::rejects_invalid_tracker_intervals ... ok
test native::config::freshness::tests::rejects_invalid_freshness_values ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_without_a_current_session ... ok
test native::config::plan::tests::missing_plan_file_loads_defaults ... ok
test native::config::plan::tests::null_plan_block_loads_defaults ... ok
test native::config::plan::tests::parses_plan_overrides_and_ignores_unknown_keys ... ok
test native::config::relations::tests::missing_file_loads_defaults ... ok
test native::config::plan::tests::reading_theme_defaults_off_and_parses_names ... ok
test native::config::relations::tests::cancel_labels_are_ordered_normalized_and_deduplicated ... ok
test native::config::relations::tests::invalid_cancel_entries_warn_and_keep_valid_peers ... ok
test native::config::relations::tests::reports_invalid_linked_from_lines_path_and_type ... ok
test native::config::relations::tests::whole_relations_section_still_requires_a_mapping ... ok
test native::config::relations::tests::linked_from_lines_defaults_true_and_parses_false ... ok
test native::config::stats::tests::duplicate_overview_and_hide_names_are_deduped ... ok
test native::config::stats::tests::missing_file_and_absent_block_use_defaults ... ok
test native::config::stats::tests::malformed_metric_entries_do_not_fail_the_load ... ok
test native::config::stats::tests::non_string_metric_key_is_stringified ... ok
test native::config::plan::tests::rejects_invalid_plan_values ... ok
test native::config::plan::tests::mistyped_plan_block_leaves_other_loaders_working ... ok
test native::catalog::tests::document_shape ... ok
test native::config::stats::tests::bad_stats_block_leaves_other_loaders_working ... ok
test native::config::plan::tests::max_ready_per_note_bounds_and_message ... ok
test native::config::tests::missing_file_message_is_command_neutral ... ok
test native::config::tests::level_by_label_matches_ascii_case_insensitively ... ok
test native::config::tests::missing_gkeep_file_loads_defaults ... ok
test native::config::tests::level_for_value_matches_exact_value_after_trim ... ok
test native::config::tests::levels_exposes_every_configured_level ... ok
test native::config::tests::mistyped_plan_block_leaves_gkeep_loader_working ... ok
test native::config::tests::mistyped_plan_block_leaves_highlights_loader_working ... ok
test native::config::tests::ignores_decay_and_rolls_keys ... ok
test native::config::tests::mistyped_plan_block_leaves_priority_loader_working ... ok
test native::config::tests::blank_highlights_pre_scan_hook_disables_file_hook ... ok
test native::config::tests::blank_and_absent_listen_command_parse_as_none ... ok
test native::catalog::tests::every_path_resolves_to_a_public_leaf ... ok
test native::config::tests::derive_seed_is_deterministic_and_sensitive_to_every_part ... ok
test native::config::stats::tests::parses_overrides_and_ignores_unknown_keys ... ok
test native::config::stats::tests::rejects_invalid_top_level_values ... ok
test native::config::tests::derive_seed_separator_prevents_part_boundary_collisions ... ok
test native::config::tests::parses_full_gkeep_section_and_ignores_unknown_keys ... ok
test native::config::tests::parses_highlights_audio_link_template ... ok
test native::config::tests::parses_highlights_coordinate_pdf_writes_switch ... ok
test native::capture_templates::store::tests::origin_replace_keeps_unknown_fields ... ok
test native::config::tests::parses_highlights_listen_command_trimmed ... ok
test native::capture_templates::store::tests::unknown_fields_survive_a_rewrite ... ok
test native::config::tests::parses_highlights_ingest_on_create_switch ... ok
test native::capture_templates::store::tests::shelf_files_use_restricted_permissions ... ok
test native::capture_templates::store::tests::corrupt_file_is_quarantined_on_write ... ok
test native::config::tests::parses_highlights_pre_scan_hook ... ok
test native::config::tests::parses_deployed_config ... ok
test native::config::tests::rejects_blank_label ... ok
test native::config::tests::rejects_blank_value ... ok
test native::completion::context::tests::env_defaults_apply_without_flags ... ok
test native::config::tests::rejects_empty_levels ... ok
test native::config::tests::rejects_duplicate_level_labels ... ok
test native::config::tests::rejects_duplicate_level_values ... ok
test native::config::tests::rejects_legacy_highlights_pre_scan_command ... ok
test native::config::tests::rejects_labels_that_differ_only_by_case ... ok
test native::completion::context::tests::parses_attached_and_short_cluster_forms ... ok
test native::config::tests::rejects_min_greater_than_max ... ok
test native::config::tests::rejects_missing_priority_property ... ok
test native::config::tests::parses_absent_highlights_config_as_none ... ok
test native::config::tests::rejects_invalid_gkeep_yaml ... ok
test native::config::tests::parses_absent_gkeep_section_as_defaults ... ok
test native::config::tests::mix64_spreads_sequential_inputs ... ok
test native::completion::tree::tests::tree_debug_assert_passes ... ok
test native::completion::context::tests::parses_long_route_and_bob_dir ... ok
test native::config::tests::rejects_missing_schedules ... ok
test native::catalog::tests::required_keyword_lookups ... ok
test native::config::tests::rejects_non_integer_min_days ... ok
test native::config::tests::rejects_non_numeric_gkeep_timeout ... ok
test native::config::tests::rejects_missing_value ... ok
test native::config::tests::rejects_value_containing_field_syntax ... ok
test native::config::tests::resolve_config_path_expands_tilde_in_xdg_config_home ... ok
test native::config::tests::resolve_config_path_falls_back_to_xdg_config_home ... ok
test native::config::tests::resolve_config_path_ignores_empty_env_values ... ok
test native::config::tests::resolve_config_path_prefers_bob_config_file ... ok
test native::config::tests::rejects_wrong_schedules_target ... ok
test native::config::tests::roll_offset_p4_window_hits_both_extremes ... ok
test native::config::tests::unrelated_highlights_keys_still_parse_with_listen_command ... ok
test native::config::themes::tests::empty_mapping_is_none ... ok
test native::catalog::tests::script_backed_leaves_resolve ... ok
test native::config::tests::resolve_config_path_falls_back_to_home_dot_config ... ok
test native::config::themes::tests::missing_block_is_none ... ok
test native::config::tests::rejects_negative_min_days ... ok
test native::config::themes::tests::parses_slots_auto_and_null ... ok
test native::config::tests::roll_offset_returns_fixed_value_when_min_equals_max ... ok
test native::config::themes::tests::rejects_bad_color ... ok
test native::config::themes::tests::rejects_non_mapping ... ok
test native::config::themes::tests::rejects_duplicate_keys ... ok
test native::dataview::tasks::filter::tests::apply_reports_a_missing_sandbox_for_function_filters ... ok
test native::dataview::tasks::filter::tests::apply_runs_without_a_sandbox_when_no_function_is_used ... ok
test native::dataview::tasks::filter::tests::global_filter_removal_only_removes_the_first_occurrence ... ok
test native::config::tests::tolerates_unusual_sibling_properties ... ok
test native::config::themes::tests::missing_file_has_no_warning ... ok
test native::dataview::tasks::filter::tests::numbered_ranges_cover_year_month_quarter_and_iso_week ... ok
test native::config::themes::tests::null_block_is_none ... ok
test native::dataview::tasks::filter::tests::relative_ranges_use_iso_weeks_and_calendar_boundaries ... ok
test native::dataview::tasks::filter::tests::weekday_and_offset_dates_are_pinned_to_now ... ok
test native::config::themes::tests::rejects_blank_and_plus_names ... ok
test native::dataview::tasks::index::tests::heading_parser_supports_atx_and_setext_headings ... ok
test native::dataview::tasks::js::tests::init_budget_is_separate_from_and_above_expression_timeout ... ok
test native::dataview::tasks::js::tests::init_budget_scales_with_task_count_and_caps ... ok
test native::config::themes::tests::rejects_non_string_key ... ok
test native::dataview::tasks::parse::tests::numbered_date_ranges_optional_priority_is_and_status_boundary_parse ... ok
test native::dataview::tasks::parse::tests::scanner_matches_tasks_line_continuation_rules ... ok
test native::dataview::tasks::parse::tests::parses_every_v8_sort_group_and_layout_key ... ok
test native::dataview::tasks::parse::tests::rejects_malformed_filters_with_actionable_errors ... ok
test native::dataview::tasks::parse::tests::ignore_global_query_can_come_from_query_file_defaults ... ok
test native::dataview::tasks::parse::tests::upstream_dialect_rejects_status_symbol_with_tasks_error ... ok
test native::dataview::tasks::parse::tests::uses_javascript_detects_by_function_clauses ... ok
test native::dataview::tasks::parse::tests::parses_every_filter_family_and_boolean_combinations ... ok
test native::completion::context::tests::task_and_repo_need_their_subcommands ... ok
test native::dataview::tasks::result::tests::build_reports_a_missing_sandbox_for_function_sorts ... ok
test native::catalog::tests::section_matches_root_subcommands ... ok
test native::dataview::tasks::result::tests::explanations_include_expanded_preset_statements ... ok
test native::dataview::tasks::parse::tests::lane_queries_run_without_the_javascript_sandbox ... ok
test native::dataview::tasks::result::tests::natural_collation_is_case_insensitive_and_numeric ... ok
test native::dataview::tasks::settings::tests::unknown_task_format_falls_back_to_emoji ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... ok
test native::dataview::tasks::parse::tests::boolean_chains_use_tasks_precedence_and_allow_operand_apostrophes ... ok
test native::dataview::tasks::filter::tests::absolute_ranges_are_inclusive_and_order_independent ... ok
test native::dataview::tasks::result::tests::build_runs_without_a_sandbox_when_no_function_is_used ... ok
test native::dataview::tasks::filter::tests::regex_flags_match_javascript_filtering_behavior ... ok
test native::dataview::tasks::task::tests::file_context_matches_tasks_expose_properties ... ok
test native::catalog::tests::aliases_resolve_to_entries_or_excluded_or_public_prefixes ... ok
test native::dataview::tasks::parse::tests::composes_global_defaults_presets_and_placeholders_in_order ... ok
test native::dataview::tests::dql_missing_table_identities_warn_per_row ... ok
test native::dataview::tests::dql_table_paths_use_first_identity_column ... ok
test native::dataview::tests::dql_task_paths_resolve_grouped_task_source_notes ... ok
test native::dataview::tasks::task::tests::recurrence_rules_are_validated_and_standardized ... ok
test native::dataview::tests::native_dql_parser_accepts_phase3_command_surface ... ok
test native::dataview::tasks::task::tests::removing_global_filter_preserves_spacing_and_only_removes_first_word ... ok
test native::dataview::tasks::task::tests::task_line_parser_matches_tasks_markers_and_spacing ... ok
test native::dataview::tasks::task::tests::urgency_due_scheduled_and_start_boundaries_match_tasks_v8 ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_from_nested_blockquotes_and_callouts ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_with_heading_context ... ok
test native::dataview::tests::dql_grouped_table_rows_warn_and_fail_when_strict ... ok
test native::dataview::tests::dql_list_paths_use_list_pair_identity ... ok
test native::dataview::tests::native_dql_parser_reports_representative_invalid_queries ... ok
test native::capture_parse::tests::theme_name_spans_report_components_with_source_offsets ... ok
test native::dataview::tasks::task::tests::metadata_must_be_trailing_but_tags_can_be_interleaved ... ok
test native::dataview::tasks::task::tests::dataview_parser_extracts_all_fields_and_cleans_description ... ok
test native::dataview::tasks::task::tests::invalid_dates_and_recurrences_match_tasks_semantics ... ok
test native::dataview::tasks::task::tests::dataview_fields_honor_delimiters_whitespace_commas_and_case ... ok
test native::dataview::tasks::task::tests::unknown_status_is_todo_and_remove_global_filter_is_display_only ... ok
test native::dataview::tasks::task::tests::urgency_matches_tasks_v8_coefficients ... ok
test native::dataview::tests::native_source_parser_accepts_phase3_source_surface ... ok
test native::dataview::tests::source_paths_are_normalized_and_deduplicated ... ok
test native::env::tests::configured_timezone_keeps_the_eastern_day_through_utc_midnight ... ok
test native::file_coordination::attempt::tests::panic_resumes_only_after_request_returns ... ok
test native::file_coordination::attempt::tests::missing_callback_is_a_failure_and_accessor_errors_are_values ... ok
test native::file_coordination::attempt::tests::zero_budget_does_not_request_access ... ok
test native::file_coordination::attempt::tests::unexpected_error_never_runs_accessor_or_waits_out_budget ... ok
test native::file_coordination::tests::direct_write_is_once_synchronous_and_keeps_accessor_errors ... ok
test native::env::tests::no_configured_timezone_uses_the_host_timezone ... ok
test native::freshness::placement::placement_tests::cancelled_is_refused_like_done ... ok
test native::file_coordination::tests::direct_move_scope_never_replaces_destination ... ok
test native::file_coordination::tests::direct_move_scope_performs_forward_and_inverse_no_clobber_moves ... ok
test native::freshness::placement::placement_tests::keeps_first_valid_wins_up_to_999 ... ok
test native::freshness::placement::placement_tests::freshness_config_defaults_match_contract ... ok
test native::freshness::placement::placement_tests::non_task_lines_are_refused ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::freshness::placement::placement_tests::keeps_invalid_values_report_zero ... ok
test native::freshness::placement::placement_tests::keeps_misplaced_lints_and_repairs ... ok
test native::freshness::placement::placement_tests::keeps_absent_reads_zero ... ok
test native::freshness::placement::placement_tests::keeps_same_day_preserve_is_noop ... ok
test native::freshness::placement::placement_tests::p01_bare_appends_fresh ... ok
test native::freshness::placement::placement_tests::generic_stamps_clear_keeps_including_same_day ... ok
test native::freshness::placement::placement_tests::keeps_canonical_order_after_refresh ... ok
test native::freshness::placement::placement_tests::p02_created_suffix ... ok
test native::freshness::placement::placement_tests::keeps_key_match_is_exact_and_paren_reads ... ok
test native::freshness::placement::placement_tests::p07_restamp_replaces_date ... ok
test native::freshness::placement::placement_tests::hooks_blocked_signals_survive_and_checkbox_swap_preserves_fresh ... ok
test native::freshness::placement::placement_tests::p08_same_day_is_noop ... ok
test native::freshness::placement::placement_tests::p03_block_id_only ... ok
test native::freshness::placement::placement_tests::p04_interleaved_suffix ... ok
test native::freshness::placement::placement_tests::p05_unknown_field_stays_left ... ok
test native::freshness::placement::placement_tests::p13_recurring_refused ... ok
test native::config::tests::roll_offset_stays_within_bounds_for_many_seeds ... ok
test native::freshness::placement::placement_tests::p09_misplaced_is_repaired ... ok
test native::freshness::placement::placement_tests::p17_done_refused ... ok
test native::freshness::placement::placement_tests::p18_deeply_indented_quote_is_not_a_task ... ok
test native::freshness::placement::placement_tests::p06_spacing_head_collapses_suffix_untouched ... ok
test native::freshness::placement::placement_tests::p12_set_and_clear_refresh ... ok
test native::freshness::placement::placement_tests::p16_indented_blocked ... ok
test native::freshness::placement::placement_tests::p10_duplicates_collapse_and_use_latest ... ok
test native::freshness::placement::placement_tests::p14_global_filter_floor ... ok
test native::freshness::placement::placement_tests::p18_quoted_task_stamps_with_prefix_kept ... ok
test native::freshness::placement::placement_tests::pomodoro_ledger_rows_are_refused_byte_for_byte_by_every_stamp_writer ... ok
test native::freshness::placement::placement_tests::p18_nested_quote_stamps ... ok
test native::freshness::placement::placement_tests::prose_that_mentions_a_time_range_remains_stampable ... ok
test native::completion::present::tests::text_started_slot_offers_no_options ... ok
test native::freshness::placement::placement_tests::p11_refresh_follows_fresh ... ok
test native::dataview::tests::flatten_budget_honors_earlier_filters_not_later_limits ... ok
test native::dataview::tests::flatten_budget_accepts_exact_limit_and_rejects_overflow ... ok
test native::freshness::placement::placement_tests::keeps_fixture_vectors_match_rust ... ok
test native::dataview::tests::flatten_aliases_empty_null_and_scalar_values ... ok
test native::freshness::placement::placement_tests::set_refresh_replaces_existing_value ... ok
test native::freshness::placement::placement_tests::refusals_leave_keeps_untouched ... ok
test native::freshness::placement::placement_tests::p15_parenthesized_field ... ok
test native::freshness::placement::placement_tests::ub4_mark_unblocked_skips_lane_landings ... ok
test native::freshness::placement::placement_tests::ub2_mark_unblocked_skips_new_without_fresh ... ok
test native::freshness::placement::placement_tests::ub5_ub6_mark_unblocked_skips_out_of_scope_rows ... ok
test native::freshness::placement::placement_tests::ub3_mark_unblocked_skips_scheduled_tickler ... ok
test native::dataview::tests::flatten_alias_and_collection_builtins_do_not_mutate_siblings ... ok
test native::dataview::tests::group_by_preserves_first_seen_order_and_member_access ... ok
test native::dataview::tests::flatten_retains_file_metadata_and_nested_task_children ... ok
test native::freshness::placement::placement_tests::ub8_prune_drops_unblocked_when_fresh_passes_it ... ok
test native::dataview::tests::grouped_sorting_repeated_grouping_and_lambda_shadowing ... ok
test native::freshness::seed::tests::oversized_notes_split_into_consecutive_chunks ... ok
test native::dataview::tests::flatten_lists_include_nested_children ... ok
test native::freshness::placement::placement_tests::ub7_stamps_clear_unblocked ... ok
test native::freshness::seed::tests::write_changes_refuses_a_file_changed_since_scan ... ok
test native::freshness::placement::placement_tests::ub_read_reports_unblocked_lints_and_latest_wins ... ok
test native::freshness::state::state_tests::cl11_checklist_beats_lane_and_tracker ... ok
test native::freshness::placement::placement_tests::ub1_mark_unblocked_keeps_refresh_and_keeps_in_order ... ok
test native::freshness::state::state_tests::cl12_repeat_without_when_done_still_pre ... ok
test native::freshness::state::state_tests::cl10_completed_occurrence_and_future_next_leave_queue ... ok
test native::freshness::placement::placement_tests::ub12_unblocked_before_tasks_fields_parses_invariantly ... ok
test native::freshness::state::state_tests::cl5_tag_matching ... ok
test native::freshness::state::state_tests::cl6_conflict_prefers_pre ... ok
test native::freshness::state::state_tests::cl7_one_off_post_keeps_new_state ... ok
test native::freshness::placement::placement_tests::parse_invariance_across_all_vectors ... ok
test native::freshness::placement::placement_tests::ub1_mark_unblocked_writes_and_replaces_older_value ... ok
test native::freshness::state::state_tests::cl4_today_and_daily_note_still_pre ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::freshness::state::state_tests::cl2_unknown_status_pre_is_queued_with_null_lane ... ok
test native::freshness::seed::tests::canonical_restamps_pass_invariance ... ok
test native::freshness::seed::tests::invariance_abort_lists_a_line_hiding_a_field ... ok
test native::freshness::state::state_tests::counts_carry_decide ... ok
test native::freshness::state::state_tests::cl9_recurring_checklist_refuses_stamp ... ok
test native::freshness::state::state_tests::cl1_recurring_pre_chore ... ok
test native::freshness::state::state_tests::l2_lane_overrides_refresh ... ok
test native::freshness::state::state_tests::l4_lane_off_switch_and_null_default ... ok
test native::freshness::state::state_tests::decide_at_limit_but_not_below ... ok
test native::freshness::state::state_tests::l3_lane_exclusions_have_no_tier ... ok
test native::freshness::state::state_tests::cl8_nine_tier_order ... ok
test native::freshness::state::state_tests::l5_lane_order_never_stamped_first ... ok
test native::freshness::state::state_tests::missing_created_sorts_after_dated_peers ... ok
test native::freshness::state::state_tests::bucket_partition_vectors ... ok
test native::freshness::state::state_tests::q1_bryan_example_orders_adjc ... ok
test native::freshness::state::state_tests::q2_tier_order_beats_path_order ... ok
test native::freshness::state::state_tests::cl3_exclusions_drop_checklist_rows ... ok
test native::freshness::state::state_tests::rc10_checklist_wins_over_recurring ... ok
test native::freshness::state::state_tests::r1_tickler_beats_older_rotten ... ok
test native::freshness::state::state_tests::rc1_arrived_recurring_row ... ok
test native::freshness::state::state_tests::rc2_arrives_today ... ok
test native::env::tests::date_command_override_runs_in_the_configured_timezone ... ok
test native::freshness::state::state_tests::rc11_stray_stamp_is_ignored ... ok
test native::freshness::state::state_tests::decide_covers_tickler_but_never_new ... ok
test native::freshness::state::state_tests::decide_on_early_dates ... ok
test native::freshness::state::state_tests::rc12_order_and_counts ... ok
test native::freshness::state::state_tests::project_interval_is_special_and_reference_freshness_is_ordinary ... ok
test native::freshness::state::state_tests::decide_zero_off_and_lane_rows ... ok
test native::freshness::state::state_tests::l1_lane_due_and_stamped_today ... ok
test native::freshness::state::state_tests::r2_tickler_orders_by_schedule_then_newest_created ... ok
test native::freshness::state::state_tests::rc5_due_only_future ... ok
test native::freshness::state::state_tests::rc6_earliest_date_wins ... ok
test native::freshness::state::state_tests::rc7_undated_recurring_stays_out ... ok
test native::freshness::state::state_tests::rc4_due_only_past ... ok
test native::freshness::state::state_tests::rc8_recurring_lane_rows_keep_lane ... ok
test native::freshness::state::state_tests::s01_new_without_stamp ... ok
test native::capture_templates::store::tests::lock_timeout_reports_busy ... ok
test native::freshness::state::state_tests::rc3_future_occurrence_stays_out ... ok
test native::dataview::tasks::task::tests::all_priorities_have_tasks_v8_names_numbers_and_scores ... ok
test native::freshness::state::state_tests::s03_boundary_is_rotten_with_zero_overdue ... ok
test native::dataview::tasks::index::tests::paragraphs_break_list_hierarchy ... ok
test native::freshness::state::state_tests::s04_overdue_counts_days ... ok
test native::freshness::state::state_tests::s05_task_interval_beats_note ... ok
test native::freshness::state::state_tests::reference_lane_interval_matches_ordinary_task ... ok
test native::freshness::state::state_tests::s07_config_interval ... ok
test native::freshness::state::state_tests::s02_fresh_with_due_on ... ok
test native::freshness::state::state_tests::s09_malformed_fresh_is_new_with_lint ... ok
test native::freshness::state::state_tests::s08_invalid_overrides_fall_through_with_lints ... ok
test native::freshness::state::state_tests::s10_future_fresh_is_new_with_lint ... ok
test native::freshness::state::state_tests::s11_resurfaced_when_schedule_returns_after_stamp ... ok
test native::dataview::tasks::index::tests::dependency_graph_matches_direct_tasks_v8_semantics ... ok
test native::freshness::state::state_tests::s06_note_interval_beats_config ... ok
test native::freshness::state::state_tests::rc9_exclusions_drop_recurring_rows ... ok
test native::freshness::state::state_tests::ub10_latest_source_wins_due_on ... ok
test native::freshness::state::state_tests::ub11_same_date_tie_resolves_to_scheduled ... ok
test native::freshness::state::state_tests::s12_equal_schedule_is_not_resurfaced ... ok
test native::freshness::state::state_tests::b1_upkeep_counts_outside_the_lanes ... ok
test native::dataview::tasks::index::tests::fixture_index_builds_hierarchy_and_ignores_fences_and_dot_directories ... ok
test native::freshness::state::state_tests::tracker_lane_precedence_and_disabled_lanes ... ok
test native::freshness::state::state_tests::ub1_unblocked_recovery_is_tickler ... ok
test native::freshness::state::state_tests::ub15_prj_schedule_return_walks_projects ... ok
test native::freshness::state::state_tests::ub13_unblock_tickler_never_decides ... ok
test native::freshness::state::state_tests::ub9_fresh_equals_unblocked_still_resurfaces ... ok
test native::completion::present::tests::root_empty_offers_sectioned_commands_in_help_order ... ok
test native::freshness::state::state_tests::s14_queue_order_new_then_due ... ok
test native::gkeep::adapter::tests::resolve_uses_override_without_path_lookup ... ok
test native::gkeep::adapter::tests::resolve_without_uv_is_a_setup_error ... ok
test native::dataview::tasks::task::tests::emoji_parser_extracts_all_fields_and_variant_selectors ... ok
test native::freshness::state::state_tests::reference_rows_share_ordinary_keep_and_tier_behavior ... ok
test native::freshness::state::state_tests::s13_out_of_scope_is_null ... ok
test native::completion::tree::tests::parse_smoke ... ok
test native::gkeep::cli::tests::bob_dir_flag_expands_tilde ... ok
test native::gkeep::config::tests::device_id_is_derived_and_pinned ... ok
test native::gkeep::config::tests::device_id_validation ... ok
test native::freshness::state::state_tests::s15_counts_and_budget_meter ... ok
test native::freshness::state::state_tests::tracking_projects_tier_and_counts ... ok
test native::gkeep::cli::tests::doctor_and_login_args ... ok
test native::gkeep::cli::tests::migrate_tasks_args_pin_options ... ok
test native::gkeep::cli::tests::pull_args_pin_every_option ... ok
test native::gkeep::config::tests::adapter_override_reads_env ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::freshness::state::state_tests::ub14_tickler_tie_orders_by_path_then_line ... ok
test native::dataview::tasks::tests::non_function_queries_skip_the_sandbox_on_a_real_vault ... ok
test native::gkeep::cli::tests::list_args_pin_defaults_and_values ... ok
test native::gkeep::config::tests::token_shape_classifier ... ok
test native::gkeep::doctor::tests::device_id_shortens_to_eight_plus_ellipsis ... ok
test native::gkeep::doctor::tests::home_prefix_collapses_to_tilde ... ok
test native::gkeep::imports::tests::malformed_store_is_actionable ... ok
test native::gkeep::config::tests::resolve_applies_defaults_and_derives_device_id ... ok
test native::gkeep::doctor::tests::check_status_names_match_the_json_contract ... ok
test native::gkeep::doctor::tests::tasks_heading_matches_headings_only ... ok
test native::gkeep::config::tests::resolve_email_override_wins ... ok
test native::gkeep::imports::tests::absent_store_is_valid ... ok
test native::gkeep::imports::tests::parse_nul_verbose_ignore_handles_spaces_and_colons ... ok
test native::gkeep::imports::tests::unsafe_paths_rejected ... ok
test native::gkeep::ledger::tests::journal_read_skips_non_utf8_lines ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_with_multiple_open_timed_entries ... ok
test native::gkeep::config::tests::read_token_warns_but_keeps_unknown_shapes ... ok
test native::gkeep::login::tests::cookie_line_picks_the_first_non_empty_line ... ok
test native::gkeep::ledger::tests::journal_read_tolerates_missing_files_and_corrupt_lines ... ok
test native::gkeep::login::tests::recovery_path_lives_under_the_state_dir ... ok
test native::gkeep::ledger::tests::marker_parsing_finds_all_hits_and_ignores_broken_ones ... ok
test native::gkeep::config::tests::read_token_returns_first_non_empty_line ... ok
test native::gkeep::ledger::tests::marker_round_trips_ids_with_dots_and_exotic_bytes ... ok
test native::gkeep::migrate_tasks::tests::edits_preserve_mixed_line_endings ... ok
test native::gkeep::ledger::tests::duplicates_name_every_location ... ok
test native::gkeep::login::tests::inbox_count_handles_singular_and_plural ... ok
test native::gkeep::migrate_tasks::tests::recognizes_legacy_source_and_preserves_label_bytes ... ok
test native::gkeep::config::tests::read_token_rejects_sign_in_cookie ... ok
test native::gkeep::ledger::tests::read_target_tasks_covers_top_level_tasks_only ... ok
test native::gkeep::imports::tests::preflight_fatal_is_an_error ... ok
test native::gkeep::ledger::tests::scan_includes_done_and_skips_excluded_dirs ... ok
test native::gkeep::config::tests::read_token_rejects_empty_and_failing_commands ... ok
test native::gkeep::model::tests::archive_success_counts_archived_and_already_archived ... ok
test native::gkeep::model::tests::canonical_json_and_fingerprint_are_pinned ... ok
test native::gkeep::model::tests::note_ref_is_pinned ... ok
test native::gkeep::model::tests::fingerprint_ignores_json_key_order_and_attachments ... ok
test native::gkeep::ledger::tests::read_target_tasks_handles_missing_created_and_markers ... ok
test native::gkeep::ledger::tests::read_target_tasks_associates_new_hidden_continuation_with_task ... ok
test native::gkeep::list::source_link_tests::collapses_only_the_generated_keep_link_shape ... ok
test native::gkeep::config::tests::resolve_rejects_bad_config ... ok
test native::file_coordination::attempt::tests::timeout_cancels_and_rejects_even_a_late_callback ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_for_completed_entries ... ok
test native::gkeep::migrate_tasks::tests::plans_compact_open_source_and_keeps_closed_source_unchanged ... ok
test native::gkeep::migrate_tasks::tests::nested_closed_checkbox_blocks_parent_source_ownership ... ok
test native::gkeep::migrate_tasks::tests::inserts_bulb_before_inline_fields_and_block_id ... ok
test native::gkeep::model::tests::requests_serialize_with_protocol_and_op ... ok
test native::gkeep::model::tests::responses_parse ... ok
test native::gkeep::model::tests::unknown_attachment_kind_deserializes_to_other ... ok
test native::gkeep::plan::tests::archived_notes_get_the_archived_state ... ok
test native::gkeep::plan::tests::empty_note_is_skipped ... ok
test native::gkeep::plan::tests::fresh_note_is_new ... ok
test native::gkeep::plan::tests::id_filter_narrows_to_selected_notes ... ok
test native::gkeep::migrate_tasks::tests::rejects_ambiguous_label_delimiters_and_unsupported_source_shape ... ok
test native::gkeep::plan::tests::ledger_hit_with_same_fingerprint_is_pending ... ok
test native::gkeep::plan::tests::journal_written_record_is_a_backstop ... ok
test native::dataview::tasks::index::tests::frontmatter_is_only_a_strictly_closed_column_zero_block ... ok
test native::gkeep::plan::tests::ledger_wins_over_journal ... ok
test native::gkeep::plan::tests::limit_counts_only_actionable_notes ... ok
test native::gkeep::plan::tests::pinned_beats_pending ... ok
test native::gkeep::plan::tests::notes_order_oldest_first_with_id_tiebreak ... ok
test native::gkeep::plan::tests::pinned_and_shared_notes_stay_unless_included_or_selected ... ok
test native::gkeep::plan::tests::ref_created_journal_drives_archive_only ... ok
test native::gkeep::plan::tests::empty_id_is_unknown ... ok
test native::gkeep::plan::tests::create_ref_counts_as_actionable_for_limit ... ok
test native::gkeep::plan::tests::ledger_hit_with_other_fingerprint_is_revised ... ok
test native::gkeep::plan::tests::non_url_only_notes_stay_tasks ... ok
test native::gkeep::plan::tests::resolve_ids_prefers_exact_ids ... ok
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpgcvULr/.git/
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpzrXNs3/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpZFkpmP/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmp5GcLT6/.git/
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
hint: of your new repositories, which will suppress this warning, call:
hint:
hint:
hint: 	git config --global init.defaultBranch <name>
hint: 	git config --global init.defaultBranch <name>
hint:
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint:
hint: 	git branch -m <name>
hint: 	git branch -m <name>
hint: Using 'master' as the name for the initial branch. This default branch name
hint: is subject to change. To configure the initial branch name to use in all
hint: of your new repositories, which will suppress this warning, call:
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpF7HkeZ/.git/
hint:
hint: 	git config --global init.defaultBranch <name>
hint:
hint: Names commonly chosen instead of 'master' are 'main', 'trunk' and
hint: 'development'. The just-created branch can be renamed via this command:
hint:
hint: 	git branch -m <name>
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmp2aEprB/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpf6NK5v/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmps0CwxZ/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmphGvMRR/.git/
test native::gkeep::plan::tests::zero_width_only_text_is_empty ... ok
test native::gkeep::plan::tests::url_only_trailing_route_is_tracked_without_becoming_the_target ... ok
test native::gkeep::render::tests::capture_grammar_lookalikes_stay_literal ... ok
test native::gkeep::pull::tests::prompt_accepts_default_reprompts_unknown_and_stops_on_eof ... ok
test native::gkeep::render::tests::display_title_is_unescaped ... ok
test native::gkeep::render::tests::empty_list_falls_back_to_untitled_title ... ok
test native::gkeep::pull::tests::git_ancestor_checks_dot_git_files_and_dirs ... ok
test native::gkeep::render::tests::escape_task_text_leaves_intended_markup_alone ... ok
test native::gkeep::render::tests::decorated_description_keeps_created_field_parseable ... ok
test native::gkeep::render::tests::created_date_follows_the_configured_day_timezone ... ok
test native::gkeep::plan::tests::resolve_ids_rejects_unknown_and_ambiguous ... ok
test native::gkeep::plan::tests::url_only_body_note_becomes_create_ref ... ok
test native::gkeep::plan::tests::url_only_percent_and_at_markers_queue_listen_intent ... ok
test native::gkeep::render::tests::fallback_child_is_last_without_markers ... ok
test native::gkeep::render::tests::crlf_and_tabs_normalize ... ok
test native::gkeep::render::tests::bare_list_markers_escape ... ok
test native::gkeep::render::tests::escape_child_text_covers_both_tables ... ok
test native::gkeep::adapter::tests::spawn_sets_parent_pid_env ... ok
test native::gkeep::adapter::tests::normal_exit_with_pipe_holding_straggler_returns_quickly ... ok
test native::gkeep::plan::tests::url_only_page_title_matching_link_title_becomes_create_ref ... ok
test native::gkeep::render::tests::labels_join_the_source_line ... ok
test native::gkeep::render::tests::markdown_has_no_trailing_newline ... ok
test native::gkeep::render::tests::mixed_attachments_pluralize ... ok
test native::gkeep::render::tests::list_with_checked_nested_and_empty_items ... ok
test native::gkeep::render::tests::revision_annotates_task_description ... ok
test native::gkeep::render::tests::markdown_looking_text_is_neutralized_in_children ... ok
test native::capture_pomodoros::tests::tasks_human_output_has_agenda_rows ... ok
test native::gkeep::render::tests::source_link_escapes_title_delimiters_and_omits_blank_urls ... ok
test native::gkeep::render::tests::image_with_ocr_renders_attachment_line_and_grandchildren ... ok
test native::gkeep::render::tests::spoofed_marker_in_keep_text_cannot_survive ... ok
test native::capture_templates::store::tests::origin_replace_swaps_in_one_write_and_keeps_history ... ok
test native::gkeep::render::tests::unknown_attachment_kind_renders_as_files ... ok
test native::gkeep::ledger::tests::journal_append_writes_leading_newline_after_torn_record ... ok
test native::gkeep::render::tests::untitled_list_takes_first_item_as_title_but_keeps_it ... ok
test native::gkeep::render::tests::space_indent_uses_two_spaces ... ok
test native::gkeep::render::tests::leading_markers_cover_headings_breaks_and_fences ... ok
test native::capture_pomodoros::tests::task_link_count_reports_ten_or_more_links ... ok
test native::gkeep::tests::error_exit_codes ... ok
test native::gkeep::ui::tests::age_buckets ... ok
test native::gkeep::render::tests::source_url_spoof_cannot_plant_a_marker ... ok
test native::gkeep::render::tests::untitled_multiline_note_takes_first_line_as_title ... ok
test native::gkeep::render::tests::titled_note_renders_task_line_and_children ... ok
test native::gkeep::render::tests::task_and_block_id_and_comment_and_field_hazards_escape ... ok
test native::gkeep::render::tests::unicode_text_passes_through ... ok
test native::gkeep::ui::tests::spinner_frames_are_braille ... ok
test native::gkeep::ui::tests::spinner_start_and_drop_never_panics ... ok
test native::highlights_ref::arxiv::tests::arxiv_author_display_covers_one_two_and_three_authors ... ok
test native::highlights_ref::arxiv::tests::arxiv_parsing_matches_sase_listen_negatives ... ok
test native::highlights_ref::birth::tests::non_reread_stems_probe_nothing ... ok
test native::highlights_ref::arxiv::tests::arxiv_versions_split_and_dedupe_without_version ... ok
test native::highlights_ref::arxiv::tests::arxiv_parsing_matches_sase_listen_positives ... ok
test native::highlights_ref::clip_adapter::tests::capture_request_omits_out_pdf_when_render_is_false ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_defaults_new_render_paths ... ok
test native::highlights_ref::birth::tests::reopen_reading_comes_from_note_own_earlier ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_reads_article_json ... ok
test native::highlights_ref::clip_adapter::tests::capture_success_preserves_gist_metadata_and_provenance ... ok
test native::highlights_ref::arxiv::tests::arxiv_metadata_rejects_error_entries ... ok
test native::gkeep::adapter::tests::token_travels_on_stdin_never_argv ... ok
test native::highlights_ref::cli::tests::help_groups_cover_every_subcommand_exactly_once ... ok
test native::highlights_ref::clip_adapter::tests::compose_request_serializes_null_collection_fields ... ok
test native::highlights_ref::clip_adapter::tests::compose_success_defaults_new_render_paths ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_keeps_explicit_non_default_ports ... ok
test native::highlights_ref::clip_adapter::tests::compose_success_deserializes ... ok
test native::highlights_ref::clip_adapter::tests::diagrams_request_json_is_byte_identical ... ok
test native::highlights_ref::clip_adapter::tests::diagrams_success_deserializes_mixed_results ... ok
test native::highlights_ref::clip_adapter::tests::diagrams_timeout_uses_item_budget_unless_env_overrides ... ok
test native::highlights_ref::clip_adapter::tests::ping_response_reads_mermaid_version ... ok
test native::highlights_ref::clip_adapter::tests::single_capture_request_json_is_byte_identical ... ok
test native::highlights_ref::clip_url::tests::arxiv_spellings_share_one_dedupe_key ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_normalizes_equivalent_path_spellings ... ok
test native::highlights_ref::arxiv::tests::arxiv_metadata_parses_titles_authors_and_dates ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_keeps_delimiter_encoded_resources_distinct ... ok
test native::highlights_ref::clip_url::tests::name_validation_strips_pdf_and_rejects_junk ... ok
test native::highlights_ref::birth::tests::version_looking_pdf_without_predecessor_stays_ordinary ... ok
test native::highlights_ref::birth::tests::url_identity_derives_chain_and_reading ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_normalizes_spellings ... ok
test native::highlights_ref::birth::tests::unrelated_occupant_never_links ... ok
test native::highlights_ref::clip_url::tests::reserved_at_sign_alias_is_only_the_medium_author_sigil ... ok
test native::highlights_ref::birth::tests::chain_copies_newest_member_entries_through_dangling_gaps ... ok
test native::highlights_ref::cli::tests::help_groups_are_alphabetical_with_matching_abouts ... ok
test native::highlights_ref::collection::tests::collection_multiline_errors_style_labels_and_indexes_only ... ok
test native::highlights_ref::code_catalog::tests::build_reports_missing_and_invalid_inputs ... ok
test native::highlights_ref::birth::tests::title_identity_matches_when_no_urls ... ok
test native::highlights_ref::clip_url::tests::non_arxiv_dedupe_keys_are_unchanged ... ok
test native::highlights_ref::collection::tests::encoded_twin_spelling_overlaps_the_recorded_capture ... ok
test native::highlights_ref::collection::tests::exact_pdf_backed_collection_refuses_or_returns_attach_for_listen ... ok
test native::highlights_ref::clip_url::tests::short_title_stem_uses_the_colon_prefix_or_six_words ... ok
test native::highlights_ref::clip_url::tests::title_stem_strips_one_trailing_text_extension ... ok
test native::highlights_ref::collection::tests::legacy_overlap_is_reported_once_per_note_and_does_not_refuse ... ok
test native::highlights_ref::collection_name::tests::collection_authors_are_deduplicated_in_part_order ... ok
test native::highlights_ref::clip_url::tests::validation_accepts_mapped_public_literals ... ok
test native::highlights_ref::clip_url::tests::stem_derivation_skips_noise_segments ... ok
test native::highlights_ref::clip_url::tests::validation_accepts_public_urls_and_strips_tracking ... ok
test native::highlights_ref::collection_name::tests::collection_title_uses_shared_title_then_fallback_and_override ... ok
test native::capture_templates::store::tests::repeated_captures_dedupe_and_bump ... ok
test native::highlights_ref::clip_url::tests::validation_rejects_non_public_urls ... ok
test native::highlights_ref::collection::tests::exact_queued_collection_requires_force_for_the_planned_target ... ok
test native::highlights_ref::create::tests::audio_link_template_precedence_is_env_then_config_then_default ... ok
test native::highlights_ref::collection_name::tests::collection_published_uses_override_or_earliest_date ... ok
test native::highlights_ref::collection::tests::partial_pdf_backed_and_queued_overlap_names_every_part_and_ignores_force ... ok
test native::highlights_ref::create::tests::audio_path_components_are_percent_encoded ... ok
test native::highlights_ref::collection_name::tests::waterfall_sources_and_report_phrases_are_stable ... ok
test native::highlights_ref::collection_name::tests::no_name_hints_and_scheme_less_rows_are_exact ... ok
test native::highlights_ref::collection_name::tests::part_order_warning_only_appears_for_a_decreasing_sequence ... ok
test native::highlights_ref::collection_name::tests::one_word_gate_counts_letters_and_part_order_sees_uncapped_slug_words ... ok
test native::highlights_ref::birth::tests::deleted_root_keeps_the_original_stem_for_birth_and_reopen ... ok
test native::highlights_ref::collection_name::tests::naming_is_order_independent_and_normalizes_site_spelling ... ok
test native::highlights_ref::code_catalog::tests::build_keeps_report_records_without_matching_destinations ... ok
test native::highlights_ref::collection_name::tests::query_only_slug_needs_page_like_variation ... ok
test native::gkeep::imports::tests::preflight_allows_receipts_after_star_exception ... ok
test native::highlights_ref::create::tests::generic_diagram_text_box_matches_letter_minus_085in_margins ... ok
test native::highlights_ref::create::tests::earlier_snapshots_sort_newest_first_and_hint_unread_ready ... ok
test native::highlights_ref::collection_name::tests::required_naming_table ... ok
test native::highlights_ref::create::tests::plan_embeds_exact_output_stem_id_when_opted_in ... ok
test native::highlights_ref::create::tests::diagrams_filter_runs_first_on_generic_route ... ok
test native::highlights_ref::birth::tests::title_identity_matches_without_urls_or_source_note ... ok
test native::gkeep::ledger::tests::journal_append_round_trips_with_tight_permissions ... ok
test native::gkeep::adapter::tests::exiting_without_reading_reports_stdout_not_stdin ... ok
test native::gkeep::adapter::tests::internal_ok_false_carries_stderr_tail ... ok
test native::highlights_ref::arxiv::tests::arxiv_fetch_metadata_degrades_with_a_warning ... ok
test native::highlights_ref::create::tests::title_prefers_frontmatter_then_h1_then_stem ... ok
test native::highlights_ref::collection::tests::collection_attach_uses_the_newest_reading_in_an_exact_family ... ok
test native::gkeep::imports::tests::preflight_names_star_gitignore_rule ... ok
test native::gkeep::imports::tests::preflight_custom_excludes_file_is_named ... ok
test native::highlights_ref::diagrams::tests::fallback_note_is_compact_but_warning_keeps_full_adapter_error ... ok
[master (root-commit) adf351d] receipt
 1 file changed, 1 insertion(+)
 create mode 100644 .bob/gkeep/imports/abc.json
test native::highlights_ref::diagrams::tests::header_and_rust_height_budgets_agree ... ok
test native::gkeep::imports::tests::preflight_parent_exclusion_names_the_rule ... ok
test native::gkeep::imports::tests::preflight_negated_allowance_is_trackable ... ok
test native::highlights_ref::diagrams::tests::parse_manifest_keeps_true_first_positions_across_interleaved_duplicates ... ok
test native::highlights_ref::diagrams::tests::kill_switch_reads_off_values_through_native_env ... ok
test native::highlights_ref::diagrams::tests::scale_helpers_match_the_a8_contract ... ok
test native::gkeep::imports::tests::preflight_ignored_target_is_called_a_note ... ok
test native::highlights_ref::diagrams::tests::prescan_counts_backtick_tilde_attribute_quoted_and_list_fences ... ok
test native::highlights_ref::diagrams::tests::write_results_emits_absolute_pdf_or_error_and_null_fallback ... ok
test native::highlights_ref::doctor::tests::pdf_write_coordination_doctor_keeps_both_cfg_branches ... ok
test native::file_coordination::attempt::tests::cancellation_and_start_have_exactly_one_winner ... ok
[master (root-commit) d9f9dc5] track
 1 file changed, 1 insertion(+)
 create mode 100644 .bob/gkeep/imports/tracked.json
test native::highlights_ref::diagrams::tests::prepare_skips_adapter_when_kill_switch_or_no_candidates ... ok
test native::highlights_ref::duplicate::tests::colored_output_dims_separators_and_hints ... ok
test native::highlights_ref::duplicate::tests::family_copies_render_reading_numbers_newest_first ... ok
test native::highlights_ref::duplicate::tests::format_error_keeps_every_hint_row ... ok
test native::capture_pomodoros::tests::task_link_count_numbers_only_numbered_links ... ok
test native::highlights_ref::duplicate::tests::next_stem_is_carried_but_never_rendered ... ok
test native::highlights_ref::duplicate::tests::queued_only_renders_already_queued_with_force_remedy ... ok
test native::highlights_ref::duplicate::tests::several_copies_list_every_path_with_also_rows ... ok
test native::highlights_ref::duplicate::tests::readings_sort_before_queued_copies ... ok
test native::highlights_ref::duplicate::tests::single_captured_copy_renders_detail_and_hints ... ok
test native::gkeep::imports::tests::preflight_tracked_path_is_trackable_despite_ignore ... ok
test native::highlights_ref::duplicate::tests::from_recorded_enriches_family_readings_newest_first ... ok
test native::highlights_ref::fetch::tests::fetch_reports_a_missing_curl_with_its_hint ... ok
test native::highlights_ref::fetch::tests::curl_pins_the_checked_address_with_resolve ... ok
test native::highlights_ref::force::tests::adopted_collection_keeps_exactly_two_targets ... ok
test native::highlights_ref::fetch::tests::fetch_refuses_private_resolved_addresses_and_unlisted_hosts ... ok
test native::highlights_ref::force::tests::adoption_emptying_target_is_missing_target ... ok
test native::highlights_ref::create::tests::section_numbering_gate_off_keeps_levels ... ok
test native::highlights_ref::force::tests::adopted_mode_word_beats_the_missing_default ... ok
test native::highlights_ref::force::tests::edit_distance_basics ... ok
test native::highlights_ref::fetch::tests::curl_passes_q_as_first_argument ... ok
test native::highlights_ref::force::tests::bare_force_means_reread_wherever_it_stands ... ok
test native::highlights_ref::force::tests::bare_force_combines_with_dry_run ... ok
test native::highlights_ref::force::tests::clustered_short_ending_in_f_equals_is_explicit ... ok
test native::highlights_ref::force::tests::glued_short_value_parses_as_output ... ok
test native::highlights_ref::force::tests::invalid_equals_mode_is_a_clap_error ... ok
test native::highlights_ref::force::tests::explicit_equals_value_never_adopts ... ok
test native::highlights_ref::force::tests::guard_escapes_keep_their_meanings ... ok
test native::highlights_ref::force::tests::full_tree_indices_match_standalone ... ok
test native::highlights_ref::force::tests::plain_url_has_no_force ... ok
test native::highlights_ref::guard::tests::porcelain_status_parser_fails_closed_on_unclassifiable_records ... ok
test native::highlights_ref::guard::tests::porcelain_status_parser_keeps_both_rename_paths ... ok
test native::highlights_ref::force::tests::repeated_force_is_a_clap_usage_error ... ok
test native::highlights_ref::guard::tests::intent_write_planned_is_true_until_the_destination_contains_identity ... ok
test native::highlights_ref::guard::tests::porcelain_status_parser_preserves_quoted_and_non_ascii_paths ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::highlights_ref::ingest::tests::error_kinds_and_retryable_flags ... ok
test native::highlights_ref::ingest::tests::fetch_hint_splits_out_of_message ... ok
test native::highlights_ref::ingest::tests::fallback_note_quoting_truncation_and_escaping ... ok
test native::highlights_ref::force::tests::stray_mode_words_refuse ... ok
test native::highlights_ref::intake::tests::plan_error_with_needs_write_pdfs_code_queues_that_reason ... ok
test native::highlights_ref::ingest::tests::for_vault_agrees_with_from_matches ... ok
test native::highlights_ref::ingest::tests::ingest_default_target_reserves_reference_ids_across_types ... ok
test native::highlights_ref::intake::tests::single_unit_size_preflight_uses_vault_sync_limit ... ok
test native::highlights_ref::intake::tests::source_pointer_mismatch_names_missing_and_different_values ... ok
test native::highlights_ref::listen::tests::accepts_canonical_and_legacy_templates ... ok
test native::highlights_ref::listen::tests::blank_env_and_missing_config_mean_unset ... ok
test native::highlights_ref::intake::tests::queue_enumeration_lists_pdfs_then_late_audio_and_skips_the_rest ... ok
test native::highlights_ref::ingest::tests::already_in_library_needs_no_network ... ok
test native::highlights_ref::listen::tests::invalid_wrappers_fail_before_any_run ... ok
test native::highlights_ref::listen::tests::env_overrides_config ... ok
test native::highlights_ref::listen::tests::placeholder_values_stay_single_arguments ... ok
test native::highlights_ref::listen::tests::rejects_malformed_quoting_and_nuls ... ok
test native::highlights_ref::create::tests::section_numbering_no_manual_numbers_unchanged ... ok
test native::highlights_ref::intake::tests::single_unit_recheck_detects_pdf_sidecar_audio_and_note_collisions ... ok
test native::highlights_ref::listen::tests::rejects_partial_launcher_prefixes ... ok
test native::highlights_ref::listen::tests::rejects_quoted_placeholders ... ok
test native::highlights_ref::create::tests::section_numbering_lone_setext_h1_moves_sections_up ... ok
test native::highlights_ref::listen::tests::rejects_templates_missing_audio_or_source ... ok
test native::highlights_ref::listen::tests::rejects_shell_wrappers_chains_and_other_programs ... ok
test native::highlights_ref::listen::tests::rejects_unknown_placeholders ... ok
test native::highlights_ref::listen::tests::run_listen_accepts_mpeg_frame_sync_audio ... ok
test native::highlights_ref::listen::tests::require_reports_the_config_path_and_snippet ... ok
test native::highlights_ref::create::tests::section_numbering_lone_h1_with_only_h3_children ... ok
test native::highlights_ref::create::tests::listen_filter_keeps_glyph_without_bound_audio ... ok
test native::highlights_ref::create::tests::code_break_filter_splits_long_inline_code_paths ... ok
test native::highlights_ref::listen::tests::run_listen_validates_before_running ... ok
test native::highlights_ref::create::tests::section_numbering_lone_atx_h1_moves_sections_up ... ok
test native::highlights_ref::create::tests::section_numbering_year_led_heading_keeps_numbering ... ok
test native::highlights_ref::create::tests::section_numbering_two_h1s_keeps_levels ... ok
test native::highlights_ref::listen::tests::run_listen_reports_interrupt_exits ... ok
test native::gkeep::adapter::tests::every_request_carries_protocol_version ... ok
test native::highlights_ref::create::tests::listen_filter_renders_card_and_encoded_play_link ... ok
test native::highlights_ref::create::tests::section_numbering_mixed_doc_unnumbered_when_any_heading_numbered ... ok
test native::highlights_ref::listen::tests::run_listen_has_no_fallback_when_sase_missing ... ok
test native::highlights_ref::listen_feed::tests::feed_notice_is_none_for_empty_or_missing_outbox ... ok
test native::gkeep::imports::tests::prepared_then_verified_round_trip ... ok
test native::highlights_ref::listen_feed::tests::doctor_row_uses_configured_state_home_and_reports_queue ... ok
test native::highlights_ref::create::tests::markdown_marker_gains_return_links_only_after_paired_render ... ok
test native::gkeep::imports::tests::preflight_metadata_directories_probe_json_entries ... ok
test native::capture_pomodoros::tests::tasks_json_includes_derived_homes ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::highlights_ref::listen::tests::legacy_template_migrates_and_preserves_flags ... ok
test native::highlights_ref::listen_feed::tests::feed_notice_keeps_nonmatching_and_missing_library_entries_as_others ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::highlights_ref::create::tests::section_numbering_without_h1_numbers_from_shallowest ... ok
test native::gkeep::adapter::tests::ping_snapshot_archive_round_trip ... ok
test native::gkeep::migrate_tasks::tests::migration_journal_recovers_only_an_exact_file_post_image ... ok
test native::highlights_ref::listen::tests::run_listen_reports_failed_exits ... ok
test native::gkeep::imports::tests::matches_head_detects_committed_unchanged_receipt ... ok
test native::file_coordination::attempt::tests::running_accessor_finishes_after_budget_without_cancellation ... ok
test native::highlights_ref::listen_feed::tests::notice_lines_format_current_and_older_queues ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::gkeep::migrate_tasks::tests::marker_free_migration_keeps_the_legacy_import_store_empty ... ok
test native::highlights_ref::listen_feed::tests::notice_lines_pluralize_omit_invalid_dates_and_truncate_errors ... ok
test native::highlights_ref::marker_write::tests::coordinated_marker_action_includes_wait_and_saved_first ... ok
test native::highlights_ref::listen_feed::tests::feed_notice_matches_identical_audio_and_keeps_other_entries ... ok
test native::highlights_ref::marker_write::tests::hold_copy_and_reason_ids_match_the_contract ... ok
test native::highlights_ref::listen::tests::run_listen_writes_id3_audio_on_success ... ok
test native::highlights_ref::model::command_error_tests::human_code_is_visible_without_losing_machine_code ... ok
test native::highlights_ref::listen_feed::tests::read_outbox_skips_bad_entries_and_sorts ... ok
test native::highlights_ref::note_snapshot::assets::tests::gif_and_webp_convert_to_png_and_unsupported_or_broken_images_fail ... ok
test native::gkeep::adapter::tests::large_request_with_fast_exit_succeeds ... ok
test native::highlights_ref::note_snapshot::bob::tests::prose_and_code_mentioning_markers_stay_lists ... ok
test native::highlights_ref::note_snapshot::bob::tests::chips_cover_priority_scheduled_repeat_and_ref ... ok
test native::highlights_ref::note_snapshot::bob::tests::ordinary_host_keeps_plain_projection ... ok
test native::highlights_ref::note_snapshot::bob::tests::medium_priority_is_consumed_without_a_chip ... ok
test native::highlights_ref::note_snapshot::bob::tests::custom_settings_without_task_filter_still_chip ... ok
test native::highlights_ref::note_snapshot::bob::tests::nested_child_rows_belong_to_the_child ... ok
test native::highlights_ref::note_snapshot::bob::tests::area_host_applies_rows_to_repeated_embeds ... ok
test native::highlights_ref::note_snapshot::bob::tests::past_and_malformed_fields_stay_readable ... ok
test native::highlights_ref::note_snapshot::bob::tests::duplicate_text_with_different_fields_chips_per_row ... ok
test native::highlights_ref::note_snapshot::bob::tests::bob_kinds_all_apply_rows ... ok
test native::highlights_ref::note_snapshot::classify::tests::exact_paths_win_over_mixed_case_basename_twins ... ok
test native::highlights_ref::create::tests::section_numbering_lone_h1_with_numbered_h2s_lists_author_numbers ... ok
test native::highlights_ref::note_snapshot::bob::tests::task_source_attribution_matches_raw_bytes ... ok
test native::highlights_ref::listen::tests::run_listen_rejects_missing_and_non_mp3_audio ... ok
test native::highlights_ref::note_snapshot::bob::tests::waits_on_and_blocks_rows_keep_resolved_labels ... ok
test native::gkeep::adapter::tests::error_kinds_carry_messages_and_hints ... ok
test native::highlights_ref::note_snapshot::bob::tests::literal_code_never_mints_chips ... ok
test native::highlights_ref::note_snapshot::fonts::tests::coverage_reports_body_and_total_gaps_separately ... ok
test native::highlights_ref::note_snapshot::classify::tests::wikilink_wrappers_aliases_and_fragments_classify_the_note ... ok
test native::highlights_ref::note_snapshot::bob::tests::untagged_checkboxes_get_chips ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::bookkeeping_drops_while_unknown_fields_stay_muted ... ok
test native::highlights_ref::note_snapshot::bob::tests::six_statuses_survive_the_bob_pass ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::callouts_keep_type_title_and_body ... ok
test native::highlights_ref::note_snapshot::bob::tests::selected_section_embed_keeps_source_rows ... ok
test native::highlights_ref::note_snapshot::bob::tests::rich_inline_content_survives_chips_and_rows ... ok
test native::highlights_ref::note_snapshot::classify::tests::read_errors_are_cached_too ... ok
test native::highlights_ref::note_snapshot::classify::tests::sources_read_once_and_share_immutable_bytes ... ok
test native::highlights_ref::note_snapshot::classify::tests::missing_names_suggest_up_to_three_near_stems ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::ambiguous_notes_warn_without_choosing ... ok
test native::highlights_ref::note_snapshot::fonts::tests::bundled_faces_cover_the_snapshot_corpus ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::comments_drop_outside_code_only ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::block_excerpts_expand_nested_same_note_block_refs ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::content_links_resolve_existing_vault_files ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::embeds_use_block_excerpts_and_existing_files_become_links ... ok
test native::highlights_ref::note_snapshot::bob::tests::subprojects_marker_converts_with_closed_chips ... ok
test native::highlights_ref::note_snapshot::bob::tests::scheduled_today_and_next_year_format ... ok
test native::highlights_ref::note_snapshot::bob::tests::unresolved_targets_stay_readable ... ok
test native::highlights_ref::fetch::tests::fetch_covers_redirects_statuses_and_exit_codes ... ok
test native::capture_templates::store::tests::origin_cases_cover_same_missing_and_existing_target ... ok
test native::capture_templates::store::tests::eviction_drops_least_recently_used_and_lowered_cap_trims ... ok
test native::highlights_ref::note_snapshot::classify::tests::excluded_existing_markdown_stays_ordinary ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::bare_paths_urls_and_long_tokens_become_code_or_links ... ok
test native::highlights_ref::note_snapshot::classify::tests::default_parent_prefers_self_then_walks_eligible_ancestors ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::excerpt_cleaning_handles_unicode_before_inline_code ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::excerpt_cleaning_keeps_intraword_underscores ... ok
test native::highlights_ref::note_snapshot::classify::tests::symlink_escapes_never_become_vault_notes ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::every_checkbox_status_without_a_filter ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::excerpt_cleaning_preserves_unknown_field_meaning ... ok
test native::highlights_ref::note_snapshot::classify::tests::existing_files_keep_their_plain_routes ... ok
test native::capture_complete::tests::output::named_start_completion_carries_keeps_ledger_and_running ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::heading_without_a_blank_line_before_it ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::headings_shift_collide_and_offer_a_title ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::frontmatter_is_dropped_but_retained ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::comment_scanner_preserves_visible_text_around_multiline_comments ... ok
test native::highlights_ref::listen::tests::quiet_runner_preserves_typed_failures ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::inline_code_protects_apparent_syntax ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::images_register_widths_and_missing_placeholders ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::same_note_block_refs_use_excerpts ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::nested_children_survive_mixed_tabs_and_spaces ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::strike_plus_wikilink_keeps_links_liftable ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::keep_and_quote_decorations_become_chips ... ok
test native::highlights_ref::note_snapshot::classify::tests::default_parent_follows_subfolder_note_ancestry_and_rejects_cycles ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::missing_block_labels_do_not_emit_raw_carets ... ok
test native::highlights_ref::note_snapshot::classify::tests::kind_comes_from_cached_frontmatter_not_paths ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::nondefault_fence_lengths_stay_literal ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::status_symbols_map_through_tasks_settings ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::markdown_local_fragments_resolve_through_the_host_index ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::raw_source_metadata_survives_projection ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::queries_become_linked_placeholders_without_executing ... ok
test native::highlights_ref::create::tests::section_numbering_self_numbered_doc_prints_author_numbers_only ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::shallowest_heading_becomes_h1 ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::note_embeds_stay_structured_requests ... ok
test native::highlights_ref::note_snapshot::classify::tests::default_parent_walk_is_bounded_to_eight_ancestor_hops ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::traps_stay_literal_through_serialization ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::unicode_survives_projection_and_serialization ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::trailing_block_ids_become_task_anchors ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::missing_fragments_warn_while_keeping_the_uri ... ok
test native::highlights_ref::note_snapshot::profile::tests::first_error_excerpt_takes_ten_context_lines ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::sectioned_ref_notes_keep_headings_without_raw_section_ids ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::very_long_lines_and_missing_newlines_project ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::underscore_caret_tokens_do_not_emit_raw_carets ... ok
test native::highlights_ref::note_snapshot::plan::tests::plan_uses_one_cached_source_for_title_parent_and_projection ... ok
test native::highlights_ref::note_snapshot::profile::tests::snapshot_diagram_text_box_matches_note_geometry ... ok
test native::highlights_ref::note_snapshot::profile::tests::warnings_respect_the_20pt_boundary_and_deduplicate ... ok
test native::highlights_ref::note_snapshot::resolve::tests::attachment_index_builds_lazily_and_caches ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::wikilinks_resolve_alias_fragments_and_failures ... ok
test native::highlights_ref::note_snapshot::resolve::tests::attachment_symlink_escapes_stay_missing ... ok
test native::highlights_ref::note_snapshot::resolve::tests::fragment_comments_follow_fence_inline_code_and_visible_heading_rules ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::nested_fenced_content_without_its_opener_stays_literal ... ok
test native::highlights_ref::note_snapshot::resolve::tests::content_targets_resolve_exact_excluded_non_markdown_files ... ok
test native::highlights_ref::note_snapshot::resolve::tests::same_note_fragments_resolve_to_the_host ... ok
test native::highlights_ref::note_snapshot::resolve::tests::note_resolution_prefers_exact_paths_then_unique_basenames ... ok
test native::highlights_ref::note_snapshot::plan::tests::plan_title_precedence_keeps_frontmatter_heading_and_exact_override ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::task_source_records_keep_comments_fields_indentation_and_callout_offsets ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::remote_and_malformed_image_lines_always_make_bounded_progress ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::path_qualified_unique_markdown_and_exact_pdf_content_links_resolve ... ok
test native::highlights_ref::note_snapshot::profile::tests::missing_package_hint_and_absent_log_fallback ... ok
test native::highlights_ref::note_snapshot::obsidian::tests::syntax_coverage_golden ... ok
test native::highlights_ref::note_snapshot::resolve::tests::link_targets_split_wrapper_alias_and_fragment ... ok
test native::highlights_ref::note_snapshot::resolve::tests::snapshot_uris_match_audio_uri_encoding ... ok
test native::highlights_ref::note_snapshot::resolve::tests::template_precedence_is_env_then_config_then_default ... ok
test native::highlights_ref::note_snapshot::resolve::tests::fragment_extents_cover_headings_blocks_and_paragraphs ... ok
test native::highlights_ref::note_snapshot::resolve::tests::width_hints_convert_on_the_shared_print_measure ... ok
test native::highlights_ref::note_snapshot::resolve::tests::content_targets_resolve_unique_excluded_files ... ok
test native::highlights_ref::note_snapshot::resolve::tests::attachment_precedence_is_exact_then_note_dir_then_basename ... ok
test native::highlights_ref::note_snapshot::resolve::tests::content_targets_resolve_path_qualified_unique_markdown ... ok
test native::highlights_ref::note_snapshot::tests::generated_view_golden_has_an_explicit_update_switch ... ok
test native::highlights_ref::note_snapshot::resolve::tests::attachment_width_hints_and_asset_registration ... ok
test native::highlights_ref::note_snapshot::tests::escaping_caps_image_width_and_keeps_authored_code_fences_intact ... ok
test native::highlights_ref::note_snapshot::tests::serializer_matches_the_hand_authored_complete_contract ... ok
test native::highlights_ref::note_snapshot::tests::serialized_internal_links_resolve_only_to_final_visible_anchors ... ok
test native::highlights_ref::note_snapshot::resolve::tests::excluded_notes_never_answer_content_links ... ok
test native::highlights_ref::note_snapshot::tests::raw_source_metadata_and_task_bodies_survive_in_the_separate_source_record ... ok
test native::highlights_ref::note_snapshot::tests::strike_serialization_never_places_links_inside_strike_nodes ... ok
test native::highlights_ref::note_snapshot::tests::internal_links_without_a_final_visible_anchor_become_plain_labels ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::explicit_ambiguous_self_headings_and_blocks_never_invent_targets ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::full_heading_and_block_embeds_project_selected_content ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::direct_self_and_multinote_cycles_become_links_and_nested_embeds_stop ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_closed_appendix_source_order ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_relationship_child_once ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::bob_project_masthead_and_sections_are_composed_from_synthetic_source ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_nested_self_omission ... ok
test native::highlights_ref::guard::tests::git_status_keeps_staged_untracked_quoted_and_renamed_targets_exact ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::missing_and_ambiguous_fragments_fall_back_without_fake_anchors ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::complete_transclusion_projection_matches_a_generated_golden ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::prj_is_blocked_and_open_deps_stay_waiting_on ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_inline_embed_policy ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::generated_markdown_badge_row_is_dropped ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::repeated_selected_embeds_namespace_prose_and_list_block_anchors ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_comment_fields_hidden ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::same_note_block_embeds_and_transcluded_tasks_resolve_existing_files ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::repeated_embeds_namespace_colliding_headings_and_task_ids ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::source_block_anchors_are_emitted_for_headings_prose_and_lists ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::ordinary_control_and_repeated_selected_embeds_keep_their_own_policy ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::terminal_project_prj_dek_strips_wikilink_syntax ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::terminal_project_without_prj_uses_frontmatter_and_keeps_unrelated_prose ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::source_bytes_and_block_excerpts_stay_consistent_after_file_mutation ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::scheduled_rows_group_this_week_this_month_and_later ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::same_note_block_refs_label_excerpts_on_relationship_rows ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::source_cache_reads_root_and_repeated_embed_once_and_projection_is_read_only ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_parent_readable_title ... ok
test native::highlights_ref::note_snapshot::visibility::tests::cancel_log_stays_off_open_tasks ... ok
test native::highlights_ref::note_snapshot::visibility::tests::counting_loader_reads_each_canonical_source_once ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::land_audit_terminal_outcome_cancel_history ... ok
test native::highlights_ref::note_snapshot::visibility::tests::include_closed_prints_full_logs_on_open_and_closed_tasks ... ok
test native::highlights_ref::note_snapshot::visibility::tests::done_and_canceled_heading_drops_and_keeps_prose ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::exact_size_and_line_limits_are_allowed_and_each_limit_is_enforced ... ok
test native::highlights_ref::note_snapshot::visibility::tests::nested_closed_do_not_escape_or_duplicate ... ok
test native::highlights_ref::note_snapshot::visibility::tests::omitting_closed_embedded_task_drops_its_empty_list_item ... ok
test native::highlights_ref::overwrite::archive::tests::allocation_skips_each_companion_and_same_day_collisions ... ok
test native::highlights_ref::overwrite::archive::tests::reader_skips_unsafe_and_mismatched_archive_paths ... ok
test native::highlights_ref::note_snapshot::visibility::tests::source_bytes_and_hashes_are_unchanged ... ok
test native::highlights_ref::note_snapshot::visibility::tests::ordinary_notes_keep_closed_tasks ... ok
test native::highlights_ref::note_snapshot::visibility::tests::omitted_and_restored_targets_rewrite_links ... ok
test native::highlights_ref::overwrite::execute::tests::changed_title_without_old_suffix_adds_none ... ok
test native::highlights_ref::note_snapshot::visibility::tests::include_closed_prints_full_kept_rows_and_hides_them_on_closed_tasks ... ok
test native::highlights_ref::overwrite::archive::tests::reader_uses_earlier_and_parent_not_unrelated_hashes ... ok
test native::highlights_ref::note_snapshot::visibility::tests::rotten_logs_condense_to_a_kept_row_and_count_entries ... ok
test native::highlights_ref::note_snapshot::visibility::tests::source_note_library_pdf_does_not_warn ... ok
test native::highlights_ref::note_snapshot::visibility::tests::schedule_and_work_logs_condense_and_count_entries ... ok
test native::highlights_ref::note_snapshot::visibility::tests::include_closed_restores_appendix_with_date_chips ... ok
test native::highlights_ref::note_snapshot::visibility::tests::six_statuses_omit_closed_in_reading_mode ... ok
test native::highlights_ref::note_snapshot::visibility::tests::self_snapshot_false_positives_stay_visible ... ok
test native::highlights_ref::note_snapshot::visibility::tests::self_snapshot_ref_is_omitted_in_both_modes ... ok
test native::highlights_ref::overwrite::execute::tests::note_local_frontmatter_drops_source_markdown_when_replacing ... ok
test native::highlights_ref::overwrite::execute::tests::note_local_frontmatter_keeps_created_lineage_and_custom_fields ... ok
test native::highlights_ref::ingest::tests::second_ingest_waits_for_the_lock ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::area_projection_keeps_blocked_ticklers_and_condenses_long_histories ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::inline_embeds_and_images_expand_inside_prose_tasks_and_lists ... ok
test native::highlights_ref::note_snapshot::fonts::tests::write_fonts_materializes_every_embedded_face ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::prelude_heading_uses_a_collision_safe_emitted_id ... ok
test native::highlights_ref::note_snapshot::tests::pandoc_parses_the_complete_contract_as_markdown_ast_when_available ... ok
test native::highlights_ref::overwrite::execute::tests::task_title_and_status_edits_preserve_other_task_content ... ok
test native::highlights_ref::note_snapshot::fonts::tests::bundled_font_hashes_match_the_release_manifest ... ok
test native::highlights_ref::overwrite::execute::tests::unchanged_title_keeps_task_subtree_byte_identical ... ok
test native::highlights_ref::note_snapshot::transclusion::tests::generated_three_hundred_task_projection_has_stable_counts_and_order ... ok
test native::highlights_ref::note_snapshot::profile::tests::pandoc_keeps_struck_code_and_fallback_glyphs_renderable ... ok
test native::highlights_ref::create::tests::section_numbering_contents_kept_only_when_listed ... ok
test native::highlights_ref::overwrite::execute::tests::named_member_missing_after_pre_sync_aborts ... ok
test native::highlights_ref::overwrite::recovery::tests::bogus_base_preserves_the_intent ... ok
test native::highlights_ref::overwrite::execute::tests::pre_sync_later_reading_aborts_default_selection ... ok
test native::highlights_ref::overwrite::recovery::tests::committed_annotated_intent_keeps_archive_and_later_saves ... ok
test native::highlights_ref::overwrite::recovery::tests::annotated_pdf_and_assets_reverse_after_crash ... ok
test native::highlights_ref::overwrite::execute::tests::pre_sync_byte_change_aborts_with_preimage_changed ... ok
test native::gkeep::adapter::tests::crash_garbage_and_timeout ... ok
test native::highlights_ref::overwrite::recovery::tests::committed_without_recorded_sha_still_retains ... ok
test native::highlights_ref::overwrite::execute::tests::changed_marker_during_coordination_is_a_specific_hold ... ok
test native::highlights_ref::overwrite::recovery::tests::committed_intent_is_retained_and_cleared ... ok
test native::highlights_ref::note_snapshot::profile::tests::pandoc_maps_every_contract_construct_to_tex ... ok
test native::highlights_ref::diagrams::tests::prepare_adapter_crash_writes_fallback_and_keeps_filter ... ok
test native::highlights_ref::overwrite::recovery::tests::dry_run_is_read_only_and_reports_recovery_required ... ok
test native::highlights_ref::overwrite::recovery::tests::created_directories_keep_unrecorded_contents ... ok
test native::highlights_ref::overwrite::recovery::tests::missing_vault_has_no_pending_intent ... ok
test native::highlights_ref::diagrams::tests::collect_finds_mermaid_fences_in_definition_lists ... ok
test native::highlights_ref::diagrams::tests::swap_preserves_identifier_and_drops_source_in_native ... ok
test native::highlights_ref::overwrite::recovery::tests::malformed_intent_fails_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::platform_reverse_notifies_inverse_with_replacement_present_or_absent ... ok
test native::highlights_ref::overwrite::recovery::tests::crash_between_pdf_and_assets_moves_recovers_both ... ok
test native::highlights_ref::overwrite::recovery::tests::crash_before_any_rename_restores_without_reversal ... ok
test native::highlights_ref::overwrite::recovery::tests::platform_reverse_refuses_a_changed_archive_without_deleting_replacement ... ok
test native::highlights_ref::overwrite::recovery::tests::rename_no_clobber_refuses_an_existing_destination ... ok
test native::highlights_ref::overwrite::recovery::tests::live_path_late_edit_fails_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::late_archive_save_fails_closed ... ok
test native::highlights_ref::overwrite::execute::tests::annotated_coordination_hold_writes_nothing_and_has_retry_hint ... ok
test native::highlights_ref::diagrams::tests::swap_error_emits_italic_note_then_source ... ok
test native::highlights_ref::overwrite::recovery::tests::duplicated_original_on_both_endpoints_removes_the_copy ... ok
test native::highlights_ref::overwrite::recovery::tests::moved_vault_preserves_the_intent_without_touching_files ... ok
test native::highlights_ref::overwrite::recovery::tests::validated_paths_rejects_empty_curdir_and_dot_components ... ok
test native::highlights_ref::overwrite::execute::tests::named_member_still_selected_after_pre_sync ... ok
test native::highlights_ref::overwrite::execute::tests::crash_without_rollback_is_recovered_to_the_old_state ... ok
test native::highlights_ref::overwrite::execute::tests::overwrite_commits_when_pre_sync_leaves_selection_unchanged ... ok
test native::highlights_ref::overwrite::tests::annotated_execution_requires_macos_and_enabled_coordination ... ok
test native::highlights_ref::overwrite::recovery::tests::invalid_paths_fail_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::unsupported_schema_version_fails_closed ... ok
test native::highlights_ref::overwrite::tests::frozen_archive_neutralizes_legacy_tracker_with_external_task ... ok
test native::highlights_ref::overwrite::tests::frozen_annotated_note_keeps_anchors_rewrites_assets_and_records_pdf ... ok
test native::highlights_ref::overwrite::tests::frozen_frontmatter_keeps_source_markdown_pointer ... ok
test native::highlights_ref::overwrite::tests::frozen_frontmatter_keeps_source_url_yaml_collection_type ... ok
test native::highlights_ref::overwrite::tests::open_annotation_task_in_highlights_region_is_refused ... ok
test native::highlights_ref::overwrite::tests::open_note_tasks_ignores_comments_and_fenced_examples ... ok
test native::highlights_ref::overwrite::tests::prose_comparison_ignores_managed_regions_and_tracker ... ok
test native::highlights_ref::overwrite::tests::repeated_archive_lineage_stays_newest_first ... ok
test native::highlights_ref::overwrite::tests::selection_does_not_allocate_a_reread_number ... ok
test native::highlights_ref::overwrite::tests::tracker_neutralization_cannot_leave_a_checkbox_task_source ... ok
test native::highlights_ref::overwrite::tests::frozen_v2_note_replaces_only_the_managed_reading_embed ... ok
test native::highlights_ref::pdf_links::tests::adjacent_same_uri_items_stay_separate_and_missing_links_stay_pageless ... ok
test native::highlights_ref::pdf_links::tests::matches_wrapped_pieces_and_page_spanning_pieces ... ok
test native::highlights_ref::pdf_links::tests::percent_decodes_only_after_exact_match_search ... ok
test native::highlights_ref::overwrite::tests::archive_path_suffixes_same_day_collisions ... ok
test native::highlights_ref::pdf_dests::tests::reads_chrome_catalog_dests_with_tree_precedence ... ok
test native::highlights_ref::pdf_meta::tests::info_metadata_accepts_plausible_values ... ok
test native::highlights_ref::overwrite::tests::annotated_plan_fingerprints_rewrites_assets_and_archive_destinations ... ok
test native::highlights_ref::diagrams::tests::collect_finds_attribute_and_nested_fences_on_both_readers ... ok
test native::highlights_ref::pdf_write_policy::tests::parses_lsappinfo_front_output ... ok
test native::highlights_ref::pdf_write_policy::tests::parses_ioreg_idle_time_nanoseconds ... ok
test native::highlights_ref::pdf_write_policy::tests::policy_applies_budget_overrides_once_from_config ... ok
test native::highlights_ref::pdf_write_policy::tests::probe_overrides_classify_frontmost_app_and_failures ... ok
test native::highlights_ref::recapture::tests::allocation_skips_occupied_and_refuses_at_cap ... ok
test native::highlights_ref::overwrite::recovery::tests::user_created_destination_fails_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::reverse_coordination_failure_fails_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::unexpected_new_asset_fails_closed ... ok
test native::highlights_ref::overwrite::execute::tests::commit_reported_as_error_keeps_the_commit ... ok
test native::highlights_ref::recapture::tests::free_title_stem_is_an_ordinary_capture ... ok
test native::highlights_ref::recapture::tests::defaults_come_from_the_newest_located_task ... ok
test native::highlights_ref::recapture::tests::attach_hit_follows_the_family_to_its_newest_reading ... ok
test native::highlights_ref::recapture::tests::exact_family_wins_over_a_larger_overlapping_collection ... ok
test native::highlights_ref::recapture::tests::exact_set_multi_reading_family_counts_as_one ... ok
test native::highlights_ref::recapture::tests::dangling_middle_member_keeps_max_reading ... ok
test native::highlights_ref::recapture::tests::legacy_only_hits_are_not_family_roots ... ok
test native::highlights_ref::recapture::tests::name_outside_the_family_refuses_with_expected_pattern ... ok
test native::highlights_ref::recapture::tests::deleted_family_root_is_recovered_from_the_oldest_lineage_entry ... ok
test native::highlights_ref::recapture::tests::occupancy_covers_sidecars_audio_assets_and_ids ... ok
test native::highlights_ref::recapture::tests::output_on_a_captured_reread_names_the_allocated_stem ... ok
test native::highlights_ref::recapture::tests::one_url_into_a_collection_is_a_partial_overlap ... ok
test native::gkeep::adapter::tests::timeout_kills_grandchild_holding_stdout ... ok
test native::highlights_ref::recapture::tests::natural_version_root_keeps_its_full_stem ... ok
test native::highlights_ref::recapture::tests::no_force_output_keeps_the_normal_family_refusal ... ok
test native::highlights_ref::overwrite::recovery::tests::reverse_rename_never_replaces_a_destination_that_appears_late ... ok
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpOrpB69/.git/
test native::highlights_ref::pdf_meta::tests::info_titles_reject_junk ... ok
test native::highlights_ref::recapture::tests::queued_only_matches_stay_queued ... ok
test native::highlights_ref::recapture::tests::report_line_covers_every_detail_row ... ok
test native::highlights_ref::reference_mutation::tests::dirty_touched_paths_without_git_are_empty ... ok
test native::highlights_ref::reference_mutation::tests::display_paths_joins_vault_paths ... ok
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpgoEKgZ/.git/
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpTnnBK5/.git/
test native::highlights_ref::overwrite::execute::tests::unrelated_staged_and_dirty_files_survive_abort ... ok
test native::highlights_ref::recapture::tests::single_url_selects_a_family_of_one ... ok
test native::highlights_ref::diagrams::tests::absent_or_corrupt_results_leave_latex_unchanged ... ok
test native::highlights_ref::recapture::tests::partial_overlap_count_is_distinct_urls_not_families ... ok
test native::highlights_ref::reference_mutation::tests::intake_query_matches_xlib_absolute_and_relative_paths ... ok
test native::highlights_ref::overwrite::execute::tests::post_sync_failure_keeps_the_commit_and_sets_push_pending ... ok
test native::highlights_ref::recapture::tests::v2_v4_occupancy_yields_v5 ... ok
test native::highlights_ref::recapture::tests::unrelated_same_identity_families_are_ambiguous ... ok
Initialized empty Git repository in /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261028_104756/.tmpfFuP1q/.git/
test native::highlights_ref::recapture::tests::same_stem_across_types_stays_ambiguous ... ok
test native::highlights_ref::reference_mutation::tests::legacy_paths_are_recognized_by_ref_type ... ok
test native::highlights_ref::reference_mutation::tests::vault_path_joins_components_with_slashes ... ok
test native::highlights_ref::reference_mutation::tests::rollback_moves_reports_missing_and_occupied_sources ... ok
test native::highlights_ref::recapture::tests::family_of_three_orders_newest_first ... ok
test native::highlights_ref::reference_mutation::tests::restore_bytes_leaves_concurrent_changes ... ok
test native::highlights_ref::overwrite::recovery::tests::previous_same_stem_commit_is_not_clobbered_by_rollback ... ok
test native::highlights_ref::reference_mutation::tests::rollback_moves_reverses_successful_renames ... ok
test native::highlights_ref::overwrite::recovery::tests::malformed_move_evidence_fails_closed ... ok
test native::highlights_ref::overwrite::recovery::tests::recovery_removes_unpublished_atomic_write_temps ... ok
test native::gkeep::adapter::tests::large_request_with_hanging_adapter_times_out ... ok
test native::highlights_ref::recapture::tests::real_later_reading_rereads_beside_its_root ... ok
test native::highlights_ref::rename::links::tests::highlight_fragments_rewrite_only_h_anchors_and_qualify_bare_targets ... ok
test native::highlights_ref::rename::links::tests::handles_dotted_stems_and_percent_encoded_markdown_paths ... ok
test native::highlights_ref::reference_mutation::tests::restore_bytes_restores_uncontended_after_image ... ok
test native::highlights_ref::reference_mutation::tests::managed_highlight_inspection_sees_live_and_removed_blocks ... ok
test native::highlights_ref::rename::links::tests::markdown_highlight_fragments_are_reported_and_code_targets_are_untouched ... ok
test native::highlights_ref::overwrite::recovery::tests::reverse_hash_is_rechecked_inside_the_accessor ... ok
test native::highlights_ref::reference_mutation::tests::dirty_touched_paths_exact_ignores_descendants ... ok
test native::highlights_ref::rename::links::tests::known_highlight_anchors_leave_dangling_links_unchanged ... ok
test native::highlights_ref::rename::links::tests::preserves_highlight_follow_up_findings_without_touching_hash_identity_text ... ok
test native::highlights_ref::rename::links::tests::rewrites_section_block_and_heading_links_with_the_note ... ok
test native::highlights_ref::rename::links::tests::rewrites_unique_bare_markdown_note_links_and_reports_ambiguous_ones ... ok
test native::highlights_ref::overwrite::execute::tests::annotated_overwrite_moves_bundle_and_merges_task_link_edit_once ... ok
test native::highlights_ref::rename::links::tests::rewrites_wikilinks_embeds_fragments_aliases_and_companion_links ... ok
test native::highlights_ref::rename::links::tests::rewrites_unique_bare_note_links_and_reports_ambiguous_ones ... ok
test native::highlights_ref::rename::links::tests::highlight_fragments_leave_ambiguous_bare_targets_unresolved ... ok
test native::highlights_ref::reference_mutation::tests::ignored_paths_under_lists_gitignored_sidecar_files ... ok
test native::highlights_ref::rename::plan::tests::coordinated::refusal_renders_in_human_and_json ... ok
test native::highlights_ref::rename::plan::tests::own_frontmatter_rewrite_changes_only_managed_path_fields ... ok
test native::highlights_ref::rename::plan::tests::reference_id_allocator_keeps_an_already_allocated_suffix ... ok
test native::highlights_ref::rename::links::tests::skips_inline_and_fenced_code_and_scans_frontmatter_done_and_daily_notes ... ok
test native::highlights_ref::rename::plan::tests::reference_id_allocator_skips_suffixed_ids_and_stems ... ok
test native::highlights_ref::rename::plan::tests::reference_id_frontmatter_rewrite_replaces_the_whole_value_and_quotes_numbers ... ok
test native::highlights_ref::overwrite::execute::tests::failed_annotated_transaction_reverses_the_pdf_move_inside_accessor ... ok
test native::highlights_ref::rename::plan::tests::same_stem_rows_allocate_the_suffix_only_for_the_repaired_duplicate ... ok
test native::highlights_ref::rename::plan::tests::reference_id_allocator_uses_ids_case_insensitively ... ok
test native::highlights_ref::render_tex::tests::header_packages_are_all_declared ... ok
test native::highlights_ref::render_tex::tests::missing_packages_returns_rest_in_order ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_listed_package ... ok
test native::highlights_ref::render_tex::tests::install_command_deduplicates_tlmgr_names ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_missing_xelatex ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_unlisted_file ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_unrelated_error ... ok
test native::highlights_ref::overwrite::recovery::tests::version_one_intent_without_moves_recovers_as_before ... ok
test native::highlights_ref::overwrite::execute::tests::after_note_failpoint_removes_new_store_and_restores_pointer ... ok
test native::highlights_ref::return_links::tests::filter_leaves_listen_cards_untouched ... ok
test native::highlights_ref::return_links::tests::filter_leaves_image_description_spans_untagged ... ok
test native::highlights_ref::return_links::tests::filter_numbers_github_duplicates_and_rejects_ambiguous_aliases ... ok
test native::highlights_ref::return_links::tests::filter_keeps_every_anchor_paired_with_exactly_one_pill ... ok
test native::highlights_ref::return_links::tests::filter_leaves_non_capable_targets_untagged ... ok
test native::highlights_ref::return_links::tests::filter_leaves_skip_context_links_untagged ... ok
test native::highlights_ref::return_links::tests::filter_counts_tags_in_bijective_base_23 ... ok
test native::highlights_ref::reference_mutation::tests::unstage_paths_clears_only_the_listed_paths ... ok
test native::highlights_ref::return_links::tests::filter_counts_rendered_cite_content_not_metadata ... ok
test native::highlights_ref::overwrite::recovery::tests::restore_skips_paths_absent_from_the_base_commit ... ok
test native::highlights_ref::return_links::tests::filter_renders_dead_links_as_plain_text ... ok
test native::highlights_ref::return_links::tests::filter_renumbers_anchors_on_prefix_collision ... ok
test native::highlights_ref::return_links::tests::filter_prefers_real_ids_over_aliases ... ok
test native::highlights_ref::overwrite::recovery::tests::wrong_subject_expected_head_rolls_back ... ok
test native::highlights_ref::return_links::tests::links_line_covers_every_variant ... ok
test native::highlights_ref::return_links::tests::report_parses_full_contract ... ok
test native::highlights_ref::return_links::tests::report_defaults_missing_lists_and_enabled ... ok
test native::highlights_ref::overwrite::recovery::tests::reverse_coordination_hold_then_retry_recovers ... ok
test native::highlights_ref::return_links::tests::read_report_rejects_wrong_version_and_bad_json ... ok
test native::highlights_ref::return_links::tests::report_parses_opt_out ... ok
test native::highlights_ref::return_links::tests::strip_flag_reads_return_links_marker_value ... ok
test native::highlights_ref::return_links::tests::tag_glyphs_match_filter_mod_table ... ok
test native::highlights_ref::return_links::tests::warnings_cover_every_variant ... ok
test native::highlights_ref::scan_json::tests::section_fields_are_omitted_when_zero ... ok
test native::highlights_ref::scan_json::tests::section_fields_are_present_when_nonzero ... ok
test native::highlights_ref::source_store::tests::layout_pointer_and_hash_are_content_addressed ... ok
test native::highlights_ref::source_store::tests::code_summary_covers_catalog_shapes ... ok
test native::highlights_ref::source_store::tests::stored_catalog_tolerates_missing_links_array ... ok
test native::highlights_ref::source_store::tests::link_summary_ranks_sites_by_frequency ... ok
test native::highlights_ref::sources::tests::marker_url_lists_are_expanded_for_dedupe_and_intake_lookup ... ok
test native::highlights_ref::sources::tests::non_arxiv_keys_pass_through_unchanged ... ok
test native::highlights_ref::sources::tests::legacy_only_notes_warn_instead_of_refusing ... ok
test native::highlights_ref::overwrite::recovery::tests::rollback_restores_half_written_files_and_removes_creations ... ok
test native::highlights_ref::sources::tests::pdf_backed_note_still_refuses_beside_a_legacy_only_note ... ok
test native::highlights_ref::sources::tests::reserved_at_sign_off_medium_is_a_distinct_capture ... ok
test native::highlights_ref::sources::tests::twin_path_spelling_refuses_as_already_captured ... ok
test native::highlights_ref::return_links::tests::filter_pairs_links_from_prose_list_cell_and_footnote ... ok
test native::highlights_ref::return_links::tests::filter_treats_nested_heading_spans_as_skip_contexts ... ok
test native::highlights_ref::stamp::tests::default_target_chains_to_3_when_2_is_taken ... ok
test native::highlights_ref::return_links::tests::filter_resolves_decoded_and_github_aliases ... ok
test native::highlights_ref::stamp::tests::default_target_collision_walk_covers_other_ref_type_directories ... ok
test native::highlights_ref::return_links::tests::filter_opt_out_returns_the_document_unchanged ... ok
test native::highlights_ref::return_links::tests::filter_places_div_span_and_needspace_rows ... ok
test native::highlights_ref::stamp::tests::default_target_derives_ref_type_output_and_valid_marker ... ok
test native::highlights_ref::stamp::tests::default_target_collision_walk_reserves_ids_from_other_ref_types ... ok
test native::highlights_ref::stamp::tests::default_target_free_base_has_no_rename ... ok
test native::highlights_ref::return_links::tests::filter_treats_table_head_foot_spans_as_skip_contexts ... ok
test native::highlights_ref::sources::tests::block_list_note_urls_participate_in_import_dedupe ... ok
test native::highlights_ref::reference_mutation::tests::git_head_and_committed_despite_error_read_the_latest_subject ... ok
test native::highlights_ref::stamp::tests::default_target_rejects_bad_stem_and_ref_type ... ok
test native::highlights_ref::sources::tests::list_valued_note_urls_participate_in_import_dedupe ... ok
test native::highlights_ref::stamp::tests::default_target_url_identity_matches_intake_or_ref_note ... ok
test native::highlights_ref::stamp::tests::exact_external_target_does_not_invent_library_destination ... ok
test native::highlights_ref::stamp::tests::exact_intake_still_refuses_mirrored_library_pdf_with_force ... ok
test native::highlights_ref::stamp::tests::exact_intake_refuses_mirrored_library_sidecar ... ok
test native::highlights_ref::stamp::tests::exact_output_accepts_uppercase_pdf_extension ... ok
test native::highlights_ref::stamp::tests::exact_library_target_requires_force_and_skips_mirrored_check ... ok
test native::highlights_ref::sources::tests::pdf_backed_legacy_url_notes_are_recorded_and_still_refuse ... ok
test native::highlights_ref::stamp::tests::exact_output_classifies_direct_library_target ... ok
test native::highlights_ref::stamp::tests::default_target_suffixes_each_occupant_kind ... ok
test native::highlights_ref::overwrite::execute::tests::task_edit_and_verification_match_the_exact_reading_block_id ... ok
test native::highlights_ref::stamp::tests::exact_output_resolves_relative_and_tilde_paths ... ok
test native::highlights_ref::stamp::tests::exact_output_does_not_treat_sibling_prefix_as_managed ... ok
test native::highlights_ref::stamp::tests::marker_rejects_wikilink_parent_and_unknown_status ... ok
test native::highlights_ref::stamp::tests::exact_output_rejects_non_pdf_paths ... ok
test native::highlights_ref::stamp::tests::normalize_lexically_drops_dot_and_parent_components ... ok
test native::highlights_ref::stamp::tests::exact_output_refuses_same_stem_markdown_sidecar_even_with_force ... ok
test native::highlights_ref::stamp::tests::marker_extras_insert_in_canonical_order_and_skip_empty ... ok
test native::highlights_ref::stamp::tests::source_note_marker_requires_a_bare_route_without_suffix_or_fragment ... ok
test native::highlights_ref::stamp::tests::marker_return_links_key_orders_after_captured_and_round_trips ... ok
test native::highlights_ref::stamp::tests::exact_output_keeps_nested_path_and_filename ... ok
test native::highlights_ref::tests::audio::audio_embed_inserts_after_ref_child_lines ... ok
test native::highlights_ref::tests::audio::companion_extensions_prefer_mp3_then_later_types ... ok
test native::highlights_ref::tests::audio::command_managed_audio_is_quoted_wikilink_and_omitted_without_companion ... ok
test native::highlights_ref::tests::audio::audio_library_root_prefers_env_then_config_then_xdg_then_home ... ok
test native::highlights_ref::tests::audio::default_note_body_embeds_audio_between_task_and_highlights ... ok
test native::highlights_ref::tests::audio::episode_id_validation_rejects_dot_dot_slash_and_underscore ... ok
test native::highlights_ref::tests::audio::execute_xlib_intake_counting_omits_failed_main_rename ... ok
test native::highlights_ref::tests::audio::episode_audio_source_resolves_bare_filename_only ... ok
test native::highlights_ref::tests::audio::execute_xlib_intake_counting_reports_pdf_when_companion_fails ... ok
test native::highlights_ref::tests::audio::episode_audio_source_rejects_traversal_and_missing_files ... ok
test native::highlights_ref::tests::audio::existing_note_inserts_embed_once_when_audio_field_is_absent ... ok
test native::highlights_ref::tests::audio::existing_note_skips_embed_when_audio_field_already_present ... ok
test native::highlights_ref::tests::audio::narration_script_candidate_strips_final_suffix ... ok
test native::highlights_ref::tests::audio::frontmatter_episode_id_parses_nested_audio_key ... ok
test native::highlights_ref::tests::audio::explicit_audio_validation_rejects_missing_and_bad_extension ... ok
test native::highlights_ref::overwrite::execute::tests::annotated_overwrite_rollback_keeps_vault_relative_paths_through_symlinked_parent ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_leaves_audio_without_any_pdf ... ok
test native::highlights_ref::stamp::tests::default_target_different_library_suffixes ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_moves_same_stem_audio_with_pdf ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_late_pairs_orphan_audio_to_library_pdf ... ok
test native::highlights_ref::tests::continuations::continuation_grammar_table ... ok
test native::highlights_ref::tests::continuations::continuation_group_page_labels ... ok
test native::highlights_ref::tests::continuations::continuation_page_index_boundary_never_joins_on_overflow ... ok
test native::highlights_ref::tests::continuations::continuation_dangling_and_literal_notes ... ok
test native::highlights_ref::tests::continuations::continuation_planner_chains_and_skips ... ok
test native::highlights_ref::tests::continuations::continuation_report_lines_cover_merged_and_dangling ... ok
test native::highlights_ref::tests::continuations::continuation_page_index_parsing ... ok
test native::highlights_ref::tests::audio::script_hash_lookup_prefers_newest_created_at ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_reports_audio_destination_conflicts ... ok
test native::highlights_ref::tests::continuations::continuation_image_notes_embed_under_the_group ... ok
test native::highlights_ref::tests::continuations::continuation_seams_and_quote_assembly ... ok
test native::highlights_ref::stamp::tests::default_target_does_not_skip_past_same_at_2 ... ok
test native::highlights_ref::tests::continuations::continuation_short_page_labels_merge_into_plural_group ... ok
test native::highlights_ref::tests::continuations::continuation_tasks_keep_piece_identity ... ok
test native::highlights_ref::tests::continuations::continuation_identity_toggle_is_stable ... ok
test native::highlights_ref::tests::continuations::skipped_items_render_after_the_group ... ok
test native::highlights_ref::tests::continuations::same_page_and_ellipsis_markers_keep_piece_boundaries_without_gaps ... ok
test native::highlights_ref::tests::continuations::continuation_round_trip_group_and_stub ... ok
test native::highlights_ref::tests::highlight_identity::heading_shaped_quote_wrap_remints_highlight_id ... ok
test native::highlights_ref::tests::continuations::legacy_hyphen_seam_migrates_through_legacy_full_text ... ok
test native::highlights_ref::tests::highlight_identity::color_grouped_quote_fix_remints_highlight_id ... ok
test native::highlights_ref::tests::image_notes::image_note_dest_path_is_deterministic_and_sanitized ... ok
test native::highlights_ref::tests::image_notes::existing_copy_with_missing_source_still_embeds ... ok
test native::highlights_ref::tests::image_notes::parse_image_note_line_heic_is_unsupported ... ok
test native::highlights_ref::tests::image_notes::parse_image_note_line_accepts_grammar_table ... ok
test native::highlights_ref::tests::image_notes::block_ids_and_tasks_ignore_image_note_lines ... ok
test native::highlights_ref::tests::continuations::legacy_fused_group_migrates_without_id_churn_or_tombstones ... ok
test native::highlights_ref::stamp::tests::stamp_install_appends_when_annots_exist_and_sets_partial_info ... ok
test native::highlights_ref::tests::image_notes::parse_image_note_line_rejects_prose_relative_and_non_image ... ok
test native::highlights_ref::tests::continuations::gas_town_golden_tucked_group_stub_and_idempotent_rerender ... ok
test native::highlights_ref::tests::image_notes::render_image_selection_plus_image_note ... ok
test native::highlights_ref::tests::image_notes::render_image_plus_comment_preserves_paragraphs ... ok
test native::highlights_ref::stamp::tests::stamp_install_without_info_leaves_trailer_info_absent ... ok
test native::highlights_ref::tests::image_notes::render_not_found_unreadable_and_unsupported ... ok
test native::highlights_ref::tests::image_notes::retina_display_width_table ... ok
test native::highlights_ref::tests::highlight_identity::highlight_identity_survives_insertion_and_underline_absorption ... ok
test native::highlights_ref::tests::image_notes::render_standalone_note_image ... ok
test native::highlights_ref::tests::image_notes::render_image_only_highlight ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_uses_marker_fields_without_fallback_parent ... ok
test native::highlights_ref::tests::highlight_identity::highlight_identity_handles_duplicates_comments_legacy_and_folds ... ok
test native::highlights_ref::tests::marker::created_stays_note_local_despite_stale_marker_fields_opt_in ... ok
test native::highlights_ref::tests::image_notes::render_two_images_and_shared_write ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_canonicalizes_parent_targets ... ok
test native::highlights_ref::stamp::tests::default_target_same_intake_refuses_then_overwrites_with_force ... ok
test native::highlights_ref::tests::marker::marker_parser_accepts_yaml_subset_and_normalizes_keys ... ok
test native::highlights_ref::tests::marker::marker_parser_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_created_key ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_linked_parent_targets ... ok
test native::highlights_ref::tests::marker::frontmatter_render_preserves_unmanaged_keys ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_missing_required_keys_type_and_duplicate_status ... ok
test native::highlights_ref::tests::marker::marker_renderer_rejects_unrepresentable_parent_links ... ok
test native::highlights_ref::rename::plan::tests::coordinated::saved_first_full_rename_holds_conservatively ... ok
test native::highlights_ref::stamp::tests::stamp_install_embeds_marker_and_info_without_annots ... ok
test native::highlights_ref::tests::marker::marker_renderer_uses_stable_key_order ... ok
test native::highlights_ref::stamp::tests::default_target_title_matches_marker_or_info_normalized ... ok
test native::highlights_ref::tests::marker::parent_canonicalization_rejects_non_scalar_values ... ok
test native::highlights_ref::tests::marker::new_note_render_emits_exactly_one_created_line ... ok
test native::highlights_ref::tests::marker::status_validation_rejects_unsupported_and_non_scalar_values ... ok
test native::highlights_ref::overwrite::execute::tests::overwrite_repoints_source_markdown_and_keeps_frozen_pointer ... ok
test native::highlights_ref::rename::plan::tests::coordinated::changed_marker_is_a_specific_hold ... ok
test native::highlights_ref::rename::plan::tests::coordinated::platform_failure_before_writes_is_distinct_and_writes_nothing ... ok
test native::highlights_ref::tests::marker_write::explicit_move_collision_balances_notification_without_claiming_success ... ok
test native::highlights_ref::tests::marker_write::explicit_move_session_saves_first_and_notifies_forward_and_inverse ... ok
test native::highlights_ref::rename::plan::tests::coordinated::occupied_destination_holds_inside_the_grant ... ok
test native::highlights_ref::tests::marker_write::explicit_move_hold_and_platform_error_never_run_the_accessor ... ok
test native::highlights_ref::tests::projection::append_stale_save_reason_joins_existing_reason ... ok
test native::highlights_ref::stamp::tests::default_target_same_library_refuses_with_and_without_force ... ok
test native::highlights_ref::rename::plan::tests::coordinated::hold_before_writes_leaves_everything_untouched ... ok
test native::highlights_ref::source_store::tests::write_store_is_write_once_and_birth_finds_it ... ok
test native::highlights_ref::tests::projection::finalize_replaced_hash_render_skips_a_drop_only_note_write ... ok
test native::highlights_ref::tests::projection::deprecated_statuses_normalize_for_synced_inputs ... ok
test native::highlights_ref::tests::projection::pdf_path_metadata_derives_nested_reference_paths ... ok
test native::highlights_ref::tests::projection::pipeline_fields_exclude_marker_user_projection ... ok
test native::highlights_ref::tests::projection::projection_snapshot_json_round_trips_compact_user_projection ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_compatible_changes ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_deletes_and_conflicts ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_reports_every_destination_conflict ... ok
test native::highlights_ref::tests::projection::relative_config_paths_resolve_under_bob_dir ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_maps_nested_paths_and_companions ... ok
test native::highlights_ref::tests::marker_write::reading_hold_skips_the_coordinator_and_writes_nothing ... ok
test native::highlights_ref::tests::projection::render_drops_continuations_of_a_removed_block_key ... ok
test native::highlights_ref::tests::projection::render_keeps_block_earlier_list_byte_identical ... ok
test native::highlights_ref::tests::projection::replaced_hash_stores_on_marker_write_drops_on_agreement ... ok
test native::highlights_ref::tests::projection::skip_stale_restore_without_write_opt_in_is_restore_alone ... ok
test native::highlights_ref::tests::projection::stale_editor_save_requires_replaced_hash_base_and_mismatch ... ok
test native::highlights_ref::tests::projection::render_places_replaced_hash_after_marker_base ... ok
test native::highlights_ref::tests::projection::validate_library_layout_rejects_equal_and_nested_paths ... ok
test native::highlights_ref::tests::publish::coordinator_failure_skips_callback ... ok
test native::highlights_ref::tests::marker_write::fake_hold_writes_nothing_for_v1 ... ok
test native::highlights_ref::tests::publish::hold_skips_callback_and_preserves_destination_and_companion ... ok
test native::highlights_ref::tests::marker_write::fake_fail_is_a_write_failure_and_writes_nothing ... ok
test native::highlights_ref::tests::publish::late_destination_collision_skips_callback ... ok
test native::highlights_ref::tests::publish::changed_marker_refuses_and_preserves_presenter_save ... ok
test native::highlights_ref::tests::marker_write::restored_capture_is_held_at_execution_and_after_coordinated_save ... ok
test native::highlights_ref::tests::marker_write::reading_hold_report_names_attended_holding_and_unknown ... ok
test native::highlights_ref::tests::publish::copy_pdf_no_clobber_refuses_an_occupant ... ok
test native::highlights_ref::tests::marker_write::key_off_writes_direct_and_never_calls_the_fake ... ok
test native::highlights_ref::stamp::tests::default_target_cap_reports_no_free_name ... ok
test native::highlights_ref::tests::publish::install_stamped_pdf_preserves_companion_on_changed_marker ... ok
test native::highlights_ref::tests::marker_write::v1_execution_refresh_carries_planned_source_pointer_through_marker_write ... ok
test native::highlights_ref::rename::plan::tests::coordinated::idless_move_uses_one_grant_and_keeps_bytes ... ok
test native::highlights_ref::tests::marker_write::fake_grant_writes_coordinated_marker_and_records_wait ... ok
test native::highlights_ref::tests::publish::grant_runs_publication_callback_exactly_once ... ok
test native::highlights_ref::tests::publish::key_off_pass_through_does_not_call_coordinator ... ok
test native::highlights_ref::tests::publish::linux_direct_pass_through_replaces_existing_dest ... ok
test native::highlights_ref::tests::publish::missing_destination_installs_without_coordination ... ok
test native::highlights_ref::tests::publish::save_pdf_no_clobber_refuses_an_occupant ... ok
test native::highlights_ref::tests::publish::production_install_pass_through_writes_missing_dest ... ok
test native::highlights_ref::tests::publish::save_with_unchanged_marker_refuses_and_preserves_bytes ... ok
test native::highlights_ref::overwrite::execute::tests::processed_highlight_identity_survives_overwrite_and_rescan ... ok
test native::highlights_ref::tests::publish::staged_listen_changed_marker_hold_preserves_save_and_audio ... ok
test native::highlights_ref::source_store::tests::inspect_reports_dangling_mismatch_missing_orphan_and_history ... ok
test native::highlights_ref::tests::publish::staged_listen_hold_installs_nothing ... ok
test native::highlights_ref::rename::plan::tests::coordinated::commit_failure_rolls_back_with_both_notifications ... ok
test native::highlights_ref::tests::marker_write::same_digest_recheck_keeps_the_planned_annotation_id ... ok
test native::highlights_ref::tests::marker_write::v2_hold_leaves_the_reading_task_untouched ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_hold_installs_neither ... ok
test native::highlights_ref::tests::publish::symlink_destination_is_refused ... ok
test native::highlights_ref::tests::publish::local_pdf_existing_dest_coordinates_then_replaces ... ok
test native::highlights_ref::tests::marker_write::saved_first_recheck_writes_to_the_fresh_annotation_id ... ok
test native::highlights_ref::tests::reading_execute::v2_guard_allows_embed_repoint_and_residence_parent ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_listen_hold_installs_neither ... ok
test native::highlights_ref::tests::publish::local_pdf_install_stamped_pdf_publishes_after_one_grant ... ok
test native::highlights_ref::rename::plan::tests::coordinated::verification_failure_reverses_forward_move_and_restores ... ok
test native::highlights_ref::tests::marker_write::marker_changed_hold_keeps_the_editor_bytes ... ok
test native::highlights_ref::tests::reading_execute::line_edit_refuses_archived_tasks ... ok
test native::highlights_ref::tests::reading_execute::revalidate_refreshes_moved_lines_and_refuses_changed_ones ... ok
test native::highlights_ref::tests::reading_plan::audio_anchors_after_managed_embed ... ok
test native::highlights_ref::tests::reading_plan::birth_adopts_newest_closed ... ok
test native::highlights_ref::tests::reading_execute::v2_guard_refuses_unrelated_edits ... ok
test native::highlights_ref::tests::reading_execute::changed_line_fails_before_any_pdf_write ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_changed_marker_hold_preserves_save ... ok
test native::highlights_ref::tests::reading_plan::audio_anchor_never_duplicates_or_invents ... ok
test native::highlights_ref::tests::reading_plan::birth_adopts_unique_orphan ... ok
test native::highlights_ref::tests::marker_write::scan_cap_holds_later_pdfs_without_calling_the_coordinator ... ok
test native::highlights_ref::tests::reading_plan::birth_body_shows_embed_not_tracker ... ok
test native::highlights_ref::tests::reading_plan::birth_body_anchors_audio_after_embed ... ok
test native::highlights_ref::tests::reading_plan::birth_parent_keeps_resolved_route ... ok
test native::highlights_ref::tests::reading_plan::birth_parent_falls_back_on_every_error_kind ... ok
test native::highlights_ref::tests::reading_plan::birth_refuses_multiple_open ... ok
test native::highlights_ref::tests::reading_execute::reopen_into_inbox_fallback_carries_warning_child ... ok
test native::highlights_ref::tests::reading_plan::classify_managed_embed_makes_existing_note_v2 ... ok
test native::highlights_ref::tests::reading_plan::classify_missing_note_is_v2_birth ... ok
test native::highlights_ref::tests::reading_plan::classify_outside_task_makes_existing_note_v2 ... ok
test native::highlights_ref::tests::reading_plan::classify_task_inside_own_note_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::classify_trackerless_legacy_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::classify_in_note_tracker_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::embed_target_forms_follow_the_design ... ok
test native::highlights_ref::tests::reading_plan::birth_with_no_candidates_inserts ... ok
test native::highlights_ref::tests::reading_plan::classify_archived_task_makes_existing_note_v2 ... ok
test native::highlights_ref::tests::marker_write::v2_birth_does_not_attach_a_source_that_fails_digest_verification ... ok
test native::highlights_ref::tests::reading_plan::fallback_child_text_is_exact ... ok
test native::highlights_ref::tests::reading_execute::birth_insert_then_rerun_adopts_without_duplication ... ok
test native::highlights_ref::tests::reading_plan::birth_refuses_open_archive_task ... ok
test native::highlights_ref::tests::publish::replacement_error_cleans_up_new_companion ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_inserts_into_resolved_parent ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_adopts_orphan ... ok
test native::highlights_ref::tests::reading_plan::heal_preserves_authored_material ... ok
test native::highlights_ref::tests::reading_plan::first_v2_transition_has_no_false_conflict ... ok
test native::highlights_ref::tests::reading_plan::heal_correct_body_is_byte_identical ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_grant_installs_render_and_audio ... ok
test native::highlights_ref::tests::reading_plan::heal_preserves_crlf ... ok
test native::highlights_ref::tests::reading_plan::marker_hint_round_trips_parent ... ok
test native::highlights_ref::tests::reading_plan::heal_without_h1_leaves_body_alone ... ok
test native::highlights_ref::tests::reading_plan::missing_task_open_surfaces_guidance ... ok
test native::highlights_ref::tests::reading_plan::heal_repoints_stale_embed ... ok
test native::highlights_ref::tests::reading_plan::missing_task_terminal_stays_silent ... ok
test native::highlights_ref::tests::reading_plan::pdf_task_question_overlay_stays_put ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_branch_hands_off ... ok
test native::highlights_ref::tests::reading_plan::plan_task_gesture_conflict_errors ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_closed_tracker_stays_silent ... ok
test native::highlights_ref::tests::reading_plan::plan_reopen_without_source_parent_uses_inbox ... ok
test native::highlights_ref::tests::reading_plan::heal_collapses_duplicate_embeds ... ok
test native::highlights_ref::tests::reading_plan::heal_inserts_missing_embed_below_h1 ... ok
test native::highlights_ref::tests::reading_plan::residence_parent_renders_from_route ... ok
test native::highlights_ref::tests::reading_plan::signal_archived_reopen_never_edits_done ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_warns_on_unresolvable_hint ... ok
test native::highlights_ref::tests::reading_plan::plan_closed_terminal_stays_quiet ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_open_tracker_reports_migrate_diagnostic ... ok
test native::highlights_ref::tests::reading_plan::plan_existing_marker_change_edits_line ... ok
test native::highlights_ref::tests::reading_plan::plan_missing_open_never_invents_a_task ... ok
test native::highlights_ref::tests::reading_plan::plan_reopen_archived_inserts_into_source_parent ... ok
test native::highlights_ref::tests::reading_plan::plan_refused_multiple_open_blocks_writes ... ok
test native::highlights_ref::tests::reading_plan::region_own_notes_excludes_managed_embed ... ok
test native::highlights_ref::tests::marker_write::attended_and_unknown_probe_do_not_hold_for_reading ... ok
test native::highlights_ref::tests::reading_plan::signal_frontmatter_only_change_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_changed_sides_agreeing_with_task_drive ... ok
test native::highlights_ref::tests::reading_plan::region_own_notes_keeps_legacy_body_verbatim ... ok
test native::highlights_ref::tests::reading_plan::signal_live_terminal_reopen_edits_the_line ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_key_off_replaces_without_coordination ... ok
test native::highlights_ref::tests::reading_plan::signal_conflicting_inputs_refuse ... ok
test native::highlights_ref::tests::publish::staged_listen_grant_installs_audio_episode_and_pdf ... ok
test native::highlights_ref::tests::reading_plan::signal_marker_only_change_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_marker_close_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_question_on_terminal_drives_reopen_ready ... ok
test native::highlights_ref::tests::reading_plan::signal_task_gesture_drives_status ... ok
test native::highlights_ref::tests::reading_plan::signal_question_overlay_agrees_with_open ... ok
test native::highlights_ref::tests::reading_plan::signal_unchanged_checkbox_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_uncheckboxable_current_refuses ... ok
test native::highlights_ref::tests::reading_plan::signal_without_base_agreement_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_unknown_mark_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_without_base_evidence_refuses_disagreement ... ok
test native::highlights_ref::tests::reading_plan::status_mark_matches_projection_marks ... ok
test native::highlights_ref::tests::reading_plan::v1_birth_body_stays_frozen ... ok
test native::highlights_ref::tests::reading_plan::without_parent_drops_only_parent ... ok
test native::highlights_ref::tests::region::color_grouped_plain_prose_and_titled_notes_survive ... ok
test native::highlights_ref::tests::region::color_grouped_genuine_loss_still_tombstones ... ok
test native::highlights_ref::tests::region::color_grouped_mirror_with_task_text_yields_no_task ... ok
test native::highlights_ref::tests::region::note_anatomy_broken_markers_yield_no_region ... ok
test native::highlights_ref::tests::region::note_anatomy_legacy_body_passes_through_verbatim ... ok
test native::highlights_ref::tests::region::note_anatomy_full_body ... ok
test native::highlights_ref::tests::region::region_parses_empty_scaffold_section ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_listen_grant_installs_episode_and_pdf ... ok
test native::highlights_ref::tests::publish::stamp_and_install_with_fresh_dest_installs_without_coordination ... ok
test native::highlights_ref::tests::region::region_parses_leaked_mirror_like_ea_graph ... ok
test native::highlights_ref::tests::region::region_parses_rendered_title_prefixed_mirror ... ok
test native::highlights_ref::tests::region::region_parses_group_spanning_pages ... ok
test native::highlights_ref::tests::region::region_parses_section_without_page_labels ... ok
test native::highlights_ref::tests::region::region_parses_section_titled_page_turners ... ok
test native::highlights_ref::tests::region::region_parses_sections_other_and_removed ... ok
test native::highlights_ref::tests::reading_execute::reopen_prefers_old_id_and_suffixes_on_collision ... ok
test native::highlights_ref::tests::reading_execute::line_edit_updates_checkbox_and_stamps_close ... ok
test native::highlights_ref::tests::region::region_section_card_images_and_warnings ... ok
test native::highlights_ref::tests::region::region_sectioned_annotation_counts_ignore_cards ... ok
test native::highlights_ref::tests::region::region_round_trip_standalone_note ... ok
test native::highlights_ref::tests::region::region_round_trip_highlight_comment_mirror ... ok
test native::highlights_ref::tests::region::region_round_trip_pages_preamble_and_tombstones ... ok
test native::highlights_ref::tests::region::color_grouped_rerender_drops_phantom_without_tombstone ... ok
test native::highlights_ref::tests::region::region_existing_fixtures_have_no_image_notes ... ok
test native::highlights_ref::tests::marker_write::coordinated_saved_first_restores_a_stale_marker_inside_the_accessor ... ok
test native::highlights_ref::tests::seams::ref_task_mark_target_seam_matches_status_aware_mapping ... ok
test native::highlights_ref::tests::seams::ref_task_mark_seam_matches_the_pdf_task_mapping ... ok
test native::highlights_ref::tests::region::region_summary_section_without_s_id_is_not_sectioned ... ok
test native::highlights_ref::tests::region::region_unknown_callout_is_unparsed ... ok
test native::highlights_ref::tests::seams::deprecated_status_seam_matches_marker_normalization ... ok
test native::highlights_ref::tests::region::title_prefixed_marker_text_is_a_mirror ... ok
test native::highlights_ref::tests::section_edges::declaring_sticky_absorbs_published_note_without_a_stub ... ok
test native::highlights_ref::tests::region::region_round_trip_highlight_with_multiline_comment ... ok
test native::highlights_ref::tests::region::region_round_trip_image ... ok
test native::highlights_ref::rename::plan::tests::coordinated::move_grants_once_and_notifies_both_directions_on_rollback ... ok
test native::highlights_ref::tests::section_edges::declaring_sticky_redirect_stub_persists_after_unlink ... ok
test native::highlights_ref::rename::plan::tests::coordinated::saved_bytes_survive_a_rollback ... ok
test native::highlights_ref::tests::region::region_stray_non_card_h3_in_sectioned_region_is_a_page_label ... ok
test native::highlights_ref::tests::section_edges::declaring_sticky_redirect_stub_disappears_without_declaration ... ok
test native::highlights_ref::tests::region::region_parses_three_tucked_pieces_with_their_own_notes ... ok
test native::highlights_ref::tests::region::region_round_trip_image_notes ... ok
test native::highlights_ref::tests::region::region_unsectioned_h4_is_not_a_page_caption ... ok
test native::highlights_ref::tests::region::region_sectioned_preamble_is_before_first_h3 ... ok
test native::highlights_ref::tests::section_edges::declaring_sticky_redirect_stub_appears_when_linked ... ok
test native::highlights_ref::tests::section_edges::missing_route_target_without_a_section_keeps_todays_error ... ok
test native::highlights_ref::tests::section_edges::missing_route_target_naming_a_section_gains_a_hint ... ok
test native::highlights_ref::tests::sections::sticky_declarations_keep_description_headings_and_empty_declarations ... ok
test native::highlights_ref::tests::sections::unicode_slugs_hash_fallback_and_collisions_are_stable ... ok
test native::highlights_ref::tests::sections::tag_scanner_handles_positions_labels_lists_codes_escapes_and_routes ... ok
test native::highlights_ref::tests::marker_write::v2_birth_attaches_verified_source_through_normalizing_marker_write ... ok
test native::highlights_ref::tests::section_edges::removed_section_needs_a_link_or_prior_stub ... ok
test native::highlights_ref::tests::section_edges::section_tag_and_task_route_share_a_note ... ok
test native::highlights_ref::tests::section_edges::removed_section_stub_disappears_when_redeclared ... ok
test native::highlights_ref::tests::sections::comment_declaration_beats_tags_and_reports_other_section ... ok
test native::highlights_ref::tests::sections::declaration_scanner_normalizes_titles_aliases_and_reserved_names ... ok
test native::highlights_ref::tests::sections::hash_declarations_accept_hash_aliases ... ok
test native::highlights_ref::tests::sections::comment_declarations_work_for_images_and_standalone_underlines ... ok
test native::highlights_ref::tests::sections::hash_display_source_consumes_and_keeps_escapes_visible ... ok
test native::highlights_ref::tests::sections::hash_identity_key_strips_hash_but_keeps_non_tags ... ok
test native::highlights_ref::tests::sections::no_declarations_produce_no_section_plan_or_tag_diagnostics ... ok
test native::highlights_ref::tests::sections::ordinary_stickies_and_comment_hash_lines_keep_their_grammar ... ok
test native::highlights_ref::tests::sections::hash_tag_scanner_handles_positions_and_rejections ... ok
test native::highlights_ref::tests::sections::comment_declarations_declare_merge_conflict_and_reject ... ok
test native::highlights_ref::tests::sections::planner_merges_underlines_by_their_display_head_and_keeps_repeated_home_tags ... ok
test native::highlights_ref::tests::sections::section_identity_key_ignores_tags_everywhere_but_keeps_an_all_tag_key ... ok
test native::highlights_ref::tests::sections::planner_consumes_follower_and_list_tags_and_reports_conflicts_and_unknowns ... ok
test native::highlights_ref::tests::sections::planner_resolves_forward_aliases_merges_duplicates_and_rejects_invalid_titles ... ok
test native::highlights_ref::tests::sections::planner_reports_literal_section_shaped_comment_lines ... ok
test native::highlights_ref::tests::sections::planner_does_not_join_tags_only_stickies_and_keeps_task_routes ... ok
test native::highlights_ref::tests::sections::hash_planner_joins_conflicts_and_reports_near_miss_only ... ok
test native::highlights_ref::tests::section_edges::removed_section_stub_appears_when_linked_and_persists ... ok
test native::highlights_ref::rename::plan::tests::coordinated::commit_reported_as_error_stays_committed ... ok
test native::highlights_ref::tests::sections::source_rewrite_consumes_only_home_tags_and_keeps_escapes_visible ... ok
test native::highlights_ref::tests::sections_render::diagnostic_vocabulary_strings_are_stable ... ok
test native::highlights_ref::tests::sections_render::declaration_ordering_merged_empty_and_other_omitted ... ok
test native::highlights_ref::tests::sections_render::comment_declaration_keeps_remaining_text_and_task_link ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_preserves_list_structure ... ok
test native::highlights_ref::tests::section_edges::section_dry_run_lines_cover_the_vocabulary ... ok
test native::highlights_ref::tests::sidecar::color_grouped_quote_hard_wrap_stays_quote_text ... ok
test native::highlights_ref::tests::sidecar::annotation_block_id_is_stable_across_space_wrapping ... ok
test native::highlights_ref::tests::sidecar::color_grouped_quote_continuation_stops_at_boundaries ... ok
test native::highlights_ref::tests::sidecar::color_grouped_title_prefixed_marker_is_excluded ... ok
test native::highlights_ref::tests::sections_render::rejected_declarations_render_literally ... ok
test native::highlights_ref::tests::sections_render::hash_playbook_shape_matches_at_spelling ... ok
test native::highlights_ref::tests::sections_render::page_captions_reset_at_each_section_and_handle_labels ... ok
test native::highlights_ref::tests::sections_render::membership_covers_notes_aliases_conflicts_and_escapes ... ok
test native::highlights_ref::tests::sections_render::hash_tags_without_declarations_render_unchanged ... ok
test native::highlights_ref::tests::sections_render::section_tasks_use_section_links_and_keep_processed_ids ... ok
test native::highlights_ref::tests::sections_render::hash_tag_toggles_keep_ids_and_match_at_spelling ... ok
test native::highlights_ref::tests::sections_render::memory_example_sections_first_with_other_last ... ok
test native::highlights_ref::tests::sections_render::no_declaration_output_has_no_consumption_or_section_layout ... ok
test native::highlights_ref::tests::sections_render::round_trip_preserves_identities_pages_and_homes ... ok
test native::highlights_ref::tests::sections_render::comment_declaration_groups_bryans_note_and_keeps_ids ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_reflows_and_dehyphenates ... ok
test native::highlights_ref::tests::sidecar::comment_first_line_hash_declares_for_highlights_and_images ... ok
test native::highlights_ref::tests::sections_render::twin_quotes_keep_association_and_stay_unique ... ok
test native::highlights_ref::tests::sidecar::leaked_mirror_and_preamble_blocks_drop_silently_while_genuine_tombstones ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_level_one_sticky_is_not_a_page_break ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_keeps_heading_shaped_quote_wrap ... ok
test native::highlights_ref::tests::sections_render::identity_survives_tag_toggles_and_declaration_changes ... ok
test native::highlights_ref::tests::sidecar::linked_quote_continuation_stops_at_annotation_date_header ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_keeps_wrapped_quotes_and_marker_mirror ... ok
test native::highlights_ref::tests::sidecar::linked_quote_hard_wrap_with_xml_lead_stays_quote_text ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_renders_image_assets_and_tasks ... ok
test native::highlights_ref::tests::sidecar::rendered_annotation_blocks_do_not_include_source_task_anchors ... ok
test native::highlights_ref::tests::sidecar::return_link_strip_keeps_block_ids_stable ... ok
test native::highlights_ref::tests::sidecar::image_block_id_is_stable_across_asset_renames ... ok
test native::highlights_ref::tests::sidecar::linked_page_headings_split_after_a_simple_marker_page ... ok
test native::highlights_ref::tests::sidecar::linked_quote_hard_wrap_starting_with_hash_stays_quote_text ... ok
test native::highlights_ref::tests::sidecar::marker_content_decoder_preserves_pdfdoc_line_separators ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_strips_comment_bullet_markers ... ok
test native::highlights_ref::tests::sidecar::pdf_text_artifact_cleanup_normalizes_extraction_noise ... ok
test native::highlights_ref::tests::sidecar::return_link_glyphs_strip_only_from_highlights_when_flagged ... ok
test native::highlights_ref::tests::sidecar::missing_image_asset_error_points_at_textbundle_export ... ok
test native::highlights_ref::tests::sidecar::sidecar_page_heading_extracts_linked_page_label ... ok
test native::highlights_ref::tests::status::blocked_task_conflicts_when_marker_moved_status_away ... ok
test native::highlights_ref::tests::status::blocked_task_reopens_terminal_projections_to_ready ... ok
test native::highlights_ref::tests::sidecar::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::tests::sidecar::sidecar_without_page_headings_has_no_preamble ... ok
test native::highlights_ref::tests::sidecar::sidecar_parser_extracts_image_annotations_and_leaves_non_images_as_notes ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_conflicts_with_competing_edit ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_contributes_abandoned ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_ready_reopens_terminal_to_ready ... ok
test native::highlights_ref::tests::sidecar::simple_sidecar_level_one_stickies_are_not_page_breaks ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_promotes_ready_and_back ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_maps_all_lifecycle_states ... ok
test native::highlights_ref::tests::sidecar::simple_sidecar_unlabeled_text_after_quote_remains_comment ... ok
test native::highlights_ref::tests::status::blocked_task_agrees_with_every_open_projection ... ok
test native::highlights_ref::tests::tasks::annotation_task_batches_append_in_insertion_order ... ok
test native::highlights_ref::tests::sidecar::setext_preamble_yields_no_annotations_and_keeps_genuine_ids_stable ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_beautifies_callout_text ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_heading_shaped_wrap_renders_inside_quote ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_create_section_after_unterminated_ref_line ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_fill_empty_tasks_section_with_blank_lines ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_reuse_h1_or_closed_atx_tasks_heading ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_preserves_crlf_line_endings ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_ignore_fenced_and_managed_tasks_headings ... ok
test native::highlights_ref::tests::tasks::annotation_task_route_suffix_is_strict_and_stripped_from_identity ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_rejects_malformed_and_duplicate_tasks ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_recognizes_generated_pdf_task ... ok
test native::highlights_ref::tests::tasks::annotation_task_section_stays_after_ref_child_lines ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_is_idempotent_and_preserves_existing_states ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidate_records_route_and_processed_id ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidates_extract_from_comments_and_notes ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_append_to_existing_tasks_section ... ok
test native::highlights_ref::tests::underlines::continuation_markers_are_respected_and_absorbed_rows_do_not_block_them ... ok
test native::highlights_ref::tests::tasks::processed_task_index_scans_states_indents_and_done_notes ... ok
test native::highlights_ref::tests::underlines::emphasis_snaps_splits_flanks_and_merges_ranges ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_ht_backlink_blocks_edited_recreation ... ok
test native::highlights_ref::tests::tasks::highlights_ref_capture_dates_follow_bob_clock ... ok
test native::highlights_ref::tests::underlines::image_selections_and_sticky_notes_cannot_host_underlines ... ok
test native::highlights_ref::tests::underlines::underline_classifier_accepts_only_fully_bold_rows ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_identity_blocks_recreation ... ok
test native::highlights_ref::tests::underlines::accepted_whole_word_occurrence_renders_inside_the_host ... ok
test native::highlights_ref::tests::underlines::continuation_member_keeps_emphasis_and_comments_with_each_piece ... ok
test native::highlights_ref::overwrite::execute::tests::coordinated_save_aborts_safely_then_retry_archives_saved_pdf ... ok
test native::highlights_ref::tests::underlines::repeated_whole_word_and_inside_word_stay_standalone ... ok
test native::highlights_ref::tests::underlines::absorbed_underline_renders_comment_image_and_task_on_host ... ok
test native::highlights_ref::tests::underlines::underline_report_lines_explain_standalone_reasons ... ok
test native::highlights_ref::web_source::tests::anchor_normalization_ignores_endings_and_edge_newlines ... ok
test native::highlights_ref::web_source::tests::anchor_matching_is_greedy_in_order ... ok
test native::highlights_ref::text::tests::strip_return_link_glyphs_covers_every_shape ... ok
test native::highlights_ref::web_source::tests::unmatched_block_keeps_later_anchors ... ok
test native::markdown::tests::blockquote_and_indented_code_detection ... ok
test native::markdown::tests::split_line_ending_preserves_crlf_lf_and_none ... ok
test native::highlights_ref::tests::underlines::underline_match_key_and_host_rules_fail_closed ... ok
test native::markdown::tests::setext_underline_accepts_levels_and_indent ... ok
test native::markdown::tests::standalone_html_comment_reads_inner_text ... ok
test native::note_ready::cli::tests::closest_names_suggest_up_to_three ... ok
test native::note_ready::render::tests::crowded_bars_mark_the_cap_and_overflow ... ok
test native::highlights_ref::tests::status::blocked_task_write_back_keeps_mark_for_open_and_closes_for_read ... ok
test native::highlights_ref::tests::underlines::whole_word_emphasis_ignores_subword_order_and_sidecar_order ... ok
test native::note_ready::render::tests::crowded_worklist_always_advertises_task_card_hints ... ok
test native::note_ready::render::tests::ready_gesture_hint_is_always_the_task_card_keys ... ok
test native::note_ready::render::tests::overview_names_crowded_notes_with_bars ... ok
test native::note_ready::render::tests::worklist_lists_rows_in_file_order ... ok
test native::note_ready::render::tests::overview_advertises_task_card_keys_on_any_day ... ok
test native::note_ready::tests::lints_emit_once_per_note ... ok
test native::highlights_ref::tests::status::close_date_stamp_inserts_once_before_ref_and_preserves_existing_dates ... ok
test native::note_ready::tests::r11_all_type_forms_are_eligible ... ok
test native::note_ready::tests::ordering_is_crowded_full_room_empty_exempt ... ok
test native::note_ready::tests::r12_stamping_moves_new_to_ready_without_changing_count ... ok
test native::note_ready::tests::r13_today_tasks_count_as_ready ... ok
test native::note_ready::tests::r1_six_tasks_is_crowded_over_by_one ... ok
test native::note_ready::tests::r2_five_tasks_is_full_without_lint ... ok
test native::note_ready::tests::r3_lane_exclusions_never_count ... ok
test native::note_ready::tests::r4_make_up_splits_new_rotten_ready ... ok
test native::note_ready::tests::r5_recurring_excluded_and_counted ... ok
test native::note_ready::render::tests::overview_all_clear_is_green_without_crowded_group ... ok
test native::note_ready::tests::r10_terminal_projects_are_not_capped ... ok
test native::note_ready::tests::r8_ready_cap_forms ... ok
test native::note_ready::tests::r14_config_cap_with_note_override ... ok
test native::note_ready::tests::r6_prj_rows_never_count ... ok
test native::highlights_ref::rename::plan::tests::coordinated::same_stem_repair_keeps_saved_annotations_with_renumbered_objects ... ok
test native::note_ready::tests::r9_nested_child_tasks_each_count ... ok
test native::note_tasks::tests::clean_description_drops_ref_after_task_filter ... ok
test native::note_tasks::tests::block_id_lookup_distinguishes_found_non_task_duplicate_and_missing ... ok
test native::note_tasks::tests::ignores_frontmatter_and_fenced_code_tasks ... ok
test native::note_tasks::tests::computes_child_spans_for_mixed_indentation_blanks_and_eof ... ok
test native::highlights_ref::tests::underlines::absorbed_identity_and_link_aware_stub_are_reversible ... ok
test native::note_tasks::tests::line_digest_fixture_vectors_match_rust ... ok
test native::note_tasks::tests::suggests_case_matches_and_unique_nearby_block_ids_only ... ok
test native::note_tasks::tests::refs_resolve_exact_shifted_stale_and_ambiguous_tasks ... ok
test native::plan_budget::cli::tests::plan_name_swatches_leave_no_color_text_unchanged ... ok
test native::note_tasks::tests::task_refs_parse_strictly_and_round_trip_scan_metadata ... ok
test native::plan_budget::tests::alias_and_md_suffix_links_count ... ok
test native::note_tasks::tests::gates_on_filter_and_cleans_descriptions_with_sections ... ok
test native::ob::tests::git_command_runs_auto_maintenance_in_foreground ... ok
test native::parent_notes::tests::dash_and_underscore_are_different ... ok
test native::note_tasks::tests::ref_task_kind_marks_filter_then_ref_rows ... ok
test native::plan_budget::tests::components_compare_case_insensitively ... ok
test native::parent_notes::tests::ambiguous_alias_names_both_notes ... ok
test native::parent_notes::tests::stem_wins_over_alias ... ok
test native::plan_budget::tests::link_forms_count_once_and_exclusions_hold ... ok
test native::plan_budget::tests::markers_and_inner_hash_links_count ... ok
test native::plan_budget::tests::eleven_links_are_over_the_cap ... ok
test native::note_tasks::tests::reads_real_statuses_and_missing_settings_fall_back_to_defaults ... ok
test native::plan_budget::tests::empty_target_means_the_daily_note ... ok
test native::plan_budget::tests::merged_name_counts_decks_once_with_duplicate_lint ... ok
test native::plan_budget::tests::lane_queries_parse_through_the_native_engine ... ok
test native::parent_notes::tests::resolves_alias_and_reports_how_it_matched ... ok
test native::parent_notes::tests::each_inbox_resolves ... ok
test native::parent_notes::tests::terminal_project_and_non_parent_hub_report_themselves ... ok
test native::parent_notes::tests::unknown_names_near_miss_and_alias_hint ... ok
test native::parent_notes::tests::resolves_stem_md_and_wikilink_forms ... ok
test native::plan_budget::tests::cancelled_and_completed_entries_never_count ... ok
test native::plan_budget::tests::lane_over_never_changes_status ... ok
test native::plan_budget::tests::four_themes_are_over_but_three_are_fine ... ok
test native::plan_budget::tests::open_inventory_label_counts_and_lints ... ok
test native::plan_budget::tests::managed_dependency_lines_do_not_count_toward_pomodoro_link_budget ... ok
test native::plan_budget::tests::running_and_highlight_flags_follow_ledger_order ... ok
test native::plan_budget::tests::fenced_links_and_fenced_entries_never_count ... ok
test native::plan_budget::tests::unnamed_placeholder_counts_only_with_links ... ok
test native::plan_budget::today::tests::closed_entries_contribute_no_links ... ok
test native::plan_budget::today::tests::aliased_links_pin_the_lineup_behavior ... ok
test native::plan_budget::tests::missing_section_reports_empty ... ok
test native::plugins::deploy::tests::force_permits_uncertain_stamps ... ok
test native::plugins::deploy::tests::digest_is_stable_for_the_same_assets ... ok
test native::plugins::deploy::tests::leftover_css_blocks_exact_bundle ... ok
test native::plugins::deploy::tests::leftover_css_does_not_break_stamp_match ... ok
test native::plugins::deploy::tests::missing_stamp_bootstraps ... ok
test native::plan_budget::tests::subheading_splits_time_totals_and_lints ... ok
test native::ob::tests::detect_git_worktree_reports_non_worktree ... ok
test native::plan_budget::today::tests::duplicate_links_dedupe_to_the_first_position ... ok
test native::plan_budget::today::tests::done_and_cancelled_tasks_drop_out_while_blocked_stays ... ok
test native::plan_budget::today::tests::fenced_links_never_count ... ok
test native::plan_budget::today::tests::gtd_empty_target_resolves_to_the_daily_note ... ok
test native::plan_budget::today::tests::missing_notes_lint_and_drop_out ... ok
test native::plan_budget::today::tests::markers_struck_and_embedded_follow_the_lineup_rule ... ok
test native::plan_budget::today::tests::mixed_and_nested_bullets_are_not_dedicated_links ... ok
warning: You appear to have cloned an empty repository.
test native::plugins::tests::json_shape_is_stable ... ok
test native::note_ready::tests::scan_covers_r11_r8_terminal_and_recurring ... ok
test native::note_ready::tests::scan_excludes_r3_and_r7_paths ... ok
test native::plugins::tests::scan_reports_states_and_counts ... ok
test native::highlights_ref::web_source::tests::figure_wrapped_code_and_images_convert_to_markdown ... ok
test native::plugins::tests::sync_reports_text_diff_for_changed_files ... ok
test native::plugins::tests::sync_state_detects_synced_drift_and_missing ... ok
test native::plugins::tests::sync_summarizes_binary_and_minified_diffs ... ok
test native::plugins::tests::pull_repo_skips_non_git_directory ... ok
test native::plugins::tests::sync_unknown_plugin_is_an_error ... ok
test native::highlights_ref::overwrite::execute::tests::older_archive_save_survives_failed_second_overwrite_rollback ... ok
test native::highlights_ref::tests::status::highlights_ref_task_checkbox_rewrite_and_dirty_allowance_are_narrow ... ok
test native::ob::tests::commit_paths_scopes_to_listed_paths ... ok
test native::plugins::tests::malformed_stamp_refuses_changing_assets ... ok
test native::plugins::tests::truncate_adds_ellipsis_only_when_needed ... ok
test native::pomodoro::tests::completed_ledger_parser_only_accepts_x_checkbox_entries ... ok
test native::plugins::tests::unreadable_repo_is_an_error ... ok
test native::plugins::tests::stamp_deployed_at_is_utc_not_the_day_zone_clock ... ok
test native::plugins::tests::vault_state_reads_enabled_disabled_and_not_installed ... ok
test native::pomodoro::tests::open_ledger_parser_requires_an_open_checkbox ... ok
test native::pomodoro::tests::tmux_theme_swatches_are_additive_and_no_color_is_byte_identical ... ok
test native::pomodoro::tests::unclosed_frontmatter_delimiter_is_content ... ok
test native::pomodoro_homes::tests::canonical_daily_notes_resolve_to_daily_bucket_only ... ok
test native::pomodoro_homes::tests::fallback_palette_fnv_vector_is_pinned ... ok
test native::pomodoro_homes::tests::note_facts_parse_theme_scalars_lists_and_off ... ok
test native::pomodoro_homes::tests::leftover_rollup_key_neither_regroups_nor_warns ... ok
test native::pomodoro_homes::tests::root_flag_makes_a_project_its_own_root_parent ... ok
test native::pomodoro_homes::tests::session_link_sibling_includes_struck_and_embedded_bare_links_only ... ok
test native::pomodoro_homes::tests::root_parent_follows_the_examples_table ... ok
test native::pomodoro_homes::tests::split_minutes_uses_ledger_order_for_remainder ... ok
test native::plugins::tests::sync_dry_run_reports_without_writing ... ok
test native::pomodoro_themes::rename::rename_tests::later_rename_away_restores_the_warning ... ok
test native::pomodoro_themes::rename::rename_tests::raw_lines_round_trip_every_terminator ... ok
test native::pomodoro_themes::rename::rename_tests::raw_tail_splice_names_the_racing_action ... ok
test native::pomodoro_themes::rename::rename_tests::re_adopted_later_covers_color_unpin_unhide_and_rename_to ... ok
test native::pomodoro_themes::rename::rename_tests::re_adopted_later_respects_journal_path_tiebreak ... ok
test native::pomodoro_themes::rename::rename_tests::replace_name_tail_preserves_prefix_bytes ... ok
test native::pomodoro_homes::tests::resolved_home_keeps_the_residence_note_chain ... ok
test native::pomodoro_themes::rename::rename_tests::rewrite_name_replaces_component_and_preserves_separators ... ok
test native::pomodoro_themes::rename::rename_tests::rewrite_preserves_crlf_terminators ... ok
test native::pomodoro_themes::rename::rename_tests::rewrite_preserves_no_final_newline_on_changed_line ... ok
test native::pomodoro_themes::rename::rename_tests::rewrite_preserves_mixed_endings_blank_and_trailing_space ... ok
test native::pomodoro_themes::rename::rename_tests::rewrite_preserves_untouched_heading_and_child_rows ... ok
test native::pomodoro_themes::rename::rename_tests::writer_order_uses_path_before_line ... ok
test native::pomodoro_themes::split::split_tests::apply_changes_preserves_crlf_terminators ... ok
test native::pomodoro_themes::split::split_tests::apply_changes_preserves_mixed_endings_blank_and_trailing_space ... ok
test native::pomodoro_themes::split::split_tests::apply_changes_preserves_no_final_newline_on_changed_line ... ok
test native::pomodoro_themes::split::split_tests::parse_map_rows_refuses_blank_or_plus_theme ... ok
test native::pomodoro_themes::split::split_tests::parse_map_rows_refuses_short_row ... ok
test native::pomodoro_themes::rename::rename_tests::verify_rejects_collateral_terminator_rewrite ... ok
test native::pomodoro_themes::split::split_tests::parse_map_rows_skips_comments_blanks_and_note_column ... ok
test native::pomodoro_themes::split::split_tests::parse_map_rows_tolerates_crlf ... ok
test native::pomodoro_themes::split::split_tests::verify_split_rejects_collateral_terminator_rewrite ... ok
test native::pomodoro_themes::tests::catalog_store_prunes_vanished_vaults_and_sweeps_orphan_files ... ok
test native::pomodoro_themes::tests::collision_hints_move_the_less_used_unpinned_pair ... ok
test native::pomodoro_themes::tests::hash_hues_match_known_collisions ... ok
test native::pomodoro_themes::tests::future_days_do_not_count_toward_recency ... ok
test native::pomodoro_themes::tests::scan_splits_named_entries_and_ignores_unnamed ... ok
test native::pomodoro_themes::tests::known_keys_store_prunes_vanished_vaults ... ok
test native::pomodoro_themes::tests::catalog_loads_scratch_vault_and_applies_area_hue ... ok
test native::pomodoro_themes::tests::shared_vectors_cover_components_hue_fold_rank_and_similar ... ok
test native::plugins::tests::optional_css_presence_and_data_json_are_preserved ... ok
test native::pomodoro_themes::tests::theme_refs_for_unknown_name_are_marked_unknown ... ok
test native::project_dependencies::tests::ancestor_chain_is_read_on_demand_cycle_safe_and_depth_limited ... ok
test native::project_dependencies::tests::project_ancestors_stop_at_the_first_non_project ... ok
test native::project_dependencies::tests::project_parent_targets_resolve_scalar_alias_path_and_heading_forms ... ok
test native::project_dependencies::tests::project_frontmatter_schedule_is_not_a_blocking_input ... ok
test native::pomodoro_themes::tests::completion_cache_keeps_today_live_and_obeys_catalog_invalidation ... ok
test native::project_dependencies::tests::project_reason_path_is_the_project_note_path ... ok
test native::project_dependencies::tests::project_reasons_apply_to_nested_and_ref_residents_but_not_fenced_lines ... ok
test native::project_dependencies::tests::project_reasons_do_not_clear_a_residents_own_reason ... ok
test native::project_dependencies::tests::project_reasons_come_from_the_prj_depends_on_line_and_schedule ... ok
test native::pomodoro_themes::tests::theme_lookup_uses_cached_history_and_refreshes_changed_today ... ok
test native::project_dependencies::tests::project_reasons_ignore_unresolved_or_closed_dependencies ... ok
test native::project_dependencies::tests::recognises_only_one_open_prj_in_a_live_project_note ... ok
test native::project_dependencies::tests::project_tree_resolves_nearest_ancestors_and_stops_at_nonprojects ... ok
test native::project_dependencies::tests::project_tree_cycle_excludes_self_and_reports_the_cycle_once ... ok
test native::projects::tests::edits::project_blocked_tag_preserves_crlf ... ok
test native::projects::tests::edits::project_blocked_tag_normalizer_deduplicates_only_the_exact_tag ... ok
test native::projects::tests::edits::project_blocked_tag_uses_metadata_position_and_is_idempotent ... ok
test native::projects::tests::edits::project_changes_delete_subproject_line_for_stale_child ... ok
test native::projects::tests::edits::project_changes_clean_duplicate_subproject_marker_lines ... ok
test native::projects::tests::edits::project_changes_hoist_frontmatter_scheduled_onto_prj_and_delete_the_key ... ok
test native::projects::tests::edits::project_changes_do_not_anchor_or_move_relation_lines ... ok
test native::projects::tests::edits::project_changes_hoist_scheduled_preserves_crlf_and_unrelated_yaml ... ok
test native::projects::tests::edits::project_changes_hoist_skips_fenced_prj_example ... ok
test native::projects::tests::edits::project_changes_insert_subproject_line_above_user_bullets ... ok
test native::projects::tests::edits::project_changes_ignore_nested_depends_on_when_inserting_subprojects ... ok
test native::projects::tests::edits::project_changes_insert_subproject_line_after_cancel_log_subtree ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_final_prj_line ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_prj_with_tab_indent ... ok
test native::plugins::tests::deploy_lock_rejects_a_second_writer ... ok
test native::projects::tests::edits::project_changes_keep_inline_prj_scheduled_when_removing_hide ... ok
test native::projects::tests::edits::project_changes_mark_last_child_closed_and_keep_subproject_line ... ok
test native::projects::tests::edits::frontmatter_keys_must_start_at_column_zero ... ok
test native::projects::tests::edits::project_changes_insert_subprojects_after_crlf_dependency_subtree_at_eof ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_for_subproject_link_insertions ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_when_appending_status ... ok
test native::projects::tests::edits::project_changes_move_subproject_marker_after_depends_on ... ok
test native::projects::tests::edits::project_changes_remove_prj_hide_tag_with_crlf ... ok
test native::projects::tests::edits::project_changes_replace_status_append_missing_status_and_add_hide_tag ... ok
test native::projects::tests::edits::project_changes_rewrite_subproject_line_in_place ... ok
test native::projects::tests::edits::schedule_only_issues_still_allow_subproject_aggregation ... ok
test native::projects::tests::edits::project_changes_insert_subproject_line_after_depends_on_and_cancel_log ... ok
test native::pomodoro_themes::tests::shared_vectors_cover_suggest_task_field_and_write_rule ... ok
test native::projects::tests::edits::project_parser_splits_surfacing_and_dash_visibility_counts ... ok
test native::plugins::tests::sync_only_filters_to_a_single_plugin ... ok
test native::projects::tests::edits::due_scheduled_projects_follow_the_normal_surfacing_rule ... ok
test native::projects::tests::edits::scheduled_tasks_keep_subproject_ledger_planning ... ok
test native::projects::tests::edits::task_schedule_edits_cover_contract_and_preserve_markdown ... ok
test native::projects::tests::parse::non_project_notes_are_ignored ... ok
test native::projects::tests::parse::prj_tag_is_token_bounded_and_does_not_match_prj_is_blocked ... ok
test native::projects::tests::edits::terminal_projects_do_not_reconcile_task_schedules ... ok
test native::projects::tests::parse::project_parser_accepts_project_type_variants_and_counts_tasks ... ok
test native::projects::tests::parse::project_parser_accepts_bare_project_type_and_prj_states ... ok
test native::projects::tests::edits::scheduled_tasks_precede_prj_surfacing_at_local_date_boundary ... ok
test native::pomodoro_homes::tests::shared_vectors_match_indexed_and_disk_sources ... ok
test native::plugins::tests::nongit_vault_has_no_ignore_warning ... ok
test native::projects::tests::parse::project_parser_records_scheduled_and_placeholder_prj ... ok
test native::projects::tests::parse::project_parser_records_prj_sub_block_marker_lines ... ok
test native::projects::tests::parse::project_parser_marks_unprioritized_prj_as_on_dash ... ok
test native::projects::tests::parse::task_tag_matches_tasks_plugin_boundaries ... ok
test native::projects::tests::parse::type_forms_all_match_project_and_area ... ok
test native::projects::tests::parse::wikilink_target_extracts_normalized_note_names ... ok
test native::projects::tests::parse::type_forms_match_article_and_keep_project_area ... ok
test native::plugins::tests::list_carries_ignore_warning_without_changing_columns ... ok
test native::projects::tests::parse::project_parser_reports_malformed_and_multiple_prj_lines ... ok
test native::projects::tests::parse::project_parser_reads_parent_wikilink_target ... ok
test native::projects::tests::parse::project_parser_reports_invalid_and_duplicate_inline_prj_scheduled ... ok
test native::projects::tests::surface::surface_agrees_blocked_sibling_hides ... ok
test native::projects::tests::parse::project_parser_accepts_prj_tag_and_strips_it_from_description ... ok
test native::plugins::tests::repeat_noop_leaves_stamp_untouched ... ok
test native::projects::tests::surface::surface_agrees_hidden_sibling_surfaces ... ok
test native::plugins::tests::sync_preserves_runtime_data_json ... ok
test native::projects::tests::surface::surface_agrees_frontmatter_schedule_defers ... ok
test native::projects::tests::edits::project_schedule_accepts_quoted_dates_and_rejects_bad_dates ... ok
test native::projects::tests::surface::surface_agrees_open_sibling_hides ... ok
test native::projects::tests::sync::project_sync_plan_does_not_hoist_without_open_prj ... ok
test native::projects::tests::parse::project_parser_stops_prj_sub_block_at_blank_line ... ok
test native::projects::tests::sync::project_sync_plan_keeps_canonical_closed_subprojects_idempotent ... ok
test native::projects::tests::surface::surface_rejects_unplannable_notes ... ok
test native::projects::tests::sync::project_sync_plan_keeps_inline_prj_scheduled_and_surfaces ... ok
test native::projects::tests::sync::project_sync_plan_flips_status_without_prj_edits_after_effective_status ... ok
test native::projects::tests::sync::project_sync_plan_hoists_frontmatter_scheduled_onto_prj ... ok
test native::plugins::tests::tracked_stamp_refuses_even_with_force ... ok
test native::projects::tests::surface::surface_agrees_dated_recount ... ok
test native::projects::tests::sync::project_sync_plan_is_idempotent_when_prj_hide_tag_matches_dash_state ... ok
test native::projects::tests::surface::surface_agrees_fence_quote_and_custom_counts ... ok
test native::projects::tests::sync::project_sync_plan_leaves_terminal_frontmatter_scheduled_untouched ... ok
test native::projects::tests::sync::project_sync_plan_marks_tracked_closed_subprojects ... ok
test native::projects::tests::sync::project_sync_plan_leaves_non_terminal_open_prj_status_untouched ... ok
test native::projects::tests::sync::project_sync_plan_matches_subproject_links_case_insensitively ... ok
test native::plugins::tests::list_reports_uncommitted_deployment ... ok
test native::projects::tests::sync::render_subprojects_line_formats_closed_children_after_open_children ... ok
test native::projects::tests::sync::subproject_display_parser_scopes_schedule_and_lifecycle_markers ... ok
test native::projects::tests::sync::project_sync_plan_treats_user_sub_bullets_as_user_owned ... ok
test native::plugins::tests::backup_failure_aborts_overwrite ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subprojects_marker_line ... ok
test native::projects::tests::sync::project_sync_plan_normalizes_subprojects_marker_drift ... ok
test native::projects::tests::surface::surface_marker_proxy_divergence_and_agreement ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subproject_schedule_markers ... ok
test native::randomize_plan::tests::identical_lines_get_distinct_rolls ... ok
test native::randomize_plan::tests::counts_due_p0_tasks_but_ignores_the_rest ... ok
test native::randomize_plan::tests::dates_survive_insertions_above_because_identity_ignores_lines ... ok
test native::randomize_plan::tests::fixed_offsets_cross_month_year_and_leap_boundaries ... ok
test native::projects::tests::sync::project_sync_plan_warns_on_placeholder_while_reopening ... ok
test native::randomize_plan::tests::ignores_tasks_scheduled_after_until ... ok
test native::randomize_plan::tests::ignores_non_open_and_fieldless_and_foreign_tasks ... ok
test native::plugins::tests::pull_repo_fast_forwards_from_remote ... ok
test native::projects::tests::sync::project_sync_plan_reopens_terminal_project_from_open_prj ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_unhidden_count ... ok
test native::projects::tests::sync::subproject_state_treats_terminal_open_prj_child_as_open ... ok
test native::randomize_plan::tests::extreme_priority_window_fails_before_any_write ... ok
test native::randomize_plan::tests::level_filtering_counts_not_selected ... ok
test native::randomize_plan::tests::level_filtering_matches_labels_case_insensitively ... ok
test native::randomize_plan::tests::load_covers_35_days_with_p0_and_new_dates ... ok
test native::randomize_plan::tests::keeps_paren_fields_and_spacing_when_replacing_the_date ... ok
test native::randomize_plan::tests::matches_pomodoro_targets_by_path_stem_and_case ... ok
test native::randomize_plan::tests::same_inputs_give_the_same_plan ... ok
test native::randomize_plan::tests::ordinary_and_daily_notes_are_edited_but_not_regrouped ... ok
test native::randomize_plan::tests::project_note_postimage_moves_the_task_under_blocked ... ok
test native::randomize_plan::tests::roll_at_the_representable_boundary_succeeds_and_past_it_fails ... ok
test native::randomize_plan::tests::project_postimage_is_byte_exact_with_blocked_move_and_badge ... ok
test native::projects::tests::sync::subproject_aggregation_marks_only_schedules_after_shared_today ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_open_subprojects ... ok
test native::randomize_plan::tests::skips_duplicate_priority_and_scheduled_fields ... ok
test native::randomize_plan::tests::skips_unparseable_scheduled_dates ... ok
test native::randomize_plan::tests::skips_unknown_priority_values_with_detail ... ok
test native::randomize_plan::tests::rerolls_ready_and_blocked_tasks ... ok
test native::randomize_plan::tests::reroll_carries_every_json_task_field ... ok
test native::randomize_plan::tests::zero_width_window_reports_unchanged_without_writing ... ok
test native::randomize_plan::tests::skips_hard_dates_from_fields_and_emoji ... ok
test native::randomize_plan::tests::skips_non_ready_open_statuses ... ok
test native::ref_jobs::kick::tests::kick_disable_values ... ok
test native::ref_jobs::output::tests::age_buckets_match_human_table ... ok
test native::ref_jobs::output::tests::empty_view_counts_nothing ... ok
test native::ref_jobs::spool::tests::corrupt_done_lines_are_skipped ... ok
test native::randomize_plan::tests::until_shifts_both_the_cutoff_and_the_roll_base ... ok
test native::randomize_plan::tests::skips_tasks_linked_from_open_pomodoros_in_every_link_form ... ok
test native::ref_jobs::fallback::tests::fallback_refuses_a_missing_vault_root ... ok
test native::ref_jobs::fallback::tests::fallback_creates_missing_target_like_capture ... ok
test native::ref_library::attach::tests::a_unit_cannot_match_across_a_page_boundary ... ok
test native::ref_jobs::spool::tests::parentless_jobs_read_as_none_and_use_the_source_inbox ... ok
test native::ref_library::attach::tests::attach_json_envelope_names_every_candidate ... ok
test native::ref_library::attach::tests::compatibility_folding_unifies_quotes_and_dashes ... ok
test native::ref_library::attach::tests::longest_paragraphs_select_but_keep_document_order ... ok
test native::ref_library::attach::tests::prose_stripping_keeps_words_not_markup ... ok
test native::ref_library::attach::tests::dropped_glyph_costs_one_character_inside_a_long_line ... ok
test native::ref_library::attach::tests::repeated_generic_fragments_cannot_be_scattered_or_reused ... ok
test native::ref_jobs::fallback::tests::fallback_appends_under_existing_tasks_with_file_indent ... ok
test native::ref_jobs::fallback::tests::concurrent_edit_retries_and_commits_once ... ok
test native::ref_library::attach::tests::titles_compare_case_and_whitespace_insensitively ... ok
test native::ref_jobs::fallback::tests::stale_preimage_is_a_conflict_error ... ok
test native::ref_library::attach::tests::materially_changed_unit_below_threshold_does_not_match ... ok
test native::ref_library::blocked_by::tests::depends_on_ids_skip_code_and_keep_order ... ok
test native::ref_library::blocked_by::tests::future_schedule_is_a_reason_today_is_not ... ok
test native::ref_library::attach::tests::verify_candidate_uses_character_matching_for_blocks_and_paragraphs ... ok
test native::ref_jobs::spool::tests::job_ids_are_unique_and_shaped ... ok
test native::ref_jobs::spool::tests::job_json_round_trips_with_all_fields ... ok
test native::ref_library::attach::tests::out_of_order_lines_do_not_form_one_matching_unit ... ok
test native::ref_library::blocked_by::tests::project_tag_is_exact_and_ignores_code ... ok
test native::ref_library::blocked_by::tests::human_suffix_joins_reasons_in_order ... ok
test native::ref_library::coverage::tests::id_lid_and_book_target_extraction ... ok
test native::ref_library::coverage::tests::mismatched_source_id_does_not_mirror ... ok
test native::ref_library::coverage::tests::multibyte_lines_never_panic_or_count ... ok
test native::ref_library::coverage::tests::non_zorg_status_values_do_not_count ... ok
test native::ref_library::coverage::tests::owner_requires_less_indent ... ok
test native::ref_library::blocked_by::tests::priority_reads_known_values_and_ignores_code ... ok
test native::ref_library::coverage::tests::record_block_range_keeps_internal_blank_lines ... ok
test native::ref_library::blocked_by::tests::scheduled_requires_a_strict_date_outside_code ... ok
test native::ref_library::coverage::tests::shared_block_pair_stays_distinct_by_source_id ... ok
test native::ref_library::coverage::tests::status_lines_count_and_mirrored_records_subtract ... ok
test native::ref_library::coverage::tests::book_note_source_blocks_subtract_chapters ... ok
test native::ref_library::lineage::tests::parses_block_entries_with_labels ... ok
test native::ref_library::links::tests::autolink_label_trims_context_punctuation ... ok
test native::ref_library::links::tests::autolink_falls_back_to_url_label_without_context ... ok
test native::ref_library::lineage::tests::parses_inline_and_bare_forms ... ok
test native::ref_library::links::tests::markdown_escapes_text_and_wraps_awkward_destinations ... ok
test native::ref_library::links::tests::written_link_uses_text_label_and_bracket_markdown ... ok
test native::ref_library::links::tests::site_covers_www_mailto_and_obsidian ... ok
test native::ref_library::list::tests::git_births_follow_renames_and_keep_the_first_add ... ok
test native::ref_library::list::tests::ref_history_parses_per_file_marks_newest_first ... ok
test native::ref_library::list::tests::since_accepts_absolute_and_relative_dates ... ok
test native::ref_jobs::spool::tests::spool_dirs_and_files_use_strict_modes ... ok
test native::ref_library::migrate_tasks::line::tests::keeps_fields_and_mark ... ok
test native::ref_library::list::tests::selection_defaults_to_the_queue_without_filters ... ok
test native::plugins::tests::nongit_source_requires_force_after_first_deploy ... ok
test native::ref_library::migrate_tasks::line::tests::migrates_basic_v1_line ... ok
test native::ref_library::migrate_tasks::write::tests::restore_returns_diverged_and_restores_clean ... ok
test native::ref_library::migrate_zorg::plan::tests::ref_kind_reads_only_lib_targets ... ok
test native::ref_library::migrate_zorg::render::tests::book_note_folds_chapters_byte_for_byte ... ok
test native::ref_library::migrate_zorg::render::tests::acronym_words_uppercase_when_humanized ... ok
test native::ref_library::migrate_zorg::plan::tests::hub_stem_strips_extension ... ok
test native::ref_library::migrate_zorg::render::tests::plain_record_renders_byte_for_byte ... ok
test native::ref_library::migrate_zorg::render::tests::title_folds_continuation_lines ... ok
test native::ref_library::migrate_zorg::render::tests::owner_line_tags_skip_zorg_ids ... ok
test native::ref_jobs::spool::tests::pending_keys_covers_pending_and_running ... ok
test native::highlights_ref::overwrite::execute::tests::older_archive_save_survives_second_overwrite_crash_recovery ... ok
test native::plugins::tests::pending_stamp_refuses_until_forced ... ok
test native::ref_library::migrate_zorg::render::tests::related_keeps_only_pipe_lines ... ok
test native::ref_library::migrate_zorg::render::tests::url_field_reads_inline_first_token_and_nested_items ... ok
test native::projects::tests::sync::project_sync_plan_skips_subproject_links_without_open_prj_edits ... ok
test native::ref_library::migrate_zorg::render::tests::wikilinks_reduce_to_display_text ... ok
test native::highlights_ref::overwrite::execute::tests::two_annotated_overwrites_keep_newest_first_archives_and_task ... ok
test native::ref_library::output::tests::chips_carry_glyph_word_and_color ... ok
test native::ref_library::output::tests::list_human_blocked_reason_is_dim_and_drops_before_the_title ... ok
test native::ref_library::output::tests::list_human_groups_carry_color_and_counts ... ok
test native::ref_library::output::tests::markdown_cells_escape_pipes_and_newlines ... ok
test native::ref_library::show::tests::markdown_digest_groups_sections ... ok
test native::ref_library::show::tests::comments_only_hides_section_headers_without_kept_members ... ok
test native::ref_library::show::tests::human_render_groups_sections_plain_and_color ... ok
test native::ref_library::show::tests::human_render_carries_chips_color_and_structure ... ok
test native::ref_library::show::tests::markdown_digest_keeps_quote_comment_and_tasks ... ok
test native::ref_library::show::tests::quote_emphasis_is_underlined_bold_in_color_output ... ok
test native::ref_library::migrate_zorg::write::tests::commit_message_names_records_notes_and_rollback ... ok
test native::plugins::tests::tracked_folder_warns_but_still_syncs ... ok
test native::ref_library::show::tests::quote_emphasis_reopens_after_wrapping ... ok
test native::ref_jobs::kick::tests::kicked_child_leaves_session_and_stdio ... ok
test native::projects::tests::sync::subproject_parent_links_classify_open_and_terminal_prj_children ... ok
test native::ref_library::show::tests::quote_emphasis_keeps_edge_whitespace_unpainted ... ok
test native::ref_library::show::tests::unsectioned_markdown_stays_byte_identical ... ok
test native::ref_library::show::tests::quote_lines_preserve_split_emphasis_delimiters ... ok
test native::ref_library::show::tests::quote_lines_consume_split_opening_and_later_runs ... ok
test native::ref_library::status::tests::book_without_chapters_stays_unknown ... ok
test native::ref_library::status::tests::non_book_legacy_ignores_chapter_statuses ... ok
test native::ref_library::status::tests::book_derivation_covers_every_branch ... ok
test native::ref_library::show::tests::show_section_json_omits_empty_optional_fields ... ok
test native::ref_library::tests::added_at_uses_a_matching_created_instant ... ok
test native::ref_library::show::tests::wrap_hard_splits_long_words_and_keeps_blanks ... ok
test native::plugins::tests::same_checkout_dirty_iteration_is_permitted ... ok
test native::ref_jobs::spool::tests::done_log_trims_to_last_thousand ... ok
test native::ref_library::migrate_zorg::write::tests::write_then_verify_round_trip ... ok
test native::ref_library::migrate_zorg::write::tests::write_refuses_pre_existing_target_and_rolls_back_partial ... ok
test native::ref_library::migrate_zorg::write::tests::verify_failure_deletes_created_files_and_prunes_own_dirs ... ok
test native::ref_library::show::tests::quote_lines_keep_emphasis_at_one_content_column ... ok
test native::plugins::tests::sync_creates_updates_and_leaves_unchanged ... ok
test native::ref_library::tests::missing_ref_dir_is_an_error ... ok
test native::ref_library::tests::medium_twins_share_one_identity_key ... ok
test native::ref_library::tests::query_classification_table ... ok
test native::ob::tests::lock_wait_behavior ... ok
test native::plugins::tests::dry_run_carries_ignore_warning_without_writing ... ok
test native::plugins::tests::symlink_alias_counts_as_same_checkout ... ok
test native::ref_library::tests::section_cards_do_not_change_ref_list_annotation_or_reading_counts ... ok
test native::ref_jobs::kick::tests::kicked_worker_drains_a_seeded_job ... ok
test native::plugins::tests::dry_run_refuses_without_writing ... ok
test native::ref_library::attach::tests::source_record_pass_preserves_route_section_numbering ... ok
test native::ref_library::tests::title_scoring_table ... ok
test native::ref_tasks::edit::tests::finds_moved_line_by_unique_content ... ok
test native::plugins::tests::sync_json_shape_is_stable ... ok
test native::ref_tasks::edit::tests::flips_checkbox_and_stamps_close ... ok
test native::ref_tasks::edit::tests::missing_destination_fails_before_any_write ... ok
test native::plugins::tests::unignored_folder_warns_but_still_syncs ... ok
test native::ref_tasks::edit::tests::flips_quoted_task_preserving_quote_and_children ... ok
test native::plugins::tests::sync_refuses_then_forces_a_dirty_vault_file ... ok
test native::ref_tasks::edit::tests::preserves_crlf_and_neighbor_bytes ... ok
test native::ref_tasks::edit::tests::preserves_existing_close_stamp ... ok
test native::ref_tasks::insert::tests::archive_read_errors_propagate ... ok
test native::ref_tasks::edit::tests::refuses_deleted_changed_and_duplicate_lines ... ok
test native::plugins::tests::clean_nonancestor_is_refused ... ok
test native::ref_tasks::edit::tests::preserves_mixed_endings_and_final_newline ... ok
test native::ref_tasks::insert::tests::archive_collision_blocks_preferred_id ... ok
test native::ref_tasks::edit::tests::unrelated_user_additions_survive ... ok
test native::ref_tasks::insert::tests::preferred_id_reused_when_free ... ok
test native::ref_tasks::insert::tests::missing_destination_is_created ... ok
test native::ref_tasks::insert::tests::collision_reallocates_and_children_join ... ok
test native::ref_tasks::insert::tests::preferred_id_suffixed_when_destination_taken ... ok
test native::ref_tasks::tests::diagnostic_code_catalog_lists_every_code ... ok
test native::ref_tasks::tests::excluded_dirs_and_conflict_copies_are_never_read ... ok
test native::ref_tasks::tests::closed_at_birth_carries_completion_or_cancelled_stamp ... ok
test native::ref_tasks::tests::blockquote_task_counts ... ok
test native::ref_tasks::tests::fenced_frontmatter_embed_and_managed_embed_are_ignored ... ok
test native::ref_tasks::tests::managed_embed_matches_positive_and_negative_cases ... ok
test native::ref_tasks::tests::managed_slot_ignores_later_authored_embed ... ok
test native::ref_tasks::tests::insert_checks_archive_and_preserves_crlf ... ok
test native::ref_tasks::tests::missing_path_target_is_keyed_for_adoption_and_orphaned ... ok
test native::highlights_ref::create::tests::section_numbering_xelatex_render_numbers_from_top_level ... ok
test native::ref_tasks::tests::bare_unique_stem_resolves_but_collision_is_ambiguous ... ok
test native::ref_tasks::tests::open_in_done_is_report_only_and_open_v1_always_fires ... ok
test native::ref_tasks::tests::reading_alias_appends_version_and_fits_long_titles ... ok
test native::ref_tasks::tests::outside_area_fires_for_daily_and_hub_notes ... ok
test native::ref_tasks::tests::reading_identity_keeps_version_before_truncation ... ok
test native::ref_tasks::tests::follow_up_full_path_is_attributed_but_same_note_is_not ... ok
test native::plugins::tests::dirty_deploy_from_other_checkout_is_refused ... ok
test native::ref_tasks::tests::ref_dir_outside_vault_yields_empty_index ... ok
test native::ref_tasks::tests::path_qualified_resolution_with_case_insensitive_fallback ... ok
test native::ref_tasks::tests::ref_task_without_link_is_orphan ... ok
test native::highlights_ref::create::tests::listen_card_xelatex_render_uses_only_existing_packages ... ok
test native::plugins::tests::ignored_folder_has_no_warning_in_git_vault ... ok
test native::ref_library::tests::arxiv_and_doi_identities_share_keys_and_conflict ... ok
test native::plugins::tests::git_vault_requires_ignored_untracked_stamp ... ok
test native::plugins::tests::clean_exact_match_lands_then_descendant_updates ... ok
test native::ref_tasks::tests::render_sanitizes_collapses_and_truncates_title ... ok
test native::ref_tasks::tests::selection_rules_cover_open_ambiguity_closed_v1_and_empty ... ok
test native::ref_tasks::tests::slug_ascii_empty_length_and_numeric_collisions ... ok
test native::relation_labels::rename::tests::line_views_preserve_crlf_offsets_and_final_newline ... ok
test native::ref_tasks::tests::v1_caret_line_is_never_candidate_or_orphan ... ok
test native::relation_labels::tests::vector_keys_match_the_one_key_function ... ok
test native::relation_labels::rename::tests::replace_spans_only_changes_the_requested_bytes ... ok
test native::ref_tasks::tests::references_does_not_count_but_uppercase_ref_does ... ok
test native::relation_labels::tests::inverse_phrases_match_the_contract_table ... ok
test native::relation_labels::tests::shared_vectors_cover_key_catalog_fold_and_rank ... ok
test native::relation_labels::tests::catalog_scan_prunes_vanished_vaults_and_sweeps_orphan_files ... ok
test native::relation_labels::tests::vector_folds_match_last_writer_wins ... ok
test native::relation_labels::tests::vector_catalogs_scan_every_scope ... ok
test native::stats::cli::tests::metrics_rejects_csv ... ok
test native::stats::cli::tests::show_all_skips_metric ... ok
test native::stats::cli::tests::overview_parses_format_json ... ok
test native::stats::cli::tests::show_requires_metric_or_all ... ok
test native::relation_labels::tests::journal_append_round_trips_through_the_host_file ... ok
test native::relation_labels::tests::vector_ranks_match_prefix_then_substring ... ok
test native::ref_tasks::tests::wrapper_without_ref_is_not_a_candidate ... ok
test native::ref_library::tests::chat_notes_are_agent_reports_with_queue_states ... ok
test native::ref_library::tests::added_dates_cover_created_and_zorg_block ... ok
test native::ref_library::tests::url_queries_match_identity_including_www_variants ... ok
test native::stats::compute::tests::malformed_range_config_and_request_fail_as_usage_or_config_errors ... ok
test native::stats::compute::tests::real_vault_parity_is_opt_in ... ok
test native::ref_library::tests::blocked_tracker_defers_to_frontmatter_without_diagnostic ... ok
test native::stats::compute::tests::missing_vault_is_io_and_emoji_vault_is_format ... ok
test native::ref_tasks::tests::residence_covers_root_done_and_other_with_outside_area ... ok
test native::stats::compute::tests::selecting_an_invalidated_metric_includes_the_registry_warning ... ok
test native::stats::compute::tests::unknown_metric_is_a_request_error_with_schema_one_envelope ... ok
test native::stats::error::tests::envelope_is_schema_one ... ok
test native::stats::error::tests::io_is_exit_one_config_is_exit_two ... ok
test native::stats::formula::tests::dependencies_dedupe_first_seen ... ok
test native::ref_library::tests::legacy_status_table_maps_every_reading_state ... ok
test native::stats::formula::tests::net_evaluates_with_worst_input_quality ... ok
test native::stats::formula::tests::non_formula_metrics_evaluate_elsewhere ... ok
test native::stats::formula::tests::division_rounds_half_away_from_zero ... ok
test native::stats::formula::tests::parses_literals_unary_parens_and_products ... ok
test native::stats::formula::tests::parser_rejects_nesting_deeper_than_sixty_four ... ok
test native::stats::formula::tests::rejects_empty_trailing_and_non_code ... ok
test native::stats::formula::tests::null_inputs_propagate_null_with_worst_quality_and_names ... ok
test native::stats::formula::tests::unevaluated_dependencies_warn_once_and_read_null ... ok
test native::stats::formula::tests::inferred_since_is_the_latest_dependency_since ... ok
test native::stats::formula::tests::division_by_zero_and_overflow_are_null_not_panics ... ok
test native::stats::homes::tests::lead_root_groups_tasks_not_projects ... ok
test native::stats::formula::tests::parses_net_builtin_expression ... ok
test native::ref_library::tests::malformed_yaml_falls_back_and_reports ... ok
test native::ref_library::tests::every_diagnostic_code_is_represented ... ok
test native::highlights_ref::note_snapshot::fonts::tests::triangular_bullet_selects_mono_before_fallback ... ok
test native::ref_library::tests::clipped_blog_row_covers_media_dates_and_tombstones ... ok
test native::stats::index::tests::default_index_is_empty ... ok
test native::ref_library::tests::task_priority_and_scheduled_and_blocked_by_cover_the_contract ... ok
test native::ref_library::tests::arxiv_queries_strip_versions_and_order_by_state ... ok
test native::stats::index::tests::interface_rows_hold_residence_dates_and_journal_facts ... ok
test native::ref_library::tests::legacy_unread_is_superseded_by_the_pdf_capture ... ok
test native::ref_library::tests::path_name_and_title_queries ... ok
test native::ref_library::tests::region_oddities_exclude_preamble_and_report_unparsed ... ok
test native::highlights_ref::note_snapshot::profile::tests::spaces_in_paths_remain_single_arguments ... ok
test native::ref_library::tests::building_the_index_writes_nothing ... ok
test native::ref_library::tests::pending_and_conflict_status_precedence ... ok
test native::stats::index::tests::invalid_utf8_journal_lines_are_malformed_not_io ... ok
test native::stats::index::tests::missing_vault_directory_fails_as_io ... ok
test native::stats::index::tests::journal_reader_validates_lines_and_orders_offsets_and_ties_deterministically ... ok
test native::stats::compute::tests::week_grouping_adds_daily_points_and_a_week_chart_band ... ok
test native::ref_library::tests::synced_paper_row_covers_the_core_fields ... ok
test native::ref_library::tests::wikilink_parent_and_opaque_url ... ok
test native::ref_library::tests::url_miss_falls_back_to_slug_title_candidates ... ok
test native::stats::compute::tests::default_range_and_overview_report_four_weeks ... ok
test native::stats::index::tests::settings_parse_and_task_format_fail_with_stats_errors ... ok
test native::ref_library::tests::tracker_dates_cover_bracket_cancelled_and_emoji_forms ... ok
test native::capture_related::tests::synthetic_vault_query_is_under_250ms ... ok
test native::ref_library::tests::index_membership_and_coverage ... ok
test native::stats::index::tests::archive_residence_and_parent_chains_resolve_with_cycle_and_ambiguity_guards ... ok
test native::stats::journal::tests::last_answer_follows_instant_not_timestamp_string ... ok
test native::stats::journal::tests::malformed_only_closed_review_day_is_a_gap ... ok
test native::stats::journal::tests::custom_tier_lists_filter_reviewed_and_intersect_keep_rate ... ok
test native::stats::compute::tests::golden_vault_reports_all_builtins_and_every_custom_kind ... ok
test native::stats::index::tests::unreadable_markdown_surfaces_io ... ok
test native::stats::index::tests::canonical_daily_notes_include_ledgers_and_ignore_lookalikes ... ok
test native::stats::index::tests::excluded_directories_are_skipped_and_done_is_included ... ok
test native::stats::index::tests::future_scheduled_dates_are_not_invalid ... ok
test native::stats::index::tests::yaml_null_frontmatter_fields_are_absent ... ok
test native::stats::index::tests::ordered_list_task_fields_do_not_leak_into_daily_fields ... ok
test native::ref_library::tests::top_level_note_has_no_status_type_or_tracker ... ok
test native::highlights_ref::create::tests::diagrams_swap_pdf_replaces_source_without_figure_caption ... ok
test native::stats::journal::tests::missing_review_closed_reports_a_limitation_not_a_gap ... ok
test native::stats::index::tests::task_parser_honors_custom_done_non_task_fences_and_date_diagnostics ... ok
test native::stats::journal::tests::gap_uses_the_registry_review_closed_evaluation ... ok
test native::stats::compute::tests::review_closed_redefined_as_formula_still_gates_journal_gaps ... ok
test native::highlights_ref::note_snapshot::profile::tests::fake_commands_verify_flags_cwd_order_and_two_passes ... ok
test native::stats::index::tests::ref_tag_without_block_id_classifies_as_ref_kind ... ok
test native::stats::compute::tests::named_preset_range_is_reported ... ok
test native::stats::index::tests::symlinked_directories_are_not_followed ... ok
test native::stats::journal::tests::non_journal_metrics_evaluate_elsewhere ... ok
test native::stats::journal::tests::unknown_outcome_including_checkmark_suffix_is_other ... ok
test native::stats::metrics::tests::checklist_early_completion_uses_the_completion_day ... ok
test native::stats::journal::tests::reader_vectors_match_the_shared_fixture ... ok
test native::stats::journal::tests::recorded_writer_vectors_feed_the_reader ... ok
test native::stats::index::tests::reads_each_markdown_file_once_and_restores_path_order ... ok
test native::ref_library::tests::tracker_diagnostics_fall_back_to_frontmatter ... ok
test native::stats::metrics::tests::checklist_intervals_deduplicate_chore_and_separate_met_from_missed ... ok
test native::stats::metrics::tests::checklist_nothing_due_is_missing_and_future_schedule_is_not_due ... ok
test native::stats::metrics::tests::checklist_tag_prefixes_do_not_match ... ok
test native::stats::metrics::tests::overnight_pomodoro_range_counts_its_minutes ... ok
test native::stats::metrics::tests::non_canonical_daily_gtd_row_is_not_excluded ... ok
test native::stats::metrics::tests::explicit_since_earlier_than_first_input_is_tracked ... ok
test native::stats::metrics::tests::review_time_predicate_drops_composite_theme_sessions ... ok
test native::stats::metrics::tests::theme_shares_keep_the_original_split_without_a_home_filter ... ok
test native::stats::metrics::tests::pomodoro_minutes_prefer_recorded_duration_and_split_odd_minutes ... ok
test native::stats::metrics::tests::path_qualified_in_does_not_match_a_same_basename_elsewhere ... ok
test native::stats::range::tests::labels_round_trip_presets ... ok
test native::stats::metrics::tests::recurring_modes_and_prj_kind_are_honored ... ok
test native::stats::range::tests::parses_explicit_inclusive_dates ... ok
test native::stats::range::tests::parses_presets_and_lengths ... ok
test native::stats::registry::tests::invalid_redefinition_does_not_fall_back ... ok
test native::stats::registry::tests::invalid_pomodoro_review_is_a_local_warning ... ok
test native::stats::metrics::tests::pomodoro_missing_section_empty_section_and_unreadable_time_are_distinct ... ok
test native::stats::metrics::tests::task_events_filter_status_recurring_tags_kind_archive_and_gtd ... ok
test native::stats::metrics::tests::checklist_reads_archive_rows_and_requires_done_plus_completion ... ok
test native::stats::range::tests::rejects_zero_negative_overflow_and_inverted ... ok
test native::stats::registry::tests::eleven_builtins_share_the_user_parser ... ok
test native::stats::metrics::tests::field_bracket_values_evaluate_as_minutes ... ok
test native::stats::metrics::tests::field_values_are_typed_and_either_does_not_fallback_after_invalid_frontmatter ... ok
test native::stats::metrics::tests::global_since_does_not_fabricate_a_start ... ok
test native::stats::registry::tests::invalidating_dropped_invalidates_net ... ok
test native::stats::registry::tests::hide_keeps_the_definition_for_deps_and_explicit_select ... ok
test native::stats::registry::tests::custom_builtin_id_replaces_the_whole_definition ... ok
test native::stats::registry::tests::pomodoro_in_and_review_filters_parse ... ok
test native::stats::registry::tests::non_string_metric_key_is_an_invalid_id ... ok
test native::stats::registry::tests::rejects_bad_task_kind_hex_color_and_formula_ratio_unit ... ok
test native::stats::registry::tests::unknown_explicit_metric_is_a_request_error ... ok
test native::stats::registry::tests::task_kind_filter_is_not_the_metric_kind ... ok
test native::stats::render::tests::detail_prints_every_task_parts_dimension ... ok
test native::stats::render::tests::detail_prints_every_pomodoro_parts_dimension ... ok
test native::stats::render::tests::bool_sparkline_marks_unmet_provisional_point_not_yet ... ok
test native::stats::render::tests::json_is_one_line ... ok
test native::stats::render::tests::net_detail_header_drops_vs_prior ... ok
test native::stats::render::tests::overview_colored_paints_sparkline ... ok
test native::stats::render::tests::sparkline_uses_null_mark_and_blocks ... ok
test native::stats::render::tests::overview_plain_contains_labels_and_today ... ok
test native::stats::render::tests::theme_dimension_uses_theme_squares_and_respects_no_color ... ok
test native::stats::render::tests::overview_header_says_summary_and_total_suffix_has_space ... ok
test native::stats::render::tests::csv_has_tidy_header_and_empty_null_value ... ok
test native::stats::registry::tests::formula_unknown_refs_and_cycles_drop_dependents ... ok
test native::stats::request::tests::at_ignores_environment ... ok
test native::stats::request::tests::new_reads_bob_now_once ... ok
test native::stats::report::tests::success_report_matches_schema_one_shape ... ok
test native::stats::series::tests::auto_grouping_thresholds_at_ninety_two_three_seventy_one_and_two ... ok
test native::stats::series::tests::boolean_and_ratio_summaries_use_days_and_pooled_parts ... ok
test native::stats::series::tests::auto_grouping_uses_inclusive_thresholds_and_iso_weeks ... ok
test native::stats::homes::tests::h_vector_review_time_includes_a_gtd_share_inside_work ... ok
test native::stats::report::tests::ratio_and_grouped_fields_are_optional ... ok
test native::stats::series::tests::chart_bands_cover_signed_values_and_all_null_windows ... ok
test native::stats::series::tests::delta_uses_multipliers_for_large_changes_and_points_for_ratios ... ok
test native::stats::series::tests::day_chart_quartiles_match_the_daily_summary ... ok
test native::stats::series::tests::checklist_states_and_chore_denominators_use_complete_days ... ok
test native::stats::series::tests::every_delta_rule_has_a_hand_derived_case ... ok
test native::stats::series::tests::all_uses_effective_since_and_rejects_offsets ... ok
test native::stats::series::tests::grouped_buckets_exclude_the_provisional_today_point ... ok
test native::stats::series::tests::all_with_no_history_matches_preset_end_convention ... ok
test native::stats::registry::tests::malformed_metric_leaves_unrelated_entries ... ok
test native::stats::series::tests::chart_and_daily_points_exclude_today_and_lead_in ... ok
test native::stats::series::tests::first_displayed_point_uses_lead_in_for_rolling_median ... ok
test native::stats::series::tests::formatting_covers_every_metric_unit ... ok
test native::stats::series::tests::grouped_daily_points_clip_to_the_display_window ... ok
test native::stats::registry::tests::selecting_an_invalidated_metric_includes_the_registry_warning ... ok
test native::stats::series::tests::explicit_offset_moves_a_full_complete_window_back ... ok
test native::stats::series::tests::grouped_ratios_pool_counts_and_boolean_days ... ok
test native::stats::series::tests::iso_week_spanning_a_year_end_is_one_grouped_bucket ... ok
test native::stats::series::tests::leap_day_is_a_valid_range_day_and_month_bucket ... ok
test native::stats::series::tests::non_net_signed_and_count_metrics_keep_median_headline ... ok
test native::stats::series::tests::month_buckets_split_december_and_january ... ok
test native::stats::series::tests::month_and_year_windows_snap_to_weeks_and_explicit_ranges_clamp_today ... ok
test native::stats::series::tests::net_headline_is_window_total_not_median ... ok
test native::stats::series::tests::grouped_today_is_a_separate_provisional_point ... ok
test native::stats::series::tests::offsets_shift_full_windows_and_never_include_today ... ok
test native::stats::series::tests::parts_collapse_only_note_and_theme ... ok
test native::stats::series::tests::huge_offset_is_a_range_error_not_a_panic ... ok
test native::stats::series::tests::one_day_range_keeps_a_full_typical_window ... ok
test native::stats::series::tests::parts_summary_keeps_top_five_and_rolls_the_rest_into_other ... ok
test native::stats::series::tests::pooled_one_of_one_and_zero_of_nine_is_ten_percent ... ok
test native::stats::series::tests::parts_summary_keeps_every_area_and_project_key ... ok
test native::stats::series::tests::presets_include_today_as_provisional_and_prior_is_equal_length ... ok
test native::stats::series::tests::rolling_median_requires_half_window_and_excludes_provisional ... ok
test native::stats::series::tests::signed_net_delta_uses_range_total_words ... ok
test native::stats::series::tests::summary_quartiles_interpolate_and_round_half_away_from_zero ... ok
test native::stats::series::tests::parts_display_formats_minutes_and_leaves_counts ... ok
test native::stats::series::tests::typical_day_is_omitted_off_day_counts_and_minutes ... ok
test native::stats::series::tests::typical_day_has_no_verdict_on_today_or_on_days_without_values ... ok
test native::stats::series::tests::summaries_exclude_today_and_build_headline_stats_and_deltas ... ok
test native::stats::series::tests::typical_day_matches_the_research_vectors ... ok
test native::stats::series::tests::typical_day_is_omitted_on_prior_and_daily_points ... ok
test native::stats::series::tests::net_prior_headline_uses_window_total ... ok
test native::stats::series::tests::typical_day_needs_four_usable_days ... ok
test native::stats::series::tests::typical_day_uses_calendar_window_and_counts_only_usable_days ... ok
test native::stats::series::tests::typical_day_words_cover_minutes_counts_equal_and_zero ... ok
test native::stats::series::tests::unmet_provisional_bool_point_displays_not_yet ... ok
test native::stats::series::tests::typical_value_matches_the_prior_day_rolling_median ... ok
test native::stats::value::tests::quality_serializes_snake_case ... ok
test native::style::tests::bob_progress_one_is_the_only_progress_env_value ... ok
test native::style::tests::clicolor_force_enables_color_without_a_tty ... ok
test native::stats::series::tests::week_and_month_chart_bands_use_bucket_values ... ok
test native::stats::series::tests::typical_day_reports_above_below_and_equal ... ok
test native::style::tests::clicolor_force_zero_does_not_force_color ... ok
test native::style::tests::empty_clicolor_force_does_not_force_color ... ok
test native::stats::series::tests::typical_day_rounds_even_medians_half_away_from_zero ... ok
test native::style::tests::no_color_wins_over_tty_and_clicolor_force ... ok
test native::stats::series::tests::typical_day_skips_out_of_window_and_provisional_history ... ok
test native::stats::series::tests::typical_day_spans_month_and_year_boundaries_and_leap_days ... ok
test native::task_cancel::tests::a_second_cancel_attempt_is_closed_and_does_not_duplicate_the_log ... ok
test native::stats::series::tests::weekly_and_monthly_buckets_flag_clipped_edges_and_partial_data ... ok
test native::stats::series::tests::typical_day_spike_does_not_drag_the_next_week ... ok
test native::task_cancel::tests::failed_daily_read_propagates_without_a_partial_plan ... ok
test native::task_cancel::tests::new_york_midnight_date_is_supplied_to_the_pure_engine ... ok
test native::stats::tests::public_surface_wires_config_registry_and_request ... ok
test native::task_cancel::tests::cancelled_dependency_recovers_with_existing_rules_without_offers ... ok
test native::task_cancel::tests::relation_rule_vectors_exercise_the_production_policy_verdict ... ok
test native::task_cancel::tests::prune_vectors_use_task_identity_and_immediate_pomodoro_semantics ... ok
test native::task_cancel::tests::source_cancel_log_preserves_crlf_and_final_newline_state ... ok
test native::task_cancel::tests::key_vectors_share_the_relation_label_key_function ... ok
test native::task_cancel::tests::config_vectors_keep_cancel_policy_conservative_and_independent ... ok
test native::task_cancel::tests::source_and_daily_overlap_produce_one_coherent_postimage ... ok
test native::task_cancel::tests::yaml_mapping_entry_is_rejected_without_dropping_valid_peers ... ok
test native::task_cancel::tests::other_open_prerequisite_and_future_schedule_keep_dependents_blocked ... ok
test native::task_cancel::tests::cancelled_project_without_id_recovers_only_eligible_residents ... ok
test native::task_cancel::tests::cancel_vectors_drive_the_real_source_writer_and_plan ... ok
test native::stats::compute::tests::golden_typical_objects_are_hand_derived ... ok
test native::stats::compute::tests::month_grouping_pools_complete_days_and_marks_the_clipped_bucket ... ok
test native::task_complete::tests::project_pull_in_tests::pp12_in_progress_prj_links_unchanged ... ok
test native::task_complete::tests::project_pull_in_tests::pp22_hide_strip_bytes ... ok
test native::task_complete::tests::project_pull_in_tests::pp10_unplanned_predecessor_surfaces ... ok
test native::task_complete::tests::project_pull_in_tests::pp13_visible_linked_next_is_silent ... ok
test native::task_cancel::tests::another_project_dependency_keeps_a_resident_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp15_all_links_dependents_and_pull_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp1_last_task_close_pulls_in_prj ... ok
test native::task_cancel::tests::inherited_project_blocking_keeps_a_dependent_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp17_pull_in_wins_over_project_task ... ok
test native::task_cancel::tests::cancelling_a_project_does_not_reconcile_its_descendant_tree ... ok
test native::task_complete::tests::project_pull_in_tests::pp15_dependent_and_pull_in_link_together ... ok
test native::task_complete::tests::project_pull_in_tests::pp24_non_empty_note_keeps_project_task ... ok
test native::task_complete::tests::project_pull_in_tests::pp27_linked_blocked_prj_skips_unblocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp27_unplanned_blocked_prj_writes_unblocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp11_disabled_link_surfaces ... ok
test native::task_complete::tests::project_pull_in_tests::pp28_frontmatter_schedule_stays_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp14_id_less_close_pulls_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp25_blocked_prj_pull_in_recovers_hidden_resident ... ok
test native::task_complete::tests::project_pull_in_tests::pp24_cross_note_dependent_pulls_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp26_dated_recount_keeps_hidden_sibling ... ok
test native::task_complete::tests::project_pull_in_tests::pp31_non_project_parent_pulls_in_nothing ... ok
test native::task_complete::tests::project_pull_in_tests::pp3_blocked_sibling_suppresses_pull_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp2_open_sibling_suppresses_pull_in ... ok
test native::task_complete::tests::project_pull_in_tests::trigger_c_prefilter_skips_index_for_ordinary_closes ... ok
test native::task_complete::tests::recovery_tests::dependent_without_completed_prerequisite_stays_blocked ... ok
test native::task_complete::tests::recovery_tests::future_scheduled_dependent_stays_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp8_open_prerequisite_stays_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::pp26_undated_hidden_sibling_pulls_in ... ok
test native::highlights_ref::note_snapshot::profile::tests::third_pass_runs_only_on_rerun_and_stops_on_failure ... ok
test native::task_complete::tests::project_pull_in_tests::pp32_tagged_parent_pull_in_stays_blocked ... ok
test native::task_complete::tests::recovery_tests::second_open_prerequisite_keeps_dependent_blocked ... ok
test native::task_complete::tests::recovery_tests::non_blocked_dependent_is_untouched ... ok
test native::task_complete::tests::recovery_tests::pdc1_project_resident_stays_blocked ... ok
test native::task_complete::tests::recovery_tests::recovery_preserves_crlf_when_writing_unblocked ... ok
test native::task_complete::tests::recovery_tests::pdc3_resident_with_own_prerequisite_stays_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::gate_needs_dependents_cases ... ok
test native::task_complete::tests::project_pull_in_tests::pp4_hidden_sibling_pulls_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp7_future_schedule_stays_blocked ... ok
test native::task_complete::tests::project_pull_in_tests::so17_emptied_project_pull_in_unpicked ... ok
test native::task_complete::tests::project_pull_in_tests::r3_project_reason_carries_scheduled ... ok
test native::task_complete::tests::recovery_tests::sole_prerequisite_recovers_to_ready ... ok
test native::task_complete::tests::project_pull_in_tests::pp5_fenced_sibling_pulls_in ... ok
test native::task_complete::tests::recovery_tests::unresolved_dependency_id_does_not_block_recovery ... ok
test native::task_complete::tests::recovery_tests::pdc2_prj_recovery_recovers_residents ... ok
test native::task_complete::tests::retirement_tests::dedupe_drops_carried_copy_when_destination_already_links_task ... ok
test native::task_complete::tests::retirement_tests::dedupe_drops_carried_copy_when_completed_fallback_already_links_task ... ok
test native::task_complete::tests::retirement_tests::mixed_bullet_with_live_second_link_does_not_move ... ok
test native::task_complete::tests::retirement_tests::move_to_last_completed_entry_when_nothing_runs ... ok
test native::task_complete::tests::project_pull_in_tests::pp6_open_subproject_marker_suppresses_pull_in ... ok
test native::task_complete::tests::project_pull_in_tests::pp9_already_linked_recovers_planned ... ok
test native::task_complete::tests::retirement_tests::move_from_placeholder_to_running_removes_emptied_placeholder ... ok
test native::task_complete::tests::retirement_tests::reconcile_without_flag_moves_instead_of_deduping ... ok
test native::stats::compute::tests::invalid_custom_and_duplicate_overview_still_compute ... ok
test native::task_complete::tests::project_pull_in_tests::r1_punctuation_hide_linked_and_surfaced ... ok
test native::stats::compute::tests::builtin_limits_describe_task_checklist_and_journal_edges ... ok
test native::task_complete::tests::project_pull_in_tests::pp5_blockquoted_and_custom_siblings_suppress_pull_in ... ok
test native::task_complete::tests::project_pull_in_tests::r2_stale_blocked_cascade_needs_dependents ... ok
test native::task_complete::tests::project_pull_in_tests::pp20_unplannable_notes_stay_silent ... ok
test native::task_complete::tests::project_pull_in_tests::so18_parent_project_pull_in_unpicked ... ok
test native::task_complete::tests::project_pull_in_tests::pp33_unplanned_subproject_close_surfaces_parent ... ok
test native::task_complete::tests::retirement_tests::retirement_preserves_crlf ... ok
test native::task_complete::tests::successor_tests::closing_placement_creates_placeholder ... ok
test native::task_complete::tests::project_pull_in_tests::pp6_closed_subproject_marker_pulls_in ... ok
test native::task_complete::tests::retirement_tests::unrelated_already_done_link_is_left_untouched ... ok
test native::task_complete::tests::project_pull_in_tests::pp29_subproject_close_pulls_in_parent ... ok
test native::task_complete::tests::successor_tests::inbox_parity_shared_cases ... ok
test native::task_complete::tests::successor_tests::closing_placement_takes_lone_stub ... ok
test native::task_complete::tests::retirement_tests::strike_in_place_under_running_entry ... ok
test native::task_complete::tests::successor_tests::idless_root_anchors_id_bearing_child_dependent ... ok
test native::task_complete::tests::successor_tests::linked_prj_recovery_lands_next ... ok
test native::ref_library::tests::extra_pass_and_additive_id_resolution_agree_on_the_fixture ... ok
test native::task_complete::tests::successor_tests::relation_lines_are_not_successor_slot_anchors ... ok
test native::task_complete::tests::successor_tests::sl16_gate_without_ids_runs_nothing ... ok
test native::task_complete::tests::successor_tests::pdc1_dependent_in_still_blocked_project_stays_blocked ... ok
test native::task_complete::tests::successor_tests::sl25_planned_next_reports_nothing ... ok
test native::task_complete::tests::successor_tests::sl18_disabled_recovers_without_links_or_mints ... ok
test native::task_complete::tests::successor_tests::sl3_and_sl4_stay_blocked_with_reasons ... ok
test native::task_complete::tests::successor_tests::sl11_project_and_hidden_tasks_recover_only ... ok
test native::task_complete::tests::successor_tests::sl12_two_predecessors_link_once_at_earlier_anchor ... ok
test native::task_complete::tests::successor_tests::sl5_already_planned_recovers_without_link ... ok
test native::task_complete::tests::successor_tests::sl23_subtask_inherits_root_anchor ... ok
test native::task_complete::tests::successor_tests::sl1_links_blocked_dependent_into_slot ... ok
test native::task_complete::tests::successor_tests::sl28_day_file_successor_names_note ... ok
test native::task_complete::tests::successor_tests::sl13_chain_waits_and_sl15_stale_ready_links ... ok
test native::task_complete::tests::project_pull_in_tests::pp30_open_sibling_or_remaining_work_suppresses_parent_pull_in ... ok
test native::task_complete::tests::successor_tests::so16_unplanned_predecessor_two_open_timed_is_no_destination ... ok
test native::task_complete::tests::successor_tests::sl26_inbox_successor_links_with_flag ... ok
test native::task_complete::tests::successor_tests::sl9_unplanned_predecessor_links_at_implicit_destination ... ok
test native::task_complete::tests::successor_tests::sl10_mints_missing_block_id ... ok
test native::task_complete::tests::successor_tests::so4_pick_none_recovers_without_links ... ok
test native::task_complete::tests::successor_tests::slot_placement_orders_and_reports_lines ... ok
test native::task_complete::tests::successor_tests::sl6_struck_history_does_not_count_as_planned ... ok
test native::task_complete::tests::successor_tests::so20_pick_stamps_fresh_unpicked_writes_unblocked ... ok
test native::task_complete::tests::successor_tests::so15_unplanned_predecessor_no_open_entry_is_no_destination ... ok
test native::task_complete::tests::successor_tests::so3_pick_all_links_every_offer ... ok
test native::task_complete::tests::successor_tests::so5_pick_subset ... ok
test native::task_complete::tests::successor_tests::pdc2_prj_recovery_offers_residents ... ok
test native::task_complete::tests::successor_tests::pdc5_tagged_prj_loses_last_prerequisite_stays_blocked ... ok
test native::task_complete::tests::tree_tests::completion_field_spacing_with_and_without_block_id ... ok
test native::task_complete::tests::successor_tests::ub_close_next_landing_skips_unblocked ... ok
test native::task_complete::tests::tree_tests::unknown_status_descendant_is_left_open ... ok
test native::task_complete::tests::successor_tests::ub_close_ready_recovery_writes_unblocked ... ok
test native::task_complete::tests::successor_tests::pdc4_inherited_resident_stays_blocked_naming_parent ... ok
test native::task_complete::tests::successor_tests::ub_close_scheduled_tickler_skips_unblocked ... ok
test native::task_complete::tests::tree_tests::canceled_descendant_is_neither_closed_nor_reported ... ok
test native::task_complete::tests::successor_tests::uppercase_prj_lookalike_links_as_ordinary_successor ... ok
test native::task_complete::tests::tree_tests::done_root_is_a_no_op_that_still_closes_open_children ... ok
test native::task_complete::tests::successor_tests::pdc6_no_close_recovery_for_tagged_descendants ... ok
test native::task_complete::tests::successor_tests::pdc3_resident_with_own_prerequisite_stays_blocked ... ok
test native::task_complete::tests::tree_tests::explicit_blocked_descendant_child_stays_open ... ok
test native::task_complete::tests::tree_tests::explicit_completes_blocked_root_while_close_link_refuses_it ... ok
test native::task_complete::tests::tree_tests::explicit_done_descendant_is_not_descended ... ok
test native::task_complete::tests::successor_tests::so2_eleven_way_fan_out ... ok
test native::task_complete::tests::successor_tests::ub_close_new_recovery_skips_unblocked ... ok
test native::task_complete::tests::tree_tests::nested_embeds_close_with_blocked_and_recurring_left_open ... ok
test native::task_dependencies::tests::dependency_line_guard_matches_every_form ... ok
test native::task_dependencies::tests::dp_discovery_context_vectors ... ok
test native::task_dependencies::tests::dw_create_and_identity_vectors ... ok
test native::task_dependencies::blocks::tests::planner_covers_missing_rewritten_canonical_removed_duplicate_and_malformed ... ok
test native::task_dependencies::tests::dw_indent_and_ending_vectors ... ok
test native::task_dependencies::tests::dp_vectors ... ok
test native::highlights_ref::create::tests::short_diagram_prints_at_natural_size ... ok
test native::task_dependencies::tests::dw_link_form_vectors ... ok
test native::task_dependencies::tests::dw_writer_form_vectors ... ok
test native::task_dependencies::blocks::tests::bk_cross_parse_and_codepoint_sort_vectors ... ok
test native::task_dependencies::blocks::tests::bk_direct_child_discovery_vectors ... ok
test native::task_complete::tree::managed_dependency_tests::embedded_tree_skips_both_managed_dependency_lines ... ok
test native::task_dependencies::blocks::tests::bk_parse_vectors ... ok
test native::task_complete::tests::successor_tests::so7_direct_dependent_resident_stays_hand_off ... ok
test native::task_dependencies::blocks::tests::formats_canonical_brick_line ... ok
test native::task_dependencies::blocks::tests::delta_resolves_identities_then_applies_add_remove_and_sorts ... ok
test native::task_fields::tests::filters_by_key ... ok
test native::task_fields::tests::format_round_trips_through_strict_parse ... ok
test native::task_fields::tests::has_any_field_checks_several_keys ... ok
test native::task_dependencies::blocks::tests::insert_slot_follows_depends_subtree_and_cancel_log ... ok
test native::task_fields::tests::key_match_is_case_sensitive ... ok
test native::task_fields::tests::matches_with_no_space_after_the_colons ... ok
test native::task_fields::tests::finds_bracket_and_paren_forms ... ok
test native::task_fields::tests::matches_with_spacing_around_the_colons ... ok
test native::task_fields::tests::reports_exact_byte_ranges ... ok
test native::task_complete::tests::successor_tests::ub_close_hidden_resident_recovers_without_unblocked ... ok
test native::task_fields::tests::strict_date_rejects_non_dates ... ok
test native::task_fields::tests::canonical_theme_name_accepts_a_single_component ... ok
test native::task_move::command::tests::fail_keeps_the_primary_error_and_warns_about_later_failures ... ok
test native::task_move::command::tests::clap_accepts_mixed_repeated_block_and_match_selectors ... ok
test native::task_move::command::tests::clap_still_requires_at_least_one_selector ... ok
test native::task_fields::tests::reports_duplicate_fields_in_order ... ok
test native::task_move::command::tests::fatal_scan_does_not_retry_even_with_budget ... ok
test native::task_fields::tests::strict_date_rejects_impossible_february ... ok
test native::task_move::tests::dest_must_be_area_or_wip_waiting_project ... ok
test native::task_move::command::tests::zero_budget_makes_a_retryable_scan_terminal ... ok
test native::task_move::tests::intake_appends_after_prose_and_ignores_fenced_tasks_and_headings ... ok
test native::task_move::tests::collision_chain_renames_incoming_x_without_stealing_x_minus_one ... ok
test native::task_move::tests::match_selects_anchorless_task_without_minting_identity ... ok
test native::task_move::tests::carried_prj_is_blocked_tag_sets_reconcile_hint ... ok
test native::task_move::tests::collapses_source_removal_seams_and_preserves_crlf_and_eof ... ok
test native::task_complete::tests::successor_tests::so10_so11_so24_folds_and_open_subprojects ... ok
test native::task_move::tests::case_variants_share_note_identity_for_refusal_and_repair ... ok
test native::task_move::tests::closed_selection_refused_without_option_and_moves_with_it ... ok
test native::task_move::tests::load_snapshot_includes_done_skips_excluded_dirs_and_fails_on_non_utf8 ... ok
test native::task_move::tests::display_errors_include_candidates_and_ctrl_shift_m_guidance ... ok
test native::task_move::tests::encoded_identity_collision_is_refused_before_rewrite ... ok
test native::task_move::tests::dest_without_final_newline_keeps_original_ending_shape ... ok
test native::task_move::tests::destination_list_matches_move_rules_and_excludes_inboxes ... ok
test native::task_move::tests::fenced_and_frontmatter_task_text_is_not_selectable ... ok
test native::task_move::tests::explicit_root_filename_disambiguates_duplicate_stems ... ok
test native::task_move::tests::fenced_examples_are_not_live_identities_or_rewritten_links ... ok
test native::task_move::tests::dest_prj_dependency_is_refused_and_blocked_dest_accepts_only_blocked_tasks ... ok
test native::task_move::tests::inserts_into_ungrouped_and_grouped_intake_and_creates_area_tasks ... ok
test native::task_move::tests::no_selectors_is_an_error ... ok
test native::task_move::tests::project_without_tasks_is_refused ... ok
test native::task_move::tests::line_selector_moves_only_the_exact_line ... ok
test native::task_move::tests::nested_paths_encode_dependency_ids_and_leave_unresolved_links ... ok
test native::task_move::tests::missing_explicit_path_does_not_fall_back_to_basename ... ok
test native::task_move::tests::pathless_stayed_and_co_moved_links_and_unresolved_links ... ok
test native::task_move::tests::mixed_out_of_order_selectors_dedup_and_keep_source_order ... ok
test native::task_complete::tests::successor_tests::so1_project_offers_pick_one ... ok
test native::task_move::tests::moves_each_open_checkbox_via_block_and_match_selectors ... ok
test native::task_move::tests::nested_child_anchors_and_co_move_links_keep_review_fields ... ok
test native::task_move::tests::intake_keeps_the_badge_strip_and_appends_after_it ... ok
test native::task_complete::tests::project_pull_in_tests::pp31_parentless_subproject_close_pulls_in_nothing ... ok
test native::task_relations::label::tests::readers_accept_long_labels ... ok
test native::task_relations::tests::formats_canonical_lines ... ok
test native::task_move::tests::refuses_done_paths_same_note_and_missing_or_ambiguous_stems ... ok
test native::task_relations::tests::linked_from_children_skip_nested ... ok
test native::task_move::tests::refuses_non_canonical_id_fields ... ok
test native::task_relations::tests::lk20_codepoint_sort_matches_bk21 ... ok
test native::task_relations::label::tests::lw11_normalizes_and_refuses ... ok
test native::task_move::tests::stale_second_id_field_is_refused ... ok
test native::task_move::tests::zero_and_ambiguous_matches_list_candidates ... ok
test native::task_move::tests::unrepresentable_destination_identity_is_refused ... ok
test native::task_move::tests::source_pathless_backlink_to_moved_task_gains_destination_path ... ok
test native::task_relations::label::tests::quoted_form_uses_quotes_for_spaces ... ok
test native::task_move::tests::repairs_canonical_ids_and_preserves_absent_ids ... ok
test native::task_move::tests::repairs_every_required_link_form_across_note_kinds ... ok
test native::task_move::tests::refuses_closed_nested_prj_and_duplicate_source_anchors ... ok
test native::task_relations::tests::lw12_reuses_four_space_indent ... ok
test native::task_relations::tests::linked_from_delta_keeps_labels_and_sorts ... ok
test native::task_relations::tests::lw13_canonical_link_forms ... ok
test native::task_relations::tests::lk15_discovery_skips_fenced_grandchild_and_non_task ... ok
test native::task_relations::tests::lk19_cross_parse_vectors ... ok
test native::task_relations::tests::lw7_lw8_insert_slots ... ok
test native::task_relations::tests::lw9_merges_duplicate_links_lines ... ok
test native::task_relations::tests::mc15_recognisers_never_claim_relation_lines ... ok
test native::task_relations::tests::lw_planner_write_vectors ... ok
test native::task_status_groups::tests::authored_heading_inside_a_managed_group_fails_closed ... ok
test native::task_relations::tests::lw10_refuses_malformed_links_line ... ok
test native::task_status_groups::tests::badge_anchors_percent_encode_the_obsidian_path_segments ... ok
test native::task_relations::tests::lw11_label_rules_on_plan ... ok
test native::task_relations::tests::lk_parse_vectors ... ok
test native::task_relations::tests::relation_label_spans_cover_links_gaps_mirrors_and_aliases ... ok
test native::task_status_groups::tests::authored_topics_receive_local_groups ... ok
test native::task_relations::tests::rule6_linked_from_planner_table ... ok
test native::task_status_groups::tests::badge_counts_refresh_when_membership_changes ... ok
test native::highlights_ref::note_snapshot::fonts::tests::glyph_table_lists_fallback_only_characters ... ok
test native::task_status_groups::tests::blank_lines_between_tasks_normalize_away ... ok
test native::task_status_groups::tests::empty_global_filter_accepts_all_checkbox_tasks ... ok
test native::task_status_groups::tests::blockless_and_duplicate_ids_still_group ... ok
test native::task_status_groups::tests::custom_terminal_statuses_and_registry_precedence ... ok
test native::task_status_groups::tests::global_filter_rejects_non_matching_lines ... ok
test native::task_status_groups::tests::h6_tasks_is_skipped_with_a_diagnostic ... ok
test native::task_status_groups::tests::authored_child_containers_get_independent_badges_and_anchors ... ok
test native::task_status_groups::tests::duplicate_badge_rows_self_heal_into_the_slot ... ok
test native::task_status_groups::tests::badge_row_is_not_a_task_or_ambiguous_boundary ... ok
test native::task_status_groups::tests::heading_hash_in_ancestry_renders_unlinked_badges ... ok
test native::task_status_groups::tests::heading_only_first_setup_is_a_change ... ok
test native::stats::homes::tests::golden_json_carries_root_parent_beside_area_and_project ... ok
test native::task_status_groups::tests::is_badge_row_accepts_linked_unlinked_and_mixed_rows ... ok
test native::task_status_groups::tests::hand_typed_empty_group_heading_is_removed ... ok
test native::task_status_groups::tests::conservation_and_source_records ... ok
test native::task_status_groups::tests::excluded_markdown_contexts_are_not_task_roots_or_headings ... ok
test native::task_status_groups::tests::interior_content_in_groups_fails_closed ... ok
test native::task_status_groups::tests::badge_marker_in_intake_is_relocated_to_the_slot ... ok
test native::task_status_groups::tests::fresh_grouping_emits_no_comments ... ok
test native::task_status_groups::tests::empty_groups_vanish_and_return_in_fixed_order ... ok
test native::task_status_groups::tests::malformed_and_duplicate_markers_fail_closed ... ok
test native::task_status_groups::tests::lazy_continuation_skips_the_container ... ok
test native::task_status_groups::tests::crlf_mixed_endings_unicode_and_missing_final_newline ... ok
test native::task_status_groups::tests::legacy_marker_never_eats_following_prose ... ok
test native::task_status_groups::tests::legacy_marker_migrates_to_a_marker_free_row_in_the_slot ... ok
test native::task_status_groups::tests::legacy_comment_out_of_slot_fails_closed ... ok
test native::task_status_groups::tests::misplaced_badge_rows_fail_closed ... ok
test native::task_status_groups::tests::legacy_migration_drops_markers_and_empty_groups_lf_and_crlf ... ok
test native::task_status_groups::tests::ordered_list_roots_and_nested_ordinary_items_are_reported ... ok
test native::task_status_groups::tests::orphaned_badge_block_is_removed_without_creating_groups ... ok
test native::stats::compute::tests::compute_is_deterministic_and_leaves_vault_and_config_untouched ... ok
test native::task_status_groups::tests::out_of_scope_spans_are_byte_identical ... ok
test native::task_status_groups::tests::prose_lookalike_is_preserved_as_intake_prose ... ok
test native::task_status_groups::tests::nested_children_travel_with_parent_status ... ok
test native::task_status_groups::tests::nested_tasks_is_processed_once ... ok
test native::task_status_groups::tests::multiple_tasks_headings_and_heading_syntax_variants ... ok
test native::stats::homes::tests::worked_root_parent_conserves_totals_in_week_grouping ... ok
test native::task_status_groups::tests::marker_free_output_emits_row_directly_under_tasks ... ok
test native::task_status_groups::tests::reserved_group_heading_lines_reports_generated_groups ... ok
test native::task_status_groups::tests::skip_codes_are_stable ... ok
test native::task_status_groups::tests::reserved_group_heading_lines_skips_authored_and_outside_tasks ... ok
test native::task_status_groups::tests::un_decoration_returns_to_plain_layout_with_zero_counts ... ok
test native::task_status_groups::tests::renamed_heading_becomes_an_authored_topic ... ok
test native::task_status_groups::tests::unmarked_group_title_with_prose_is_a_collision ... ok
test native::task_status_groups::tests::standalone_prose_is_not_attached_to_a_task ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_drops_both_fields_for_r9 ... ok
test native::task_status_groups::tests::zero_chips_render_unlinked_while_open_stays_linked ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_lands_right_of_fresh_and_replaces_stale ... ok
test native::task_status_groups::tests::reserved_group_heading_lines_follows_lowercase_tasks_container ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_places_id_before_depends_on_before_block_id ... ok
test native::task_status_hooks::reconcile::fields::tests::dr_field_projection_vectors ... ok
test native::task_status_groups::tests::reopening_a_task_to_ready_appends_to_intake ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_field_before_trailing_tags ... ok
test native::task_status_groups::tests::reserved_group_heading_lines_ignores_fenced_and_frontmatter_titles ... ok
test native::task_status_groups::tests::reserved_group_heading_lines_includes_nested_group_under_authored_topic ... ok
test native::task_status_groups::tests::section_end_rule_preserves_trailing_whitespace ... ok
test native::task_status_groups::tests::tabs_internal_blanks_and_fences_stay_in_the_task_block ... ok
test native::task_status_groups::tests::unmarked_groups_emit_only_non_empty_groups_without_comments ... ok
test native::task_status_groups::tests::ready_only_and_empty_sections_are_not_decorated ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_removes_depends_on_when_empty ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_stamps_target_past_hide_tag ... ok
test native::task_status_hooks::retry::tests::allowed_transient_reasons_are_retried_without_applied_files ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_fields_between_tags ... ok
test native::task_status_hooks::retry::tests::any_error_listing_applied_files_is_never_retried ... ok
test native::task_status_hooks::retry::tests::partial_apply_is_never_retried_even_with_no_applied_files ... ok
test native::task_status_groups::tests::golden_layout_groups_every_status_bucket_and_keeps_ready_intake ... ok
test native::task_status_hooks::tests::structure::blocks_parser_does_not_claim_other_managed_child_lines ... ok
test native::task_status_hooks::tests::structure::blocks_lines_are_recognized_as_managed ... ok
test native::task_status_hooks::tests::blocks::malformed_dependents_are_uncertain_not_edges ... ok
test native::task_status_hooks::tests::structure::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::structure::both_managed_dependency_lines_are_not_pomodoro_task_links ... ok
test native::task_status_hooks::tests::structure::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::task_status_hooks::tests::structure::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::blocks::explicit_edges_include_idless_dependents ... ok
test native::task_status_hooks::tests::structure::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::structure::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_hooks::tests::structure::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::tests::structure::capture_consumption_keeps_link_only_notes_as_clean_task_text ... ok
test native::task_status_hooks::tests::structure::capture_only_removes_pomodoros_emptied_by_this_consumption ... ok
test native::task_status_hooks::tests::blocks::explicit_edges_exclude_implicit_resident_and_br18_br20 ... ok
test native::task_status_hooks::tests::structure::consumes_blocked_live_link_and_keeps_the_entry ... ok
test native::task_status_hooks::tests::structure::consuming_last_child_empties_the_pomodoro ... ok
test native::task_status_hooks::tests::structure::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_parenthesized_metadata ... ok
test native::task_status_hooks::retry::tests::retry_ceiling_progression_caps_at_thirty_seconds ... ok
test native::task_status_hooks::tests::structure::consumption_skips_closed_entries_and_struck_links ... ok
test native::task_status_hooks::tests::structure::consumption_removes_link_only_subtree_with_child_notes ... ok
test native::task_status_hooks::tests::structure::consumption_strips_the_token_from_a_prose_bullet ... ok
test native::task_status_hooks::retry::tests::retry_delay_stays_within_upper_half_of_ceiling ... ok
test native::task_status_hooks::tests::structure::dependency_line_forms_are_managed ... ok
test native::task_status_hooks::tests::structure::direct_child_scan_counts_plain_children_but_ignores_fences ... ok
test native::task_status_hooks::tests::structure::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::structure::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::structure::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::structure::empty_blocked_set_does_not_consume_question_status_links ... ok
test native::task_status_hooks::tests::structure::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::structure::empty_pomodoro_deletion_removes_full_blocks_and_preserves_crlf_eof ... ok
test native::task_status_hooks::retry::tests::retry_loop_stops_immediately_on_terminal_reason_without_noise ... ok
test native::task_status_hooks::tests::structure::empty_timed_entries_are_not_current_targets_or_ambiguity_inputs ... ok
test native::task_status_hooks::tests::structure::extracts_only_block_links_under_open_pomodoros ... ok
test native::task_status_hooks::tests::structure::entries_emptied_by_duplicate_cleanup_are_removed_in_same_pass ... ok
test native::task_status_hooks::tests::structure::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::retry::tests::terminal_and_unknown_reasons_are_never_retried ... ok
test native::task_status_hooks::tests::structure::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::structure::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::structure::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::structure::moving_last_child_removes_source_but_retains_destination ... ok
test native::highlights_ref::create::tests::link_catalog_records_uris_with_anchor_pages ... ok
test native::task_status_hooks::retry::tests::random_unit_interval_varies_and_stays_in_unit_range ... ok
test native::task_status_hooks::tests::structure::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::structure::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::task_status_hooks::tests::sync::archive_targets_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::structure::relation_lines_are_managed_link_lines_not_dependency_lines ... ok
test native::task_status_hooks::tests::sync::ambiguous_basename_does_not_resolve ... ok
test native::task_status_hooks::tests::structure::two_non_empty_timed_entries_still_match_the_ambiguity_guard ... ok
test native::task_status_hooks::tests::structure::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::structure::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::sync::blocked_project_marks_and_tags_residents ... ok
test native::task_status_hooks::retry::tests::retry_decision_log_includes_run_attempt_reason_and_recovery_directory ... ok
test native::task_status_hooks::retry::tests::retry_loop_with_zero_budget_makes_one_attempt_and_never_sleeps ... ok
test native::task_status_hooks::tests::sync::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::sync::child_links_are_not_dependency_edges ... ok
test native::task_status_hooks::tests::sync::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::task_status_hooks::retry::tests::retry_loop_clamps_sleep_to_remaining_budget ... ok
test native::task_status_hooks::tests::sync::reading_embeds_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::task_status_hooks::tests::sync::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::sync::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::tests::sync::dependency_line_links_are_promotion_edges ... ok
test native::task_status_hooks::tests::sync::desired_statuses_raise_a_directly_linked_prj ... ok
test native::task_status_hooks::tests::sync::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::sync::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::tests::sync::recovery_strips_tag_and_writes_unblocked ... ok
test native::task_status_hooks::tests::sync::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::sync::desired_statuses_walk_through_project_tasks_without_raising_them ... ok
test native::task_status_hooks::tests::sync::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::task_status_hooks::tests::sync::sticky_lanes_keep_next_and_in_progress_outside_daily_notes ... ok
test native::task_status_hooks::tests::sync::hand_blocked_prj_with_no_reasons_recovers ... ok
test native::task_status_hooks::tests::sync::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::sync::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::task_status_hooks::tests::sync::hand_copied_tag_outside_blocked_projects_is_stripped ... ok
test native::task_status_hooks::tests::sync::residents_inherit_prj_links_as_implicit_edges ... ok
test native::task_status_hooks::tests::sync::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::sync::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::tests::sync::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::task_status_hooks::tests::sync::parenthesized_repeat_skips_unblocked_write ... ok
test native::task_status_hooks::tests::sync::misplaced_existing_tag_is_not_counted_as_added ... ok
test native::task_status_hooks::tests::sync::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::sync::stale_unblocked_field_is_pruned_without_status_change ... ok
test native::task_status_hooks_write::tests::changed_tasks_settings_prevent_write ... ok
test native::task_status_hooks_write::tests::changed_previous_daily_prevents_write ... ok
test native::task_status_hooks_write::tests::symlink_substitution_prevents_write ... ok
test native::ref_library::tests::same_index_twice_serializes_identically ... ok
test native::task_status_hooks::tests::sync::prj_reports_only_own_reasons ... ok
test native::task_status_hooks::tests::sync::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test native::task_status_hooks::tests::sync::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
test native::task_status_hooks_write::tests::future_mtime_defers_without_sleeping ... ok
test native::task_status_hooks_write::tests::multiply_linked_output_is_rejected ... ok
test native::task_status_hooks_write::tests::noop_creates_no_recovery_or_staging ... ok
test native::task_status_hooks_write::tests::live_rescan_sees_new_vault_file ... ok
test native::task_status_hooks_write::tests::new_or_deleted_scan_candidate_invalidates_plan ... ok
test native::task_status_hooks_write::tests::equal_length_change_with_restored_mtime_prevents_write ... ok
test native::task_status_hooks_write::tests::quiet_period_waits_once_then_defers_if_changed ... ok
test native::task_status_hooks_write::tests::replacement_inode_prevents_write ... ok
test native::task_status_hooks_write::tests::deletion_prevents_write ... ok
test native::highlights_ref::create::tests::tall_diagram_opt_out_shares_page_without_pills ... ok
test native::url_routing::policy::tests::defaults_cover_the_plan_list ... ok
test native::url_routing::policy::tests::normalization_strips_scheme_www_and_dot ... ok
test native::url_routing::policy::tests::invalid_yaml_is_an_error ... ok
test native::url_routing::policy::tests::subdomain_matching ... ok
test native::url_routing::policy::tests::toggles_gate_entries_independently ... ok
test native::url_routing::policy::tests::overrides_and_empty_list ... ok
test native::url_routing::tests::phase_api_hangs_together ... ok
test native::url_routing::intent::tests::display_elides_long_urls ... ok
test native::url_routing::intent::tests::display_keeps_explicit_non_default_ports ... ok
test native::url_routing::intent::tests::classifier_table ... ok
test native::url_routing::intent::tests::url_list_lines_are_lexical ... ok
test native::task_status_hooks::retry::tests::retry_loop_retries_lock_contention_then_succeeds ... ok
test native::vault_clobber::tests::added_and_deleted_status_codes_are_not_candidates ... ok
test native::url_routing::policy::tests::empty_list_excludes_nothing ... ok
test native::vault_clobber::tests::a_single_duplicated_task_is_not_foreign ... ok
test native::vault_clobber::tests::excluded_paths_skip_conflicts_done_daily_and_dot_dirs ... ok
test native::vault_clobber::tests::deleting_most_of_a_note_is_not_foreign ... ok
test native::vault_clobber::tests::grep_needles_cover_created_prj_and_new_ids ... ok
test native::url_routing::verdict::tests::missing_ref_dir_counts_as_empty ... ok
test native::vault_links::tests::basename_walk_skips_hidden_directories ... ok
test native::vault_clobber::tests::incident_shaped_copy_matches_foreign_identity ... ok
test native::vault_links::tests::exact_root_note_does_not_build_the_vault_index ... ok
test native::vault_clobber::tests::notes_under_five_distinct_lines_are_not_displaced ... ok
test native::vault_clobber::tests::task_move_style_transfer_is_not_foreign ... ok
test native::vault_sync::tests::clobber_notifications_follow_env_override ... ok
test native::vault_links::tests::with_additional_unions_staged_notes_without_rebuilding ... ok
test native::task_status_hooks::retry::tests::retry_loop_never_starts_another_attempt_once_budget_is_exhausted ... ok
test native::vault_sync::tests::legacy_status_record_defaults_new_fields ... ok
test native::vault_links::tests::resolves_exact_path_before_unique_case_insensitive_basename ... ok
test native::vault_sync::tests::lock_contention_detection_matches_ref_and_index_locks ... ok
test native::vault_sync::tests::vault_identity_accepts_symlink_aliases ... ok
test native::stats::compute::tests::archive_move_does_not_change_task_metric_values ... ok
test runner::tests::epipe_classifier_rejects_non_epipe_panics ... ok
test runner::tests::every_native_command_is_on_exactly_one_canonical_path ... ok
test print_fonts::tests::web_clip_reader_skips_display_and_emoji ... ok
test print_fonts::tests::web_clip_reader_reuses_print_font_bytes ... ok
test print_fonts::tests::web_clip_reader_omits_variable_woff2 ... ok
test runner::tests::alias_rewrite_preserves_separator_and_non_utf8_tail ... ok
test runner::tests::aliases_resolve_to_leaves_and_do_not_collide_with_root_names ... ok
test runner::tests::subcommands_are_contiguous_in_section_order_and_alphabetical ... ok
test runner::tests::build_cli_renders_without_panicking ... ok
test native::vault_rewrite::tests::not_a_worktree_refuses ... ok
test runner::tests::epipe_classifier_accepts_stdout_and_stderr_broken_pipes ... ok
test native::vault_sync::tests::vault_identity_checks_default_fallback_and_missing_paths ... ok
test native::url_routing::verdict::tests::verdicts_cover_every_library_state ... ok
test runner::tests::guard_thread_panic_prints_and_exits_zero ... ok
test runner::tests::guard_unrelated_panic_prints_once ... ok
test runner::tests::guard_epipe_panic_exits_zero_quietly ... ok
test native::stats::homes::tests::root_flag_regroups_blog_minutes_under_its_own_root ... ok
test native::stats::compute::tests::recorded_durations_add_up_to_the_reported_total ... ok
test native::stats::compute::tests::report_serializes_as_schema_one_with_optional_fields ... ok
test native::vault_rewrite::tests::stale_note_aborts_before_writing ... ok
test native::vault_rewrite::tests::offline_dirty_paths_refuse ... ok
test native::vault_rewrite::tests::verify_failure_restores_before_images ... ok
test native::stats::homes::tests::review_bucket_carries_short_label_for_compact_views ... ok
test native::vault_rewrite::tests::online_presync_failure_maps_to_sync_failed ... ok
test native::vault_rewrite::tests::offline_run_writes_files_and_makes_one_commit ... ok
test native::highlights_ref::note_snapshot::profile::tests::diagrams_filter_runs_first_on_snapshot_route ... ok
test native::task_status_hooks_write::tests::edit_between_staging_and_revalidate_survives ... ok
test native::task_move::command::tests::staging_failure_writes_no_notes_and_keeps_recovery ... ok
test native::stats::homes::tests::h_vectors_cover_parts_buckets_apportioned_and_theme_filter ... ok
test native::task_status_hooks_write::tests::staging_failure_preserves_notes_and_foreign_temps ... ok
test native::highlights_ref::create::tests::tall_anchored_figure_div_shares_page_and_keeps_destinations ... ok
test native::task_status_hooks_write::tests::fresh_attempt_after_vault_changed_replans_from_intervening_edit ... ok
test native::task_status_hooks_write::tests::exclusive_temp_and_mode_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::retention_keeps_incomplete_and_prunes_old_completed ... ok
test native::task_status_hooks_write::tests::tool_scopes_recovery_root_manifest_and_pruning ... ok
test native::completion::present::tests::structural_latency_is_warn_only ... ok
test native::vault_rewrite::tests::online_postsync_failure_reports_sync_pending ... ok
test native::highlights_ref::create::tests::tall_diagram_shares_page_with_heading_and_stays_in_margin ... ok
test native::task_status_hooks_write::tests::edit_before_later_replacement_reports_partial ... ok
test native::task_move::command::tests::failure_after_destination_leaves_later_files_deferred ... ok
test native::capture_related::tests::synthetic_vault_draft_contract_is_under_250ms ... ok
test native::task_status_hooks_write::tests::unchanged_read_set_applies_and_records_recovery_bytes ... ok
test native::task_move::command::tests::partial_write_leaves_source_when_its_last_replacement_is_interrupted ... ok
test native::task_move::command::tests::retryable_scan_is_retried_until_a_fresh_snapshot_succeeds ... ok
test native::test_stub::tests::executable_stubs_stay_executable_while_other_threads_fork ... ok
test native::task_status_hooks_write::tests::quiet_period_skips_wait_for_stable_files_and_status_only ... ok
test native::task_move::command::tests::secondary_commit_failure_after_partial_apply_is_a_warning ... ok
test native::task_move::command::tests::ordinary_commit_failure_skips_post_sync_and_keeps_the_write ... ok
test native::task_move::command::tests::changed_read_set_and_new_markdown_backlink_trigger_fresh_replan ... ok
test native::highlights_ref::create::tests::diagrams_swap_pdf_error_keeps_note_and_source ... ok
test native::highlights_ref::create::tests::code_catalog_preserves_source_and_maps_rendered_pages ... ok
test native::highlights_ref::overwrite::execute::tests::failpoints_that_abort_before_commit_restore_the_old_state ... ok
test native::highlights_ref::create::tests::return_link_xelatex_render_pairs_pills_with_destinations ... ok
test native::highlights_ref::overwrite::execute::tests::annotated_failpoint_sweep_restores_bundle_links_and_clears_intent ... ok
test native::vault_rewrite::tests::lock_busy_when_maintenance_lock_held ... ok
test native::highlights_ref::create::tests::diagrams_absent_results_match_unhooked_pdf ... ok
test native::highlights_ref::note_snapshot::assets::tests::png_and_jpeg_are_preserved_and_oversized_images_are_downscaled ... ok
test native::highlights_ref::note_snapshot::profile::tests::diagrams_swap_snapshot_centers_image_and_drops_source ... ok
test native::highlights_ref::note_snapshot::profile::tests::tall_snapshot_diagram_shares_page_with_heading_without_vbox_overflow ... ok
test native::highlights_ref::note_snapshot::profile::tests::diagrams_swap_snapshot_error_keeps_note_and_source ... ok
test native::highlights_ref::note_snapshot::profile::tests::navigation_shows_page_numbers_only_above_eight_pages ... ok
test native::highlights_ref::note_snapshot::profile::tests::renders_contract_with_clean_text_layer_and_metadata ... ok

test result: ok. 3818 passed; 0 failed; 1 ignored; 0 measured; 0 filtered out; finished in 24.51s

     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/bob-39abebeb4ad07360)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/bob_notify-f1a59fb8e3d29c43)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/bob_pomodoro-a1880c6eed04140e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/tmux_bob_pomodoro-5d65a532f2abf4a7)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/cli-862b59fffc4caf66)

running 2331 tests
test articles::article_help_exposes_the_cli_contract ... ok
test articles::adopt_help_lists_options_alphabetically ... ok
test articles::adopt_stdin_json_returns_plan_without_writing ... ok
test articles::dry_run_shows_inbound_diffs_without_writing ... ok
test articles::format_rewrites_inbound_links_in_two_other_notes ... ok
test articles::all_formats_every_article_and_skips_untyped_notes ... ok
test articles::all_writes_good_articles_when_another_article_is_refused ... ok
test articles::format_reports_unrepairable_inbound_and_resolves_duplicate_titles ... ok
test articles::adopt_write_inserts_type_and_adopting_twice_is_a_noop ... ok
test articles::adopt_note_completion_is_a_vault_note ... ok
test capture::batch::capture_batch_duplicate_block_id_failure_leaves_no_partial_write ... ok
test articles::article_note_completion_shows_section_count ... ok
test articles::check_and_dry_run_report_changes_without_writing ... ok
test capture::authored::capture_authored_bullets_accept_dash_star_and_plus_markers ... ok
test capture::batch::capture_global_destination_can_be_declared_at_the_end_of_any_item ... ok
test capture::batch::capture_batch_json_is_ordered_and_keeps_legacy_top_level ... ok
test articles::bare_articles_lists_only_marked_notes_and_honors_exclusions ... ok
test aliases::randomize_alias_matches_canonical_dry_run_seed ... ok
test capture::bare::capture_bare_terminal_marker_multiple_open_timed_pomodoros_is_io_error ... ok
test articles::adopt_previews_without_writing_and_reports_replaced_numbers ... ok
test aliases::notify_alias_matches_canonical_help_and_bad_arity ... ok
test capture::batch::capture_global_destination_conflict_and_declaration_only_are_usage_errors ... ok
test capture::blocked_tasks::forced_target_rejections_name_the_typed_sigil ... ok
test capture::authored::capture_authored_bullets_sub_bullet_nests_children_two_levels ... ok
test aliases::group_help_matches_snapshots_within_80_columns ... ok
test capture::authored::capture_authored_bullets_duplicate_route_marker_across_lines_is_usage_error ... ok
test capture::batch::capture_global_batch_failure_leaves_every_fixture_unchanged ... ok
test capture::authored::capture_authored_bullets_duplicate_schedule_marker_across_lines_is_usage_error ... ok
test articles::format_writes_atomically_and_check_is_idempotent ... ok
test capture::batch::capture_batch_human_output_numbers_items ... ok
test capture::batch::capture_global_destination_human_and_stdin_and_dry_run ... ok
test aliases::tmux_pomodoro_alias_matches_canonical_on_fixture ... ok
test capture::authored::capture_authored_bullets_reject_item_emptied_by_markers ... ok
test articles::stdin_json_fills_inbound_entries_without_writing ... ok
test articles::list_json_keeps_report_fields_but_omits_edits ... ok
test capture::authored::capture_authored_nested_bullets_render_under_their_owners ... ok
test capture::blocked_tasks::ampersand_same_note_prerequisite_below_dependent_relocates ... ok
test capture::authored::capture_authored_bullets_dry_run_reports_children_without_writing ... ok
test capture::bare::capture_bare_terminal_marker_selects_the_last_of_two_completed_pomodoros ... ok
test capture::batch::capture_batch_dry_run_reports_all_items_without_writing ... ok
test articles::named_non_article_reports_refusal_in_json ... ok
test articles::format_rewrites_inbound_embeds ... ok
test capture::authored::capture_authored_bullets_reject_orphaned_nested_lines ... ok
test articles::stdin_json_returns_plan_without_writing ... ok
test capture::batch::capture_global_destination_on_authored_child_line_applies_draft_wide ... ok
test capture::blocked_tasks::fenced_example_does_not_hide_real_task ... ok
test capture::bare::capture_bare_terminal_marker_dry_run_reports_plan_and_writes_nothing ... ok
test articles::adopt_refuses_other_types_and_tasks ... ok
test articles::non_utf8_markdown_does_not_break_list_or_format_all ... ok
test articles::outline_json_and_human_show_numbering_and_stubs ... ok
test capture::authored::capture_authored_bullets_skip_placeholder_lines ... ok
test capture::authored::capture_authored_bullets_preserve_crlf_line_endings ... ok
test capture::batch::capture_global_sub_bullet_inserts_ordered_siblings_and_keeps_authored_children ... ok
test capture::bare::capture_bare_terminal_marker_writes_pomodoro_note_under_current_pomodoro ... ok
test capture::authored::capture_authored_bullet_marker_on_child_line_configures_whole_capture ... ok
test capture::blocks::capture_blocks_dry_run_reports_without_writing ... ok
test capture::authored::capture_bare_terminal_marker_authored_children_nest_one_level_deeper ... ok
test capture::batch::capture_global_destination_routes_unmarked_items_and_keeps_overrides ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_land_under_the_same_pomodoro_in_order ... ok
test capture::authored::capture_authored_bullets_reject_indented_or_nonbullet_lines ... ok
test articles::unresolved_notes_show_nearby_and_ambiguous_candidates ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_stack_under_the_same_completed_pomodoro ... ok
test aliases::completion_offers_group_members_status_flags_and_alias_options ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_last_completed_pomodoro ... ok
test aliases::capture_grammar_does_not_swallow_group_words ... ok
test capture::authored::capture_authored_bullets_use_two_space_target_indentation ... ok
test capture::bare::capture_bare_terminal_marker_human_output_shows_the_ledger_entry ... ok
test capture::authored::capture_authored_bullets_preserve_inline_markdown_and_checkbox_text ... ok
test capture::bare::capture_bare_terminal_marker_preflight_failures_leave_daily_note_untouched ... ok
test capture::clip::capture_history_without_a_provider_has_actionable_guidance ... ok
test capture::clip::capture_history_dry_run_plans_colliding_files_without_writes ... ok
test capture::clip::capture_flat_clipboard_list_routes_normalized_children ... ok
test capture::clip::capture_clip_json_always_emits_collection_fields ... ok
test capture::complete_block_id::block_id_missing_note_is_not_an_error ... ok
test capture::complete_block_id::block_id_suggestions_follow_body_examples ... ok
test capture::blocked_tasks::close_with_ampersand_emits_dependency_updates_array ... ok
test capture::complete_block_id::block_id_link_candidates_are_filtered_and_annotated ... ok
test capture::clip::capture_clip_failures_leave_vault_untouched ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_first_future_pomodoro ... ok
test capture::clip::capture_percent_one_is_an_exact_single_clip_alias ... ok
test capture::bare::capture_bare_terminal_marker_keeps_crlf_line_endings ... ok
test capture::authored::capture_authored_bullets_bullet_capture_uses_section_prefix_with_children ... ok
test capture::complete_blocked_task::missing_day_file_is_empty_ledger_without_warning ... ok
test capture::clip::capture_bare_terminal_marker_clipboard_marker_writes_children_beneath_note ... ok
test capture::complete_block_id::block_id_used_covers_done_nontask_duplicates_and_order ... ok
test capture::blocked_tasks::st9_prj_internal_refuse ... ok
test capture::complete_blocked_task::task_id_assignment_returns_star_replacement_with_quoted_locator ... ok
test capture::complete_dependency::empty_query_orders_lanes_before_history_and_hides_last ... ok
test capture::complete_dependency::note_path_assigns_nested_case_sensitive_notes ... ok
test capture::complete_blocked_task::existing_owner_reports_self_existing_edges_and_typed_blocked_rows ... ok
test capture::complete_dependency::note_path_preserves_quoting_and_case_in_the_replacement ... ok
test capture::complete_editor::capture_complete_cursor_in_body_text_is_an_empty_success ... ok
test capture::complete_block_id::block_id_json_shape_and_human_line ... ok
test capture::complete_dependency::existing_owner_marks_self_and_already_added_rows ... ok
test capture::complete_editor::capture_complete_bare_hash_marker_is_an_empty_success ... ok
test capture::complete_editor::capture_complete_discovery_failure_reports_an_actionable_error ... ok
test capture::authored::capture_authored_bullets_pomodoro_linked_capture_includes_children ... ok
test capture::authored::capture_authored_bullets_render_task_with_children_in_order ... ok
test capture::complete_block_id::block_id_incomplete_close_list_still_links ... ok
test capture::blocks::capture_new_task_with_explicit_id_stages_blocks_row ... ok
test capture::blocked_tasks::st10_cycles_refuse ... ok
test capture::blocks::capture_blocks_kill_switch_writes_nothing ... ok
test capture::complete_dependency::rows_carry_exact_identities_and_id_flow_metadata ... ok
test capture::blocks::capture_new_task_without_id_mints_dependent_block_id ... ok
test capture::complete_editor::capture_complete_empty_text_defaults_to_an_empty_draft ... ok
test capture::blocked_tasks::human_dry_run_residents_and_kept_notes ... ok
test capture::complete_dependency::closed_tasks_need_the_opt_in_and_stay_closed ... ok
test capture::complete_editor::capture_complete_never_creates_the_vault_directory ... ok
test capture::complete_editor::capture_complete_missing_note_behind_a_resolved_route_is_an_empty_success ... ok
test capture::complete_editor::capture_complete_human_output_is_plain_and_concise ... ok
test capture::complete_dependency::protected_spans_never_open_the_dependency_picker ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_outside_the_text ... ok
test aliases::group_routing_and_help ... ok
test capture::complete_blocked_task::disabled_rows_explain_duplicate_ids_cycles_and_internal_projects ... ok
test capture::clip::capture_sub_bullet_task_ref_recovers_shift_and_nests_clipboard ... ok
test capture::complete_dependency::previous_daily_snapshot_is_read_only ... ok
test capture::complete_editor::capture_complete_reports_utf8_byte_offsets ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_human_labels_rows ... ok
test capture::blocks::capture_dependency_only_add_stages_blocks_row ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_that_splits_a_multibyte_character ... ok
test capture::complete_block_id::project_task_block_id_reports_stem_body_used_and_suggestions ... ok
test capture::blocked_tasks::st15_kill_switch_still_mints ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_lists_named_and_nameable_rows ... ok
test capture::complete_editor::capture_complete_wikilink_same_note_heading_uses_capture_route ... ok
test capture::complete_dependency::refetch_at_replacement_start_returns_the_full_snapshot ... ok
test capture::complete_editor::capture_complete_wikilink_note_json_returns_replacement_and_cursor_after ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_child_line ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_nested_child_line ... ok
test capture::complete_query::capture_complete_all_tasks_works_on_a_global_sub_bullet_declaration ... ok
test capture::blocked_tasks::st1_new_blocker_ready_unlinked ... ok
test capture::complete_query::capture_complete_inherited_route_is_the_same_note_for_wikilinks ... ok
test capture::blocked_tasks::same_note_task_blocks_relocate_by_block_id ... ok
test capture::complete_blocked_task::partial_star_fields_rank_today_running_then_lanes_and_owner_note ... ok
test capture::complete_query::capture_complete_section_json_lists_headings_of_the_resolved_route ... ok
test capture::complete_dependency::traversal_and_ambiguous_paths_fail_without_writing ... ok
test capture::complete_query::capture_complete_route_json_ranks_prefix_before_substring ... ok
test capture::complete_query::capture_complete_section_json_skips_generated_status_groups ... ok
test capture::complete_relationship_owner::capture_complete_help_documents_additive_owner_fields ... ok
test capture::complete_editor::capture_complete_pomodoro_close_protocol ... ok
test capture::complete_query::capture_complete_all_tasks_uses_global_ranges_in_later_batch_item ... ok
test capture::blocked_tasks::st11_a8_refusals ... ok
test capture::complete_query::capture_complete_task_json_only_offers_tasks_with_a_block_id ... ok
test capture::complete_dependency::query_ranks_matches_and_keeps_history_findable ... ok
test capture::complete_ref_kind::ref_kind_appears_on_hat_picker ... ok
test capture::authored::capture_task_section_authored_children_and_composition ... ok
test capture::complete_relationship_owner::caret_star_picker_disables_the_owner_task_itself ... ok
test aliases::pomodoro_status_forms_match_with_and_without_show_stale ... ok
test capture::complete_task_complete::complete_padded_line_offers_no_picker ... ok
test capture::complete_query::capture_complete_scopes_to_later_batch_item_and_ignores_separator ... ok
test capture::complete_task_complete::complete_id_less_and_recurring_rows_carry_guards ... ok
test capture::complete_query::capture_complete_task_block_id_marker_completes_only_route_side ... ok
test capture::complete_task_complete::complete_bare_bang_lists_today_first_with_picker ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_json_covers_empty_and_new_queries ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_skips_create_when_ledger_cannot_place_it ... ok
test capture::complete_query::capture_complete_all_tasks_is_opt_in_and_plus_context_only ... ok
test capture::clip::capture_history_provider_failures_leave_the_vault_untouched ... ok
test capture::blocked_tasks::st3_delete_empty_running_entry ... ok
test capture::complete_ref_kind::ref_kind_appears_on_amp_and_bang_pickers ... ok
test capture::complete_task_complete::complete_second_item_marks_already_selected ... ok
test capture::complete_query::capture_complete_global_declaration_replaces_only_the_active_component ... ok
test capture::complete_ref_kind::ref_kind_appears_on_colon_and_plus_pickers ... ok
test capture::blocked_tasks::st6_link_then_consume ... ok
test capture::blocked_tasks::st14_insert_between ... ok
test capture::blocked_tasks::st4_notes_kept ... ok
test capture::blocked_tasks::st16_later_link_drops_n ... ok
test capture::blocks::capture_dependency_drop_removes_blocks_entry ... ok
test capture::complete_task_complete::complete_partial_query_decodes_and_drops_continuation_keys ... ok
test capture::blocked_tasks::st7_unrelated_placeholder_untouched ... ok
test capture::complete_editor::capture_complete_pomodoro_ranges_preserve_start_suffix ... ok
test capture::blocked_tasks::st8_prj_blocks_residents ... ok
test capture::complete_task_complete::shell_completion_serves_identified_enabled_bang_rows ... ok
test capture::flag_guard::capture_complete_unknown_long_flag_is_rejected_with_json ... ok
test capture::complete_task_link::complete_parent_task_plus_serves_json_and_human_candidates ... ok
test capture::blocked_tasks::st2_consume_link_keep_session ... ok
test capture::complete_relationship_owner::owner_metadata_resolves_existing_alias_and_new_task_text ... ok
test capture::complete_relationship_owner::scoped_parent_picker_applies_the_same_relationship_guards ... ok
test capture::complete_themes::theme_recent_shell_description_and_quoted_replacement ... ok
test capture::clip::capture_headerless_clip_marker_renders_under_tasks_and_pomodoros ... ok
test capture::complete_task_link::complete_task_link_lists_the_worked_example_in_json_and_human ... ok
test capture::complete_task_complete::capture_task_id_reports_complete_replacement_in_both_modes ... ok
test capture::flag_guard::capture_templates_save_guard_json_carries_a_stable_code ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_an_identified_task ... ok
test capture::blocked_tasks::st5_nested_identity ... ok
test capture::blocked_tasks::st12_already_present_noop ... ok
test capture::flag_guard::capture_parse_unknown_long_flag_is_rejected_with_json ... ok
test capture::flag_guard::capture_templates_save_unknown_flag_leaves_the_shelf_unchanged ... ok
test capture::flag_guard::capture_rewrite_unknown_long_flag_is_rejected_with_json ... ok
test capture::flag_guard::capture_unknown_long_flag_human_error_writes_nothing ... ok
test capture::flag_guard::capture_mixed_short_cluster_unknown_long_is_rejected_with_json ... ok
test capture::flag_guard::capture_unknown_long_flag_is_rejected_with_json_and_writes_nothing ... ok
test capture::inbox_route::inbox_route_choice_guard_stays_hidden_from_help ... ok
test capture::complete_editor::capture_complete_task_section_json_covers_components_and_warnings ... ok
test capture::complete_themes::configured_shell_describes_never_used_and_unconfigured_create ... ok
test capture::inbox_route::ir_conflicting_duplicate_answers_are_usage_errors ... ok
test capture::freshness_stamps::capture_new_tasks_carry_no_fresh ... ok
test capture::complete_relationship_owner::project_cannot_depend_on_its_resident_and_unmodified_shape_is_frozen ... ok
test capture::inbox_route::ir_gkeep_inbox_child_is_classified_from_its_live_parent ... ok
test capture::inbox_route::ir_stale_route_key_lists_current_candidates ... ok
test capture::complete_editor::capture_complete_pomodoro_start_drop_protocol ... ok
test capture::inbox_route::ir_pull_in_choice_refusal_precedes_inbox_route_choice_refusal ... ok
test capture::complete_parent_task::plus_picker_fixture_vault_catalog_and_entry_points ... ok
test capture::complete_editor::capture_complete_pomodoro_close_selection_protocol ... ok
test capture::clip::capture_clip_uses_each_target_notes_indent_and_tabs_for_a_fresh_note ... ok
test capture::inbox_route::ir_pull_in_and_route_answers_combine_in_one_batch ... ok
test capture::complete_themes::accepting_hidden_theme_keeps_preferences_and_today_row ... ok
test capture::complete_block_id::block_id_link_new_and_project_note_intents ... ok
test capture::clip::capture_history_is_headerless_structured_and_composes_with_routes ... ok
test capture::complete_relationship_owner::parent_picker_reports_resolved_relationships_and_guards_rows ... ok
test capture::open_notes::open_notes_human_output_is_unchanged ... ok
test capture::inbox_route::ir_route_refusals_name_the_destination_and_the_rule ... ok
test capture::ensure_next::capture_ensure_next_on_project_blocked_resident_refuses_drop ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_keeps_in_progress ... ok
test capture::open_notes::open_notes_library_hit_has_no_line ... ok
test capture::blocked_tasks::st13_multiple_and_duplicate ... ok
test capture::clip::capture_clip_marker_composes_with_schedule_routes_bullets_and_pomodoro ... ok
test capture::link_guard::capture_toggle_on_tagged_child_prj_promotes_ancestor ... ok
test capture::link_guard::capture_pomodoro_link_on_tagged_child_is_not_linked ... ok
test capture::link_guard::capture_toggle_on_tagged_child_resident_promotes_ancestor ... ok
test capture::complete_task_link::parent_picker_acceptance_round_trips_and_id_assignment_returns_replacement ... ok
test capture::flag_guard::capture_delimiter_literal_and_trailing_flag_word_still_capture ... ok
test capture::link_guard::own_dependency_drop_is_refused_for_a_project_task ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_offers_a_create_row ... ok
test capture::clip::capture_clip_saves_attachments_snippets_and_reports_dry_run ... ok
test capture::complete_editor::capture_complete_override_name_json_carries_keeps_ledger_and_running ... ok
test capture::open_notes::open_notes_new_inbox_task ... ok
test capture::open_notes::open_notes_link_guard_lands_on_the_blocked_child ... ok
test capture::freshness_stamps::capture_link_never_stamps_recurring_tasks ... ok
test capture::complete_task_link::complete_task_link_pull_forward_agrees_with_the_scheduled_retire ... ok
test capture::ensure_next::capture_ensure_next_drops_own_dependency_and_relocates ... ok
test capture::parse::capture_parse_human_output_is_plain_and_concise ... ok
test capture::open_notes::open_notes_routed_task ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_a_task_without_an_id ... ok
test capture::freshness_stamps::capture_link_clears_keep_streak ... ok
test capture::complete_task_link::complete_task_link_batch_accepts_two_queries ... ok
test capture::freshness_stamps::capture_link_stamps_next_when_it_retires_future_schedule ... ok
test capture::parse::capture_parse_json_output_is_stable_and_parseable ... ok
test capture::parse::capture_parse_json_reports_batch_items_with_global_ranges ... ok
test capture::link_guard::capture_new_task_into_tagged_project_is_unlinked ... ok
test capture::parse::capture_parse_json_reports_wikilink_semantic_spans ... ok
test capture::open_notes::open_notes_pomodoro_adjust ... ok
test capture::parse::capture_parse_json_reports_retired_double_colon_as_migration_guidance ... ok
test capture::freshness_stamps::capture_link_leaves_next_untouched_without_future_schedule ... ok
test capture::parse::capture_parse_json_reports_pomodoro_note_mode_and_span ... ok
test capture::parse::capture_parse_named_pomodoro_reports_incomplete_need ... ok
test capture::parse::capture_parse_human_reports_start_suffix ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_moves_link_and_sets_next ... ok
test capture::parse::capture_parse_missing_text_is_a_usage_error ... ok
test capture::open_notes::open_notes_queued_link_is_empty ... ok
test capture::link_guard::pomodoro_link_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::open_notes::open_notes_pomodoro_start ... ok
test capture::inbox_route::ir_completed_task_routes_home_without_stamp ... ok
test capture::link_guard::link_toggle_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::link_guard::close_link_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::parse::capture_parse_reports_diagnostics_without_failing ... ok
test capture::open_notes::open_notes_pomodoro_reset ... ok
test capture::link_guard::ensure_next_pulls_forward_a_scheduled_resident_of_an_unblocked_project ... ok
test capture::open_notes::open_notes_pomodoro_shift ... ok
test capture::parse::capture_parse_reports_global_destination_metadata ... ok
test capture::parse::capture_parse_reports_orphaned_nested_bullet_diagnostic ... ok
test capture::parse::capture_parse_reads_one_stdin_line_when_text_is_omitted ... ok
test capture::parse::capture_parse_reports_duplicate_global_destination_diagnostics ... ok
test capture::parse::capture_parse_reports_nested_sub_bullets_and_depths ... ok
test capture::parse::capture_parse_json_reports_task_block_id_marker_spans_and_needs ... ok
test aliases::move_done_tasks_alias_matches_canonical_on_git_fixture ... ok
test capture::parse::capture_parse_json_reports_explicit_toggle_span_and_plain_ensure_next ... ok
test capture::parse::capture_parse_reports_utf8_byte_offsets ... ok
test capture::parse::capture_parse_reports_sub_bullets_for_a_multiline_draft ... ok
test capture::open_notes::open_notes_sub_bullet_lands_on_the_added_child_under_the_block ... ok
test capture::open_notes::open_notes_sub_bullet ... ok
test capture::open_notes::open_notes_section_bullet ... ok
test capture::parse_blocked_task::bang_keeps_precedence_over_star ... ok
test capture::parse_blocked_task::body_bearing_close_with_star_fails_capture ... ok
test capture::parse_blocked_task::blocked_task_parses_separately_with_directional_spans ... ok
test capture::freshness_stamps::capture_link_stamping_is_idempotent_same_day ... ok
test capture::open_notes::open_notes_project_note_with_task_links ... ok
test capture::inbox_route::ir_dependency_touch_follows_its_routed_task ... ok
test capture::blocked_tasks::st17_two_item_equivalent ... ok
test capture::clip::capture_clip_options_force_or_disable_marker_parsing ... ok
test capture::inbox_route::ir_preview_report_matches_write_and_hidden_guard_refuses_write_free ... ok
test capture::parse_blocked_task::blocked_task_note_star_is_invalid ... ok
test capture::parse_dependency::capture_prj_dependency_refuses_descendant_targets ... ok
test capture::parse_dependency::child_line_dependency_belongs_to_the_item ... ok
test capture::parse_dependency::capture_prj_dependency_refuses_same_note_targets ... ok
test capture::parse_dependency::complete_reports_task_dependency_field ... ok
test capture::parse::capture_parse_never_touches_the_vault_or_clipboard ... ok
test capture::parse_dependency::capture_prj_dependency_sees_implicit_resident_cycles ... ok
test capture::parse::capture_parse_json_reports_project_task_ids_spans_and_mode ... ok
test capture::parse_dependency::dependency_new_task_reports_modifiers_and_target ... ok
test capture::open_notes::open_notes_pomodoro_link_lands_on_the_resident ... ok
test capture::open_notes::open_notes_ensure_next_toggle_opens_task_and_day ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_same_note_batch_and_rollback ... ok
test capture::parse_dependency::escaped_ampersand_leaves_visible_token ... ok
test capture::parse_dependency::dependency_only_colon_alias_reports_existing_target ... ok
test capture::parse_dependency::block_id_intent_follows_dependency_ownership ... ok
test capture::parse_dependency::leading_dependency_run_skips_a_destination_marker ... ok
test capture::parse_dependency::dependency_only_plus_target_reports_task_dependency ... ok
test capture::parse_dependency::ownerless_dependency_needs_its_target ... ok
test capture::parse_dependency::caret_alias_reports_existing_task_owner ... ok
test capture::open_notes::open_notes_template_draft ... ok
test capture::link_guard::own_dependency_drop_is_refused_for_a_project_blocked_resident ... ok
test capture::parse::capture_parse_and_capture_report_shadowed_global_destination_warnings ... ok
test capture::parse::capture_parse_json_reports_project_note_markers ... ok
test capture::parse_dependency::dependency_only_suffixed_colon_target_is_rejected ... ok
test capture::parse_dependency::section_bullet_with_dependency_is_rejected ... ok
test capture::parse_dependency::quoted_note_reports_decoded_identity_and_offsets ... ok
test capture::parse_dependency::rewrite_never_absorbs_ampersands_or_the_colon_alias ... ok
test capture::parse_dependency::inherited_parent_selects_the_existing_dependent ... ok
test capture::inbox_route::ir_block_id_collision_renames_on_route ... ok
test capture::parse_dependency::capture_keeps_literal_ampersand_prose ... ok
test capture::parse_dependency::suffixed_plus_owner_keeps_must_be_bare ... ok
test capture::parse_dependency::malformed_modifiers_report_invalid_dependency ... ok
test capture::inbox_route::ir_idless_recovered_dependent_moves_by_line ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_chain_items ... ok
test capture::open_notes::open_notes_task_complete_with_ledger ... ok
test capture::parse_dependency::relationship_only_owner_reports_needs_text ... ok
test capture::parse_relation::relation_after_close_is_refused ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_human_line ... ok
test capture::open_notes::open_notes_three_items_dedupe_and_keep_first_landing ... ok
test capture::parse_relation::relation_clock_lookalike_needs_relation_target ... ok
test capture::parse_dependency::dependency_markers_interleave_with_destination_in_either_order ... ok
test capture::parse::capture_parse_json_reports_sub_bullet_section_and_incomplete_needs ... ok
test capture::freshness_stamps::capture_link_stamps_ready_and_blocked_to_next ... ok
test capture::parse_dependency::plus_selector_beside_modifiers_needs_task_parent ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_incomplete_needs_task ... ok
test capture::parse_relation::relation_escape_leaves_visible_tilde ... ok
test capture::complete_parent_task::plus_picker_accepts_insert_and_preserves_operators ... ok
test capture::open_notes::open_notes_pomodoro_close_opens_only_the_day_file ... ok
test capture::parse_relation::relation_grammar_absent_without_tilde ... ok
test capture::inbox_route::ir_two_candidates_move_to_two_destinations_in_one_bulk ... ok
test capture::blocked_tasks::human_star_line_and_consumption ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_valid_spec_and_spans ... ok
test capture::parse_relation::relation_invalid_label_is_refused ... ok
test capture::parse_relation::relation_mid_line_stays_prose ... ok
test aliases::every_alias_matches_canonical_help_and_invalid_option ... ok
test capture::parse_relation::relation_code_and_wikilinks_stay_literal ... ok
test capture::parse_blocked_task::both_directions_keep_independent_lists_and_blocked_task_order ... ok
test capture::parse_relation::relation_only_existing_owner_reports_task_dependency ... ok
test capture::parse_dependency::partial_queries_need_task_dependency ... ok
test capture::parse_dependency::capture_dependency_failures_leave_the_vault_intact ... ok
test capture::parse_relation::relation_empty_double_pipe_needs_relation_label ... ok
test capture::parse_relation::relation_ownerless_reuses_dependency_target ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_diagnostics_match_execution ... ok
test capture::parse::capture_parse_reports_start_suffix_spans_and_batch_offsets ... ok
test capture::parse_relation::relation_triple_tilde_is_invalid ... ok
test aliases::script_fallback_uses_embedded_assets_for_canonical_and_old_spellings ... ok
test capture::parse_relation::relation_labels_after_pipe ... ok
test capture::parse_template::human_output_adds_template_summary ... ok
test capture::parse_template::template_parse_reports_typed_spans_items_and_summary ... ok
test capture::parse_relation::relation_partial_labels_need_relation_label ... ok
test capture::parse_relation::relation_double_pipe_marks_label_hidden ... ok
test capture::parse_relation::relation_strike_guard_stays_literal ... ok
test capture::parse_dependency::literal_ampersands_stay_prose ... ok
test capture::parse_relation::relation_single_pipe_omits_hidden ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_human_and_help ... ok
test capture::parse_relation::relation_bare_and_partial_targets_need_relation_target ... ok
test capture::parse_relation::relation_interleaves_with_dependencies_in_either_order ... ok
test capture::parse_relation::relation_triple_pipe_is_teaching_error ... ok
test capture::parse_relation::relation_complete_to_from_label_and_owner_reuse ... ok
test capture::parse_template::template_parse_one_line_values_share_line_with_per_value_ranges ... ok
test capture::parse_template::expanded_row_diagnostics_map_bad_ids_to_fields_and_dedupe_literals ... ok
test capture::parse_blocked_task::star_twins_of_ampersand_rejections_name_the_sigil ... ok
test capture::parse_template::headerless_placeholder_suggests_template_without_changing_capture_items ... ok
test capture::parse_relation::relation_digit_and_slash_guards_stay_literal ... ok
test capture::plan_budget::capture_complete_start_name_new_row_reports_plan_themes ... ok
test capture::plan_budget::capture_complete_create_row_reports_plan_themes ... ok
test capture::plan_budget::capture_complete_create_row_omits_plan_themes_without_config ... ok
test capture::plan_budget::capture_complete_start_name_again_row_reports_plan_themes ... ok
test capture::complete_themes::theme_menu_vectors ... ok
test capture::open_notes::open_notes_task_dependency_lands_on_the_item_block_id ... ok
test capture::plan_budget::capture_parse_link_close_with_drop_reports_close ... ok
test capture::parse_blocked_task::blocked_task_parse_vectors_cover_leading_quoted_and_nested ... ok
test capture::parse_relation::relation_session_token_drops_are_unchanged ... ok
test capture::parse_template::template_clipboard_follows_expanded_instances ... ok
test capture::pomodoro_chain::chain_capture_parse_reports_per_token_items ... ok
test capture::plan_budget::capture_strict_mode_refuses_project_note_path ... ok
test capture::plan_budget::capture_strict_mode_refuses_new_theme_past_cap_atomically ... ok
test capture::plan_budget::capture_strict_mode_refuses_toggle_path ... ok
test capture::open_notes::open_notes_relative_day_file_includes_day_and_matches_written_digest ... ok
test capture::parse_template::template_placeholders_split_capture_spans_and_refusals_are_reported ... ok
test capture::parse_template::template_row_need_and_arity_diagnostic_use_typed_ranges ... ok
test capture::pomodoro_chain::chain_dry_run_writes_nothing ... ok
test capture::parse_template::placeholders_suppress_per_row_picker_needs_but_constant_pickers_remain ... ok
test capture::pomodoro_chain::chain_capture_complete_returns_no_candidates ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_human_and_help ... ok
test capture::parse_template::template_session_suffixes_are_refused_with_typed_ranges ... ok
test capture::parse_dependency::capture_executes_new_task_dependencies ... ok
test capture::parse_dependency::capture_prj_dependency_deprojects_existing_descendant_links ... ok
test capture::plan_budget::capture_invalid_config_without_ledger_change_has_no_warning ... ok
test capture::pomodoro_chain::chain_failure_rolls_back_with_item_two_prefix ... ok
test capture::plan_budget::capture_without_ledger_change_has_no_plan_budget ... ok
test capture::plan_budget::capture_strict_mode_never_refuses_named_starts ... ok
test capture::plan_budget::capture_trailing_now_tag_fails_like_any_other_tag ... ok
test capture::inbox_route::ir_routed_bulk_with_one_off_relation_repairs_once_and_guards_write_nothing ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_human_and_help ... ok
test capture::parse_dependency::capture_consumption_reports_and_deletes_only_the_emptied_running_entry ... ok
test capture::open_notes::open_notes_ampersand_and_star_open_the_owner_only ... ok
test capture::parse_dependency::capture_dependency_consumes_links_when_newly_blocked ... ok
test capture::parse_dependency::capture_consumption_keeps_authored_notes_under_plain_task_text ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_extends_and_reports_json ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_batch_rollback ... ok
test capture::parse_dependency::capture_promotion_walks_through_prj_without_raising_it ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_reports_full_block ... ok
test capture::pomodoro_chain::chain_adjust_then_close_reports_one_cumulative_block ... ok
test capture::pomodoro_chain::chain_close_then_start_reports_next_started_block ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_batch_atomicity_and_dry_run ... ok
test capture::parse_dependency::human_consumption_line_replaces_the_legacy_warning ... ok
test capture::freshness_stamps::capture_close_to_in_progress_stamps_but_complete_does_not ... ok
test capture::inbox_route::ir_keep_answers_keep_the_task_and_satisfy_the_guard ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_drop_protocol ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_protocol ... ok
test capture::pomodoro_close_retired::double_equals_close_teaches_the_bare_spelling ... ok
test capture::plan_budget::capture_plan_budget_human_reports_meter_and_destination ... ok
test capture::plan_budget::capture_plan_budget_invalid_config_skips_with_warning ... ok
test capture::plan_budget::capture_plan_budget_warns_on_link_growth_past_cap ... ok
test capture::plan_budget::capture_plan_budget_warns_when_new_theme_grows_past_cap ... ok
test capture::plan_budget::capture_plan_budget_stays_quiet_when_over_cap_does_not_grow ... ok
test capture::plan_budget::capture_plan_budget_dry_run_matches_real_run ... ok
test capture::parse_dependency::capture_prj_dependency_blocks_tags_and_unlinks_residents ... ok
test capture::ensure_next::capture_task_toggle_named_ensure_next_moves_creates_and_noops ... ok
test capture::plan_budget::capture_strict_mode_never_refuses_session_starts ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_unchanged_next_block ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_nested_wording ... ok
test capture::pomodoro_close_retired::retired_close_in_a_chain_rolls_the_whole_batch_back ... ok
test capture::parse_blocked_task::blocked_task_picker_and_markdown_guards_are_distinct ... ok
test capture::pomodoro_close_retired::capture_parse_reports_retired_closes_as_close_diagnostics ... ok
test capture::pomodoro_close::capture_pomodoro_close_maps_unnamed_session_after_day_file_work_log ... ok
test capture::pomodoro_close::capture_pomodoro_close_maps_repeated_name_after_multiple_work_log_lines ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_parse ... ok
test capture::inbox_route::ir_routed_link_moves_with_repair_stamp_follow_and_open_notes ... ok
test capture::blocked_tasks::st19_existing_owner_and_forced_task ... ok
test capture::pomodoro_close::capture_pomodoro_close_tracks_blocks_past_day_file_work_log ... ok
test capture::pomodoro_close_retired::retired_link_aliases_name_the_x_spelling_and_write_nothing ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_covers_open_states_and_failures ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_retired_tail ... ok
test capture::parse_pomodoro::capture_parse_named_pomodoro_start_protocol ... ok
test capture::complete_themes::theme_literal_vectors_round_trip_through_capture ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_preserves_metadata_crlf_and_fallbacks ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_clamps_and_crosses_midnight ... ok
test capture::pomodoro_chain::chain_human_output_numbers_both_items ... ok
test capture::pomodoro_chain::chain_positional_args_form_works ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_protocol ... ok
test capture::parse_dependency::capture_executes_dependency_only_updates_idempotently ... ok
test capture::plan_budget::capture_destination_human_arrows_name_each_role ... ok
test capture::pomodoro_close_retired::retired_whole_item_closes_name_the_bare_rewrite_and_write_nothing ... ok
test capture::pomodoro_link::capture_malformed_pomodoro_marker_is_usage_error_without_writes ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_complete_target ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_execution_errors ... ok
test capture::pomodoro_close_log::capture_parse_pomodoro_close_log_protocol ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_already_current ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_moved_source_and_next ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_full_blocks ... ok
test capture::pomodoro_close::capture_pomodoro_close_task_reports_closed_and_next ... ok
test capture::pomodoro_close_successors::close_all_day_file_successor_composes_edits ... ok
test capture::pomodoro_link::capture_pomodoro_dry_run_validates_and_changes_neither_note ... ok
test capture::pomodoro_close_successors::close_successor_human_rows_and_next_line ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_all ... ok
test capture::pomodoro_close_successors::close_with_invalid_dependency_note_reports_unavailable ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_plain_reports_numbered_lineup ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_complete_listed ... ok
test capture::pomodoro_close_successors::close_then_start_opens_successor_continuation ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_dry_run_and_blocks ... ok
test capture::pomodoro_close_successors::close_without_identities_reports_no_successors ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_human_output ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_rest ... ok
test capture::pomodoro_close_successors::close_successor_dry_run_matches_real ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_crlf_day_file ... ok
test capture::pomodoro_link::capture_pomodoro_missing_daily_note_does_not_create_target ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_on_project_task_refuses_drop ... ok
test capture::pomodoro_close_successors::sl17_unpicked_offers_link_none_of_six_successors ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_in_progress_and_complete ... ok
test capture::pomodoro_close_successors::sl12_two_predecessors_link_shared_dependent_once ... ok
test capture::pomodoro_close_successors::sl20_second_completion_drops_first_link_net ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_protocol ... ok
test capture::pomodoro_close_successors::sl24_successor_reuses_later_same_name_entry ... ok
test capture::pomodoro_close_successors::sl27_dropped_link_is_not_relinked ... ok
test capture::pomodoro_close_successors::sl7_close_all_creates_continuation_holding_only_successor ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_dry_run_matches_real_run ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_human_output ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_drops_own_dependency_and_closes ... ok
test capture::pomodoro_name::capture_human_names_the_starting_pomodoro_and_its_time ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_own_dependency_and_links_atomically ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_land_fixes ... ok
test capture::pomodoro_chain::chain_bare_named_start_matches_hash_spelling ... ok
test capture::pomodoro_link::capture_named_pomodoro_batch_reuses_new_placeholder ... ok
test capture::pomodoro_name::capture_pomodoros_human_output_is_plain_when_piped ... ok
test capture::pomodoro_close_successors::sl8_embed_close_appends_successor_after_carried_links ... ok
test capture::pomodoro_link::capture_pomodoro_preflight_failures_leave_both_notes_untouched ... ok
test capture::pomodoro_link::failed_start_rolls_back_a_staged_dependency_drop_for_real_and_dry_runs ... ok
test capture::pomodoro_link::capture_pomodoro_link_uses_default_day_file_and_untimed_fallback ... ok
test capture::pomodoro_name::capture_pomodoros_missing_note_and_section_warn_in_json ... ok
test capture::pomodoro_close_successors::pomodoro_close_pulls_in_parent_of_closed_subproject ... ok
test capture::pomodoro_override::override_restart_batch_rollback ... ok
test capture::pomodoro_name::capture_pomodoros_json_lists_open_entries_with_stable_picker_shape ... ok
test capture::pomodoro_name::capture_pomodoro_name_warns_when_name_is_unconfigured ... ok
test capture::pomodoro_override::override_restart_refuses_multiple_running ... ok
test capture::pomodoro_link::capture_named_pomodoro_updates_both_notes_and_skips_current ... ok
test capture::pomodoro_override::override_restart_human_output ... ok
test capture::pomodoro_close_successors::route_close_links_predecessor_then_closes_with_successor ... ok
test capture::pomodoro_override::override_swap_batch_rollback ... ok
test capture::pomodoro_link::link_suffix_timing_errors_leave_notes_byte_identical ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_dependencies_when_already_linked ... ok
test capture::pomodoro_chain::chain_matches_blank_line_batch_file_by_file ... ok
test capture::pomodoro_chain::chain_wildcard_close_matches_blank_line_batch ... ok
test capture::pomodoro_chain::chain_switches_sessions_like_a_blank_line_batch ... ok
test capture::pomodoro_name::capture_pomodoro_name_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::pomodoro_link::capture_pomodoro_linked_task_updates_both_notes_and_reports_json ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_created_named_destination ... ok
test capture::pomodoro_link::capture_pomodoro_task_with_open_dependency_is_created_unlinked ... ok
test capture::pomodoro_override::override_swap_naming_running_refuses ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_rejects_bad_grammar_and_targets ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_move_destination_first ... ok
test capture::pomodoro_name::capture_pomodoros_task_link_count_matches_dry_run_lineup ... ok
test capture::pomodoro_override::override_swap_human_output ... ok
test capture::pomodoro_name::capture_pomodoro_name_rejects_write_free_failures ... ok
test capture::pomodoro_link::dependency_drop_keeps_closed_and_unresolved_links_verbatim ... ok
test capture::pomodoro_override::override_restart_keeps_note_bearing_session ... ok
test capture::pomodoro_link::dependency_drop_human_output_names_the_removed_link ... ok
test capture::pomodoro_override::override_swap_did_you_mean_spells_override ... ok
test capture::pomodoro_override::override_swap_teaching_errors ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_protocol ... ok
test capture::pomodoro_link::dependency_drop_reasons_report_schedule_and_managed_line_refusals ... ok
test capture::pomodoro_override::override_swap_keeps_annotated_ledger_verbatim ... ok
test capture::pomodoro_link::dependency_drop_supports_named_pomodoro_start ... ok
test capture::pomodoro_link::capture_pomodoro_task_reports_running_entry_block ... ok
test capture::pomodoro_link::pomodoro_link_guard_consumes_an_aliased_live_link_by_identity ... ok
test capture::pomodoro_override::override_restart_dry_run_matches_real ... ok
test capture::pomodoro_override::override_swap_kept_ledger_worked_example ... ok
test capture::pomodoro_override::override_swap_fresh_timing_worked_example ... ok
test capture::pomodoro_link::link_form_reuses_completed_multiword_pomodoro_name ... ok
test capture::pomodoro_link::link_with_start_creates_started_entry_from_completed_name ... ok
test capture::pomodoro_link::bare_named_link_suffix_writes_the_same_result_as_hash_before_equals ... ok
test capture::pomodoro_link::link_with_start_moves_queued_link_into_reused_completed_name ... ok
test capture::pomodoro_override::override_swap_placeholder_above_stays_first_future ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_park ... ok
test capture::pomodoro_override::override_swap_drops_target_lineup ... ok
test capture::pomodoro_override::override_swap_strict_never_refuses_created_target ... ok
test capture::pomodoro_override::eq_override_close_first_and_overdue ... ok
test capture::plan_budget::capture_destination_roles_cover_current_next_up_named_created ... ok
test capture::pomodoro_start::capture_pomodoro_start_active_and_ambiguous_fail_atomically ... ok
test capture::pomodoro_reset::pomodoro_reset_clears_note_free_session ... ok
test capture::pomodoro_reset::pomodoro_reset_moves_before_earlier_future ... ok
test capture::pomodoro_name::capture_pomodoro_name_plus_is_selectable_and_targetable ... ok
test capture::pomodoro_override::override_swap_unnamed_running ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_only_forms ... ok
test capture::pomodoro_override::override_swap_reports_notes ... ok
test capture::pomodoro_override::eq_override_human_warning_lines ... ok
test capture::pomodoro_override::override_swap_again_and_created_targets ... ok
test capture::pomodoro_override::override_restart_preserves_crlf_and_missing_newline ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_runtime ... ok
test capture::pomodoro_start::capture_pomodoro_start_dry_run_and_batch_rollback ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_batches ... ok
test capture::pomodoro_start::capture_pomodoro_start_batch_adjusts_moved_entry ... ok
test capture::pomodoro_link::capture_pomodoro_link_drops_dependencies_without_existing_link ... ok
test capture::pomodoro_link::capture_named_pomodoro_dry_run_and_failures_leave_notes_untouched ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_reports_full_block ... ok
test capture::pomodoro_override::override_swap_preserves_crlf_and_missing_newline ... ok
test capture::pomodoro_override::override_swap_chains ... ok
test capture::pomodoro_override::override_swap_named_restart_matches_plain_restart ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_wildcard_logs_resolve_once_against_staged_lineup ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_named_destination_before_link_move ... ok
test capture::pomodoro_start_named::named_start_human_created_dry_run_and_forced_flags ... ok
test capture::pomodoro_start_drop::start_drop_out_of_range_and_empty_lineup ... ok
test capture::pomodoro_override::idle_start_omits_override_metadata_and_fallback_copy ... ok
test capture::pomodoro_override::retired_doubled_starts_teach_the_single_equals_rewrite ... ok
test capture::pomodoro_start::capture_pomodoro_start_crlf_no_final_newline_moves_up ... ok
test capture::pomodoro_start_named::named_start_grammar_errors_are_precise ... ok
test capture::pomodoros_agenda::agenda_all_lists_completed_with_empty_payloads ... ok
test capture::pomodoro_start::capture_pomodoro_start_rejects_invalid_and_conflicting_syntax ... ok
test capture::pomodoro_start::capture_pomodoro_start_already_in_slot_keeps_blank_line ... ok
test capture::pomodoro_override::override_swap_dry_run_matches_real ... ok
test capture::pomodoro_start_drop::start_drop_bare_removes_link_with_nested_note ... ok
test capture::pomodoro_start_drop::start_drop_crlf_day_file ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_moves_first ... ok
test capture::pomodoro_start_named::named_start_again_creates_from_completed_name ... ok
test capture::pomodoro_start_named::named_start_existing_reports_json_and_moves_to_current_slot ... ok
test capture::pomodoro_override::override_restart_matches_reset_then_start_on_note_free ... ok
test capture::pomodoros_agenda::agenda_budget_includes_real_zero_for_empty_and_completed_only_ledgers ... ok
test capture::pomodoros_agenda::agenda_default_output_stays_byte_identical ... ok
test capture::pomodoros_agenda::agenda_empty_golden ... ok
test capture::pomodoro_start_named::named_start_created_reports_added_block ... ok
test capture::pomodoro_start_drop::start_lineup_numbered_human_and_json ... ok
test capture::pomodoros_agenda::agenda_current_golden ... ok
test capture::pomodoros_agenda::agenda_multiple_timed_golden ... ok
test capture::pomodoros_agenda::agenda_no_daily_note_golden ... ok
test capture::pomodoros_agenda::agenda_nothing_running_golden ... ok
test capture::pomodoro_reset::pomodoro_reset_note_fallback_stays_close ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_acceptance ... ok
test capture::priority::capture_priority_dry_run_prints_schedule_log_without_writing ... ok
test capture::pomodoros_agenda::agenda_budget_output_is_repeatable_and_read_only ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_moved_block ... ok
test capture::pomodoros_agenda::agenda_budget_uses_configured_caps_and_strict_over_comparison ... ok
test capture::pomodoros_agenda::agenda_heavy_golden ... ok
test capture::priority::capture_priority_missing_config_file_is_io_error_without_writes ... ok
test capture::pomodoros_agenda::agenda_budget_omits_missing_section_and_degrades_on_invalid_config ... ok
test capture::priority::capture_priority_level_four_rolls_scheduled_date_in_window ... ok
test capture::pomodoros_agenda::agenda_budget_matches_plan_for_merged_exempt_alias_and_prose_links ... ok
test capture::priority::capture_mid_line_dollar_amount_stays_task_text ... ok
test capture::pomodoro_start_drop::start_lineup_counted_and_named ... ok
test capture::priority::capture_priority_level_one_rolls_scheduled_date_in_window ... ok
test capture::pomodoro_start_named::named_start_bare_spelling_writes_the_same_as_hash ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_moves_and_reports_json ... ok
test capture::priority::capture_parse_reports_priority_spans_and_retired_markers ... ok
test capture::priority::capture_priority_out_of_range_is_usage_error_without_writes ... ok
test capture::pomodoro_reset::pomodoro_reset_uppercase_and_modifiers ... ok
test capture::priority::capture_without_priority_token_tolerates_missing_config_file ... ok
test capture::priority::capture_priority_with_clip_orders_clip_children_before_schedule_log ... ok
test capture::priority::capture_priority_with_explicit_schedule_skips_roll ... ok
test capture::pomodoro_start_named::named_start_missing_creates_and_warns_on_near_miss ... ok
test capture::project_note::capture_project_note_named_caret_form_rejects_the_unused_pomodoro ... ok
test capture::pomodoro_override::override_restart_worked_example_rows ... ok
test capture::pomodoro_start_named::named_start_prefix_and_duration_forms ... ok
test capture::priority::capture_priority_renders_before_scheduled_and_before_pomodoro_block_id ... ok
test capture::priority::capture_bare_dollar_matches_priority_level_one ... ok
test capture::project_note::capture_project_note_retired_colon_forms_fail_with_teaching_errors ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_bare_defaults_and_midnight_wrap ... ok
test capture::pomodoros_agenda::agenda_numbers_match_operator_lineups ... ok
test capture::pomodoro_override::refuse_override_guard ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_chains ... ok
test capture::priority::capture_priority_sub_bullet_nests_schedule_log_under_the_child ... ok
test capture::priority::capture_priority_schedule_log_uses_the_target_notes_indent_unit ... ok
test capture::pomodoro_start_named::named_start_running_guards_and_switch_chain ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_batch_atomicity_and_dry_run ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_preserves_metadata_and_matches_plugin ... ok
test capture::priority::capture_priority_json_includes_priority_fields_only_when_set ... ok
test capture::project_close::close_leaves_inherited_resident_blocked_naming_parent ... ok
test capture::project_close::close_leaves_resident_blocked_by_project ... ok
test capture::pomodoro_start::capture_pomodoro_start_midnight_wrap_and_bob_now ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_listed_matches_ledger ... ok
test capture::pomodoro_start::capture_pomodoro_start_creates_unnamed_when_no_placeholder ... ok
test capture::priority::capture_escaped_dollar_amount_stays_task_text ... ok
test capture::project_note::capture_project_note_creates_plain_note_with_json_and_human_output ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_to_current_slot_screenshot_repro ... ok
test capture::project_close::close_leaves_tagged_prj_blocked_without_recovery ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_and_new ... ok
test capture::pomodoro_start::capture_pomodoro_start_unnamed_moves_between_done_and_review ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_and_new_task_wildcards ... ok
test capture::project_note::capture_project_note_renders_authored_tasks_sections_and_tasks_merge ... ok
test capture::priority::capture_retired_priority_marker_is_a_usage_error ... ok
test capture::project_note::capture_project_note_schedule_and_priority_write_inline_date_and_log ... ok
test capture::r#ref::capture_bracketed_url_queues_without_brackets ... ok
test capture::pomodoro_override::override_unnamed_running_session_carries_derived_homes ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_selects_first_placeholder_and_moves ... ok
test capture::project_note::capture_project_note_reports_created_pomodoro_block ... ok
test capture::project_note::capture_project_note_dry_run_and_batch_parenting_and_rollback ... ok
test capture::r#ref::capture_config_off_and_invalid_config_keep_tasks ... ok
test capture::pomodoro_start_drop::link_and_task_starts_stay_byte_stable ... ok
test capture::r#ref::capture_dry_run_and_parse_never_touch_the_network_or_spool ... ok
test capture::r#ref::capture_spool_hit_is_clipping ... ok
test capture::project_pull_in::unplanned_pull_in_is_reported_as_surface_in_human_output ... ok
test capture::r#ref::capture_excluded_and_corporate_hosts_stay_tasks ... ok
test capture::r#ref::queued_job_ids_deduplicate_a_claim_overlap_and_keep_extra_jobs ... ok
test capture::r#ref::capture_dry_run_routes_each_pdf_backed_list_source_to_library ... ok
test capture::project_pull_in::already_planned_pull_in_raises_project_without_duplicate_link ... ok
test capture::r#ref::capture_parse_reports_ref_mode_and_span ... ok
test capture::r#ref::capture_lone_url_queues_a_ref_job ... ok
test capture::r#ref::capture_inline_global_blocks_ref_claim ... ok
test capture::relate_existing::rx11_cycle_path_starts_at_new_edge_source ... ok
test capture::r#ref::capture_repeat_in_draft_is_duplicate ... ok
test capture::project_pull_in::pomodoro_close_pulls_in_project_at_continuation ... ok
test capture::pomodoro_start_drop::start_drop_lexical_errors ... ok
test capture::project_note::capture_project_note_task_links_need_the_day_file_only_for_links ... ok
test capture::pomodoro_override::override_swap_matches_reset_then_start ... ok
test capture::pomodoro_close::capture_pomodoro_close_worked_example ... ok
test capture::relate_existing::rx10_child_bullets_need_text ... ok
test capture::ref_grammar::capture_lone_bare_url_stays_a_task_while_routing_is_off ... ok
test capture::ref_grammar::capture_url_list_writes_one_task_per_line ... ok
test capture::project_pull_in::still_blocked_project_row_has_trigger_and_context_before_reason ... ok
test capture::r#ref::capture_dry_run_matches_real_apart_from_dry_run_and_job ... ok
test capture::project_pull_in::tagged_parent_prj_close_stays_blocked_naming_grandparent ... ok
test capture::r#ref::capture_staged_write_failure_removes_jobs ... ok
test capture::project_pull_in::stale_blocked_resident_stays_blocked ... ok
test capture::project_close::close_recovers_prj_and_residents_with_unblocked ... ok
test capture::r#ref::explicit_url_clip_forms_keep_the_clipboard_path ... ok
test capture::project_note::capture_project_note_rejections_leave_no_partial_write ... ok
test capture::r#ref::capture_with_kick_returns_before_the_clip_finishes ... ok
test capture::r#ref::capture_mixed_list_and_draft_plan_each_item ... ok
test capture::project_note::capture_project_note_task_links_write_the_worked_example ... ok
test capture::project_note::capture_project_note_task_links_report_the_resolved_pomodoro_name ... ok
test capture::project_note::capture_project_note_task_links_use_the_implicit_pomodoro ... ok
test capture::project_pull_in::parent_pull_in_row_drops_when_parent_prj_also_closes ... ok
test capture::project_pull_in::punctuation_hide_pull_in_and_sync_agrees ... ok
test capture::relations::dry_run_human_says_would ... ok
test capture::relations::ld_dry_run_previews_hides_without_writing ... ok
test capture::project_pull_in::idless_last_task_close_pulls_in_and_sync_agrees ... ok
test capture::related::bulk_draft_anchors_dedupe_linked_tasks_and_project_modes ... ok
test capture::r#ref::capture_url_list_queues_one_item_per_line ... ok
test capture::related::linked_candidates_are_reported_and_excluded_and_closed_rows_use_split_defaults ... ok
test capture::related::draft_gates_short_titles_templates_and_noncreating_items_before_vault_io ... ok
test capture::related::idless_rows_offer_suggestions_and_atomic_code_spans_stay_distinct ... ok
test capture::relations::lx11_operator_relation_error ... ok
test capture::project_pull_in::disabled_pull_in_surfaces_and_in_progress_pull_in_stays_in_progress ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_forms ... ok
test capture::relate_existing::rx13_suffixed_owners_keep_must_be_bare ... ok
test capture::project_note::capture_project_note_task_links_dry_run_batch_and_rollback ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_selection_protocol ... ok
test capture::relate_existing::rx16_new_task_prints_per_prerequisite_row ... ok
test capture::r#ref::capture_library_hits_are_unchanged ... ok
test capture::project_pull_in::due_project_schedule_applies_sync_hidden_task_recount ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_guards_fail_write_free ... ok
test capture::relate_existing::rx7_closed_star_owner_is_refused ... ok
test capture::related::recapture_contract_golden_includes_actions_defaults_and_cross_note_matches ... ok
test capture::relations::lx10_malformed_linked_from_skips_mirror ... ok
test capture::r#ref::capture_unknown_library_queues_with_message ... ok
test capture::project_pull_in::multi_item_project_pull_ins_obey_surface_and_net_pass ... ok
test capture::pomodoro_start_drop::start_drop_counted_offset_named_and_empty_session ... ok
test capture::r#ref::capture_ref_parent_selection_reports_canonical_routes_and_hints ... ok
test capture::relations::lx9_malformed_links_refuses ... ok
test capture::rewrite::capture_rewrite_human_output_is_plain_and_concise ... ok
test capture::rewrite::capture_parse_does_not_apply_the_separator_toggle ... ok
test capture::rewrite::capture_rewrite_json_absorbs_a_local_marker ... ok
test capture::rewrite::capture_rewrite_json_reports_a_rule_a5_notice_without_changing_text ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_adjustments ... ok
test capture::relate_existing::rx8_unresolved_plus_selector_never_creates_a_task ... ok
test capture::r#ref::capture_url_with_markers_or_flags_stays_a_task ... ok
test capture::relate_existing::rx9_relationship_needs_text_in_parse_and_execute ... ok
test capture::r#ref::capture_end_to_end_falls_back_on_blocked ... ok
test capture::project_pull_in::subproject_close_pulls_in_parent_and_sync_agrees ... ok
test capture::rewrite::capture_rewrite_json_starts_a_template ... ok
test capture::rewrite::capture_rewrite_json_reports_no_rewrite_without_a_bare_at_at ... ok
test capture::rewrite::capture_rewrite_reads_stdin_when_text_is_omitted ... ok
test capture::r#ref::percent_listen_reference_never_reads_clipboard_and_queues_listen_job ... ok
test capture::rewrite::capture_rewrite_rejects_a_cursor_off_a_char_boundary ... ok
test capture::relations::ld_read_only_journal_still_captures_with_retry_warning ... ok
test capture::rewrite::capture_rewrite_json_switches_a_block_id_separator ... ok
test capture::routing::capture_empty_input_is_usage_error ... ok
test capture::routing::capture_json_failure_prints_error_object ... ok
test capture::rewrite::capture_rewrite_never_touches_the_vault_or_clipboard ... ok
test capture::routing::capture_dry_run_reports_without_writing ... ok
test capture::rewrite::capture_rewrite_missing_text_is_a_usage_error ... ok
test capture::relations::lx1_new_task_to_archived_skips_mirror_without_mint ... ok
test capture::relations::lx8_self_non_task_and_missing_id_refuse ... ok
test capture::relate_existing::rx5_colon_alias_still_owns ... ok
test capture::r#ref::capture_end_to_end_clips_through_the_worker ... ok
test capture::pomodoro_start::capture_pomodoro_start_new_entry_uses_first_open_placement ... ok
test capture::relations::lx13_relation_is_inert ... ok
test capture::relations::ld_mixed_pipes_and_repeated_keys_collapse_to_one_event ... ok
test capture::relations::lx16_same_note_pair_composes ... ok
test capture::project_pull_in::external_blocker_pull_in_and_unplanned_ready_recovery ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_queued_tasks ... ok
test capture::relations::ld_new_one_off_label_writes_plain_label_and_hides ... ok
test capture::routing::capture_legacy_standalone_marker_form_is_usage_error ... ok
test capture::routing::capture_rejects_stdin_continuation_text_that_is_not_a_bullet ... ok
test capture::relations::previous_daily_target_skips_mirror ... ok
test capture::routing::capture_schedule_only_is_usage_error ... ok
test capture::routing::capture_json_omits_sub_bullets_for_an_ordinary_single_line_capture ... ok
test capture::routing::capture_scheduled_dry_run_reports_without_writing ... ok
test capture::relations::lx5_todays_daily_target_gets_mirror_and_mints_source ... ok
test capture::routing::capture_json_output_is_machine_readable ... ok
test capture::relations::lx7_from_target_path_refusals_leave_vault_untouched ... ok
test capture::relate_existing::rx2_existing_owner_star ... ok
test capture::relations::lx15_to_and_from_same_target_are_independent ... ok
test capture::routing::capture_json_output_includes_scheduled_date ... ok
test capture::routing::capture_scheduled_offset_out_of_range_is_usage_error ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_shifts ... ok
test capture::routing::capture_route_override_keeps_at_tokens_literal ... ok
test capture::routing::capture_nonterminal_schedule_token_stays_literal ... ok
test capture::routing::capture_bullet_json_reports_rendered_line ... ok
test capture::routing::capture_reads_the_complete_piped_stdin_stream_when_text_is_absent ... ok
test capture::sections::capture_forced_section_requires_route ... ok
test capture::r#ref::failed_percent_listen_worker_keeps_listen_retry_guidance ... ok
test capture::relations::lx4_ampersand_blocks_and_relation_stays_inert ... ok
test capture::sections::capture_sections_json_skips_generated_status_groups ... ok
test capture::related::calibration_excludes_self_before_closed_suppression_and_limits ... ok
test capture::sections::capture_sections_json_lists_sections_in_order ... ok
test capture::routing::capture_unrouted_appends_to_mac_inbox ... ok
test capture::routing::capture_unrouted_scheduled_offset_appends_property ... ok
test capture::relations::lx14_duplicate_noop_and_conflicting_labels_refuse ... ok
test capture::sections::capture_sections_missing_note_returns_empty_json ... ok
test capture::relations::lx2_from_relation_mints_new_task_and_writes_both_sides ... ok
test capture::relate_existing::rx14_in_progress_owner_consumes_running_link ... ok
test capture::routing::capture_leading_route_bullet_inserts_into_section_by_prefix ... ok
test capture::sections::capture_sections_invalid_or_missing_route_errors_cleanly ... ok
test capture::routing::capture_scheduled_zero_uses_created_date ... ok
test capture::sections::capture_tasks_json_lists_open_tasks_with_stable_picker_shape ... ok
test capture::routing::capture_routed_bullet_inserts_into_section_by_prefix ... ok
test capture::sections::capture_tasks_human_output_is_plain_when_piped ... ok
test capture::routing::capture_routed_prefers_tasks_section_over_root_task ... ok
test capture::routing::capture_routed_task_into_tagged_project_lands_blocked_and_tagged ... ok
test capture::sections::capture_article_exact_raw_title_precedes_earlier_identity_match ... ok
test capture::relate_existing::rx12_sub_bullet_prints_children_then_relationship ... ok
test capture::routing::capture_routed_task_into_blocked_project_lands_blocked_and_tagged ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_batches_compose_and_roll_back ... ok
test capture::sections::capture_article_prefix_prefers_raw_number_in_document_order ... ok
test capture::sections::capture_forced_section_inserts_exact_bullet ... ok
test capture::routing::capture_unrouted_prefers_tasks_section_in_existing_inbox ... ok
test capture::relate_existing::rx3_existing_owner_both_directions ... ok
test capture::routing::capture_bullet_prefix_prefers_non_h1_and_ignores_prefix_case ... ok
test capture::relations::lx6_kill_switch_skips_mirror_and_source_mint ... ok
test capture::sections::capture_article_prefix_matches_de_numbered_identity ... ok
test capture::rewrite::capture_rewrite_pomodoro_close_protocol ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_starts ... ok
test capture::sections::capture_forced_task_section_option_errors ... ok
test capture::routing::capture_bullet_marker_order_routes_equivalently ... ok
test capture::routing::capture_routed_prefix_inserts_and_suffix_creates_file ... ok
test capture::successor_offers::so27_require_choice_refuses_when_offers_exist ... ok
test capture::r#ref::percent_listen_reference_runs_existing_worker_and_installs_audio ... ok
test capture::targets::capture_targets_empty_vault_still_lists_inbox_default ... ok
test capture::sub_bullet::capture_sub_bullet_task_option_keeps_at_tokens_literal ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_running_entry_block ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_complete_subtree_before_parent_logs ... ok
test capture::targets::capture_targets_json_failure_prints_error_object ... ok
test capture::targets::capture_targets_human_groups_and_summarizes_without_ansi ... ok
test capture::relate_existing::rx6_inherited_owner_writes_edge_only ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_rejects_shape_and_forced_flags ... ok
test capture::relations::ld_visible_existing_label_warns_and_hides ... ok
test capture::sub_bullet::capture_sub_bullet_uses_dominant_indent_preserves_crlf_and_dry_run ... ok
test capture::routing::capture_scheduled_offset_routes_in_either_order ... ok
test capture::targets::capture_targets_json_lists_picker_targets_in_order ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_last_completed_entry_block ... ok
test capture::task_blocks::capture_task_blocks_dry_run_reports_the_parent_block ... ok
test capture::task_complete::already_done_is_a_noop ... ok
test capture::task_blocks::capture_task_blocks_human_output_is_unchanged ... ok
test capture::task_blocks::capture_task_blocks_omitted_without_sub_bullets ... ok
test capture::successor_offers::so15_no_open_entry_is_no_destination ... ok
test capture::successor_offers::so16_two_open_timed_is_no_destination ... ok
test capture::task_blocks::capture_task_blocks_and_pomodoro_blocks_report_independently ... ok
test capture::sections::capture_article_forced_section_matches_identity_and_stale_number ... ok
test capture::targets::capture_targets_json_reports_aliases_and_human_shows_aka ... ok
test capture::targets::capture_targets_verbose_emits_skip_warnings ... ok
test capture::task_complete::ambiguous_and_duplicate_refusals_state_exit_code_and_leave_vault_untouched ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_json_and_human ... ok
test capture::successor_offers::so6_bad_picks_are_usage_and_write_free ... ok
test capture::task_complete::ambiguous_note_and_duplicate_id_and_forced_flags_fail ... ok
test capture::task_complete::failure_in_item_two_rolls_item_one_back ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_diagnostics ... ok
test capture::task_complete::forced_flags_exit_2_with_exact_message_and_untouched_vault ... ok
test capture::task_complete::hello_ignores_poisoned_note_only_discovery_would_touch ... ok
test capture::sections::capture_task_section_managed_log_geometry ... ok
test capture::successor_offers::no_successors_still_reports_pull_in ... ok
test capture::successor_offers::so14_unplanned_predecessor_implicit_destination ... ok
test capture::successor_integration::close_successor_then_consume_net ... ok
test capture::sections::capture_forced_task_section_matches_title_exactly ... ok
test capture::sections::capture_non_article_numbered_heading_keeps_raw_title_matching ... ok
test capture::task_blocks::capture_task_blocks_real_run_equals_dry_run_except_dry_run ... ok
test capture::successor_offers::so19_disabled_config_has_no_offers ... ok
test capture::successor_offers::so17_emptied_project_unpicked ... ok
test capture::task_complete::embedded_subtasks_close_and_blocked_descendant_stays_open ... ok
test capture::task_complete::complete_without_id_skips_dependent_lookup ... ok
test capture::successor_integration::restart_and_reset_never_complete_prerequisites ... ok
test capture::task_complete::sl19_reapplied_close_reports_nothing ... ok
test capture::relate_existing::rx1_existing_owner_ampersand_either_order ... ok
test capture::pomodoro_start::capture_pomodoro_start_default_and_explicit_durations ... ok
test capture::task_complete::refusals_leave_the_vault_intact ... ok
test capture::task_complete_parse::task_complete_padded_item_refuses_without_capturing ... ok
test capture::successor_offers::so26_human_lists_offers_without_linking ... ok
test capture::task_complete_parse::task_complete_padded_item_reports_invalid_task_complete ... ok
test capture::sections::capture_task_section_inserts_into_first_middle_and_last_sections ... ok
test capture::sections::capture_task_section_prefix_vs_whole_slug_and_multiword ... ok
test capture::successor_offers::dry_run_parity_matches_pull_in_rows ... ok
test capture::r#ref::capture_human_wording_for_every_case ... ok
test capture::task_complete_parse::task_complete_query_refuses_with_the_picker_teaching_error ... ok
test capture::task_complete_parse::task_complete_token_executes_now_that_execute_landed ... ok
test capture::task_goto::capture_goto_query_fails_with_the_t3_teaching_error ... ok
test capture::successor_integration::ref_task_successor_links_like_an_ordinary_task ... ok
test capture::task_complete_parse::task_complete_query_reports_incomplete_needing_task_complete ... ok
test capture::task_goto::complete_goto_candidates_carry_note_path_and_target_without_link_keys ... ok
test capture::task_goto::capture_batch_with_a_slash_item_captures_both_items_as_usual ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_with_parent_indentation_and_reports_json ... ok
test capture::task_complete::invalid_dependency_note_reports_unavailable_and_skips_linking ... ok
test capture::task_complete::next_completes_with_running_session_strike ... ok
test capture::task_complete::custom_global_filter_yields_clean_text_and_human_output ... ok
test capture::task_goto::complete_goto_human_lines_show_note_path_and_line ... ok
test capture::task_complete::carried_link_dedupes_into_morning_entry_when_nothing_runs ... ok
test capture::task_complete::close_completing_nothing_ignores_poisoned_note ... ok
test capture::task_complete::batch_of_two_completions_reports_already_done_for_repeats ... ok
test capture::pomodoro_start_drop::start_drop_batch_chain_and_rollback ... ok
test capture::sub_bullet::capture_sub_bullet_selectors_and_batch_keep_order_above_logs ... ok
test capture::task_goto::capture_parse_goto_query_reports_incomplete_task_goto ... ok
test capture::task_complete_parse::single_item_task_complete_mirrors_top_level_object ... ok
test capture::task_complete_parse::task_complete_token_reports_mode_spans_and_object ... ok
test capture::task_goto::capture_complete_goto_query_reports_task_goto_without_query_or_picker ... ok
test capture::relations::lx3_existing_owner_relabel_and_unchanged_rerun ... ok
test capture::task_complete::task_living_in_todays_daily_note_completes_in_place ... ok
test capture::task_complete::dry_run_json_matches_real ... ok
test capture::task_complete::sl10_successor_block_id_is_minted ... ok
test capture::task_complete::day_file_successor_without_block_id_mints_in_place ... ok
test capture::task_complete::day_file_successor_composes_task_and_ledger_edits ... ok
test capture::task_complete::blocked_root_completes_and_dependent_unblocks ... ok
test capture::task_link::capture_parse_colon_query_reports_incomplete_task_link ... ok
test capture::task_complete::placeholder_link_moves_to_running_entry_and_placeholder_is_removed ... ok
test capture::relations::ld_hidden_label_writes_no_event ... ok
test capture::task_link::capture_colon_query_fails_with_the_picker_teaching_error ... ok
test capture::task_goto::shell_completion_serves_no_goto_rows ... ok
test capture::task_link::capture_colon_query_teaches_the_at_spelling_for_links ... ok
test capture::task_complete_parse::bang_prose_rows_parse_as_editor_tasks_and_queries ... ok
test capture::task_link::capture_colon_query_json_failure_reports_ok_false ... ok
test capture::task_marker::capture_malformed_task_block_id_marker_is_usage_error_without_writes ... ok
test capture::task_marker::capture_retired_double_colon_marker_is_usage_error_without_writes ... ok
test capture::task_link::capture_batch_with_a_colon_query_writes_nothing ... ok
test capture::task_link::capture_complete_colon_query_reports_task_link_with_empty_candidates ... ok
test capture::task_complete::sl16_gate_reports_checked_with_empty_rows ... ok
test capture::template::bad_template_origin_is_a_usage_error ... ok
test capture::template::expand_with_bad_template_origin_is_a_usage_error ... ok
test capture::task_id::capture_task_sections_json_and_human_list_sections ... ok
test capture::successor_offers::so1_project_offers_pick_one ... ok
test capture::task_complete::sl18_disabled_config_recovers_without_link ... ok
test capture::template::duplicate_ids_across_template_rows_refuse_with_the_later_row ... ok
test capture::template::a_late_duplicate_id_refuses_the_whole_template_with_row_context ... ok
test capture::task_toggle::capture_task_toggle_on_project_scheduled_resident_reports_date ... ok
test capture::task_toggle::capture_task_toggle_on_date_blocked_prj_is_refused ... ok
test capture::task_marker::capture_task_block_id_marker_creates_missing_routed_note ... ok
test capture::task_complete_parse::bang_prose_rows_still_capture_as_tasks ... ok
test capture::task_marker::capture_task_block_id_dry_run_and_duplicate_preflight_do_not_write ... ok
test capture::template::parser_diagnostics_keep_the_template_source_line ... ok
test capture::task_complete::human_output_names_transition_ledger_and_unblocked ... ok
test capture::sections::capture_task_section_errors_leave_the_note_unchanged ... ok
test capture::task_complete::sl2_successor_keeps_slot_retirement_moves_predecessor ... ok
test capture::task_complete::sl1_successor_links_into_vacated_slot ... ok
test capture::task_id::capture_task_id_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::template::template_human_summary_names_the_source_rows ... ok
test capture::task_complete::two_completions_plus_close_commit_as_one_batch ... ok
test capture::task_complete::sl9_unplanned_predecessor_recovers_without_link ... ok
test capture::template::template_clipboard_markers_refuse_even_with_no_clip ... ok
test capture::template_expand::capture_expand_ignores_capture_options_and_never_needs_a_vault ... ok
test capture::task_toggle::capture_task_toggle_can_edit_task_in_daily_note ... ok
test capture::template::template_execution_reports_first_issue_in_draft_order ... ok
test capture::template_expand::capture_expand_reports_language_errors_as_usage_errors ... ok
test capture::task_complete::exact_human_output_for_subtasks_and_unblocked ... ok
test capture::template_expand::capture_expand_is_identity_for_plain_drafts ... ok
test capture::template::template_url_listen_marker_is_not_clipboard_capture ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_rejects_bad_grammar_and_targets ... ok
test capture::task_goto::capture_goto_refusals_cover_slash_forms_and_leave_the_vault_untouched ... ok
test capture::template::unwritable_shelf_keeps_exit_zero_with_not_saved ... ok
test capture::task_toggle::promotion_walks_through_a_blocked_seed_without_raising_it ... ok
test capture_templates::bare_delete_is_a_usage_error_and_leaves_the_store_absent ... ok
test capture::template::template_one_placeholder_one_line_dry_run_matches_three_lines ... ok
test capture::theme_warnings::capture_deferred_priority_still_warns_when_theme_grows ... ok
test capture::template_expand::capture_expand_prints_template_text_and_json_summary ... ok
test capture::task_toggle::capture_task_toggle_reports_unlink_removal_from_two_entries ... ok
test catalog::missing_protocol_exits_2_with_usage ... ok
test capture::relate_existing::rx4_caret_alias_executes_like_plus_owner ... ok
test catalog::protocol_2_returns_json_error_and_exit_2 ... ok
test capture_templates::save_of_headerless_draft_is_not_a_template ... ok
test capture::template::template_session_suffixes_refuse_in_execution ... ok
test capture::task_complete::sl14_ambiguous_basename_uses_dir_link ... ok
test capture::template_expand::capture_expand_one_line_values_equal_three_line_rows ... ok
test catalog::catalog_is_read_only ... ok
test capture::pomodoro_close::capture_pomodoro_close_diagnostics ... ok
test catalog::protocol_1_parses_with_schema_version_one ... ok
test capture::task_goto::complete_goto_route_ref_sequence_equals_task_link ... ok
test catalog::catalog_is_fast ... ok
test capture::task_goto::capture_parse_goto_prose_rows_keep_their_current_parse ... ok
test capture::task_toggle::capture_task_toggle_on_project_blocked_resident_refuses_drop ... ok
test capture::sections::capture_task_section_indent_units_crlf_and_dry_run ... ok
test capture_templates::newer_schema_with_changed_field_type_stays_readable_and_refuses_writes ... ok
test completion::bash::bash_default_target_honors_env ... ok
test capture::template::template_human_output_reports_saved ... ok
test completion::bash::bash_completes_attached_format_value ... ok
test completion::bash::bash_counts_unicode_prefix_in_chars ... ok
test completion::bash::bash_shell_selection ... ok
test capture::template::plain_captures_stay_byte_identical_without_a_header ... ok
test completion::bash::bash_print_matches_installed_bytes ... ok
test completion::bash::bash_completes_command_prefix ... ok
test completion::bash::bash_completes_attached_files_in_value ... ok
test completion::bash::bash_maps_dirs_directive ... ok
test capture::template::template_executes_rows_and_adds_row_metadata ... ok
test capture::task_marker::capture_task_block_id_marker_writes_ordinary_task_and_ignores_daily_note ... ok
test capture::successor_offers::so2_so32_fan_out_offers_every_dependent ... ok
test completion::bash::bash_filters_create_target_by_extension ... ok
test capture::template::template_clip_flag_and_session_operators_have_stable_codes ... ok
test catalog::protocol_equals_form_matches_space_form ... ok
test completion::bash::bash_keeps_spaces_in_one_argument ... ok
test capture_templates::definition_errors_and_newer_schema_have_stable_recovery_paths ... ok
test capture::template::non_saving_runs_leave_the_shelf_absent ... ok
test capture_templates::clear_also_removes_the_corrupt_quarantine ... ok
test capture::task_toggle::capture_task_toggle_reports_created_named_entry ... ok
test capture::task_toggle::capture_task_toggle_reports_inserted_link_block ... ok
test capture_templates::show_by_index_prints_the_insertable_draft ... ok
test completion::bash::bash_offers_nothing_once_text_starts ... ok
test capture::relate_existing::rx15_repeat_is_already_present_noop ... ok
test completion::bash::bash_open_quote_completes_route ... ok
test capture::task_toggle::capture_task_toggle_batch_uses_staged_snapshots_and_rolls_back ... ok
test capture::successor_offers::so18_parent_project_unpicked_and_picked ... ok
test completion::capture_text::caret_completes_active_tasks ... ok
test capture::task_toggle::capture_task_toggle_errors_are_actionable_without_writes ... ok
test completion::capture_text::partial_route_returns_full_set_for_shell_filtering ... ok
test completion::capture_text::newline_in_word_returns_nothing ... ok
test completion::bash::bash_unquotes_single_quoted_word ... ok
test completion::bash::bash_strips_every_wordbreak_not_just_colon ... ok
test completion::bash::bash_install_status_uninstall_round_trip ... ok
test completion::capture_text::body_bearing_route_colon_suggests_new_id ... ok
test completion::capture_text::routes_complete_at_end_of_text_word ... ok
test capture::theme_warnings::capture_skips_close_link_inventory_and_unconfigured_vocab ... ok
test completion::capture_text::options_stay_hidden_once_text_starts ... ok
test capture::successor_offers::so29_zero_offers_are_a_noop ... ok
test completion::capture_text::suffix_returns_nothing ... ok
test completion::capture_text::named_start_completes_after_hash ... ok
test completion::capture_text::bare_plus_shell_completion_returns_only_identified_parent_markers ... ok
test completion::capture_text::quoted_word_keeps_prefix_with_prefix_directive ... ok
test completion::bash::bash_reassembles_colon_split_marker ... ok
test completion::capture_text::named_start_after_inline_close_keeps_prefix ... ok
test capture::task_toggle::capture_task_toggle_drops_own_dependency_and_links ... ok
test completion::capture_text::safe_rows_only_omit_missing_ids ... ok
test completion::capture_text::task_sections_complete_after_id_hash ... ok
test completion::capture_text::sections_complete_after_hash ... ok
test capture::theme_warnings::capture_warns_on_unconfigured_start_again_and_name_field ... ok
test completion::bash::bash_verify_reports_source_remedy ... ok
test completion::capture_text::solo_route_colon_lists_existing_tasks ... ok
test completion::lifecycle::dry_run_writes_nothing ... ok
test completion::capture_text::body_bearing_text_agrees_with_capture_complete_intent ... ok
test capture_templates::human_list_covers_empty_populated_and_saving_off ... ok
test capture::task_complete::successor_dry_run_matches_real_with_human_rows ... ok
test completion::lifecycle::path_shadow_warns ... ok
test completion::lifecycle::zsh_print_matches_installed_bytes ... ok
test completion::capture_text::capture_parse_and_rewrite_share_the_text_slot ... ok
test capture::template::human_replaced_names_the_checked_out_origin ... ok
test completion::capture_text::unicode_prefix_counts_chars_not_bytes ... ok
test completion::lifecycle::first_install_then_idempotent_unchanged ... ok
test completion::lifecycle::plain_output_has_no_ansi_when_piped ... ok
test completion::protocol::double_dash_offers_long_forms_only ... ok
test completion::capture_text::relation_labels_complete_after_double_pipe ... ok
test capture::template::one_row_and_many_rows_save_the_same_shelf_entry ... ok
test completion::lifecycle::previous_install_target_rule_and_reason ... ok
test completion::protocol::attached_option_value_uses_prefix ... ok
test completion::lifecycle::status_without_verify_warns_on_recorded_unhealthy ... ok
test completion::protocol::malformed_request_exits_two ... ok
test completion::protocol::conflicting_option_is_dropped ... ok
test capture::task_link::bare_caret_link_suffix_writes_the_same_result_as_hash_before_equals ... ok
test capture_templates::list_save_show_and_delete_follow_the_template_protocol ... ok
test capture::sub_bullet::capture_sub_bullet_errors_are_actionable_in_human_and_json_modes ... ok
test capture::task_id::capture_task_id_recovers_a_shifted_line_and_rejects_write_free_failures ... ok
test completion::protocol::freshness_short_option_value_completes ... ok
test completion::protocol::format_values_carry_the_slot_group ... ok
test completion::protocol::hidden_aliases_stay_hidden ... ok
test completion::vault::locked_vault_fixture_is_removed_after_guard_and_tempdir_drop ... ok
test capture::task_toggle::capture_task_toggle_unlink_keeps_every_lane ... ok
test completion::protocol::empty_root_offers_commands_then_capture_protocol_without_options ... ok
test completion::protocol::lone_dash_offers_paired_forms ... ok
test capture::task_complete::ledger_json_carries_text_struck_in_and_dropped ... ok
test completion::protocol::present_option_is_dropped ... ok
test completion::protocol::nested_subcommands_complete ... ok
test completion::lifecycle::recorded_verification_survives_into_status ... ok
test completion::protocol::protocol_skew_reports_both_directions ... ok
test completion::protocol::alias_completion_uses_canonical_path_and_freshness_seed_is_hidden ... ok
test completion::capture_text::close_shorthands_offer_nothing ... ok
test completion::zsh_adapter::adapter_source_has_required_properties ... ok
test completion::protocol::partial_command_word_yields_the_full_unfiltered_set ... ok
test completion::protocol::file_and_dir_slots_emit_directives ... ok
test completion::protocol::pull_in_value_is_free_text ... ok
test capture::task_toggle::capture_task_toggle_link_and_unlink_updates_notes_and_reports_json ... ok
test completion::lifecycle::zsh_bound_to_function_reports ... ok
test capture::task_id::capture_task_sections_empty_and_error_paths ... ok
test completion::protocol::text_started_slot_offers_no_options ... ok
test completion::lifecycle::home_default_fpath_line_prints_without_probe ... ok
test completion::protocol::debug_log_writes_the_file_and_nothing_else ... ok
test completion::lifecycle::not_installed_shell_never_probes_and_never_fails ... ok
test completion::lifecycle::outdated_adapter_updates_without_force ... ok
test completion::lifecycle::missing_manifest_entry_reports_missing ... ok
test completion::lifecycle::target_move_removes_previous_adapter ... ok
test completion::lifecycle::externally_managed_adapter_is_reported_never_adopted ... ok
test completion::vault::levels_come_from_config_in_order ... ok
test completion::lifecycle::unrecorded_stamped_file_is_outdated_externally_managed ... ok
test completion::vault::plugins_come_from_the_repo_checkout ... ok
test completion::lifecycle::install_without_shell_args_honors_shell_plus_owned ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_worked_table ... ok
test completion::lifecycle::status_json_shape_and_bare_forms ... ok
test completion::vault::pomodoro_refs_offer_open_entries ... ok
test completion::lifecycle::usage_errors_exit_2_and_shell_selection ... ok
test completion::protocol::saved_template_group_and_format_complete_as_commands_and_static_choices ... ok
test completion::vault::unknown_route_offers_nothing ... ok
test completion::vault::routes_are_grouped_in_scan_order ... ok
test completion::protocol::task_move_is_discoverable_with_its_options ... ok
test dataview::dataview_native_table_json_projects_frontmatter_rows ... ok
test completion::lifecycle::fake_bash_never_reports_registered_when_missing ... ok
test completion::zsh_adapter::colon_escaping_empty_fields_and_defaults ... ok
test capture::task_toggle::capture_task_toggle_named_creation_dry_run_and_pull_forward ... ok
test completion::vault::task_sections_offer_exact_titles ... ok
test completion::zsh_adapter::no_color_uses_plain_header ... ok
test dataview::dataview_native_dql_paths_walks_parent_frontmatter_headlessly ... ok
test completion::lifecycle::probe_without_controlling_terminal_via_zpty ... ok
test completion::zsh_adapter::user_descriptions_format_wins ... ok
test completion::zsh_adapter::request_argv_unquotes_words_and_passes_suffix ... ok
test completion::zsh_adapter::candidate_groups_keep_order_and_nospace_flag ... ok
test completion::zsh_adapter::directives_map_to_native_widgets ... ok
test completion::protocol::empty_cursor_at_positional_slot_offers_values_first ... ok
test completion::lifecycle::closers_tell_the_truth ... ok
test completion::lifecycle::uninstall_removes_only_bob_owned_files ... ok
test dataview::dataview_obsidian_dql_paths_extracts_and_deduplicates_note_paths ... ok
test completion::vault::vault_notes_answer_files_in ... ok
test dataview::dataview_native_where_false_returns_no_rows ... ok
test dataview::dataview_obsidian_dql_json_reads_query_file_and_forwards_env_vault ... ok
test completion::zsh_adapter::default_styles_use_green_headers ... ok
test dataview::dataview_obsidian_reports_missing_command_without_query_blob ... ok
test completion::vault::missing_prerequisites_name_the_flag ... ok
test completion::zsh_adapter::empty_output_returns_one ... ok
test dataview::dataview_obsidian_markdown_prints_rendered_markdown ... ok
test completion::zsh_adapter::stderr_is_discarded ... ok
test epipe::closed_stderr_usage_error_exits_two_quietly ... ok
test dataview::dataview_rejects_removed_sync_option ... ok
test dataview::dataview_obsidian_reports_not_running_without_javascript_blob ... ok
test dataview::dataview_obsidian_source_uses_path_command_and_sentinel_protocol ... ok
test completion::protocol::ref_create_force_value_completes_both_modes ... ok
test epipe::closed_stdout_help_exits_zero_quietly ... ok
test completion::vault::deadline_override_keeps_working ... ok
test completion::vault::relation_rename_arguments_complete_catalog_labels_including_hidden ... ok
test dataview_oom::synthetic_list_census_counts_nested_children ... ok
test capture::successor_offers::so13_later_item_drops_stale_offers ... ok
test freshness::list_emoji_vault_is_refused_with_exit_2 ... ok
test dataview::dataview_native_table_paths_match_list_rows_headlessly ... ok
test dataview::dataview_obsidian_reports_protocol_errors ... ok
test dataview::dataview_obsidian_reports_missing_and_malformed_sentinel ... ok
test capture::successor_offers::so3_so4_so5_all_none_and_subset ... ok
test dataview::dataview_obsidian_dql_paths_warn_or_fail_for_missing_identities ... ok
test freshness::list_invalid_config_exits_2 ... ok
test dataview::dataview_obsidian_query_does_not_run_ob_command ... ok
test freshness::list_invalid_decay_exits_2 ... ok
test freshness::list_invalid_canonical_budget_exits_2 ... ok
test completion::lifecycle::target_rules_pick_in_order ... ok
test completion::vault::sections_follow_long_short_and_attached_route_forms ... ok
test freshness::list_invalid_tracker_intervals_exit_2 ... ok
test completion::vault::split_old_offers_themes_and_map_offers_files ... ok
test freshness::list_budget_meter_uses_upkeep ... ok
test freshness::list_canonical_budget_key_wins_and_warns ... ok
test freshness::list_hidden_reference_stays_out_while_visible_walks ... ok
test freshness::list_config_interval_and_budget ... ok
test help::capture_complete_help_is_native_only ... ok
test freshness::list_human_shows_reference_in_new_before_rotten_divider ... ok
test dataview::dataview_rejects_unsafe_origin_and_missing_bob_dir ... ok
test completion::vault::tasks_offer_open_block_ids_with_text ... ok
test completion::lifecycle::foreign_edited_and_symlink_refuse_without_force ... ok
test help::capture_pomodoros_help_is_native_only ... ok
test capture::task_complete::exact_human_output_for_strike_move_dedupe_and_done ... ok
test dataview::dataview_rejects_invalid_argument_combinations ... ok
test help::capture_pomodoro_name_help_is_native_only ... ok
test freshness::seed_preserves_existing_keeps ... ok
test freshness::list_lane_rows_cover_pending_and_next ... ok
test freshness::list_walks_projects_after_new_with_decoupled_counts ... ok
test help::capture_sections_help_is_native_only ... ok
test freshness::list_excludes_today_and_daily_lane_tasks ... ok
test dataview::dataview_short_options_are_accepted ... ok
test freshness::seed_dry_run_writes_nothing_and_reports_buckets ... ok
test help::capture_help_is_native_only ... ok
test freshness::list_json_reports_queue_counts_and_contract ... ok
test freshness::list_decay_off_and_zero_limit ... ok
test help::capture_parse_help_is_native_only ... ok
test epipe::closed_stdout_pipe_exits_zero_with_empty_stderr ... ok
test freshness::list_tracker_intervals_and_hide_gate ... ok
test freshness::list_limit_truncates_rows_not_counts ... ok
test freshness::seed_dry_run_lists_files_without_writing ... ok
test freshness::list_excludes_today_tasks ... ok
test freshness::seed_invariance_abort_lists_the_line ... ok
test help::capture_targets_help_is_native_only ... ok
test help::capture_tasks_help_is_native_only ... ok
test capture::pomodoro_name::capture_pomodoro_link_solo_grammar_and_atomic_execution ... ok
test capture::task_toggle::capture_task_toggle_links_unlinked_lanes_without_status_change ... ok
test completion::protocol::value_hints_beat_generic_kinds_entries ... ok
test help::highlights_ref_help_is_native_only ... ok
test help::capture_task_id_help_is_native_only ... ok
test help::dataview_help_is_native_only ... ok
test freshness::list_unblocked_tickler_reports_return_source ... ok
test freshness::seed_guard_refuses_and_force_overrides ... ok
test help::capture_task_sections_help_is_native_only ... ok
test help_options::capture_related_help_lists_options_alphabetically ... ok
test help::move_done_tasks_help_is_native_only ... ok
test help_options::capture_complete_help_lists_options_alphabetically ... ok
test freshness::list_json_and_human_cover_checklist_tiers ... ok
test completion::bash::bash_readline_inserts_what_bob_returned ... ok
test help::help_routes_reject_non_command_paths_before_dispatch ... ok
test help_options::capture_pomodoros_help_lists_options_alphabetically ... ok
test help::projects_help_is_native_only ... ok
test help::ref_help_matches_grouped_snapshot ... ok
test help::root_help_matches_sectioned_short_and_long_snapshots ... ok
test freshness::list_human_has_sections_and_no_ansi ... ok
test help_options::capture_task_sections_help_lists_options_alphabetically ... ok
test help_options::capture_targets_help_lists_options_alphabetically ... ok
test freshness::list_reports_keeps_and_decide_per_schema_9 ... ok
test freshness::list_json_and_human_cover_recurring_tier ... ok
test help_options::capture_tasks_help_lists_options_alphabetically ... ok
test help_options::capture_parse_help_lists_options_alphabetically ... ok
test help::nightly_help_exits_before_operational_work ... ok
test help::capture_named_start_help_mentions_start_forms ... ok
test help_options::dataview_help_lists_options_alphabetically ... ok
test help_options::capture_pomodoro_name_help_lists_options_alphabetically ... ok
test capture::template::real_template_capture_saves_and_reports_statuses ... ok
test help_options::capture_help_lists_options_alphabetically ... ok
test help_options::capture_rewrite_help_lists_options_alphabetically ... ok
test help_options::capture_task_id_help_lists_options_alphabetically ... ok
test help::freshness_seed_stays_callable_but_hidden_from_help_and_completion ... ok
test help_options::capture_sections_help_lists_options_alphabetically ... ok
test help_options::freshness_list_help_lists_options_alphabetically ... ok
test help_options::completion_help_lists_subcommands_and_options_alphabetically ... ok
test help::cache_extraction_writes_expected_files_and_modes ... ok
test help_options::freshness_help_hides_the_seed_subcommand ... ok
test help::legacy_binary_help_is_safe_and_plain ... ok
test freshness::seed_applies_stamps_and_rerun_is_noop ... ok
test freshness::list_legacy_budget_key_warns_once_and_still_counts ... ok
test help_options::highlights_ref_scan_help_lists_options_alphabetically ... ok
test help_options::highlights_ref_help_lists_subcommands_alphabetically ... ok
test help_options::highlights_ref_scan_json_verbose_is_usage_error ... ok
test help_options::ready_help_lists_options_alphabetically ... ok
test help_options::ref_attach_source_help_lists_options_alphabetically_and_explains_adoption ... ok
test help_options::highlights_ref_sync_help_lists_options_alphabetically ... ok
test help_options::highlights_create_help_lists_options_alphabetically ... ok
test help_options::freshness_seed_help_lists_options_alphabetically ... ok
test help_options::task_status_hooks_help_lists_options_alphabetically ... ok
test help_options::plugins_sync_help_lists_options_alphabetically ... ok
test help_options::plugins_help_lists_subcommand_and_options ... ok
test help_options::highlights_clip_alias_help_matches_create_help ... ok
test completion::vault::theme_mutations_and_relation_hide_use_their_catalogs ... ok
test dataview_oom::tasks_skips_dataview_index_under_address_space_cap ... ok
test help_options::projects_help_lists_subcommands_and_options ... ok
test highlights::create::highlights_create_arxiv_api_failure_falls_back_with_warning ... ok
test help_options::stats_help_lists_options_alphabetically ... ok
test help::task_status_hooks_help_is_native_only ... ok
test help_options::default_subcommands_are_labeled_in_help ... ok
test highlights::create::highlights_create_clip_alias_is_byte_identical_on_error_path ... ok
test help::highlights_ref_subcommand_help_works ... ok
test highlights::create::highlights_create_bare_force_fresh_url_dry_run_proceeds ... ok
test help::pomodoro_help_documents_show_stale_option ... ok
test highlights::create::highlights_create_article_dry_run_writes_nothing ... ok
test highlights::create::highlights_create_arxiv_dry_run_shows_override_sources ... ok
test highlights::create::highlights_create_clip_alias_rereads_filed_url ... ok
test highlights::continuations::continuation_scan_reports_dangling_marker ... ok
test highlights::create::highlights_create_article_maps_options_to_clip ... ok
test freshness::list_lane_intervals_false_null_and_invalid ... ok
test highlights::create::highlights_create_collection_partial_overlap_with_listen_never_listens ... ok
test completion::lifecycle::install_glyphs_follow_registration ... ok
test highlights::create::highlights_create_collection_overwrite_fresh_set_refuses_before_adapter ... ok
test highlights::continuations::show_exposes_group_pieces_with_seams_and_omits_them_for_singles ... ok
test highlights::create::highlights_create_article_default_target_avoids_ids_in_other_types ... ok
test highlights::create::highlights_create_collection_dry_run_skips_compose_and_writes ... ok
test highlights::create::highlights_create_article_routes_bot_wall_to_adapter ... ok
test highlights::create::highlights_create_collection_listen_dry_run_prints_audio_and_would_run ... ok
test highlights::create::highlights_create_closed_and_plain_require_one_vault_note ... ok
test highlights::create::highlights_create_clip_alias_matches_create_for_force ... ok
test highlights::create::highlights_create_arxiv_uses_api_metadata_and_short_stem ... ok
test highlights::create::highlights_create_collection_dry_run_validates_explicit_audio ... ok
test highlights::create::highlights_create_article_output_stem_becomes_marker_id ... ok
test highlights::create::highlights_create_arxiv_rereads_from_original_source ... ok
test highlights::create::highlights_create_collection_failing_part_writes_nothing ... ok
test highlights::create::highlights_create_dry_run_rejects_unknown_parent_with_hints ... ok
test highlights::create::highlights_create_dry_run_prints_plan_without_writes ... ok
test highlights::create::highlights_create_article_binds_explicit_audio ... ok
test highlights::create::highlights_create_dry_run_reports_planned_audio_copy ... ok
test highlights::create::highlights_create_dry_run_resolves_parent_alias_to_canonical_route ... ok
test highlights::create::highlights_create_arxiv_captures_a_legacy_only_url_note_with_a_warning ... ok
test completion::lifecycle::verify_probe_classifications ... ok
test highlights::create::highlights_create_exact_output_refuses_an_existing_reference_id ... ok
test highlights::create::highlights_create_bare_force_filed_url_rereads ... ok
test highlights::create::highlights_create_article_routes_through_clip_engine ... ok
test dataview_oom::tasks_ignores_dataview_only_page_metadata ... ok
test highlights::create::highlights_create_filed_url_refusal_names_next_reread ... ok
test highlights::create::highlights_create_and_clip_attach_listen_to_the_newest_reading ... ok
test completion::vault::vault_slots_stay_fast ... ok
test highlights::create::highlights_create_force_glued_short_is_output_path_error ... ok
test highlights::create::highlights_create_collection_rejects_invalid_target_lists_before_work ... ok
test highlights::create::highlights_create_collection_listen_post_failure_hint_keeps_all_urls ... ok
test highlights::create::highlights_create_collection_reread_failed_part_writes_nothing ... ok
test highlights::create::highlights_create_collection_listen_failure_leaves_vault_unchanged ... ok
test highlights::create::highlights_create_folded_still_refuses_a_pdf_backed_url_note ... ok
test highlights::create::highlights_create_force_invalid_equals_mode_is_clap_error ... ok
test highlights::create::highlights_create_force_adopted_empty_target_matches_missing_target_usage ... ok
test highlights::create::highlights_create_folded_dry_run_writes_nothing ... ok
test capture::sub_bullet::capture_sub_bullet_lands_before_direct_managed_logs ... ok
test highlights::create::highlights_create_collection_partial_overlap_refuses_under_every_mode ... ok
test completion::capture_text::wikilinks_return_nothing_quickly ... ok
test highlights::create::highlights_create_collection_binds_explicit_audio ... ok
test help::script_fallback_help_is_safe_and_plain ... ok
test highlights::create::highlights_create_force_top_level_option_keeps_explicit_value ... ok
test highlights::create::highlights_create_force_stray_mode_guard_runs_no_adapter_and_writes_nothing ... ok
test freshness::list_decides_on_early_dates ... ok
test highlights::create::highlights_create_force_repeated_flag_is_clap_usage_error ... ok
test highlights::create::highlights_create_folded_rejects_protocol_errors ... ok
test highlights::create::highlights_create_markdown_marker_carries_author_and_published ... ok
test highlights::create::highlights_create_local_pdf_overrides_author_and_published ... ok
test highlights::create::highlights_create_collection_refuses_pdf_parts ... ok
test highlights::create::highlights_create_folded_refuses_library_and_dedupe_collisions_early ... ok
test highlights::continuations::continuation_scan_tucks_two_pages_and_is_idempotent ... ok
test highlights::create::highlights_create_folded_direct_pdf_falls_back_to_slug_title ... ok
test highlights::create::highlights_create_folded_library_without_url_suffixes ... ok
test highlights::create::highlights_create_missing_parent_fails_before_any_work ... ok
test highlights::create::highlights_create_no_audio_skips_discovery ... ok
test highlights::create::highlights_create_output_dry_run_reports_direct_library_target ... ok
test highlights::create::highlights_create_output_existing_pdf_still_refuses_without_force ... ok
test highlights::create::highlights_create_output_dry_run_reports_intake_library_destination ... ok
test highlights::create::highlights_create_html_replay_rereads_without_fetch ... ok
test highlights::create::highlights_create_collection_listens_to_staged_pdf_before_install ... ok
test highlights::create::highlights_create_output_dry_run_prints_exact_path_without_writes ... ok
test highlights::create::highlights_create_local_pdf_dry_run_writes_nothing_and_refuses_junk ... ok
test highlights::create::highlights_create_folded_reports_adapter_failures_with_hints ... ok
test highlights::create::highlights_create_library_pdf_as_target_refuses_reread_with_hint ... ok
test highlights::create::highlights_create_local_pdf_reread_keeps_earlier_bundle_bytes ... ok
test highlights::create::highlights_create_folded_force_overwrites_the_same_intake_target ... ok
test highlights::create::highlights_create_local_pdf_installs_and_stamps ... ok
test highlights::create::highlights_create_overwrite_fresh_url_refuses_before_fetch ... ok
test highlights::create::highlights_create_pdf_url_rejects_claimed_pdf_and_404 ... ok
test highlights::create::highlights_create_folded_success_writes_stamped_intake_pdf ... ok
test help::vault_sync_help_is_native_only_and_defaults_to_run ... ok
test highlights::create::highlights_create_refuses_library_destination_audio ... ok
test highlights::create::highlights_create_local_pdf_title_override_and_name_type_output ... ok
test highlights::create::highlights_create_copies_audio_before_pdf_with_play_link ... ok
test highlights::create::highlights_create_refuses_existing_library_pdf_with_or_without_force ... ok
test highlights::create::highlights_create_rejects_html_with_local_target_before_any_work ... ok
test highlights::create::highlights_create_rejects_conflicting_audio_flags ... ok
test highlights::create::highlights_create_local_pdf_inside_library_is_refused_with_listen_hint ... ok
test highlights::create::highlights_create_rejects_bad_published_before_any_work ... ok
test highlights::create::highlights_create_folded_captures_a_legacy_only_url_note_with_a_warning ... ok
test highlights::create::highlights_create_rejects_output_combined_with_ref_type ... ok
test highlights::create::highlights_create_rejects_non_pdf_output ... ok
test highlights::create::highlights_create_collection_three_parts_derives_title_and_authors ... ok
test highlights::create::highlights_create_refuses_mapped_private_literals_without_fetching ... ok
test highlights::create::highlights_create_rejects_non_utf8_include_id_before_writes ... ok
test highlights::create::highlights_create_overwrite_filed_url_reaches_preflight ... ok
test highlights::create::highlights_create_local_pdf_prepends_marker_and_snake_cases_stem ... ok
test highlights::create::highlights_create_refuses_different_audio_without_force ... ok
test highlights::create::highlights_create_rejects_bad_audio_paths ... ok
test highlights::create::highlights_create_refuses_each_url_in_pdf_backed_frontmatter_lists ... ok
test highlights::create::highlights_create_collection_installs_list_marker_and_scan_finds_each_part ... ok
test highlights::create::highlights_create_reports_pandoc_failure_diagnostics ... ok
test highlights::create::highlights_create_reuses_identical_existing_companion ... ok
test highlights::create::highlights_create_folded_rejects_before_the_adapter_runs ... ok
test highlights::create::highlights_create_pdf_url_colliding_slug_suffixes ... ok
test highlights::create::highlights_create_reread_title_free_name_and_output_guards ... ok
test highlights::create::highlights_create_collection_reread_guards ... ok
test highlights::create::highlights_create_vault_note_dry_run_uses_title_parent_and_fixed_date ... ok
test highlights::create::highlights_create_same_title_library_rereads_from_original_source ... ok
test highlights::create::highlights_create_collection_unrelated_families_ask_for_name ... ok
test highlights::create::landing_bare_library_pdf_renames ... ok
test highlights::create::landing_library_collision_hints_listen_attach ... ok
test highlights::create::landing_name_alone_does_not_embed_marker_id ... ok
test highlights::create::highlights_create_reread_omits_parent_and_overrides_type_status ... ok
test highlights::create::highlights_create_folded_round_trips_through_scan ... ok
test highlights::create::route_guards_overwrite_markdown_exact_output_preparent_probe ... ok
test highlights::create::highlights_create_local_pdf_different_title_suffixes_with_id ... ok
test highlights::create::route_guards_overwrite_pdf_exact_output_tilde_preparent_probe ... ok
test highlights::create::highlights_create_pdf_url_rereads_from_original_source ... ok
test highlights::create::highlights_create_same_stem_different_title_remains_a_new_capture ... ok
test highlights::create::highlights_create_pdf_url_binds_explicit_audio ... ok
test highlights::create::highlights_create_folded_forwards_overrides_and_html ... ok
test highlights::create::highlights_create_reread_url_member_selection_and_rejection ... ok
test highlights::create::route_guards_overwrite_url_exact_output_replaces ... ok
test highlights::create::highlights_create_markdown_renders_outside_xlib ... ok
test highlights::diagrams::highlights_create_definition_list_dry_run_stays_browser_free ... ok
test highlights::create::highlights_create_collection_collision_walk_and_exact_output ... ok
test highlights::create::highlights_create_pdf_url_stamps_and_dedupes ... ok
test highlights::create::highlights_create_vault_note_same_day_rereads ... ok
test highlights::create::highlights_create_url_reread_keeps_earlier_bundle_bytes ... ok
test highlights::create::landing_marked_pdf_outside_vault_is_refused ... ok
test highlights::create::highlights_create_warns_and_proceeds_for_legacy_list_note ... ok
test highlights::create::route_guards_redirect_guard_refuses_outside_family_via_curl ... ok
test completion::vault::completion_is_read_only ... ok
test highlights::create::route_guards_overwrite_collection_exact_output_replaces ... ok
test highlights::create::landing_companion_beside_source_is_copied ... ok
test highlights::create::route_guards_library_pdf_reread_force_listen_refuses ... ok
test highlights::diagrams::highlights_create_mermaid_dry_run_counts_without_starting_tools ... ok
test highlights::create::route_guards_vault_preflight_orders_before_parent ... ok
test highlights::create::highlights_create_reread_listen_narrates_new_reading ... ok
test highlights::create::route_guards_plain_reread_without_audio_has_no_narrated_hint ... ok
test highlights::create::route_guards_redirect_guard_refuses_outside_family_via_adapter ... ok
test highlights::create::highlights_create_plain_vault_note_keeps_snapshot_provenance ... ok
test help::all_top_level_subcommand_help_is_safe_and_plain ... ok
test highlights::create::ingest_characterizes_url_failure_modes ... ok
test highlights::create::highlights_create_folded_supports_ref_type_output_and_name ... ok
test highlights::create::highlights_create_local_pdf_recapture_rereads_after_scan ... ok
test highlights::create::highlights_create_reread_queued_then_scan_files_lineage ... ok
test highlights::create::highlights_create_queued_url_overwrite_replaces ... ok
test highlights::create::highlights_create_stamps_rendered_pdf_through_shared_install ... ok
test highlights::create::highlights_create_retries_without_force_never_mint_readings ... ok
test highlights::create::highlights_create_collection_listen_attaches_to_same_set ... ok
test highlights::create::route_guards_plain_reread_names_narrated_reading_without_inheriting ... ok
test dataview_oom::flatten_later_limit_does_not_hide_default_budget ... ok
test highlights::create::highlights_create_collection_reread_listen_narrates_new_reading ... ok
test highlights::create::highlights_create_folded_doctor_reports_web_clip_rows ... ok
test highlights::create::highlights_create_collection_queued_only_replacement_both_modes ... ok
test help::public_help_surfaces_do_not_list_long_only_options ... ok
test highlights::create::highlights_create_diagram_doctor_warns_without_browser_and_reports_off ... ok
test highlights::doctor_library::doctor_coverage_uses_provenance_mirroring ... ok
test highlights::doctor_library::doctor_annotations_warn_on_leaked_marker_mirror ... ok
test highlights::doctor_library::doctor_intake_last_row_keeps_a_multiline_message_on_one_line ... ok
test highlights::doctor_library::doctor_dangling_earlier_entry_warns ... ok
test highlights::doctor_library::doctor_coverage_warn_counts_unmirrored_zorg_records ... ok
test highlights::doctor_library::doctor_intake_last_row_reads_the_recorded_status ... ok
test highlights::doctor_library::doctor_identity_warn_on_identity_shared_by_two_pdfs ... ok
test highlights::doctor_library::doctor_warns_when_a_queued_pdf_is_over_an_hour_old ... ok
test highlights::image_notes::image_notes_copy_embed_and_snapshot ... ok
test highlights::jobs::ref_jobs_bare_lists_empty_vault_state ... ok
test highlights::doctor_library::doctor_reference_ids_allow_only_a_suffix_that_avoids_a_duplicate ... ok
test highlights::doctor_library::doctor_identity_ok_reports_superseded_legacy_note ... ok
test highlights::doctor_library::doctor_library_diagnostics_warn_lists_codes_and_paths ... ok
test highlights::doctor_library::doctor_ref_sources_warns_on_ignored_catalog ... ok
test highlights::doctor_library::doctor_reference_ids_ok_when_ids_match_stems ... ok
test highlights::jobs::ref_jobs_group_flag_before_jobs_lists ... ok
test highlights::doctor_library::doctor_xlib_row_shows_the_oldest_age_without_warning_when_fresh ... ok
test highlights::doctor_library::doctor_library_rows_report_ok_on_clean_vault ... ok
test highlights::doctor_library::doctor_xlib_rows_stay_plain_when_nothing_is_queued ... ok
test highlights::jobs::ref_jobs_old_created_records_still_render_as_clipped ... ok
test highlights::jobs::ref_jobs_list_shows_the_parent ... ok
test highlights::doctor_library::doctor_ref_sources_warns_on_dangling_mismatch_missing_and_orphan ... ok
test highlights::jobs::ref_jobs_second_worker_exits_zero ... ok
test docs_reference::cli_reference_is_current ... ok
test highlights::jobs::ref_jobs_list_windows_and_json ... ok
test highlights::doctor_library::doctor_reference_ids_warn_on_mismatch_and_case_insensitive_duplicate ... ok
test highlights::create::highlights_create_collection_name_waterfall_is_local_and_options_parse_after_urls ... ok
test highlights::create::highlights_create_collection_post_listen_recheck_keeps_narration ... ok
test capture::related::draft_related_stays_under_the_debug_perf_gate ... ok
test highlights::jobs::ref_jobs_unwritable_running_fails_promptly ... ok
test highlights::jobs::ref_jobs_stale_running_twice_falls_back_without_clipping ... ok
test highlights::jobs::ref_jobs_run_filed_family_never_mints_reread ... ok
test highlights::jobs::ref_jobs_stuck_fallback_is_retried_without_clipping ... ok
test highlights::jobs::ref_jobs_run_uses_job_bob_dir_not_env ... ok
test highlights::create::highlights_create_collection_reread_three_generations ... ok
test highlights::doctor_library::doctor_family_identity_exempt_but_outsider_warns ... ok
test dataview_oom::synthetic_task_census_counts_are_exact ... ok
test highlights::listen::create_article_listen_uses_adapter_render ... ok
test highlights::listen::create_listen_captures_and_binds_episode ... ok
test highlights::jobs::ref_jobs_run_falls_back_on_blocked ... ok
test highlights::jobs::ref_jobs_fallback_bytes_match_capture_twin_vault ... ok
test highlights::image_notes::image_notes_missing_source_warns_then_heals ... ok
test highlights::jobs::ref_jobs_run_falls_back_into_the_staged_parent ... ok
test highlights::jobs::ref_jobs_run_clips_a_seeded_article ... ok
test highlights::jobs::ref_jobs_run_parentless_job_uses_the_source_inbox ... ok
test highlights::ingest::create_rejects_an_invalid_ingest_on_create_env_before_any_write ... ok
test highlights::listen::listen_conflicts_with_audio_and_no_audio ... ok
test highlights::listen::listen_arxiv_offline_renders_via_sase ... ok
test highlights::listen::listen_dry_run_prints_would_run_without_invoking ... ok
test highlights::listen::listen_attach_refuses_when_audio_exists ... ok
test highlights::listen::listen_invalid_template_is_an_error ... ok
test highlights::listen::listen_attaches_to_ref_note_capture ... ok
test highlights::listen::listen_attaches_for_legacy_url_arxiv_note ... ok
test highlights::listen::listen_failure_writes_nothing ... ok
test dataview_oom::synthetic_task_census_stays_under_address_space_cap ... ok
test highlights::listen::listen_dry_run_uses_normalized_launcher ... ok
test highlights::listen::listen_has_no_fallback_when_sase_missing ... ok
test highlights::create::highlights_create_diagram_doctor_warns_when_test_render_fails ... ok
test highlights::jobs::ref_jobs_stale_running_once_is_requeued_and_clipped ... ok
test highlights::listen::listen_unconfigured_fails_before_fetch ... ok
test highlights::listen::listen_interrupted_exits_130 ... ok
test highlights::listen::listen_attaches_to_queued_intake_pdf ... ok
test highlights::listen::listen_post_listen_collision_keeps_scratch ... ok
test highlights::ingest::create_queues_for_non_git_and_other_vaults_without_touching_bob_dir ... ok
test highlights::doctor_library::doctor_ref_sources_ok_counts_saved_code_blocks ... ok
test highlights::listen::listen_plugin_failure_has_no_fallback ... ok
test capture::pomodoro_close::capture_pomodoro_close_links_batches_and_files ... ok
test highlights::listen::listen_legacy_env_migrates_and_preserves_flags ... ok
test highlights::listen::listen_attaches_when_target_is_the_library_pdf ... ok
test highlights::listen::listen_without_audio_is_an_error ... ok
test highlights::listen::listen_literal_values_arrive_intact ... ok
test highlights::listen::listen_refusal_without_flag_points_at_listen ... ok
test highlights::listen::listen_pdf_url_streams_output_and_quotes_title ... ok
test highlights::marker::highlights_ref_marker_uses_first_page_text_annotation ... ok
test highlights::listen::doctor_warns_for_queued_listen_feed_publish ... ok
test help::help_routes_match_direct_help_for_root_and_nested_commands ... ok
test highlights::marker::highlights_ref_doctor_warns_on_missing_latex_packages ... ok
test highlights::marker::highlights_ref_frontmatter_missing_parent_fails_before_pdf_writeback ... ok
test highlights::marker::highlights_ref_comment_edit_keeps_stable_block_id ... ok
test highlights::marker::highlights_ref_deleted_highlight_is_tombstoned ... ok
test highlights::jobs::ref_jobs_run_rejects_an_invalid_ingest_on_create_env_before_xlib_write ... ok
test highlights::listen::listen_legacy_only_hit_captures_fresh_instead_of_attaching ... ok
test highlights::marker::highlights_ref_frontmatter_unsupported_status_fails_before_pdf_writeback ... ok
test highlights::marker::highlights_ref_marker_edit_updates_frontmatter ... ok
test highlights::marker::highlights_ref_rejects_wikilink_marker_parent_before_writes ... ok
test highlights::jobs::ref_jobs_run_queues_when_maintenance_lock_is_held ... ok
test highlights::marker::highlights_ref_short_options_are_accepted ... ok
test highlights::listen::listen_markdown_binds_episode_and_play_uri ... ok
test highlights::listen::listen_queued_publish_warns_after_create_summary ... ok
test highlights::corpus_gate::classifies_file_warnings_against_the_complete_gate ... ok
test highlights::listen::listen_wrappers_and_chains_fail_before_fetch ... ok
test highlights::marker::highlights_ref_conflicting_edits_fail_and_prefer_frontmatter_resolves ... ok
test highlights::marker_write::unattended_scan_holds_editor_active_when_the_probe_says_reading ... ok
test highlights::marker_write::json_unattended_scan_counts_a_hold_as_neither_note_nor_failure ... ok
test highlights::marker_write::attended_scan_bypasses_the_reading_hold ... ok
test highlights::create::highlights_create_collection_rereads_exact_set_reversed ... ok
test highlights::marker_write::verbose_unattended_scan_names_the_reading_hold ... ok
test highlights::marker::highlights_ref_frontmatter_edit_updates_marker_when_pdf_writes_enabled ... ok
test highlights::jobs::ref_jobs_doctor_row_tracks_pending_and_stuck ... ok
test highlights::marker::highlights_ref_non_overlapping_edits_auto_merge_and_settle ... ok
test highlights::marker::highlights_ref_doctor_no_hooks_reports_skipped ... ok
test highlights::marker::highlights_ref_doctor_checks_vault_git_without_writes ... ok
test highlights::marker::highlights_ref_doctor_warns_on_orphan_companion_audio ... ok
test highlights::marker::highlights_ref_doctor_reports_configured_pre_scan_executable ... ok
test dataview_oom::flatten_default_budget_fails_cli_json_and_markdown ... ok
test highlights::marker::highlights_ref_dry_run_and_inspection_do_not_modify_vault_files ... ok
test highlights::marker_write::ref_sync_bypasses_the_reading_hold ... ok
test highlights::marker_write::key_off_scan_ignores_the_reading_probe_and_omits_coordination_header ... ok
test highlights::marker::highlights_ref_deprecated_done_status_migrates_to_read_with_pdf_write ... ok
test highlights::ingest::create_keeps_intake_for_flag_config_env_and_dry_run ... ok
test highlights::ingest::create_rolls_back_pdf_when_birth_task_selection_refuses ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_wildcard_forms ... ok
test highlights::overwrite::writing_create_and_intake_scan_recover_crashed_overwrite ... ok
test highlights::jobs::ref_jobs_run_ingests_into_a_synced_vault ... ok
test completion::zsh_adapter::real_zsh_first_tab_completes ... ok
test highlights::listen::listen_attach_files_queued_pdf_with_companion_audio ... ok
test highlights::overwrite::refusal_leaves_vault_and_intent_unchanged ... ok
test highlights::listen::listen_attach_files_audio_for_a_library_capture ... ok
test highlights::ingest::create_ingests_pdf_audio_note_and_parent_as_one_scoped_pushed_commit ... ok
test highlights::create::highlights_create_lists_earlier_snapshots_and_hints_unread_ready ... ok
test highlights::overwrite_local::free_name_on_title_route_is_still_fresh_for_overwrite ... ok
test highlights::overwrite_local::library_pdf_target_still_refuses_overwrite ... ok
test highlights::listen::doctor_listen_rows_cover_unset_ok_and_invalid ... ok
test highlights::doctor_library::doctor_reference_ids_repair_through_rename_clears_the_row ... ok
test highlights::overwrite_local::local_pdf_overwrite_dry_run_writes_nothing ... ok
test highlights::overwrite_annotated::open_annotation_task_in_highlights_region_refuses_before_host_gate ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_failure_leaves_bytes_unchanged ... ok
test highlights::overwrite_local::local_pdf_overwrite_marker_failure_after_narration_keeps_scratch ... ok
test highlights::overwrite_annotated::coordination_key_on_still_refuses_annotated_overwrite_off_macos ... ok
test highlights::overwrite_annotated::explicit_output_flag_still_wins_on_annotated_targets ... ok
test highlights::create::highlights_create_collection_overwrites_exact_set_with_listen ... ok
test highlights::overwrite_annotated::exact_set_collection_refuses_annotated_target_before_adapter ... ok
test highlights::overwrite_annotated::dirty_inbound_highlight_file_wins_over_annotated_gate ... ok
test highlights::overwrite_annotated::dry_run_previews_annotated_archive_and_writes_nothing ... ok
test highlights::overwrite_recovery::overwrite_recovery_blocks_dry_run_create ... ok
test highlights::overwrite_recovery::overwrite_recovery_reports_pending_in_json_dry_run ... ok
test highlights::overwrite_recovery::overwrite_recovery_keeps_committed_overwrite_on_scan ... ok
test highlights::overwrite_recovery::overwrite_recovery_rolls_back_on_writing_scan ... ok
test highlights::overwrite_recovery::task_move_refuses_while_overwrite_intent_is_pending ... ok
test highlights::create::highlights_create_vault_note_marker_survives_scan_and_sync ... ok
test highlights::overwrite_recovery::overwrite_recovery_reverses_annotated_pdf_move_on_scan ... ok
test highlights::overwrite_local::overwrite_refuses_disabled_ingest_and_unstampable_status_before_render ... ok
test highlights::overwrite_local::bare_local_reread_hints_at_overwrite_on_real_and_dry_runs ... ok
test highlights::overwrite_local::overwrite_refuses_gitignored_sidecar_file_as_dirty_paths ... ok
test highlights::ingest::create_reread_files_inline_with_lineage_and_versioned_task ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_failure_after_narration_keeps_scratch ... ok
test highlights::overwrite_recovery::vault_sync_recovers_a_planted_overwrite_intent ... ok
test highlights::overwrite::overwrite_preserves_task_children_relations_freshness_and_inbound_links ... ok
test highlights::overwrite_local::local_pdf_overwrite_changes_title ... ok
test highlights::overwrite_local::local_pdf_overwrite_replaces_in_place_without_archive ... ok
test highlights::overwrite_local::local_pdf_overwrite_archives_authored_prose ... ok
test highlights::overwrite::unrelated_dirty_and_staged_files_survive_overwrite ... ok
test highlights::overwrite_local::local_pdf_overwrite_keeps_archived_closed_task ... ok
test highlights::overwrite_local::local_pdf_overwrite_preserves_blocked_overlay ... ok
test highlights::overwrite_local::local_pdf_overwrite_audio_extension_replaces_companion ... ok
test highlights::overwrite_local::local_pdf_overwrite_listen_replaces_companion ... ok
test highlights::create::highlights_create_vault_note_dry_run_reports_image_processing ... ok
test highlights::overwrite_web::annotated_web_target_refuses_without_network ... ok
test highlights::overwrite_local::no_force_overwrite_remedy_uses_the_selected_reading ... ok
test highlights::replaced_capture::explicit_sync_holds_in_human_and_dry_run_modes ... ok
test highlights::overwrite::frozen_archive_is_inert_across_list_find_doctor_and_create ... ok
test highlights::overwrite_local::markdown_overwrite_ignored_catalog_warns_and_commits_source ... ok
test highlights::replaced_capture::human_scan_holds_v1_and_v2_before_import_and_continues_other_pdfs ... ok
test highlights::overwrite_local::overwrite_kept_closed_task_reports_reopen_hint_inline ... ok
test highlights::scan::highlights_ref_scan_allows_duplicate_basenames_in_different_ref_types ... ok
test highlights::scan::highlights_ref_scan_default_output_reports_inline_errors ... ok
test highlights::scan::highlights_ref_scan_detects_same_target_collision_before_writing ... ok
test highlights::scan::highlights_ref_scan_dry_run_previews_xlib_intake_without_writes ... ok
test highlights::scan::highlights_ref_scan_dry_run_reports_valid_and_invalid_pdfs ... ok
test highlights::replaced_capture::json_scan_checks_all_archives_and_keeps_dry_run_holds_as_previews ... ok
test highlights::overwrite_web::web_overwrite_refuses_disabled_ingest_before_dry_run_or_network ... ok
test highlights::overwrite_web::web_overwrite_dry_run_writes_nothing_without_network ... ok
test highlights::overwrite_local::markdown_overwrite_uses_fake_pandoc_and_skips_it_on_dry_run ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_pdf_and_writes_note_in_same_run ... ok
test highlights::scan::highlights_ref_scan_refuses_audio_destination_conflict ... ok
test highlights::overwrite_local::overwrite_without_title_change_keeps_task_file_byte_identical ... ok
test highlights::overwrite_local::overwrite_preserves_custom_task_alias ... ok
test highlights::overwrite_local::overwrite_reports_final_state_and_commit ... ok
test highlights::scan::highlights_ref_scan_refuses_xlib_intake_conflict_before_writes ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_sidecars_with_pdfs ... ok
test highlights::scan::highlights_ref_scan_intakes_pdf_and_mp3_and_embeds_player ... ok
test highlights::scan::highlights_ref_scan_jobs_flag_matches_sequential_output ... ok
test highlights::overwrite_local::overwrite_refuses_incompatible_flags_without_writing ... ok
test highlights::scan::highlights_ref_scan_treats_later_page_note_as_missing_marker ... ok
test highlights::overwrite_local::overwrite_carries_aliases_topics_and_research ... ok
test highlights::scan::ref_scan_human_dry_run_ignores_maintenance_lock ... ok
test highlights::overwrite_web::web_overwrite_redirect_to_other_family_refuses ... ok
test highlights::scan::ref_scan_human_lock_busy_when_maintenance_lock_held ... ok
test highlights::scan::ref_scan_human_hard_failure_writes_error_receipt ... ok
test highlights::scan::ref_scan_human_scan_busy_when_writer_lock_held ... ok
test highlights::scan::highlights_ref_scan_late_pairs_audio_onto_existing_note ... ok
test highlights::scan::ref_scan_json_dry_run_ignores_maintenance_lock ... ok
test highlights::scan::ref_scan_json_dry_run_ignores_writer_lock ... ok
test highlights::scan::ref_scan_json_dry_run_plans_intake_without_writing ... ok
test highlights::overwrite_local::local_pdf_overwrite_selected_older_reading ... ok
test highlights::scan::ref_scan_json_dry_run_writes_no_receipt ... ok
test highlights::scan::ref_scan_json_hard_failure_writes_error_receipt ... ok
test highlights::overwrite_web::bare_web_reread_hints_at_dry_run ... ok
test highlights::scan::ref_scan_json_lock_busy_when_maintenance_lock_held ... ok
test highlights::scan::highlights_ref_scan_writes_valid_pdfs_despite_invalid_pdf ... ok
test highlights::scan::ref_scan_human_scan_writes_equivalent_receipt ... ok
test highlights::scan::ref_scan_json_lock_busy_writes_no_receipt ... ok
test highlights::scan::highlights_ref_scan_groups_routed_tasks_with_parallel_jobs ... ok
test highlights::scan::ref_scan_json_scan_busy_when_writer_lock_held ... ok
test highlights::scan::ref_scan_default_destination_exemption_is_not_shared_with_explicit_route ... ok
test highlights::scan::ref_scan_holds_every_plan_rejecting_a_shared_dirty_route ... ok
test highlights::scan::highlights_ref_scan_round_trips_provenance_marker_fields ... ok
test highlights::scan::ref_scan_json_receipt_failure_only_warns ... ok
test highlights::scan::highlights_ref_scan_default_output_is_concise ... ok
test highlights::scan::ref_scan_json_receipt_matches_stdout ... ok
test highlights::scan_hooks::highlights_ref_scan_dry_run_reports_env_pre_scan_without_executing ... ok
test highlights::scan::ref_scan_writes_when_maintenance_lock_is_free ... ok
test highlights::scan::highlights_ref_scan_recurses_dry_runs_and_writes_multiple_pdfs ... ok
test highlights::scan_hooks::highlights_ref_scan_fails_when_pre_scan_hook_fails ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_command_key ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_env ... ok
test highlights::scan::ref_sync_writes_no_receipt ... ok
test highlights::scan_hooks::highlights_ref_scan_empty_env_disables_configured_pre_scan ... ok
test highlights::overwrite_web::arxiv_overwrite_keeps_api_metadata ... ok
test highlights::overwrite::leftover_committed_intent_then_second_overwrite_of_same_stem ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_after_subcommand_skips_configured_hook ... ok
test highlights::scan_hooks::highlights_ref_scan_hook_child_sees_in_hook_marker ... ok
test highlights::scan_hooks::ref_scan_json_hook_failure_error_envelope ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_before_subcommand_skips_configured_hook ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_overrides_env_hook ... ok
test highlights::scan::ref_scan_json_intake_lists_pdf_only_when_audio_moves_alone ... ok
test highlights::scan::highlights_ref_scan_stamps_created_on_category_and_intake_notes ... ok
test highlights::scan::ref_scan_json_partial_failure_reports_pdf_stage_and_message ... ok
test highlights::scan_hooks::highlights_ref_scan_runs_configured_pre_scan_before_xlib_intake ... ok
test highlights::scan_hooks::ref_scan_json_hook_stdout_reaches_stderr_not_stdout ... ok
test highlights::scan::ref_scan_json_success_envelope_names_created_and_updated_notes ... ok
test highlights::scan::ref_scan_json_marker_write_direct_with_status_change ... ok
test highlights::scan::ref_scan_json_dirty_note_is_a_successful_hold ... ok
test highlights::overwrite_web::article_overwrite_replaces_filed_reference ... ok
test highlights::overwrite_local::vault_note_same_day_overwrite_plain_markdown ... ok
test highlights::scan::ref_scan_json_holds_dirty_pdf_and_writes_clean_independent_pdf ... ok
test highlights::scan_intake::intake_only_empty_queue_writes_no_receipt ... ok
test highlights::overwrite_web::saved_html_overwrite_replays_without_fetch ... ok
test highlights::overwrite_web::pdf_url_overwrite_clears_source_markdown ... ok
test highlights::overwrite_local::overwrite_root_without_title_change_adds_no_version_suffix ... ok
test highlights::overwrite_web::pdf_url_overwrite_stamps_fetched_pdf ... ok
test highlights::scan_intake::intake_only_conflicts_with_write_pdfs ... ok
test highlights::overwrite_local::local_pdf_overwrite_preserves_wip_and_explicit_ready ... ok
test highlights::scan_intake::full_scan_aborts_before_moving_any_queued_reread_with_an_occupant ... ok
test highlights::overwrite_annotated::linux_refuses_each_annotation_kind_before_render_and_leaves_vault ... ok
test highlights::scan_integration::v2_adoption_reports_neither_created_nor_updated ... ok
test highlights::scan_intake::intake_only_leaves_a_library_pdf_without_a_note_alone ... ok
test highlights::overwrite_web::web_overwrite_rollback_removes_new_store ... ok
test highlights::scan_intake::full_scan_files_queued_reread_with_lineage ... ok
test highlights::scan_integration::v2_alias_parent_resolves_to_canonical_residence ... ok
test highlights::overwrite::no_prose_overwrite_removes_each_sidecar_shape_and_stays_stable ... ok
test highlights::scan_intake::intake_only_fails_with_lock_busy_when_work_waits_behind_the_lock ... ok
test highlights::scan_intake::intake_only_dry_run_previews_without_locks_or_writes ... ok
test highlights::overwrite_web::pdf_link_annotations_for_navigation_and_audio_do_not_refuse ... ok
test highlights::scan_integration::v2_ambiguity_leaves_bytes_unchanged_with_pdf_writes ... ok
test highlights::scan_integration::v2_concise_scan_flags_open_v1_with_migrate_hint ... ok
test highlights::overwrite_local::pdf_overwrite_clears_source_markdown ... ok
test highlights::scan_intake::intake_only_with_an_empty_queue_takes_no_lock_and_exits_zero ... ok
test highlights::scan_integration::v2_birth_honors_configured_ref_dir ... ok
test highlights::scan_intake::intake_only_preview_reports_a_queued_reread_occupant ... ok
test highlights::scan_integration::v2_birth_without_tasks_heading_creates_section ... ok
test highlights::scan_integration::v2_dry_run_writes_nothing ... ok
test highlights::overwrite::two_same_day_prose_overwrites_keep_distinct_archives_and_family ... ok
test highlights::scan_integration::v2_destination_collision_suffixes_preview_id ... ok
test highlights::scan_intake::intake_only_json_dry_run_lists_would_queue_items_with_ok_true ... ok
test highlights::scan_integration::v2_archive_reopen_inserts_fresh_task_with_suffixed_id ... ok
test highlights::scan_intake::intake_only_hard_fails_when_pre_sync_cannot_pull ... ok
test highlights::scan_integration::v2_fallback_parent_uses_inbox_with_warning ... ok
test highlights::scan_integration::v2_deleted_managed_embed_heals_without_new_task ... ok
test highlights::scan_integration::v2_orphan_recovery_adopts_existing_task ... ok
test highlights::scan_intake::intake_only_files_version_looking_pdf_without_predecessor_as_ordinary ... ok
test highlights::scan_integration::v2_json_scan_reports_births_without_human_lines ... ok
test highlights::scan_integration::v2_archive_move_dedups_follow_up ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_creations ... ok
test highlights::scan_integration::v2_parallel_matches_sequential ... ok
test highlights::scan_integration::v2_missing_task_never_gains_automatic_replacement ... ok
test highlights::scan_integration::v2_failed_pdf_does_not_consume_sibling_follow_up ... ok
test highlights::scan_integration::v2_moved_task_residence_heals_embed ... ok
test highlights::scan_integration::v2_multiple_open_tasks_refuse_replacement ... ok
test highlights::scan_integration::v2_dirty_parent_accepts_default_follow_up ... ok
test highlights::scan::highlights_ref_scan_continues_after_write_failure ... ok
test highlights::scan_integration::v2_sidecar_free_birth_pins_created_date ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_updates ... ok
test highlights::scan_integration::v2_parent_move_settles_without_pdf_opt_in ... ok
test highlights::scan_integration::v2_ready_parent_accepts_default_follow_up ... ok
test highlights::scan_integration::v2_single_pdf_report_names_performed_reading_write ... ok
test highlights::scan_integration::v2_same_stem_in_two_categories_stays_distinct ... ok
test highlights::scan_integration::v2_lifecycle_needs_opt_in_and_settles_on_rerun ... ok
test highlights::scan_integration::v2_opt_in_refreshes_stale_marker_hint ... ok
test highlights::scan_intake::intake_only_files_queued_reread_with_lineage_and_stable_second_scan ... ok
test highlights::scan_intake::intake_status_records_a_writing_full_scan_but_not_a_dry_run ... ok
test highlights::overwrite_web::web_overwrite_listen_narrates_replacement ... ok
test highlights::stale_save::dry_run_previews_the_stale_restore ... ok
test highlights::scan_intake::intake_only_preserves_version_in_long_stem_task_ids ... ok
test highlights::scan_intake::intake_only_human_drain_writes_receipt ... ok
test highlights::stale_save::v1_stale_save_keeps_next_lane_and_restores_marker ... ok
test highlights::scan_integration::v2_two_births_share_one_parent_and_settle ... ok
test highlights::sync::highlights_ref_sync_dry_run_reads_literal_marker_newlines ... ok
test highlights::overwrite_local::overwrite_title_change_keeps_old_version_suffix ... ok
test highlights::stale_save::replaced_hash_drops_on_a_note_write_that_observes_agreement ... ok
test highlights::stale_save::no_write_pdfs_skips_restore_alone_without_refusal ... ok
test highlights::stale_save::genuine_marker_edit_is_still_adopted ... ok
test highlights::scan_intake::intake_status_records_a_queued_drain_as_a_failure ... ok
test highlights::stale_save::json_marker_write_restored_is_true_for_a_stale_save ... ok
test highlights::stale_save::missing_replaced_hash_disables_the_guard ... ok
test highlights::sync::highlights_ref_sync_maps_relative_pdf_paths_through_a_symlinked_vault ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_parent_without_note_write ... ok
test highlights::stale_save::v2_gesture_during_stale_save_applies_without_conflict ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_status_without_note_write ... ok
test highlights::overwrite_local::overwrite_same_stem_source_selects_named_member ... ok
test highlights::overwrite_web::web_overwrite_selects_older_member_with_name ... ok
test highlights::stale_save::v2_stale_save_does_not_reopen_a_finished_task ... ok
test highlights::sync::highlights_ref_sync_rejects_unsupported_marker_status_without_note_write ... ok
test highlights::stale_save::v2_stale_save_keeps_next_lane_and_restores_marker ... ok
test highlights::overwrite_local::overwrite_refuses_all_remaining_preflight_codes_without_writing ... ok
test highlights::scan_intake::intake_only_drains_a_queued_pdf_into_one_pushed_commit ... ok
test highlights::sync::highlights_ref_sync_resolves_relative_library_pdf_paths_before_mapping ... ok
test highlights::sync::highlights_ref_sync_preserves_legacy_research_frontmatter ... ok
test highlights::overwrite_web::web_overwrite_without_source_view_clears_pointer ... ok
test highlights::scan_intake::intake_only_json_drain_writes_matching_receipt ... ok
test highlights::sync_tasks::highlights_ref_sync_missing_routed_target_fails_before_writes ... ok
test highlights::store_gaps::store_dry_run_prints_planned_pointer_and_writes_nothing ... ok
test highlights::sync_tasks::highlights_ref_sync_beautifies_linked_sidecar_rendering ... ok
test highlights::sync::highlights_ref_sync_rejects_malformed_and_duplicate_marker_lists ... ok
test highlights::sync::highlights_ref_sync_sets_created_timestamp_on_new_sidecar_free_note ... ok
test highlights::sync::highlights_ref_sync_creates_note_frontmatter_from_marker_pdf_note ... ok
test highlights::sync::highlights_ref_sync_stamps_cancellation_date_when_it_cancels_ref_task ... ok
test highlights::sync::highlights_ref_sync_refuses_dirty_target_note_before_writing ... ok
test highlights::sync_tasks::highlights_ref_sync_keeps_created_fixed_across_sidecar_updates ... ok
test highlights::sync_tasks::highlights_ref_sync_creates_tasks_from_pdf_note_task_bullets ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_vault_scan_when_no_annotation_candidates ... ok
test highlights::scan_intake::intake_only_attaches_audio_to_an_existing_reread ... ok
test highlights::sync::highlights_ref_sync_preserves_authored_created_and_rejects_marker_created ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_legacy_highlight_task_property ... ok
test highlights::sync_tasks::highlights_ref_sync_creates_annotation_tasks_for_open_statuses ... ok
test highlights::sync_tasks::highlights_ref_sync_supports_linked_sidecar_style ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_sidecar_highlights_and_notes ... ok
test highlights::overwrite_web::every_annotation_source_refuses_with_the_contract_remedy ... ok
test highlights::sync_tasks::highlights_ref_sync_drops_leaked_mirror_without_tombstone ... ok
test highlights::store_gaps::store_output_outside_library_writes_no_store ... ok
test highlights::sync_tasks::highlights_ref_sync_preserves_manual_sections_and_rejects_missing_markers ... ok
test highlights::sync_tasks::highlights_ref_sync_drops_color_grouped_mirror_without_tombstone ... ok
test highlights::url_routing::url_routing_duplicate_refuses_before_missing_parent ... ok
test highlights::sync::highlights_ref_sync_allows_dirty_tracked_frontmatter_writeback ... ok
test highlights::url_routing::url_routing_in_library_matches_create_refusal ... ok
test highlights::url_routing::url_routing_in_intake_matches_create_refusal ... ok
test highlights::underlines::standalone_underline_reason_appears_in_sync_and_scan_json ... ok
test highlights::url_routing::url_routing_legacy_matches_create_warning ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_textbundle_image_selections ... ok
test highlights::tasks::highlights_ref_task_cancelled_competing_status_edits_fail ... ok
test highlights::tasks::highlights_ref_task_checked_competing_status_edits_fail ... ok
test highlights::tasks::highlights_ref_task_cancelled_scan_write_pdfs_writes_pdf_marker ... ok
test highlights::sync_tasks::highlights_ref_sync_routes_annotation_tasks_to_existing_root_note ... ok
test highlights::scan_intake::intake_only_attaches_late_audio_to_a_library_pdf ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_annotation_tasks_for_terminal_statuses ... ok
test move_done::move_done_tasks_moves_canceled_tasks_in_non_repo_vault ... ok
test highlights::overwrite_local::markdown_overwrite_repoints_and_reuses_unchanged_bytes ... ok
test highlights::create::highlights_create_output_renders_pdf_at_requested_path_when_available ... ok
test highlights::tasks::highlights_ref_status_abandoned_rewrites_generated_task_to_cancelled ... ok
test highlights::tasks::highlights_ref_task_checked_sync_imports_ready_annotation_tasks_before_closing ... ok
test highlights::tasks::highlights_ref_task_checked_scan_creates_annotation_tasks_before_closing ... ok
test highlights::tasks::highlights_ref_task_checked_dirty_tracked_note_is_allowed ... ok
test highlights::create::highlights_create_markdown_text_layer_avoids_hyphen_splits_and_ligatures ... ok
test highlights::tasks::highlights_ref_blocked_task_syncs_as_status_neutral_overlay ... ok
test move_done::move_done_tasks_rewrites_stayed_pathless_links_in_archive ... ok
test highlights::sync::highlights_ref_sync_stamps_completion_date_when_it_closes_ref_task ... ok
test move_done::move_done_tasks_warns_and_skips_git_for_non_repo_vault ... ok
test highlights::tasks::highlights_ref_task_checked_sync_creates_annotation_tasks_before_closing ... ok
test plan::plan_help_lists_options_alphabetically ... ok
test highlights::scan_intake::intake_only_files_each_queued_pdf_in_its_own_commit ... ok
test plan::plan_human_shows_derived_chip_for_unnamed_entry ... ok
test plan::plan_counts_only_visible_lane_tasks ... ok
test highlights::tasks::highlights_ref_task_cancelled_dry_run_requires_and_writes_pdf_marker ... ok
test plan::plan_loads_a_config_that_still_has_max_now ... ok
test plan::plan_placeholder_only_section_shows_daily_file ... ok
test plan::plan_json_entries_include_derived_project_homes ... ok
test highlights::tasks::highlights_ref_task_ready_scan_reopens_read_ref_to_ready ... ok
test plan::plan_rejects_invalid_config_with_exit_2 ... ok
test plan::plan_reports_lane_over_cap_without_changing_status ... ok
test highlights::underlines::underline_scan_merges_comment_and_stays_idempotent ... ok
test plan::plan_reports_over_cap_with_lints ... ok
test plan::plan_without_pomodoros_section_still_shows_lanes ... ok
test plan::plan_reports_full_budget_as_json ... ok
test plan::plan_reports_human_budget_without_ansi_when_piped ... ok
test highlights::scan_intake::intake_only_json_reports_filed_notes_and_queued_items ... ok
test plan::plan_without_daily_note_still_shows_today_zero_and_lanes ... ok
test plugins::plugins_default_subcommand_runs_list ... ok
test highlights::url_routing::url_routing_doctor_prints_routing_row ... ok
test plan::plan_lints_unconfigured_theme_and_invalid_themes_block ... ok
test plugins::plugins_list_json_is_machine_readable ... ok
test plugins::plugins_list_unreadable_repo_reports_error ... ok
test plugins::plugins_list_renders_table_and_summary ... ok
test highlights::scan_intake::intake_only_queues_late_audio_when_the_marker_needs_a_pdf_write ... ok
test plugins::plugins_sync_backs_up_overwritten_file ... ok
test plugins::plugins_sync_json_reports_errors_as_object ... ok
test highlights::overwrite_web::web_collection_overwrite_repoints_new_bytes ... ok
test move_done::move_done_tasks_commits_and_pushes_collection_changes_only ... ok
test move_done::move_done_tasks_commits_metadata_only_source_updates ... ok
test highlights::overwrite_local::local_pdf_overwrite_keeps_and_replaces_audio ... ok
test move_done::move_done_tasks_commits_link_repairs_with_collection_changes ... ok
test move_done::move_done_tasks_commits_metadata_only_archive_repairs ... ok
test pomodoro::pomodoro_accepts_legacy_unbolded_inline_duration_field_in_time_range ... ok
test pomodoro::pomodoro_formats_native_pomodoro_status ... ok
test highlights::tasks::highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker ... ok
test move_done::move_done_tasks_deduplicates_archive_block_ids_and_repairs_links ... ok
test highlights::overwrite_web::web_overwrite_frozen_note_keeps_old_pointer ... ok
test move_done::move_done_tasks_rewrites_dirty_candidate_files ... ok
test pomodoro::pomodoro_named_session_skips_home_resolution ... ok
test pomodoro::pomodoro_missing_day_file_is_a_successful_noop ... ok
test pomodoro::pomodoro_prints_derived_chip_for_unnamed_linked_session ... ok
test pomodoro::pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test pomodoro::pomodoro_unnamed_unlinked_session_prints_range_only ... ok
test move_done::move_done_tasks_rewrites_dirty_link_repair_files ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_archive ... ok
test plugins::plugins_sync_dry_run_json_writes_nothing ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_source ... ok
test plugins::plugins_sync_dry_run_reports_without_writing ... ok
test pomodoro::tmux_pomodoro_appends_named_budget_meter ... ok
test pomodoro::tmux_pomodoro_omits_meter_without_pomodoros_section ... ok
test pomodoro::tmux_pomodoro_formats_native_pomodoro_status ... ok
test plugins::plugins_sync_single_plugin_copies_only_that_plugin ... ok
test pomodoro::tmux_pomodoro_prints_derived_chip_for_unnamed_linked_session ... ok
test plugins::plugins_sync_preserves_runtime_data_json ... ok
test projects::list::projects_list_ignores_leftover_rollup_key ... ok
test plugins::plugins_list_and_json_report_uncommitted_deployment ... ok
test projects::list::projects_list_reports_invalid_and_duplicate_inline_prj_scheduled ... ok
test pomodoro::tmux_pomodoro_reverses_over_cap_meter ... ok
test plugins::plugins_sync_json_reports_file_actions ... ok
test projects::list::projects_list_reports_prj_errors_without_aborting_scan ... ok
test projects::list::projects_list_scans_project_notes_and_renders_counts ... ok
test highlights::scan_intake::intake_only_refuses_fabricated_reread_occupants_and_recovers ... ok
test highlights::scan_intake::intake_only_queues_a_stem_taken_by_a_peer_and_exits_nonzero ... ok
test projects::schedule::projects_schedule_errors_are_per_file_and_leave_invalid_file_untouched ... ok
test projects::sync::projects_sync_does_not_hoist_without_open_prj ... ok
test projects::schedule::projects_sync_shows_sole_prj_task_when_schedule_is_due ... ok
test projects::sync::projects_sync_keeps_pruned_closed_entries_gone ... ok
test projects::schedule::projects_sync_surfaces_due_scheduled_project_with_only_closed_tasks ... ok
test projects::sync::projects_sync_marks_canceled_subproject_same_run ... ok
test projects::sync::projects_sync_normalizes_mangled_subprojects_line ... ok
test projects::sync::projects_sync_preserves_user_sub_bullets_and_inserts_subprojects_line ... ok
test projects::schedule::projects_sync_propagates_scheduled_task_properties_at_date_boundary ... ok
test projects::sync::projects_sync_reports_prj_errors_without_aborting_scan ... ok
test plugins::plugins_sync_explicit_repo_from_foreign_checkout_is_allowed ... ok
test projects::sync::projects_sync_subproject_line_dry_run_reports_without_writing ... ok
test projects::sync::projects_sync_treats_children_without_open_prj_as_childless ... ok
test projects::sync::projects_sync_reopens_parent_ledger_when_child_prj_is_reopened_same_run ... ok
test projects::sync::projects_sync_orders_open_then_closed_subprojects_in_one_run ... ok
test pomodoro::pomodoro_show_stale_keeps_no_open_day_empty ... ok
test projects::sync::projects_sync_hides_parent_projects_with_open_subprojects ... ok
test pomodoro::script_pomodoro_accepts_inline_duration_field_in_time_range ... ok
test projects::sync::projects_sync_unhides_parent_when_child_prj_is_checked_same_run ... ok
test ready::cap_preview_rejects_out_of_range_values ... ok
test ready::overview_all_clear_reports_room ... ok
test pomodoro::script_pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test plugins::plugins_sync_git_vault_requires_ignored_stamp ... ok
test plugins::plugins_sync_refuses_dirty_vault_file_then_forces ... ok
test ready::ready_help_documents_usage_options_and_environment ... ok
test ready::cap_preview_replaces_only_the_default ... ok
test pomodoro::script_pomodoro_accepts_legacy_unbolded_time_range ... ok
test ready::overview_all_expands_room_empty_and_lints ... ok
test projects::sync::projects_sync_reconciles_future_subproject_markers_at_date_boundary ... ok
test ready::ready_rejects_invalid_config_with_exit_2 ... ok
test plugins::plugins_sync_bare_from_resolved_checkout_is_allowed ... ok
test ready::overview_human_has_sections_order_and_no_ansi ... ok
test ready::overview_json_reports_totals_and_order ... ok
test highlights::create::highlights_create_reports_paired_links_and_dead_warnings_when_available ... ok
test ready::worklist_lists_file_order_with_also_here ... ok
test ready::worklist_json_carries_tasks_and_also ... ok
test plugins::plugins_list_no_pull_uses_existing_checkout ... ok
test highlights::web_source_store::web_article_exact_output_saves_nothing ... ok
test pomodoro::pomodoro_worked_reports_closed_ledger_total_only_when_status_is_empty ... ok
test highlights::diagrams::highlights_create_without_mermaid_does_not_spawn_stub ... ok
test plugins::plugins_list_json_stdout_stays_machine_readable_after_pull ... ok
test plugins::plugins_sync_bare_from_unrelated_cwd_is_allowed ... ok
test projects::sync::projects_sync_updates_status_prj_hide_tag_warns_and_is_idempotent ... ok
test ref_library::attach::attach_keeps_missing_search_path_as_a_usage_error ... ok
test ready::check_exits_3_when_crowded_and_0_when_clear ... ok
test highlights::store_gaps::store_rename_keeps_pointer_and_store_directory ... ok
test plugins::plugins_list_pulls_repo_before_analysis ... ok
test highlights::create::highlights_create_renders_pdf_with_outline_and_marker_when_available ... ok
test ready::overview_human_always_advertises_task_card_keys ... ok
test highlights::store_gaps::store_plain_note_create_records_plain_route_with_source_note ... ok
test plugins::plugins_sync_bare_from_foreign_checkout_refuses_before_pull_or_copy ... ok
test highlights::store_gaps::store_write_failure_warns_and_files_without_pointer ... ok
test highlights::scan_intake::intake_status_records_drain_success_and_doctor_shows_it ... ok
test highlights::store_gaps::store_ignored_catalog_warns_but_files_reference ... ok
test ready::worklist_rejects_ambiguous_unknown_and_untyped_notes ... ok
test ref_library::code::code_human_output_groups_sections_and_hints_shortest_ref ... ok
test ref_library::code::code_json_golden_pins_envelope_and_block_fields ... ok
test ref_library::code::code_fenced_uses_longer_fence_for_backtick_runs ... ok
test ready::worklist_resolves_paths_stems_and_case ... ok
test plugins::plugins_sync_clean_landing_reconciles_then_updates ... ok
test ref_library::code::code_raw_bytes_match_exact_block_text ... ok
test ref_library::code::code_summaries_skip_noise_and_read_mermaid_frontmatter ... ok
test plugins::plugins_sync_pulls_repo_before_copying ... ok
test highlights::store_gaps::store_markdown_create_records_route_and_pointer ... ok
test ref_library::find::find_family_plus_unrelated_duplicate_still_warns ... ok
test ref_library::code::code_page_filter_keeps_spanning_blocks ... ok
test ref_library::code::code_source_prints_exact_bytes_and_rejects_combinations ... ok
test ref_library::find::find_doi_and_arxiv_doi_queries ... ok
test ref_library::find::find_batch_from_stdin_keeps_order_and_duplicates ... ok
test ref_library::find::find_go_link_keys_stay_opaque ... ok
test pomodoro::pomodoro_stale_cutoff_is_empty_unless_requested ... ok
test ref_library::find::find_human_blocks_carry_chips_and_footnotes ... ok
test ref_library::code::code_non_json_exits_cover_statuses_and_errors ... ok
test ref_library::find::find_intake_unavailable_without_intake_dir ... ok
test plugins::plugins_sync_refuses_dirty_deploy_from_another_checkout ... ok
test highlights::web_source_store::web_article_create_without_source_view_files_without_pointer ... ok
test ref_library::find::find_conflict_and_unknown_states ... ok
test ref_library::code::code_all_six_statuses_in_json ... ok
test ref_library::find::find_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::find::find_missing_ref_dir_fails_in_both_formats ... ok
test ref_library::find::find_intake_hit_with_marker_pdf ... ok
test ref_library::find::find_natural_versioned_stem_forms_no_family ... ok
test ref_library::find::find_markdown_table_and_coverage_line ... ok
test ref_library::find::find_intake_list_marker_indexes_each_url ... ok
test ref_library::find::find_intake_records_both_marker_url_fields ... ok
test ref_library::find::find_medium_twins_are_one_identity ... ok
test ref_library::find::find_ranks_the_newest_reading_first_with_reason_aware_also ... ok
test ref_library::find::find_not_found_still_exits_zero ... ok
test ref_library::links::links_human_output_groups_sections_and_hints_shortest_ref ... ok
test ref_library::find::find_path_source_pdf_stem_and_id_queries ... ok
test ref_library::links::links_json_golden_pins_envelope_and_computed_fields ... ok
test ref_library::find::find_pending_sync_marks_status_with_footnote ... ok
test ref_library::find::find_url_variants_share_one_identity ... ok
test ref_library::find::find_title_exact_and_title_candidates ... ok
test ref_library::find::find_min_score_filters_title_candidates ... ok
test ref_library::find::find_www_and_slash_variants_with_superseded_secondary ... ok
test ref_library::links::links_markdown_n_and_list_with_escaping ... ok
test ref_library::find::find_rows_carry_blocked ... ok
test ref_library::links::links_raw_bytes_match_exact_url_without_newline ... ok
test ref_library::links::links_page_filter_keeps_exact_page ... ok
test ref_library::list::list_family_json_carries_reading_and_earlier ... ok
test ref_library::list::list_git_dates_without_git_warns_and_continues ... ok
test ref_library::list::list_family_rows_wear_reading_chips ... ok
test ref_library::find::find_alias_matches_canonical ... ok
test ref_library::list::list_empty_views_say_so ... ok
test ref_library::list::list_json_always_exposes_added_at_without_git_dates ... ok
test ref_library::list::list_git_births_follow_renames_for_v1_and_v2_rows ... ok
test ref_library::list::list_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::find::find_leaves_the_vault_untouched ... ok
test ref_library::links::links_non_json_exits_cover_statuses_and_errors ... ok
test ref_library::list::list_hides_superseded_notes_everywhere ... ok
test ref_library::find::find_slug_fallback_for_url_miss ... ok
test ref_library::list::list_missing_ref_dir_fails_like_find ... ok
test ref_library::list::list_rows_carry_always_present_blocked ... ok
test ref_library::list::list_git_dates_backfills_modern_notes_only ... ok
test ref_library::list::list_markdown_covers_dropped_rows ... ok
test ref_library::list::list_human_rows_align_dated_and_undated_columns ... ok
test highlights::overwrite_web::web_overwrite_repoints_and_reuses_unchanged_bytes ... ok
test ref_library::migrate_tasks::help_lists_options_alphabetically ... ok
test aliases::reconcile_aliases_match_canonical_dry_run_json_and_live_write ... ok
test ref_library::links::links_all_seven_statuses_in_json ... ok
test ref_library::list::list_legacy_collapse_versus_status_filter ... ok
test ref_library::migrate_tasks::ambiguous_bare_stem_left_unchanged ... ok
test highlights::diagrams::highlights_create_mermaid_kill_switch_skips_stub_and_prints_source ... ok
test ref_library::list::list_orders_states_era_status_dates_and_titles ... ok
test ref_library::list::list_default_view_is_the_queue_in_every_format ... ok
test ref_library::find::find_json_envelope_is_stable_and_honest ... ok
test ref_library::list::list_limit_all_and_truncation ... ok
test ref_library::list::list_unknown_and_conflict_states ... ok
test ref_library::migrate_zorg::invariant_note_chapter_skipped_equals_doctor_count ... ok
test ref_library::migrate_zorg::shared_block_pair_stays_distinct_under_provenance ... ok
test ref_library::migrate_zorg::book_folds_lid_and_book_tied_chapters ... ok
test ref_library::migrate_tasks::tsv_round_trip_with_comments_and_extra_columns ... ok
test ref_library::list::list_since_filters_by_row_date ... ok
test highlights::web_source_store::web_article_queued_create_birth_adopts_store ... ok
test ref_library::migrate_zorg::book_without_chapters_stays_unknown_and_strays_skip ... ok
test ref_library::list::list_leaves_the_vault_untouched ... ok
test ref_library::migrate_tasks::closed_and_legacy_notes_unchanged ... ok
test ref_library::migrate_zorg::write_refuses_dirty_zorg_with_nothing_written ... ok
test ref_library::migrate_zorg::write_blocked_hub_dir_fails_clean_with_nothing_committed ... ok
test ref_library::migrate_zorg::write_refuses_non_git_vault ... ok
test highlights::diagrams::highlights_create_renders_mermaid_via_stub_adapter ... ok
test ref_library::migrate_zorg::stem_collisions_rename_against_vault_and_same_run ... ok
test ref_library::migrate_zorg::multi_url_and_unusable_url_records ... ok
test ref_library::migrate_tasks::marks_preserve_fields_and_links ... ok
test ref_library::migrate_zorg::dry_run_plans_one_plain_record ... ok
test highlights::jobs::ref_jobs_slow_clip_still_drains_a_late_job ... ok
test ref_library::recatalog::recatalog_uses_snapshot_reader_for_snapshot_sources ... ok
test ref_library::migrate_tasks::second_write_is_noop_and_non_git_fails ... ok
test highlights::store_gaps::store_reread_gets_new_directory_and_pointer ... ok
test ref_library::rename::bundle_dry_run_includes_companions_done_daily_and_ambiguous_bare_links ... ok
test ref_library::migrate_zorg::write_revert_restores_tree_and_doctor_count ... ok
test ref_library::migrate_tasks::depends_on_and_pomodoro_links_rewritten ... ok
test ref_library::migrate_tasks::unmapped_refuses_write_and_map_wins ... ok
test highlights::web_source_store::web_collection_create_saves_one_source_and_catalog ... ok
test ref_library::migrate_tasks::crash_adoption_writes_embed_without_second_task ... ok
test highlights::web_source_store::web_article_create_saves_source_and_catalog ... ok
test ref_library::rename::rename_help_lists_options_alphabetically_with_short_aliases ... ok
test ref_library::rename::dotted_stem_dry_run_preserves_the_full_stem ... ok
test ref_library::migrate_tasks::json_modes_and_commit_subject ... ok
test ref_library::list::list_filters_or_within_and_across_options ... ok
test ref_library::list::list_rows_carry_task_facts_blocked_by_and_human_reason ... ok
test ref_library::rename::gist_dry_run_reports_moves_links_and_id_rekey_without_writing ... ok
test ref_library::show::show_collapses_an_all_one_family_hit_set_to_the_newest ... ok
test ref_library::show::show_comments_only_without_comments_reports_empty ... ok
test ref_library::migrate_zorg::wrong_vault_refuses_before_syncing_or_migrating ... ok
test note_walkers::bob_dir_saved_sources_are_ignored_by_note_walkers ... ok
test ref_library::migrate_tasks::wrong_vault_refuses_before_syncing_or_migrating ... ok
test ref_library::show::show_excludes_color_grouped_mirror_with_counts ... ok
test ref_library::show::show_counts_preamble_blocks_as_excluded ... ok
test ref_library::migrate_zorg::write_offline_writes_notes_and_commits_only_zorg ... ok
test ref_library::show::show_ambiguous_stem_never_picks_first ... ok
test ref_library::show::show_dangling_middle_reading_keeps_numbers_and_warns ... ok
test ref_library::rename::colliding_reference_ids_receive_the_first_available_suffix ... ok
test ref_library::show::show_family_json_carries_reading_earlier_and_later ... ok
test ref_library::recatalog::recatalog_dry_run_then_commits_only_additive_link_records ... ok
test ref_library::show::show_legacy_note_reports_absent_annotations ... ok
test ref_library::show::show_missing_ref_dir_fails ... ok
test highlights::diagrams::highlights_create_mermaid_scale_warning_when_figure_is_wide ... ok
test ref_library::ref_help_matches_aliases_for_every_verb ... ok
test ref_library::show::show_json_exposes_marker_id_and_null_for_missing_ids ... ok
test ref_library::show::show_excludes_mirrors_with_counts ... ok
test ref_library::rename::resolver_scope_name_collision_and_highlight_refusals_are_structured ... ok
test ref_library::rename::idless_reference_rename_keeps_idless_state_and_pdf_bytes ... ok
test ref_library::show::show_natural_versioned_stem_has_no_chips_or_lineage ... ok
test ref_library::show::show_resolves_id_doi_arxiv_and_source_pdf ... ok
test ref_library::show::show_keeps_quotes_comments_images_and_tombstone_counts ... ok
test ref_library::show::show_resolves_before_printing_anything ... ok
test ref_library::show::show_root_names_later_readings_and_wears_v1 ... ok
test ref_library::rename::annotated_same_stem_repair_succeeds_and_full_rename_still_refuses ... ok
test ref_library::show::show_markdown_digest_covers_research_and_sections ... ok
test ref_library::ref_error_paths_match_aliases_for_every_verb ... ok
test ref_library::show::show_unparsed_region_reports_raw ... ok
test ref_library::rename::family_member_rename_rewrites_later_reading_earlier_link ... ok
test ref_library::show::show_miss_suggests_title_hints ... ok
test ref_library::show::show_comments_only_and_no_annotations ... ok
test ref_library::tasks::list_rows_carry_task_parent_status_and_diagnostics ... ok
test ref_library::show::show_resolves_every_exact_kind ... ok
test ref_library::today::completed_pomodoro_ref_is_closed ... ok
test ref_library::today::default_with_q_is_already_current ... ok
test ref_library::tasks::git_dates_never_backfills_v2_finished ... ok
test ref_library::show::show_rows_carry_blocked ... ok
test ref_library::tasks::list_parent_resolution_matches_routes_aliases_and_literals ... ok
test ref_library::show::show_tasks_own_notes_and_multiline_comments ... ok
test ref_library::today::help_lists_today_and_selectors ... ok
test ref_library::today::default_without_q_links_the_running_entry ... ok
test ref_library::today::exact_name_creates_when_only_prefix_matches ... ok
test ref_library::today::listing_flags_and_human_open_pomodoros ... ok
test ref_library::show::show_separates_several_refs_in_order ... ok
test ref_library::rename::same_stem_repair_updates_only_id_and_is_idempotent ... ok
test ref_library::today::dry_run_capture_object_matches_write_apart_from_dry_run ... ok
test ref_library::today::exact_name_reuses_whole_slug ... ok
test ref_library::tasks::show_human_and_json_carry_reading_tasks ... ok
test ref_library::show::show_superseded_url_picks_the_live_note_with_also ... ok
test ref_library::today::moving_q_creates_the_named_destination ... ok
test ref_library::show::show_sections_json_human_markdown_and_flags ... ok
test highlights::diagrams::highlights_create_mermaid_partial_failure_keeps_note_and_exits_0 ... ok
test ref_library::today::named_prefix_selects_bugs ... ok
test ref_library::today::moving_to_duplicate_unnamed_entry_reports_its_post_move_line ... ok
test highlights::diagrams::highlights_create_mermaid_missing_adapter_warns_and_exits_0 ... ok
test ref_library::today::pomodoro_ref_targets_an_unnamed_entry ... ok
test ref_library::today::project_blocked_reading_task_is_link_guard ... ok
test ref_library::today::own_depends_on_is_dropped_and_linked ... ok
test ref_library::rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test ref_library::today::stale_pomodoro_ref_writes_nothing ... ok
test run_env::clicolor_force_emits_ansi_on_piped_stdout ... ok
test ref_library::show::show_is_read_only ... ok
test ref_library::today::unnamed_rows_carry_derived_homes_and_label ... ok
test relations::relations_lists_catalog_counts_on_scratch_vault ... ok
test ref_library::today::next_and_in_progress_keep_their_lanes ... ok
test run_env::clicolor_force_zero_emits_no_ansi_on_piped_stdout ... ok
test relations::relations_help_is_in_tasks_and_projects_and_lists_options ... ok
test run_env::no_color_wins_over_clicolor_force ... ok
test run_env::unwritable_run_receipt_warns_and_keeps_the_exit_code ... ok
test run_env::bob_progress_emits_a_line_on_piped_stderr ... ok
test ref_library::today::ready_becomes_next_with_fresh_stamp ... ok
test stats::help_names_docs_and_exit_codes ... ok
test stats::invalid_range_is_exit_two ... ok
test relations::relations_hide_refuses_unknown_and_invalid_labels ... ok
test stats::real_vault_parity_is_opt_in ... ok
test stats::completion_includes_worked ... ok
test stats::missing_vault_is_exit_one ... ok
test relations_rename::relations_rename_refuses_malformed_matching_lines ... ok
test ref_library::today::scheduled_blocked_task_is_pulled_forward ... ok
test relations::relations_hide_unhide_round_trip_folds_across_hosts ... ok
test support::note_profile_package_skip_tests::note_profile_package_skip_reports_missing_packages ... ok
test run_env::run_receipt_records_success_usage_and_failure ... ok
test support::tempdir_drop_does_not_chmod_symlink_target ... ok
test support::tempdir_drop_removes_write_locked_tree ... ok
test ref_library::rename::offline_write_verifies_identity_sync_and_already_renamed_reruns ... ok
test stats::unknown_metric_is_exit_two_json_envelope ... ok
test task_move::help_lists_sorted_options_and_short_aliases ... ok
test stats::show_worked_json_includes_compare_points ... ok
test stats::overview_human_names_metrics ... ok
test ref_library::rename::other_vault_preview_and_offline_rename_remain_available ... ok
test stats::show_all_json_lists_visible_metrics ... ok
test ref_library::tasks::doctor_reports_ref_tasks_and_parents_rows ... ok
test stats::metrics_json_omits_points ... ok
test stats::overview_csv_has_tidy_header ... ok
test stats::metrics_catalog_lists_worked ... ok
test task_move::dry_run_reports_operational_plan_errors_as_json ... ok
test stats::overview_json_is_ok_schema_one ... ok
test task_move::live_zero_budget_refuses_a_held_lock_before_writing ... ok
test relations_rename::relations_rename_applies_case_only_and_requires_merge_for_existing_key ... ok
test task_move::dry_run_works_while_lock_is_held_and_writes_no_state_or_notes ... ok
test relations_rename::relations_list_reports_a_label_used_again_after_rename ... ok
test ref_library::migrate_zorg::write_sync_sandwich_merges_peer_and_pushes_scoped_commit ... ok
test task_status_hooks::blocked::reconcile_derives_project_schedule_blocking ... ok
test task_status_hooks::blocked::reconcile_cascades_to_child_projects ... ok
test task_status_hooks::blocked::reconcile_does_not_promote_same_note_ids_through_resident_edges ... ok
test relations::relations_concurrent_hides_both_survive ... ok
test task_status_hooks::blocked::reconcile_does_not_warn_for_an_unfielded_internal_child_link ... ok
test ref_library::rename::offline_write_moves_companions_and_refuses_dirty_or_stale_inputs ... ok
test task_move::identity_refusals_write_nothing ... ok
test task_status_hooks::blocked::reconcile_filters_project_internal_ids_by_id_field_only ... ok
test task_status_hooks::blocked::reconcile_ignores_notes_with_two_open_prj_lines ... ok
test task_status_hooks::blocked::reconcile_ignores_canonical_daily_note_projects ... ok
test ref_library::today::ledger_and_resolution_refusals ... ok
test task_status_hooks::blocked::reconcile_ignores_terminal_projects ... ok
test task_status_hooks::blocked::reconcile_ignores_two_scheduled_prj_tasks ... ok
test ref_library::today::refusals_cover_task_and_ledger_codes ... ok
test highlights::overwrite_local::markdown_overwrite_keeps_play_link_for_kept_audio ... ok
test task_status_hooks::blocked::reconcile_keeps_field_only_internal_prj_ids_unprojected ... ok
test task_status_hooks::blocked::reconcile_keeps_prj_internal_links_unprojected ... ok
test relations_rename::relations_rename_previews_rewrites_every_scope_and_reverts_as_one_commit ... ok
test task_status_hooks::blocked::reconcile_treats_uppercase_prj_anchor_as_an_ordinary_task ... ok
test task_status_hooks::blocked::reconcile_warns_inherited_resident_cycle ... ok
test task_status_hooks::blocked::task_status_hooks_blocked_status_guard_writes_nothing ... ok
test ref_library::rename::listen_link_not_in_sync_dirty_and_live_mode_refusals ... ok
test relations_rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test task_status_hooks::blocked::reconcile_raises_directly_linked_prj ... ok
test ref_library::today::today_matches_capture_on_identical_vaults ... ok
test task_move::git_dry_run_changes_no_notes_or_git_state ... ok
test ref_library::ref_doctor_and_scan_dry_run_match_aliases_on_fixture_vault ... ok
test task_status_hooks::blocks::br12_previous_daily_is_never_written_or_listed ... ok
test task_move::pre_sync_failure_does_not_write_move_data ... ok
test task_status_hooks::blocks::br18_unresolved_self_and_non_task_are_not_listed ... ok
test task_status_hooks::blocks::br17_malformed_dependent_is_kept_not_newly_added ... ok
test task_status_hooks::blocks::br20_internal_prj_target_is_not_listed ... ok
test projects::schedule::projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test task_status_hooks::blocks::br25_invalid_kill_switch_behaves_as_true ... ok
test projects::schedule::project_schedule_tasks_flip_between_dash_and_blocked_queries_when_due ... ok
test ref_library::attach::attach_named_reference_without_search_reports_no_saved_source ... ok
test task_status_hooks::blocks::br28_owner_future_mtime_defers_structurally ... ok
test ref_library::attach::attach_dry_run_verifies_but_writes_nothing ... ok
test ref_library::attach::attach_json_write_mode_keeps_search_attachment_stdout_parseable ... ok
test ref_library::attach::attach_without_refs_and_search_stays_silent_without_orphans ... ok
test ref_library::attach::attach_adopts_an_orphan_without_search_and_preserves_catalog ... ok
test highlights::create::highlights_create_renders_vault_note_snapshot_when_available ... ok
test ref_library::attach::attach_ambiguous_saved_sources_never_fall_through_to_search ... ok
test task_move::mixed_selectors_dedup_and_keep_source_order ... ok
test ref_library::attach::attach_json_names_every_candidate_verdict ... ok
test ref_library::attach::attach_adoption_dry_run_writes_nothing ... ok
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_catalog_is_invalid ... ok
test ref_library::attach::attach_skips_an_edited_candidate_below_threshold ... ok
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_store_is_claimed ... ok
test ref_library::attach::attach_skips_ambiguous_stem_when_none_verify ... ok
test ref_library::attach::attach_rejects_a_saved_store_claimed_by_another_note ... ok
test ref_library::attach::attach_reports_already_attached_and_snapshot_rows ... ok
test task_status_hooks::blocked::reconcile_preserves_crlf_on_tag_rewrite ... ok
test ref_library::attach::attach_refuses_same_byte_candidate_when_existing_store_has_wrong_pdf ... ok
test task_move::non_git_live_move_writes_and_reports_null_git_stages ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test task_status_hooks::blocked::task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test ref_library::attach::attach_json_write_mode_keeps_adoption_stdout_parseable ... ok
test ref_library::attach::attach_attaches_single_passing_ambiguous_candidate ... ok
test task_status_hooks::blocks::br10_closed_owner_is_frozen ... ok
test task_status_hooks::blocks::br13_hand_added_entry_without_edge_is_removed ... ok
test task_status_hooks::blocked::task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test ref_library::attach::attach_json_reports_failed_saved_source_before_search_fallback ... ok
test task_status_hooks::blocked::reconcile_terminal_project_prerequisite_does_not_block_residents ... ok
test ref_library::attach::attach_explicit_pair_attaches_despite_title_mismatch ... ok
test task_status_hooks::blocks::br14_canonicalizes_blocking_label ... ok
test task_status_hooks::blocked::reconcile_pdf1_databricks_ref_residents ... ok
test task_move::ordinary_commit_failure_keeps_the_write_without_post_sync ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test ref_library::attach::attach_saved_source_with_wrong_pdf_path_falls_back_to_search ... ok
test task_status_hooks::consume::reconcile_keeps_a_link_when_the_block_clears_in_the_same_run ... ok
test ref_library::attach::attach_skips_ambiguous_and_title_mismatch_candidates ... ok
test ref_library::attach::attach_verifies_and_records_a_fixture_source ... ok
test task_status_hooks::blocks::br15_deduplicates_and_deletes_orphans ... ok
test task_status_hooks::blocks::br16_malformed_blocks_line_is_left_alone ... ok
test ref_library::attach::attach_unverified_saved_source_reports_failure_then_uses_search ... ok
test task_status_hooks::blocks::br1_same_note_insert ... ok
test task_status_hooks::blocks::br21_field_only_dependency_is_adopted_and_listed ... ok
test task_status_hooks::dependency_lines::reconcile_warns_dependency_cycle_and_keeps_members_blocked ... ok
test relations::relations_hide_lock_busy_when_maintenance_lock_held ... ok
test task_status_hooks::blocks::br22_cycle_each_lists_the_other ... ok
test task_status_hooks::blocks::br19_prj_lists_only_the_project_task ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_unresolved_link_and_breadcrumbs ... ok
test task_move::post_sync_conflict_keeps_the_local_commit_and_reports_remote_wins ... ok
test task_status_hooks::blocks::br24_kill_switch_removes_open_lines_and_skips_mints ... ok
test task_status_hooks::dependency_lines::reconcile_never_writes_previous_daily_target ... ok
test task_status_hooks::dependency_lines::reconcile_skips_closed_dependents ... ok
test task_status_hooks::dependency_lines::reconcile_projection_only_write_defers_in_quiet_interval ... ok
test task_move::offline_git_move_commits_only_repaired_paths_and_preserves_task_state ... ok
test task_status_hooks::relations::lr17_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unadoptable_id_and_keeps_field ... ok
test task_status_hooks::blocks::br23_hide_ref_inbox_and_daily_are_listed ... ok
test task_status_hooks::relations::configured_cancel_label_stays_inert_during_reconcile ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unencodable_target_without_projecting ... ok
test task_status_hooks::relations::lr12_malformed_linked_from_left_alone ... ok
test task_status_hooks::relations::lr21_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::relations::lr14_unresolved_non_task_self_warned_and_omitted ... ok
test task_status_hooks::relations::lr23_duplicate_source_id_not_listed ... ok
test task_move::pre_sync_uses_the_peer_snapshot_and_commits_pending_local_edits ... ok
test task_status_hooks::relations::lr22_archived_source_keeps_done_form ... ok
test ref_library::attach::attach_adopts_an_exact_render_with_one_lost_pdf_glyph ... ok
test task_status_hooks::blocks::br27_second_run_is_idempotent ... ok
test task_status_hooks::relations::lr7_done_and_previous_daily_targets_never_written ... ok
test task_move::post_sync_failure_keeps_the_scoped_local_commit_and_reports_failure ... ok
test task_status_hooks::blocks::br29_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::relations::lr_human_output_includes_knot_group ... ok
test task_status_hooks::blocks::br2_unique_and_ambiguous_basename_links ... ok
test highlights::diagrams::highlights_create_recognizes_definition_list_mermaid_fences ... ok
test task_status_hooks::retry::task_status_hooks_defers_when_maintenance_lock_is_held ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_terminal_failure_and_exit_status ... ok
test task_move::co_move_then_reconcile_keeps_canonical_identities ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_ignores_retry_timeout ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_creates_no_lock_or_recovery ... ok
test task_status_hooks::blocks::br4_mints_idless_dependent_without_id_or_fresh_fields ... ok
test task_status_hooks::blocks::br3_one_line_sorted_across_notes ... ok
test task_status_hooks::retry::task_status_hooks_rejects_invalid_retry_timeout ... ok
test task_status_hooks::retry::task_status_hooks_live_noop_may_lock_but_creates_no_recovery ... ok
test task_status_hooks::blocks::br6_inserts_after_depends_on_subtree ... ok
test task_status_hooks::blocks::br7_inserts_second_after_cancel_log ... ok
test task_status_hooks::blocks::br5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::structure::task_status_hooks_drops_carried_link_already_in_completed_fallback ... ok
test task_status_hooks::structure::task_status_hooks_composes_daily_status_and_structural_edits ... ok
test task_status_hooks::structure::task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks::structure::task_status_hooks_keeps_archive_out_of_active_dependency_sync ... ok
test task_status_hooks::blocks::br8_prj_order_then_projects_sync_is_noop ... ok
test task_status_hooks::consume::reconcile_deletes_a_pomodoro_emptied_by_blocked_consumption ... ok
test task_status_hooks::structure::task_status_hooks_resolves_archive_references_read_only ... ok
test task_status_hooks::blocks::br11_reopened_owner_is_reprojected ... ok
test task_status_hooks::subprojects::blocked_subproject_links_are_consumed_and_promote_ancestor_prerequisites ... ok
test task_status_hooks::dependency_lines::reconcile_daily_note_keeps_adoption_and_stamp ... ok
test task_status_hooks::subprojects::descendant_project_targets_stay_unprojected_and_warn ... ok
test task_status_hooks::subprojects::inherited_edges_participate_in_r7_cycle_detection ... ok
test task_status_hooks::subprojects::projects_sync_ignores_cascade_tags_and_keeps_marker_state ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw3_dw6_rewrite_keeps_link_order ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw1_inserts_adopted_line_before_schedule_log ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw2_inserts_adopted_line_after_cancel_log ... ok
test task_status_hooks::subprojects::project_parent_cycles_warn_once_and_only_inherit_other_projects_reasons ... ok
test task_status_hooks::sync::task_status_hooks_nulls_plan_budget_on_invalid_config ... ok
test task_status_hooks::subprojects::reconcile_cascades_reasons_and_tags_through_multiple_project_levels ... ok
test task_status_hooks::consume::consumption_promoted_daily_note_prerequisite_may_clear_next_run ... ok
test task_status_hooks::subprojects::reconciled_cascade_tree_has_no_second_run_changes ... ok
test task_status_hooks::subprojects::reconcile_recovers_subprojects_and_keeps_nearest_remaining_reason ... ok
test task_status_hooks::consume::reconcile_consumes_blocked_resident_links_and_keeps_the_entry ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_deletes_line_and_field ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_with_adoptable_id_deletes_line_and_field ... ok
test task_status_hooks::blocked::reconcile_derives_project_blocking_tag_and_unblocked ... ok
test task_status_hooks::structure::task_status_hooks_removes_empty_pomodoros_and_reports_them ... ok
test task_status_hooks::dependency_line_writes::summary_reports_dependency_counts ... ok
test themes::themes_concurrent_hides_both_survive ... ok
test themes::themes_bare_is_list ... ok
test task_status_hooks::dependency_lines::reconcile_field_writer_handles_trailing_tags ... ok
test task_status_hooks::structure::task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test task_status_hooks::structure::task_status_hooks_normalizes_live_archive_terminal_references ... ok
test themes::themes_hidden_filter_reads_journal ... ok
test task_status_hooks::dependency_lines::reconcile_does_not_read_child_links_as_dependencies ... ok
test task_status_hooks::dependency_lines::reconcile_canonicalizes_legacy_line_variants ... ok
test task_status_hooks::dependency_lines::reconcile_ignores_archive_children_outside_the_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_adopts_field_ids_into_canonical_line ... ok
test task_status_hooks::dependency_lines::reconcile_drops_stale_field_id ... ok
test task_status_hooks::dependency_lines::reconcile_dependency_chain_settles_in_one_run ... ok
test task_status_hooks::sync::task_status_hooks_reports_grouping_warnings_without_noop_text ... ok
test themes::themes_fresh_and_cached_json_agree ... ok
test themes::themes_json_schema_and_query_ranks_fix_before_fixes ... ok
test themes::themes_lists_expected_hues_on_scratch_vault ... ok
test task_status_hooks::sync::task_status_hooks_reports_plan_budget_in_json_and_human ... ok
test themes::themes_list_emits_collision_hints ... ok
test task_status_hooks::dependency_lines::reconcile_removes_empty_line_and_leaves_malformed_alone ... ok
test themes::themes_list_emits_not_configured_hints ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test task_status_hooks::dependency_lines::reconcile_projects_line_into_field_and_stamps_target_id ... ok
test task_status_hooks::dependency_lines::reconcile_same_index_insert_does_not_clobber_replace ... ok
test themes::themes_help_is_in_daily_workflow_and_lists_options ... ok
test task_status_hooks::structure::task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test themes::themes_write_refusals_are_json_on_nonzero_exit ... ok
test task_status_hooks::structure::task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test task_status_hooks::dependency_lines::reconcile_warns_non_task_and_self_links_without_projecting ... ok
test task_status_hooks::relations::lr15_duplicate_linked_from_lines_deduplicated ... ok
test task_status_hooks::dependency_lines::reconcile_breadcrumb_heals_when_target_returns ... ok
test task_status_hooks::dependency_lines::reconcile_heals_moved_link ... ok
test themes::themes_hide_unhide_color_round_trip_folds_two_hosts ... ok
test themes_rename::themes_rename_dry_run_previews_collapse_and_leaves_vault_untouched ... ok
test task_status_hooks::retry::task_status_hooks_exhausts_retry_budget_and_still_fails ... ok
test themes_split::themes_split_stdin_map_works ... ok
test vault_sync::conflict_directory_is_skipped_by_vault_walkers ... ok
test task_status_hooks::relations::lr10_noncanonical_line_is_canonicalized ... ok
test task_status_hooks::relations::lr13_malformed_links_never_newly_added ... ok
test task_status_hooks::dependency_lines::reconcile_stamps_cross_note_target_id ... ok
test themes_split::themes_split_template_lists_old_entries_and_round_trips_as_keep ... ok
test themes_rename::themes_rename_refuses_configured_old_and_warns_unconfigured_new ... ok
test themes_split::themes_split_dry_run_reports_flags_and_leaves_vault_untouched ... ok
test themes_rename::themes_rename_leaves_fenced_prose_and_tasks_untouched ... ok
test themes_rename::themes_rename_preserves_crlf_bytes_in_offline_write ... ok
test task_status_hooks::sync::reconcile_status_only_flips_skip_quiet_period_but_structural_edits_wait ... ok
test themes_rename::themes_rename_apply_verifies_commits_and_reappears ... ok
test themes_split::themes_split_preserves_crlf_bytes_in_offline_write ... ok
test vault_sync::renamed_old_top_level_commands_are_unknown ... ok
test themes_rename::themes_rename_refusals_are_json_on_nonzero_exit ... ok
test themes_rename::themes_rename_later_color_or_unhide_clears_reappearance ... ok
test themes_rename::themes_rename_later_hide_does_not_clear_reappearance ... ok
test task_status_hooks::relations::lr2_labelled_edge ... ok
test task_status_hooks::relations::lr20_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::relations::lr19_symmetric_edges ... ok
test task_status_hooks::blocks::br26_rebuilds_identical_bytes_after_delete ... ok
test themes_rename::themes_rename_later_unhide_clears_reappearance ... ok
test themes_split::themes_split_write_commits_without_journal_and_invalidates_cache ... ok
test task_status_hooks::relations::lr24_prj_target_gets_the_mirror ... ok
test task_status_hooks::relations::lr3_sorted_sources_include_done ... ok
test task_status_hooks::relations::lr1_same_note_insert ... ok
test task_status_hooks::relations::lr6_closed_target_still_mirrored ... ok
test task_status_hooks::relations::lr4_mints_source_id ... ok
test themes_rename::wrong_vault_refuses_before_syncing_or_renaming ... ok
test themes_rename::themes_rename_cycle_does_not_report_reappearance ... ok
test task_status_hooks::sync::task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test task_status_hooks::retry::task_status_hooks_human_retry_progress_goes_to_stdout ... ok
test themes_split::wrong_vault_refuses_before_syncing_or_splitting ... ok
test themes_split::themes_split_refusals_are_json_on_nonzero_exit ... ok
test vault_sync::vault_sync_concurrent_invocation_exits_zero_silently ... ok
test task_status_hooks::relations::lr8_done_and_previous_daily_sources_are_listed ... ok
test task_status_hooks::relations::lr5_quiet_interval_skips_mint_until_next_run ... ok
test vault_sync::vault_sync_no_change_cycle_writes_status_without_committing ... ok
test highlights::store_gaps::store_snapshot_create_records_note_snapshot_route ... ok
test vault_sync::vault_sync_refuses_95_mib_file_before_staging ... ok
test task_status_hooks::retry::task_status_hooks_json_retry_progress_stays_off_stdout ... ok
test task_status_hooks::sync::task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test task_status_hooks::relations::lr9_hand_added_and_deleted_entries ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_retry_and_final_result ... ok
test vault_sync::nightly_articles_step_reports_without_writing_and_still_passes ... ok
test vault_sync::vault_sync_local_only_change_commits_and_pushes ... ok
test vault_sync::vault_sync_dry_run_reports_clobber_without_writing ... ok
test vault_sync::nightly_failed_step_still_runs_later_steps_and_exits_nonzero ... ok
test vault_sync::vault_sync_ignores_legitimate_rewrites ... ok
test vault_sync::vault_sync_remote_only_change_fast_forwards ... ok
test vault_sync::executable_stubs_stay_executable_while_other_threads_fork ... ok
test vault_sync::nightly_runs_vault_sync_move_done_tasks_vault_sync_in_order ... ok
test vault_sync::vault_sync_both_added_file_quarantines_local_copy ... ok
test vault_sync::vault_sync_delete_modify_conflict_keeps_the_file ... ok
test vault_sync::vault_sync_non_overlapping_edits_merge_cleanly ... ok
test vault_sync::vault_sync_quarantines_incident_shaped_clobber ... ok
test vault_sync::vault_sync_binary_conflict_quarantines_uncorrupted_local_copy ... ok
test vault_sync::vault_sync_same_line_edit_quarantines_local_copy_and_keeps_remote ... ok
test vault_sync::vault_sync_recovers_interrupted_merge_and_finishes_cycle ... ok
test vault_sync::vault_sync_conflict_copy_on_ignored_path_still_commits_merge ... ok
test vault_sync::vault_sync_completes_fast_forward_left_by_head_lock ... ok
test vault_sync::vault_sync_push_race_retries_and_succeeds ... ok
test task_status_hooks::blocks::br9_last_dependent_close_removes_line ... ok
test vault_sync::vault_sync_halts_on_repeated_interrupted_merge_of_same_remote ... ok
test vault_sync::vault_sync_retries_fast_forward_blocked_by_head_lock ... ok
test highlights::create::highlights_create_stamps_return_links_marker_only_when_links_paired ... ok
test task_status_hooks::structure::task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test task_status_hooks::relations::lr16_kill_switch_removes_writable_lines_and_skips_mints ... ok
test task_status_hooks::sync::task_status_hooks_un_decorates_legacy_groups_holding_only_ready ... ok
test task_status_hooks::sync::task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test task_status_hooks::sync::task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test task_status_hooks::relations::lr11_rebuilds_identical_bytes_after_delete ... ok
test themes::themes_hide_lock_busy_when_maintenance_lock_held ... ok
test themes_rename::themes_rename_lock_busy_when_maintenance_lock_held ... ok
test highlights::diagrams::highlights_create_live_mermaid_pdf_is_highlights_safe ... ok
test task_status_hooks::relations::lr18_inert_statuses_and_fields ... ok
test highlights::diagrams::highlights_create_mermaid_adapter_crash_invalid_and_timeout_degrade ... ok
test task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses ... ok
test highlights::diagrams::highlights_create_snapshot_mermaid_success_and_failure_shape ... ok
test highlights::ingest::create_queues_when_locks_or_pre_sync_prevent_inline_intake has been running for over 60 seconds
test highlights::ingest::create_queues_when_locks_or_pre_sync_prevent_inline_intake ... ok
test highlights::scan_intake::intake_status_records_create_outcomes_and_keeps_the_other_field has been running for over 60 seconds
test highlights::scan_intake::intake_status_records_create_outcomes_and_keeps_the_other_field ... ok

test result: ok. 2331 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 67.56s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/dataview_parity-045096bc8cc5f0cf)

running 27 tests
test dataview_live_obsidian_parity_harness_compares_supported_native_cases ... ok
test dataview_parity_fixture_vault_covers_contract_surface ... ok
test dataview_obsidian_calendar_markdown_golden_fails_cleanly ... ok
test dataview_obsidian_paths_goldens_cover_grouped_and_flattened_warnings ... ok
test dataview_native_current_paths_golden_uses_fixture_vault ... ok
test dataview_native_calendar_markdown_fails_cleanly ... ok
test dataview_native_index_values_cover_yaml_inline_dates_and_links ... ok
test dataview_native_expression_core_supports_swizzling_and_lambdas ... ok
test dataview_native_index_skips_hidden_directories ... ok
test dataview_native_function_library_supports_numeric_and_container_functions ... ok
test dataview_native_index_builds_task_and_list_objects ... ok
test dataview_native_dql_from_accepts_source_expressions ... ok
test dataview_native_function_library_supports_string_functions ... ok
test dataview_native_dql_from_ref_prefers_folder_when_note_also_exists ... ok
test dataview_native_function_library_supports_constructors_and_utilities ... ok
test dataview_obsidian_markdown_goldens_cover_supported_exports ... ok
test dataview_native_current_json_golden_uses_bob_wrapper_shape ... ok
test dataview_obsidian_dql_json_goldens_cover_result_shapes ... ok
test dataview_native_expression_core_supports_this_comparison_and_sorting ... ok
test dataview_native_function_library_works_in_where_sort_and_list ... ok
test dataview_native_expression_core_evaluates_table_and_list_values ... ok
test dataview_native_markdown_goldens_cover_supported_exports ... ok
test dataview_native_index_builds_file_metadata_and_link_graph ... ok
test dataview_obsidian_source_goldens_cover_source_expression_contract ... ok
test dataview_native_dql_execution_supports_phase6_result_shapes ... ok
test dataview_native_source_expressions_match_fixture_goldens ... ok
test dataview_native_source_smoke_handles_generated_vault_with_many_lists ... ok

test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.37s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_adapter-a41834edd3018b24)

running 6 tests
test note_builder_shapes_a_keep_note ... ok
test fake_adapter_serves_ping_and_records_the_call ... ok
test fake_adapter_exit_is_a_crash_without_output ... ok
test fake_adapter_prefers_nth_responses ... ok
test fake_adapter_serves_errors_and_exchange ... ok
test fake_adapter_honors_sleep ... ok

test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.21s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_auth-f4da0806ca5ba93e)

running 11 tests
test login_missing_email_is_a_setup_error ... ok
test login_preflight_failure_leaves_the_cookie_unconsumed ... ok
test doctor_adapter_crash_skips_keep ... ok
test doctor_cookie_token_fails_and_keep_skips ... ok
test doctor_missing_target_fails ... ok
test login_readback_mismatch_writes_a_recovery_file ... ok
test login_store_failure_writes_a_recovery_file ... ok
test doctor_json_reports_the_check_shape ... ok
test login_email_override_wins_and_warns_on_cookie_shape ... ok
test doctor_all_ok_reports_the_checklist ... ok
test login_via_stdin_exchanges_stores_and_verifies ... ok

test result: ok. 11 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.05s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_cli-a204c8fbda174c45)

running 6 tests
test top_help_pins_the_command_surface ... ok
test usage_errors_exit_2 ... ok
test top_level_options_match_list_and_default_to_list ... ok
test default_command_note_appears_exactly_once_in_short_and_long_help ... ok
test subcommand_options_are_alphabetical ... ok
test subcommand_help_blocks_carry_examples_and_environment ... ok

test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.04s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_list-36fbd230bb53870f)

running 20 tests
test all_with_no_tasks_prints_no_tasks ... ok
test vault_rows_sort_oldest_first_with_missing_last ... ok
test missing_target_prints_exact_line ... ok
test dst_gap_reports_45m_not_now ... ok
test keep_age_is_correct_outside_utc ... ok
test ages_follow_bob_now ... ok
test marked_keep_source_link_is_compact_in_table_and_preserved_in_json ... ok
test json_output_has_schema_version_and_sections ... ok
test output_is_plain_when_piped ... ok
test still_in_keep_covers_pinned_shared_and_empty ... ok
test keep_source_omits_the_vault_section ... ok
test default_subcommand_is_list ... ok
test url_only_note_shows_parent_hint_for_resolved_and_asks_routes ... ok
test keep_auth_error_still_shows_the_vault ... ok
test all_shows_archived_notes_and_done_tasks ... ok
test duplicate_markers_warn_on_stderr ... ok
test vault_source_needs_no_config_or_adapter ... ok
test each_state_is_rendered ... ok
test url_only_note_shows_ref_hint_and_json_verdict ... ok
test footer_covers_the_clear_and_actionable_cases ... ok

test result: ok. 20 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.08s

     Running tests/gkeep_migrate.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_migrate-3f3c4b52e1837a47)

running 9 tests
test dry_run_reports_without_writing_or_metadata ... ok
test malformed_ambiguous_and_code_examples_are_retained ... ok
test restrictive_allowlist_leaves_markers_and_evidence_untouched ... ok
test source_child_keeps_link_and_removes_only_marker ... ok
test done_tasks_migrated_and_excluded_dirs_skipped ... ok
test json_shape_and_line_endings_preserved ... ok
test removes_standalone_markers_and_creates_verified_receipts ... ok
test allowlist_migrates_markers_and_reuses_uncommitted_receipt ... ok
test needs_no_config_or_adapter ... ok

test result: ok. 9 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.80s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_pull-dd0da037d577b7d1)

running 47 tests
test dry_run_json_reports_unwritten ... ok
test missing_target_reports_before_vault_lock ... ok
test snapshot_auth_error_writes_nothing ... ok
test pull_lock_contention_exits_1 ... ok
test dry_run_with_lock_held_still_succeeds ... ok
test dry_run_previews_ref_without_clipping ... ok
test url_only_matrix_classifies_without_clipping ... ok
test percent_and_at_listen_markers_survive_keep_pull_planning ... ok
test retryable_clip_failure_needs_no_target ... ok
test already_in_library_archives_without_fetch ... ok
test filed_two_reading_family_never_mints_reread ... ok
test dry_run_no_archive_reports_not_requested ... ok
test production_allowlist_refuses_ignored_receipt_without_writes ... ok
test retryable_clip_failure_stays_in_keep_and_fails ... ok
test target_missing_and_unknown_or_ambiguous_ids_exit_2 ... ok
test all_clip_pull_needs_no_target ... ok
test double_modification_abort_keeps_exact_bytes ... ok
test keep_parent_precedence_note_route_cli_alias_and_fallback ... ok
test crlf_endings_preserved_and_space_indent_used ... ok
test archive_changed_after_clip_reports_and_keeps_journal ... ok
test empty_snapshot_second_pull_reports_nothing ... ok
test dry_run_previews_exact_markdown_without_writing_or_archiving ... ok
test dry_run_markdown_equals_real_run ... ok
test ref_created_repull_needs_no_target ... ok
test no_ref_flag_keeps_url_as_task ... ok
test non_git_vault_writes_without_commit_and_json_shape ... ok
test url_only_pdf_note_clips_and_archives_without_task ... ok
test ignored_target_parent_exclusion_and_fatal_git_are_truthful ... ok
test second_note_with_same_url_reports_already_queued ... ok
test normal_pull_writes_verifies_commits_and_archives ... ok
test quiet_verify_failure_reports_once_with_empty_stdout ... ok
test target_race_once_replans_and_succeeds ... ok
test crash_after_commit_before_archive_recovers_as_pending ... ok
test interactive_parent_prompt_sticky_default_and_reprompt ... ok
test no_archive_writes_but_leaves_notes_then_next_pull_archives_only ... ok
test archive_only_pull_reports_no_failure ... ok
test archive_crash_reports_once_in_both_modes ... ok
test quiet_success_is_silent_and_target_race_aborts ... ok
test production_allowlist_with_receipt_exception_commits_and_archives ... ok
test second_pull_after_success_is_archive_only_with_no_duplicate_write ... ok
test limit_and_explicit_pinned_selection ... ok
test permanent_clip_failure_writes_task_with_warning ... ok
test archive_failure_json_keeps_markdown_and_reports ... ok
test archive_changed_reports_and_next_pull_writes_revision ... ok
test archive_missing_error_and_crash_keep_the_committed_vault ... ok
test create_ref_fallback_verify_failure_counts_as_failed ... ok
test url_only_pdf_note_files_into_a_synced_vault ... ok

test result: ok. 47 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.71s

     Running tests/gkeep_pull_recovery.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/gkeep_pull_recovery-5e7761c13c11d64b)

running 7 tests
test identical_url_less_notes_use_multiplicity ... ok
test target_crash_finalizes_without_appending_again ... ok
test portability_second_host_with_empty_state_adds_nothing ... ok
test prepare_crash_retries_without_duplicate ... ok
test archive_only_uses_recorded_destination_not_inbox ... ok
test ignored_uncommitted_receipt_retries_commit_before_archive ... ok
test committed_receipt_survives_missing_original_note ... ok

test result: ok. 7 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.24s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/randomize-f69db91da68364ae)

running 15 tests
test randomize_help_lists_options_alphabetically ... ok
test randomize_dry_run_writes_nothing_and_prints_replay ... ok
test randomize_needs_a_look_skips_are_reported ... ok
test randomize_nothing_due_missing_config ... ok
test randomize_date_bounds_reject_unrepresentable_offsets_and_windows ... ok
test randomize_unreachable_remote_fails_presync_with_offline_hint ... ok
test randomize_held_lock_fails_fast_with_no_writes ... ok
test randomize_non_git_vault_warns_and_writes ... ok
test randomize_hooks_parity_after_live_run ... ok
test randomize_live_offline_rewrites_notes_with_status_log_and_grouping ... ok
test randomize_json_contract_keys_and_failure_shape ... ok
test randomize_offline_commits_without_pushing ... ok
test randomize_seed_replays_dry_run_dates_filters_levels_and_until ... ok
test randomize_bare_remote_syncs_scoped_commit_and_push ... ok
test randomize_post_sync_conflict_keeps_local_commit_and_warns ... ok

test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.42s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/tasks_parity-a579f56c8602ab2e)

running 33 tests
test tasks_live_obsidian_parity_harness_renders_and_scrapes_tasks_blocks ... ok
test tasks_parity_fixture_vault_covers_phase1_contract ... ok
test path_qualified_dependency_ids_keep_duplicate_block_fragments_distinct ... ok
test tasks_native_filterless_paths_golden_includes_underscore_folders ... ok
test hide_tags_only_removes_recognized_task_tags ... ok
test tasks_native_filterless_json_golden_reads_settings_and_tasks ... ok
test tasks_by_function_exposes_tasks_query_context_and_real_moment_dates ... ok
test tasks_markdown_honors_tree_layout_fields_counts_and_explain ... ok
test blocked_note_includes_dependency_and_future_scheduled_status_reasons ... ok
test tasks_native_dashboard_defaults_run_function_filters_with_pinned_moment ... ok
test sort_by_function_evaluates_each_task_key_once ... ok
test tasks_query_parser_accepts_the_daily_note_query_surface ... ok
test tasks_by_function_runs_dash_filters_and_stacked_sorts ... ok
test tasks_note_rejects_status_symbol_but_function_filter_selects_next ... ok
test tasks_cli_rejects_invalid_combinations_and_unsupported_surface ... ok
test tasks_javascript_exposes_priority_digits_and_pins_all_moment_clocks ... ok
test tasks_note_reports_the_failing_block_context ... ok
test tasks_settings_have_stable_defaults_when_plugin_data_is_absent ... ok
test tasks_plugin_emoji_setting_selects_emoji_metadata_parser ... ok
test tasks_query_parser_composes_dash_defaults_and_serializes_the_ast ... ok
test tasks_short_flags_files_stdin_and_comments_reach_filterless_slice ... ok
test tasks_result_pipeline_sorts_groups_and_limits_like_tasks_v8 ... ok
test tasks_group_by_function_reports_array_keys_and_runtime_errors ... ok
test tasks_note_executes_every_dashboard_block_with_origin_defaults ... ok
test tasks_note_and_origin_normalize_leading_current_directory_components ... ok
test tasks_note_identifies_blocks_in_paths_and_markdown_output ... ok
test tasks_native_boolean_and_implicit_and_filters_match_goldens ... ok
test tasks_explicit_origin_preserves_indexed_note_compatibility ... ok
test tasks_group_by_function_keeps_null_empty_array_and_empty_string_tasks ... ok
test tasks_native_date_filters_match_pinned_range_boundaries ... ok
test tasks_native_filter_families_match_fixture_goldens ... ok
test tasks_every_native_sort_and_group_key_executes ... ok
test tasks_by_function_surfaces_parse_return_type_and_sort_errors ... ok

test result: ok. 33 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.18s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/tasks_real_vault_parity-0d2dc2f594a35474)

running 1 test
test real_vault_dash_matches_independent_raw_ground_truth_and_all_blocks_execute ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws15-261028_104756/build/debug/deps/bob_obsidian_assets-f60551e36047b0e6)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

   Doc-tests bob_cli

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

   Doc-tests bob_obsidian_assets

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

succeeded  exit=0  duration=188372ms

