#gh:gh_bobs-org__bob-cli I suspect that the way (e.g. how and when) we default include task links in the
closed pomodoro when using the `x` and `x=` capture syntaxes is inconsistent and
incorrect.

- Namely, we should only default include a task link if all task links are included
  (i.e. no indices were provided--including indices after `!` and `*`).
- Otherwise, only task links that had their index explicitly referenced should be
  included (what "included" means depends on whether the index was after a `!` or `*`).

Does this make sense and do you agree with this policy? #if_so_plan %m:@xlarge