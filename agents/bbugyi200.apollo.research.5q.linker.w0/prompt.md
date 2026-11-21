#gh:gh_bobs-org__bob-cli When I review bank rows in the morning, sometimes I would like to leave a note
on one of them (to clarify what the purchase was or why it was made, for example). I
think we can accomplish this via a new `<space>` keymap in the bank row category picker
panel that prompts the user for a note. Can you help me implement this?

- This note should then be added to the bank row in some visually appealing way without
  progressing to the next bank row in the bank row walk.
- Review the bank_row_note_stage.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.5q.linker