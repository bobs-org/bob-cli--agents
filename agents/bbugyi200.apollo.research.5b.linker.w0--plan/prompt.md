#gh:gh_bobs-org__bob-cli I would like to start automatically adding good `<` and `>` links to all record
notes which point to the previous/next record note in that album. Can you help me
implement this?

- These links should work well with the `[n` and `]n` keymaps.
- This walk should be alphabetical and should cycle around to the next record. For
  example, an album with only two record notes should result in each record containing
  `<` and `>` links that both point to the other record note.
- As a part of this change, we should also start rendering the `N of M` text (or
  something like that) somewhere close to these links where `N` is the current record
  note's index (i.e. position in the walk) and `M` is the total number of record notes
  in that album.
- Review the record_nav_ring.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.5b.linker