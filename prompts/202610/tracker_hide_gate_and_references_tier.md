- **PLAN:**
  [202610/tracker_hide_gate_and_references_tier.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/tracker_hide_gate_and_references_tier.md)
- **AGENTS:**
  - [bbugyi200.athena.0vp--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0vp.md)

I think there are some problems with the way we are handling `^prj` and `^ref` tasks in
Obsidian. Can you help me fix these issues?

- I think we overcomplicated the freshness check criteria for project tasks. Namely, we
  should only check `^prj` tasks that do NOT have the `#hide` tag. The `#hide` tag
  should already be removed from `^prj` tasks by the `bob projects sync` command when
  appropriate. Note that `^ref` tasks should be checked regardless of their `#hide` tag.
- Speaking of the `bob projects sync` command, it appears to have a bug. Namely, it
  should remove the `#hide` tag when appropriate (i.e. when the project note contains no
  open tasks and has no open sub-projects) regardless of whether or not that project
  note file has the `scheduled` frontmatter field set when that `scheduled` date is
  already today or a day in the past (if the project is scheduled for a future date,
  then we should leave it hidden). For example, the `^prj` task in the
  ~/bob/sase_sites.md file should have its `#hide` tag removed by this command once you
  fix this.
- Regarding `^ref` tasks, we should change the configuration (in my chezmoi repo) so
  these are reviewed for freshness every 7 days (like normal tasks) instead of every 3
  days. Also, let's start reviewing these (when using the `]s` keymap to iterate over
  tasks that need our attention) as a part of their own group right before ROTTEN tasks.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
