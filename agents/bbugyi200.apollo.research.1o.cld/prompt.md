%id(cld, clan=research.1o)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.1o.cdx`, `research.1o.grk`, `research.1o.mus`, `research.1o.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
want a way to specify that a particular markdown file in my vault should always be
treated as an article / design doc / some content with sections.

- This will allow us to treat (e.g. format) these files differently from other note
  files in my Obsidian vault.
- For example, the ~/bob/sase_blog_contents.md file is one of these notes.
- As our first use-case, I would like to start auto-formatting (think hard about what
  formatting rules to apply) these files and auto-numbering (starting at 1 with support
  for sub-sections) the sections contained within these files.
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)