# Chat History - ace-run (bob-cli-87.2.1.1--mon-0)

- **TIMESTAMP:** 2026-10-16 07:51:57 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-87.2.1.1--mon-0

## Prompt

sase monitor start --command 'just check' --reason 'Verify the snapshot model-contract phase before closing its assigned bead'

## Response

sase tool run 95a790ccf7730a39d5e863d7e415e4cf

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces
    Checking typenum v1.20.1
    Checking stable_deref_trait v1.2.1
    Checking cfg-if v1.0.4
   Compiling shlex v2.0.1
    Checking equivalent v1.0.2
    Checking foldhash v0.2.0
    Checking allocator-api2 v0.2.21
    Checking memchr v2.8.1
    Checking writeable v0.6.4
    Checking litemap v0.8.3
    Checking utf8_iter v1.0.4
    Checking utf8parse v0.2.2
    Checking smallvec v1.15.2
    Checking rand_core v0.10.1
    Checking tinyvec_macros v0.1.1
    Checking is_terminal_polyfill v1.70.2
    Checking anstyle-query v1.1.5
    Checking bitflags v2.12.1
    Checking colorchoice v1.0.5
    Checking anstyle v1.0.14
    Checking cpufeatures v0.3.0
    Checking itoa v1.0.18
    Checking simd-adler32 v0.3.9
    Checking adler2 v2.0.1
    Checking clap_lex v1.1.0
    Checking cpufeatures v0.2.17
    Checking strsim v0.11.1
    Checking percent-encoding v2.3.2
    Checking unicode-properties v0.1.4
    Checking unicode-bidi v0.3.18
    Checking const-oid v0.10.2
    Checking bytecount v0.6.9
    Checking regex-syntax v0.8.10
    Checking ryu v1.0.23
    Checking log v0.4.30
    Checking unsafe-libyaml v0.2.11
    Checking iana-time-zone v0.1.65
    Checking weezl v0.1.12
    Checking is_executable v1.0.6
    Checking rangemap v1.7.1
    Checking ttf-parser v0.25.1
    Checking hex v0.4.3
    Checking similar v2.7.0
    Checking deranged v0.5.8
    Checking time-core v0.1.9
    Checking linux-raw-sys v0.12.1
    Checking libc v0.2.186
    Checking icu_normalizer_data v2.3.0
    Checking icu_properties_data v2.3.0
    Checking serde_core v1.0.228
    Checking zmij v1.0.21
    Checking powerfmt v0.2.0
    Checking num-conv v0.2.2
    Checking fallible-streaming-iterator v0.1.9
    Checking fallible-iterator v0.3.0
    Checking fastrand v2.5.0
    Checking once_cell v1.21.4
    Checking base64 v0.22.1
    Checking num-traits v0.2.19
    Checking zerofrom v0.1.8
    Checking thiserror v2.0.18
    Checking anstyle-parse v1.0.0
    Checking crc32fast v1.5.0
    Checking encoding_rs v0.8.35
    Checking form_urlencoded v1.2.2
    Checking miniz_oxide v0.8.9
    Checking tinyvec v1.11.0
    Checking generic-array v0.14.7
    Checking hybrid-array v0.4.12
    Checking chrono v0.4.44
    Checking hashbrown v0.17.1
   Compiling cc v1.2.63
    Checking yoke v0.8.3
    Checking serde v1.0.228
    Checking getrandom v0.4.2
    Checking fs2 v0.4.3
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking serde_json v1.0.150
    Checking quick-xml v0.41.0
    Checking time v0.3.53
    Checking rustix v1.1.5
    Checking chacha20 v0.10.2
    Checking anstream v1.0.0
    Checking unicode-normalization v0.1.25
    Checking flate2 v1.1.9
    Checking crypto-common v0.2.2
    Checking block-buffer v0.12.0
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking indexmap v2.14.0
    Checking hashlink v0.12.1
    Checking clap_builder v4.6.7
    Checking rand v0.10.1
    Checking regex-automata v0.4.14
    Checking inout v0.1.4
    Checking stringprep v0.1.5
    Checking digest v0.10.7
    Checking digest v0.11.3
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking nom_locate v5.0.0
    Checking tempfile v3.27.0
    Checking serde_yaml v0.9.34+deprecated
    Checking plist v1.10.0
    Checking cipher v0.4.4
    Checking md-5 v0.10.6
    Checking sha2 v0.10.9
    Checking icu_collections v2.3.0
    Checking icu_locale_core v2.3.0
    Checking sha2 v0.11.0
    Checking clap v4.6.7
    Checking cbc v0.1.2
    Checking aes v0.8.4
    Checking ecb v0.1.2
    Checking regex v1.12.3
    Checking clap_complete v4.6.11
    Checking lopdf v0.40.0
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking rusqlite v0.40.1
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_13)
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

error: unused import: `serialize::serialize_projected_markdown`
  --> src/native/highlights_ref/note_snapshot/mod.rs:13:16
   |
13 | pub(crate) use serialize::serialize_projected_markdown;
   |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = note: `-D unused-imports` implied by `-D unused`
   = help: to override `-D unused` add `#[allow(unused_imports)]`

error: unused imports: `AnchorIdentity`, `AssetMediaKind`, `Block`, `ChipKind`, `Chip`, `HeadingClass`, `HeadingLevel`, `Inline`, `LinkTarget`, `ListItem`, `ListKind`, `ParsedSource`, `ParsedTaskLine`, `SnapshotAnchor`, `SnapshotAsset`, `SnapshotHeading`, `SnapshotLinkCounts`, `SnapshotMasthead`, `SnapshotSection`, `SnapshotSummary`, `SnapshotTaskStatus`, `SnapshotTask`, `SnapshotView`, `SnapshotWarningKind`, `SnapshotWarning`, `SourceExtent`, `SourceFrontmatter`, `SourceIdentity`, `SourceIndentation`, `SourceLocation`, and `StatusCount`
  --> src/native/highlights_ref/note_snapshot/mod.rs:15:5
   |
15 |     AnchorIdentity, AssetMediaKind, Block, Chip, ChipKind, HeadingClass,
   |     ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^  ^^^^^  ^^^^  ^^^^^^^^  ^^^^^^^^^^^^
16 |     HeadingLevel, Inline, LinkTarget, ListItem, ListKind, ParsedSource,
   |     ^^^^^^^^^^^^  ^^^^^^  ^^^^^^^^^^  ^^^^^^^^  ^^^^^^^^  ^^^^^^^^^^^^
17 |     ParsedTaskLine, SnapshotAnchor, SnapshotAsset, SnapshotHeading,
   |     ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^
18 |     SnapshotLinkCounts, SnapshotMasthead, SnapshotSection, SnapshotSummary,
   |     ^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^
19 |     SnapshotTask, SnapshotTaskStatus, SnapshotView, SnapshotWarning,
   |     ^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^  ^^^^^^^^^^^^^^^
20 |     SnapshotWarningKind, SourceExtent, SourceFrontmatter, SourceIdentity,
   |     ^^^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^  ^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^
21 |     SourceIndentation, SourceLocation, StatusCount,
   |     ^^^^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^  ^^^^^^^^^^^

warning: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:991:1
     |
 991 | / fn resolve_prerequisites(
 992 | |     ctx: &DependencyContext,
 993 | |     planner: &mut CaptureBatchPlanner,
 994 | |     bob_dir: &Path,
...    |
 999 | |     dependent_desc: &str,
1000 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments
     = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1333:24
     |
1333 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#type_complexity
     = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1956:6
     |
1956 |   ) -> Result<
     |  ______^
1957 | |     (
1958 | |         Vec<MergedMember>,
1959 | |         BTreeSet<(String, String)>,
...    |
1963 | |     CaptureError,
1964 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#type_complexity

warning: this function has too many arguments (9/7)
   --> src/native/capture/output.rs:284:5
    |
284 | /     pub(super) fn from_items(
285 | |         items: Vec<CaptureItemResult>,
286 | |         global_destination: Option<GlobalDestinationSummary>,
287 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
293 | |         pull_in: PullInJson,
294 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
    --> src/native/capture/output.rs:1481:5
     |
1481 | /     if result.kind == "pomodoro_start" {
1482 | |         if let Some(start) = result.pomodoro_start.as_ref() {
1483 | |             print_human_pomodoro_start_success(
1484 | |                 result,
...    |
1494 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
     = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
     |
1481 ~     if result.kind == "pomodoro_start"
1482 ~         && let Some(start) = result.pomodoro_start.as_ref() {
1483 |             print_human_pomodoro_start_success(
 ...
1492 |             return;
1493 ~         }
     |

warning: this function has too many arguments (9/7)
   --> src/native/capture/plan.rs:499:1
    |
499 | / pub(super) fn plan_capture_item(
500 | |     request: &CaptureRequest,
501 | |     parsed_item: ParsedCaptureItem,
502 | |     now: chrono::NaiveDateTime,
...   |
508 | |     dependency_ctx: &mut DependencyContext,
509 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:647:9
    |
647 | /         let Some(relative_close) = line[open..].find(')') else {
648 | |             return None;
649 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: this `match` expression can be replaced with `?`
   --> src/native/capture/pomodoro_adjust.rs:896:19
    |
896 |       let minutes = match minutes_part {
    |  ___________________^
897 | |         Some(part) => {
898 | |             let part = part.trim();
899 | |             let core = part.strip_suffix('m')?;
...   |
909 | |         None => return None,
910 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
896 ~     let minutes = {
897 +         let part = minutes_part?;
898 +         let part = part.trim();
899 +         let core = part.strip_suffix('m')?;
900 +         let core = core.trim_end();
901 +         if core.is_empty() {
902 +             return None;
903 +         }
904 +         if !core.bytes().all(|byte| byte.is_ascii_digit()) {
905 +             return None;
906 +         }
907 +         core.parse::<u64>().ok()?
908 ~     };
    |

warning: manual `rem_euclid` implementation
    --> src/native/capture/pomodoro_adjust.rs:1002:5
     |
1002 |     (((value % 1440) + 1440) % 1440) as u64
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

warning: the borrowed expression implements the required traits
   --> src/native/capture/project_deps.rs:303:42
    |
303 |         None => match fs::read_to_string(&day_absolute) {
    |                                          ^^^^^^^^^^^^^ help: change this to: `day_absolute`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/capture/project_deps.rs:373:23
    |
373 |         .item_pre_day(&day_absolute)
    |                       ^^^^^^^^^^^^^ help: change this to: `day_absolute`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
    = note: `#[warn(clippy::needless_borrow)]` on by default

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

warning: this function has too many arguments (9/7)
   --> src/native/capture_complete/candidates.rs:746:1
    |
746 | / fn relationship_disabled_reason(
747 | |     bob_dir: &Path,
748 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
749 | |     graph: &HashMap<
...   |
758 | |     blocked_tasks: &[ResolvedRelationshipEntry],
759 | | ) -> Option<String> {
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: manual case-insensitive ASCII comparison
   --> src/native/capture_complete/engine.rs:507:12
    |
507 |         || content.to_ascii_lowercase() == "@@template:"
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_ignore_case_cmp
    = note: `#[warn(clippy::manual_ignore_case_cmp)]` on by default
help: consider using `.eq_ignore_ascii_case()` instead
    |
507 -         || content.to_ascii_lowercase() == "@@template:"
507 +         || content.eq_ignore_ascii_case("@@template:")
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

warning: taken reference of right operand
   --> src/native/capture_language/dependencies.rs:657:20
    |
657 |                 if raw.as_bytes() == &[sigil] =>
    |                    ^^^^^^^^^^^^^^^^^^--------
    |                                      |
    |                                      help: use the right value directly: `[sigil]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#op_ref
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#map_identity
    = note: `#[warn(clippy::map_identity)]` on by default

warning: unnecessary map of the identity function
   --> src/native/capture_language/editor_classify.rs:612:60
    |
612 |               let (after_x, x_len) = classify_link_close(raw)
    |  ____________________________________________________________^
613 | |                 .map(|(selection, x_len)| (selection, x_len))
    | |_____________________________________________________________^ help: remove the call to `map`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#map_identity

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:491:1
    |
491 | / pub(super) enum TokenParse {
492 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 352 bytes
493 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
494 | | }
    | |_^ the entire enum is at least 352 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
492 -     Marker(MarkerParse),
492 +     Marker(Box<MarkerParse>),
    |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/editor_parse.rs:1069:9
     |
1069 | /         if is_standalone_listen_marker(tokens[1].text) {
1070 | |             if let Some(intent) = classify_token(tokens[0].text) {
1071 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
1072 | |                     return None;
...    |
1116 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1069 ~         if is_standalone_listen_marker(tokens[1].text)
1070 ~             && let Some(intent) = classify_token(tokens[0].text) {
1071 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
 ...
1114 |                 });
1115 ~             }
     |

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/editor_pomodoro.rs:269:1
    |
269 | / pub(super) fn parse_editor_named_start_item<'a>(
270 | |     item: &CaptureItem<'a>,
271 | |     parent_trimmed: &str,
272 | |     suffix: String,
...   |
277 | |     override_token: bool,
278 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/editor_pomodoro.rs:969:1
    |
969 | / pub(super) fn parse_editor_start_item<'a>(
970 | |     item: &CaptureItem<'a>,
971 | |     parent_trimmed: &str,
972 | |     suffix: String,
...   |
977 | |     override_token: bool,
978 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:1990:17
     |
1990 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/capture_language/item.rs:177:9
    |
177 | /         if is_standalone_listen_marker(tokens[1].text) {
178 | |             if let Some(intent) = classify_token(tokens[0].text) {
179 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
180 | |                     return None;
...   |
222 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
177 ~         if is_standalone_listen_marker(tokens[1].text)
178 ~             && let Some(intent) = classify_token(tokens[0].text) {
179 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
...
220 |                 ));
221 ~             }
    |

warning: match expression looks like `matches!` macro
    --> src/native/capture_language/item.rs:1320:31
     |
1320 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
1321 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1322 | |                 (false, '~', Some(b'@')) => true,
1323 | |                 _ => false,
1324 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
1320 -             let want_second = match (name.is_some(), first_sigil, second) {
1321 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1322 -                 (false, '~', Some(b'@')) => true,
1323 -                 _ => false,
1324 -             };
1320 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1698:5
     |
1698 | /     if let Some((_, after_tilde)) = drop {
1699 | |         if lex_start_drop(&after_tilde, 0, nospace)
1700 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1701 | |             == false
...    |
1705 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1698 ~     if let Some((_, after_tilde)) = drop
1699 ~         && lex_start_drop(&after_tilde, 0, nospace)
1700 |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
 ...
1703 |             return false;
1704 ~         }
     |

warning: equality checks against false can be replaced by a negation
    --> src/native/capture_language/item.rs:1699:12
     |
1699 |           if lex_start_drop(&after_tilde, 0, nospace)
     |  ____________^
1700 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1701 | |             == false
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bool_comparison
     = note: `#[warn(clippy::bool_comparison)]` on by default
help: try
     |
1699 ~         if !lex_start_drop(&after_tilde, 0, nospace)
1700 +             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1707:5
     |
1707 | /     if let Some((_, after_at)) = timing {
1708 | |         if parse_pomodoro_start_suffix(&after_at).is_err() {
1709 | |             return false;
1710 | |         }
1711 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1707 ~     if let Some((_, after_at)) = timing
1708 ~         && parse_pomodoro_start_suffix(&after_at).is_err() {
1709 |             return false;
1710 ~         }
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2034:31
     |
2034 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
2034 -                 Err(error) => return Err(error.message),
2034 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2042:21
     |
2042 | /                     return Err(close_inline_dangling_error(
2043 | |                         &head, index, plain,
2044 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
2042 ~                     Err(close_inline_dangling_error(
2043 +                         &head, index, plain,
2044 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2080:21
     |
2080 | /                     return Ok(Some(parsed_capture_item_outcome(
2081 | |                         item,
2082 | |                         ParsedCaptureText {
2083 | |                             body,
...    |
2095 | |                         None,
2096 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
2080 ~                     Ok(Some(parsed_capture_item_outcome(
2081 +                         item,
2082 +                         ParsedCaptureText {
2083 +                             body,
2084 +                             clip: None,
2085 +                             route: None,
2086 +                             kind: CaptureKind::PomodoroClose { spec },
2087 +                             scheduled_offset: None,
2088 +                             priority_level: None,
2089 +                             sub_bullets: Vec::new(),
2090 +                             dependencies: Vec::new(),
2091 +                             blocked_tasks: Vec::new(),
2092 +                             dependency_target: None,
2093 +                         },
2094 +                         Vec::new(),
2095 +                         None,
2096 ~                     )))
     |

warning: this `if` statement can be collapsed
   --> src/native/capture_language/template.rs:121:5
    |
121 | /     if let Some((_, line_number)) = analysis.header.as_ref() {
122 | |         if let Some(line) = lines.get(line_number.saturating_sub(1)) {
123 | |             bytes[line.start..line.end].fill(b' ');
124 | |         }
125 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
121 ~     if let Some((_, line_number)) = analysis.header.as_ref()
122 ~         && let Some(line) = lines.get(line_number.saturating_sub(1)) {
123 |             bytes[line.start..line.end].fill(b' ');
124 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/capture_language/template.rs:327:5
    |
327 | /     if !fields_used.is_empty() {
328 | |         if fields_used.iter().copied().ne(0..field_count) {
329 | |             let missing = (0..field_count)
330 | |                 .find(|index| !fields_used.contains(index))
...   |
361 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
327 ~     if !fields_used.is_empty()
328 ~         && fields_used.iter().copied().ne(0..field_count) {
329 |             let missing = (0..field_count)
...
359 |             ));
360 ~         }
    |

warning: returning the result of a `let` binding from a block
   --> src/native/capture_language/template.rs:346:17
    |
341 | /                 let shown = fields_used
342 | |                     .iter()
343 | |                     .map(|field| format!("{{{field}}}"))
344 | |                     .collect::<Vec<_>>()
345 | |                     .join(" and ");
    | |___________________________________- unnecessary `let` binding
346 |                   shown
    |                   ^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#let_and_return
    = note: `#[warn(clippy::let_and_return)]` on by default
help: return the expression directly
    |
341 ~                 
342 ~                 fields_used
343 +                     .iter()
344 +                     .map(|field| format!("{{{field}}}"))
345 +                     .collect::<Vec<_>>()
346 +                     .join(" and ")
    |

warning: redundant guard
   --> src/native/capture_language/tokens.rs:709:43
    |
709 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_guards
help: try
    |
709 -                 Some((after_x, x_len)) if after_x.is_empty() => {
709 +                 Some(("", x_len)) => {
    |

warning: unnecessary map of the identity function
    --> src/native/capture_language/tokens.rs:1154:59
     |
1154 |       let (after_x, x_len) = classify_link_close(raw_suffix)
     |  ___________________________________________________________^
1155 | |         .map(|(selection, x_len)| (selection, x_len))
     | |_____________________________________________________^ help: remove the call to `map`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#map_identity

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1586:13
     |
1586 | /             return Ok(Some(parsed_capture_item_outcome(
1587 | |                 item,
1588 | |                 ParsedCaptureText {
1589 | |                     body: String::new(),
...    |
1607 | |                 Some(marker_text),
1608 | |             )));
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
1586 ~             Ok(Some(parsed_capture_item_outcome(
1587 +                 item,
1588 +                 ParsedCaptureText {
1589 +                     body: String::new(),
1590 +                     clip: None,
1591 +                     route: Some(route),
1592 +                     kind: CaptureKind::PomodoroLink {
1593 +                         block_id: parts.block_id,
1594 +                         pomodoro_name: parts.pomodoro_name,
1595 +                         start: parts.start,
1596 +                         close: parts.close,
1597 +                         spelling: PomodoroLinkSpelling::Caret,
1598 +                     },
1599 +                     scheduled_offset: None,
1600 +                     priority_level: None,
1601 +                     sub_bullets: Vec::new(),
1602 +                     dependencies: Vec::new(),
1603 +                     blocked_tasks: Vec::new(),
1604 +                     dependency_target: None,
1605 +                 },
1606 +                 Vec::new(),
1607 +                 Some(marker_text),
1608 ~             )))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1669:13
     |
1669 |             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
1669 -             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
1669 +             Err(POMODORO_LINK_SHAPE_ERROR.to_string())
     |

warning: this `match` expression can be replaced with `?`
   --> src/native/capture_link_tasks.rs:296:9
    |
296 | /         match best_field_tier(raw_fields, term) {
297 | |             Some(tier) => total += tier,
298 | |             None => return None,
299 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
296 ~         {
297 +             let tier = best_field_tier(raw_fields, term)?;
298 +             total += tier
299 +         }
    |

warning: this `if` statement can be collapsed
   --> src/native/capture_parse.rs:972:9
    |
972 | /         if let Some(diagnostic) = refusal_diagnostic(
973 | |             &parsed.spans,
974 | |             parsed.mode,
975 | |             &parsed.pomodoro_start,
...   |
983 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
979 ~         )
980 ~             && diagnostic.code != "template_clipboard" {
981 |                 refusal_diagnostics.push(diagnostic);
982 ~             }
    |

warning: redundant closure
   --> src/native/capture_parse.rs:999:29
    |
999 |             .unwrap_or_else(|| empty_wire_item());
    |                             ^^^^^^^^^^^^^^^^^^^^ help: replace the closure with the function itself: `empty_wire_item`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_closure
    = note: `#[warn(clippy::redundant_closure)]` on by default

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_lifetimes
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bind_instead_of_map
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#filter_map_bool_then
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#filter_map_bool_then
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#filter_map_bool_then
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1250 ~         if let Some(url) = source_url.as_deref()
1251 ~             && !supported_keep_url(url) {
1252 |                 skip.get_or_insert_with(|| {
 ...
1255 |                 });
1256 ~             }
     |

warning: this block may be rewritten with the `?` operator
    --> src/native/gkeep/migrate_tasks.rs:1536:12
     |
1536 |       } else if let Some(raw_labels) = tail.strip_prefix(" · 🏷 ") {
     |  ____________^
1537 | |         if let Some(labels) = raw_labels.strip_suffix(" · revised") {
1538 | |             let ambiguous = labels.contains(" · ");
1539 | |             (Some(labels), true, ambiguous)
...    |
1545 | |         return None;
1546 | |     };
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: replace it with
     |
1536 ~     } else {
1537 ~         let raw_labels = tail.strip_prefix(" · 🏷 ")?;
1538 ~         if let Some(labels) = raw_labels.strip_suffix(" · revised") {
1539 ~             let ambiguous = labels.contains(" · ");
1540 +             (Some(labels), true, ambiguous)
1541 +         } else {
1542 ~             let ambiguous = raw_labels.contains(" · ");
1543 +             (Some(raw_labels), false, ambiguous)
1544 +         }
1545 ~     };
     |

warning: derefed type is same as origin
    --> src/native/gkeep/migrate_tasks.rs:1547:8
     |
1547 |       if labels
     |  ________^
1548 | |         .as_deref()
     | |___________________^ help: try: `labels`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_option_as_deref
     = note: `#[warn(clippy::needless_option_as_deref)]` on by default

warning: consider using `sort_by_key`
    --> src/native/gkeep/migrate_tasks.rs:1953:5
     |
1953 |     ordered.sort_by(|left, right| right.start.cmp(&left.start));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_sort_by
     = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
     |
1953 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1953 +     ordered.sort_by_key(|left| std::cmp::Reverse(left.start));
     |

warning: length comparison to zero
    --> src/native/gkeep/migrate_tasks.rs:2282:18
     |
2282 |     let failed = failures.len() > 0;
     |                  ^^^^^^^^^^^^^^^^^^ help: using `!is_empty` is clearer and more explicit: `!failures.is_empty()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#len_zero
     = note: `#[warn(clippy::len_zero)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:393:5
    |
393 | /     if let Some(name) = matches.get_one::<String>("name") {
394 | |         if let Err(error) = super::clip_url::validate_name(name) {
395 | |             let styler = Styler::detect();
396 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
399 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
393 ~     if let Some(name) = matches.get_one::<String>("name")
394 ~         && let Err(error) = super::clip_url::validate_name(name) {
395 |             let styler = Styler::detect();
396 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
397 |             return 1;
398 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:401:5
    |
401 | /     if let Some(ref_type) = &ref_type {
402 | |         if let Err(error) = validate_ref_type(ref_type) {
403 | |             let styler = Styler::detect();
404 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
407 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
401 ~     if let Some(ref_type) = &ref_type
402 ~         && let Err(error) = validate_ref_type(ref_type) {
403 |             let styler = Styler::detect();
404 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
405 |             return 1;
406 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:408:5
    |
408 | /     if let Some(published) = matches.get_one::<String>("published") {
409 | |         if let Err(error) = super::clip_url::validate_published(published) {
410 | |             let styler = Styler::detect();
411 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
414 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
408 ~     if let Some(published) = matches.get_one::<String>("published")
409 ~         && let Err(error) = super::clip_url::validate_published(published) {
410 |             let styler = Styler::detect();
411 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
412 |             return 1;
413 ~         }
    |

warning: this `match` expression can be replaced with `?`
    --> src/native/highlights_ref/create.rs:1026:17
     |
1026 | /                 match companion_mod::copy_audio_for_install(plan.audio.as_ref())
1027 | |                 {
1028 | |                     Ok(created) => created,
1029 | |                     Err(error) => return Err(error),
1030 | |                 }
     | |_________________^ help: try instead: `companion_mod::copy_audio_for_install(plan.audio.as_ref())?`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:1769:1
     |
1769 | / fn print_pdf_dry_run(
1770 | |     config: &Config,
1771 | |     styler: &Styler,
1772 | |     source_display: &str,
...    |
1780 | |     legacy: &[sources_mod::RecordedSource],
1781 | | ) {
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

warning: this `match` expression can be replaced with `?`
   --> src/native/highlights_ref/collection.rs:131:25
    |
131 |       let resolved_name = match collection_name::resolve_collection_name(
    |  _________________________^
132 | |         options.name.as_deref(),
133 | |         output_stem,
134 | |         options.title.as_deref(),
...   |
138 | |         Err(error) => return Err(error),
139 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
131 ~     let resolved_name = collection_name::resolve_collection_name(
132 +         options.name.as_deref(),
133 +         output_stem,
134 +         options.title.as_deref(),
135 +         &urls,
136 ~     )?;
    |

warning: redundant closure
   --> src/native/highlights_ref/collection_name.rs:151:27
    |
151 |         parsed.iter().map(|url| slug_words(url)).collect();
    |                           ^^^^^^^^^^^^^^^^^^^^^ help: replace the closure with the function itself: `slug_words`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_closure

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/highlights_ref/collection_name.rs:156:65
    |
156 |         if is_useful_name(&shared.words, allows_one_word_series(&urls, &parsed))
    |                                                                 ^^^^^ help: change this to: `urls`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: unneeded `return` statement
   --> src/native/highlights_ref/collection_name.rs:214:13
    |
214 |             return Ok(ResolvedName { name, source });
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
    |
214 -             return Ok(ResolvedName { name, source });
214 +             Ok(ResolvedName { name, source })
    |

warning: unneeded `return` statement
   --> src/native/highlights_ref/collection_name.rs:226:13
    |
226 | /             return Err(CommandError::new(name_error_message(urls, &reason))
227 | |                 .with_exit_code(2));
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
    |
226 ~             Err(CommandError::new(name_error_message(urls, &reason))
227 ~                 .with_exit_code(2))
    |

warning: this loop could be written as a `for` loop
   --> src/native/highlights_ref/collection_name.rs:665:5
    |
665 |     while let Some((byte_index, first_char)) = chars.next() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `for (byte_index, first_char) in chars`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#while_let_on_iterator
    = note: `#[warn(clippy::while_let_on_iterator)]` on by default

warning: you should use the `starts_with` method
   --> src/native/highlights_ref/listen.rs:690:23
    |
690 |     if length == 0 || rest[length..].chars().next() != Some('}') {
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: like this: `!rest[length..].starts_with('}')`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chars_next_cmp
    = note: `#[warn(clippy::chars_next_cmp)]` on by default

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/serialize.rs:275:5
    |
275 | /     if let Some(target) = &chip.target {
276 | |         if let Some(destination) = render_target(view, target) {
277 | |             return format!("[{content}]({destination}){{{classes}}}");
278 | |         }
279 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
275 ~     if let Some(target) = &chip.target
276 ~         && let Some(destination) = render_target(view, target) {
277 |             return format!("[{content}]({destination}){{{classes}}}");
278 ~         }
    |

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/note_snapshot/serialize.rs:696:10
    |
696 |           .replace('\n', " ")
    |  __________^
697 | |         .replace('\r', " ")
    | |___________________________^ help: replace with: `replace(['\n', '\r'], " ")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace
    = note: `#[warn(clippy::collapsible_str_replace)]` on by default

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:155:34
    |
155 |                         url.host.replace('.', "_").replace('-', "_"),
    |                                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '-'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: used consecutive `str::replace` call
   --> src/native/highlights_ref/pdf_target.rs:311:33
    |
311 |     format!("arxiv_{}", full_id.replace('.', "_").replace('/', "_"))
    |                                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace with: `replace(['.', '/'], "_")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
913 ~         if let Some((k, _)) = line.split_once(':')
914 ~             && k.trim() == "highlights_marker_hash" {
915 |                 // Preserve quoting style: single-quoted string.
916 |                 out.push(format!("highlights_marker_hash: '{hash}'"));
917 |                 continue;
918 ~             }
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
   --> src/native/projects/scan.rs:226:5
    |
226 | /     let Some(&(line_number, raw_value)) = fields.first() else {
227 | |         return None;
228 | |     };
    | |______^ help: replace it with: `let &(line_number, raw_value) = fields.first()?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
918 -         .last()
918 +         .next_back()
    |

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
410 ~         if let Err(error) = fs::remove_file(path)
411 ~             && error.kind() != std::io::ErrorKind::NotFound {
412 |                 failures.push(format!(
...
415 |                 ));
416 ~             }
    |

warning: redundant reference in `format!` argument
  --> src/native/ref_library/migrate_tasks/line.rs:47:33
   |
47 |         body = format!("{} {}", &body[..open].trim_end(), &body[end..]);
   |                                 ^^^^^^^^^^^^^^^^^^^^^^^^ help: remove the redundant `&`: `body[..open].trim_end()`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#useless_borrows_in_formatting
   = note: `#[warn(clippy::useless_borrows_in_formatting)]` on by default

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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#format_in_format_args
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
740 ~                 .is_some_and(|e| e.eq_ignore_ascii_case("md"))
741 ~                 && let Ok(rel) = path.strip_prefix(bob_dir) {
742 |                     ref_notes.push(rel.to_string_lossy().replace('\\', "/"));
743 ~                 }
    |

warning: you seem to want to iterate on a map's keys
   --> src/native/ref_library/migrate_tasks/write.rs:878:22
    |
878 |     for (file, _) in plan.rewrites.iter() {
    |                      ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#for_kv_map
    = note: `#[warn(clippy::for_kv_map)]` on by default
help: use the corresponding method
    |
878 -     for (file, _) in plan.rewrites.iter() {
878 +     for file in plan.rewrites.keys() {
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
634 ~         if (b == b'#' || b == b'^') {
635 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
636 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
639 |                 return true;
640 ~             }
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1673:1
     |
1673 | / fn apply_verdicts(
1674 | |     input: SuccessorInput,
1675 | |     files: Vec<FileScan>,
1676 | |     verdicts: Vec<DependentVerdict>,
...    |
1681 | |     project_folds: Vec<ProjectFold>,
1682 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/successors.rs:2102:29
     |
2102 |             project_states: &project_states,
     |                             ^^^^^^^^^^^^^^^ help: change this to: `project_states`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: using `chunks_exact` with a constant chunk size
   --> src/native/task_dependencies/mod.rs:205:10
    |
205 |         .chunks_exact(2)
    |          ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0.iter()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chunks_exact_to_as_chunks

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#filter_map_bool_then
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
   --> src/native/task_status_hooks/sync.rs:440:5
    |
440 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:307:9
    |
307 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1200:1
     |
1200 | / fn consume_blocked_links_after_compose(
1201 | |     compose: &mut ComposeResult,
1202 | |     files: &[FileScan],
1203 | |     daily_path: &Path,
...    |
1214 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1215 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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

warning: `bob-cli` (lib) generated 147 warnings
error: could not compile `bob-cli` (lib) due to 2 previous errors; 147 warnings emitted
warning: build failed, waiting for other jobs to finish...
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#items_after_test_module
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
  --> src/native/capture_language/tests/goto.rs:54:42
   |
54 |         let completion = field(raw, end).expect(&format!("{raw:?} completes"));
   |                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw:?} completes"))`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call
   = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:102:22
    |
102 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:115:35
    |
115 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:1993:35
     |
1993 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2030:48
     |
2030 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2039:22
     |
2039 |         execute(raw).expect(&format!("{raw} executes as prose"));
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
    --> src/native/capture_parse.rs:2431:9
     |
2431 | /         for raw in ["Plan =x"] {
2432 | |             let prose = json(raw);
2433 | |             assert_eq!(prose["mode"], "task", "{raw}");
2434 | |             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
2435 | |             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
2436 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_element_loop
     = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
     |
2431 ~         {
2432 +             let raw = "Plan =x";
2433 +             let prose = json(raw);
2434 +             assert_eq!(prose["mode"], "task", "{raw}");
2435 +             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
2436 +             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
2437 +         }
     |

warning: items after a test module
   --> src/native/capture_pomodoro_close/ledger.rs:915:1
    |
915 |   mod managed_dependency_tests {
    |   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
...
944 | / fn collect_work_log_note_groups(
945 | |     spans: &[LineSpan<'_>],
946 | |     entry_index: usize,
947 | |     range: &Range<usize>,
948 | |     fenced: &BTreeSet<usize>,
949 | | ) -> Vec<WorkLogNoteGroup> {
    | |__________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

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

warning: equality checks against false can be replaced by a negation
   --> src/native/gkeep/imports.rs:968:17
    |
968 |         assert!(has_verified(&loaded, "note-1", "0123456789ab") == false);
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `!has_verified(&loaded, "note-1", "0123456789ab")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bool_comparison

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

warning: items after a test module
   --> src/native/task_complete/tree.rs:832:1
    |
832 |   mod managed_dependency_tests {
    |   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
...
875 | / pub(crate) fn complete_embedded_trees<V: CloseVault>(
876 | |     vault: &V,
877 | |     roots: &[EmbeddedTreeRoot<'_>],
878 | |     completion_date: &str,
879 | | ) -> Result<EmbeddedTreesOutcome, String> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#items_after_test_module
    = help: move the items to before the test module was defined

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:922:9
    |
922 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> src/native/task_complete/tests/successor_tests.rs:954:9
    |
954 |         &day,
    |         ^^^^ help: change this to: `day`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_complete/tests/successor_tests.rs:1368:14
     |
1368 |         Some(&day),
     |              ^^^^ help: change this to: `day`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
    --> src/native/task_status_groups/tests.rs:1443:23
     |
1443 |     assert_idempotent(&crlf);
     |                       ^^^^^ help: change this to: `crlf`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:729:27
    |
729 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:741:27
    |
741 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:753:27
    |
753 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("proj.md", "prj")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:849:27
    |
849 |     assert!(scanned.edges.get(&edge("proj.md", "prj")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("proj.md", "prj"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_get_then_check

warning: `bob-cli` (lib test) generated 172 warnings (147 duplicates) (run `cargo clippy --fix --lib -p bob-cli --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 17 suggestions)
error: recipe `check` failed on line 27 with exit code 101
failed  exit=101  duration=55855ms

