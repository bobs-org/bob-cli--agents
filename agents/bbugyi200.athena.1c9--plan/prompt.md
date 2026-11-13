#gh:gh_bobs-org__bob-cli Is there a plan to use this function by an in-progress epic? #if_not_plan See
the command output below for context.

#plan %m:@xlarge

```
  $ just --justfile ~/projects/github/bobs-org/bob-cli/justfile install
warning: function `command_on_path` is never used
   --> src/native/desktop_notify.rs:116:15
    |
116 | pub(crate) fn command_on_path(command: &str) -> bool {
    |               ^^^^^^^^^^^^^^^
    |
    = note: `#[warn(dead_code)]` (part of `#[warn(unused)]`) on by default
warning: `bob-obsidian` (lib) generated 1 warning
```