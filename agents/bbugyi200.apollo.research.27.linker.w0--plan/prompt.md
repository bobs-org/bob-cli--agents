#gh:gh_bobs-org__bob-cli I would love to be able to start showing likely related tasks in the
bob-mac-capture app's preview panel when the capture the user has input will result in
one or more new tasks being created. Can you help me implement this?

- The main benefit of this feature would be that it gives the user a heads up about
  duplicate tasks and/or related tasks that they might want to link to in some way.
- The biggest concern here is performance. The bob-mac-capture app must remain blazing
  fast.
- A secondary concern would be how we fit all of this in the panel without making it too
  cramped or making the user need to scroll too often.
- Review the capture_similar_tasks_band.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %auto %w:research.27.linker