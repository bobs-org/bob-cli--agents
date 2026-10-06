%id(cdx, clan=research.0d)
%m:codex/gpt-6.1-sol@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cdx in a 5-researcher swarm.
The other researchers, `research.0d.cld`, `research.0d.grk`, `research.0d.mus`, `research.0d.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cld.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cdx.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to integrate more of my keymaps with my GTD morning review, which I trigger
via the `]s` Obsidian keymap and continue walking through using `]s` until I have
reviewed all items from all review groups.

- I already added support for the `<ctrl+enter>` keymap for the PRE review group, but
  I'm thinking that anytime that we close the current review item using this keymap, we
  should use this behavior (i.e. automatically jump to the next/first review item).
- Also, there are multiple other keymaps that trigger actions which also imply that we
  should iterate to the next review item. The `<ctrl+shift+enter>` and `<ctrl+shift+p>`
  (assuming a task card option is selected that removes the review item from the review
  stack) keymaps, for example, should ideally trigger an automatic jump to the next
  review item.
- You should look for and propose other keymaps / actions that should trigger a jump to
  the next review item when in the middle of a GTD morning review.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cdx)