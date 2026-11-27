# Chat History - ace-run (bob-cli-qi.land--mon-d)

- **TIMESTAMP:** 2026-11-26 21:26:39 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-qi.land--mon-d

## Prompt

sase monitor start --command "bash -lc 'cd /home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/linked/bob-plugins && git diff --check && node --check scripts/obsidian-frontmatter-takeover-e2e.cjs && npm run build:check && node --test scripts/test-ledger-tools-property-card-*.cjs scripts/test-ledger-tools-home-card-*.cjs scripts/test-ledger-tools-property-editor-*.cjs'" --reason 'Recheck generated plugin bundle and focused card suites after the confirmed live-navigation event-order defect'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))

> bob-plugins@0.1.0 build:check
> node scripts/build-plugins.mjs --check

  checked   block-id-prompt
  checked   bob-articles
  checked   bob-chips
  checked   bob-command-mode
  checked   bob-emoji
  checked   bob-ledger-tools
  checked   bob-mail
  checked   bob-navigation-hotkeys
  checked   task-status-cycler
TAP version 13
# Subtest: area card uses the field tile, Settings, chips, Ready, and a collapsible summary
ok 1 - area card uses the field tile, Settings, chips, Ready, and a collapsible summary
  ---
  duration_ms: 15.710224
  ...
# Subtest: project card uses the pennant tile, ancestry pip, ROOT, and a visible lifecycle
ok 2 - project card uses the pennant tile, ancestry pip, ROOT, and a visible lifecycle
  ---
  duration_ms: 5.29966
  ...
# Subtest: collapsed cards keep kicker, title, and lifecycle while hiding summary and chips
ok 3 - collapsed cards keep kicker, title, and lifecycle while hiding summary and chips
  ---
  duration_ms: 2.729152
  ...
# Subtest: terminal projects outline the pennant and omit the chip row
ok 4 - terminal projects outline the pennant and omit the chip row
  ---
  duration_ms: 2.064733
  ...
# Subtest: missing ^prj, shadowed clock, and unknown Ready stay truthful in the DOM
ok 5 - missing ^prj, shadowed clock, and unknown Ready stay truthful in the DOM
  ---
  duration_ms: 3.339475
  ...
# Subtest: builder fails closed and CSS keeps field, pennant, pip, and collapse tokens
ok 6 - builder fails closed and CSS keeps field, pennant, pip, and collapse tokens
  ---
  duration_ms: 3.580896
  ...
# Subtest: project collapse is a compact fold with a live keycap
ok 7 - project collapse is a compact fold with a live keycap
  ---
  duration_ms: 1.777002
  ...
# Subtest: host registers one shared adapter with desktop gates and no embed display
ok 8 - host registers one shared adapter with desktop gates and no embed display
  ---
  duration_ms: 1.969992
  ...
# Subtest: denied contexts never show the card
ok 9 - denied contexts never show the card
  ---
  duration_ms: 1.096584
  ...
# Subtest: the same eligibility decision drives the mount
ok 10 - the same eligibility decision drives the mount
  ---
  duration_ms: 1.114588
  ...
# Subtest: modifier-aware links open tabs and splits
ok 11 - modifier-aware links open tabs and splits
  ---
  duration_ms: 0.278011
  ...
# Subtest: collapsed cards keep kicker, title, lifecycle, and foot while summary and chips hide
ok 12 - collapsed cards keep kicker, title, lifecycle, and foot while summary and chips hide
  ---
  duration_ms: 8.890122
  ...
# Subtest: collapse state is a per-normalized-path session map shared across panes
ok 13 - collapse state is a per-normalized-path session map shared across panes
  ---
  duration_ms: 1.674537
  ...
# Subtest: home setup registers area and project folds on one toggle
ok 14 - home setup registers area and project folds on one toggle
  ---
  duration_ms: 1.067118
  ...
# Subtest: where-marks stay truthful and housekeeping folds into managed
ok 15 - where-marks stay truthful and housekeeping folds into managed
  ---
  duration_ms: 1.088578
  ...
# Subtest: chip handoff uses one adapter callback and renders inert text without the editor
ok 16 - chip handoff uses one adapter callback and renders inert text without the editor
  ---
  duration_ms: 1.82261
  ...
# Subtest: title adoption never consumes ^prj and the source task offsets survive the build
ok 17 - title adoption never consumes ^prj and the source task offsets survive the build
  ---
  duration_ms: 1.137402
  ...
# Subtest: painting introduces no writes and no card-triggered subprocesses
ok 18 - painting introduces no writes and no card-triggered subprocesses
  ---
  duration_ms: 2.954241
  ...
# Subtest: visible body navigation skips frontmatter, its separator, and an owned title
ok 19 - visible body navigation skips frontmatter, its separator, and an owned title
  ---
  duration_ms: 0.327966
  ...
# Subtest: home-card gg and Up stop at visible body text without swallowing insert-mode g
ok 20 - home-card gg and Up stop at visible body text without swallowing insert-mode g
  ---
  duration_ms: 0.713733
  ...
# Subtest: inbox route API is the only inbox authority
ok 21 - inbox route API is the only inbox authority
  ---
  duration_ms: 0.448907
  ...
# Subtest: theme hue reads pomodoroThemeHueFor and api.themes.hueFor, never taskThemeOf
ok 22 - theme hue reads pomodoroThemeHueFor and api.themes.hueFor, never taskThemeOf
  ---
  duration_ms: 0.519312
  ...
# Subtest: Ready requires a live snapshot before forNote
ok 23 - Ready requires a live snapshot before forNote
  ---
  duration_ms: 0.503591
  ...
# Subtest: failed mount removes the card and restores the native title
ok 24 - failed mount removes the card and restores the native title
  ---
  duration_ms: 1.49811
  ...
# Subtest: editor availability is part of the paint signature
ok 25 - editor availability is part of the paint signature
  ---
  duration_ms: 0.448526
  ...
# Subtest: source cache drops on metadata, rename, and delete, then delayed reads refresh
ok 26 - source cache drops on metadata, rename, and delete, then delayed reads refresh
  ---
  duration_ms: 19.603046
  ...
# Subtest: fallback rows claim only values the connected card represents
ok 27 - fallback rows claim only values the connected card represents
  ---
  duration_ms: 1.853749
  ...
# Subtest: whole ownership suppresses the row fallback; loss restores native and rows
ok 28 - whole ownership suppresses the row fallback; loss restores native and rows
  ---
  duration_ms: 8.459031
  ...
# Subtest: contract codes file under the stable settings-contract ids
ok 29 - contract codes file under the stable settings-contract ids
  ---
  duration_ms: 2.527928
  ...
# Subtest: issue normalization keeps code and message rows and drops the rest
ok 30 - issue normalization keeps code and message rows and drops the rest
  ---
  duration_ms: 1.762154
  ...
# Subtest: a missing, stale, or entry-less snapshot patches nothing, never zero
ok 31 - a missing, stale, or entry-less snapshot patches nothing, never zero
  ---
  duration_ms: 15.980383
  ...
# Subtest: dependency-blocked projects gain at most two waits-on links
ok 32 - dependency-blocked projects gain at most two waits-on links
  ---
  duration_ms: 1.807641
  ...
# Subtest: same-note dependency targets stay text while other notes link
ok 33 - same-note dependency targets stay text while other notes link
  ---
  duration_ms: 1.002724
  ...
# Subtest: inherited blocking names the nearest blocked ancestor
ok 34 - inherited blocking names the nearest blocked ancestor
  ---
  duration_ms: 0.923123
  ...
# Subtest: the ancestor walk stops at cycles and unblocked chains
ok 35 - the ancestor walk stops at cycles and unblocked chains
  ---
  duration_ms: 0.928563
  ...
# Subtest: done projects without a line date gain the report close date
ok 36 - done projects without a line date gain the report close date
  ---
  duration_ms: 1.086875
  ...
# Subtest: a line date always beats the report close date
ok 37 - a line date always beats the report close date
  ---
  duration_ms: 0.938532
  ...
# Subtest: reason links render as anchors and navigate like crumbs
ok 38 - reason links render as anchors and navigate like crumbs
  ---
  duration_ms: 5.363579
  ...
# Subtest: reason links stay text when no opener is present
ok 39 - reason links stay text when no opener is present
  ---
  duration_ms: 1.41438
  ...
# Subtest: open and today readouts paint from a present snapshot only
ok 40 - open and today readouts paint from a present snapshot only
  ---
  duration_ms: 1.758959
  ...
# Subtest: areas show direct today only and never count subtrees
ok 41 - areas show direct today only and never count subtrees
  ---
  duration_ms: 1.967838
  ...
# Subtest: terminal projects keep no report readout but gain an undated close date
ok 42 - terminal projects keep no report readout but gain an undated close date
  ---
  duration_ms: 1.433818
  ...
# Subtest: contract issues ride the patch with the first affected setting
ok 43 - contract issues ride the patch with the first affected setting
  ---
  duration_ms: 0.588965
  ...
# Subtest: foot lint counts contract issues and names the first setting
ok 44 - foot lint counts contract issues and names the first setting
  ---
  duration_ms: 0.605546
  ...
# Subtest: the goal line locator follows the recognized ^prj task only
ok 45 - the goal line locator follows the recognized ^prj task only
  ---
  duration_ms: 1.132453
  ...
# Subtest: the Reading lookup finds the goal row before any H2 and skips the rest
ok 46 - the Reading lookup finds the goal row before any H2 and skips the rest
  ---
  duration_ms: 1.444638
  ...
# Subtest: the Reading lookup skips nested tasks
ok 47 - the Reading lookup skips nested tasks
  ---
  duration_ms: 0.520774
  ...
# Subtest: eligibility is typed homes only and excludes area/project type notes, archives, and templates
ok 48 - eligibility is typed homes only and excludes area/project type notes, archives, and templates
  ---
  duration_ms: 4.015496
  ...
# Subtest: title prefers the first-body H1, then alias, then the stem verbatim
ok 49 - title prefers the first-body H1, then alias, then the stem verbatim
  ---
  duration_ms: 10.061489
  ...
# Subtest: home title recognizer stops before a following ^prj line
ok 50 - home title recognizer stops before a following ^prj line
  ---
  duration_ms: 0.433367
  ...
# Subtest: ancestry omits the area sentinel and self, collapses the middle, and never invents links
ok 51 - ancestry omits the area sentinel and self, collapses the middle, and never invents links
  ---
  duration_ms: 3.788073
  ...
# Subtest: pending source defers lifecycle and chips so WIP never flickers
ok 52 - pending source defers lifecycle and chips so WIP never flickers
  ---
  duration_ms: 0.446733
  ...
# Subtest: project lifecycle covers WIP, schedule boundaries, blocked, done, canceled, and missing
ok 53 - project lifecycle covers WIP, schedule boundaries, blocked, done, canceled, and missing
  ---
  duration_ms: 5.360255
  ...
# Subtest: authored chips keep order, false clock, type off, and legacy theme, and ignore unauthored keys
ok 54 - authored chips keep order, false clock, type off, and legacy theme, and ignore unauthored keys
  ---
  duration_ms: 2.808051
  ...
# Subtest: Ready omits unknown data, keeps cap provenance, and uses room/full/crowded/exempt ink
ok 55 - Ready omits unknown data, keeps cap provenance, and uses room/full/crowded/exempt ink
  ---
  duration_ms: 1.324649
  ...
# Subtest: material, inbox, root, summary, created, and managed grouping stay local
ok 56 - material, inbox, root, summary, created, and managed grouping stay local
  ---
  duration_ms: 1.054373
  ...
# Subtest: nested ^prj tasks never become the project lifecycle
ok 57 - nested ^prj tasks never become the project lifecycle
  ---
  duration_ms: 0.74403
  ...
# Subtest: invalid authored policy shapes stay out of chips and do not claim where-marks
ok 58 - invalid authored policy shapes stay out of chips and do not claim where-marks
  ---
  duration_ms: 1.418709
  ...
# Subtest: live source policy beats stale cached frontmatter and never paints cache-only chips
ok 59 - live source policy beats stale cached frontmatter and never paints cache-only chips
  ---
  duration_ms: 0.610826
  ...
# Subtest: the top ancestor crumb pip uses the ancestor hue, not the leaf override
ok 60 - the top ancestor crumb pip uses the ancestor hue, not the leaf override
  ---
  duration_ms: 0.747146
  ...
# Subtest: created formatting follows the card species and represented day
ok 61 - created formatting follows the card species and represented day
  ---
  duration_ms: 28.235781
  ...
# Subtest: date-only values never invent midnight and remain calendar dates
ok 62 - date-only values never invent midnight and remain calendar dates
  ---
  duration_ms: 2.834792
  ...
# Subtest: space-separated midnight timestamps and supported offsets parse
ok 63 - space-separated midnight timestamps and supported offsets parse
  ---
  duration_ms: 4.329094
  ...
# Subtest: YAML Date objects use source syntax to distinguish dates from timestamps
ok 64 - YAML Date objects use source syntax to distinguish dates from timestamps
  ---
  duration_ms: 1.542996
  ...
# Subtest: impossible dates are invalid and preserve their raw source
ok 65 - impossible dates are invalid and preserve their raw source
  ---
  duration_ms: 0.794146
  ...
# Subtest: offset timestamps render in explicit viewer zones across date boundaries
ok 66 - offset timestamps render in explicit viewer zones across date boundaries
  ---
  duration_ms: 2.046227
  ...
# Subtest: fold state follows species defaults and health-stamped choices
ok 67 - fold state follows species defaults and health-stamped choices
  ---
  duration_ms: 2.850061
  ...
# Subtest: fold target is connected, visible, path-matched, registered, and view-local
ok 68 - fold target is connected, visible, path-matched, registered, and view-local
  ---
  duration_ms: 2.296425
  ...
# Subtest: fold row has a live body id, unique mount ids, attention, and a conditional keycap
ok 69 - fold row has a live body id, unique mount ids, attention, and a conditional keycap
  ---
  duration_ms: 1.135227
  ...
# Subtest: the details command queues a pending reveal that the next open row consumes
ok 70 - the details command queues a pending reveal that the next open row consumes
  ---
  duration_ms: 0.70698
  ...
# Subtest: fold keycap appears only for desktop Live Preview Vim
ok 71 - fold keycap appears only for desktop Live Preview Vim
  ---
  duration_ms: 0.271017
  ...
# Subtest: stored boolean collapse maps to an open/closed choice
ok 72 - stored boolean collapse maps to an open/closed choice
  ---
  duration_ms: 0.309371
  ...
# Subtest: compact decorate stamps fold attrs, a hidden shell, and a hover keycap
ok 73 - compact decorate stamps fold attrs, a hidden shell, and a hover keycap
  ---
  duration_ms: 0.548618
  ...
# Subtest: album identity-only cards still carry the foot with a faint missing stamp
ok 74 - album identity-only cards still carry the foot with a faint missing stamp
  ---
  duration_ms: 10.099954
  ...
# Subtest: album report cards mark record→schema, keep the foot last, and hide only record
ok 75 - album report cards mark record→schema, keep the foot last, and hide only record
  ---
  duration_ms: 40.044427
  ...
# Subtest: album adapter unbind releases its path and leaves other notes open
ok 76 - album adapter unbind releases its path and leaves other notes open
  ---
  duration_ms: 2.976092
  ...
# Subtest: a closing album pane preserves its peer foot and can reopen the same note
ok 77 - a closing album pane preserves its peer foot and can reopen the same note
  ---
  duration_ms: 0.915688
  ...
# Subtest: album EnsureSource stays quiet without vault.read
ok 78 - album EnsureSource stays quiet without vault.read
  ---
  duration_ms: 0.271539
  ...
# Subtest: day/week/quarter/year identity-only cards still carry a quiet foot
ok 79 - day/week/quarter/year identity-only cards still carry a quiet foot
  ---
  duration_ms: 11.452114
  ...
# Subtest: bank setup appends the foot after BuildEl, including collapsed, and hides only bank
ok 80 - bank setup appends the foot after BuildEl, including collapsed, and hides only bank
  ---
  duration_ms: 11.289797
  ...
# Subtest: adapter EnsureSource caches a first empty read without refresh
ok 81 - adapter EnsureSource caches a first empty read without refresh
  ---
  duration_ms: 2.527546
  ...
# Subtest: tag search opens a tag query for adapters and record sheets, with command fallback
ok 82 - tag search opens a tag query for adapters and record sheets, with command fallback
  ---
  duration_ms: 1.159253
  ...
# Subtest: foot open state is per path and starts closed
ok 83 - foot open state is per path and starts closed
  ---
  duration_ms: 1.894016
  ...
# Subtest: rename carries open state and delete releases it
ok 84 - rename carries open state and delete releases it
  ---
  duration_ms: 1.826538
  ...
# Subtest: disclosure IDs stay unique across panes on one note
ok 85 - disclosure IDs stay unique across panes on one note
  ---
  duration_ms: 0.398712
  ...
# Subtest: releaseScope drops detached mounts and keeps foreign paths
ok 86 - releaseScope drops detached mounts and keeps foreign paths
  ---
  duration_ms: 0.453226
  ...
# Subtest: toggleProperties acts only on a live matching mount inside the supplied view
ok 87 - toggleProperties acts only on a live matching mount inside the supplied view
  ---
  duration_ms: 1.79631
  ...
# Subtest: orphaned mounts heal on toggle when the foot is still mounted and visible
ok 88 - orphaned mounts heal on toggle when the foot is still mounted and visible
  ---
  duration_ms: 0.421605
  ...
# Subtest: two-pane toggle heals an orphaned foot in its own pane
ok 89 - two-pane toggle heals an orphaned foot in its own pane
  ---
  duration_ms: 0.587271
  ...
# Subtest: toggle listeners notify adapters and the editor hook starts unset
ok 90 - toggle listeners notify adapters and the editor hook starts unset
  ---
  duration_ms: 0.531335
  ...
# Subtest: closed foot shows disclosure, count, and stamp without building rows
ok 91 - closed foot shows disclosure, count, and stamp without building rows
  ---
  duration_ms: 3.584112
  ...
# Subtest: foot disclosure gains a - keycap when keyLive
ok 92 - foot disclosure gains a - keycap when keyLive
  ---
  duration_ms: 0.777023
  ...
# Subtest: open foot groups loose, card, and managed rows with where marks
ok 93 - open foot groups loose, card, and managed rows with where marks
  ---
  duration_ms: 2.875309
  ...
# Subtest: lint chip names problems and never opens the drawer
ok 94 - lint chip names problems and never opens the drawer
  ---
  duration_ms: 20.86628
  ...
# Subtest: value shapes render distinctly
ok 95 - value shapes render distinctly
  ---
  duration_ms: 2.902411
  ...
# Subtest: duplicate keys render one row per occurrence with exact lines
ok 96 - duplicate keys render one row per occurrence with exact lines
  ---
  duration_ms: 1.028644
  ...
# Subtest: unparseable and unclosed frontmatter show the recovery line
ok 97 - unparseable and unclosed frontmatter show the recovery line
  ---
  duration_ms: 0.884609
  ...
# Subtest: disclosure click toggles and scrolls only on expand
ok 98 - disclosure click toggles and scrolls only on expand
  ---
  duration_ms: 1.177889
  ...
# Subtest: key labels invoke the editor only when registered
ok 99 - key labels invoke the editor only when registered
  ---
  duration_ms: 1.535521
  ...
# Subtest: managed sub-fold toggles locally without a repaint
ok 100 - managed sub-fold toggles locally without a repaint
  ---
  duration_ms: 0.950936
  ...
# Subtest: contract lint chip jumps to the first affected setting and never the drawer
ok 101 - contract lint chip jumps to the first affected setting and never the drawer
  ---
  duration_ms: 0.641975
  ...
# Subtest: contract lint chip stays inert without an opener or a known setting
ok 102 - contract lint chip stays inert without an opener or a known setting
  ---
  duration_ms: 0.985612
  ...
# Subtest: Source toggle and path change drop the owner in the same transaction
ok 103 - Source toggle and path change drop the owner in the same transaction
  ---
  duration_ms: 2.97963
  ...
# Subtest: the ownership coordinator registers its Live Preview StateField
ok 104 - the ownership coordinator registers its Live Preview StateField
  ---
  duration_ms: 0.741216
  ...
# Subtest: deferred editor ownership: async dispatch, idempotent path, generations, releaseAll
ok 105 - deferred editor ownership: async dispatch, idempotent path, generations, releaseAll
  ---
  duration_ms: 3.397687
  ...
# Subtest: a replaced owner released before its effect lands never strands the old container
ok 106 - a replaced owner released before its effect lands never strands the old container
  ---
  duration_ms: 0.496288
  ...
# Subtest: editor denial: embeds, popovers, mobile, missing views, missing fields
ok 107 - editor denial: embeds, popovers, mobile, missing views, missing fields
  ---
  duration_ms: 0.82745
  ...
# Subtest: Reading adds the class, inert, and a generation-bound observer
ok 108 - Reading adds the class, inert, and a generation-bound observer
  ---
  duration_ms: 0.742778
  ...
# Subtest: Reading generations: an old handle never clears a newer owner
ok 109 - Reading generations: an old handle never clears a newer owner
  ---
  duration_ms: 0.349948
  ...
# Subtest: Reading ignores embeds, editor scopes, and missing paths
ok 110 - Reading ignores embeds, editor scopes, and missing paths
  ---
  duration_ms: 0.277199
  ...
# Subtest: focusin inside the hidden container returns focus to the editor
ok 111 - focusin inside the hidden container returns focus to the editor
  ---
  duration_ms: 0.833822
  ...
# Subtest: propertyCardOwnFrontmatter dispatches by scope
ok 112 - propertyCardOwnFrontmatter dispatches by scope
  ---
  duration_ms: 0.75954
  ...
# Subtest: source/cache evidence requires a closed duplicate-free matching mapping
ok 113 - source/cache evidence requires a closed duplicate-free matching mapping
  ---
  duration_ms: 1.389924
  ...
# Subtest: mounted card ownership is capability and source gated, then a matching cache change keeps it
ok 114 - mounted card ownership is capability and source gated, then a matching cache change keeps it
  ---
  duration_ms: 1.783475
  ...
# Subtest: a changed event whose cache no longer matches the source releases synchronously
ok 115 - a changed event whose cache no longer matches the source releases synchronously
  ---
  duration_ms: 1.010739
  ...
# Subtest: rename and delete still release ownership unconditionally
ok 116 - rename and delete still release ownership unconditionally
  ---
  duration_ms: 1.040377
  ...
# Subtest: a Reading mount whose adapter source cache was already dropped fails open
ok 117 - a Reading mount whose adapter source cache was already dropped fails open
  ---
  duration_ms: 0.705577
  ...
# Subtest: eligibility holds while getFileCache returns null inside the hold window
ok 118 - eligibility holds while getFileCache returns null inside the hold window
  ---
  duration_ms: 0.874549
  ...
# Subtest: supported card kinds own independent panes; replacement, stale release, and unload are generation safe
ok 119 - supported card kinds own independent panes; replacement, stale release, and unload are generation safe
  ---
  duration_ms: 6.049431
  ...
# Subtest: a detached Reading card acquires after attachment without letting stale callbacks own or release
ok 120 - a detached Reading card acquires after attachment without letting stale callbacks own or release
  ---
  duration_ms: 2.028865
  ...
# Subtest: host register installs the field once; teardown releaseAll is exported
ok 121 - host register installs the field once; teardown releaseAll is exported
  ---
  duration_ms: 0.255488
  ...
# Subtest: area and project mounts acquire through the shared coordinator with contract evidence
ok 122 - area and project mounts acquire through the shared coordinator with contract evidence
  ---
  duration_ms: 1.026951
  ...
# Subtest: home release leaves other card kinds owned and still releases Area/Project mounts
ok 123 - home release leaves other card kinds owned and still releases Area/Project mounts
  ---
  duration_ms: 2.49251
  ...
# Subtest: every adapter mounted release call is filtered by kind or kinds
ok 124 - every adapter mounted release call is filtered by kind or kinds
  ---
  duration_ms: 37.78999
  ...
# Subtest: area and project require the typed settings contract; bank and albums need only props_v1
ok 125 - area and project require the typed settings contract; bank and albums need only props_v1
  ---
  duration_ms: 1.311544
  ...
# Subtest: area mounts need the home source path and a connected foot
ok 126 - area mounts need the home source path and a connected foot
  ---
  duration_ms: 0.720225
  ...
# Subtest: area and project mounts in split panes own independently; replacement and release are path bound
ok 127 - area and project mounts in split panes own independently; replacement and release are path bound
  ---
  duration_ms: 1.058331
  ...
# Subtest: the contract gate is species specific and coordinator confirmation refreshes home mounts
ok 128 - the contract gate is species specific and coordinator confirmation refreshes home mounts
  ---
  duration_ms: 0.331904
  ...
# Subtest: kit CSS sets Obsidian visibility variables and a direct-child fallback
ok 129 - kit CSS sets Obsidian visibility variables and a direct-child fallback
  ---
  duration_ms: 4.808923
  ...
# Subtest: target state: explicit state wins, unresolved means creatable, else exists
ok 130 - target state: explicit state wins, unresolved means creatable, else exists
  ---
  duration_ms: 2.699203
  ...
# Subtest: group row: null without an arm or a centre, and never throws
ok 131 - group row: null without an arm or a centre, and never throws
  ---
  duration_ms: 1.342533
  ...
# Subtest: group row: three grid cells, arm reading order, aria-hidden marks, tooltips, and names
ok 132 - group row: three grid cells, arm reading order, aria-hidden marks, tooltips, and names
  ---
  duration_ms: 1.879749
  ...
# Subtest: group mark: Lucide skip-back / skip-forward drawn inline with createElementNS
ok 133 - group mark: Lucide skip-back / skip-forward drawn inline with createElementNS
  ---
  duration_ms: 0.761845
  ...
# Subtest: group row: a missing arm or centre keeps its column with a gap span
ok 134 - group row: a missing arm or centre keeps its column with a gap span
  ---
  duration_ms: 0.506618
  ...
# Subtest: group row states: creatable plus, ghost note, no href, aria-disabled, and Enter or Space activation
ok 135 - group row states: creatable plus, ghost note, no href, aria-disabled, and Enter or Space activation
  ---
  duration_ms: 1.206344
  ...
# Subtest: group row: wrap glyph, narrow spans, and arms that never paint a landing
ok 136 - group row: wrap glyph, narrow spans, and arms that never paint a landing
  ---
  duration_ms: 0.528369
  ...
# Subtest: group row centre: only the track, a hidden position label, a title, and ticks per member state
ok 137 - group row centre: only the track, a hidden position label, a title, and ticks per member state
  ---
  duration_ms: 0.99511
  ...
# Subtest: group row centre: a one-member group has no centre and no track
ok 138 - group row centre: a one-member group has no centre and no track
  ---
  duration_ms: 0.482721
  ...
# Subtest: group row track: groups larger than 21 or without members use a bar and thumb
ok 139 - group row track: groups larger than 21 or without members use a bar and thumb
  ---
  duration_ms: 0.694366
  ...
# Subtest: group row writes text only through text nodes
ok 140 - group row writes text only through text nodes
  ---
  duration_ms: 0.337394
  ...
# Subtest: rail items and chips: state mapping, unresolved back-compat, plus, ghost note, and stated navigation
ok 141 - rail items and chips: state mapping, unresolved back-compat, plus, ghost note, and stated navigation
  ---
  duration_ms: 1.44559
  ...
# Subtest: rail group row: between the step row and the children, group-only rails, and the group return
ok 142 - rail group row: between the step row and the children, group-only rails, and the group return
  ---
  duration_ms: 1.294602
  ...
# Subtest: legacy rail specs (no state, no group) render byte-identical DOM
ok 143 - legacy rail specs (no state, no group) render byte-identical DOM
  ---
  duration_ms: 10.921631
  ...
# Subtest: styles: the group-row block follows the kit block with states, narrow, forced-colors, and reduced motion
ok 144 - styles: the group-row block follows the kit block with states, narrow, forced-colors, and reduced motion
  ---
  duration_ms: 3.768164
  ...
# Subtest: host helpers are exported beside ownership
ok 145 - host helpers are exported beside ownership
  ---
  duration_ms: 1.816328
  ...
# Subtest: setup registers once and a second setup does not duplicate processors
ok 146 - setup registers once and a second setup does not duplicate processors
  ---
  duration_ms: 1.208157
  ...
# Subtest: two panes of the same path both paint, and a stale unload keeps the live one
ok 147 - two panes of the same path both paint, and a stale unload keeps the live one
  ---
  duration_ms: 1.779187
  ...
# Subtest: detached then attached roots paint on refresh and teardown cancels pending batches
ok 148 - detached then attached roots paint on refresh and teardown cancels pending batches
  ---
  duration_ms: 1.085112
  ...
# Subtest: a new host defaults to excluding embeds, while adapters may opt in
ok 149 - a new host defaults to excluding embeds, while adapters may opt in
  ---
  duration_ms: 3.010569
  ...
# Subtest: failed mounts roll back through commitMount and editorAttributes restore owned classes
ok 150 - failed mounts roll back through commitMount and editorAttributes restore owned classes
  ---
  duration_ms: 2.214108
  ...
# Subtest: album, record, and bank keep their Reading priorities and existing method names
ok 151 - album, record, and bank keep their Reading priorities and existing method names
  ---
  duration_ms: 21.477676
  ...
# Subtest: workspace events refresh by default, and an adapter handler replaces that refresh
ok 152 - workspace events refresh by default, and an adapter handler replaces that refresh
  ---
  duration_ms: 1.203438
  ...
# Subtest: record file-open and layout-change schedule only its Reading-view mount
ok 153 - record file-open and layout-change schedule only its Reading-view mount
  ---
  duration_ms: 7.993062
  ...
# Subtest: record keeps editorAttributes and mount events alongside one shared ownership subscription
ok 154 - record keeps editorAttributes and mount events alongside one shared ownership subscription
  ---
  duration_ms: 9.206877
  ...
# Subtest: a host without editorAttributes does not install the facet
ok 155 - a host without editorAttributes does not install the facet
  ---
  duration_ms: 0.594766
  ...
# Subtest: record Source-mode lint stays on the bank adapter, not behind an LP return
ok 156 - record Source-mode lint stays on the bank adapter, not behind an LP return
  ---
  duration_ms: 2.275274
  ...
# Subtest: LAND: failed Reading repaint releases previous ownership
ok 157 - LAND: failed Reading repaint releases previous ownership
  ---
  duration_ms: 0.725886
  ...
# Subtest: LAND: failed editor rebuild releases previous ownership
ok 158 - LAND: failed editor rebuild releases previous ownership
  ---
  duration_ms: 1.060224
  ...
# Subtest: failed Reading repaint recovers on the next successful refresh
ok 159 - failed Reading repaint recovers on the next successful refresh
  ---
  duration_ms: 0.759581
  ...
# Subtest: failed editor construction releases ownership and stays recoverable
ok 160 - failed editor construction releases ownership and stays recoverable
  ---
  duration_ms: 0.626376
  ...
# Subtest: teardown releases Reading and editor ownership
ok 161 - teardown releases Reading and editor ownership
  ---
  duration_ms: 0.674208
  ...
# Subtest: stale Reading callback cannot clear a newer mount in the same scope
ok 162 - stale Reading callback cannot clear a newer mount in the same scope
  ---
  duration_ms: 0.929906
  ...
# Subtest: two panes of the same path both recover after a failed repaint
ok 163 - two panes of the same path both recover after a failed repaint
  ---
  duration_ms: 1.149265
  ...
# Subtest: album, record, and bank adapters keep failure cleanup wired
ok 164 - album, record, and bank adapters keep failure cleanup wired
  ---
  duration_ms: 20.915283
  ...
# Subtest: registry covers twelve frozen species with presentation and fold defaults
ok 165 - registry covers twelve frozen species with presentation and fold defaults
  ---
  duration_ms: 3.269984
  ...
# Subtest: accessible names lead with the species word
ok 166 - accessible names lead with the species word
  ---
  duration_ms: 0.3453
  ...
# Subtest: applyIdentity stamps kind, label, and a group role without replacing one
ok 167 - applyIdentity stamps kind, label, and a group role without replacing one
  ---
  duration_ms: 0.495807
  ...
# Subtest: glyph tiles: every form, emoji versus icon fallback, and leaf band/value
ok 168 - glyph tiles: every form, emoji versus icon fallback, and leaf band/value
  ---
  duration_ms: 2.115829
  ...
# Subtest: title block: kicker, links, single heading, pill, subtitle, and actions slot
ok 169 - title block: kicker, links, single heading, pill, subtitle, and actions slot
  ---
  duration_ms: 1.600255
  ...
# Subtest: title block keeps markup-looking text literal and fails closed
ok 170 - title block keeps markup-looking text literal and fails closed
  ---
  duration_ms: 0.312827
  ...
# Subtest: rail: empty is null, gaps hold columns, labels, children, and navigation
ok 171 - rail: empty is null, gaps hold columns, labels, children, and navigation
  ---
  duration_ms: 1.511947
  ...
# Subtest: preview fixtures build offline with the real kit builders
ok 172 - preview fixtures build offline with the real kit builders
  ---
  duration_ms: 5.794322
  ...
# Subtest: identity badge: tile plus species word, never a heading, fails closed
ok 173 - identity badge: tile plus species word, never a heading, fails closed
  ---
  duration_ms: 1.577481
  ...
# Subtest: identity badge CSS: own accent and ink fallbacks, kicker type, and forced colors
ok 174 - identity badge CSS: own accent and ink fallbacks, kicker type, and forced colors
  ---
  duration_ms: 2.33608
  ...
# Subtest: preview adopted kinds: the bank card leaves the pixel gate for structural checks
ok 175 - preview adopted kinds: the bank card leaves the pixel gate for structural checks
  ---
  duration_ms: 6.010758
  ...
# Subtest: source order, quoted keys, CRLF, BOM, nested maps, flow values, and block scalars
ok 176 - source order, quoted keys, CRLF, BOM, nested maps, flow values, and block scalars
  ---
  duration_ms: 6.150282
  ...
# Subtest: duplicates retain both stable occurrences and report shared cache values
ok 177 - duplicates retain both stable occurrences and report shared cache values
  ---
  duration_ms: 1.260347
  ...
# Subtest: managed grouping follows source order and explicit where marks win
ok 178 - managed grouping follows source order and explicit where marks win
  ---
  duration_ms: 0.908855
  ...
# Subtest: adapter managed keys fold ordinary leftovers without a global reclassification
ok 179 - adapter managed keys fold ordinary leftovers without a global reclassification
  ---
  duration_ms: 0.74837
  ...
# Subtest: typed values keep absent, null, empty, false, and zero distinct
ok 180 - typed values keep absent, null, empty, false, and zero distinct
  ---
  duration_ms: 0.550431
  ...
# Subtest: cache bookkeeping is excluded and absent source falls back to cache order as pending
ok 181 - cache bookkeeping is excluded and absent source falls back to cache order as pending
  ---
  duration_ms: 0.862246
  ...
# Subtest: malformed and unclosed frontmatter recover without value rows
ok 182 - malformed and unclosed frontmatter recover without value rows
  ---
  duration_ms: 0.714344
  ...
# Subtest: scanner ignores YAML nested structure and detects source lines
ok 183 - scanner ignores YAML nested structure and detects source lines
  ---
  duration_ms: 0.305003
  ...
# Subtest: two panes own the same keys independently
ok 184 - two panes own the same keys independently
  ---
  duration_ms: 4.091812
  ...
# Subtest: stale release cannot clear a newer mount
ok 185 - stale release cannot clear a newer mount
  ---
  duration_ms: 0.474466
  ...
# Subtest: replacement Properties DOM and renamed keys stay scoped
ok 186 - replacement Properties DOM and renamed keys stay scoped
  ---
  duration_ms: 1.584786
  ...
# Subtest: denied scopes keep native fields
ok 187 - denied scopes keep native fields
  ---
  duration_ms: 0.450671
  ...
# Subtest: record adapter owns schema rows plus sheet title only
ok 188 - record adapter owns schema rows plus sheet title only
  ---
  duration_ms: 1.362732
  ...
# Subtest: record adapter denies embeds and null mounts
ok 189 - record adapter denies embeds and null mounts
  ---
  duration_ms: 0.284774
  ...
# Subtest: album owns exactly record and bank owns exactly bank
ok 190 - album owns exactly record and bank owns exactly bank
  ---
  duration_ms: 1.341181
  ...
# Subtest: failed mounts roll back and teardown clears every adapter
ok 191 - failed mounts roll back and teardown clears every adapter
  ---
  duration_ms: 2.117964
  ...
# Subtest: a pane's stale binding for an earlier note keeps the current card's rows owned
ok 192 - a pane's stale binding for an earlier note keeps the current card's rows owned
  ---
  duration_ms: 0.798875
  ...
# Subtest: one card's teardown never clears another card's newer owner of the scope
ok 193 - one card's teardown never clears another card's newer owner of the scope
  ---
  duration_ms: 0.800448
  ...
# Subtest: plugin teardown releases every album and bank mount
ok 194 - plugin teardown releases every album and bank mount
  ---
  duration_ms: 1.595046
  ...
# Subtest: Live Preview album and bank cards own rows under the CodeMirror editor
ok 195 - Live Preview album and bank cards own rows under the CodeMirror editor
  ---
  duration_ms: 12.850693
  ...
# Subtest: one bounded stylesheet rule hides owned rows without a species surface gate
ok 196 - one bounded stylesheet rule hides owned rows without a species surface gate
  ---
  duration_ms: 5.653726
  ...
# Subtest: all card painters are passive and repeated fold refreshes stay read-only
ok 197 - all card painters are passive and repeated fold refreshes stay read-only
  ---
  duration_ms: 27.956126
  ...
# Subtest: a live cache is recorded and returned during a null re-parse gap
ok 198 - a live cache is recorded and returned during a null re-parse gap
  ---
  duration_ms: 2.074301
  ...
# Subtest: a never-cached file returns null
ok 199 - a never-cached file returns null
  ---
  duration_ms: 0.177068
  ...
# Subtest: a different TFile or a missing vault entry returns null
ok 200 - a different TFile or a missing vault entry returns null
  ---
  duration_ms: 0.288361
  ...
# Subtest: the hold expires after PROPERTY_CARD_SETTLED_CACHE_HOLD_MS
ok 201 - the hold expires after PROPERTY_CARD_SETTLED_CACHE_HOLD_MS
  ---
  duration_ms: 0.257011
  ...
# Subtest: changed replaces the entry; rename and delete drop it
ok 202 - changed replaces the entry; rename and delete drop it
  ---
  duration_ms: 0.658918
  ...
# Subtest: the facade delegates other members and binds functions to the real cache
ok 203 - the facade delegates other members and binds functions to the real cache
  ---
  duration_ms: 1.459167
  ...
# Subtest: bind runs once per plugin and reset clears the map
ok 204 - bind runs once per plugin and reset clears the map
  ---
  duration_ms: 0.3506
  ...
# Subtest: Reading: mounts before Properties, owns the title, hides the H1, and promotes the one heading
ok 205 - Reading: mounts before Properties, owns the title, hides the H1, and promotes the one heading
  ---
  duration_ms: 8.901728
  ...
# Subtest: Live Preview: returns slot at once, then mounts and dispatches ownership outside the update
ok 206 - Live Preview: returns slot at once, then mounts and dispatches ownership outside the update
  ---
  duration_ms: 3.151777
  ...
# Subtest: a pending Live Preview re-adopt keeps one mount and inserts the latest node
ok 207 - a pending Live Preview re-adopt keeps one mount and inserts the latest node
  ---
  duration_ms: 1.399481
  ...
# Subtest: a Live Preview mounted re-adopt with a new node keeps the slotted card
ok 208 - a Live Preview mounted re-adopt with a new node keeps the slotted card
  ---
  duration_ms: 1.231581
  ...
# Subtest: a Live Preview same-path re-adopt re-inserts when the slot map misses
ok 209 - a Live Preview same-path re-adopt re-inserts when the slot map misses
  ---
  duration_ms: 1.643097
  ...
# Subtest: a Live Preview re-adopt on a rebuilt editor in the same source view keeps the path
ok 210 - a Live Preview re-adopt on a rebuilt editor in the same source view keeps the path
  ---
  duration_ms: 1.575708
  ...
# Subtest: a Live Preview re-adopt follows a disconnected editor of the same path
ok 211 - a Live Preview re-adopt follows a disconnected editor of the same path
  ---
  duration_ms: 1.640792
  ...
# Subtest: releasing one species leaves the other species' slot on the same editor
ok 212 - releasing one species leaves the other species' slot on the same editor
  ---
  duration_ms: 1.261608
  ...
# Subtest: no slot (embed, mobile, Source mode) falls back with the heading demoted and no ownership
ok 213 - no slot (embed, mobile, Source mode) falls back with the heading demoted and no ownership
  ---
  duration_ms: 1.187788
  ...
# Subtest: onLost(path-changed) releases the title in the same frame, notifies once deferred, and a re-adopt remounts
ok 214 - onLost(path-changed) releases the title in the same frame, notifies once deferred, and a re-adopt remounts
  ---
  duration_ms: 3.318917
  ...
# Subtest: release restores native rendering in the same frame and never calls onLost
ok 215 - release restores native rendering in the same frame and never calls onLost
  ---
  duration_ms: 1.150858
  ...
# Subtest: an old handle never clears a newer adoption
ok 216 - an old handle never clears a newer adoption
  ---
  duration_ms: 1.692673
  ...
# Subtest: unstable and insert-failed paths stay in the fallback until a new path or an explicit release
ok 217 - unstable and insert-failed paths stay in the fallback until a new path or an explicit release
  ---
  duration_ms: 5.435659
  ...
# Subtest: a routine release forgets the sticky fallback once the pane shows another note
ok 218 - a routine release forgets the sticky fallback once the pane shows another note
  ---
  duration_ms: 1.247041
  ...
# Subtest: a same-node re-adopt never remounts; a changed recognizer key re-owns
ok 219 - a same-node re-adopt never remounts; a changed recognizer key re-owns
  ---
  duration_ms: 1.513861
  ...
# Subtest: propertyCardAdoptPatch swaps children and attributes but keeps the slot class and attributes
ok 220 - propertyCardAdoptPatch swaps children and attributes but keeps the slot class and attributes
  ---
  duration_ms: 1.339097
  ...
# Subtest: Reading slot restoration reacquires frontmatter only for a currently eligible mounted card
ok 221 - Reading slot restoration reacquires frontmatter only for a currently eligible mounted card
  ---
  duration_ms: 12.997936
  ...
# Subtest: heading helpers, reading-view lookup, and releaseAll
ok 222 - heading helpers, reading-view lookup, and releaseAll
  ---
  duration_ms: 2.344737
  ...
# Subtest: album ranges: H1 line only after frontmatter, and every non-match is null
ok 223 - album ranges: H1 line only after frontmatter, and every non-match is null
  ---
  duration_ms: 5.204788
  ...
# Subtest: album ranges keep exact offsets across a BOM, CRLF, and no frontmatter
ok 224 - album ranges keep exact offsets across a BOM, CRLF, and no frontmatter
  ---
  duration_ms: 0.946567
  ...
# Subtest: album title ranges consume trailing blanks with exact newline offsets
ok 225 - album title ranges consume trailing blanks with exact newline offsets
  ---
  duration_ms: 0.645713
  ...
# Subtest: heading cleanup strips markers, escapes, wikilinks, and whitespace
ok 226 - heading cleanup strips markers, escapes, wikilinks, and whitespace
  ---
  duration_ms: 0.259265
  ...
# Subtest: day ranges: every H1 shape and alias, both nav forms, and trailing blanks
ok 227 - day ranges: every H1 shape and alias, both nav forms, and trailing blanks
  ---
  duration_ms: 12.990721
  ...
# Subtest: period ranges: week, quarter, and year with alias, nav, and child links
ok 228 - period ranges: week, quarter, and year with alias, nav, and child links
  ---
  duration_ms: 18.537975
  ...
# Subtest: heading-less recognizers start at an accepted follower line
ok 229 - heading-less recognizers start at an accepted follower line
  ---
  duration_ms: 0.458365
  ...
# Subtest: reveal boundaries follow the inclusive touch rule
ok 230 - reveal boundaries follow the inclusive touch rule
  ---
  duration_ms: 0.445851
  ...
# Subtest: reducer: own, stale release, Source mode, file change, doc change, and reveal
ok 231 - reducer: own, stale release, Source mode, file change, doc change, and reveal
  ---
  duration_ms: 1.674306
  ...
# Subtest: the extension is one lazily defined StateField with decorations and attributes
ok 232 - the extension is one lazily defined StateField with decorations and attributes
  ---
  duration_ms: 0.484244
  ...
# Subtest: deferred editor ownership: async dispatch, idempotent keys, generations, releaseAll
ok 233 - deferred editor ownership: async dispatch, idempotent keys, generations, releaseAll
  ---
  duration_ms: 2.349145
  ...
# Subtest: a field that drops the owner every transaction re-arms once
ok 234 - a field that drops the owner every transaction re-arms once
  ---
  duration_ms: 0.559719
  ...
# Subtest: a replaced owner released before its effect lands never strands the old range
ok 235 - a replaced owner released before its effect lands never strands the old range
  ---
  duration_ms: 0.477933
  ...
# Subtest: editor denial: embeds, missing views, missing recognizers, and missing fields
ok 236 - editor denial: embeds, missing views, missing recognizers, and missing fields
  ---
  duration_ms: 0.882575
  ...
# Subtest: Reading tags the h1 and nav p, never the section wrapper, a card, or embeds
ok 237 - Reading tags the h1 and nav p, never the section wrapper, a card, or embeds
  ---
  duration_ms: 3.413869
  ...
# Subtest: Reading absorbs <br>-joined nav and child lines and stops at prose
ok 238 - Reading absorbs <br>-joined nav and child lines and stops at prose
  ---
  duration_ms: 3.937739
  ...
# Subtest: Reading ignores unrecognized or late headings and denied scopes
ok 239 - Reading ignores unrecognized or late headings and denied scopes
  ---
  duration_ms: 0.881503
  ...
# Subtest: Reading re-tags late sections and keeps generations safe
ok 240 - Reading re-tags late sections and keeps generations safe
  ---
  duration_ms: 2.164643
  ...
# Subtest: propertyCardOwnTitle dispatches by scope
ok 241 - propertyCardOwnTitle dispatches by scope
  ---
  duration_ms: 0.791882
  ...
# Subtest: host opt-in registers the title field once per plugin; others register nothing new
ok 242 - host opt-in registers the title field once per plugin; others register nothing new
  ---
  duration_ms: 1.865421
  ...
# Subtest: Live Preview mounts between the inline title and Properties for every Properties shape
ok 243 - Live Preview mounts between the inline title and Properties for every Properties shape
  ---
  duration_ms: 6.041845
  ...
# Subtest: Reading mounts before Properties or appends to .mod-header
ok 244 - Reading mounts before Properties or appends to .mod-header
  ---
  duration_ms: 0.798605
  ...
# Subtest: the observer re-inserts a removed node and re-anchors before new Properties
ok 245 - the observer re-inserts a removed node and re-anchors before new Properties
  ---
  duration_ms: 1.124397
  ...
# Subtest: a replaced .mod-header moves the card and its observers
ok 246 - a replaced .mod-header moves the card and its observers
  ---
  duration_ms: 0.799406
  ...
# Subtest: exhausting the re-insertion budget self-releases as unstable
ok 247 - exhausting the re-insertion budget self-releases as unstable
  ---
  duration_ms: 2.222283
  ...
# Subtest: release handles are generation-bound, idempotent, and complete
ok 248 - release handles are generation-bound, idempotent, and complete
  ---
  duration_ms: 0.931328
  ...
# Subtest: moving a node to another scope releases the first; a new node replaces the old
ok 249 - moving a node to another scope releases the first; a new node replaces the old
  ---
  duration_ms: 0.968189
  ...
# Subtest: denied scopes return null with no DOM change
ok 250 - denied scopes return null with no DOM change
  ---
  duration_ms: 2.056796
  ...
# Subtest: a denial after mount releases the scope's existing entry
ok 251 - a denial after mount releases the scope's existing entry
  ---
  duration_ms: 0.875011
  ...
# Subtest: switching to Source self-releases with onLost(denied)
ok 252 - switching to Source self-releases with onLost(denied)
  ---
  duration_ms: 1.209119
  ...
# Subtest: a currentPath mismatch self-releases with onLost(path-changed)
ok 253 - a currentPath mismatch self-releases with onLost(path-changed)
  ---
  duration_ms: 0.614864
  ...
# Subtest: a throwing onLost is swallowed and explicit releases never call it
ok 254 - a throwing onLost is swallowed and explicit releases never call it
  ---
  duration_ms: 0.676342
  ...
# Subtest: Live Preview insertions and height changes redraw the Vim cursor
ok 255 - Live Preview insertions and height changes redraw the Vim cursor
  ---
  duration_ms: 1.489424
  ...
# Subtest: cursor redraw is safe when Vim hooks are absent or broken
ok 256 - cursor redraw is safe when Vim hooks are absent or broken
  ---
  duration_ms: 0.498181
  ...
# Subtest: observer re-insertion redraws the Live Preview Vim cursor
ok 257 - observer re-insertion redraws the Live Preview Vim cursor
  ---
  duration_ms: 0.430543
  ...
# Subtest: hosts without observers still mount and release
ok 258 - hosts without observers still mount and release
  ---
  duration_ms: 0.428198
  ...
# Subtest: an insertion that throws returns null and leaves no entry
ok 259 - an insertion that throws returns null and leaves no entry
  ---
  duration_ms: 0.297007
  ...
# Subtest: a later mount prunes entries whose scope was disconnected
ok 260 - a later mount prunes entries whose scope was disconnected
  ---
  duration_ms: 0.546574
  ...
# Subtest: ReleaseAll and plugin teardown leave no slot node and no live observer
ok 261 - ReleaseAll and plugin teardown leave no slot node and no live observer
  ---
  duration_ms: 10.10379
  ...
# Subtest: Reading re-measures through the renderer's updateHeader
ok 262 - Reading re-measures through the renderer's updateHeader
  ---
  duration_ms: 0.526685
  ...
# Subtest: the Live Preview measure rescues a scroll target CodeMirror would drop
ok 263 - the Live Preview measure rescues a scroll target CodeMirror would drop
  ---
  duration_ms: 0.596839
  ...
# Subtest: Live Preview keeps the visible text still when an off-screen card resizes
ok 264 - Live Preview keeps the visible text still when an off-screen card resizes
  ---
  duration_ms: 0.673506
  ...
# Subtest: a closed leaf self-releases with onLost(disconnected)
ok 265 - a closed leaf self-releases with onLost(disconnected)
  ---
  duration_ms: 0.439279
  ...
# Subtest: a Reading header virtualized out of the sizer parks the card instead of losing it
ok 266 - a Reading header virtualized out of the sizer parks the card instead of losing it
  ---
  duration_ms: 0.682914
  ...
# Subtest: Live Preview never parks: a vanished .cm-sizer child set is a denial
ok 267 - Live Preview never parks: a vanished .cm-sizer child set is a denial
  ---
  duration_ms: 0.450921
  ...
# Subtest: the editor update listener arms the rescue only for an editor with a mounted Live Preview card
ok 268 - the editor update listener arms the rescue only for an editor with a mounted Live Preview card
  ---
  duration_ms: 0.588804
  ...
# Subtest: Live Preview measure requests are budgeted so a size loop cannot freeze the renderer
ok 269 - Live Preview measure requests are budgeted so a size loop cannot freeze the renderer
  ---
  duration_ms: 0.576631
  ...
# Subtest: cursor redraw is Live Preview only and missing or throwing Vim hooks are fail-safe
ok 270 - cursor redraw is Live Preview only and missing or throwing Vim hooks are fail-safe
  ---
  duration_ms: 1.416234
  ...
# Subtest: o/O/Mod+; map to add placements and stay native inside inputs
ok 271 - o/O/Mod+; map to add placements and stay native inside inputs
  ---
  duration_ms: 2.437303
  ...
# Subtest: insertion anchors are source keys, not group indexes, and empty notes have none
ok 272 - insertion anchors are source keys, not group indexes, and empty notes have none
  ---
  duration_ms: 1.600355
  ...
# Subtest: name inventory uses types and counts, falls back without inventing types, and keeps order
ok 273 - name inventory uses types and counts, falls back without inventing types, and keeps order
  ---
  duration_ms: 1.030968
  ...
# Subtest: Tab/Enter takes a completion type and Shift+Enter keeps a literal text key
ok 274 - Tab/Enter takes a completion type and Shift+Enter keeps a literal text key
  ---
  duration_ms: 0.516626
  ...
# Subtest: Obsidian widget property infos preserve completion types and literal override
ok 275 - Obsidian widget property infos preserve completion types and literal override
  ---
  duration_ms: 26.362483
  ...
# Subtest: add ops carry before/after and checkbox/url kinds stay on supported wire types
ok 276 - add ops carry before/after and checkbox/url kinds stay on supported wire types
  ---
  duration_ms: 0.40826
  ...
# Subtest: o below, O above, and Mod+; start name stages on the selected source key
ok 277 - o below, O above, and Mod+; start name stages on the selected source key
  ---
  duration_ms: 1.720024
  ...
# Subtest: empty notes add at the end and mode=add opens the name stage
ok 278 - empty notes add at the end and mode=add opens the name stage
  ---
  duration_ms: 0.507018
  ...
# Subtest: mode=edit opens a loose value stage once without flipping a checkbox
ok 279 - mode=edit opens a loose value stage once without flipping a checkbox
  ---
  duration_ms: 0.978378
  ...
# Subtest: name cancellation and value cancellation write nothing
ok 280 - name cancellation and value cancellation write nothing
  ---
  duration_ms: 0.897294
  ...
# Subtest: Shift+Enter override and Tab completion open the matching value stage
ok 281 - Shift+Enter override and Tab completion open the matching value stage
  ---
  duration_ms: 0.977085
  ...
# Subtest: API absence still completes names as text without invented types
ok 282 - API absence still completes names as text without invented types
  ---
  duration_ms: 0.654941
  ...
# Subtest: duplicate and missing-anchor races keep the draft and do not move the destination
ok 283 - duplicate and missing-anchor races keep the draft and do not move the destination
  ---
  duration_ms: 3.155426
  ...
# Subtest: unsafe prospective names keep the draft and surface bob's refusal
ok 284 - unsafe prospective names keep the draft and surface bob's refusal
  ---
  duration_ms: 2.344646
  ...
# Subtest: first-property create uses one prop.set and undo/redo round-trip
ok 285 - first-property create uses one prop.set and undo/redo round-trip
  ---
  duration_ms: 1.894987
  ...
# Subtest: name stage painter lists type and count and retains the input
ok 286 - name stage painter lists type and count and retains the input
  ---
  duration_ms: 1.28832
  ...
# Subtest: Mod+C and Mod+V are browse shortcuts while text inputs keep native clipboard behavior
ok 287 - Mod+C and Mod+V are browse shortcuts while text inputs keep native clipboard behavior
  ---
  duration_ms: 2.096373
  ...
# Subtest: clipboard selection uses focused fallback and file order for marks
ok 288 - clipboard selection uses focused fallback and file order for marks
  ---
  duration_ms: 1.642116
  ...
# Subtest: paste plan skips all protected roles and opaque values
ok 289 - paste plan skips all protected roles and opaque values
  ---
  duration_ms: 0.590678
  ...
# Subtest: copy emits exact source bytes in source order, including comments and read-only keys
ok 290 - copy emits exact source bytes in source order, including comments and read-only keys
  ---
  duration_ms: 8.062304
  ...
# Subtest: copy permission denial is reported without writing the note
ok 291 - copy permission denial is reported without writing the note
  ---
  duration_ms: 1.180443
  ...
# Subtest: paste previews ordered New, Replace, and skipped keys as one undoable batch
ok 292 - paste previews ordered New, Replace, and skipped keys as one undoable batch
  ---
  duration_ms: 3.467921
  ...
# Subtest: new protected names become skips through Bob dry-run; all-skipped paste cannot apply
ok 293 - new protected names become skips through Bob dry-run; all-skipped paste cannot apply
  ---
  duration_ms: 0.672624
  ...
# Subtest: malformed YAML, invalid values, and recovery reports block paste
ok 294 - malformed YAML, invalid values, and recovery reports block paste
  ---
  duration_ms: 0.838952
  ...
# Subtest: paste clipboard permission failures block without a Bob write
ok 295 - paste clipboard permission failures block without a Bob write
  ---
  duration_ms: 0.392118
  ...
# Subtest: stale preview refreshes the listing and keeps the same batch for explicit confirmation
ok 296 - stale preview refreshes the listing and keeps the same batch for explicit confirmation
  ---
  duration_ms: 1.316443
  ...
# Subtest: ownership change refreshes the listing but never silently shrinks the displayed batch
ok 297 - ownership change refreshes the listing but never silently shrinks the displayed batch
  ---
  duration_ms: 0.834733
  ...
# Subtest: cancellation during clipboard read prevents later classification
ok 298 - cancellation during clipboard read prevents later classification
  ---
  duration_ms: 0.492781
  ...
# Subtest: entry paths accept Markdown and resolve explicit over active
ok 299 - entry paths accept Markdown and resolve explicit over active
  ---
  duration_ms: 3.882303
  ...
# Subtest: species hand-off maps owners and refuses unknown editors
ok 300 - species hand-off maps owners and refuses unknown editors
  ---
  duration_ms: 0.323358
  ...
# Subtest: recovery line prefers the earliest row, then frontmatter, then line one
ok 301 - recovery line prefers the earliest row, then frontmatter, then line one
  ---
  duration_ms: 0.667114
  ...
# Subtest: the + arm acts on a bare normal-mode plus, shifted included, and every guard refuses
ok 302 - the + arm acts on a bare normal-mode plus, shifted included, and every guard refuses
  ---
  duration_ms: 0.690779
  ...
# Subtest: setup registers the palette command, the + arm, and the drawer hook
ok 303 - setup registers the palette command, the + arm, and the drawer hook
  ---
  duration_ms: 2.402138
  ...
# Subtest: bare + opens the generic Property Editor on bank.md
ok 304 - bare + opens the generic Property Editor on bank.md
  ---
  duration_ms: 0.710687
  ...
# Subtest: drawer opener actions route through the editor hook with add/browse modes
ok 305 - drawer opener actions route through the editor hook with add/browse modes
  ---
  duration_ms: 0.960774
  ...
# Subtest: record sheet drawer exposes the same hook-gated opener actions
ok 306 - record sheet drawer exposes the same hook-gated opener actions
  ---
  duration_ms: 0.709194
  ...
# Subtest: drawer body shows Add and Edit-all actions only while the hook is registered
ok 307 - drawer body shows Add and Edit-all actions only while the hook is registered
  ---
  duration_ms: 4.035755
  ...
# Subtest: drawer key buttons open the editor while value links keep navigating
ok 308 - drawer key buttons open the editor while value links keep navigating
  ---
  duration_ms: 1.161988
  ...
# Subtest: openPropertyEditor refuses unusable targets with useful reasons
ok 309 - openPropertyEditor refuses unusable targets with useful reasons
  ---
  duration_ms: 0.977636
  ...
# Subtest: openPropertyEditor opens the shared modal and resolves the active note
ok 310 - openPropertyEditor opens the shared modal and resolves the active note
  ---
  duration_ms: 1.731827
  ...
# Subtest: species hand-offs close the modal and pass the field
ok 311 - species hand-offs close the modal and pass the field
  ---
  duration_ms: 0.957639
  ...
# Subtest: ordinary notes keep the modal open with a missing-route explanation
ok 312 - ordinary notes keep the modal open with a missing-route explanation
  ---
  duration_ms: 0.538989
  ...
# Subtest: browse equals hands card rows to the species editor and keeps drafts
ok 313 - browse equals hands card rows to the species editor and keeps drafts
  ---
  duration_ms: 2.652103
  ...
# Subtest: props excursion begins with the note path and stays leaf-pinned
ok 314 - props excursion begins with the note path and stays leaf-pinned
  ---
  duration_ms: 1.064803
  ...
# Subtest: y excursion jumps to the reported key line and installs Done state
ok 315 - y excursion jumps to the reported key line and installs Done state
  ---
  duration_ms: 2.028673
  ...
# Subtest: YAML recovery uses the parser line even when a cached key is selected
ok 316 - YAML recovery uses the parser line even when a cached key is selected
  ---
  duration_ms: 0.938322
  ...
# Subtest: YAML escape retains the selected duplicate occurrence through modal close
ok 317 - YAML escape retains the selected duplicate occurrence through modal close
  ---
  duration_ms: 1.102775
  ...
# Subtest: Done refuses stale excursions and failed saves without reopening
ok 318 - Done refuses stale excursions and failed saves without reopening
  ---
  duration_ms: 0.745103
  ...
# Subtest: Done saves, restores the leaf mode, and reopens the same surviving key
ok 319 - Done saves, restores the leaf mode, and reopens the same surviving key
  ---
  duration_ms: 0.548577
  ...
# Subtest: Done after an external delete lands on the nearest surviving source position
ok 320 - Done after an external delete lands on the nearest surviving source position
  ---
  duration_ms: 0.444699
  ...
# Subtest: Done retains the second duplicate after a source line shift
ok 321 - Done retains the second duplicate after a source line shift
  ---
  duration_ms: 0.501157
  ...
# Subtest: legacy Done records without selection still reopen by key
ok 322 - legacy Done records without selection still reopen by key
  ---
  duration_ms: 0.395926
  ...
# Subtest: Done reopens recovery mode when the YAML stays damaged
ok 323 - Done reopens recovery mode when the YAML stays damaged
  ---
  duration_ms: 0.333898
  ...
# Subtest: a present loose key selects its row
ok 324 - a present loose key selects its row
  ---
  duration_ms: 6.882142
  ...
# Subtest: a missing loose key opens Add prefilled with the value focused
ok 325 - a missing loose key opens Add prefilled with the value focused
  ---
  duration_ms: 7.743884
  ...
# Subtest: a missing summary on a notebook opens Add through the catalog path
ok 326 - a missing summary on a notebook opens Add through the catalog path
  ---
  duration_ms: 0.835535
  ...
# Subtest: a present summary on a notebook selects its row
ok 327 - a present summary on a notebook selects its row
  ---
  duration_ms: 0.613632
  ...
# Subtest: a duplicate key selects its first row
ok 328 - a duplicate key selects its first row
  ---
  duration_ms: 0.520384
  ...
# Subtest: a degraded report keeps the safe first row
ok 329 - a degraded report keeps the safe first row
  ---
  duration_ms: 0.544059
  ...
# Subtest: an old-bob report keeps the safe first row
ok 330 - an old-bob report keeps the safe first row
  ---
  duration_ms: 0.446062
  ...
# Subtest: the Esc/q/Ctrl+[ ladder still closes from focus-or-add
ok 331 - the Esc/q/Ctrl+[ ladder still closes from focus-or-add
  ---
  duration_ms: 1.254405
  ...
# Subtest: an explicit add mode prefills the requested key
ok 332 - an explicit add mode prefills the requested key
  ---
  duration_ms: 0.593023
  ...
# Subtest: the setting path on area notes never touches Add
ok 333 - the setting path on area notes never touches Add
  ---
  duration_ms: 0.588213
  ...
# Subtest: t maps to kind conversion while text inputs keep native typing
ok 334 - t maps to kind conversion while text inputs keep native typing
  ---
  duration_ms: 1.977165
  ...
# Subtest: safe scalar conversions and single text to one-item list emit prop.set
ok 335 - safe scalar conversions and single text to one-item list emit prop.set
  ---
  duration_ms: 2.716426
  ...
# Subtest: null, empty, false, and zero stay distinct
ok 336 - null, empty, false, and zero stay distinct
  ---
  duration_ms: 0.433387
  ...
# Subtest: validated date tokens convert; datetime to date stays editable
ok 337 - validated date tokens convert; datetime to date stays editable
  ---
  duration_ms: 18.902922
  ...
# Subtest: multi-item lists and invalid numbers need explicit input
ok 338 - multi-item lists and invalid numbers need explicit input
  ---
  duration_ms: 0.506607
  ...
# Subtest: date-looking text cannot force a different inferred kind
ok 339 - date-looking text cannot force a different inferred kind
  ---
  duration_ms: 0.234097
  ...
# Subtest: tags and aliases stay key-specific
ok 340 - tags and aliases stay key-specific
  ---
  duration_ms: 0.311274
  ...
# Subtest: maps use the YAML stage; opaque and protected rows are refused
ok 341 - maps use the YAML stage; opaque and protected rows are refused
  ---
  duration_ms: 0.417737
  ...
# Subtest: converting created to datetime adds the offset-stripping warning
ok 342 - converting created to datetime adds the offset-stripping warning
  ---
  duration_ms: 2.948189
  ...
# Subtest: type manager adapter handles missing, throwing, and asynchronous setters
ok 343 - type manager adapter handles missing, throwing, and asynchronous setters
  ---
  duration_ms: 0.636385
  ...
# Subtest: note counts prefer the property-info API and fall back to cache iteration
ok 344 - note counts prefer the property-info API and fall back to cache iteration
  ---
  duration_ms: 0.657936
  ...
# Subtest: vault confirmation names the key, type, and note count
ok 345 - vault confirmation names the key, type, and note count
  ---
  duration_ms: 0.284252
  ...
# Subtest: protected rows cannot open the conversion stage
ok 346 - protected rows cannot open the conversion stage
  ---
  duration_ms: 2.171596
  ...
# Subtest: local conversion drafts prop.set and does not touch the type manager
ok 347 - local conversion drafts prop.set and does not touch the type manager
  ---
  duration_ms: 1.704173
  ...
# Subtest: vault confirmation can be cancelled without applying
ok 348 - vault confirmation can be cancelled without applying
  ---
  duration_ms: 1.028693
  ...
# Subtest: successful vault type changes stay on the injected manager
ok 349 - successful vault type changes stay on the injected manager
  ---
  duration_ms: 0.870282
  ...
# Subtest: unsupported managers teach All Properties and make no global change
ok 350 - unsupported managers teach All Properties and make no global change
  ---
  duration_ms: 0.513631
  ...
# Subtest: failed setters report the error and skip property undo
ok 351 - failed setters report the error and skip property undo
  ---
  duration_ms: 0.631125
  ...
# Subtest: conversion stage paint shows current value, warning, and vault confirmation
ok 352 - conversion stage paint shows current value, warning, and vault confirmation
  ---
  duration_ms: 1.533729
  ...
# Subtest: close ladder still treats conversion as a stage
ok 353 - close ladder still treats conversion as a stage
  ---
  duration_ms: 0.25648
  ...
# Subtest: parent stage handler is registered with kind parent
ok 354 - parent stage handler is registered with kind parent
  ---
  duration_ms: 2.27809
  ...
# Subtest: parent stage build writes one quoted wikilink op
ok 355 - parent stage build writes one quoted wikilink op
  ---
  duration_ms: 2.163871
  ...
# Subtest: parent stage build refuses an empty home
ok 356 - parent stage build refuses an empty home
  ---
  duration_ms: 0.215342
  ...
# Subtest: parent sync names run exactly the catalogs bob named
ok 357 - parent sync names run exactly the catalogs bob named
  ---
  duration_ms: 0.315974
  ...
# Subtest: parent sync report names refreshed catalogs and failed syncs
ok 358 - parent sync report names refreshed catalogs and failed syncs
  ---
  duration_ms: 0.435582
  ...
# Subtest: parent stem parsing strips brackets, anchors, and extensions
ok 359 - parent stem parsing strips brackets, anchors, and extensions
  ---
  duration_ms: 0.239928
  ...
# Subtest: r and Alt+J/K/arrows map to rename and source moves; inputs keep native typing
ok 360 - r and Alt+J/K/arrows map to rename and source moves; inputs keep native typing
  ---
  duration_ms: 2.10032
  ...
# Subtest: rename validator excludes the current key and accepts quoted Unicode and integer-like names
ok 361 - rename validator excludes the current key and accepts quoted Unicode and integer-like names
  ---
  duration_ms: 1.632066
  ...
# Subtest: source-order neighbors ignore grouped visible order and treat protected rows as position references
ok 362 - source-order neighbors ignore grouped visible order and treat protected rows as position references
  ---
  duration_ms: 1.296496
  ...
# Subtest: rename remaps focus and one mark onto the new key without dropping other marks
ok 363 - rename remaps focus and one mark onto the new key without dropping other marks
  ---
  duration_ms: 0.474907
  ...
# Subtest: r opens a seeded rename stage; duplicate and protected destinations keep the draft
ok 364 - r opens a seeded rename stage; duplicate and protected destinations keep the draft
  ---
  duration_ms: 6.31743
  ...
# Subtest: successful rename applies prop.rename, moves focus and its mark, and keeps other marks
ok 365 - successful rename applies prop.rename, moves focus and its mark, and keeps other marks
  ---
  duration_ms: 2.670177
  ...
# Subtest: same-name rename is a no-op and late preview edits do not apply a stale latch
ok 366 - same-name rename is a no-op and late preview edits do not apply a stale latch
  ---
  duration_ms: 0.962367
  ...
# Subtest: moves use source neighbors, skip held keys, and refuse filter, stage, and pending writes
ok 367 - moves use source neighbors, skip held keys, and refuse filter, stage, and pending writes
  ---
  duration_ms: 1.849462
  ...
# Subtest: a move with identical semantic fingerprints still records one undo step
ok 368 - a move with identical semantic fingerprints still records one undo step
  ---
  duration_ms: 2.47158
  ...
# Subtest: paint exposes rename and move actions, a 120ms slide, and reduced-motion skip
ok 369 - paint exposes rename and move actions, a 120ms slide, and reduced-motion skip
  ---
  duration_ms: 17.773003
  ...
# Subtest: rename and reorder paint do not spawn a writer until an explicit apply
ok 370 - rename and reorder paint do not spawn a writer until an explicit apply
  ---
  duration_ms: 0.375497
  ...
# Subtest: nearest-row keeps requested keys across line shifts
ok 371 - nearest-row keeps requested keys across line shifts
  ---
  duration_ms: 2.010108
  ...
# Subtest: constructor and reconcile preserve the requested key, not the first row
ok 372 - constructor and reconcile preserve the requested key, not the first row
  ---
  duration_ms: 3.868695
  ...
# Subtest: openPropertyEditor with key and edit mode opens that key's stage
ok 373 - openPropertyEditor with key and edit mode opens that key's stage
  ---
  duration_ms: 1.665179
  ...
# Subtest: wanted selection falls back to the requested open key
ok 374 - wanted selection falls back to the requested open key
  ---
  duration_ms: 0.196104
  ...
# Subtest: wanted selection prefers stored duplicate ordinal over collapsed cache
ok 375 - wanted selection prefers stored duplicate ordinal over collapsed cache
  ---
  duration_ms: 0.213398
  ...
# Subtest: cache-first reopen keeps the second duplicate through report reconciliation
ok 376 - cache-first reopen keeps the second duplicate through report reconciliation
  ---
  duration_ms: 0.619713
  ...
# Subtest: empty cache still opens the requested key's stage after the report arrives
ok 377 - empty cache still opens the requested key's stage after the report arrives
  ---
  duration_ms: 0.668456
  ...
# Subtest: confirmed overlays replace cached values and drop deleted keys
ok 378 - confirmed overlays replace cached values and drop deleted keys
  ---
  duration_ms: 0.433668
  ...
# Subtest: foot frontmatter paints the overlay post-image without spawning
ok 379 - foot frontmatter paints the overlay post-image without spawning
  ---
  duration_ms: 0.562133
  ...
# Subtest: digest changes when the editor hook registers or unregisters
ok 380 - digest changes when the editor hook registers or unregisters
  ---
  duration_ms: 0.473965
  ...
# Subtest: recovery shows bob's message verbatim and targets the parse-error line
ok 381 - recovery shows bob's message verbatim and targets the parse-error line
  ---
  duration_ms: 0.755543
  ...
# Subtest: duplicate-key YAML targets the duplicate line
ok 382 - duplicate-key YAML targets the duplicate line
  ---
  duration_ms: 0.209731
  ...
# Subtest: datetimes without an existing offset send wall time with matching seconds
ok 383 - datetimes without an existing offset send wall time with matching seconds
  ---
  duration_ms: 22.310508
  ...
# Subtest: datetimes keep an existing offset across every documented spelling
ok 384 - datetimes keep an existing offset across every documented spelling
  ---
  duration_ms: 2.747916
  ...
# Subtest: tags normalize only the typed item; untouched stages are no-ops
ok 385 - tags normalize only the typed item; untouched stages are no-ops
  ---
  duration_ms: 0.618
  ...
# Subtest: an untouched null text stage is a no-op instead of writing empty
ok 386 - an untouched null text stage is a no-op instead of writing empty
  ---
  duration_ms: 0.312938
  ...
# Subtest: an exact typed name wins over a lingering highlight on Enter or Tab
ok 387 - an exact typed name wins over a lingering highlight on Enter or Tab
  ---
  duration_ms: 0.403931
  ...
# Subtest: o, O, and Mod+; refuse while a value stage is open
ok 388 - o, O, and Mod+; refuse while a value stage is open
  ---
  duration_ms: 1.172238
  ...
# Subtest: visible groups keep grouped row order and search complete nested values
ok 389 - visible groups keep grouped row order and search complete nested values
  ---
  duration_ms: 4.846543
  ...
# Subtest: selection keys distinguish Space, visual range, filter, and shifted arrows
ok 390 - selection keys distinguish Space, visual range, filter, and shifted arrows
  ---
  duration_ms: 0.782965
  ...
# Subtest: visual range follows grouped visible order, reverses at its anchor, and keeps marks on exit
ok 391 - visual range follows grouped visible order, reverses at its anchor, and keeps marks on exit
  ---
  duration_ms: 3.448183
  ...
# Subtest: filter opening preserves marks; query edits clear marks and hidden rows; empty results keep a target
ok 392 - filter opening preserves marks; query edits clear marks and hidden rows; empty results keep a target
  ---
  duration_ms: 2.471258
  ...
# Subtest: an empty filter layer does not clear marks when Esc dismisses it
ok 393 - an empty filter layer does not clear marks when Esc dismisses it
  ---
  duration_ms: 0.460139
  ...
# Subtest: Esc with a query repaints the cleared filter layer
ok 394 - Esc with a query repaints the cleared filter layer
  ---
  duration_ms: 0.365477
  ...
# Subtest: a successful multi-delete sends one source-ordered guarded batch and reconciles focus
ok 395 - a successful multi-delete sends one source-ordered guarded batch and reconciles focus
  ---
  duration_ms: 3.363492
  ...
# Subtest: mixed protected selection refuses the whole batch and names every locked row
ok 396 - mixed protected selection refuses the whole batch and names every locked row
  ---
  duration_ms: 0.63897
  ...
# Subtest: refresh reconciliation follows a unique key across line changes and never guesses a duplicate
ok 397 - refresh reconciliation follows a unique key across line changes and never guesses a duplicate
  ---
  duration_ms: 0.583915
  ...
# Subtest: selection, filtering, and paint options do not create a session or call writers
ok 398 - selection, filtering, and paint options do not create a session or call writers
  ---
  duration_ms: 3.426904
  ...
# Subtest: paint shows accessible mark gutters, filter controls, and a disabled filtered reorder action
ok 399 - paint shows accessible mark gutters, filter controls, and a disabled filtered reorder action
  ---
  duration_ms: 8.967021
  ...
# Subtest: setting op helpers emit typed set/clear shapes and refuse a scalar clock
ok 400 - setting op helpers emit typed set/clear shapes and refuse a scalar clock
  ---
  duration_ms: 3.73415
  ...
# Subtest: summary, ready cap, and review enforce boundaries while long summary still saves
ok 401 - summary, ready cap, and review enforce boundaries while long summary still saves
  ---
  duration_ms: 0.490898
  ...
# Subtest: ghost Enter seeds an override draft from effective data and writes nothing until save
ok 402 - ghost Enter seeds an override draft from effective data and writes nothing until save
  ---
  duration_ms: 4.510491
  ...
# Subtest: summary save uses setting.set and keeps ordinary text stages on prop.set
ok 403 - summary save uses setting.set and keeps ordinary text stages on prop.set
  ---
  duration_ms: 2.217233
  ...
# Subtest: ready cap writes off, never a stored count, and review stays in 1–365
ok 404 - ready cap writes off, never a stored count, and review stays in 1–365
  ---
  duration_ms: 5.023671
  ...
# Subtest: capture names keep order on setting.set and clock never submits a scalar
ok 405 - capture names keep order on setting.set and clock never submits a scalar
  ---
  duration_ms: 2.039624
  ...
# Subtest: stats root Enter sets true or clears, never root:false, and stays locked on top-level projects
ok 406 - stats root Enter sets true or clears, never root:false, and stays locked on top-level projects
  ---
  duration_ms: 2.46702
  ...
# Subtest: preview warnings and candidate effective labels stay out of confirmed report state
ok 407 - preview warnings and candidate effective labels stay out of confirmed report state
  ---
  duration_ms: 6.806147
  ...
# Subtest: older apply responses without contract invalidate it and re-read props show
ok 408 - older apply responses without contract invalidate it and re-read props show
  ---
  duration_ms: 12.996422
  ...
# Subtest: clear, undo, and repeated Enter keep one inverse history item
ok 409 - clear, undo, and repeated Enter keep one inverse history item
  ---
  duration_ms: 4.784996
  ...
# Subtest: stale setting previews keep the draft and ordinary YAML/list builders stay on prop.*
ok 410 - stale setting previews keep the draft and ordinary YAML/list builders stay on prop.*
  ---
  duration_ms: 1.898495
  ...
# Subtest: later phases can replace only their setting handler
ok 411 - later phases can replace only their setting handler
  ---
  duration_ms: 0.185524
  ...
# Subtest: Hue stage lists inherited palette choices and builds set or clear ops
ok 412 - Hue stage lists inherited palette choices and builds set or clear ops
  ---
  duration_ms: 0.925978
  ...
# Subtest: Default type picker includes Inherit, off, configured and unconfigured values
ok 413 - Default type picker includes Inherit, off, configured and unconfigured values
  ---
  duration_ms: 1.393511
  ...
# Subtest: Clock policy stage preserves shadowed off-clock types in one normalized setting op
ok 414 - Clock policy stage preserves shadowed off-clock types in one normalized setting op
  ---
  duration_ms: 1.53469
  ...
# Subtest: ready cap effect line uses local noteReady counts and stays quiet when unavailable
ok 415 - ready cap effect line uses local noteReady counts and stays quiet when unavailable
  ---
  duration_ms: 0.390034
  ...
# Subtest: a mixed setting-plus-property clear dry-runs first, and a refused preview never applies
ok 416 - a mixed setting-plus-property clear dry-runs first, and a refused preview never applies
  ---
  duration_ms: 1.071886
  ...
# Subtest: Ctrl+D on a ghost is a no-op and parent clear stays refused
ok 417 - Ctrl+D on a ghost is a no-op and parent clear stays refused
  ---
  duration_ms: 1.502809
  ...
# Subtest: confirmed merge never copies a dry-run candidate contract onto the live report
ok 418 - confirmed merge never copies a dry-run candidate contract onto the live report
  ---
  duration_ms: 0.295775
  ...
# Subtest: a generic setting stage paints its notes above the preview and Save/Cancel
ok 419 - a generic setting stage paints its notes above the preview and Save/Cancel
  ---
  duration_ms: 1.461099
  ...
# Subtest: Review shows its residence scope once even when Bob's effect repeats it
ok 420 - Review shows its residence scope once even when Bob's effect repeats it
  ---
  duration_ms: 1.224388
  ...
# Subtest: caller keys map onto their logical setting id
ok 421 - caller keys map onto their logical setting id
  ---
  duration_ms: 1.75446
  ...
# Subtest: area and project register after the builtins with bank precedence
ok 422 - area and project register after the builtins with bank precedence
  ---
  duration_ms: 5.286635
  ...
# Subtest: registry setup is idempotent and teardown removes only area and project
ok 423 - registry setup is idempotent and teardown removes only area and project
  ---
  duration_ms: 0.498562
  ...
# Subtest: day notes keep the temporal extension while area and project coexist
ok 424 - day notes keep the temporal extension while area and project coexist
  ---
  duration_ms: 2.513269
  ...
# Subtest: == and Settings open the editor on the first settings row
ok 425 - == and Settings open the editor on the first settings row
  ---
  duration_ms: 0.604094
  ...
# Subtest: a setting request selects its row on reconcile, even for ghosts
ok 426 - a setting request selects its row on reconcile, even for ghosts
  ---
  duration_ms: 8.644073
  ...
# Subtest: a bare first-settings request selects the first settings row once
ok 427 - a bare first-settings request selects the first settings row once
  ---
  duration_ms: 4.106389
  ...
# Subtest: a requested setting pre-selects its declared source row while loading
ok 428 - a requested setting pre-selects its declared source row while loading
  ---
  duration_ms: 1.045716
  ...
# Subtest: a degraded report selects the corresponding real property, else the safe first row
ok 429 - a degraded report selects the corresponding real property, else the safe first row
  ---
  duration_ms: 1.497309
  ...
# Subtest: policy chips and Settings route through homeCardOpenSetting by setting id
ok 430 - policy chips and Settings route through homeCardOpenSetting by setting id
  ---
  duration_ms: 0.961126
  ...
# Subtest: openPropertyEditor forwards setting requests and maps keys in browse mode
ok 431 - openPropertyEditor forwards setting requests and maps keys in browse mode
  ---
  duration_ms: 1.171647
  ...
# Subtest: browse = inside an area or project editor focuses settings without reopening
ok 432 - browse = inside an area or project editor focuses settings without reopening
  ---
  duration_ms: 4.586859
  ...
# Subtest: project task rows hand off to the Task Card at the validated ^prj line
ok 433 - project task rows hand off to the Task Card at the validated ^prj line
  ---
  duration_ms: 1.483041
  ...
# Subtest: project status rows navigate only, without writing
ok 434 - project status rows navigate only, without writing
  ---
  duration_ms: 0.669107
  ...
# Subtest: a stale ^prj line refuses instead of landing on another task
ok 435 - a stale ^prj line refuses instead of landing on another task
  ---
  duration_ms: 0.539269
  ...
# Subtest: an editor that disagrees with the vault refuses the handoff
ok 436 - an editor that disagrees with the vault refuses the handoff
  ---
  duration_ms: 0.473945
  ...
# Subtest: a missing Task Card falls back to the cursor without writing
ok 437 - a missing Task Card falls back to the cursor without writing
  ---
  duration_ms: 0.470358
  ...
# Subtest: an absent ^prj reports absence without creating anything
ok 438 - an absent ^prj reports absence without creating anything
  ---
  duration_ms: 0.614543
  ...
# Subtest: a closed project still navigates to its ^prj line
ok 439 - a closed project still navigates to its ^prj line
  ---
  duration_ms: 0.461722
  ...
# Subtest: a project not shown in any pane opens before its ^prj line is validated
ok 440 - a project not shown in any pane opens before its ^prj line is validated
  ---
  duration_ms: 0.70169
  ...
# Subtest: a project that still cannot be shown refuses without touching another note
ok 441 - a project that still cannot be shown refuses without touching another note
  ---
  duration_ms: 0.588684
  ...
# Subtest: the contract capability requires a complete, correctly ordered, kind-matched block
ok 442 - the contract capability requires a complete, correctly ordered, kind-matched block
  ---
  duration_ms: 4.144214
  ...
# Subtest: show and update decoders retain contract, effects, and warnings without making them required
ok 443 - show and update decoders retain contract, effects, and warnings without making them required
  ---
  duration_ms: 2.01662
  ...
# Subtest: area settings use report order and stable IDs; source rows stay in their own groups
ok 444 - area settings use report order and stable IDs; source rows stay in their own groups
  ---
  duration_ms: 6.153889
  ...
# Subtest: bank ignores the old hybrid settings contract and keeps its card handoff row
ok 445 - bank ignores the old hybrid settings contract and keeps its card handoff row
  ---
  duration_ms: 0.538899
  ...
# Subtest: project task rows carry current line text and become unavailable without a current task
ok 446 - project task rows carry current line text and become unavailable without a current task
  ---
  duration_ms: 1.40329
  ...
# Subtest: project virtual rows hand off to the Task Card at the current ^prj line
ok 447 - project virtual rows hand off to the Task Card at the current ^prj line
  ---
  duration_ms: 1.665991
  ...
# Subtest: missing required parent stays a ghost warning with no inherited value
ok 448 - missing required parent stays a ghost warning with no inherited value
  ---
  duration_ms: 0.386438
  ...
# Subtest: settings selection survives clear reconciliation and filtering includes setting identity
ok 449 - settings selection survives clear reconciliation and filtering includes setting identity
  ---
  duration_ms: 4.29486
  ...
# Subtest: managed rows stay folded, preserve return focus, and clear marks when hidden
ok 450 - managed rows stay folded, preserve return focus, and clear marks when hidden
  ---
  duration_ms: 1.920367
  ...
# Subtest: settings and virtual rows paint as non-source rows with a faint, legible ghost state
ok 451 - settings and virtual rows paint as non-source rows with a faint, legible ghost state
  ---
  duration_ms: 1.22559
  ...
# Subtest: expanded managed rows show Bob's reason or writer; other rows add no label
ok 452 - expanded managed rows show Bob's reason or writer; other rows add no label
  ---
  duration_ms: 1.151569
  ...
# Subtest: done_tasks opens its archive link without mutating the property
ok 453 - done_tasks opens its archive link without mutating the property
  ---
  duration_ms: 0.626988
  ...
# Subtest: YAML escape from synthetic rows targets only real source keys or exact project lines
ok 454 - YAML escape from synthetic rows targets only real source keys or exact project lines
  ---
  duration_ms: 1.400695
  ...
# Subtest: setting activation and unsupported direct actions never issue generic writes
ok 455 - setting activation and unsupported direct actions never issue generic writes
  ---
  duration_ms: 1.991974
  ...
# Subtest: clear maps a declared setting to one setting.clear and a ghost to a no-op
ok 456 - clear maps a declared setting to one setting.clear and a ghost to a no-op
  ---
  duration_ms: 1.660911
  ...
# Subtest: a batch clears settings and unsets loose properties once, while protected rows refuse the whole batch
ok 457 - a batch clears settings and unsets loose properties once, while protected rows refuse the whole batch
  ---
  duration_ms: 1.677402
  ...
# Subtest: disabled settings and project virtual rows are read-only through direct delete
ok 458 - disabled settings and project virtual rows are read-only through direct delete
  ---
  duration_ms: 0.788065
  ...
# Subtest: copy selection resolves legacy aliases and both clock source keys, and refuses ghosts or mixed virtual rows
ok 459 - copy selection resolves legacy aliases and both clock source keys, and refuses ghosts or mixed virtual rows
  ---
  duration_ms: 1.438296
  ...
# Subtest: ghost copying teaches without reading a source snapshot or writing
ok 460 - ghost copying teaches without reading a source snapshot or writing
  ---
  duration_ms: 0.604714
  ...
# Subtest: degraded old-Bob and damaged-frontmatter reports keep generic rows without synthetic settings
ok 461 - degraded old-Bob and damaged-frontmatter reports keep generic rows without synthetic settings
  ---
  duration_ms: 0.793786
  ...
# Subtest: declared setting copy writes its hidden source keys through the fresh-report reconcile
ok 462 - declared setting copy writes its hidden source keys through the fresh-report reconcile
  ---
  duration_ms: 5.595082
  ...
# Subtest: group rows keep source order and duplicate keys stay separate
ok 463 - group rows keep source order and duplicate keys stay separate
  ---
  duration_ms: 2.933522
  ...
# Subtest: empty values stay distinct in row text
ok 464 - empty values stay distinct in row text
  ---
  duration_ms: 0.374044
  ...
# Subtest: roles gate every action and unresolved never becomes loose
ok 465 - roles gate every action and unresolved never becomes loose
  ---
  duration_ms: 0.498202
  ...
# Subtest: header handles every wire note kind
ok 466 - header handles every wire note kind
  ---
  duration_ms: 0.483804
  ...
# Subtest: degraded states carry verbatim copy and write gates
ok 467 - degraded states carry verbatim copy and write gates
  ---
  duration_ms: 0.738069
  ...
# Subtest: cache rows never authorize a mutation
ok 468 - cache rows never authorize a mutation
  ---
  duration_ms: 0.264896
  ...
# Subtest: browse keys map and typing stays native
ok 469 - browse keys map and typing stays native
  ---
  duration_ms: 0.679056
  ...
# Subtest: close ladder parks menu, stage, and reserved filter before the modal
ok 470 - close ladder parks menu, stage, and reserved filter before the modal
  ---
  duration_ms: 0.207527
  ...
# Subtest: modal reconciles without losing selection and closes cleanly
ok 471 - modal reconciles without losing selection and closes cleanly
  ---
  duration_ms: 4.080761
  ...
# Subtest: browse focus follows the selected source row after repaint: first / second
ok 472 - browse focus follows the selected source row after repaint: first / second
  ---
  duration_ms: 1.04243
  ...
# Subtest: browse focus follows the selected source row after repaint: duplicate / duplicate
ok 473 - browse focus follows the selected source row after repaint: duplicate / duplicate
  ---
  duration_ms: 0.241962
  ...
# Subtest: an empty editor focuses its browse host so the first add receives keyboard input
ok 474 - an empty editor focuses its browse host so the first add receives keyboard input
  ---
  duration_ms: 0.285745
  ...
# Subtest: opening the value stage transfers browse focus to its input
ok 475 - opening the value stage transfers browse focus to its input
  ---
  duration_ms: 0.35096
  ...
# Subtest: opening the name stage transfers browse focus to its input
ok 476 - opening the name stage transfers browse focus to its input
  ---
  duration_ms: 0.238646
  ...
# Subtest: browse host returns focus to a row after deletion reconciliation
ok 477 - browse host returns focus to a row after deletion reconciliation
  ---
  duration_ms: 0.668998
  ...
# Subtest: browse host returns focus to a row after the initial report
ok 478 - browse host returns focus to a row after the initial report
  ---
  duration_ms: 0.505595
  ...
# Subtest: discrete ops build exact envelopes and history round-trips
ok 479 - discrete ops build exact envelopes and history round-trips
  ---
  duration_ms: 0.51832
  ...
# Subtest: locked rows refuse discrete actions without spawning
ok 480 - locked rows refuse discrete actions without spawning
  ---
  duration_ms: 0.93763
  ...
# Subtest: paintRow marks selected and locked classes
ok 481 - paintRow marks selected and locked classes
  ---
  duration_ms: 0.985011
  ...
# Subtest: paintRow leaves a loose unselected row without lock or selection classes
ok 482 - paintRow leaves a loose unselected row without lock or selection classes
  ---
  duration_ms: 0.421665
  ...
# Subtest: paintRow keeps the row grid on an inner span
ok 483 - paintRow keeps the row grid on an inner span
  ---
  duration_ms: 0.244908
  ...
# Subtest: property editor shell CSS distinguishes selected and locked rows
ok 484 - property editor shell CSS distinguishes selected and locked rows
  ---
  duration_ms: 3.809783
  ...
# Subtest: source entries keep order, spans, trivia, and value fragments
ok 485 - source entries keep order, spans, trivia, and value fragments
  ---
  duration_ms: 4.177115
  ...
# Subtest: source entries handle BOM, CRLF, and missing final newline
ok 486 - source entries handle BOM, CRLF, and missing final newline
  ---
  duration_ms: 0.482892
  ...
# Subtest: source entries preserve empty, null, false, zero, and coercible text
ok 487 - source entries preserve empty, null, false, zero, and coercible text
  ---
  duration_ms: 0.437785
  ...
# Subtest: source entries support quoted colons, unicode, and numeric-looking keys
ok 488 - source entries support quoted colons, unicode, and numeric-looking keys
  ---
  duration_ms: 0.39811
  ...
# Subtest: source entries keep block scalars, nesting, and duplicates separate
ok 489 - source entries keep block scalars, nesting, and duplicates separate
  ---
  duration_ms: 0.656814
  ...
# Subtest: source entries keep chomping indicators and flow roots
ok 490 - source entries keep chomping indicators and flow roots
  ---
  duration_ms: 0.707561
  ...
# Subtest: source entries mark anchors, aliases, merge keys, and tags unsupported
ok 491 - source entries mark anchors, aliases, merge keys, and tags unsupported
  ---
  duration_ms: 0.423408
  ...
# Subtest: source entries reject missing, unclosed, and non-mapping frontmatter
ok 492 - source entries reject missing, unclosed, and non-mapping frontmatter
  ---
  duration_ms: 0.186496
  ...
# Subtest: source fragments validate keys through the injected parser
ok 493 - source fragments validate keys through the injected parser
  ---
  duration_ms: 0.972437
  ...
# Subtest: clipboard decoder accepts one mapping, optionally wrapped
ok 494 - clipboard decoder accepts one mapping, optionally wrapped
  ---
  duration_ms: 0.900269
  ...
# Subtest: clipboard decoder refuses fences, bodies, duplicates, and opaque input
ok 495 - clipboard decoder refuses fences, bodies, duplicates, and opaque input
  ---
  duration_ms: 0.370267
  ...
# Subtest: source entries attach inter-entry comments to the following entry like prop.move
ok 496 - source entries attach inter-entry comments to the following entry like prop.move
  ---
  duration_ms: 0.42426
  ...
# Subtest: source assembler keeps block bytes and rebuilds flow with braces
ok 497 - source assembler keeps block bytes and rebuilds flow with braces
  ---
  duration_ms: 0.348866
  ...
# Subtest: snapshot reader validates path, inventory, unsaved panes, and cancel
ok 498 - snapshot reader validates path, inventory, unsaved panes, and cancel
  ---
  duration_ms: 1.366429
  ...
# Subtest: stage selection uses only supported props kinds and loose rows
ok 499 - stage selection uses only supported props kinds and loose rows
  ---
  duration_ms: 2.75999
  ...
# Subtest: text and number stages preserve empty strings, null, zero, and finite numbers
ok 500 - text and number stages preserve empty strings, null, zero, and finite numbers
  ---
  duration_ms: 0.621848
  ...
# Subtest: date and datetime stages resolve local tokens, preserve explicit offsets, and reject DST ambiguity
ok 501 - date and datetime stages resolve local tokens, preserve explicit offsets, and reject DST ambiguity
  ---
  duration_ms: 26.995423
  ...
# Subtest: lists keep their shape and values; tags omit \#; aliases stay ordered
ok 502 - lists keep their shape and values; tags omit \#; aliases stay ordered
  ---
  duration_ms: 0.650972
  ...
# Subtest: suggestions read same-key vault values and vault tags in ranked order
ok 503 - suggestions read same-key vault values and vault tags in ranked order
  ---
  duration_ms: 1.852397
  ...
# Subtest: stage painter retains the focused input, caret, and prose band across preview paints
ok 504 - stage painter retains the focused input, caret, and prose band across preview paints
  ---
  duration_ms: 1.184812
  ...
# Subtest: collection stages repaint the typed item draft, never the empty scalar value
ok 505 - collection stages repaint the typed item draft, never the empty scalar value
  ---
  duration_ms: 0.484815
  ...
# Subtest: Enter latches to the exact preview and an edit invalidates the latch
ok 506 - Enter latches to the exact preview and an edit invalidates the latch
  ---
  duration_ms: 6.418443
  ...
# Subtest: selection and stale reports keep drafts but invalidate pending Enter
ok 507 - selection and stale reports keep drafts but invalidate pending Enter
  ---
  duration_ms: 1.09995
  ...
# Subtest: S16 uses the shared proseField API with the note as source and no task subjects
ok 508 - S16 uses the shared proseField API with the note as source and no task subjects
  ---
  duration_ms: 0.657075
  ...
# Subtest: the Summary stage is a soft-line textarea and the counter is unchanged
ok 509 - the Summary stage is a soft-line textarea and the counter is unchanged
  ---
  duration_ms: 2.861924
  ...
# Subtest: a fold note surfaces through the setting notes
ok 510 - a fold note surfaces through the setting notes
  ---
  duration_ms: 0.338967
  ...
# Subtest: Shift+Enter saves on a soft-line Summary and passes through elsewhere
ok 511 - Shift+Enter saves on a soft-line Summary and passes through elsewhere
  ---
  duration_ms: 0.923853
  ...
# Subtest: setDraft during an in-flight write is ignored and the write still lands
ok 512 - setDraft during an in-flight write is ignored and the write still lands
  ---
  duration_ms: 6.670628
  ...
# Subtest: a second write while one is in flight is refused without touching history
ok 513 - a second write while one is in flight is refused without touching history
  ---
  duration_ms: 0.887134
  ...
# Subtest: close during an apply defers until the write settles, then records history
ok 514 - close during an apply defers until the write settles, then records history
  ---
  duration_ms: 0.929545
  ...
# Subtest: close during a failed apply surfaces the refusal without history
ok 515 - close during a failed apply surfaces the refusal without history
  ---
  duration_ms: 0.780901
  ...
# Subtest: two quick undos serialize: the second is refused and history stays exact
ok 516 - two quick undos serialize: the second is refused and history stays exact
  ---
  duration_ms: 1.207315
  ...
# Subtest: a generation change during a write waits for the outcome, then notifies
ok 517 - a generation change during a write waits for the outcome, then notifies
  ---
  duration_ms: 1.118616
  ...
# Subtest: an error envelope never marks bob as old; needs-bob still does
ok 518 - an error envelope never marks bob as old; needs-bob still does
  ---
  duration_ms: 3.893123
  ...
# Subtest: cancel, close, and selection changes refuse visibly while a save runs
ok 519 - cancel, close, and selection changes refuse visibly while a save runs
  ---
  duration_ms: 1.940284
  ...
# Subtest: a rejected apply always clears pendingApply so the modal stays usable
ok 520 - a rejected apply always clears pendingApply so the modal stays usable
  ---
  duration_ms: 1.118035
  ...
# Subtest: onEscapeKey peels the close ladder instead of closing outright
ok 521 - onEscapeKey peels the close ladder instead of closing outright
  ---
  duration_ms: 0.419651
  ...
# Subtest: the yaml action closes the modal first and keeps the key for Done
ok 522 - the yaml action closes the modal first and keeps the key for Done
  ---
  duration_ms: 1.355388
  ...
# Subtest: browse equals opens the owning card editor and explains ordinary notes
ok 523 - browse equals opens the owning card editor and explains ordinary notes
  ---
  duration_ms: 0.658207
  ...
# Subtest: a stale lock wait paints its state and Esc stops the wait
ok 524 - a stale lock wait paints its state and Esc stops the wait
  ---
  duration_ms: 0.443476
  ...
# Subtest: modal sessions register on ensure and unregister on close
ok 525 - modal sessions register on ensure and unregister on close
  ---
  duration_ms: 1.144225
  ...
# Subtest: a vault modify notifies only the session for that path
ok 526 - a vault modify notifies only the session for that path
  ---
  duration_ms: 0.783235
  ...
# Subtest: rename and delete close the open modal and clear dead Done buttons
ok 527 - rename and delete close the open modal and clear dead Done buttons
  ---
  duration_ms: 2.260757
  ...
# Subtest: leaf choice prefers the origin leaf, then the active leaf, then any leaf
ok 528 - leaf choice prefers the origin leaf, then the active leaf, then any leaf
  ---
  duration_ms: 0.501979
  ...
# Subtest: yaml routing takes loose maps and opaque rows, never typed or locked rows
ok 529 - yaml routing takes loose maps and opaque rows, never typed or locked rows
  ---
  duration_ms: 1.849041
  ...
# Subtest: yaml leaves y and Ctrl+E on the Source excursion
ok 530 - yaml leaves y and Ctrl+E on the Source excursion
  ---
  duration_ms: 0.501658
  ...
# Subtest: yaml build emits one prop.set_yaml op and tracks the seed
ok 531 - yaml build emits one prop.set_yaml op and tracks the seed
  ---
  duration_ms: 1.247532
  ...
# Subtest: yaml build passes malformed and injection drafts through for Bob's verdict
ok 532 - yaml build passes malformed and injection drafts through for Bob's verdict
  ---
  duration_ms: 0.236491
  ...
# Subtest: yaml build keeps the null versus empty distinction
ok 533 - yaml build keeps the null versus empty distinction
  ---
  duration_ms: 0.281988
  ...
# Subtest: yaml ordinal counts same-key rows in source order
ok 534 - yaml ordinal counts same-key rows in source order
  ---
  duration_ms: 0.249697
  ...
# Subtest: yaml editor texts read only panes showing the note
ok 535 - yaml editor texts read only panes showing the note
  ---
  duration_ms: 0.51365
  ...
# Subtest: yaml seed keeps block maps, scalars, and nulls byte-exact
ok 536 - yaml seed keeps block maps, scalars, and nulls byte-exact
  ---
  duration_ms: 6.061582
  ...
# Subtest: yaml seed picks the selected duplicate occurrence
ok 537 - yaml seed picks the selected duplicate occurrence
  ---
  duration_ms: 0.652335
  ...
# Subtest: yaml seed marks anchored content opaque with a diagnostic
ok 538 - yaml seed marks anchored content opaque with a diagnostic
  ---
  duration_ms: 0.653107
  ...
# Subtest: yaml seed marks opaque rows for inspection even with plain bytes
ok 539 - yaml seed marks opaque rows for inspection even with plain bytes
  ---
  duration_ms: 0.453867
  ...
# Subtest: yaml seed prefers a differing editor snapshot and refuses to guess
ok 540 - yaml seed prefers a differing editor snapshot and refuses to guess
  ---
  duration_ms: 0.740944
  ...
# Subtest: yaml seed honors cancellation and missing input
ok 541 - yaml seed honors cancellation and missing input
  ---
  duration_ms: 0.463765
  ...
# Subtest: Enter opens the yaml stage for loose maps and keeps typed stages
ok 542 - Enter opens the yaml stage for loose maps and keeps typed stages
  ---
  duration_ms: 3.695115
  ...
# Subtest: the menu route edits another loose value as yaml and refuses locked rows
ok 543 - the menu route edits another loose value as yaml and refuses locked rows
  ---
  duration_ms: 1.152991
  ...
# Subtest: Mod+Enter saves the yaml draft as one set_yaml batch with the preview latch
ok 544 - Mod+Enter saves the yaml draft as one set_yaml batch with the preview latch
  ---
  duration_ms: 4.152299
  ...
# Subtest: an edit after Enter invalidates the pending yaml preview
ok 545 - an edit after Enter invalidates the pending yaml preview
  ---
  duration_ms: 0.80682
  ...
# Subtest: Bob's yaml refusal shows verbatim and keeps the draft
ok 546 - Bob's yaml refusal shows verbatim and keeps the draft
  ---
  duration_ms: 0.81692
  ...
# Subtest: an opaque save surfaces prop_opaque with the draft retained
ok 547 - an opaque save surfaces prop_opaque with the draft retained
  ---
  duration_ms: 0.577944
  ...
# Subtest: stale reports keep the yaml draft but require a new preview
ok 548 - stale reports keep the yaml draft but require a new preview
  ---
  duration_ms: 0.865502
  ...
# Subtest: Esc cancels the yaml stage without closing the modal
ok 549 - Esc cancels the yaml stage without closing the modal
  ---
  duration_ms: 1.96911
  ...
# Subtest: plain Enter inserts a newline while Mod+Enter saves
ok 550 - plain Enter inserts a newline while Mod+Enter saves
  ---
  duration_ms: 0.813073
  ...
# Subtest: undo and redo cover the yaml batch
ok 551 - undo and redo cover the yaml batch
  ---
  duration_ms: 1.408529
  ...
# Subtest: yaml paint uses a multiline textarea with a diagnostic and key hints
ok 552 - yaml paint uses a multiline textarea with a diagnostic and key hints
  ---
  duration_ms: 0.97431
  ...
# Subtest: the All actions menu offers yaml editing and names it in the hints
ok 553 - the All actions menu offers yaml editing and names it in the hints
  ---
  duration_ms: 6.062123
  ...
1..553
# tests 553
# suites 0
# pass 553
# fail 0
# cancelled 0
# skipped 0
# todo 0
# duration_ms 5777.216234

