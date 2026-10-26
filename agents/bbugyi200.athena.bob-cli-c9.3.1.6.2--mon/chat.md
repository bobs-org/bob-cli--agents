# Chat History - ace-run (bob-cli-c9.3.1.6.2--mon)

- **TIMESTAMP:** 2026-10-25 20:23:29 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-c9.3.1.6.2--mon

## Prompt

sase monitor start --command 'cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces' --reason 'Verify the assigned family-matching phase before closing its bead'

## Response

sase tool run 992f6ad320188e6acfbc31bbc9c8482d
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

warning: useless use of `format!`
   --> src/native/articles/render.rs:137:25
    |
137 |                         format!("{}", display_path(&plan.path))
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `display_path(&plan.path).to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format
    = note: `#[warn(clippy::useless_format)]` on by default

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

warning: literal with an empty format string
   --> src/native/articles/render.rs:215:9
    |
215 |         "STATE"
    |         ^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#print_literal
    = note: `#[warn(clippy::print_literal)]` on by default
help: try
    |
209 ~         "{}  {}  {}  {}  {}  STATE",
210 |         pad_right("ARTICLE", article_width),
...
213 |         pad_right("TODO", 4),
214 ~         pad_right("FINDINGS", 8)
    |

warning: literal with an empty format string
   --> src/native/articles/render.rs:269:9
    |
269 |         "Preamble",
    |         ^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#print_literal
help: try
    |
267 ~         "  {}  Preamble  {} w",
268 ~         styler.dim("¶"),
    |

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
    --> src/native/capture/dependencies.rs:1976:6
     |
1976 |   ) -> Result<
     |  ______^
1977 | |     (
1978 | |         Vec<MergedMember>,
1979 | |         BTreeSet<(String, String)>,
...    |
1983 | |     CaptureError,
1984 | | > {
     | |_^
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

warning: this `if` statement can be collapsed
    --> src/native/capture/output.rs:1812:5
     |
1812 | /     if result.kind == "pomodoro_start" {
1813 | |         if let Some(start) = result.pomodoro_start.as_ref() {
1814 | |             print_human_pomodoro_start_success(
1815 | |                 result,
...    |
1825 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
     = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
     |
1812 ~     if result.kind == "pomodoro_start"
1813 ~         && let Some(start) = result.pomodoro_start.as_ref() {
1814 |             print_human_pomodoro_start_success(
 ...
1823 |             return;
1824 ~         }
     |

warning: returning the result of a `let` binding from a block
    --> src/native/capture/output.rs:2649:5
     |
2620 | /     let verb = match (update.direction, update.action, dry_run) {
2621 | |         (RelationDirection::To, RelationAction::Added, false) => {
2622 | |             format!("🪢 links to {quoted}{label}{locator}")
...    |
2648 | |     };
     | |______- unnecessary `let` binding
2649 |       verb
     |       ^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#let_and_return
     = note: `#[warn(clippy::let_and_return)]` on by default
help: return the expression directly
     |
2620 ~     
2621 ~     match (update.direction, update.action, dry_run) {
2622 +         (RelationDirection::To, RelationAction::Added, false) => {
2623 ~             format!("🪢 links to {quoted}{label}{locator}")
2624 +         }
2625 +         (RelationDirection::To, RelationAction::Added, true) => {
2626 ~             format!("🪢 would link to {quoted}{label}{locator}")
2627 +         }
2628 +         (RelationDirection::From, RelationAction::Added, false) => {
2629 +             format!(
2630 ~                 "🪢 {quoted} now links here{label}   {} ^{}",
2631 +                 update.source.path, update.source.block_id
2632 +             )
2633 +         }
2634 +         (RelationDirection::From, RelationAction::Added, true) => {
2635 +             format!(
2636 ~                 "🪢 {quoted} would now link here{label}   {} ^{}",
2637 +                 update.source.path, update.source.block_id
2638 +             )
2639 +         }
2640 +         (_, RelationAction::Relabeled, false) => {
2641 ~             format!("🪢 relabeled {quoted}{label}{locator}")
2642 +         }
2643 +         (_, RelationAction::Relabeled, true) => {
2644 ~             format!("🪢 would relabel {quoted}{label}{locator}")
2645 +         }
2646 +         (_, RelationAction::Unchanged, _) => {
2647 ~             format!("🪢 unchanged {quoted}{locator}")
2648 +         }
2649 +     }
     |

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

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:657:9
    |
657 | /         let Some(relative_close) = line[open..].find(')') else {
658 | |             return None;
659 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: manual `rem_euclid` implementation
    --> src/native/capture/pomodoro_adjust.rs:1012:5
     |
1012 |     (((value % 1440) + 1440) % 1440) as u64
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `value.rem_euclid(1440)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_rem_euclid
     = note: `#[warn(clippy::manual_rem_euclid)]` on by default

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

warning: this `map_or` can be simplified
   --> src/native/capture/pomodoro_start.rs:477:20
    |
477 |                 && anchor.map_or(true, |anchor| *index > anchor)
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_map_or
    = note: `#[warn(clippy::unnecessary_map_or)]` on by default
help: use `is_none_or` instead
    |
477 -                 && anchor.map_or(true, |anchor| *index > anchor)
477 +                 && anchor.is_none_or(|anchor| *index > anchor)
    |

warning: the borrowed expression implements the required traits
   --> src/native/capture/project_deps.rs:306:42
    |
306 |         None => match fs::read_to_string(&day_absolute) {
    |                                          ^^^^^^^^^^^^^ help: change this to: `day_absolute`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/capture/project_deps.rs:376:23
    |
376 |         .item_pre_day(&day_absolute)
    |                       ^^^^^^^^^^^^^ help: change this to: `day_absolute`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
    = note: `#[warn(clippy::needless_borrow)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/capture/relations.rs:513:5
    |
513 | /     if action != RelationAction::Unchanged && existing_owner {
514 | |         if let Some(block_id) = owner.block_id.as_deref() {
515 | |             let located = locate_task_by_block_id(
516 | |                 ctx,
...   |
527 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
513 ~     if action != RelationAction::Unchanged && existing_owner
514 ~         && let Some(block_id) = owner.block_id.as_deref() {
515 |             let located = locate_task_by_block_id(
...
525 |             });
526 ~         }
    |

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:904:1
    |
904 | / fn relation_update_json(
905 | |     direction: RelationDirection,
906 | |     source_relative: &Path,
907 | |     source_line: usize,
...   |
912 | |     previous_label: Option<String>,
913 | | ) -> RelationUpdateJson {
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

warning: this `if` statement can be collapsed
    --> src/native/capture_complete/candidates.rs:1249:5
     |
1249 | /     if let Some(identity) = &owner_identity {
1250 | |         if let Some(targets) = graph.get(identity) {
1251 | |             prerequisites.extend(targets.iter().cloned());
1252 | |         }
1253 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1249 ~     if let Some(identity) = &owner_identity
1250 ~         && let Some(targets) = graph.get(identity) {
1251 |             prerequisites.extend(targets.iter().cloned());
1252 ~         }
     |

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

warning: manual case-insensitive ASCII comparison
   --> src/native/capture_complete/engine.rs:594:12
    |
594 |         || content.to_ascii_lowercase() == "@@template:"
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_ignore_case_cmp
    = note: `#[warn(clippy::manual_ignore_case_cmp)]` on by default
help: consider using `.eq_ignore_ascii_case()` instead
    |
594 -         || content.to_ascii_lowercase() == "@@template:"
594 +         || content.eq_ignore_ascii_case("@@template:")
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

warning: this `if` can be collapsed into the outer `match`
   --> src/native/capture_language/completion.rs:422:17
    |
422 | /                 if entry.separator.map(|(start, _)| start) == Some(separator) {
423 | |                     return Some((entry.start, entry.direction, entry.hidden));
424 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
    = note: `#[warn(clippy::collapsible_match)]` on by default
help: collapse nested if block
    |
421 ~             ScannedRelation::Complete(entry)
422 ~                 if entry.separator.map(|(start, _)| start) == Some(separator) => {
423 |                     return Some((entry.start, entry.direction, entry.hidden));
424 ~                 }
    |

warning: taken reference of right operand
   --> src/native/capture_language/dependencies.rs:686:20
    |
686 |                 if raw.as_bytes() == &[sigil] =>
    |                    ^^^^^^^^^^^^^^^^^^--------
    |                                      |
    |                                      help: use the right value directly: `[sigil]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#op_ref
    = note: `#[warn(clippy::op_ref)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/capture_language/draft.rs:671:13
    |
671 | /             if let Some(row) =
672 | |                 super::template::row_number_for_issue(&analysis, first_issue)
673 | |             {
674 | |                 if let Some(execution) = first_leading_execution_error(
...   |
684 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
672 ~                 super::template::row_number_for_issue(&analysis, first_issue)
673 ~                 && let Some(execution) = first_leading_execution_error(
674 |                     raw_text,
...
681 |                     return Err(execution);
682 ~                 }
    |

warning: unnecessary map of the identity function
   --> src/native/capture_language/draft.rs:876:10
    |
876 |           )
    |  __________^
877 | |         .map_err(|error| error)?;
    | |_______________________________^ help: remove the call to `map_err`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity
    = note: `#[warn(clippy::map_identity)]` on by default

warning: unnecessary map of the identity function
   --> src/native/capture_language/editor_classify.rs:717:60
    |
717 |               let (after_x, x_len) = classify_link_close(raw)
    |  ____________________________________________________________^
718 | |                 .map(|(selection, x_len)| (selection, x_len))
    | |_____________________________________________________________^ help: remove the call to `map`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity

warning: this `if` statement can be collapsed
    --> src/native/capture_language/editor_classify.rs:1116:21
     |
1116 | /                     if let Some((timing_offset, timing_text)) = timing.as_ref()
1117 | |                     {
1118 | |                         if !timing_text.is_empty() {
1119 | |                             extra_spans.push(Span {
...    |
1129 | |                     }
     | |_____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1116 ~                     if let Some((timing_offset, timing_text)) = timing.as_ref()
1117 ~                         && !timing_text.is_empty() {
1118 |                             extra_spans.push(Span {
 ...
1126 |                             });
1127 ~                         }
     |

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

warning: this `if` statement can be collapsed
    --> src/native/capture_language/editor_parse.rs:1126:9
     |
1126 | /         if is_standalone_listen_marker(tokens[1].text) {
1127 | |             if let Some(intent) = classify_token(tokens[0].text) {
1128 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
1129 | |                     return None;
...    |
1174 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1126 ~         if is_standalone_listen_marker(tokens[1].text)
1127 ~             && let Some(intent) = classify_token(tokens[0].text) {
1128 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
 ...
1172 |                 });
1173 ~             }
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

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:2081:17
     |
2081 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/capture_language/item.rs:184:9
    |
184 | /         if is_standalone_listen_marker(tokens[1].text) {
185 | |             if let Some(intent) = classify_token(tokens[0].text) {
186 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
187 | |                     return None;
...   |
231 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
184 ~         if is_standalone_listen_marker(tokens[1].text)
185 ~             && let Some(intent) = classify_token(tokens[0].text) {
186 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
...
229 |                 ));
230 ~             }
    |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1349:12
     |
1349 |       } else if !doubled && suffix.is_empty() {
     |  ____________^
1350 | |         if let Some(name_len) = bare_start_name_len(rest) {
1351 | |             name = Some(rest[..name_len].to_string());
1352 | |             name_spelling = Some(NameSpelling::Bare);
...    |
1355 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1349 ~     } else if !doubled && suffix.is_empty()
1350 ~         && let Some(name_len) = bare_start_name_len(rest) {
1351 |             name = Some(rest[..name_len].to_string());
1352 |             name_spelling = Some(NameSpelling::Bare);
1353 |             token_len += name_len;
1354 ~         }
     |

warning: match expression looks like `matches!` macro
    --> src/native/capture_language/item.rs:1392:31
     |
1392 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
1393 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1394 | |                 (false, '~', Some(b'@')) => true,
1395 | |                 _ => false,
1396 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
1392 -             let want_second = match (name.is_some(), first_sigil, second) {
1393 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1394 -                 (false, '~', Some(b'@')) => true,
1395 -                 _ => false,
1396 -             };
1392 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:1710:1
     |
1710 | / pub(super) fn named_shape_error_with_drop(
1711 | |     token: &str,
1712 | |     suffix: &str,
1713 | |     name: &str,
...    |
1718 | |     is_literal: bool,
1719 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1853:5
     |
1853 | /     if let Some((_, after_tilde)) = drop {
1854 | |         if lex_start_drop(&after_tilde, 0, nospace)
1855 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1856 | |             == false
...    |
1860 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1853 ~     if let Some((_, after_tilde)) = drop
1854 ~         && lex_start_drop(&after_tilde, 0, nospace)
1855 |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
 ...
1858 |             return false;
1859 ~         }
     |

warning: equality checks against false can be replaced by a negation
    --> src/native/capture_language/item.rs:1854:12
     |
1854 |           if lex_start_drop(&after_tilde, 0, nospace)
     |  ____________^
1855 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1856 | |             == false
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_comparison
     = note: `#[warn(clippy::bool_comparison)]` on by default
help: try
     |
1854 ~         if !lex_start_drop(&after_tilde, 0, nospace)
1855 +             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1862:5
     |
1862 | /     if let Some((_, after_at)) = timing {
1863 | |         if parse_pomodoro_start_suffix(&after_at).is_err() {
1864 | |             return false;
1865 | |         }
1866 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1862 ~     if let Some((_, after_at)) = timing
1863 ~         && parse_pomodoro_start_suffix(&after_at).is_err() {
1864 |             return false;
1865 ~         }
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2192:31
     |
2192 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
2192 -                 Err(error) => return Err(error.message),
2192 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2200:21
     |
2200 | /                     return Err(close_inline_dangling_error(
2201 | |                         &head, index, plain,
2202 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
2200 ~                     Err(close_inline_dangling_error(
2201 +                         &head, index, plain,
2202 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2238:21
     |
2238 | /                     return Ok(Some(parsed_capture_item_outcome(
2239 | |                         item,
2240 | |                         ParsedCaptureText {
2241 | |                             body,
...    |
2254 | |                         None,
2255 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
2238 ~                     Ok(Some(parsed_capture_item_outcome(
2239 +                         item,
2240 +                         ParsedCaptureText {
2241 +                             body,
2242 +                             clip: None,
2243 +                             route: None,
2244 +                             kind: CaptureKind::PomodoroClose { spec },
2245 +                             scheduled_offset: None,
2246 +                             priority_level: None,
2247 +                             sub_bullets: Vec::new(),
2248 +                             dependencies: Vec::new(),
2249 +                             blocked_tasks: Vec::new(),
2250 +                             relations: Vec::new(),
2251 +                             dependency_target: None,
2252 +                         },
2253 +                         Vec::new(),
2254 +                         None,
2255 ~                     )))
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

warning: useless use of `format!`
   --> src/native/capture_language/relations.rs:752:17
    |
752 |                 format!("relation label is empty after trimming")
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `"relation label is empty after trimming".to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format

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

warning: this `if` statement can be collapsed
   --> src/native/capture_language/template.rs:181:5
    |
181 | /     if let Some((_, line_number)) = analysis.header.as_ref() {
182 | |         if let Some(line) = lines.get(line_number.saturating_sub(1)) {
183 | |             bytes[line.start..line.end].fill(b' ');
184 | |         }
185 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
181 ~     if let Some((_, line_number)) = analysis.header.as_ref()
182 ~         && let Some(line) = lines.get(line_number.saturating_sub(1)) {
183 |             bytes[line.start..line.end].fill(b' ');
184 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/capture_language/template.rs:387:5
    |
387 | /     if !fields_used.is_empty() {
388 | |         if fields_used.iter().copied().ne(0..field_count) {
389 | |             let missing = (0..field_count)
390 | |                 .find(|index| !fields_used.contains(index))
...   |
421 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
387 ~     if !fields_used.is_empty()
388 ~         && fields_used.iter().copied().ne(0..field_count) {
389 |             let missing = (0..field_count)
...
419 |             ));
420 ~         }
    |

warning: returning the result of a `let` binding from a block
   --> src/native/capture_language/template.rs:406:17
    |
401 | /                 let shown = fields_used
402 | |                     .iter()
403 | |                     .map(|field| format!("{{{field}}}"))
404 | |                     .collect::<Vec<_>>()
405 | |                     .join(" and ");
    | |___________________________________- unnecessary `let` binding
406 |                   shown
    |                   ^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#let_and_return
help: return the expression directly
    |
401 ~                 
402 ~                 fields_used
403 +                     .iter()
404 +                     .map(|field| format!("{{{field}}}"))
405 +                     .collect::<Vec<_>>()
406 +                     .join(" and ")
    |

warning: unnecessary map of the identity function
   --> src/native/capture_language/tokens.rs:782:55
    |
782 |       let spec = parse_pomodoro_start_suffix(&effective).map_err(|message| {
    |  _______________________________________________________^
783 | |         // A glued timing (`=3bugs`) already returned above via the length
784 | |         // check; any remaining effective failure is overflow/invalid timing.
785 | |         message
786 | |     })?;
    | |______^ help: remove the call to `map_err`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity

warning: redundant guard
   --> src/native/capture_language/tokens.rs:961:43
    |
961 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
    |
961 -                 Some((after_x, x_len)) if after_x.is_empty() => {
961 +                 Some(("", x_len)) => {
    |

warning: unnecessary map of the identity function
    --> src/native/capture_language/tokens.rs:1721:59
     |
1721 |       let (after_x, x_len) = classify_link_close(raw_suffix)
     |  ___________________________________________________________^
1722 | |         .map(|(selection, x_len)| (selection, x_len))
     | |_____________________________________________________^ help: remove the call to `map`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#map_identity

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:2228:13
     |
2228 | /             return Ok(Some(parsed_capture_item_outcome(
2229 | |                 item,
2230 | |                 ParsedCaptureText {
2231 | |                     body: String::new(),
...    |
2252 | |                 Some(marker_text),
2253 | |             )));
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
2228 ~             Ok(Some(parsed_capture_item_outcome(
2229 +                 item,
2230 +                 ParsedCaptureText {
2231 +                     body: String::new(),
2232 +                     clip: None,
2233 +                     route: Some(route),
2234 +                     kind: CaptureKind::PomodoroLink {
2235 +                         block_id: parts.block_id,
2236 +                         pomodoro_name: parts.pomodoro_name,
2237 +                         pomodoro_name_is_literal: parts
2238 +                             .pomodoro_name_is_literal,
2239 +                         start: parts.start,
2240 +                         close: parts.close,
2241 +                         spelling: PomodoroLinkSpelling::Caret,
2242 +                     },
2243 +                     scheduled_offset: None,
2244 +                     priority_level: None,
2245 +                     sub_bullets: Vec::new(),
2246 +                     dependencies: Vec::new(),
2247 +                     blocked_tasks: Vec::new(),
2248 +                     relations: Vec::new(),
2249 +                     dependency_target: None,
2250 +                 },
2251 +                 Vec::new(),
2252 +                 Some(marker_text),
2253 ~             )))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:2317:13
     |
2317 |             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
     |
2317 -             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
2317 +             Err(POMODORO_LINK_SHAPE_ERROR.to_string())
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_parse.rs:1177:9
     |
1177 | /         if let Some(diagnostic) = refusal_diagnostic(
1178 | |             &parsed.spans,
1179 | |             parsed.mode,
1180 | |             &parsed.pomodoro_start,
...    |
1188 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1184 ~         )
1185 ~             && diagnostic.code != "template_clipboard" {
1186 |                 refusal_diagnostics.push(diagnostic);
1187 ~             }
     |

warning: redundant closure
    --> src/native/capture_parse.rs:1204:29
     |
1204 |             .unwrap_or_else(|| empty_wire_item());
     |                             ^^^^^^^^^^^^^^^^^^^^ help: replace the closure with the function itself: `empty_wire_item`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_closure
     = note: `#[warn(clippy::redundant_closure)]` on by default

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

warning: this `if` statement can be collapsed
   --> src/native/capture_related/draft.rs:380:5
    |
380 | /     if let Some(global) = global.filter(|global| global.block_id.is_some()) {
381 | |         if item.local_destination_markers.is_empty() {
382 | |             if let (Some(route), Some(block_id)) =
383 | |                 (&global.route, &global.block_id)
...   |
392 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
380 ~     if let Some(global) = global.filter(|global| global.block_id.is_some())
381 ~         && item.local_destination_markers.is_empty() {
382 |             if let (Some(route), Some(block_id)) =
...
390 |             }
391 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/capture_related/draft.rs:381:9
    |
381 | /         if item.local_destination_markers.is_empty() {
382 | |             if let (Some(route), Some(block_id)) =
383 | |                 (&global.route, &global.block_id)
...   |
391 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
381 ~         if item.local_destination_markers.is_empty()
382 ~             && let (Some(route), Some(block_id)) =
383 |                 (&global.route, &global.block_id)
...
389 |                 ));
390 ~             }
    |

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:429:1
    |
429 | / fn draft_match(
430 | |     ranked: bands::RankedMatch<'_>,
431 | |     item: &EditorItemParse,
432 | |     draft: &str,
...   |
437 | |     index: &NoteIndex,
438 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:560:1
    |
560 | / fn verify_link_action(
561 | |     action: &str,
562 | |     item: &EditorItemParse,
563 | |     draft: &str,
...   |
568 | |     options: &EditorParseOptions<'_>,
569 | | ) -> bool {
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

warning: the borrowed expression implements the required traits
   --> src/native/env.rs:304:13
    |
304 |             &dir.join(file_name),
    |             ^^^^^^^^^^^^^^^^^^^^ help: change this to: `dir.join(file_name)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

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
   --> src/native/highlights_ref/create.rs:584:5
    |
584 | /     if let Some(name) = matches.get_one::<String>("name") {
585 | |         if let Err(error) = super::clip_url::validate_name(name) {
586 | |             let styler = Styler::detect();
587 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
590 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
584 ~     if let Some(name) = matches.get_one::<String>("name")
585 ~         && let Err(error) = super::clip_url::validate_name(name) {
586 |             let styler = Styler::detect();
587 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
588 |             return 1;
589 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:592:5
    |
592 | /     if let Some(ref_type) = &ref_type {
593 | |         if let Err(error) = validate_ref_type(ref_type) {
594 | |             let styler = Styler::detect();
595 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
598 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
592 ~     if let Some(ref_type) = &ref_type
593 ~         && let Err(error) = validate_ref_type(ref_type) {
594 |             let styler = Styler::detect();
595 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
596 |             return 1;
597 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:599:5
    |
599 | /     if let Some(published) = matches.get_one::<String>("published") {
600 | |         if let Err(error) = super::clip_url::validate_published(published) {
601 | |             let styler = Styler::detect();
602 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
605 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
599 ~     if let Some(published) = matches.get_one::<String>("published")
600 ~         && let Err(error) = super::clip_url::validate_published(published) {
601 |             let styler = Styler::detect();
602 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
603 |             return 1;
604 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:661:5
    |
661 | /     if !matches!(prepared, PreparedTarget::VaultNote { .. })
662 | |         && parent_input.is_none()
663 | |         && reread.is_none()
...   |
670 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
663 ~         && reread.is_none()
664 ~         && let Some(code) = check_duplicate_before_parent(
665 |             &config, &target_os, &prepared, matches, force,
666 |         ) {
667 |             return code;
668 ~         }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/create.rs:1097:13
     |
1097 | /             if listen {
1098 | |                 if let Some(hit) = sources_mod::find_refusing_hit(
1099 | |                     &recorded,
1100 | |                     &dedupe_key,
...    |
1153 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1097 ~             if listen
1098 ~                 && let Some(hit) = sources_mod::find_refusing_hit(
1099 |                     &recorded,
 ...
1151 |                     }
1152 ~                 }
     |

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1715:1
     |
1715 | / fn plan_target_for(
1716 | |     config: &Config,
1717 | |     stem: &str,
1718 | |     ref_type: &str,
...    |
1723 | |     source_display: &str,
1724 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `match` expression can be replaced with `?`
    --> src/native/highlights_ref/create.rs:2707:17
     |
2707 | /                 match companion_mod::copy_audio_for_install(plan.audio.as_ref())
2708 | |                 {
2709 | |                     Ok(created) => created,
2710 | |                     Err(error) => return Err(error),
2711 | |                 }
     | |_________________^ help: try instead: `companion_mod::copy_audio_for_install(plan.audio.as_ref())?`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:3564:1
     |
3564 | / fn print_pdf_dry_run(
3565 | |     config: &Config,
3566 | |     styler: &Styler,
3567 | |     source_display: &str,
...    |
3575 | |     legacy: &[sources_mod::RecordedSource],
3576 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:3800:1
     |
3800 | / fn compose_markdown_marker(
3801 | |     status: &str,
3802 | |     parent: &str,
3803 | |     title: &str,
...    |
3808 | |     return_links: bool,
3809 | | ) -> Result<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:278:5
    |
278 | /     if !unit.is_library_pdf() {
279 | |         if let Err(failure) = session.pre_sync() {
280 | |             return IntakeOutcome::Queued {
281 | |                 path,
...   |
286 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
278 ~     if !unit.is_library_pdf()
279 ~         && let Err(failure) = session.pre_sync() {
280 |             return IntakeOutcome::Queued {
...
284 |             };
285 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:818:5
    |
818 | /     if let IntakeUnit::Audio { .. } = unit {
819 | |         if !pdf.with_extension("pdf").is_file() {
820 | |             return Err(QueueFailure::new(
821 | |                 QueueReason::Collision,
...   |
828 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
818 ~     if let IntakeUnit::Audio { .. } = unit
819 ~         && !pdf.with_extension("pdf").is_file() {
820 |             return Err(QueueFailure::new(
...
826 |             ));
827 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:867:9
    |
867 | /         if let Some(parent) = moved.to.parent() {
868 | |             if let Err(error) = fs::create_dir_all(parent) {
869 | |                 let detail = format!("create {}: {error}", parent.display());
870 | |                 return Err(rollback_moves(&mut completed, detail));
871 | |             }
872 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
867 ~         if let Some(parent) = moved.to.parent()
868 ~             && let Err(error) = fs::create_dir_all(parent) {
869 |                 let detail = format!("create {}: {error}", parent.display());
870 |                 return Err(rollback_moves(&mut completed, detail));
871 ~             }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/intake.rs:1227:13
     |
1227 | /             if report.filed_count() > 0 {
1228 | |                 if let Some(warning) =
1229 | |                     intake_status::record_success(COMMAND, report.filed_count())
...    |
1233 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1227 ~             if report.filed_count() > 0
1228 ~                 && let Some(warning) =
1229 |                     intake_status::record_success(COMMAND, report.filed_count())
1230 |                 {
1231 |                     eprintln!("{warning}");
1232 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/intake.rs:1243:13
     |
1243 | /             if let Some((reason, detail)) = stuck {
1244 | |                 if let Some(warning) =
1245 | |                     intake_status::record_failure(COMMAND, reason, detail)
...    |
1249 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1243 ~             if let Some((reason, detail)) = stuck
1244 ~                 && let Some(warning) =
1245 |                     intake_status::record_failure(COMMAND, reason, detail)
1246 |                 {
1247 |                     eprintln!("{warning}");
1248 ~                 }
     |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:163:17
    |
163 | /                 if title.is_none() {
164 | |                     title = value;
165 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
162 ~             "title"
163 ~                 if title.is_none() => {
164 |                     title = value;
165 ~                 }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:168:17
    |
168 | /                 if value.is_some_and(|value| !value.is_empty()) {
169 | |                     has_audio = true;
170 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
167 ~             "audio"
168 ~                 if value.is_some_and(|value| !value.is_empty()) => {
169 |                     has_audio = true;
170 ~                 }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:246:21
    |
246 | /                     if source_pdf.is_none() {
247 | |                         source_pdf = entry.value.as_ref().and_then(|value| {
248 | |                             value.as_string().map(str::to_string)
249 | |                         });
250 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
245 ~                 "source_pdf"
246 ~                     if source_pdf.is_none() => {
247 |                         source_pdf = entry.value.as_ref().and_then(|value| {
248 |                             value.as_string().map(str::to_string)
249 |                         });
250 ~                     }
    |

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:253:21
    |
253 | /                     if entry.value.as_ref().is_some_and(|value| {
254 | |                         value.as_string().is_some_and(|value| !value.is_empty())
255 | |                     }) {
256 | |                         has_audio = true;
257 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
252 ~                 "audio"
253 |                     if entry.value.as_ref().is_some_and(|value| {
254 |                         value.as_string().is_some_and(|value| !value.is_empty())
255 ~                     }) => {
256 |                         has_audio = true;
257 ~                     }
    |

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/attach.rs:338:1
    |
338 | / pub(super) fn run_attach(
339 | |     config: &Config,
340 | |     listen: &ListenCommand,
341 | |     attach: &AttachTarget,
...   |
346 | |     scratch: &mut super::ScratchDir,
347 | | ) -> Result<()> {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: clamp-like pattern without using clamp function
   --> src/native/highlights_ref/clip_adapter.rs:735:5
    |
735 | /     DIAGRAM_TIMEOUT_BASE_SECS
736 | |         .saturating_add(
737 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
740 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
735 ~     DIAGRAM_TIMEOUT_BASE_SECS
736 +         .saturating_add(
737 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
738 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: this `match` expression can be replaced with `?`
   --> src/native/highlights_ref/collection.rs:173:25
    |
173 |       let resolved_name = match collection_name::resolve_collection_name(
    |  _________________________^
174 | |         options.name.as_deref(),
175 | |         output_stem,
176 | |         options.title.as_deref(),
...   |
180 | |         Err(error) => return Err(error),
181 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark
help: try instead
    |
173 ~     let resolved_name = collection_name::resolve_collection_name(
174 +         options.name.as_deref(),
175 +         output_stem,
176 +         options.title.as_deref(),
177 +         &urls,
178 ~     )?;
    |

warning: this `match` expression can be replaced with `?`
   --> src/native/highlights_ref/collection.rs:319:33
    |
319 |               let resolved_name = match collection_name::resolve_collection_name(
    |  _________________________________^
320 | |                 options.name.as_deref(),
321 | |                 output_stem,
322 | |                 options.title.as_deref(),
...   |
326 | |                 Err(error) => return Err(error),
327 | |             };
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark
help: try instead
    |
319 ~             let resolved_name = collection_name::resolve_collection_name(
320 +                 options.name.as_deref(),
321 +                 output_stem,
322 +                 options.title.as_deref(),
323 +                 urls,
324 ~             )?;
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/highlights_ref/collection.rs:373:9
    |
373 | /         &reread_title_fallback(
374 | |             matches.get_one::<String>("name").map(String::as_str),
375 | |             urls,
376 | |         ),
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
help: change this to
    |
373 ~         reread_title_fallback(
374 +             matches.get_one::<String>("name").map(String::as_str),
375 +             urls,
376 ~         ),
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/highlights_ref/collection.rs:593:13
    |
593 |             &reread_title_fallback(options.name.as_deref(), urls),
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `reread_title_fallback(options.name.as_deref(), urls)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: redundant closure
   --> src/native/highlights_ref/collection_name.rs:155:27
    |
155 |         parsed.iter().map(|url| slug_words(url)).collect();
    |                           ^^^^^^^^^^^^^^^^^^^^^ help: replace the closure with the function itself: `slug_words`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_closure

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/highlights_ref/collection_name.rs:160:65
    |
160 |         if is_useful_name(&shared.words, allows_one_word_series(&urls, &parsed))
    |                                                                 ^^^^^ help: change this to: `urls`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: unneeded `return` statement
   --> src/native/highlights_ref/collection_name.rs:218:13
    |
218 |             return Ok(ResolvedName { name, source });
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
    |
218 -             return Ok(ResolvedName { name, source });
218 +             Ok(ResolvedName { name, source })
    |

warning: unneeded `return` statement
   --> src/native/highlights_ref/collection_name.rs:230:13
    |
230 | /             return Err(CommandError::new(name_error_message(urls, &reason))
231 | |                 .with_exit_code(2));
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
    |
230 ~             Err(CommandError::new(name_error_message(urls, &reason))
231 ~                 .with_exit_code(2))
    |

warning: this loop could be written as a `for` loop
   --> src/native/highlights_ref/collection_name.rs:669:5
    |
669 |     while let Some((byte_index, first_char)) = chars.next() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `for (byte_index, first_char) in chars`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#while_let_on_iterator
    = note: `#[warn(clippy::while_let_on_iterator)]` on by default

warning: using `contains()` instead of `iter().any()` is more efficient
   --> src/native/highlights_ref/continuation.rs:192:13
    |
192 |         if !distinct.iter().any(|seen| *seen == label) {
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `distinct.contains(&label)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_contains
    = note: `#[warn(clippy::manual_contains)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/doctor.rs:801:9
    |
801 | /         if duplicate {
802 | |             if let Some(id) = row.id.as_deref() {
803 | |                 duplicated
804 | |                     .entry(id.to_ascii_lowercase())
...   |
808 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
801 ~         if duplicate
802 ~             && let Some(id) = row.id.as_deref() {
803 |                 duplicated
...
806 |                     .push(row.path.as_str());
807 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/duplicate.rs:156:17
    |
156 | /                 if title == title_fallback || title.is_empty() {
157 | |                     if let Some(note_title) = note_title(&hit.path) {
158 | |                         title = note_title;
159 | |                     }
160 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
156 ~                 if (title == title_fallback || title.is_empty()) {
157 ~                     && let Some(note_title) = note_title(&hit.path) {
158 |                         title = note_title;
159 ~                     }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/duplicate.rs:164:17
    |
164 | /                 if title == title_fallback || title.is_empty() {
165 | |                     if let Some(marker_title) = queued_title(&hit.path) {
166 | |                         title = marker_title;
167 | |                     }
168 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
164 ~                 if (title == title_fallback || title.is_empty()) {
165 ~                     && let Some(marker_title) = queued_title(&hit.path) {
166 |                         title = marker_title;
167 ~                     }
    |

warning: unneeded `return` statement
  --> src/native/highlights_ref/io.rs:26:9
   |
26 | /         return if status == 0 {
27 | |             Ok(())
28 | |         } else {
29 | |             Err(std::io::Error::last_os_error())
30 | |         };
   | |_________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_return
help: remove `return`
   |
26 ~         if status == 0 {
27 +             Ok(())
28 +         } else {
29 +             Err(std::io::Error::last_os_error())
30 ~         }
   |

warning: you should use the `starts_with` method
   --> src/native/highlights_ref/listen.rs:690:23
    |
690 |     if length == 0 || rest[length..].chars().next() != Some('}') {
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: like this: `!rest[length..].starts_with('}')`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#chars_next_cmp
    = note: `#[warn(clippy::chars_next_cmp)]` on by default

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:688:1
    |
688 | / pub(super) enum PdfSyncOutcome {
689 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
690 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
691 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
689 -     Written(SyncWriteReport),
689 +     Written(Box<SyncWriteReport>),
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:743:1
    |
743 | / pub(super) enum ScanWriteOutcome {
744 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
745 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
746 | |     Failed(ScanFailure),
747 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
744 -     Written(SyncWriteReport),
744 +     Written(Box<SyncWriteReport>),
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

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:345:5
    |
345 | /     if path.components().count() > 1 && path.is_relative() {
346 | |         if let Ok(cwd) = std::env::current_dir() {
347 | |             return cwd.join(path);
348 | |         }
349 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
345 ~     if path.components().count() > 1 && path.is_relative()
346 ~         && let Ok(cwd) = std::env::current_dir() {
347 |             return cwd.join(path);
348 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:356:5
    |
356 | /     if path.is_relative() {
357 | |         if let Ok(cwd) = std::env::current_dir() {
358 | |             return cwd.join(path);
359 | |         }
360 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
356 ~     if path.is_relative()
357 ~         && let Ok(cwd) = std::env::current_dir() {
358 |             return cwd.join(path);
359 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:376:16
    |
376 |           } else if line.contains("Overfull") {
    |  ________________^
377 | |             if let Some(width) = overfull_width_pt(line) {
378 | |                 if width > 20.0 {
379 | |                     let key = format!("overfull:{line}");
...   |
387 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
376 ~         } else if line.contains("Overfull")
377 ~             && let Some(width) = overfull_width_pt(line) {
378 |                 if width > 20.0 {
...
385 |                 }
386 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:377:13
    |
377 | /             if let Some(width) = overfull_width_pt(line) {
378 | |                 if width > 20.0 {
379 | |                     let key = format!("overfull:{line}");
380 | |                     if seen.insert(key) {
...   |
386 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
377 ~             if let Some(width) = overfull_width_pt(line)
378 ~                 && width > 20.0 {
379 |                     let key = format!("overfull:{line}");
...
384 |                     }
385 ~                 }
    |

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

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/classify.rs:505:13
    |
505 | /             if let Some(canonical) = vault.existing_vault_file(&parsed) {
506 | |                 if vault_member_relative(store.vault_root(), &canonical)
507 | |                     .is_none()
508 | |                     && markdown_extension(&canonical)
...   |
517 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
505 ~             if let Some(canonical) = vault.existing_vault_file(&parsed)
506 ~                 && vault_member_relative(store.vault_root(), &canonical)
507 |                     .is_none()
...
515 |                     return Ok(SnapshotTarget::PlainMarkdown(canonical));
516 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/obsidian.rs:940:13
    |
940 | /             if is_single_embed_line(&line.text) {
941 | |                 if let Some(block) = self.parse_line_embed(line) {
942 | |                     blocks.push(block);
943 | |                     index += 1;
...   |
946 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
940 ~             if is_single_embed_line(&line.text)
941 ~                 && let Some(block) = self.parse_line_embed(line) {
942 |                     blocks.push(block);
943 |                     index += 1;
944 |                     continue;
945 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/obsidian.rs:976:9
    |
976 | /         if let Some(rest) = trimmed.strip_prefix('!') {
977 | |             if let Some(image) =
978 | |                 self.parse_markdown_image_line(rest, line.line_no)
...   |
982 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
976 ~         if let Some(rest) = trimmed.strip_prefix('!')
977 ~             && let Some(image) =
978 |                 self.parse_markdown_image_line(rest, line.line_no)
979 |             {
980 |                 return Some(image);
981 ~             }
    |

warning: you seem to be trying to use `match` for destructuring a single pattern. Consider using `if let`
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1210:13
     |
1210 | /             match block_id {
1211 | |                 Some(id) => {
1212 | |                     let tid = self.claim_anchor_id(&format!("t-{id}"));
1213 | |                     let anchor = self.push_anchor(AnchorKind::Block, id, tid);
...    |
1216 | |                 None => {}
1217 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_match
     = note: `#[warn(clippy::single_match)]` on by default
help: try
     |
1210 ~             if let Some(id) = block_id {
1211 +                 let tid = self.claim_anchor_id(&format!("t-{id}"));
1212 +                 let anchor = self.push_anchor(AnchorKind::Block, id, tid);
1213 +                 content.push(Inline::Anchor(anchor));
1214 +             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1272:9
     |
1272 | /         if let Some(first) = inner.first() {
1273 | |             if let Some((parsed_kind, parsed_title)) =
1274 | |                 parse_callout_header(&first.text)
...    |
1280 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1272 ~         if let Some(first) = inner.first()
1273 ~             && let Some((parsed_kind, parsed_title)) =
1274 |                 parse_callout_header(&first.text)
 ...
1278 |                 inner.remove(0);
1279 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1429:5
     |
1429 | /     if let Some(rest) = trimmed.strip_prefix('!') {
1430 | |         if let Some((_, after)) = split_balanced(rest, '[', ']') {
1431 | |             if after.starts_with('(') {
1432 | |                 if let Some((_, tail)) = split_balanced(&after, '(', ')') {
...    |
1437 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1429 ~     if let Some(rest) = trimmed.strip_prefix('!')
1430 ~         && let Some((_, after)) = split_balanced(rest, '[', ']') {
1431 |             if after.starts_with('(') {
 ...
1435 |             }
1436 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1430:9
     |
1430 | /         if let Some((_, after)) = split_balanced(rest, '[', ']') {
1431 | |             if after.starts_with('(') {
1432 | |                 if let Some((_, tail)) = split_balanced(&after, '(', ')') {
1433 | |                     return tail.trim().is_empty();
...    |
1436 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1430 ~         if let Some((_, after)) = split_balanced(rest, '[', ']')
1431 ~             && after.starts_with('(') {
1432 |                 if let Some((_, tail)) = split_balanced(&after, '(', ')') {
1433 |                     return tail.trim().is_empty();
1434 |                 }
1435 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1431:13
     |
1431 | /             if after.starts_with('(') {
1432 | |                 if let Some((_, tail)) = split_balanced(&after, '(', ')') {
1433 | |                     return tail.trim().is_empty();
1434 | |                 }
1435 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1431 ~             if after.starts_with('(')
1432 ~                 && let Some((_, tail)) = split_balanced(&after, '(', ')') {
1433 |                     return tail.trim().is_empty();
1434 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1560:5
     |
1560 | /     if let Some(path) = target.strip_suffix('"') {
1561 | |         if let Some(bare) = path.rsplit_once(" \"") {
1562 | |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1563 | |         }
1564 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1560 ~     if let Some(path) = target.strip_suffix('"')
1561 ~         && let Some(bare) = path.rsplit_once(" \"") {
1562 |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1563 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1565:5
     |
1565 | /     if let Some(path) = target.strip_suffix('\'') {
1566 | |         if let Some(bare) = path.rsplit_once(" '") {
1567 | |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1568 | |         }
1569 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1565 ~     if let Some(path) = target.strip_suffix('\'')
1566 ~         && let Some(bare) = path.rsplit_once(" '") {
1567 |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1568 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1570:5
     |
1570 | /     if let Some(path) = target.strip_suffix(')') {
1571 | |         if let Some(bare) = path.rsplit_once(" (") {
1572 | |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1573 | |         }
1574 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1570 ~     if let Some(path) = target.strip_suffix(')')
1571 ~         && let Some(bare) = path.rsplit_once(" (") {
1572 |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1573 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1758:9
     |
1758 | /         if rest.starts_with('`') && !is_escaped(text, cursor) {
1759 | |             if let Some((content, consumed)) = match_code_span(text, cursor) {
1760 | |                 if is_inline_query(&content) {
1761 | |                     return Some((
...    |
1775 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1758 ~         if rest.starts_with('`') && !is_escaped(text, cursor)
1759 ~             && let Some((content, consumed)) = match_code_span(text, cursor) {
1760 |                 if is_inline_query(&content) {
 ...
1773 |                 return Some((vec![Inline::Code(content)], consumed));
1774 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1776:9
     |
1776 | /         if rest.starts_with("![[") {
1777 | |             if let Some(end) = rest.find("]]") {
1778 | |                 let inner = rest[3..end].to_string();
1779 | |                 if !inner.contains("[[") {
...    |
1784 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1776 ~         if rest.starts_with("![[")
1777 ~             && let Some(end) = rest.find("]]") {
1778 |                 let inner = rest[3..end].to_string();
 ...
1782 |                 }
1783 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1785:9
     |
1785 | /         if rest.starts_with("[[") {
1786 | |             if let Some(end) = rest.find("]]") {
1787 | |                 let inner = rest[2..end].to_string();
1788 | |                 let tail = rest[end + 2..].to_string();
...    |
1793 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1785 ~         if rest.starts_with("[[")
1786 ~             && let Some(end) = rest.find("]]") {
1787 |                 let inner = rest[2..end].to_string();
 ...
1791 |                 return Some((inlines, end + 2 + extra));
1792 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1794:9
     |
1794 | /         if rest.starts_with("![") && !rest.starts_with("![[") {
1795 | |             if let Some(link) =
1796 | |                 self.match_markdown_link(text, cursor, line_no, true)
...    |
1800 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1794 ~         if rest.starts_with("![") && !rest.starts_with("![[")
1795 ~             && let Some(link) =
1796 |                 self.match_markdown_link(text, cursor, line_no, true)
1797 |             {
1798 |                 return Some(link);
1799 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1819:9
     |
1819 | /         if rest.starts_with('(') {
1820 | |             if let Some((key, value, len)) = match_bracket_field(rest) {
1821 | |                 if BOOKKEEPING_FIELDS.contains(&key.as_str()) {
1822 | |                     return Some((Vec::new(), len));
...    |
1831 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1819 ~         if rest.starts_with('(')
1820 ~             && let Some((key, value, len)) = match_bracket_field(rest) {
1821 |                 if BOOKKEEPING_FIELDS.contains(&key.as_str()) {
 ...
1829 |                 ));
1830 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1832:9
     |
1832 | /         if rest.starts_with("~~") {
1833 | |             if let Some((inner, consumed)) = match_delimited(rest, "~~") {
1834 | |                 let content = self.parse_inlines(&inner, line_no);
1835 | |                 return Some((vec![Inline::Strike(content)], consumed));
1836 | |             }
1837 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1832 ~         if rest.starts_with("~~")
1833 ~             && let Some((inner, consumed)) = match_delimited(rest, "~~") {
1834 |                 let content = self.parse_inlines(&inner, line_no);
1835 |                 return Some((vec![Inline::Strike(content)], consumed));
1836 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1838:9
     |
1838 | /         if rest.starts_with("**") {
1839 | |             if let Some((inner, consumed)) = match_delimited(rest, "**") {
1840 | |                 let content = self.parse_inlines(&inner, line_no);
1841 | |                 return Some((vec![Inline::Strong(content)], consumed));
1842 | |             }
1843 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1838 ~         if rest.starts_with("**")
1839 ~             && let Some((inner, consumed)) = match_delimited(rest, "**") {
1840 |                 let content = self.parse_inlines(&inner, line_no);
1841 |                 return Some((vec![Inline::Strong(content)], consumed));
1842 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1844:9
     |
1844 | /         if rest.starts_with("__") {
1845 | |             if let Some((inner, consumed)) =
1846 | |                 match_delimited_underscore(rest, 2, prev)
...    |
1851 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1844 ~         if rest.starts_with("__")
1845 ~             && let Some((inner, consumed)) =
1846 |                 match_delimited_underscore(rest, 2, prev)
 ...
1849 |                 return Some((vec![Inline::Strong(content)], consumed));
1850 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1852:9
     |
1852 | /         if rest.starts_with('*') {
1853 | |             if let Some((inner, consumed)) = match_delimited(rest, "*") {
1854 | |                 let content = self.parse_inlines(&inner, line_no);
1855 | |                 return Some((vec![Inline::Emphasis(content)], consumed));
1856 | |             }
1857 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1852 ~         if rest.starts_with('*')
1853 ~             && let Some((inner, consumed)) = match_delimited(rest, "*") {
1854 |                 let content = self.parse_inlines(&inner, line_no);
1855 |                 return Some((vec![Inline::Emphasis(content)], consumed));
1856 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1858:9
     |
1858 | /         if rest.starts_with('_') {
1859 | |             if let Some((inner, consumed)) =
1860 | |                 match_delimited_underscore(rest, 1, prev)
...    |
1865 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1858 ~         if rest.starts_with('_')
1859 ~             && let Some((inner, consumed)) =
1860 |                 match_delimited_underscore(rest, 1, prev)
 ...
1863 |                 return Some((vec![Inline::Emphasis(content)], consumed));
1864 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1866:9
     |
1866 | /         if rest.starts_with('#') {
1867 | |             if let Some((tag, len)) = match_tag(text, cursor) {
1868 | |                 if STRUCTURAL_TAGS.contains(&tag.as_str()) {
1869 | |                     return Some((Vec::new(), len));
...    |
1876 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1866 ~         if rest.starts_with('#')
1867 ~             && let Some((tag, len)) = match_tag(text, cursor) {
1868 |                 if STRUCTURAL_TAGS.contains(&tag.as_str()) {
 ...
1874 |                 ));
1875 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1887:9
     |
1887 | /         if rest.starts_with('^') && is_word_boundary(prev) {
1888 | |             if let Some((label, len)) = match_caret_residue_label(rest) {
1889 | |                 return Some((vec![Inline::Text(label)], len));
1890 | |             }
1891 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1887 ~         if rest.starts_with('^') && is_word_boundary(prev)
1888 ~             && let Some((label, len)) = match_caret_residue_label(rest) {
1889 |                 return Some((vec![Inline::Text(label)], len));
1890 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1892:9
     |
1892 | /         if rest.starts_with("<http") {
1893 | |             if let Some(end) = rest.find('>') {
1894 | |                 let url = rest[1..end].to_string();
1895 | |                 if url.starts_with("http://") || url.starts_with("https://") {
...    |
1905 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1892 ~         if rest.starts_with("<http")
1893 ~             && let Some(end) = rest.find('>') {
1894 |                 let url = rest[1..end].to_string();
 ...
1903 |                 }
1904 ~             }
     |

warning: used consecutive `str::replace` call
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:2152:22
     |
2152 |                       .replace('\n', " ")
     |  ______________________^
2153 | |                     .replace('\r', " ");
     | |_______________________________________^ help: replace with: `replace(['\n', '\r'], " ")`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace
     = note: `#[warn(clippy::collapsible_str_replace)]` on by default

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:2516:25
     |
2516 | /                         if is_self {
2517 | |                             if let Some(warning) =
2518 | |                                 self.check_host_fragment(fragment)
...    |
2528 | |                         }
     | |_________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
2516 ~                         if is_self
2517 ~                             && let Some(warning) =
2518 |                                 self.check_host_fragment(fragment)
 ...
2526 |                                 );
2527 ~                             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3118:5
     |
3118 | /     if rest.starts_with('[') {
3119 | |         if let Some((key, _, len)) = match_bracket_field(rest) {
3120 | |             if key == "h" {
3121 | |                 return gap + len;
...    |
3124 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3118 ~     if rest.starts_with('[')
3119 ~         && let Some((key, _, len)) = match_bracket_field(rest) {
3120 |             if key == "h" {
3121 |                 return gap + len;
3122 |             }
3123 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3119:9
     |
3119 | /         if let Some((key, _, len)) = match_bracket_field(rest) {
3120 | |             if key == "h" {
3121 | |                 return gap + len;
3122 | |             }
3123 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3119 ~         if let Some((key, _, len)) = match_bracket_field(rest)
3120 ~             && key == "h" {
3121 |                 return gap + len;
3122 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3151:5
     |
3151 | /     if text.starts_with('[') {
3152 | |         if let Some(close) = text.find(']') {
3153 | |             let symbol = text[1..close].trim();
3154 | |             if symbol.chars().count() <= 1 {
...    |
3158 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3151 ~     if text.starts_with('[')
3152 ~         && let Some(close) = text.find(']') {
3153 |             let symbol = text[1..close].trim();
 ...
3156 |             }
3157 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3227:9
     |
3227 | /         if after.starts_with('(') {
3228 | |             if let Some((_, tail)) = split_balanced(&after, '(', ')') {
3229 | |                 out.push_str(&rest[..open]);
3230 | |                 out.push_str(&label);
...    |
3234 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3227 ~         if after.starts_with('(')
3228 ~             && let Some((_, tail)) = split_balanced(&after, '(', ')') {
3229 |                 out.push_str(&rest[..open]);
 ...
3232 |                 continue;
3233 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3315:9
     |
3315 | /         if rest.starts_with('[') || rest.starts_with('(') {
3316 | |             if let Some((key, value, len)) = match_bracket_field(rest) {
3317 | |                 if !hidden_excerpt_field(&key) && !value.is_empty() {
3318 | |                     out.push_str(&format!("{key}: {value}"));
...    |
3324 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3315 ~         if (rest.starts_with('[') || rest.starts_with('(')) {
3316 ~             && let Some((key, value, len)) = match_bracket_field(rest) {
3317 |                 if !hidden_excerpt_field(&key) && !value.is_empty() {
 ...
3322 |                 continue;
3323 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3340:9
     |
3340 | /         if text[cursor..].starts_with('#') {
3341 | |             if let Some((tag, len)) = match_tag(text, cursor) {
3342 | |                 if !STRUCTURAL_TAGS.contains(&tag.as_str()) {
3343 | |                     out.push_str(&tag);
...    |
3348 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3340 ~         if text[cursor..].starts_with('#')
3341 ~             && let Some((tag, len)) = match_tag(text, cursor) {
3342 |                 if !STRUCTURAL_TAGS.contains(&tag.as_str()) {
 ...
3346 |                 continue;
3347 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:3365:9
     |
3365 | /         if is_word_boundary(prev) {
3366 | |             if let Some((key, value, len)) = match_bare_field(&text[cursor..]) {
3367 | |                 if !hidden_excerpt_field(&key) {
3368 | |                     out.push_str(&format!("{key}: {value} "));
...    |
3373 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
3365 ~         if is_word_boundary(prev)
3366 ~             && let Some((key, value, len)) = match_bare_field(&text[cursor..]) {
3367 |                 if !hidden_excerpt_field(&key) {
 ...
3371 |                 continue;
3372 ~             }
     |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/resolve.rs:154:5
    |
154 | /     if let Some(inner) = text.strip_prefix("[[") {
155 | |         if let Some(stripped) = inner.strip_suffix("]]") {
156 | |             text = stripped;
157 | |         }
158 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
154 ~     if let Some(inner) = text.strip_prefix("[[")
155 ~         && let Some(stripped) = inner.strip_suffix("]]") {
156 |             text = stripped;
157 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/resolve.rs:964:5
    |
964 | /     if let Some(inner) = text.strip_prefix("[[") {
965 | |         if let Some(stripped) = inner.strip_suffix("]]") {
966 | |             text = stripped;
967 | |         }
968 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
964 ~     if let Some(inner) = text.strip_prefix("[[")
965 ~         && let Some(stripped) = inner.strip_suffix("]]") {
966 |             text = stripped;
967 ~         }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/resolve.rs:1108:9
     |
1108 | /         if let Some(parent) = source_note_relative.parent() {
1109 | |             if let Some(found) = self.exact_vault_hit(&parent.join(target_path))
1110 | |             {
1111 | |                 return Ok(self.describe(found, parsed.width_px));
1112 | |             }
1113 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1108 ~         if let Some(parent) = source_note_relative.parent()
1109 ~             && let Some(found) = self.exact_vault_hit(&parent.join(target_path))
1110 |             {
1111 |                 return Ok(self.describe(found, parsed.width_px));
1112 ~             }
     |

warning: using `clone` on type `AssetMediaKind` which implements the `Copy` trait
    --> src/native/highlights_ref/note_snapshot/resolve.rs:1174:25
     |
1174 |             media_kind: attachment.media_kind.clone(),
     |                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try removing the `clone` call: `attachment.media_kind`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#clone_on_copy
     = note: `#[warn(clippy::clone_on_copy)]` on by default

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

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/serialize.rs:440:5
    |
440 | /     if let Some(target) = &chip.target {
441 | |         if let Some(destination) = render_target(view, target) {
442 | |             return format!("[{content}]({destination}){{{classes}}}");
443 | |         }
444 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
440 ~     if let Some(target) = &chip.target
441 ~         && let Some(destination) = render_target(view, target) {
442 |             return format!("[{content}]({destination}){{{classes}}}");
443 ~         }
    |

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/note_snapshot/serialize.rs:987:10
    |
987 |           .replace('\n', " ")
    |  __________^
988 | |         .replace('\r', " ")
    | |___________________________^ help: replace with: `replace(['\n', '\r'], " ")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:249:13
    |
249 | /             if let Some(outcome) = &mut project_outcome {
250 | |                 if !outcome.history.is_empty() {
251 | |                     sections.push(outcome_history_section(
252 | |                         &note.identity,
...   |
257 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
249 ~             if let Some(outcome) = &mut project_outcome
250 ~                 && !outcome.history.is_empty() {
251 |                     sections.push(outcome_history_section(
...
255 |                     ));
256 ~                 }
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

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1260:5
     |
1260 | /     if outcome.is_none() && *kind == NoteKind::TerminalProject {
1261 | |         if let Some(status) = metadata
1262 | |             .and_then(|metadata| metadata_value(metadata, "status"))
1263 | |             .and_then(yaml_scalar_text)
...    |
1274 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1260 ~     if outcome.is_none() && *kind == NoteKind::TerminalProject
1261 ~         && let Some(status) = metadata
1262 |             .and_then(|metadata| metadata_value(metadata, "status"))
 ...
1272 |             }
1273 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:2166:17
     |
2166 | /                 if let Some(original) = &task.anchor {
2167 | |                     if let Some(anchor) = mapping
2168 | |                         .get(&(original.identity.clone(), original.id.clone()))
...    |
2172 | |                 }
     | |_________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
2166 ~                 if let Some(original) = &task.anchor
2167 ~                     && let Some(anchor) = mapping
2168 |                         .get(&(original.identity.clone(), original.id.clone()))
2169 |                     {
2170 |                         task.anchor = Some(anchor.clone());
2171 ~                     }
     |

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

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:450:25
    |
450 |                         extracted.extend(nested.drain(..));
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extend_with_drain
    = note: `#[warn(clippy::extend_with_drain)]` on by default

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:477:21
    |
477 |                     extracted.extend(nested.drain(..));
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extend_with_drain

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:497:21
    |
497 |                     extracted.extend(nested.drain(..));
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extend_with_drain

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/pdf_target.rs:124:1
    |
124 | / pub(super) fn plan_pdf_url(
125 | |     url: &WebUrl,
126 | |     downloaded: &Path,
127 | |     name_override: Option<&str>,
...   |
132 | |     progress: Option<&dyn Fn(&str)>,
133 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:155:34
    |
155 |                         url.host.replace('.', "_").replace('-', "_"),
    |                                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '-'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:209:1
    |
209 | / pub(super) fn plan_arxiv(
210 | |     paper: &ArxivPaper,
211 | |     name_override: Option<&str>,
212 | |     title_override: Option<&str>,
...   |
218 | |     progress: Option<&dyn Fn(&str)>,
219 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:311:33
    |
311 |     format!("arxiv_{}", full_id.replace('.', "_").replace('/', "_"))
    |                                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '/'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_str_replace

warning: the borrowed expression implements the required traits
   --> src/native/highlights_ref/pdf_target.rs:462:21
    |
462 |                     &format!("re-sync {}", canonical.display()),
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `format!("re-sync {}", canonical.display())`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:804:9
    |
804 | /         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line) {
805 | |             if crate::native::ref_tasks::is_open_mark(hit.mark) {
806 | |                 tracker_idx = Some(i);
807 | |                 break;
808 | |             }
809 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
804 ~         if let Some(hit) = crate::native::ref_tasks::parse_tracker_line(line)
805 ~             && crate::native::ref_tasks::is_open_mark(hit.mark) {
806 |                 tracker_idx = Some(i);
807 |                 break;
808 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:883:5
    |
883 | /     if has_hash && has_base {
884 | |         if let Some(updated) = recompute_parent_free_hash(&front_lines) {
885 | |             front_lines = updated;
886 | |         }
887 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
883 ~     if has_hash && has_base
884 ~         && let Some(updated) = recompute_parent_free_hash(&front_lines) {
885 |             front_lines = updated;
886 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:896:9
    |
896 | /         if let Some((k, v)) = line.split_once(':') {
897 | |             if k.trim() == "highlights_marker_base" {
898 | |                 let mut v = v.trim().to_string();
899 | |                 if (v.starts_with('\'') && v.ends_with('\'') && v.len() >= 2)
...   |
908 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
896 ~         if let Some((k, v)) = line.split_once(':')
897 ~             && k.trim() == "highlights_marker_base" {
898 |                 let mut v = v.trim().to_string();
...
906 |                 base_json = Some(v);
907 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/reading_plan.rs:921:9
    |
921 | /         if let Some((k, _)) = line.split_once(':') {
922 | |             if k.trim() == "highlights_marker_hash" {
923 | |                 // Preserve quoting style: single-quoted string.
924 | |                 out.push(format!("highlights_marker_hash: '{hash}'"));
...   |
927 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
921 ~         if let Some((k, _)) = line.split_once(':')
922 ~             && k.trim() == "highlights_marker_hash" {
923 |                 // Preserve quoting style: single-quoted string.
924 |                 out.push(format!("highlights_marker_hash: '{hash}'"));
925 |                 continue;
926 ~             }
    |

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:709:1
    |
709 | / pub(super) fn preflight_for_url(
710 | |     config: &Config,
711 | |     rows: &[RefRow],
712 | |     recorded: &[RecordedSource],
...   |
717 | |     title_fallback: &str,
718 | | ) -> Result<Option<RereadPreflight>, CommandError> {
    | |__________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:759:1
    |
759 | / pub(super) fn preflight_for_stem(
760 | |     config: &Config,
761 | |     rows: &[RefRow],
762 | |     stem: &str,
...   |
767 | |     identity: StemIdentity<'_>,
768 | | ) -> Result<Option<RereadPreflight>, CommandError> {
    | |__________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/recapture.rs:827:1
    |
827 | / fn finish_selection(
828 | |     config: &Config,
829 | |     family: SelectedFamily,
830 | |     name: Option<&str>,
...   |
836 | |     attach_available: bool,
837 | | ) -> Result<Option<RereadPreflight>, CommandError> {
    | |__________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: deref which would be done by auto-deref
   --> src/native/highlights_ref/region.rs:540:38
    |
540 |     let block_id = region_section_id(*lines.get(index)?)?;
    |                                      ^^^^^^^^^^^^^^^^^^ help: try: `lines.get(index)?`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_auto_deref
    = note: `#[warn(clippy::explicit_auto_deref)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/rename/plan.rs:790:17
    |
790 | /                 if current != *before {
791 | |                     if let Err(error) = atomic_write_bytes(path, before) {
792 | |                         failures.push(format!(
793 | |                             "could not restore PDF bytes at {}: {error}",
...   |
797 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
790 ~                 if current != *before
791 ~                     && let Err(error) = atomic_write_bytes(path, before) {
792 |                         failures.push(format!(
...
795 |                         ));
796 ~                     }
    |

warning: this block may be rewritten with the `?` operator
   --> src/native/highlights_ref/sections.rs:503:9
    |
503 | /         if hash_tag_key(tag_name).is_none() {
504 | |             return None;
505 | |         }
    | |_________^ help: replace it with: `hash_tag_key(tag_name)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/sections.rs:695:21
    |
695 | /                     if hit.span.start > 0
696 | |                         && line.as_bytes()[hit.span.start - 1] == b'\\'
697 | |                     {
698 | |                         edits.push((hit.span.start - 1..hit.span.start, ""));
699 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_match
help: collapse nested if block
    |
694 ~                 SectionTagHitKind::Escaped if hit.sigil == '@'
695 ~                     && hit.span.start > 0
696 |                         && line.as_bytes()[hit.span.start - 1] == b'\\'
697 ~                     => {
698 |                         edits.push((hit.span.start - 1..hit.span.start, ""));
699 ~                     }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sections.rs:1390:16
     |
1390 |           } else if sticky_only_tags {
     |  ________________^
1391 | |             if let Some((_, annotation, _, hit)) =
1392 | |                 tag_hits.iter().find(|(_, _, _, hit)| {
1393 | |                     hit.kind == SectionTagHitKind::Positional
...    |
1410 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1390 ~         } else if sticky_only_tags
1391 ~             && let Some((_, annotation, _, hit)) =
1392 |                 tag_hits.iter().find(|(_, _, _, hit)| {
 ...
1408 |                 });
1409 ~             }
     |

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/sidecar.rs:298:1
    |
298 | / pub(super) fn flush_sidecar_chunk(
299 | |     annotations: &mut Vec<SidecarAnnotation>,
300 | |     chunk: &mut Vec<String>,
301 | |     page_label: Option<&str>,
...   |
306 | |     page_ordinals: &mut BTreeMap<String, usize>,
307 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/highlights_ref/sidecar.rs:476:9
    |
476 | /         let Some(heading) = section_heading_text(&candidate) else {
477 | |             return None;
478 | |         };
    | |__________^ help: replace it with: `let heading = section_heading_text(&candidate)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

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

warning: this block may be rewritten with the `?` operator
    --> src/native/highlights_ref/sidecar_render.rs:2716:12
     |
2716 |       } else if let Some(rest) = lower.strip_prefix("p ") {
     |  ____________^
2717 | |         rest
2718 | |     } else {
2719 | |         return None;
2720 | |     };
     | |_____^ help: replace it with: `{ lower.strip_prefix("p ")? }`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: the borrowed expression implements the required traits
   --> src/native/highlights_ref/stamp.rs:450:25
    |
450 | /                         &format!(
451 | |                             "add audio with bob ref create {} --listen",
452 | |                             library_destination.display()
453 | |                         ),
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
help: change this to
    |
450 ~                         format!(
451 +                             "add audio with bob ref create {} --listen",
452 +                             library_destination.display()
453 ~                         ),
    |

warning: the borrowed expression implements the required traits
   --> src/native/highlights_ref/stamp.rs:482:25
    |
482 | /                         &format!(
483 | |                             "add audio with bob ref create {} --listen",
484 | |                             library_destination.display()
485 | |                         ),
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
help: change this to
    |
482 ~                         format!(
483 +                             "add audio with bob ref create {} --listen",
484 +                             library_destination.display()
485 ~                         ),
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/stamp.rs:807:5
    |
807 | /     if let (Ok(child_c), Ok(parent_c)) =
808 | |         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
809 | |     {
810 | |         if let Some(rel) = relative_inside(&child_c, &parent_c) {
...   |
813 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
808 ~         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
809 ~         && let Some(rel) = relative_inside(&child_c, &parent_c) {
810 |             return Some(rel);
811 ~         }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1408:9
     |
1408 | /         if trimmed.starts_with("done_tasks:") {
1409 | |             if let Some(start) = trimmed.find("[[") {
1410 | |                 if let Some(end) = trimmed[start..].find("]]") {
1411 | |                     let target = &trimmed[start + 2..start + end];
...    |
1419 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1408 ~         if trimmed.starts_with("done_tasks:")
1409 ~             && let Some(start) = trimmed.find("[[") {
1410 |                 if let Some(end) = trimmed[start..].find("]]") {
 ...
1417 |                 }
1418 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1409:13
     |
1409 | /             if let Some(start) = trimmed.find("[[") {
1410 | |                 if let Some(end) = trimmed[start..].find("]]") {
1411 | |                     let target = &trimmed[start + 2..start + end];
1412 | |                     let mut rel = target.trim().to_string();
...    |
1418 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1409 ~             if let Some(start) = trimmed.find("[[")
1410 ~                 && let Some(end) = trimmed[start..].find("]]") {
1411 |                     let target = &trimmed[start + 2..start + end];
 ...
1416 |                     return Some(rel);
1417 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1422:5
     |
1422 | /     if relative.components().count() == 1 {
1423 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1424 | |             return Some(format!("done/{stem}_done.md"));
1425 | |         }
1426 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
1422 ~     if relative.components().count() == 1
1423 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1424 |             return Some(format!("done/{stem}_done.md"));
1425 ~         }
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
   --> src/native/pomodoro_homes/resolve.rs:283:17
    |
283 | /                 chain[nearest_home..end]
284 | |                     .iter()
285 | |                     .filter(|(_, facts)| facts.kind == NoteKind::Project)
286 | |                     .last()
    | |___________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
286 -                     .last()
286 +                     .next_back()
    |

warning: this function has too many arguments (8/7)
  --> src/native/pomodoro_homes/session.rs:59:1
   |
59 | / pub(crate) fn attribute_ledger_entry<S: HomeSource>(
60 | |     contents: &str,
61 | |     entry_line: usize,
62 | |     name: Option<&str>,
...  |
67 | |     resolver: &mut HomeResolver<S>,
68 | | ) -> SessionHomes {
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

warning: needlessly taken reference of both operands
    --> src/native/pomodoro_themes/rename.rs:1090:16
     |
1090 |             if &contents != &planned.after_contents {
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#op_ref
help: use the values directly
     |
1090 -             if &contents != &planned.after_contents {
1090 +             if contents != planned.after_contents {
     |

warning: this `if` statement can be collapsed
   --> src/native/pomodoro_themes/mod.rs:387:5
    |
387 | /     if completion {
388 | |         if let Some((mut records, mut days, cached_warnings)) =
389 | |             cache::load_completion(vault, today, &years)
...   |
396 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
387 ~     if completion
388 ~         && let Some((mut records, mut days, cached_warnings)) =
389 |             cache::load_completion(vault, today, &years)
...
394 |             return (records, days);
395 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/pomodoro_themes/mod.rs:462:5
    |
462 | /     if let Some(summary) = today_summary.as_ref() {
463 | |         if let Some((mtime_ns, size)) = cache::fingerprint(&today_path) {
464 | |             vault_cache.files.insert(
465 | |                 today_relative,
...   |
473 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
462 ~     if let Some(summary) = today_summary.as_ref()
463 ~         && let Some((mtime_ns, size)) = cache::fingerprint(&today_path) {
464 |             vault_cache.files.insert(
...
471 |             );
472 ~         }
    |

warning: this binary expression can be simplified
   --> src/native/pomodoro_themes/mod.rs:545:12
    |
545 |         if date > today || date == today {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `date >= today`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_comparisons
    = note: `#[warn(clippy::double_comparisons)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/pref_journal/mod.rs:258:41
    |
258 |             .then_with(|| left_path.cmp(&right_path))
    |                                         ^^^^^^^^^^^ help: change this to: `right_path`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/projects/scan.rs:226:5
    |
226 | /     let Some(&(line_number, raw_value)) = fields.first() else {
227 | |         return None;
228 | |     };
    | |______^ help: replace it with: `let &(line_number, raw_value) = fields.first()?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

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

warning: this `if` statement can be collapsed
   --> src/native/ref_jobs/spool.rs:416:9
    |
416 | /         if let Err(error) = fs::remove_file(path) {
417 | |             if error.kind() != std::io::ErrorKind::NotFound {
418 | |                 failures.push(format!(
419 | |                     "remove staged ref job {}: {error}",
...   |
423 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
416 ~         if let Err(error) = fs::remove_file(path)
417 ~             && error.kind() != std::io::ErrorKind::NotFound {
418 |                 failures.push(format!(
...
421 |                 ));
422 ~             }
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

warning: this `if` statement can be collapsed
   --> src/native/ref_library/show.rs:951:17
    |
951 | /                 if character == '*' {
952 | |                     if let Some(first) = source {
953 | |                         if paired_firsts.contains(&first) {
954 | |                             flush_quote_segment(
...   |
974 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
951 ~                 if character == '*'
952 ~                     && let Some(first) = source {
953 |                         if paired_firsts.contains(&first) {
...
972 |                         }
973 ~                     }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_library/show.rs:952:21
    |
952 | /                     if let Some(first) = source {
953 | |                         if paired_firsts.contains(&first) {
954 | |                             flush_quote_segment(
955 | |                                 &mut rendered,
...   |
973 | |                     }
    | |_____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
952 ~                     if let Some(first) = source
953 ~                         && paired_firsts.contains(&first) {
954 |                             flush_quote_segment(
...
971 |                             continue;
972 ~                         }
    |

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

warning: doc list item without indentation
   --> src/native/ref_library/mod.rs:904:5
    |
904 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
904 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
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

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:239:9
    |
239 | /         if trimmed.starts_with("done_tasks:") {
240 | |             if let Some(start) = trimmed.find("[[") {
241 | |                 if let Some(end) = trimmed[start..].find("]]") {
242 | |                     let target = &trimmed[start + 2..start + end];
...   |
250 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
239 ~         if trimmed.starts_with("done_tasks:")
240 ~             && let Some(start) = trimmed.find("[[") {
241 |                 if let Some(end) = trimmed[start..].find("]]") {
...
248 |                 }
249 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:240:13
    |
240 | /             if let Some(start) = trimmed.find("[[") {
241 | |                 if let Some(end) = trimmed[start..].find("]]") {
242 | |                     let target = &trimmed[start + 2..start + end];
243 | |                     let mut rel = target.trim().to_string();
...   |
249 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
240 ~             if let Some(start) = trimmed.find("[[")
241 ~                 && let Some(end) = trimmed[start..].find("]]") {
242 |                     let target = &trimmed[start + 2..start + end];
...
247 |                     return Some(rel);
248 ~                 }
    |

warning: this `if` statement can be collapsed
   --> src/native/ref_tasks/insert.rs:257:5
    |
257 | /     if relative.components().count() == 1 {
258 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
259 | |             return Some(format!("done/{stem}_done.md"));
260 | |         }
261 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
257 ~     if relative.components().count() == 1
258 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
259 |             return Some(format!("done/{stem}_done.md"));
260 ~         }
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
   --> src/native/ref_tasks/walk.rs:650:9
    |
650 | /         if b == b'#' || b == b'^' {
651 | |             if bytes[i + 1].eq_ignore_ascii_case(&b'r')
652 | |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
653 | |                 && bytes[i + 3].eq_ignore_ascii_case(&b'f')
...   |
657 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
650 ~         if (b == b'#' || b == b'^') {
651 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
652 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
655 |                 return true;
656 ~             }
    |

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
   --> src/native/relation_labels/rename.rs:758:5
    |
758 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
758 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
758 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

warning: returning the result of a `let` binding from a block
   --> src/native/relation_labels/write.rs:117:5
    |
106 | /     let command = ClapCommand::new(command_name(kind))
107 | |         .about(about(kind))
108 | |         .long_about(long_about(kind))
109 | |         .after_help(after_help(kind))
...   |
115 | |         .arg(via_arg())
116 | |         .arg(label_arg());
    | |__________________________- unnecessary `let` binding
117 |       command
    |       ^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#let_and_return
help: return the expression directly
    |
106 ~     
107 ~     ClapCommand::new(command_name(kind))
108 +         .about(about(kind))
109 +         .long_about(long_about(kind))
110 +         .after_help(after_help(kind))
111 +         .disable_help_flag(true)
112 +         .arg(allow_unused_arg(kind))
113 +         .arg(bob_dir_arg())
114 +         .arg(format_arg())
115 +         .arg(help_arg())
116 +         .arg(via_arg())
117 +         .arg(label_arg())
    |

warning: this `if` statement can be collapsed
   --> src/native/stats/homes.rs:121:25
    |
121 | /                         if home.area == path_key {
122 | |                             if let Some(hue) = home.hue {
123 | |                                 top_areas
124 | |                                     .entry(hue)
...   |
128 | |                         }
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
121 ~                         if home.area == path_key
122 ~                             && let Some(hue) = home.hue {
123 |                                 top_areas
...
126 |                                     .push((home.label.clone(), path_key));
127 ~                             }
    |

warning: this `if` statement can be collapsed
   --> src/native/stats/render.rs:906:5
    |
906 | /     if metric.unit == "minutes" {
907 | |         if let Some(project) = metric.parts_summary.get("project") {
908 | |             let total: i64 = project.iter().map(|part| part.value).sum();
909 | |             let split: i64 =
...   |
925 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
906 ~     if metric.unit == "minutes"
907 ~         && let Some(project) = metric.parts_summary.get("project") {
908 |             let total: i64 = project.iter().map(|part| part.value).sum();
...
923 |             }
924 ~         }
    |

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1213:1
     |
1213 | / fn attach_offer(
1214 | |     verdict: &mut DependentVerdict,
1215 | |     files: &[FileScan],
1216 | |     day: &DayView,
...    |
1221 | |     project: Option<PathBuf>,
1222 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:1314:1
     |
1314 | / fn apply_project_member_classes(
1315 | |     verdicts: &mut Vec<DependentVerdict>,
1316 | |     folds: &mut Vec<ProjectFold>,
1317 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
1326 | |     _note_settings: &NoteTaskSettings,
1327 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1663:1
     |
1663 | / fn apply_verdicts(
1664 | |     input: SuccessorInput,
1665 | |     files: Vec<FileScan>,
1666 | |     verdicts: Vec<DependentVerdict>,
...    |
1671 | |     project_folds: Vec<ProjectFold>,
1672 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/successors.rs:2092:29
     |
2092 |             project_states: &project_states,
     |                             ^^^^^^^^^^^^^^^ help: change this to: `project_states`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this `if` statement can be collapsed
   --> src/native/task_move/command.rs:931:5
    |
931 | /     if let Some(recovery) = &report.recovery_directory {
932 | |         if !report.deferred_paths.is_empty() || report.error.is_some() {
933 | |             println!("  Recovery: {recovery}");
934 | |         }
935 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
931 ~     if let Some(recovery) = &report.recovery_directory
932 ~         && (!report.deferred_paths.is_empty() || report.error.is_some()) {
933 |             println!("  Recovery: {recovery}");
934 ~         }
    |

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/plan.rs:1375:6
     |
1375 | ) -> Result<(Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>), PlanError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this `if` statement can be collapsed
  --> src/native/task_relations/format.rs:88:5
   |
88 | /     if kind == RelationSlotKind::LinkedFrom {
89 | |         if let Some(child) = links_children_of(lines, fenced, task_line).first()
90 | |         {
91 | |             return RelationInsertSlot {
...  |
96 | |     }
   | |_____^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
   |
88 ~     if kind == RelationSlotKind::LinkedFrom
89 ~         && let Some(child) = links_children_of(lines, fenced, task_line).first()
90 |         {
...
94 |             };
95 ~         }
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

warning: called `iter().copied().collect()` on a slice to create a `Vec`. Calling `to_vec()` is both faster and more readable
   --> src/native/task_status_hooks/relations.rs:135:41
    |
135 |         let line_refs: Vec<&str> = lines.iter().copied().collect();
    |                                         ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `.to_vec()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#iter_cloned_collect
    = note: `#[warn(clippy::iter_cloned_collect)]` on by default

warning: called `iter().copied().collect()` on a slice to create a `Vec`. Calling `to_vec()` is both faster and more readable
   --> src/native/task_status_hooks/relations.rs:312:41
    |
312 |         let line_refs: Vec<&str> = lines.iter().copied().collect();
    |                                         ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `.to_vec()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#iter_cloned_collect

warning: this `if` statement can be collapsed
   --> src/native/task_status_hooks/relations.rs:351:13
    |
351 | /             if duplicated {
352 | |                 if let Some(block_id) = &task.block_id {
353 | |                     self.outcome.warnings.push(RelationWarning {
354 | |                         kind: "duplicate_block_id".to_string(),
...   |
365 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
351 ~             if duplicated
352 ~                 && let Some(block_id) = &task.block_id {
353 |                     self.outcome.warnings.push(RelationWarning {
...
363 |                         .insert((relative.clone(), block_id.clone()));
364 ~                 }
    |

warning: you seem to want to iterate on a map's keys
   --> src/native/task_status_hooks/relations.rs:592:32
    |
592 |             for (target, _) in &collected.by_target {
    |                                ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#for_kv_map
    = note: `#[warn(clippy::for_kv_map)]` on by default
help: use the corresponding method
    |
592 -             for (target, _) in &collected.by_target {
592 +             for target in collected.by_target.keys() {
    |

warning: called `iter().copied().collect()` on a slice to create a `Vec`. Calling `to_vec()` is both faster and more readable
   --> src/native/task_status_hooks/relations.rs:611:45
    |
611 |             let line_refs: Vec<&str> = lines.iter().copied().collect();
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `.to_vec()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#iter_cloned_collect

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:462:5
    |
462 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:329:9
    |
329 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1252:1
     |
1252 | / fn consume_blocked_links_after_compose(
1253 | |     compose: &mut ComposeResult,
1254 | |     files: &[FileScan],
1255 | |     daily_path: &Path,
...    |
1266 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1267 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this manual char comparison can be written more succinctly
   --> src/native/vault_links.rs:353:17
    |
353 |         .rsplit(|character| matches!(character, '/' | '\\'))
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `['/', '\\']`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_pattern_char_comparison

warning: this `impl` can be derived
   --> src/native/vault_sync.rs:169:1
    |
169 | / impl Default for RunOptions {
170 | |     fn default() -> Self {
171 | |         Self {
172 | |             dry_run: false,
...   |
177 | | }
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#derivable_impls
    = note: `#[warn(clippy::derivable_impls)]` on by default
help: replace the manual implementation with a derive attribute
    |
163 + #[derive(Default)]
164 | struct RunOptions {
    |

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

warning: items after a test module
    --> src/native/capture/link_guard.rs:732:1
     |
 732 |   mod tests {
     |   ^^^^^^^^^
...
1071 | / pub(super) fn apply_new_task_project_block(
1072 | |     line: &str,
1073 | |     status_types: &BTreeMap<char, task_status_hooks::TaskStatusType>,
1074 | | ) -> Option<String> {
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
    --> src/native/capture_parse.rs:2753:9
     |
2753 | /         for raw in ["Plan x"] {
2754 | |             let prose = json(raw);
2755 | |             assert_eq!(prose["mode"], "task", "{raw}");
2756 | |             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
2757 | |             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
2758 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
     = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
     |
2753 ~         {
2754 +             let raw = "Plan x";
2755 +             let prose = json(raw);
2756 +             assert_eq!(prose["mode"], "task", "{raw}");
2757 +             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
2758 +             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
2759 +         }
     |

warning: items after a test module
   --> src/native/capture_pomodoro_close/ledger.rs:915:1
    |
915 |   mod managed_dependency_tests {
    |   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
...
946 | / fn collect_work_log_note_groups(
947 | |     spans: &[LineSpan<'_>],
948 | |     entry_index: usize,
949 | |     range: &Range<usize>,
950 | |     fenced: &BTreeSet<usize>,
951 | | ) -> Vec<WorkLogNoteGroup> {
    | |__________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

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
  --> src/native/file_coordination.rs:79:9
   |
79 |         assert!(!IS_COORDINATED);
   |         ^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: consider moving this into a const block: `const { assert!(..) }`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants
   = note: `#[warn(clippy::assertions_on_constants)]` on by default

warning: equality checks against false can be replaced by a negation
   --> src/native/gkeep/imports.rs:968:17
    |
968 |         assert!(has_verified(&loaded, "note-1", "0123456789ab") == false);
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `!has_verified(&loaded, "note-1", "0123456789ab")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_comparison

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

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/create.rs:5903:13
     |
5903 | /             if text.contains('↩') {
5904 | |                 if pill_page == 0 {
5905 | |                     pill_page = page;
5906 | |                 }
5907 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
     |
5903 ~             if text.contains('↩')
5904 ~                 && pill_page == 0 {
5905 |                     pill_page = page;
5906 ~                 }
     |

warning: calling `push_str()` using a single-character string literal
    --> src/native/highlights_ref/note_snapshot/profile.rs:1417:13
     |
1417 |             long_md.push_str("\n");
     |             ^^^^^^^^^^^^^^^^^^^^^^ help: consider using `push` with a character literal: `long_md.push('\n')`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_char_add_str
     = note: `#[warn(clippy::single_char_add_str)]` on by default

warning: you seem to be trying to use `match` for destructuring a single pattern. Consider using `if let`
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1210:13
     |
1210 | /             match block_id {
1211 | |                 Some(id) => {
1212 | |                     let tid = self.claim_anchor_id(&format!("t-{id}"));
1213 | |                     let anchor = self.push_anchor(AnchorKind::Block, id, tid);
...    |
1216 | |                 None => {}
1217 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_match
help: try
     |
1210 ~             if let Some(id) = block_id {
1211 +                 let tid = self.claim_anchor_id(&format!("t-{id}"));
1212 +                 let anchor = self.push_anchor(AnchorKind::Block, id, tid);
1213 +                 content.push(Inline::Anchor(anchor));
1214 +             }
     |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/tests.rs:822:9
    |
822 | /         if character == '\\' {
823 | |             if chars.peek().is_some_and(|next| next.is_ascii_punctuation()) {
824 | |                 out.push(chars.next().expect("peeked punctuation"));
825 | |                 continue;
826 | |             }
827 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#collapsible_if
help: collapse nested if block
    |
822 ~         if character == '\\'
823 ~             && chars.peek().is_some_and(|next| next.is_ascii_punctuation()) {
824 |                 out.push(chars.next().expect("peeked punctuation"));
825 |                 continue;
826 ~             }
    |

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/highlights_ref/note_snapshot/tests.rs:945:9
    |
945 | /         let Some(relative) =
946 | |             bytes[cursor..].iter().position(|byte| *byte == b'`')
947 | |         else {
948 | |             return None;
949 | |         };
    | |__________^ help: replace it with: `let relative = bytes[cursor..].iter().position(|byte| *byte == b'`')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#question_mark

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/tests/continuations.rs:249:42
    |
249 |     let plan = super::plan_continuations(&[first.clone()]);
    |                                          ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&first)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: useless use of `format!`
   --> src/native/highlights_ref/tests/highlight_identity.rs:517:37
    |
517 |       let legacy_prior = region_note(&format!(
    |  _____________________________________^
518 | |         "### Page 4\n\n> [!quote] legacy quote\n\n^h-aaaaaaaaaaaaaaaa\n"
519 | |     ));
    | |_____^ help: consider using `.to_string()`: `"### Page 4\n\n> [!quote] legacy quote\n\n^h-aaaaaaaaaaaaaaaa\n".to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format

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
   --> src/native/pomodoro.rs:878:51
    |
878 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
    |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: usage of `bool::then` in `filter_map`
   --> src/native/relation_labels/tests.rs:224:14
    |
224 |             .filter_map(|(key, _)| prefs.hidden(key).then(|| key.clone()))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use `filter` then `map` instead: `filter(|&(key, _)| prefs.hidden(key)).map(|(key, _)| key.clone())`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_map_bool_then

warning: used `assert_eq!` with a literal bool
    --> src/native/stats/series.rs:1806:9
     |
1806 |         assert_eq!(summary.headline.value.is_some_and(|v| v < 0), true);
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_assert_comparison
     = note: `#[warn(clippy::bool_assert_comparison)]` on by default
help: replace it with `assert!(..)`
     |
1806 -         assert_eq!(summary.headline.value.is_some_and(|v| v < 0), true);
1806 +         assert!(summary.headline.value.is_some_and(|v| v < 0));
     |

warning: items after a test module
   --> src/native/task_complete/tree.rs:832:1
    |
832 |   mod managed_dependency_tests {
    |   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
...
877 | / pub(crate) fn complete_embedded_trees<V: CloseVault>(
878 | |     vault: &V,
879 | |     roots: &[EmbeddedTreeRoot<'_>],
880 | |     completion_date: &str,
881 | | ) -> Result<EmbeddedTreesOutcome, String> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:939:9
    |
939 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:971:9
    |
971 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/tests/successor_tests.rs:1385:14
     |
1385 |         Some(&day),
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

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:462:5
    |
462 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:329:9
    |
329 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

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

warning: this pattern reimplements `Result::unwrap_or`
    --> src/runner.rs:1737:28
     |
1737 |                   let code = match outcome {
     |  ____________________________^
1738 | |                     Ok(code) => code,
1739 | |                     Err(_) => 101,
1740 | |                 };
     | |_________________^ help: replace with: `outcome.unwrap_or(101)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_unwrap_or
     = note: `#[warn(clippy::manual_unwrap_or)]` on by default

warning: this pattern reimplements `Result::unwrap_or`
    --> src/runner.rs:1779:28
     |
1779 |                   let code = match outcome {
     |  ____________________________^
1780 | |                     Ok(code) => code,
1781 | |                     Err(_) => 101,
1782 | |                 };
     | |_________________^ help: replace with: `outcome.unwrap_or(101)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_unwrap_or

warning: this pattern reimplements `Result::unwrap_or`
    --> src/runner.rs:1810:28
     |
1810 |                   let code = match outcome {
     |  ____________________________^
1811 | |                     Ok(code) => code,
1812 | |                     Err(_) => 101,
1813 | |                 };
     | |_________________^ help: replace with: `outcome.unwrap_or(101)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_unwrap_or

warning: `bob-obsidian` (lib) generated 293 warnings (run `cargo clippy --fix --lib -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 200 suggestions)
warning: `bob-obsidian` (lib test) generated 335 warnings (291 duplicates) (run `cargo clippy --fix --lib -p bob-obsidian --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 27 suggestions)
warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/articles.rs:162:9
    |
162 | /         &mut article_command(&fixture)
163 | |             .args(["format", "-s", "draft", "-f", "json"]),
    | |__________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
    = note: `#[warn(clippy::needless_borrow)]` on by default
help: change this to
    |
162 ~         article_command(&fixture)
163 ~             .args(["format", "-s", "draft", "-f", "json"]),
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/articles.rs:459:9
    |
459 | /         &mut article_command(&fixture)
460 | |             .args(["adopt", "-s", "plain", "-f", "json"]),
    | |_________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
help: change this to
    |
459 ~         article_command(&fixture)
460 ~             .args(["adopt", "-s", "plain", "-f", "json"]),
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/articles.rs:682:9
    |
682 | /         &mut article_command(&fixture)
683 | |             .args(["format", "-s", "draft", "-f", "json"]),
    | |__________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
help: change this to
    |
682 ~         article_command(&fixture)
683 ~             .args(["format", "-s", "draft", "-f", "json"]),
    |

warning: unneeded use of `concat!` macro
   --> tests/cli/capture/complete_blocked_task.rs:195:9
    |
195 |         concat!("- [ ] #task Owner ^owner\n",),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `"- [ ] #task Owner ^owner\n"`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_concat
    = note: `#[warn(clippy::useless_concat)]` on by default

warning: for loop over a single element
   --> tests/cli/capture/parse_pomodoro_close.rs:337:5
    |
337 | /     for (text, range) in [("x - wired", [2, 3])] {
338 | |         let value = parse(text);
339 | |         assert_eq!(
340 | |             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
...   |
347 | |         );
348 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
    = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
    |
337 ~     {
338 +         let (text, range) = ("x - wired", [2, 3]);
339 +         let value = parse(text);
340 +         assert_eq!(
341 +             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
342 +             "{text}"
343 +         );
344 +         assert_eq!(
345 +             value["diagnostics"][0]["range"],
346 +             serde_json::json!(range),
347 +             "{text}"
348 +         );
349 +     }
    |

warning: for loop over a single element
   --> tests/cli/capture/parse_pomodoro_close.rs:556:5
    |
556 | /     for text in ["Plan x1"] {
557 | |         let value = parse(text);
558 | |         assert_eq!(value["mode"], "task", "{text}");
559 | |         assert!(value.get("pomodoro_close").is_none(), "{text}: {value}");
560 | |         assert_eq!(value["diagnostics"], serde_json::json!([]), "{text}");
561 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
help: try
    |
556 ~     {
557 +         let text = "Plan x1";
558 +         let value = parse(text);
559 +         assert_eq!(value["mode"], "task", "{text}");
560 +         assert!(value.get("pomodoro_close").is_none(), "{text}: {value}");
561 +         assert_eq!(value["diagnostics"], serde_json::json!([]), "{text}");
562 +     }
    |

warning: the borrowed expression implements the required traits
   --> tests/cli/capture/pomodoro_close_log.rs:346:18
    |
346 |             .arg(&args[0])
    |                  ^^^^^^^^ help: change this to: `args[0]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

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

warning: unnecessary use of `to_string`
   --> tests/cli/capture/pomodoro_shift.rs:581:11
    |
581 |         + &String::from_utf8_lossy(&shape_out.stdout).to_string();
    |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `String::from_utf8_lossy(&shape_out.stdout).as_ref()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_to_owned
    = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: for loop over a single element
   --> tests/cli/capture/pomodoros_agenda.rs:648:5
    |
648 | /     for field in ["status"] {
649 | |         assert_eq!(agenda["plan_budget"][field], plan[field]);
650 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
help: try
    |
648 ~     {
649 +         let field = "status";
650 +         assert_eq!(agenda["plan_budget"][field], plan[field]);
651 +     }
    |

warning: used `assert_eq!` with a literal bool
    --> tests/cli/capture/ref.rs:1217:5
     |
1217 | /     assert_eq!(
1218 | |         mixed_json["items"][1]["ref_listen"]
1219 | |             .as_bool()
1220 | |             .unwrap_or(false),
1221 | |         false,
1222 | |         "{mixed_json}"
1223 | |     );
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_assert_comparison
     = note: `#[warn(clippy::bool_assert_comparison)]` on by default
help: replace it with `assert!(..)`
     |
1217 ~     assert!(
1218 ~         !mixed_json["items"][1]["ref_listen"]
1219 |             .as_bool()
1220 ~             .unwrap_or(false),
     |

warning: using `contains()` instead of `iter().any()` is more efficient
   --> tests/cli/capture/rewrite.rs:338:9
    |
338 | /         codes
339 | |             .iter()
340 | |             .any(|code| *code == "invalid_pomodoro_block_id"),
    | |_____________________________________________________________^ help: try: `codes.contains(&"invalid_pomodoro_block_id")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_contains
    = note: `#[warn(clippy::manual_contains)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
  --> tests/cli/capture_templates.rs:41:9
   |
41 |         &mut command(&file).args(["save", "-f", "json"]),
   |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
  --> tests/cli/capture_templates.rs:85:9
   |
85 | /         &mut command(&file).args([
86 | |             "save",
87 | |             "--template-origin",
88 | |             id,
89 | |             "-f",
90 | |             "json",
91 | |         ]),
   | |__________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
help: change this to
   |
85 ~         command(&file).args([
86 +             "save",
87 +             "--template-origin",
88 +             id,
89 +             "-f",
90 +             "json",
91 ~         ]),
   |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:120:9
    |
120 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:160:9
    |
160 | /         &mut command(&disabled_file)
161 | |             .arg("save")
162 | |             .args(["-f", "json"])
163 | |             .env("BOB_CONFIG_FILE", config),
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow
help: change this to
    |
160 ~         command(&disabled_file)
161 +             .arg("save")
162 +             .args(["-f", "json"])
163 ~             .env("BOB_CONFIG_FILE", config),
    |

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:246:9
    |
246 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:296:9
    |
296 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:316:9
    |
316 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:328:9
    |
328 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: length comparison to zero
    --> tests/cli/highlights/create.rs:6207:9
     |
6207 |         std::fs::read(&library).expect("read library PDF").len() > 0,
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: using `!is_empty` is clearer and more explicit: `!std::fs::read(&library).expect("read library PDF").is_empty()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#len_zero
     = note: `#[warn(clippy::len_zero)]` on by default

warning: needless call to `as_bytes`
   --> tests/cli/highlights/diagrams.rs:822:13
    |
822 |     assert!(long_tmpdir.to_string_lossy().as_bytes().len() > 40);
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: `len()` can be called directly on strings: `long_tmpdir.to_string_lossy().len()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_as_bytes
    = note: `#[warn(clippy::needless_as_bytes)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/highlights/fake_clip.rs:203:32
    |
203 |             root = json_string(&path_str(&root)),
    |                                ^^^^^^^^^^^^^^^^ help: change this to: `path_str(&root)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrow

warning: equality checks against false can be replaced by a negation
    --> tests/cli/highlights/listen.rs:1668:9
     |
1668 |         vault.join("xlib").exists() == false
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `!vault.join("xlib").exists()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_comparison
     = note: `#[warn(clippy::bool_comparison)]` on by default

warning: useless use of `format!`
    --> tests/cli/highlights/scan.rs:2445:9
     |
2445 |         format!("{text}").into_bytes(),
     |         ^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `text.to_string()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format
     = note: `#[warn(clippy::useless_format)]` on by default

warning: useless use of `format!`
    --> tests/cli/highlights/scan.rs:2647:9
     |
2647 |         format!("{text}").into_bytes(),
     |         ^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `text.to_string()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format

warning: useless use of `format!`
   --> tests/cli/highlights/scan_intake.rs:776:9
    |
776 |         format!("{text}").into_bytes(),
    |         ^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `text.to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format

warning: useless use of `format!`
    --> tests/cli/highlights/scan_intake.rs:1144:24
     |
1144 |         line.contains(&format!(" (v2)]] [created::")),
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `" (v2)]] [created::".to_string()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format

warning: the borrowed expression implements the required traits
   --> tests/cli/highlights/scan_integration.rs:674:29
    |
674 |         !fs::read_to_string(&vault.join("mac_inbox.md"))
    |                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `vault.join("mac_inbox.md")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
  --> tests/cli/ref_library/migrate_tasks.rs:85:32
   |
85 |     let output = git_in(vault, &["log", "--format=%s"]);
   |                                ^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["log", "--format=%s"]`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:226:20
    |
226 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:227:20
    |
227 |     git_in(&vault, &["commit", "-q", "-m", "dep"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "dep"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:357:20
    |
357 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:358:20
    |
358 |     git_in(&vault, &["commit", "-q", "-m", "unmapped"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "unmapped"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:381:20
    |
381 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:382:20
    |
382 |     git_in(&vault, &["commit", "-q", "-m", "mapped"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "mapped"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:458:20
    |
458 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:459:20
    |
459 |     git_in(&vault, &["commit", "-q", "-m", "crash"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "crash"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args

warning: used `assert_eq!` with a literal bool
   --> tests/cli/task_move.rs:343:5
    |
343 | /     assert_eq!(
344 | |         fs::read_to_string(vault.join("source.md"))
345 | |             .unwrap()
346 | |             .contains("Move this task"),
347 | |         false
348 | |     );
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#bool_assert_comparison
help: replace it with `assert!(..)`
    |
343 ~     assert!(
344 ~         !fs::read_to_string(vault.join("source.md"))
345 |             .unwrap()
346 ~             .contains("Move this task")
    |

warning: `bob-obsidian` (test "cli") generated 39 warnings (run `cargo clippy --fix --test "cli" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 38 suggestions)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.13s
succeeded  exit=0  duration=322ms

