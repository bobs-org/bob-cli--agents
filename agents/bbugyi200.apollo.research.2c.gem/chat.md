# Chat History - ace-run (research.2c.gem)

- **TIMESTAMP:** 2026-10-24 06:24:39 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.2c.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261024_061232.md`

## Prompt

%id(gem, clan=research.2c)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.2c.cdx`, `research.2c.cld`, `research.2c.grk`, `research.2c.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add much better support for "pomodoro themes" (aka "pomodoro names",
"themes").

- We should add a new glossary term for this.
- We should start suggesting the names of previously used themes anywhere that themes /
  pomodoro names are shown in a completion menu (including the bob-mac-capture app).
- If existing theme / pomodoro names are listed in the same completion menu (and not
  filtered out by the user's query), those should be prioritized (i.e. shown at the top)
  over previously used themes.
- The user should have the ability to rename themes globally (all daily files that use
  that theme should be updated).
- The user also needs to be able to disable a theme, which should result in it no longer
  appearing in completion menus. Think hard about how/where we should support this
  functionality (via a new `<ctrl+d>` keymap in completion menus maybe?).
- Themes should be given a distinct color somehow, which should be deterministic based
  on the theme name. We should try to use these colors anywhere that themes are shown
  (including in Obsidian itself).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: Pomodoro Themes Ecosystem Design

The independent research investigation on **Pomodoro Themes** has been completed by researcher `gem`. The full design and research report has been written to the research sidecar repository and registered as a durable SASE artifact:

- **Absolute Report Path:** [`pomodoro_theme_support_and_styling__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/pomodoro_theme_support_and_styling__gem.md)
- **Repo-Relative Path:** `202610/pomodoro_theme_support_and_styling__gem.md`
- **Durable Artifact ID:** `explicit:10add0f741b8b4618226e23d` (`research:202610/pomodoro_theme_support_and_styling__gem.md`)

---

## Executive Summary of Findings & Recommended Design

### 1. Proposed SASE Glossary Definition
A new glossary strand note has been authored for `sase/memory/glossary/pomodoro-theme.md`:
- **Keyword:** `Pomodoro Theme` (aliases: `pomodoro name`, `theme`, `session theme`).
- **Definition & Syntax:** Formalizes the em dash suffix (` — NAME`) under `## Pomodoros` in daily notes (`YYYY/YYYYMMDD.md`), character constraints (`A-Z`, `0-9`, and `& ' ( ) + , . / -`), and composite split semantics (`BOB + DECKS`).
- **System Distinctions:** Formally defines boundaries separating active themes from triage inventory labels (`LATER`, `MISC`, `NEW FEATURES`) and cap-exempt operational themes (`GTD`).

---

### 2. Critique of Requirements & Key Adjustments

1. **Sub-15ms Completion via a Persistent Theme Index:**
   - *Problem:* Keystroke completion (`bob capture-complete`) runs on every character typed in Bob Mac Capture. Scanning years of historical daily notes on every keystroke would introduce 300–500ms lag.
   - *Adjustment:* Implement a lightweight index at `~/.cache/bob-cli/themes.json` updated incrementally on capture writes and audited during `bob nightly`. Cold vault scan is performed once; warm completion reads the cache in `< 1ms`.

2. **Strict 4-Tier Completion Menu Ranking:**
   - When Bryan types `=#` or `@route:id=#`, completion candidates must be ranked into four strict tiers:
     1. **Tier 1 (Today's Active):** Running, next up, or open planned sessions in today's daily note.
     2. **Tier 2 (Today's Completed):** Sessions finished earlier today (`Again` rows).
     3. **Tier 3 (Historical Themes):** Themes from the cache that are not disabled and not yet planned today, ranked by a weighted recency/frequency score.
     4. **Tier 4 (Create New):** Novel name creation row (`+ Create "NAME"`).

3. **Pivot on `<ctrl+d>` in Completion Menus:**
   - *Problem:* In Bob Mac Capture (a native macOS AppKit/SwiftUI app), `Ctrl+D` is bound by the Cocoa text system to `deleteForward:` (deleting the character to the right). Hijacking `<ctrl+d>` causes users accustomed to standard macOS text navigation to accidentally disable themes while typing. Furthermore, disabling without an undo path creates high anxiety.
   - *Adjustment:*
     - Use a conflict-free secondary shortcut: `<alt+d>` / `<Option+D>` (or `<ctrl+x>`).
     - Display an immediate non-modal undo toast: *"Disabled theme 'SASE'. Press ⌘Z to undo."*
     - Persist disabled themes in `~/.config/bob/config.yml` under `themes.disabled: [...]`.
     - Expose typed CLI commands: `bob theme disable <NAME>` and `bob theme enable <NAME>`.

4. **Composite-Aware Global Theme Renaming (`bob theme rename`):**
   - Implements `bob theme rename <OLD_NAME> <NEW_NAME>` with `--dry-run` and `--format json`.
   - Uses strict regex and AST boundaries around ` — ` and ` + ` delimiters to avoid corrupting substrings (e.g., renaming `BOB` will never alter `BOBCAT`).
   - Safely preserves composite theme pairings: renaming `BOB` to `BOB-CLI` converts `BOB + DECKS` to `BOB-CLI + DECKS`.

5. **Deterministic Theme Colors via a Curated 16-Hue Harmonic Palette:**
   - *Problem:* Continuous HSL (`hash % 360`) generates muddy yellows, unreadable pastels, and poor light/dark contrast.
   - *Adjustment:* Map the theme name via 32-bit FNV-1a hash to an index in a calibrated 16-hue designer palette with hand-tuned Light-Mode and Dark-Mode hex values (guaranteeing WCAG AA contrast).
   - *Cross-Platform Styling:*
     - **Obsidian:** A CodeMirror 6 `MatchDecorator` transforms ` — THEME` in daily notes into an inline pill widget `.bob-theme-pill`.
     - **Bob Mac Capture:** Renders theme color dots in completion rows and tinted capsules in the agenda banner.
     - **CLI:** ANSI 24-bit RGB truecolor escape sequences in `bob capture-pomodoros`, `bob plan`, and `bob theme list`.
     - **Mac Menu Bar Indicator:** Tinted session bullet in `mac pom` (`pomodoro_countdown.lua`).

---

## Multi-Repo Implementation Plan

| Repository | Scope & Touched Components |
| :--- | :--- |
| **`bob-cli`** | Add `src/native/themes/` (cache, CLI subcommands), `src/native/theme_color.rs` (FNV-1a palette), enrich `PomodoroNameCandidate` in [`capture_complete/pomodoros.rs`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/src/native/capture_complete/pomodoros.rs), and add `bob theme rename/disable/enable`. |
| **`bob-mac-capture`** | Update `CompletionRowContent.swift` and `CaptureModels.swift` to decode `color_hex` and `is_historical`; add theme color dots in `CapturePickerRowView.swift`; wire `<Option+D>` and ⌘Z undo in `CapturePanelModel.swift`. |
| **`bob-plugins`** | Add CM6 theme pill decorator for `## Pomodoros` lines; update [`PomodoroLinkPickerModal`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/linked/bob-plugins/plugins/block-id-prompt/src/085-pomodoro-link-picker-modal.js) and `PomodoroEntryMovePickerModal` with historical themes and color dots. |

For the complete technical breakdown, mathematical formulas, and schema specifications, please see the registered report: [`pomodoro_theme_support_and_styling__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_17/sase/repos/research/202610/pomodoro_theme_support_and_styling__gem.md).
