# Chat History - ace-run (bob-cli-pl.4.1.3--mon-4)

- **TIMESTAMP:** 2026-11-24 14:01:12 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-pl.4.1.3--mon-4

## Prompt

sase monitor start --command 'bash -c \'set +e\nnpm run test:perf\nperf_rc=$?\necho "test:perf exit=$perf_rc"\nnpm run docs:check\ndocs_rc=$?\necho "docs:check exit=$docs_rc"\nnpm run validate\nvalidate_rc=$?\necho "validate exit=$validate_rc"\nif [ "$perf_rc" -ne 0 ] || [ "$docs_rc" -ne 0 ] || [ "$validate_rc" -ne 0 ]; then exit 1; fi\'' --reason 'Run the requested bob-plugins phase verification gates'

## Response

sase tool run d2759c2c432908ad17be821f6a1bf3f9

> bob-plugins@0.1.0 test:perf
> node --test --test-concurrency=1 scripts/test-block-id-prompt-task-wikilink-index-performance.cjs scripts/test-block-id-prompt-task-links-api-performance.cjs scripts/test-copy-chips-live-preview-performance.cjs scripts/test-navigation-copy-card-task-scope-performance.cjs scripts/test-navigation-prose-field-performance.cjs scripts/test-navigation-dependencies-stage-performance.cjs

✔ api.taskLinks session open (snapshot plus first rank) takes at most 50 ms (500.772563ms)
ℹ session open: 39.58 ms
✔ api.taskLinks keystroke-to-rows p95 takes at most 12 ms over 5,000 tasks (787.175328ms)
ℹ keystroke p95: 9.79 ms
✔ api.taskLinks performs no vault reads while filtering (679.167972ms)
✔ api.taskLinks typed keystrokes p95 takes at most 12 ms over 5,000 tasks (3171.358401ms)
ℹ typed keystroke p95: 11.00 ms
✔ cold build of 6,500 notes / 5,000 tasks fits 1.5 s in chunks of at most 16 ms (607.786184ms)
✔ warm snapshot plus order takes at most 50 ms (303.666508ms)
✔ one keystroke rank of 5,000 rows takes at most 12 ms (321.711362ms)
✔ no vault reads happen while filtering (225.290738ms)
✔ cold build growth stays near-linear over a 6x step (253.868017ms)
✔ 2,000-line daily note with 200 chips fits the 35 ms CPU budget (25.623392ms)
✔ narrow viewport visits only visible syntax ranges (4.158773ms)
✔ clipboard writes stay out of the perf path (1.641211ms)
✔ 2,000-line mixed note paints both kinds inside the 35 ms CPU budget (90.819136ms)
✔ mixed discovery stays inside the viewport and re-resolves only on a new catalog (234.337117ms)
✔ 2,000-line task, scope, and chip resolution fit the 50 ms CPU budget (246.657912ms)
✔ stage opening builds 200/400/1000-task notes without cubic growth (61.400864ms)
✔ stage snapshots match standalone parsing across grammar vectors (9.04321ms)
✔ stage Warm-empty cache is ready without a vault fallback (0.925501ms)
✔ stage opening renders cross-note results with zero writes and cap (53.87108ms)
✔ stage CURRENT covers same-note, cross-note, blocked, and counted parents (2.386173ms)
✔ stage collections reuse one snapshot per parent (0.619323ms)
✔ stage cold refresh yields, preserves state, and performs no search reads (120.951171ms)
✔ stage cold refresh abandons after dismissal or replacement (56.041519ms)
✔ stage 400-task opening finishes in a child process before the parent timeout (269.197383ms)
✔ 10k-note keystroke-to-rows p95 is ≤ 8 ms CPU (646.00784ms)
✔ 10k-note first link-index build is ≤ 40 ms CPU (501.63516ms)
ℹ tests 26
ℹ suites 0
ℹ pass 26
ℹ fail 0
ℹ cancelled 0
ℹ skipped 0
ℹ todo 0
ℹ duration_ms 10574.39635
test:perf exit=0

> bob-plugins@0.1.0 docs:check
> bash scripts/docs-check.sh

From https://github.com/bobs-org/bob-cli
 + dbf405e3...3deee354 master     -> origin/master  (forced update)
HEAD is now at 3deee354 fix(props): satisfy settings contract lint gates
docs-check: using bob-cli /home/bryan/.cache/bob-plugins-docs/bob-cli with BOB_DOCS_BOB_PLUGINS_DIR=/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins

✅  DOCS CHECK
────────────────────────────────────────────────
uv run --project tools/docs bob-docs check
docs-check: assemble and validate source context

docs-check: lint
warning: docs/develop/plugins/plugin-apis.md:1: budget: over budget at 9073 words (cap 8000 for develop/)
bob-docs lint: 1 warning(s)
docs-check: passed (lint)

docs-check: generated drift
Plugin documentation inventory is up to date.
generated contract content is up to date
docs-check: passed (generated drift)

docs-check: strict Zensical build
Build started
No issues found
Build finished in 30.76s
running: zensical build --strict --config-file /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/mkdocs.yml
built site: /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site
docs-check: passed (strict Zensical build)

docs-check: published URLs
wrote /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/urls.txt (251 published pages)
urls: OK (251 pages, 949 mentions checked, 64 curated links)
docs-check: passed (published URLs)

docs-check: offline lychee with fragments
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/capture-agenda.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/capture-agenda.png'
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/capture-agenda-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/task-completion.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/task-completion.png'
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/task-completion-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/task-completion-dark.png'
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/refs-browse.png#only-light due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/refs-browse.png'
  [WARN] Skipping fragment check for file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/refs-browse-dark.png#only-dark due to the following error: Cannot read input content from file '/home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/reference/mac-capture/images/refs-browse-dark.png'
🔍 76137 Total (in 4s 285ms) 🔗 4301 Unique ✅ 74801 OK 🚫 0 Errors 👻 1336 Excluded

running: /home/bryan/.cache/bob-docs/bin/lychee --offline --no-progress --include-fragments --exclude-path (^|/)index[.]md$ --index-files index.html --root-dir /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site --remap https://bobs-org.github.io/ file:///home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/ /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site
links: OK (offline lychee with fragment checking)
docs-check: passed (offline lychee with fragments)

docs-check: edit links point at real sources
edit-links: OK (243 edit link(s) point at real source files)
docs-check: passed (edit links point at real sources)

docs-check: search smoke
search smoke: OK (133 cases; index /home/bryan/.cache/bob-plugins-docs/bob-cli/target/docs/site/search.json)
docs-check: passed (search smoke)

docs-check: executable first-day tutorial
   Compiling proc-macro2 v1.0.106
   Compiling quote v1.0.45
   Compiling unicode-ident v1.0.24
   Compiling cfg-if v1.0.4
   Compiling siphasher v1.0.4
   Compiling typenum v1.20.1
   Compiling stable_deref_trait v1.2.1
   Compiling version_check v0.9.5
   Compiling libc v0.2.186
   Compiling fastrand v2.5.0
   Compiling smallvec v1.15.2
   Compiling memchr v2.8.1
   Compiling bitflags v2.12.1
   Compiling parking_lot_core v0.9.12
   Compiling autocfg v1.5.1
   Compiling shlex v2.0.1
   Compiling writeable v0.6.4
   Compiling new_debug_unreachable v1.0.6
   Compiling scopeguard v1.2.0
   Compiling serde_core v1.0.228
   Compiling phf_shared v0.14.0
   Compiling litemap v0.8.3
   Compiling lock_api v0.4.14
   Compiling precomputed-hash v0.1.1
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling icu_properties_data v2.3.0
   Compiling itoa v1.0.18
   Compiling icu_normalizer_data v2.3.0
   Compiling utf8_iter v1.0.4
   Compiling generic-array v0.14.7
   Compiling find-msvc-tools v0.1.9
   Compiling crc32fast v1.5.0
   Compiling phf_generator v0.14.0
   Compiling simd-adler32 v0.3.9
   Compiling foldhash v0.2.0
   Compiling cc v1.2.63
   Compiling adler2 v2.0.1
   Compiling serde v1.0.228
   Compiling rand_core v0.10.1
   Compiling num-traits v0.2.19
   Compiling phf_codegen v0.14.0
   Compiling log v0.4.30
   Compiling utf8parse v0.2.2
   Compiling hashbrown v0.17.1
   Compiling getrandom v0.4.2
   Compiling miniz_oxide v0.8.9
   Compiling anstyle-parse v1.0.0
   Compiling anstyle-query v1.1.5
   Compiling anstyle v1.0.14
   Compiling tinyvec_macros v0.1.1
   Compiling cpufeatures v0.3.0
   Compiling is_terminal_polyfill v1.70.2
   Compiling colorchoice v1.0.5
   Compiling dtoa v1.0.11
   Compiling tinyvec v1.11.0
   Compiling tendril v0.5.1
   Compiling zmij v1.0.21
   Compiling anstream v1.0.0
   Compiling weezl v0.1.12
   Compiling dtoa-short v0.3.5
   Compiling rustix v1.1.5
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling string_cache_codegen v0.11.2
   Compiling hybrid-array v0.4.12
   Compiling flate2 v1.1.9
   Compiling unicode-width v0.2.3
   Compiling cpufeatures v0.2.17
   Compiling thiserror v2.0.18
   Compiling strsim v0.11.1
   Compiling clap_lex v1.1.0
   Compiling getopts v0.2.24
   Compiling unicode-normalization v0.1.25
   Compiling indexmap v2.14.0
   Compiling clap_builder v4.6.7
   Compiling web_atoms v0.3.0
   Compiling crypto-common v0.2.2
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling parking_lot v0.12.5
   Compiling block-buffer v0.10.4
   Compiling inout v0.1.4
   Compiling block-buffer v0.12.0
   Compiling chacha20 v0.10.2
   Compiling aho-corasick v1.1.4
   Compiling digest v0.10.7
   Compiling nom v8.0.0
   Compiling cipher v0.4.4
   Compiling fdeflate v0.3.7
   Compiling string_cache v0.11.0
   Compiling phf_shared v0.12.1
   Compiling servo_arc v0.5.0
   Compiling byteorder-lite v0.1.0
   Compiling pulldown-cmark v0.13.6
   Compiling rquickjs-sys v0.12.1
   Compiling unicode-properties v0.1.4
   Compiling linux-raw-sys v0.12.1
   Compiling pxfm v0.1.30
   Compiling quick-error v2.0.1
   Compiling const-oid v0.10.2
   Compiling percent-encoding v2.3.2
   Compiling unicode-bidi v0.3.18
   Compiling rustc-hash v2.1.3
   Compiling chrono-tz v0.10.4
   Compiling color_quant v1.1.0
   Compiling zune-core v0.5.3
   Compiling iana-time-zone v0.1.65
   Compiling bytecount v0.6.9
   Compiling regex-syntax v0.8.10
   Compiling serde_json v1.0.150
   Compiling stringprep v0.1.5
   Compiling zune-jpeg v0.5.15
   Compiling gif v0.14.2
   Compiling digest v0.11.3
   Compiling form_urlencoded v1.2.2
   Compiling image-webp v0.2.4
   Compiling png v0.18.1
   Compiling phf v0.12.1
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling cbc v0.1.2
   Compiling ecb v0.1.2
   Compiling aes v0.8.4
   Compiling rand v0.10.1
   Compiling clap v4.6.7
   Compiling encoding_rs v0.8.35
   Compiling ryu v1.0.23
   Compiling ttf-parser v0.25.1
   Compiling rangemap v1.7.1
   Compiling is_executable v1.0.6
   Compiling bytemuck v1.25.2
   Compiling unicase v2.10.0
   Compiling once_cell v1.21.4
   Compiling pulldown-cmark-escape v0.11.0
   Compiling ego-tree v0.11.1
   Compiling unsafe-libyaml v0.2.11
   Compiling moxcms v0.8.1
   Compiling clap_complete v4.6.11
   Compiling tempfile v3.27.0
   Compiling nom_locate v5.0.0
   Compiling synstructure v0.14.0
   Compiling regex-automata v0.4.14
   Compiling sha2 v0.11.0
   Compiling fs2 v0.4.3
   Compiling roxmltree v0.21.2
   Compiling hex v0.4.3
   Compiling base64 v0.22.1
   Compiling glob v0.3.4
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.cache/bob-plugins-docs/bob-cli/crates/bob-obsidian-assets)
   Compiling similar v2.7.0
   Compiling phf_macros v0.14.0
   Compiling serde_derive v1.0.228
   Compiling derive_more-impl v2.1.1
   Compiling thiserror-impl v2.0.18
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling cssparser-macros v0.7.1
   Compiling phf v0.14.0
   Compiling cssparser v0.38.0
   Compiling derive_more v2.1.1
   Compiling regex v1.12.3
   Compiling lopdf v0.40.0
   Compiling zerofrom v0.1.8
   Compiling yoke v0.8.3
   Compiling markup5ever v0.40.0
   Compiling selectors v0.41.0
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling html5ever v0.40.1
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_collections v2.3.0
   Compiling scraper v0.29.0
   Compiling image v0.25.10
   Compiling icu_locale_core v2.3.0
   Compiling chrono v0.4.44
   Compiling serde_yaml v0.9.34+deprecated
   Compiling icu_provider v2.3.1
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.6.0 (/home/bryan/.cache/bob-plugins-docs/bob-cli)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 3m 47s

TUTORIAL_FENCE 5 docs/start/install.md:72
bob 0.6.0

TUTORIAL_FENCE 7 docs/start/first-bob-day.md:24
Using demo vault: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261124_134647/bob-docs-sandbox-3h3n5umh/tmp/bob-first-day.c9uzJd/vault

TUTORIAL_FENCE 8 docs/start/first-bob-day.md:46
✓ captured  mac_inbox.md
  - [ ] #task Sort the seed packets [created::2026-10-20] ^seed-packet

TUTORIAL_FENCE 9 docs/start/first-bob-day.md:61
✓ captured  garden.md
  - [ ] #task Water the seedlings [created::2026-10-20] ^seedlings

TUTORIAL_FENCE 10 docs/start/first-bob-day.md:76
bob plan - Tue 2026-10-20 - no daily note yet

  PLAN  0/10 links      TODAY 0 - PENDING 0/10 - NEXT 0/15


TUTORIAL_FENCE 11 docs/start/first-bob-day.md:92
Created daily note: /home/bryan/.cache/sase/tmp/agent-tmp/gh_bobs-org__bob-cli-ws15-261124_134647/bob-docs-sandbox-3h3n5umh/tmp/bob-first-day.c9uzJd/vault/2026/20261020.md

TUTORIAL_FENCE 12 docs/start/first-bob-day.md:117
✓ started  2026/20261020.md
  FOCUS 0905-0930 (25m) (created) at line 4
  - [ ] (**0905-0930** [t:: 25m]) — FOCUS
  nothing queued
plan 0/10 links

TUTORIAL_FENCE 13 docs/start/first-bob-day.md:128
✓ link  garden.md
  [ ] → [*]  Water the seedlings  ^seedlings
  Linked under FOCUS
plan 1/10 links
{"caps":{"max_links":10,"max_next":15,"max_pending":10,"max_ready":100},"daily_file":"2026/20261020.md","date":"2026-10-20","entries":[{"components":["FOCUS"],"exempt":false,"highlight":true,"homes":{"chip":"garden","hue":"magenta","kind":"work","label":"garden","parts":[{"area":"garden.md","area_label":"garden","hue":"magenta","key":"garden.md","kind":"area","label":"garden","share":100,"tasks":1}],"state":"forecast"},"line":4,"links":1,"name":"FOCUS","running":true,"themes":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"time_range":"0905-0930"}],"links":{"cap":10,"count":1,"off_clock":0,"over":false},"next":{"cap":15,"count":1,"over":false},"ok":true,"pending":{"cap":10,"count":0,"over":false},"schema_version":3,"status":"ok","theme_names":["FOCUS"],"theme_refs":[{"hue":"yellow","hue_source":"hash","key":"focus","name":"FOCUS"}],"today":{"count":1},"today_roots":[{"hue":"magenta","key":"garden.md","label":"garden","tasks":1}],"today_tasks":[{"block_id":"seedlings","entry_line":4,"entry_name":"FOCUS","ledger_line":5,"line":8,"path":"garden.md","status_name":"Next","status_symbol":"*","text":"Water the seedlings"}],"warnings":[]}

TUTORIAL_FENCE 14 docs/start/first-bob-day.md:141
bob capture: warning: FOCUS has not started: it starts at 0905, so closing now records a zero-length session; capture `x0` to reset it instead
✓ closed FOCUS 0905-0930 → 0905-0905 (0m, −25m) · 2026/20261020.md line 4
  1 [*] → [x] Water the seedlings garden.md ^seedlings
  next: FOCUS (created) at line 6 · carries 0 links
plan 0/10 links

TUTORIAL_FENCE 15 docs/start/first-bob-day.md:154
{"config":{"decay":{"enabled":true,"enter":null,"keeps":3,"limits":{"next":3,"pending":3,"ready":3}},"interval":7,"next_interval":1,"pending_interval":1,"post_stages":[],"pre_stages":[],"project_interval":null,"rotten_daily_budget":null},"counts":{"budget":null,"budget_met":false,"by_tier":{"new":1,"next":0,"pending":0,"post":0,"pre":0,"projects":1,"recurring":0,"rotten":0,"tickler":0},"decide":0,"due":2,"fresh":0,"new":2,"next_due":0,"pending_due":0,"post_due":0,"pre_due":0,"projects_due":1,"recurring_due":0,"refreshed_today":1,"resurfaced":0,"rotten":0,"upkeep_today":1,"walk":2},"date":"2026-10-20","ok":true,"queue":[{"block_id":"seed-packet","bucket":"new","created":"2026-10-20","days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":7,"path":"mac_inbox.md","rank":1,"returned_by":null,"scheduled":null,"stage":null,"stage_rank":null,"stage_total":null,"state":"new","status_symbol":" ","text":"Sort the seed packets ^seed-packet","tier":"new","unblocked_on":null},{"block_id":"prj","bucket":"new","created":null,"days_overdue":null,"decide":false,"due_on":null,"fresh":null,"interval":7,"interval_source":"default","keeps":0,"lane":"ready","line":11,"path":"Projects/seedlings.md","rank":2,"returned_by":null,"scheduled":null,"stage":null,"stage_rank":null,"stage_total":null,"state":"new","status_symbol":" ","text":"#prj Raise healthy seedlings for the garden ^prj","tier":"projects","unblocked_on":null}],"schema_version":16,"warnings":[]}
skipped: docs/start/install.md:16: network clone needs a remote and user credentials
skipped: docs/start/install.md:27: toolchain install changes the host and needs network
skipped: docs/start/install.md:42: install writes outside the tutorial sandbox
skipped: docs/start/install.md:66: PATH export edits the reader shell profile
skipped: docs/start/install.md:92: network install needs a remote and writes outside the sandbox
skipped: docs/start/obsidian.md:18: opening Obsidian needs the desktop app
skipped: docs/start/obsidian.md:28: Tasks install needs the Obsidian app and network
skipped: docs/start/obsidian.md:52: plugin clone needs network and a plugin source checkout
skipped: docs/start/obsidian.md:69: plugin sync needs a plugin source checkout and Obsidian
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
rootdir: /home/bryan/.cache/bob-plugins-docs/bob-cli/tools/docs
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
================== 447 passed, 1 skipped in 81.53s (0:01:21) ===================
running: uv run --project tools/docs --group material pytest tools/docs/tests
docs-check: passed (documentation unit tests)

docs-check: follow-on gates
skipped: CLI reference golden is a cargo test, not a docs-check gate

docs-check: all implemented gates passed
docs:check exit=0

> bob-plugins@0.1.0 validate
> node scripts/build-plugins.mjs --check && npm run docs:inventory:check && node scripts/validate-manifests.mjs

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-chips
  checked   bob-command-mode
  checked   bob-emoji
  checked   bob-ledger-tools
  checked   bob-mail
  checked   bob-navigation-hotkeys
  checked   task-status-cycler

> bob-plugins@0.1.0 docs:inventory:check
> node scripts/docs-inventory.mjs --check

Plugin documentation inventory is up to date.
  ok    block-id-prompt
  ok    bob-articles
  ok    bob-chips
  ok    bob-command-mode
  ok    bob-emoji
  ok    bob-ledger-tools
  ok    bob-mail
  ok    bob-navigation-hotkeys
  ok    bob-project-tasks
  ok    bob-vim-surround
  ok    bob-vim-yank-flash
  ok    task-status-cycler

12/12 plugin(s) valid
validate exit=0
succeeded  exit=0  duration=474123ms

