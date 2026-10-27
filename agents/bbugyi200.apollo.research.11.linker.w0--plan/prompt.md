#gh:gh_bobs-org__bob-cli Instead of automatically adding successor task links to the current / next
pomodoro, I would like to start prompting the user which unblocked tasks (if any) they
would like to pull in as successor task links when completing a task that blocks other
tasks (via any supported method). Can you help me implement this?

- I'm not sure what the UX should look like for this but I was thinking that the user
  should be able to easily select one or more unblocked tasks from one or more new
  panels (we'll probably need a custom / separate solution for the bob-mac-capture app,
  but you should verify this is needed).
- I think we have a limit currently where we only pull in at most 5 successors. That
  limit should be gone now since the user can pick them explicitly.
- As a part of this change, when a task unblocks a project task that has open tasks, the
  new panel that pops up should include all open tasks that belong to that project
  (which should also been unblocked by closing the task the project depended on). I
  thought we did this already, but just tried this by closing the ^bar task in the
  ~/bob/sase.md file and it did not pull in the (non-project) tasks contained in the
  ~/bob/sase_foo.md project note as successors as I expected.
- This change should also apply to the project tasks / parent project tasks we pull in
  as successors when closing the last open task / sub-project for a project.
- Review the successor_pull_in_offers.md file in the research sidecar repo for context
  and inspiration before planning. I agree with all of the requirements recommended in
  that research file (but keep in mind that you are responsible for planning and
  splitting up this work appropriately).

#plan %m:@xlarge %w:research.11.linker