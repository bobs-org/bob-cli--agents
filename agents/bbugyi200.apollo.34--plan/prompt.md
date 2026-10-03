#gh:gh_bobs-org__bob-cli We recently added support for using `=x` as input to the `bob capture` command
and the corresponding bob-mac-capture app. Can you now help me add support for the
`=x<N>`, `=x!<M>`, and `=x<N>!<M>` syntaxes?

- `<N>` and `<M>` are both comma-separated lists of integers that correspond with the
  task links in the current pomodoro.
- We will use this syntax to perform something similar to what I do manually when I
  append `#` to the end of task links (to mark that they should not be marked as
  in-progress) and transclude task links (to mark that the corresponding task should be
  completed) before closing the pomodoro with the `<ctrl+enter>` keymap in Obsidian.
- The task links specified by `<N>` are the tasks that should be marked as in-progress.
  In other words, if `<N>` is specified, then any task link not specified by `<N>`
  should NOT be marked as in-progress (as if they had `#` prepended to them when the
  `<ctrl+enter>` keymap was used in Obsidian).
- The task links specified by `<M>` should have their tasks completed and should then be
  striked out.
- Make sure the index of each task link is made clear to the user in some visually
  appealing way in the preview that is shown when `=x` is typed.
- #beau

#plan %m:@xlarge %auto