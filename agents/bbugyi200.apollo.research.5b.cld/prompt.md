%id(cld, clan=research.5b)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.5b.cdx`, `research.5b.grk`, `research.5b.mus`, `research.5b.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start automatically adding good `<` and `>` links to all record notes
which point to the previous/next record note in that album.

- These links should work well with the `[n` and `]n` keymaps.
- This walk should be alphabetical and should cycle around to the next record. For
  example, an album with only two record notes should result in each record containing
  `<` and `>` links that both point to the other record note.
- As a part of this change, we should also start rendering the `N of M` text (or
  something like that) somewhere close to these links where `N` is the current record
  note's index (i.e. position in the walk) and `M` is the total number of record notes
  in that album.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)