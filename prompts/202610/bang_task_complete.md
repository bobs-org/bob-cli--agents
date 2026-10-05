- **PLAN:**
  [202610/bang_task_complete.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bang_task_complete.md)
- **AGENTS:**
  - [bbugyi200.apollo.5a--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.5a.md)

Can you help me add support for a new `!file:id` capture input syntax to the
`bob capture` command and the corresponding bob-mac-capture app?

- This syntax must be the entire contents of the capture input (but supports bulk
  capture).
- Pressing `!` at the start of the input in the bob-mac-capture app should result in the
  user being prompted to select from any open task with support for filtering (like `:`
  does, for example) but with tasks that have task links in today's daily file
  prioritized at the top.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
