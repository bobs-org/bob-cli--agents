%id(cld, clan=research.3o)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.3o.cdx`, `research.3o.grk`, `research.3o.mus`, `research.3o.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already support opening the corresponding PDF in the Highlights app via the
`<cmd+enter>` keymap when a ref task is selected. I would now like to add support for
this keymap to be used when a quote/annotation in a ref note is selected (we link to
these from tasks created when `#task` is found in annotations).

- We should jump to the appropriate page in the Highlights app when this keymap is used
  in this context.
- We should make it clear to the user when this keymap is available somehow (do the same
  thing when a ref task is selected).
- Make sure to display an appropriate toast in Obsidian so it is clear (for a moment at
  least) what is happening.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)