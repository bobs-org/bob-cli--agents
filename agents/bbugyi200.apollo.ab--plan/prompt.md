#gh:gh_bobs-org__bob-cli This repo is failing to build with the `just install` command on my macbook
(see the partial command output below for context). Can you help me diagnose the root
cause of this issue and fix it? #plan %m:@xlarge %auto

```
error[E0063]: missing field `verified` in initializer of `StoreWriteParams<'_>`
    --> src/native/highlights_ref/create.rs:3566:18
     |
3566 |     let params = super::source_store::StoreWriteParams {
     |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ missing `verified`

For more information about this error, try `rustc --explain E0063`.
error: could not compile `bob-obsidian` (lib) due to 1 previous error
error: failed to compile `bob-obsidian v0.3.1 (/Users/bbugyi/projects/github/bobs-org/bob-cli)`, intermediate artifacts can be found at `/Users/bbugyi/projects/github/bobs-org/bob-cli/target`.
To reuse those artifacts with a future compilation, set the environment variable `CARGO_BUILD_BUILD_DIR` to that path.
error: recipe `install` failed with exit code 101
  ✗ 1 new commit · 6f2f1932 → 36ae0ef0 · install failed (exit 101)

```