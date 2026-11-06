- **AGENTS:**
  - [bbugyi200.apollo.research.36.cdx](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.36.cdx/README.md)

#gh:gh_bobs-org__bob-cli %id(cdx, clan=research.36) %m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm. The other researchers,
`research.36.cld`, `research.36.grk`, `research.36.mus`, `research.36.gem`, are
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

I would like to add better support for moving tasks from one note file to another and
add excellent (new) support for merging tasks to / creating new tasks from bullets of
other tasks.

- We should add support for a new `@a+aid @b+bid > @c` capture syntax where any number
  of notes can be on the left-hand side of the `>` character and `@c` can have a
  `#drawer` suffix to specify that the tasks should be converted to notes and moved to
  that drawer (this drawer should be created if it does not already exist).
- We should also be able to use a target of the form `@c+cid` after the `>`, in which
  case we should merge the source tasks into the `^cid` task in the ~/bob/c.md file. We
  should also be able to use the `@c+cid#drawer` syntax to target a specific drawer in
  the `^cid` task (this drawer should be created if it does not already exist).
- When merging one task into another, we should not delete the source tasks. Instead, we
  should add a new "merged into" task relation that points from the source tasks to the
  destination task (and auto-cancels the source task). This "merged into" task relation
  should be able to be used on its own (in Obsidian via the `<ctrl+shift+l>` keymap, for
  example) to perform the same operation (see how we associate other task relations with
  specific operations for inspiration--this "merged into" relation should be
  configurable if possible/desirable).
- We should add a new `<ctrl+shift+t>` keymap to Obsidian that makes it easy to split
  out one or more top-level bullets from a task into new tasks. When this is done, the
  bullets (and their child bullets) should be replaced by some concise and useful text
  containing inline links to the new tasks that were created from the old bullets (the
  old tasks should wind up being given "linked from" mentions which are triggered by
  these inline links).
- Make sure that we have good command-line support for all of this new functionality.
- FYI: I already am in the process of adding support for the `@file+id` capture syntax
  multiple times on the same line (see the capture_multi_target.md file in the plans
  sidecar repo for context).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cdx)
