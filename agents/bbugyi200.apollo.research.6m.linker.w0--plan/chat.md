# Chat History - ace-run (research.6m.linker.w0--plan)

- **TIMESTAMP:** 2026-11-26 16:02:55 EST
- **MODEL:** claude/opus
- **AGENT:** research.6m.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/property_card_cabinets.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/property_card_cabinets.md`

> # Property Card Cabinets
> ## Why
> Area, project, and album notes carry bob-owned catalogs under H2 sections: `## Areas`,
> `## Projects`, `## Notebooks`, `## Albums`, and `## Records`. They push the note's own
> work (`## Tasks`, prose) down the page. Their status is scattered, and each looks
> different from the Property Card above it. Bryan wants these catalogs in **cabinets**:
> named compartments at the bottom of the note's Property Card. Each cabinet holds the
> same data its H2 section held and folds independently.
> The card already has two such compartments in two styles. One is the Properties foot,
> toggled with `-`, which becomes the **property cabinet**. The other is the full-width

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli I would like to start rendering child areas, sub-projects, notebooks, albums,
and records as collapsable sections, which we will name "cabinets", at the bottom of the
property card for the given file instead of in H2 sections. Can you help me implement
this?

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi,
  bob-cli-qj, bob-cli-qm, and bob-cli-qp epic beads.
- These cabinets should contain the same data that the corresponding H2 section used to
  contain.
- Our first cabinet already exists, it is just not named as such. The "property cabinet"
  can be expanded/collapsed via the `-` keymap.
- The collapsible "Schema" widget found on album cards and the bank card should also be
  migrated to a new cabinet (above the property cabinet). I think the only change that
  needs to be made is that the collapsible "Schema" and "Properties" widgets should use
  the same styling.
- The `_` keymap, which already serves to expand/collapse the schema section, should
  continue to serve this purpose, but should have a special behavior when more than one
  cabinet exists above the property cabinet.
  - Namely, the footer should change in Obsidian to show hints for numbers, starting at
    1, that are associated with the cabinets above the property cabinet starting from
    the bottom non-property cabinet (i.e. the one right above the property cabinet,
    which should always be the bottom cabinet).
  - If the user presses one of these numbers (they should also be able to use `<esc>` or
    `<ctrl+[>` to abort), then that cabinet should be expanded/collapsed.
- As a part of this change we should add an excellent new glossary term for "cabinet".
- Review the property_card_cabinets.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.6m.linker

## Response

I'm reading the property-card cabinets research report before planning.

Now checking the bob-plugins code (fold kit, Properties foot, `_` keymap, footer) to ground the plan.

Reading the walker-footer host and the Ctrl+W window-prefix precedent next.

Checking the qm and qp plans for phase file seams before designing the phase graph.

Skimming the swarm reports' proposed phase splits and the home/album card layouts.

Comparing the existing Properties-foot and fold-row styles, which the plan has to unify.

Reading the relevant glossary strands and docs memory, which the plan's memory decisions depend on.

Checking whether all card species share one mount seam where the cabinet stack can be assembled.

Running the plan validator's `--explain` on a stub to get the exact epic schema.

Checking the beads reference memory on whether agents may add cross-epic dependency edges.

Looking at the Properties foot builder to specify the unified header precisely.

Reading the governing decision records the plan will cite.

Verifying two small claims from the research (bank foot keycap, catalog painters' title status) before writing.

I have what I need. Writing the epic plan now.

The validator treats edits to existing glossary strands as one note, so I'm consolidating the memory decisions and adding one ordinary decision about the go-live gate.

Validation passes. Re-reading the full plan once for coherence before proposing.

Plan validates and has no workspace paths. Proposing it now.

I've written the plan as a 9-phase epic, "Property Card Cabinets", and submitted it; it's staged for your review. It passed validation. All the code work is in bob-plugins, and nothing changes in bob-cli code or Bob Mac Capture, so nothing rides the release train.

**One change to the premise (from the research, which you accepted).** The H2 catalogs stay in the Markdown as bob-owned callouts. Cabinets show them inside the card and hide the stored section only while a working cabinet is mounted in that view. Source mode, mobile, embeds, hover, print and any failure show the stored section as today. This keeps every reader of those bytes working (bob's `SUBOPEN`, capture, git, agents).

**Parallel work.** Very little coordination turned out to be needed:
- **bob-cli-qi:** fully closed, so no seam.
- **bob-cli-qj:** no shared code at all.
- **bob-cli-qm and bob-cli-qp:**
  - All cabinet code ships behind a `cabinetsPreview` gate. With it off, their cards render exactly as today, so their acceptance runs and screenshots aren't disturbed.
  - Their in-flight card files are never edited: Schema, Setup, the prose Outline and Properties become cabinets through the shared builders they already call. That removes the research's wait on qm.5.
  - Acceptance runs use isolated scratch vaults, so cabinet acceptance can run alongside qm.6 and qp.7. This corrects the research.
- **The only hold:** switching cabinets on waits for the qm and qp go-lives (qm.7, qp.8), because they also edit `glossary:property-card` and the family docs. The first phase adds bead dependency edges for this, and the go-live phase re-checks them before starting.

**Phase graph.** Three phases start immediately and in parallel: `kit` (the cabinet model, state and a `_` targeting fix), `footer` (the footer overlay) and `absorption` (hiding the stored sections). `chrome` (the shared look) follows `kit`. `keys`, `host-cabinets` and `records-cabinet` then run in parallel, followed by `acceptance` and `go-live`.

**Design choices I made:**
- **Shared look:** every cabinet, Properties included, uses one header row of noun, count and qualifiers, e.g. `Projects · 4 open · 1 blocked · 12 closed`. Sync buttons sit beside the header rather than inside it.
- **Order and defaults:** order is fixed, with content cabinets first, then Schema or Setup, then Properties last. Records starts open; the other content cabinets start closed. Album Schema now starts closed when healthy and opens itself for a new problem.
- **`_` behaviour:**
  - With no cabinet above Properties, `_` keeps the card's details fold.
  - With one, it toggles that cabinet.
  - With two or more, it arms a pick. Digits light on the cabinet headers immediately, and the footer shows them after 150 ms so a fast `_1` doesn't flash it.
  - While armed, `__` picks 1, `-` toggles Properties, and Esc, `q` and Ctrl+[ cancel.
  - Hovering a cabinet header shows its chord (e.g. `_3`).
- **Risk handled first:** the `absorption` phase starts by testing in real Obsidian that Vim motion behaves over hidden ranges. It has a defined fallback (a one-line "in the card above" stub) so it can't get stuck.

**Your decisions at approval:**
- **Wait for qp.8 as well as qm.7?** Defaults to yes; choosing no lets cabinets switch on sooner.
- **Add `glossary:cabinet`?** Defaults to yes, since you asked for it; the plan includes a full draft.
- **Update the property-card, area-card and project-card strands?** Defaults to yes, because cabinets make their current `_` wording false.
- **Add a decision record that cabinets absorb catalogs at render time?** Defaults to no, as it's new guidance you didn't ask for.

The album-card and bank-card strands stay as written: nothing in them becomes false. The go-live phase will note the "Properties cabinet" rewording for them as a proposed follow-up.
