%id(cld, clan=research.3s)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 5-researcher swarm.
The other researchers, `research.3s.cdx`, `research.3s.grk`, `research.3s.mus`, `research.3s.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__mus.md` and `__gem.md`. Your report will end in `__cld.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to migrate the `bob highlights` command to a new `bob ref` command that
supports all of the same commands that the `bob highlights` command currently does but
also adds new commands that make it easy for agents (and myself) to see what references
I have read, which I am tracking / plan to read, which I've finished reading, etc...

- The main use-case for this command would be for agents that are recommending new
  reading material for me (these agents would find it useful to know what articles /
  papers I have already read).
- With that said, I also think it would be useful to be able to read the annotations
  that I left on these reference PDFs (using the Highlights app on my macbook). These
  are automatically written to markdown files in the ~/bob/ref/ directory.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)