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
- #beau

#plan %m:@xlarge %w:research.5v.linker