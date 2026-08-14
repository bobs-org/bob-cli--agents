#gh:gh_bobs-org__bob-cli %w:00w.f0.f0 Can you help me add excellent support for sub-bullets to the
tasks/notes that get added by the `bob capture` command?

- We should treat any bullet found after the initial line of input text (which must be a
  single line) as a bullet that should be added as a sub-bullet on the Obsidian
  task/note that we create.
- Make sure that the special markers that we support in capture input (e.g. `@filename`,
  `p:1`, `s:5`, etc...) still work by loosening the restriction that they be placed at
  the end of the input and allowing them to be placed at the end of any line in the
  input (including bullets).
- We should improve the bob-mac-capture app to support this feature:
  - Make the `<ctrl+j>` keymap automatically prepend `- ` to the newline that it
    creates.
  - Pressing backspace on a line containing only `- ` should result in that line being
    completely deleted.
  - Make sure we render these bullets properly in the preview (they should be shown as
    sub-bullets).
- Make sure that when the new task/note is created, that these sub-bullets are added as
  well, with the proper indentation (use the same indentation used by default for
  Obsidian sub-bullets).
- #beau

#plan