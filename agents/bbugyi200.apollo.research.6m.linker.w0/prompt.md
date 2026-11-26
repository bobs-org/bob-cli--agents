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
- #beau

#plan %m:@xlarge %w:research.6m.linker