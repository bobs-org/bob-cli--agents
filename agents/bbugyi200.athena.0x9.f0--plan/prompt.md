#gh:gh_bobs-org__bob-cli #fork:0x9 It doesn't seem like when we do auto-jump through the tasks that need
review that we always go in order (in particularly when the `<ctrl+shift+m>` keymap is
used, which we just fixed, but I'm not sure about that). For example, I keep jumping to
a review item that is in the 40s for some reason when I expect to jump to the first
review item. Can you help me confirm/deny my suspicion, diagnose the true root cause,
and fix the issue?

#plan %m:@xlarge %auto