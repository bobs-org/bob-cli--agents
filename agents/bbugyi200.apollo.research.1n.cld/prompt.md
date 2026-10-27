%id(cld, clan=research.1n)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.1n.cdx`, `research.1n.grk`, `research.1n.mus`, `research.1n.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We
recently added support to the `bob capture` command and the corresponding
bob-mac-capture app for capture templates (see the bob-cli-7w epic bead for context).
Can you now help me add support for persisting templates to disk automatically when they
are used?

- We should then allow the user to access and modify the templates that have been saved
  in the bob-mac-capture app.
- This should work in a similar way to the capture stash.
  - We should use a new `<ctrl+t>` keymap that allows the user to view/modify saved
    templates.
  - Just like with the stash, we should pop a template when it is selected (it will just
    get re-added when the capture is submitted if the template is used).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)