#gh:gh_bobs-org__bob-cli Can you help me identify the 10 largest Rust files in this repository and then
create an epic plan using your /sase_plan skill with one phase of large size per file
(so 10 large phases)?

- Each phase should depend on the previous so these agents run in a sequence. Each agent
  should be tasked with splitting a single Rust file into multiple files, with the goal
  of keeping each file <=1500 lines in length.
- Recommend an approach to splitting each file but make it clear to these agents that
  they are responsible for planning the final split. In particular they may need to
  adjust their approach based on how the file they were assigned looks when that agent
  actually runs.

%m:@xlarge %auto %wait(bead=bob-cli-2d)