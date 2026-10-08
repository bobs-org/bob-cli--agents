- **PLAN:**
  [202610/ref_create_default_target_dedupe.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/ref_create_default_target_dedupe.md)
- **AGENTS:**
  - [bbugyi200.athena.0y6--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y6.md)

Can you help me make sure that the `bob ref create` command de-duplicates the target PDF
filename that is automatically used unless the `-o|--output` option is given explicitly?
If not, use your /sase_plan skill to plan the appropriate changes. I'm pretty sure that
this command currently fails if the automatically chosen PDF path already exists (which
is not correct). We should still fail if the same ref note has already been captured
(i.e. we already track this reference in my Obsidian vault).
