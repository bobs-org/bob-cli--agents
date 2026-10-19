#gh:gh_bobs-org__bob-cli Sometimes while I'm reading through a reference note PDF in the Highlights app,
I want to make a single highlight or take a single note (on a highlight) that spans
across pages or across different points in a paragraph. Can you help me implement this?

- The Highlights app does not currently suppot this.
- I want to add support by having the `bob ref` command automatically merge a highlight
  (and its notes) with the previous one (in the corresponding ref note) iff the
  highlight note starts with the `<` character (optionally followed by a space and note
  text).
- See the ~/tmp/screenshots/20261019_063505.png screenshot for an example / my first
  use-case for this feature.
- Review the highlight_continuation_marker.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.4u.linker