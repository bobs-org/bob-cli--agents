- **AGENTS:**
  - [bbugyi200.apollo.research.6k.cdx](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6k.cdx/README.md)

#gh:gh_bobs-org__bob-cli %id(cdx, clan=research.6k) %m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm. The other researchers,
`research.6k.cld`, `research.6k.grk`, `research.6k.mus`, `research.6k.gem`, are
independently investigating the same request and will write their own self-named reports
ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end
in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start rendering property cards at the top of prose (fka article) notes
and notebooks.

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qi and
  bob-cli-qj epic beads.
- These property cards should act like other property cards (e.g. the native Obsidian
  "Properties" should be hidden in these note files).
- Prose notes and notebooks do not currently support many custom frontmatter properties
  (just a summary?), but we should include rich, useful data related to the prose note /
  notebook in these cards. Think hard about what data would be most useful for us to
  show on these cards.
- As a part of this change, we should add excellent new glossary terms for "prose card"
  and "notebook card".
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cdx)
