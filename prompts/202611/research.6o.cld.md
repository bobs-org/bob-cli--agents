- **AGENTS:**
  - [bbugyi200.apollo.research.6o.cld](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.6o.cld/README.md)

%id(cld, clan=research.6o) %m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli You are researcher cld in a 5-researcher swarm. The other
researchers, `research.6o.cdx`, `research.6o.grk`, `research.6o.mus`, `research.6o.gem`,
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

I would like to add support to area notes, project notes, notebooks, and prose notes for
the link walks (triggered via the `]n` keymap).

- We should implement this work in parallel (think hard about the best way to do this
  and whether or not coordination is even needed) with the in-progress bob-cli-qq epic
  bead.
- We should render a nice link walk widget at the bottom of the property card like we do
  for other files that support the link walk. As a part of this change we should make
  sure that the link walk widget is always shown at the very bottom of the property card
  (below all cabinets).
- For each of these new supported note types, the walk should only include notes of the
  same type that share the same parent note.
- We should group the members of this walk by their parent.
- As a part of this change we should add an excellent new glossary term for "link walk".
- For example, assume we are in the bar.md project note, which has the foo.md project
  note as its parent which, in turn, has the pig.md area note as its parent. The `]n`
  keymap would then jump to the baz.md file, assuming that is the next (alphabetically)
  project note that has the foo.md project note as its parent.
- I would like to support the `]N` keymap as well, but I'm not sure how the grouping
  would work. Think hard about this. If you can think of an intuitive way to group this
  walk such that the `]N` keymap works, then we should implement it.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cld)
