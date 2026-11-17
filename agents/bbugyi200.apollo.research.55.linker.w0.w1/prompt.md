#gh:gh_bobs-org__bob-cli %w:research.55.linker.w0 Can you help me add new `J`/`K` and `1-9` keymaps to
Obsidian when the schema editing cards (supported by album notes, record notes, and the
~/bob/bank.md file) are open in Obsidian?

- The `J` and `K` keymaps should trigger a jump from the current selection to the
  next/previous selection, respectively, that represents a field.
- For example, consider the ~/tmp/screenshots/20261117_110414.png screenshot. In this
  case, if I used the `J` keymap, I would expect my current selection to jump down to
  the "Claim" field.
- The `1-9` keymaps should jump directly to the field associated with that number. To
  support these keymaps, we should start indexing each field selection (starting at 1)
  and showing that index in the schema editing panel somewhere close to its
  corresponding field name.
- Also, as a part of this change, we should add some vertical space before field
  selections (so it is clearer which choices are associated with which fields).
- #beau

#plan %m:@xlarge