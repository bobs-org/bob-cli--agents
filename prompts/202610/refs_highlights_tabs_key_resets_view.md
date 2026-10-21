- **PLAN:**
  [202610/refs_highlights_tabs_key_resets_view.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/refs_highlights_tabs_key_resets_view.md)
- **AGENTS:**
  - [bbugyi200.athena.12s--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.12s.md)

When the `<cmd+t>` keymap is used in the Highlights app, all previous state that was
persisted for the bob-mac-capture app's ref panel should be cleared (as if the user used
the `<ctrl+z>` keymap on that panel). See the ~/tmp/screenshots/20261021_073902.png
screenshot for an example of a problem we experience because we don't currently do this.
Can you help me fix this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
