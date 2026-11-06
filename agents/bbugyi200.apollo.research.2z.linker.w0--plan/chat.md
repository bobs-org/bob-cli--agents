# Chat History - ace-run (research.2z.linker.w0--plan)

- **TIMESTAMP:** 2026-11-01 21:46:23 EST
- **MODEL:** claude/opus
- **AGENT:** research.2z.linker.w0--plan

**Plan:** /home/bryan/.sase/plans/202611/off_clock_pomodoros.md


## Prompt

%auto
#gh:gh_bobs-org__bob-cli We recently / are in the middle of adding support for the `#untracked` tag to
Google Calendar events. The plan (see the bob-cli-f6 epic bead for context) was to not
track the pomodoros corresponding to untracked event tasks at all, but I'm not sure this
is the best approach. I'd like to start tracking these pomodoros as a part of a
separate, "untracked" group of stats instead somehow. Can you help me implement this?

- I think we can probably implment this by using the `u::` task property for untracked
  pomodoro (this way we still track the duration of each pomodoro somehow).
- The stats dash and the `bob stats` command would then need some way to toggle over to
  showing untracked time (preferably with an option to show just untracked time and all
  time, including untracked).
- As a part of this change, we should generalize this concept of an "untracked pomodoro"
  a bit (which should maybe be named something else, since the time will techinically
  still be tracked after this change?).
  - Add an excellent new glossary term for "untracked pomodoro" (or whatever we decide
    to call these).
  - A pomodoro should be untracked iff all of its task links correspond with tasks that
    have the `#untracked` tag.
- Review the off_clock_pomodoro_stats.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge %w:research.2z.linker %wait(bead=bob-cli-f6)

## Response

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/off_clock_pomodoros.md`

> # Off-Clock Pomodoros, recorded and counted on their own clock
> ## Goal
> `bob-cli-f6` made a session spent on an `#untracked` Google Calendar event (lunch, the
> gym) a timed row without `[t::]` that every reader ignores. The time is lost: Bryan
> cannot ask "how much time went to family this week?", the day has holes where life
> happened, and the ledger says lunch ran 1200–1300 while no total includes it.
> This epic keeps that time and counts it apart. It adopts the research recommendation in
> `research:202611/off_clock_pomodoro_stats/off_clock_pomodoro_stats.md` in full (Bryan
> agreed to all of its requirements) and splits it into phases that distinct agents can
> land.

*See full plan file for details.*

