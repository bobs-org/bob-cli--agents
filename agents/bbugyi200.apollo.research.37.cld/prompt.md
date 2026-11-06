%id(cld, clan=research.37)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.37.cdx`, `research.37.grk`, `research.37.mus`, `research.37.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for a new `^^` capture syntax that can be used with the
`@foo[^:]bar@` syntax.

- See the bob-cli-gl epic bead for context on the recent support we added for pulling in
  child tasks from the parent project when using the `@foo[^:]bar@` syntax.
- When `^^` is found as the only contents of a capture bullet using this syntax, we
  should prompt the user to select one or more tasks from the parent project after they
  submit the capture.
- The selected tasks will be added as `^foo` / `:foo` bullets as if the syntax
  introduced by the bob-cli-gl epic bead was used directly.
- This task prompt should take inspiration from the successor prompt I'm thinking, but
  keep in mind that we need a way to support `:` as well as `^` (and not selected, which
  should be the default).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)