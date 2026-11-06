- **AGENTS:**
  - [bbugyi200.apollo.research.32.cdx](https://github.com/bobs-org/bob-cli--agents/blob/main/agents/bbugyi200.apollo.research.32.cdx/README.md)

#gh:gh_bobs-org__bob-cli %id(cdx, clan=research.32) %m:gpt-6-astra %q(1.5x, w=0.25)

You are researcher cdx in a 5-researcher swarm. The other researchers,
`research.32.cld`, `research.32.grk`, `research.32.mus`, `research.32.gem`, are
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

I want to make some improvements to the way we handle freshness updates using the
`<alt+f>` and `<ctrl+alt+f>` keymaps.

- I want to generalize and unify the "task decay" supported by bob currently. We should
  add a new glossary term for "task decay" that does a good job of explaining this new /
  improved policy.
- We should add one more more appropriate config field to make this functionality
  flexible (I was thinking just allowed rolls for each task status, but I'll let you
  decide) and add them to my bob/config.yml file in my chezmoi repo (with good, but
  concise, comments).
- I would like my bob to allow 2 keeps in each status/priority before defaulting to
  rolling to the next status/priority. We already support this for priorities I believe,
  but it should be configured explicitly.
- We already support a way to decay ready tasks (after 3 keeps currently--this should be
  changed to 2).
  - There seems to be a problem with ready task decay right now though that you should
    look into.
  - Namely, it says that no priority ladder is configured (I think we should just always
    use P1, right?).
  - We should fix this issue as a part of this change.
  - See the ~/tmp/screenshots/20261102_134505.png screenshot for context.
- WIP tasks should decay to next tasks by default when their keep limit has been
  reached.
- Next tasks should decay to ready tasks by default when their keep limit has been
  reached.
- The user should have an option to keep the status the same for all of these
  transitions / prompts, which should reset the keep count for that task.
- Make sure the rotten log entries reflect all of these transitions appropriately.
- Let's stop prompting for a work log entry when marking WIP tasks as fresh in Obsidian.
  These WIP tasks should be considered rotten, which means that we should prompt for a
  rotten log entry instead.
- We should continue to prompt for a rotten log entry for next tasks (like we do now),
  but a rotten log entry should always be added (either explicitly or using a default).
- If the user does not give a rotten log entry, then a default one should be added which
  specifies the status that was kept (make sure it is clear how many times each task was
  kept in each status). We already do something like this for ready tasks I believe, but
  we might want to unify the process a bit (I'll let you decide on this one).
- #beau

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution.
#research(suffix=cdx)
