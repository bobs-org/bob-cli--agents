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
- #beau

#plan %m:@xlarge %w:research.2z.linker %wait(bead=bob-cli-f6)