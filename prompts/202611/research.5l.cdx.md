- **AGENTS:**
  - [bbugyi200.apollo.research.5l.cdx](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.5l.cdx/README.md)

#gh:gh_bobs-org__bob-cli %id(cdx, clan=research.5l) %m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm. The other researchers,
`research.5l.cld`, `research.5l.grk`, `research.5l.mus`, `research.5l.gem`, are
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

Once I've completed the work described by the property_card_title_block.md file in the
research sidecar repo, I want to add the new `[N` and `]N` keymaps, which should be
immediately useful for daily files, period notes, and record notes.

- These should be configurable in any Obsidian note somehow. I was thinking we could
  look for links that start with `<<` or `>>`, respectively, but that's just my first
  thought. Think hard about the best way to implement this.
- For daily files, the << link should point to the first day of the previous week and
  the >> link should point to the first day of the next week.
- For period notes, the << link should point to the first period note of the same level
  (ex: weekly period note if inside a weekly period note currently) in the previous
  period of a level one higher. The >> link should point to the first period note of the
  same level in the next period of a level one higher.
  - For example, this means the ~/bob/2026/2026-W30.md file should have a << link that
    points to the ~/bob/2026/2026-W14.md file and a >> link that points to the
    ~/bob/2026/2026-W40.md file.
  - This also means that yearly period notes should not support this functionality (i.e.
    should not have << or >> links).
  - Make sure that we make it clear (in a visually appealing way) when one of these
    files does not yet exist somehow.
- Album notes should be able to configure a field that its record notes should be
  grouped by in order to support these new keymaps.
  - The `[n` and `]n` keymaps should then start walking through all record notes with
    that field set to the same value in sequence before moving on to the prev/next
    record group (i.e. group of record notes with this field all set to the same value).
  - The `[N` and `]N` keymaps should jump to the first record note of the previous/next,
    respectively, record group.
  - As our first use-cases, I would like to configure the ~/bob/sase_blog_zettel.md
    album note to start using its `section` field to group this walk. Think hard about
    whether or not the other albums in my vault would benefit from configuring a
    grouping field as well (configure the appropriate field for these if so).
- Make sure that the `[{` and `]}` keymaps work properly with these keymaps.
- We should make sure these links render nicely at the bottom of property cards (see the
  bob-cli-nh epic bead for context).
- We should also make sure to add support for appropriate hints to the walker footer for
  these new links.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cdx)
