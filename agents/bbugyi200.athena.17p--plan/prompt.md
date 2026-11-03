#gh:gh_bobs-org__bob-cli It looks like the `just install` command is failing again (see recent, related
git commits). Can you help me fix this? See the partial command output below for
context. Leave notes on any beads as appropriate (I suspect an in-progress epic bead is
to blame for this breakage and the previous one).

#plan %m:@xlarge %auto

```
error[E0062]: field `note_pull` specified more than once
    --> src/native/capture/plan.rs:2102:21
     |
2020 |                     note_pull: None,
     |                     --------------- first use of `note_pull`
...
2102 |                     note_pull: None,
     |                     ^^^^^^^^^ used more than once

For more information about this error, try `rustc --explain E0062`.
error: could not compile `bob-obsidian` (lib) due to 1 previous error
error: failed to compile `bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)`, intermediate artifacts can be found at `/Users/bbugyi/projects/github/bobs-org/bob-cli/target`.
To reuse those artifacts with a future compilation, set the environment variable `CARGO_BUILD_BUILD_DIR` to that path.
error: recipe `install` failed with exit code 101
  ✗ 1 new commit · 9a606395 → a95d5d8f · install failed (exit 101)
```