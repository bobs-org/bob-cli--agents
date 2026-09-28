- **PLAN:**
  [202609/split_largest_rust_files.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202609/split_largest_rust_files.md)
- **AGENTS:**
  - [bbugyi200.apollo.2u--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.2u.md)

Can you help me identify the 10 largest Rust files in this repository and then create an
epic plan using your /sase_plan skill with one phase of large size per file (so 10 large
phases)?

- Each phase should depend on the previous so these agents run in a sequence. Each agent
  should be tasked with splitting a single Rust file into multiple files, with the goal
  of keeping each file <=1500 lines in length.
- Recommend an approach to splitting each file but make it clear to these agents that
  they are responsible for planning the final split. In particular they may need to
  adjust their approach based on how the file they were assigned looks when that agent
  actually runs.
