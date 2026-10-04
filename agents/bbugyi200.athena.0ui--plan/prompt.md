#gh:gh_bobs-org__bob-cli Can you help me add support to the `bob capture` command and the
bob-mac-capture app for adding work log sub-bullets to the worked task links when using
the `=x<N>` syntax, where `<N>` is a list of indices corresponding with the task links
that were actually worked?

- We should use the `=x<N> <n> <work_log_entry1> <m> <work_log_entry2> ...` syntax for
  this, where `<n>` and `<m>` must be indices specified by `<N>` or, if `<N>` was not
  specified, any index that corresponds with a task link on the current pomodoro.
- For example, `=x2,3 2 foo bar baz` should result in the 2nd and 3rd task links being
  worked (e.g. marked as in-progress and have references left behind in the closed
  pomodoro) and the work log note / task link sub-bullet `foo bar baz` being added to
  the task corresponding with index 2 before closing the pomodoro (which should then
  result in the actual work log entry being added).
- #beau

#plan %m:@xlarge %auto