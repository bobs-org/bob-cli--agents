#gh:gh_bobs-org__bob-cli I would like to add support for grouping one or more annotations under another
annotation (a "section annotation") when rendering ref notes from ref PDF annotations
(made using the Highlights app). Can you help me implement this?

- A section annotation should be of the form `# <name>`, with an optional description
  after a blank line.
- Any highlight note / underline note / standalone note that then contains `@<name>`
  should be rendered under a nice, visually appealing section of some sort. Think hard
  about the best way to persist and render this grouping.
- This grouping should be plesent to view in Obsidian and in the bob-mac-capture app's
  ref panel (and anywhere else we view ref notes).
- Review the ref_note_annotation_sections.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.2d.linker %auto