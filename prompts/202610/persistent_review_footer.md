- **PLAN:**
  [202610/persistent_review_footer.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/persistent_review_footer.md)
- **AGENTS:**
  - [bbugyi200.apollo.4w--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4w.md)

The review indicators that we show in Obsidian on the bottom right (shown in the
~/tmp/screenshots/20261003_172431.png screenshot) are useful, but I'd like to make some
improvements. Can you help me implement these?

- We should only show a review group if there are 1 or more tasks in that group. For
  example, in the ~/tmp/screenshots/20261003_172431.png screenshot, `projects 0` should
  not be shown.
- The toast that is shown by the `]s` keymap is nice, but it would be better if a
  condensed form of that information was always visible while there are still tasks to
  review. Let's start showing it on the bottom of Obsidian somewhere, but only if there
  are tasks to review. Otherwise, we should not show it or any of these counts.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
