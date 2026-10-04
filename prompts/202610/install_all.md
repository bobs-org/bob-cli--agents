- **PLAN:**
  [202610/install_all.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/install_all.md)
- **AGENTS:**
  - [bbugyi200.athena.0we--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0we.md)

Can you help me add new `just install-all` and `just install-all-and-restart` commands?

- The `just install-all` command should first sync the repo by running `git pull`. It
  should then run `just install` for the bob-cli project, then install the bob-plugins
  and bob-mac-capture projects by running the `git pull` and `bob plugins sync` (for the
  bob-plugins repo) / `just install` (for the bob-mac-capture repo) commands in those
  directories. Think hard about this and make sure to get these installations right
  (make any changes to my requirements you think are necessary but clearly call these
  out in your plan).
- We should check for these project directories in the parent directory of the bob-cli
  project (in the ~/projects/github/bobs-org/ directory on this machine, for example).
  If one of those directories does not exist, we should skip the install for that
  project gracefully.
- The `just install-all-and-restart` command should first run the `just install-all`
  command and should then restart the Obsidian app, if it is running on that machine.
- I intend to use this to make it easier to re-install bob-cli, bob-plugins, and
  bob-mac-capture all at once and then restart Obsidian on my macbook.
- I want you to lead the design on this one. Make sure you design this feature so it is
  intuitive, reliable, and (last but not least) beautiful!

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
