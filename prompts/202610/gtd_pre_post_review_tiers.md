- **PLAN:**
  [202610/gtd_pre_post_review_tiers.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/gtd_pre_post_review_tiers.md)
- **AGENTS:**
  - [bbugyi200.apollo.research.07.linker.w1--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.07.linker.w1.md)

I want to add two new review groups to the GTD morning review that I trigger with the
`]s` keymap in Obsidian: PRE and POST

- PRE should be reviewed before any other review group and POST should be reviewed after
  any other review group.
- The PRE review group should contain any ready task that has the `#gtd` and `#pre`
  tags. You should add these tags to all of the tasks in the ~/bob/gtd_daily.md file
  that recur daily except for the "Morning review" task.
- The POST review group should contain any ready task that has the `#gtd` and `#post`
  tags. You should add these tags to the "Morning review" task in the ~/bob/gtd_daily.md
  file.
- The idea is that we will close out each of these recurring GTD tasks as we get to them
  (the "Morning review" task is last so I can check off that I completed my morning
  review, which includes all of the items before it--unless there are some ROTTEN tasks
  I can't get to that day).
- Review the gtd_pre_post_checklist_tiers.md file in the research sidecar repo for
  context and inspiration before planning. I agree with almost (see the below bullet)
  all of the recommendations made in that research file.
- Note, however, that (despite what the research suggests) we should NOT wait for a
  trial to be over. There is no trial (remove it if there is some code that actually
  references/uses one and make sure that future agents don't suggest we wait for this
  trial again by updating memories accordingly--you are allowed to update memory
  decisions inline for this one; don't create new decisions memory files).

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
