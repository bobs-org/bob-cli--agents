#gh:gh_bobs-org__bob-cli Can you help me start having the `bob task reconcile` command merge continuous
pomodoro lines that use the same task type(s) in the current daily file, if any exist?

- The goal of this change is to make it easier to read daily files while encouraging
  small, honest pomodoros (since I won't be discouraged by the noise/clutter I'm adding
  to the daily file).
- For example, in the ~/bob/2026/20261105.md file, the pomodoros that span the 0840-0855
  time range should be merged and the pomodoros that span the 0900-0910 time range
  should be merged.

#plan %m:@xlarge