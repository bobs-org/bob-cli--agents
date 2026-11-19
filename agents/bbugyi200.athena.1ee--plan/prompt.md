#gh:gh_bobs-org__bob-cli Can you help me make the capture panel's sucessor panel work more like the
successor panel in Obsidian?

- Namely, I would like to add a new `<tab>` keymap that selects the current successor
  and then focuses the next one in the list (if any).
- We should keep support for the `<space>` keymap, which does the same thing but without
  focusing the next successor.
- As a part of this change, we should also add a new `<space>` keymap to the Obsidian
  successor panel that is only active when the user has not typed any text (to filter
  the successors shown).

#plan %m:@xlarge