#gh:gh_bobs-org__bob-cli We recently added support for link relations, which are currently always
directed. I would like to start making any relation that does not have a description an
undirected relation instead. Can you help me implement this?

- I was thinking we should just show `links` instead of `links to` and `links from` for
  these.
- Any relation with a description would then become a directed relation (update the
  glossary term and add new ones for "directed" and "undirected" relations).
- Linking another note to the current note (using the `~~` syntax, for example) then
  only makes sense if a relation description is provided (otherwise, it is the same as
  linking to a task directly using `~`, for example).
- Review the undirected_task_relations.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the requirements recommended in that research
  file (but keep in mind that you are responsible for planning and splitting up this
  work appropriately).
- #beau

#plan %m:@xlarge %w:research.29.linker