# Chat History - ace-run (research.5v.linker.w0--plan)

- **TIMESTAMP:** 2026-11-22 13:35:44 EST
- **MODEL:** claude/opus
- **AGENT:** research.5v.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/card_owned_frontmatter.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/card_owned_frontmatter.md`

> # Plan: Property cards own the frontmatter
> This epic turns the research consensus in
> `research:202611/card_owned_frontmatter/card_owned_frontmatter.md` into six phases.
> Bryan accepted every requirement that research recommends, including adjustments R1–R7
> and resolutions D1–D8. Memory edits are the only exception: they happen only through the
> memory decisions above. Each phase below is self-contained. Read the research report
> with
> `sase artifact read research:202611/card_owned_frontmatter/card_owned_frontmatter.md "<why>"`
> when a phase needs the reasoning behind a rule. Its sibling `__gem.md` §4.4 lists the
> YAML byte-safety invariants this plan turns into `bob props` tests.

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like for property cards to start taking over all properties defined in
that file's frontmatter. Can you help me implement this?

- We should stop showing the built-in Obsidian "Properties" section for these notes
  completely.
- Instead, a read-only collapsable (collapsed by default) view of these properties
  should be able to be found at the bottom of the property card (it should be a part of
  the card).
- We should add a new `=-` keymap that allows me to expand/collapse this properties
  section of the property card.
- We should also add support for editing these properties via a new property editor,
  which should be triggered by a new `=+` keymap. This property editor should be at
  least as powerful as Obsidian's builtin "Properties" header (ideally more so and much
  easier to use via the keyboard).
- We should attemmpt to represent the `created` property somewhere concisely on all
  property cards even when the properties section of the card is collapsed.
- Review the card_owned_frontmatter.md file in the research sidecar repo for context and
  inspiration before planning. I agree with all of the requirements recommended in that
  research file (except for any sase memory file changes, which should only be
  implemented if I approve them or explicitly asked for them in this prompt), but keep
  in mind that you are responsible for planning and splitting up this work
  appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5v.linker

## Response

Reading the research report and exploring the property-card code in bob-plugins next.

Exploring the property-card kit, `==` gate, record sheet, and day/period card code in bob-plugins.

Now the bob-cli side: `yaml_spans.rs`, the records update protocol, and the CLI/docs rules.

Still mapping bob-cli's CLI registration and the records update writer so the `bob props` phase is grounded.

Checking how `periods update` takes the vault lock (the closest analog for a generic-note writer), then the relevant glossary/decision records.

Reviewing gem's YAML-safety invariants (they become `bob props` acceptance tests in the plan).

Checking how bob's command catalog classifies envelope writers like `records update` (a new `bob props` would need the same treatment).

I have enough grounding on the code. Since the plan would leave the `Property Card` and `Record Card` glossary strands false, I need the memory-write skill to author that decision correctly.

I have the full picture. Checking the epic plan schema before authoring.

Validator schema understood (max 5 decisions; memory decisions last). Writing the epic plan now.

Fixing a typo and adding the required `phases:` list, then validating with `--explain`.

The memory selectors resolved to the same note; trying the strand-path form.

The validator treats strand selectors in one web as one note, so I'll merge the two glossary corrections into a single memory decision.

Validation passes. Submitting the plan.

I've written the plan and submitted it for your review. It is an epic with six phases, and nothing has been implemented yet. It follows the research report's recommendations, with one addition of my own: native Properties only hides once your installed bob can write properties.

**How it will look and work**
- **Foot row:** every card ends in one quiet line, below the nav rail, so opening it never moves the Previous/Next arrows. The left side reads `▸ Properties · 14` and the right side shows the `created` stamp. It stays visible when the card is collapsed.
- **`created` stamp:**
  - On a daily note created that same day, it shows only the time (`created 6:43 AM`), because the title already gives the date.
  - Other day, week, quarter and year cards use absolute dates, never "yesterday".
  - It never invents a date from file times. A missing value shows nothing on dated cards and a faint `no created date` on album and record cards.
- **`=-` drawer:** read-only and collapsed by default. It lists every key in file order, in three groups:
  - keys the card doesn't show anywhere else;
  - keys the card already shows, each marked with where it appears (title, field, summary…);
  - bob-managed keys like `*_digest` and `zorg_*`, in a closed sub-section.
- **`=+` editor:** works on any Markdown note, using the same modal style as the record editor.
  - Each key goes to exactly one place for editing:
    - most keys are edited right in the editor;
    - keys a card already edits hand off to that card's `==` editor;
    - keys bob computes itself are locked, with a one-line reason.
  - Rows use Obsidian's own property-type icons.
  - It covers everything native Properties can do: add with vault-wide name completion, rename, reorder, delete, multi-select, copy/paste as YAML, and change type. It adds filtering, multi-step undo/redo, and a YAML editor for nested values, which native Properties can't edit at all.
- **Hiding native Properties:** it disappears on card notes and comes back on every failure path (Source mode, embeds, bad YAML, plugin unload, and so on).
  - It only hides once your installed bob is confirmed new enough to write properties. That way, a machine with an older bob never loses its only in-document editor.
  - `Mod+;` opens `=+` instead of hitting a hidden widget.
  - The right-sidebar File Properties view stays as the escape hatch.

**Phases**
- `foot-drawer`, `props-cli` and `owns-frontmatter` can run in parallel:
  - **`foot-drawer`:** the foot row, drawer, `created` stamp and `=-`. The record card's existing "N other properties" fold and "added …" line move into it.
  - **`props-cli`:** a new `bob props show|update` command in bob-cli. It rewrites only the lines of the key being changed and leaves the rest of the YAML byte-for-byte as it was.
  - **`owns-frontmatter`:** the hiding mechanism, built but not yet switched on, plus an early test in real Obsidian. That test checks that Vim motions and Tab never land in the hidden Properties block, which the research flagged as the biggest risk.
- **`editor-core`**, then **`editor-parity`:** the `=+` editor, split into the basic editing flow and then the remaining parity and extra features.
- **`takeover`** comes last: it switches on the hiding only after the editor can already do everything native Properties does.

**Decisions waiting for you when you review**
- **Bank card:** I default to giving it the foot row, drawer and `created` stamp. You asked for `created` on all cards; bank.md still keeps its native Properties block, as the research recommended.
- **Drawer memory:** default is per note for the session; the alternative is per pane, so the drawer stays open while you walk `]n` through days.
- **Memory changes:**
  - Correcting the Property Card and Record Card glossary entries defaults to yes, because the takeover would make them false.
  - Adding a new decision record defaults to no, since you didn't ask for it.

Created-date backfill, a single timestamp-offset style for new `created` values, and title cards for area/project/notebook/reference notes are listed as out of scope.
