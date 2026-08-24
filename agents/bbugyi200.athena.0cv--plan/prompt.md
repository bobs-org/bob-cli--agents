#gh:gh_bobs-org__bob-cli We recently added support for a global `@@file+id` spec (where `+id` is
optional) to the `bob capture` command and the bob-mac-capture app (see recent, related
git commits). There are a few problems with the design however. Can you help me fix
these issues / make these improvements?

- The syntax shouldn't need to be located on a line by itself at the top of the file.
  Instead, it should be able to be located on any note/task in the capture input at the
  end of any line.
- Let's start making `@@`, if typed anywhere inside a note/task that already has a
  `@file` reference, deletes the other reference and copies it after the `@@` that was
  typed.
- This functionality serves as a convenience so users don't need to manually go back to
  previous lines to delete the previously entered `@file` syntax and also serves as a
  safety net to make sure we don't use `@@file` on a note/task that already uses
  `@file`.
- #beau

#plan