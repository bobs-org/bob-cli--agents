#gh:gh_bobs-org__bob-cli I recently added support for keymaps that are prefixed with `<ctrl+w>` to make
it easier to manage split windows in Obsidian (see the bob-cli-m0 epic bead for
context). I would now like to add support for the new `<ctrl+w>N` keymaps, which should
trigger a jump to the `N`th Obsidian tab. Can you help me implement this?

- `N` should be determined by a hint that is rendered next to each file's name in
  Obsidian's tab title bar.
- The tab that we jump to should remaining in the same vertical window that it was in
  before invoking the `<ctrl+w>N` keymap.
- Review the obsidian_ctrl_w_numbered_tab_jump.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- #beau

#plan %m:@xlarge %w:research.4y.linker