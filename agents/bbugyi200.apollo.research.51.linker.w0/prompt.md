#gh:gh_bobs-org__bob-cli I would like to make the bank/album schema editors much easier / more
convenient to use. Can you help me implement this?

- See the ~/tmp/screenshots/20261116_134836.png screenshot for an example of what the
  album schema editor looks like now.
- For one, we should support excellent emoji completion and filtering when prompting for
  emojis (as shown in the screenshot).
- We should also make it much easier to move fields/choices up/ddown multiple spots with
  a great preview and fast performance (it seems like we can only move them up/down a
  single slot at the moment and it takes a few seconds for the "Apply" button to finish
  applying changes).
- Review the schema_editor_emoji_and_multislot_reorder.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.51.linker