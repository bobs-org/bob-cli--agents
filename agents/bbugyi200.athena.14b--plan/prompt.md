#gh:gh_bobs-org__bob-cli Currently, the bob-mac-capture app's ref panel can be triggered from the
Highlights app via the `<cmd+t>` keymap. The ref panel is filtered to the currently
opened ref note PDFs opened in Highlights when this keymap is used, however, this
implementation has several problems.

- Exiting from the ref panel should not save the ref panel state when it was triggered
  via the `<cmd+t>` keymap.
- When this keymap is used, the currently focused PDF in Highlights should always have
  its ref note selected.
- When this keymap is used, if there are any notes on the current Highlights app, then
  the preview pane in the ref panel should always be automatically scrolled so the
  current page's notes (or the notes closest to the current page) are visible.

Can you help me fix these issues? #plan %m:@xlarge