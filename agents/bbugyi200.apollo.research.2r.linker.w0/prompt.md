#gh:gh_bobs-org__bob-cli I would like to add support for certain configured relation descriptions to
automatically trigger the cancelation of the source task. Can you help me implement
this?

- To start, we should configure (in my chezmoi repo) the "duplicate of" and "superseded
  by" relation descriptions to auto-cancel the source task.
- We should provide a clear indication to the user when the relation description they
  are selecting would result in cancelation.
- We should make sure to remove any task links in the current daily file that point to
  the canceled task (handle this case just like other cases where we cancel tasks).
- Review the cancel_labels_for_task_relations.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.2r.linker