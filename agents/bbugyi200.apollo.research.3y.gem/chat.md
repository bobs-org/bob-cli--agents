# Chat History - ace-run (research.3y.gem)

- **TIMESTAMP:** 2026-11-09 11:14:19 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3y.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261109_110046.md`

## Prompt

%id(gem, clan=research.3y)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3y.cdx`, `research.3y.cld`, `research.3y.grk`, `research.3y.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to display a little hint to the user in the bob-mac-capture app when they
type a character that they could have used a capture alias for.

- For example, if they press `@` to select an area/project note, we should show a hint
  teaching them about the `.` alias.
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

### Research Summary: Capture Alias Discovery Hints in `bob-mac-capture`

As researcher `gem`, I have completed an independent architectural and UX investigation into designing capture alias discovery hints for `bob-mac-capture`.

The full research report has been written, verified, and durably registered:
- **Report Location**: [`sase/repos/research/202611/capture_alias_discovery_hints__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/capture_alias_discovery_hints__gem.md)
- **Durable Snapshot**: `sase artifact create` registered the report as `research:202611/capture_alias_discovery_hints__gem.md` (`file:explicit:d015cf1c161b98ca3e598c2f`).

---

### Key Findings & Plan Critique

#### 1. Is Teaching Aliases a Good Idea?
**Yes, but with strict pedagogical safeguards.**
Bob capture grammar (`src/native/capture_language/rewrite.rs`) defines a set of unshifted aliases for canonical punctuation that normally requires holding Shift:
- `.` for `@` (area/project note route) and `^` (block ID / project task move)
- `/` or `\` for `#` (task type, drawer, heading, Pomodoro name)
- `,` for `+` (parent task picker / target run continuation)
- `=` for `~` (relation / Links To picker)
- `x` for `!` and `s` for `*` (close outcomes)

Because unshifted keys are on the home/bottom row, adopting them significantly accelerates high-velocity GTD capture. However, capture is a low-latency, high-focus workflow. Unsolicited typing hints risk becoming the **"Clippy Anti-Pattern"**—distracting users, causing layout jumping, and patronizing users who intentionally stick with `@` out of longstanding muscle memory.

#### 2. The Syntax Asymmetry Risk
A naive client-side check (*"user typed `@` → suggest `.`"*) is **factually wrong** in several common syntax positions:
- `@inbox` at column 0: `.` is **not** an alias (dot at column 0 is a list bullet or literal period).
- `- @inbox` at bullet-body start: `.` is **not** an alias.
- `- [ ] @inbox` after a bare checkbox: `.` is **not** an alias (`dot_route_alias_position_ok` explicitly refuses).
- Inside code spans or wikilinks: `.` is **not** an alias.

If the app blindly hints `.` in those positions, the user's subsequent `.inbox` capture will fail.

#### 3. Thin-Client Architecture Mandate
Per `decisions:mac-capture-is-a-thin-client`, `bob-cli` is the sole authority on capture grammar. The Swift frontend must **never** evaluate syntax or guess alias eligibility. Instead, `bob-cli`'s `capture-parse` must test whether the alias would have expanded at that exact character offset and emit an additive `alias_hint` payload.

---

### Recommended Solution & Design

#### 1. In-Picker Keycap Badge (Placement)
- **Avoid**: Floating caret popovers (which collide with completion menus and clip against window borders) or inline ghost text.
- **Adopt**: Render the hint directly in the **footer of the completion picker** (`CapturePickerKeyHints` in `CapturePickerView.swift`).
- When the user types `@` and route completion opens, the bottom key hints row displays:
  ```text
  [↑↓] choose   [↵] select   [esc] dismiss
  💡 Tip: [ . ] also opens routes without Shift
  ```
- Uses Bob's native macOS keycap styling: `.font(.caption.monospaced())`, subtle translucent glass background (`Color.primary.opacity(0.08)`), 0.5pt border, and a 4pt corner radius.

#### 2. The Pedagogical State Machine (Fatigue Mitigation)
To prevent annoying the user, the hint adheres to three non-negotiable rules:
1. **Immediate Retirement Upon Use**: When the user types `buy milk .inbox` and Bob expands it via `expand_sigil_alias`, the app records `alias-used.route = true` in `UserDefaults`. Hints for that alias are **permanently disabled**.
2. **Three-Strike Impression Cap**: If a user encounters the hint 3 times without adopting it, hints for that alias are silenced permanently.
3. **Settings Opt-Out**: A toggle in `SettingsView` (`Show typing syntax tips`) allows instant suppression.

#### 3. Backend & Frontend Contract
1. **`bob-cli` (`src/native/capture_language/rewrite.rs`)**:
   Add `available_alias_for_typed_sigil(raw_text: &str, cursor: usize) -> Option<CaptureAliasHint>`. It tests candidate alias expansion through the existing rewrite rules, guaranteeing 100% grammar consistency with zero false positives.
2. **Protocol (`CaptureParseResult`)**:
   Include an additive `alias_hint: Option<CaptureAliasHint>` field.
3. **`bob-mac-capture` (`CapturePanelModel.swift`)**:
   Decodes `aliasHint` from `CaptureParseResponse`, gates presentation against `UserDefaults` exposure counts, and marks adoption upon successful `expand_sigil_alias` rewrites.
