- **PLAN:**
  [202610/install_all_restart_on_plugin_change.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/install_all_restart_on_plugin_change.md)
- **AGENTS:**
  - [bbugyi200.athena.0wh--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0wh.md)

We recently added the `just install-all` and `just install-all-and-restart` commands. I
would like to get rid of the `just install-all-and-restart` command in favor of merging
this functionality into the `just install-all` command with one change: We should only
restart Obsidian if the `bob plugins sync` command made changes to my Obsidian vault
(i.e. if the bob-plugins repo had changes, which justifies updating Obsidian). Can you
help me implement this?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
