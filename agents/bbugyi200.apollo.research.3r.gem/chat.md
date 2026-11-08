# Chat History - ace-run (research.3r.gem)

- **TIMESTAMP:** 2026-11-08 10:45:00 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3r.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261108_102847.md`

## Prompt

%id(gem, clan=research.3r)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3r.cdx`, `research.3r.cld`, `research.3r.grk`, `research.3r.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already support a few different short-hand characters (ex: `,`, `.`, `=`, `;`) that
are auto-replaced with other characters in the bob-mac-capture app in certain contexts.
I would now like to add support for two new similar short-hand characters.

- These characters will be `x` and `s`.
- These will be replaced with `!` and `*` respectively, when used with the `x` syntax.
  For example, typing `xx` should result in `x!` in contexts where the `x` capture
  syntax is respected.
- Similarly, these will be repaced with `!` and `*`, respectively, when used instead of
  the second `=` that is supported by the `x=` capture syntax. For example, typing
  `x=1=s` should result in `x=1=*` in contexts where the `x=` capture syntax is
  supported.

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

# Research Analysis & Recommendation: Shorthand Expansion for Pomodoro Close (`x` → `!` and `s` → `*`)

**Researcher:** `gem` (Independent Swarm Evaluation)  
**Report File:** [`capture_close_shorthand_x_and_s__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/capture_close_shorthand_x_and_s__gem.md)  
**Durable Artifact Snapshot:** `research:202611/capture_close_shorthand_x_and_s__gem.md` (`ref: file:explicit:41f778f44f0945a8a42b9e02`)

---

## 1. Executive Summary & Verdict

The proposal to introduce `x` (auto-replaced with `!`) and `s` (auto-replaced with `*`) in Pomodoro Close contexts is **strongly recommended**, subject to one crucial requirement disambiguation and two architectural safeguards:

1. **High Ergonomic Payoff**: `!` (`Shift + 1`) and `*` (`Shift + 8`) require awkward finger reaches and shift-key chords. In contrast, `x` and `s` are unshifted keys located directly under the left hand on the lower and home rows. Typing `xx` (double-tap) for Complete All and `xs` (smooth home-row roll) for Park All saves substantial physical effort on one of the most frequent daily gestures in Bob.
2. **Critical Disambiguation ("Instead of the second `=`")**: In `x=` past pomodoro grammar, the second `=` **must remain required** (`x=1=s` → `x=1=*`), exactly as demonstrated in your example. Attempting to omit the second `=` (`x=1s` → `x=1=*`) would collide directly with Pomodoro theme names (e.g., `x=1s` is a valid 1-block session with theme `S`, and typing themes like `study` or `sase` would be hijacked).
3. **Architectural Placement (Thin-Client Architecture)**: In accordance with **Decision 10 (`mac-capture-is-a-thin-client`)**, the rewrite rules must be implemented canonically in `bob-cli` under `bob capture-rewrite` (`src/native/capture_language/rewrite.rs`). `bob-mac-capture` acts as a thin client that routes the keystroke intent, invokes `capture-rewrite`, and applies the native AppKit edit.
4. **Typing Performance Guard**: Because `s` is one of the most frequent letters in English (~6.3% of all characters), `bob-mac-capture` must contextually gate recording rewrite intents for `s` and `x` to close-eligible contexts (empty/`x` drafts, or post-delimiter positions) so prose task typing never triggers spurious subprocess calls.
5. **Immediate Return-Key Protection**: Rapid gestures like `xx<Return>` must defer submission until the in-flight rewrite completes, preventing race conditions where raw `xx` could be submitted before expanding to `x!`.

---

## 2. Critique of the Plan

### Why This Is a Good Idea
- **Physical Keyboard Geometry**: Reaching for `Shift + 1` requires stretching the left hand, and `Shift + 8` requires a two-handed chord. In contrast, `xx` is a rapid double-tap with the left index/middle finger, and `xs` is a quick upward flick to the home row.
- **Consistency with Precedent**: Bob already provides an extensive suite of unshifted aliases to avoid awkward chords: `.` → `^`, `;` → `:`, `,` → `+`, `-` → `~` in `x=`, `=` → `~` in relations, and `/` or `\` → `#`. Adding `x` and `s` continues this exact design philosophy.
- **Clear Semantics**:
  - `x!` = Complete All
  - `x*` = Park All
  - `x=1=!` = 1 block, Complete All
  - `x=1=*` = 1 block, Park All

---

## 3. Critical Requirement Adjustments & Disambiguations

### 1. Disambiguating "Instead of the Second `=`"
The prompt stated:
> *"Similarly, these will be repaced with `!` and `*`, respectively, when used instead of the second `=` that is supported by the `x=` capture syntax. For example, typing `x=1=s` should result in `x=1=*` in contexts where the `x=` capture syntax is supported."*

- **The Danger of `x=1s` (Omitting the second `=`)**:
  In Bob's past pomodoro grammar (`src/native/capture_language/past.rs`), unquoted alphabetic characters following digits in `E` represent Pomodoro theme names:
  - `x=1s` parses as: 1 block (5 minutes), theme `"S"`.
  - `x=1study` parses as: 1 block, theme `"STUDY"`.
  - `x=1sase` parses as: 1 block, theme `"SASE"`.
  If typing `s` immediately after `x=1` rewrote to `x=1=*`, any user attempting to log a theme starting with `s` would have their theme hijacked the millisecond they pressed `s`. Furthermore, `x=1!` before the second `=` designates **repair mode**, not complete-all.
- **The Correct Rule**:
  Require the second `=`, as shown in your example `x=1=s` → `x=1=*`. The second `=` cleanly terminates elapsed time and theme entry. In the close specification following the second `=`, letters `s` and `x` have zero legal meaning in raw grammar. Rewriting `s` → `*` and `x` → `!` after the second `=` has **zero syntactic collisions**.

### 2. Recommended Extended Scope: After In-Progress Task Numbers
In both bare close and past close, digits represent task numbers in progress:
- `x1!` means "task 1 in progress, complete all other tasks".
- `x1*` means "task 1 in progress, park all other tasks".
- `x=1=1!` means "1 block, task 1 in progress, complete all other tasks".
- `x=1=1*` means "1 block, task 1 in progress, park all other tasks".

Because letters `x` and `s` immediately following digits in a close list are currently syntax errors, extending the rewrite rule to also handle:
- `x1x` → `x1!` and `x1s` → `x1*`
- `x=1=1x` → `x=1=1!` and `x=1=1s` → `x=1=1*`

creates a completely unified mental model: **`x` always means Complete All and `s` always means Park All anywhere within close syntax.** Subsequent numbers (e.g. typing `2` after `xs` or `x=1=s`) naturally append to form `x*2` or `x=1=*2`.

---

## 4. Recommended Technical Architecture

### 1. `bob-cli` Canonical Implementation (`src/native/capture_language/rewrite.rs`)
In `expand_sigil_alias`, add handling for `alias == "x"` and `alias == "s"`:
- **Bare Close**: If the caret is at `xx` or `xs` at item start, or after valid in-progress task digits (`x<digits>x`, `x<digits>s`), emit a single-character replacement (`x` → `!` or `s` → `*`) with rule `RewriteRule::ExpandSigilAlias`.
- **Past Close**: If the caret is within an `x=` token, the second `=` precedes the alias, and any intervening characters are valid task numbers/commas (`x=...=s`, `x=...=x`, `x=...=<digits>s`, `x=...=<digits>x`), emit the replacement edit.
- **Prose Guard**: In all other contexts (prose tasks, themes like `x=1s`, mid-word text), return `None`.

### 2. `bob-mac-capture` Thin-Client Wiring
- **`CapturePanelController.swift`**: Add `characters == "x" || characters == "s"` to key interception, gated by a fast context check (draft is empty/`"x"`, caret follows `=`, or latest parse is `pomodoro_close`/`pomodoro_past`). This prevents sending rewrite requests on every `s` typed in ordinary task titles.
- **`CapturePanelModel.swift`**: Add `"x"` and `"s"` to `noteSeparatorToggleIntent`.
- **Submit Deferral**: Generalize `deferSubmitForPastSegmentDash` to cover close rewrites so that an ultra-fast `xx<Return>` or `xs<Return>` gesture safely awaits rewrite completion before submitting.
- **Native Undo**: AppKit's native `NSTextView.insertText(_:replacementRange:)` ensures that pressing `Cmd-Z` seamlessly reverts the rewrite.

---

## 5. Artifact & Deliverable Summary

The detailed research report has been published and registered:
- **Report Path:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/capture_close_shorthand_x_and_s__gem.md`
- **Artifact Ref:** `file:explicit:41f778f44f0945a8a42b9e02`
- **Artifact Label:** `research:202611/capture_close_shorthand_x_and_s__gem.md`
- **SASE Final Declaration:** Submitted and accepted for turn completion.
