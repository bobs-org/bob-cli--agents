#gh:gh_bobs-org__bob-cli Can you help me add support for a new `!file:id` capture input syntax to the
`bob capture` command and the corresponding bob-mac-capture app?

- This syntax must be the entire contents of the capture input (but supports bulk
  capture).
- Pressing `!` at the start of the input in the bob-mac-capture app should result in the
  user being prompted to select from any open task with support for filtering (like `:`
  does, for example) but with tasks that have task links in today's daily file
  prioritized at the top.
- #beau

#plan %m:@xlarge %auto