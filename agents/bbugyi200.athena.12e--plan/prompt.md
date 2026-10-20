#gh:gh_bobs-org__bob-cli Can you help me start remembering the last state of the bob-mac-capture app's
ref panel like we do with its capture panel?

- This should include the current filter state (including showing only active Highlights
  tabs and sorting by capture date and the doc type filters), the currently typed filter
  text, the currently selected ref note PDF, and the current scroll location (so the
  user doesn't lose their place when reading through notes left on this reference).
- To support this change we should add a new `<ctrl+u>` keymap that resets all of these
  states to their defaults (i.e. shows what we currently show when the ref panel is
  first opened).

#plan %m:@xlarge