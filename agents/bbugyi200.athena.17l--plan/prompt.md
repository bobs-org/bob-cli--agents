#gh:gh_bobs-org__bob-cli I think we broken something recently (see the partial `just install` command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan %m:@xlarge 
```
  Installing bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)
    Updating crates.io index
   Compiling bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)
error[E0063]: missing field `note_pull` in initializer of `native::capture::output::CaptureItemResult`
    --> src/native/capture/plan.rs:2012:25
     |
2012 |                 result: CaptureItemResult {
     |                         ^^^^^^^^^^^^^^^^^ missing `note_pull`

    Building [=======================> ] 204/209: bob-obsidian
```