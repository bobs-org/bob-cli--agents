# Chat History - ace-run (bob-cli-9d.1--mon)

- **TIMESTAMP:** 2026-10-18 15:54:11 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-9d.1--mon

## Prompt

sase monitor start --command 'just check' --reason 'Run the required bob-cli phase verification before closing bob-cli-9d.1'

## Response

sase tool run 2756b67cadb07556871267cb95de1b7f

✅  CHECK
────────────────────────────────────────────────
cargo fmt --check
cargo clippy --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
    Checking typenum v1.20.1
   Compiling version_check v0.9.5
    Checking cfg-if v1.0.4
    Checking stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
    Checking foldhash v0.2.0
    Checking allocator-api2 v0.2.21
    Checking equivalent v1.0.2
    Checking memchr v2.8.1
    Checking writeable v0.6.4
   Compiling libc v0.2.186
    Checking litemap v0.8.3
    Checking utf8_iter v1.0.4
    Checking simd-adler32 v0.3.9
   Compiling icu_properties_data v2.3.0
    Checking bitflags v2.12.1
   Compiling autocfg v1.5.1
   Compiling icu_normalizer_data v2.3.0
   Compiling crc32fast v1.5.0
   Compiling serde_core v1.0.228
    Checking adler2 v2.0.1
    Checking smallvec v1.15.2
    Checking rand_core v0.10.1
   Compiling getrandom v0.4.2
    Checking utf8parse v0.2.2
    Checking anstyle-query v1.1.5
   Compiling serde v1.0.228
    Checking anstyle v1.0.14
    Checking colorchoice v1.0.5
    Checking cpufeatures v0.3.0
    Checking tinyvec_macros v0.1.1
    Checking is_terminal_polyfill v1.70.2
    Checking cpufeatures v0.2.17
   Compiling zmij v1.0.21
    Checking itoa v1.0.18
    Checking strsim v0.11.1
    Checking weezl v0.1.12
   Compiling thiserror v2.0.18
    Checking clap_lex v1.1.0
    Checking byteorder-lite v0.1.0
    Checking const-oid v0.10.2
    Checking pxfm v0.1.30
    Checking bytecount v0.6.9
   Compiling serde_json v1.0.150
    Checking percent-encoding v2.3.2
    Checking quick-error v2.0.1
    Checking unicode-properties v0.1.4
    Checking regex-syntax v0.8.10
    Checking color_quant v1.1.0
    Checking unicode-bidi v0.3.18
    Checking zune-core v0.5.3
    Checking iana-time-zone v0.1.65
    Checking log v0.4.30
    Checking ryu v1.0.23
    Checking rangemap v1.7.1
    Checking ttf-parser v0.25.1
    Checking is_executable v1.0.6
    Checking bytemuck v1.25.2
    Checking unsafe-libyaml v0.2.11
    Checking hex v0.4.3
    Checking similar v2.7.0
   Compiling vcpkg v0.2.15
   Compiling pkg-config v0.3.33
   Compiling rustix v1.1.5
    Checking time-core v0.1.9
    Checking powerfmt v0.2.0
    Checking num-conv v0.2.2
   Compiling generic-array v0.14.7
    Checking fdeflate v0.3.7
    Checking encoding_rs v0.8.35
    Checking linux-raw-sys v0.12.1
    Checking deranged v0.5.8
   Compiling cc v1.2.63
    Checking once_cell v1.21.4
    Checking hashbrown v0.17.1
    Checking base64 v0.22.1
    Checking fallible-streaming-iterator v0.1.9
    Checking fallible-iterator v0.3.0
    Checking fastrand v2.5.0
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking hybrid-array v0.4.12
    Checking quick-xml v0.41.0
    Checking form_urlencoded v1.2.2
    Checking zune-jpeg v0.5.15
    Checking miniz_oxide v0.8.9
   Compiling num-traits v0.2.19
    Checking anstyle-parse v1.0.0
    Checking tinyvec v1.11.0
    Checking chacha20 v0.10.2
    Checking image-webp v0.2.4
    Checking gif v0.14.2
    Checking indexmap v2.14.0
    Checking hashlink v0.12.1
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
    Checking time v0.3.53
    Checking fs2 v0.4.3
    Checking regex-automata v0.4.14
    Checking block-buffer v0.12.0
    Checking crypto-common v0.2.2
    Checking flate2 v1.1.9
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking unicode-normalization v0.1.25
    Checking anstream v1.0.0
    Checking nom_locate v5.0.0
    Checking rand v0.10.1
    Checking inout v0.1.4
    Checking tempfile v3.27.0
    Checking png v0.18.1
    Checking digest v0.10.7
    Checking digest v0.11.3
    Checking moxcms v0.8.1
    Checking chrono v0.4.44
    Checking clap_builder v4.6.7
    Checking stringprep v0.1.5
    Checking regex v1.12.3
    Checking cipher v0.4.4
    Checking rusqlite v0.40.1
    Checking md-5 v0.10.6
    Checking sha2 v0.10.9
    Checking sha2 v0.11.0
    Checking aes v0.8.4
    Checking cbc v0.1.2
    Checking ecb v0.1.2
    Checking clap v4.6.7
    Checking image v0.25.10
    Checking rquickjs-core v0.12.1
   Compiling syn v3.0.6
   Compiling syn v2.0.117
    Checking clap_complete v4.6.11
    Checking rquickjs v0.12.1
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
    Checking lopdf v0.40.0
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
    Checking zerofrom v0.1.8
    Checking serde_yaml v0.9.34+deprecated
    Checking plist v1.10.0
    Checking yoke v0.8.3
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking icu_collections v2.3.0
    Checking icu_locale_core v2.3.0
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_12)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:444:12
    |
444 |         if child_end >= entry_line_index + 1 {
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

error[E0063]: missing field `added_at` in initializer of `native::ref_library::row::RefRow`
    --> src/native/highlights_ref/rename/plan.rs:2510:19
     |
2510 |         let row = RefRow {
     |                   ^^^^^^ missing `added_at`

warning: useless use of `format!`
   --> src/native/articles/render.rs:137:25
    |
137 |                         format!("{}", display_path(&plan.path))
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `display_path(&plan.path).to_string()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#useless_format
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#format_in_format_args
    = note: `#[warn(clippy::format_in_format_args)]` on by default

warning: literal with an empty format string
   --> src/native/articles/render.rs:215:9
    |
215 |         "STATE"
    |         ^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#print_literal
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#print_literal
help: try
    |
267 ~         "  {}  Preamble  {} w",
268 ~         styler.dim("¶"),
    |

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

warning: this function has too many arguments (8/7)
  --> src/native/capture/open_notes.rs:82:1
   |
82 | / fn open_note_for_item(
83 | |     bob_dir: &Path,
84 | |     item: &CaptureItemResult,
85 | |     path: &Path,
...  |
90 | |     settings: &note_tasks::NoteTaskSettings,
91 | | ) -> OpenNoteJson {
   | |_________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/output.rs:299:5
    |
299 | /     pub(super) fn from_items(
300 | |         items: Vec<CaptureItemResult>,
301 | |         global_destination: Option<GlobalDestinationSummary>,
302 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
309 | |         pull_in: PullInJson,
310 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
    --> src/native/capture/output.rs:1524:5
     |
1524 | /     if result.kind == "pomodoro_start" {
1525 | |         if let Some(start) = result.pomodoro_start.as_ref() {
1526 | |             print_human_pomodoro_start_success(
1527 | |                 result,
...    |
1537 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
     = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
     |
1524 ~     if result.kind == "pomodoro_start"
1525 ~         && let Some(start) = result.pomodoro_start.as_ref() {
1526 |             print_human_pomodoro_start_success(
 ...
1535 |             return;
1536 ~         }
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
   --> src/native/capture_complete/engine.rs:506:12
    |
506 |         || content.to_ascii_lowercase() == "@@template:"
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_ignore_case_cmp
    = note: `#[warn(clippy::manual_ignore_case_cmp)]` on by default
help: consider using `.eq_ignore_ascii_case()` instead
    |
506 -         || content.to_ascii_lowercase() == "@@template:"
506 +         || content.eq_ignore_ascii_case("@@template:")
    |

warning: redundant guard
   --> src/native/capture_language/close_log.rs:221:23
    |
221 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#redundant_guards
    = note: `#[warn(clippy::redundant_guards)]` on by default
help: try
    |
221 -         Some(list) if list.is_empty() => {
221 +         Some([]) => {
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/close_log.rs:511:1
    |
511 | / fn check_index_loggable(
512 | |     index: u32,
513 | |     index_range: (usize, usize),
514 | |     close_token: &str,
...   |
520 | |     complete_all: bool,
521 | | ) -> Result<(), CloseLogError> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:686:1
    |
686 | / pub(crate) fn lex_close_inline_entry_with_all(
687 | |     entry_tokens: &[Token<'_>],
688 | |     close_token: &str,
689 | |     in_progress: Option<&[u32]>,
...   |
694 | |     complete_all: bool,
695 | | ) -> Result<CloseInlineLex, CloseLogError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:931:1
    |
931 | / pub(crate) fn lex_close_log_bullets_with_all(
932 | |     child_lines: &[ItemLine<'_>],
933 | |     close_token: &str,
934 | |     in_progress: Option<&[u32]>,
...   |
939 | |     complete_all: bool,
940 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: taken reference of right operand
   --> src/native/capture_language/dependencies.rs:658:20
    |
658 |                 if raw.as_bytes() == &[sigil] =>
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
    --> src/native/capture_language/editor_parse.rs:1078:9
     |
1078 | /         if is_standalone_listen_marker(tokens[1].text) {
1079 | |             if let Some(intent) = classify_token(tokens[0].text) {
1080 | |                 if !policy.admits(&intent, RoutingEntry::Capture) {
1081 | |                     return None;
...    |
1125 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1078 ~         if is_standalone_listen_marker(tokens[1].text)
1079 ~             && let Some(intent) = classify_token(tokens[0].text) {
1080 |                 if !policy.admits(&intent, RoutingEntry::Capture) {
 ...
1123 |                 });
1124 ~             }
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
    --> src/native/capture_language/editor_pomodoro.rs:2002:17
     |
2002 |                 &first.to_string(),
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
    --> src/native/capture_language/item.rs:1329:31
     |
1329 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
1330 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1331 | |                 (false, '~', Some(b'@')) => true,
1332 | |                 _ => false,
1333 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
1329 -             let want_second = match (name.is_some(), first_sigil, second) {
1330 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1331 -                 (false, '~', Some(b'@')) => true,
1332 -                 _ => false,
1333 -             };
1329 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1716:5
     |
1716 | /     if let Some((_, after_tilde)) = drop {
1717 | |         if lex_start_drop(&after_tilde, 0, nospace)
1718 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1719 | |             == false
...    |
1723 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1716 ~     if let Some((_, after_tilde)) = drop
1717 ~         && lex_start_drop(&after_tilde, 0, nospace)
1718 |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
 ...
1721 |             return false;
1722 ~         }
     |

warning: equality checks against false can be replaced by a negation
    --> src/native/capture_language/item.rs:1717:12
     |
1717 |           if lex_start_drop(&after_tilde, 0, nospace)
     |  ____________^
1718 | |             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
1719 | |             == false
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bool_comparison
     = note: `#[warn(clippy::bool_comparison)]` on by default
help: try
     |
1717 ~         if !lex_start_drop(&after_tilde, 0, nospace)
1718 +             .is_ok_and(|outcome| matches!(outcome, StartDropOutcome::Valid(_)))
     |

warning: this `if` statement can be collapsed
    --> src/native/capture_language/item.rs:1725:5
     |
1725 | /     if let Some((_, after_at)) = timing {
1726 | |         if parse_pomodoro_start_suffix(&after_at).is_err() {
1727 | |             return false;
1728 | |         }
1729 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1725 ~     if let Some((_, after_at)) = timing
1726 ~         && parse_pomodoro_start_suffix(&after_at).is_err() {
1727 |             return false;
1728 ~         }
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2052:31
     |
2052 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
2052 -                 Err(error) => return Err(error.message),
2052 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2060:21
     |
2060 | /                     return Err(close_inline_dangling_error(
2061 | |                         &head, first, index, plain,
2062 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
2060 ~                     Err(close_inline_dangling_error(
2061 +                         &head, first, index, plain,
2062 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:2098:21
     |
2098 | /                     return Ok(Some(parsed_capture_item_outcome(
2099 | |                         item,
2100 | |                         ParsedCaptureText {
2101 | |                             body,
...    |
2113 | |                         None,
2114 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
help: remove `return`
     |
2098 ~                     Ok(Some(parsed_capture_item_outcome(
2099 +                         item,
2100 +                         ParsedCaptureText {
2101 +                             body,
2102 +                             clip: None,
2103 +                             route: None,
2104 +                             kind: CaptureKind::PomodoroClose { spec },
2105 +                             scheduled_offset: None,
2106 +                             priority_level: None,
2107 +                             sub_bullets: Vec::new(),
2108 +                             dependencies: Vec::new(),
2109 +                             blocked_tasks: Vec::new(),
2110 +                             dependency_target: None,
2111 +                         },
2112 +                         Vec::new(),
2113 +                         None,
2114 ~                     )))
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#let_and_return
    = note: `#[warn(clippy::let_and_return)]` on by default
help: return the expression directly
    |
401 ~                 
402 ~                 fields_used
403 +                     .iter()
404 +                     .map(|field| format!("{{{field}}}"))
405 +                     .collect::<Vec<_>>()
406 +                     .join(" and ")
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
    --> src/native/capture_parse.rs:1005:9
     |
1005 | /         if let Some(diagnostic) = refusal_diagnostic(
1006 | |             &parsed.spans,
1007 | |             parsed.mode,
1008 | |             &parsed.pomodoro_start,
...    |
1016 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1012 ~         )
1013 ~             && diagnostic.code != "template_clipboard" {
1014 |                 refusal_diagnostics.push(diagnostic);
1015 ~             }
     |

warning: redundant closure
    --> src/native/capture_parse.rs:1032:29
     |
1032 |             .unwrap_or_else(|| empty_wire_item());
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

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_task_toggle/ledger.rs:208:49
    |
208 | pub(crate) fn default_pomodoro_link_destination<'a>(
    |                                                 ^^
209 |     scan: &'a capture_pomodoros::PomodoroScan,
    |            ^^
210 |     queue_owner_line: Option<usize>,
211 | ) -> Option<&'a capture_pomodoros::PomodoroEntry> {
    |              ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
208 ~ pub(crate) fn default_pomodoro_link_destination(
209 ~     scan: &capture_pomodoros::PomodoroScan,
210 |     queue_owner_line: Option<usize>,
211 ~ ) -> Option<&capture_pomodoros::PomodoroEntry> {
    |

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
   --> src/native/highlights_ref/create.rs:537:5
    |
537 | /     if let Some(name) = matches.get_one::<String>("name") {
538 | |         if let Err(error) = super::clip_url::validate_name(name) {
539 | |             let styler = Styler::detect();
540 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
543 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
537 ~     if let Some(name) = matches.get_one::<String>("name")
538 ~         && let Err(error) = super::clip_url::validate_name(name) {
539 |             let styler = Styler::detect();
540 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
541 |             return 1;
542 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:545:5
    |
545 | /     if let Some(ref_type) = &ref_type {
546 | |         if let Err(error) = validate_ref_type(ref_type) {
547 | |             let styler = Styler::detect();
548 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
551 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
545 ~     if let Some(ref_type) = &ref_type
546 ~         && let Err(error) = validate_ref_type(ref_type) {
547 |             let styler = Styler::detect();
548 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
549 |             return 1;
550 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/create.rs:552:5
    |
552 | /     if let Some(published) = matches.get_one::<String>("published") {
553 | |         if let Err(error) = super::clip_url::validate_published(published) {
554 | |             let styler = Styler::detect();
555 | |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
...   |
558 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
552 ~     if let Some(published) = matches.get_one::<String>("published")
553 ~         && let Err(error) = super::clip_url::validate_published(published) {
554 |             let styler = Styler::detect();
555 |             eprintln!("{COMMAND_NAME}: {}: {error}", styler.red("error"));
556 |             return 1;
557 ~         }
    |

warning: this `match` expression can be replaced with `?`
    --> src/native/highlights_ref/create.rs:2049:17
     |
2049 | /                 match companion_mod::copy_audio_for_install(plan.audio.as_ref())
2050 | |                 {
2051 | |                     Ok(created) => created,
2052 | |                     Err(error) => return Err(error),
2053 | |                 }
     | |_________________^ help: try instead: `companion_mod::copy_audio_for_install(plan.audio.as_ref())?`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:2809:1
     |
2809 | / fn print_pdf_dry_run(
2810 | |     config: &Config,
2811 | |     styler: &Styler,
2812 | |     source_display: &str,
...    |
2820 | |     legacy: &[sources_mod::RecordedSource],
2821 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:3036:1
     |
3036 | / fn compose_markdown_marker(
3037 | |     status: &str,
3038 | |     parent: &str,
3039 | |     title: &str,
...    |
3044 | |     return_links: bool,
3045 | | ) -> Result<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:248:5
    |
248 | /     if !unit.is_library_pdf() {
249 | |         if let Err(failure) = session.pre_sync() {
250 | |             return IntakeOutcome::Queued {
251 | |                 path,
...   |
256 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
248 ~     if !unit.is_library_pdf()
249 ~         && let Err(failure) = session.pre_sync() {
250 |             return IntakeOutcome::Queued {
...
254 |             };
255 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:644:5
    |
644 | /     if let IntakeUnit::Audio { .. } = unit {
645 | |         if !pdf.with_extension("pdf").is_file() {
646 | |             return Err(QueueFailure::new(
647 | |                 QueueReason::Collision,
...   |
654 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
644 ~     if let IntakeUnit::Audio { .. } = unit
645 ~         && !pdf.with_extension("pdf").is_file() {
646 |             return Err(QueueFailure::new(
...
652 |             ));
653 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/intake.rs:693:9
    |
693 | /         if let Some(parent) = moved.to.parent() {
694 | |             if let Err(error) = fs::create_dir_all(parent) {
695 | |                 let detail = format!("create {}: {error}", parent.display());
696 | |                 return Err(rollback_moves(&mut completed, detail));
697 | |             }
698 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
693 ~         if let Some(parent) = moved.to.parent()
694 ~             && let Err(error) = fs::create_dir_all(parent) {
695 |                 let detail = format!("create {}: {error}", parent.display());
696 |                 return Err(rollback_moves(&mut completed, detail));
697 ~             }
    |

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
735 ~     DIAGRAM_TIMEOUT_BASE_SECS
736 +         .saturating_add(
737 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
738 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: this `match` expression can be replaced with `?`
   --> src/native/highlights_ref/collection.rs:134:25
    |
134 |       let resolved_name = match collection_name::resolve_collection_name(
    |  _________________________^
135 | |         options.name.as_deref(),
136 | |         output_stem,
137 | |         options.title.as_deref(),
...   |
141 | |         Err(error) => return Err(error),
142 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: try instead
    |
134 ~     let resolved_name = collection_name::resolve_collection_name(
135 +         options.name.as_deref(),
136 +         output_stem,
137 +         options.title.as_deref(),
138 +         &urls,
139 ~     )?;
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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_return
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#chars_next_cmp
    = note: `#[warn(clippy::chars_next_cmp)]` on by default

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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:344:5
    |
344 | /     if path.components().count() > 1 && path.is_relative() {
345 | |         if let Ok(cwd) = std::env::current_dir() {
346 | |             return cwd.join(path);
347 | |         }
348 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
344 ~     if path.components().count() > 1 && path.is_relative()
345 ~         && let Ok(cwd) = std::env::current_dir() {
346 |             return cwd.join(path);
347 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:355:5
    |
355 | /     if path.is_relative() {
356 | |         if let Ok(cwd) = std::env::current_dir() {
357 | |             return cwd.join(path);
358 | |         }
359 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
355 ~     if path.is_relative()
356 ~         && let Ok(cwd) = std::env::current_dir() {
357 |             return cwd.join(path);
358 ~         }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:375:16
    |
375 |           } else if line.contains("Overfull") {
    |  ________________^
376 | |             if let Some(width) = overfull_width_pt(line) {
377 | |                 if width > 20.0 {
378 | |                     let key = format!("overfull:{line}");
...   |
386 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
375 ~         } else if line.contains("Overfull")
376 ~             && let Some(width) = overfull_width_pt(line) {
377 |                 if width > 20.0 {
...
384 |                 }
385 ~             }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/note_snapshot/profile.rs:376:13
    |
376 | /             if let Some(width) = overfull_width_pt(line) {
377 | |                 if width > 20.0 {
378 | |                     let key = format!("overfull:{line}");
379 | |                     if seen.insert(key) {
...   |
385 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
376 ~             if let Some(width) = overfull_width_pt(line)
377 ~                 && width > 20.0 {
378 |                     let key = format!("overfull:{line}");
...
383 |                     }
384 ~                 }
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: methods called `as_*` usually take `self` by reference or `self` by mutable reference
  --> src/native/highlights_ref/note_snapshot/classify.rs:54:32
   |
54 |     pub(crate) const fn as_str(self) -> &'static str {
   |                                ^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#wrong_self_convention
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_match
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1570 ~     if let Some(path) = target.strip_suffix(')')
1571 ~         && let Some(bare) = path.rsplit_once(" (") {
1572 |             return (bare.0.trim().to_string(), Some(bare.1.to_string()));
1573 ~         }
     |

warning: this block may be rewritten with the `?` operator
    --> src/native/highlights_ref/note_snapshot/obsidian.rs:1604:12
     |
1604 |       } else if let Some(stripped) = text.strip_prefix('(') {
     |  ____________^
1605 | |         (')', stripped)
1606 | |     } else {
1607 | |         return None;
1608 | |     };
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#question_mark
help: replace it with
     |
1604 ~     } else {
1605 +         let stripped = text.strip_prefix('(')?;
1606 +         (')', stripped)
1607 ~     };
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#clone_on_copy
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#large_enum_variant
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_str_replace

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
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
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:415:17
    |
415 |         blocks: &mut Vec<Block>,
    |                 ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#ptr_arg
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#replace_box
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#type_complexity

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1194:1
     |
1194 | / fn compose_bob_masthead<L: SourceLoader>(
1195 | |     masthead: &mut SnapshotMasthead,
1196 | |     source: &SourceIdentity,
1197 | |     kind: &NoteKind,
...    |
1204 | |     settings: &TasksSettings,
1205 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1259:5
     |
1259 | /     if outcome.is_none() && *kind == NoteKind::TerminalProject {
1260 | |         if let Some(status) = metadata
1261 | |             .and_then(|metadata| metadata_value(metadata, "status"))
1262 | |             .and_then(yaml_scalar_text)
...    |
1273 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1259 ~     if outcome.is_none() && *kind == NoteKind::TerminalProject
1260 ~         && let Some(status) = metadata
1261 |             .and_then(|metadata| metadata_value(metadata, "status"))
 ...
1271 |             }
1272 ~         }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:2163:17
     |
2163 | /                 if let Some(original) = &task.anchor {
2164 | |                     if let Some(anchor) = mapping
2165 | |                         .get(&(original.identity.clone(), original.id.clone()))
...    |
2169 | |                 }
     | |_________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
2163 ~                 if let Some(original) = &task.anchor
2164 ~                     && let Some(anchor) = mapping
2165 |                         .get(&(original.identity.clone(), original.id.clone()))
2166 |                     {
2167 |                         task.anchor = Some(anchor.clone());
2168 ~                     }
     |

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/visibility.rs:193:21
    |
193 | /                     *inner = Box::new(
194 | |                         nested.into_iter().next().expect("embedded block"),
195 | |                     );
    | |_____________________^ help: replace existing content with inner value instead: `**inner = nested.into_iter().next().expect("embedded block")`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#replace_box

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:418:25
    |
418 |                         extracted.extend(nested.drain(..));
    |                         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#extend_with_drain
    = note: `#[warn(clippy::extend_with_drain)]` on by default

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:445:21
    |
445 |                     extracted.extend(nested.drain(..));
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#extend_with_drain

warning: use of `extend` instead of `append` for adding the full range of a second vector
   --> src/native/highlights_ref/note_snapshot/visibility.rs:465:21
    |
465 |                     extracted.extend(nested.drain(..));
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `extracted.append(&mut nested)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#extend_with_drain

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
790 ~                 if current != *before
791 ~                     && let Err(error) = atomic_write_bytes(path, before) {
792 |                         failures.push(format!(
...
795 |                         ));
796 ~                     }
    |

warning: this `if` statement can be collapsed
   --> src/native/highlights_ref/stamp.rs:519:5
    |
519 | /     if let (Ok(child_c), Ok(parent_c)) =
520 | |         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
521 | |     {
522 | |         if let Some(rel) = relative_inside(&child_c, &parent_c) {
...   |
525 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
520 ~         (std::fs::canonicalize(child), std::fs::canonicalize(parent))
521 ~         && let Some(rel) = relative_inside(&child_c, &parent_c) {
522 |             return Some(rel);
523 ~         }
    |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1070:9
     |
1070 | /         if trimmed.starts_with("done_tasks:") {
1071 | |             if let Some(start) = trimmed.find("[[") {
1072 | |                 if let Some(end) = trimmed[start..].find("]]") {
1073 | |                     let target = &trimmed[start + 2..start + end];
...    |
1081 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1070 ~         if trimmed.starts_with("done_tasks:")
1071 ~             && let Some(start) = trimmed.find("[[") {
1072 |                 if let Some(end) = trimmed[start..].find("]]") {
 ...
1079 |                 }
1080 ~             }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1071:13
     |
1071 | /             if let Some(start) = trimmed.find("[[") {
1072 | |                 if let Some(end) = trimmed[start..].find("]]") {
1073 | |                     let target = &trimmed[start + 2..start + end];
1074 | |                     let mut rel = target.trim().to_string();
...    |
1080 | |             }
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1071 ~             if let Some(start) = trimmed.find("[[")
1072 ~                 && let Some(end) = trimmed[start..].find("]]") {
1073 |                     let target = &trimmed[start + 2..start + end];
 ...
1078 |                     return Some(rel);
1079 ~                 }
     |

warning: this `if` statement can be collapsed
    --> src/native/highlights_ref/sync.rs:1084:5
     |
1084 | /     if relative.components().count() == 1 {
1085 | |         if let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1086 | |             return Some(format!("done/{stem}_done.md"));
1087 | |         }
1088 | |     }
     | |_____^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
     |
1084 ~     if relative.components().count() == 1
1085 ~         && let Some(stem) = destination.file_stem().and_then(|s| s.to_str()) {
1086 |             return Some(format!("done/{stem}_done.md"));
1087 ~         }
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/ref_library/today.rs:330:6
    |
330 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/ref_library/today.rs:644:1
    |
644 | / fn fail(
645 | |     format: Format,
646 | |     dry_run: bool,
647 | |     code: &str,
...   |
652 | |     pomodoros: &[TodayPomodoroRow],
653 | | ) -> i32 {
    | |________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#collapsible_if
help: collapse nested if block
    |
650 ~         if (b == b'#' || b == b'^') {
651 ~             && bytes[i + 1].eq_ignore_ascii_case(&b'r')
652 |                 && bytes[i + 2].eq_ignore_ascii_case(&b'e')
...
655 |                 return true;
656 ~             }
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

warning: this manual char comparison can be written more succinctly
   --> src/native/vault_links.rs:314:17
    |
314 |         .rsplit(|character| matches!(character, '/' | '\\'))
    |                 ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using an array of `char`: `['/', '\\']`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_pattern_char_comparison

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

warning: `bob-cli` (lib) generated 220 warnings (run `cargo clippy --fix --lib -p bob-cli -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 159 suggestions)
For more information about this error, try `rustc --explain E0063`.
warning: `bob-cli` (lib test) generated 2 warnings (2 duplicates)
error: could not compile `bob-cli` (lib test) due to 1 previous error; 2 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/articles.rs:162:9
    |
162 | /         &mut article_command(&fixture)
163 | |             .args(["format", "-s", "draft", "-f", "json"]),
    | |__________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#useless_concat
    = note: `#[warn(clippy::useless_concat)]` on by default

warning: for loop over a single element
   --> tests/cli/capture/parse_pomodoro_close.rs:346:5
    |
346 | /     for (text, range) in [("=x - wired", [3, 4])] {
347 | |         let value = parse(text);
348 | |         assert_eq!(
349 | |             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
...   |
356 | |         );
357 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_element_loop
    = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
    |
346 ~     {
347 +         let (text, range) = ("=x - wired", [3, 4]);
348 +         let value = parse(text);
349 +         assert_eq!(
350 +             value["diagnostics"][0]["code"], "invalid_pomodoro_close",
351 +             "{text}"
352 +         );
353 +         assert_eq!(
354 +             value["diagnostics"][0]["range"],
355 +             serde_json::json!(range),
356 +             "{text}"
357 +         );
358 +     }
    |

warning: the borrowed expression implements the required traits
   --> tests/cli/capture/pomodoro_close_log.rs:378:18
    |
378 |             .arg(&args[0])
    |                  ^^^^^^^^ help: change this to: `args[0]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:483:14
    |
483 |         .arg("-2 =x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#suspicious_command_arg_space
    = note: `#[warn(clippy::suspicious_command_arg_space)]` on by default
help: consider splitting the argument
    |
483 -         .arg("-2 =x\n- 1 wired the lexer")
483 +         .args(["-2", "=x\n- 1 wired the lexer"])
    |

warning: unnecessary use of `to_string`
   --> tests/cli/capture/pomodoro_shift.rs:581:11
    |
581 |         + &String::from_utf8_lossy(&shape_out.stdout).to_string();
    |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: use: `String::from_utf8_lossy(&shape_out.stdout).as_ref()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#unnecessary_to_owned
    = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: for loop over a single element
   --> tests/cli/capture/pomodoros_agenda.rs:648:5
    |
648 | /     for field in ["status"] {
649 | |         assert_eq!(agenda["plan_budget"][field], plan[field]);
650 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#single_element_loop
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bool_assert_comparison
     = note: `#[warn(clippy::bool_assert_comparison)]` on by default
help: replace it with `assert!(..)`
     |
1217 ~     assert!(
1218 ~         !mixed_json["items"][1]["ref_listen"]
1219 |             .as_bool()
1220 ~             .unwrap_or(false),
     |

warning: using `contains()` instead of `iter().any()` is more efficient
   --> tests/cli/capture/rewrite.rs:308:9
    |
308 | /         codes
309 | |             .iter()
310 | |             .any(|code| *code == "invalid_pomodoro_block_id"),
    | |_____________________________________________________________^ help: try: `codes.contains(&"invalid_pomodoro_block_id")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#manual_contains
    = note: `#[warn(clippy::manual_contains)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
  --> tests/cli/capture_templates.rs:41:9
   |
41 |         &mut command(&file).args(["save", "-f", "json"]),
   |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

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
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:160:9
    |
160 | /         &mut command(&disabled_file)
161 | |             .arg("save")
162 | |             .args(["-f", "json"])
163 | |             .env("BOB_CONFIG_FILE", config),
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:296:9
    |
296 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:316:9
    |
316 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/capture_templates.rs:328:9
    |
328 |         &mut command(&file).args(["save", "-f", "json"]),
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `command(&file).args(["save", "-f", "json"])`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: needless call to `as_bytes`
   --> tests/cli/highlights/diagrams.rs:806:13
    |
806 |     assert!(long_tmpdir.to_string_lossy().as_bytes().len() > 40);
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: `len()` can be called directly on strings: `long_tmpdir.to_string_lossy().len()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_as_bytes
    = note: `#[warn(clippy::needless_as_bytes)]` on by default

warning: this expression creates a reference which is immediately dereferenced by the compiler
   --> tests/cli/highlights/fake_clip.rs:192:32
    |
192 |             root = json_string(&path_str(&root)),
    |                                ^^^^^^^^^^^^^^^^ help: change this to: `path_str(&root)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrow

warning: equality checks against false can be replaced by a negation
    --> tests/cli/highlights/listen.rs:1554:9
     |
1554 |         vault.join("xlib").exists() == false
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `!vault.join("xlib").exists()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#bool_comparison
     = note: `#[warn(clippy::bool_comparison)]` on by default

warning: the borrowed expression implements the required traits
   --> tests/cli/highlights/scan_integration.rs:674:29
    |
674 |         !fs::read_to_string(&vault.join("mac_inbox.md"))
    |                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `vault.join("mac_inbox.md")`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
  --> tests/cli/ref_library/migrate_tasks.rs:85:32
   |
85 |     let output = git_in(vault, &["log", "--format=%s"]);
   |                                ^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["log", "--format=%s"]`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:223:20
    |
223 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:224:20
    |
224 |     git_in(&vault, &["commit", "-q", "-m", "dep"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "dep"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:354:20
    |
354 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:355:20
    |
355 |     git_in(&vault, &["commit", "-q", "-m", "unmapped"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "unmapped"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:378:20
    |
378 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:379:20
    |
379 |     git_in(&vault, &["commit", "-q", "-m", "mapped"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "mapped"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:455:20
    |
455 |     git_in(&vault, &["add", "-A"]);
    |                    ^^^^^^^^^^^^^^ help: change this to: `["add", "-A"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: the borrowed expression implements the required traits
   --> tests/cli/ref_library/migrate_tasks.rs:456:20
    |
456 |     git_in(&vault, &["commit", "-q", "-m", "crash"]);
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change this to: `["commit", "-q", "-m", "crash"]`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.99.0/index.html#needless_borrows_for_generic_args

warning: `bob-cli` (test "cli") generated 32 warnings (run `cargo clippy --fix --test "cli" -p bob-cli -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces` to apply 31 suggestions)
error: recipe `check` failed on line 27 with exit code 101
failed  exit=101  duration=97712ms

