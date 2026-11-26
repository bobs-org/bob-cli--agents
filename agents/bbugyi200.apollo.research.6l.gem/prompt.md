%id(gem, clan=research.6l)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6l.cdx`, `research.6l.cld`, `research.6l.grk`, `research.6l.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to implement "ref cards", a new type of property card for ref notes.

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
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=gem)