# Chat History - ace-run (0we--mon)

- **TIMESTAMP:** 2026-10-04 10:52:30 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 0we--mon

## Prompt

sase monitor start --command 'just all' --reason 'Run the approved plan’s full bob-cli verification suite'

## Response

sase tool run 00a718d0bc0429193e34000f1a7960e8

🎨  FORMAT
────────────────────────────────────────────────
cargo fmt --check

🔍  LINT
────────────────────────────────────────────────
cargo clippy --all-targets --all-features
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
    Checking typenum v1.20.1
   Compiling version_check v0.9.5
    Checking stable_deref_trait v1.2.1
    Checking cfg-if v1.0.4
   Compiling find-msvc-tools v0.1.9
   Compiling shlex v2.0.1
    Checking foldhash v0.2.0
    Checking allocator-api2 v0.2.21
    Checking equivalent v1.0.2
    Checking memchr v2.8.1
    Checking writeable v0.6.4
   Compiling libc v0.2.186
    Checking litemap v0.8.3
   Compiling serde_core v1.0.228
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
    Checking utf8_iter v1.0.4
    Checking utf8parse v0.2.2
   Compiling getrandom v0.4.2
    Checking rand_core v0.10.1
    Checking smallvec v1.15.2
    Checking tinyvec_macros v0.1.1
    Checking anstyle-query v1.1.5
    Checking is_terminal_polyfill v1.70.2
    Checking bitflags v2.12.1
    Checking cpufeatures v0.3.0
   Compiling crc32fast v1.5.0
   Compiling serde v1.0.228
   Compiling autocfg v1.5.1
    Checking colorchoice v1.0.5
    Checking anstyle v1.0.14
    Checking itoa v1.0.18
    Checking adler2 v2.0.1
    Checking cpufeatures v0.2.17
   Compiling thiserror v2.0.18
    Checking simd-adler32 v0.3.9
   Compiling zmij v1.0.21
    Checking strsim v0.11.1
    Checking clap_lex v1.1.0
    Checking bytecount v0.6.9
    Checking const-oid v0.10.2
    Checking unicode-properties v0.1.4
    Checking percent-encoding v2.3.2
   Compiling serde_json v1.0.150
    Checking regex-syntax v0.8.10
    Checking unicode-bidi v0.3.18
    Checking is_executable v1.0.6
    Checking unsafe-libyaml v0.2.11
    Checking weezl v0.1.12
    Checking rangemap v1.7.1
    Checking ryu v1.0.23
    Checking ttf-parser v0.25.1
    Checking log v0.4.30
    Checking iana-time-zone v0.1.65
    Checking hex v0.4.3
    Checking similar v2.7.0
   Compiling pkg-config v0.3.33
   Compiling vcpkg v0.2.15
   Compiling rustix v1.1.5
    Checking time-core v0.1.9
    Checking deranged v0.5.8
    Checking powerfmt v0.2.0
    Checking linux-raw-sys v0.12.1
    Checking num-conv v0.2.2
    Checking fallible-iterator v0.3.0
    Checking fastrand v2.5.0
    Checking fallible-streaming-iterator v0.1.9
    Checking anstyle-parse v1.0.0
    Checking tinyvec v1.11.0
    Checking once_cell v1.21.4
    Checking form_urlencoded v1.2.2
    Checking base64 v0.22.1
    Checking encoding_rs v0.8.35
   Compiling generic-array v0.14.7
    Checking miniz_oxide v0.8.9
    Checking chacha20 v0.10.0
   Compiling cc v1.2.63
   Compiling num-traits v0.2.19
    Checking hashbrown v0.17.1
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking quick-xml v0.41.0
    Checking hybrid-array v0.4.12
    Checking anstream v1.0.0
    Checking unicode-normalization v0.1.25
    Checking fs2 v0.4.3
    Checking flate2 v1.1.9
    Checking clap_builder v4.6.7
    Checking time v0.3.53
    Checking crypto-common v0.2.2
    Checking block-buffer v0.12.0
    Checking indexmap v2.14.0
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking hashlink v0.12.1
    Checking rand v0.10.1
    Checking stringprep v0.1.5
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
    Checking chrono v0.4.44
    Checking digest v0.10.7
    Checking inout v0.1.4
    Checking regex-automata v0.4.14
    Checking digest v0.11.3
    Checking cipher v0.4.4
    Checking md-5 v0.10.6
    Checking sha2 v0.10.9
    Checking tempfile v3.27.0
   Compiling syn v3.0.6
   Compiling syn v2.0.117
    Checking sha2 v0.11.0
    Checking cbc v0.1.2
    Checking ecb v0.1.2
    Checking aes v0.8.4
    Checking nom_locate v5.0.0
    Checking clap v4.6.7
    Checking clap_complete v4.6.11
    Checking regex v1.12.3
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
    Checking lopdf v0.40.0
    Checking zerofrom v0.1.8
    Checking yoke v0.8.3
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking serde_yaml v0.9.34+deprecated
    Checking plist v1.10.0
    Checking icu_collections v2.3.0
    Checking icu_locale_core v2.3.0
    Checking icu_provider v2.3.1
    Checking icu_normalizer v2.3.0
    Checking icu_properties v2.3.0
    Checking idna_adapter v1.2.2
    Checking idna v1.1.0
    Checking url v2.5.8
    Checking rusqlite v0.40.1
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:297:12
    |
297 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:120:20
    |
120 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#int_plus_one

warning: this function has too many arguments (8/7)
   --> src/native/capture/dependencies.rs:510:1
    |
510 | / fn resolve_prerequisites(
511 | |     ctx: &DependencyContext,
512 | |     planner: &mut CaptureBatchPlanner,
513 | |     bob_dir: &Path,
...   |
518 | |     dependent_desc: &str,
519 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
    | |_______________________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture/dependencies.rs:728:24
    |
728 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
    |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#type_complexity
    = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1239:6
     |
1239 |   ) -> Result<
     |  ______^
1240 | |     (
1241 | |         Vec<MergedMember>,
1242 | |         BTreeSet<(String, String)>,
...    |
1246 | |     CaptureError,
1247 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#type_complexity

warning: this `if` statement can be collapsed
   --> src/native/capture/output.rs:550:5
    |
550 | /     if result.kind == "pomodoro_start" {
551 | |         if let Some(start) = result.pomodoro_start.as_ref() {
552 | |             print_human_pomodoro_start_success(
553 | |                 result,
...   |
562 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#collapsible_if
    = note: `#[warn(clippy::collapsible_if)]` on by default
help: collapse nested if block
    |
550 ~     if result.kind == "pomodoro_start"
551 ~         && let Some(start) = result.pomodoro_start.as_ref() {
552 |             print_human_pomodoro_start_success(
...
560 |             return;
561 ~         }
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture/plan.rs:119:1
    |
119 | / pub(super) fn plan_capture_item(
120 | |     request: &CaptureRequest,
121 | |     parsed_item: ParsedCaptureItem,
122 | |     now: chrono::NaiveDateTime,
...   |
128 | |     dependency_ctx: &mut DependencyContext,
129 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

warning: this `let...else` may be rewritten with the `?` operator
   --> src/native/capture/pomodoro_adjust.rs:627:9
    |
627 | /         let Some(relative_close) = line[open..].find(')') else {
628 | |             return None;
629 | |         };
    | |__________^ help: replace it with: `let relative_close = line[open..].find(')')?;`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#question_mark
    = note: `#[warn(clippy::question_mark)]` on by default

warning: this `match` expression can be replaced with `?`
   --> src/native/capture/pomodoro_adjust.rs:876:19
    |
876 |       let minutes = match minutes_part {
    |  ___________________^
877 | |         Some(part) => {
878 | |             let part = part.trim();
879 | |             let core = part.strip_suffix('m')?;
...   |
889 | |         None => return None,
890 | |     };
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#question_mark
help: try instead
    |
876 ~     let minutes = {
877 +         let part = minutes_part?;
878 +         let part = part.trim();
879 +         let core = part.strip_suffix('m')?;
880 +         let core = core.trim_end();
881 +         if core.is_empty() {
882 +             return None;
883 +         }
884 +         if !core.bytes().all(|byte| byte.is_ascii_digit()) {
885 +             return None;
886 +         }
887 +         core.parse::<u64>().ok()?
888 ~     };
    |

warning: manual `rem_euclid` implementation
   --> src/native/capture/pomodoro_adjust.rs:982:5
    |
982 |     (((value % 1440) + 1440) % 1440) as u64
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `value.rem_euclid(1440)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#manual_rem_euclid
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

warning: this `map_or` can be simplified
   --> src/native/capture/pomodoro_start.rs:396:20
    |
396 |                 && anchor.map_or(true, |anchor| *index > anchor)
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_map_or
    = note: `#[warn(clippy::unnecessary_map_or)]` on by default
help: use `is_none_or` instead
    |
396 -                 && anchor.map_or(true, |anchor| *index > anchor)
396 +                 && anchor.is_none_or(|anchor| *index > anchor)
    |

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_active_tasks.rs:318:12
    |
318 |     tasks: &mut Vec<ActiveTask>,
    |            ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#ptr_arg
    = note: `#[warn(clippy::ptr_arg)]` on by default
help: change this to
    |
318 -     tasks: &mut Vec<ActiveTask>,
318 +     tasks: &mut [ActiveTask],
    |

warning: redundant guard
   --> src/native/capture_language/close_log.rs:206:23
    |
206 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#redundant_guards
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

warning: unnecessary map of the identity function
   --> src/native/capture_language/editor_classify.rs:612:60
    |
612 |               let (after_x, x_len) = classify_link_close(raw)
    |  ____________________________________________________________^
613 | |                 .map(|(selection, x_len)| (selection, x_len))
    | |_____________________________________________________________^ help: remove the call to `map`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#map_identity
    = note: `#[warn(clippy::map_identity)]` on by default

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:408:1
    |
408 | / pub(super) enum TokenParse {
409 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
410 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
411 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
409 -     Marker(MarkerParse),
409 +     Marker(Box<MarkerParse>),
    |

warning: unnecessary use of `to_string`
    --> src/native/capture_language/editor_pomodoro.rs:1631:17
     |
1631 |                 &first.to_string(),
     |                 ^^^^^^^^^^^^^^^^^^ help: use: `first`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_to_owned
     = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1428:31
     |
1428 |                 Err(error) => return Err(error.message),
     |                               ^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_return
     = note: `#[warn(clippy::needless_return)]` on by default
help: remove `return`
     |
1428 -                 Err(error) => return Err(error.message),
1428 +                 Err(error) => Err(error.message),
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1436:21
     |
1436 | /                     return Err(close_inline_dangling_error(
1437 | |                         &head, index, plain,
1438 | |                     ));
     | |______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_return
help: remove `return`
     |
1436 ~                     Err(close_inline_dangling_error(
1437 +                         &head, index, plain,
1438 ~                     ))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/item.rs:1474:21
     |
1474 | /                     return Ok(Some(parsed_capture_item_outcome(
1475 | |                         item,
1476 | |                         ParsedCaptureText {
1477 | |                             body,
...    |
1488 | |                         None,
1489 | |                     )));
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_return
help: remove `return`
     |
1474 ~                     Ok(Some(parsed_capture_item_outcome(
1475 +                         item,
1476 +                         ParsedCaptureText {
1477 +                             body,
1478 +                             clip: None,
1479 +                             route: None,
1480 +                             kind: CaptureKind::PomodoroClose { spec },
1481 +                             scheduled_offset: None,
1482 +                             priority_level: None,
1483 +                             sub_bullets: Vec::new(),
1484 +                             dependencies: Vec::new(),
1485 +                             dependency_target: None,
1486 +                         },
1487 +                         Vec::new(),
1488 +                         None,
1489 ~                     )))
     |

warning: redundant guard
   --> src/native/capture_language/tokens.rs:566:43
    |
566 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#redundant_guards
help: try
    |
566 -                 Some((after_x, x_len)) if after_x.is_empty() => {
566 +                 Some(("", x_len)) => {
    |

warning: unnecessary map of the identity function
    --> src/native/capture_language/tokens.rs:1006:59
     |
1006 |       let (after_x, x_len) = classify_link_close(raw_suffix)
     |  ___________________________________________________________^
1007 | |         .map(|(selection, x_len)| (selection, x_len))
     | |_____________________________________________________^ help: remove the call to `map`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#map_identity

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1383:13
     |
1383 | /             return Ok(Some(parsed_capture_item_outcome(
1384 | |                 item,
1385 | |                 ParsedCaptureText {
1386 | |                     body: String::new(),
...    |
1403 | |                 Some(marker_text),
1404 | |             )));
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_return
help: remove `return`
     |
1383 ~             Ok(Some(parsed_capture_item_outcome(
1384 +                 item,
1385 +                 ParsedCaptureText {
1386 +                     body: String::new(),
1387 +                     clip: None,
1388 +                     route: Some(route),
1389 +                     kind: CaptureKind::PomodoroLink {
1390 +                         block_id: parts.block_id,
1391 +                         pomodoro_name: parts.pomodoro_name,
1392 +                         start: parts.start,
1393 +                         close: parts.close,
1394 +                         spelling: PomodoroLinkSpelling::Caret,
1395 +                     },
1396 +                     scheduled_offset: None,
1397 +                     priority_level: None,
1398 +                     sub_bullets: Vec::new(),
1399 +                     dependencies: Vec::new(),
1400 +                     dependency_target: None,
1401 +                 },
1402 +                 Vec::new(),
1403 +                 Some(marker_text),
1404 ~             )))
     |

warning: unneeded `return` statement
    --> src/native/capture_language/tokens.rs:1465:13
     |
1465 |             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
     |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_return
help: remove `return`
     |
1465 -             return Err(POMODORO_LINK_SHAPE_ERROR.to_string());
1465 +             Err(POMODORO_LINK_SHAPE_ERROR.to_string())
     |

warning: this `match` expression can be replaced with `?`
   --> src/native/capture_link_tasks.rs:287:9
    |
287 | /         match best_field_tier(raw_fields, term) {
288 | |             Some(tier) => total += tier,
289 | |             None => return None,
290 | |         }
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#question_mark
help: try instead
    |
287 ~         {
288 +             let tier = best_field_tier(raw_fields, term)?;
289 +             total += tier
290 +         }
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:195:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
195 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:242:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
242 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:430:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
430 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:447:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
447 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:467:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
467 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:490:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
490 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:552:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
552 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:635:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
635 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:789:10
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
789 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:862:6
    |
111 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
862 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1131:6
     |
 111 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1131 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#result_large_err

warning: using `chunks_exact` with a constant chunk size
   --> src/native/capture_pomodoro_close/links.rs:255:10
    |
255 |         .chunks_exact(2)
    |          ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0.iter()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#chunks_exact_to_as_chunks
    = note: `#[warn(clippy::chunks_exact_to_as_chunks)]` on by default

warning: using `chunks_exact` with a constant chunk size
  --> src/native/dataview/functions/scalar.rs:36:24
   |
36 |     for pair in values.chunks_exact(2) {
   |                        ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#chunks_exact_to_as_chunks

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#collapsible_if
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#question_mark

warning: using `chunks_exact` with a constant chunk size
   --> src/native/task_dependencies/mod.rs:198:10
    |
198 |         .chunks_exact(2)
    |          ^^^^^^^^^^^^^^^ help: consider using `as_chunks` instead: `as_chunks::<2>().0.iter()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#chunks_exact_to_as_chunks

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#too_many_arguments

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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#collapsible_if
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
   --> src/native/task_status_hooks/sync.rs:388:5
    |
388 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:256:9
    |
256 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this `impl` can be derived
   --> src/native/vault_sync.rs:165:1
    |
165 | / impl Default for RunOptions {
166 | |     fn default() -> Self {
167 | |         Self {
168 | |             dry_run: false,
...   |
173 | | }
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#derivable_impls
    = note: `#[warn(clippy::derivable_impls)]` on by default
help: replace the manual implementation with a derive attribute
    |
159 + #[derive(Default)]
160 | struct RunOptions {
    |

warning: `bob-cli` (lib) generated 49 warnings (run `cargo clippy --fix --lib -p bob-cli -- ` to apply 20 suggestions)
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#match_single_binding
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#match_single_binding
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
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#match_single_binding
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
    --> src/native/capture_language/tests/grammar.rs:1856:35
     |
1856 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#expect_fun_call
     = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:1893:48
     |
1893 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:1902:22
     |
1902 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#expect_fun_call

warning: for loop over a single element
    --> src/native/capture_parse.rs:1404:9
     |
1404 | /         for raw in ["Plan =x"] {
1405 | |             let prose = json(raw);
1406 | |             assert_eq!(prose["mode"], "task", "{raw}");
1407 | |             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1408 | |             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1409 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#single_element_loop
     = note: `#[warn(clippy::single_element_loop)]` on by default
help: try
     |
1404 ~         {
1405 +             let raw = "Plan =x";
1406 +             let prose = json(raw);
1407 +             assert_eq!(prose["mode"], "task", "{raw}");
1408 +             assert!(prose.get("pomodoro_close").is_none(), "{raw}");
1409 +             assert!(prose.get("pomodoro_start").is_none(), "{raw}");
1410 +         }
     |

warning: unnecessary use of `get(Path::new("b.md")).is_none()`
   --> src/native/capture_pomodoro_close/linked_task_tests.rs:223:28
    |
223 |         plan.changed_files.get(Path::new("b.md")).is_none(),
    |         -------------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |         |
    |         help: replace it with: `!plan.changed_files.contains_key(Path::new("b.md"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_get_then_check
    = note: `#[warn(clippy::unnecessary_get_then_check)]` on by default

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:711:27
    |
711 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:723:27
    |
723 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:735:27
    |
735 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_get_then_check

warning: `bob-cli` (lib test) generated 60 warnings (49 duplicates) (run `cargo clippy --fix --lib -p bob-cli --tests -- ` to apply 4 suggestions)
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#single_element_loop
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#needless_borrows_for_generic_args
    = note: `#[warn(clippy::needless_borrows_for_generic_args)]` on by default

warning: single argument that looks like it should be multiple arguments
   --> tests/cli/capture/pomodoro_close_log.rs:451:14
    |
451 |         .arg("-2 =x\n- 1 wired the lexer")
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#suspicious_command_arg_space
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
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.98.0/index.html#unnecessary_to_owned
    = note: `#[warn(clippy::unnecessary_to_owned)]` on by default

warning: `bob-cli` (test "cli") generated 4 warnings (run `cargo clippy --fix --test "cli" -p bob-cli -- ` to apply 3 suggestions)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 43.42s

🧪  TEST
────────────────────────────────────────────────
cargo test
   Compiling typenum v1.20.1
   Compiling stable_deref_trait v1.2.1
   Compiling cfg-if v1.0.4
   Compiling shlex v2.0.1
   Compiling allocator-api2 v0.2.21
   Compiling foldhash v0.2.0
   Compiling equivalent v1.0.2
   Compiling memchr v2.8.1
   Compiling writeable v0.6.4
   Compiling litemap v0.8.3
   Compiling utf8_iter v1.0.4
   Compiling smallvec v1.15.2
   Compiling utf8parse v0.2.2
   Compiling rand_core v0.10.1
   Compiling bitflags v2.12.1
   Compiling tinyvec_macros v0.1.1
   Compiling anstyle-query v1.1.5
   Compiling colorchoice v1.0.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling cpufeatures v0.3.0
   Compiling anstyle v1.0.14
   Compiling simd-adler32 v0.3.9
   Compiling adler2 v2.0.1
   Compiling itoa v1.0.18
   Compiling cpufeatures v0.2.17
   Compiling strsim v0.11.1
   Compiling clap_lex v1.1.0
   Compiling unicode-bidi v0.3.18
   Compiling percent-encoding v2.3.2
   Compiling regex-syntax v0.8.10
   Compiling unicode-properties v0.1.4
   Compiling bytecount v0.6.9
   Compiling const-oid v0.10.2
   Compiling is_executable v1.0.6
   Compiling iana-time-zone v0.1.65
   Compiling log v0.4.30
   Compiling ryu v1.0.23
   Compiling weezl v0.1.12
   Compiling ttf-parser v0.25.1
   Compiling unsafe-libyaml v0.2.11
   Compiling rangemap v1.7.1
   Compiling hex v0.4.3
   Compiling similar v2.7.0
   Compiling linux-raw-sys v0.12.1
   Compiling time-core v0.1.9
   Compiling deranged v0.5.8
   Compiling powerfmt v0.2.0
   Compiling num-conv v0.2.2
   Compiling once_cell v1.21.4
   Compiling fallible-iterator v0.3.0
   Compiling libc v0.2.186
   Compiling icu_properties_data v2.3.0
   Compiling icu_normalizer_data v2.3.0
   Compiling serde_core v1.0.228
   Compiling zmij v1.0.21
   Compiling fastrand v2.5.0
   Compiling base64 v0.22.1
   Compiling fallible-streaming-iterator v0.1.9
   Compiling num-traits v0.2.19
   Compiling thiserror v2.0.18
   Compiling zerofrom v0.1.8
   Compiling cc v1.2.63
   Compiling crc32fast v1.5.0
   Compiling encoding_rs v0.8.35
   Compiling nom v8.0.0
   Compiling aho-corasick v1.1.4
   Compiling quick-xml v0.41.0
   Compiling hashbrown v0.17.1
   Compiling chacha20 v0.10.0
   Compiling anstyle-parse v1.0.0
   Compiling tinyvec v1.11.0
   Compiling form_urlencoded v1.2.2
   Compiling miniz_oxide v0.8.9
   Compiling yoke v0.8.3
   Compiling rustix v1.1.5
   Compiling generic-array v0.14.7
   Compiling hybrid-array v0.4.12
   Compiling chrono v0.4.44
   Compiling anstream v1.0.0
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling unicode-normalization v0.1.25
   Compiling flate2 v1.1.9
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
   Compiling getrandom v0.4.2
   Compiling fs2 v0.4.3
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling indexmap v2.14.0
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling hashlink v0.12.1
   Compiling clap_builder v4.6.7
   Compiling rand v0.10.1
   Compiling time v0.3.53
   Compiling digest v0.10.7
   Compiling inout v0.1.4
   Compiling stringprep v0.1.5
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling regex-automata v0.4.14
   Compiling serde v1.0.228
   Compiling serde_json v1.0.150
   Compiling cipher v0.4.4
   Compiling digest v0.11.3
   Compiling icu_collections v2.3.0
   Compiling md-5 v0.10.6
   Compiling sha2 v0.10.9
   Compiling tempfile v3.27.0
   Compiling icu_locale_core v2.3.0
   Compiling sha2 v0.11.0
   Compiling cbc v0.1.2
   Compiling aes v0.8.4
   Compiling ecb v0.1.2
   Compiling serde_yaml v0.9.34+deprecated
   Compiling nom_locate v5.0.0
   Compiling icu_provider v2.3.1
   Compiling lopdf v0.40.0
   Compiling clap v4.6.7
   Compiling plist v1.10.0
   Compiling icu_normalizer v2.3.0
   Compiling icu_properties v2.3.0
   Compiling clap_complete v4.6.11
   Compiling regex v1.12.3
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-cli v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 48.76s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261004_101720/build/debug/deps/bob_cli-189bf77a0c2a798f)

running 1654 tests
test native::capture::budget::tests::destination_roles_follow_the_contract ... ok
test native::capture::budget::tests::theme_warning_names_added_themes_with_hint ... ok
test native::capture::output::tests::typed_entry_details_print_two_spaces_under_their_entry ... ok
test native::capture::output::tests::log_entry_details_omitted_when_empty ... ok
test native::capture::output::tests::typed_work_log_details_align_with_entries_when_present ... ok
test native::capture::output::tests::typed_work_log_details_omitted_when_no_entry_has_details ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_tab_children_and_interior_blanks ... ok
test native::capture::pomodoro_blocks::tests::block_range_keeps_fenced_child_lines_verbatim ... ok
test native::capture::pomodoro_blocks::tests::block_range_stops_at_section_end_and_covers_last_entry ... ok
test native::capture::pomodoro_blocks::tests::block_range_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::block_range_trims_trailing_blanks_and_stops_at_zero_indent ... ok
test native::capture::pomodoro_blocks::tests::depth_continuation_lines_take_parent_depth_plus_one ... ok
test native::capture::pomodoro_blocks::tests::depth_counts_nested_list_items ... ok
test native::capture::pomodoro_blocks::tests::depth_supports_two_space_and_mixed_indentation ... ok
test native::capture::pomodoro_blocks::tests::pairing_created_block_is_all_added ... ok
test native::capture::pomodoro_blocks::tests::pairing_pure_insert_is_added_and_pure_delete_is_removed ... ok
test native::capture::pomodoro_blocks::tests::pairing_replace_becomes_changed_with_before ... ok
test native::capture::pomodoro_blocks::tests::pairing_uneven_replace_splits_changed_added_removed ... ok
test native::capture::pomodoro_blocks::tests::tracker_autodetects_an_unreported_child_insert ... ok
test native::capture::pomodoro_blocks::tests::resolution_rejects_a_non_entry_after - should panic ... ok
test native::capture::pomodoro_blocks::tests::forwarding_panics_when_a_tracked_headline_is_deleted - should panic ... ok
test native::capture::pomodoro_blocks::tests::tracker_resolves_created_before_and_reports_roles_once ... ok
test native::capture::pomodoro_blocks::tests::tracker_reports_one_cumulative_block_across_items ... ok
test native::capture::pomodoro_blocks::tests::tracker_forwards_a_tracked_block_across_an_insert_above ... ok
test native::capture::pomodoro_blocks::tests::vanished_entry_is_dropped_silently - should panic ... ok
test native::capture::pomodoro_blocks::tests::unreported_headline_rewrite_emits_unchanged_block - should panic ... ok
test native::capture::tests::assembly::assembles_capture_block_with_clip_children_then_schedule_log ... ok
test native::capture::tests::assembly::assembles_capture_block_with_sub_bullets_before_clip_and_schedule_log ... ok
test native::capture::tests::assembly::finds_the_earliest_direct_child_managed_log ... ok
test native::capture::tests::assembly::formats_pomodoro_task_with_block_id_as_final_token ... ok
test native::capture::tests::assembly::formats_task_line ... ok
test native::capture::tests::assembly::formats_task_with_block_id_as_ordinary_task_with_final_block_id ... ok
test native::capture::tests::assembly::named_pomodoro_creation_ignores_cancelled_nested_and_fenced_entries ... ok
test native::capture::task_blocks::tests::block_range_maps_byte_end_to_line_range ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_in_empty_and_crlf_sections ... ok
test native::capture::tests::assembly::named_pomodoro_link_bypasses_multiple_open_timed_guard ... ok
test native::capture::tests::assembly::named_pomodoro_link_first_duplicate_wins ... ok
test native::capture::task_blocks::tests::toggle_plus_subbullet_shows_the_task_line_as_changed ... ok
test native::capture::tests::assembly::pomodoro_link_falls_back_to_first_open_and_ignores_nested_tasks ... ok
test native::capture::tests::assembly::pomodoro_link_prefers_the_single_timed_open_entry ... ok
test native::capture::tests::assembly::pomodoro_link_preserves_crlf_and_reuses_nearby_child_indentation ... ok
test native::capture::tests::assembly::pomodoro_note_appends_after_completed_entry_children ... ok
test native::capture::tests::assembly::named_pomodoro_link_selects_placeholder_and_timed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_current_wins_over_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_first_future_when_nothing_is_completed ... ok
test native::capture::tests::assembly::named_pomodoro_link_creates_placeholder_on_no_open_match ... ok
test native::capture::tests::assembly::pomodoro_link_rejects_missing_section_target_and_timed_ambiguity ... ok
test native::capture::tests::assembly::pomodoro_note_last_completed_wins_over_a_future_entry ... ok
test native::capture::tests::assembly::pomodoro_note_ignores_cancelled_and_nested_completed_entries ... ok
test native::capture::tests::assembly::pomodoro_note_preserves_crlf_under_a_completed_entry ... ok
test native::capture::tests::assembly::pomodoro_note_returned_text_comes_from_the_completed_parser ... ok
test native::capture::tests::assembly::pomodoro_note_scan_ignores_fenced_completed_lookalikes ... ok
test native::capture::tests::assembly::pomodoro_note_timed_ambiguity_wins_over_completed_fallback ... ok
test native::capture::tests::assembly::sub_bullet_insertion_keeps_dependency_lines_first ... ok
test native::capture::tests::assembly::pomodoro_section_scan_ignores_fenced_lookalikes ... ok
test native::capture::tests::grammar::extracts_trailing_schedule_from_terminal_region ... ok
test native::capture::tests::grammar::extracts_priority_markers_from_terminal_region ... ok
test native::capture::tests::assembly::pomodoro_selection_policies_diverge_on_completed_plus_future ... ok
test native::capture::tests::assembly::recognizes_plugin_compatible_managed_log_markers ... ok
test native::capture::tests::grammar::clip_markers_are_terminal_forgiving_and_can_be_disabled ... ok
test native::capture::tests::grammar::parses_schedule_tokens ... ok
test native::capture::tests::grammar::extracts_clip_and_schedule_markers_from_terminal_region ... ok
test native::capture::tests::grammar::forced_route_bypasses_auto_route_parsing ... ok
test native::capture::tests::grammar::bare_sub_bullet_markers_toggle_instead_of_erroring ... ok
test native::capture::tests::placement::adds_leading_newline_when_inserting_after_non_newline_eof ... ok
test native::capture::task_blocks::tests::created_parent_reports_every_row_added ... ok
test native::capture::tests::grammar::pomodoro_route_requires_a_body_and_stays_literal_in_middle_or_forced ... ok
test native::capture::tests::grammar::parses_task_block_id_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::grammar::retired_double_colon_markers_are_usage_errors ... ok
test native::capture::tests::grammar::normalizes_whitespace ... ok
test native::capture::tests::grammar::malformed_task_block_id_markers_are_usage_errors ... ok
test native::capture::tests::grammar::time_tokens_stay_literal_and_leading_route_wins ... ok
test native::capture::tests::placement::bare_bullet_marker_prefers_non_h1_section ... ok
test native::capture::tests::placement::bare_bullet_marker_ignores_exact_flag ... ok
test native::capture::tests::grammar::malformed_sub_bullet_markers_are_usage_errors ... ok
test native::capture::tests::placement::bare_trailing_hash_resolves_pomodoro_note ... ok
test native::capture::task_blocks::tests::authored_children_and_schedule_log_are_added_in_order ... ok
test native::capture::tests::placement::bullet_inserts_after_last_ordinary_bullet_block ... ok
test native::capture::tests::placement::bullet_inserts_after_matched_section_header ... ok
test native::capture::tests::placement::bullet_prefers_non_h1_match_over_earlier_h1_match ... ok
test native::capture::tests::placement::bullet_section_prefix_matches_case_insensitively ... ok
test native::capture::task_blocks::tests::global_batch_reports_one_block_with_two_added_rows ... ok
test native::capture::tests::grammar::malformed_named_pomodoro_markers_are_usage_errors ... ok
test native::capture::tests::placement::bare_bullet_marker_selects_first_non_tasks_section ... ok
test native::capture::tests::placement::inserts_after_single_top_level_task ... ok
test native::capture::tests::placement::inserts_multiline_capture_as_one_task_block ... ok
test native::capture::tests::placement::bullet_ignores_headings_in_frontmatter_and_fences ... ok
test native::capture::tests::placement::later_task_outside_tasks_section_does_not_win ... ok
test native::capture::tests::placement::json_success_shape_is_stable ... ok
test native::capture::tests::placement::bullet_skips_tasks_section_matching_prefix ... ok
test native::capture::tests::placement::appends_to_empty_and_no_task_files ... ok
test native::capture::tests::grammar::parses_pomodoro_routes_in_terminal_positions_with_schedules ... ok
test native::capture::tests::placement::legacy_standalone_bullet_markers_are_rejected ... ok
test native::capture::task_blocks::tests::crlf_note_reports_verbatim_texts_without_terminators ... ok
test native::capture::tests::placement::skips_indented_and_blank_then_indented_continuation_lines ... ok
test native::capture::tests::placement::suffixed_route_token_without_body_is_usage_error ... ok
test native::capture::tests::grammar::parses_priority_tokens ... ok
test native::capture::tests::grammar::parses_auto_routes_like_hammerspoon ... ok
test native::capture::tests::placement::exact_bullet_section_no_match_falls_back_to_zeroth_section ... ok
test native::capture::tests::grammar::parses_scheduled_offsets_with_routes ... ok
test native::capture::task_blocks::tests::interior_blank_lines_are_kept_in_the_block ... ok
test native::capture::tests::placement::forced_route_rejects_terminal_marker_but_keeps_middle_hashtag ... ok
test native::capture::tests::placement::formats_scheduled_date_from_offset ... ok
test native::capture::tests::grammar::parses_sub_bullet_routes_with_precedence_and_terminal_markers ... ok
test native::capture::task_blocks::tests::section_insertion_nests_the_added_row_at_depth_two ... ok
test native::capture::tests::placement::ignores_tasks_headings_in_frontmatter_and_fenced_code ... ok
test native::capture::tests::grammar::parses_named_pomodoro_routes_in_terminal_positions ... ok
test native::capture::tests::placement::inserts_after_last_of_many_task_blocks ... ok
test native::capture::tests::placement::marker_only_bullet_input_is_usage_error ... ok
test native::capture::tests::grammar::parses_picker_task_refs_strictly ... ok
test native::capture::task_blocks::tests::two_parents_forward_across_an_insert_above ... ok
test native::capture::tests::placement::formats_bullet_line ... ok
test native::capture::tests::placement::bullet_treats_checkbox_only_section_as_empty ... ok
test native::capture::tests::placement::bullet_uses_h1_match_when_no_non_h1_match_exists ... ok
test native::capture::tests::placement::exact_bullet_section_keeps_non_h1_preference ... ok
test native::capture::tests::placement::inserts_after_final_continuation_running_to_eof ... ok
test native::capture::tests::placement::forced_section_forces_exact_bullet_with_forced_route ... ok
test native::capture::tests::placement::exact_bullet_section_wins_over_prefix_sibling ... ok
test native::capture::tests::placement::nested_heading_stops_empty_tasks_section_insertion ... ok
test native::capture::tests::placement::tasks_heading_at_eof_inserts_after_blank_line ... ok
test native::capture::tests::placement::exact_bullet_section_matches_case_insensitively ... ok
test native::capture::tests::placement::parses_suffixed_route_token_as_bullet ... ok
test native::capture::tests::placement::formats_sub_bullet_line ... ok
test native::capture::tests::placement::ignores_indented_task_lines_as_insertion_anchors ... ok
test native::capture::tests::grammar::malformed_terminal_pomodoro_routes_are_usage_errors ... ok
test native::capture::tests::placement::tasks_section_wins_over_root_task_when_empty ... ok
test native::capture::tests::placement::forced_section_requires_route_and_non_empty_title ... ok
test native::capture::task_blocks::tests::nested_parent_reports_depths_relative_to_its_line ... ok
test native::capture::tests::placement::tasks_section_inserts_after_last_task_block_in_section ... ok
test native::capture::tests::started::started_pomodoro_ignores_cancelled_fenced_and_nested_anchors ... ok
test native::capture::tests::placement::tasks_section_inserts_below_generated_status_badges ... ok
test native::capture::task_blocks::tests::task_ref_parent_omits_block_id_but_reports_its_block ... ok
test native::capture::tests::placement::zeroth_section_insertion_after_frontmatter ... ok
test native::capture::tests::placement::unmatched_prefix_falls_back_to_zeroth_section ... ok
test native::capture::tests::started::non_tasks_section_headings_match_bullet_heading_scan ... ok
test native::capture::tests::started::started_pomodoro_moves_after_completed_with_grandchildren ... ok
test native::capture::tests::started::started_pomodoro_moves_before_first_open_without_completed ... ok
test native::capture::task_blocks::tests::cross_note_first_touch_order_with_revisit_and_second_parent ... ok
test native::capture::tests::started::started_pomodoro_already_in_slot_keeps_blank_line ... ok
test native::capture::tests::started::started_pomodoro_moves_down_to_eof_without_newline ... ok
test native::capture::tests::started::started_pomodoro_moves_interior_blank_line_and_keeps_trailing ... ok
test native::capture::tests::started::started_pomodoro_eof_without_newline_moves_up ... ok
test native::capture::tests::started::started_pomodoro_interleaved_moves_after_last_completed ... ok
test native::capture::tests::started::started_pomodoro_move_preserves_crlf ... ok
test native::capture::task_blocks::tests::plain_insertion_reports_one_added_row_before_schedule_log ... ok
test native::capture_active_tasks::tests::excludes_tasks_without_ids_and_closed_statuses ... ok
test native::capture_active_tasks::tests::orders_queued_first_then_wip_then_next ... ok
test native::capture_block_ids::tests::suggestions_follow_the_pinned_examples ... ok
test native::capture_complete::tests::output::build_cli_renders_without_panicking ... ok
test native::capture_block_ids::tests::used_covers_done_nontask_duplicates_and_document_order ... ok
test native::capture_complete::tests::output::empty_json_context_is_null ... ok
test native::capture_complete::tests::output::human_output_is_plain_without_color ... ok
test native::capture_complete::tests::output::json_shape_is_stable ... ok
test native::capture_block_ids::tests::allowed_regex_agrees_with_validator_for_every_ascii_char ... ok
test native::capture_complete::tests::output::empty_completion_has_no_context_and_a_zero_length_replacement ... ok
test native::capture_active_tasks::tests::clears_is_current_with_multiple_open_timed_entries ... ok
test native::capture_complete::tests::output::trailing_hash_fragment_requests_no_completion ... ok
test native::capture_active_tasks::tests::warns_when_the_day_file_is_missing ... ok
test native::capture_active_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_complete::tests::output::wikilink_completion_surfaces_bounded_index_warnings ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_offers_queued_tasks_first ... ok
test native::capture_clip::tests::aggregate_planner_does_not_alias_snippets_and_attachments ... ok
test native::capture_complete::tests::pomodoros::plan_themes_after_counts_only_fresh_non_exempt_components ... ok
test native::capture_active_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_active_tasks::tests::annotates_duplicate_links_with_the_first_owner ... ok
test native::capture_complete::tests::output::wikilink_note_completion_returns_alias_metadata_and_cursor_after ... ok
test native::capture_complete::tests::pomodoros::pomodoro_creation_json_omits_ref_and_keeps_schema_version ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_keeps_nameable_rows_for_a_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_candidates_omit_next_up ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_lists_named_then_nameable_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_for_empty_or_invalid_queries ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_offers_creation_before_substring_and_nameable_rows ... ok
test native::capture_clip::tests::detects_structural_lines ... ok
test native::capture_clip::tests::formats_headers ... ok
test native::capture_clip::tests::merges_live_clipboard_with_up_to_date_and_lagging_histories ... ok
test native::capture_active_tasks::tests::ranks_prefix_matches_before_substring_matches ... ok
test native::capture_clip::tests::normalizes_clipboard_text_and_rejects_binary_or_empty ... ok
test native::capture_clip::tests::percent_decodes_file_uris ... ok
test native::capture_clip::tests::flat_unordered_lists_keep_the_inline_line_boundary ... ok
test native::capture_clip::tests::recognizes_and_renders_flat_unordered_lists ... ok
test native::capture_clip::tests::sanitizes_attachment_names_and_builds_slugs ... ok
test native::capture_active_tasks::tests::excludes_ready_tasks_even_with_now_text ... ok
test native::capture_clip::tests::renders_inline_lines_and_long_text_modes ... ok
test native::capture_complete::tests::active_tasks::active_task_human_rows_name_the_queue ... ok
test native::capture_complete::tests::output::wikilink_completion_takes_precedence_over_marker_text_inside_link ... ok
test native::capture_clip::tests::tab_indent_renders_every_clipboard_shape ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_capture_route_then_inbox_fallback ... ok
test native::capture_clip::tests::unsafe_or_incomplete_unordered_lists_remain_snippets ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_skips_creation_when_the_ledger_cannot_place_it ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_suppresses_creation_for_open_name_matches ... ok
test native::capture_clip::tests::classifies_paths_structured_text_and_attachment_limits ... ok
test native::capture_complete::tests::output::wikilink_same_note_heading_uses_the_cursor_item_route ... ok
test native::capture_complete::tests::output::close_items_and_suffixes_request_no_completion ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_missing_daily_note_warns ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_treats_plus_names_as_named_not_nameable ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_badge_creation ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_human_rows_include_time_and_badges ... ok
test native::capture_complete::tests::output::close_bullet_lines_suppress_wikilink_block_but_keep_note ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_filters_and_creates_by_query ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_again_rows_preview_plan_budget ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_lists_start_again_and_name_it_rows ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_human_labels_cover_every_row_kind ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_puts_the_running_entry_last ... ok
test native::capture_complete::tests::pomodoros::pomodoro_start_name_matches_pomodoro_name_warnings ... ok
test native::capture_complete::tests::routes_tasks::route_completion_lists_every_target_for_an_empty_query ... ok
test native::capture_complete::tests::routes_tasks::section_completion_on_a_missing_note_is_an_empty_success ... ok
test native::capture_complete::tests::routes_tasks::section_completion_lists_headings_of_the_resolved_route ... ok
test native::capture_complete::tests::routes_tasks::route_completion_ranks_prefix_matches_before_substring_matches ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_lists_identified_tasks_before_unidentified_tasks ... ok
test native::capture_complete::tests::routes_tasks::default_task_completion_stays_identified_only ... ok
test native::capture_dependency_tasks::tests::hidden_tasks_detect_only_the_exact_tag ... ok
test native::capture_complete::tests::routes_tasks::sub_bullet_task_completion_reports_full_task_metadata ... ok
test native::capture_dependency_tasks::tests::quoted_locator_round_trips_through_replacement ... ok
test native::capture_complete::tests::routes_tasks::task_block_id_completion_offers_routes_but_not_authored_ids ... ok
test native::capture_language::close_log::tests::assign_log_positions_follows_the_assignment_rule ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_empty_block_id_is_an_empty_success ... ok
test native::capture_language::close_log::tests::first_bullet_kind_detection_skips_placeholders ... ok
test native::capture_language::close_log::tests::default_log_index_covers_every_close_shape ... ok
test native::capture_language::close_log::tests::inline_entry_defaults_and_leading_numbers ... ok
test native::capture_language::close_log::tests::inline_entry_reports_dangling ... ok
test native::capture_language::close_log::tests::inline_entry_reports_diagnostics_in_order ... ok
test native::capture_language::close_log::tests::lexes_entries_and_details ... ok
test native::capture_complete::tests::routes_tasks::pomodoro_block_id_completion_only_offers_tasks_with_a_block_id ... ok
test native::capture_language::close_log::tests::mixed_numbering_fails_both_orders ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_does_not_change_pomodoro_completion ... ok
test native::capture_language::close_log::tests::positional_entries_carry_their_typed_position ... ok
test native::capture_complete::tests::routes_tasks::all_tasks_search_keeps_identified_groups_ahead_of_unidentified ... ok
test native::capture_complete::tests::routes_tasks::task_completion_before_an_explicit_toggle_bang_does_not_replace_the_bang ... ok
test native::capture_language::close_log::tests::rejects_bad_bullets ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_report_lexical_failures ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_stay_unresolved_without_a_selection ... ok
test native::capture_language::close_log::tests::unnumbered_bullets_resolve_positionally_in_selection_mode ... ok
test native::capture_language::close_log::tests::reports_dangling ... ok
test native::capture_language::close_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::close_selection::tests::lex_reports_drop_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_short_alias_wildcards ... ok
test native::capture_language::close_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::close_selection::tests::lex_reports_valid_selections ... ok
test native::capture_language::close_selection::tests::lex_reports_park_selections ... ok
test native::capture_language::close_selection::tests::selection_shape_detection ... ok
test native::capture_language::dependencies::tests::bare_sigil_is_directive_only_at_the_ends ... ok
test native::capture_dependency_tasks::tests::unique_basename_resolves_before_ambiguous_paths ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_warns_once_for_an_unresolvable_parent ... ok
test native::capture_complete::tests::routes_tasks::three_component_marker_keeps_route_and_task_contexts ... ok
test native::capture_language::dependencies::tests::escape_consumes_only_its_backslash ... ok
test native::capture_language::dependencies::tests::mid_line_modifiers_stay_literal ... ok
test native::capture_language::dependencies::tests::protected_spans_are_never_modifiers ... ok
test native::capture_language::dependencies::tests::quoted_escapes_decode ... ok
test native::capture_language::dependencies::tests::quoted_note_with_spaces_stays_atomic ... ok
test native::capture_language::dependencies::tests::trailing_complete_modifier_strips_and_spans ... ok
test native::capture_complete::tests::routes_tasks::task_section_completion_lists_ranked_slugs_for_the_parent_task ... ok
test native::capture_language::dependencies::tests::traversal_and_bad_ids_are_invalid ... ok
test native::capture_language::dependencies::tests::unicode_offsets_stay_on_char_boundaries ... ok
test native::capture_language::dependencies::tests::unterminated_quote_is_one_partial ... ok
test native::capture_language::project_tasks::tests::lexer_accepts_the_boundary_set ... ok
test native::capture_language::project_tasks::tests::reserved_name_matches_in_any_letter_case ... ok
test native::capture_language::project_tasks::tests::suffix_helpers_split_on_the_last_word ... ok
test native::capture_language::start_selection::tests::lex_reports_dangling_separators_as_incomplete ... ok
test native::capture_language::start_selection::tests::lex_reports_precise_diagnostics ... ok
test native::capture_language::start_selection::tests::lex_reports_valid_drop_lists ... ok
test native::capture_language::tests::chain::chain_token_predicate_covers_the_documented_table ... ok
test native::capture_dependency_tasks::tests::ranking_shares_the_tiered_matcher_vectors ... ok
test native::capture_language::tests::chain::draft_attaches_chain_child_lines_to_the_close ... ok
test native::capture_dependency_tasks::tests::groups_follow_the_picker_sections ... ok
test native::capture_language::tests::chain::draft_chain_works_with_a_global_declaration ... ok
test native::capture_language::tests::chain::completion_requests_nothing_anywhere_on_a_chain ... ok
test native::capture_language::tests::chain::draft_keeps_sequential_indices_across_crlf_with_a_chain ... ok
test native::capture_language::tests::chain::draft_splits_a_two_token_chain_with_absolute_ranges ... ok
test native::capture_language::tests::chain::chain_token_predicate_equals_claimed_for_single_tokens ... ok
test native::capture_language::tests::chain::draft_splits_tabs_and_runs_of_spaces ... ok
test native::capture_language::tests::chain::editor_chain_items_do_not_inherit_a_global_declaration ... ok
test native::capture_language::tests::chain::editor_reports_a_broken_second_token_with_its_own_diagnostic ... ok
test native::capture_complete::tests::parent_tasks::bare_plus_serves_vault_candidates_and_operator_hints ... ok
test native::capture_language::tests::chain::editor_reports_a_dangling_close_separator_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_chain_with_absolute_spans ... ok
test native::capture_dependency_tasks::tests::catalog_covers_every_task_bearing_note_kind ... ok
test native::capture_language::tests::chain::editor_reports_a_named_start_plus_adjustment_chain ... ok
test native::capture_dependency_tasks::tests::empty_query_orders_same_note_lanes_history ... ok
test native::capture_language::tests::chain::editor_reports_selection_spans_at_absolute_offsets_in_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_an_incomplete_named_start_inside_a_chain ... ok
test native::capture_language::tests::chain::editor_reports_two_items_with_absolute_spans_for_a_chain ... ok
test native::capture_language::tests::chain::execution_attaches_chain_child_lines_to_the_close ... ok
test native::capture_language::tests::chain::execution_carries_a_close_selection_through_a_chain ... ok
test native::capture_language::tests::chain::execution_distinguishes_spaced_start_adjust_from_offset_start ... ok
test native::capture_language::tests::chain::execution_reports_a_broken_second_token_on_its_own_range ... ok
test native::capture_language::tests::chain::execution_leaves_non_chains_unchanged ... ok
test native::capture_language::tests::chain::execution_rejects_forced_destinations_on_the_first_chain_token ... ok
test native::capture_language::tests::chain::execution_switches_sessions_with_close_then_start ... ok
test native::capture_language::tests::chain::execution_runs_a_chain_left_to_right ... ok
test native::capture_language::tests::completion::bare_at_completes_an_empty_route ... ok
test native::capture_language::tests::completion::completion_inside_a_child_bullet_marker_has_no_completion ... ok
test native::capture_language::tests::completion::completion_inside_an_item_stays_item_local_with_a_global_declaration ... ok
test native::capture_language::tests::completion::completion_field_uses_byte_offsets_after_multibyte_prefix_text ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_never_offers_a_leading_route ... ok
test native::capture_language::tests::completion::completion_on_a_global_declaration_excludes_both_sigils_and_plus ... ok
test native::capture_language::tests::completion::block_id_project_note_sigil_is_excluded_from_replacement ... ok
test native::capture_language::tests::completion::completion_on_a_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_on_a_nested_child_line_completes_a_trailing_route ... ok
test native::capture_language::tests::completion::completion_on_nested_prefix_or_orphaned_nested_line_is_empty ... ok
test native::capture_language::tests::completion::completion_on_the_parent_line_still_supports_leading_markers ... ok
test native::capture_language::tests::completion::cursor_in_body_text_has_no_completion ... ok
test native::capture_language::tests::completion::completion_works_on_an_earlier_child_line_not_only_the_last ... ok
test native::capture_language::tests::completion::cursor_past_a_trailing_space_has_no_completion ... ok
test native::capture_language::tests::completion::cursor_mid_route_fragment_uses_the_prefix_before_the_cursor ... ok
test native::capture_language::tests::completion::cursor_on_a_middle_token_has_no_completion ... ok
test native::capture_language::tests::completion::cursor_in_route_or_block_id_of_three_component_marker_keeps_existing_contexts ... ok
test native::capture_language::tests::completion::empty_block_id_with_section_still_yields_a_task_section_field ... ok
test native::capture_language::tests::completion::empty_selector_after_hash_is_a_zero_length_task_section_field ... ok
test native::capture_language::tests::completion::leading_route_fragment_completes_with_no_body_yet ... ok
test native::capture_language::tests::completion::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::capture_language::tests::completion::legacy_pomodoro_alias_completes_the_same_as_the_canonical_form ... ok
test native::capture_language::tests::completion::invalid_block_id_characters_still_produce_a_field ... ok
test native::capture_language::tests::completion::missing_route_portion_of_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_pomodoro_marker_completes_a_route ... ok
test native::capture_language::tests::completion::leading_three_component_marker_completes_each_component ... ok
test native::capture_language::tests::completion::explicit_toggle_task_completion_replacement_ends_before_the_bang ... ok
test native::capture_language::tests::completion::completion_field_stays_on_unicode_scalar_boundaries ... ok
test native::capture_language::tests::completion::hash_separator_is_not_part_of_block_id_or_section_replacement ... ok
test native::capture_language::tests::completion::pomodoro_block_id_completes_after_a_resolved_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_sub_bullet_marker_completes_a_route ... ok
test native::capture_language::tests::completion::missing_route_portion_of_task_block_id_marker_completes_a_route ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_per_token_inside_chains ... ok
test native::capture_language::tests::completion::operator_items_have_no_hash_completion ... ok
test native::capture_language::tests::completion::pomodoro_name_completes_after_hash_even_without_a_block_id ... ok
test native::capture_language::tests::completion::parent_task_plus_completes_the_terminal_token_with_utf8_byte_ranges ... ok
test native::capture_language::tests::completion::pomodoro_name_completion_keeps_route_and_id_contexts ... ok
test native::capture_language::tests::completion::pomodoro_start_name_completes_after_hash_on_a_named_start ... ok
test native::capture_language::tests::completion::completion_field_stays_on_boundaries_of_a_three_component_marker ... ok
test native::capture_language::tests::completion::parent_task_plus_is_shared_across_parent_and_authored_lines ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_lone_colon ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_caret_id ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_a_partial_id ... ok
test native::capture_language::tests::completion::project_task_block_id_completes_only_first_level_project_bullets ... ok
test native::capture_language::tests::completion::project_task_id_before_a_child_line_route_marker_still_completes ... ok
test native::capture_language::tests::completion::parent_task_plus_preserves_operator_and_protected_text_boundaries ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_first_level_and_nested_items ... ok
test native::capture_language::tests::completion::pomodoro_start_name_leaves_link_form_names_alone ... ok
test native::capture_language::tests::draft::authored_line_classifier_rejects_every_other_shape ... ok
test native::capture_language::tests::draft::editor_child_line_alone_can_resolve_the_capture_mode ... ok
test native::capture_language::tests::draft::editor_child_line_markers_extend_spans_with_absolute_offsets ... ok
test native::capture_language::tests::completion::section_completes_after_a_resolved_route ... ok
test native::capture_language::tests::draft::editor_diagnoses_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::completion::retired_double_colon_marker_has_no_completion_field ... ok
test native::capture_language::tests::completion::right_component_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_invalid_child_line_without_failing ... ok
test native::capture_language::tests::draft::editor_diagnoses_an_orphaned_nested_child_without_failing ... ok
test native::capture_language::tests::completion::task_completes_after_a_resolved_sub_bullet_route ... ok
test native::capture_language::tests::draft::editor_placeholder_child_lines_produce_no_sub_bullet_or_diagnostic ... ok
test native::capture_language::tests::draft::editor_diagnoses_duplicate_markers_across_lines_but_keeps_the_first ... ok
test native::capture_language::tests::draft::editor_reports_nested_sub_bullets_and_depths ... ok
test native::capture_language::tests::draft::editor_reports_sub_bullets_for_a_multiline_draft ... ok
test native::capture_language::tests::completion::pomodoro_completion_ranges_end_before_the_start_suffix ... ok
test native::capture_complete::tests::parent_tasks::plus_query_ranks_candidates_and_scoped_descriptors_keep_exact_ranges ... ok
test native::capture_language::tests::completion::task_block_id_route_and_authored_id_both_complete ... ok
test native::capture_language::tests::completion::task_section_completes_after_hash_on_a_sub_bullet_marker ... ok
test native::capture_language::tests::draft::execution_allows_the_same_marker_kind_once_across_the_whole_draft ... ok
test native::capture_language::tests::draft::execution_batch_parser_prefixes_item_and_line_context ... ok
test native::capture_language::tests::completion::terminal_markers_do_not_interfere_with_route_completion ... ok
test native::capture_language::tests::completion::task_link_query_completes_the_sigil_inclusive_token ... ok
test native::capture_language::tests::draft::execution_composes_a_trailing_marker_from_any_child_line ... ok
test native::capture_language::tests::draft::execution_forced_route_keeps_child_markers_literal ... ok
test native::capture_language::tests::draft::execution_nested_placeholders_do_not_require_or_clear_an_owner ... ok
test native::capture_language::tests::draft::execution_rejects_a_child_emptied_by_marker_removal ... ok
test native::capture_language::tests::draft::execution_preserves_unicode_child_bodies ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_global_declarations_by_line ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_route_markers_across_lines ... ok
test native::capture_language::tests::completion::three_component_right_side_without_a_resolved_route_has_no_completion ... ok
test native::capture_language::tests::completion::trailing_hash_fragments_have_no_completion ... ok
test native::capture_language::tests::draft::execution_rejects_indented_or_deeper_child_lines ... ok
test native::capture_language::tests::draft::execution_rejects_duplicate_schedule_priority_and_clip_markers_across_lines ... ok
test native::capture_language::tests::completion::work_log_bullet_lines_request_no_marker_completion ... ok
test native::capture_language::tests::draft::authored_line_classifier_accepts_placeholders_without_items ... ok
test native::capture_language::tests::draft::execution_renders_authored_children_in_source_order ... ok
test native::capture_language::tests::draft::execution_rejects_orphaned_nested_child_lines ... ok
test native::capture_language::tests::editor_modes::editor_reports_task_link_queries_as_incomplete ... ok
test native::capture_language::tests::draft::execution_rejects_nonbullet_continuation_prose ... ok
test native::capture_language::tests::draft::execution_skips_placeholder_child_lines ... ok
test native::capture_language::tests::editor_spans::diagnostics_serialize_with_a_nullable_range_pair ... ok
test native::capture_language::tests::draft::execution_single_item_parser_rejects_blank_line_batches ... ok
test native::capture_language::tests::editor_spans::editor_leading_marker_wins_over_trailing_marker ... ok
test native::capture_language::tests::draft::split_capture_draft_reports_ranges_and_ignores_separator_runs ... ok
test native::capture_language::tests::editor_spans::editor_keeps_middle_and_time_tokens_literal ... ok
test native::capture_language::tests::editor_spans::editor_accepts_marker_only_input_with_an_empty_body ... ok
test native::capture_language::tests::draft::execution_tracks_nested_children_under_the_nearest_first_level_owner ... ok
test native::capture_language::tests::editor_spans::editor_normalizes_intra_line_whitespace_like_execution ... ok
test native::capture_language::tests::draft::split_physical_lines_drops_only_one_trailing_terminator ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_partial_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::draft::split_physical_lines_reports_byte_offsets_excluding_terminators ... ok
test native::capture_language::tests::editor_spans::editor_leaves_caret_lookalikes_and_prose_literal ... ok
test native::capture_language::tests::draft::split_physical_lines_treats_lf_crlf_and_bare_cr_as_terminators ... ok
test native::capture_complete::tests::parent_tasks::scoped_missing_and_empty_notes_keep_picker_and_empty_catalog ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::editor_reports_legacy_bullet_markers_without_failing ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_partials_as_incomplete ... ok
test native::capture_language::tests::editor_spans::editor_reports_caret_near_misses_and_conflicts ... ok
test native::capture_language::tests::editor_modes::editor_holds_unused_pomodoro_while_a_colon_id_is_unfinished ... ok
test native::capture_language::tests::editor_modes::editor_rejects_checkbox_only_project_task_ids_over_the_id_token ... ok
test native::capture_language::tests::editor_modes::caret_close_conflicts_agree_with_execution ... ok
test native::capture_language::tests::editor_modes::editor_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::editor_modes::interactive_markers_are_the_only_divergence_from_execution ... ok
test native::capture_language::tests::editor_spans::editor_reports_invalid_components_as_diagnostics ... ok
test native::capture_language::tests::editor_modes::editor_spans_cover_every_marker_shape ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_start_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_never_applies_global_destination_to_caret_items ... ok
test native::capture_language::tests::editor_spans::editor_reports_terminal_marker_spans ... ok
test native::capture_language::tests::editor_modes::editor_reports_named_pomodoro_start_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::editor_spans::editor_serializes_snake_case_vocabulary ... ok
test native::capture_language::tests::draft::execution_treats_crlf_and_bare_cr_children_like_lf ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_now_tag_without_task_text ... ok
test native::capture_language::tests::editor_spans::editor_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::editor_modes::editor_reports_unused_project_note_pomodoro_over_the_name ... ok
test native::capture_language::tests::editor_spans::editor_reports_retired_double_colon_as_migration_guidance ... ok
test native::capture_language::tests::editor_modes::pomodoro_start_suffix_reports_spec_and_non_overlapping_spans ... ok
test native::capture_language::tests::editor_spans::editor_spans_use_original_byte_offsets_after_multibyte_text ... ok
test native::capture_language::tests::editor_spans::tokenizer_records_half_open_byte_spans ... ok
test native::capture_language::tests::editor_spans::task_link_query_spans_the_whole_token_as_a_placeholder ... ok
test native::capture_language::tests::editor_spans::editor_reports_solo_at_pomodoro_links ... ok
test native::capture_language::tests::editor_spans::tokenizer_keeps_multibyte_and_crlf_offsets_on_char_boundaries ... ok
test native::capture_language::tests::editor_modes::editor_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_language::tests::globals::execution_accepts_a_later_declaration_only_line ... ok
test native::capture_language::tests::editor_spans::plan_worked_example_matches_documented_offsets ... ok
test native::capture_language::tests::editor_modes::editor_modes_and_needs_cover_every_marker_shape ... ok
test native::capture_language::tests::globals::execution_an_ensure_next_item_participates_normally_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_rejects_a_declaration_only_draft ... ok
test native::capture_language::tests::globals::execution_an_explicit_toggle_item_participates_in_a_multi_item_draft ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_sub_bullet_and_keeps_authored_children ... ok
test native::capture_language::tests::globals::execution_inherits_a_global_task_route_unless_an_item_overrides ... ok
test native::capture_language::tests::globals::execution_strips_inline_declarations_before_terminal_markers ... ok
test native::capture_language::tests::globals::split_capture_draft_ignores_leading_blanks_and_crlf ... ok
test native::capture_language::tests::editor_spans::mixed_separators_keep_the_first_family_and_do_not_steal_section_suffixes ... ok
test native::capture_language::tests::globals::split_capture_draft_strips_declaration_only_lines ... ok
test native::capture_language::tests::globals::execution_warns_when_a_local_marker_shadows_its_declaration ... ok
test native::capture_language::tests::globals::execution_rejects_unsupported_global_forms ... ok
test native::capture_language::tests::globals::execution_local_markers_override_a_global_declaration ... ok
test native::capture_language::tests::editor_modes::editor_reports_project_task_ids_with_modes_spans_and_diagnostics ... ok
test native::capture_language::tests::grammar::a_toggle_with_body_text_stays_a_sub_bullet_marker ... ok
test native::capture_language::tests::grammar::a_terminal_bang_on_a_marker_only_toggle_is_explicit_toggle ... ok
test native::capture_language::tests::grammar::execution_forced_route_keeps_retired_and_special_markers_literal ... ok
test native::capture_language::tests::grammar::a_bare_sub_bullet_marker_becomes_a_task_toggle ... ok
test native::capture_language::tests::grammar::execution_evaluates_project_note_markers_parents_and_children_in_order ... ok
test native::capture_language::tests::grammar::execution_keeps_equals_wording_off_caret_tokens_without_plus ... ok
test native::capture_language::tests::grammar::execution_keeps_task_id_lookalikes_literal_outside_project_notes ... ok
test native::capture_language::tests::grammar::execution_keeps_other_trailing_hash_tags_rejected ... ok
test native::capture_language::tests::editor_spans::normalize_task_text_still_collapses_newlines_as_whitespace ... ok
test native::capture_language::tests::globals::editor_reports_incomplete_and_declaration_only_globals ... ok
test native::capture_language::tests::globals::editor_item_at_uses_the_inherited_global_route ... ok
test native::capture_language::tests::globals::editor_inherits_global_destination_and_keeps_local_overrides ... ok
test native::capture_language::tests::grammar::execution_ordinary_single_line_capture_has_no_sub_bullets ... ok
test native::capture_language::tests::grammar::execution_keeps_pomodoro_note_and_other_families_unchanged ... ok
test native::capture_language::tests::grammar::execution_parses_project_note_markers ... ok
test native::capture_language::tests::grammar::execution_parses_equals_family_starts_alongside_close ... ok
test native::capture_language::tests::grammar::execution_accepts_project_task_ids_and_strips_them_from_bodies ... ok
test native::capture_language::tests::grammar::global_declaration_rejects_project_note_shapes ... ok
test native::capture_language::tests::grammar::execution_plus_sub_bullet_does_not_conflict_with_authored_plus_child ... ok
test native::capture_language::tests::editor_modes::editor_agrees_with_execution_for_resolved_captures ... ok
test native::capture_language::tests::grammar::lua_accepts_legacy_boundary_aliases ... ok
test native::capture_language::tests::grammar::lua_gives_sub_bullet_markers_precedence_over_pomodoro_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_a_trailing_now_tag_like_any_other_tag ... ok
test native::capture_language::tests::grammar::execution_rejects_checkbox_only_project_task_ids ... ok
test native::capture_language::tests::grammar::execution_parses_three_component_sub_bullet_markers ... ok
test native::capture_language::tests::grammar::lua_clipboard_composition_body_follows_bob_terminal_extraction ... ok
test native::capture_language::tests::grammar::lua_keeps_middle_markers_literal_and_marker_only_bodies_empty ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_pomodoro_forms ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_task_block_id_forms ... ok
test native::capture_language::tests::grammar::explicit_toggle_near_misses_have_focused_diagnostics ... ok
test native::capture_language::tests::grammar::lua_leaves_invalid_or_unsupported_terminal_regions_to_bob_capture ... ok
test native::capture_language::tests::grammar::execution_rejects_route_less_retired_project_note_markers ... ok
test native::capture_language::tests::grammar::lua_preserves_existing_note_and_section_descriptors ... ok
test native::capture_language::tests::grammar::execution_retired_double_colon_is_a_usage_error ... ok
test native::capture_language::tests::grammar::lua_parses_all_four_canonical_sub_bullet_forms ... ok
test native::capture_language::tests::grammar::lua_rejects_invalid_sub_bullet_and_pomodoro_components ... ok
test native::capture_language::tests::grammar::lua_preserves_crossed_clipboard_and_schedule_markers ... ok
test native::capture_language::tests::grammar::execution_rejects_project_note_shape_errors ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_parent_lines_marker_from_a_child_lines_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_sub_bullet_local_marker ... ok
test native::capture_language::tests::grammar::execution_three_component_marker_composes_on_multiline_first_line_only ... ok
test native::capture_language::tests::rewrite::rewrite_draft_declines_when_the_item_has_two_local_markers ... ok
test native::capture_language::tests::grammar::marker_only_task_toggle_spellings_are_a_three_way_intent_matrix ... ok
test native::capture_language::tests::grammar::project_note_markers_stay_in_their_families ... ok
test native::capture_language::tests::grammar::plus_parent_picker_does_not_claim_operators_or_work_log_text ... ok
test native::capture_language::tests::grammar::execution_rejects_project_task_id_rule_violations_verbatim ... ok
test native::capture_language::tests::grammar::plus_parent_picker_is_incomplete_but_keeps_the_lone_adjustment ... ok
test native::capture_language::tests::grammar::task_link_query_leaves_prose_byte_identical ... ok
test native::capture_language::tests::grammar::plus_in_a_pomodoro_name_does_not_select_the_sub_bullet_family ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_trailing_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_a_no_op_without_a_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_avoids_double_spaces_and_the_result_parses_cleanly ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_declaration_only_line_into_a_later_items_bare_at_at ... ok
test native::capture_language::tests::rewrite::rewrite_draft_absorbs_a_leading_local_marker ... ok
test native::capture_language::tests::rewrite::rewrite_draft_is_idempotent ... ok
test native::capture_language::tests::grammar::task_link_query_rejects_single_colon_tokens_with_teaching_errors ... ok
test native::capture_language::tests::rewrite::rewrite_draft_keeps_offsets_on_char_boundaries_with_multibyte_input ... ok
test native::capture_link_tasks::tests::ranker_orders_by_tier_sum_then_canonical_order ... ok
test native::capture_language::tests::rewrite::rewrite_draft_selects_the_bare_at_at_under_the_cursor_else_the_last ... ok
test native::capture_language::tests::grammar::task_link_claim_is_equivalent_across_execution_editor_and_completion ... ok
test native::capture_link_tasks::tests::ranker_passes_the_dependency_contract_dk_vectors ... ok
test native::capture_language::tests::rewrite::rewrite_draft_reports_rule_a5_notices_for_non_absorbable_markers ... ok
test native::capture_links::tests::scanner_recovers_from_nested_openers ... ok
test native::capture_links::tests::scans_complete_incomplete_embed_and_subpath_spans ... ok
test native::capture_links::tests::scanner_ignores_escaped_and_code_literal_links ... ok
test native::capture_parse::tests::build_cli_renders_without_panicking ... ok
test native::capture_parse::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_parse::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_parse::tests::cli_keeps_hyphenated_text_literal_like_bob_capture ... ok
test native::capture_links::tests::note_completion_deduplicates_existing_close_and_synthesizes_missing_close ... ok
test native::capture_parse::tests::format_pomodoro_close_describes_wildcard_scope ... ok
test native::capture_parse::tests::format_pomodoro_close_reports_detail_counts ... ok
test native::capture_links::tests::index_skips_hidden_generated_template_and_symlink_directories ... ok
test native::capture_parse::tests::json_ignores_wikilinks_inside_code_literals ... ok
test native::capture_links::tests::heading_and_block_completion_resolve_target_same_note_and_vault_scope ... ok
test native::capture_parse::tests::json_reports_a_declaration_only_draft_as_a_diagnostic ... ok
test native::capture_parse::tests::cli_rejects_an_unknown_format ... ok
test native::capture_parse::tests::human_output_is_plain_without_color ... ok
test native::capture_parse::tests::json_reports_batch_items_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_a_global_sub_bullet_declaration_and_local_override ... ok
test native::capture_parse::tests::json_reports_an_inherited_global_destination_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_invalid_start_suffixes_as_diagnostics ... ok
test native::capture_parse::tests::missing_text_uses_the_shared_capture_message ... ok
test native::capture_link_tasks::tests::warns_for_unreadable_notes_and_keeps_other_candidates ... ok
test native::capture_parse::tests::json_reports_per_item_start_suffixes_for_batches ... ok
test native::capture_link_tasks::tests::suggestions_avoid_used_ids_including_non_task_anchors ... ok
test native::capture_parse::tests::spans_stay_ordered_and_on_character_boundaries ... ok
test native::capture_parse::tests::json_reports_diagnostics_with_a_range_pair ... ok
test native::capture_link_tasks::tests::excludes_closed_unknown_terminal_untyped_and_unroutable ... ok
test native::capture_link_tasks::tests::warns_when_the_day_file_is_missing_but_lists_tasks ... ok
test native::capture_parse::tests::json_reports_named_pomodoro_starts ... ok
test native::capture_link_tasks::tests::pulls_forward_only_for_a_single_future_scheduled_field ... ok
test native::capture_parse::tests::json_shape_is_stable ... ok
test native::capture_parse::tests::json_reports_wikilink_semantic_spans_without_changing_capture_body ... ok
test native::capture_parse::tests::json_reports_pomodoro_name_spans_needs_and_diagnostics ... ok
test native::capture_parse::tests::json_reports_the_additive_start_suffix_without_bumping_schema ... ok
test native::capture_parse::tests::json_reports_retired_double_colon_as_a_diagnostic ... ok
test native::capture_parse::tests::json_reports_every_mode_and_marker_kind ... ok
test native::capture_link_tasks::tests::warns_when_the_pomodoros_section_is_missing ... ok
test native::capture_link_tasks::tests::ranker_matches_the_worked_example_queries ... ok
test native::capture_parse::tests::json_reports_pomodoro_close_modes_spans_specs_and_diagnostics ... ok
test native::capture_pomodoro_close::linked_task_tests::closing_a_dependent_leaves_depends_on_prerequisites_open ... ok
test native::capture_pomodoro_close::linked_task_tests::mentioned_first_bare_link_gets_number_and_blocked_warning ... ok
test native::capture_language::tests::grammar::lua_composes_clipboard_terminal_markers_around_every_picker_token ... ok
test native::capture_pomodoro_close::linked_task_tests::close_plan_preserves_crlf_in_changed_task_notes ... ok
test native::capture_links::tests::note_completion_ranks_aliases_stems_paths_and_limits_empty_queries ... ok
test native::capture_pomodoro_close::linked_task_tests::listed_duplicate_embedded_and_plain_warns_once_for_not_completed ... ok
test native::capture_pomodoro_close::linked_task_tests::same_task_numbered_twice_carries_lowest_number ... ok
test native::capture_pomodoro_close::linked_task_tests::blocked_done_and_in_progress_bare_targets_are_not_started ... ok
test native::capture_pomodoro_close::linked_task_tests::recursively_closes_embedded_tasks_and_retires_closed_ledger_embeds ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_appends_after_existing_descendants ... ok
test native::capture_link_tasks::tests::worked_example_lists_eight_rows_in_canonical_order ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_listed_row_warns_exactly_once ... ok
test native::capture_pomodoro_close::linked_task_tests::custom_in_progress_symbol_gets_no_listed_warning ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_ambiguous_duplicate_and_non_task_links_warn_and_skip ... ok
test native::capture_pomodoro_close::linked_task_tests::unresolved_typed_target_warns_and_stays_in_pomodoro ... ok
test native::capture_pomodoro_close::selection_tests::conflicting_duplicates_fail_and_same_outcome_passes ... ok
test native::capture_pomodoro_close::linked_task_tests::day_file_can_also_be_a_task_note_and_receives_its_work_log ... ok
test native::capture_pomodoro_close::selection_tests::embedded_hash_alias_and_tomato ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_child_indent_follows_first_child_or_link_indent ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::selection_tests::fenced_links_are_unnumbered ... ok
test native::capture_pomodoro_close::selection_tests::drop_removes_from_closed_session_without_carry ... ok
test native::capture_pomodoro_close::selection_tests::lexically_resolved_positional_entry_reports_nested_wording ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_on_complete_target_land_in_completed_task ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_nest_undated_in_task_work_log ... ok
test native::capture_pomodoro_close::selection_tests::log_entries_keep_typed_order_for_repeated_index ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_lands_in_task_work_log_as_typed_subset ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_details_align_with_typed_entries ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_in_progress_and_complete_updates_both_tasks ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_text_that_numbers_a_link_fails_loudly ... ok
test native::capture_pomodoro_close::selection_tests::mixed_lines_are_unnumbered ... ok
test native::capture_pomodoro_close::linked_task_tests::selection_complete_writes_done_task_with_completion_date ... ok
test native::capture_pomodoro_close::selection_tests::numbers_the_worked_example ... ok
test native::capture_pomodoro_close::selection_tests::apply_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::linked_task_tests::typed_entry_on_complete_target_lands_in_completed_task ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_with_one_and_zero_links ... ok
test native::capture_complete::tests::parent_tasks::unicode_duplicates_and_queued_pomodoros_stay_in_catalog ... ok
test native::capture_pomodoro_close::selection_tests::outcome_table_covers_every_row ... ok
test native::capture_pomodoro_close::selection_tests::out_of_range_messages ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_resolve_against_session_worked_links ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_share_a_single_worked_link ... ok
test native::capture_pomodoro_close::selection_tests::none_is_byte_identical_to_plan_ledger_close ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_skip_nested_links ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_accepts_an_empty_lineup_but_explicit_positive_indices_do_not ... ok
test native::capture_pomodoro_close::selection_tests::rewrite_keeps_prefix_and_drops_tomato ... ok
test native::capture_pomodoro_close::selection_tests::positional_entries_follow_drop_and_complete_outcomes ... ok
test native::capture_pomodoro_close::selection_tests::parked_links_record_work_but_are_not_carried ... ok
test native::capture_pomodoro_close::selection_tests::listed_blocked_and_done_warnings ... ok
test native::capture_pomodoro_close::selection_tests::positional_resolution_reports_session_failures ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_positional_logs_wait_for_and_use_top_level_worked_lineup ... ok
test native::capture_pomodoro_close::linked_task_tests::worked_example_updates_tasks_and_writes_dated_work_logs ... ok
test native::capture_pomodoro_close::selection_tests::wildcard_outcomes_cover_remaining_numbered_links_and_keep_exceptions ... ok
test native::capture_pomodoro_close::tests::deferred_line_leaves_orphaned_children ... ok
test native::capture_pomodoro_close::tests::fenced_lines_are_untouched ... ok
test native::capture_pomodoro_close::tests::deferred_lookalikes_are_not_removed ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x2 ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x_complete ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x1_complete_2 ... ok
test native::capture_pomodoro_close::tests::midnight_crossing_range_uses_signed_remaining ... ok
test native::capture_complete::tests::parent_tasks::vault_catalog_excludes_non_capture_and_terminal_notes ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_preserve_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_preserves_crlf_and_missing_final_newline ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_details_nest_one_level_under_the_entry ... ok
test native::capture_pomodoro_close::selection_tests::nested_bare_links_are_numbered ... ok
test native::capture_pomodoro_close::tests::missing_section_is_an_error ... ok
test native::capture_pomodoro_close::selection_tests::log_entry_errors ... ok
test native::capture_pomodoro_close::tests::no_open_timed_entry_reports_next_placeholder ... ok
test native::capture_pomodoro_close::tests::multiple_open_timed_entries_are_an_error ... ok
test native::capture_pomodoro_close::selection_tests::ledger_post_image_for_x0_and_x1_2 ... ok
test native::capture_pomodoro_close::tests::nothing_carried_with_later_entry_creates_nothing ... ok
test native::capture_pomodoro_close::tests::no_decrement_when_fewer_than_five_minutes_remain ... ok
test native::capture_pomodoro_close::tests::nested_worked_on_links_keep_their_indent_when_carried ... ok
test native::capture_pomodoro_close::tests::start_in_the_future_clamps_to_zero_minutes ... ok
test native::capture_pomodoro_close::tests::range_cuts_at_a_blank_line ... ok
test native::capture_pomodoro_close::tests::preserves_crlf ... ok
test native::capture_pomodoro_close::tests::unnamed_empty_last_entry_creates_placeholder_and_stub ... ok
test native::capture_pomodoro_close::tests::true_deferred_hash_is_removed_and_carried_without_hash ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_excludes_ready_tasks ... ok
test native::capture_pomodoro_close::tests::preserves_missing_final_newline ... ok
test native::capture_pomodoro_close::tests::struck_markers_collapse_and_embedded_drop ... ok
test native::capture_pomodoro_name::tests::canonicalizes_names_and_rejects_invalid_ones ... ok
test native::capture_pomodoro_name::tests::build_cli_renders_without_panicking ... ok
test native::capture_pomodoro_close::tests::worked_example_ledger_is_byte_for_byte ... ok
test native::capture_pomodoro_name::tests::json_and_human_success_shapes_are_stable ... ok
test native::capture_pomodoro_close::selection_tests::full_close_reports_numbered_lineup_with_none ... ok
test native::capture_pomodoro_name::tests::dry_run_returns_the_plan_without_writing ... ok
test native::capture_pomodoro_start::drop_tests::created_session_reports_the_new_session_variant ... ok
test native::capture_pomodoro_start::drop_tests::dropped_last_line_without_final_newline_leaves_none ... ok
test native::capture_pomodoro_name::tests::names_a_crlf_note_without_touching_other_bytes ... ok
test native::capture_pomodoro_start::drop_tests::dropped_middle_line_without_final_newline_keeps_structure ... ok
test native::capture_pomodoro_start::drop_tests::drops_embedded_and_unresolved_rows_by_number ... ok
test native::capture_pomodoro_start::drop_tests::drops_nested_links_with_their_parent ... ok
test native::capture_pomodoro_start::drop_tests::drops_numbered_subtree_and_keeps_gaps ... ok
test native::capture_pomodoro_start::drop_tests::empty_drop_is_byte_identical ... ok
test native::capture_pomodoro_start::drop_tests::empty_lineup_suggests_the_token_without_its_drop ... ok
test native::capture_pomodoro_start::drop_tests::fenced_lines_are_not_numbered ... ok
test native::capture_pomodoro_start::drop_tests::preserves_crlf ... ok
test native::capture_pomodoro_start::drop_tests::three_bad_numbers_join_with_commas ... ok
test native::capture_pomodoro_start::drop_tests::out_of_range_names_every_bad_number ... ok
test native::capture_pomodoro_name::tests::recovers_a_shifted_line_and_repairs_an_untypeable_name ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_with_a_plus_and_returns_a_selectable_slug ... ok
test native::capture_pomodoro_name::tests::names_a_placeholder_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::capture_clip::tests::aggregate_save_cleans_up_files_after_a_later_failure ... ok
test native::capture_clip::tests::snippet_names_use_deterministic_collision_counters ... ok
test native::capture_pomodoro_start::lineup_tests::lists_direct_children_in_ledger_order ... ok
test native::capture_pomodoro_start::lineup_tests::skips_deeper_descendants_embeds_and_struck_lines ... ok
test native::capture_pomodoro_start::lineup_tests::skips_fenced_lines ... ok
test native::capture_pomodoros::tests::classifies_slugs_and_selectability ... ok
test native::capture_pomodoros::tests::human_output_is_plain_and_lists_badges ... ok
test native::capture_pomodoro_start::drop_tests::duplicate_still_queued_warns ... ok
test native::capture_pomodoros::tests::current_requires_exactly_one_open_timed_entry ... ok
test native::capture_pomodoro_start::lineup_tests::resolves_rows_through_the_staged_view ... ok
test native::capture_pomodoros::tests::ignores_nested_and_fenced_lookalikes ... ok
test native::capture_pomodoros::tests::includes_completed_entries_and_status_symbols ... ok
test native::capture_pomodoro_name::tests::validation_failures_are_write_free ... ok
test native::capture_pomodoros::tests::json_success_shape_is_stable ... ok
test native::capture_pomodoros::tests::parses_names_after_range_tail_only ... ok
test native::capture_pomodoros::tests::plus_names_are_selectable_and_prefix_matched ... ok
test native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes ... FAILED
test native::capture_pomodoros::tests::refs_resolve_exact_shifted_stale_and_ambiguous ... ok
test native::capture_pomodoros::tests::scans_timed_placeholder_and_range_less_entries ... ok
test native::capture_pomodoros::tests::selection_reports_completed_only_and_unique_suggestion ... ok
test native::capture_project_note::tests::acronym_titles_do_not_preserve_capitals ... ok
test native::capture_pomodoros::tests::selection_uses_whole_slug_before_earlier_prefix ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_keeps_suffixes_and_names_pomodoros ... ok
test native::capture_project_note::tests::all_caps_section_with_children_becomes_a_header ... ok
test native::capture_project_note::tests::basename_replaces_dashes_and_keeps_case ... ok
test native::capture_project_note::tests::authored_tasks_render_with_created_stamps_and_tab_children ... ok
test native::capture_project_note::tests::bare_all_caps_bullet_without_children_stays_a_task ... ok
test native::capture_project_note::tests::basic_note_matches_the_plan_example ... ok
test native::capture_project_note::tests::caret_task_keeps_its_authored_checkbox ... ok
test native::capture_project_note::tests::created_timestamp_derives_from_the_passed_datetime ... ok
test native::capture_project_note::tests::equal_section_titles_merge_in_source_order ... ok
test native::capture_project_note::tests::managed_log_shaped_bullets_are_not_special_cased ... ok
test native::capture_project_note::tests::named_all_caps_bullet_with_children_stays_a_task ... ok
test native::capture_project_note::tests::named_task_keeps_an_existing_created_stamp_before_the_id ... ok
test native::capture_project_note::tests::named_tasks_render_ids_last_with_next_status_for_links ... ok
test native::capture_project_note::tests::priority_writes_an_inline_field_before_hide ... ok
test native::capture_project_note::tests::prj_task_is_never_linked ... ok
test native::capture_project_note::tests::schedule_log_lines_land_directly_under_the_prj_task ... ok
test native::capture_project_note::tests::scheduled_date_lands_in_frontmatter_with_a_blocked_checkbox ... ok
test native::capture_project_note::tests::scheduled_project_renders_linked_tasks_as_blocked ... ok
test native::capture_project_note::tests::section_title_shape_rejects_mixed_case_and_banners ... ok
test native::capture_complete::tests::active_tasks::active_task_completion_ranks_queries_and_pins_json_shape ... ok
test native::capture_project_note::tests::tasks_section_merges_into_the_generated_header ... ok
test native::capture_rewrite::tests::build_cli_renders_without_panicking ... ok
test native::capture_rewrite::tests::cli_accepts_the_json_format_alias ... ok
test native::capture_rewrite::tests::cli_joins_text_arguments_with_spaces ... ok
test native::capture_rewrite::tests::cli_rejects_an_unknown_format ... ok
test native::capture_rewrite::tests::human_output_is_plain_without_color ... ok
test native::capture_rewrite::tests::json_reports_a_rule_a5_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_omits_cursor_when_not_supplied ... ok
test native::capture_rewrite::tests::json_reports_a_task_toggle_notice_without_changing_text ... ok
test native::capture_rewrite::tests::json_reports_no_rewrite_with_no_bare_at_at ... ok
test native::capture_rewrite::tests::close_items_are_never_rewritten ... ok
test native::capture_rewrite::tests::missing_text_reports_a_usage_error ... ok
test native::capture_schedule_log::tests::entry_line_uses_the_exact_codepoints ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_short_form_with_no_prior_date ... ok
test native::capture_schedule_log::tests::entry_text_renders_the_transition_form_with_a_prior_date ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_after_existing_children ... ok
test native::capture_rewrite::tests::json_shape_absorbs_the_local_marker ... ok
test native::capture_schedule_log::tests::insertion_creates_a_marker_for_a_childless_task ... ok
test native::capture_schedule_log::tests::insertion_ignores_a_marker_nested_under_another_child ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_legacy_marker ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_spaced_marker ... ok
test native::capture_schedule_log::tests::insertion_prepends_under_a_tabbed_marker ... ok
test native::capture_schedule_log::tests::insertion_preserves_a_missing_final_newline ... ok
test native::capture_schedule_log::tests::insertion_preserves_crlf_endings ... ok
test native::capture_schedule_log::tests::marker_text_keeps_the_variation_selector ... ok
test native::capture_schedule_log::tests::plan_matches_the_picker_fixture ... ok
test native::capture_schedule_log::tests::plan_uses_a_two_space_indent_unit ... ok
test native::capture_schedule_log::tests::priority_roll_reason_collapses_when_the_level_is_unchanged ... ok
test native::capture_schedule_log::tests::priority_roll_reason_keeps_fixed_window_endpoints ... ok
test native::capture_schedule_log::tests::randomize_reason_appends_the_until_base ... ok
test native::capture_schedule_log::tests::randomize_reason_keeps_a_fixed_window ... ok
test native::capture_schedule_log::tests::randomize_reason_names_the_tool_without_a_from_suffix ... ok
test native::capture_sections::tests::json_success_shape_is_stable ... ok
test native::capture_sections::tests::route_validation_lowercases_valid_route ... ok
test native::capture_sections::tests::existing_file_lists_non_tasks_sections_in_order ... ok
test native::capture_targets::tests::area_and_project_frontmatter_are_classified ... ok
test native::capture_sections::tests::missing_file_returns_empty_sections ... ok
test native::capture_targets::tests::routable_route_requires_lowercase_valid_token ... ok
test native::capture_targets::tests::json_shape_is_stable ... ok
test native::capture_task_id::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_id::tests::json_success_shape_is_stable ... ok
test native::capture_task_sections::tests::build_cli_renders_without_panicking ... ok
test native::capture_task_sections::tests::checkboxed_all_caps_children_are_not_sections ... ok
test native::capture_complete::tests::parent_tasks::leading_plus_query_refetch_keeps_token_range_and_full_catalog ... ok
test native::capture_targets::tests::scan_orders_inbox_areas_then_active_projects ... ok
test native::capture_task_sections::tests::exact_title_match_is_case_insensitive_and_not_a_slug ... ok
test native::capture_task_sections::tests::empty_section_bullet_still_qualifies ... ok
test native::capture_task_sections::tests::grandchild_is_not_a_direct_child_section ... ok
test native::capture_task_sections::tests::insertion_geometry_preserves_crlf_offsets ... ok
test native::capture_task_sections::tests::json_success_shape_and_key_order_are_stable ... ok
test native::capture_task_sections::tests::insertion_geometry_for_middle_last_blank_and_managed_log ... ok
test native::capture_task_sections::tests::ordered_and_star_plus_markers_qualify ... ok
test native::capture_task_sections::tests::slug_trims_collapses_whitespace_and_lowercases ... ok
test native::capture_task_sections::tests::suggests_unique_nearby_titles_and_slugs ... ok
test native::capture_task_sections::tests::managed_logs_are_never_sections_plain_titles_are ... ok
test native::capture_task_toggle::tests::blocked_is_forced_to_next ... ok
test native::capture_task_sections::tests::whole_slug_beats_earlier_prefix_and_first_duplicate_wins ... ok
test native::capture_task_sections::tests::tab_two_space_four_space_and_mixed_indentation ... ok
test native::capture_task_toggle::tests::errors_when_no_eligible_open_entry ... ok
test native::capture_task_sections::tests::title_whitelist_edges ... ok
test native::capture_task_toggle::tests::errors_when_no_pomodoros_section ... ok
test native::capture_task_toggle::tests::errors_on_multiple_open_timed_entries ... ok
test native::capture_task_toggle::tests::idempotent_insertion_skips_when_already_linked ... ok
test native::capture_task_toggle::tests::implicit_insertion_targets_single_open_timed_entry ... ok
test native::capture_task_toggle::tests::insertion_removes_duplicate_from_later_open_entry ... ok
test native::capture_task_toggle::tests::invalid_pomodoro_name_is_rejected ... ok
test native::capture_task_sections::tests::lists_sections_in_document_order_for_a_block_id ... ok
test native::capture_task_sections::tests::resolved_task_with_no_sections_is_a_successful_empty_list ... ok
test native::capture_task_toggle::tests::named_relocation_is_a_noop_when_already_at_the_named_destination ... ok
test native::capture_task_toggle::tests::link_operations_preserve_crlf ... ok
test native::capture_task_toggle::tests::named_relocation_inserts_before_the_first_future_entry ... ok
test native::capture_task_toggle::tests::implicit_insertion_falls_back_to_first_open_entry_without_timed ... ok
test native::capture_task_sections::tests::task_ref_resolves_a_task_without_a_block_id ... ok
test native::capture_task_sections::tests::request_validation_covers_route_and_exclusive_selectors ... ok
test native::capture_task_toggle::tests::named_relocation_moves_to_an_exact_open_match ... ok
test native::capture_task_toggle::tests::named_relocation_prefix_match_loses_to_a_whole_slug ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_an_invalid_name ... ok
test native::capture_task_toggle::tests::named_relocation_creates_on_completed_only_and_missing_names ... ok
test native::capture_task_toggle::tests::named_relocation_rejects_creation_with_multiple_timed_entries ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_descendants_and_destination_indent ... ok
test native::capture_task_toggle::tests::named_relocation_preserves_crlf_when_creating ... ok
test native::capture_task_toggle::tests::named_relocation_selects_an_existing_name_despite_multiple_timed ... ok
test native::capture_task_toggle::tests::named_selection_reports_creation_needed ... ok
test native::capture_task_toggle::tests::named_selection_targets_existing_open_entry ... ok
test native::capture_task_toggle::tests::no_schedule_log_marker_means_no_entry_even_when_field_removed ... ok
test native::capture_task_toggle::tests::named_relocation_same_location_noop_does_not_edit_bytes ... ok
test native::capture_task_toggle::tests::past_or_today_schedule_retires_nothing ... ok
test native::capture_task_toggle::tests::pull_forward_entry_text_matches_vault_fixture ... ok
test native::capture_task_toggle::tests::relocation_errors_on_duplicate_movable_links ... ok
test native::capture_task_toggle::tests::preserves_crlf_line_endings ... ok
test native::capture_task_toggle::tests::relocation_errors_when_the_link_is_missing ... ok
test native::capture_task_toggle::tests::relocation_is_a_noop_when_the_link_is_already_current ... ok
test native::capture_task_sections::tests::missing_note_and_unresolvable_parents_are_errors ... ok
test native::capture_complete::tests::pomodoros::pomodoro_name_completion_works_without_a_block_id ... ok
test native::capture_task_toggle::tests::relocation_moves_a_descendant_bearing_task_link_as_a_subtree ... ok
test native::capture_task_toggle::tests::relocation_falls_back_to_the_first_open_entry_without_timed ... ok
test native::capture_task_toggle::tests::relocation_moves_a_later_link_into_the_timed_current_pomodoro ... ok
test native::capture_task_toggle::tests::relocation_preserves_crlf_and_a_missing_final_newline ... ok
test native::capture_task_toggle::tests::relocation_moves_an_earlier_link_into_a_later_destination ... ok
test native::capture_task_toggle::tests::relocation_ignores_completed_history_and_mixed_text_lookalikes ... ok
test native::capture_task_toggle::tests::relocation_reports_an_unnamed_endpoint ... ok
test native::capture_task_toggle::tests::relocation_reuses_implicit_selection_errors ... ok
test native::capture_task_toggle::tests::relocation_uses_the_destination_child_indentation ... ok
test native::capture_task_toggle::tests::removal_deletes_whole_subtree_for_sole_content_bullet ... ok
test native::capture_task_toggle::tests::removal_never_touches_completed_pomodoros ... ok
test native::capture_task_toggle::tests::removal_only_strips_the_link_when_bullet_has_other_text ... ok
test native::capture_task_toggle::tests::removal_reports_no_changes_when_nothing_matches ... ok
test native::capture_task_toggle::tests::returns_none_for_non_task_or_out_of_range_lines ... ok
test native::capture_task_toggle::tests::removes_single_future_scheduled_field ... ok
test native::capture_task_toggle::tests::sets_next_without_schedule_field ... ok
test native::capture_task_toggle::tests::two_scheduled_fields_retire_nothing ... ok
test native::capture_task_toggle::tests::schedule_log_falls_back_to_marker_indent_plus_tab_with_no_existing_entries ... ok
test native::capture_task_toggle::tests::writes_pull_forward_entry_reusing_existing_indentation ... ok
test native::capture_tasks::tests::json_success_shape_is_stable ... ok
test native::collect_done::tests::plan::canceled_only_tasks_below_threshold_remain_in_source ... ok
test native::capture_tasks::tests::route_validation_lowercases_valid_route ... ok
test native::capture_work_log::tests::appends_work_log_after_schedule_log_and_uses_task_indent_style ... ok
test native::capture_work_log::tests::empty_existing_marker_derives_child_indent_and_marker ... ok
test native::capture_work_log::tests::prepends_under_existing_work_marker_and_inherits_entry_prefix ... ok
test native::capture_work_log::tests::preserves_crlf_and_missing_final_newline ... ok
test native::capture_work_log::tests::writes_same_target_groups_in_source_order_with_prior_cursor ... ok
test native::collect_done::tests::plan::canceled_only_tasks_move_when_threshold_is_met ... ok
test native::capture_complete::tests::routes_tasks::hash_after_a_bare_block_id_marker_completes_a_pomodoro_name ... ok
test native::collect_done::tests::plan::collecting_tasks_adds_done_tasks_to_source ... ok
test native::capture_tasks::tests::missing_file_returns_empty_tasks ... ok
test native::collect_done::tests::plan::duplicate_moved_block_ids_do_not_rewrite_links ... ok
test native::collect_done::tests::plan::existing_archive_creates_metadata_only_source_update ... ok
test native::collect_done::tests::plan::existing_archive_with_stale_metadata_creates_archive_only_plan ... ok
test native::collect_done::tests::plan::includes_nested_path_note_when_it_meets_threshold ... ok
test native::collect_done::tests::plan::missing_archive_without_threshold_tasks_is_not_planned ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_for_new_archive_note ... ok
test native::collect_done::tests::plan::already_linked_source_with_existing_archive_is_not_planned ... ok
test native::collect_done::tests::unit::creates_source_frontmatter_for_done_tasks ... ok
test native::capture_task_id::tests::dry_run_returns_the_plan_without_writing ... ok
test native::collect_done::tests::unit::dependency_ids_preserve_path_case_and_qualify_nested_notes ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_are_ambiguous ... ok
test native::collect_done::tests::unit::adds_archive_parent_to_existing_frontmatter ... ok
test native::collect_done::tests::unit::extracts_block_ids_from_every_moved_task_block_line ... ok
test native::collect_done::tests::unit::adds_done_tasks_to_existing_source_frontmatter ... ok
test native::collect_done::tests::unit::extracts_nested_blocks_and_continuations ... ok
test native::collect_done::tests::unit::inserts_missing_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::leaves_correct_archive_frontmatter_unchanged ... ok
test native::collect_done::tests::unit::leaves_correct_done_tasks_frontmatter_unchanged ... ok
test native::collect_done::tests::unit::block_ids_are_only_end_of_line_obsidian_anchors ... ok
test native::collect_done::tests::unit::completed_child_moves_without_collecting_active_parent ... ok
test native::capture_tasks::tests::lists_only_open_tasks_in_document_order_with_sections_and_depth ... ok
test native::collect_done::tests::unit::creates_archive_frontmatter_with_nested_source_parent ... ok
test native::collect_done::tests::unit::maps_archive_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::unit::maps_source_notes_to_archive_notes ... ok
test native::collect_done::tests::unit::prepends_archive_frontmatter_when_existing_note_has_none ... ok
test native::collect_done::tests::unit::maps_source_notes_to_obsidian_wiki_links ... ok
test native::collect_done::tests::unit::preserves_crlf_when_adding_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::preserves_crlf_when_repairing_archive_frontmatter ... ok
test native::collect_done::tests::unit::preserves_line_endings_in_source_and_archive ... ok
test native::collect_done::tests::unit::recognizes_done_and_canceled_task_lines_only ... ok
test native::collect_done::tests::unit::rejects_zero_threshold ... ok
test native::collect_done::tests::unit::replaces_stale_archive_type_frontmatter ... ok
test native::collect_done::tests::unit::replaces_stale_done_tasks_frontmatter ... ok
test native::collect_done::tests::unit::updates_existing_archive_parent_frontmatter ... ok
test native::completion::adapters::tests::bash_stamp_matches_protocol ... ok
test native::collect_done::tests::unit::parses_attached_short_threshold_option ... ok
test native::collect_done::tests::unit::parses_default_threshold ... ok
test native::collect_done::tests::unit::parses_short_threshold_equals_option ... ok
test native::collect_done::tests::unit::parses_short_threshold_option ... ok
test native::collect_done::tests::unit::parses_threshold_equals_option ... ok
test native::collect_done::tests::unit::parses_threshold_option ... ok
test native::collect_done::tests::unit::pathless_archive_links_gain_the_source_note_path ... ok
test native::completion::adapters::tests::zsh_stamp_matches_protocol ... ok
test native::completion::kinds::tests::path_specific_entries_win ... ok
test native::collect_done::tests::unit::markdown_repair_skips_wikilink_spans ... ok
test native::collect_done::tests::unit::repairs_simple_markdown_inline_block_links ... ok
test native::collect_done::tests::plan::task_moving_plan_writes_archive_with_nested_source_parent ... ok
test native::completion::protocol::tests::encoder_sanitizes_fields_and_drops_bad_values ... ok
test native::collect_done::tests::unit::leaves_ambiguous_basename_links_unchanged ... ok
test native::completion::protocol::tests::parses_attached_forms ... ok
test native::completion::protocol::tests::parses_full_request ... ok
test native::collect_done::tests::unit::repairs_same_note_nested_and_unique_basename_links ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_rewrites_exact_tokens_only ... ok
test native::collect_done::tests::unit::unqualifiable_paths_do_not_abort_identity_indexing ... ok
test native::collect_done::tests::plan::link_repair_scan_includes_done_notes ... ok
test native::collect_done::tests::unit::below_threshold_block_ids_do_not_trigger_link_repair ... ok
test native::collect_done::tests::unit::repairs_wikilinks_embeds_and_aliases_to_moved_blocks ... ok
test native::collect_done::tests::unit::duplicate_moved_block_ids_become_unique_archive_ids ... ok
test native::collect_done::tests::plan::generated_tag_pages_do_not_make_source_basename_ambiguous ... ok
test native::collect_done::tests::plan::source_block_id_keeps_links_pointing_at_source ... ok
test native::collect_done::tests::unit::existing_archive_block_ids_reserve_original_ids ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_preserves_distinct_moved_ids ... ok
test native::collect_done::tests::plan::self_heals_preexisting_block_links_to_archive ... ok
test native::collect_done::tests::unit::link_repair_uses_renamed_unique_moved_block_id ... ok
test native::collect_done::tests::unit::dependency_metadata_repair_supports_task_field_grammar_and_skips_code ... ok
test native::collect_done::tests::plan::planned_source_and_archive_contents_are_link_repaired ... ok
test native::collect_done::tests::plan::generated_and_template_directories_are_not_collected_or_repaired ... ok
test native::completion::protocol::tests::rejects_malformed_requests ... ok
test native::collect_done::tests::plan::task_moving_plan_repairs_links_in_separate_notes ... ok
test native::completion::report::tests::tilde_collapses_home ... ok
test native::collect_done::tests::unit::block_id_deduplication_preserves_crlf_line_endings ... ok
test native::collect_done::tests::plan::scans_markdown_files_with_exclusions_and_threshold ... ok
test native::completion::protocol::tests::skew_messages_cover_both_directions ... ok
test native::collect_done::tests::unit::block_id_suffix_selection_skips_existing_candidates ... ok
test native::completion::tree::tests::descriptor_names_match_canonical_paths ... ok
test native::config::freshness::tests::decay_false_counts_but_never_asks ... ok
test native::config::freshness::tests::decay_parses_zero_and_fixed_entry ... ok
test native::capture_complete::tests::task_links::task_link_completion_keeps_candidates_when_the_day_file_is_missing ... ok
test native::config::freshness::tests::absent_freshness_block_loads_defaults ... ok
test native::config::freshness::tests::lane_intervals_default_absent_and_null ... ok
test native::config::freshness::tests::legacy_budget_key_supplies_budget_with_deprecation_flag ... ok
test native::config::freshness::tests::legacy_budget_key_recovers_and_rejects_like_canonical ... ok
test native::config::freshness::tests::missing_freshness_file_loads_defaults ... ok
test native::config::freshness::tests::canonical_budget_key_wins_over_legacy ... ok
test native::completion::verify::tests::timeout_override_falls_back ... ok
test native::config::freshness::tests::null_freshness_block_loads_defaults ... ok
test native::completion::tests::deadline_defaults_and_falls_back ... ok
test native::completion::tree::tests::hand_descriptor_drift ... ok
test native::config::freshness::tests::decay_defaults_when_absent_null_true_or_empty ... ok
test native::config::freshness::tests::parses_freshness_overrides_and_ignores_unknown_keys ... ok
test native::completion::context::tests::env_defaults_apply_without_flags ... ok
test native::completion::context::tests::alias_words_rewrite_to_the_canonical_path ... ok
test native::config::freshness::tests::lane_intervals_parse_false_and_integers ... ok
test native::config::freshness::tests::null_values_fall_back_to_defaults ... ok
test native::config::freshness::tests::tracker_intervals_default_absent_and_null ... ok
test native::config::freshness::tests::rejects_invalid_lane_intervals ... ok
test native::config::freshness::tests::rejects_invalid_decay_values ... ok
test native::config::freshness::tests::tracker_intervals_parse_integers ... ok
test native::config::freshness::tests::rejects_invalid_tracker_intervals ... ok
test native::config::plan::tests::absent_plan_block_loads_defaults ... ok
test native::config::plan::tests::missing_plan_file_loads_defaults ... ok
test native::config::plan::tests::null_plan_block_loads_defaults ... ok
test native::config::freshness::tests::mistyped_freshness_block_leaves_other_loaders_working ... ok
test native::config::tests::derive_seed_is_deterministic_and_sensitive_to_every_part ... ok
test native::config::plan::tests::parses_plan_overrides_and_ignores_unknown_keys ... ok
test native::config::tests::blank_highlights_pre_scan_hook_disables_file_hook ... ok
test native::config::tests::derive_seed_separator_prevents_part_boundary_collisions ... ok
test native::completion::tree::tests::mounted_names_have_no_spaces ... ok
test native::completion::context::tests::unknown_words_never_fail_the_parse ... ok
test native::completion::kinds::tests::every_table_entry_matches_the_tree ... ok
test native::completion::context::tests::parses_long_route_and_bob_dir ... ok
test native::config::tests::level_by_label_matches_ascii_case_insensitively ... ok
test native::config::tests::missing_gkeep_file_loads_defaults ... ok
test native::config::tests::level_for_value_matches_exact_value_after_trim ... ok
test native::config::plan::tests::rejects_invalid_plan_values ... ok
test native::capture_complete::tests::task_links::task_link_completion_lists_worked_example_in_canonical_order ... ok
test native::config::tests::levels_exposes_every_configured_level ... ok
test native::config::plan::tests::mistyped_plan_block_leaves_other_loaders_working ... ok
test native::config::tests::ignores_decay_and_rolls_keys ... ok
test native::config::plan::tests::absent_max_ready_per_note_falls_back_to_default ... ok
test native::config::tests::parses_absent_gkeep_section_as_defaults ... ok
test native::config::tests::parses_absent_highlights_config_as_none ... ok
test native::config::plan::tests::max_ready_per_note_bounds_and_message ... ok
test native::config::tests::missing_file_message_is_command_neutral ... ok
test native::config::tests::parses_full_gkeep_section_and_ignores_unknown_keys ... ok
test native::config::tests::parses_highlights_pre_scan_hook ... ok
test native::config::tests::parses_deployed_config ... ok
test native::config::freshness::tests::rejects_invalid_freshness_values ... ok
test native::config::tests::rejects_blank_value ... ok
test native::config::tests::rejects_blank_label ... ok
test native::completion::present::tests::double_dash_offers_long_forms_only ... ok
test native::completion::kinds::tests::every_value_arg_has_a_decision ... ok
test native::completion::present::tests::root_empty_offers_sectioned_commands_in_help_order ... ok
test native::completion::present::tests::attached_option_values_carry_prefix ... ok
test native::completion::tree::tests::tree_debug_assert_passes ... ok
test native::config::tests::mistyped_plan_block_leaves_gkeep_loader_working ... ok
test native::config::tests::mistyped_plan_block_leaves_highlights_loader_working ... ok
test native::config::tests::mistyped_plan_block_leaves_priority_loader_working ... ok
test native::config::tests::rejects_duplicate_level_labels ... ok
test native::config::tests::rejects_empty_levels ... ok
test native::config::tests::rejects_legacy_highlights_pre_scan_command ... ok
test native::completion::present::tests::text_started_slot_offers_no_options ... ok
test native::config::tests::rejects_labels_that_differ_only_by_case ... ok
test native::config::tests::rejects_invalid_gkeep_yaml ... ok
test native::config::tests::rejects_missing_priority_property ... ok
test native::config::tests::rejects_duplicate_level_values ... ok
test native::config::tests::rejects_missing_schedules ... ok
test native::config::tests::rejects_negative_min_days ... ok
test native::config::tests::rejects_min_greater_than_max ... ok
test native::config::tests::rejects_non_integer_min_days ... ok
test native::config::tests::rejects_non_numeric_gkeep_timeout ... ok
test native::config::tests::resolve_config_path_expands_tilde_in_xdg_config_home ... ok
test native::config::tests::rejects_value_containing_field_syntax ... ok
test native::config::tests::mix64_spreads_sequential_inputs ... ok
test native::config::tests::resolve_config_path_falls_back_to_home_dot_config ... ok
test native::config::tests::resolve_config_path_ignores_empty_env_values ... ok
test native::config::tests::rejects_missing_value ... ok
test native::config::tests::resolve_config_path_prefers_bob_config_file ... ok
test native::config::tests::rejects_wrong_schedules_target ... ok
test native::completion::tree::tests::hidden_aliases_and_help_are_absent ... ok
test native::config::tests::roll_offset_p4_window_hits_both_extremes ... ok
test native::config::tests::resolve_config_path_falls_back_to_xdg_config_home ... ok
test native::completion::tree::tests::mounted_names_match_subcommands_in_order ... ok
test native::completion::context::tests::task_and_repo_need_their_subcommands ... ok
test native::dataview::tasks::filter::tests::global_filter_removal_only_removes_the_first_occurrence ... ok
test native::config::tests::roll_offset_returns_fixed_value_when_min_equals_max ... ok
test native::config::tests::tolerates_unusual_sibling_properties ... ok
test native::dataview::tasks::filter::tests::absolute_ranges_are_inclusive_and_order_independent ... ok
test native::dataview::tasks::filter::tests::relative_ranges_use_iso_weeks_and_calendar_boundaries ... ok
test native::dataview::tasks::filter::tests::numbered_ranges_cover_year_month_quarter_and_iso_week ... ok
test native::dataview::tasks::index::tests::heading_parser_supports_atx_and_setext_headings ... ok
test native::dataview::tasks::filter::tests::weekday_and_offset_dates_are_pinned_to_now ... ok
test native::capture_complete::tests::task_links::task_link_completion_pins_json_shape_and_omissions ... ok
test native::dataview::tasks::parse::tests::boolean_chains_use_tasks_precedence_and_allow_operand_apostrophes ... ok
test native::dataview::tasks::parse::tests::numbered_date_ranges_optional_priority_is_and_status_boundary_parse ... ok
test native::dataview::tasks::parse::tests::parses_every_filter_family_and_boolean_combinations ... ok
test native::dataview::tasks::parse::tests::rejects_malformed_filters_with_actionable_errors ... ok
test native::dataview::tasks::parse::tests::scanner_matches_tasks_line_continuation_rules ... ok
test native::dataview::tasks::task::tests::file_context_matches_tasks_expose_properties ... ok
test native::completion::tree::tests::parse_smoke ... ok
test native::dataview::tasks::parse::tests::upstream_dialect_rejects_status_symbol_with_tasks_error ... ok
test native::dataview::tasks::parse::tests::ignore_global_query_can_come_from_query_file_defaults ... ok
test native::dataview::tasks::result::tests::natural_collation_is_case_insensitive_and_numeric ... ok
test native::dataview::tasks::task::tests::urgency_due_scheduled_and_start_boundaries_match_tasks_v8 ... ok
test native::dataview::tasks::parse::tests::parses_every_v8_sort_group_and_layout_key ... ok
test native::dataview::tasks::settings::tests::unknown_task_format_falls_back_to_emoji ... ok
test native::dataview::tests::dql_grouped_table_rows_warn_and_fail_when_strict ... ok
test native::dataview::tasks::task::tests::recurrence_rules_are_validated_and_standardized ... ok
test native::dataview::tasks::result::tests::explanations_include_expanded_preset_statements ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_with_heading_context ... ok
test native::dataview::tests::dql_list_paths_use_list_pair_identity ... ok
test native::dataview::tasks::task::tests::removing_global_filter_preserves_spacing_and_only_removes_first_word ... ok
test native::dataview::tests::dql_missing_table_identities_warn_per_row ... ok
test native::dataview::tasks::task::tests::task_line_parser_matches_tasks_markers_and_spacing ... ok
test native::dataview::tests::dql_table_paths_use_first_identity_column ... ok
test native::completion::context::tests::parses_attached_and_short_cluster_forms ... ok
test native::dataview::tasks::tests::extracts_tasks_fences_from_nested_blockquotes_and_callouts ... ok
test native::dataview::tests::dql_task_paths_resolve_grouped_task_source_notes ... ok
test native::dataview::tasks::parse::tests::composes_global_defaults_presets_and_placeholders_in_order ... ok
test native::dataview::tests::native_source_parser_accepts_phase3_source_surface ... ok
test native::freshness::placement::placement_tests::cancelled_is_refused_like_done ... ok
test native::freshness::placement::placement_tests::freshness_config_defaults_match_contract ... ok
test native::freshness::placement::placement_tests::keeps_absent_reads_zero ... ok
test native::capture_task_id::tests::validation_failures_are_write_free ... ok
test native::dataview::tests::native_dql_parser_accepts_phase3_command_surface ... ok
test native::dataview::tasks::task::tests::unknown_status_is_todo_and_remove_global_filter_is_display_only ... ok
test native::dataview::tasks::filter::tests::regex_flags_match_javascript_filtering_behavior ... ok
test native::freshness::placement::placement_tests::generic_stamps_clear_keeps_including_same_day ... ok
test native::freshness::placement::placement_tests::keeps_first_valid_wins_up_to_999 ... ok
test native::dataview::tests::source_paths_are_normalized_and_deduplicated ... ok
test native::freshness::placement::placement_tests::keeps_canonical_order_after_refresh ... ok
test native::completion::present::tests::lone_dash_pairs_forms_with_identical_descriptions ... ok
test native::dataview::tests::native_dql_parser_reports_representative_invalid_queries ... ok
test native::freshness::placement::placement_tests::non_task_lines_are_refused ... ok
test native::freshness::placement::placement_tests::hooks_blocked_signals_survive_and_checkbox_swap_preserves_fresh ... ok
test native::freshness::placement::placement_tests::keeps_invalid_values_report_zero ... ok
test native::freshness::placement::placement_tests::keeps_misplaced_lints_and_repairs ... ok
test native::freshness::placement::placement_tests::p02_created_suffix ... ok
test native::freshness::placement::placement_tests::p03_block_id_only ... ok
test native::freshness::placement::placement_tests::p01_bare_appends_fresh ... ok
test native::freshness::placement::placement_tests::keeps_same_day_preserve_is_noop ... ok
test native::freshness::placement::placement_tests::p04_interleaved_suffix ... ok
test native::freshness::placement::placement_tests::keeps_key_match_is_exact_and_paren_reads ... ok
test native::freshness::placement::placement_tests::p06_spacing_head_collapses_suffix_untouched ... ok
test native::freshness::placement::placement_tests::p05_unknown_field_stays_left ... ok
test native::freshness::placement::placement_tests::p08_same_day_is_noop ... ok
test native::freshness::placement::placement_tests::p07_restamp_replaces_date ... ok
test native::freshness::placement::placement_tests::p13_recurring_refused ... ok
test native::freshness::placement::placement_tests::p09_misplaced_is_repaired ... ok
test native::freshness::placement::placement_tests::p14_global_filter_floor ... ok
test native::freshness::placement::placement_tests::p12_set_and_clear_refresh ... ok
test native::freshness::placement::placement_tests::p10_duplicates_collapse_and_use_latest ... ok
test native::freshness::placement::placement_tests::p18_deeply_indented_quote_is_not_a_task ... ok
test native::dataview::tasks::task::tests::metadata_must_be_trailing_but_tags_can_be_interleaved ... ok
test native::freshness::placement::placement_tests::p11_refresh_follows_fresh ... ok
test native::freshness::placement::placement_tests::p17_done_refused ... ok
test native::freshness::placement::placement_tests::p18_quoted_task_stamps_with_prefix_kept ... ok
test native::freshness::placement::placement_tests::p18_nested_quote_stamps ... ok
test native::dataview::tasks::task::tests::dataview_parser_extracts_all_fields_and_cleans_description ... ok
test native::freshness::placement::placement_tests::p16_indented_blocked ... ok
test native::dataview::tasks::task::tests::invalid_dates_and_recurrences_match_tasks_semantics ... ok
test native::dataview::tasks::task::tests::urgency_matches_tasks_v8_coefficients ... ok
test native::dataview::tasks::task::tests::dataview_fields_honor_delimiters_whitespace_commas_and_case ... ok
test native::freshness::placement::placement_tests::p15_parenthesized_field ... ok
test native::freshness::seed::tests::oversized_notes_split_into_consecutive_chunks ... ok
test native::freshness::placement::placement_tests::refusals_leave_keeps_untouched ... ok
test native::freshness::placement::placement_tests::set_refresh_replaces_existing_value ... ok
test native::freshness::seed::tests::invariance_abort_lists_a_line_hiding_a_field ... ok
test native::freshness::state::state_tests::cl10_completed_occurrence_and_future_next_leave_queue ... ok
test native::freshness::seed::tests::write_changes_refuses_a_file_changed_since_scan ... ok
test native::freshness::state::state_tests::cl11_checklist_beats_lane_and_tracker ... ok
test native::freshness::seed::tests::canonical_restamps_pass_invariance ... ok
test native::freshness::state::state_tests::cl5_tag_matching ... ok
test native::freshness::state::state_tests::cl1_recurring_pre_chore ... ok
test native::capture_complete::tests::task_links::task_link_completion_queries_cover_the_sigil_and_rank ... ok
test native::freshness::state::state_tests::cl2_unknown_status_pre_is_queued_with_null_lane ... ok
test native::freshness::state::state_tests::bucket_partition_vectors ... ok
test native::freshness::state::state_tests::cl7_one_off_post_keeps_new_state ... ok
test native::freshness::state::state_tests::cl6_conflict_prefers_pre ... ok
test native::freshness::state::state_tests::cl12_repeat_without_when_done_still_pre ... ok
test native::freshness::state::state_tests::cl4_today_and_daily_note_still_pre ... ok
test native::freshness::state::state_tests::cl9_recurring_checklist_refuses_stamp ... ok
test native::freshness::state::state_tests::decide_at_limit_but_not_below ... ok
test native::freshness::state::state_tests::l1_lane_due_and_stamped_today ... ok
test native::freshness::state::state_tests::l2_lane_overrides_refresh ... ok
test native::freshness::state::state_tests::decide_on_early_dates ... ok
test native::freshness::state::state_tests::decide_covers_returned_but_never_new ... ok
test native::freshness::state::state_tests::l4_lane_off_switch_and_null_default ... ok
test native::freshness::state::state_tests::decide_zero_off_and_lane_rows ... ok
test native::freshness::state::state_tests::l3_lane_exclusions_have_no_tier ... ok
test native::freshness::state::state_tests::cl3_exclusions_drop_checklist_rows ... ok
test native::freshness::state::state_tests::lane_reference_uses_ready_chain_without_configured_cadence ... ok
test native::freshness::state::state_tests::l5_lane_order_never_stamped_first ... ok
test native::freshness::state::state_tests::missing_created_sorts_after_dated_peers ... ok
test native::freshness::state::state_tests::r1_returned_beats_older_rotten ... ok
test native::freshness::state::state_tests::counts_carry_decide ... ok
test native::freshness::state::state_tests::r2_returned_orders_by_schedule_then_newest_created ... ok
test native::freshness::state::state_tests::reference_interval_boundary ... ok
test native::freshness::state::state_tests::cl8_nine_tier_order ... ok
test native::freshness::state::state_tests::s02_fresh_with_due_on ... ok
test native::freshness::state::state_tests::s03_boundary_is_rotten_with_zero_overdue ... ok
test native::freshness::state::state_tests::q1_bryan_example_orders_adjc ... ok
test native::freshness::state::state_tests::q2_tier_order_beats_path_order ... ok
test native::freshness::state::state_tests::resurfaced_reference_walks_references_without_decide ... ok
test native::freshness::state::state_tests::s05_task_interval_beats_note ... ok
test native::freshness::state::state_tests::s01_new_without_stamp ... ok
test native::freshness::state::state_tests::s06_note_interval_beats_config ... ok
test native::freshness::state::state_tests::s07_config_interval ... ok
test native::freshness::state::state_tests::s09_malformed_fresh_is_new_with_lint ... ok
test native::freshness::state::state_tests::s04_overdue_counts_days ... ok
test native::freshness::state::state_tests::s10_future_fresh_is_new_with_lint ... ok
test native::freshness::state::state_tests::s11_resurfaced_when_schedule_returns_after_stamp ... ok
test native::freshness::state::state_tests::s08_invalid_overrides_fall_through_with_lints ... ok
test native::freshness::state::state_tests::s12_equal_schedule_is_not_resurfaced ... ok
test native::freshness::state::state_tests::s14_queue_order_new_then_due ... ok
test native::freshness::state::state_tests::tracker_lane_precedence_and_disabled_lanes ... ok
test native::freshness::state::state_tests::tracking_projects_tier_and_counts ... ok
test native::config::tests::roll_offset_stays_within_bounds_for_many_seeds ... ok
test native::capture_complete::tests::task_links::task_link_completion_scopes_to_the_batch_second_item ... ok
test native::freshness::state::state_tests::tracker_intervals_override_for_matching_type ... ok
test native::gkeep::adapter::tests::resolve_without_uv_is_a_setup_error ... ok
test native::freshness::state::state_tests::b1_upkeep_counts_outside_the_lanes ... ok
test native::freshness::state::state_tests::seven_tier_order_with_references ... ok
test native::freshness::state::state_tests::s13_out_of_scope_is_null ... ok
test native::gkeep::config::tests::adapter_override_reads_env ... ok
test native::gkeep::cli::tests::bob_dir_flag_expands_tilde ... ok
test native::gkeep::config::tests::device_id_is_derived_and_pinned ... ok
test native::gkeep::adapter::tests::resolve_uses_override_without_path_lookup ... ok
test native::freshness::placement::placement_tests::parse_invariance_across_all_vectors ... ok
test native::gkeep::cli::tests::list_args_pin_defaults_and_values ... ok
test native::gkeep::doctor::tests::check_status_names_match_the_json_contract ... ok
test native::freshness::state::state_tests::s15_counts_and_budget_meter ... ok
test native::dataview::tests::flatten_budget_honors_earlier_filters_not_later_limits ... ok
test native::gkeep::cli::tests::doctor_and_login_args ... ok
test native::dataview::tests::flatten_budget_accepts_exact_limit_and_rejects_overflow ... ok
test native::gkeep::config::tests::token_shape_classifier ... ok
test native::gkeep::config::tests::device_id_validation ... ok
test native::gkeep::config::tests::resolve_email_override_wins ... ok
test native::gkeep::doctor::tests::home_prefix_collapses_to_tilde ... ok
test native::gkeep::config::tests::resolve_applies_defaults_and_derives_device_id ... ok
test native::gkeep::doctor::tests::tasks_heading_matches_headings_only ... ok
test native::gkeep::cli::tests::pull_args_pin_every_option ... ok
test native::gkeep::ledger::tests::journal_read_skips_non_utf8_lines ... ok
test native::gkeep::login::tests::inbox_count_handles_singular_and_plural ... ok
test native::gkeep::login::tests::recovery_path_lives_under_the_state_dir ... ok
test native::gkeep::model::tests::archive_success_counts_archived_and_already_archived ... ok
test native::gkeep::model::tests::canonical_json_and_fingerprint_are_pinned ... ok
test native::gkeep::doctor::tests::device_id_shortens_to_eight_plus_ellipsis ... ok
test native::gkeep::ledger::tests::journal_read_tolerates_missing_files_and_corrupt_lines ... ok
test native::gkeep::model::tests::fingerprint_ignores_json_key_order_and_attachments ... ok
test native::gkeep::model::tests::unknown_attachment_kind_deserializes_to_other ... ok
test native::gkeep::model::tests::responses_parse ... ok
test native::gkeep::plan::tests::archived_notes_get_the_archived_state ... ok
test native::gkeep::ledger::tests::marker_round_trips_ids_with_dots_and_exotic_bytes ... ok
test native::dataview::tests::flatten_lists_include_nested_children ... ok
test native::gkeep::config::tests::read_token_returns_first_non_empty_line ... ok
test native::dataview::tests::flatten_alias_and_collection_builtins_do_not_mutate_siblings ... ok
test native::gkeep::ledger::tests::duplicates_name_every_location ... ok
test native::dataview::tests::flatten_retains_file_metadata_and_nested_task_children ... ok
test native::dataview::tests::group_by_preserves_first_seen_order_and_member_access ... ok
test native::dataview::tests::grouped_sorting_repeated_grouping_and_lambda_shadowing ... ok
test native::gkeep::login::tests::cookie_line_picks_the_first_non_empty_line ... ok
test native::gkeep::ledger::tests::read_target_tasks_handles_missing_created_and_markers ... ok
test native::gkeep::plan::tests::empty_id_is_unknown ... ok
test native::gkeep::plan::tests::empty_note_is_skipped ... ok
test native::gkeep::ledger::tests::read_target_tasks_covers_top_level_tasks_only ... ok
test native::gkeep::plan::tests::ledger_hit_with_same_fingerprint_is_pending ... ok
test native::gkeep::model::tests::note_ref_is_pinned ... ok
test native::gkeep::model::tests::requests_serialize_with_protocol_and_op ... ok
test native::gkeep::ledger::tests::marker_parsing_finds_all_hits_and_ignores_broken_ones ... ok
test native::gkeep::plan::tests::limit_counts_only_actionable_notes ... ok
test native::gkeep::plan::tests::resolve_ids_prefers_exact_ids ... ok
test native::gkeep::plan::tests::pinned_beats_pending ... ok
test native::gkeep::plan::tests::notes_order_oldest_first_with_id_tiebreak ... ok
test native::gkeep::plan::tests::id_filter_narrows_to_selected_notes ... ok
test native::gkeep::plan::tests::pinned_and_shared_notes_stay_unless_included_or_selected ... ok
test native::gkeep::plan::tests::zero_width_only_text_is_empty ... ok
test native::gkeep::render::tests::capture_grammar_lookalikes_stay_literal ... ok
test native::gkeep::render::tests::display_title_is_unescaped ... ok
test native::gkeep::render::tests::empty_list_falls_back_to_untitled_title ... ok
test native::gkeep::plan::tests::ledger_hit_with_other_fingerprint_is_revised ... ok
test native::gkeep::plan::tests::journal_written_record_is_a_backstop ... ok
test native::gkeep::plan::tests::ledger_wins_over_journal ... ok
test native::gkeep::ledger::tests::scan_includes_done_and_skips_excluded_dirs ... ok
test native::gkeep::plan::tests::fresh_note_is_new ... ok
test native::gkeep::plan::tests::resolve_ids_rejects_unknown_and_ambiguous ... ok
test native::gkeep::render::tests::bare_list_markers_escape ... ok
test native::gkeep::render::tests::escape_child_text_covers_both_tables ... ok
test native::gkeep::render::tests::crlf_and_tabs_normalize ... ok
test native::gkeep::pull::tests::git_ancestor_checks_dot_git_files_and_dirs ... ok
test native::gkeep::render::tests::escape_task_text_leaves_intended_markup_alone ... ok
test native::gkeep::render::tests::labels_join_the_source_line ... ok
test native::gkeep::render::tests::leading_markers_cover_headings_breaks_and_fences ... ok
test native::gkeep::render::tests::image_with_ocr_renders_attachment_line_and_grandchildren ... ok
test native::capture_task_id::tests::recovers_a_shifted_line_and_returns_the_new_line ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_a_crlf_note_without_touching_other_bytes ... ok
test native::gkeep::render::tests::markdown_has_no_trailing_newline ... ok
test native::capture_task_id::tests::assigns_a_block_id_on_an_lf_note_and_returns_the_updated_ref ... ok
test native::gkeep::render::tests::list_with_checked_nested_and_empty_items ... ok
test native::gkeep::render::tests::markdown_looking_text_is_neutralized_in_children ... ok
test native::collect_done::tests::plan::self_healing_is_idempotent_after_links_are_repaired ... ok
test native::dataview::tasks::task::tests::all_priorities_have_tasks_v8_names_numbers_and_scores ... ok
test native::dataview::tasks::index::tests::paragraphs_break_list_hierarchy ... ok
test native::gkeep::config::tests::resolve_rejects_bad_config ... ok
test native::dataview::tasks::index::tests::dependency_graph_matches_direct_tasks_v8_semantics ... ok
test native::collect_done::tests::plan::task_moves_repair_dependency_ids_in_archive_and_all_dependents ... ok
test native::freshness::placement::placement_tests::keeps_fixture_vectors_match_rust ... ok
test native::dataview::tasks::task::tests::emoji_parser_extracts_all_fields_and_variant_selectors ... ok
test native::dataview::tasks::index::tests::fixture_index_builds_hierarchy_and_ignores_fences_and_dot_directories ... ok
test native::gkeep::render::tests::mixed_attachments_pluralize ... ok
test native::gkeep::render::tests::revision_flags_the_source_line ... ok
test native::gkeep::render::tests::space_indent_uses_two_spaces ... ok
test native::gkeep::render::tests::source_url_spoof_cannot_plant_a_marker ... ok
test native::dataview::tasks::index::tests::frontmatter_is_only_a_strictly_closed_column_zero_block ... ok
test native::gkeep::tests::error_exit_codes ... ok
test native::gkeep::ui::tests::age_buckets ... ok
test native::highlights_ref::clip_url::tests::validation_accepts_public_urls_and_strips_tracking ... ok
test native::gkeep::render::tests::unknown_attachment_kind_renders_as_files ... ok
test native::gkeep::ui::tests::spinner_frames_are_braille ... ok
test native::gkeep::render::tests::unicode_text_passes_through ... ok
test native::highlights_ref::clip_url::tests::stem_derivation_skips_noise_segments ... ok
test native::gkeep::render::tests::untitled_multiline_note_takes_first_line_as_title ... ok
test native::gkeep::render::tests::untitled_list_takes_first_item_as_title_but_keeps_it ... ok
test native::gkeep::ui::tests::spinner_start_and_drop_never_panics ... ok
test native::highlights_ref::clip_url::tests::validation_rejects_non_public_urls ... ok
test native::gkeep::render::tests::task_and_block_id_and_comment_and_field_hazards_escape ... ok
test native::highlights_ref::create::tests::title_prefers_frontmatter_then_h1_then_stem ... ok
test native::gkeep::render::tests::titled_note_renders_task_line_and_children ... ok
test native::highlights_ref::clip_url::tests::name_validation_strips_pdf_and_rejects_junk ... ok
test native::highlights_ref::clip_url::tests::dedupe_key_normalizes_spellings ... ok
test native::gkeep::render::tests::spoofed_marker_in_keep_text_cannot_survive ... ok
test native::highlights_ref::stamp::tests::exact_output_resolves_relative_and_tilde_paths ... ok
test native::highlights_ref::stamp::tests::marker_rejects_wikilink_parent_and_unknown_status ... ok
test native::highlights_ref::stamp::tests::normalize_lexically_drops_dot_and_parent_components ... ok
test native::highlights_ref::stamp::tests::marker_extras_insert_in_canonical_order_and_skip_empty ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker::frontmatter_projection_uses_marker_fields_without_fallback_parent ... ok
test native::highlights_ref::tests::marker::created_stays_note_local_despite_stale_marker_fields_opt_in ... ok
test native::highlights_ref::tests::marker::marker_parser_accepts_yaml_subset_and_normalizes_keys ... ok
test native::highlights_ref::tests::marker::frontmatter_render_preserves_unmanaged_keys ... ok
test native::highlights_ref::tests::marker::marker_parser_canonicalizes_parent_targets ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_created_key ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_linked_parent_targets ... ok
test native::highlights_ref::tests::marker::marker_renderer_rejects_unrepresentable_parent_links ... ok
test native::highlights_ref::tests::marker::marker_parser_rejects_missing_required_keys_type_and_duplicate_status ... ok
test native::highlights_ref::tests::marker::marker_renderer_uses_stable_key_order ... ok
test native::highlights_ref::tests::marker::parent_canonicalization_rejects_non_scalar_values ... ok
test native::highlights_ref::tests::marker::new_note_render_emits_exactly_one_created_line ... ok
test native::highlights_ref::tests::marker::status_validation_rejects_unsupported_and_non_scalar_values ... ok
test native::highlights_ref::tests::projection::deprecated_statuses_normalize_for_synced_inputs ... ok
test native::highlights_ref::tests::projection::pdf_path_metadata_derives_nested_reference_paths ... ok
test native::highlights_ref::tests::projection::pipeline_fields_exclude_marker_user_projection ... ok
test native::highlights_ref::tests::projection::projection_snapshot_json_round_trips_compact_user_projection ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_compatible_changes ... ok
test native::highlights_ref::tests::projection::projection_three_way_merge_handles_deletes_and_conflicts ... ok
test native::highlights_ref::tests::projection::relative_config_paths_resolve_under_bob_dir ... ok
test native::highlights_ref::tests::projection::validate_library_layout_rejects_equal_and_nested_paths ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_preserves_list_structure ... ok
test native::highlights_ref::tests::sidecar::annotation_block_id_is_stable_across_space_wrapping ... ok
test native::highlights_ref::tests::sidecar::beautify_annotation_text_reflows_and_dehyphenates ... ok
test native::highlights_ref::tests::sidecar::marker_content_decoder_preserves_pdfdoc_line_separators ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_strips_comment_bullet_markers ... ok
test native::highlights_ref::tests::sidecar::linked_sidecar_parser_keeps_wrapped_quotes_and_marker_mirror ... ok
test native::highlights_ref::tests::sidecar::pdf_text_artifact_cleanup_normalizes_extraction_noise ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_beautifies_callout_text ... ok
test native::highlights_ref::tests::sidecar::sidecar_page_heading_extracts_linked_page_label ... ok
test native::highlights_ref::tests::sidecar::sidecar_quote_continuation_does_not_capture_labeled_comment ... ok
test native::highlights_ref::tests::sidecar::rendered_annotation_blocks_do_not_include_source_task_anchors ... ok
test native::highlights_ref::tests::sidecar::sidecar_parser_extracts_image_annotations_and_leaves_non_images_as_notes ... ok
test native::highlights_ref::tests::sidecar::simple_sidecar_unlabeled_text_after_quote_remains_comment ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_contributes_abandoned ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_conflicts_with_competing_edit ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_maps_all_lifecycle_states ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_promotes_ready_and_back ... ok
test native::highlights_ref::tests::status::highlights_ref_pdf_task_status_signal_ready_reopens_terminal_to_ready ... ok
test native::highlights_ref::tests::tasks::annotation_task_batches_append_in_insertion_order ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_preserves_crlf_line_endings ... ok
test native::highlights_ref::tests::tasks::annotation_task_route_suffix_is_strict_and_stripped_from_identity ... ok
test native::highlights_ref::tests::status::highlights_ref_task_checkbox_rewrite_and_dirty_allowance_are_narrow ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_create_section_after_unterminated_ref_line ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_append_to_existing_tasks_section ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidates_extract_from_comments_and_notes ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_fill_empty_tasks_section_with_blank_lines ... ok
test native::highlights_ref::tests::tasks::annotation_task_insertion_is_idempotent_and_preserves_existing_states ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_ignore_fenced_and_managed_tasks_headings ... ok
test native::highlights_ref::tests::tasks::annotation_tasks_reuse_h1_or_closed_atx_tasks_heading ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_recognizes_generated_pdf_task ... ok
test native::highlights_ref::tests::tasks::highlights_ref_task_line_parser_rejects_malformed_and_duplicate_tasks ... ok
test native::markdown::tests::blockquote_and_indented_code_detection ... ok
test native::markdown::tests::setext_underline_accepts_levels_and_indent ... ok
test native::markdown::tests::split_line_ending_preserves_crlf_lf_and_none ... ok
test native::markdown::tests::standalone_html_comment_reads_inner_text ... ok
test native::note_ready::cli::tests::closest_names_suggest_up_to_three ... ok
test native::note_ready::render::tests::crowded_bars_mark_the_cap_and_overflow ... ok
test native::note_ready::render::tests::crowded_worklist_always_advertises_task_card_hints ... ok
test native::note_ready::render::tests::overview_all_clear_is_green_without_crowded_group ... ok
test native::note_ready::render::tests::overview_advertises_task_card_keys_on_any_day ... ok
test native::gkeep::config::tests::read_token_rejects_sign_in_cookie ... ok
test native::note_ready::render::tests::overview_names_crowded_notes_with_bars ... ok
test native::note_ready::render::tests::ready_gesture_hint_is_always_the_task_card_keys ... ok
test native::gkeep::config::tests::read_token_warns_but_keeps_unknown_shapes ... ok
test native::note_ready::render::tests::worklist_lists_rows_in_file_order ... ok
test native::note_ready::tests::ordering_is_crowded_full_room_empty_exempt ... ok
test native::note_ready::tests::r10_terminal_projects_are_not_capped ... ok
test native::note_ready::tests::lints_emit_once_per_note ... ok
test native::note_ready::tests::r11_all_type_forms_are_eligible ... ok
test native::note_ready::tests::r12_stamping_moves_new_to_ready_without_changing_count ... ok
test native::note_ready::tests::r14_config_cap_with_note_override ... ok
test native::note_ready::tests::r13_today_tasks_count_as_ready ... ok
test native::note_ready::tests::r1_six_tasks_is_crowded_over_by_one ... ok
test native::note_ready::tests::r2_five_tasks_is_full_without_lint ... ok
test native::note_ready::tests::r4_make_up_splits_new_rotten_ready ... ok
test native::highlights_ref::tests::sidecar::missing_image_asset_error_points_at_textbundle_export ... ok
test native::note_ready::tests::r3_lane_exclusions_never_count ... ok
test native::note_ready::tests::r5_recurring_excluded_and_counted ... ok
test native::note_ready::tests::r8_ready_cap_forms ... ok
test native::note_ready::tests::r9_nested_child_tasks_each_count ... ok
test native::highlights_ref::tests::tasks::annotation_task_candidate_records_route_and_processed_id ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_maps_nested_paths_and_companions ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_ht_backlink_blocks_edited_recreation ... ok
test native::highlights_ref::tests::tasks::processed_task_index_legacy_identity_blocks_recreation ... ok
test native::highlights_ref::tests::sidecar::render_sidecar_highlights_renders_image_assets_and_tasks ... ok
test native::highlights_ref::tests::sidecar::image_block_id_is_stable_across_asset_renames ... ok
test native::highlights_ref::tests::tasks::processed_task_index_scans_states_indents_and_done_notes ... ok
test native::highlights_ref::stamp::tests::exact_output_does_not_treat_sibling_prefix_as_managed ... ok
test native::note_tasks::tests::block_id_lookup_distinguishes_found_non_task_duplicate_and_missing ... ok
test native::note_ready::tests::r6_prj_rows_never_count ... ok
test native::highlights_ref::stamp::tests::exact_intake_refuses_mirrored_library_sidecar ... ok
test native::highlights_ref::tests::projection::plan_xlib_intake_reports_every_destination_conflict ... ok
test native::note_tasks::tests::ignores_frontmatter_and_fenced_code_tasks ... ok
test native::note_tasks::tests::computes_child_spans_for_mixed_indentation_blanks_and_eof ... ok
test native::note_tasks::tests::gates_on_filter_and_cleans_descriptions_with_sections ... ok
test native::note_tasks::tests::refs_resolve_exact_shifted_stale_and_ambiguous_tasks ... ok
test native::note_tasks::tests::task_refs_parse_strictly_and_round_trip_scan_metadata ... ok
test native::gkeep::adapter::tests::normal_exit_with_pipe_holding_straggler_returns_quickly ... ok
test native::note_tasks::tests::suggests_case_matches_and_unique_nearby_block_ids_only ... ok
test native::highlights_ref::stamp::tests::exact_output_accepts_uppercase_pdf_extension ... ok
test native::plan_budget::tests::four_themes_are_over_but_three_are_fine ... ok
test native::note_tasks::tests::reads_real_statuses_and_missing_settings_fall_back_to_defaults ... ok
test native::plan_budget::tests::alias_and_md_suffix_links_count ... ok
test native::highlights_ref::stamp::tests::default_target_derives_ref_type_output_and_valid_marker ... ok
test native::highlights_ref::stamp::tests::exact_external_target_does_not_invent_library_destination ... ok
test native::highlights_ref::stamp::tests::exact_output_refuses_same_stem_markdown_sidecar_even_with_force ... ok
test native::plan_budget::tests::cancelled_and_completed_entries_never_count ... ok
test native::plan_budget::tests::components_compare_case_insensitively ... ok
test native::highlights_ref::stamp::tests::exact_output_classifies_direct_library_target ... ok
test native::plan_budget::tests::empty_target_means_the_daily_note ... ok
test native::plan_budget::tests::markers_and_inner_hash_links_count ... ok
test native::plan_budget::tests::fenced_links_and_fenced_entries_never_count ... ok
test native::plan_budget::tests::eleven_links_are_over_the_cap ... ok
test native::plan_budget::tests::link_forms_count_once_and_exclusions_hold ... ok
test native::plan_budget::tests::lane_over_never_changes_status ... ok
test native::plan_budget::tests::missing_section_reports_empty ... ok
test native::plan_budget::tests::merged_name_counts_decks_once_with_duplicate_lint ... ok
test native::highlights_ref::stamp::tests::target_refuses_existing_library_pdf_even_with_force ... ok
test native::plan_budget::tests::open_inventory_label_counts_and_lints ... ok
test native::highlights_ref::stamp::tests::exact_output_rejects_non_pdf_paths ... ok
test native::highlights_ref::stamp::tests::target_refuses_existing_pdf_without_force ... ok
test native::highlights_ref::stamp::tests::target_refuses_highlights_markdown_sidecar_even_with_force ... ok
test native::plan_budget::today::tests::closed_entries_contribute_no_links ... ok
test native::highlights_ref::stamp::tests::target_refuses_existing_library_sidecar ... ok
test native::plan_budget::tests::running_and_highlight_flags_follow_ledger_order ... ok
test native::highlights_ref::stamp::tests::default_target_rejects_bad_stem_and_ref_type ... ok
test native::highlights_ref::stamp::tests::exact_intake_still_refuses_mirrored_library_pdf_with_force ... ok
test native::gkeep::adapter::tests::spawn_sets_parent_pid_env ... ok
test native::plan_budget::tests::unnamed_placeholder_counts_only_with_links ... ok
test native::plan_budget::tests::subheading_splits_time_totals_and_lints ... ok
test native::gkeep::adapter::tests::internal_ok_false_carries_stderr_tail ... ok
test native::plan_budget::today::tests::mixed_and_nested_bullets_are_not_dedicated_links ... ok
test native::plan_budget::today::tests::aliased_links_pin_the_lineup_behavior ... ok
test native::plan_budget::today::tests::fenced_links_never_count ... ok
test native::plan_budget::today::tests::gtd_empty_target_resolves_to_the_daily_note ... ok
test native::plugins::tests::sync_reports_text_diff_for_changed_files ... ok
test native::plugins::tests::truncate_adds_ellipsis_only_when_needed ... ok
test native::highlights_ref::create::tests::plan_embeds_markdown_stem_id_when_opted_in ... ok
test native::plan_budget::today::tests::duplicate_links_dedupe_to_the_first_position ... ok
test native::plugins::tests::sync_summarizes_binary_and_minified_diffs ... ok
test native::pomodoro::tests::completed_ledger_parser_only_accepts_x_checkbox_entries ... ok
test native::highlights_ref::stamp::tests::exact_output_keeps_nested_path_and_filename ... ok
test native::pomodoro::tests::open_ledger_parser_requires_an_open_checkbox ... ok
test native::plan_budget::today::tests::done_and_cancelled_tasks_drop_out_while_blocked_stays ... ok
test native::plugins::tests::unreadable_repo_is_an_error ... ok
test native::plan_budget::today::tests::missing_notes_lint_and_drop_out ... ok
test native::highlights_ref::stamp::tests::exact_library_target_requires_force_and_skips_mirrored_check ... ok
test native::projects::tests::edits::project_changes_clean_duplicate_subproject_marker_lines ... ok
test native::projects::tests::edits::project_changes_delete_subproject_line_for_stale_child ... ok
test native::plugins::tests::json_shape_is_stable ... ok
test native::pomodoro::tests::unclosed_frontmatter_delimiter_is_content ... ok
test native::plan_budget::today::tests::markers_struck_and_embedded_follow_the_lineup_rule ... ok
test native::projects::tests::edits::project_changes_insert_subproject_line_above_user_bullets ... ok
test native::plugins::tests::sync_unknown_plugin_is_an_error ... ok
test native::plugins::tests::vault_state_reads_enabled_disabled_and_not_installed ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_prj_with_tab_indent ... ok
test native::projects::tests::edits::project_changes_mark_last_child_closed_and_keep_subproject_line ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_for_subproject_link_insertions ... ok
test native::projects::tests::edits::project_changes_preserve_crlf_when_appending_status ... ok
test native::projects::tests::edits::project_changes_remove_prj_fields_with_adjacent_whitespace ... ok
test native::projects::tests::edits::project_changes_insert_subproject_links_after_final_prj_line ... ok
test native::projects::tests::edits::project_changes_remove_prj_hide_tag_with_crlf ... ok
test native::ob::tests::detect_git_worktree_reports_non_worktree ... ok
test native::projects::tests::edits::project_changes_replace_status_append_missing_status_and_add_hide_tag ... ok
test native::projects::tests::edits::schedule_only_issues_still_allow_subproject_aggregation ... ok
test native::projects::tests::edits::project_changes_rewrite_subproject_line_in_place ... ok
test native::projects::tests::parse::non_project_notes_are_ignored ... ok
test native::projects::tests::edits::task_schedule_edits_cover_contract_and_preserve_markdown ... ok
test native::projects::tests::parse::task_tag_matches_tasks_plugin_boundaries ... ok
test native::projects::tests::parse::wikilink_target_extracts_normalized_note_names ... ok
test native::projects::tests::edits::frontmatter_keys_must_start_at_column_zero ... ok
test native::projects::tests::parse::type_forms_all_match_project_and_area ... ok
test native::projects::tests::edits::scheduled_tasks_keep_subproject_ledger_planning ... ok
test native::highlights_ref::stamp::tests::stamp_install_without_info_leaves_trailer_info_absent ... ok
test native::projects::tests::edits::project_parser_splits_surfacing_and_dash_visibility_counts ... ok
test native::projects::tests::parse::project_parser_marks_unprioritized_prj_as_on_dash ... ok
test native::projects::tests::edits::terminal_projects_do_not_reconcile_task_schedules ... ok
test native::projects::tests::parse::project_parser_reads_parent_wikilink_target ... ok
test native::projects::tests::parse::project_parser_records_scheduled_and_placeholder_prj ... ok
test native::projects::tests::parse::project_parser_stops_prj_sub_block_at_blank_line ... ok
test native::projects::tests::sync::render_subprojects_line_formats_closed_children_after_open_children ... ok
test native::projects::tests::sync::subproject_display_parser_scopes_schedule_and_lifecycle_markers ... ok
test native::projects::tests::sync::project_sync_plan_flips_status_without_prj_edits_after_effective_status ... ok
test native::plugins::tests::pull_repo_skips_non_git_directory ... ok
test native::randomize_plan::tests::counts_due_p0_tasks_but_ignores_the_rest ... ok
test native::highlights_ref::stamp::tests::stamp_install_appends_when_annots_exist_and_sets_partial_info ... ok
test native::randomize_plan::tests::dates_survive_insertions_above_because_identity_ignores_lines ... ok
test native::randomize_plan::tests::extreme_priority_window_fails_before_any_write ... ok
test native::randomize_plan::tests::identical_lines_get_distinct_rolls ... ok
test native::randomize_plan::tests::fixed_offsets_cross_month_year_and_leap_boundaries ... ok
test native::randomize_plan::tests::ignores_non_open_and_fieldless_and_foreign_tasks ... ok
test native::randomize_plan::tests::ignores_tasks_scheduled_after_until ... ok
test native::randomize_plan::tests::level_filtering_counts_not_selected ... ok
test native::randomize_plan::tests::keeps_paren_fields_and_spacing_when_replacing_the_date ... ok
test native::randomize_plan::tests::level_filtering_matches_labels_case_insensitively ... ok
test native::randomize_plan::tests::load_covers_35_days_with_p0_and_new_dates ... ok
test native::randomize_plan::tests::matches_pomodoro_targets_by_path_stem_and_case ... ok
test native::plugins::tests::sync_only_filters_to_a_single_plugin ... ok
test native::randomize_plan::tests::project_note_postimage_moves_the_task_under_blocked ... ok
test native::randomize_plan::tests::ordinary_and_daily_notes_are_edited_but_not_regrouped ... ok
test native::randomize_plan::tests::project_postimage_is_byte_exact_with_blocked_move_and_badge ... ok
test native::randomize_plan::tests::reroll_carries_every_json_task_field ... ok
test native::randomize_plan::tests::roll_at_the_representable_boundary_succeeds_and_past_it_fails ... ok
test native::randomize_plan::tests::rerolls_ready_and_blocked_tasks ... ok
test native::plugins::tests::backup_failure_aborts_overwrite ... ok
test native::randomize_plan::tests::same_inputs_give_the_same_plan ... ok
test native::randomize_plan::tests::skips_duplicate_priority_and_scheduled_fields ... ok
test native::randomize_plan::tests::skips_non_ready_open_statuses ... ok
test native::randomize_plan::tests::skips_hard_dates_from_fields_and_emoji ... ok
test native::randomize_plan::tests::skips_unknown_priority_values_with_detail ... ok
test native::randomize_plan::tests::skips_unparseable_scheduled_dates ... ok
test native::randomize_plan::tests::zero_width_window_reports_unchanged_without_writing ... ok
test native::task_dependencies::tests::dependency_line_guard_matches_every_form ... ok
test native::task_dependencies::tests::dp_discovery_context_vectors ... ok
test native::randomize_plan::tests::until_shifts_both_the_cutoff_and_the_roll_base ... ok
test native::task_dependencies::tests::dp_vectors ... ok
test native::task_dependencies::tests::dw_create_and_identity_vectors ... ok
test native::task_dependencies::tests::dw_indent_and_ending_vectors ... ok
test native::task_dependencies::tests::dw_link_form_vectors ... ok
test native::task_dependencies::tests::dw_writer_form_vectors ... ok
test native::randomize_plan::tests::skips_tasks_linked_from_open_pomodoros_in_every_link_form ... ok
test native::task_dependencies::tests::legacy_child_shapes ... ok
test native::task_fields::tests::finds_bracket_and_paren_forms ... ok
test native::task_fields::tests::filters_by_key ... ok
test native::task_fields::tests::format_round_trips_through_strict_parse ... ok
test native::task_fields::tests::has_any_field_checks_several_keys ... ok
test native::task_fields::tests::matches_with_no_space_after_the_colons ... ok
test native::task_fields::tests::key_match_is_case_sensitive ... ok
test native::gkeep::ledger::tests::journal_append_writes_leading_newline_after_torn_record ... ok
test native::task_fields::tests::matches_with_spacing_around_the_colons ... ok
test native::task_fields::tests::reports_exact_byte_ranges ... ok
test native::task_fields::tests::strict_date_rejects_impossible_february ... ok
test native::task_fields::tests::strict_date_rejects_non_dates ... ok
test native::task_fields::tests::reports_duplicate_fields_in_order ... ok
test native::capture_clip::tests::saves_reuses_and_hash_suffixes_attachments_atomically ... ok
test native::task_status_groups::tests::authored_heading_inside_a_managed_group_fails_closed ... ok
test native::task_status_groups::tests::badge_anchors_percent_encode_the_obsidian_path_segments ... ok
test native::task_status_groups::tests::badge_row_is_not_a_task_or_ambiguous_boundary ... ok
test native::task_status_groups::tests::badge_counts_refresh_when_membership_changes ... ok
test native::task_status_groups::tests::authored_child_containers_get_independent_badges_and_anchors ... ok
test native::task_status_groups::tests::badge_marker_in_intake_is_relocated_to_the_slot ... ok
test native::task_status_groups::tests::authored_topics_receive_local_groups ... ok
test native::task_status_groups::tests::blockless_and_duplicate_ids_still_group ... ok
test native::task_status_groups::tests::conservation_and_source_records ... ok
test native::task_status_groups::tests::custom_terminal_statuses_and_registry_precedence ... ok
test native::task_status_groups::tests::empty_global_filter_accepts_all_checkbox_tasks ... ok
test native::task_status_groups::tests::crlf_mixed_endings_unicode_and_missing_final_newline ... ok
test native::task_status_groups::tests::global_filter_rejects_non_matching_lines ... ok
test native::task_status_groups::tests::h6_tasks_is_skipped_with_a_diagnostic ... ok
test native::task_status_groups::tests::heading_hash_in_ancestry_renders_unlinked_badges ... ok
test native::task_status_groups::tests::lazy_continuation_skips_the_container ... ok
test native::task_status_groups::tests::heading_only_first_setup_is_a_change ... ok
test native::task_status_groups::tests::excluded_markdown_contexts_are_not_task_roots_or_headings ... ok
test native::task_status_groups::tests::malformed_and_duplicate_markers_fail_closed ... ok
test native::task_status_groups::tests::empty_groups_are_retained_once_created ... ok
test native::task_status_groups::tests::malformed_badge_markers_fail_closed ... ok
test native::task_status_groups::tests::ordered_list_roots_and_nested_ordinary_items_are_reported ... ok
test native::task_status_groups::tests::orphaned_badge_block_is_removed_without_creating_groups ... ok
test native::task_status_groups::tests::nested_children_travel_with_parent_status ... ok
test native::task_status_groups::tests::nested_tasks_is_processed_once ... ok
test native::task_status_groups::tests::ready_only_and_empty_sections_are_not_decorated ... ok
test native::task_status_groups::tests::multiple_tasks_headings_and_heading_syntax_variants ... ok
test native::task_status_groups::tests::out_of_scope_spans_are_byte_identical ... ok
test native::task_status_groups::tests::skip_codes_are_stable ... ok
test native::task_status_groups::tests::prose_inside_managed_groups_is_preserved ... ok
test native::task_status_groups::tests::unmarked_group_title_with_prose_is_a_collision ... ok
test native::task_status_groups::tests::safe_legacy_adoption_completes_a_partial_set ... ok
test native::task_status_groups::tests::reopening_a_task_to_ready_appends_to_intake ... ok
test native::task_status_groups::tests::standalone_prose_is_not_attached_to_a_task ... ok
test native::task_status_groups::tests::tabs_internal_blanks_and_fences_stay_in_the_task_block ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_drops_both_fields_for_r9 ... ok
test native::task_status_hooks::reconcile::fields::tests::dr_field_projection_vectors ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_places_id_before_depends_on_before_block_id ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_lands_right_of_fresh_and_replaces_stale ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_removes_depends_on_when_empty ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_field_before_trailing_tags ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_fields_between_tags ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_parenthesized_metadata ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_stamps_target_past_hide_tag ... ok
test native::task_status_hooks::retry::tests::allowed_transient_reasons_are_retried_without_applied_files ... ok
test native::task_status_hooks::retry::tests::any_error_listing_applied_files_is_never_retried ... ok
test native::task_status_hooks::retry::tests::partial_apply_is_never_retried_even_with_no_applied_files ... ok
test native::task_status_hooks::retry::tests::random_unit_interval_varies_and_stays_in_unit_range ... ok
test native::task_status_hooks::retry::tests::retry_ceiling_progression_caps_at_thirty_seconds ... ok
test native::task_status_hooks::retry::tests::retry_delay_stays_within_upper_half_of_ceiling ... ok
test native::task_status_hooks::retry::tests::retry_loop_stops_immediately_on_terminal_reason_without_noise ... ok
test native::task_status_hooks::retry::tests::retry_decision_log_includes_run_attempt_reason_and_recovery_directory ... ok
test native::task_status_hooks::retry::tests::terminal_and_unknown_reasons_are_never_retried ... ok
test native::task_status_hooks::tests::structure::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::task_status_hooks::tests::structure::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::structure::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::tests::structure::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::structure::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::structure::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_hooks::tests::structure::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::tests::structure::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::structure::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::structure::dependency_lines_are_not_legacy_children ... ok
test native::task_status_hooks::tests::structure::direct_child_scan_counts_plain_children_but_ignores_fences ... ok
test native::task_status_hooks::tests::structure::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::structure::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::structure::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::structure::empty_pomodoro_deletion_removes_full_blocks_and_preserves_crlf_eof ... ok
test native::task_status_hooks::tests::structure::empty_timed_entries_are_not_current_targets_or_ambiguity_inputs ... ok
test native::task_status_hooks::tests::structure::entries_emptied_by_duplicate_cleanup_are_removed_in_same_pass ... ok
test native::task_status_hooks::tests::structure::extracts_only_block_links_under_open_pomodoros ... ok
test native::task_status_hooks::tests::structure::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::tests::structure::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::structure::moving_last_child_removes_source_but_retains_destination ... ok
test native::task_status_hooks::tests::structure::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::structure::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::structure::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::task_status_hooks::tests::structure::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::structure::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::structure::two_non_empty_timed_entries_still_match_the_ambiguity_guard ... ok
test native::task_status_hooks::tests::sync::ambiguous_basename_does_not_resolve ... ok
test native::task_status_hooks::tests::sync::archive_targets_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::sync::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::task_status_hooks::tests::sync::dependency_line_links_are_promotion_edges ... ok
test native::task_status_hooks::tests::sync::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::tests::sync::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::sync::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::sync::legacy_children_without_field_coverage_are_not_edges ... ok
test native::task_status_hooks::tests::sync::legacy_plain_embedded_and_struck_children_are_edges_with_field_coverage ... ok
test native::task_status_hooks::tests::sync::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::plan_budget::tests::lane_queries_parse_through_the_native_engine ... ok
test native::task_status_hooks::tests::sync::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::sync::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::sync::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::tests::sync::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::projects::tests::sync::project_sync_plan_skips_subproject_links_without_open_prj_edits ... ok
test native::task_status_hooks::retry::tests::retry_loop_never_starts_another_attempt_once_budget_is_exhausted ... ok
test native::gkeep::adapter::tests::exiting_without_reading_reports_stdout_not_stdin ... ok
test native::task_status_hooks::tests::sync::reading_embeds_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::sync::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::projects::tests::sync::subproject_parent_links_classify_open_and_terminal_prj_children ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_open_subprojects ... ok
test native::projects::tests::sync::project_sync_plan_keeps_canonical_closed_subprojects_idempotent ... ok
test native::task_status_hooks::tests::sync::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::sync::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::tests::sync::sticky_lanes_keep_next_and_in_progress_outside_daily_notes ... ok
test native::task_status_hooks::tests::sync::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::projects::tests::sync::subproject_state_treats_terminal_open_prj_child_as_open ... ok
test native::task_status_hooks::tests::sync::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test native::task_status_hooks::tests::sync::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
test native::task_status_hooks_write::tests::deletion_prevents_write ... ok
test native::task_status_hooks_write::tests::future_mtime_defers_without_sleeping ... ok
test native::task_status_hooks_write::tests::live_rescan_sees_new_vault_file ... ok
test native::gkeep::config::tests::read_token_rejects_empty_and_failing_commands ... ok
test native::task_status_hooks_write::tests::multiply_linked_output_is_rejected ... ok
test native::capture_complete::tests::task_links::task_link_human_rows_name_queues_and_missing_ids ... ok
test native::task_status_hooks_write::tests::new_or_deleted_scan_candidate_invalidates_plan ... ok
test native::task_status_hooks_write::tests::noop_creates_no_recovery_or_staging ... ok
test native::task_status_hooks_write::tests::replacement_inode_prevents_write ... ok
test native::task_status_hooks_write::tests::changed_previous_daily_prevents_write ... ok
test native::task_status_hooks_write::tests::equal_length_change_with_restored_mtime_prevents_write ... ok
test native::task_status_hooks_write::tests::changed_tasks_settings_prevent_write ... ok
test native::task_status_hooks_write::tests::quiet_period_waits_once_then_defers_if_changed ... ok
test native::task_status_groups::tests::golden_layout_groups_every_status_bucket_and_keeps_ready_intake ... ok
test native::task_status_hooks_write::tests::symlink_substitution_prevents_write ... ok
test native::vault_links::tests::basename_walk_skips_hidden_directories ... ok
test native::vault_links::tests::exact_root_note_does_not_build_the_vault_index ... ok
test runner::tests::alias_rewrite_preserves_separator_and_non_utf8_tail ... ok
test runner::tests::aliases_resolve_to_leaves_and_do_not_collide_with_root_names ... ok
test runner::tests::every_native_command_is_on_exactly_one_canonical_path ... ok
test native::vault_links::tests::resolves_exact_path_before_unique_case_insensitive_basename ... ok
test runner::tests::subcommands_are_contiguous_in_section_order_and_alphabetical ... ok
test native::highlights_ref::stamp::tests::stamp_install_embeds_marker_and_info_without_annots ... ok
test runner::tests::build_cli_renders_without_panicking ... ok
warning: You appear to have cloned an empty repository.
test native::gkeep::adapter::tests::token_travels_on_stdin_never_argv ... ok
test native::plugins::tests::sync_refuses_then_forces_a_dirty_vault_file ... ok
test native::gkeep::adapter::tests::every_request_carries_protocol_version ... ok
test native::gkeep::ledger::tests::journal_append_round_trips_with_tight_permissions ... ok
test native::ob::tests::commit_paths_scopes_to_listed_paths ... ok
test native::capture_pomodoro_close::linked_task_tests::embedded_recursion_obeys_depth_and_target_caps ... ok
test native::plugins::tests::scan_reports_states_and_counts ... ok
test native::plugins::tests::sync_state_detects_synced_drift_and_missing ... ok
test native::dataview::tests::flatten_aliases_empty_null_and_scalar_values ... ok
test native::task_status_hooks::retry::tests::retry_loop_with_zero_budget_makes_one_attempt_and_never_sleeps ... ok
test native::projects::tests::parse::project_parser_records_prj_sub_block_marker_lines ... ok
test native::plugins::tests::sync_dry_run_reports_without_writing ... ok
test native::task_status_hooks::retry::tests::retry_loop_clamps_sleep_to_remaining_budget ... ok
test native::projects::tests::parse::project_parser_accepts_bare_project_type_and_prj_states ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subprojects_marker_line ... ok
test native::projects::tests::sync::project_sync_plan_marks_tracked_closed_subprojects ... ok
test native::projects::tests::parse::project_parser_accepts_project_type_variants_and_counts_tasks ... ok
test native::projects::tests::parse::project_parser_reports_malformed_and_multiple_prj_lines ... ok
test native::projects::tests::sync::project_sync_plan_warns_on_placeholder_while_reopening ... ok
test native::projects::tests::sync::project_sync_plan_removes_stale_scheduled_field ... ok
test native::projects::tests::parse::project_parser_accepts_prj_tag_and_strips_it_from_description ... ok
test native::plugins::tests::sync_creates_updates_and_leaves_unchanged ... ok
test native::plugins::tests::sync_preserves_runtime_data_json ... ok
test native::projects::tests::sync::project_sync_plan_treats_user_sub_bullets_as_user_owned ... ok
test native::projects::tests::sync::project_sync_plan_matches_subproject_links_case_insensitively ... ok
test native::projects::tests::sync::project_sync_plan_normalizes_subprojects_marker_drift ... ok
test native::projects::tests::sync::project_sync_plan_reconciles_subproject_schedule_markers ... ok
test native::capture_clip::tests::aggregate_planner_flattens_entries_and_reserves_all_paths ... ok
test native::task_status_hooks::retry::tests::retry_loop_retries_lock_contention_then_succeeds ... ok
test native::projects::tests::edits::project_schedule_accepts_quoted_dates_and_rejects_bad_dates ... ok
test native::projects::tests::sync::project_sync_plan_leaves_non_terminal_open_prj_status_untouched ... ok
test native::projects::tests::sync::project_sync_plan_reopens_terminal_project_from_open_prj ... ok
test native::projects::tests::edits::scheduled_tasks_precede_prj_surfacing_at_local_date_boundary ... ok
test native::projects::tests::sync::project_sync_plan_is_idempotent_when_prj_hide_tag_matches_dash_state ... ok
test native::projects::tests::sync::subproject_aggregation_marks_only_schedules_after_shared_today ... ok
test native::projects::tests::edits::due_scheduled_projects_follow_the_normal_surfacing_rule ... ok
test native::projects::tests::sync::project_sync_plan_manages_prj_hide_tag_from_unhidden_count ... ok
test native::gkeep::adapter::tests::ping_snapshot_archive_round_trip ... ok
test native::gkeep::adapter::tests::large_request_with_fast_exit_succeeds ... ok
test native::note_ready::tests::scan_covers_r11_r8_terminal_and_recurring ... ok
test native::note_ready::tests::scan_excludes_r3_and_r7_paths ... ok
test native::gkeep::adapter::tests::error_kinds_carry_messages_and_hints ... ok
test native::task_status_hooks_write::tests::edit_between_staging_and_revalidate_survives ... ok
test native::completion::present::tests::structural_latency_is_warn_only ... ok
test native::plugins::tests::pull_repo_fast_forwards_from_remote ... ok
test native::task_status_hooks_write::tests::staging_failure_preserves_notes_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::exclusive_temp_and_mode_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::fresh_attempt_after_vault_changed_replans_from_intervening_edit ... ok
test native::task_status_hooks_write::tests::retention_keeps_incomplete_and_prunes_old_completed ... ok
test native::task_status_hooks_write::tests::tool_scopes_recovery_root_manifest_and_pruning ... ok
test native::task_status_hooks_write::tests::edit_before_later_replacement_reports_partial ... ok
test native::task_status_hooks_write::tests::unchanged_read_set_applies_and_records_recovery_bytes ... ok
test native::highlights_ref::create::tests::code_break_filter_splits_long_inline_code_paths ... ok
test native::ob::tests::lock_wait_behavior ... ok
test native::capture_clip::tests::rejects_unsupported_and_unmigrated_clipy_databases ... ok
test native::task_status_hooks_write::tests::quiet_period_skips_wait_for_stable_files_and_status_only ... ok
test native::gkeep::adapter::tests::crash_garbage_and_timeout ... ok
test native::capture_clip::tests::reads_clipy_sqlite_assets_in_deterministic_order ... ok
test native::gkeep::adapter::tests::timeout_kills_grandchild_holding_stdout ... ok
test native::gkeep::adapter::tests::large_request_with_hanging_adapter_times_out ... ok

failures:

---- native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes stdout ----

thread 'native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes' (1936011) panicked at src/native/capture_pomodoros.rs:1196:9:
assertion `left == right` failed
  left: 1
 right: 0


failures:
    native::capture_pomodoros::tests::missing_note_and_missing_section_are_warning_successes

test result: FAILED. 1653 passed; 1 failed; 0 ignored; 0 measured; 0 filtered out; finished in 2.23s

error: test failed, to rerun pass `--lib`
error: recipe `test` failed on line 20 with exit code 101
failed  exit=101  duration=97637ms

