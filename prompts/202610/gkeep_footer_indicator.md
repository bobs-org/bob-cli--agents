- **AGENTS:**
  - [bbugyi200.apollo.research.2y.linker.w0](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.research.2y.linker.w0.md)

%auto #gh:gh_bobs-org__bob-cli I would like to add a new indicator to the footer in
Obsidian that shows how many notes I currently have in Google Keep that would be synced
if the `bob gkeep pull` command were run. Can you help me implement this?

- This indicator should only be shown if Google Keep has been properly authenticated
  (i.e. the `bob gkeep pull` command would actually work).
- We should be careful not to sync with Google Keep too often to avoid overwhelming the
  API or doing more work on my macbook than is necessary/useful. Think hard about the
  best way to approach this.
- We should also show the number of non-closed (any status but `[x]` or `[-]`) tasks in
  the ~/bob/gkeep_inbox.md file (this count can be synced much more often--it should
  take seconds at most). Make sure this count is made visually distinct from the Google
  Keep note count somehow.
- Review the gkeep_inbox_footer_indicator.md file in the research sidecar repo for
  context and inspiration before planning. I agree with all of the requirements
  recommended in that research file (but keep in mind that you are responsible for
  planning and splitting up this work appropriately).
- #beau

#plan %m:@xlarge %w:research.2y.linker
