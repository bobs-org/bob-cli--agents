# Chat History - ace-run (1ag--code)

- **TIMESTAMP:** 2026-11-09 10:41:48 EST
- **MODEL:** claude/sonnet
- **AGENT:** 1ag--code

## Prompt

%model:@small
#gh:gh_bobs-org__bob-cli @plan:202611/capture_alias_glossary_term.md

The above plan has been reviewed and approved. Implement it now.

%macros_enabled:false
Reviewer decisions for this plan (final · reviewer via ACE):
- memory_capture_alias_strand = yes 🧠. Memory edits are authorized for glossary:capture-alias, glossary only. Context: "Should a new glossary:capture-alias strand define Capture Alias and republish the roster?".
No other memory note may be edited.
Implement only the branches selected above.
%macros_enabled:true


## Response

Sources match the draft, so I'm creating the strand now.

I added the Capture Alias glossary term (alias `sigil alias`) and regenerated everything built from the glossary. `bob-docs gen --check` passes, but `just docs-check` fails, and I did not fix that.

**What failed:** the lint step reports three over-budget pages, all under `docs/reference/mac-capture/`:
- `capture-panel.md`: 6020 words
- `capture-previews.md`: 6174 words
- `keyboard.md`: 6029 words

The cap is 6000. I did not touch those files, and they aren't in my diff, so the failure looks like it was already there. I did not run the check on a clean tree to confirm. Fixing it means trimming those pages, which is outside this plan.

**What changed:**
- **New strand:** `sase/memory/glossary/capture-alias.md` covers the single-character substitutions, their escapes, and what is not a capture alias, including the `Command-\` hotkey, route aliases, wikilink `|alias` and `#offclock`.
- **Sources:** before writing I checked the draft against bob-cli's `docs/capture.md` ("Sigil alias") and the Mac app's `docs/keyboard.md`. They matched, so I used the draft unchanged. The strand names no bead IDs.
- **Regenerated, not hand-edited:** `AGENTS.md`, `CLAUDE.md`, `sase/memory/README.md` and `sase/memory/glossary.md`. The roster now reads `Capture Alias (sigil alias)`, between Capture and Command Mode.
- **Public glossary page:** `docs/reference/glossary.md` was regenerated. It also picks up the Project Note Capture term, which was missing before.
- **Closure check:** `sase memory show glossary:capture-alias` pulls in only the Capture family (Capture, Task Link, Task Type, Pomodoro, Task Relation, Project Note, Task Freshness, Task Successor), so there are no incidental matches.
- **Linked references:** the strand has no unresolved-link warnings.

No other memory note, bob-cli source or `bob-mac-capture` file changed. The final declaration is submitted, so the host will commit it after this turn.
