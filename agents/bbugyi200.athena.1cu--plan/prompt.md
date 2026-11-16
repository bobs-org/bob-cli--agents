#gh:gh_bobs-org__bob-cli Can you help me fix all of these issues (including the warnings)? See the command
output below for context. #plan %m:claude-fable-5

```
  $ just --justfile ~/projects/github/bobs-org/bob-cli/justfile install
error[E0061]: this function takes 6 arguments but 4 arguments were supplied
   --> src/native/bank/check_subscriptions.rs:58:18
    |
 58 |         .then(|| compute_ledger(registry, journal, rows, today));
    |                  ^^^^^^^^^^^^^^-------------------------------- two arguments of type `std::option::Option<&BankConfig>` and `&std::collections::HashMap<std::string::String, std::string::String>` are missing
    |
note: function defined here
   --> src/native/bank/subscriptions/ledger.rs:118:15
    |
118 | pub(crate) fn compute_ledger(
    |               ^^^^^^^^^^^^^^
...
123 |     config: Option<&BankConfig>,
    |     ---------------------------
124 |     raw_descs: &HashMap<String, String>,
    |     -----------------------------------
help: provide the arguments
    |
 58 |         .then(|| compute_ledger(registry, journal, rows, today, /* std::option::Option<&BankConfig> */, /* &std::collections::HashMap<std::string::String, std::string::String> */));
    |                                                               ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
For more information about this error, try `rustc --explain E0061`.
error: could not compile `bob-obsidian` (lib) due to 1 previous error
error: failed to compile `bob-obsidian v0.5.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)`, intermediate artifacts can be found at `/Users/bbugyi/projects/github/bobs-org/bob-cli/target`.
To reuse those artifacts with a future compilation, set the environment variable `CARGO_BUILD_BUILD_DIR` to that path.
  ✗ build failed after 0:54 · exit 101
      error[E0061]: this function takes 6 arguments but 4 arguments were supplied
         --> src/native/bank/check_subscriptions.rs:58:18
          |
       58 |         .then(|| compute_ledger(registry, journal, rows, today));
          |                  ^^^^^^^^^^^^^^-------------------------------- two arguments of type `std::option::Option<&BankConfig>` and `&std::collections::HashMap<std::string::String, std::string::String>` are missing
          |
      note: function defined here
         --> src/native/bank/subscriptions/ledger.rs:118:15
          |
      118 | pub(crate) fn compute_ledger(
          |               ^^^^^^^^^^^^^^
      ...
      123 |     config: Option<&BankConfig>,
          |     ---------------------------
      124 |     raw_descs: &HashMap<String, String>,
          |     -----------------------------------
      help: provide the arguments
          |
       58 |         .then(|| compute_ledger(registry, journal, rows, today, /* std::option::Option<&BankConfig> */, /* &std::collections::HashMap<std::string::String, std::string::String> */));
          |                                                               ++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

      For more information about this error, try `rustc --explain E0061`.
      error: could not compile `bob-obsidian` (lib) due to 1 previous error
      error: failed to compile `bob-obsidian v0.5.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)`, intermediate artifacts can be found at `/Users/bbugyi/projects/github/bobs-org/bob-cli/target`.
      To reuse those artifacts with a future compilation, set the environment variable `CARGO_BUILD_BUILD_DIR` to that path.
      full log  ~/.local/state/bob-cli/install-all/logs/20261115-193126-93628-bob-cli.log
      rerun with  just install-all -v  to stream build output
error: recipe `install` failed with exit code 101
  ✗ 5 new commits · 055f9b6e → 219e854e · install failed (exit 101)
```