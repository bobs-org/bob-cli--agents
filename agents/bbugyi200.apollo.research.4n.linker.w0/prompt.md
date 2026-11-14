#gh:gh_bobs-org__bob-cli I would like to add the new `[b`, `]b`, `[B`, and `]B` keymaps to Obsidian. Can
you help me implement this?

- These keymaps should be used to traverse the bank transactions that have been saved to
  Obsidian (via the `bob bank import` command).
- These keymaps should have their own walker footer associated with them.
- The `[b` and `]b` keymaps should allow me to jump to the next/previous bank
  transaction, respectively. When there are bank transactions that need review, these
  keymaps should only traverse these bank rows. Otherwise these keymaps should traverse
  all bank rows.
- The `[B` and `]B` keymaps should allow me to navigate to the first bank row in the
  previous/next day, respectively.
- Review the bank_walk_family_b.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.4n.linker