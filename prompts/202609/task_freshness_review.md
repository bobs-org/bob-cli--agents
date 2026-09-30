- **PLAN:**
  [202609/task_freshness_review.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/task_freshness_review.md)
- **AGENTS:**
  - [bbugyi200.apollo.research.v.linker.w0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.v.linker.w0.md)

I'm currently re-designing my GTD process a bit (see the bob-cli-2y epic bead for
context), but there is still one major requirement that is unmet. Can you help me
implement a solution for this?

- Namely, it is important that I at least glance at every task that I captured the
  previous day in case something is in there that should really get addressed today. For
  example, what if my wife and I are speed walking and she asks me to pick up our
  daughter in the morning? I'll add it to my Google Keep and sync that with my Obsidian
  the next morning using the `bob gkeep pull` command, but if I don't glance at that
  task, it does me no good.
- This is why I used to review the Ready section in the ~/bob/dash.md file every
  morning. This habit, where I would review every task in that section and attempt to
  reduce the number of ready tasks for each project to <=5, forced me to glance at inbox
  items every morning.
- The problem with this approach was that I was reviewing some tasks way more often than
  necessary, which wasted time and introduced friction into the process.
- I think we can solve this by using a new concept named "task freshness" (aka
  "freshness"), which should be added to the glossary memory web.
- This new policy/process will require that every ready task have some new property, say
  `fresh`, that has a date as a value. That date is meant to indicate the last time a
  human being looked at that task and confirmed it still needs to be done and should
  still look the way it does (e.g. same priority, description, parent project, etc...).
- By default, we should use 7 days as our task refresh interval, but tasks should be
  able to override this with a dataview property. Also, we should be able to
  configure/override the refresh interval for every task in a project by adding an
  appropriate frontmatter property to that project note file.
- Making any changes (e.g. via Obsidian keymaps we support--we do not need to actually
  monitor for manual task changes) to a ready task (including making it ready--going
  from blocked to ready, for example) should result in the freshness date being updated
  for that task automatically.
- Any task that is past due for a refresh should show up in my new freshness review
  process, which you should help me flesh out.
  - I should be able to see how many of my tasks our out-of-date as well as how many
    tasks I have refreshed today at a glance somehow during this review process.
  - I should have keymaps that allow me to easily jump to the next/previous out-of-date
    task. I should also have a keymap that allows me to refresh the currently selected
    task without making any other changes to it.
- This solution addresses the problem of me needing to glance at inbox tasks every
  morning (these should be out-of-date by default since they have never been marked as
  fresh), but it also minimizes the amount of work that I need to do during any kind of
  weekly review (which is not something that I currently do).
- It's possible that even this becomes too much work every morning but, if that becomes
  a problem, I can always limit myself to reviewing N out-of-date tasks per day (and
  then introduce a weekly review where I refresh all out-of-date tasks).
- Review the ready_task_freshness_review.md file in the research sidecar repo for
  context and inspiration before planning.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
