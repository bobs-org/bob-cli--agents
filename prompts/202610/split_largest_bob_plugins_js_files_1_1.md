- **PLAN:**
  [202610/split_largest_bob_plugins_js_files_1.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/split_largest_bob_plugins_js_files_1.md)
- **AGENTS:**
  - [bbugyi200.apollo.54--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.54.md)

Can you help me identify the 4 largest JavaScript files in bob-plugins and then create
an epic plan using your /sase_plan skill with one phase of large size per file (so 4
large phases)?

- Each phase should depend on the previous so these agents run in a sequence. Each agent
  should be tasked with splitting a single JavaScript file into multiple files, with the
  goal of keeping each file <=1000 lines in length.
- Recommend an approach to splitting each file but make it clear to these agents that
  they are responsible for planning the final split. In particular they may need to
  adjust their approach based on how the file they were assigned looks when that agent
  actually runs.
