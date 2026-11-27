#gh:gh_bobs-org__bob-cli I would like to add support to area notes, project notes, notebooks, and prose
notes for the link walks (triggered via the `]n` keymap). Can you help me implement
this?

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qq epic
  bead.
- We should render a nice link walk widget at the bottom of the property card like we do
  for other files that support the link walk. As a part of this change we should make
  sure that the link walk widget is always shown at the very bottom of the property card
  (below all cabinets).
- For each of these new supported note types, the walk should only include notes of the
  same type that share the same parent note.
- We should group the members of this walk by their parent.
- As a part of this change we should add an excellent new glossary term for "link walk".
- For example, assume we are in the bar.md project note, which has the foo.md project
  note as its parent which, in turn, has the pig.md area note as its parent. The `]n`
  keymap would then jump to the baz.md file, assuming that is the next (alphabetically)
  project note that has the foo.md project note as its parent.
- I would like to support the `]N` keymap as well, but I'm not sure how the grouping
  would work. Think hard about this. If you can think of an intuitive way to group this
  walk such that the `]N` keymap works, then we should implement it.
- Review the tree_note_link_walks.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.6o.linker