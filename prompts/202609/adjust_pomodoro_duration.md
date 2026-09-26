- **PLAN:**
  [202609/adjust_pomodoro_duration.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/adjust_pomodoro_duration.md)
- **AGENTS:**
  - [bbugyi200.apollo.21--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.21.md)

Can you now help me add a new `+<N>` and `-<N>` syntax, where `<N>` is some integer and
`+<N>` or `-<N>` is the only part of that input capture unit, that allows me to
reproduce the same functionality as the `\p` (for `+<N>`) and `\P` (for `-<N>`) Obsidian
keymaps?

- See the bob-cli-26 epic bead for context.
- Bulk capture should be supported with, for example, `+5` on the same line to increment
  the endtime of the current pomodoro by 25 minutes.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
