# Chat History - ace-run (bob-cli-ey.1.1.1--mon-0)

- **TIMESTAMP:** 2026-10-31 14:00:38 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-ey.1.1.1--mon-0

## Prompt

sase monitor start --command 'just docs-gen && just docs-check && just check' --reason 'Run regenerated capture docs and the full Rust verification suite after the global route block-ID removal'

## Response

sase tool run 2fa5c52bf882c8e2a024114790469787

⚙️  DOCS GENERATE
────────────────────────────────────────────────
BOB_UPDATE_GOLDENS=1 cargo test --test cli docs_reference
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.24s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261031_133254/build/debug/deps/cli-e2865b96c4cb0370)

running 1 test
test docs_reference::cli_reference_is_current ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 2566 filtered out; finished in 1.10s

uv run --project tools/docs bob-docs gen
Generated inventory for 8 plugins and 101 registered commands.

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
bob-docs lint: ok
docs-check: passed (lint)

docs-check: generated drift
Plugin documentation inventory is up to date.
generated contract content is up to date
docs-check: passed (generated drift)

docs-check: strict Zensical build
Build started
No issues found
Build finished in 17.41s
running: zensical build --strict --config-file /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/mkdocs.yml
built site: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site
docs-check: passed (strict Zensical build)

docs-check: published URLs
wrote /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/urls.txt (179 published pages)
urls: OK (179 pages, 550 mentions checked, 60 curated links)
docs-check: passed (published URLs)

docs-check: offline lychee with fragments
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/task-completion-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/task-completion-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/task-completion.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/task-completion.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/capture-agenda.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/capture-agenda.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/refs-browse-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/refs-browse-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/refs-browse.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/reference/mac-capture/images/refs-browse.png'
🔍 42770 Total (in 2s 531ms) 🔗 2784 Unique ✅ 41772 OK 🚫 0 Errors 👻 998 Excluded

running: /home/bryan/.cache/bob-docs/bin/lychee --offline --no-progress --include-fragments --exclude-path (^|/)index[.]md$ --index-files index.html --root-dir /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site --remap https://bobs-org.github.io/ file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/ /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site
links: OK (offline lychee with fragment checking)
docs-check: passed (offline lychee with fragments)

docs-check: edit links point at real sources
edit-links: OK (177 edit link(s) point at real source files)
docs-check: passed (edit links point at real sources)

docs-check: search smoke
search smoke: OK (110 cases; index /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/target/docs/site/search.json)
docs-check: passed (search smoke)

docs-check: executable first-day tutorial
   Compiling bitflags v2.12.1
   Compiling png v0.18.1
   Compiling lopdf v0.40.0
   Compiling image v0.25.10
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 1m 50s

TUTORIAL_FENCE 5 docs/start/install.md:67
bob 0.4.0

TUTORIAL_FENCE 7 docs/start/first-bob-day.md:24
Using demo vault: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws11-261031_133254/bob-docs-sandbox-o02l6nv4/tmp/bob-first-day.fh2Gut/vault

TUTORIAL_FENCE 8 docs/start/first-bob-day.md:46
✓ captured  mac_inbox.md
  - [ ] #task Sort the seed packets [created::2026-10-20] ^seed-packet

TUTORIAL_FENCE 9 docs/start/first-bob-day.md:61
✓ captured  garden.md
  - [ ] #task Water the seedlings [created::2026-10-20] ^seedlings

TUTORIAL_FENCE 10 docs/start/first-bob-day.md:76
bob plan - Tue 2026-10-20 - no daily note yet

  PLAN  0/3 types - 0/10 links      TODAY 0 - PENDING 0/10 - NEXT 0/15


TUTORIAL_FENCE 11 docs/start/first-bob-day.md:92
Created daily note: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws11-261031_133254/bob-docs-sandbox-o02l6nv4/tmp/bob-first-day.fh2Gut/vault/2026/20261020.md

TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117
✓ started  2026/20261020.md
  FOCUS 0905-0930 (25m) (created) at line 4
  - [ ] (**0905-0930** [t:: 25m]) — FOCUS
  nothing queued
plan 1/3 types · 0/10 links  (+1 type: FOCUS)

TUTORIAL_FENCE 13 docs/start/first-bob-day.md:128
✓ link  garden.md
  [ ] → [*]  Water the seedlings  ^seedlings
  Linked under FOCUS
plan 1/3 types · 1/10 links
{"caps":{"max_links":10,"max_next":15,"max_pending":10,"max_ready":100,"max_themes":3,"strict":false},"daily_file":"2026/20261020.md","date":"2026-10-20","entries":[{"components":["FOCUS"],"exempt":false,"highlight":true,"homes":{"chip":"garden","hue":"magenta","kind":"work","label":"garden","parts":[{"area":"garden.md","area_label":"garden","hue":"magenta","key":"garden.md","kind":"area","label":"garden","share":100,"tasks":1}],"state":"forecast"},"line":4,"links":1,"name":"FOCUS","running":true,"themes":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"time_range":"0905-0930"}],"links":{"cap":10,"count":1,"over":false},"next":{"cap":15,"count":1,"over":false},"ok":true,"pending":{"cap":10,"count":0,"over":false},"schema_version":2,"status":"ok","theme_names":["FOCUS"],"theme_refs":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"themes":{"cap":3,"count":1,"over":false},"today":{"count":1},"today_tasks":[{"block_id":"seedlings","entry_line":4,"entry_name":"FOCUS","ledger_line":5,"line":8,"path":"garden.md","status_name":"Next","status_symbol":"*","text":"Water the seedlings"}],"warnings":[]}

TUTORIAL_FENCE 14 docs/start/first-bob-day.md:141
✓ closed FOCUS 0905-0930 → 0905-0905 (0m, −25m) · 2026/20261020.md line 4
  1 [*] → [x] Water the seedlings garden.md ^seedlings
  next: FOCUS (created) at line 6 · carries 0 links
plan 1/3 types · 0/10 links

TUTORIAL_FENCE 15 docs/start/first-bob-day.md:154
{"config":{"decay":{"enabled":true,"enter":null,"keeps":3},"interval":7,"next_interval":1,"pending_interval":1,"project_interval":null,"rotten_daily_budget":null},"counts":{"budget":null,"budget_met":false,"by_tier":{"new":1,"next":0,"pending":0,"post":0,"pre":0,"projects":1,"recurring":0,"rotten":0,"tickler":0},"decide":0,"due":2,"fresh":0,"new":2,"next_due":0,"pending_due":0,"post_due":0,"pre_due":0,"projects_due":1,"recurring_due":0,"refreshed_today":1,"resurfaced":0,"rotten":0,"upkeep_today":1,"walk":2},"date":"2026-10-20","ok":true,"queue":[{"block_id":"seed-packet","bucket":"new","created":"2026-10-20","days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":7,"path":"mac_inbox.md","rank":1,"returned_by":null,"scheduled":null,"state":"new","status_symbol":" ","text":"Sort the seed packets ^seed-packet","tier":"new","unblocked_on":null},{"block_id":"prj","bucket":"new","created":null,"days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":11,"path":"Projects/seedlings.md","rank":2,"returned_by":null,"scheduled":null,"state":"new","status_symbol":" ","text":"#prj Raise healthy seedlings for the garden ^prj","tier":"projects","unblocked_on":null}],"schema_version":14,"warnings":[]}
skipped: docs/start/install.md:16: network clone needs a remote and user credentials
skipped: docs/start/install.md:27: toolchain install changes the host and needs network
skipped: docs/start/install.md:42: install writes outside the tutorial sandbox
skipped: docs/start/install.md:61: PATH export edits the reader shell profile
skipped: docs/start/install.md:87: network install needs a remote and writes outside the sandbox
skipped: docs/start/obsidian.md:18: opening Obsidian needs the desktop app
skipped: docs/start/obsidian.md:28: Tasks install needs the Obsidian app and network
skipped: docs/start/obsidian.md:52: plugin clone needs network and a plugin source checkout
skipped: docs/start/obsidian.md:57: plugin sync needs a plugin source checkout and Obsidian
skipped: docs/start/mac-capture.md:19: Mac build needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:26: Mac bundle needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:33: Mac install needs macOS and the Apple toolchain
skipped: docs/start/mac-capture.md:40: Mac launch needs the Mac app bundle
skipped: docs/start/mac-capture.md:54: panel setup needs the Mac app
skipped: docs/start/mac-capture.md:81: first Mac capture needs the Mac panel
tutorial: passed
docs-check: passed (executable first-day tutorial)

docs-check: CLI media determinism
media: check passed (regeneration is byte-stable)
docs-check: passed (CLI media determinism)

docs-check: documentation unit tests
============================= test session starts ==============================
platform linux -- Python 3.14.4, pytest-9.1.1, pluggy-1.7.0
rootdir: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/tools/docs
configfile: pyproject.toml
plugins: platformdirs-4.13.5
collected 448 items

tools/docs/tests/test_assemble.py ....                                   [  0%]
tools/docs/tests/test_assets.py .....s.                                  [  2%]
tools/docs/tests/test_capture_token_coverage.py ..                       [  2%]
tools/docs/tests/test_check.py ....                                      [  3%]
tools/docs/tests/test_compatibility.py ......                            [  5%]
tools/docs/tests/test_contracts.py ........                              [  6%]
tools/docs/tests/test_demo_tasks.py ..                                   [  7%]
tools/docs/tests/test_edit_links.py ....                                 [  8%]
tools/docs/tests/test_environment.py ........                            [ 10%]
tools/docs/tests/test_fences.py .......                                  [ 11%]
tools/docs/tests/test_gen_components.py ....                             [ 12%]
tools/docs/tests/test_gen_plugins.py ...........                         [ 14%]
tools/docs/tests/test_gen_reference.py ........                          [ 16%]
tools/docs/tests/test_generated.py .....                                 [ 17%]
tools/docs/tests/test_host.py ..................                         [ 21%]
tools/docs/tests/test_host_workflow.py .........                         [ 23%]
tools/docs/tests/test_links.py ...........                               [ 26%]
tools/docs/tests/test_links_online.py ......                             [ 27%]
tools/docs/tests/test_lint.py .......................................... [ 37%]
................                                                         [ 40%]
tools/docs/tests/test_media.py .........                                 [ 42%]
tools/docs/tests/test_mounts.py ........................................ [ 51%]
....................................                                     [ 59%]
tools/docs/tests/test_publish_drill.py ..........                        [ 61%]
tools/docs/tests/test_publish_issue.py .............                     [ 64%]
tools/docs/tests/test_publish_plan.py ........................           [ 70%]
tools/docs/tests/test_publish_record.py ..............                   [ 73%]
tools/docs/tests/test_publish_verify.py ...........                      [ 75%]
tools/docs/tests/test_publish_workflow.py .........................      [ 81%]
tools/docs/tests/test_search_smoke.py ........                           [ 83%]
tools/docs/tests/test_templates.py .....                                 [ 84%]
tools/docs/tests/test_tutorial.py ..................                     [ 88%]
tools/docs/tests/test_urls.py .........................                  [ 93%]
tools/docs/tests/test_weekly_issue.py ......                             [ 95%]
tools/docs/tests/test_weekly_workflow.py ....................            [ 99%]
tools/docs/tests/test_yaml_tools.py ..                                   [100%]

=========================== short test summary info ============================
SKIPPED [1] tools/docs/tests/test_assets.py:75: generation dependencies are absent (run with --group fonts)
================== 447 passed, 1 skipped in 63.78s (0:01:03) ===================
running: uv run --project tools/docs --group material pytest tools/docs/tests
docs-check: passed (documentation unit tests)

docs-check: follow-on gates
skipped: CLI reference golden is a cargo test, not a docs-check gate

docs-check: all implemented gates passed

✅  CHECK
────────────────────────────────────────────────
cargo fmt --all -- --check
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking typenum v1.20.1
    Checking cfg-if v1.0.4
    Checking stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
    Checking equivalent v1.0.2
    Checking allocator-api2 v0.2.21
    Checking memchr v2.8.1
    Checking foldhash v0.2.0
    Checking litemap v0.8.3
    Checking writeable v0.6.4
    Checking utf8_iter v1.0.4
    Checking simd-adler32 v0.3.9
    Checking bitflags v2.12.1
    Checking zerofrom v0.1.8
    Checking libc v0.2.186
    Checking smallvec v1.15.2
    Checking rand_core v0.10.1
    Checking utf8parse v0.2.2
    Checking adler2 v2.0.1
    Checking anstyle-parse v1.0.0
    Checking crc32fast v1.5.0
    Checking num-traits v0.2.19
   Compiling cc v1.2.63
    Checking miniz_oxide v0.8.9
    Checking yoke v0.8.3
    Checking serde_core v1.0.228
    Checking icu_properties_data v2.3.0
    Checking icu_normalizer_data v2.3.0
    Checking cpufeatures v0.3.0
    Checking is_terminal_polyfill v1.70.2
    Checking colorchoice v1.0.5
    Checking anstyle v1.0.14
    Checking tinyvec_macros v0.1.1
    Checking anstyle-query v1.1.5
    Checking clap_lex v1.1.0
    Checking hashbrown v0.17.1
    Checking strsim v0.11.1
    Checking tinyvec v1.11.0
    Checking weezl v0.1.12
    Checking zerovec v0.11.8
    Checking zerotrie v0.2.5
    Checking siphasher v1.0.4
    Checking itoa v1.0.18
    Checking anstream v1.0.0
    Checking cpufeatures v0.2.17
    Checking phf_shared v0.12.1
    Checking chacha20 v0.10.2
    Checking nom v8.0.0
    Checking aho-corasick v1.1.4
    Checking fdeflate v0.3.7
    Checking clap_builder v4.6.7
    Checking const-oid v0.10.2
    Checking flate2 v1.1.9
    Checking regex-syntax v0.8.10
    Checking zune-core v0.5.3
    Checking unicode-normalization v0.1.25
    Checking tinystr v0.8.4
    Checking potential_utf v0.1.6
    Checking indexmap v2.14.0
    Checking unicode-bidi v0.3.18
    Checking percent-encoding v2.3.2
    Checking icu_locale_core v2.3.0
    Checking icu_collections v2.3.0
    Checking unicode-properties v0.1.4
    Checking color_quant v1.1.0
    Checking quick-error v2.0.1
    Checking iana-time-zone v0.1.65
    Checking pxfm v0.1.30
    Checking getrandom v0.4.2
    Checking bytecount v0.6.9
    Checking byteorder-lite v0.1.0
    Checking chrono v0.4.44
    Checking gif v0.14.2
    Checking form_urlencoded v1.2.2
    Checking generic-array v0.14.7
    Checking hybrid-array v0.4.12
    Checking rand v0.10.1
    Checking stringprep v0.1.5
    Checking png v0.18.1
    Checking zune-jpeg v0.5.15
    Checking phf v0.12.1
    Checking icu_provider v2.3.1
    Checking thiserror v2.0.18
    Checking image-webp v0.2.4
    Checking zmij v1.0.21
    Checking crypto-common v0.1.7
    Checking block-padding v0.3.3
    Checking block-buffer v0.10.4
    Checking block-buffer v0.12.0
    Checking crypto-common v0.2.2
   Compiling rquickjs-sys v0.12.1
    Checking icu_normalizer v2.3.0
    Checking inout v0.1.4
    Checking digest v0.10.7
    Checking cipher v0.4.4
    Checking icu_properties v2.3.0
    Checking encoding_rs v0.8.35
    Checking ttf-parser v0.25.1
    Checking sha2 v0.10.9
    Checking md-5 v0.10.6
    Checking clap v4.6.7
    Checking aes v0.8.4
    Checking ecb v0.1.2
    Checking cbc v0.1.2
    Checking rangemap v1.7.1
    Checking ryu v1.0.23
    Checking log v0.4.30
    Checking serde v1.0.228
    Checking bytemuck v1.25.2
    Checking unsafe-libyaml v0.2.11
    Checking regex-automata v0.4.14
    Checking is_executable v1.0.6
    Checking serde_json v1.0.150
    Checking chrono-tz v0.10.4
    Checking fs2 v0.4.3
    Checking clap_complete v4.6.11
    Checking similar v2.7.0
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/crates/bob-obsidian-assets)
    Checking hex v0.4.3
   Compiling libsqlite3-sys v0.38.1
    Checking digest v0.11.3
    Checking sha2 v0.11.0
    Checking linux-raw-sys v0.12.1
    Checking deranged v0.5.8
    Checking num-conv v0.2.2
    Checking idna_adapter v1.2.2
    Checking serde_yaml v0.9.34+deprecated
    Checking powerfmt v0.2.0
    Checking idna v1.1.0
    Checking time-core v0.1.9
    Checking hashlink v0.12.1
    Checking quick-xml v0.41.0
    Checking fallible-streaming-iterator v0.1.9
    Checking moxcms v0.8.1
    Checking rustix v1.1.5
    Checking fallible-iterator v0.3.0
    Checking url v2.5.8
    Checking base64 v0.22.1
    Checking once_cell v1.21.4
    Checking fastrand v2.5.0
    Checking nom_locate v5.0.0
    Checking lopdf v0.40.0
    Checking time v0.3.53
    Checking tempfile v3.27.0
    Checking regex v1.12.3
    Checking image v0.25.10
    Checking plist v1.10.0
    Checking rusqlite v0.40.1
    Checking rquickjs-core v0.12.1
    Checking rquickjs v0.12.1
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:566:12
    |
566 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:434:20
    |
434 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

warning: the type of the `self` parameter does not need to be arbitrary
  --> src/native/event_task.rs:79:28
   |
79 |     pub(crate) fn classify(self: &Self, span: EventSpan) -> ClockClass {
   |                            ^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_arbitrary_self_type
   = note: `#[warn(clippy::needless_arbitrary_self_type)]` on by default
help: remove the type
   |
79 -     pub(crate) fn classify(self: &Self, span: EventSpan) -> ClockClass {
79 +     pub(crate) fn classify(&self, span: EventSpan) -> ClockClass {
   |

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
    --> src/native/capture/dependencies.rs:1100:1
     |
1100 | / fn resolve_prerequisites(
1101 | |     ctx: &DependencyContext,
1102 | |     planner: &mut CaptureBatchPlanner,
1103 | |     bob_dir: &Path,
...    |
1108 | |     dependent_desc: &str,
1109 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
     = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1442:24
     |
1442 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
     = note: `#[warn(clippy::type_complexity)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2001:6
     |
2001 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
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
   --> src/native/capture/output.rs:395:5
    |
395 | /     pub(super) fn from_items(
396 | |         items: Vec<CaptureItemResult>,
397 | |         global_destination: Option<GlobalDestinationSummary>,
398 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
406 | |         inbox_route: InboxRouteReport,
407 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
   --> src/native/capture/plan.rs:641:1
    |
641 | / pub(super) fn plan_capture_item(
642 | |     request: &CaptureRequest,
643 | |     parsed_item: ParsedCaptureItem,
644 | |     now: chrono::NaiveDateTime,
...   |
652 | |     task_theme_context: &mut CaptureTaskThemeContext,
653 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/capture/pomodoro_insert.rs:376:1
    |
376 | / pub(super) fn insert_named_pomodoro_child_block(
377 | |     contents: &str,
378 | |     block: &str,
379 | |     selector: &str,
...   |
385 | |     open: &[(usize, &str)],
386 | | ) -> Result<(String, Placement, usize, String), CaptureError> {
    | |_____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:914:1
    |
914 | / fn relation_update_json(
915 | |     direction: RelationDirection,
916 | |     source_relative: &Path,
917 | |     source_line: usize,
...   |
922 | |     previous_label: Option<String>,
923 | | ) -> RelationUpdateJson {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

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

warning: this function has too many arguments (8/7)
   --> src/native/capture/task_theme.rs:115:5
    |
115 | /     pub(super) fn apply_new_task(
116 | |         &mut self,
117 | |         planner: &mut CaptureBatchPlanner,
118 | |         target: &Path,
...   |
123 | |         warnings: &mut Vec<CaptureWarning>,
124 | |     ) -> Result<Option<AppliedTaskTheme>, CaptureError> {
    | |_______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/capture/task_theme.rs:317:5
    |
317 | /     pub(super) fn apply_existing_task(
318 | |         &mut self,
319 | |         planner: &mut CaptureBatchPlanner,
320 | |         target: &Path,
...   |
326 | |         warnings: &mut Vec<CaptureWarning>,
327 | |     ) -> Result<Option<AppliedTaskTheme>, CaptureError> {
    | |_______________________________________________________^
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
   --> src/native/capture_complete/candidates.rs:775:1
    |
775 | / fn relationship_disabled_reason(
776 | |     bob_dir: &Path,
777 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
778 | |     graph: &HashMap<
...   |
787 | |     blocked_tasks: &[ResolvedRelationshipEntry],
788 | | ) -> Option<String> {
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1407:6
     |
1407 |   ) -> (
     |  ______^
1408 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1409 | |     Vec<String>,
1410 | |     Vec<(String, usize)>,
1411 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
   --> src/native/capture_complete/theme_menu.rs:186:1
    |
186 | / pub(super) fn compose_task_aware(
187 | |     scan: &PomodoroScan,
188 | |     query: &str,
189 | |     hint: Option<&PlanCreationHint>,
...   |
194 | |     choice: MenuChoice,
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
    = note: `#[warn(clippy::nonminimal_bool)]` on by default
help: try
    |
261 ~             || row
262 +                 .name
263 +                 .as_deref().is_none_or(|name| normalize_component(name) != key)
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

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:554:1
    |
554 | / pub(super) enum TokenParse {
555 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
556 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
557 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
555 -     Marker(MarkerParse),
555 +     Marker(Box<MarkerParse>),
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
    --> src/native/capture_language/item.rs:1615:31
     |
1615 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
1616 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1617 | |                 (false, '~', Some(b'@')) => true,
1618 | |                 _ => false,
1619 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
1615 -             let want_second = match (name.is_some(), first_sigil, second) {
1616 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
1617 -                 (false, '~', Some(b'@')) => true,
1618 -                 _ => false,
1619 -             };
1615 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:1934:1
     |
1934 | / pub(super) fn named_shape_error_with_drop(
1935 | |     token: &str,
1936 | |     suffix: &str,
1937 | |     name: &str,
...    |
1942 | |     is_literal: bool,
1943 | | ) -> String {
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

warning: this boolean expression can be simplified
   --> src/native/capture_language/rewrite.rs:388:8
    |
388 |       if !raw_text[..run_start]
    |  ________^
389 | |         .chars()
390 | |         .next_back()
391 | |         .is_some_and(|before| !before.is_whitespace())
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
388 ~     if raw_text[..run_start]
389 +         .chars()
390 +         .next_back().is_none_or(|before| before.is_whitespace())
    |

warning: redundant guard
   --> src/native/capture_language/tokens.rs:932:43
    |
932 |                 Some((after_x, x_len)) if after_x.is_empty() => {
    |                                           ^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
    |
932 -                 Some((after_x, x_len)) if after_x.is_empty() => {
932 +                 Some(("", x_len)) => {
    |

warning: this `if` has identical blocks
   --> src/native/capture_language/type_marker.rs:590:45
    |
590 |           } else if lex.decoded.contains('+') {
    |  _____________________________________________^
591 | |             (
592 | |                 TypeMarkerOccurrence::Invalid {
593 | |                     span: start..raw_end,
...   |
598 | |         } else if marker_end != raw_end {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/type_marker.rs:598:41
    |
598 |           } else if marker_end != raw_end {
    |  _________________________________________^
599 | |             (
600 | |                 TypeMarkerOccurrence::Invalid {
601 | |                     span: start..raw_end,
...   |
606 | |         } else {
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else
    = note: `#[warn(clippy::if_same_then_else)]` on by default

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:136:1
    |
136 | / pub(crate) enum PomodoroCloseOutcome {
137 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 536 bytes
138 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
139 | | }
    | |_^ the entire enum is at least 536 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
137 -     Close(PomodoroClosePlan),
137 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:243:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
243 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
    = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:290:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
290 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:478:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
478 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:495:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
495 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:515:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
515 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:538:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
538 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:601:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
601 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:674:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
674 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:828:10
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
828 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:905:6
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
905 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:929:6
    |
131 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
929 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1266:6
     |
 131 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1266 | ) -> Result<(), PomodoroClosePlanError> {
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
   --> src/native/capture_related/draft.rs:413:1
    |
413 | / fn draft_match(
414 | |     ranked: bands::RankedMatch<'_>,
415 | |     item: &EditorItemParse,
416 | |     draft: &str,
...   |
421 | |     index: &NoteIndex,
422 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:544:1
    |
544 | / fn verify_link_action(
545 | |     action: &str,
546 | |     item: &EditorItemParse,
547 | |     draft: &str,
...   |
552 | |     options: &EditorParseOptions<'_>,
553 | | ) -> bool {
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
   --> src/native/capture_task_toggle/ledger.rs:325:49
    |
325 | pub(crate) fn default_pomodoro_link_destination<'a>(
    |                                                 ^^
326 |     scan: &'a capture_pomodoros::PomodoroScan,
    |            ^^
327 |     queue_owner_line: Option<usize>,
328 | ) -> Option<&'a capture_pomodoros::PomodoroEntry> {
    |              ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
325 ~ pub(crate) fn default_pomodoro_link_destination(
326 ~     scan: &capture_pomodoros::PomodoroScan,
327 |     queue_owner_line: Option<usize>,
328 ~ ) -> Option<&capture_pomodoros::PomodoroEntry> {
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_task_toggle/relocation.rs:536:18
    |
536 |       let anchor = scan
    |  __________________^
537 | |         .entries
538 | |         .iter()
539 | |         .filter(|entry| entry.state == PomodoroState::Open)
540 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
540 -         .last()
540 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
  --> src/native/capture_task_wikilinks.rs:79:5
   |
79 | /     wikilink_task_tokens(raw)
80 | |         .into_iter()
81 | |         .filter_map(|token| field_at_token(raw, token, cursor))
82 | |         .last()
   | |_______________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
   |
82 -         .last()
82 +         .next_back()
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

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/gcal/journal.rs:114:6
    |
114 |   ) -> std::io::Result<(
    |  ______^
115 | |     BTreeMap<(String, String), OccurrenceState>,
116 | |     Vec<String>,
117 | |     Option<(DateTime<FixedOffset>, String)>,
118 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: large size difference between variants
   --> src/native/gcal/journal.rs:162:1
    |
162 | / enum Update {
163 | |     Row(RowRecord),
    | |     -------------- the largest variant contains at least 232 bytes
164 | |     Link,
165 | |     Gone,
166 | |     Flag(String),
    | |     ------------ the second-largest variant contains at least 24 bytes
167 | | }
    | |_^ the entire enum is at least 232 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
163 -     Row(RowRecord),
163 +     Row(Box<RowRecord>),
    |

warning: consider using `sort_by_key`
   --> src/native/gcal/login.rs:638:5
    |
638 |     paths.sort_by(|a, b| b.0.cmp(&a.0));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
    = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
    |
638 -     paths.sort_by(|a, b| b.0.cmp(&a.0));
638 +     paths.sort_by_key(|b| std::cmp::Reverse(b.0));
    |

warning: this boolean expression can be simplified
   --> src/native/gcal/render.rs:111:5
    |
111 | /     !result
112 | |         .suggestion
113 | |         .is_some_and(|suggestion| suggestion.theme.name == "MEET")
    | |__________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
111 ~     result
112 +         .suggestion.is_none_or(|suggestion| suggestion.theme.name != "MEET")
    |

warning: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
    --> src/native/gcal/sync.rs:1071:47
     |
1071 | fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
     |                                               ^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
1071 - fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
1071 + fn display_rel(vault: &std::path::Path, path: &Path) -> String {
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
help: try
     |
1952 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1952 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.start));
     |

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1979:1
     |
1979 | / pub(super) fn stamp_overwrite_source(
1980 | |     config: &Config,
1981 | |     plan: &OverwritePreflight,
1982 | |     options: &CreateOptions,
...    |
1987 | |     info: &PdfInfo,
1988 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2021:1
     |
2021 | / pub(super) fn stage_overwrite_audio(
2022 | |     options: &CreateOptions,
2023 | |     plan: &OverwritePreflight,
2024 | |     request: &OverwriteRequest,
...    |
2029 | |     title: &str,
2030 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2703:1
     |
2703 | / fn plan_target_for(
2704 | |     config: &Config,
2705 | |     stem: &str,
2706 | |     ref_type: &str,
...    |
2711 | |     source_display: &str,
2712 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3711:1
     |
3711 | / fn stage_overwrite_source_store(
3712 | |     _config: &Config,
3713 | |     plan: &OverwritePreflight,
3714 | |     scratch: &Path,
...    |
3721 | |     catalog: &super::code_catalog::CatalogOutcome,
3722 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4392:1
     |
4392 | / fn overwrite_pdf_url(
4393 | |     config: &Config,
4394 | |     url: super::clip_url::WebUrl,
4395 | |     downloaded: PathBuf,
...    |
4400 | |     selection: &OverwriteSelection,
4401 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4473:1
     |
4473 | / fn create_pdf_url_route(
4474 | |     config: &Config,
4475 | |     url: super::clip_url::WebUrl,
4476 | |     downloaded: PathBuf,
...    |
4481 | |     listen: Option<&super::listen::ListenCommand>,
4482 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5207:1
     |
5207 | / fn print_pdf_dry_run(
5208 | |     config: &Config,
5209 | |     styler: &Styler,
5210 | |     source_display: &str,
...    |
5218 | |     legacy: &[sources_mod::RecordedSource],
5219 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:5443:1
     |
5443 | / fn compose_markdown_marker(
5444 | |     status: &str,
5445 | |     parent: &str,
5446 | |     title: &str,
...    |
5451 | |     return_links: bool,
5452 | | ) -> Result<String> {
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
   --> src/native/highlights_ref/clip_adapter.rs:763:5
    |
763 | /     DIAGRAM_TIMEOUT_BASE_SECS
764 | |         .saturating_add(
765 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
768 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
763 ~     DIAGRAM_TIMEOUT_BASE_SECS
764 +         .saturating_add(
765 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
766 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:736:1
    |
736 | / pub(super) enum PdfSyncOutcome {
737 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
738 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
739 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
737 -     Written(SyncWriteReport),
737 +     Written(Box<SyncWriteReport>),
    |

warning: large size difference between variants
   --> src/native/highlights_ref/model.rs:808:1
    |
808 | / pub(super) enum ScanWriteOutcome {
809 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
810 | |     Held(ScanHold),
811 | |     Failed(ScanFailure),
    | |     ------------------- the second-largest variant contains at least 144 bytes
812 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
809 -     Written(SyncWriteReport),
809 +     Written(Box<SyncWriteReport>),
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
   --> src/native/pomodoro_homes/resolve.rs:414:25
    |
414 | /                         chain[nearest_home..end]
415 | |                             .iter()
416 | |                             .filter(|(_, facts)| {
417 | |                                 facts.kind == NoteKind::Project
418 | |                             })
419 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
419 -                             .last()
419 +                             .next_back()
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

warning: this function has too many arguments (9/7)
  --> src/native/pomodoro_themes/preselect.rs:67:1
   |
67 | / pub(crate) fn choose(
68 | |     suggestion: &ThemeRef,
69 | |     entries: &[MenuEntry<'_>],
70 | |     exempt: &[String],
...  |
76 | |     already_queued: bool,
77 | | ) -> MenuChoice {
   | |_______________^
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
   --> src/native/ref_library/today.rs:351:6
    |
351 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/ref_library/today.rs:846:1
    |
846 | / fn fail(
847 | |     format: Format,
848 | |     dry_run: bool,
849 | |     code: &str,
...   |
854 | |     listing: &TodayListing,
855 | | ) -> i32 {
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
   --> src/native/ref_library/mod.rs:919:5
    |
919 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
919 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
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
   --> src/native/relation_labels/cli.rs:485:22
    |
485 |       let mut counts = format!(
    |  ______________________^
486 | |         "{} {} {} {} {} {}",
487 | |         report.counts.labels,
488 | |         label_word(report.counts.labels),
...   |
492 | |         format!("{} hidden", report.counts.hidden,),
493 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: consider using `sort_by_key`
   --> src/native/relation_labels/rename.rs:817:5
    |
817 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
817 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
817 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
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
    --> src/native/task_complete/successors.rs:1439:1
     |
1439 | / fn attach_offer(
1440 | |     verdict: &mut DependentVerdict,
1441 | |     files: &[FileScan],
1442 | |     day: &DayView,
...    |
1447 | |     project: Option<PathBuf>,
1448 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:1540:1
     |
1540 | / fn apply_project_member_classes(
1541 | |     verdicts: &mut Vec<DependentVerdict>,
1542 | |     folds: &mut Vec<ProjectFold>,
1543 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
1552 | |     _note_settings: &NoteTaskSettings,
1553 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2111:1
     |
2111 | / fn apply_verdicts(
2112 | |     input: SuccessorInput,
2113 | |     files: Vec<FileScan>,
2114 | |     verdicts: Vec<DependentVerdict>,
...    |
2119 | |     project_folds: Vec<ProjectFold>,
2120 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_move/command.rs:644:6
    |
644 | ) -> Result<(Option<(PathBuf, String)>, Vec<RelocatedInfo>), String> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

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
   --> src/native/task_status_hooks/sync.rs:494:5
    |
494 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:361:9
    |
361 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1282:1
     |
1282 | / fn consume_blocked_links_after_compose(
1283 | |     compose: &mut ComposeResult,
1284 | |     files: &[FileScan],
1285 | |     daily_path: &Path,
...    |
1296 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1297 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: `bob-obsidian` (lib) generated 141 warnings (run `cargo clippy --fix --lib -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 15 suggestions)
warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
  --> tests/gcal_lifecycle.rs:62:5
   |
62 | /     journal
63 | |         .iter()
64 | |         .filter(|line| {
65 | |             line["kind"] == "gcal.row" && line["key"]["event_id"] == event_id
66 | |         })
67 | |         .last()
   | |_______________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
   = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
   |
67 -         .last()
67 +         .next_back()
   |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> tests/gcal_lifecycle.rs:628:19
    |
628 |       let learned = journal
    |  ___________________^
629 | |         .iter()
630 | |         .filter(|line| line["kind"] == "gcal.series_root")
631 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
631 -         .last()
631 +         .next_back()
    |

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> tests/gcal_lifecycle.rs:664:21
    |
664 |       let relearned = journal
    |  _____________________^
665 | |         .iter()
666 | |         .filter(|line| line["kind"] == "gcal.series_root")
667 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
667 -         .last()
667 +         .next_back()
    |

warning: `bob-obsidian` (test "gcal_lifecycle") generated 3 warnings (run `cargo clippy --fix --test "gcal_lifecycle" -p bob-obsidian -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 3 suggestions)
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
    --> src/native/capture_language/tests/grammar.rs:2161:35
     |
2161 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2198:48
     |
2198 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2207:22
     |
2207 |         execute(raw).expect(&format!("{raw} executes as prose"));
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

error: for loop over a single element
   --> tests/cli/capture/capture_type_marker.rs:695:5
    |
695 | /     for args in ["-r sase --task parent A child #fix"] {
696 | |         let (_, error) = if args.starts_with("-r ") {
697 | |             capture_error_json(
698 | |                 &vault,
...   |
706 | |         assert_eq!(error["code"], "type_marker_not_applicable", "{error}");
707 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_element_loop
    = note: requested on the command line with `-D clippy::single-element-loop`
help: try
    |
695 ~     {
696 +         let args = "-r sase --task parent A child #fix";
697 +         let (_, error) = if args.starts_with("-r ") {
698 +             capture_error_json(
699 +                 &vault,
700 +                 &day_file,
701 +                 &config,
702 +                 &["-r", "sase", "--task", "parent", "A child #fix"],
703 +             )
704 +         } else {
705 +             capture_error_json(&vault, &day_file, &config, &[args])
706 +         };
707 +         assert_eq!(error["code"], "type_marker_not_applicable", "{error}");
708 +     }
    |

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

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/pomodoro.rs:874:51
    |
874 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
    |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

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

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: `bob-obsidian` (test "cli") generated 4 warnings
error: could not compile `bob-obsidian` (test "cli") due to 1 previous error; 4 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:494:5
    |
494 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:361:9
    |
361 |     let mut files = Vec::with_capacity(markdown_files.len());
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

warning: `bob-obsidian` (lib test) generated 165 warnings (140 duplicates) (run `cargo clippy --fix --lib -p bob-obsidian --tests -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator` to apply 7 suggestions)
error: Recipe `check` failed on line 79 with exit code 101
failed  exit=101  duration=421970ms

