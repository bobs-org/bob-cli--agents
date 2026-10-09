%auto
#gh:gh_bobs-org__bob-cli %w:61.w1 Can you help me add support to the `bob capture` command and the
corresponding bob-mac-capture app for a new `==` syntax that works just like the `=`
syntax but allows you to override the current pomodoro? This will allow us to change the
ledger used for the current pomodoro and/or, by using the `#pomodoro` suffix, make a
different pomodoro in today's daily file the new current pomodoro (and migrate the old
one to the first future pomodoro). By default, if `==#pomodoro` is used without
specifying the start/end range (using a special syntax between the last `=` and the
`#`), then we should keep the ledger as it is, but just make the targeted pomodoro the
new current pomodoro. #beau

#plan %m:@xlarge 