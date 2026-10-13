# Chat History - ace-run (79--mon)

- **TIMESTAMP:** 2026-10-13 08:12:09 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 79--mon

## Prompt

sase monitor start --command 'just check' --reason 'Verify the approved rustc warning cleanup and lint gate'

## Response

sase tool run c86b25f5f93e0a980be0f00c22d81e50

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces
    Checking chacha20 v0.10.2
    Checking rand v0.10.1
    Checking lopdf v0.40.0
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12)
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

error: unused variable: `block_end_excl`
   --> src/native/ref_library/migrate_tasks/plan.rs:232:14
    |
232 |         let (block_end_excl, children) =
    |              ^^^^^^^^^^^^^^ help: if this is intentional, prefix it with an underscore: `_block_end_excl`
    |
    = note: `-D unused-variables` implied by `-D unused`
    = help: to override `-D unused` add `#[allow(unused_variables)]`

warning: this function has too many arguments (8/7)
   --> src/native/capture/dependencies.rs:876:1
    |
876 | / fn resolve_prerequisites(
877 | |     ctx: &DependencyContext,
878 | |     planner: &mut CaptureBatchPlanner,
879 | |     bob_dir: &Path,
...   |
884 | |     dependent_desc: &str,
885 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
    | |_______________________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1218:24
     |
1218 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
     = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1758:6
     |
1758 |   ) -> Result<
     |  ______^
1759 | |     (
1760 | |         Vec<MergedMember>,
1761 | |         BTreeSet<(String, String)>,
...    |
1765 | |     CaptureError,
1766 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this `if` statement can be collapsed
    --> src/native/capture/output.rs:1020:5
     |
1020 | /     if result.kind == "pomodoro_start" {
1021 | |         if let Some(start) = result.pomodoro_start.as_ref() {
1022 | |             print_human_pomodoro_start_success(
1023 | |                 result,
...    |
1032 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
     = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
     |
1020 ~     if result.kind == "pomodoro_start"
1021 ~         && let Some(start) = result.pomodoro_start.as_ref() {
1022 |             print_human_pomodoro_start_success(
 ...
1030 |             return;
1031 ~         }
     |

warning: this function has too many arguments (9/7)
   --> src/native/capture/plan.rs:457:1
    |
457 | / pub(super) fn plan_capture_item(
458 | |     request: &CaptureRequest,
459 | |     parsed_item: ParsedCaptureItem,
460 | |     now: chrono::NaiveDateTime,
...   |
466 | |     dependency_ctx: &mut DependencyContext,
467 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:635:9
    |
635 | /         let Some(relative_close) = line[open..].find(')') else {
636 | |             return None;
637 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: manual `rem_euclid` implementation
   --> src/native/capture/pomodoro_adjust.rs:990:5
    |
990 |     (((value % 1440) + 1440) % 1440) as u64
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
   --> src/native/capture_language/editor_model.rs:459:1
    |
459 | / pub(super) enum TokenParse {
460 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 352 bytes
461 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
462 | | }
    | |_^ the entire enum is at least 352 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
460 -     Marker(MarkerParse),
460 +     Marker(Box<MarkerParse>),
    |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/editor_parse.rs:959:9
     |
 959 | /         if is_standalone_listen_marker(tokens[1].text) {
 960 | |             if let Some(intent) = classify_token(tokens[0].text) {
 961 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
 962 | |                     return None;
...    |
1005 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
 959 ~         if is_standalone_listen_marker(tokens[1].text)
 960 ~             && let Some(intent) = classify_token(tokens[0].text) {
 961 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
 ...
1003 |                 });
1004 ~             }
     |

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:1683:17
     |
1683 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/capture_language/item.rs:186:9
    |
186 | /         if is_standalone_listen_marker(tokens[1].text) {
187 | |             if let Some(intent) = classify_token(tokens[0].text) {
188 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
189 | |                     return None;
...   |
229 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
186 ~         if is_standalone_listen_marker(tokens[1].text)
187 ~             && let Some(intent) = classify_token(tokens[0].text) {
188 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
...
227 |                 ));
228 ~             }
    |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1817:31
     |
1817 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
1817 -                 Err(error) => return Err(error.message),
1817 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1825:21
     |
1825 | /                     return Err(close_inline_dangling_error(
1826 | |                         &head, index, plain,
1827 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1825 ~                     Err(close_inline_dangling_error(
1826 +                         &head, index, plain,
1827 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1863:21
     |
1863 | /                     return Ok(Some(parsed_capture_item_outcome(
1864 | |                         item,
1865 | |                         ParsedCaptureText {
1866 | |                             body,
...    |
1877 | |                         None,
1878 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
1863 ~                     Ok(Some(parsed_capture_item_outcome(
1864 +                         item,
1865 +                         ParsedCaptureText {
1866 +                             body,
1867 +                             clip: None,
1868 +                             route: None,
1869 +                             kind: CaptureKind::PomodoroClose { spec },
1870 +                             scheduled_offset: None,
1871 +                             priority_level: None,
1872 +                             sub_bullets: Vec::new(),
1873 +                             dependencies: Vec::new(),
1874 +                             dependency_target: None,
1875 +                         },
1876 +                         Vec::new(),
1877 +                         None,
1878 ~                     )))
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

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/gkeep/imports.rs:420:26
    |
420 | pub(super) fn unfinished<'a>(
    |                          ^^
421 |     files: &'a [(PathBuf, TransactionFile)],
    |             ^^
422 | ) -> Vec<&'a (PathBuf, TransactionFile)> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
420 ~ pub(super) fn unfinished(
421 ~     files: &[(PathBuf, TransactionFile)],
422 ~ ) -> Vec<&(PathBuf, TransactionFile)> {
    |

warning: using `Option.and_then(|x| Some(y))`, which is more succinctly expressed as `map(|x| y)`
   --> src/native/gkeep/migrate.rs:755:5
    |
755 | /     parse_source_url(&description).and_then(|encoded| {
756 | |         // Decode percent-encoding back to the raw Keep URL for storage.
757 | |         Some(percent_decode(&encoded).unwrap_or(encoded))
758 | |     })
    | |______^ help: try: `parse_source_url(&description).map(|encoded| percent_decode(&encoded).unwrap_or(encoded))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bind_instead_of_map
    = note: `#[warn(clippy::bind_instead_of_map)]` on by default

warning: usage of `bool::then` in `filter_map`
   --> src/native/gkeep/migrate_tasks.rs:472:14
    |
472 |               .filter_map(|(_, receipt)| {
    |  ______________^
473 | |                 (receipt.state == EntryState::Prepared)
474 | |                     .then(|| receipt.destination.clone())
475 | |             })
    | |______________^ help: use `filter` then `map` instead: `filter(|&(_, receipt)| (receipt.state == EntryState::Prepared)).map(|(_, receipt)| receipt.destination.clone())`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_map_bool_then
    = note: `#[warn(clippy::filter_map_bool_then)]` on by default

warning: usage of `bool::then` in `filter_map`
   --> src/native/gkeep/migrate_tasks.rs:673:58
    |
673 |                       receipt_paths.extend(receipts.iter().filter_map(
    |  __________________________________________________________^
674 | |                         |(path, receipt)| {
675 | |                             (receipt.destination == plan.rel).then(|| {
676 | |                                 path.strip_prefix(&bob_dir)
...   |
680 | |                         },
681 | |                     ));
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_map_bool_then
help: use `filter` then `map` instead
    |
673 ~                     receipt_paths.extend(receipts.iter().filter(|&(path, receipt)| (receipt.destination == plan.rel)).map(|(path, receipt)| path.strip_prefix(&bob_dir)
674 +                                     .unwrap_or(path)
675 ~                                     .to_path_buf()));
    |

warning: usage of `bool::then` in `filter_map`
   --> src/native/gkeep/migrate_tasks.rs:684:55
    |
684 |                       receipt_paths.extend(files.iter().filter_map(
    |  _______________________________________________________^
685 | |                         |(path, tx)| {
686 | |                             (tx.destination == plan.rel
687 | |                                 && tx.transaction_id.starts_with("mt-"))
...   |
693 | |                         },
694 | |                     ));
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_map_bool_then
help: use `filter` then `map` instead
    |
684 ~                     receipt_paths.extend(files.iter().filter(|&(path, tx)| (tx.destination == plan.rel
685 +                                 && tx.transaction_id.starts_with("mt-"))).map(|(path, tx)| path.strip_prefix(&bob_dir)
686 +                                     .unwrap_or(path)
687 ~                                     .to_path_buf()));
    |

warning: this `if` statement can be collapsed
    --> src/native/gkeep/migrate_tasks.rs:1250:9
     |
1250 | /         if let Some(url) = source_url.as_deref() {
1251 | |             if !supported_keep_url(url) {
1252 | |                 skip.get_or_insert_with(|| {
1253 | |                     "source destination is not a supported HTTP(S) Keep URL"
...    |
1257 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1250 ~         if let Some(url) = source_url.as_deref()
1251 ~             && !supported_keep_url(url) {
1252 |                 skip.get_or_insert_with(|| {
 ...
1255 |                 });
1256 ~             }
     |

warning: derefed type is same as origin
    --> src/native/gkeep/migrate_tasks.rs:1547:8
     |
1547 |       if labels
     |  ________^
1548 | |         .as_deref()
     | |___________________^ help: try: `labels`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_option_as_deref
     = note: `#[warn(clippy::needless_option_as_deref)]` on by default

warning: consider using `sort_by_key`
    --> src/native/gkeep/migrate_tasks.rs:1953:5
     |
1953 |     ordered.sort_by(|left, right| right.start.cmp(&left.start));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
     = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
     |
1953 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1953 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.start));
     |

warning: length comparison to zero
    --> src/native/gkeep/migrate_tasks.rs:2282:18
     |
2282 |     let failed = failures.len() > 0;
     |                  ^^^^^^^^^^^^^^^^^^ help: using `!is_empty` is clearer and more explicit: `!failures.is_empty()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#len_zero
     = note: `#[warn(clippy::len_zero)]` on by default

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
   --> src/native/highlights_ref/listen.rs:690:23
    |
690 |     if length == 0 || rest[length..].chars().next() != Some('}') {
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
   --> src/native/highlights_ref/reading_plan.rs:796:9
    |
796 | /         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line) {
797 | |             if crate::native::ref_tasks::is_open_mark(hit.mark) {
798 | |                 tracker_idx = Some(i);
799 | |                 break;
800 | |             }
801 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
796 ~         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line)
797 ~             && crate::native::ref_tasks::is_open_mark(hit.mark) {
798 |                 tracker_idx = Some(i);
799 |                 break;
800 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:875:5
    |
875 | /     if has_hash && has_base {
876 | |         if let Some(updated) = recompute_parent_free_hash(&front_lines) {
877 | |             front_lines = updated;
878 | |         }
879 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
875 ~     if has_hash && has_base
876 ~         && let Some(updated) = recompute_parent_free_hash(&front_lines) {
877 |             front_lines = updated;
878 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:888:9
    |
888 | /         if let Some((k, v)) = line.split_once(':') {
889 | |             if k.trim() == "highlights_marker_base" {
890 | |                 let mut v = v.trim().to_string();
891 | |                 if (v.starts_with('\'') && v.ends_with('\'') && v.len() >= 2)
...   |
900 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
888 ~         if let Some((k, v)) = line.split_once(':')
889 ~             && k.trim() == "highlights_marker_base" {
890 |                 let mut v = v.trim().to_string();
...
898 |                 base_json = Some(v);
899 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:913:9
    |
913 | /         if let Some((k, _)) = line.split_once(':') {
914 | |             if k.trim() == "highlights_marker_hash" {
915 | |                 // Preserve quoting style: single-quoted string.
916 | |                 out.push(format!("highlights_marker_hash: '{hash}'"));
...   |
919 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
913 ~         if let Some((k, _)) = line.split_once(':')
914 ~             && k.trim() == "highlights_marker_hash" {
915 |                 // Preserve quoting style: single-quoted string.
916 |                 out.push(format!("highlights_marker_hash: '{hash}'"));
917 |                 continue;
918 ~             }
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

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1051:9
     |
1051 | /         if trimmed.starts_with("done_tasks:") {
1052 | |             if let Some(start) = trimmed.find("[[") {
1053 | |                 if let Some(end) = trimmed[start..].find("]]") {
1054 | |                     let target = &trimmed[start + 2..start + end];
...    |
1062 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1051 ~         if trimmed.starts_with("done_tasks:")
1052 ~             && let Some(start) = trimmed.find("[[") {
1053 |                 if let Some(end) = trimmed[start..].find("]]") {
 ...
1060 |                 }
1061 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1052:13
     |
1052 | /             if let Some(start) = trimmed.find("[[") {
1053 | |                 if let Some(end) = trimmed[start..].find("]]") {
1054 | |                     let target = &trimmed[start + 2..start + end];
1055 | |                     let mut rel = target.trim().to_string();
...    |
1061 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1052 ~             if let Some(start) = trimmed.find("[[")
1053 ~                 && let Some(end) = trimmed[start..].find("]]") {
1054 |                     let target = &trimmed[start + 2..start + end];
 ...
1059 |                     return Some(rel);
1060 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1065:5
     |
1065 | /     if relative.components().count() == 1 {
1066 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1067 | |             return Some(format!("done/{stem}_done.md"));
1068 | |         }
1069 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1065 ~     if relative.components().count() == 1
1066 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1067 |             return Some(format!("done/{stem}_done.md"));
1068 ~         }
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
   --> src/native/projects/scan.rs:226:5
    |
226 | /     let Some(&(line_number, raw_value)) = fields.first() else {
227 | |         return None;
228 | |     };
    | |______^ help: replace it with: `let &(line_number, raw_value) = fields.first()?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this `if` statement can be collapsed
   --> src/native/ref_jobs/spool.rs:410:9
    |
410 | /         if let Err(error) = fs::remove_file(path) {
411 | |             if error.kind() != std::io::ErrorKind::NotFound {
412 | |                 failures.push(format!(
413 | |                     "remove staged ref job {}: {error}",
...   |
417 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
410 ~         if let Err(error) = fs::remove_file(path)
411 ~             && error.kind() != std::io::ErrorKind::NotFound {
412 |                 failures.push(format!(
...
415 |                 ));
416 ~             }
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
   --> src/native/ref_library/migrate_tasks/plan.rs:706:13
    |
706 | /             if let Some((key, value)) = raw.split_once(':') {
707 | |                 if key.trim().eq_ignore_ascii_case("title") {
708 | |                     let mut v = value.trim().to_string();
709 | |                     if (v.starts_with('"') && v.ends_with('"') && v.len() >= 2)
...   |
720 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
706 ~             if let Some((key, value)) = raw.split_once(':')
707 ~                 && key.trim().eq_ignore_ascii_case("title") {
708 |                     let mut v = value.trim().to_string();
...
718 |                     }
719 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:731:13
    |
731 | /             if let Some((key, value)) = raw.split_once(':') {
732 | |                 if key.trim().eq_ignore_ascii_case("created") {
733 | |                     let mut v = value.trim().to_string();
734 | |                     if (v.starts_with('"') && v.ends_with('"') && v.len() >= 2)
...   |
753 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
731 ~             if let Some((key, value)) = raw.split_once(':')
732 ~                 && key.trim().eq_ignore_ascii_case("created") {
733 |                     let mut v = value.trim().to_string();
...
751 |                     }
752 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:773:9
    |
773 | /         if let Some(archive_rel) = archive_rel_for(bob_dir, dest_abs, &contents)
774 | |         {
775 | |             if let Ok(archive) =
776 | |                 std::fs::read_to_string(bob_dir.join(&archive_rel))
...   |
784 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
773 ~         if let Some(archive_rel) = archive_rel_for(bob_dir, dest_abs, &contents)
774 ~             && let Ok(archive) =
775 |                 std::fs::read_to_string(bob_dir.join(&archive_rel))
...
781 |                 );
782 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:797:9
    |
797 | /         if trimmed.starts_with("done_tasks:") {
798 | |             if let Some(start) = trimmed.find("[[") {
799 | |                 if let Some(end) = trimmed[start..].find("]]") {
800 | |                     let target = &trimmed[start + 2..start + end];
...   |
808 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
797 ~         if trimmed.starts_with("done_tasks:")
798 ~             && let Some(start) = trimmed.find("[[") {
799 |                 if let Some(end) = trimmed[start..].find("]]") {
...
806 |                 }
807 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:798:13
    |
798 | /             if let Some(start) = trimmed.find("[[") {
799 | |                 if let Some(end) = trimmed[start..].find("]]") {
800 | |                     let target = &trimmed[start + 2..start + end];
801 | |                     let mut rel = target.trim().to_string();
...   |
807 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
798 ~             if let Some(start) = trimmed.find("[[")
799 ~                 && let Some(end) = trimmed[start..].find("]]") {
800 |                     let target = &trimmed[start + 2..start + end];
...
805 |                     return Some(rel);
806 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/migrate_tasks/plan.rs:811:5
    |
811 | /     if relative.components().count() == 1 {
812 | |         if let Some(stem) = dest_abs.file_stem().and_then(|s| s.to_str()) {
813 | |             return Some(format!("done/{stem}_done.md"));
814 | |         }
815 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
811 ~     if relative.components().count() == 1
812 ~         && let Some(stem) = dest_abs.file_stem().and_then(|s| s.to_str()) {
813 |             return Some(format!("done/{stem}_done.md"));
814 ~         }
    |

warning: `format!` in `format!` args
   --> src/native/ref_library/migrate_tasks/plan.rs:990:20
    |
990 |               return format!(
    |  ____________________^
991 | |                 "{}{}",
992 | |                 &line[..caret + 1],
993 | |                 format!("{new_id}{}", &line[trimmed_end..])
994 | |             );
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
   --> src/native/ref_tasks/walk.rs:634:9
    |
634 | /         if b == b'#' || b == b'^' {
635 | |             if bytes[i + 1].eq_ignore_ascii_case(&b'r')
636 | |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
637 | |                 && bytes[i + 3].eq_ignore_ascii_case(&b'f')
...   |
641 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
634 ~         if (b == b'#' || b == b'^') {
635 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
636 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
639 |                 return true;
640 ~             }
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/successors.rs:1396:29
     |
1396 |             project_states: &project_states,
     |                             ^^^^^^^^^^^^^^^ help: change this to: `project_states`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

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

warning: usage of `bool::then` in `filter_map`
   --> src/native/task_status_hooks/references.rs:521:54
    |
521 |                       targets.extend(identities.iter().filter_map(
    |  ______________________________________________________^
522 | |                         |(path, block)| {
523 | |                             (!project_tree
524 | |                                 .is_internal_target(owner_index, path))
525 | |                             .then(|| (path.clone(), block.clone()))
526 | |                         },
527 | |                     ));
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_map_bool_then
help: use `filter` then `map` instead
    |
521 ~                     targets.extend(identities.iter().filter(|&(path, block)| (!project_tree
522 ~                                 .is_internal_target(owner_index, path))).map(|(path, block)| (path.clone(), block.clone())));
    |

warning: this `if` statement can be collapsed
   --> src/native/task_status_hooks/references.rs:593:5
    |
593 | /     if let Some(Some(task_id)) =
594 | |         task_ids.get(&(target_path.to_path_buf(), block_id.to_string()))
595 | |     {
596 | |         if task
...   |
603 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
594 ~         task_ids.get(&(target_path.to_path_buf(), block_id.to_string()))
595 ~         && task
596 |             .depends_on
...
600 |             return true;
601 ~         }
    |

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:403:5
    |
403 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:270:9
    |
270 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1123:1
     |
1123 | / fn consume_blocked_links_after_compose(
1124 | |     compose: &mut ComposeResult,
1125 | |     files: &[FileScan],
1126 | |     daily_path: &Path,
...    |
1137 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1138 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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

warning: `bob-cli` (lib) generated 111 warnings
error: could not compile `bob-cli` (lib) due to 1 previous error; 111 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: items after a test module
    --> src/native/capture/link_guard.rs:671:1
     |
 671 |   mod tests {
     |   ^^^^^^^^^
...
1007 | / pub(super) fn apply_new_task_project_block(
1008 | |     line: &str,
1009 | |     status_types: &BTreeMap<char, task_status_hooks::TaskStatusType>,
1010 | | ) -> Option<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#items_after_test_module
     = note: `#[warn(clippy::items_after_test_module)]` on by default
     = help: move the items to before the test module was defined

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
    --> src/native/capture_parse.rs:1554:9
     |
1554 | /         for raw in ["Plan =x"] {
1555 | |             let prose = json(raw);
1556 | |             assert_eq!(prose["mode"], "task", "{raw}");
1557 | |             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1558 | |             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1559 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
     = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
     |
1554 ~         {
1555 +             let raw = "Plan =x";
1556 +             let prose = json(raw);
1557 +             assert_eq!(prose["mode"], "task", "{raw}");
1558 +             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1559 +             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1560 +         }
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

warning: equality checks against false can be replaced by a negation
   --> src/native/gkeep/imports.rs:968:17
    |
968 |         assert!(has_verified(&loaded, "note-1", "0123456789ab") == false);
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `!has_verified(&loaded, "note-1", "0123456789ab")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_comparison
    = note: `#[warn(clippy::bool_comparison)]` on by default

warning: items after a test module
   --> src/native/gkeep/list.rs:657:1
    |
657 |   mod source_link_tests {
    |   ^^^^^^^^^^^^^^^^^^^^^
...
680 |   fn footer(plan: &Plan) -> String {
    |   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
...
743 | / fn print_json(
744 | |     args: &ListArgs,
745 | |     vault: &VaultData,
746 | |     keep: Option<&KeepView>,
747 | |     keep_error: Option<&GkeepError>,
748 | |     ref_hints: &RefHints,
749 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:800:9
    |
800 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:832:9
    |
832 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/tests/successor_tests.rs:1181:14
     |
1181 |         Some(&day),
     |              ^^^^ help: change this to: `day`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_status_groups/tests.rs:1443:23
     |
1443 |     assert_idempotent(&crlf);
     |                       ^^^^^ help: change this to: `crlf`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:729:27
    |
729 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:741:27
    |
741 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:753:27
    |
753 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("proj.md", "prj")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:849:27
    |
849 |     assert!(scanned.edges.get(&edge("proj.md", "prj")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("proj.md", "prj"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: `bob-cli` (lib test) generated 131 warnings (111 duplicates)
error: could not compile `bob-cli` (lib test) due to 1 previous error; 131 warnings emitted
error: Recipe `check` failed on line 27 with exit code 101
failed  exit=101  duration=73308ms

