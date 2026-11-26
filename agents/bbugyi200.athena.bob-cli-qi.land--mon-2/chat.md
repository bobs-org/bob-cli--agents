# Chat History - ace-run (bob-cli-qi.land--mon-2)

- **TIMESTAMP:** 2026-11-26 17:24:40 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-qi.land--mon-2

## Prompt

sase monitor start --command 'export CARGO_TARGET_DIR="$PWD/target" TMPDIR=/tmp; cargo build && mkdir -p target/bank-hub-home-takeover-acceptance-20261126-run1/screenshots && BOB_BIN="$PWD/target/debug/bob" BOB_CLI_DIR="$PWD" xvfb-run -a node "$PWD/sase/repos/linked/bob-plugins/scripts/obsidian-frontmatter-takeover-e2e.cjs" -e /snap/obsidian/current/app/obsidian -o "$PWD/target/bank-hub-home-takeover-acceptance-20261126-run1/screenshots" -r "$PWD/target/bank-hub-home-takeover-acceptance-20261126-run1/report.json" --profile full' --reason 'Run the expanded full bank and home-card takeover acceptance in isolated Obsidian'

## Response

sase tool run 0448d08de5a9d5084a79bc586864f635
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling cfg-if v1.0.4
   Compiling typenum v1.20.1
   Compiling siphasher v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling version_check v0.9.5
   Compiling libc v0.2.186
   Compiling fastrand v2.5.0
   Compiling smallvec v1.15.2
   Compiling memchr v2.8.1
   Compiling parking_lot_core v0.9.12
   Compiling bitflags v2.12.1
   Compiling litemap v0.8.3
   Compiling new_debug_unreachable v1.0.6
   Compiling shlex v2.0.1
   Compiling serde_core v1.0.228
   Compiling writeable v0.6.4
   Compiling scopeguard v1.2.0
   Compiling autocfg v1.5.1
   Compiling precomputed-hash v0.1.1
   Compiling find-msvc-tools v0.1.9
   Compiling simd-adler32 v0.3.9
   Compiling itoa v1.0.18
   Compiling foldhash v0.2.0
   Compiling generic-array v0.14.7
   Compiling utf8_iter v1.0.4
   Compiling allocator-api2 v0.2.21
   Compiling phf_shared v0.14.0
   Compiling lock_api v0.4.14
   Compiling crc32fast v1.5.0
   Compiling equivalent v1.0.2
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
   Compiling serde v1.0.228
   Compiling num-traits v0.2.19
   Compiling cc v1.2.63
   Compiling log v0.4.30
   Compiling getrandom v0.4.2
   Compiling adler2 v2.0.1
   Compiling utf8parse v0.2.2
   Compiling rand_core v0.10.1
   Compiling phf_generator v0.14.0
   Compiling is_terminal_polyfill v1.70.2
   Compiling hashbrown v0.17.1
   Compiling miniz_oxide v0.8.9
   Compiling anstyle-parse v1.0.0
   Compiling dtoa v1.0.11
   Compiling cpufeatures v0.3.0
   Compiling tinyvec_macros v0.1.1
   Compiling anstyle v1.0.14
   Compiling phf_codegen v0.14.0
   Compiling anstyle-query v1.1.5
   Compiling colorchoice v1.0.5
   Compiling dtoa-short v0.3.5
   Compiling tendril v0.5.1
   Compiling tinyvec v1.11.0
   Compiling rustix v1.1.5
   Compiling hybrid-array v0.4.12
   Compiling unicode-width v0.2.3
   Compiling cpufeatures v0.2.17
   Compiling anstream v1.0.0
   Compiling zmij v1.0.21
   Compiling flate2 v1.1.9
   Compiling weezl v0.1.12
   Compiling rquickjs-sys v0.12.1
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling string_cache_codegen v0.11.2
   Compiling thiserror v2.0.18
   Compiling strsim v0.11.1
   Compiling parking_lot v0.12.5
   Compiling clap_lex v1.1.0
   Compiling unicode-normalization v0.1.25
   Compiling getopts v0.2.24
   Compiling indexmap v2.14.0
   Compiling block-buffer v0.12.0
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling web_atoms v0.3.0
   Compiling crypto-common v0.2.2
   Compiling clap_builder v4.6.7
   Compiling string_cache v0.11.0
   Compiling chacha20 v0.10.2
   Compiling nom v8.0.0
   Compiling inout v0.1.4
   Compiling digest v0.10.7
   Compiling aho-corasick v1.1.4
   Compiling fdeflate v0.3.7
   Compiling phf_shared v0.12.1
   Compiling cipher v0.4.4
   Compiling servo_arc v0.5.0
   Compiling const-oid v0.10.2
   Compiling byteorder-lite v0.1.0
   Compiling iana-time-zone v0.1.65
   Compiling pulldown-cmark v0.13.6
   Compiling regex-syntax v0.8.10
   Compiling chrono-tz v0.10.4
   Compiling serde_json v1.0.150
   Compiling zune-core v0.5.3
   Compiling quick-error v2.0.1
   Compiling bytecount v0.6.9
   Compiling percent-encoding v2.3.2
   Compiling unicode-bidi v0.3.18
   Compiling unicode-properties v0.1.4
   Compiling color_quant v1.1.0
   Compiling pxfm v0.1.30
   Compiling linux-raw-sys v0.12.1
   Compiling rustc-hash v2.1.3
   Compiling image-webp v0.2.4
   Compiling form_urlencoded v1.2.2
   Compiling zune-jpeg v0.5.15
   Compiling gif v0.14.2
   Compiling digest v0.11.3
   Compiling aes v0.8.4
   Compiling cbc v0.1.2
   Compiling stringprep v0.1.5
   Compiling ecb v0.1.2
   Compiling png v0.18.1
   Compiling phf v0.12.1
   Compiling rand v0.10.1
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling encoding_rs v0.8.35
   Compiling rangemap v1.7.1
   Compiling ego-tree v0.11.1
   Compiling once_cell v1.21.4
   Compiling is_executable v1.0.6
   Compiling bytemuck v1.25.2
   Compiling unsafe-libyaml v0.2.11
   Compiling pulldown-cmark-escape v0.11.0
   Compiling unicase v2.10.0
   Compiling ttf-parser v0.25.1
   Compiling clap v4.6.7
   Compiling ryu v1.0.23
   Compiling clap_complete v4.6.11
   Compiling sha2 v0.11.0
   Compiling nom_locate v5.0.0
   Compiling regex-automata v0.4.14
   Compiling fs2 v0.4.3
   Compiling phf_macros v0.14.0
   Compiling serde_derive v1.0.228
   Compiling derive_more-impl v2.1.1
   Compiling thiserror-impl v2.0.18
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling cssparser-macros v0.7.1
   Compiling phf v0.14.0
   Compiling tempfile v3.27.0
   Compiling moxcms v0.8.1
   Compiling roxmltree v0.21.2
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling derive_more v2.1.1
   Compiling cssparser v0.38.0
   Compiling similar v2.7.0
   Compiling hex v0.4.3
   Compiling glob v0.3.4
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/crates/bob-obsidian-assets)
   Compiling base64 v0.22.1
   Compiling zerofrom v0.1.8
   Compiling yoke v0.8.3
   Compiling lopdf v0.40.0
   Compiling markup5ever v0.40.0
   Compiling selectors v0.41.0
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling html5ever v0.40.1
   Compiling regex v1.12.3
   Compiling chrono v0.4.44
   Compiling serde_yaml v0.9.34+deprecated
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling scraper v0.29.0
   Compiling icu_locale_core v2.3.0
   Compiling icu_collections v2.3.0
   Compiling icu_provider v2.3.1
   Compiling image v0.25.10
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling rquickjs-core v0.12.1
   Compiling rquickjs v0.12.1
   Compiling bob-obsidian v0.6.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15)
    Finished `dev` profile [unoptimized + debuginfo] target(s) in 2m 21s
[frontmatter-takeover] check start own-day-live 2026-11-26T22:21:37.361Z
[frontmatter-takeover] check done own-day-live status=pass 2026-11-26T22:21:37.676Z
[frontmatter-takeover] check start own-day-reading 2026-11-26T22:21:37.676Z
[frontmatter-takeover] check done own-day-reading status=pass 2026-11-26T22:21:38.078Z
[frontmatter-takeover] check start own-week-live 2026-11-26T22:21:38.078Z
[frontmatter-takeover] check done own-week-live status=pass 2026-11-26T22:21:38.440Z
[frontmatter-takeover] check start own-week-reading 2026-11-26T22:21:38.441Z
[frontmatter-takeover] check done own-week-reading status=pass 2026-11-26T22:21:38.792Z
[frontmatter-takeover] check start own-record-live 2026-11-26T22:21:38.792Z
[frontmatter-takeover] check done own-record-live status=pass 2026-11-26T22:21:39.192Z
[frontmatter-takeover] check start own-record-reading 2026-11-26T22:21:39.192Z
[frontmatter-takeover] check done own-record-reading status=pass 2026-11-26T22:21:39.546Z
[frontmatter-takeover] check start own-album-live 2026-11-26T22:21:39.546Z
[frontmatter-takeover] check done own-album-live status=pass 2026-11-26T22:21:40.223Z
[frontmatter-takeover] check start own-album-reading 2026-11-26T22:21:40.223Z
[frontmatter-takeover] check done own-album-reading status=pass 2026-11-26T22:21:40.541Z
[frontmatter-takeover] check start own-area-live 2026-11-26T22:21:40.542Z
[frontmatter-takeover] check done own-area-live status=pass 2026-11-26T22:21:41.015Z
[frontmatter-takeover] check start own-area-reading 2026-11-26T22:21:41.015Z
[frontmatter-takeover] check done own-area-reading status=pass 2026-11-26T22:21:41.365Z
[frontmatter-takeover] check start own-subarea-live 2026-11-26T22:21:41.365Z
[frontmatter-takeover] check done own-subarea-live status=pass 2026-11-26T22:21:41.707Z
[frontmatter-takeover] check start own-subarea-reading 2026-11-26T22:21:41.707Z
[frontmatter-takeover] check done own-subarea-reading status=pass 2026-11-26T22:21:42.058Z
[frontmatter-takeover] check start own-inbox-live 2026-11-26T22:21:42.058Z
[frontmatter-takeover] check done own-inbox-live status=pass 2026-11-26T22:21:42.392Z
[frontmatter-takeover] check start own-inbox-reading 2026-11-26T22:21:42.392Z
[frontmatter-takeover] check done own-inbox-reading status=pass 2026-11-26T22:21:42.741Z
[frontmatter-takeover] check start own-project-live 2026-11-26T22:21:42.741Z
[frontmatter-takeover] check done own-project-live status=pass 2026-11-26T22:21:43.075Z
[frontmatter-takeover] check start own-project-reading 2026-11-26T22:21:43.075Z
[frontmatter-takeover] check done own-project-reading status=pass 2026-11-26T22:21:43.441Z
[frontmatter-takeover] check start own-project-terminal-live 2026-11-26T22:21:43.441Z
[frontmatter-takeover] check done own-project-terminal-live status=pass 2026-11-26T22:21:43.791Z
[frontmatter-takeover] check start own-project-terminal-reading 2026-11-26T22:21:43.791Z
[frontmatter-takeover] check done own-project-terminal-reading status=pass 2026-11-26T22:21:44.157Z
[frontmatter-takeover] check start excluded-home-cards-native 2026-11-26T22:21:44.157Z
[frontmatter-takeover] check done excluded-home-cards-native status=pass 2026-11-26T22:21:44.541Z
[frontmatter-takeover] check start foreign-refresh-keeps-ownership 2026-11-26T22:21:44.541Z
[frontmatter-takeover] check done foreign-refresh-keeps-ownership status=pass 2026-11-26T22:21:47.941Z
[frontmatter-takeover] check start bank-cache-parity 2026-11-26T22:21:47.941Z
[frontmatter-takeover] check done bank-cache-parity status=pass 2026-11-26T22:21:48.896Z
[frontmatter-takeover] check start own-bank-live 2026-11-26T22:21:48.896Z
[frontmatter-takeover] check done own-bank-live status=pass 2026-11-26T22:21:49.728Z
[frontmatter-takeover] check start own-bank-reading 2026-11-26T22:21:49.728Z
[frontmatter-takeover] check done own-bank-reading status=pass 2026-11-26T22:21:50.673Z
[frontmatter-takeover] check start bank-pane-path-lifecycle 2026-11-26T22:21:50.673Z
[frontmatter-takeover] check done bank-pane-path-lifecycle status=pass 2026-11-26T22:21:52.506Z
[frontmatter-takeover] check start bank-generic-editor-gestures 2026-11-26T22:21:52.506Z
[frontmatter-takeover] check done bank-generic-editor-gestures status=pass 2026-11-26T22:21:53.627Z
[frontmatter-takeover] check start home-card-gestures-live 2026-11-26T22:21:53.628Z
[frontmatter-takeover] check done home-card-gestures-live status=fail 2026-11-26T22:22:03.870Z
[frontmatter-takeover] check start project-prj-line-integrity-live 2026-11-26T22:22:03.870Z
[frontmatter-takeover] check done project-prj-line-integrity-live status=fail 2026-11-26T22:22:04.507Z
[frontmatter-takeover] check start own-quarter-live 2026-11-26T22:22:04.507Z
[frontmatter-takeover] check done own-quarter-live status=pass 2026-11-26T22:22:04.823Z
[frontmatter-takeover] check start own-year-live 2026-11-26T22:22:04.823Z
[frontmatter-takeover] check done own-year-live status=pass 2026-11-26T22:22:05.140Z
[frontmatter-takeover] check start own-identity-day-live 2026-11-26T22:22:05.140Z
[frontmatter-takeover] check done own-identity-day-live status=pass 2026-11-26T22:22:05.474Z
[frontmatter-takeover] check start own-identity-day-reading 2026-11-26T22:22:05.475Z
[frontmatter-takeover] check done own-identity-day-reading status=pass 2026-11-26T22:22:05.840Z
[frontmatter-takeover] check start title-slot-anchor-live 2026-11-26T22:22:05.840Z
[frontmatter-takeover] check done title-slot-anchor-live status=pass 2026-11-26T22:22:05.964Z
[frontmatter-takeover] check start variables-live 2026-11-26T22:22:05.965Z
[frontmatter-takeover] check done variables-live status=pass 2026-11-26T22:22:06.322Z
[frontmatter-takeover] check start vim-k-gg-up-live 2026-11-26T22:22:06.322Z
[frontmatter-takeover] check done vim-k-gg-up-live status=pass 2026-11-26T22:22:09.793Z
[frontmatter-takeover] check start tab-live 2026-11-26T22:22:09.793Z
[frontmatter-takeover] check done tab-live status=pass 2026-11-26T22:22:10.722Z
[frontmatter-takeover] check start bank-vim-k-gg-live 2026-11-26T22:22:10.722Z
[frontmatter-takeover] check done bank-vim-k-gg-live status=pass 2026-11-26T22:22:11.823Z
[frontmatter-takeover] check start bank-focusin-guard 2026-11-26T22:22:11.823Z
[frontmatter-takeover] check done bank-focusin-guard status=pass 2026-11-26T22:22:12.291Z
[frontmatter-takeover] check start title-slot-anchor-reading 2026-11-26T22:22:12.291Z
[frontmatter-takeover] check done title-slot-anchor-reading status=pass 2026-11-26T22:22:12.427Z
[frontmatter-takeover] check start variables-reading 2026-11-26T22:22:12.427Z
[frontmatter-takeover] check done variables-reading status=pass 2026-11-26T22:22:12.821Z
[frontmatter-takeover] check start tab-reading 2026-11-26T22:22:12.821Z
[frontmatter-takeover] check done tab-reading status=pass 2026-11-26T22:22:13.502Z
[frontmatter-takeover] check start source-toggle-releases 2026-11-26T22:22:13.503Z
[frontmatter-takeover] check done source-toggle-releases status=pass 2026-11-26T22:22:14.557Z
[frontmatter-takeover] check start deny-embed 2026-11-26T22:22:14.557Z
[frontmatter-takeover] check done deny-embed status=pass 2026-11-26T22:22:15.257Z
[frontmatter-takeover] check start deny-hover 2026-11-26T22:22:15.257Z
[frontmatter-takeover] check done deny-hover status=pass 2026-11-26T22:22:16.123Z
[frontmatter-takeover] check start deny-canvas 2026-11-26T22:22:16.123Z
[frontmatter-takeover] check done deny-canvas status=pass 2026-11-26T22:22:16.125Z
[frontmatter-takeover] check start deny-print 2026-11-26T22:22:16.125Z
[frontmatter-takeover] check done deny-print status=pass 2026-11-26T22:22:16.126Z
[frontmatter-takeover] check start deny-mobile 2026-11-26T22:22:16.126Z
[frontmatter-takeover] check done deny-mobile status=pass 2026-11-26T22:22:16.715Z
[frontmatter-takeover] check start deny-malformed 2026-11-26T22:22:16.715Z
[frontmatter-takeover] check done deny-malformed status=pass 2026-11-26T22:22:16.889Z
[frontmatter-takeover] check start deny-unclosed 2026-11-26T22:22:16.890Z
[frontmatter-takeover] check done deny-unclosed status=pass 2026-11-26T22:22:17.475Z
[frontmatter-takeover] check start stale-cache-releases 2026-11-26T22:22:17.476Z
[frontmatter-takeover] check done stale-cache-releases status=pass 2026-11-26T22:22:19.824Z
[frontmatter-takeover] check start bank-cache-skew-releases 2026-11-26T22:22:19.824Z
[frontmatter-takeover] check done bank-cache-skew-releases status=pass 2026-11-26T22:22:20.323Z
[frontmatter-takeover] check start live-autosave-keeps-ownership 2026-11-26T22:22:20.323Z
[frontmatter-takeover] check done live-autosave-keeps-ownership status=pass 2026-11-26T22:22:30.877Z
[frontmatter-takeover] check start live-slow-reparse-keeps-card 2026-11-26T22:22:30.878Z
[frontmatter-takeover] check done live-slow-reparse-keeps-card status=pass 2026-11-26T22:22:42.641Z
[frontmatter-takeover] check start same-pane-file-change 2026-11-26T22:22:42.641Z
[frontmatter-takeover] check done same-pane-file-change status=pass 2026-11-26T22:22:43.270Z
[frontmatter-takeover] check start injected-mount-failure 2026-11-26T22:22:43.270Z
[frontmatter-takeover] check done injected-mount-failure status=pass 2026-11-26T22:22:43.793Z
[frontmatter-takeover] check start replaced-container-reapplies 2026-11-26T22:22:43.793Z
[frontmatter-takeover] check done replaced-container-reapplies status=pass 2026-11-26T22:22:44.456Z
[frontmatter-takeover] check start disable-unload-restores 2026-11-26T22:22:44.456Z
[frontmatter-takeover] check done disable-unload-restores status=pass 2026-11-26T22:22:46.506Z
[frontmatter-takeover] check start pending-capability-native 2026-11-26T22:22:46.506Z
[frontmatter-takeover] check done pending-capability-native status=pass 2026-11-26T22:22:48.004Z
[frontmatter-takeover] check start absent-old-bob-native 2026-11-26T22:22:48.004Z
[frontmatter-takeover] check done absent-old-bob-native status=pass 2026-11-26T22:22:49.438Z
[frontmatter-takeover] check start failed-probe-native 2026-11-26T22:22:49.438Z
[frontmatter-takeover] check done failed-probe-native status=pass 2026-11-26T22:22:50.809Z
[frontmatter-takeover] check start bank-props-v1-only-owned 2026-11-26T22:22:50.809Z
[frontmatter-takeover] check done bank-props-v1-only-owned status=fail 2026-11-26T22:22:52.320Z
[frontmatter-takeover] check start path-switch-native 2026-11-26T22:22:52.321Z
[frontmatter-takeover] check done path-switch-native status=pass 2026-11-26T22:22:53.878Z
[frontmatter-takeover] check start late-after-unload-native 2026-11-26T22:22:53.878Z
[frontmatter-takeover] check done late-after-unload-native status=pass 2026-11-26T22:22:56.256Z
[frontmatter-takeover] check start mod-semicolon-add-owned 2026-11-26T22:22:56.256Z
[frontmatter-takeover] check done mod-semicolon-add-owned status=pass 2026-11-26T22:22:57.145Z
[frontmatter-takeover] check start palette-add-owned 2026-11-26T22:22:57.145Z
[frontmatter-takeover] check done palette-add-owned status=pass 2026-11-26T22:22:57.945Z
[frontmatter-takeover] check start custom-shortcut-add-owned 2026-11-26T22:22:57.945Z
[frontmatter-takeover] check done custom-shortcut-add-owned status=pass 2026-11-26T22:22:59.242Z
[frontmatter-takeover] check start bank-add-file-property 2026-11-26T22:22:59.242Z
[frontmatter-takeover] check done bank-add-file-property status=pass 2026-11-26T22:23:00.478Z
[frontmatter-takeover] check start ordinary-native 2026-11-26T22:23:00.478Z
[frontmatter-takeover] check done ordinary-native status=pass 2026-11-26T22:23:00.988Z
[frontmatter-takeover] check start bank-sidebar-native 2026-11-26T22:23:00.988Z
[frontmatter-takeover] check done bank-sidebar-native status=pass 2026-11-26T22:23:01.632Z
[frontmatter-takeover] check start field-focused-helper 2026-11-26T22:23:01.633Z
[frontmatter-takeover] check done field-focused-helper status=pass 2026-11-26T22:23:02.752Z
[frontmatter-takeover] check start failed-opener-fallback 2026-11-26T22:23:02.752Z
[frontmatter-takeover] check done failed-opener-fallback status=pass 2026-11-26T22:23:03.517Z
[frontmatter-takeover] check start drawer-exposes-every-key 2026-11-26T22:23:03.517Z
[frontmatter-takeover] check done drawer-exposes-every-key status=pass 2026-11-26T22:23:03.917Z
[frontmatter-takeover] screenshot day-live-light-narrow sha256=49e42240fada5281b21215550ac6fea5e729b5651df18336c2a8dba0e7ce5a51
[frontmatter-takeover] screenshot day-reading-light-narrow sha256=74adb1198d90f327382f8af97c4697ecc5c5ad40d59355dd426b9978d4450b7d
[frontmatter-takeover] screenshot day-live-light-wide sha256=2386b23149037e59eaf0323000b13f10d8f347a58669bf56722ebc3eea5bf733
[frontmatter-takeover] screenshot day-reading-light-wide sha256=d6bc0581126610bbe1763e96e382dda954ddb87c3d953e5a978693bc6ca2f3bc
[frontmatter-takeover] screenshot day-live-dark-narrow sha256=17bdf2101ca903e0fb421211e9f29a52b8fed2ad43f73d0f961077ad04ad6384
[frontmatter-takeover] screenshot day-reading-dark-narrow sha256=4a856ee6041bbbe604c63014de077c72a8ce1bf42bd59163429ff9000ddb8f68
[frontmatter-takeover] screenshot day-live-dark-wide sha256=59062fd420b2b5eac022c0805e1364c73151afa2ec8382ad1aa86e64fd657bb3
[frontmatter-takeover] screenshot day-reading-dark-wide sha256=1bca8a689b65f829aabf7f0c31a87e4e7299ecd65278486fa56021f5fb5af09e
[frontmatter-takeover] screenshot week-live-light-narrow sha256=5916501acd2b749d4e3bb88eaae06f3c1f012d87eb5be422d057cd90b16591b7
[frontmatter-takeover] screenshot week-reading-light-narrow sha256=285e40bd615615bb88779400198e34ffe332cda63bd32c12b003d3d280a830c6
[frontmatter-takeover] screenshot week-live-light-wide sha256=13431592a8b5b47e831a375a242010c4deb892aaf098b4c706b8d8ee524f74e8
[frontmatter-takeover] screenshot week-reading-light-wide sha256=b0caa793998bf4fac379c2c48d6a81a92c91d8d5e1b99c8837c172363743a381
[frontmatter-takeover] screenshot week-live-dark-narrow sha256=8d348a7dbd05ad98729fd64b05073badc94055766e0237b1ac810bf9bca33b9a
[frontmatter-takeover] screenshot week-reading-dark-narrow sha256=6686dbf72f86d3fe0f7ce0d1b8a6f114954890acd158b63e37b40f2e8ba19f0d
[frontmatter-takeover] screenshot week-live-dark-wide sha256=1634159fd34803990313a0f8aad30fc49c035f0d0bc28eeb2f22fa1547838359
[frontmatter-takeover] screenshot week-reading-dark-wide sha256=1dc8454039f87e4fd4498c18f57f07d491c92b9269b97e7cb82ad21bcf120eca
[frontmatter-takeover] screenshot record-live-light-narrow sha256=23f33b42ea314c81291cca394196ca836486ca348ac6285d666c6c7cba3ffc91
[frontmatter-takeover] screenshot record-reading-light-narrow sha256=ccb7361703089c911601b9dadacd52016676aacbf77c6ba8bc119fce8efff64a
[frontmatter-takeover] screenshot record-live-light-wide sha256=678bb855f584afa750bd31e980623fd935a92e631ee59a989115b8003e5e883c
[frontmatter-takeover] screenshot record-reading-light-wide sha256=04791cee3597e12430de1d85069f4fda15543f2fbaf4ae911e700a48e12c70e6
[frontmatter-takeover] screenshot record-live-dark-narrow sha256=2888e5555db486cbca0e21932f5626119b28eb3065d39cbfe9cd1b8e49e41f62
[frontmatter-takeover] screenshot record-reading-dark-narrow sha256=66b08fea62e7b5a24005b169bb369772fca04aee7c95cabb532e4a2713795f2a
[frontmatter-takeover] screenshot record-live-dark-wide sha256=eab70b945a04e8ef867bba1758077aa500474d65306231b679992be4764cdb48
[frontmatter-takeover] screenshot record-reading-dark-wide sha256=3b7f1215406d14e027092d0603c92fffc9953d8af0c17f672a68616ae59e3201
[frontmatter-takeover] screenshot album-live-light-narrow sha256=e0cdf8a549c11cb61c2cc647fe74362ff2a158bee4fd99bdfaa94dc87704186c
[frontmatter-takeover] screenshot album-reading-light-narrow sha256=ad3c14d6076543488c4f9429b6beff39767c12defc12d562fbf55952a03ff970
[frontmatter-takeover] screenshot album-live-light-wide sha256=a8a284a7f4aecfd38dfa44110f6ffd7cc65044df71895660b3336228b3ae0031
[frontmatter-takeover] screenshot album-reading-light-wide sha256=31cf95c18629c8d261176cbde045bb044f5d32bc3ed6db11aebfd5b4d8469557
[frontmatter-takeover] screenshot album-live-dark-narrow sha256=e05df5d54a28ede1f8b6e214194d07f2441914a394f9e64e18ca2171e9af5ad9
[frontmatter-takeover] screenshot album-reading-dark-narrow sha256=1e2d15f3210ddddb4f840703752cbeb9b8ce68e587c238422a036b37f8cefd61
[frontmatter-takeover] screenshot album-live-dark-wide sha256=8903ed187f4410584d902ca6057912e19868aa32491bc72990eb630def581ab4
[frontmatter-takeover] screenshot album-reading-dark-wide sha256=cd319d4add24e0c0dc49a43c0e2b2a6d4598a4ecd45fbb4df3e6337c56df93bf
[frontmatter-takeover] screenshot bank-live-light-narrow sha256=029bdb5fde00fe497bc359db6948a74f104639a10d06ae317703ddd5c112b7fa
[frontmatter-takeover] screenshot bank-reading-light-narrow sha256=5cb6b956d835396e79aa46050a743c3aed5cbd985d8fc695d6330154d7d76867
[frontmatter-takeover] screenshot bank-live-light-wide sha256=1190efd94601b587f98c2c4dfd75ce9b057b5475fcbaa297a50804a3b541a457
[frontmatter-takeover] screenshot bank-reading-light-wide sha256=b282e27d168d90f62fddb23114a44d72ca9e24c3be7a9813ed104169b78409b1
[frontmatter-takeover] screenshot bank-live-dark-narrow sha256=fa10068cb86ded66f0a2d7b8c9a01ef40d98d22919df04da39ef3724f3aac391
[frontmatter-takeover] screenshot bank-reading-dark-narrow sha256=905e3dc298596375ec5ffa475bdb380710d924a41746c809d4734f7b289eafc3
[frontmatter-takeover] screenshot bank-live-dark-wide sha256=43f9305f63aa43ad426d03ec812bae7e3349bccda8fd5151c89bf8a4cd662945
[frontmatter-takeover] screenshot bank-reading-dark-wide sha256=42aaf19b9357cea9a31693b272c7b2adabbd28fb9e6c90adfbacc49541d3e89f
[frontmatter-takeover] screenshot area-live-light-narrow sha256=33837ea071414b785c193f231336329480076a83a3b46355ef9e4ac292bd80cc
[frontmatter-takeover] screenshot area-reading-light-narrow sha256=35b3d4cb6c47b387db62cd11d6bad4377910aff17f5a0c7e85b660ec2faefd1c
[frontmatter-takeover] screenshot area-live-light-wide sha256=674f6a855ec7b0d3e43c000d2997c6d21b5d833dca72120242d7f86614ce9186
[frontmatter-takeover] screenshot area-reading-light-wide sha256=919ee4c9c95e82917349879564a127ac4e289ecd2be0dd3b2ffd616fa36a6e7c
[frontmatter-takeover] screenshot area-live-dark-narrow sha256=65b4732328cbf65128089b2500900337e67b28b61c9cd70d02cbb10958cf79de
[frontmatter-takeover] screenshot area-reading-dark-narrow sha256=458a6753c108e1e47b75fa1d61c8d55e3fbe60e13d1766c24d5f51212eccf78c
[frontmatter-takeover] screenshot area-live-dark-wide sha256=dc5cc5df4cc81c99c75fa45ddfc4a0a86b3bf52c39a55a398cdf58bb4bc569a4
[frontmatter-takeover] screenshot area-reading-dark-wide sha256=2b020b8b6c5d8d6ee732f4bb9d3470513f95b1f408e59a5a5da899fce4ebf27f
[frontmatter-takeover] screenshot inbox-live-light-narrow sha256=d04f944855fc1abc5197c2f5910f42047f6e687907487f5628beed07593e4a66
[frontmatter-takeover] screenshot inbox-reading-light-narrow sha256=da0f2a299d498faa1ad04a46963a7b6174ca5c91862930cec09bf40466c82bfc
[frontmatter-takeover] screenshot inbox-live-light-wide sha256=ebfdd5ed12640436c10894cb348606f792c3c014f7cfd27fcd4550f68b932af6
[frontmatter-takeover] screenshot inbox-reading-light-wide sha256=eeac245a7cba886433860073a2a8c0ad94d475be9e16d7b83e27d911f5d3376b
[frontmatter-takeover] screenshot inbox-live-dark-narrow sha256=9656946da9c983d3d179238b36293a0e1f5ebe907f8bd815c31307bfbc77e4ee
[frontmatter-takeover] screenshot inbox-reading-dark-narrow sha256=fcb3e04db8dd6e15d3ffe13dc7ce69664d37807f6116b8e874f2d66329b2802e
[frontmatter-takeover] screenshot inbox-live-dark-wide sha256=886aa0c6ff5c61eb15e6d65a50e55e0e79272e5933792c93b1a8d577e331069f
[frontmatter-takeover] screenshot inbox-reading-dark-wide sha256=c3836e5b92ab45985ae82a1e677b4af59a2aa17baf235ae55fc0b2802e38bef4
[frontmatter-takeover] screenshot project-live-light-narrow sha256=27645eb277bddecd3aca6ff575a05b720ddf6e82c1225f5600ad69dcb462cae3
[frontmatter-takeover] screenshot project-reading-light-narrow sha256=857a67ac02595f3b332754fb41a77ee0e51fe8672bcc58ae86b9038c52decb8b
[frontmatter-takeover] screenshot project-live-light-wide sha256=00b6530da36836c6ab69500efc4d09e1141884ae1016e21bff628f4870d0860f
[frontmatter-takeover] screenshot project-reading-light-wide sha256=e26051710bdcada95a4f8b37e44cb3e26c8d9141e7363ff206d602d3079be1e7
[frontmatter-takeover] screenshot project-live-dark-narrow sha256=9545501ff20f8b95df05b797743e64fcedcc5a240a01a79434c0b413d7b37c60
[frontmatter-takeover] screenshot project-reading-dark-narrow sha256=bcb7fb8880b73aeb7921725d27bcfda10d55c6929d8b7f9c714848f6fd844e84
[frontmatter-takeover] screenshot project-live-dark-wide sha256=1a5c3c0d1dde44a984d60a61c156b794cf23b0b31cd8ebbf90328d8bebeccaf2
[frontmatter-takeover] screenshot project-reading-dark-wide sha256=658208e1e5530ad923be22cf26791238b997ad86088dc6ca34b377e9e3987ede
[frontmatter-takeover] screenshot project-terminal-live-light-narrow sha256=d65eaf1cc2b9839831ecfebaf2e561d17896cc22cb94ba147df91b88180f922a
[frontmatter-takeover] screenshot project-terminal-reading-light-narrow sha256=e6a1cc97add1f480ac9034e3d8916cf398980097ae845dda06a93cfcd991e31d
[frontmatter-takeover] screenshot project-terminal-live-light-wide sha256=199b0581d9e75f0e5e28b9b97bed533efde567f3873f394c22b74d12e1c4039c
[frontmatter-takeover] screenshot project-terminal-reading-light-wide sha256=59e127ac7602cd320d9ff92638cff0dbd4d7a3fd88fe8112e392009674b03b98
[frontmatter-takeover] screenshot project-terminal-live-dark-narrow sha256=8a88356b2ad0cc64eacadb8abd3a6a3403d95eee0b0fb869a2d79c8d3cb6ddcb
[frontmatter-takeover] screenshot project-terminal-reading-dark-narrow sha256=9825d86cbffe58d2207722ebf8781f5fd233023617e33064297ff82c439b232c
[frontmatter-takeover] screenshot project-terminal-live-dark-wide sha256=db1a057e12536830021e4d24de1b6f869dce22076693920da7e5cba2675baabb
[frontmatter-takeover] screenshot project-terminal-reading-dark-wide sha256=5f07cb9bb66cc50ee87feb042793125fb3c0fed8d66062c4079d1ca01c4aa7ae
[frontmatter-takeover] screenshot ordinary-add-light-narrow sha256=046032ca5ee6f35439b5900bfa345acf6232c0ee52e37d30f901b077903660e4
[frontmatter-takeover] screenshot ordinary-add-light-wide sha256=85c5d151e1261eca677573677f364df382fbe009c6e31d98ecf8f43203ba2a68
[frontmatter-takeover] screenshot ordinary-add-dark-narrow sha256=98571809b14284f0d387f9fd525c28e1f7bd44eeaf9c59f867e1c3fa8cf0d890
[frontmatter-takeover] screenshot ordinary-add-dark-wide sha256=d429ce7c2fbade9e65ba5d085b69db482dc0409e7a1c26d5706e50e98b48ddba
[frontmatter-takeover] screenshot fallback-source-day sha256=59ce883eb31eeecc7ee2648202f1634dce97c30f8c0b8bbaf4115eacc4e23cec
[frontmatter-takeover] screenshot fallback-malformed-day sha256=92568ef4a779922838a574c0d7f2e4697d121a183b7c2bd04bb284fd2c5f69c6
{
  "obsidian": "1.15.1",
  "plugin": "1.170.0",
  "commit": "319862a7f4a8606c961302e2bb26d0e6b89b8332",
  "bob": {
    "path": "/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/target/debug/bob",
    "sha256": "0669e24cf7c6334a4e6a0335c772f6675e6c2aec7fb6c4ad5a11fce712c7a6fa",
    "version": "bob 0.6.0",
    "sourceSha": "33fe3425b51207b39215bb2a8553224b3302bea7"
  },
  "verdict": "NO-GO",
  "fallback": [],
  "addFilePropertyCommand": {
    "id": "markdown:add-metadata-property",
    "name": "Add file property",
    "detail": {
      "found": true,
      "id": "markdown:add-metadata-property",
      "name": "Add file property",
      "callbackType": "undefined",
      "checkCallbackType": "function",
      "commandHotkeys": [
        {
          "modifiers": [
            "Mod"
          ],
          "key": ";"
        }
      ],
      "registeredHotkeys": null,
      "defaultHotkeys": [
        {
          "modifiers": [
            "Mod"
          ],
          "key": ";"
        }
      ],
      "obsidianVersion": "1.15.1"
    },
    "exactMatches": 1
  },
  "failed": [
    "home-card-gestures-live",
    "project-prj-line-integrity-live",
    "bank-props-v1-only-owned",
    "no-paint-spawn",
    "no-console-exceptions"
  ],
  "screenshots": 78,
  "consoleExceptions": 6,
  "skippedChecks": 0
}
report: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/target/bank-hub-home-takeover-acceptance-20261126-run1/report.json
screenshots: /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/target/bank-hub-home-takeover-acceptance-20261126-run1/screenshots
failed  exit=1  duration=346398ms

