#gh:gh_bobs-org__bob-cli #fork:4r I made several mistakes with the previous request. Can you help me fix
these issues?

- We should only show a `^prj` task if that project note file has no open tasks
  (including blocked, pending, and next; but not closed or done).
- We should actually add two new configuration fields to control how often we need to
  review the freshness of `^prj` and `^ref` tasks. `^prj` tasks should be configured (in
  my chezmoi repo) to `1` (so, even if they have a `fresh` property already, I am made
  aware of projects that have no open tasks the next day when I do my morning GTD)
  whereas `^ref` tasks should be configured to `3`.
- Let's close all open `^ref` tasks that were created more than 7 days ago. Most of
  these are read anyway and this would be too much to review otherwise.

#plan %m:gpt-6-astra %auto