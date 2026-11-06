# Chat History - ace-run (research.3c.mus)

- **TIMESTAMP:** 2026-11-05 08:50:40 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** research.3c.mus
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_084433.md`

## Prompt

%id(mus, clan=research.3c)
%m:muse/muse-spark-1.3-contributor@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher mus in a 5-researcher swarm.
The other researchers, `research.3c.cdx`, `research.3c.cld`, `research.3c.grk`, `research.3c.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__gem.md`. Your report will end in `__mus.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

We already support the `offclock` boolean area note / project note file frontmatter
field to specify that all tasks in an area/project, recursively, should be treated as
offclock. I would now like to add support for a new `offclock_types` property that takes
a list of task type names as values.

- This field should work just like `offclock`, but only tasks which have one of the
  types listed by this field should be treated as offclock.
- As our first use-case I would like to migrate the area notes in my Obsidian vault that
  currently use `offclock` to start using `offclock_types` instead, with MEET being the
  only task type that they filter for.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__mus` suffix, i.e. `<stem>__mus.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research complete.

I wrote `202611/offclock_types_conditional_clock__mus.md` in the research repo and registered it as `research:202611/offclock_types_conditional_clock__mus.md` (artifact `explicit:23bd67be3d2390c27d634f4a`).

Headline findings: the plan is sound but "the task's type" must mean the effective PT13 type, not the line's `[type::]` field — gcal sync omits `[type:: MEET]` exactly when the suggestion is already MEET, so a field-only check misclassifies the synced meetings this feature targets. The report also pins a single-walk precedence rule for notes declaring both keys, a required gcal probe-line fix (synthetic probes carry no type), a catalog-free type-key check for the hot path, and a per-area (not blanket) migration runbook since `offclock: true` → `[MEET]` flips future non-meeting sessions to Worked. Final declaration accepted; host will commit the research repo.
