# Chat History - ace-run (research.3i.gem)

- **TIMESTAMP:** 2026-11-06 10:48:47 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3i.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261106_103445.md`

## Prompt

%id(gem, clan=research.3i)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3i.cdx`, `research.3i.cld`, `research.3i.grk`, `research.3i.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We recently added support for using `-` / `=` instead of `~` in some cases in the
bob-mac-capture app; however, there are still a few problems with the way the
bob-mac-capture app handles task relations (i.e. the `~foo:bar` capture syntax). There
are also some ways we can improve the way this app handles these relations in general.
Can you help me fix these issues / make these improvements?

- I think we should make the `=` character the only alias for `~` when appropriate since
  I don't think the `=` capture syntax is ever needed in the same context where we would
  want to trigger the task relation menu.
- The `~` or `=` character should be able to be typed after `~foo:bar` style links to
  automatically trigger a transformation to `~~foo:bar` (the reverse transformation
  should also be supported).
- Make sure that we can escape the `=` sign (anywhere that we use it as an alias for
  `~`) by pressing `==` fast enough.
- When `~` or `=` is pressed in the task relation panel, we already properly toggle
  between "link to" and "linked from", but we should also do this in the task relation
  label panel. This way, if I realize the relation is pointing the wrong way when I go
  to pick a label (which has happened several times), then I have an easy way to toggle
  the direction.

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

# Research Report: Task Relation Equals Alias & Direction Toggle Improvements

**Report File:** [`task_relation_equals_alias_and_direction_toggle__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202611/task_relation_equals_alias_and_direction_toggle__gem.md)  
**Durable Artifact Snapshot:** `research:202611/task_relation_equals_alias_and_direction_toggle__gem.md` (`file:explicit:1457a909efc4829e67a64b78`)

---

## Executive Summary & Critique

Your proposed plan to improve task relation handling in `bob-mac-capture` and `bob-cli` is **conceptually sound, ergonomic, and eliminates notable friction points and technical debt**. 

Specifically:
1. **Making `=` the sole alias for `~` (and retiring `-`)**: **Strongly Recommended.** The recent `-` alias experiment in commit `591e4ed` introduced severe false-positive collisions with ordinary prose (spaced hyphens, en-dashes, subtraction/math, sub-bullets, and CLI flags), necessitating fragile restore-arm heuristics (`CaptureRelationDashArm`). In contrast, an audit of the Bob capture grammar reveals that a space followed by `=` in a task body is *never* valid capture syntax.
2. **Post-link direction toggle (`~` or `=` after `~foo:bar`)**: **Recommended with one vital constraint.** The toggle must require the trigger to be **glued** directly to the relation token (`~foo:bar=` or `~foo:bar~`). If whitespace were permitted between the token and the trigger (`~foo:bar =`), it would conflict with Bob's support for multiple relations on a single task (`~foo:bar ~baz:qux`).
3. **Escaping `=` via fast `==`**: **Recommended.** Following the established double-tap precedent in `bob-mac-capture` (where `\\` escapes the `#` alias to yield a single literal `\`), typing `==` quickly must escape to a **single literal `=`** (`let x = `) rather than `==`, closing/cancelling any opened relation picker.
4. **Direction toggle in the Task Relation Label Panel**: **Strongly Recommended.** When picking or viewing relation labels, users frequently realize the relationship direction was created backwards (e.g., "depends on" vs. "blocks"). Allowing `~` or `=` to toggle direction in place without closing the label panel or losing typed query text eliminates significant workflow friction.

---

## Analysis of the Four Requirements

### 1. Make `=` the Sole Alias for `~` (Retiring `-`)
* **Grammar Audit**: In Bob, `=` is used for item-initial Pomodoro operations (`=bugs`, `=/`, `=*`, `=3`, `=-2`), glued task link suffixes (`^task=`, `@task=bugs`), and past pomodoro tokens (`x=3!`). In task body prose, a standalone `=` preceded by whitespace is never capture syntax.
* **Why Retiring `-` is Justified**: In prose, `-` is heavily overloaded. Retiring `-` allows deleting `CaptureRelationDashArm`, `relationDashRestoreCommand`, and `restoreRelationDashLiteral`, significantly simplifying keyboard routing.
* **Backend Rewrite**: In `src/native/capture_language/rewrite.rs`, remove `expand_relation_dash_alias` and introduce `expand_relation_equals_alias` that expands `=` preceded by whitespace to `~` when in `CompletionContext::RelationTo`.

### 2. Post-Link Direction Toggle (`~` or `=` after `~foo:bar`)
* **Glued Requirement**: Block IDs and note stems never contain `~` or `=`. Therefore, `~note:id=` and `~note:id~` are 100% unambiguous syntax errors today.
* **Symmetry**:
  - `~note:id=` and `~note:id~` -> `~~note:id`
  - `~~note:id=` and `~~note:id~` -> `~note:id`
  - Labelled relations: `~note:id|label=` -> `~~note:id|label`
* **Implementation Precedent**: Mirrors `switch_block_id_separator` in `bob-cli` (`capture-rewrite`). The trigger key is consumed, the prefix is toggled, and the cursor lands at the end of the unchanged identifier/label.
* **Picker Trailing Space Interaction**: When accepting a relation row at the end of a draft, the picker appends a space (`~note:id `). To flip a relation from the editor after accepting, the user presses `Backspace` once to delete the space, then `=` or `~`. (Alternatively, Requirement 4 allows toggling directly inside the picker or label panel *before* accepting).

### 3. Escaping `=` via Fast `==`
* **Escape Semantics**: Double-tapping `=` fast produces a **single literal `=`** (`let x = `) and closes/cancels the relation picker. If a user needs `==` (e.g. equality in code or Obsidian highlight `==text==`), a third tap (`===`) appends the second `=`.
* **Dual-Race Implementation** (matching `HashAliasProbe` and `hashAliasLiteralArm`):
  1. *Keystroke 2 arrives before Bob's rewrite reply*: `noteEqualsAliasBeforeReply` records an `EqualsAliasProbe`, suppresses the rewrite, replaces the draft with a single literal `=`, and dismisses completion.
  2. *Keystroke 2 arrives after Bob's rewrite reply*: `equalsAliasLiteralArm` intercepts the second `=`, restores the literal `=`, and dismisses the relation picker.

### 4. Direction Toggle in the Task Relation Label Panel
* **UX Mechanics**: In `relationLabelPromptCommand`, intercept unmodified `~` and `=` (when rename mode is not active):
  - Invert `prompt.direction` (`.linksTo` <-> `.linkedFrom`).
  - In `plainDraft` and `prompt.draftSnapshot`, insert or remove one tilde at `prompt.tokenRange.start` (`~` <-> `~~`).
  - Shift `tokenRange`, `labelRange`, and `restoreCursor` by `+1` or `-1`.
  - The live sentence preview (`relationLabelSentenceSource` and `relationLabelSentenceTarget`) instantly swaps subject and object:  
    `“Owner task” [label] “Target task”` <-> `“Target task” [label] “Owner task”`.
  - The typed label query text and input focus remain undisturbed (note that `~` is already a forbidden character in relation labels in Bob).

---

## Gesture Summary Table

| Context | Typed Gesture | Resulting Action | Draft Result |
| :--- | :--- | :--- | :--- |
| Task body prose | `foo =` | Expands `=` to `~`, opens Links To picker | `foo ~` |
| Task body prose | `foo ==` (fast) | Escapes alias, cancels picker | `foo =` |
| Open relation picker | `~` or `=` | Flips direction Links To ↔ Linked From in place | `~` ↔ `~~` |
| Relation label panel | `~` or `=` | Flips direction in place, live-updates sentence | `~note:id` ↔ `~~note:id` |
| Editor draft (glued) | `~note:id=` | Rewrites relation to Linked From | `~~note:id` |
| Editor draft (glued) | `~~note:id=` | Rewrites relation to Links To | `~note:id` |
| Editor draft (glued) | `~note:id~` | Rewrites relation to Linked From | `~~note:id` |
| Editor draft (glued) | `~~note:id~` | Rewrites relation to Links To | `~note:id` |

---

## Recommended Next Steps

1. **`bob-cli`**:
   - Retire `expand_relation_dash_alias` and add `expand_relation_equals_alias` in `src/native/capture_language/rewrite.rs`.
   - Implement `switch_relation_direction` rule for glued `~` and `=` after completed relation tokens.
   - Update tests in `tests/cli/capture/rewrite.rs` and documentation in `docs/capture.md`.
2. **`bob-mac-capture`**:
   - Remove `CaptureRelationDashArm` and relation dash restore routing.
   - Add `equalsAliasLiteralArm` and double-tap probe handling in `CapturePanelModel.swift` and `CapturePanelController.swift`.
   - Add `.flipRelationLabelPromptDirection` in `CaptureKeyCommandRouter.swift` and `CapturePanelModel.swift`.
   - Update `docs/relationship-pickers.md` and `docs/protocol.md`.
