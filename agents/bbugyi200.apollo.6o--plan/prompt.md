#gh:gh_bobs-org__bob-cli We seemed to have broken the completion menu that is supposed to pop-up when
the user types a colon after a `@file` reference (i.e. `@file:`) in the bob-mac-capture
app. See the ~/tmp/screenshots/20261011_054243.png screenshot for context. I think we
may have broken this when implementing the new functionality that allows you to easily
swap `^` with `:` in this app and vice-versa but I'm not sure. Can you help me
confirm/deny my suspicion, diagnose the true root cause, and fix the issue?

#plan %m:@xlarge %auto