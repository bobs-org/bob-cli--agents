- **AGENTS:**
  - [bbugyi200.apollo.research.4e.cld](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.4e.cld/README.md)

%id(cld, clan=research.4e) %m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher cld in a 5-researcher swarm. The other
researchers, `research.4e.cdx`, `research.4e.grk`, `research.4e.mus`, `research.4e.gem`,
are independently investigating the same request and will write their own self-named
reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report
will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We currently always show the GTD review footer. I would like to start making this footer
only show when the GTD review walk is active (i.e. the `s` key is active and will be
triggered by the `[[` and `]]` keymaps).

- As a part of this change, we should add two appropriate new footers that are active
  only when the `w` walk or `n` walk is active.
- The `w` walk should have indicators that show how many pending/next/ready tasks are in
  that walk, for example.
- We should add an excellent new "walker footer" glossary term to describe these footers
  (note that a "review footer" should be considered a type of "walker footer").
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cld)
