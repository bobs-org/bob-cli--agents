- **PLAN:**
  [202608/canceled_draft_stash.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202608/canceled_draft_stash.md)
- **AGENTS:**
  - [bbugyi200.athena.024--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/families/bbugyi200.athena.024.md)

  Can you help me add support to the bob-mac-capture app for stashing the contents of
  the last `<N>` inputs that were canceled via the `<ctrl+c>` keymap?

- `<N>` should be configurable but should default to 10.
- Let's add a new `<ctrl+s>` keymap that allows the user to trigger a pop-up menu from
  the capture panel and (with a single keypress) select an entry to pop from the stash.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
