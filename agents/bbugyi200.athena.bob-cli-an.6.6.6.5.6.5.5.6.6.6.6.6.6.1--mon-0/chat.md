# Chat History - ace-run (bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--mon-0)

- **TIMESTAMP:** 2026-10-26 13:44:13 EDT
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-an.6.6.6.5.6.5.5.6.6.6.6.6.6.1--mon-0

## Prompt

sase monitor start --command 'cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11/sase/repos/linked/bob-plugins && node --test scripts/test-task-status-cycler-pomodoro-reopen.cjs scripts/test-task-status-cycler-freshness.cjs scripts/test-ledger-tools-freshness-placement.cjs scripts/test-ledger-tools-freshness-keeps.cjs scripts/test-navigation-stamps.cjs scripts/test-block-id-prompt-plan-budget-and-freshness.cjs && cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11 && cargo test --lib native::freshness::placement_tests' --reason 'Run the approved phase’s focused plugin regressions and Rust freshness placement tests'

## Response

sase tool run 73ac6ca15a51cb09068732b886e06fa3
TAP version 13
# Subtest: plan budget suffix: link Notice appends the meter computed on post-write daily content
ok 1 - plan budget suffix: link Notice appends the meter computed on post-write daily content
  ---
  duration_ms: 6.989567
  ...
# Subtest: plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
ok 2 - plan budget suffix: link Notice omits the meter when the ledger-tools API is missing
  ---
  duration_ms: 1.793064
  ...
# Subtest: plan budget suffix: unlink Notice marks an over-cap plan with 🔴
ok 3 - plan budget suffix: unlink Notice marks an over-cap plan with 🔴
  ---
  duration_ms: 2.002464
  ...
# Subtest: plan budget suffix: Next task without a block ID prompts for one and omits the meter
ok 4 - plan budget suffix: Next task without a block ID prompts for one and omits the meter
  ---
  duration_ms: 0.404102
  ...
# Subtest: plan budget suffix: Task Link Notice appends the meter from post-write daily content
ok 5 - plan budget suffix: Task Link Notice appends the meter from post-write daily content
  ---
  duration_ms: 2.108366
  ...
# Subtest: plan budget suffix: Task Link Notice omits the meter when no daily note takes part
ok 6 - plan budget suffix: Task Link Notice omits the meter when no daily note takes part
  ---
  duration_ms: 0.557104
  ...
# Subtest: planTargetTaskUpdate stamps the rewritten line last via injected stamper
ok 7 - planTargetTaskUpdate stamps the rewritten line last via injected stamper
  ---
  duration_ms: 0.369376
  ...
# Subtest: planTargetTaskUpdate without a stamper never stamps (identity default)
ok 8 - planTargetTaskUpdate without a stamper never stamps (identity default)
  ---
  duration_ms: 0.134206
  ...
# Subtest: planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
ok 9 - planTargetTaskUpdate stamp-only input stays unchanged and never calls the stamper
  ---
  duration_ms: 0.356872
  ...
# Subtest: planTargetTaskUpdate stamps a Next task that gains a block ID
ok 10 - planTargetTaskUpdate stamps a Next task that gains a block ID
  ---
  duration_ms: 0.527788
  ...
# Subtest: planTargetTaskUpdate tolerates a throwing stamper
ok 11 - planTargetTaskUpdate tolerates a throwing stamper
  ---
  duration_ms: 0.215682
  ...
# Subtest: Depends-On line recogniser covers the contract DP vectors
ok 12 - Depends-On line recogniser covers the contract DP vectors
  ---
  duration_ms: 0.434359
  ...
# Subtest: dedicated-link helpers reject Depends-On lines
ok 13 - dedicated-link helpers reject Depends-On lines
  ---
  duration_ms: 0.325852
  ...
# Subtest: Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
ok 14 - Ctrl+Shift+Enter on a Depends-On link is refused without deleting anything
  ---
  duration_ms: 0.36129
  ...
# Subtest: malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
ok 15 - malformed Depends-On lines refuse Ctrl+Shift+Enter instead of deleting the link token
  ---
  duration_ms: 0.123997
  ...
# Subtest: Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
ok 16 - Ctrl+Shift+Enter on a not-a-line Depends-On shape skips the dependency refusal
  ---
  duration_ms: 0.260578
  ...
# Subtest: Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
ok 17 - Ctrl+Shift+Enter on a malformed Depends-On line is refused without deleting anything
  ---
  duration_ms: 0.203328
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent
ok 18 - readPlanBudgetMeter keeps per-cap over flags independent
  ---
  duration_ms: 0.194611
  ...
# Subtest: readPlanBudgetMeter keeps per-cap over flags independent (mirror)
ok 19 - readPlanBudgetMeter keeps per-cap over flags independent (mirror)
  ---
  duration_ms: 0.105742
  ...
# Subtest: block-id-prompt freshness accessors degrade without ledger-tools
ok 20 - block-id-prompt freshness accessors degrade without ledger-tools
  ---
  duration_ms: 0.213187
  ...
# Subtest: block-id-prompt refuses Pomodoro ledger lines before calling a stamper
ok 21 - block-id-prompt refuses Pomodoro ledger lines before calling a stamper
  ---
  duration_ms: 0.192518
  ...
# Subtest: K1 absent: no keeps means 0 with no lints
ok 22 - K1 absent: no keeps means 0 with no lints
  ---
  duration_ms: 2.250868
  ...
# Subtest: K8 misplaced: keeps inside the Tasks suffix reads with a lint
ok 23 - K8 misplaced: keeps inside the Tasks suffix reads with a lint
  ---
  duration_ms: 0.390906
  ...
# Subtest: K9 duplicates and invalid values: first valid wins, else 0
ok 24 - K9 duplicates and invalid values: first valid wins, else 0
  ---
  duration_ms: 0.619072
  ...
# Subtest: K10 ceiling and NEW: 999 reads, never-confirmed reads 0
ok 25 - K10 ceiling and NEW: 999 reads, never-confirmed reads 0
  ---
  duration_ms: 0.197617
  ...
# Subtest: K13 exact keys: near-miss keys are not keeps; parens read
ok 26 - K13 exact keys: near-miss keys are not keeps; parens read
  ---
  duration_ms: 0.190984
  ...
# Subtest: keeps value parser accepts only decimal 1-999
ok 27 - keeps value parser accepts only decimal 1-999
  ---
  duration_ms: 0.170285
  ...
# Subtest: K2 first valid canonical: uncounted keep preserves and repairs
ok 28 - K2 first valid canonical: uncounted keep preserves and repairs
  ---
  duration_ms: 0.824314
  ...
# Subtest: K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
ok 29 - K3 refresh/keeps order canonicalizes to fresh, refresh, keeps
  ---
  duration_ms: 0.522478
  ...
# Subtest: K4 same-day preserve noop: canonical kept line is byte-identical
ok 30 - K4 same-day preserve noop: canonical kept line is byte-identical
  ---
  duration_ms: 0.4342
  ...
# Subtest: K5 generic stamp clears, even same-day
ok 31 - K5 generic stamp clears, even same-day
  ---
  duration_ms: 0.462222
  ...
# Subtest: K6 set-refresh clears keeps
ok 32 - K6 set-refresh clears keeps
  ---
  duration_ms: 0.269995
  ...
# Subtest: K7 stale stamp clears keeps
ok 33 - K7 stale stamp clears keeps
  ---
  duration_ms: 0.171667
  ...
# Subtest: K8b misplaced keeps repaired to canonical order by a keep
ok 34 - K8b misplaced keeps repaired to canonical order by a keep
  ---
  duration_ms: 0.205762
  ...
# Subtest: K11 refusals preserve: closed and recurring lines never write
ok 35 - K11 refusals preserve: closed and recurring lines never write
  ---
  duration_ms: 0.248665
  ...
# Subtest: counted keep increments a stale streak once in the same write
ok 36 - counted keep increments a stale streak once in the same write
  ---
  duration_ms: 0.200363
  ...
# Subtest: first counted keep on a streakless due task writes keeps 1
ok 37 - first counted keep on a streakless due task writes keeps 1
  ---
  duration_ms: 0.227505
  ...
# Subtest: counted keep saturates at 999 and never wraps
ok 38 - counted keep saturates at 999 and never wraps
  ---
  duration_ms: 0.201144
  ...
# Subtest: counted keep needs a valid prior fresh before today
ok 39 - counted keep needs a valid prior fresh before today
  ---
  duration_ms: 0.352022
  ...
# Subtest: counted keep repairs malformed and duplicate placement
ok 40 - counted keep repairs malformed and duplicate placement
  ---
  duration_ms: 0.277139
  ...
# Subtest: uncounted keep preserves the valid value while canonicalizing
ok 41 - uncounted keep preserves the valid value while canonicalizing
  ---
  duration_ms: 0.198069
  ...
# Subtest: UB13 keep on an unblock TICKLER preserves the streak and skips the card
ok 42 - UB13 keep on an unblock TICKLER preserves the streak and skips the card
  ---
  duration_ms: 0.781222
  ...
# Subtest: a scheduled tickler still counts when schedule wins an unblock tie
ok 43 - a scheduled tickler still counts when schedule wins an unblock tie
  ---
  duration_ms: 0.276348
  ...
# Subtest: decay normalization: absent, null, true, and {} enable with 3
ok 44 - decay normalization: absent, null, true, and {} enable with 3
  ---
  duration_ms: 0.608332
  ...
# Subtest: decay false counts and displays but never asks
ok 45 - decay false counts and displays but never asks
  ---
  duration_ms: 0.103888
  ...
# Subtest: decay keeps 0 and fixed entry normalize
ok 46 - decay keeps 0 and fixed entry normalize
  ---
  duration_ms: 0.116172
  ...
# Subtest: invalid decay shapes fail the freshness config contract
ok 47 - invalid decay shapes fail the freshness config contract
  ---
  duration_ms: 0.294923
  ...
# Subtest: B: at-limit Ready due rows decide on every local day
ok 48 - B: at-limit Ready due rows decide on every local day
  ---
  duration_ms: 0.476069
  ...
# Subtest: D1 early date: an at-limit Ready due row decides
ok 49 - D1 early date: an at-limit Ready due row decides
  ---
  duration_ms: 0.111152
  ...
# Subtest: D2 at limit decides; D3 below limit stamps without a card
ok 50 - D2 at limit decides; D3 below limit stamps without a card
  ---
  duration_ms: 0.119568
  ...
# Subtest: D4 tickler counts as due; D5 NEW never decides
ok 51 - D4 tickler counts as due; D5 NEW never decides
  ---
  duration_ms: 0.138875
  ...
# Subtest: D6 zero limit asks on every due Ready re-confirmation
ok 52 - D6 zero limit asks on every due Ready re-confirmation
  ---
  duration_ms: 0.091114
  ...
# Subtest: D7 off never asks; D8 lane rows never decide
ok 53 - D7 off never asks; D8 lane rows never decide
  ---
  duration_ms: 0.080964
  ...
# Subtest: evaluator, queue, and counts carry keeps and decide
ok 54 - evaluator, queue, and counts carry keeps and decide
  ---
  duration_ms: 1.045506
  ...
# Subtest: no keeps: the existing mark is unchanged
ok 55 - no keeps: the existing mark is unchanged
  ---
  duration_ms: 0.862386
  ...
# Subtest: aging with two keeps: faint pips plus a counting-only line
ok 56 - aging with two keeps: faint pips plus a counting-only line
  ---
  duration_ms: 0.24622
  ...
# Subtest: confirmed today with two keeps: check glyph, faint dots
ok 57 - confirmed today with two keeps: check glyph, faint dots
  ---
  duration_ms: 0.190865
  ...
# Subtest: due below threshold: orange capsule keeps its glyph, adds dots
ok 58 - due below threshold: orange capsule keeps its glyph, adds dots
  ---
  duration_ms: 0.200072
  ...
# Subtest: resting marks show historical dots quietly and never decide
ok 59 - resting marks show historical dots quietly and never decide
  ---
  duration_ms: 0.296646
  ...
# Subtest: active decision due: data stays truthful, leaf stays gated
ok 60 - active decision due: data stays truthful, leaf stays gated
  ---
  duration_ms: 0.201836
  ...
# Subtest: dot caps follow the threshold with +N overflow
ok 61 - dot caps follow the threshold with +N overflow
  ---
  duration_ms: 0.507279
  ...
# Subtest: keeps tooltip wording: singulars, zero threshold, off state
ok 62 - keeps tooltip wording: singulars, zero threshold, off state
  ---
  duration_ms: 0.096935
  ...
# Subtest: noncanonical keeps never fold but keep their repair pill
ok 63 - noncanonical keeps never fold but keep their repair pill
  ---
  duration_ms: 0.268693
  ...
# Subtest: quoted lines fold; rendered fragments fold without task checks
ok 64 - quoted lines fold; rendered fragments fold without task checks
  ---
  duration_ms: 0.190744
  ...
# Subtest: unresolved marks show the line's own pips quietly and never decide
ok 65 - unresolved marks show the line's own pips quietly and never decide
  ---
  duration_ms: 0.192427
  ...
# Subtest: consensus sees count and decision eligibility: ambiguity stays neutral
ok 66 - consensus sees count and decision eligibility: ambiguity stays neutral
  ---
  duration_ms: 0.399122
  ...
# Subtest: pips render as one aria-hidden span with the count in the label
ok 67 - pips render as one aria-hidden span with the count in the label
  ---
  duration_ms: 0.896592
  ...
# Subtest: placement vectors P1-P11, P14-P16, P18 stamp canonically
ok 68 - placement vectors P1-P11, P14-P16, P18 stamp canonically
  ---
  duration_ms: 3.270295
  ...
# Subtest: P12 set and clear refresh stamps alongside
ok 69 - P12 set and clear refresh stamps alongside
  ---
  duration_ms: 0.260147
  ...
# Subtest: P13 recurring and P17 done tasks are refused unchanged
ok 70 - P13 recurring and P17 done tasks are refused unchanged
  ---
  duration_ms: 0.20398
  ...
# Subtest: Pomodoro ledger rows are refused byte-for-byte by every fresh writer
ok 71 - Pomodoro ledger rows are refused byte-for-byte by every fresh writer
  ---
  duration_ms: 0.44998
  ...
# Subtest: a time range later in task prose remains eligible for freshness
ok 72 - a time range later in task prose remains eligible for freshness
  ---
  duration_ms: 0.15172
  ...
# Subtest: U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
ok 73 - U1-U2 stamp vectors clear unblocked while preserving keeps in seed mode
  ---
  duration_ms: 0.614564
  ...
# Subtest: reader reports misplaced and duplicate fields
ok 74 - reader reports misplaced and duplicate fields
  ---
  duration_ms: 0.266278
  ...
# Subtest: freshness delegation guards reject Pomodoro ledger rows before injected writers
ok 75 - freshness delegation guards reject Pomodoro ledger rows before injected writers
  ---
  duration_ms: 3.137922
  ...
# Subtest: refresh picker refuses a legacy Pomodoro heading before its refresher runs
ok 76 - refresh picker refuses a legacy Pomodoro heading before its refresher runs
  ---
  duration_ms: 0.484987
  ...
# Subtest: lane commit stamps an open Ready task
ok 77 - lane commit stamps an open Ready task
  ---
  duration_ms: 1.548016
  ...
# Subtest: lane release stamps an open Next task
ok 78 - lane release stamps an open Next task
  ---
  duration_ms: 0.370638
  ...
# Subtest: lane without a stamper leaves lines as they were
ok 79 - lane without a stamper leaves lines as they were
  ---
  duration_ms: 0.300043
  ...
# Subtest: counted property set stamps every rewritten open task
ok 80 - counted property set stamps every rewritten open task
  ---
  duration_ms: 2.071406
  ...
# Subtest: counted delete-property stamps the rewritten task
ok 81 - counted delete-property stamps the rewritten task
  ---
  duration_ms: 0.542987
  ...
# Subtest: stamp lands before the suffix after a priority edit on a stamped line
ok 82 - stamp lands before the suffix after a priority edit on a stamped line
  ---
  duration_ms: 0.49763
  ...
# Subtest: recurring tasks are never stamped
ok 83 - recurring tasks are never stamped
  ---
  duration_ms: 0.451372
  ...
# Subtest: cancel never stamps
ok 84 - cancel never stamps
  ---
  duration_ms: 1.305353
  ...
# Subtest: fresh and refresh never go through the end-append writers
ok 85 - fresh and refresh never go through the end-append writers
  ---
  duration_ms: 0.244647
  ...
# Subtest: counted dependency edit stamps the rewritten parent
ok 86 - counted dependency edit stamps the rewritten parent
  ---
  duration_ms: 4.662353
  ...
# Subtest: moved tasks are stamped at their destination
ok 87 - moved tasks are stamped at their destination
  ---
  duration_ms: 2.57119
  ...
# Subtest: move without a stamper leaves lines as they were
ok 88 - move without a stamper leaves lines as they were
  ---
  duration_ms: 0.504834
  ...
# Subtest: refresh row shows the effective interval in task mode
ok 89 - refresh row shows the effective interval in task mode
  ---
  duration_ms: 0.71757
  ...
# Subtest: refresh row hides without the api and on closed tasks
ok 90 - refresh row hides without the api and on closed tasks
  ---
  duration_ms: 0.117485
  ...
# Subtest: refresh row covers counted and link modes, including mixed
ok 91 - refresh row covers counted and link modes, including mixed
  ---
  duration_ms: 0.291867
  ...
# Subtest: refresh value items offer presets and use default
ok 92 - refresh value items offer presets and use default
  ---
  duration_ms: 0.655823
  ...
# Subtest: setRefreshLine stamps and sets or clears the interval
ok 93 - setRefreshLine stamps and sets or clears the interval
  ---
  duration_ms: 0.311825
  ...
# Subtest: cycler freshness: local-fallback rewrite stamps last via injected stamper
ok 94 - cycler freshness: local-fallback rewrite stamps last via injected stamper
  ---
  duration_ms: 1.529541
  ...
# Subtest: cycler freshness: rewrites without a stamper are unchanged (identity default)
ok 95 - cycler freshness: rewrites without a stamper are unchanged (identity default)
  ---
  duration_ms: 0.320442
  ...
# Subtest: cycler freshness: a throwing stamper leaves the rewritten line intact
ok 96 - cycler freshness: a throwing stamper leaves the rewritten line intact
  ---
  duration_ms: 0.209079
  ...
# Subtest: cycler line guard skips Pomodoro signatures before injected stampers
ok 97 - cycler line guard skips Pomodoro signatures before injected stampers
  ---
  duration_ms: 0.266909
  ...
# Subtest: cycler skips legacy Pomodoro headlines in local and Tasks-command writes
ok 98 - cycler skips legacy Pomodoro headlines in local and Tasks-command writes
  ---
  duration_ms: 1.330771
  ...
# Subtest: cycler freshness: transcluded rewrite stamps last via injected stamper
ok 99 - cycler freshness: transcluded rewrite stamps last via injected stamper
  ---
  duration_ms: 0.165466
  ...
# Subtest: cycler freshness: cycling a plain line stamps through the follow-up edit
ok 100 - cycler freshness: cycling a plain line stamps through the follow-up edit
  ---
  duration_ms: 0.305043
  ...
# Subtest: cycler freshness: Tasks-command rewrite with the expected status is stamped
ok 101 - cycler freshness: Tasks-command rewrite with the expected status is stamped
  ---
  duration_ms: 0.306886
  ...
# Subtest: cycler freshness: Tasks command that inserts a line never stamps
ok 102 - cycler freshness: Tasks command that inserts a line never stamps
  ---
  duration_ms: 0.542557
  ...
# Subtest: cycler freshness: Tasks command that deletes the line never stamps the next task
ok 103 - cycler freshness: Tasks command that deletes the line never stamps the next task
  ---
  duration_ms: 0.611437
  ...
# Subtest: cycler freshness: Tasks command that leaves a different status never stamps
ok 104 - cycler freshness: Tasks command that leaves a different status never stamps
  ---
  duration_ms: 0.342143
  ...
# Subtest: cycler freshness: cycling without ledger-tools writes no stamp
ok 105 - cycler freshness: cycling without ledger-tools writes no stamp
  ---
  duration_ms: 0.248444
  ...
# Subtest: cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
ok 106 - cycler freshness: getFreshnessStampLine degrades when ledger-tools is missing or old
  ---
  duration_ms: 0.170876
  ...
# Subtest: selected Done Pomodoro transclusion reopens only its cross-file root
ok 107 - selected Done Pomodoro transclusion reopens only its cross-file root
  ---
  duration_ms: 5.787893
  ...
# Subtest: selected same-file Done target reopens root-only in the live editor
ok 108 - selected same-file Done target reopens root-only in the live editor
  ---
  duration_ms: 1.181646
  ...
# Subtest: selected retired link reopens its root and restores the historical occurrence
ok 109 - selected retired link reopens its root and restores the historical occurrence
  ---
  duration_ms: 0.995702
  ...
# Subtest: incomplete selected Pomodoro transclusion still closes recursively
ok 110 - incomplete selected Pomodoro transclusion still closes recursively
  ---
  duration_ms: 1.821478
  ...
# Subtest: Done Pomodoro reopens direct roots and clears only its block-link markers
ok 111 - Done Pomodoro reopens direct roots and clears only its block-link markers
  ---
  duration_ms: 2.901841
  ...
# Subtest: reopening timed, placeholder, and legacy ledger rows never stamps the headline
ok 112 - reopening timed, placeholder, and legacy ledger rows never stamps the headline
  ---
  duration_ms: 2.732498
  ...
# Subtest: Done Pomodoro reopen restores its own block reference after reopening direct roots
ok 113 - Done Pomodoro reopen restores its own block reference after reopening direct roots
  ---
  duration_ms: 1.303559
  ...
# Subtest: Done Pomodoro markers remain when the Todo transition does not occur
ok 114 - Done Pomodoro markers remain when the Todo transition does not occur
  ---
  duration_ms: 0.231402
  ...
# Subtest: registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
ok 115 - registered Ctrl+Enter completes an open Pomodoro from every non-selected-embed child shape
  ---
  duration_ms: 11.406171
  ...
# Subtest: registered Ctrl+Enter immediately recovers a same-file dependent
ok 116 - registered Ctrl+Enter immediately recovers a same-file dependent
  ---
  duration_ms: 9.949179
  ...
# Subtest: registered Ctrl+Enter immediately recovers a cross-file dependent
ok 117 - registered Ctrl+Enter immediately recovers a cross-file dependent
  ---
  duration_ms: 2.32027
  ...
# Subtest: child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
ok 118 - child-line Ctrl+Enter produces the same rollover and cursor target as parent completion
  ---
  duration_ms: 2.287157
  ...
# Subtest: Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
ok 119 - Ctrl+Enter preserves cross-file move-only targets while ordinary duplicates still start
  ---
  duration_ms: 1.29846
  ...
# Subtest: selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
ok 120 - selected embedded Pomodoro children keep recursive close and root-only reopen dispatch
  ---
  duration_ms: 2.6392
  ...
# Subtest: selected unresolved or excluded embedded children are consumed as no-ops
ok 121 - selected unresolved or excluded embedded children are consumed as no-ops
  ---
  duration_ms: 1.161488
  ...
# Subtest: Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
ok 122 - Ctrl+Enter behavior stays generic outside open Pomodoro child ranges
  ---
  duration_ms: 2.512307
  ...
1..122
# tests 122
# suites 0
# pass 122
# fail 0
# cancelled 0
# skipped 0
# todo 0
# duration_ms 195.799513
   Compiling proc-macro2 v1.0.106
   Compiling unicode-ident v1.0.24
   Compiling quote v1.0.45
   Compiling typenum v1.20.1
   Compiling version_check v0.9.5
   Compiling cfg-if v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling find-msvc-tools v0.1.9
   Compiling allocator-api2 v0.2.21
   Compiling equivalent v1.0.2
   Compiling memchr v2.8.1
   Compiling foldhash v0.2.0
   Compiling autocfg v1.5.1
   Compiling litemap v0.8.3
   Compiling writeable v0.6.4
   Compiling libc v0.2.186
   Compiling crc32fast v1.5.0
   Compiling serde_core v1.0.228
   Compiling icu_normalizer_data v2.3.0
   Compiling bitflags v2.12.1
   Compiling utf8_iter v1.0.4
   Compiling simd-adler32 v0.3.9
   Compiling icu_properties_data v2.3.0
   Compiling adler2 v2.0.1
   Compiling getrandom v0.4.2
   Compiling rand_core v0.10.1
   Compiling smallvec v1.15.2
   Compiling utf8parse v0.2.2
   Compiling pkg-config v0.3.33
   Compiling cpufeatures v0.3.0
   Compiling is_terminal_polyfill v1.70.2
   Compiling colorchoice v1.0.5
   Compiling anstyle-query v1.1.5
   Compiling vcpkg v0.2.15
   Compiling anstyle v1.0.14
   Compiling tinyvec_macros v0.1.1
   Compiling serde v1.0.228
   Compiling rustix v1.1.5
   Compiling cpufeatures v0.2.17
   Compiling thiserror v2.0.18
   Compiling weezl v0.1.12
   Compiling strsim v0.11.1
   Compiling itoa v1.0.18
   Compiling clap_lex v1.1.0
   Compiling siphasher v1.0.4
   Compiling zmij v1.0.21
   Compiling powerfmt v0.2.0
   Compiling chrono-tz v0.10.4
   Compiling deranged v0.5.8
   Compiling iana-time-zone v0.1.65
   Compiling unicode-bidi v0.3.18
   Compiling time-core v0.1.9
   Compiling byteorder-lite v0.1.0
   Compiling unicode-properties v0.1.4
   Compiling pxfm v0.1.30
   Compiling color_quant v1.1.0
   Compiling bytecount v0.6.9
   Compiling const-oid v0.10.2
   Compiling serde_json v1.0.150
   Compiling quick-error v2.0.1
   Compiling regex-syntax v0.8.10
   Compiling percent-encoding v2.3.2
   Compiling zune-core v0.5.3
   Compiling num-conv v0.2.2
   Compiling linux-raw-sys v0.12.1
   Compiling base64 v0.22.1
   Compiling ryu v1.0.23
   Compiling fastrand v2.5.0
   Compiling fallible-streaming-iterator v0.1.9
   Compiling bytemuck v1.25.2
   Compiling cc v1.2.63
   Compiling rangemap v1.7.1
   Compiling ttf-parser v0.25.1
   Compiling once_cell v1.21.4
   Compiling generic-array v0.14.7
   Compiling is_executable v1.0.6
   Compiling fallible-iterator v0.3.0
   Compiling encoding_rs v0.8.35
   Compiling unsafe-libyaml v0.2.11
   Compiling image-webp v0.2.4
   Compiling log v0.4.30
   Compiling similar v2.7.0
   Compiling nom v8.0.0
   Compiling aho-corasick v1.1.4
   Compiling quick-xml v0.41.0
   Compiling hex v0.4.3
   Compiling hybrid-array v0.4.12
   Compiling num-traits v0.2.19
   Compiling zune-jpeg v0.5.15
   Compiling hashbrown v0.17.1
   Compiling miniz_oxide v0.8.9
   Compiling fdeflate v0.3.7
   Compiling form_urlencoded v1.2.2
   Compiling anstyle-parse v1.0.0
   Compiling tinyvec v1.11.0
   Compiling phf_shared v0.12.1
   Compiling chacha20 v0.10.2
   Compiling gif v0.14.2
   Compiling time v0.3.53
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
   Compiling block-buffer v0.12.0
   Compiling crypto-common v0.2.2
   Compiling fs2 v0.4.3
   Compiling anstream v1.0.0
   Compiling phf v0.12.1
   Compiling indexmap v2.14.0
   Compiling hashlink v0.12.1
   Compiling unicode-normalization v0.1.25
   Compiling flate2 v1.1.9
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling clap_builder v4.6.7
   Compiling moxcms v0.8.1
   Compiling chrono v0.4.44
   Compiling rand v0.10.1
   Compiling digest v0.11.3
   Compiling nom_locate v5.0.0
   Compiling digest v0.10.7
   Compiling inout v0.1.4
   Compiling regex-automata v0.4.14
   Compiling tempfile v3.27.0
   Compiling stringprep v0.1.5
   Compiling png v0.18.1
   Compiling sha2 v0.11.0
   Compiling cipher v0.4.4
   Compiling sha2 v0.10.9
   Compiling md-5 v0.10.6
   Compiling syn v3.0.6
   Compiling syn v2.0.117
   Compiling cbc v0.1.2
   Compiling aes v0.8.4
   Compiling ecb v0.1.2
   Compiling clap v4.6.7
   Compiling clap_complete v4.6.11
   Compiling serde_derive v1.0.228
   Compiling thiserror-impl v2.0.18
   Compiling regex v1.12.3
   Compiling synstructure v0.14.0
   Compiling zerovec-derive v0.11.6
   Compiling displaydoc v0.2.7
   Compiling lopdf v0.40.0
   Compiling zerofrom-derive v0.1.8
   Compiling yoke-derive v0.8.4
   Compiling rusqlite v0.40.1
   Compiling image v0.25.10
   Compiling zerofrom v0.1.8
   Compiling yoke v0.8.3
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling serde_yaml v0.9.34+deprecated
   Compiling plist v1.10.0
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling icu_collections v2.3.0
   Compiling icu_locale_core v2.3.0
   Compiling icu_provider v2.3.1
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling rquickjs-core v0.12.1
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling rquickjs v0.12.1
   Compiling url v2.5.8
   Compiling bob-obsidian v0.3.1 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_11)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 1m 29s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws11-261026_133551/build/debug/deps/bob_cli-7dc5ace38803397f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 3624 filtered out; finished in 0.00s

succeeded  exit=0  duration=90301ms

