#gh:gh_bobs-org__bob-cli We already support opening the corresponding PDF in the Highlights app via the
`<cmd+enter>` keymap when a ref task is selected. I would now like to add support for
this keymap to be used when a quote/annotation in a ref note is selected (we link to
these from tasks created when `#task` is found in annotations). Can you help me
implement this?

- We should jump to the appropriate page in the Highlights app when this keymap is used
  in this context.
- We should make it clear to the user when this keymap is available somehow (do the same
  thing when a ref task is selected).
- Make sure to display an appropriate toast in Obsidian so it is clear (for a moment at
  least) what is happening.
- Review the highlights_annotation_page_jump.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.3o.linker