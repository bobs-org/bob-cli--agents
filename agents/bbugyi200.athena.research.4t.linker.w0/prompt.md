#gh:gh_bobs-org__bob-cli We currently label every pomodoro with a theme and use these themes to
aggregate statistics in the ~/bob/dash_stats.md file. I would like to start
automatically labeling pomodoros by the corresponding projects and/or areas of the task
links contained in them. Can you help me implement this?

- As a part of this change, we should start aggregating the stats shown in the
  ~/bob/dash_stats.md file by area and project when possible.
- We will need the ability to exclude sub-projects of some projects from being
  aggregated and/or used to label pomodoros directly. Instead, task links to tasks in
  these sub-projects should be treated as if (when labeling pomodoro and aggregating
  stats) they pointed to tasks in the parent project that configured this. We should
  configure the ~/bob/sase.md project note to use this functionality.
- I'm not sure how/when/what to label pomodoros, so you should think hard about this.
- Review the pomodoro_area_project_attribution.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.4t.linker