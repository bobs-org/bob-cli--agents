#gh:gh_bobs-org__bob-cli The mac pom flashes red when we show the `OVERDUE` text forever, which is shown
after the current pomodoro is >=10 minutes overdue. Can you now help me make it so we
also flash when <=10 minutes overdue but only for the first 5 seconds of every minute
(including the first 5 overdue seconds--e.g. `+00:00`to `+00:05`)? This way the user's
attention is grabbed once a minute by a new flashing red light, but we don't flash the
whole time, which would be annoying since it is normal for a pomodoro to go 5 or 10
minutes over.

#plan %m:@xlarge %auto