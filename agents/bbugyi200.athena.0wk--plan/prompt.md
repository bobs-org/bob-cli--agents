#gh:gh_bobs-org__bob-cli The pomodoro indicator in the menu bar on my macbook (defined by Hammerspoon in
my chezmoi repo) has `OVERDUE` text that is shown when the current pomodoro is
overdue >=10 minutes and flashes red. I would like to do something like this (flash) for
the `NO POMODORO` text that is shown when there is no current pomodoro, but it can't
flash all of the time because that would be annoying. Instead, can you help me make the
`NO POMODORO` text flash green for 60 seconds on every 10th minute?

- This way I'll wind up remembering that I should set a pomodoro more often (sometimes I
  close the current one and then forget to set a new one).
- Make sure that the `NO POMODORO` text always flashes green for the first 60 seconds
  that it is shown (and then for 60 seconds every 10 minutes atter that). This way I'm
  always reminded to set a new pomodoro right after closing the current one.
- #beau

#plan %m:@xlarge %auto