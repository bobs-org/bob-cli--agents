#gh:gh_bobs-org__bob-cli The mac pom `NO POMODORO` text currently flashes for 60s after the first 60s of
it showing and then for 60s every 5m after that. Can you help me start using the
fibanocci sequence to determine how many minutes we wait in-betweeen each 60s flashing
step instead?

- So, in other words, we should wait for 60s before the first 60s flash step (1). The
  next 60s flash step should then occur after another 60s of no flashing (1). The next
  60s flash step should then occur after 2m of no flashing (2). And then 3m of no
  flashing (3). And then 5m of no flashing (5). etc...
- Also, let's start showing how many minutes we just waited for next to the
  `NO POMODORO` text during each 60s flash step (it should go away during non-flashing
  steps) separated by the phi symbol (used to represent the fibanocci sequence).
- #beau

#plan %m:@xlarge %auto