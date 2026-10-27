%id(cld, clan=research.1j)
%m:claude/opus@xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher cld in a 4-researcher swarm.
The other researchers, `research.1j.cdx`, `research.1j.grk`, `research.1j.gem`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__grk.md` and `__gem.md`. Your report will end in `__cld.md`.

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
want to add support to the `bob capture` command and the corresponding bob-mac-capture
app for defining a template as the first input of a bulk capture.

- Subsequent capture inputs in that bulk capture should then be treated as templates for
  the first capture input.
- For example, consider the following bulk capture using the new syntax that I was
  thinking of using (think hard about what the best syntax is for this functionality):

  ```
  Apply to {0}! @job_2026_apply_29:{1}
  - **URL**: {2}

  Foobar foo http://foobar.com/career/some_foo_job

  Bazbuz baz http://bazbuz.com/career/some_baz_job
  ```

- After this change, that should be equivalent to the following:

  ```
  Apply to Foobar! @job_2026_apply_29:foo
  - **URL**: http://foobar.com/career/some_foo_job

  Apply to Bazbuz! @job_2026_apply_29:baz
  - **URL**: http://bazbuz.com/career/some_baz_job
  ```

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. #research(suffix=cld)