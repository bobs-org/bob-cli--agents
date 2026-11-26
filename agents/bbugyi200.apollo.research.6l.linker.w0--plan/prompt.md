#gh:gh_bobs-org__bob-cli I would like to implement "ref cards", a new type of property card for ref
notes. Can you help me implement this?

- See how other property cards are implemented and the bob-cli-qm epic bead, which is
  in-progress and implements notebook cards and prose cards, for context and
  inspiration.
- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qm epic.
- Think hard about how this card should look. It should contain as much genuinely useful
  information about the reference as possible without cluttering the card.
- Also, think hard about whether or not ref cards should support the `==` keymap and, if
  so, what kinds of operations the schema editor that is triggered should support.
- As a part of this change, we should add an excellent new glossary term for "ref card".
- Review the ref_cards.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (except for any sase memory file changes, which should only be implemented if I
  approve them or explicitly asked for them in this prompt), but keep in mind that you
  are responsible for planning and splitting up this work appropriately.
- #beau

#plan %m:@xlarge %w:research.6l.linker