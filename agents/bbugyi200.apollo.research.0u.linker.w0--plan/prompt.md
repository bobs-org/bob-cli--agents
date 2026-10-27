#gh:gh_bobs-org__bob-cli I want to start tracking my daily habits/stats somehow. Can you help me
implement this?

- Each of the stats I would like to track (ATM at least) boils down to a single integer
  per day:
  - The total number of morning GTD review tasks I completed each day (by iterating over
    and processing each one using the `]s` keymap).
  - The total number of pomodoro hours and minutes worked each day. Note that I already
    show this via an inline query in the "Pomodoro" section of each daily file.
  - The total number of tasks that I complete each day.
  - The total number of tasks that I create each day.
  - Think hard about what other metrics I should consider tracking in this v1
    implementation.
- It also needs to be easy to start tracking new daily metrics like these that I think
  of later.
- I'm not sure what the UX should look like for this, but it should make it easy to
  visualize my progress for a given metric over a given time period (which I should be
  able to adjust).
- Review the bob_daily_stats.md file in the research sidecar repo for context and
  inspiration before planning. I agree with all of the requirements recommended in that
  research file.
- #beau

#plan %m:@xlarge %auto %w:research.0u.linker