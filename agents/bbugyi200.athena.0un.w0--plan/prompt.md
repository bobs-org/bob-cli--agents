#gh:gh_bobs-org__bob-cli %w:0un Can you help me add support to the `bob capture` command and the
corresponding bob-mac-capture app for a new `=x*<N>` syntax that works like the `=x<N>`
syntax except that the selected task links are not copied over to the new pomodoro that
is created?

- This will be useful, for example, when we just launched an agent swarm to complete
  some work that we won't be able to verify for another few hours (we don't want that
  task link hanging out in our daily file all day).
- This syntax needs to compose with and work well with the other supported `=x` syntaxes
  (for example, `=x1*2,3!4,5` should work if there are 5 task links in the current
  pomodoro).
- #beau

#plan %m:gpt-6-astra %auto