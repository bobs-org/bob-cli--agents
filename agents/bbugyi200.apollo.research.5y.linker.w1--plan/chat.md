# Chat History - ace-run (research.5y.linker.w1--plan)

- **TIMESTAMP:** 2026-11-22 19:04:13 EST
- **MODEL:** claude/opus
- **AGENT:** research.5y.linker.w1--plan

**Plan:** /home/bryan/.sase/plans/202611/area_project_cards.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/area_project_cards.md`

> <!-- sase:links:start -->
> ## Links
> | Relation | Artifact | Why |
> | --- | --- | --- |
> | derives-from | [research:202611/area_project_property_cards/area_project_property_cards.md][1] | Consolidated research whose recommended requirements Bryan accepted for this epic |
> | related | [plan:202611/card_owned_frontmatter.md][2] | Builds on bob-cli-pf's foot row, drawer, =+ editor, bob props writer, and takeover |
> [1]: https://github.com/bobs-org/bob-cli--research/blob/main/202611/area_project_property_cards/area_project_property_cards.md
> [2]: https://github.com/bobs-org/bob-cli--plans/blob/main/202611/card_owned_frontmatter.md
> <!-- sase:links:end -->
> # Plan: Area and project cards

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Once the bob-cli-pf epic bead is complete, I want to start using property cards
in area notes and project notes. Can you help me implement this?

- Think hard about what these cards should look like and what fields the corresponding
  schema editors (triggered via the `=+` keymap) should support.
- Review the area_project_property_cards.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (except for any sase memory file changes, which
  should only be implemented if I approve them or explicitly asked for them in this
  prompt), but keep in mind that you are responsible for planning and splitting up this
  work appropriately.
- As a part of this change, we should add new glossary terms for "area card" and
  "project card".
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.5y.linker

## Response

Locating the research report in the sidecar repo before reading it.

Reading the 626-line consolidated research report now.

The report is thorough. Next I'm reading the pf epic plan it builds on, plus the relevant memory notes.

Opened bob-plugins; now surveying the property-card kit and species registry there.

Found a second `processFrontMatter` writer on project notes that the research missed (project creation sets `parent`). Checking it and the parent-change stack.

Reading the glossary definitions for cards and area/project notes (output saved to a file).

Still exploring: reading the docs, CLI-rules, and vault memory notes the plan's phases must follow.

Checking how plugin updates reach the other machines, since that affects the count-writer cleanup ordering.

Mockup images aren't readable as artifacts, so I'm reading the cld member report's card and editor design sections instead.

Now checking how the kit draws tile forms, so the area/project tiles fit the existing species.

I have enough design context. Before authoring memory steps into the plan, loading the memory-write skill as required.

Checking a handful of facts the phases will rely on: checkbox marks, the `noteReady` API, palette hues, and catalog sync commands.

Checking where `status: waiting` is still documented, since the research says to retire it from the docs and Bases.

Looking at `projects.base`, which still reads the retired count keys and `waiting`.

Verifying the existing card edit affordance and collapse conventions so the new cards match them.

I have the full picture. Writing the epic plan now.

Fixing a stray typo in §7 before validating.

Validation passes, with two warnings: the new-strand selectors don't match the file paths the body names. Switching them to path selectors.

Path selectors aren't allowed; reverting to keyword selectors and rephrasing the callouts so they don't name raw strand paths.

Validation passes cleanly. The file grew to ~1000 lines, so I'm checking whether the validator reformatted it.

The file is intact (just long). No workspace paths appear in it. Proposing the validated plan.

I've written the plan for area and project cards, and it's staged for your review. Nothing starts until you approve it. It's a nine-phase epic, and no phase begins until `bob-cli-pf` is closed (each phase checks this first and stops if it isn't). It passed validation with no warnings. No product files were changed this turn, only the plan.

**The cards**
- **Shared look:** each card is about five lines. A tile and an `AREA` or `PROJECT` label sit beside a clickable trail of parent notes. Below come the title (first H1, then first alias, then the file name as-is), one subtitle line, a row of chips, and the foot row from `bob-cli-pf`.
- **Area card:** a `layers` tile whose fill shows the note's color, and the `summary:` as subtitle. Inbox notes get an `INBOX` pill.
- **Project card:** a pennant-shaped `target` tile and a `ROOT` pill when `root: true`. The subtitle is the project's state (WIP, SCHEDULED, BLOCKED and why, DONE or CANCELED with a date), never the `^prj` criterion. The `^prj` line stays exactly where it is, slightly emphasized.
- **What paints when:** the state shows immediately from the `^prj` checkbox and its schedule date, since Blocked is already written as `[?]`. The blocked reason and the open/today counts fill in a moment later from the reports the catalogs already load.
- **Chips:** only settings the note declares itself (default type, clock policy, review interval, capture names), plus a Ready count like `2/5 ready`. No dashboard elements, inherited values, or progress bars.

**The settings editor (`=+`, and `==` on these notes)**
- There is no second editor. `=+` gains an `AREA SETTINGS` / `PROJECT SETTINGS` group in a fixed order: Summary, Lives under (parent), Hue, Default type, Clock, Stats root, Ready cap, Review, Capture names.
- A setting the note doesn't declare shows a faint row with the value in effect and where it comes from, e.g. "● blue · from dev". Enter overrides it; Ctrl+D clears a declared setting back to inherit.
- Each setting gets a fitting input. Hue swatches tint the editor header as you browse. Clock is one control with four modes. Changing the parent shows bob's preview of what changes (color, Stats root, catalogs), then refreshes the affected catalogs.
- bob validates every value on every write path, so nothing invalid can be written, and every change is undoable byte-for-byte.

**Phases**
1. `one-writer`: removes the plugin code that rewrites `task_count`/`open_task_count`, sweeps those keys from the vault, updates `projects.base`, and retires `status: waiting`.
2. `contract-writes` and 3. `contract-reads` (bob-cli): the validation, the new setting operations, and what `bob props show` reports.
4. `home-cards`: the cards.
5. `card-live`: the late-arriving state details and counts.
6. `editor-settings`, 7. `editor-policy-stages`, 8. `editor-parent`: the editor work.
9. `takeover`: hides native Properties on these notes, including bank.md (after a quick test that its bank card survives), and makes the glossary edits.

**Where I departed from the research**
- **Second writer:** project creation also rewrites the whole frontmatter (`660-plugin-project-notes.js:58`), which the research missed. Phase 1 fixes it.
- **Retired count keys:** they stay deletable instead of locked, since nothing will maintain them.
- **Stricter takeover:** native Properties only disappears once that machine's bob has the settings validation.
- **Other machines:** after phase 1, athena and the Mac each need `bob plugins sync`. Until then they can re-add the count keys. That's harmless: they show as legacy rows and the cleanup script can be re-run.

**Decisions waiting on you**
- `card_structure_counts` (default off): whether the card also counts sub-areas and sub-projects. I left it off because the catalogs below already show them.
- New "Area Card" and "Project Card" glossary entries (default on, as you asked).
- Correcting the "Property Card" glossary entry, whose species list will be out of date (default on).

No other memory files are touched.
