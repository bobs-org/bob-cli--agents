# Chat History - ace-run (bob-cli-5y.10--mon)

- **TIMESTAMP:** 2026-10-09 20:38:35 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** bob-cli-5y.10--mon

## Prompt

sase monitor start --command 'just check' --reason 'Verify before host completion'

## Response

sase tool run 0307e74932af8cd9c686ccdd3dbe9ed6

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
cargo clippy --all-targets --all-features
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
warning: unused import: `self::model::RefParent`
   --> src/native/capture_language/mod.rs:102:16
    |
102 | pub(crate) use self::model::RefParent;
    |                ^^^^^^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:297:12
    |
297 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:120:20
    |
120 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#int_plus_one

warning: unused import: `RegionTask`
   --> src/native/highlights_ref/mod.rs:155:39
    |
155 |     split_note_body, RegionBlockKind, RegionTask,
    |                                       ^^^^^^^^^^

warning: unused import: `TrackerHit`
  --> src/native/ref_library/mod.rs:51:40
   |
51 | pub(crate) use status::{decide_status, TrackerHit};
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

warning: unused imports: `InsertedRefTask` and `insert_ref_task`
  --> src/native/ref_tasks/mod.rs:27:5
   |
27 |     insert_ref_task, insert_ref_task_with_preferred_id, InsertedRefTask,
   |     ^^^^^^^^^^^^^^^                                     ^^^^^^^^^^^^^^^

warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, `RefFollowUp`, `sanitize_title_alias`, and `stamp_close_date_any_id`
  --> src/native/ref_tasks/mod.rs:31:27
   |
31 |     render_ref_task_line, sanitize_title_alias, slug_ref_stem,
   |                           ^^^^^^^^^^^^^^^^^^^^
32 |     stamp_close_date_any_id, strip_blockquote_prefix, task_mark, OrphanRefTask,
   |     ^^^^^^^^^^^^^^^^^^^^^^^                                      ^^^^^^^^^^^^^
33 |     RefFollowUp, REF_BLOCK_ID_MAX_LEN,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^

warning: unused imports: `managed_region_line_range` and `parse_tracker_line`
  --> src/native/ref_tasks/mod.rs:40:20
   |
40 |     find_trackers, managed_region_line_range, parse_tracker_line, TrackerHit,
   |                    ^^^^^^^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^

warning: unused imports: `find_trackers`, `managed_region_line_range`, and `parse_tracker_line`
   --> src/native/ref_library/status.rs:308:5
    |
308 |     find_trackers, managed_region_line_range, parse_tracker_line,
    |     ^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^

warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, `RefFollowUp`, and `sanitize_title_alias`
  --> src/native/ref_tasks/mod.rs:31:27
   |
31 |     render_ref_task_line, sanitize_title_alias, slug_ref_stem,
   |                           ^^^^^^^^^^^^^^^^^^^^
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

warning: struct `RefParent` is never constructed
   --> src/native/capture_language/model.rs:426:19
    |
426 | pub(crate) struct RefParent {
    |                   ^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: method `ref_parent` is never used
   --> src/native/gkeep/ledger.rs:366:19
    |
249 | impl Journal {
    | ------------ method in this implementation
...
366 |     pub(super) fn ref_parent(&self, id: &str, fp: &str) -> Option<String> {
    |                   ^^^^^^^^^^

warning: field `refreshed` is never read
    --> src/native/highlights_ref/sync.rs:1705:5
     |
1703 | struct V2ReadingOutcome {
     |        ---------------- field in this struct
1704 |     execution: Option<ReadingTaskExecution>,
1705 |     refreshed: Option<ref_tasks_mod::LocatedRefTask>,
     |     ^^^^^^^^^

warning: function `insert_ref_task` is never used
  --> src/native/ref_tasks/insert.rs:45:15
   |
45 | pub(crate) fn insert_ref_task(
   |               ^^^^^^^^^^^^^^^

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1079:24
     |
1079 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#type_complexity
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#type_complexity

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:633:9
    |
633 | /         let Some(relative_close) = line[open..].find(')') else {
634 | |             return None;
635 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: this `match` expression can be replaced with `?`
   --> src/native/capture/pomodoro_adjust.rs:882:19
    |
882 |       let minutes = match minutes_part {
    |  ___________________^
883 | |         Some(part) => {
884 | |             let part = part.trim();
885 | |             let core = part.strip_suffix('m')?;
...   |
895 | |         None => return None,
896 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
882 ~     let minutes = {
883 +         let part = minutes_part?;
884 +         let part = part.trim();
885 +         let core = part.strip_suffix('m')?;
886 +         let core = core.trim_end();
887 +         if core.is_empty() {
888 +             return None;
889 +         }
890 +         if !core.bytes().all(|byte| byte.is_ascii_digit()) {
891 +             return None;
892 +         }
893 +         core.parse::<u64>().ok()?
894 ~     };
    |

warning: manual `rem_euclid` implementation
   --> src/native/capture/pomodoro_adjust.rs:988:5
    |
988 |     (((value % 1440) + 1440) % 1440) as u64
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `value.rem_euclid(1440)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_rem_euclid
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `map_or` can be simplified
   --> src/native/capture/pomodoro_start.rs:419:20
    |
419 |                 && anchor.map_or(true, |anchor| *index > anchor)
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_map_or
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#ptr_arg
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_guards
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: unnecessary map of the identity function
   --> src/native/capture_language/editor_classify.rs:612:60
    |
612 |               let (after_x, x_len) = classify_link_close(raw)
    |  ____________________________________________________________^
613 | |                 .map(|(selection, x_len)| (selection, x_len))
    | |_____________________________________________________________^ help: remove the call to `map`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#map_identity
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#large_enum_variant
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:1675:17
     |
1675 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture_language/item.rs:171:9
    |
171 | /         let Some(route) = route_parsed.route else {
172 | |             return None;
173 | |         };
    | |__________^ help: replace it with: `let route = route_parsed.route?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1684:31
     |
1684 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_guards
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#map_identity

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
1571 -             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
1571 +             Err(POMODORO_LINK_SHAPE_ERROR.to_string())
     |

warning: this `match` expression can be replaced with `?`
   --> src/native/capture_link_tasks.rs:290:9
    |
290 | /         match best_field_tier(raw_fields, term) {
291 | |             Some(tier) => total += tier,
292 | |             None => return None,
293 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
290 ~         {
291 +             let tier = best_field_tier(raw_fields, term)?;
292 +             total += tier
293 +         }
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#large_enum_variant
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

warning: using `chunks_exact` with a constant chunk size
   --> src/native/capture_pomodoro_close/links.rs:255:10
    |
255 |         .chunks_exact(2)
    |          ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0.iter()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chunks_exact_to_as_chunks
    = note: `#[warn(clippy::chunks_exact_to_as_chunks)]` on by default

warning: using `chunks_exact` with a constant chunk size
  --> src/native/dataview/functions/scalar.rs:36:24
   |
36 |     for pair in values.chunks_exact(2) {
   |                        ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chunks_exact_to_as_chunks

warning: the borrowed expression implements the required traits
   --> src/native/env.rs:301:13
    |
301 |             &dir.join(file_name),
    |             ^^^^^^^^^^^^^^^^^^^^ help: change this to: `dir.join(file_name)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/gkeep/plan.rs:293:9
    |
293 | /         let Some(route) = parse_trailing_route(route_token) else {
294 | |             return None;
295 | |         };
    | |__________^ help: replace it with: `let route = parse_trailing_route(route_token)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/gkeep/plan.rs:296:9
    |
296 | /         let Some(intent) = classify_token(url_token) else {
297 | |             return None;
298 | |         };
    | |__________^ help: replace it with: `let intent = classify_token(url_token)?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` can be collapsed into the outer `match`
   --> src/native/highlights_ref/attach.rs:166:17
    |
166 | /                 if value.is_some_and(|value| !value.is_empty()) {
167 | |                     has_audio = true;
168 | |                 }
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_match
    = note: `#[warn(clippy::collapsible_match)]` on by default
help: collapse nested if block
    |
165 ~             "audio"
166 ~                 if value.is_some_and(|value| !value.is_empty()) => {
167 |                     has_audio = true;
168 ~                 }
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_match
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chars_next_cmp
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:154:34
    |
154 |                         url.host.replace('.', "_").replace('-', "_"),
    |                                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '-'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:310:33
    |
310 |     format!("arxiv_{}", full_id.replace('.', "_").replace('/', "_"))
    |                                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '/'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
519 ~         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
520 ~         && let Some(rel) = relative_inside(&child_c, &parent_c) {
521 |             return Some(rel);
522 ~         }
    |

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#useless_format
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
399 ~         if let Err(error) = fs::remove_file(path)
400 ~             && error.kind() != std::io::ErrorKind::NotFound {
401 |                 failures.push(format!(
...
404 |                 ));
405 ~             }
    |

warning: the loop variable `index` is used to index `lines`
  --> src/native/ref_tasks/embed.rs:76:22
   |
76 |         for index in start..end.min(lines.len()) {
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_range_loop
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_range_loop
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_pattern_char_comparison
   = note: `#[warn(clippy::manual_pattern_char_comparison)]` on by default

warning: this manual char comparison can be written more succinctly
  --> src/native/ref_tasks/line.rs:79:53
   |
79 |     let trimmed_start = stripped.trim_start_matches(|c| c == ' ' || c == '\t');
   |                                                     ^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `[' ', '\t']`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_pattern_char_comparison

warning: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#explicit_counter_loop
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
648 ~         if (b == b'#' || b == b'^') {
649 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
650 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
653 |                 return true;
654 ~             }
    |

warning: using `chunks_exact` with a constant chunk size
   --> src/native/task_dependencies/mod.rs:198:10
    |
198 |         .chunks_exact(2)
    |          ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0.iter()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chunks_exact_to_as_chunks

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_locals
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#derivable_impls
    = note: `#[warn(clippy::derivable_impls)]` on by default
help: replace the manual implementation with a derive attribute
    |
158 + #[derive(Default)]
159 | struct RunOptions {
    |

warning: `bob-cli` (lib) generated 108 warnings (run `cargo clippy --fix --lib -p bob-cli -- ` to apply 50 suggestions)
warning: associated function `for_tests` is never used
   --> src/native/highlights_ref/model.rs:484:19
    |
472 | impl ScanContext {
    | ---------------- associated function in this implementation
...
484 |     pub(super) fn for_tests(
    |                   ^^^^^^^^^

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#match_single_binding
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#match_single_binding
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#match_single_binding
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call
     = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2029:48
     |
2029 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2038:22
     |
2038 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_match
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_element_loop
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check
    = note: `#[warn(clippy::unnecessary_get_then_check)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:764:9
    |
764 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
    = note: `#[warn(clippy::needless_borrow)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:796:9
    |
796 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:711:27
    |
711 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:723:27
    |
723 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:735:27
    |
735 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unused variable: `note`
   --> tests/cli/highlights/scan_integration.rs:480:9
    |
480 |     let note = vault.join("ref/missing.md");
    |         ^^^^ help: if this is intentional, prefix it with an underscore: `_note`
    |
    = note: `#[warn(unused_variables)]` (part of `#[warn(unused)]`) on by default

warning: `bob-cli` (lib test) generated 116 warnings (99 duplicates) (run `cargo clippy --fix --lib -p bob-cli --tests -- ` to apply 9 suggestions)
warning: for loop over a single element
   --> tests/cli/capture/parse_pomodoro_close.rs:328:5
    |
328 | /     for (text, range) in [("=x - wired", [3, 4])] {
329 | |         let value = parse(text);
330 | |         assert_eq!(
331 | |             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
...   |
338 | |         );
339 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_element_loop
    = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
    |
328 ~     {
329 +         let (text, range) = ("=x - wired", [3, 4]);
330 +         let value = parse(text);
331 +         assert_eq!(
332 +             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
333 +             "{text}"
334 +         );
335 +         assert_eq!(
336 +             value["diagnostics"][0]["range"],
337 +             serde_json::json!(range),
338 +             "{text}"
339 +         );
340 +     }
    |

warning: the borrowed expression implements the required traits
   --> tests/cli/capture/pomodoro_close_log.rs:346:18
    |
346 |             .arg(&args[0])
    |                  ^^^^^^^^ help: change this to: `args[0]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:451:14
    |
451 |         .arg("-2 =x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#suspicious_command_arg_space
    = note: `#[warn(clippy::suspicious_command_arg_space)]` on by default
help: consider splitting the argument
    |
451 -         .arg("-2 =x\n- 1 wired the lexer")
451 +         .args(["-2", "=x\n- 1 wired the lexer"])
    |

warning: unnecessary use of `to_string`
   --> tests/cli/capture/pomodoro_shift.rs:581:11
    |
581 |         + &String::from_utf8_lossy(&shape_out.stdout).to_string();
    |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `String::from_utf8_lossy(&shape_out.stdout).as_ref()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_to_owned
    = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: the borrowed expression implements the required traits
   --> tests/cli/highlights/scan_integration.rs:675:29
    |
675 |         !fs::read_to_string(&vault.join("mac_inbox.md"))
    |                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `vault.join("mac_inbox.md")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: `bob-cli` (test "cli") generated 6 warnings (run `cargo clippy --fix --test "cli" -p bob-cli -- ` to apply 5 suggestions)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 30.69s
cargo test --no-fail-fast
   Compiling bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
warning: unused import: `self::model::RefParent`
   --> src/native/capture_language/mod.rs:102:16
    |
102 | pub(crate) use self::model::RefParent;
    |                ^^^^^^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default

warning: unused import: `RegionTask`
   --> src/native/highlights_ref/mod.rs:155:39
    |
155 |     split_note_body, RegionBlockKind, RegionTask,
    |                                       ^^^^^^^^^^

warning: unused imports: `find_trackers`, `managed_region_line_range`, and `parse_tracker_line`
   --> src/native/ref_library/status.rs:308:5
    |
308 |     find_trackers, managed_region_line_range, parse_tracker_line,
    |     ^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^

warning: unused import: `TrackerHit`
  --> src/native/ref_library/mod.rs:51:40
   |
51 | pub(crate) use status::{decide_status, TrackerHit};
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

warning: unused imports: `InsertedRefTask` and `insert_ref_task`
  --> src/native/ref_tasks/mod.rs:27:5
   |
27 |     insert_ref_task, insert_ref_task_with_preferred_id, InsertedRefTask,
   |     ^^^^^^^^^^^^^^^                                     ^^^^^^^^^^^^^^^

warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, `RefFollowUp`, and `sanitize_title_alias`
  --> src/native/ref_tasks/mod.rs:31:27
   |
31 |     render_ref_task_line, sanitize_title_alias, slug_ref_stem,
   |                           ^^^^^^^^^^^^^^^^^^^^
32 |     stamp_close_date_any_id, strip_blockquote_prefix, task_mark, OrphanRefTask,
   |                                                                  ^^^^^^^^^^^^^
33 |     RefFollowUp, REF_BLOCK_ID_MAX_LEN,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^

warning: type `FindSummary` is more private than the item `print_find_json`
  --> src/native/ref_library/output.rs:61:1
   |
61 | / pub(crate) fn print_find_json(
62 | |     coverage: &Coverage,
63 | |     library: &LibraryCounts,
64 | |     summary: &FindSummary,
65 | |     results: &[FindResult],
66 | | ) {
   | |_^ function `print_find_json` is reachable at visibility `pub(crate)`
   |
note: but type `FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
  --> src/native/ref_library/find.rs:70:1
   |
70 | pub(super) struct FindSummary {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   = note: `#[warn(private_interfaces)]` on by default

warning: type `FindResult` is more private than the item `print_find_json`
  --> src/native/ref_library/output.rs:61:1
   |
61 | / pub(crate) fn print_find_json(
62 | |     coverage: &Coverage,
63 | |     library: &LibraryCounts,
64 | |     summary: &FindSummary,
65 | |     results: &[FindResult],
66 | | ) {
   | |_^ function `print_find_json` is reachable at visibility `pub(crate)`
   |
note: but type `FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
  --> src/native/ref_library/find.rs:57:1
   |
57 | pub(super) struct FindResult {
   | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `FindSummary` is more private than the item `render_find_human`
   --> src/native/ref_library/output.rs:250:1
    |
250 | / pub(crate) fn render_find_human(
251 | |     coverage: &Coverage,
252 | |     summary: &FindSummary,
253 | |     results: &[FindResult],
...   |
256 | |     width: usize,
257 | | ) -> String {
    | |___________^ function `render_find_human` is reachable at visibility `pub(crate)`
    |
note: but type `FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:70:1
    |
 70 | pub(super) struct FindSummary {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `FindResult` is more private than the item `render_find_human`
   --> src/native/ref_library/output.rs:250:1
    |
250 | / pub(crate) fn render_find_human(
251 | |     coverage: &Coverage,
252 | |     summary: &FindSummary,
253 | |     results: &[FindResult],
...   |
256 | |     width: usize,
257 | | ) -> String {
    | |___________^ function `render_find_human` is reachable at visibility `pub(crate)`
    |
note: but type `FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:57:1
    |
 57 | pub(super) struct FindResult {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `FindSummary` is more private than the item `render_find_markdown`
   --> src/native/ref_library/output.rs:492:1
    |
492 | / pub(crate) fn render_find_markdown(
493 | |     summary: &FindSummary,
494 | |     results: &[FindResult],
495 | | ) -> String {
    | |___________^ function `render_find_markdown` is reachable at visibility `pub(crate)`
    |
note: but type `FindSummary` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:70:1
    |
 70 | pub(super) struct FindSummary {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: type `FindResult` is more private than the item `render_find_markdown`
   --> src/native/ref_library/output.rs:492:1
    |
492 | / pub(crate) fn render_find_markdown(
493 | |     summary: &FindSummary,
494 | |     results: &[FindResult],
495 | | ) -> String {
    | |___________^ function `render_find_markdown` is reachable at visibility `pub(crate)`
    |
note: but type `FindResult` is only usable at visibility `pub(in crate::native::ref_library)`
   --> src/native/ref_library/find.rs:57:1
    |
 57 | pub(super) struct FindResult {
    | ^^^^^^^^^^^^^^^^^^^^^^^^^^^^

warning: struct `RefParent` is never constructed
   --> src/native/capture_language/model.rs:426:19
    |
426 | pub(crate) struct RefParent {
    |                   ^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default

warning: method `ref_parent` is never used
   --> src/native/gkeep/ledger.rs:366:19
    |
249 | impl Journal {
    | ------------ method in this implementation
...
366 |     pub(super) fn ref_parent(&self, id: &str, fp: &str) -> Option<String> {
    |                   ^^^^^^^^^^

warning: associated function `for_tests` is never used
   --> src/native/highlights_ref/model.rs:484:19
    |
472 | impl ScanContext {
    | ---------------- associated function in this implementation
...
484 |     pub(super) fn for_tests(
    |                   ^^^^^^^^^

warning: field `refreshed` is never read
    --> src/native/highlights_ref/sync.rs:1705:5
     |
1703 | struct V2ReadingOutcome {
     |        ---------------- field in this struct
1704 |     execution: Option<ReadingTaskExecution>,
1705 |     refreshed: Option<ref_tasks_mod::LocatedRefTask>,
     |     ^^^^^^^^^

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

warning: `bob-cli` (lib test) generated 19 warnings (run `cargo fix --lib -p bob-cli --tests` to apply 8 suggestions)
warning: unused imports: `OrphanRefTask`, `REF_BLOCK_ID_MAX_LEN`, `RefFollowUp`, `sanitize_title_alias`, and `stamp_close_date_any_id`
  --> src/native/ref_tasks/mod.rs:31:27
   |
31 |     render_ref_task_line, sanitize_title_alias, slug_ref_stem,
   |                           ^^^^^^^^^^^^^^^^^^^^
32 |     stamp_close_date_any_id, strip_blockquote_prefix, task_mark, OrphanRefTask,
   |     ^^^^^^^^^^^^^^^^^^^^^^^                                      ^^^^^^^^^^^^^
33 |     RefFollowUp, REF_BLOCK_ID_MAX_LEN,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^^^

warning: unused imports: `managed_region_line_range` and `parse_tracker_line`
  --> src/native/ref_tasks/mod.rs:40:20
   |
40 |     find_trackers, managed_region_line_range, parse_tracker_line, TrackerHit,
   |                    ^^^^^^^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^

warning: function `insert_ref_task` is never used
  --> src/native/ref_tasks/insert.rs:45:15
   |
45 | pub(crate) fn insert_ref_task(
   |               ^^^^^^^^^^^^^^^

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

warning: `bob-cli` (lib) generated 25 warnings (16 duplicates) (run `cargo fix --lib -p bob-cli` to apply 2 suggestions)
warning: unused variable: `note`
   --> tests/cli/highlights/scan_integration.rs:480:9
    |
480 |     let note = vault.join("ref/missing.md");
    |         ^^^^ help: if this is intentional, prefix it with an underscore: `_note`
    |
    = note: `#[warn(unused_variables)]` (part of `#[warn(unused)]`) on by default

warning: `bob-cli` (test "cli") generated 1 warning (run `cargo fix --test "cli" -p bob-cli` to apply 1 suggestion)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 43.08s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/bob_cli-f63e4849155c311f)

running 2156 tests
test native::capture::budget::tests::destination_roles_follow_the_contract ... ok
test native::capture::budget::tests::theme_warning_names_added_themes_with_hint ... ok
test native::capture::output::tests::typed_entry_details_print_two_spaces_under_their_entry ... ok
test native::capture::output::tests::log_entry_details_omitted_when_empty ... ok
test native::capture::output::tests::typed_work_log_details_align_with_entries_when_present ... ok
test native::capture::output::tests::typed_work_log_details_omitted_when_no_entry_has_details ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_tab_children_and_interior_blanks ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_fenced_child_lines_verbatim ... ok
test native::capture::pomodoro_blocks::tests::block_range_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::block_range_trims_trailing_blanks_and_stops_at_zero_indent ... ok
test native::capture::pomodoro_blocks::tests::block_range_stops_at_section_end_and_covers_last_entry ... ok
test native::capture::pomodoro_blocks::tests::depth_continuation_lines_take_parent_depth_plus_one ... ok
test native::capture::pomodoro_blocks::tests::depth_counts_nested_list_items ... ok
test native::capture::pomodoro_blocks::tests::depth_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::pairing_pure_insert_is_added_and_pure_delete_is_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_replace_becomes_changed_with_before ... ok
test native::capture::pomodoro_blocks::tests::pairing_uneven_replace_splits_changed_added_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_created_block_is_all_added ... ok
test native::capture::pomodoro_blocks::tests::tracker_autodetects_an_unreported_child_insert ... ok
test native::capture::pomodoro_blocks::tests::resolution_rejects_a_non_entry_after - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_reports_one_cumulative_block_across_items ... ok
test native::capture::pomodoro_blocks::tests::forwarding_panics_when_a_tracked_headline_is_deleted - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_resolves_created_before_and_reports_roles_once ... ok
test native::capture::pomodoro_blocks::tests::vanished_entry_is_dropped_silently - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_forwards_a_tracked_block_across_an_insert_above ... ok
test native::capture::pomodoro_blocks::tests::unreported_headline_rewrite_emits_unchanged_block - should panic ... ok
test native::capture::tests::assembly::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::assembly::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembly::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::tests::assembly::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::assembly::formats_task_line ... ok
test native::capture::tests::assembly::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::assembly::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::assembly::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::tests::assembly::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::assembly::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::assembly::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::tests::assembly::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::assembly::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::assembly::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::assembly::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::assembly::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::assembly::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::tests::assembly::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::assembly::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::assembly::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::assembly::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::assembly::sub_bullet_insertion_keeps_dependency_lines_first ... ok
test native::capture::tests::grammar::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::tests::grammar::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::grammar::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::grammar::clip_markers_are_terminal_forgiving_and_can_be_disabled ... ok
test native::capture::tests::grammar::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::grammar::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::grammar::normalizes_whitespace ... ok
test native::capture::tests::grammar::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::grammar::parses_picker_task_refs_strictly ... ok
test native::capture::tests::grammar::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::grammar::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::grammar::parses_priority_tokens ... ok
test native::capture::tests::grammar::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::grammar::parses_schedule_tokens ... ok
test native::capture::tests::grammar::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::grammar::parses_scheduled_offsets_with_routes ... ok
test native::capture::tests::grammar::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::grammar::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::grammar::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::grammar::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::placement::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::placement::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::grammar::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::placement::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::tests::placement::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::placement::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::placement::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::placement::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::tests::placement::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::placement::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::placement::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::placement::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::tests::placement::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::placement::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::placement::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::placement::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::placement::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::grammar::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::tests::placement::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::placement::forced_route_rejects_terminal_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::placement::formats_bullet_line ... ok
test native::capture::tests::placement::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::tests::placement::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::placement::formats_sub_bullet_line ... ok
test native::capture::tests::placement::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::placement::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::placement::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::placement::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::placement::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::placement::inserts_after_single_top_level_task ... ok
test native::capture::tests::placement::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::placement::json_success_shape_is_stable ... ok
test native::capture::tests::placement::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::placement::legacy_standalone_bullet_markers_are_rejected ... ok
test native::capture::tests::placement::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::placement::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::placement::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::placement::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::placement::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::placement::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::tests::placement::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::placement::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::placement::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::started::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::placement::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::started::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::started::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::started::started_pomodoro_move_preserves_crlf ... ok
test native::capture::tests::started::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::started::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::started::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::tests::started::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture_block_ids::tests::suggestions_follow_the_pinned_examples ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_block_ids::tests::allowed_regex_agrees_with_validator_for_every_ascii_char ... ok
test native::capture_clip::tests::formats_headers ... ok
test native::capture_block_ids::tests::successor_mints_follow_the_pinned_vectors ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_block_ids::tests::used_covers_done_nontask_duplicates_and_document_order ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_completable_tasks::tests::guard_reasons_match_the_contract ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture_complete::tests::output::empty_json_context_is_null ... ok
test native::capture_complete::tests::output::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::output::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::output::json_shape_is_stable ... ok
test native::capture::tests::placement::formats_scheduled_date_from_offset ... ok
test native::capture::dependencies::tests::prefiltered_snapshot_matches_full_read ... ok
test native::capture::task_blocks::tests::toggle_plus_subbullet_shows_the_task_line_as_changed ... ok
test native::capture::task_blocks::tests::created_parent_reports_every_row_added ... ok
test native::capture::task_blocks::tests::authored_children_and_schedule_log_are_added_in_order ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_excludes_ready_tasks ... ok
test native::capture_complete::tests::output::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture_complete::tests::active_tasks::active_task_human_rows_name_the_queue ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture::task_blocks::tests::block_range_maps_byte_end_to_line_range ... ok
test native::capture::task_blocks::tests::global_batch_reports_one_block_with_two_added_rows ... ok
test native::capture::task_blocks::tests::crlf_note_reports_verbatim_texts_without_terminators ... ok
test native::capture_complete::tests::pomodoros::plan_themes_after_counts_only_fresh_non_exempt_components ... ok
test native::capture::task_blocks::tests::nested_parent_reports_depths_relative_to_its_line ... ok
test native::capture_complete::tests::pomodoros::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::output::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_schedule_log ... ok
test native::capture::task_blocks::tests::cross_note_first_touch_order_with_revisit_and_second_parent ... ok
test native::capture_completable_tasks::tests::recurring_today_rows_sink_below_visible_rows_in_the_same_entry ... ok
test native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture::task_blocks::tests::task_ref_parent_omits_block_id_but_reports_its_block ... ok
test native::capture::task_blocks::tests::interior_blank_lines_are_kept_in_the_block ... ok
test native::capture::task_blocks::tests::two_parents_forward_across_an_insert_above ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_candidates_omit_next_up ... ok
test native::capture::tests::commit::refuses_when_absent_target_appears_before_commit ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture::tests::commit::refuses_when_existing_target_deleted_before_commit ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture::tests::commit::refuses_when_second_note_edited_externally ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_suppresses_creation_for_open_name_matches ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::output::close_items_and_suffixes_request_no_completion ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_offers_creation_before_substring_and_nameable_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_completable_tasks::tests::hidden_and_recurring_sink_within_their_section ... ok
test native::capture_completable_tasks::tests::struck_fenced_and_depends_on_links_never_place ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_completable_tasks::tests::draft_selected_marks_only_other_items ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_puts_the_running_entry_last ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_filters_and_creates_by_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_again_rows_preview_plan_budget ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_matches_pomodoro_name_warnings ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_human_labels_cover_every_row_kind ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_lists_start_again_and_name_it_rows ... ok
test native::capture_active_tasks::tests::excludes_ready_tasks_even_with_now_text ... ok
test native::capture_dependency_tasks::tests::hidden_tasks_detect_only_the_exact_tag ... ok
test native::capture_dependency_tasks::tests::quoted_locator_round_trips_through_replacement ... ok
test native::capture_language::close_log::tests::assign_log_positions_follows_the_assignment_rule ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_language::close_log::tests::default_log_index_covers_every_close_shape ... ok
test native::capture_complete::tests::output::trailing_hash_fragment_requests_no_completion ... ok
test native::capture_completable_tasks::tests::empty_query_orders_today_first_then_status ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_complete::tests::parent_tasks::bare_plus_serves_vault_candidates_and_operator_hints ... ok
test native::capture_language::close_log::tests::first_bullet_kind_detection_skips_placeholders ... ok
test native::capture_language::close_log::tests::inline_entry_reports_dangling ... ok
test native::capture_completable_tasks::tests::open_tasks_list_with_locators_scheduled_and_suggestions ... ok
test native::capture_language::close_log::tests::inline_entry_defaults_and_leading_numbers ... ok
test native::capture_language::close_log::tests::mixed_numbering_fails_both_orders ... ok
test native::capture_language::close_log::tests::lexes_entries_and_details ... ok
test native::capture_language::close_log::tests::positional_entries_carry_their_typed_position ... ok
test native::capture_language::close_log::tests::reports_dangling ... ok
test native::capture_language::close_log::tests::rejects_bad_bullets ... ok
test native::capture_language::close_log::tests::inline_entry_reports_diagnostics_in_order ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_report_lexical_failures ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_stay_unresolved_without_a_selection ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_positionally_in_selection_mode ... ok
test native::capture_language::close_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::close_selection::tests::lex_reports_drop_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::close_selection::tests::lex_reports_park_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_short_alias_wildcards ... ok
test native::capture_language::close_selection::tests::lex_reports_valid_selections ... ok
test native::capture_language::close_selection::tests::selection_shape_detection ... ok
test native::capture_language::dependencies::tests::bare_sigil_is_directive_only_at_the_ends ... ok
test native::capture_language::dependencies::tests::escape_consumes_only_its_backslash ... ok
test native::capture_language::dependencies::tests::protected_spans_are_never_modifiers ... ok
test native::capture_language::dependencies::tests::mid_line_modifiers_stay_literal ... ok
test native::capture_language::dependencies::tests::quoted_escapes_decode ... ok
test native::capture_language::dependencies::tests::quoted_note_with_spaces_stays_atomic ... ok
test native::capture_language::dependencies::tests::trailing_complete_modifier_strips_and_spans ... ok
test native::capture_language::dependencies::tests::traversal_and_bad_ids_are_invalid ... ok
test native::capture_language::dependencies::tests::unicode_offsets_stay_on_char_boundaries ... ok
test native::capture_language::dependencies::tests::unterminated_quote_is_one_partial ... ok
test native::capture_language::project_tasks::tests::lexer_accepts_the_boundary_set ... ok
test native::capture_language::project_tasks::tests::reserved_name_matches_in_any_letter_case ... ok
test native::capture_language::project_tasks::tests::suffix_helpers_split_on_the_last_word ... ok
test native::capture_language::start_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::start_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::start_selection::tests::lex_reports_valid_drop_lists ... ok
test native::capture_language::tests::chain::bang_claim_beats_dependency_errors ... ok
test native::capture_language::tests::chain::chain_token_predicate_covers_the_documented_table ... ok
test native::capture_language::tests::chain::bang_items_claim_each_blank_line_block_independently ... ok
test native::capture_language::tests::chain::draft_chain_works_with_a_global_declaration ... ok
test native::capture_language::tests::chain::draft_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::draft_keeps_sequential_indices_across_crlf_with_a_chain ... ok
test native::capture_language::tests::chain::completion_requests_nothing_anywhere_on_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_a_two_token_chain_with_absolute_ranges ... ok
test native::capture_language::tests::chain::draft_splits_tabs_and_runs_of_spaces ... ok
test native::capture_language::tests::chain::chain_token_predicate_equals_claimed_for_single_tokens ... ok
test native::capture_language::tests::chain::editor_chain_items_do_not_inherit_a_global_declaration ... ok
test native::capture_language::tests::chain::draft_splits_override_chains_with_absolute_ranges ... ok
test native::capture_language::tests::chain::editor_reports_a_broken_second_token_with_its_own_diagnostic ... ok
test native::capture_language::tests::chain::editor_reports_a_dangling_close_separator_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_chain_with_absolute_spans ... ok
test native::capture_language::tests::chain::editor_reports_an_incomplete_named_start_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_plus_adjustment_chain ... ok
test native::capture_language::tests::chain::editor_reports_selection_spans_at_absolute_offsets_in_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_two_items_with_absolute_spans_for_a_chain ... ok
test native::capture_language::tests::chain::execution_carries_a_close_selection_through_a_chain ... ok
test native::capture_language::tests::chain::execution_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::execution_rejects_forced_destinations_on_the_first_chain_token ... ok
test native::capture_language::tests::chain::execution_reports_a_broken_second_token_on_its_own_range ... ok
test native::capture_language::tests::chain::execution_distinguishes_spaced_start_adjust_from_offset_start ... ok
test native::capture_language::tests::chain::execution_leaves_non_chains_unchanged ... ok
test native::capture_language::tests::chain::execution_switches_sessions_with_close_then_start ... ok
test native::capture_language::tests::chain::execution_runs_a_chain_left_to_right ... ok
test native::capture_language::tests::completion::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::completion::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_language::tests::completion::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion::completion_on_a_global_declaration_excludes_both_sigils_and_plus ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::block_id_project_note_sigil_is_excluded_from_replacement ... ok
test native::capture_language::tests::completion::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::completion::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::completion::empty_block_id_with_section_still_yields_a_task_section_field ... ok
test native::capture_language::tests::completion::empty_selector_after_hash_is_a_zero_length_task_section_field ... ok
test native::capture_language::tests::completion::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::completion::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::completion::hash_separator_is_not_part_of_block_id_or_section_replacement ... ok
test native::capture_language::tests::completion::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_language::tests::completion::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::completion::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::completion::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::completion::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::completion::operator_items_have_no_hash_completion ... ok
test native::capture_language::tests::completion::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_language::tests::completion::parent_task_plus_completes_the_terminal_token_with_utf8_byte_ranges ... ok
test native::capture_language::tests::completion::parent_task_plus_is_shared_across_parent_and_authored_lines ... ok
test native::capture_language::tests::completion::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_per_token_inside_chains ... ok
test native::capture_language::tests::completion::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture_language::tests::completion::pomodoro_override_name_completes_after_hash_with_wider_offsets ... ok
test native::capture_language::tests::completion::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::completion::parent_task_plus_preserves_operator_and_protected_text_boundaries ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_after_hash_on_a_named_start ... ok
test native::capture_language::tests::completion::pomodoro_start_name_leaves_link_form_names_alone ... ok
test native::capture_language::tests::completion::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_lone_colon ... ok
test native::capture_language::tests::completion::pomodoro_start_override_reports_sigil_and_suffix_emptiness ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_caret_id ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_partial_id ... ok
test native::capture_language::tests::completion::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_only_first_level_project_bullets ... ok
test native::capture_language::tests::completion::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::completion::task_block_id_route_and_authored_id_both_complete ... ok
test native::capture_language::tests::completion::task_section_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::completion::project_task_id_before_a_child_line_route_marker_still_completes ... ok
test native::capture_language::tests::completion::task_link_query_completes_the_sigil_inclusive_token ... ok
test native::capture_language::tests::completion::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::completion::work_log_bullet_lines_request_no_marker_completion ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::completion::trailing_hash_fragments_have_no_completion ... ok
test native::capture_language::tests::draft::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::completion::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::draft::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::draft::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::draft::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::draft::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::draft::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::draft::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::draft::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::draft::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::draft::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::draft::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::draft::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::draft::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::draft::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::draft::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::draft::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::draft::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::draft::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::draft::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::draft::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::draft::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::draft::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::draft::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::draft::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::draft::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_language::tests::draft::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::draft::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::editor_modes::editor_holds_unused_pomodoro_while_a_colon_id_is_unfinished ... ok
test native::capture_language::tests::editor_modes::caret_close_conflicts_agree_with_execution ... ok
test native::capture_language::tests::editor_modes::editor_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::editor_modes::editor_rejects_checkbox_only_project_task_ids_over_the_id_token ... ok
test native::capture_language::tests::editor_modes::editor_reports_override_family_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_complete_modes_needs_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_link_queries_as_incomplete ... ok
test native::capture_language::tests::editor_modes::editor_reports_named_pomodoro_start_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_reports_unused_project_note_pomodoro_over_the_name ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_start_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::editor_modes::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::editor_spans::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::editor_spans::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_language::tests::editor_spans::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::editor_modes::editor_reports_project_task_ids_with_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_modes::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_partial_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_now_tag_without_task_text ... ok
test native::capture_language::tests::editor_spans::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_modes::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_spans::editor_reports_legacy_bullet_markers_without_failing ... ok
test native::capture_language::tests::editor_modes::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::editor_spans::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_spans::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::editor_spans::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::editor_spans::editor_spans_cover_task_complete_tokens ... ok
test native::capture_language::tests::editor_spans::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::editor_spans::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_spans::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::editor_spans::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::editor_spans::task_link_query_spans_the_whole_token_as_a_placeholder ... ok
test native::capture_language::tests::editor_spans::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::globals::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::globals::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::globals::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::editor_spans::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::globals::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::globals::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_sub_bullet_and_keeps_authored_children ... ok
test native::capture_language::tests::globals::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::globals::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::globals::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::globals::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::globals::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::globals::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::globals::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::globals::task_complete_items_skip_global_inheritance ... ok
test native::capture_language::tests::grammar::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::grammar::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::grammar::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::grammar::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::grammar::execution_evaluates_project_note_markers_parents_and_children_in_order ... ok
test native::capture_language::tests::grammar::execution_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::grammar::bang_claim_covers_the_contract_table ... ok
test native::capture_language::tests::grammar::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::grammar::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::grammar::execution_keeps_other_trailing_hash_tags_rejected ... ok
test native::capture_language::tests::grammar::execution_keeps_task_id_lookalikes_literal_outside_project_notes ... ok
test native::capture_language::tests::grammar::execution_accepts_project_task_ids_and_strips_them_from_bodies ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_parses_override_family_with_identical_claim_rules ... ok
test native::capture_language::tests::grammar::execution_rejects_checkbox_only_project_task_ids ... ok
test native::capture_language::tests::grammar::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::grammar::execution_parses_equals_family_starts_alongside_close ... ok
test native::capture_language::tests::grammar::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_route_less_retired_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::grammar::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::grammar::execution_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::grammar::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::grammar::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::grammar::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::grammar::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::grammar::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::grammar::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::grammar::execution_rejects_project_task_id_rule_violations_verbatim ... ok
test native::capture_language::tests::grammar::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::grammar::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::grammar::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::grammar::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::grammar::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::grammar::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::grammar::plus_parent_picker_does_not_claim_operators_or_work_log_text ... ok
test native::capture_language::tests::grammar::plus_parent_picker_is_incomplete_but_keeps_the_lone_adjustment ... ok
test native::capture_language::tests::grammar::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::grammar::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::grammar::task_link_query_leaves_prose_byte_identical ... ok
test native::capture_language::tests::ref_grammar::bare_url_claims_reference_item_when_routing_is_on ... ok
test native::capture_language::tests::editor_modes::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::grammar::task_link_query_rejects_single_colon_tokens_with_teaching_errors ... ok
test native::capture_language::tests::ref_grammar::editor_url_list_items_each_report_ref ... ok
test native::capture_language::tests::ref_grammar::editor_ref_route_spans_use_byte_offsets_including_utf8 ... ok
test native::capture_language::tests::ref_grammar::editor_reports_ref_mode_with_one_exact_span ... ok
test native::capture_language::tests::ref_grammar::excluded_hosts_stay_tasks ... ok
test native::capture_language::tests::ref_grammar::mixed_list_classifies_each_line_on_its_own ... ok
test native::capture_language::tests::grammar::task_link_claim_is_equivalent_across_execution_editor_and_completion ... ok
test native::capture_language::tests::ref_grammar::forced_destination_global_and_clip_keep_tasks ... ok
test native::capture_language::tests::ref_grammar::routing_off_keeps_bare_url_a_task ... ok
test native::capture_language::tests::ref_grammar::url_list_split_handles_crlf_with_exact_ranges ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::ref_grammar::url_list_requires_every_line ... ok
test native::capture_language::tests::ref_grammar::url_list_block_splits_into_one_item_per_line ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::ref_grammar::claim_off_cases_stay_tasks ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_sub_bullet_local_marker ... ok
test native::capture_language::tests::ref_grammar::ref_parent_sources_cover_explicit_global_and_default ... ok
test native::capture_language::tests::rewrite::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_link_tasks::tests::ranker_orders_by_tier_sum_then_canonical_order ... ok
test native::capture_language::tests::rewrite::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_link_tasks::tests::ranker_passes_the_dependency_contract_dk_vectors ... ok
test native::capture_language::tests::grammar::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_language::tests::ref_grammar::claim_accepts_wrapper_case_and_hints ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_completable_tasks::tests::nonempty_query_keeps_today_matches_on_top ... ok
test native::capture_completable_tasks::tests::missing_day_file_means_no_today_rows ... ok
test native::capture_complete::tests::output::override_name_completion_omits_running_without_a_single_runner ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_complete::tests::routes_tasks::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::routes_tasks::default_task_completion_stays_identified_only ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::format_pomodoro_close_describes_wildcard_scope ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_lists_identified_tasks_before_unidentified_tasks ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_complete::tests::routes_tasks::route_completion_matches_aliases_with_canonical_replacement_after_prefix ... ok
test native::capture_parse::tests::format_pomodoro_close_reports_detail_counts ... ok
test native::capture_complete::tests::routes_tasks::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_search_keeps_identified_groups_ahead_of_unidentified ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_a_global_sub_bullet_declaration_and_local_override ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::parent_tasks::scoped_missing_and_empty_notes_keep_picker_and_empty_catalog ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_complete::tests::routes_tasks::task_block_id_completion_offers_routes_but_not_authored_ids ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_complete::tests::output::override_name_completion_carries_keeps_ledger_and_running ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_parse::tests::json_reports_invalid_start_suffixes_as_diagnostics ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_parse::tests::json_reports_override_starts_with_the_doubled_sigil ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_complete::tests::routes_tasks::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_named_pomodoro_starts ... ok
test native::capture_complete::tests::routes_tasks::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_completable_tasks::tests::today_roles_precedence_sessions_and_pomodoro ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_parse::tests::json_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_pomodoro_close::linked_task_tests::closing_a_dependent_leaves_depends_on_prerequisites_open ... ok
test native::capture_pomodoro_close::linked_task_tests::listed_duplicate_embedded_and_plain_warns_once_for_not_completed ... ok
test native::capture_pomodoro_close::linked_task_tests::custom_in_progress_symbol_gets_no_listed_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::mentioned_first_bare_link_gets_number_and_blocked_warning ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_empty_block_id_is_an_empty_success ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::linked_task_tests::same_task_numbered_twice_carries_lowest_number ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_lists_ranked_slugs_for_the_parent_task ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_warns_once_for_an_unresolvable_parent ... ok
test native::capture_pomodoro_close::selection_tests::embedded_hash_alias_and_tomato ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_pomodoro_close::selection_tests::conflicting_duplicates_fail_and_same_outcome_passes ... ok
test native::capture_pomodoro_close::selection_tests::drop_removes_from_closed_session_without_carry ... ok
test native::capture_pomodoro_close::selection_tests::fenced_links_are_unnumbered ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_typed_target_warns_and_stays_in_pomodoro ... ok
test native::capture_pomodoro_close::selection_tests::apply_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_listed_row_warns_exactly_once ... ok
test native::capture_pomodoro_close::selection_tests::lexically_resolved_positional_entry_reports_nested_wording ... ok
test native::capture_pomodoro_close::selection_tests::log_entries_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_nest_undated_in_task_work_log ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_appends_after_existing_descendants ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_lands_in_task_work_log_as_typed_subset ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_child_indent_follows_first_child_or_link_indent ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_preserve_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_text_that_numbers_a_link_fails_loudly ... ok
test native::capture_pomodoro_close::selection_tests::mixed_lines_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::nested_bare_links_are_numbered ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_on_complete_target_lands_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_nest_one_level_under_the_entry ... ok
test native::capture_complete::tests::task_links::task_link_completion_keeps_candidates_when_the_day_file_is_missing ... ok
test native::capture_pomodoro_close::selection_tests::numbers_the_worked_example ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_complete_writes_done_task_with_completion_date ... ok
test native::capture_pomodoro_close::selection_tests::listed_blocked_and_done_warnings ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_align_with_typed_entries ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_with_one_and_zero_links ... ok
test native::capture_complete::tests::task_links::task_link_completion_lists_worked_example_in_canonical_order ... ok
test native::capture_pomodoro_close::selection_tests::none_is_byte_identical_to_plan_ledger_close ... ok
test native::capture_pomodoro_close::selection_tests::full_close_reports_numbered_lineup_with_none ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_resolve_against_session_worked_links ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_messages ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_errors ... ok
test native::capture_complete::tests::task_links::task_link_completion_pins_json_shape_and_omissions ... ok
test native::capture_pomodoro_close::selection_tests::outcome_table_covers_every_row ... ok
test native::capture_pomodoro_close::selection_tests::parked_links_record_work_but_are_not_carried ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_accepts_an_empty_lineup_but_explicit_positive_indices_do_not ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_follow_drop_and_complete_outcomes ... ok
test native::capture_complete::tests::task_links::task_link_human_rows_name_queues_and_missing_ids ... ok
test native::capture_pomodoro_close::selection_tests::positional_resolution_reports_session_failures ... ok
test native::capture_pomodoro_close::selection_tests::rewrite_keeps_prefix_and_drops_tomato ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_share_a_single_worked_link ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_skip_nested_links ... ok
test native::capture_complete::tests::task_links::task_link_completion_scopes_to_the_batch_second_item ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_positional_logs_wait_for_and_use_top_level_worked_lineup ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_in_progress_and_complete_updates_both_tasks ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x2 ... ok
test native::capture_complete::tests::output::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_complete::tests::task_links::task_link_completion_queries_cover_the_sigil_and_rank ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_dated_work_logs ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_complete::tests::output::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::output::close_bullet_lines_suppress_wikilink_block_but_keep_note ... ok
test native::capture_complete::tests::routes_tasks::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_complete::tests::parent_tasks::leading_plus_query_refetch_keeps_token_range_and_full_catalog ... ok
test native::capture_completable_tasks::tests::bang_replacement_quotes_reserved_locators ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x_complete ... ok
test native::capture_complete::tests::parent_tasks::plus_query_ranks_candidates_and_scoped_descriptors_keep_exact_ranges ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x1_complete_2 ... ok
test native::capture_dependency_tasks::tests::groups_follow_the_picker_sections ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_on_complete_target_land_in_completed_task ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_does_not_change_pomodoro_completion ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x0_and_x1_2 ... ok
test native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_dependency_tasks::tests::empty_query_orders_same_note_lanes_history ... ok
test native::capture_dependency_tasks::tests::catalog_covers_every_task_bearing_note_kind ... ok
test native::capture_dependency_tasks::tests::ranking_shares_the_tiered_matcher_vectors ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_complete::tests::parent_tasks::vault_catalog_excludes_non_capture_and_terminal_notes ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_link_tasks::tests::suggestions_avoid_used_ids_including_non_task_anchors ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_link_tasks::tests::pulls_forward_only_for_a_single_future_scheduled_field ... ok
test native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_link_tasks::tests::worked_example_lists_eight_rows_in_canonical_order ... ok
test native::capture_link_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_outcomes_cover_remaining_numbered_links_and_keep_exceptions ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_dependency_tasks::tests::unique_basename_resolves_before_ambiguous_paths ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_complete::tests::routes_tasks::task_completion_before_an_explicit_toggle_bang_does_not_replace_the_bang ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture_link_tasks::tests::warns_when_the_day_file_is_missing_but_lists_tasks ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_pomodoro_start::drop_tests::created_session_reports_the_new_session_variant ... ok
test native::capture_link_tasks::tests::excludes_closed_unknown_terminal_untyped_and_unroutable ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_link_tasks::tests::ranker_matches_the_worked_example_queries ... ok
test native::capture_pomodoro_start::drop_tests::drops_embedded_and_unresolved_rows_by_number ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_pomodoro_start::drop_tests::drops_nested_links_with_their_parent ... ok
test native::capture_pomodoro_start::drop_tests::drops_numbered_subtree_and_keeps_gaps ... ok
test native::capture_pomodoro_start::drop_tests::empty_lineup_suggests_the_token_without_its_drop ... ok
test native::capture_pomodoro_start::drop_tests::empty_drop_is_byte_identical ... ok
test native::capture_pomodoro_start::drop_tests::duplicate_still_queued_warns ... ok
test native::capture_pomodoro_start::drop_tests::fenced_lines_are_not_numbered ... ok
test native::capture_pomodoro_start::drop_tests::three_bad_numbers_join_with_commas ... ok
test native::capture_pomodoro_start::drop_tests::preserves_crlf ... ok
test native::capture_pomodoro_start::drop_tests::out_of_range_names_every_bad_number ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_start::lineup_tests::lists_direct_children_in_ledger_order ... ok
test native::capture_complete::tests::routes_tasks::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_pomodoro_start::drop_tests::dropped_last_line_without_final_newline_leaves_none ... ok
test native::capture_pomodoro_start::lineup_tests::skips_deeper_descendants_embeds_and_struck_lines ... ok
test native::capture_pomodoro_start::lineup_tests::skips_fenced_lines ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoro_start::lineup_tests::resolves_rows_through_the_staged_view ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture_pomodoro_start::drop_tests::dropped_middle_line_without_final_newline_keeps_structure ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_without_a_current_session ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::caret_task_keeps_its_authored_checkbox ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::named_all_caps_bullet_with_children_stays_a_task ... ok
test native::capture_project_note::tests::named_task_keeps_an_existing_created_stamp_before_the_id ... ok
test native::capture_project_note::tests::named_tasks_render_ids_last_with_next_status_for_links ... ok
test native::capture_project_note::tests::prj_task_is_never_linked ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::scheduled_date_lands_in_frontmatter_with_a_blocked_checkbox ... ok
test native::capture_project_note::tests::section_title_shape_rejects_mixed_case_and_banners ... ok
test native::capture_project_note::tests::scheduled_project_renders_linked_tasks_as_blocked ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::json_reports_a_task_toggle_notice_without_changing_text ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_rewrite::tests::close_items_are_never_rewritten ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_for_a_childless_task ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_after_existing_children ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_legacy_marker ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_spaced_marker ... ok
test native::capture_schedule_log::tests::insertion_ignores_a_marker_nested_under_another_child ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_tabbed_marker ... ok
test native::capture_schedule_log::tests::insertion_preserves_crlf_endings ... ok
test native::capture_schedule_log::tests::insertion_preserves_a_missing_final_newline ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_schedule_log::tests::randomize_reason_appends_the_until_base ... ok
test native::capture_schedule_log::tests::randomize_reason_keeps_a_fixed_window ... ok
test native::capture_schedule_log::tests::randomize_reason_names_the_tool_without_a_from_suffix ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_task_sections::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_sections::tests::checkboxed_all_caps_children_are_not_sections ... ok
test native::capture_task_sections::tests::empty_section_bullet_still_qualifies ... ok
test native::capture_task_sections::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_task_sections::tests::grandchild_is_not_a_direct_child_section ... ok
test native::capture_task_sections::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_task_sections::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_task_sections::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_task_sections::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_task_sections::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_task_sections::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_task_toggle::tests::blocked_is_forced_to_next ... ok
test native::capture_task_sections::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_task_sections::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_task_sections::tests::managed_logs_are_never_sections_plain_titles_are ... ok
test native::capture_task_toggle::tests::errors_on_multiple_open_timed_entries ... ok
test native::capture_task_toggle::tests::errors_when_no_pomodoros_section ... ok
test native::capture_task_toggle::tests::errors_when_no_eligible_open_entry ... ok
test native::capture_task_sections::tests::title_whitelist_edges ... ok
test native::capture_task_sections::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_task_toggle::tests::implicit_insertion_falls_back_to_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::idempotent_insertion_skips_when_already_linked ... ok
test native::capture_task_toggle::tests::invalid_pomodoro_name_is_rejected ... ok
test native::capture_task_toggle::tests::insertion_removes_duplicate_from_later_open_entry ... ok
test native::capture_task_toggle::tests::implicit_insertion_targets_single_open_timed_entry ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_for_completed_entries ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::collect_done::tests::unit::adds_archive_parent_to_existing_frontmatter ... ok
test native::capture_pomodoros::tests::task_link_count_numbers_only_numbered_links ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::collect_done::tests::unit::adds_done_tasks_to_existing_source_frontmatter ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_complete::tests::parent_tasks::unicode_duplicates_and_queued_pomodoros_stay_in_catalog ... ok
test native::collect_done::tests::unit::block_ids_are_only_end_of_line_obsidian_anchors ... ok
test native::collect_done::tests::unit::completed_child_moves_without_collecting_active_parent ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_for_new_archive_note ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_with_nested_source_parent ... ok
test native::collect_done::tests::unit::creates_source_frontmatter_for_done_tasks ... ok
test native::collect_done::tests::unit::dependency_ids_preserve_path_case_and_qualify_nested_notes ... ok
test native::capture_pomodoros::tests::task_link_count_reports_ten_or_more_links ... ok
test native::capture_pomodoros::tests::task_link_count_is_null_with_multiple_open_timed_entries ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_are_ambiguous ... ok
test native::collect_done::tests::unit::below_threshold_block_ids_do_not_trigger_link_repair ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... ok
test native::collect_done::tests::plan::task_moving_plan_writes_archive_with_nested_source_parent ... ok
test native::capture_pomodoros_agenda::tests::overnight_ranges_roll_the_end_date ... ok
test native::capture_pomodoros_agenda::tests::current_numbers_match_number_task_links_walk ... ok
test native::collect_done::tests::unit::extracts_nested_blocks_and_continuations ... ok
test native::collect_done::tests::unit::extracts_block_ids_from_every_moved_task_block_line ... ok
test native::capture_pomodoros_agenda::tests::crlf_and_missing_final_newline_resolve ... ok
test native::collect_done::tests::unit::inserts_missing_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_become_unique_archive_ids ... ok
test native::collect_done::tests::unit::leaves_correct_archive_frontmatter_unchanged ... ok
test native::collect_done::tests::unit::leaves_correct_done_tasks_frontmatter_unchanged ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_pomodoros_agenda::tests::roles_numbers_and_retired_counts ... ok
test native::collect_done::tests::unit::maps_archive_notes_to_obsidian_wiki_links ... ok
test native::capture_pomodoros_agenda::tests::logs_tag_subtrees_and_prose_is_untagged ... ok
test native::collect_done::tests::unit::maps_source_notes_to_archive_notes ... ok
test native::collect_done::tests::unit::maps_source_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::unit::parses_attached_short_threshold_option ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::collect_done::tests::unit::parses_default_threshold ... ok
test native::capture_pomodoros_agenda::tests::task_block_lines_have_clean_text_kinds_and_depths ... ok
test native::collect_done::tests::unit::parses_short_threshold_equals_option ... ok
test native::collect_done::tests::unit::parses_short_threshold_option ... ok
test native::collect_done::tests::unit::parses_threshold_equals_option ... ok
test native::collect_done::tests::unit::parses_threshold_option ... ok
test native::collect_done::tests::unit::pathless_archive_links_gain_the_source_note_path ... ok
test native::collect_done::tests::unit::prepends_archive_frontmatter_when_existing_note_has_none ... ok
test native::collect_done::tests::unit::preserves_crlf_when_adding_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::preserves_crlf_when_repairing_archive_frontmatter ... ok
test native::collect_done::tests::unit::preserves_line_endings_in_source_and_archive ... ok
test native::collect_done::tests::unit::recognizes_done_and_canceled_task_lines_only ... ok
test native::collect_done::tests::unit::rejects_zero_threshold ... ok
test native::collect_done::tests::unit::replaces_stale_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::replaces_stale_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::updates_existing_archive_parent_frontmatter ... ok
test native::collect_done::tests::unit::repairs_wikilinks_embeds_and_aliases_to_moved_blocks ... ok
test native::completion::adapters::tests::bash_stamp_matches_protocol ... ok
test native::collect_done::tests::unit::repairs_simple_markdown_inline_block_links ... ok
test native::collect_done::tests::unit::repairs_same_note_nested_and_unique_basename_links ... ok
test native::collect_done::tests::unit::markdown_repair_skips_wikilink_spans ... ok
test native::collect_done::tests::unit::leaves_ambiguous_basename_links_unchanged ... ok
test native::completion::adapters::tests::zsh_stamp_matches_protocol ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_rewrites_exact_tokens_only ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_supports_task_field_grammar_and_skips_code ... ok
test native::completion::kinds::tests::path_specific_entries_win ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::capture_task_sections::tests::resolved_task_with_no_sections_is_a_successful_empty_list ... ok
test native::capture_task_sections::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::collect_done::tests::plan::canceled_only_tasks_below_threshold_remain_in_source ... ok
test native::collect_done::tests::plan::already_linked_source_with_existing_archive_is_not_planned ... ok
test native::collect_done::tests::plan::canceled_only_tasks_move_when_threshold_is_met ... ok
test native::collect_done::tests::plan::collecting_tasks_adds_done_tasks_to_source ... ok
test native::capture_task_sections::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::completion::protocol::tests::encoder_sanitizes_fields_and_drops_bad_values ... ok
test native::completion::protocol::tests::parses_attached_forms ... ok
test native::completion::protocol::tests::parses_full_request ... ok
test native::collect_done::tests::plan::duplicate_moved_block_ids_do_not_rewrite_links ... ok
test native::collect_done::tests::plan::existing_archive_creates_metadata_only_source_update ... ok
test native::completion::protocol::tests::rejects_malformed_requests ... ok
test native::collect_done::tests::plan::existing_archive_with_stale_metadata_creates_archive_only_plan ... ok
test native::completion::report::tests::tilde_collapses_home ... ok
test native::completion::tests::deadline_defaults_and_falls_back ... ok
test native::collect_done::tests::plan::generated_and_template_directories_are_not_collected_or_repaired ... ok
test native::completion::tree::tests::hand_descriptor_drift ... ok
test native::collect_done::tests::plan::includes_nested_path_note_when_it_meets_threshold ... ok
test native::collect_done::tests::plan::missing_archive_without_threshold_tasks_is_not_planned ... ok
test native::completion::tree::tests::descriptor_names_match_canonical_paths ... ok
test native::collect_done::tests::plan::link_repair_scan_includes_done_notes ... ok
test native::collect_done::tests::plan::planned_source_and_archive_contents_are_link_repaired ... ok
test native::collect_done::tests::plan::generated_tag_pages_do_not_make_source_basename_ambiguous ... ok
test native::collect_done::tests::plan::self_heals_preexisting_block_links_to_archive ... ok
test native::capture_pomodoros_agenda::tests::long_task_blocks_truncate_at_150_lines ... ok
test native::collect_done::tests::unit::block_id_deduplication_preserves_crlf_line_endings ... ok
test native::collect_done::tests::plan::scans_markdown_files_with_exclusions_and_threshold ... ok
test native::completion::tree::tests::hidden_aliases_and_help_are_absent ... ok
test native::completion::tree::tests::mounted_names_have_no_spaces ... ok
test native::completion::context::tests::unknown_words_never_fail_the_parse ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_preserves_distinct_moved_ids ... ok
test native::collect_done::tests::plan::task_moving_plan_repairs_links_in_separate_notes ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_skips_existing_candidates ... ok
test native::completion::context::tests::env_defaults_apply_without_flags ... ok
test native::completion::tree::tests::mounted_names_match_subcommands_in_order ... ok
test native::completion::present::tests::double_dash_offers_long_forms_only ... ok
test native::completion::tree::tests::tree_debug_assert_passes ... ok
test native::completion::kinds::tests::every_table_entry_matches_the_tree ... ok
test native::completion::context::tests::parses_long_route_and_bob_dir ... ok
test native::capture_pomodoros_agenda::tests::pomodoro_markers_and_prose_mix_with_links ... ok
test native::capture_pomodoros_agenda::tests::resolutions_cover_every_failure_mode ... ok
test native::capture_pomodoros_agenda::tests::unreadable_notes_fail_soft ... ok
test native::collect_done::tests::unit::existing_archive_block_ids_reserve_original_ids ... ok
test native::capture_targets::tests::scan_warns_on_shadowed_alias ... ok
test native::collect_done::tests::plan::source_block_id_keeps_links_pointing_at_source ... ok
test native::collect_done::tests::unit::unqualifiable_paths_do_not_abort_identity_indexing ... ok
test native::capture_targets::tests::scan_reads_aliases_and_warns_on_conflicts ... ok
test native::collect_done::tests::unit::link_repair_uses_renamed_unique_moved_block_id ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_task_sections::tests::lists_sections_in_document_order_for_a_block_id ... ok
test native::completion::protocol::tests::skew_messages_cover_both_directions ... ok
test native::config::plan::tests::missing_plan_file_loads_defaults ... ok
test native::config::plan::tests::max_ready_per_note_bounds_and_message ... ok
test native::completion::verify::tests::timeout_override_falls_back ... ok
test native::config::plan::tests::null_plan_block_loads_defaults ... ok
test native::config::freshness::tests::absent_freshness_block_loads_defaults ... ok
test native::config::freshness::tests::canonical_budget_key_wins_over_legacy ... ok
test native::config::freshness::tests::decay_false_counts_but_never_asks ... ok
test native::config::freshness::tests::decay_parses_zero_and_fixed_entry ... ok
test native::config::freshness::tests::lane_intervals_default_absent_and_null ... ok
test native::config::freshness::tests::missing_freshness_file_loads_defaults ... ok
test native::config::freshness::tests::legacy_budget_key_supplies_budget_with_deprecation_flag ... ok
test native::config::freshness::tests::legacy_budget_key_recovers_and_rejects_like_canonical ... ok
test native::config::freshness::tests::decay_defaults_when_absent_null_true_or_empty ... ok
test native::config::freshness::tests::null_freshness_block_loads_defaults ... ok
test native::config::freshness::tests::null_values_fall_back_to_defaults ... ok
test native::config::freshness::tests::parses_freshness_overrides_and_ignores_unknown_keys ... ok
test native::config::freshness::tests::tracker_intervals_default_absent_and_null ... ok
test native::config::plan::tests::absent_plan_block_loads_defaults ... ok
test native::config::plan::tests::absent_max_ready_per_note_falls_back_to_default ... ok
test native::config::freshness::tests::tracker_intervals_parse_integers ... ok
test native::config::freshness::tests::rejects_invalid_lane_intervals ... ok
test native::config::plan::tests::link_unblocked_defaults_true_and_parses_false ... ok
test native::config::freshness::tests::rejects_invalid_tracker_intervals ... ok
test native::config::freshness::tests::rejects_invalid_decay_values ... ok
test native::capture_pomodoros_agenda::tests::each_note_reads_once_per_filter_mode ... ok
test native::config::plan::tests::mistyped_plan_block_leaves_other_loaders_working ... ok
test native::config::freshness::tests::rejects_invalid_freshness_values ... ok
test native::config::freshness::tests::lane_intervals_parse_false_and_integers ... ok
test native::config::plan::tests::rejects_invalid_plan_values ... ok
test native::config::freshness::tests::mistyped_freshness_block_leaves_other_loaders_working ... ok
test native::config::tests::ignores_decay_and_rolls_keys ... ok
test native::config::tests::derive_seed_is_deterministic_and_sensitive_to_every_part ... ok
test native::config::tests::derive_seed_separator_prevents_part_boundary_collisions ... ok
test native::config::tests::missing_file_message_is_command_neutral ... ok
test native::config::tests::missing_gkeep_file_loads_defaults ... ok
test native::config::tests::mistyped_plan_block_leaves_gkeep_loader_working ... ok
test native::config::tests::blank_highlights_pre_scan_hook_disables_file_hook ... ok
test native::config::tests::blank_and_absent_listen_command_parse_as_none ... ok
test native::config::tests::mistyped_plan_block_leaves_highlights_loader_working ... ok
test native::config::tests::level_for_value_matches_exact_value_after_trim ... ok
test native::config::plan::tests::parses_plan_overrides_and_ignores_unknown_keys ... ok
test native::config::tests::parses_absent_gkeep_section_as_defaults ... ok
test native::config::tests::levels_exposes_every_configured_level ... ok
test native::config::tests::level_by_label_matches_ascii_case_insensitively ... ok
test native::config::tests::parses_absent_highlights_config_as_none ... ok
test native::config::tests::parses_highlights_listen_command_trimmed ... ok
test native::config::tests::mistyped_plan_block_leaves_priority_loader_working ... ok
test native::config::tests::parses_highlights_pre_scan_hook ... ok
test native::completion::context::tests::alias_words_rewrite_to_the_canonical_path ... ok
test native::config::tests::mix64_spreads_sequential_inputs ... ok
test native::config::tests::rejects_blank_value ... ok
test native::config::tests::rejects_duplicate_level_labels ... ok
test native::config::tests::parses_deployed_config ... ok
test native::config::tests::parses_full_gkeep_section_and_ignores_unknown_keys ... ok
test native::config::tests::rejects_non_integer_min_days ... ok
test native::config::tests::rejects_non_numeric_gkeep_timeout ... ok
test native::config::tests::parses_highlights_audio_link_template ... ok
test native::config::tests::resolve_config_path_expands_tilde_in_xdg_config_home ... ok
test native::completion::context::tests::parses_attached_and_short_cluster_forms ... ok
test native::config::tests::rejects_blank_label ... ok
test native::config::tests::resolve_config_path_falls_back_to_home_dot_config ... ok
test native::config::tests::resolve_config_path_falls_back_to_xdg_config_home ... ok
test native::config::tests::rejects_value_containing_field_syntax ... ok
test native::config::tests::resolve_config_path_ignores_empty_env_values ... ok
test native::config::tests::resolve_config_path_prefers_bob_config_file ... ok
test native::completion::context::tests::task_and_repo_need_their_subcommands ... ok
test native::config::tests::rejects_duplicate_level_values ... ok
test native::config::tests::roll_offset_returns_fixed_value_when_min_equals_max ... ok
test native::config::tests::rejects_invalid_gkeep_yaml ... ok
test native::config::tests::rejects_empty_levels ... ok
test native::config::tests::unrelated_highlights_keys_still_parse_with_listen_command ... ok
test native::dataview::tasks::filter::tests::apply_reports_a_missing_sandbox_for_function_filters ... ok
test native::config::tests::rejects_legacy_highlights_pre_scan_command ... ok
test native::config::tests::rejects_labels_that_differ_only_by_case ... ok
test native::config::tests::tolerates_unusual_sibling_properties ... ok
test native::dataview::tasks::filter::tests::apply_runs_without_a_sandbox_when_no_function_is_used ... ok
test native::dataview::tasks::filter::tests::global_filter_removal_only_removes_the_first_occurrence ... ok
test native::dataview::tasks::filter::tests::numbered_ranges_cover_year_month_quarter_and_iso_week ... ok
test native::config::tests::rejects_missing_priority_property ... ok
test native::config::tests::rejects_min_greater_than_max ... ok
test native::config::tests::rejects_missing_value ... ok
test native::dataview::tasks::filter::tests::relative_ranges_use_iso_weeks_and_calendar_boundaries ... ok
test native::config::tests::rejects_missing_schedules ... ok
test native::config::tests::rejects_negative_min_days ... ok
test native::dataview::tasks::filter::tests::weekday_and_offset_dates_are_pinned_to_now ... ok
test native::config::tests::rejects_wrong_schedules_target ... ok
test native::config::tests::roll_offset_p4_window_hits_both_extremes ... ok
test native::dataview::tasks::js::tests::init_budget_is_separate_from_and_above_expression_timeout ... ok
test native::dataview::tasks::filter::tests::absolute_ranges_are_inclusive_and_order_independent ... ok
test native::dataview::tasks::js::tests::init_budget_scales_with_task_count_and_caps ... ok
test native::dataview::tasks::index::tests::heading_parser_supports_atx_and_setext_headings ... ok
test native::dataview::tasks::parse::tests::numbered_date_ranges_optional_priority_is_and_status_boundary_parse ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::dataview::tasks::parse::tests::boolean_chains_use_tasks_precedence_and_allow_operand_apostrophes ... ok
test native::dataview::tasks::parse::tests::rejects_malformed_filters_with_actionable_errors ... ok
test native::dataview::tasks::parse::tests::ignore_global_query_can_come_from_query_file_defaults ... ok
test native::dataview::tasks::parse::tests::uses_javascript_detects_by_function_clauses ... ok
test native::completion::present::tests::attached_option_values_carry_prefix ... ok
test native::dataview::tasks::parse::tests::lane_queries_run_without_the_javascript_sandbox ... ok
test native::dataview::tasks::parse::tests::parses_every_v8_sort_group_and_layout_key ... ok
test native::dataview::tasks::parse::tests::parses_every_filter_family_and_boolean_combinations ... ok
test native::dataview::tasks::result::tests::natural_collation_is_case_insensitive_and_numeric ... ok
test native::dataview::tasks::parse::tests::scanner_matches_tasks_line_continuation_rules ... ok
test native::dataview::tasks::parse::tests::upstream_dialect_rejects_status_symbol_with_tasks_error ... ok
test native::dataview::tasks::result::tests::build_reports_a_missing_sandbox_for_function_sorts ... ok
test native::dataview::tasks::result::tests::build_runs_without_a_sandbox_when_no_function_is_used ... ok
test native::dataview::tasks::task::tests::file_context_matches_tasks_expose_properties ... ok
test native::dataview::tasks::result::tests::explanations_include_expanded_preset_statements ... ok
test native::dataview::tasks::settings::tests::unknown_task_format_falls_back_to_emoji ... ok
test native::dataview::tasks::task::tests::task_line_parser_matches_tasks_markers_and_spacing ... ok
test native::dataview::tasks::filter::tests::regex_flags_match_javascript_filtering_behavior ... ok
test native::dataview::tasks::task::tests::urgency_due_scheduled_and_start_boundaries_match_tasks_v8 ... ok
test native::completion::present::tests::text_started_slot_offers_no_options ... ok
test native::dataview::tasks::task::tests::recurrence_rules_are_validated_and_standardized ... ok
test native::dataview::tests::dql_grouped_table_rows_warn_and_fail_when_strict ... ok
test native::dataview::tasks::task::tests::removing_global_filter_preserves_spacing_and_only_removes_first_word ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_from_nested_blockquotes_and_callouts ... ok
test native::dataview::tasks::parse::tests::composes_global_defaults_presets_and_placeholders_in_order ... ok
test native::dataview::tests::dql_list_paths_use_list_pair_identity ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_with_heading_context ... ok
test native::dataview::tests::dql_missing_table_identities_warn_per_row ... ok
test native::dataview::tests::dql_table_paths_use_first_identity_column ... ok
test native::completion::present::tests::lone_dash_pairs_forms_with_identical_descriptions ... ok
test native::completion::kinds::tests::every_value_arg_has_a_decision ... ok
test native::dataview::tests::native_source_parser_accepts_phase3_source_surface ... ok
test native::dataview::tests::native_dql_parser_reports_representative_invalid_queries ... ok
test native::dataview::tests::source_paths_are_normalized_and_deduplicated ... ok
test native::freshness::placement::placement_tests::cancelled_is_refused_like_done ... ok
test native::freshness::placement::placement_tests::freshness_config_defaults_match_contract ... ok
test native::freshness::placement::placement_tests::keeps_absent_reads_zero ... ok
test native::freshness::placement::placement_tests::keeps_first_valid_wins_up_to_999 ... ok
test native::completion::tree::tests::parse_smoke ... ok
test native::freshness::placement::placement_tests::non_task_lines_are_refused ... ok
test native::freshness::placement::placement_tests::keeps_canonical_order_after_refresh ... ok
test native::freshness::placement::placement_tests::p01_bare_appends_fresh ... ok
test native::freshness::placement::placement_tests::generic_stamps_clear_keeps_including_same_day ... ok
test native::dataview::tests::dql_task_paths_resolve_grouped_task_source_notes ... ok
test native::freshness::placement::placement_tests::keeps_invalid_values_report_zero ... ok
test native::freshness::placement::placement_tests::keeps_key_match_is_exact_and_paren_reads ... ok
test native::freshness::placement::placement_tests::keeps_same_day_preserve_is_noop ... ok
test native::freshness::placement::placement_tests::p02_created_suffix ... ok
test native::freshness::placement::placement_tests::p04_interleaved_suffix ... ok
test native::freshness::placement::placement_tests::hooks_blocked_signals_survive_and_checkbox_swap_preserves_fresh ... ok
test native::freshness::placement::placement_tests::keeps_misplaced_lints_and_repairs ... ok
test native::freshness::placement::placement_tests::p03_block_id_only ... ok
test native::dataview::tests::native_dql_parser_accepts_phase3_command_surface ... ok
test native::dataview::tasks::task::tests::dataview_parser_extracts_all_fields_and_cleans_description ... ok
test native::dataview::tasks::task::tests::metadata_must_be_trailing_but_tags_can_be_interleaved ... ok
test native::dataview::tasks::task::tests::dataview_fields_honor_delimiters_whitespace_commas_and_case ... ok
test native::dataview::tasks::task::tests::unknown_status_is_todo_and_remove_global_filter_is_display_only ... ok
test native::dataview::tasks::task::tests::invalid_dates_and_recurrences_match_tasks_semantics ... ok
test native::dataview::tasks::task::tests::urgency_matches_tasks_v8_coefficients ... ok
test native::freshness::placement::placement_tests::p05_unknown_field_stays_left ... ok
test native::freshness::placement::placement_tests::p06_spacing_head_collapses_suffix_untouched ... ok
test native::freshness::placement::placement_tests::p07_restamp_replaces_date ... ok
test native::freshness::placement::placement_tests::p08_same_day_is_noop ... ok
test native::freshness::placement::placement_tests::p13_recurring_refused ... ok
test native::freshness::placement::placement_tests::p09_misplaced_is_repaired ... ok
test native::freshness::placement::placement_tests::p14_global_filter_floor ... ok
test native::freshness::placement::placement_tests::p12_set_and_clear_refresh ... ok
test native::freshness::placement::placement_tests::p17_done_refused ... ok
test native::freshness::placement::placement_tests::p18_deeply_indented_quote_is_not_a_task ... ok
test native::freshness::placement::placement_tests::p11_refresh_follows_fresh ... ok
test native::freshness::placement::placement_tests::p10_duplicates_collapse_and_use_latest ... ok
test native::freshness::placement::placement_tests::p16_indented_blocked ... ok
test native::freshness::placement::placement_tests::p18_nested_quote_stamps ... ok
test native::freshness::placement::placement_tests::p15_parenthesized_field ... ok
test native::freshness::placement::placement_tests::p18_quoted_task_stamps_with_prefix_kept ... ok
test native::completion::present::tests::root_empty_offers_sectioned_commands_in_help_order ... ok
test native::freshness::placement::placement_tests::set_refresh_replaces_existing_value ... ok
test native::freshness::seed::tests::oversized_notes_split_into_consecutive_chunks ... ok
test native::freshness::placement::placement_tests::refusals_leave_keeps_untouched ... ok
test native::freshness::seed::tests::invariance_abort_lists_a_line_hiding_a_field ... ok
test native::freshness::state::state_tests::cl11_checklist_beats_lane_and_tracker ... ok
test native::freshness::seed::tests::canonical_restamps_pass_invariance ... ok
test native::freshness::seed::tests::write_changes_refuses_a_file_changed_since_scan ... ok
test native::freshness::state::state_tests::cl12_repeat_without_when_done_still_pre ... ok
test native::freshness::state::state_tests::cl6_conflict_prefers_pre ... ok
test native::freshness::state::state_tests::cl1_recurring_pre_chore ... ok
test native::freshness::state::state_tests::bucket_partition_vectors ... ok
test native::freshness::state::state_tests::cl5_tag_matching ... ok
test native::freshness::state::state_tests::cl10_completed_occurrence_and_future_next_leave_queue ... ok
test native::freshness::state::state_tests::cl2_unknown_status_pre_is_queued_with_null_lane ... ok
test native::freshness::state::state_tests::cl7_one_off_post_keeps_new_state ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... ok
test native::capture_pomodoros_agenda::tests::september_shaped_vault_finishes_fast ... ok
test native::freshness::state::state_tests::counts_carry_decide ... ok
test native::freshness::state::state_tests::cl4_today_and_daily_note_still_pre ... ok
test native::freshness::state::state_tests::cl9_recurring_checklist_refuses_stamp ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::collect_done::tests::plan::self_healing_is_idempotent_after_links_are_repaired ... ok
test native::freshness::state::state_tests::decide_covers_tickler_but_never_new ... ok
test native::freshness::state::state_tests::l4_lane_off_switch_and_null_default ... ok
test native::freshness::state::state_tests::decide_at_limit_but_not_below ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::freshness::state::state_tests::decide_zero_off_and_lane_rows ... ok
test native::collect_done::tests::plan::task_moves_repair_dependency_ids_in_archive_and_all_dependents ... ok
test native::freshness::state::state_tests::decide_on_early_dates ... ok
test native::freshness::state::state_tests::l2_lane_overrides_refresh ... ok
test native::freshness::state::state_tests::q2_tier_order_beats_path_order ... ok
test native::freshness::state::state_tests::l1_lane_due_and_stamped_today ... ok
test native::freshness::state::state_tests::cl8_ten_tier_order ... ok
test native::freshness::state::state_tests::cl3_exclusions_drop_checklist_rows ... ok
test native::freshness::state::state_tests::rc11_stray_stamp_is_ignored ... ok
test native::freshness::state::state_tests::rc4_due_only_past ... ok
test native::freshness::state::state_tests::rc3_future_occurrence_stays_out ... ok
test native::freshness::state::state_tests::rc10_checklist_wins_over_recurring ... ok
test native::freshness::state::state_tests::rc5_due_only_future ... ok
test native::freshness::state::state_tests::lane_reference_uses_lane_interval_without_configured_cadence ... ok
test native::freshness::state::state_tests::r1_tickler_beats_older_rotten ... ok
test native::freshness::state::state_tests::missing_created_sorts_after_dated_peers ... ok
test native::freshness::state::state_tests::rc6_earliest_date_wins ... ok
test native::freshness::state::state_tests::l5_lane_order_never_stamped_first ... ok
test native::freshness::state::state_tests::ref_identity_is_tag_or_exact_block_id ... ok
test native::freshness::state::state_tests::rc12_order_and_counts ... ok
test native::freshness::state::state_tests::l3_lane_exclusions_have_no_tier ... ok
test native::freshness::state::state_tests::rc2_arrives_today ... ok
test native::freshness::state::state_tests::q1_bryan_example_orders_adjc ... ok
test native::freshness::state::state_tests::reference_interval_boundary ... ok
test native::freshness::state::state_tests::rc1_arrived_recurring_row ... ok
test native::freshness::state::state_tests::s02_fresh_with_due_on ... ok
test native::freshness::state::state_tests::rc7_undated_recurring_stays_out ... ok
test native::freshness::state::state_tests::resurfaced_reference_walks_references_without_decide ... ok
test native::freshness::state::state_tests::r2_tickler_orders_by_schedule_then_newest_created ... ok
test native::dataview::tests::flatten_budget_honors_earlier_filters_not_later_limits ... ok
test native::freshness::state::state_tests::s03_boundary_is_rotten_with_zero_overdue ... ok
test native::freshness::state::state_tests::b1_upkeep_counts_outside_the_lanes ... ok
test native::freshness::state::state_tests::s01_new_without_stamp ... ok
test native::freshness::state::state_tests::s08_invalid_overrides_fall_through_with_lints ... ok
test native::freshness::state::state_tests::rc8_recurring_lane_rows_keep_lane ... ok
test native::freshness::state::state_tests::s10_future_fresh_is_new_with_lint ... ok
test native::freshness::state::state_tests::s09_malformed_fresh_is_new_with_lint ... ok
test native::config::tests::roll_offset_stays_within_bounds_for_many_seeds ... ok
test native::freshness::state::state_tests::s04_overdue_counts_days ... ok
test native::freshness::state::state_tests::s12_equal_schedule_is_not_resurfaced ... ok
test native::freshness::state::state_tests::s05_task_interval_beats_note ... ok
test native::dataview::tests::flatten_budget_accepts_exact_limit_and_rejects_overflow ... ok
test native::freshness::state::state_tests::s14_queue_order_new_then_due ... ok
test native::freshness::state::state_tests::tag_only_ready_ref_walks_references ... ok
test native::dataview::tests::flatten_aliases_empty_null_and_scalar_values ... ok
test native::freshness::state::state_tests::s07_config_interval ... ok
test native::freshness::state::state_tests::s11_resurfaced_when_schedule_returns_after_stamp ... ok
test native::freshness::state::state_tests::s06_note_interval_beats_config ... ok
test native::freshness::state::state_tests::rc9_exclusions_drop_recurring_rows ... ok
test native::freshness::state::state_tests::tracker_lane_precedence_and_disabled_lanes ... ok
test native::freshness::placement::placement_tests::parse_invariance_across_all_vectors ... ok
test native::freshness::state::state_tests::tracking_projects_tier_and_counts ... ok
test native::freshness::state::state_tests::tracker_intervals_override_for_matching_type ... ok
test native::freshness::state::state_tests::s13_out_of_scope_is_null ... ok
test native::freshness::state::state_tests::seven_tier_order_with_references ... ok
test native::gkeep::adapter::tests::resolve_uses_override_without_path_lookup ... ok
test native::gkeep::config::tests::token_shape_classifier ... ok
test native::freshness::placement::placement_tests::keeps_fixture_vectors_match_rust ... ok
test native::gkeep::adapter::tests::resolve_without_uv_is_a_setup_error ... ok
test native::gkeep::doctor::tests::check_status_names_match_the_json_contract ... ok
test native::gkeep::doctor::tests::device_id_shortens_to_eight_plus_ellipsis ... ok
test native::gkeep::doctor::tests::home_prefix_collapses_to_tilde ... ok
test native::gkeep::doctor::tests::tasks_heading_matches_headings_only ... ok
test native::gkeep::config::tests::resolve_applies_defaults_and_derives_device_id ... ok
test native::gkeep::config::tests::resolve_email_override_wins ... ok
test native::gkeep::config::tests::device_id_validation ... ok
test native::gkeep::cli::tests::bob_dir_flag_expands_tilde ... ok
test native::freshness::state::state_tests::s15_counts_and_budget_meter ... ok
test native::gkeep::cli::tests::list_args_pin_defaults_and_values ... ok
test native::gkeep::cli::tests::doctor_and_login_args ... ok
test native::dataview::tests::flatten_lists_include_nested_children ... ok
test native::gkeep::config::tests::adapter_override_reads_env ... ok
test native::gkeep::cli::tests::pull_args_pin_every_option ... ok
test native::gkeep::config::tests::device_id_is_derived_and_pinned ... ok
test native::dataview::tests::grouped_sorting_repeated_grouping_and_lambda_shadowing ... ok
test native::gkeep::ledger::tests::journal_read_skips_non_utf8_lines ... ok
test native::gkeep::login::tests::cookie_line_picks_the_first_non_empty_line ... ok
test native::gkeep::ledger::tests::journal_read_tolerates_missing_files_and_corrupt_lines ... ok
test native::gkeep::ledger::tests::read_target_tasks_handles_missing_created_and_markers ... ok
test native::gkeep::ledger::tests::duplicates_name_every_location ... ok
test native::gkeep::login::tests::inbox_count_handles_singular_and_plural ... ok
test native::gkeep::model::tests::fingerprint_ignores_json_key_order_and_attachments ... ok
test native::gkeep::model::tests::requests_serialize_with_protocol_and_op ... ok
test native::dataview::tasks::index::tests::fixture_index_builds_hierarchy_and_ignores_fences_and_dot_directories ... ok
test native::gkeep::model::tests::responses_parse ... ok
test native::gkeep::model::tests::unknown_attachment_kind_deserializes_to_other ... ok
test native::gkeep::login::tests::recovery_path_lives_under_the_state_dir ... ok
test native::gkeep::model::tests::archive_success_counts_archived_and_already_archived ... ok
test native::gkeep::model::tests::canonical_json_and_fingerprint_are_pinned ... ok
test native::gkeep::ledger::tests::marker_parsing_finds_all_hits_and_ignores_broken_ones ... ok
test native::gkeep::ledger::tests::marker_round_trips_ids_with_dots_and_exotic_bytes ... ok
test native::gkeep::ledger::tests::scan_includes_done_and_skips_excluded_dirs ... ok
test native::gkeep::model::tests::note_ref_is_pinned ... ok
test native::gkeep::plan::tests::archived_notes_get_the_archived_state ... ok
test native::gkeep::plan::tests::empty_id_is_unknown ... ok
test native::gkeep::plan::tests::fresh_note_is_new ... ok
test native::gkeep::plan::tests::id_filter_narrows_to_selected_notes ... ok
test native::gkeep::plan::tests::journal_written_record_is_a_backstop ... ok
test native::gkeep::plan::tests::ledger_hit_with_same_fingerprint_is_pending ... ok
test native::gkeep::plan::tests::create_ref_counts_as_actionable_for_limit ... ok
test native::gkeep::plan::tests::ledger_wins_over_journal ... ok
test native::gkeep::plan::tests::zero_width_only_text_is_empty ... ok
test native::gkeep::ledger::tests::read_target_tasks_covers_top_level_tasks_only ... ok
test native::gkeep::plan::tests::url_only_trailing_route_is_tracked_without_becoming_the_target ... ok
test native::gkeep::plan::tests::url_only_page_title_matching_link_title_becomes_create_ref ... ok
test native::gkeep::pull::tests::git_ancestor_checks_dot_git_files_and_dirs ... ok
test native::dataview::tasks::tests::non_function_queries_skip_the_sandbox_on_a_real_vault ... ok
test native::dataview::tasks::task::tests::all_priorities_have_tasks_v8_names_numbers_and_scores ... ok
test native::gkeep::plan::tests::url_only_body_note_becomes_create_ref ... ok
test native::gkeep::adapter::tests::normal_exit_with_pipe_holding_straggler_returns_quickly ... ok
test native::dataview::tasks::index::tests::paragraphs_break_list_hierarchy ... ok
test native::dataview::tasks::index::tests::dependency_graph_matches_direct_tasks_v8_semantics ... ok
test native::gkeep::plan::tests::empty_note_is_skipped ... ok
test native::gkeep::plan::tests::ledger_hit_with_other_fingerprint_is_revised ... ok
test native::gkeep::plan::tests::limit_counts_only_actionable_notes ... ok
test native::gkeep::plan::tests::pinned_beats_pending ... ok
test native::gkeep::plan::tests::resolve_ids_prefers_exact_ids ... ok
test native::capture::tests::commit::cumulative_stages_into_one_note_commit ... ok
test native::gkeep::plan::tests::ref_created_journal_drives_archive_only ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::gkeep::plan::tests::non_url_only_notes_stay_tasks ... ok
test native::gkeep::plan::tests::resolve_ids_rejects_unknown_and_ambiguous ... ok
test native::gkeep::render::tests::capture_grammar_lookalikes_stay_literal ... ok
test native::gkeep::pull::tests::prompt_accepts_default_reprompts_unknown_and_stops_on_eof ... ok
test native::gkeep::plan::tests::notes_order_oldest_first_with_id_tiebreak ... ok
test native::gkeep::plan::tests::pinned_and_shared_notes_stay_unless_included_or_selected ... ok
test native::gkeep::render::tests::revision_flags_the_source_line ... ok
test native::gkeep::render::tests::empty_list_falls_back_to_untitled_title ... ok
test native::gkeep::render::tests::display_title_is_unescaped ... ok
test native::gkeep::render::tests::escape_task_text_leaves_intended_markup_alone ... ok
test native::gkeep::render::tests::unknown_attachment_kind_renders_as_files ... ok
test native::gkeep::render::tests::fallback_child_sits_just_before_source ... ok
test native::gkeep::tests::error_exit_codes ... ok
test native::gkeep::render::tests::source_url_spoof_cannot_plant_a_marker ... ok
test native::gkeep::render::tests::labels_join_the_source_line ... ok
test native::gkeep::render::tests::markdown_has_no_trailing_newline ... ok
test native::gkeep::render::tests::bare_list_markers_escape ... ok
test native::gkeep::render::tests::crlf_and_tabs_normalize ... ok
test native::gkeep::render::tests::untitled_list_takes_first_item_as_title_but_keeps_it ... ok
test native::gkeep::render::tests::titled_note_renders_task_line_and_children ... ok
test native::gkeep::render::tests::space_indent_uses_two_spaces ... ok
test native::gkeep::render::tests::task_and_block_id_and_comment_and_field_hazards_escape ... ok
test native::gkeep::render::tests::escape_child_text_covers_both_tables ... ok
test native::gkeep::render::tests::unicode_text_passes_through ... ok
test native::gkeep::render::tests::spoofed_marker_in_keep_text_cannot_survive ... ok
test native::gkeep::render::tests::markdown_looking_text_is_neutralized_in_children ... ok
test native::gkeep::render::tests::untitled_multiline_note_takes_first_line_as_title ... ok
test native::gkeep::render::tests::image_with_ocr_renders_attachment_line_and_grandchildren ... ok
test native::gkeep::render::tests::mixed_attachments_pluralize ... ok
test native::gkeep::render::tests::list_with_checked_nested_and_empty_items ... ok
test native::gkeep::render::tests::leading_markers_cover_headings_breaks_and_fences ... ok
test native::gkeep::ui::tests::age_buckets ... ok
test native::gkeep::ui::tests::spinner_frames_are_braille ... ok
test native::highlights_ref::arxiv::tests::arxiv_parsing_matches_sase_listen_negatives ... ok
test native::highlights_ref::arxiv::tests::arxiv_versions_split_and_dedupe_without_version ... ok
test native::highlights_ref::arxiv::tests::arxiv_parsing_matches_sase_listen_positives ... ok
test native::gkeep::ui::tests::spinner_start_and_drop_never_panics ... ok
test native::highlights_ref::arxiv::tests::arxiv_author_display_covers_one_two_and_three_authors ... ok
test native::highlights_ref::clip_url::tests::name_validation_strips_pdf_and_rejects_junk ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_normalizes_spellings ... ok
test native::highlights_ref::clip_url::tests::short_title_stem_uses_the_colon_prefix_or_six_words ... ok
test native::highlights_ref::clip_url::tests::arxiv_spellings_share_one_dedupe_key ... ok
test native::highlights_ref::clip_url::tests::validation_accepts_public_urls_and_strips_tracking ... ok
test native::highlights_ref::clip_url::tests::validation_rejects_non_public_urls ... ok
test native::highlights_ref::cli::tests::help_groups_cover_every_subcommand_exactly_once ... ok
test native::highlights_ref::cli::tests::help_groups_are_alphabetical_with_matching_abouts ... ok
test native::highlights_ref::clip_url::tests::non_arxiv_dedupe_keys_are_unchanged ... ok
test native::highlights_ref::clip_url::tests::validation_accepts_mapped_public_literals ... ok
test native::highlights_ref::clip_url::tests::stem_derivation_skips_noise_segments ... ok
test native::highlights_ref::arxiv::tests::arxiv_metadata_rejects_error_entries ... ok
test native::highlights_ref::create::tests::audio_link_template_precedence_is_env_then_config_then_default ... ok
test native::highlights_ref::create::tests::audio_path_components_are_percent_encoded ... ok
test native::highlights_ref::listen::tests::blank_env_and_missing_config_mean_unset ... ok
test native::highlights_ref::create::tests::title_prefers_frontmatter_then_h1_then_stem ... ok
test native::highlights_ref::listen::tests::rejects_quoted_placeholders ... ok
test native::highlights_ref::listen::tests::rejects_unknown_placeholders ... ok
test native::highlights_ref::listen::tests::rejects_templates_missing_audio_or_source ... ok
test native::highlights_ref::listen::tests::env_overrides_config ... ok
test native::highlights_ref::listen::tests::run_listen_accepts_mpeg_frame_sync_audio ... ok
test native::highlights_ref::ingest::tests::error_kinds_and_retryable_flags ... ok
test native::highlights_ref::listen::tests::accepts_complete_and_shell_syntax_templates ... ok
test native::gkeep::adapter::tests::spawn_sets_parent_pid_env ... ok
test native::dataview::tasks::index::tests::frontmatter_is_only_a_strictly_closed_column_zero_block ... ok
test native::highlights_ref::ingest::tests::fetch_hint_splits_out_of_message ... ok
test native::highlights_ref::listen::tests::require_reports_the_config_path_and_snippet ... ok
test native::highlights_ref::ingest::tests::fallback_note_quoting_truncation_and_escaping ... ok
test native::highlights_ref::ingest::tests::already_in_library_needs_no_network ... ok
test native::highlights_ref::listen::tests::run_listen_validates_before_running ... ok
test native::highlights_ref::render_tex::tests::header_packages_are_all_declared ... ok
test native::highlights_ref::render_tex::tests::missing_packages_returns_rest_in_order ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_listed_package ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_unlisted_file ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_unrelated_error ... ok
test native::highlights_ref::render_tex::tests::render_failure_hint_for_missing_xelatex ... ok
test native::highlights_ref::render_tex::tests::install_command_deduplicates_tlmgr_names ... ok
test native::highlights_ref::fetch::tests::fetch_reports_a_missing_curl_with_its_hint ... ok
test native::gkeep::adapter::tests::exiting_without_reading_reports_stdout_not_stdin ... ok
test native::gkeep::adapter::tests::internal_ok_false_carries_stderr_tail ... ok
test native::highlights_ref::pdf_meta::tests::info_metadata_accepts_plausible_values ... ok
test native::highlights_ref::return_links::tests::links_line_covers_every_variant ... ok
test native::dataview::tasks::task::tests::emoji_parser_extracts_all_fields_and_variant_selectors ... ok
test native::highlights_ref::arxiv::tests::arxiv_metadata_parses_titles_authors_and_dates ... ok
test native::highlights_ref::return_links::tests::report_defaults_missing_lists_and_enabled ... ok
test native::highlights_ref::return_links::tests::report_parses_full_contract ... ok
test native::highlights_ref::return_links::tests::report_parses_opt_out ... ok
test native::highlights_ref::return_links::tests::read_report_rejects_wrong_version_and_bad_json ... ok
test native::highlights_ref::return_links::tests::strip_flag_reads_return_links_marker_value ... ok
test native::highlights_ref::return_links::tests::tag_glyphs_match_filter_mod_table ... ok
test native::highlights_ref::return_links::tests::warnings_cover_every_variant ... ok
test native::highlights_ref::sources::tests::non_arxiv_keys_pass_through_unchanged ... ok
test native::highlights_ref::sources::tests::pdf_backed_note_still_refuses_beside_a_legacy_only_note ... ok
test native::highlights_ref::listen::tests::run_listen_writes_id3_audio_on_success ... ok
test native::gkeep::ledger::tests::journal_append_writes_leading_newline_after_torn_record ... ok
test native::highlights_ref::stamp::tests::default_target_derives_ref_type_output_and_valid_marker ... ok
test native::highlights_ref::pdf_meta::tests::info_titles_reject_junk ... ok
test native::dataview::tests::flatten_alias_and_collection_builtins_do_not_mutate_siblings ... ok
test native::highlights_ref::fetch::tests::fetch_refuses_private_resolved_addresses_and_unlisted_hosts ... ok
test native::highlights_ref::listen::tests::run_listen_reports_interrupt_exits ... ok
test native::highlights_ref::create::tests::plan_embeds_markdown_stem_id_when_opted_in ... ok
test native::highlights_ref::stamp::tests::default_target_chains_to_3_when_2_is_taken ... ok
test native::dataview::tests::flatten_retains_file_metadata_and_nested_task_children ... ok
test native::highlights_ref::fetch::tests::curl_passes_q_as_first_argument ... ok
test native::highlights_ref::listen::tests::run_listen_reports_failed_exits ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::highlights_ref::fetch::tests::curl_pins_the_checked_address_with_resolve ... ok
test native::dataview::tests::group_by_preserves_first_seen_order_and_member_access ... ok
test native::gkeep::config::tests::read_token_rejects_empty_and_failing_commands ... ok
test native::highlights_ref::stamp::tests::default_target_rejects_bad_stem_and_ref_type ... ok
test native::highlights_ref::stamp::tests::default_target_free_base_has_no_rename ... ok
test native::gkeep::config::tests::read_token_warns_but_keeps_unknown_shapes ... ok
test native::highlights_ref::stamp::tests::exact_external_target_does_not_invent_library_destination ... ok
test native::highlights_ref::stamp::tests::default_target_url_identity_matches_intake_or_ref_note ... ok
test native::highlights_ref::stamp::tests::exact_intake_refuses_mirrored_library_sidecar ... ok
test native::highlights_ref::stamp::tests::exact_output_keeps_nested_path_and_filename ... ok
test native::highlights_ref::stamp::tests::exact_output_resolves_relative_and_tilde_paths ... ok
test native::highlights_ref::stamp::tests::exact_library_target_requires_force_and_skips_mirrored_check ... ok
test native::highlights_ref::stamp::tests::exact_output_classifies_direct_library_target ... ok
test native::highlights_ref::stamp::tests::marker_rejects_wikilink_parent_and_unknown_status ... ok
test native::highlights_ref::arxiv::tests::arxiv_fetch_metadata_degrades_with_a_warning ... ok
test native::highlights_ref::stamp::tests::marker_extras_insert_in_canonical_order_and_skip_empty ... ok
test native::highlights_ref::stamp::tests::exact_output_accepts_uppercase_pdf_extension ... ok
test native::highlights_ref::stamp::tests::normalize_lexically_drops_dot_and_parent_components ... ok
test native::highlights_ref::stamp::tests::marker_return_links_key_orders_after_captured_and_round_trips ... ok
test native::highlights_ref::stamp::tests::exact_output_does_not_treat_sibling_prefix_as_managed ... ok
test native::highlights_ref::stamp::tests::exact_intake_still_refuses_mirrored_library_pdf_with_force ... ok
test native::highlights_ref::tests::audio::audio_library_root_prefers_env_then_config_then_xdg_then_home ... ok
test native::highlights_ref::tests::audio::audio_embed_inserts_after_ref_child_lines ... ok
test native::highlights_ref::tests::audio::companion_extensions_prefer_mp3_then_later_types ... ok
test native::highlights_ref::stamp::tests::exact_output_refuses_same_stem_markdown_sidecar_even_with_force ... ok
test native::highlights_ref::tests::audio::default_note_body_embeds_audio_between_task_and_highlights ... ok
test native::highlights_ref::stamp::tests::exact_output_rejects_non_pdf_paths ... ok
test native::highlights_ref::listen::tests::run_listen_rejects_missing_and_non_mp3_audio ... ok
test native::highlights_ref::tests::audio::command_managed_audio_is_quoted_wikilink_and_omitted_without_companion ... ok
test native::gkeep::adapter::tests::token_travels_on_stdin_never_argv ... ok
test native::highlights_ref::tests::audio::episode_id_validation_rejects_dot_dot_slash_and_underscore ... ok
test native::highlights_ref::tests::audio::episode_audio_source_resolves_bare_filename_only ... ok
test native::highlights_ref::tests::audio::existing_note_skips_embed_when_audio_field_already_present ... ok
test native::highlights_ref::tests::audio::existing_note_inserts_embed_once_when_audio_field_is_absent ... ok
test native::highlights_ref::tests::audio::execute_xlib_intake_counting_omits_failed_main_rename ... ok
test native::highlights_ref::tests::audio::narration_script_candidate_strips_final_suffix ... ok
test native::highlights_ref::tests::audio::frontmatter_episode_id_parses_nested_audio_key ... ok
test native::highlights_ref::tests::audio::explicit_audio_validation_rejects_missing_and_bad_extension ... ok
test native::highlights_ref::tests::audio::execute_xlib_intake_counting_reports_pdf_when_companion_fails ... ok
test native::highlights_ref::tests::audio::episode_audio_source_rejects_traversal_and_missing_files ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_leaves_audio_without_any_pdf ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_late_pairs_orphan_audio_to_library_pdf ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker::created_stays_note_local_despite_stale_marker_fields_opt_in ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_uses_marker_fields_without_fallback_parent ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_moves_same_stem_audio_with_pdf ... ok
test native::highlights_ref::tests::marker::marker_parser_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker::marker_parser_accepts_yaml_subset_and_normalizes_keys ... ok
test native::highlights_ref::tests::marker::frontmatter_render_preserves_unmanaged_keys ... ok
test native::highlights_ref::tests::audio::plan_xlib_intake_reports_audio_destination_conflicts ... ok
test native::highlights_ref::stamp::tests::default_target_suffixes_each_occupant_kind ... ok
test native::highlights_ref::tests::audio::script_hash_lookup_prefers_newest_created_at ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_created_key ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_linked_parent_targets ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_missing_required_keys_type_and_duplicate_status ... ok
test native::highlights_ref::tests::marker::marker_renderer_rejects_unrepresentable_parent_links ... ok
test native::highlights_ref::tests::marker::marker_renderer_uses_stable_key_order ... ok
test native::highlights_ref::tests::marker::parent_canonicalization_rejects_non_scalar_values ... ok
test native::highlights_ref::tests::marker::new_note_render_emits_exactly_one_created_line ... ok
test native::highlights_ref::tests::marker::status_validation_rejects_unsupported_and_non_scalar_values ... ok
test native::highlights_ref::tests::projection::deprecated_statuses_normalize_for_synced_inputs ... ok
test native::highlights_ref::tests::projection::pdf_path_metadata_derives_nested_reference_paths ... ok
test native::highlights_ref::tests::projection::pipeline_fields_exclude_marker_user_projection ... ok
test native::highlights_ref::tests::projection::projection_snapshot_json_round_trips_compact_user_projection ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_compatible_changes ... ok
test native::highlights_ref::tests::projection::relative_config_paths_resolve_under_bob_dir ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_deletes_and_conflicts ... ok
test native::highlights_ref::tests::projection::validate_library_layout_rejects_equal_and_nested_paths ... ok
test native::highlights_ref::tests::reading_execute::line_edit_refuses_archived_tasks ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_maps_nested_paths_and_companions ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_reports_every_destination_conflict ... ok
test native::highlights_ref::tests::reading_plan::audio_anchor_never_duplicates_or_invents ... ok
test native::highlights_ref::tests::reading_execute::v2_guard_allows_embed_repoint_and_residence_parent ... ok
test native::highlights_ref::tests::reading_execute::v2_guard_refuses_unrelated_edits ... ok
test native::highlights_ref::tests::reading_plan::audio_anchors_after_managed_embed ... ok
test native::highlights_ref::tests::reading_execute::changed_line_fails_before_any_pdf_write ... ok
test native::highlights_ref::tests::reading_plan::birth_adopts_newest_closed ... ok
test native::highlights_ref::tests::reading_plan::birth_adopts_unique_orphan ... ok
test native::highlights_ref::tests::reading_plan::birth_body_anchors_audio_after_embed ... ok
test native::highlights_ref::tests::reading_plan::birth_body_shows_embed_not_tracker ... ok
test native::highlights_ref::tests::reading_plan::birth_parent_falls_back_on_every_error_kind ... ok
test native::highlights_ref::tests::reading_plan::birth_parent_keeps_resolved_route ... ok
test native::highlights_ref::tests::reading_plan::birth_refuses_multiple_open ... ok
test native::highlights_ref::tests::reading_plan::birth_refuses_open_archive_task ... ok
test native::highlights_ref::tests::reading_plan::birth_with_no_candidates_inserts ... ok
test native::highlights_ref::tests::reading_plan::classify_archived_task_makes_existing_note_v2 ... ok
test native::highlights_ref::tests::reading_plan::classify_in_note_tracker_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::classify_managed_embed_makes_existing_note_v2 ... ok
test native::highlights_ref::listen::tests::quoting_round_trips_through_shell ... ok
test native::highlights_ref::tests::reading_plan::classify_missing_note_is_v2_birth ... ok
test native::highlights_ref::tests::reading_plan::classify_outside_task_makes_existing_note_v2 ... ok
test native::highlights_ref::tests::reading_plan::classify_task_inside_own_note_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::classify_trackerless_legacy_stays_v1 ... ok
test native::highlights_ref::tests::reading_plan::embed_target_forms_follow_the_design ... ok
test native::highlights_ref::tests::reading_plan::fallback_child_text_is_exact ... ok
test native::highlights_ref::tests::reading_plan::first_v2_transition_has_no_false_conflict ... ok
test native::highlights_ref::tests::reading_plan::heal_collapses_duplicate_embeds ... ok
test native::highlights_ref::tests::reading_plan::heal_correct_body_is_byte_identical ... ok
test native::highlights_ref::tests::reading_plan::heal_inserts_missing_embed_below_h1 ... ok
test native::highlights_ref::tests::reading_plan::heal_preserves_authored_material ... ok
test native::highlights_ref::tests::reading_plan::heal_preserves_crlf ... ok
test native::highlights_ref::tests::reading_plan::heal_repoints_stale_embed ... ok
test native::highlights_ref::tests::reading_plan::heal_without_h1_leaves_body_alone ... ok
test native::highlights_ref::tests::reading_plan::marker_hint_round_trips_parent ... ok
test native::highlights_ref::tests::reading_plan::missing_task_open_surfaces_guidance ... ok
test native::highlights_ref::tests::reading_plan::missing_task_terminal_stays_silent ... ok
test native::highlights_ref::tests::reading_plan::pdf_task_question_overlay_stays_put ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_adopts_orphan ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_inserts_into_resolved_parent ... ok
test native::highlights_ref::tests::reading_plan::plan_birth_warns_on_unresolvable_hint ... ok
test native::highlights_ref::tests::reading_plan::plan_closed_terminal_stays_quiet ... ok
test native::highlights_ref::tests::reading_plan::plan_existing_marker_change_edits_line ... ok
test native::highlights_ref::tests::reading_plan::plan_missing_open_never_invents_a_task ... ok
test native::highlights_ref::tests::reading_plan::plan_refused_multiple_open_blocks_writes ... ok
test native::highlights_ref::tests::reading_plan::plan_reopen_archived_inserts_into_source_parent ... ok
test native::highlights_ref::tests::reading_plan::plan_task_gesture_conflict_errors ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_branch_hands_off ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_closed_tracker_stays_silent ... ok
test native::highlights_ref::tests::reading_plan::plan_reopen_without_source_parent_uses_inbox ... ok
test native::highlights_ref::tests::reading_plan::plan_v1_open_tracker_reports_migrate_diagnostic ... ok
test native::highlights_ref::tests::reading_plan::region_own_notes_keeps_legacy_body_verbatim ... ok
test native::highlights_ref::tests::reading_plan::region_own_notes_excludes_managed_embed ... ok
test native::highlights_ref::tests::reading_plan::residence_parent_renders_from_route ... ok
test native::highlights_ref::tests::reading_plan::signal_archived_reopen_never_edits_done ... ok
test native::highlights_ref::tests::reading_plan::signal_changed_sides_agreeing_with_task_drive ... ok
test native::highlights_ref::tests::reading_plan::signal_conflicting_inputs_refuse ... ok
test native::highlights_ref::tests::reading_plan::signal_frontmatter_only_change_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_live_terminal_reopen_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_marker_close_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_marker_only_change_edits_the_line ... ok
test native::highlights_ref::tests::reading_plan::signal_question_on_terminal_drives_reopen_ready ... ok
test native::highlights_ref::tests::reading_plan::signal_question_overlay_agrees_with_open ... ok
test native::highlights_ref::tests::reading_plan::signal_task_gesture_drives_status ... ok
test native::highlights_ref::tests::reading_plan::signal_unchanged_checkbox_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_uncheckboxable_current_refuses ... ok
test native::highlights_ref::tests::reading_plan::signal_unknown_mark_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_without_base_agreement_is_quiet ... ok
test native::highlights_ref::tests::reading_plan::signal_without_base_evidence_refuses_disagreement ... ok
test native::highlights_ref::tests::reading_plan::status_mark_matches_projection_marks ... ok
test native::highlights_ref::tests::reading_plan::v1_birth_body_stays_frozen ... ok
test native::highlights_ref::tests::reading_plan::without_parent_drops_only_parent ... ok
test native::highlights_ref::tests::region::note_anatomy_broken_markers_yield_no_region ... ok
test native::highlights_ref::tests::region::note_anatomy_legacy_body_passes_through_verbatim ... ok
test native::highlights_ref::tests::region::note_anatomy_full_body ... ok
test native::highlights_ref::tests::region::region_parses_leaked_mirror_like_ea_graph ... ok
test native::highlights_ref::tests::region::region_round_trip_highlight_comment_mirror ... ok
test native::highlights_ref::tests::region::region_round_trip_highlight_with_multiline_comment ... ok
test native::highlights_ref::tests::region::region_unknown_callout_is_unparsed ... ok
test native::highlights_ref::tests::seams::deprecated_status_seam_matches_marker_normalization ... ok
test native::highlights_ref::tests::seams::ref_task_mark_seam_matches_the_pdf_task_mapping ... ok
test native::highlights_ref::tests::seams::ref_task_mark_target_seam_matches_status_aware_mapping ... ok
test native::highlights_ref::tests::region::region_round_trip_standalone_note ... ok
test native::highlights_ref::tests::region::region_round_trip_pages_preamble_and_tombstones ... ok
test native::highlights_ref::tests::region::region_round_trip_image ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_preserves_list_structure ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_reflows_and_dehyphenates ... ok
test native::highlights_ref::tests::sidecar::annotation_block_id_is_stable_across_space_wrapping ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_keeps_wrapped_quotes_and_marker_mirror ... ok
test native::highlights_ref::tests::sidecar::marker_content_decoder_preserves_pdfdoc_line_separators ... ok
test native::highlights_ref::tests::sidecar::leaked_mirror_and_preamble_blocks_drop_silently_while_genuine_tombstones ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_strips_comment_bullet_markers ... ok
test native::highlights_ref::tests::sidecar::pdf_text_artifact_cleanup_normalizes_extraction_noise ... ok
test native::highlights_ref::tests::sidecar::missing_image_asset_error_points_at_textbundle_export ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_beautifies_callout_text ... ok
test native::highlights_ref::tests::sidecar::image_block_id_is_stable_across_asset_renames ... ok
test native::highlights_ref::tests::sidecar::rendered_annotation_blocks_do_not_include_source_task_anchors ... ok
test native::highlights_ref::tests::sidecar::sidecar_page_heading_extracts_linked_page_label ... ok
test native::highlights_ref::tests::sidecar::return_link_strip_keeps_block_ids_stable ... ok
test native::highlights_ref::tests::sidecar::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::tests::sidecar::sidecar_parser_extracts_image_annotations_and_leaves_non_images_as_notes ... ok
test native::highlights_ref::tests::sidecar::return_link_glyphs_strip_only_from_highlights_when_flagged ... ok
test native::highlights_ref::tests::sidecar::setext_preamble_yields_no_annotations_and_keeps_genuine_ids_stable ... ok
test native::highlights_ref::tests::sidecar::sidecar_without_page_headings_has_no_preamble ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_renders_image_assets_and_tasks ... ok
test native::highlights_ref::tests::sidecar::simple_sidecar_unlabeled_text_after_quote_remains_comment ... ok
test native::highlights_ref::tests::status::blocked_task_agrees_with_every_open_projection ... ok
test native::highlights_ref::tests::status::blocked_task_conflicts_when_marker_moved_status_away ... ok
test native::highlights_ref::tests::status::blocked_task_reopens_terminal_projections_to_ready ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_conflicts_with_competing_edit ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_contributes_abandoned ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_promotes_ready_and_back ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_maps_all_lifecycle_states ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_ready_reopens_terminal_to_ready ... ok
test native::highlights_ref::tests::tasks::annotation_task_batches_append_in_insertion_order ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidate_records_route_and_processed_id ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidates_extract_from_comments_and_notes ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_preserves_crlf_line_endings ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_is_idempotent_and_preserves_existing_states ... ok
test native::highlights_ref::tests::tasks::annotation_task_route_suffix_is_strict_and_stripped_from_identity ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_append_to_existing_tasks_section ... ok
test native::highlights_ref::tests::tasks::annotation_task_section_stays_after_ref_child_lines ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_create_section_after_unterminated_ref_line ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_fill_empty_tasks_section_with_blank_lines ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_ignore_fenced_and_managed_tasks_headings ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_reuse_h1_or_closed_atx_tasks_heading ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_recognizes_generated_pdf_task ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_rejects_malformed_and_duplicate_tasks ... ok
test native::highlights_ref::tests::status::blocked_task_write_back_keeps_mark_for_open_and_closes_for_read ... ok
test native::highlights_ref::text::tests::strip_return_link_glyphs_covers_every_shape ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_ht_backlink_blocks_edited_recreation ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_identity_blocks_recreation ... ok
test native::markdown::tests::blockquote_and_indented_code_detection ... ok
test native::markdown::tests::setext_underline_accepts_levels_and_indent ... ok
test native::highlights_ref::tests::tasks::processed_task_index_scans_states_indents_and_done_notes ... ok
test native::markdown::tests::split_line_ending_preserves_crlf_lf_and_none ... ok
test native::markdown::tests::standalone_html_comment_reads_inner_text ... ok
test native::note_ready::cli::tests::closest_names_suggest_up_to_three ... ok
test native::note_ready::render::tests::crowded_bars_mark_the_cap_and_overflow ... ok
test native::note_ready::render::tests::crowded_worklist_always_advertises_task_card_hints ... ok
test native::note_ready::render::tests::overview_all_clear_is_green_without_crowded_group ... ok
test native::note_ready::render::tests::ready_gesture_hint_is_always_the_task_card_keys ... ok
test native::note_ready::render::tests::overview_advertises_task_card_keys_on_any_day ... ok
test native::note_ready::render::tests::overview_names_crowded_notes_with_bars ... ok
test native::note_ready::render::tests::worklist_lists_rows_in_file_order ... ok
test native::note_ready::tests::lints_emit_once_per_note ... ok
test native::note_ready::tests::ordering_is_crowded_full_room_empty_exempt ... ok
test native::note_ready::tests::r10_terminal_projects_are_not_capped ... ok
test native::note_ready::tests::r11_all_type_forms_are_eligible ... ok
test native::note_ready::tests::r12_stamping_moves_new_to_ready_without_changing_count ... ok
test native::note_ready::tests::r13_today_tasks_count_as_ready ... ok
test native::note_ready::tests::r14_config_cap_with_note_override ... ok
test native::note_ready::tests::r1_six_tasks_is_crowded_over_by_one ... ok
test native::note_ready::tests::r2_five_tasks_is_full_without_lint ... ok
test native::note_ready::tests::r3_lane_exclusions_never_count ... ok
test native::note_ready::tests::r4_make_up_splits_new_rotten_ready ... ok
test native::note_ready::tests::r5_recurring_excluded_and_counted ... ok
test native::gkeep::adapter::tests::ping_snapshot_archive_round_trip ... ok
test native::note_ready::tests::r6_prj_rows_never_count ... ok
test native::note_ready::tests::r8_ready_cap_forms ... ok
test native::note_ready::tests::r9_nested_child_tasks_each_count ... ok
test native::highlights_ref::tests::status::close_date_stamp_inserts_once_before_ref_and_preserves_existing_dates ... ok
test native::note_tasks::tests::clean_description_drops_ref_after_task_filter ... ok
test native::note_tasks::tests::block_id_lookup_distinguishes_found_non_task_duplicate_and_missing ... ok
test native::note_tasks::tests::computes_child_spans_for_mixed_indentation_blanks_and_eof ... ok
test native::note_tasks::tests::ignores_frontmatter_and_fenced_code_tasks ... ok
test native::note_tasks::tests::gates_on_filter_and_cleans_descriptions_with_sections ... ok
test native::note_tasks::tests::refs_resolve_exact_shifted_stale_and_ambiguous_tasks ... ok
test native::note_tasks::tests::ref_task_kind_marks_filter_then_ref_rows ... ok
test native::note_tasks::tests::suggests_case_matches_and_unique_nearby_block_ids_only ... ok
test native::note_tasks::tests::task_refs_parse_strictly_and_round_trip_scan_metadata ... ok
test native::note_tasks::tests::reads_real_statuses_and_missing_settings_fall_back_to_defaults ... ok
test native::parent_notes::tests::ambiguous_alias_names_both_notes ... ok
test native::parent_notes::tests::dash_and_underscore_are_different ... ok
test native::highlights_ref::tests::reading_execute::revalidate_refreshes_moved_lines_and_refuses_changed_ones ... ok
test native::gkeep::config::tests::resolve_rejects_bad_config ... ok
test native::ob::tests::detect_git_worktree_reports_non_worktree ... ok
test native::parent_notes::tests::resolves_alias_and_reports_how_it_matched ... ok
test native::parent_notes::tests::each_inbox_resolves ... ok
test native::parent_notes::tests::stem_wins_over_alias ... ok
test native::plan_budget::tests::alias_and_md_suffix_links_count ... ok
test native::plan_budget::tests::cancelled_and_completed_entries_never_count ... ok
test native::parent_notes::tests::terminal_project_and_non_parent_hub_report_themselves ... ok
test native::parent_notes::tests::resolves_stem_md_and_wikilink_forms ... ok
test native::parent_notes::tests::unknown_names_near_miss_and_alias_hint ... ok
test native::plan_budget::tests::components_compare_case_insensitively ... ok
test native::plan_budget::tests::fenced_links_and_fenced_entries_never_count ... ok
test native::plan_budget::tests::eleven_links_are_over_the_cap ... ok
test native::plan_budget::tests::empty_target_means_the_daily_note ... ok
test native::plan_budget::tests::four_themes_are_over_but_three_are_fine ... ok
test native::plan_budget::tests::lane_over_never_changes_status ... ok
test native::plan_budget::tests::link_forms_count_once_and_exclusions_hold ... ok
test native::plan_budget::tests::merged_name_counts_decks_once_with_duplicate_lint ... ok
test native::plan_budget::tests::markers_and_inner_hash_links_count ... ok
test native::plan_budget::tests::missing_section_reports_empty ... ok
test native::plan_budget::tests::open_inventory_label_counts_and_lints ... ok
test native::plan_budget::tests::running_and_highlight_flags_follow_ledger_order ... ok
test native::plan_budget::tests::subheading_splits_time_totals_and_lints ... ok
test native::plan_budget::tests::lane_queries_parse_through_the_native_engine ... ok
test native::plan_budget::tests::unnamed_placeholder_counts_only_with_links ... ok
test native::plan_budget::today::tests::closed_entries_contribute_no_links ... ok
test native::plan_budget::today::tests::aliased_links_pin_the_lineup_behavior ... ok
test native::highlights_ref::tests::status::highlights_ref_task_checkbox_rewrite_and_dirty_allowance_are_narrow ... ok
test native::plan_budget::today::tests::fenced_links_never_count ... ok
test native::plan_budget::today::tests::duplicate_links_dedupe_to_the_first_position ... ok
test native::plan_budget::today::tests::mixed_and_nested_bullets_are_not_dedicated_links ... ok
test native::plan_budget::today::tests::done_and_cancelled_tasks_drop_out_while_blocked_stays ... ok
test native::plan_budget::today::tests::gtd_empty_target_resolves_to_the_daily_note ... ok
test native::plan_budget::today::tests::missing_notes_lint_and_drop_out ... ok
test native::plan_budget::today::tests::markers_struck_and_embedded_follow_the_lineup_rule ... ok
test native::plugins::tests::json_shape_is_stable ... ok
test native::plugins::tests::backup_failure_aborts_overwrite ... ok
test native::note_ready::tests::scan_covers_r11_r8_terminal_and_recurring ... ok
test native::note_ready::tests::scan_excludes_r3_and_r7_paths ... ok
test native::gkeep::adapter::tests::every_request_carries_protocol_version ... ok
test native::plugins::tests::pull_repo_skips_non_git_directory ... ok
test native::highlights_ref::create::tests::listen_filter_renders_card_and_encoded_play_link ... ok
test native::plugins::tests::sync_reports_text_diff_for_changed_files ... ok
test native::plugins::tests::scan_reports_states_and_counts ... ok
test native::plugins::tests::sync_summarizes_binary_and_minified_diffs ... ok
test native::plugins::tests::sync_only_filters_to_a_single_plugin ... ok
test native::plugins::tests::truncate_adds_ellipsis_only_when_needed ... ok
test native::plugins::tests::sync_unknown_plugin_is_an_error ... ok
test native::highlights_ref::return_links::tests::filter_leaves_image_description_spans_untagged ... ok
test native::plugins::tests::sync_state_detects_synced_drift_and_missing ... ok
test native::plugins::tests::unreadable_repo_is_an_error ... ok
test native::pomodoro::tests::completed_ledger_parser_only_accepts_x_checkbox_entries ... ok
test native::pomodoro::tests::open_ledger_parser_requires_an_open_checkbox ... ok
test native::pomodoro::tests::unclosed_frontmatter_delimiter_is_content ... ok
test native::plugins::tests::vault_state_reads_enabled_disabled_and_not_installed ... ok
test native::projects::tests::edits::project_changes_clean_duplicate_subproject_marker_lines ... ok
test native::projects::tests::edits::project_changes_delete_subproject_line_for_stale_child ... ok
test native::projects::tests::edits::project_changes_insert_subproject_line_above_user_bullets ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_final_prj_line ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_prj_with_tab_indent ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_for_subproject_link_insertions ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_when_appending_status ... ok
test native::plugins::tests::sync_dry_run_reports_without_writing ... ok
test native::projects::tests::edits::project_changes_remove_prj_fields_with_adjacent_whitespace ... ok
test native::projects::tests::edits::project_changes_replace_status_append_missing_status_and_add_hide_tag ... ok
test native::projects::tests::edits::project_changes_rewrite_subproject_line_in_place ... ok
test native::plugins::tests::sync_preserves_runtime_data_json ... ok
test native::projects::tests::edits::frontmatter_keys_must_start_at_column_zero ... ok
test native::projects::tests::edits::schedule_only_issues_still_allow_subproject_aggregation ... ok
test native::projects::tests::edits::project_changes_mark_last_child_closed_and_keep_subproject_line ... ok
test native::plugins::tests::sync_creates_updates_and_leaves_unchanged ... ok
test native::gkeep::adapter::tests::large_request_with_fast_exit_succeeds ... ok
test native::plugins::tests::sync_json_shape_is_stable ... ok
test native::projects::tests::edits::task_schedule_edits_cover_contract_and_preserve_markdown ... ok
test native::projects::tests::parse::non_project_notes_are_ignored ... ok
test native::projects::tests::edits::project_parser_splits_surfacing_and_dash_visibility_counts ... ok
test native::projects::tests::edits::project_changes_remove_prj_hide_tag_with_crlf ... ok
test native::projects::tests::edits::scheduled_tasks_keep_subproject_ledger_planning ... ok
test native::projects::tests::edits::terminal_projects_do_not_reconcile_task_schedules ... ok
test native::projects::tests::parse::project_parser_marks_unprioritized_prj_as_on_dash ... ok
test native::projects::tests::parse::project_parser_accepts_project_type_variants_and_counts_tasks ... ok
test native::highlights_ref::tests::reading_execute::reopen_into_inbox_fallback_carries_warning_child ... ok
test native::projects::tests::parse::project_parser_reads_parent_wikilink_target ... ok
test native::highlights_ref::ingest::tests::for_vault_agrees_with_from_matches ... ok
warning: You appear to have cloned an empty repository.
test native::highlights_ref::sources::tests::pdf_backed_legacy_url_notes_are_recorded_and_still_refuse ... ok
test native::projects::tests::parse::project_parser_accepts_prj_tag_and_strips_it_from_description ... ok
test native::highlights_ref::create::tests::markdown_marker_gains_return_links_only_after_paired_render ... ok
test native::gkeep::ledger::tests::journal_append_round_trips_with_tight_permissions ... ok
test native::projects::tests::parse::project_parser_accepts_bare_project_type_and_prj_states ... ok
test native::projects::tests::parse::project_parser_records_prj_sub_block_marker_lines ... ok
test native::highlights_ref::sources::tests::legacy_only_notes_warn_instead_of_refusing ... ok
test native::projects::tests::parse::type_forms_all_match_project_and_area ... ok
test native::projects::tests::parse::project_parser_records_scheduled_and_placeholder_prj ... ok
test native::projects::tests::parse::project_parser_stops_prj_sub_block_at_blank_line ... ok
test native::projects::tests::parse::task_tag_matches_tasks_plugin_boundaries ... ok
test native::projects::tests::parse::project_parser_reports_malformed_and_multiple_prj_lines ... ok
test native::projects::tests::parse::wikilink_target_extracts_normalized_note_names ... ok
test native::gkeep::config::tests::read_token_returns_first_non_empty_line ... ok
test native::gkeep::config::tests::read_token_rejects_sign_in_cookie ... ok
test native::projects::tests::edits::scheduled_tasks_precede_prj_surfacing_at_local_date_boundary ... ok
test native::projects::tests::edits::due_scheduled_projects_follow_the_normal_surfacing_rule ... ok
test native::highlights_ref::return_links::tests::filter_leaves_listen_cards_untouched ... ok
test native::highlights_ref::return_links::tests::filter_opt_out_returns_the_document_unchanged ... ok
test native::highlights_ref::return_links::tests::filter_renumbers_anchors_on_prefix_collision ... ok
test native::highlights_ref::return_links::tests::filter_pairs_links_from_prose_list_cell_and_footnote ... ok
test native::gkeep::adapter::tests::error_kinds_carry_messages_and_hints ... ok
test native::projects::tests::sync::render_subprojects_line_formats_closed_children_after_open_children ... ok
test native::projects::tests::sync::project_sync_plan_flips_status_without_prj_edits_after_effective_status ... ok
test native::projects::tests::sync::project_sync_plan_keeps_canonical_closed_subprojects_idempotent ... ok
test native::projects::tests::sync::subproject_display_parser_scopes_schedule_and_lifecycle_markers ... ok
test native::highlights_ref::return_links::tests::filter_resolves_decoded_and_github_aliases ... ok
test native::projects::tests::edits::project_schedule_accepts_quoted_dates_and_rejects_bad_dates ... ok
test native::randomize_plan::tests::counts_due_p0_tasks_but_ignores_the_rest ... ok
test native::projects::tests::sync::project_sync_plan_warns_on_placeholder_while_reopening ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subprojects_marker_line ... ok
test native::projects::tests::sync::project_sync_plan_marks_tracked_closed_subprojects ... ok
test native::randomize_plan::tests::extreme_priority_window_fails_before_any_write ... ok
test native::projects::tests::sync::project_sync_plan_removes_stale_scheduled_field ... ok
test native::projects::tests::sync::project_sync_plan_matches_subproject_links_case_insensitively ... ok
test native::randomize_plan::tests::identical_lines_get_distinct_rolls ... ok
test native::randomize_plan::tests::ignores_non_open_and_fieldless_and_foreign_tasks ... ok
test native::randomize_plan::tests::dates_survive_insertions_above_because_identity_ignores_lines ... ok
test native::randomize_plan::tests::ignores_tasks_scheduled_after_until ... ok
test native::randomize_plan::tests::keeps_paren_fields_and_spacing_when_replacing_the_date ... ok
test native::randomize_plan::tests::load_covers_35_days_with_p0_and_new_dates ... ok
test native::randomize_plan::tests::fixed_offsets_cross_month_year_and_leap_boundaries ... ok
test native::randomize_plan::tests::level_filtering_counts_not_selected ... ok
test native::randomize_plan::tests::matches_pomodoro_targets_by_path_stem_and_case ... ok
test native::randomize_plan::tests::level_filtering_matches_labels_case_insensitively ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_unhidden_count ... ok
test native::projects::tests::sync::project_sync_plan_leaves_non_terminal_open_prj_status_untouched ... ok
test native::randomize_plan::tests::project_note_postimage_moves_the_task_under_blocked ... ok
test native::randomize_plan::tests::project_postimage_is_byte_exact_with_blocked_move_and_badge ... ok
test native::randomize_plan::tests::rerolls_ready_and_blocked_tasks ... ok
test native::randomize_plan::tests::reroll_carries_every_json_task_field ... ok
test native::randomize_plan::tests::roll_at_the_representable_boundary_succeeds_and_past_it_fails ... ok
test native::randomize_plan::tests::skips_unknown_priority_values_with_detail ... ok
test native::randomize_plan::tests::skips_duplicate_priority_and_scheduled_fields ... ok
test native::randomize_plan::tests::same_inputs_give_the_same_plan ... ok
test native::projects::tests::sync::project_sync_plan_treats_user_sub_bullets_as_user_owned ... ok
test native::randomize_plan::tests::skips_non_ready_open_statuses ... ok
test native::randomize_plan::tests::ordinary_and_daily_notes_are_edited_but_not_regrouped ... ok
test native::randomize_plan::tests::until_shifts_both_the_cutoff_and_the_roll_base ... ok
test native::randomize_plan::tests::zero_width_window_reports_unchanged_without_writing ... ok
test native::projects::tests::sync::project_sync_plan_is_idempotent_when_prj_hide_tag_matches_dash_state ... ok
test native::randomize_plan::tests::skips_unparseable_scheduled_dates ... ok
test native::randomize_plan::tests::skips_hard_dates_from_fields_and_emoji ... ok
test native::projects::tests::sync::project_sync_plan_normalizes_subprojects_marker_drift ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subproject_schedule_markers ... ok
test native::ref_jobs::kick::tests::kick_disable_values ... ok
test native::ref_jobs::output::tests::age_buckets_match_human_table ... ok
test native::ref_jobs::output::tests::empty_view_counts_nothing ... ok
test native::projects::tests::sync::project_sync_plan_reopens_terminal_project_from_open_prj ... ok
test native::ref_library::coverage::tests::id_lid_and_book_target_extraction ... ok
test native::ref_library::coverage::tests::mismatched_source_id_does_not_mirror ... ok
test native::projects::tests::sync::subproject_state_treats_terminal_open_prj_child_as_open ... ok
test native::ref_library::coverage::tests::book_note_source_blocks_subtract_chapters ... ok
test native::ref_jobs::fallback::tests::fallback_refuses_a_missing_vault_root ... ok
test native::ref_library::coverage::tests::non_zorg_status_values_do_not_count ... ok
test native::ref_library::coverage::tests::multibyte_lines_never_panic_or_count ... ok
test native::ref_library::coverage::tests::owner_requires_less_indent ... ok
test native::ref_library::coverage::tests::record_block_range_keeps_internal_blank_lines ... ok
test native::ref_library::coverage::tests::shared_block_pair_stays_distinct_by_source_id ... ok
test native::ref_library::list::tests::ref_history_parses_per_file_marks_newest_first ... ok
test native::ref_library::coverage::tests::status_lines_count_and_mirrored_records_subtract ... ok
test native::ref_library::migrate_zorg::plan::tests::hub_stem_strips_extension ... ok
test native::ref_library::list::tests::since_accepts_absolute_and_relative_dates ... ok
test native::ref_library::migrate_zorg::plan::tests::ref_kind_reads_only_lib_targets ... ok
test native::ref_library::migrate_zorg::render::tests::acronym_words_uppercase_when_humanized ... ok
test native::ref_library::migrate_zorg::render::tests::book_note_folds_chapters_byte_for_byte ... ok
test native::ref_library::migrate_zorg::render::tests::owner_line_tags_skip_zorg_ids ... ok
test native::ref_library::migrate_zorg::render::tests::plain_record_renders_byte_for_byte ... ok
test native::ref_library::migrate_zorg::render::tests::related_keeps_only_pipe_lines ... ok
test native::ref_library::migrate_zorg::render::tests::title_folds_continuation_lines ... ok
test native::ref_library::migrate_zorg::render::tests::url_field_reads_inline_first_token_and_nested_items ... ok
test native::ref_library::migrate_zorg::render::tests::wikilinks_reduce_to_display_text ... ok
test native::randomize_plan::tests::skips_tasks_linked_from_open_pomodoros_in_every_link_form ... ok
test native::projects::tests::sync::project_sync_plan_skips_subproject_links_without_open_prj_edits ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_open_subprojects ... ok
test native::ref_library::output::tests::chips_carry_glyph_word_and_color ... ok
test native::ref_library::list::tests::selection_defaults_to_the_queue_without_filters ... ok
test native::ref_library::output::tests::list_human_groups_carry_color_and_counts ... ok
test native::ref_library::output::tests::markdown_cells_escape_pipes_and_newlines ... ok
test native::projects::tests::sync::subproject_aggregation_marks_only_schedules_after_shared_today ... ok
test native::ref_jobs::spool::tests::corrupt_done_lines_are_skipped ... ok
test native::ref_library::show::tests::wrap_hard_splits_long_words_and_keeps_blanks ... ok
test native::ref_library::show::tests::human_render_carries_chips_color_and_structure ... ok
test native::ref_library::show::tests::markdown_digest_keeps_quote_comment_and_tasks ... ok
test native::ref_library::status::tests::book_without_chapters_stays_unknown ... ok
test native::ref_library::status::tests::non_book_legacy_ignores_chapter_statuses ... ok
test native::highlights_ref::create::tests::listen_filter_keeps_glyph_without_bound_audio ... ok
test native::capture::tests::commit::commits_matching_multi_file_preimage ... ok
test native::ref_library::status::tests::book_derivation_covers_every_branch ... ok
test native::highlights_ref::create::tests::code_break_filter_splits_long_inline_code_paths ... ok
test native::highlights_ref::return_links::tests::filter_treats_table_head_foot_spans_as_skip_contexts ... ok
test native::ref_jobs::spool::tests::parentless_jobs_read_as_none_and_use_the_source_inbox ... ok
test native::ref_library::migrate_zorg::write::tests::commit_message_names_records_notes_and_rollback ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::ref_library::tests::missing_ref_dir_is_an_error ... ok
test native::highlights_ref::fetch::tests::fetch_covers_redirects_statuses_and_exit_codes ... ok
test native::highlights_ref::return_links::tests::filter_counts_tags_in_bijective_base_23 ... ok
test native::projects::tests::sync::subproject_parent_links_classify_open_and_terminal_prj_children ... ok
test native::highlights_ref::return_links::tests::filter_renders_dead_links_as_plain_text ... ok
test native::highlights_ref::return_links::tests::filter_numbers_github_duplicates_and_rejects_ambiguous_aliases ... ok
test native::plugins::tests::sync_refuses_then_forces_a_dirty_vault_file ... ok
test native::highlights_ref::return_links::tests::filter_leaves_skip_context_links_untagged ... ok
test native::ref_library::tests::query_classification_table ... ok
test native::ref_jobs::fallback::tests::fallback_creates_missing_target_like_capture ... ok
test native::highlights_ref::tests::reading_execute::birth_insert_then_rerun_adopts_without_duplication ... ok
test native::highlights_ref::stamp::tests::stamp_install_without_info_leaves_trailer_info_absent ... ok
test native::highlights_ref::stamp::tests::default_target_does_not_skip_past_same_at_2 ... ok
test native::highlights_ref::return_links::tests::filter_counts_rendered_cite_content_not_metadata ... ok
test native::highlights_ref::stamp::tests::default_target_different_library_suffixes ... ok
test native::highlights_ref::stamp::tests::default_target_title_matches_marker_or_info_normalized ... ok
test native::highlights_ref::return_links::tests::filter_treats_nested_heading_spans_as_skip_contexts ... ok
test native::highlights_ref::stamp::tests::stamp_install_appends_when_annots_exist_and_sets_partial_info ... ok
test native::highlights_ref::stamp::tests::default_target_same_intake_refuses_then_overwrites_with_force ... ok
test native::ref_library::tests::title_scoring_table ... ok
test native::ref_tasks::edit::tests::missing_destination_fails_before_any_write ... ok
test native::highlights_ref::return_links::tests::filter_leaves_non_capable_targets_untagged ... ok
test native::ref_tasks::edit::tests::preserves_existing_close_stamp ... ok
test native::highlights_ref::stamp::tests::stamp_install_embeds_marker_and_info_without_annots ... ok
test native::ref_tasks::insert::tests::archive_read_errors_propagate ... ok
test native::highlights_ref::return_links::tests::filter_prefers_real_ids_over_aliases ... ok
test native::highlights_ref::return_links::tests::filter_keeps_every_anchor_paired_with_exactly_one_pill ... ok
test native::highlights_ref::return_links::tests::filter_places_div_span_and_needspace_rows ... ok
test native::ref_jobs::kick::tests::kicked_child_leaves_session_and_stdio ... ok
test native::ref_tasks::edit::tests::refuses_deleted_changed_and_duplicate_lines ... ok
test native::ref_library::tests::clipped_blog_row_covers_media_dates_and_tombstones ... ok
test native::ref_library::tests::added_dates_cover_created_and_zorg_block ... ok
test native::ref_library::tests::arxiv_and_doi_identities_share_keys_and_conflict ... ok
test native::ref_tasks::tests::diagnostic_code_catalog_lists_every_code ... ok
test native::ref_library::tests::index_membership_and_coverage ... ok
test native::ref_library::tests::path_name_and_title_queries ... ok
test native::ref_library::tests::legacy_unread_is_superseded_by_the_pdf_capture ... ok
test native::ref_library::tests::arxiv_queries_strip_versions_and_order_by_state ... ok
test native::ref_library::tests::legacy_status_table_maps_every_reading_state ... ok
test native::ref_library::tests::malformed_yaml_falls_back_and_reports ... ok
test native::ob::tests::commit_paths_scopes_to_listed_paths ... ok
test native::ref_library::tests::top_level_note_has_no_status_type_or_tracker ... ok
test native::ref_tasks::tests::closed_at_birth_carries_completion_or_cancelled_stamp ... ok
test native::ref_library::tests::every_diagnostic_code_is_represented ... ok
test native::ref_tasks::tests::blockquote_task_counts ... ok
test native::ref_library::tests::blocked_tracker_defers_to_frontmatter_without_diagnostic ... ok
test native::ref_tasks::tests::managed_slot_ignores_later_authored_embed ... ok
test native::ref_tasks::tests::managed_embed_matches_positive_and_negative_cases ... ok
test native::ref_tasks::tests::open_in_done_is_report_only_and_open_v1_always_fires ... ok
test native::ref_tasks::tests::outside_area_fires_for_daily_and_hub_notes ... ok
test native::ref_tasks::tests::missing_path_target_is_keyed_for_adoption_and_orphaned ... ok
test native::ref_tasks::tests::excluded_dirs_and_conflict_copies_are_never_read ... ok
test native::ref_library::tests::chat_notes_are_agent_reports_with_queue_states ... ok
test native::ref_library::tests::url_queries_match_identity_including_www_variants ... ok
test native::ref_tasks::tests::path_qualified_resolution_with_case_insensitive_fallback ... ok
test native::ref_tasks::tests::ref_dir_outside_vault_yields_warning_and_empty_index ... ok
test native::ref_tasks::tests::render_sanitizes_collapses_and_truncates_title ... ok
test native::ref_tasks::tests::ref_task_without_link_is_orphan ... ok
test native::ref_tasks::tests::bare_unique_stem_resolves_but_collision_is_ambiguous ... ok
test native::task_complete::tests::retirement_tests::dedupe_drops_carried_copy_when_destination_already_links_task ... ok
test native::ref_tasks::tests::selection_rules_cover_open_ambiguity_closed_v1_and_empty ... ok
test native::ref_tasks::tests::slug_ascii_empty_length_and_numeric_collisions ... ok
test native::task_complete::tests::recovery_tests::dependent_without_completed_prerequisite_stays_blocked ... ok
test native::task_complete::tests::recovery_tests::non_blocked_dependent_is_untouched ... ok
test native::task_complete::tests::recovery_tests::future_scheduled_dependent_stays_blocked ... ok
test native::task_complete::tests::recovery_tests::second_open_prerequisite_keeps_dependent_blocked ... ok
test native::task_complete::tests::recovery_tests::sole_prerequisite_recovers_to_ready ... ok
test native::task_complete::tests::recovery_tests::unresolved_dependency_id_does_not_block_recovery ... ok
test native::ref_tasks::tests::fenced_frontmatter_embed_and_managed_embed_are_ignored ... ok
test native::task_complete::tests::retirement_tests::mixed_bullet_with_live_second_link_does_not_move ... ok
test native::task_complete::tests::retirement_tests::move_to_last_completed_entry_when_nothing_runs ... ok
test native::task_complete::tests::retirement_tests::move_from_placeholder_to_running_removes_emptied_placeholder ... ok
test native::task_complete::tests::retirement_tests::reconcile_without_flag_moves_instead_of_deduping ... ok
test native::ref_library::tests::tracker_diagnostics_fall_back_to_frontmatter ... ok
test native::ref_tasks::tests::wrapper_without_ref_is_not_a_candidate ... ok
test native::ref_tasks::tests::v1_caret_line_is_never_candidate_or_orphan ... ok
test native::task_complete::tests::retirement_tests::strike_in_place_under_running_entry ... ok
test native::task_complete::tests::retirement_tests::retirement_preserves_crlf ... ok
test native::ref_tasks::tests::references_does_not_count_but_uppercase_ref_does ... ok
test native::task_complete::tests::retirement_tests::unrelated_already_done_link_is_left_untouched ... ok
test native::highlights_ref::ingest::tests::second_ingest_waits_for_the_lock ... ok
test native::task_complete::tests::successor_tests::closing_placement_creates_placeholder ... ok
test native::task_complete::tests::successor_tests::closing_placement_takes_lone_stub ... ok
test native::task_complete::tests::successor_tests::inbox_parity_shared_cases ... ok
test native::ref_library::tests::tracker_dates_cover_bracket_cancelled_and_emoji_forms ... ok
test native::ref_library::tests::building_the_index_writes_nothing ... ok
test native::task_complete::tests::successor_tests::sl11_project_and_hidden_tasks_recover_only ... ok
test native::task_complete::tests::successor_tests::idless_root_anchors_id_bearing_child_dependent ... ok
test native::task_complete::tests::successor_tests::sl10_mints_missing_block_id ... ok
test native::task_complete::tests::successor_tests::sl12_two_predecessors_link_once_at_earlier_anchor ... ok
test native::ref_tasks::tests::residence_covers_root_done_and_other_with_outside_area ... ok
test native::task_complete::tests::successor_tests::sl13_chain_waits_and_sl15_stale_ready_links ... ok
test native::task_complete::tests::successor_tests::sl16_gate_without_ids_runs_nothing ... ok
test native::task_complete::tests::successor_tests::sl18_disabled_recovers_without_links_or_mints ... ok
test native::task_complete::tests::successor_tests::sl17_breaker_links_none ... ok
test native::ref_library::tests::wikilink_parent_and_opaque_url ... ok
test native::task_complete::tests::successor_tests::sl23_subtask_inherits_root_anchor ... ok
test native::task_complete::tests::successor_tests::sl25_planned_next_reports_nothing ... ok
test native::task_complete::tests::tree_tests::completion_field_spacing_with_and_without_block_id ... ok
test native::task_complete::tests::successor_tests::slot_placement_orders_and_reports_lines ... ok
test native::task_complete::tests::successor_tests::sl3_and_sl4_stay_blocked_with_reasons ... ok
test native::task_complete::tests::successor_tests::sl1_links_blocked_dependent_into_slot ... ok
test native::task_complete::tests::successor_tests::sl5_already_planned_recovers_without_link ... ok
test native::task_complete::tests::successor_tests::sl28_day_file_successor_names_note ... ok
test native::task_complete::tests::successor_tests::sl26_inbox_successor_links_with_flag ... ok
test native::task_complete::tests::successor_tests::sl9_unplanned_predecessor_recovers_without_link ... ok
test native::task_dependencies::tests::dependency_line_guard_matches_every_form ... ok
test native::task_complete::tests::tree_tests::done_root_is_a_no_op_that_still_closes_open_children ... ok
test native::task_dependencies::tests::dp_discovery_context_vectors ... ok
test native::task_dependencies::tests::dw_create_and_identity_vectors ... ok
test native::task_complete::tests::tree_tests::canceled_descendant_is_neither_closed_nor_reported ... ok
test native::task_dependencies::tests::dw_indent_and_ending_vectors ... ok
test native::task_dependencies::tests::dp_vectors ... ok
test native::task_dependencies::tests::dw_link_form_vectors ... ok
test native::ref_library::tests::url_miss_falls_back_to_slug_title_candidates ... ok
test native::task_dependencies::tests::dw_writer_form_vectors ... ok
test native::task_complete::tests::tree_tests::explicit_completes_blocked_root_while_close_link_refuses_it ... ok
test native::task_dependencies::tests::legacy_child_shapes ... ok
test native::task_complete::tests::successor_tests::sl6_struck_history_does_not_count_as_planned ... ok
test native::task_complete::tests::tree_tests::explicit_blocked_descendant_child_stays_open ... ok
test native::task_fields::tests::filters_by_key ... ok
test native::task_complete::tests::tree_tests::unknown_status_descendant_is_left_open ... ok
test native::task_fields::tests::format_round_trips_through_strict_parse ... ok
test native::task_fields::tests::finds_bracket_and_paren_forms ... ok
test native::task_complete::tests::tree_tests::explicit_done_descendant_is_not_descended ... ok
test native::task_fields::tests::has_any_field_checks_several_keys ... ok
test native::task_fields::tests::key_match_is_case_sensitive ... ok
test native::task_fields::tests::matches_with_no_space_after_the_colons ... ok
test native::task_fields::tests::matches_with_spacing_around_the_colons ... ok
test native::task_fields::tests::reports_exact_byte_ranges ... ok
test native::task_fields::tests::strict_date_rejects_impossible_february ... ok
test native::task_complete::tests::tree_tests::nested_embeds_close_with_blocked_and_recurring_left_open ... ok
test native::task_fields::tests::strict_date_rejects_non_dates ... ok
test native::task_fields::tests::reports_duplicate_fields_in_order ... ok
test native::task_status_groups::tests::authored_heading_inside_a_managed_group_fails_closed ... ok
test native::task_status_groups::tests::badge_anchors_percent_encode_the_obsidian_path_segments ... ok
test native::task_status_groups::tests::badge_row_is_not_a_task_or_ambiguous_boundary ... ok
test native::task_status_groups::tests::conservation_and_source_records ... ok
test native::task_status_groups::tests::badge_counts_refresh_when_membership_changes ... ok
test native::task_status_groups::tests::authored_child_containers_get_independent_badges_and_anchors ... ok
test native::task_status_groups::tests::blockless_and_duplicate_ids_still_group ... ok
test native::task_status_groups::tests::authored_topics_receive_local_groups ... ok
test native::task_status_groups::tests::badge_marker_in_intake_is_relocated_to_the_slot ... ok
test native::task_status_groups::tests::custom_terminal_statuses_and_registry_precedence ... ok
test native::task_status_groups::tests::empty_global_filter_accepts_all_checkbox_tasks ... ok
test native::task_status_groups::tests::crlf_mixed_endings_unicode_and_missing_final_newline ... ok
test native::task_status_groups::tests::global_filter_rejects_non_matching_lines ... ok
test native::task_status_groups::tests::h6_tasks_is_skipped_with_a_diagnostic ... ok
test native::task_status_groups::tests::duplicate_badge_rows_self_heal_into_the_slot ... ok
test native::task_status_groups::tests::heading_hash_in_ancestry_renders_unlinked_badges ... ok
test native::task_status_groups::tests::heading_only_first_setup_is_a_change ... ok
test native::task_status_groups::tests::is_badge_row_accepts_linked_unlinked_and_mixed_rows ... ok
test native::task_status_groups::tests::excluded_markdown_contexts_are_not_task_roots_or_headings ... ok
test native::task_status_groups::tests::lazy_continuation_skips_the_container ... ok
test native::ref_library::tests::pending_and_conflict_status_precedence ... ok
test native::task_status_groups::tests::empty_groups_are_retained_once_created ... ok
test native::task_status_groups::tests::misplaced_badge_rows_fail_closed ... ok
test native::task_status_groups::tests::malformed_and_duplicate_markers_fail_closed ... ok
test native::task_status_groups::tests::legacy_marker_never_eats_following_prose ... ok
test native::task_status_groups::tests::marker_free_output_emits_row_directly_under_tasks ... ok
test native::task_status_groups::tests::orphaned_badge_block_is_removed_without_creating_groups ... ok
test native::task_status_groups::tests::ordered_list_roots_and_nested_ordinary_items_are_reported ... ok
test native::task_status_groups::tests::legacy_marker_migrates_to_a_marker_free_row_in_the_slot ... ok
test native::task_status_groups::tests::nested_children_travel_with_parent_status ... ok
test native::task_status_groups::tests::ready_only_and_empty_sections_are_not_decorated ... ok
test native::task_status_groups::tests::skip_codes_are_stable ... ok
test native::task_status_groups::tests::out_of_scope_spans_are_byte_identical ... ok
test native::task_status_groups::tests::prose_lookalike_is_preserved_as_intake_prose ... ok
test native::task_status_groups::tests::unmarked_group_title_with_prose_is_a_collision ... ok
test native::task_status_groups::tests::nested_tasks_is_processed_once ... ok
test native::task_status_groups::tests::prose_inside_managed_groups_is_preserved ... ok
test native::task_status_hooks::reconcile::fields::tests::dr_field_projection_vectors ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_drops_both_fields_for_r9 ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_lands_right_of_fresh_and_replaces_stale ... ok
test native::task_status_groups::tests::standalone_prose_is_not_attached_to_a_task ... ok
test native::task_status_groups::tests::safe_legacy_adoption_completes_a_partial_set ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_removes_depends_on_when_empty ... ok
test native::task_status_groups::tests::multiple_tasks_headings_and_heading_syntax_variants ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_places_id_before_depends_on_before_block_id ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_fields_between_tags ... ok
test native::task_status_groups::tests::tabs_internal_blanks_and_fences_stay_in_the_task_block ... ok
test native::task_status_groups::tests::reopening_a_task_to_ready_appends_to_intake ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_parenthesized_metadata ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_stamps_target_past_hide_tag ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_field_before_trailing_tags ... ok
test native::task_status_hooks::retry::tests::allowed_transient_reasons_are_retried_without_applied_files ... ok
test native::ref_library::tests::synced_paper_row_covers_the_core_fields ... ok
test native::task_status_hooks::retry::tests::any_error_listing_applied_files_is_never_retried ... ok
test native::task_status_hooks::retry::tests::partial_apply_is_never_retried_even_with_no_applied_files ... ok
test native::task_status_hooks::retry::tests::random_unit_interval_varies_and_stays_in_unit_range ... ok
test native::task_status_hooks::retry::tests::retry_ceiling_progression_caps_at_thirty_seconds ... ok
test native::task_status_hooks::retry::tests::retry_delay_stays_within_upper_half_of_ceiling ... ok
test native::ref_library::tests::region_oddities_exclude_preamble_and_report_unparsed ... ok
test native::task_status_hooks::retry::tests::retry_loop_stops_immediately_on_terminal_reason_without_noise ... ok
test native::task_status_hooks::retry::tests::terminal_and_unknown_reasons_are_never_retried ... ok
test native::task_status_hooks::tests::structure::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::structure::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::structure::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_hooks::tests::structure::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::tests::structure::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::structure::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::tests::structure::dependency_lines_are_not_legacy_children ... ok
test native::task_status_hooks::tests::structure::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::structure::direct_child_scan_counts_plain_children_but_ignores_fences ... ok
test native::task_status_hooks::tests::structure::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::structure::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::structure::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::structure::empty_timed_entries_are_not_current_targets_or_ambiguity_inputs ... ok
test native::task_status_hooks::tests::structure::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::structure::extracts_only_block_links_under_open_pomodoros ... ok
test native::task_status_hooks::tests::structure::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::task_status_hooks::tests::structure::empty_pomodoro_deletion_removes_full_blocks_and_preserves_crlf_eof ... ok
test native::task_status_hooks::tests::structure::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::structure::entries_emptied_by_duplicate_cleanup_are_removed_in_same_pass ... ok
test native::task_status_hooks::tests::structure::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::tests::structure::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::structure::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::structure::moving_last_child_removes_source_but_retains_destination ... ok
test native::task_status_hooks::tests::structure::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::task_status_hooks::tests::structure::two_non_empty_timed_entries_still_match_the_ambiguity_guard ... ok
test native::task_status_hooks::tests::structure::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::sync::ambiguous_basename_does_not_resolve ... ok
test native::task_status_hooks::tests::structure::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::sync::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::task_status_hooks::tests::sync::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::sync::archive_targets_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::sync::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::retry::tests::retry_loop_with_zero_budget_makes_one_attempt_and_never_sleeps ... ok
test native::task_status_hooks::tests::sync::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::task_status_hooks::tests::sync::legacy_children_without_field_coverage_are_not_edges ... ok
test native::task_status_hooks::tests::sync::dependency_line_links_are_promotion_edges ... ok
test native::task_status_hooks::tests::sync::legacy_plain_embedded_and_struck_children_are_edges_with_field_coverage ... ok
test native::task_status_hooks::tests::sync::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::task_status_hooks::tests::sync::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::sync::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::sync::reading_embeds_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::sync::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::task_status_hooks::tests::sync::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::task_status_hooks::tests::sync::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::tests::sync::sticky_lanes_keep_next_and_in_progress_outside_daily_notes ... ok
test native::task_status_hooks::tests::sync::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::sync::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
test native::task_status_hooks::tests::sync::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::sync::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::retry::tests::retry_loop_clamps_sleep_to_remaining_budget ... ok
test native::task_status_hooks_write::tests::deletion_prevents_write ... ok
test native::task_status_hooks::tests::sync::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test native::task_status_hooks::retry::tests::retry_decision_log_includes_run_attempt_reason_and_recovery_directory ... ok
test native::task_status_hooks_write::tests::multiply_linked_output_is_rejected ... ok
test native::task_status_groups::tests::golden_layout_groups_every_status_bucket_and_keeps_ready_intake ... ok
test native::task_status_hooks_write::tests::live_rescan_sees_new_vault_file ... ok
test native::ref_tasks::tests::follow_up_full_path_is_attributed_but_same_note_is_not ... ok
test native::task_status_hooks_write::tests::changed_tasks_settings_prevent_write ... ok
test native::task_status_hooks_write::tests::changed_previous_daily_prevents_write ... ok
test native::task_status_hooks_write::tests::noop_creates_no_recovery_or_staging ... ok
test native::task_status_hooks_write::tests::equal_length_change_with_restored_mtime_prevents_write ... ok
test native::task_status_hooks_write::tests::future_mtime_defers_without_sleeping ... ok
test native::task_status_hooks_write::tests::quiet_period_waits_once_then_defers_if_changed ... ok
test native::task_status_hooks_write::tests::replacement_inode_prevents_write ... ok
test native::url_routing::intent::tests::classifier_table ... ok
test native::task_status_hooks_write::tests::new_or_deleted_scan_candidate_invalidates_plan ... ok
test native::task_status_hooks_write::tests::symlink_substitution_prevents_write ... ok
test native::task_status_hooks::retry::tests::retry_loop_retries_lock_contention_then_succeeds ... ok
test native::task_status_hooks::retry::tests::retry_loop_never_starts_another_attempt_once_budget_is_exhausted ... ok
test native::url_routing::intent::tests::url_list_lines_are_lexical ... ok
test native::url_routing::policy::tests::defaults_cover_the_plan_list ... ok
test native::url_routing::intent::tests::display_elides_long_urls ... ok
test native::url_routing::policy::tests::empty_list_excludes_nothing ... ok
test native::url_routing::policy::tests::normalization_strips_scheme_www_and_dot ... ok
test native::url_routing::policy::tests::invalid_yaml_is_an_error ... ok
test native::url_routing::policy::tests::subdomain_matching ... ok
test native::url_routing::policy::tests::toggles_gate_entries_independently ... ok
test native::url_routing::policy::tests::overrides_and_empty_list ... ok
test native::url_routing::tests::phase_api_hangs_together ... ok
test native::url_routing::verdict::tests::missing_ref_dir_counts_as_empty ... ok
test native::vault_links::tests::with_additional_unions_staged_notes_without_rebuilding ... ok
test runner::tests::alias_rewrite_preserves_separator_and_non_utf8_tail ... ok
test runner::tests::every_native_command_is_on_exactly_one_canonical_path ... ok
test runner::tests::aliases_resolve_to_leaves_and_do_not_collide_with_root_names ... ok
test runner::tests::subcommands_are_contiguous_in_section_order_and_alphabetical ... ok
test native::ref_jobs::fallback::tests::concurrent_edit_retries_and_commits_once ... ok
test native::ref_jobs::fallback::tests::fallback_appends_under_existing_tasks_with_file_indent ... ok
test native::ref_jobs::fallback::tests::stale_preimage_is_a_conflict_error ... ok
test runner::tests::build_cli_renders_without_panicking ... ok
test native::ref_tasks::insert::tests::missing_destination_is_created ... ok
test native::vault_links::tests::basename_walk_skips_hidden_directories ... ok
test native::vault_links::tests::exact_root_note_does_not_build_the_vault_index ... ok
test native::vault_links::tests::resolves_exact_path_before_unique_case_insensitive_basename ... ok
test native::highlights_ref::stamp::tests::default_target_cap_reports_no_free_name ... ok
test native::url_routing::verdict::tests::verdicts_cover_every_library_state ... ok
test native::ref_library::tests::same_index_twice_serializes_identically ... ok
test native::ref_jobs::spool::tests::job_json_round_trips_with_all_fields ... ok
test native::ref_library::migrate_zorg::write::tests::write_refuses_pre_existing_target_and_rolls_back_partial ... ok
test native::ref_library::migrate_zorg::write::tests::write_then_verify_round_trip ... ok
test native::ref_library::migrate_zorg::write::tests::verify_failure_deletes_created_files_and_prunes_own_dirs ... ok
test native::ref_tasks::edit::tests::preserves_crlf_and_neighbor_bytes ... ok
test native::highlights_ref::tests::reading_execute::reopen_prefers_old_id_and_suffixes_on_collision ... ok
test native::ref_tasks::edit::tests::flips_checkbox_and_stamps_close ... ok
test native::highlights_ref::tests::reading_execute::line_edit_updates_checkbox_and_stamps_close ... FAILED
test native::ref_tasks::edit::tests::unrelated_user_additions_survive ... ok
test native::ref_tasks::edit::tests::finds_moved_line_by_unique_content ... ok
test native::ref_tasks::insert::tests::preferred_id_reused_when_free ... ok
test native::ref_tasks::insert::tests::collision_reallocates_and_children_join ... ok
test native::ref_tasks::edit::tests::flips_quoted_task_preserving_quote_and_children ... ok
test native::ref_tasks::edit::tests::preserves_mixed_endings_and_final_newline ... ok
test native::ref_tasks::insert::tests::archive_collision_blocks_preferred_id ... ok
test native::highlights_ref::stamp::tests::default_target_same_library_refuses_with_and_without_force ... ok
test native::ref_jobs::spool::tests::done_log_trims_to_last_thousand ... ok
test native::ref_tasks::insert::tests::preferred_id_suffixed_when_destination_taken ... ok
test native::ref_jobs::spool::tests::job_ids_are_unique_and_shaped ... ok
test native::ref_jobs::spool::tests::spool_dirs_and_files_use_strict_modes ... ok
test native::ref_tasks::tests::insert_checks_archive_and_preserves_crlf ... ok
test native::ref_jobs::spool::tests::pending_keys_covers_pending_and_running ... ok
test native::task_status_hooks_write::tests::edit_between_staging_and_revalidate_survives ... ok
test native::plugins::tests::pull_repo_fast_forwards_from_remote ... ok
test native::completion::present::tests::structural_latency_is_warn_only ... ok
test native::task_status_hooks_write::tests::staging_failure_preserves_notes_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::retention_keeps_incomplete_and_prunes_old_completed ... ok
test native::task_status_hooks_write::tests::fresh_attempt_after_vault_changed_replans_from_intervening_edit ... ok
test native::task_status_hooks_write::tests::exclusive_temp_and_mode_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::tool_scopes_recovery_root_manifest_and_pruning ... ok
test native::task_status_hooks_write::tests::edit_before_later_replacement_reports_partial ... ok
test native::task_status_hooks_write::tests::unchanged_read_set_applies_and_records_recovery_bytes ... ok
test native::ob::tests::lock_wait_behavior ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::gkeep::adapter::tests::crash_garbage_and_timeout ... ok
test native::task_status_hooks_write::tests::quiet_period_skips_wait_for_stable_files_and_status_only ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::gkeep::adapter::tests::timeout_kills_grandchild_holding_stdout ... ok
test native::gkeep::adapter::tests::large_request_with_hanging_adapter_times_out ... ok
test native::highlights_ref::create::tests::listen_card_xelatex_render_uses_only_existing_packages ... ok
test native::highlights_ref::create::tests::return_link_xelatex_render_pairs_pills_with_destinations ... ok
test native::ref_jobs::kick::tests::kicked_worker_drains_a_seeded_job ... ok

failures:

---- native::highlights_ref::tests::reading_execute::line_edit_updates_checkbox_and_stamps_close stdout ----

thread 'native::highlights_ref::tests::reading_execute::line_edit_updates_checkbox_and_stamps_close' (1593955) panicked at src/native/highlights_ref/tests/reading_execute.rs:158:5:
- [x] #task #ref [[ref/papers/stem|Stem]] [created::2026-10-09] [completion:: 2026-10-10] ^ref-stem


failures:
    native::highlights_ref::tests::reading_execute::line_edit_updates_checkbox_and_stamps_close

test result: FAILED. 2155 passed; 1 failed; 0 ignored; 0 measured; 0 filtered out; finished in 31.90s

error: test failed, to rerun pass `--lib`
     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/bob-acab5a1cce33695e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/bob_notify-9cb84ae19692fc72)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/bob_pomodoro-8de41553a00f154c)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/tmux_bob_pomodoro-ee07736efd4ef465)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/cli-1f9ff39b0a0a5744)

running 1324 tests
test capture::authored::capture_authored_bullets_reject_item_emptied_by_markers ... ok
test capture::authored::capture_authored_bullets_dry_run_reports_children_without_writing ... ok
test capture::authored::capture_authored_bullets_reject_orphaned_nested_lines ... ok
test capture::clip::capture_history_without_a_provider_has_actionable_guidance ... ok
test aliases::tmux_pomodoro_alias_matches_canonical_on_fixture ... ok
test capture::authored::capture_authored_bullets_duplicate_route_marker_across_lines_is_usage_error ... ok
test capture::complete_block_id::block_id_incomplete_close_list_still_links ... ok
test aliases::randomize_alias_matches_canonical_dry_run_seed ... ok
test capture::authored::capture_authored_bullets_accept_dash_star_and_plus_markers ... ok
test capture::authored::capture_authored_bullet_marker_on_child_line_configures_whole_capture ... ok
test capture::batch::capture_batch_human_output_numbers_items ... ok
test capture::authored::capture_authored_bullets_skip_placeholder_lines ... ok
test aliases::group_help_matches_snapshots_within_80_columns ... ok
test capture::authored::capture_authored_bullets_duplicate_schedule_marker_across_lines_is_usage_error ... ok
test capture::batch::capture_global_batch_failure_leaves_every_fixture_unchanged ... ok
test aliases::pomodoro_status_forms_match_with_and_without_show_stale ... ok
test capture::bare::capture_bare_terminal_marker_dry_run_reports_plan_and_writes_nothing ... ok
test capture::authored::capture_authored_bullets_reject_indented_or_nonbullet_lines ... ok
test capture::complete_block_id::block_id_link_candidates_are_filtered_and_annotated ... ok
test capture::complete_block_id::block_id_missing_note_is_not_an_error ... ok
test capture::complete_block_id::block_id_suggestions_follow_body_examples ... ok
test capture::complete_block_id::block_id_used_covers_done_nontask_duplicates_and_order ... ok
test aliases::notify_alias_matches_canonical_help_and_bad_arity ... ok
test capture::batch::capture_global_destination_conflict_and_declaration_only_are_usage_errors ... ok
test capture::complete_editor::capture_complete_bare_hash_marker_is_an_empty_success ... ok
test capture::batch::capture_batch_duplicate_block_id_failure_leaves_no_partial_write ... ok
test capture::batch::capture_global_destination_human_and_stdin_and_dry_run ... ok
test capture::batch::capture_batch_dry_run_reports_all_items_without_writing ... ok
test capture::bare::capture_bare_terminal_marker_multiple_open_timed_pomodoros_is_io_error ... ok
test capture::complete_block_id::block_id_json_shape_and_human_line ... ok
test capture::complete_dependency::note_path_preserves_quoting_and_case_in_the_replacement ... ok
test capture::complete_dependency::rows_carry_exact_identities_and_id_flow_metadata ... ok
test capture::complete_dependency::existing_owner_marks_self_and_already_added_rows ... ok
test capture::complete_dependency::empty_query_orders_lanes_before_history_and_hides_last ... ok
test capture::complete_dependency::note_path_assigns_nested_case_sensitive_notes ... ok
test capture::authored::capture_authored_bullets_bullet_capture_uses_section_prefix_with_children ... ok
test capture::clip::capture_sub_bullet_task_ref_recovers_shift_and_nests_clipboard ... ok
test capture::complete_editor::capture_complete_cursor_in_body_text_is_an_empty_success ... ok
test capture::complete_editor::capture_complete_discovery_failure_reports_an_actionable_error ... ok
test capture::complete_editor::capture_complete_empty_text_defaults_to_an_empty_draft ... ok
test capture::complete_dependency::protected_spans_never_open_the_dependency_picker ... ok
test capture::complete_editor::capture_complete_human_output_is_plain_and_concise ... ok
test aliases::capture_grammar_does_not_swallow_group_words ... ok
test capture::complete_block_id::project_task_block_id_reports_stem_body_used_and_suggestions ... ok
test capture::complete_dependency::refetch_at_replacement_start_returns_the_full_snapshot ... ok
test capture::complete_dependency::previous_daily_snapshot_is_read_only ... ok
test capture::complete_editor::capture_complete_never_creates_the_vault_directory ... ok
test capture::complete_editor::capture_complete_missing_note_behind_a_resolved_route_is_an_empty_success ... ok
test aliases::completion_offers_group_members_status_flags_and_alias_options ... ok
test capture::clip::capture_history_dry_run_plans_colliding_files_without_writes ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_outside_the_text ... ok
test capture::complete_editor::capture_complete_rejects_a_cursor_that_splits_a_multibyte_character ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_lists_named_and_nameable_rows ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_human_labels_rows ... ok
test capture::complete_editor::capture_complete_reports_utf8_byte_offsets ... ok
test capture::complete_editor::capture_complete_wikilink_note_json_returns_replacement_and_cursor_after ... ok
test capture::complete_dependency::query_ranks_matches_and_keeps_history_findable ... ok
test capture::complete_editor::capture_complete_wikilink_same_note_heading_uses_capture_route ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_child_line ... ok
test capture::complete_query::capture_complete_all_tasks_works_on_a_global_sub_bullet_declaration ... ok
test capture::complete_dependency::closed_tasks_need_the_opt_in_and_stay_closed ... ok
test capture::complete_editor::capture_complete_pomodoro_close_protocol ... ok
test capture::bare::capture_bare_terminal_marker_preflight_failures_leave_daily_note_untouched ... ok
test capture::complete_dependency::traversal_and_ambiguous_paths_fail_without_writing ... ok
test capture::complete_query::capture_complete_completes_a_marker_on_a_nested_child_line ... ok
test capture::authored::capture_authored_nested_bullets_render_under_their_owners ... ok
test capture::complete_query::capture_complete_inherited_route_is_the_same_note_for_wikilinks ... ok
test capture::complete_query::capture_complete_route_json_ranks_prefix_before_substring ... ok
test capture::authored::capture_authored_bullets_preserve_inline_markdown_and_checkbox_text ... ok
test capture::complete_query::capture_complete_section_json_lists_headings_of_the_resolved_route ... ok
test capture::complete_query::capture_complete_all_tasks_uses_global_ranges_in_later_batch_item ... ok
test capture::batch::capture_global_destination_on_authored_child_line_applies_draft_wide ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_skips_create_when_ledger_cannot_place_it ... ok
test capture::batch::capture_global_destination_can_be_declared_at_the_end_of_any_item ... ok
test capture::complete_query::capture_complete_task_json_only_offers_tasks_with_a_block_id ... ok
test capture::clip::capture_clip_failures_leave_vault_untouched ... ok
test capture::complete_query::capture_complete_scopes_to_later_batch_item_and_ignores_separator ... ok
test capture::complete_editor::capture_complete_pomodoro_start_name_json_covers_empty_and_new_queries ... ok
test capture::complete_task_complete::complete_padded_line_offers_no_picker ... ok
test capture::complete_query::capture_complete_task_block_id_marker_completes_only_route_side ... ok
test capture::complete_editor::capture_complete_pomodoro_ranges_preserve_start_suffix ... ok
test capture::complete_ref_kind::ref_kind_appears_on_hat_picker ... ok
test capture::complete_task_complete::complete_id_less_and_recurring_rows_carry_guards ... ok
test capture::complete_task_complete::complete_bare_bang_lists_today_first_with_picker ... ok
test capture::complete_task_complete::complete_second_item_marks_already_selected ... ok
test capture::complete_query::capture_complete_global_declaration_replaces_only_the_active_component ... ok
test capture::complete_query::capture_complete_all_tasks_is_opt_in_and_plus_context_only ... ok
test capture::complete_editor::capture_complete_override_name_json_carries_keeps_ledger_and_running ... ok
test capture::complete_task_complete::shell_completion_serves_identified_enabled_bang_rows ... ok
test capture::complete_ref_kind::ref_kind_appears_on_colon_and_plus_pickers ... ok
test capture::complete_ref_kind::ref_kind_appears_on_amp_and_bang_pickers ... ok
test capture::clip::capture_history_provider_failures_leave_the_vault_untouched ... ok
test capture::complete_task_complete::complete_partial_query_decodes_and_drops_continuation_keys ... ok
test capture::authored::capture_authored_bullets_preserve_crlf_line_endings ... ok
test capture::clip::capture_flat_clipboard_list_routes_normalized_children ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_stack_under_the_same_completed_pomodoro ... ok
test capture::clip::capture_clip_json_always_emits_collection_fields ... ok
test capture::complete_task_link::complete_parent_task_plus_serves_json_and_human_candidates ... ok
test capture::authored::capture_bare_terminal_marker_authored_children_nest_one_level_deeper ... ok
test capture::authored::capture_authored_bullets_render_task_with_children_in_order ... ok
test capture::clip::capture_percent_one_is_an_exact_single_clip_alias ... ok
test aliases::group_routing_and_help ... ok
test capture::complete_task_link::complete_task_link_lists_the_worked_example_in_json_and_human ... ok
test capture::complete_task_complete::capture_task_id_reports_complete_replacement_in_both_modes ... ok
test capture::complete_editor::capture_complete_task_section_json_covers_components_and_warnings ... ok
test capture::parse::capture_parse_json_reports_batch_items_with_global_ranges ... ok
test capture::parse::capture_parse_json_output_is_stable_and_parseable ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_an_identified_task ... ok
test capture::parse::capture_parse_json_reports_retired_double_colon_as_migration_guidance ... ok
test capture::parse::capture_parse_human_output_is_plain_and_concise ... ok
test capture::parse::capture_parse_json_reports_wikilink_semantic_spans ... ok
test capture::complete_editor::capture_complete_pomodoro_close_selection_protocol ... ok
test capture::parse::capture_parse_named_pomodoro_reports_incomplete_need ... ok
test capture::parse::capture_parse_reads_one_stdin_line_when_text_is_omitted ... ok
test capture::parse::capture_parse_json_reports_pomodoro_note_mode_and_span ... ok
test capture::parse::capture_parse_human_reports_start_suffix ... ok
test capture::complete_editor::capture_complete_pomodoro_start_drop_protocol ... ok
test capture::parse::capture_parse_reports_diagnostics_without_failing ... ok
test capture::parse::capture_parse_reports_duplicate_global_destination_diagnostics ... ok
test capture::parse::capture_parse_reports_global_destination_metadata ... ok
test capture::parse::capture_parse_missing_text_is_a_usage_error ... ok
test aliases::script_fallback_uses_embedded_assets_for_canonical_and_old_spellings ... ok
test capture::parse::capture_parse_json_reports_task_block_id_marker_spans_and_needs ... ok
test capture::parse::capture_parse_reports_nested_sub_bullets_and_depths ... ok
test capture::parse::capture_parse_reports_orphaned_nested_bullet_diagnostic ... ok
test capture::parse::capture_parse_reports_sub_bullets_for_a_multiline_draft ... ok
test capture::parse::capture_parse_reports_utf8_byte_offsets ... ok
test capture::bare::capture_bare_terminal_marker_writes_pomodoro_note_under_current_pomodoro ... ok
test capture::authored::capture_authored_bullets_sub_bullet_nests_children_two_levels ... ok
test capture::complete_editor::capture_complete_pomodoro_name_json_offers_a_create_row ... ok
test capture::batch::capture_global_destination_routes_unmarked_items_and_keeps_overrides ... ok
test capture::complete_parent_task::plus_picker_fixture_vault_catalog_and_entry_points ... ok
test capture::batch::capture_batch_json_is_ordered_and_keeps_legacy_top_level ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_first_future_pomodoro ... ok
test capture::complete_block_id::block_id_link_new_and_project_note_intents ... ok
test capture::bare::capture_bare_terminal_marker_human_output_shows_the_ledger_entry ... ok
test capture::bare::capture_bare_terminal_marker_keeps_crlf_line_endings ... ok
test capture::bare::capture_bare_terminal_marker_selects_the_last_of_two_completed_pomodoros ... ok
test capture::bare::capture_bare_terminal_marker_falls_back_to_the_last_completed_pomodoro ... ok
test capture::parse_dependency::child_line_dependency_belongs_to_the_item ... ok
test capture::parse::capture_parse_json_reports_explicit_toggle_span_and_plain_ensure_next ... ok
test capture::authored::capture_authored_bullets_use_two_space_target_indentation ... ok
test capture::parse_dependency::dependency_new_task_reports_modifiers_and_target ... ok
test capture::bare::capture_bare_terminal_marker_batch_items_land_under_the_same_pomodoro_in_order ... ok
test capture::parse::capture_parse_never_touches_the_vault_or_clipboard ... ok
test capture::parse_dependency::escaped_ampersand_leaves_visible_token ... ok
test capture::parse_dependency::dependency_only_colon_alias_reports_existing_target ... ok
test capture::parse_dependency::dependency_only_plus_target_reports_task_dependency ... ok
test capture::parse_dependency::complete_reports_task_dependency_field ... ok
test capture::parse_dependency::dependency_only_suffixed_colon_target_is_rejected ... ok
test capture::parse_dependency::section_bullet_with_dependency_is_rejected ... ok
test capture::parse_dependency::rewrite_never_absorbs_ampersands_or_the_colon_alias ... ok
test capture::parse_dependency::quoted_note_reports_decoded_identity_and_offsets ... ok
test capture::parse_dependency::ownerless_dependency_needs_its_target ... ok
test capture::parse::capture_parse_json_reports_project_note_markers ... ok
test capture::parse::capture_parse_json_reports_project_task_ids_spans_and_mode ... ok
test capture::parse_dependency::malformed_modifiers_report_invalid_dependency ... ok
test capture::parse_dependency::inherited_parent_selects_the_existing_dependent ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_human_line ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_chain_items ... ok
test capture::parse_dependency::block_id_intent_follows_dependency_ownership ... ok
test capture::plan_budget::capture_complete_create_row_omits_plan_themes_without_config ... ok
test capture::plan_budget::capture_complete_start_name_again_row_reports_plan_themes ... ok
test capture::plan_budget::capture_complete_create_row_reports_plan_themes ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_valid_spec_and_spans ... ok
test capture::plan_budget::capture_complete_start_name_new_row_reports_plan_themes ... ok
test capture::parse_dependency::dependency_markers_interleave_with_destination_in_either_order ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_incomplete_needs_task ... ok
test capture::clip::capture_bare_terminal_marker_clipboard_marker_writes_children_beneath_note ... ok
test capture::complete_task_link::parent_picker_acceptance_round_trips_and_id_assignment_returns_replacement ... ok
test capture::freshness_stamps::capture_new_tasks_carry_no_fresh ... ok
test capture::parse::capture_parse_json_reports_sub_bullet_section_and_incomplete_needs ... ok
test capture::parse_pomodoro_start_drop::parse_start_drop_diagnostics_match_execution ... ok
test capture::parse_dependency::partial_queries_need_task_dependency ... ok
test capture::plan_budget::capture_strict_mode_refuses_new_theme_past_cap_atomically ... ok
test capture::plan_budget::capture_parse_link_close_with_drop_reports_close ... ok
test capture::parse::capture_parse_reports_start_suffix_spans_and_batch_offsets ... ok
test capture::parse_dependency::literal_ampersands_stay_prose ... ok
test capture::plan_budget::capture_strict_mode_refuses_project_note_path ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_human_and_help ... ok
test capture::parse_dependency::capture_dependency_failures_leave_the_vault_intact ... ok
test capture::plan_budget::capture_strict_mode_refuses_toggle_path ... ok
test capture::pomodoro_chain::chain_capture_parse_reports_per_token_items ... ok
test capture::pomodoro_chain::chain_capture_complete_returns_no_candidates ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_human_and_help ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_protocol ... ok
test capture::pomodoro_chain::chain_dry_run_writes_nothing ... ok
test capture::parse_dependency::capture_keeps_literal_ampersand_prose ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_human_and_help ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_drop_protocol ... ok
test capture::parse_pomodoro::capture_parse_named_pomodoro_start_protocol ... ok
test capture::pomodoro_chain::chain_failure_rolls_back_with_item_two_prefix ... ok
test capture::complete_parent_task::plus_picker_accepts_insert_and_preserves_operators ... ok
test capture::authored::capture_authored_bullets_pomodoro_linked_capture_includes_children ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_keeps_in_progress ... ok
test capture::parse::capture_parse_and_capture_report_shadowed_global_destination_warnings ... ok
test capture::plan_budget::capture_invalid_config_without_ledger_change_has_no_warning ... ok
test capture::batch::capture_global_sub_bullet_inserts_ordered_siblings_and_keeps_authored_children ... ok
test aliases::every_alias_matches_canonical_help_and_invalid_option ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_adjust_protocol ... ok
test capture::plan_budget::capture_without_ledger_change_has_no_plan_budget ... ok
test capture::plan_budget::capture_strict_mode_never_refuses_named_starts ... ok
test capture::plan_budget::capture_trailing_now_tag_fails_like_any_other_tag ... ok
test capture::pomodoro_chain::chain_close_then_start_reports_next_started_block ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_reports_full_block ... ok
test capture::pomodoro_chain::chain_adjust_then_close_reports_one_cumulative_block ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_batch_rollback ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_extends_and_reports_json ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_batch_atomicity_and_dry_run ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_nested_wording ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_parse ... ok
test aliases::move_done_tasks_alias_matches_canonical_on_git_fixture ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_unchanged_next_block ... ok
test capture::freshness_stamps::capture_link_leaves_next_untouched_without_future_schedule ... ok
test capture::complete_task_link::complete_task_link_round_trip_for_a_task_without_an_id ... ok
test capture::clip::capture_headerless_clip_marker_renders_under_tasks_and_pomodoros ... ok
test capture::complete_task_link::complete_task_link_pull_forward_agrees_with_the_scheduled_retire ... ok
test capture::complete_task_link::complete_task_link_batch_accepts_two_queries ... ok
test capture::clip::capture_clip_uses_each_target_notes_indent_and_tabs_for_a_fresh_note ... ok
test capture::freshness_stamps::capture_link_clears_keep_streak ... ok
test capture::freshness_stamps::capture_link_never_stamps_recurring_tasks ... ok
test capture::freshness_stamps::capture_link_stamps_next_when_it_retires_future_schedule ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_shift_protocol ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_retired_tail ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_moves_link_and_sets_next ... ok
test capture::pomodoro_close_log::capture_parse_pomodoro_close_log_protocol ... ok
test capture::plan_budget::capture_plan_budget_human_reports_meter_and_destination ... ok
test capture::parse_dependency::capture_executes_new_task_dependencies ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_execution_errors ... ok
test capture::pomodoro_close::capture_pomodoro_close_tracks_blocks_past_day_file_work_log ... ok
test capture::authored::capture_task_section_authored_children_and_composition ... ok
test capture::plan_budget::capture_plan_budget_invalid_config_skips_with_warning ... ok
test capture::plan_budget::capture_plan_budget_dry_run_matches_real_run ... ok
test capture::plan_budget::capture_plan_budget_warns_when_new_theme_grows_past_cap ... ok
test capture::plan_budget::capture_strict_mode_never_refuses_session_starts ... ok
test capture::plan_budget::capture_plan_budget_stays_quiet_when_over_cap_does_not_grow ... ok
test capture::plan_budget::capture_plan_budget_warns_on_link_growth_past_cap ... ok
test capture::parse_pomodoro::capture_parse_pomodoro_start_protocol ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_same_note_batch_and_rollback ... ok
test capture::clip::capture_history_is_headerless_structured_and_composes_with_routes ... ok
test capture::freshness_stamps::capture_link_stamping_is_idempotent_same_day ... ok
test capture::clip::capture_clip_saves_attachments_snippets_and_reports_dry_run ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_preserves_metadata_crlf_and_fallbacks ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_clamps_and_crosses_midnight ... ok
test capture::clip::capture_clip_marker_composes_with_schedule_routes_bullets_and_pomodoro ... ok
test capture::pomodoro_link::capture_malformed_pomodoro_marker_is_usage_error_without_writes ... ok
test capture::pomodoro_chain::chain_positional_args_form_works ... ok
test capture::pomodoro_chain::chain_human_output_numbers_both_items ... ok
test capture::parse_pomodoro_close::capture_parse_pomodoro_close_selection_protocol ... ok
test capture::pomodoro_link::capture_pomodoro_dry_run_validates_and_changes_neither_note ... ok
test capture::freshness_stamps::capture_link_stamps_ready_and_blocked_to_next ... ok
test capture::pomodoro_close::capture_pomodoro_close_reports_full_blocks ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_already_current ... ok
test capture::pomodoro_close::capture_pomodoro_close_link_reports_moved_source_and_next ... ok
test capture::pomodoro_link::capture_pomodoro_missing_daily_note_does_not_create_target ... ok
test capture::clip::capture_clip_options_force_or_disable_marker_parsing ... ok
test capture::pomodoro_link::capture_pomodoro_preflight_failures_leave_both_notes_untouched ... ok
test capture::pomodoro_name::capture_human_names_the_starting_pomodoro_and_its_time ... ok
test capture::pomodoro_close::capture_pomodoro_close_task_reports_closed_and_next ... ok
test capture::plan_budget::capture_destination_human_arrows_name_each_role ... ok
test capture::parse_dependency::capture_executes_dependency_only_updates_idempotently ... ok
test capture::pomodoro_close_successors::close_then_start_opens_successor_continuation ... ok
test capture::pomodoro_close_successors::close_with_invalid_dependency_note_reports_unavailable ... ok
test capture::pomodoro_close_successors::close_successor_dry_run_matches_real ... ok
test capture::pomodoro_close_successors::close_all_day_file_successor_composes_edits ... ok
test capture::pomodoro_close_successors::close_without_identities_reports_no_successors ... ok
test capture::pomodoro_adjust::capture_pomodoro_adjust_rejects_bad_grammar_and_targets ... ok
test capture::pomodoro_close_successors::close_successor_human_rows_and_next_line ... ok
test capture::pomodoro_name::capture_pomodoros_human_output_is_plain_when_piped ... ok
test capture::pomodoro_override::override_restart_batch_rollback ... ok
test capture::pomodoro_name::capture_pomodoros_missing_note_and_section_warn_in_json ... ok
test capture::pomodoro_name::capture_pomodoros_json_lists_open_entries_with_stable_picker_shape ... ok
test capture::pomodoro_name::capture_pomodoro_name_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::pomodoro_override::override_restart_human_output ... ok
test capture::pomodoro_name::capture_pomodoro_name_rejects_write_free_failures ... ok
test capture::pomodoro_override::override_restart_refuses_multiple_running ... ok
test capture::pomodoro_override::override_swap_batch_rollback ... ok
test capture::pomodoro_name::capture_pomodoros_task_link_count_matches_dry_run_lineup ... ok
test capture::pomodoro_close_successors::sl17_breaker_links_none_of_six_successors ... ok
test capture::pomodoro_close_successors::sl12_two_predecessors_link_shared_dependent_once ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_complete_target ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_plain_reports_numbered_lineup ... ok
test capture::pomodoro_override::override_swap_human_output ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_crlf_day_file ... ok
test capture::pomodoro_close_successors::sl20_second_completion_drops_first_link_net ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_in_progress_and_complete ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_human_output ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_all ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_complete_listed ... ok
test capture::pomodoro_close_successors::sl27_dropped_link_is_not_relinked ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_dry_run_and_blocks ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_defer_rest ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop ... ok
test capture::pomodoro_close_successors::sl24_successor_reuses_later_same_name_entry ... ok
test capture::pomodoro_override::override_swap_naming_running_refuses ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_human_output ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_dry_run_matches_real_run ... ok
test capture::pomodoro_override::override_swap_teaching_errors ... ok
test capture::pomodoro_link::capture_pomodoro_link_uses_default_day_file_and_untimed_fallback ... ok
test capture::pomodoro_override::override_swap_did_you_mean_spells_override ... ok
test capture::pomodoro_override::override_restart_dry_run_matches_real ... ok
test capture::pomodoro_override::override_restart_keeps_note_bearing_session ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_land_fixes ... ok
test capture::pomodoro_close_successors::route_close_links_predecessor_then_closes_with_successor ... ok
test capture::pomodoro_start::capture_pomodoro_start_active_and_ambiguous_fail_atomically ... ok
test capture::pomodoro_override::override_swap_fresh_timing_worked_example ... ok
test capture::pomodoro_link::capture_named_pomodoro_updates_both_notes_and_skips_current ... ok
test capture::pomodoro_link::capture_named_pomodoro_batch_reuses_new_placeholder ... ok
test capture::pomodoro_close_successors::sl7_close_all_creates_continuation_holding_only_successor ... ok
test capture::ensure_next::capture_task_toggle_named_ensure_next_moves_creates_and_noops ... ok
test capture::pomodoro_close_successors::sl8_embed_close_appends_successor_after_carried_links ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_created_named_destination ... ok
test capture::pomodoro_override::override_swap_drops_target_lineup ... ok
test capture::pomodoro_start::capture_pomodoro_start_dry_run_and_batch_rollback ... ok
test capture::pomodoro_reset::pomodoro_reset_clears_note_free_session ... ok
test capture::pomodoro_override::override_swap_placeholder_above_stays_first_future ... ok
test capture::pomodoro_override::override_swap_keeps_annotated_ledger_verbatim ... ok
test capture::pomodoro_link::capture_pomodoro_linked_task_updates_both_notes_and_reports_json ... ok
test capture::pomodoro_reset::pomodoro_reset_moves_before_earlier_future ... ok
test capture::pomodoro_link::capture_pomodoro_task_reports_running_entry_block ... ok
test capture::pomodoro_link::capture_pomodoro_link_reports_move_destination_first ... ok
test capture::pomodoro_override::override_swap_strict_never_refuses_created_target ... ok
test capture::freshness_stamps::capture_close_to_in_progress_stamps_but_complete_does_not ... ok
test capture::pomodoro_override::override_swap_kept_ledger_worked_example ... ok
test capture::pomodoro_override::override_swap_reports_notes ... ok
test capture::ensure_next::capture_task_toggle_ensure_next_covers_open_states_and_failures ... ok
test capture::pomodoro_override::override_swap_unnamed_running ... ok
test capture::pomodoro_name::capture_pomodoro_name_plus_is_selectable_and_targetable ... ok
test capture::pomodoro_start_drop::start_drop_out_of_range_and_empty_lineup ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_reports_full_block ... ok
test capture::pomodoro_override::override_swap_again_and_created_targets ... ok
test capture::pomodoro_override::override_restart_preserves_crlf_and_missing_newline ... ok
test capture::pomodoro_override::override_swap_chains ... ok
test capture::pomodoro_start::capture_pomodoro_start_rejects_invalid_and_conflicting_syntax ... ok
test capture::pomodoro_start_named::named_start_human_created_dry_run_and_forced_flags ... ok
test capture::pomodoro_start::capture_pomodoro_start_batch_adjusts_moved_entry ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_named_destination_before_link_move ... ok
test capture::pomodoro_start_named::named_start_grammar_errors_are_precise ... ok
test capture::pomodoro_chain::chain_switches_sessions_like_a_blank_line_batch ... ok
test capture::pomodoro_chain::chain_matches_blank_line_batch_file_by_file ... ok
test capture::pomodoro_chain::chain_wildcard_close_matches_blank_line_batch ... ok
test capture::pomodoro_override::override_swap_dry_run_matches_real ... ok
test capture::pomodoro_override::override_swap_named_restart_matches_plain_restart ... ok
test capture::pomodoro_start_drop::start_drop_bare_removes_link_with_nested_note ... ok
test capture::pomodoro_start_drop::start_drop_crlf_day_file ... ok
test capture::pomodoros_agenda::agenda_default_output_stays_byte_identical ... ok
test capture::pomodoros_agenda::agenda_all_lists_completed_with_empty_payloads ... ok
test capture::pomodoros_agenda::agenda_current_golden ... ok
test capture::pomodoros_agenda::agenda_empty_golden ... ok
test capture::pomodoro_start_named::named_start_again_creates_from_completed_name ... ok
test capture::pomodoro_override::override_swap_preserves_crlf_and_missing_newline ... ok
test capture::pomodoros_agenda::agenda_no_daily_note_golden ... ok
test capture::pomodoros_agenda::agenda_nothing_running_golden ... ok
test capture::pomodoros_agenda::agenda_multiple_timed_golden ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_guards_fail_write_free ... ok
test capture::pomodoros_agenda::agenda_heavy_golden ... ok
test capture::pomodoro_start_named::named_start_existing_reports_json_and_moves_to_current_slot ... ok
test capture::pomodoro_start::capture_pomodoro_start_already_in_slot_keeps_blank_line ... ok
test capture::pomodoro_start_named::named_start_created_reports_added_block ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_bare_defaults_and_midnight_wrap ... ok
test capture::pomodoro_start_drop::start_lineup_numbered_human_and_json ... ok
test capture::pomodoro_override::override_restart_matches_reset_then_start_on_note_free ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_park ... ok
test capture::priority::capture_priority_dry_run_prints_schedule_log_without_writing ... ok
test capture::priority::capture_priority_missing_config_file_is_io_error_without_writes ... ok
test capture::pomodoros_agenda::agenda_numbers_match_operator_lineups ... ok
test capture::priority::capture_priority_out_of_range_is_usage_error_without_writes ... ok
test capture::project_note::capture_project_note_named_caret_form_rejects_the_unused_pomodoro ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_moves_and_reports_json ... ok
test capture::pomodoro_start::capture_pomodoro_start_crlf_no_final_newline_moves_up ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_moved_block ... ok
test capture::pomodoro_start_named::named_start_running_guards_and_switch_chain ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_moves_first ... ok
test capture::pomodoro_reset::pomodoro_reset_note_fallback_stays_close ... ok
test capture::priority::capture_priority_level_one_rolls_scheduled_date_in_window ... ok
test capture::priority::capture_priority_level_four_rolls_scheduled_date_in_window ... ok
test capture::priority::capture_without_priority_token_tolerates_missing_config_file ... ok
test capture::priority::capture_priority_with_clip_orders_clip_children_before_schedule_log ... ok
test capture::priority::capture_priority_with_explicit_schedule_skips_roll ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_wildcard_logs_resolve_once_against_staged_lineup ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_runtime ... ok
test capture::pomodoro_link::capture_named_pomodoro_dry_run_and_failures_leave_notes_untouched ... ok
test capture::project_note::capture_project_note_retired_colon_forms_fail_with_teaching_errors ... ok
test capture::r#ref::capture_bracketed_url_queues_without_brackets ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_batches ... ok
test capture::r#ref::capture_config_off_and_invalid_config_keep_tasks ... ok
test capture::plan_budget::capture_destination_roles_cover_current_next_up_named_created ... ok
test capture::pomodoro_start_drop::start_drop_lexical_errors ... ok
test capture::r#ref::capture_dry_run_and_parse_never_touch_the_network_or_spool ... ok
test capture::pomodoro_start_drop::start_lineup_counted_and_named ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_drop_only_forms ... ok
test capture::r#ref::capture_excluded_and_corporate_hosts_stay_tasks ... ok
test capture::pomodoro_reset::pomodoro_reset_uppercase_and_modifiers ... ok
test capture::r#ref::capture_inline_global_blocks_ref_claim ... ok
test capture::r#ref::capture_parse_reports_ref_mode_and_span ... ok
test capture::priority::capture_priority_schedule_log_uses_the_target_notes_indent_unit ... ok
test capture::project_note::capture_project_note_creates_plain_note_with_json_and_human_output ... ok
test capture::pomodoro_start_named::named_start_prefix_and_duration_forms ... ok
test capture::priority::capture_priority_sub_bullet_nests_schedule_log_under_the_child ... ok
test capture::pomodoro_override::override_restart_worked_example_rows ... ok
test capture::pomodoro_start_named::named_start_missing_creates_and_warns_on_near_miss ... ok
test capture::r#ref::capture_spool_hit_is_clipping ... ok
test capture::project_note::capture_project_note_dry_run_and_batch_parenting_and_rollback ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_adjustments ... ok
test capture::rewrite::capture_rewrite_human_output_is_plain_and_concise ... ok
test capture::rewrite::capture_rewrite_json_absorbs_a_local_marker ... ok
test capture::rewrite::capture_rewrite_json_reports_a_rule_a5_notice_without_changing_text ... ok
test capture::project_note::capture_project_note_renders_authored_tasks_sections_and_tasks_merge ... ok
test capture::rewrite::capture_rewrite_json_reports_no_rewrite_without_a_bare_at_at ... ok
test capture::rewrite::capture_rewrite_never_touches_the_vault_or_clipboard ... ok
test capture::rewrite::capture_rewrite_missing_text_is_a_usage_error ... ok
test capture::rewrite::capture_rewrite_reads_stdin_when_text_is_omitted ... ok
test capture::rewrite::capture_rewrite_rejects_a_cursor_off_a_char_boundary ... ok
test capture::priority::capture_priority_json_includes_priority_fields_only_when_set ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_shifts ... ok
test capture::ref_grammar::capture_lone_bare_url_stays_a_task_while_routing_is_off ... ok
test capture::project_note::capture_project_note_schedule_and_priority_write_frontmatter_and_log ... ok
test capture::ref_grammar::capture_url_list_writes_one_task_per_line ... ok
test capture::routing::capture_empty_input_is_usage_error ... ok
test capture::routing::capture_json_failure_prints_error_object ... ok
test capture::routing::capture_dry_run_reports_without_writing ... ok
test capture::pomodoro_start::capture_pomodoro_start_moves_to_current_slot_screenshot_repro ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_batch_atomicity_and_dry_run ... ok
test capture::routing::capture_legacy_standalone_marker_form_is_usage_error ... ok
test capture::rewrite::capture_complete_and_rewrite_ignore_starts ... ok
test capture::pomodoro_override::override_idle_fallback_matches_plain_start ... ok
test capture::rewrite::capture_rewrite_pomodoro_close_protocol ... ok
test capture::routing::capture_rejects_stdin_continuation_text_that_is_not_a_bullet ... ok
test capture::r#ref::capture_url_with_markers_or_flags_stays_a_task ... ok
test capture::r#ref::capture_staged_write_failure_removes_jobs ... ok
test capture::r#ref::capture_lone_url_queues_a_ref_job ... ok
test capture::r#ref::capture_repeat_in_draft_is_duplicate ... ok
test capture::r#ref::capture_dry_run_matches_real_apart_from_dry_run_and_job ... ok
test capture::routing::capture_schedule_only_is_usage_error ... ok
test capture::routing::capture_scheduled_offset_out_of_range_is_usage_error ... ok
test capture::routing::capture_scheduled_dry_run_reports_without_writing ... ok
test capture::routing::capture_json_omits_sub_bullets_for_an_ordinary_single_line_capture ... ok
test capture::routing::capture_json_output_includes_scheduled_date ... ok
test capture::routing::capture_route_override_keeps_at_tokens_literal ... ok
test capture::routing::capture_reads_the_complete_piped_stdin_stream_when_text_is_absent ... ok
test capture::routing::capture_json_output_is_machine_readable ... ok
test capture::priority::capture_priority_renders_before_scheduled_and_before_pomodoro_block_id ... ok
test capture::project_note::capture_project_note_reports_created_pomodoro_block ... ok
test capture::r#ref::capture_with_kick_returns_before_the_clip_finishes ... ok
test capture::project_note::capture_project_note_rejections_leave_no_partial_write ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_preserves_metadata_and_matches_plugin ... ok
test capture::routing::capture_nonterminal_schedule_token_stays_literal ... ok
test capture::sections::capture_sections_missing_note_returns_empty_json ... ok
test capture::sections::capture_forced_section_requires_route ... ok
test capture::sections::capture_sections_json_lists_sections_in_order ... ok
test capture::sections::capture_sections_invalid_or_missing_route_errors_cleanly ... ok
test capture::sections::capture_tasks_human_output_is_plain_when_piped ... ok
test capture::routing::capture_unrouted_appends_to_mac_inbox ... ok
test capture::routing::capture_scheduled_zero_uses_created_date ... ok
test capture::sections::capture_tasks_json_lists_open_tasks_with_stable_picker_shape ... ok
test capture::r#ref::capture_mixed_list_and_draft_plan_each_item ... ok
test capture::r#ref::capture_library_hits_are_unchanged ... ok
test capture::sections::capture_forced_task_section_option_errors ... ok
test capture::routing::capture_bullet_json_reports_rendered_line ... ok
test capture::routing::capture_unrouted_scheduled_offset_appends_property ... ok
test capture::r#ref::capture_ref_parent_selection_reports_canonical_routes_and_hints ... ok
test capture::pomodoro_start::capture_pomodoro_start_midnight_wrap_and_bob_now ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_selects_first_placeholder_and_moves ... ok
test capture::routing::capture_leading_route_bullet_inserts_into_section_by_prefix ... ok
test capture::pomodoro_start::capture_pomodoro_start_unnamed_moves_between_done_and_review ... ok
test capture::pomodoro_start::capture_pomodoro_start_named_existing_and_new ... ok
test capture::pomodoro_start::capture_pomodoro_start_creates_unnamed_when_no_placeholder ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_positional_acceptance ... ok
test capture::targets::capture_targets_empty_vault_still_lists_inbox_default ... ok
test capture::targets::capture_targets_human_groups_and_summarizes_without_ansi ... ok
test capture::targets::capture_targets_json_failure_prints_error_object ... ok
test capture::targets::capture_targets_json_lists_picker_targets_in_order ... ok
test capture::task_blocks::capture_task_blocks_dry_run_reports_the_parent_block ... ok
test capture::task_blocks::capture_task_blocks_human_output_is_unchanged ... ok
test capture::task_blocks::capture_task_blocks_and_pomodoro_blocks_report_independently ... ok
test capture::routing::capture_routed_bullet_inserts_into_section_by_prefix ... ok
test capture::routing::capture_routed_prefers_tasks_section_over_root_task ... ok
test capture::task_blocks::capture_task_blocks_omitted_without_sub_bullets ... ok
test capture::targets::capture_targets_json_reports_aliases_and_human_shows_aka ... ok
test capture::targets::capture_targets_verbose_emits_skip_warnings ... ok
test capture::routing::capture_unrouted_prefers_tasks_section_in_existing_inbox ... ok
test capture::task_complete::already_done_is_a_noop ... ok
test capture::task_complete::ambiguous_and_duplicate_refusals_state_exit_code_and_leave_vault_untouched ... ok
test capture::task_complete::ambiguous_note_and_duplicate_id_and_forced_flags_fail ... ok
test capture::sections::capture_forced_section_inserts_exact_bullet ... ok
test capture::r#ref::capture_unknown_library_queues_with_message ... ok
test capture::r#ref::capture_url_list_queues_one_item_per_line ... ok
test capture::project_note::capture_project_note_task_links_need_the_day_file_only_for_links ... ok
test capture::pomodoro_start_drop::link_and_task_starts_stay_byte_stable ... ok
test capture::routing::capture_routed_prefix_inserts_and_suffix_creates_file ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_last_completed_entry_block ... ok
test capture::routing::capture_scheduled_offset_routes_in_either_order ... ok
test capture::sub_bullet::capture_pomodoro_note_reports_running_entry_block ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_complete_subtree_before_parent_logs ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_chains ... ok
test capture::task_complete::failure_in_item_two_rolls_item_one_back ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_rejects_shape_and_forced_flags ... ok
test capture::routing::capture_bullet_prefix_prefers_non_h1_and_ignores_prefix_case ... ok
test capture::routing::capture_bullet_marker_order_routes_equivalently ... ok
test capture::sub_bullet::capture_sub_bullet_uses_dominant_indent_preserves_crlf_and_dry_run ... ok
test capture::project_note::capture_project_note_task_links_report_the_resolved_pomodoro_name ... ok
test capture::project_note::capture_project_note_task_links_use_the_implicit_pomodoro ... ok
test capture::sub_bullet::capture_sub_bullet_task_option_keeps_at_tokens_literal ... ok
test capture::project_note::capture_project_note_task_links_write_the_worked_example ... ok
test capture::pomodoro_override::override_swap_matches_reset_then_start ... ok
test capture::task_complete::forced_flags_exit_2_with_exact_message_and_untouched_vault ... ok
test capture::task_complete::sl19_reapplied_close_reports_nothing ... ok
test capture::task_complete::complete_without_id_skips_dependent_lookup ... ok
test capture::task_blocks::capture_task_blocks_real_run_equals_dry_run_except_dry_run ... ok
test capture::sections::capture_task_section_errors_leave_the_note_unchanged ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_and_new_task_wildcards ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_listed_matches_ledger ... ok
test capture::task_complete::hello_ignores_poisoned_note_only_discovery_would_touch ... ok
test capture::task_complete::embedded_subtasks_close_and_blocked_descendant_stays_open ... ok
test capture::sections::capture_task_section_managed_log_geometry ... ok
test capture::r#ref::capture_end_to_end_falls_back_on_blocked ... ok
test capture::task_complete_parse::task_complete_padded_item_reports_invalid_task_complete ... ok
test capture::task_complete_parse::task_complete_padded_item_refuses_without_capturing ... ok
test capture::task_complete_parse::single_item_task_complete_mirrors_top_level_object ... ok
test capture::project_note::capture_project_note_task_links_dry_run_batch_and_rollback ... ok
test capture::task_complete_parse::task_complete_query_refuses_with_the_picker_teaching_error ... ok
test capture::task_complete_parse::task_complete_query_reports_incomplete_needing_task_complete ... ok
test capture::task_complete_parse::task_complete_token_executes_now_that_execute_landed ... ok
test capture::task_complete_parse::bang_prose_rows_parse_as_editor_tasks_and_queries ... ok
test capture::r#ref::capture_end_to_end_clips_through_the_worker ... ok
test capture::task_link::capture_batch_with_a_colon_query_writes_nothing ... ok
test capture::task_complete::refusals_leave_the_vault_intact ... ok
test capture::task_link::capture_colon_query_fails_with_the_picker_teaching_error ... ok
test capture::task_complete_parse::task_complete_token_reports_mode_spans_and_object ... ok
test capture::task_link::capture_colon_query_teaches_the_at_spelling_for_links ... ok
test capture::task_link::capture_parse_colon_query_reports_incomplete_task_link ... ok
test capture::task_id::capture_task_sections_json_and_human_list_sections ... ok
test capture::task_marker::capture_malformed_task_block_id_marker_is_usage_error_without_writes ... ok
test capture::task_link::capture_complete_colon_query_reports_task_link_with_empty_candidates ... ok
test capture::task_link::capture_colon_query_json_failure_reports_ok_false ... ok
test capture::task_marker::capture_retired_double_colon_marker_is_usage_error_without_writes ... ok
test capture::successor_integration::restart_and_reset_never_complete_prerequisites ... ok
test capture::task_complete::sl9_unplanned_predecessor_recovers_without_link ... ok
test capture::successor_integration::close_successor_then_consume_net ... ok
test capture::pomodoro_start_drop::start_drop_counted_offset_named_and_empty_session ... ok
test capture::task_marker::capture_task_block_id_dry_run_and_duplicate_preflight_do_not_write ... ok
test capture::task_id::capture_task_id_assigns_and_dry_runs_lf_and_crlf_notes ... ok
test capture::task_complete::task_living_in_todays_daily_note_completes_in_place ... ok
test capture::task_complete::blocked_root_completes_and_dependent_unblocks ... ok
test capture::task_complete::close_completing_nothing_ignores_poisoned_note ... ok
test capture::task_complete::batch_of_two_completions_reports_already_done_for_repeats ... ok
test capture::task_complete::carried_link_dedupes_into_morning_entry_when_nothing_runs ... ok
test completion::bash::bash_completes_attached_format_value ... ok
test completion::bash::bash_completes_attached_files_in_value ... ok
test completion::bash::bash_completes_command_prefix ... ok
test capture::sections::capture_forced_task_section_matches_title_exactly ... ok
test capture::sections::capture_task_section_inserts_into_first_middle_and_last_sections ... ok
test capture::sections::capture_task_section_prefix_vs_whole_slug_and_multiword ... ok
test capture::task_complete::custom_global_filter_yields_clean_text_and_human_output ... ok
test capture::task_complete::day_file_successor_without_block_id_mints_in_place ... ok
test capture::task_complete::dry_run_json_matches_real ... ok
test capture::task_marker::capture_task_block_id_marker_creates_missing_routed_note ... ok
test capture::task_complete::day_file_successor_composes_task_and_ledger_edits ... ok
test completion::bash::bash_default_target_honors_env ... ok
test completion::bash::bash_shell_selection ... ok
test completion::bash::bash_print_matches_installed_bytes ... ok
test capture::sub_bullet::capture_sub_bullet_errors_are_actionable_in_human_and_json_modes ... ok
test completion::bash::bash_counts_unicode_prefix_in_chars ... ok
test completion::bash::bash_maps_dirs_directive ... ok
test completion::bash::bash_filters_create_target_by_extension ... ok
test completion::bash::bash_offers_nothing_once_text_starts ... ok
test completion::bash::bash_open_quote_completes_route ... ok
test completion::bash::bash_keeps_spaces_in_one_argument ... ok
test completion::bash::bash_reassembles_colon_split_marker ... ok
test capture::task_complete_parse::bang_prose_rows_still_capture_as_tasks ... ok
test capture::sub_bullet::capture_sub_bullet_inserts_with_parent_indentation_and_reports_json ... ok
test capture::sub_bullet::capture_sub_bullet_selectors_and_batch_keep_order_above_logs ... ok
test capture::task_complete::invalid_dependency_note_reports_unavailable_and_skips_linking ... ok
test completion::capture_text::body_bearing_route_colon_suggests_new_id ... ok
test capture::task_complete::next_completes_with_running_session_strike ... ok
test completion::capture_text::bare_plus_shell_completion_returns_only_identified_parent_markers ... ok
test completion::bash::bash_strips_every_wordbreak_not_just_colon ... ok
test capture::task_id::capture_task_sections_empty_and_error_paths ... ok
test capture::task_toggle::capture_task_toggle_errors_are_actionable_without_writes ... ok
test completion::capture_text::newline_in_word_returns_nothing ... ok
test completion::capture_text::options_stay_hidden_once_text_starts ... ok
test completion::capture_text::named_start_completes_after_hash ... ok
test completion::capture_text::caret_completes_active_tasks ... ok
test completion::bash::bash_unquotes_single_quoted_word ... ok
test completion::capture_text::named_start_after_inline_close_keeps_prefix ... ok
test completion::bash::bash_install_status_uninstall_round_trip ... ok
test completion::capture_text::partial_route_returns_full_set_for_shell_filtering ... ok
test completion::capture_text::quoted_word_keeps_prefix_with_prefix_directive ... ok
test completion::capture_text::routes_complete_at_end_of_text_word ... ok
test completion::capture_text::body_bearing_text_agrees_with_capture_complete_intent ... ok
test capture::r#ref::capture_human_wording_for_every_case ... ok
test completion::lifecycle::dry_run_writes_nothing ... ok
test completion::capture_text::suffix_returns_nothing ... ok
test capture::task_toggle::capture_task_toggle_can_edit_task_in_daily_note ... ok
test completion::capture_text::safe_rows_only_omit_missing_ids ... ok
test capture::task_complete::placeholder_link_moves_to_running_entry_and_placeholder_is_removed ... ok
test capture::task_complete::sl18_disabled_config_recovers_without_link ... ok
test capture::task_complete::sl2_successor_keeps_slot_retirement_moves_predecessor ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_queued_tasks ... ok
test capture::task_complete::human_output_names_transition_ledger_and_unblocked ... ok
test capture::task_complete::sl10_successor_block_id_is_minted ... ok
test capture::task_complete::sl1_successor_links_into_vacated_slot ... ok
test capture::task_complete::sl16_gate_reports_checked_with_empty_rows ... ok
test capture::task_id::capture_task_id_recovers_a_shifted_line_and_rejects_write_free_failures ... ok
test completion::capture_text::capture_parse_and_rewrite_share_the_text_slot ... ok
test capture::successor_integration::ref_task_successor_links_like_an_ordinary_task ... ok
test completion::capture_text::wikilinks_return_nothing_quickly ... ok
test completion::capture_text::sections_complete_after_hash ... ok
test completion::capture_text::solo_route_colon_lists_existing_tasks ... ok
test completion::capture_text::unicode_prefix_counts_chars_not_bytes ... ok
test completion::capture_text::task_sections_complete_after_id_hash ... ok
test completion::bash::bash_verify_reports_source_remedy ... ok
test completion::lifecycle::path_shadow_warns ... ok
test completion::lifecycle::first_install_then_idempotent_unchanged ... ok
test completion::lifecycle::zsh_print_matches_installed_bytes ... ok
test completion::lifecycle::plain_output_has_no_ansi_when_piped ... ok
test completion::protocol::conflicting_option_is_dropped ... ok
test completion::protocol::double_dash_offers_long_forms_only ... ok
test completion::protocol::attached_option_value_uses_prefix ... ok
test completion::lifecycle::previous_install_target_rule_and_reason ... ok
test completion::capture_text::close_shorthands_offer_nothing ... ok
test completion::protocol::malformed_request_exits_two ... ok
test completion::protocol::alias_completion_uses_canonical_path_and_freshness_seed_is_hidden ... ok
test completion::protocol::format_values_carry_the_slot_group ... ok
test capture::task_complete::two_completions_plus_close_commit_as_one_batch ... ok
test completion::protocol::empty_root_offers_commands_then_capture_protocol_without_options ... ok
test completion::protocol::freshness_short_option_value_completes ... ok
test completion::lifecycle::not_installed_shell_never_probes_and_never_fails ... ok
test completion::protocol::hidden_aliases_stay_hidden ... ok
test completion::protocol::lone_dash_offers_paired_forms ... ok
test completion::protocol::debug_log_writes_the_file_and_nothing_else ... ok
test completion::protocol::file_and_dir_slots_emit_directives ... ok
test completion::lifecycle::unrecorded_stamped_file_is_outdated_externally_managed ... ok
test completion::lifecycle::outdated_adapter_updates_without_force ... ok
test completion::lifecycle::closers_tell_the_truth ... ok
test completion::protocol::present_option_is_dropped ... ok
test completion::protocol::protocol_skew_reports_both_directions ... ok
test completion::protocol::partial_command_word_yields_the_full_unfiltered_set ... ok
test completion::protocol::nested_subcommands_complete ... ok
test completion::lifecycle::target_move_removes_previous_adapter ... ok
test completion::lifecycle::status_without_verify_warns_on_recorded_unhealthy ... ok
test completion::lifecycle::status_json_shape_and_bare_forms ... ok
test completion::protocol::text_started_slot_offers_no_options ... ok
test completion::lifecycle::usage_errors_exit_2_and_shell_selection ... ok
test completion::zsh_adapter::adapter_source_has_required_properties ... ok
test capture::task_toggle::capture_task_toggle_reports_unlink_removal_from_two_entries ... ok
test completion::lifecycle::zsh_bound_to_function_reports ... ok
test capture::task_complete::exact_human_output_for_subtasks_and_unblocked ... ok
test completion::lifecycle::missing_manifest_entry_reports_missing ... ok
test completion::lifecycle::recorded_verification_survives_into_status ... ok
test capture::pomodoro_close::capture_pomodoro_close_worked_example ... ok
test completion::vault::plugins_come_from_the_repo_checkout ... ok
test completion::protocol::empty_cursor_at_positional_slot_offers_values_first ... ok
test completion::vault::levels_come_from_config_in_order ... ok
test completion::vault::routes_are_grouped_in_scan_order ... ok
test completion::lifecycle::externally_managed_adapter_is_reported_never_adopted ... ok
test completion::vault::task_sections_offer_exact_titles ... ok
test completion::lifecycle::uninstall_removes_only_bob_owned_files ... ok
test completion::vault::unknown_route_offers_nothing ... ok
test completion::vault::pomodoro_refs_offer_open_entries ... ok
test completion::zsh_adapter::default_styles_use_green_headers ... ok
test completion::zsh_adapter::no_color_uses_plain_header ... ok
test completion::zsh_adapter::colon_escaping_empty_fields_and_defaults ... ok
test completion::zsh_adapter::empty_output_returns_one ... ok
test dataview::dataview_native_where_false_returns_no_rows ... ok
test completion::lifecycle::install_without_shell_args_honors_shell_plus_owned ... ok
test dataview::dataview_native_table_json_projects_frontmatter_rows ... ok
test completion::lifecycle::home_default_fpath_line_prints_without_probe ... ok
test dataview::dataview_obsidian_dql_json_reads_query_file_and_forwards_env_vault ... ok
test dataview::dataview_native_dql_paths_walks_parent_frontmatter_headlessly ... ok
test completion::zsh_adapter::user_descriptions_format_wins ... ok
test completion::zsh_adapter::request_argv_unquotes_words_and_passes_suffix ... ok
test completion::zsh_adapter::directives_map_to_native_widgets ... ok
test completion::zsh_adapter::stderr_is_discarded ... ok
test completion::vault::missing_prerequisites_name_the_flag ... ok
test completion::zsh_adapter::candidate_groups_keep_order_and_nospace_flag ... ok
test dataview::dataview_obsidian_dql_paths_extracts_and_deduplicates_note_paths ... ok
test completion::vault::vault_notes_answer_files_in ... ok
test dataview::dataview_obsidian_reports_missing_command_without_query_blob ... ok
test dataview::dataview_obsidian_markdown_prints_rendered_markdown ... ok
test completion::lifecycle::fake_bash_never_reports_registered_when_missing ... ok
test dataview::dataview_rejects_removed_sync_option ... ok
test dataview::dataview_obsidian_reports_not_running_without_javascript_blob ... ok
test capture::task_marker::capture_task_block_id_marker_writes_ordinary_task_and_ignores_daily_note ... ok
test capture::pomodoro_start::capture_pomodoro_start_new_entry_uses_first_open_placement ... ok
test capture::sections::capture_task_section_indent_units_crlf_and_dry_run ... ok
test dataview::dataview_native_table_paths_match_list_rows_headlessly ... ok
test dataview::dataview_obsidian_query_does_not_run_ob_command ... ok
test dataview::dataview_obsidian_source_uses_path_command_and_sentinel_protocol ... ok
test completion::vault::deadline_override_keeps_working ... ok
test dataview::dataview_obsidian_dql_paths_warn_or_fail_for_missing_identities ... ok
test freshness::list_emoji_vault_is_refused_with_exit_2 ... ok
test dataview_oom::synthetic_list_census_counts_nested_children ... ok
test completion::vault::sections_follow_long_short_and_attached_route_forms ... ok
test completion::lifecycle::foreign_edited_and_symlink_refuse_without_force ... ok
test completion::vault::tasks_offer_open_block_ids_with_text ... ok
test dataview::dataview_obsidian_reports_protocol_errors ... ok
test dataview::dataview_rejects_invalid_argument_combinations ... ok
test freshness::list_invalid_canonical_budget_exits_2 ... ok
test freshness::list_hidden_recurring_reference_stays_out_while_visible_walks ... ok
test dataview::dataview_obsidian_reports_missing_and_malformed_sentinel ... ok
test dataview::dataview_rejects_unsafe_origin_and_missing_bob_dir ... ok
test capture::task_toggle::capture_task_toggle_reports_inserted_link_block ... ok
test capture::task_toggle::capture_task_toggle_reports_created_named_entry ... ok
test completion::protocol::value_hints_beat_generic_kinds_entries ... ok
test freshness::list_excludes_today_and_daily_lane_tasks ... ok
test freshness::list_invalid_config_exits_2 ... ok
test freshness::list_invalid_tracker_intervals_exit_2 ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_link_forms ... ok
test freshness::list_human_shows_references_before_rotten_divider ... ok
test freshness::list_invalid_decay_exits_2 ... ok
test freshness::list_budget_meter_uses_upkeep ... ok
test freshness::list_canonical_budget_key_wins_and_warns ... ok
test freshness::list_config_interval_and_budget ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_selection_diagnostics ... ok
test freshness::list_excludes_today_tasks ... ok
test help::capture_complete_help_is_native_only ... ok
test help::capture_help_is_native_only ... ok
test help::capture_pomodoros_help_is_native_only ... ok
test help::capture_sections_help_is_native_only ... ok
test freshness::list_lane_rows_cover_pending_and_next ... ok
test help::capture_parse_help_is_native_only ... ok
test freshness::list_json_reports_queue_counts_and_contract ... ok
test dataview::dataview_short_options_are_accepted ... ok
test help::capture_targets_help_is_native_only ... ok
test help::capture_pomodoro_name_help_is_native_only ... ok
test freshness::list_tracker_intervals_and_hide_gate ... ok
test help::capture_task_id_help_is_native_only ... ok
test freshness::list_walks_projects_after_new_with_decoupled_counts ... ok
test help::capture_task_sections_help_is_native_only ... ok
test help::dataview_help_is_native_only ... ok
test freshness::list_decay_off_and_zero_limit ... ok
test freshness::seed_dry_run_writes_nothing_and_reports_buckets ... ok
test help::capture_tasks_help_is_native_only ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_batches_compose_and_roll_back ... ok
test freshness::seed_dry_run_lists_files_without_writing ... ok
test freshness::seed_invariance_abort_lists_the_line ... ok
test help::highlights_ref_help_is_native_only ... ok
test help::move_done_tasks_help_is_native_only ... ok
test help::ref_help_matches_grouped_snapshot ... ok
test help::capture_named_start_help_mentions_start_forms ... ok
test help::legacy_binary_help_is_safe_and_plain ... ok
test freshness::list_limit_truncates_rows_not_counts ... ok
test freshness::seed_preserves_existing_keeps ... ok
test help::projects_help_is_native_only ... ok
test capture::task_toggle::capture_task_toggle_batch_uses_staged_snapshots_and_rolls_back ... ok
test freshness::list_json_and_human_cover_recurring_tier ... ok
test help_options::capture_parse_help_lists_options_alphabetically ... ok
test help_options::capture_pomodoro_name_help_lists_options_alphabetically ... ok
test help_options::capture_complete_help_lists_options_alphabetically ... ok
test help::help_routes_reject_non_command_paths_before_dispatch ... ok
test capture::task_toggle::capture_task_toggle_unlink_keeps_every_lane ... ok
test help::nightly_help_exits_before_operational_work ... ok
test help_options::capture_pomodoros_help_lists_options_alphabetically ... ok
test help_options::capture_help_lists_options_alphabetically ... ok
test freshness::list_human_has_sections_and_no_ansi ... ok
test help_options::capture_targets_help_lists_options_alphabetically ... ok
test help_options::capture_sections_help_lists_options_alphabetically ... ok
test help_options::capture_tasks_help_lists_options_alphabetically ... ok
test help::freshness_seed_stays_callable_but_hidden_from_help_and_completion ... ok
test help::cache_extraction_writes_expected_files_and_modes ... ok
test help::root_help_matches_sectioned_short_and_long_snapshots ... ok
test help_options::capture_task_sections_help_lists_options_alphabetically ... ok
test help_options::capture_rewrite_help_lists_options_alphabetically ... ok
test help_options::freshness_help_hides_the_seed_subcommand ... ok
test freshness::list_reports_keeps_and_decide_per_schema_9 ... ok
test freshness::seed_guard_refuses_and_force_overrides ... ok
test help_options::freshness_list_help_lists_options_alphabetically ... ok
test help_options::highlights_ref_scan_json_verbose_is_usage_error ... ok
test help_options::highlights_ref_sync_help_lists_options_alphabetically ... ok
test help_options::capture_task_id_help_lists_options_alphabetically ... ok
test help_options::highlights_ref_help_lists_subcommands_alphabetically ... ok
test help_options::dataview_help_lists_options_alphabetically ... ok
test help_options::freshness_seed_help_lists_options_alphabetically ... ok
test completion::lifecycle::target_rules_pick_in_order ... ok
test freshness::list_json_and_human_cover_checklist_tiers ... ok
test help_options::highlights_ref_scan_help_lists_options_alphabetically ... ok
test help_options::highlights_create_help_lists_options_alphabetically ... ok
test help_options::plugins_sync_help_lists_options_alphabetically ... ok
test help_options::ready_help_lists_options_alphabetically ... ok
test capture::task_complete::sl14_ambiguous_basename_uses_dir_link ... ok
test help_options::task_status_hooks_help_lists_options_alphabetically ... ok
test help_options::completion_help_lists_subcommands_and_options_alphabetically ... ok
test help_options::plugins_help_lists_subcommand_and_options ... ok
test help_options::highlights_clip_alias_help_matches_create_help ... ok
test freshness::list_legacy_budget_key_warns_once_and_still_counts ... ok
test highlights::create::highlights_create_dry_run_rejects_unknown_parent_with_hints ... ok
test highlights::create::highlights_create_dry_run_reports_planned_audio_copy ... ok
test highlights::create::highlights_create_dry_run_resolves_parent_alias_to_canonical_route ... ok
test freshness::seed_applies_stamps_and_rerun_is_noop ... ok
test capture::task_complete::successor_dry_run_matches_real_with_human_rows ... ok
test highlights::create::highlights_create_dry_run_prints_plan_without_writes ... ok
test help::pomodoro_help_documents_show_stale_option ... ok
test help_options::projects_help_lists_subcommands_and_options ... ok
test help::task_status_hooks_help_is_native_only ... ok
test highlights::create::highlights_create_arxiv_api_failure_falls_back_with_warning ... ok
test highlights::create::highlights_create_clip_alias_is_byte_identical_on_error_path ... ok
test highlights::create::highlights_create_folded_refuses_library_and_dedupe_collisions_early ... ok
test help::highlights_ref_subcommand_help_works ... ok
test help_options::default_subcommands_are_labeled_in_help ... ok
test capture::pomodoro_shift::capture_pomodoro_shift_rejects_bad_grammar_and_targets ... ok
test highlights::create::highlights_create_article_dry_run_writes_nothing ... ok
test capture::pomodoro_whole_item::capture_pomodoro_whole_item_start_reports_json_and_human ... ok
test highlights::create::highlights_create_arxiv_dry_run_shows_override_sources ... ok
test highlights::create::highlights_create_markdown_marker_carries_author_and_published ... ok
test highlights::create::highlights_create_folded_dry_run_writes_nothing ... ok
test highlights::create::highlights_create_local_pdf_overrides_author_and_published ... ok
test highlights::create::highlights_create_missing_parent_fails_before_any_work ... ok
test highlights::create::highlights_create_folded_rejects_protocol_errors ... ok
test highlights::create::highlights_create_folded_still_refuses_a_pdf_backed_url_note ... ok
test highlights::create::highlights_create_no_audio_skips_discovery ... ok
test highlights::create::highlights_create_output_dry_run_reports_direct_library_target ... ok
test help::script_fallback_help_is_safe_and_plain ... ok
test highlights::create::highlights_create_output_dry_run_reports_intake_library_destination ... ok
test highlights::create::highlights_create_output_existing_pdf_still_refuses_without_force ... ok
test highlights::create::highlights_create_output_dry_run_prints_exact_path_without_writes ... ok
test freshness::list_lane_intervals_false_null_and_invalid ... ok
test highlights::create::highlights_create_local_pdf_dry_run_writes_nothing_and_refuses_junk ... ok
test completion::vault::vault_slots_stay_fast ... ok
test capture::task_toggle::capture_task_toggle_link_and_unlink_updates_notes_and_reports_json ... ok
test capture::task_toggle::capture_task_toggle_named_creation_dry_run_and_pull_forward ... ok
test highlights::create::highlights_create_refuses_library_destination_audio ... ok
test highlights::create::highlights_create_pdf_url_rejects_claimed_pdf_and_404 ... ok
test highlights::create::highlights_create_refuses_existing_library_pdf_with_or_without_force ... ok
test capture::pomodoro_start_drop::start_drop_batch_chain_and_rollback ... ok
test highlights::create::highlights_create_refuses_different_audio_without_force ... ok
test highlights::create::highlights_create_rejects_conflicting_audio_flags ... ok
test highlights::create::highlights_create_rejects_bad_published_before_any_work ... ok
test highlights::create::highlights_create_refuses_mapped_private_literals_without_fetching ... ok
test highlights::create::highlights_create_local_pdf_title_override_and_name_type_output ... ok
test highlights::create::highlights_create_rejects_html_with_local_target_before_any_work ... ok
test highlights::create::highlights_create_article_maps_options_to_clip ... ok
test highlights::create::highlights_create_rejects_non_pdf_output ... ok
test highlights::create::highlights_create_rejects_bad_audio_paths ... ok
test highlights::create::highlights_create_rejects_output_combined_with_ref_type ... ok
test highlights::create::highlights_create_refuses_same_title_library_pdf_with_or_without_force ... ok
test highlights::create::highlights_create_folded_reports_adapter_failures_with_hints ... ok
test highlights::create::highlights_create_rejects_non_utf8_include_id_before_writes ... ok
test highlights::create::highlights_create_reuses_identical_existing_companion ... ok
test highlights::create::highlights_create_reports_pandoc_failure_diagnostics ... ok
test highlights::create::landing_bare_library_pdf_renames ... ok
test highlights::create::landing_name_alone_does_not_embed_marker_id ... ok
test highlights::create::landing_library_collision_hints_listen_attach ... ok
test highlights::create::highlights_create_article_routes_bot_wall_to_adapter ... ok
test highlights::create::highlights_create_folded_library_without_url_suffixes ... ok
test capture::task_toggle::capture_task_toggle_links_unlinked_lanes_without_status_change ... ok
test highlights::create::highlights_create_folded_direct_pdf_falls_back_to_slug_title ... ok
test highlights::create::highlights_create_folded_rejects_before_the_adapter_runs ... ok
test highlights::create::highlights_create_article_routes_through_clip_engine ... ok
test highlights::create::highlights_create_local_pdf_installs_and_stamps ... ok
test highlights::create::highlights_create_folded_force_overwrites_the_same_intake_target ... ok
test highlights::create::highlights_create_markdown_renders_outside_xlib ... ok
test highlights::create::highlights_create_arxiv_uses_api_metadata_and_short_stem ... ok
test completion::lifecycle::install_glyphs_follow_registration ... ok
test highlights::jobs::ref_jobs_group_flag_before_jobs_lists ... ok
test capture::task_complete::ledger_json_carries_text_struck_in_and_dropped ... ok
test highlights::create::highlights_create_pdf_url_colliding_slug_suffixes ... ok
test highlights::create::highlights_create_copies_audio_before_pdf_with_play_link ... ok
test highlights::jobs::ref_jobs_list_shows_the_parent ... ok
test highlights::create::highlights_create_folded_success_writes_stamped_intake_pdf ... ok
test highlights::create::highlights_create_local_pdf_inside_library_is_refused_with_listen_hint ... ok
test highlights::jobs::ref_jobs_bare_lists_empty_vault_state ... ok
test highlights::create::highlights_create_arxiv_captures_a_legacy_only_url_note_with_a_warning ... ok
test freshness::list_decides_on_early_dates ... ok
test completion::lifecycle::verify_probe_classifications ... ok
test highlights::jobs::ref_jobs_list_windows_and_json ... ok
test highlights::jobs::ref_jobs_second_worker_exits_zero ... ok
test highlights::create::highlights_create_article_binds_explicit_audio ... ok
test help::all_top_level_subcommand_help_is_safe_and_plain ... ok
test highlights::create::highlights_create_folded_captures_a_legacy_only_url_note_with_a_warning ... ok
test highlights::create::highlights_create_local_pdf_prepends_marker_and_snake_cases_stem ... ok
test highlights::create::highlights_create_pdf_url_stamps_and_dedupes ... ok
test highlights::create::highlights_create_stamps_rendered_pdf_through_shared_install ... ok
test highlights::listen::listen_conflicts_with_audio_and_no_audio ... ok
test highlights::jobs::ref_jobs_unwritable_running_fails_promptly ... ok
test capture::pomodoro_start::capture_pomodoro_start_default_and_explicit_durations ... ok
test highlights::listen::listen_dry_run_prints_would_run_without_invoking ... ok
test highlights::create::landing_marked_pdf_outside_vault_is_refused ... ok
test highlights::create::highlights_create_pdf_url_binds_explicit_audio ... ok
test highlights::listen::listen_invalid_template_is_an_error ... ok
test highlights::create::highlights_create_local_pdf_different_title_suffixes_with_id ... ok
test completion::vault::completion_is_read_only ... ok
test highlights::create::ingest_characterizes_url_failure_modes ... ok
test highlights::jobs::ref_jobs_stale_running_twice_falls_back_without_clipping ... ok
test capture::pomodoro_close::capture_pomodoro_close_diagnostics ... ok
test highlights::listen::listen_attach_refuses_when_audio_exists ... ok
test highlights::listen::listen_unconfigured_fails_before_fetch ... ok
test highlights::jobs::ref_jobs_stuck_fallback_is_retried_without_clipping ... ok
test highlights::listen::listen_interrupted_exits_130 ... ok
test highlights::listen::listen_failure_writes_nothing ... ok
test highlights::create::highlights_create_folded_round_trips_through_scan ... ok
test capture::task_complete::exact_human_output_for_strike_move_dedupe_and_done ... ok
test highlights::create::landing_companion_beside_source_is_copied ... ok
test highlights::jobs::ref_jobs_run_uses_job_bob_dir_not_env ... ok
test highlights::create::highlights_create_folded_forwards_overrides_and_html ... ok
test highlights::listen::listen_post_listen_collision_keeps_scratch ... ok
test highlights::listen::listen_attaches_for_legacy_url_arxiv_note ... ok
test highlights::create::highlights_create_local_pdf_recapture_refuses_then_overwrites ... ok
test highlights::listen::listen_attaches_to_ref_note_capture ... ok
test highlights::listen::listen_without_audio_is_an_error ... ok
test highlights::marker::highlights_ref_marker_uses_first_page_text_annotation ... ok
test highlights::create::highlights_create_folded_doctor_reports_web_clip_rows ... ok
test highlights::marker::highlights_ref_deleted_highlight_is_tombstoned ... ok
test highlights::jobs::ref_jobs_run_falls_back_into_the_staged_parent ... ok
test highlights::jobs::ref_jobs_run_parentless_job_uses_the_source_inbox ... ok
test highlights::jobs::ref_jobs_run_falls_back_on_blocked ... ok
test highlights::marker::highlights_ref_frontmatter_missing_parent_fails_before_pdf_writeback ... ok
test help::vault_sync_help_is_native_only_and_defaults_to_run ... ok
test highlights::marker::highlights_ref_comment_edit_keeps_stable_block_id ... ok
test highlights::marker::highlights_ref_frontmatter_unsupported_status_fails_before_pdf_writeback ... ok
test highlights::marker::highlights_ref_short_options_are_accepted ... ok
test highlights::scan::highlights_ref_scan_detects_same_target_collision_before_writing ... ok
test highlights::marker::highlights_ref_rejects_wikilink_marker_parent_before_writes ... ok
test highlights::marker::highlights_ref_marker_edit_updates_frontmatter ... ok
test highlights::scan::highlights_ref_scan_dry_run_previews_xlib_intake_without_writes ... ok
test highlights::scan::highlights_ref_scan_dry_run_reports_valid_and_invalid_pdfs ... ok
test highlights::scan::highlights_ref_scan_default_output_reports_inline_errors ... ok
test highlights::scan::highlights_ref_scan_refuses_audio_destination_conflict ... ok
test highlights::marker::highlights_ref_doctor_warns_on_missing_latex_packages ... ok
test highlights::listen::create_listen_captures_and_binds_episode ... ok
test highlights::create::highlights_create_folded_supports_ref_type_output_and_name ... ok
test highlights::listen::listen_refusal_without_flag_points_at_listen ... ok
test highlights::jobs::ref_jobs_run_clips_a_seeded_article ... ok
test highlights::jobs::ref_jobs_fallback_bytes_match_capture_twin_vault ... ok
test highlights::scan::highlights_ref_scan_refuses_xlib_intake_conflict_before_writes ... ok
test highlights::scan::ref_scan_human_scan_busy_when_writer_lock_held ... ok
test highlights::listen::listen_attaches_when_target_is_the_library_pdf ... ok
test highlights::listen::listen_attaches_to_queued_intake_pdf ... ok
test highlights::listen::create_article_listen_uses_adapter_render ... ok
test highlights::scan::highlights_ref_scan_treats_later_page_note_as_missing_marker ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_pdf_and_writes_note_in_same_run ... ok
test highlights::scan::ref_scan_json_dry_run_ignores_writer_lock ... ok
test highlights::scan::ref_scan_json_scan_busy_when_writer_lock_held ... ok
test highlights::scan::ref_scan_json_dry_run_plans_intake_without_writing ... ok
test highlights::listen::listen_markdown_binds_episode_and_play_uri ... ok
test highlights::scan_hooks::highlights_ref_scan_dry_run_reports_env_pre_scan_without_executing ... ok
test highlights::scan_hooks::highlights_ref_scan_fails_when_pre_scan_hook_fails ... ok
test highlights::doctor_library::doctor_annotations_warn_on_leaked_marker_mirror ... ok
test highlights::doctor_library::doctor_coverage_warn_counts_unmirrored_zorg_records ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_command_key ... ok
test highlights::listen::listen_legacy_only_hit_captures_fresh_instead_of_attaching ... ok
test highlights::scan_hooks::highlights_ref_scan_rejects_legacy_pre_scan_env ... ok
test highlights::scan::highlights_ref_scan_writes_valid_pdfs_despite_invalid_pdf ... ok
test highlights::listen::listen_pdf_url_streams_output_and_quotes_title ... ok
test help::public_help_surfaces_do_not_list_long_only_options ... ok
test highlights::doctor_library::doctor_coverage_uses_provenance_mirroring ... ok
test highlights::doctor_library::doctor_identity_warn_on_identity_shared_by_two_pdfs ... ok
test highlights::scan::highlights_ref_scan_jobs_flag_matches_sequential_output ... ok
test highlights::scan::ref_scan_json_partial_failure_reports_pdf_stage_and_message ... ok
test highlights::doctor_library::doctor_library_rows_report_ok_on_clean_vault ... ok
test highlights::doctor_library::doctor_library_diagnostics_warn_lists_codes_and_paths ... ok
test highlights::scan_hooks::highlights_ref_scan_empty_env_disables_configured_pre_scan ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_after_subcommand_skips_configured_hook ... ok
test highlights::scan_hooks::ref_scan_json_hook_failure_error_envelope ... ok
test highlights::scan_integration::v2_adoption_reports_neither_created_nor_updated ... ok
test highlights::scan::highlights_ref_scan_round_trips_provenance_marker_fields ... ok
test highlights::doctor_library::doctor_identity_ok_reports_superseded_legacy_note ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_overrides_env_hook ... ok
test highlights::scan_hooks::highlights_ref_scan_hook_child_sees_in_hook_marker ... ok
test highlights::scan::highlights_ref_scan_continues_after_write_failure ... ok
test highlights::scan_integration::v2_dry_run_writes_nothing ... ok
test highlights::scan::highlights_ref_scan_allows_duplicate_basenames_in_different_ref_types ... ok
test highlights::scan_hooks::highlights_ref_scan_no_hooks_before_subcommand_skips_configured_hook ... ok
test highlights::marker::highlights_ref_non_overlapping_edits_auto_merge_and_settle ... ok
test highlights::scan::highlights_ref_scan_intakes_pdf_and_mp3_and_embeds_player ... ok
test highlights::scan_integration::v2_concise_scan_flags_open_v1_with_migrate_hint ... ok
test highlights::jobs::ref_jobs_stale_running_once_is_requeued_and_clipped ... ok
test highlights::marker::highlights_ref_frontmatter_edit_updates_marker_when_pdf_writes_enabled ... ok
test highlights::scan_hooks::ref_scan_json_hook_stdout_reaches_stderr_not_stdout ... ok
test highlights::scan_integration::v2_orphan_recovery_adopts_existing_task ... ok
test highlights::marker::highlights_ref_deprecated_done_status_migrates_to_read_with_pdf_write ... ok
test highlights::scan_hooks::highlights_ref_scan_runs_configured_pre_scan_before_xlib_intake ... ok
test highlights::scan::highlights_ref_scan_intakes_xlib_sidecars_with_pdfs ... ok
test highlights::scan::highlights_ref_scan_late_pairs_audio_onto_existing_note ... ok
test highlights::scan_integration::v2_fallback_parent_uses_inbox_with_warning ... ok
test highlights::marker::highlights_ref_conflicting_edits_fail_and_prefer_frontmatter_resolves ... ok
test highlights::sync::highlights_ref_sync_dry_run_reads_literal_marker_newlines ... ok
test highlights::scan_integration::v2_parallel_matches_sequential ... ok
test highlights::scan_integration::v2_birth_without_tasks_heading_creates_section ... ok
test highlights::scan_integration::v2_alias_parent_resolves_to_canonical_residence ... ok
test highlights::scan_integration::v2_destination_collision_suffixes_preview_id ... ok
test highlights::scan::ref_scan_json_dirty_targets_error_envelope ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_parent_without_note_write ... ok
test highlights::sync::highlights_ref_sync_rejects_missing_marker_status_without_note_write ... ok
test highlights::marker::highlights_ref_doctor_no_hooks_reports_skipped ... ok
test highlights::marker::highlights_ref_doctor_reports_configured_pre_scan_executable ... ok
test highlights::sync::highlights_ref_sync_rejects_unsupported_marker_status_without_note_write ... ok
test highlights::scan_integration::v2_ambiguity_leaves_bytes_unchanged_with_pdf_writes ... ok
test highlights::scan::ref_scan_json_success_envelope_names_created_and_updated_notes ... ok
test highlights::scan_integration::v2_birth_honors_configured_ref_dir ... ok
test highlights::scan::highlights_ref_scan_recurses_dry_runs_and_writes_multiple_pdfs ... ok
test highlights::scan_integration::v2_json_scan_reports_births_without_human_lines ... ok
test highlights::marker::highlights_ref_doctor_warns_on_orphan_companion_audio ... ok
test highlights::sync_tasks::highlights_ref_sync_missing_routed_target_fails_before_writes ... ok
test capture::pomodoro_name::capture_pomodoro_link_solo_grammar_and_atomic_execution ... ok
test highlights::marker::highlights_ref_doctor_checks_vault_git_without_writes ... ok
test highlights::sync::highlights_ref_sync_rejects_malformed_and_duplicate_marker_lists ... ok
test highlights::sync::highlights_ref_sync_preserves_legacy_research_frontmatter ... ok
test highlights::marker::highlights_ref_dry_run_and_inspection_do_not_modify_vault_files ... ok
test highlights::scan::ref_scan_json_intake_lists_pdf_only_when_audio_moves_alone ... ok
test highlights::scan_integration::v2_deleted_managed_embed_heals_without_new_task ... ok
test highlights::jobs::ref_jobs_doctor_row_tracks_pending_and_stuck ... ok
test help::help_routes_match_direct_help_for_root_and_nested_commands ... ok
test highlights::sync_tasks::highlights_ref_sync_creates_tasks_from_pdf_note_task_bullets ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_sidecar_highlights_and_notes ... ok
test highlights::scan_integration::v2_single_pdf_report_names_performed_reading_write ... ok
test highlights::sync_tasks::highlights_ref_sync_supports_linked_sidecar_style ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_vault_scan_when_no_annotation_candidates ... ok
test highlights::sync_tasks::highlights_ref_sync_beautifies_linked_sidecar_rendering ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_legacy_highlight_task_property ... ok
test highlights::scan_integration::v2_sidecar_free_birth_pins_created_date ... ok
test highlights::scan_integration::v2_multiple_open_tasks_refuse_replacement ... ok
test highlights::scan_integration::v2_missing_task_never_gains_automatic_replacement ... ok
test highlights::url_routing::url_routing_in_library_matches_create_refusal ... ok
test highlights::url_routing::url_routing_legacy_matches_create_warning ... ok
test highlights::url_routing::url_routing_in_intake_matches_create_refusal ... ok
test highlights::scan::highlights_ref_scan_stamps_created_on_category_and_intake_notes ... ok
test highlights::scan_integration::v2_moved_task_residence_heals_embed ... ok
test dataview_oom::flatten_later_limit_does_not_hide_default_budget ... ok
test highlights::sync_tasks::highlights_ref_sync_keeps_created_fixed_across_sidecar_updates ... ok
test move_done::move_done_tasks_moves_canceled_tasks_in_non_repo_vault ... ok
test highlights::scan_integration::v2_parent_move_settles_without_pdf_opt_in ... ok
test highlights::sync::highlights_ref_sync_stamps_cancellation_date_when_it_cancels_ref_task ... ok
test highlights::scan_integration::v2_failed_pdf_does_not_consume_sibling_follow_up ... ok
test capture::sub_bullet::capture_sub_bullet_lands_before_direct_managed_logs ... ok
test highlights::scan_integration::v2_archive_reopen_inserts_fresh_task_with_suffixed_id ... ok
test highlights::sync_tasks::highlights_ref_sync_preserves_manual_sections_and_rejects_missing_markers ... ok
test highlights::sync::highlights_ref_sync_preserves_authored_created_and_rejects_marker_created ... ok
test highlights::sync_tasks::highlights_ref_sync_drops_leaked_mirror_without_tombstone ... ok
test highlights::tasks::highlights_ref_task_cancelled_competing_status_edits_fail ... ok
test highlights::tasks::highlights_ref_task_checked_competing_status_edits_fail ... ok
test highlights::sync::highlights_ref_sync_sets_created_timestamp_on_new_sidecar_free_note ... ok
test move_done::move_done_tasks_warns_and_skips_git_for_non_repo_vault ... ok
test highlights::sync::highlights_ref_sync_creates_note_frontmatter_from_marker_pdf_note ... ok
test plan::plan_help_lists_options_alphabetically ... ok
test move_done::move_done_tasks_rewrites_stayed_pathless_links_in_archive ... ok
test highlights::scan::highlights_ref_scan_default_output_is_concise ... ok
test plan::plan_placeholder_only_section_shows_daily_file ... ok
test highlights::scan::highlights_ref_scan_groups_routed_tasks_with_parallel_jobs ... ok
test highlights::scan_integration::v2_archive_move_dedups_follow_up ... ok
test plan::plan_loads_a_config_that_still_has_max_now ... ok
test highlights::scan_integration::v2_opt_in_refreshes_stale_marker_hint ... ok
test plan::plan_reports_lane_over_cap_without_changing_status ... ok
test plan::plan_reports_full_budget_as_json ... ok
test plan::plan_reports_human_budget_without_ansi_when_piped ... ok
test highlights::scan_integration::v2_same_stem_in_two_categories_stays_distinct ... ok
test plan::plan_counts_only_visible_lane_tasks ... ok
test plan::plan_rejects_invalid_config_with_exit_2 ... ok
test plan::plan_without_pomodoros_section_still_shows_lanes ... ok
test highlights::listen::doctor_listen_rows_cover_unset_ok_and_invalid ... ok
test plan::plan_reports_over_cap_with_lints ... ok
test highlights::sync::highlights_ref_sync_refuses_dirty_target_note_before_writing ... ok
test highlights::scan_integration::v2_lifecycle_needs_opt_in_and_settles_on_rerun ... ok
test highlights::scan_integration::v2_dirty_parent_accepts_default_follow_up ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_creations ... ok
test plugins::plugins_default_subcommand_runs_list ... ok
test plugins::plugins_list_unreadable_repo_reports_error ... ok
test plugins::plugins_list_renders_table_and_summary ... ok
test pomodoro::pomodoro_formats_native_pomodoro_status ... ok
test pomodoro::pomodoro_missing_day_file_is_a_successful_noop ... ok
test plan::plan_without_daily_note_still_shows_today_zero_and_lanes ... ok
test pomodoro::pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test plugins::plugins_sync_dry_run_json_writes_nothing ... ok
test plugins::plugins_list_json_is_machine_readable ... ok
test plugins::plugins_sync_dry_run_reports_without_writing ... ok
test plugins::plugins_sync_json_reports_errors_as_object ... ok
test pomodoro::tmux_pomodoro_omits_meter_without_pomodoros_section ... ok
test pomodoro::tmux_pomodoro_appends_named_budget_meter ... ok
test pomodoro::tmux_pomodoro_formats_native_pomodoro_status ... ok
test pomodoro::tmux_pomodoro_reverses_over_cap_meter ... ok
test pomodoro::pomodoro_accepts_legacy_unbolded_inline_duration_field_in_time_range ... ok
test plugins::plugins_sync_backs_up_overwritten_file ... ok
test plugins::plugins_sync_preserves_runtime_data_json ... ok
test plugins::plugins_sync_single_plugin_copies_only_that_plugin ... ok
test projects::list::projects_list_reports_prj_errors_without_aborting_scan ... ok
test plugins::plugins_sync_json_reports_file_actions ... ok
test highlights::tasks::highlights_ref_task_cancelled_scan_write_pdfs_writes_pdf_marker ... ok
test highlights::tasks::highlights_ref_task_checked_scan_creates_annotation_tasks_before_closing ... ok
test projects::list::projects_list_scans_project_notes_and_renders_counts ... ok
test highlights::url_routing::url_routing_doctor_prints_routing_row ... ok
test projects::schedule::projects_sync_shows_sole_prj_task_when_schedule_is_due ... ok
test highlights::sync_tasks::highlights_ref_sync_renders_textbundle_image_selections ... ok
test projects::schedule::projects_schedule_errors_are_per_file_and_leave_invalid_file_untouched ... ok
test projects::sync::projects_sync_marks_canceled_subproject_same_run ... ok
test highlights::scan_integration::v2_concise_scan_reports_reading_task_updates ... ok
test projects::schedule::projects_sync_surfaces_due_scheduled_project_with_only_closed_tasks ... ok
test highlights::sync_tasks::highlights_ref_sync_routes_annotation_tasks_to_existing_root_note ... ok
test projects::schedule::projects_sync_propagates_scheduled_task_properties_at_date_boundary ... ok
test projects::sync::projects_sync_subproject_line_dry_run_reports_without_writing ... ok
test pomodoro::script_pomodoro_reads_default_bare_daily_file_from_bob_dir ... ok
test pomodoro::script_pomodoro_accepts_inline_duration_field_in_time_range ... ok
test highlights::tasks::highlights_ref_task_cancelled_dry_run_requires_and_writes_pdf_marker ... ok
test pomodoro::pomodoro_show_stale_keeps_no_open_day_empty ... ok
test pomodoro::script_pomodoro_accepts_legacy_unbolded_time_range ... ok
test projects::sync::projects_sync_preserves_user_sub_bullets_and_inserts_subprojects_line ... ok
test projects::sync::projects_sync_normalizes_mangled_subprojects_line ... ok
test projects::sync::projects_sync_keeps_pruned_closed_entries_gone ... ok
test projects::sync::projects_sync_reports_prj_errors_without_aborting_scan ... ok
test projects::sync::projects_sync_treats_children_without_open_prj_as_childless ... ok
test ready::ready_help_documents_usage_options_and_environment ... ok
test highlights::tasks::highlights_ref_status_abandoned_rewrites_generated_task_to_cancelled ... ok
test ready::cap_preview_rejects_out_of_range_values ... ok
test projects::sync::projects_sync_unhides_parent_when_child_prj_is_checked_same_run ... ok
test ready::overview_all_clear_reports_room ... ok
test ready::ready_rejects_invalid_config_with_exit_2 ... ok
test projects::sync::projects_sync_reopens_parent_ledger_when_child_prj_is_reopened_same_run ... ok
test projects::sync::projects_sync_orders_open_then_closed_subprojects_in_one_run ... ok
test projects::sync::projects_sync_hides_parent_projects_with_open_subprojects ... ok
test ready::overview_all_expands_room_empty_and_lints ... ok
test ready::overview_json_reports_totals_and_order ... ok
test ready::overview_human_has_sections_order_and_no_ansi ... ok
test ready::cap_preview_replaces_only_the_default ... ok
test ready::worklist_json_carries_tasks_and_also ... ok
test ready::worklist_lists_file_order_with_also_here ... ok
test plugins::plugins_sync_bare_from_resolved_checkout_is_allowed ... ok
test projects::sync::projects_sync_reconciles_future_subproject_markers_at_date_boundary ... ok
test plugins::plugins_sync_refuses_dirty_vault_file_then_forces ... ok
test plugins::plugins_sync_bare_from_unrelated_cwd_is_allowed ... ok
test highlights::tasks::highlights_ref_blocked_task_syncs_as_status_neutral_overlay ... ok
test ref_library::find::find_batch_from_stdin_keeps_order_and_duplicates ... ok
test completion::lifecycle::probe_without_controlling_terminal_via_zpty ... ok
test ref_library::find::find_missing_ref_dir_fails_in_both_formats ... ok
test highlights::tasks::highlights_ref_task_ready_scan_reopens_read_ref_to_ready ... ok
test ref_library::find::find_go_link_keys_stay_opaque ... ok
test move_done::move_done_tasks_commits_link_repairs_with_collection_changes ... ok
test highlights::tasks::highlights_ref_task_checked_dry_run_requires_and_writes_pdf_marker ... ok
test plugins::plugins_sync_explicit_repo_from_foreign_checkout_is_allowed ... ok
test move_done::move_done_tasks_commits_metadata_only_archive_repairs ... ok
test move_done::move_done_tasks_rewrites_dirty_candidate_files ... ok
test ref_library::find::find_doi_and_arxiv_doi_queries ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_archive ... ok
test ref_library::find::find_human_blocks_carry_chips_and_footnotes ... ok
test highlights::tasks::highlights_ref_task_checked_dirty_tracked_note_is_allowed ... ok
test projects::sync::projects_sync_updates_status_prj_hide_tag_warns_and_is_idempotent ... ok
test move_done::move_done_tasks_commits_and_pushes_collection_changes_only ... ok
test ref_library::find::find_markdown_table_and_coverage_line ... ok
test ref_library::list::list_git_dates_without_git_warns_and_continues ... ok
test ready::check_exits_3_when_crowded_and_0_when_clear ... ok
test ref_library::find::find_intake_unavailable_without_intake_dir ... ok
test ref_library::find::find_not_found_still_exits_zero ... ok
test ref_library::list::list_missing_ref_dir_fails_like_find ... ok
test ref_library::find::find_path_source_pdf_stem_and_id_queries ... ok
test move_done::move_done_tasks_rewrites_dirty_metadata_only_source ... ok
test ref_library::find::find_pending_sync_marks_status_with_footnote ... ok
test ready::overview_human_always_advertises_task_card_keys ... ok
test ref_library::migrate_zorg::book_folds_lid_and_book_tied_chapters ... ok
test highlights::sync_tasks::highlights_ref_sync_skips_annotation_tasks_for_non_wip_statuses ... ok
test ref_library::migrate_zorg::book_without_chapters_stays_unknown_and_strays_skip ... ok
test ref_library::find::find_www_and_slash_variants_with_superseded_secondary ... ok
test ref_library::find::find_rows_carry_blocked ... ok
test ref_library::migrate_zorg::invariant_note_chapter_skipped_equals_doctor_count ... ok
test move_done::move_done_tasks_commits_metadata_only_source_updates ... ok
test ref_library::find::find_url_variants_share_one_identity ... ok
test ref_library::find::find_conflict_and_unknown_states ... ok
test move_done::move_done_tasks_rewrites_dirty_link_repair_files ... ok
test ref_library::migrate_zorg::shared_block_pair_stays_distinct_under_provenance ... ok
test ref_library::migrate_zorg::stem_collisions_rename_against_vault_and_same_run ... ok
test ref_library::list::list_human_rows_align_dated_and_undated_columns ... ok
test ref_library::migrate_zorg::dry_run_plans_one_plain_record ... ok
test pomodoro::pomodoro_stale_cutoff_is_empty_unless_requested ... ok
test ref_library::list::list_empty_views_say_so ... ok
test move_done::move_done_tasks_deduplicates_archive_block_ids_and_repairs_links ... ok
test ref_library::list::list_markdown_covers_dropped_rows ... ok
test ref_library::migrate_zorg::write_refuses_non_git_vault ... ok
test ref_library::migrate_zorg::multi_url_and_unusable_url_records ... ok
test highlights::tasks::highlights_ref_task_checked_sync_creates_annotation_tasks_before_closing ... ok
test ref_library::find::find_title_exact_and_title_candidates ... ok
test highlights::sync::highlights_ref_sync_allows_dirty_tracked_frontmatter_writeback ... ok
test ready::worklist_rejects_ambiguous_unknown_and_untyped_notes ... ok
test ref_library::show::show_comments_only_without_comments_reports_empty ... ok
test ref_library::find::find_intake_records_both_marker_url_fields ... ok
test ref_library::find::find_intake_hit_with_marker_pdf ... ok
test ref_library::show::show_missing_ref_dir_fails ... ok
test ref_library::list::list_rows_carry_always_present_blocked ... ok
test ref_library::find::find_slug_fallback_for_url_miss ... ok
test highlights::sync::highlights_ref_sync_stamps_completion_date_when_it_closes_ref_task ... ok
test ready::worklist_resolves_paths_stems_and_case ... ok
test ref_library::show::show_counts_preamble_blocks_as_excluded ... ok
test ref_library::list::list_legacy_collapse_versus_status_filter ... ok
test ref_library::find::find_min_score_filters_title_candidates ... ok
test ref_library::show::show_resolves_id_doi_arxiv_and_source_pdf ... ok
test ref_library::show::show_unparsed_region_reports_raw ... ok
test ref_library::show::show_legacy_note_reports_absent_annotations ... ok
test ref_library::show::show_resolves_before_printing_anything ... ok
test ref_library::list::list_hides_superseded_notes_everywhere ... ok
test highlights::scan_integration::v2_two_births_share_one_parent_and_settle ... ok
test ref_library::list::list_git_dates_backfills_modern_notes_only ... ok
test ref_library::list::list_orders_states_era_status_dates_and_titles ... ok
test ref_library::show::show_resolves_every_exact_kind ... ok
test ref_library::show::show_rows_carry_blocked ... ok
test ref_library::list::list_default_view_is_the_queue_in_every_format ... ok
test ref_library::show::show_tasks_own_notes_and_multiline_comments ... ok
test ref_library::show::show_ambiguous_stem_never_picks_first ... ok
test ref_library::list::list_since_filters_by_row_date ... ok
test ref_library::show::show_excludes_mirrors_with_counts ... ok
test ref_library::list::list_unknown_and_conflict_states ... ok
test ref_library::find::find_leaves_the_vault_untouched ... ok
test ref_library::find::find_alias_matches_canonical ... ok
test ref_library::show::show_miss_suggests_title_hints ... ok
test ref_library::find::find_json_envelope_is_stable_and_honest ... ok
test ref_library::list::list_limit_all_and_truncation ... ok
test task_status_hooks::blocked::task_status_hooks_blocked_status_guard_writes_nothing ... ok
test dataview_oom::synthetic_task_census_counts_are_exact ... ok
test ref_library::show::show_markdown_digest_covers_research_and_sections ... ok
test ref_library::show::show_superseded_url_picks_the_live_note_with_also ... ok
test ref_library::show::show_keeps_quotes_comments_images_and_tombstone_counts ... ok
test ref_library::show::show_separates_several_refs_in_order ... ok
test ref_library::migrate_zorg::write_refuses_dirty_zorg_with_nothing_written ... ok
test ref_library::tasks::list_rows_carry_task_parent_status_and_diagnostics ... ok
test dataview_oom::synthetic_task_census_stays_under_address_space_cap ... ok
test ref_library::tasks::git_dates_never_backfills_v2_rows ... ok
test ref_library::tasks::list_parent_resolution_matches_routes_aliases_and_literals ... ok
test task_status_hooks::dependency_lines::reconcile_warns_dependency_cycle_and_keeps_members_blocked ... ok
test ref_library::ref_help_matches_aliases_for_every_verb ... ok
test ref_library::list::list_leaves_the_vault_untouched ... ok
test ref_library::show::show_comments_only_and_no_annotations ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test ref_library::ref_error_paths_match_aliases_for_every_verb ... ok
test ref_library::list::list_filters_or_within_and_across_options ... ok
test task_status_hooks::retry::task_status_hooks_defers_when_maintenance_lock_is_held ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_terminal_failure_and_exit_status ... ok
test ref_library::migrate_zorg::write_blocked_hub_dir_fails_clean_with_nothing_committed ... ok
test ref_library::tasks::show_human_and_json_carry_reading_tasks ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_creates_no_lock_or_recovery ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_ignores_retry_timeout ... ok
test ref_library::show::show_is_read_only ... ok
test task_status_hooks::retry::task_status_hooks_rejects_invalid_retry_timeout ... ok
test task_status_hooks::retry::task_status_hooks_live_noop_may_lock_but_creates_no_recovery ... ok
test plugins::plugins_list_no_pull_uses_existing_checkout ... ok
test dataview_oom::flatten_default_budget_fails_cli_json_and_markdown ... ok
test capture::pomodoro_close_log::capture_pomodoro_close_log_worked_table ... ok
test plugins::plugins_sync_pulls_repo_before_copying ... ok
test plugins::plugins_list_pulls_repo_before_analysis ... ok
test plugins::plugins_list_json_stdout_stays_machine_readable_after_pull ... ok
test ref_library::tasks::doctor_reports_ref_tasks_and_parents_rows ... ok
test plugins::plugins_sync_bare_from_foreign_checkout_refuses_before_pull_or_copy ... ok
test task_status_hooks::structure::task_status_hooks_resolves_archive_references_read_only ... ok
test task_status_hooks::sync::task_status_hooks_nulls_plan_budget_on_invalid_config ... ok
test ref_library::migrate_zorg::write_revert_restores_tree_and_doctor_count ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_unresolved_link_and_breadcrumbs ... ok
test ref_library::migrate_zorg::write_offline_writes_notes_and_commits_only_zorg ... ok
test task_status_hooks::dependency_lines::reconcile_never_writes_previous_daily_target ... ok
test task_status_hooks::dependency_lines::reconcile_skips_closed_dependents ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unadoptable_id_and_keeps_field ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unencodable_target_without_projecting ... ok
test vault_sync::conflict_directory_is_skipped_by_vault_walkers ... ok
test task_status_hooks::structure::task_status_hooks_composes_daily_status_and_structural_edits ... ok
test task_status_hooks::sync::task_status_hooks_reports_grouping_warnings_without_noop_text ... ok
test task_status_hooks::sync::task_status_hooks_reports_plan_budget_in_json_and_human ... ok
test task_status_hooks::structure::task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks::structure::task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test task_status_hooks::structure::task_status_hooks_keeps_archive_out_of_active_dependency_sync ... ok
test vault_sync::renamed_old_top_level_commands_are_unknown ... ok
test task_status_hooks::structure::task_status_hooks_removes_empty_pomodoros_and_reports_them ... ok
test task_status_hooks::structure::task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test ref_library::migrate_zorg::write_sync_sandwich_merges_peer_and_pushes_scoped_commit ... ok
test ref_library::ref_doctor_and_scan_dry_run_match_aliases_on_fixture_vault ... ok
test task_status_hooks::dependency_lines::reconcile_legacy_window_with_line_and_children ... ok
test task_status_hooks::dependency_lines::reconcile_archive_legacy_children_follow_archive_rule ... ok
test task_status_hooks::dependency_lines::reconcile_projection_only_write_defers_in_quiet_interval ... ok
test projects::schedule::projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test vault_sync::vault_sync_concurrent_invocation_exits_zero_silently ... ok
test task_status_hooks::structure::task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test task_status_hooks::structure::task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test vault_sync::executable_stubs_stay_executable_while_other_threads_fork ... ok
test task_status_hooks::structure::task_status_hooks_normalizes_live_archive_terminal_references ... ok
test vault_sync::vault_sync_no_change_cycle_writes_status_without_committing ... ok
test vault_sync::vault_sync_refuses_95_mib_file_before_staging ... ok
test vault_sync::vault_sync_local_only_change_commits_and_pushes ... ok
test vault_sync::nightly_failed_step_still_runs_later_steps_and_exits_nonzero ... ok
test projects::schedule::project_schedule_tasks_flip_between_dash_and_blocked_queries_when_due ... ok
test vault_sync::nightly_runs_vault_sync_move_done_tasks_vault_sync_in_order ... ok
test vault_sync::vault_sync_both_added_file_quarantines_local_copy ... ok
test vault_sync::vault_sync_remote_only_change_fast_forwards ... ok
test task_status_hooks::sync::task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test vault_sync::vault_sync_non_overlapping_edits_merge_cleanly ... ok
test vault_sync::vault_sync_binary_conflict_quarantines_uncorrupted_local_copy ... ok
test task_status_hooks::sync::task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test vault_sync::vault_sync_delete_modify_conflict_keeps_the_file ... ok
test task_status_hooks::retry::task_status_hooks_exhausts_retry_budget_and_still_fails ... ok
test vault_sync::vault_sync_same_line_edit_quarantines_local_copy_and_keeps_remote ... ok
test vault_sync::vault_sync_recovers_interrupted_merge_and_finishes_cycle ... ok
test vault_sync::vault_sync_push_race_retries_and_succeeds ... ok
test task_status_hooks::sync::task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_retry_and_final_result ... ok
test task_status_hooks::retry::task_status_hooks_json_retry_progress_stays_off_stdout ... ok
test task_status_hooks::sync::task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test task_status_hooks::retry::task_status_hooks_human_retry_progress_goes_to_stdout ... ok
test capture::pomodoro_close::capture_pomodoro_close_links_batches_and_files ... ok
test aliases::reconcile_aliases_match_canonical_dry_run_json_and_live_write ... ok
test task_status_hooks::blocked::task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test task_status_hooks::dependency_lines::reconcile_breadcrumb_heals_when_target_returns ... ok
test task_status_hooks::dependency_lines::reconcile_daily_note_keeps_adoption_and_stamp ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw1_inserts_adopted_line_before_schedule_log ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw2_inserts_adopted_line_after_cancel_log ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test task_status_hooks::blocked::task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test task_status_hooks::dependency_line_writes::summary_reports_dependency_counts ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_deletes_line_and_field ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_with_adoptable_id_deletes_line_and_field ... ok
test task_status_hooks::dependency_lines::reconcile_adopts_field_ids_into_canonical_line ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw3_dw6_rewrite_keeps_link_order ... ok
test highlights::create::highlights_create_reports_paired_links_and_dead_warnings_when_available ... ok
test task_status_hooks::dependency_lines::reconcile_drops_stale_field_id ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test task_status_hooks::dependency_lines::reconcile_heals_moved_link ... ok
test task_status_hooks::dependency_lines::reconcile_dependency_chain_settles_in_one_run ... ok
test task_status_hooks::dependency_lines::reconcile_canonicalizes_legacy_line_variants ... ok
test task_status_hooks::dependency_lines::reconcile_field_writer_handles_trailing_tags ... ok
test task_status_hooks::dependency_lines::reconcile_removes_empty_line_and_leaves_malformed_alone ... ok
test task_status_hooks::dependency_lines::reconcile_same_index_insert_does_not_clobber_replace ... ok
test task_status_hooks::dependency_lines::reconcile_projects_line_into_field_and_stamps_target_id ... ok
test highlights::create::highlights_create_output_renders_pdf_at_requested_path_when_available ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test task_status_hooks::dependency_lines::reconcile_warns_non_task_and_self_links_without_projecting ... ok
test highlights::create::highlights_create_renders_pdf_with_outline_and_marker_when_available ... ok
test task_status_hooks::dependency_lines::reconcile_stamps_cross_note_target_id ... ok
test capture::pomodoro_close_selection::capture_pomodoro_close_short_alias_equivalence ... ok
test completion::zsh_adapter::real_zsh_first_tab_completes ... ok
test highlights::jobs::ref_jobs_slow_clip_still_drains_a_late_job ... ok
test task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses ... ok
test highlights::create::highlights_create_stamps_return_links_marker_only_when_links_paired ... ok
test completion::bash::bash_readline_inserts_what_bob_returned ... ok

test result: ok. 1324 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 23.35s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/dataview_parity-bc4164a938267aab)

running 27 tests
test dataview_live_obsidian_parity_harness_compares_supported_native_cases ... ok
test dataview_parity_fixture_vault_covers_contract_surface ... ok
test dataview_obsidian_calendar_markdown_golden_fails_cleanly ... ok
test dataview_obsidian_paths_goldens_cover_grouped_and_flattened_warnings ... ok
test dataview_obsidian_markdown_goldens_cover_supported_exports ... ok
test dataview_obsidian_dql_json_goldens_cover_result_shapes ... ok
test dataview_native_index_skips_hidden_directories ... ok
test dataview_native_dql_from_accepts_source_expressions ... ok
test dataview_native_current_paths_golden_uses_fixture_vault ... ok
test dataview_obsidian_source_goldens_cover_source_expression_contract ... ok
test dataview_native_expression_core_supports_swizzling_and_lambdas ... ok
test dataview_native_current_json_golden_uses_bob_wrapper_shape ... ok
test dataview_native_index_values_cover_yaml_inline_dates_and_links ... ok
test dataview_native_calendar_markdown_fails_cleanly ... ok
test dataview_native_dql_from_ref_prefers_folder_when_note_also_exists ... ok
test dataview_native_function_library_supports_numeric_and_container_functions ... ok
test dataview_native_index_builds_task_and_list_objects ... ok
test dataview_native_function_library_supports_string_functions ... ok
test dataview_native_function_library_supports_constructors_and_utilities ... ok
test dataview_native_function_library_works_in_where_sort_and_list ... ok
test dataview_native_expression_core_evaluates_table_and_list_values ... ok
test dataview_native_index_builds_file_metadata_and_link_graph ... ok
test dataview_native_expression_core_supports_this_comparison_and_sorting ... ok
test dataview_native_markdown_goldens_cover_supported_exports ... ok
test dataview_native_dql_execution_supports_phase6_result_shapes ... ok
test dataview_native_source_expressions_match_fixture_goldens ... ok
test dataview_native_source_smoke_handles_generated_vault_with_many_lists ... ok

test result: ok. 27 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 1.36s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/gkeep_adapter-99fae548c0b85081)

running 6 tests
test note_builder_shapes_a_keep_note ... ok
test fake_adapter_serves_ping_and_records_the_call ... ok
test fake_adapter_prefers_nth_responses ... ok
test fake_adapter_exit_is_a_crash_without_output ... ok
test fake_adapter_serves_errors_and_exchange ... ok
test fake_adapter_honors_sleep ... ok

test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.21s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/gkeep_auth-406652d0273f91d8)

running 11 tests
test login_preflight_failure_leaves_the_cookie_unconsumed ... ok
test login_missing_email_is_a_setup_error ... ok
test doctor_cookie_token_fails_and_keep_skips ... ok
test doctor_adapter_crash_skips_keep ... ok
test doctor_json_reports_the_check_shape ... ok
test login_email_override_wins_and_warns_on_cookie_shape ... ok
test doctor_missing_target_fails ... ok
test login_via_stdin_exchanges_stores_and_verifies ... ok
test doctor_all_ok_reports_the_checklist ... ok
test login_store_failure_writes_a_recovery_file ... ok
test login_readback_mismatch_writes_a_recovery_file ... ok

test result: ok. 11 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.06s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/gkeep_cli-c54800693a46802b)

running 6 tests
test top_help_pins_the_command_surface ... ok
test usage_errors_exit_2 ... ok
test top_level_options_match_list_and_default_to_list ... ok
test default_command_note_appears_exactly_once_in_short_and_long_help ... ok
test subcommand_help_blocks_carry_examples_and_environment ... ok
test subcommand_options_are_alphabetical ... ok

test result: ok. 6 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.02s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/gkeep_list-cec82f0109176e7d)

running 19 tests
test all_with_no_tasks_prints_no_tasks ... ok
test vault_source_needs_no_config_or_adapter ... ok
test missing_target_prints_exact_line ... ok
test vault_rows_sort_oldest_first_with_missing_last ... ok
test keep_age_is_correct_outside_utc ... ok
test dst_gap_reports_45m_not_now ... ok
test ages_follow_bob_now ... ok
test json_output_has_schema_version_and_sections ... ok
test output_is_plain_when_piped ... ok
test default_subcommand_is_list ... ok
test keep_source_omits_the_vault_section ... ok
test url_only_note_shows_parent_hint_for_resolved_and_asks_routes ... ok
test keep_auth_error_still_shows_the_vault ... ok
test url_only_note_shows_ref_hint_and_json_verdict ... ok
test all_shows_archived_notes_and_done_tasks ... ok
test duplicate_markers_warn_on_stderr ... ok
test footer_covers_the_clear_and_actionable_cases ... ok
test each_state_is_rendered ... ok
test still_in_keep_covers_pinned_shared_and_empty ... ok

test result: ok. 19 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.08s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/gkeep_pull-51135638064ecdd0)

running 40 tests
test pull_lock_contention_exits_1 ... ok
test missing_target_reports_before_vault_lock ... ok
test dry_run_with_lock_held_still_succeeds ... ok
test dry_run_previews_ref_without_clipping ... ok
test dry_run_json_reports_unwritten ... ok
test snapshot_auth_error_writes_nothing ... ok
test retryable_clip_failure_needs_no_target ... ok
test url_only_matrix_classifies_without_clipping ... ok
test retryable_clip_failure_stays_in_keep_and_fails ... ok
test keep_parent_precedence_note_route_cli_alias_and_fallback ... ok
test target_missing_and_unknown_or_ambiguous_ids_exit_2 ... ok
test dry_run_no_archive_reports_not_requested ... ok
test double_modification_abort_keeps_exact_bytes ... ok
test already_in_library_archives_without_fetch ... ok
test non_git_vault_writes_without_commit_and_json_shape ... ok
test no_ref_flag_keeps_url_as_task ... ok
test empty_snapshot_second_pull_reports_nothing ... ok
test crlf_endings_preserved_and_space_indent_used ... ok
test normal_pull_writes_verifies_commits_and_archives ... ok
test dry_run_previews_exact_markdown_without_writing_or_archiving ... ok
test all_clip_pull_needs_no_target ... ok
test dry_run_markdown_equals_real_run ... ok
test quiet_verify_failure_reports_once_with_empty_stdout ... ok
test target_race_once_replans_and_succeeds ... ok
test no_archive_writes_but_leaves_notes_then_next_pull_archives_only ... ok
test archive_only_pull_reports_no_failure ... ok
test quiet_success_is_silent_and_target_race_aborts ... ok
test archive_changed_after_clip_reports_and_keeps_journal ... ok
test ref_created_repull_needs_no_target ... ok
test crash_after_commit_before_archive_recovers_as_pending ... ok
test archive_crash_reports_once_in_both_modes ... ok
test second_pull_after_success_is_archive_only_with_no_duplicate_write ... ok
test limit_and_explicit_pinned_selection ... ok
test url_only_pdf_note_clips_and_archives_without_task ... ok
test permanent_clip_failure_writes_task_with_warning ... ok
test archive_failure_json_keeps_markdown_and_reports ... ok
test second_note_with_same_url_reports_already_queued ... ok
test archive_changed_reports_and_next_pull_writes_revision ... ok
test archive_missing_error_and_crash_keep_the_committed_vault ... ok
test create_ref_fallback_verify_failure_counts_as_failed ... ok

test result: ok. 40 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.52s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/randomize-77dd7db86679ea99)

running 15 tests
test randomize_help_lists_options_alphabetically ... ok
test randomize_dry_run_writes_nothing_and_prints_replay ... ok
test randomize_needs_a_look_skips_are_reported ... ok
test randomize_date_bounds_reject_unrepresentable_offsets_and_windows ... ok
test randomize_nothing_due_missing_config ... ok
test randomize_unreachable_remote_fails_presync_with_offline_hint ... ok
test randomize_held_lock_fails_fast_with_no_writes ... ok
test randomize_hooks_parity_after_live_run ... ok
test randomize_non_git_vault_warns_and_writes ... ok
test randomize_live_offline_rewrites_notes_with_status_log_and_grouping ... ok
test randomize_json_contract_keys_and_failure_shape ... ok
test randomize_seed_replays_dry_run_dates_filters_levels_and_until ... ok
test randomize_offline_commits_without_pushing ... ok
test randomize_bare_remote_syncs_scoped_commit_and_push ... ok
test randomize_post_sync_conflict_keeps_local_commit_and_warns ... ok

test result: ok. 15 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.47s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/tasks_parity-7c0ba51307cedfd3)

running 32 tests
test tasks_live_obsidian_parity_harness_renders_and_scrapes_tasks_blocks ... ok
test tasks_parity_fixture_vault_covers_phase1_contract ... ok
test path_qualified_dependency_ids_keep_duplicate_block_fragments_distinct ... ok
test tasks_native_filterless_paths_golden_includes_underscore_folders ... ok
test hide_tags_only_removes_recognized_task_tags ... ok
test tasks_plugin_emoji_setting_selects_emoji_metadata_parser ... ok
test tasks_native_filterless_json_golden_reads_settings_and_tasks ... ok
test tasks_by_function_exposes_tasks_query_context_and_real_moment_dates ... ok
test tasks_query_parser_accepts_the_daily_note_query_surface ... ok
test tasks_native_dashboard_defaults_run_function_filters_with_pinned_moment ... ok
test tasks_query_parser_composes_dash_defaults_and_serializes_the_ast ... ok
test sort_by_function_evaluates_each_task_key_once ... ok
test tasks_by_function_runs_dash_filters_and_stacked_sorts ... ok
test blocked_note_includes_dependency_and_future_scheduled_status_reasons ... ok
test tasks_settings_have_stable_defaults_when_plugin_data_is_absent ... ok
test tasks_cli_rejects_invalid_combinations_and_unsupported_surface ... ok
test tasks_note_reports_the_failing_block_context ... ok
test tasks_markdown_honors_tree_layout_fields_counts_and_explain ... ok
test tasks_javascript_exposes_priority_digits_and_pins_all_moment_clocks ... ok
test tasks_result_pipeline_sorts_groups_and_limits_like_tasks_v8 ... ok
test tasks_note_rejects_status_symbol_but_function_filter_selects_next ... ok
test tasks_group_by_function_reports_array_keys_and_runtime_errors ... ok
test tasks_note_identifies_blocks_in_paths_and_markdown_output ... ok
test tasks_note_executes_every_dashboard_block_with_origin_defaults ... ok
test tasks_note_and_origin_normalize_leading_current_directory_components ... ok
test tasks_short_flags_files_stdin_and_comments_reach_filterless_slice ... ok
test tasks_native_boolean_and_implicit_and_filters_match_goldens ... ok
test tasks_group_by_function_keeps_null_empty_array_and_empty_string_tasks ... ok
test tasks_native_date_filters_match_pinned_range_boundaries ... ok
test tasks_native_filter_families_match_fixture_goldens ... ok
test tasks_every_native_sort_and_group_key_executes ... ok
test tasks_by_function_surfaces_parse_return_type_and_sort_errors ... ok

test result: ok. 32 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.22s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws0-261009_123049/build/debug/deps/tasks_real_vault_parity-6c2229232d902624)

running 1 test
test real_vault_dash_matches_independent_raw_ground_truth_and_all_blocks_execute ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

   Doc-tests bob_cli

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

error: 1 target failed:
    `--lib`
error: recipe `check` failed on line 27 with exit code 101
failed  exit=101  duration=141647ms

