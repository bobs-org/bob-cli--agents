#gh:gh_bobs-org__bob-cli Can you help me make it so, whenever the `bob gcal sync` command creates a new
event task, a corresponding past/current/future (depending on the time range of the
event) pomodoro is created with a task link corresponding to each event (with a
preference for putting all events in the same pomodoro when they are all the same type
of pomodoro--for example, we should group all future event tasks that this command
creates in the same pomodoro)? This means that every event task that the `bob gcal sync`
command creates should have either a next (`[*]`) or closed (`[/]`) status.

#plan %m:@xlarge %wait(bead=bob-cli-es)