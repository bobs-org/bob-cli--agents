#gh:gh_bobs-org__bob-cli Can you help me make it so the input box (where user's type the contents of
their note/task) in the pop-up triggered by the bob-mac-capture app is only as large as
it needs to be, based on the typed text?

- The input box should start out with a height just large enough to fit a single line of
  input.
- Make sure that this change doesn't cause the completion menu to block the typed text
  or preview.
- Let's add a new `<ctrl+j>` keymap (if this doesn't already work) to allow the user to
  insert a newline, which should increase the input box height accordingly.
- #beau

#plan