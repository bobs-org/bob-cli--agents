#gh:gh_bobs-org__bob-cli I would like to add support for a new `x=<E>=<X>[!]` syntax that allows me to
start and close a (new) past pomodoro in a single operation. Can you help me implement
this?

- `<E>` should accept mostly the same type of values as the `=<E>` capture syntax (to
  start a pomodoro), with the exception of the `-<N>` syntax, since the `x=` syntax
  works in the past by default.
- `<X>` should accept the same type of arguments as the `x<X>` capture syntax.
- When we use this syntax, the 5-minute block count provided by `<E>` should be treated
  as the number of blocks back in the past that the pomodoro was started in. For
  example, `x=3` should be equivalent to `=3-3 x`.
- We should support using this syntax multiple times in a row, in which case the earlier
  past pomodoro time ranges that we add should be offset (i.e. subtracted) by the time
  ranges specified by subsequent past pomodoros (specified via later uses of the `x=`
  syntax on the same line).
- We should show an error if one of the past pomodoros that we specified would overlap
  with an existing past pomodoro.
  - This error should be downgraded to a warning when the optional `!` suffix is
    provided, in which case the new past pomodoro should steal the overlapping time from
    the old past pomodoro (by updating the past pomodoro's time range appropriately).
  - It should be an error to use the `!` suffix when it is not needed.
- Some examples (assume a current time of 0921):
  - `x=build` should start and close the BUILD pomodoro for the 0900-0925 time range.
  - `x=build@2 x=fix@3` should start and close the BUILD pomodoro with the 0900-0910
    time range and start and close the FIX pomodoro with the 0910-0925 time range.
  - `x=2#fix=*3 apollo agent` should be equivalent to `x=fix@2=*3 apollo agent`, which
    should work and dismiss (from the daily file) the 3rd task listed in the FIX
    pomodoro and append an "apollo agent" entry to that task's work log. This should
    create a past pomodoro with a time range of 0915-0925.
  - `x==1!2` creates a past pomodoro using the next/top future pomodoro with a time
    range of 0900-0925 that works the 1st task in that pomodoro and closes the 2nd.
  - Assuming a past pomodoro for the 0855-0920 time range already exists, the `x=3!`
    capture would create a past pomodoro from the next/top future pomodoro with a time
    range of 0910-0925 and update the old past pomodoro's time range to 0855-0910.
- Review the recording_past_pomodoros.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.38.linker