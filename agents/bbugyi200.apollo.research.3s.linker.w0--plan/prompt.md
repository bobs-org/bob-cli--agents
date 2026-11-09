#gh:gh_bobs-org__bob-cli I would like to add support for a new `<N>` prefix to the existing `x` capture
syntax, where `<N>` is a positive integer. Can you help me implement this?

- When this syntax is used, `<N>` should be meant to indicate the size (in 5 minute
  increments) the pomodoro should be re-sized to before being closed.
- The goal is to help reduce the amount of mental arithmetic needed in some cases.
- For example, assuming the currently running pomodoro has a duration of 25 minutes,
  then the `2x!2` capture should be equivalent to `-3 x!2`.
- Review the sized_pomodoro_close.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.3s.linker %wait(bead=bob-cli-is)