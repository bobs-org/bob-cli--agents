- **PLAN:**
  [202610/hammerspoon_chezmoi_restart.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/hammerspoon_chezmoi_restart.md)
- **AGENTS:**
  - [bbugyi200.athena.0yd--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0yd.md)

I thought that we had some chezmoi logic set up so when Lua code related to Hammerspoon
is changed, we restart Hammerspoon automatically when `chezmoi apply` is run on that
machine, but this does not seem to be working. Can you help me fix this / implement this
feature if it does not already exist? Think this through thoroughly and create a plan
using your `/sase_plan` skill. Choose and author the appropriate tier, validate and
revalidate until it passes, then submit it with `sase plan propose` (as the skill
instructs) before making any file changes.
