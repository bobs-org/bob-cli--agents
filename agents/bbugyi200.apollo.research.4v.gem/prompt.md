%id(gem, clan=research.4v)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4v.cdx`, `research.4v.cld`, `research.4v.grk`, `research.4v.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add much better support for vertically split windows in Obsidian.

- See the ~/tmp/screenshots/20261115_171818.png screenshot for an example of what this
  looks like.
- Let's add new `<ctrl+w><key>` keymaps, where various `<key>` values are supported.
- For example, the `<ctrl+w>h` and `<ctrl+w>l` keymaps should navigate to the other
  (i.e. not currently focused) split when a vertical split is active.
- The `<ctrl+w>H` and `<ctrl+w>L` keymaps should be able to be used to move the current
  window to a split on the left or right, respectively (creating the split when
  necessary). These keymaps should also be able to be used to destroy a split, when
  moving the last window from a split to the other side.
- Make sure we show a good hint to the user when `<ctrl+w>` is pressed.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=gem)