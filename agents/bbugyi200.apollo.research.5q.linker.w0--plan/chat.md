# Chat History - ace-run (research.5q.linker.w0--plan)

- **TIMESTAMP:** 2026-11-21 11:25:50 EST
- **MODEL:** claude/opus
- **AGENT:** research.5q.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/bank_row_notes.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/bank_row_notes.md`

> # Bank row notes: Space opens a note stage on the Category card
> ## Goal
> During the morning `]b` walk, Bryan wants to leave a short note on a bank row ("why was
> this bought?") without leaving the walk. Space on the bank Category card opens an
> in-card note stage. Enter writes the note into the row's existing inline `— note` tail
> as its own undo step and returns to the same card on the same row: no tick, no advance,
> no session filing. A muted italic caption then shows the note on the row everywhere it
> appears.
> This plan follows the consolidated research report
> `research:202611/bank_row_note_stage/bank_row_note_stage.md`. Bryan agreed with every

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli When I review bank rows in the morning, sometimes I would like to leave a note
on one of them (to clarify what the purchase was or why it was made, for example). I
think we can accomplish this via a new `<space>` keymap in the bank row category picker
panel that prompts the user for a note. Can you help me implement this?

- This note should then be added to the bank row in some visually appealing way without
  progressing to the next bank row in the bank row walk.
- Review the bank_row_note_stage.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5q.linker

## Response

Reading the research file from the sidecar before I explore the code.

Reading the category card UI and stage code next.

Now checking bob-cli's Rust row grammar (the source of truth for notes).

Checking the test layout, CSS build, and docs locations next.

Command Mode discovers commands generically, so the new command needs no extra wiring. Now gauging how much existing test coverage pins Space.

Now reading the docs memory (required before planning docs/ changes) and the Esc/q decision the stage must honor.

I have the core picture. Checking a few remaining touchpoints: the subscription+category write plan, the queue-row render, test harness loading, and Rust consumers of `note`.

Now loading the memory-write skill, since the plan will carry the (approval-gated) memory follow-ups.

I have what I need from the code. One last check on bob-cli's validation commands before writing the plan.

Writing the epic plan now.

Fixing the frontmatter: epic schema needs `title`, `goal`, and a `phases` list, and memory decisions must be `memory:` toggles.

Validation passes with zero warnings. One last sanity check that the plan doesn't name my workspace directory, then I'll propose it.

The plan is staged. Finishing the turn through the finalizer.

I've written a four-phase plan for bank row notes and submitted it for your review. Nothing has been built yet and no files have changed. It follows the research report, including moving "no category" off Space onto `-`.

**How it works on a row:**
```
]b → Ctrl+Enter → card → Space → "LEGO set for Max" → Enter → (same card, note shows) → d → next row
```
- **Space** opens a one-line note box inside the card, right where the note appears under the payee. The category tiles stay visible but dimmed. Enter saves, Esc backs out with nothing written, and `q` types like any other letter.
- **Saving stays on the row.** It doesn't tick the row, move the walk, or count as a filing, and the highlighted suggestion stays put. The note is its own undo step, so Ctrl+Z after filing undoes the filing first, then the note.
- **The same Space key edits a note** (the box opens prefilled) **or removes one** (save it empty; the card says "Removes the note" before you confirm).
- **Other key changes:**
  - `-` now files with no category, or removes the category in "Bank: set category" (Delete does the same there).
  - When categories can't load from bob, Enter acknowledges and Space still writes a note. Enter does nothing while the card is still loading, so a quick Enter can't file a row with no category.
- **A new palette command, `Bank: note this row`,** opens just the note box on any row. It can't go in Command Mode, which only lists bob's own commands.

**How it looks:** the note is stored in the row's existing `— note` text, which bob already reads, lists, and keeps across imports. On the row it shows as muted italic text after a faint em dash, never as a pill. It looks the same in the editor, reading view, the card header and the bank queue view. The note box sits exactly where that caption sits, and after a save the caption glows briefly instead of showing a popup. Notes on ticked rows stay readable.

**Safety:**
- Before saving, the card shows anything in your note it will change, such as links, tags, `!!`, or `[k:: v]`. Each of these would otherwise change the row's meaning: a link would be copied into future imports, `!!` would flag the row. `#task` is refused.
- Every save re-reads the row and checks that only the note changed; otherwise it writes nothing.
- The plan also fixes five existing bugs the research found:
  - bob and the plugin read notes differently: one drops `!`, the other drops dashes inside notes. A shared test table pins both to the same rule.
  - The plugin's idea of where a note starts and ends can overlap the row's other parts.
  - The subscription link gets inserted after a note instead of before it.
  - A `$` inside a note can turn into math formatting.
  - Payee learning gets a test confirming it ignores notes.

**The four phases** run one after another, because each plugin phase rebuilds and redeploys the same plugin:
1. **Parser fixes** (both repos): the shared note rule and the bug fixes above.
2. **Note display:** the caption on every surface.
3. **Note writer:** the save logic and its checks, with no UI yet.
4. **The card:** the new keys, the note box, the palette command, the end-to-end test update and the docs.

Your review has two memory decisions, both off by default as you asked: a decision record for the new keymap, and one sentence added to the Bank Row glossary entry. Turn either on if you want them.

I picked the plain dash-and-italic caption over the research's two fancier options: a 💬 glyph, or an accent-line "margin note" style. It adds nothing new to rows that already carry emoji. Both alternatives are CSS-only changes if you'd rather try one.
