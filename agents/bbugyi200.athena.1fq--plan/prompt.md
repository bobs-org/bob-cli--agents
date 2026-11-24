#gh:gh_bobs-org__bob-cli The `just install` command just failed (see the command output below for context). Can you help me diagnose the root cause of this issue and fix it? #plan %m:@xlarge 
```
error[E0106]: missing lifetime specifier
   --> src/native/meetings/dossier.rs:348:56
    |
348 | fn class_fence(line: &str, class_name: &str) -> Option<&str> {
    |                      ----              ----            ^ expected named lifetime parameter
    |
    = help: this function's return type contains a borrowed value, but the signature does not say whether it is borrowed from `line` or `class_name`
help: consider introducing a named lifetime parameter
    |
348 | fn class_fence<'a>(line: &'a str, class_name: &'a str) -> Option<&'a str> {
    |               ++++        ++                   ++                 ++
warning: unused imports: `DossierDocument`, `DossierError`, and `render_dossier`
  --> src/native/meetings/mod.rs:19:20
   |
19 |     parse_dossier, render_dossier, DossierDocument, DossierError,
   |                    ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^  ^^^^^^^^^^^^
   |
   = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default
warning: unused imports: `MAX_NOTES_BYTES`, `NotesError`, `NotesInput`, `NotesSource`, and `read_notes`
  --> src/native/meetings/mod.rs:22:5
   |
22 |     read_notes, NotesError, NotesInput, NotesSource, MAX_NOTES_BYTES,
   |     ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^  ^^^^^^^^^^^^^^^
warning: unused import: `normalize::normalize`
  --> src/native/meetings/mod.rs:24:16
   |
24 | pub(crate) use normalize::normalize;
   |                ^^^^^^^^^^^^^^^^^^^^
warning: unused imports: `RecapState`, `ReplaceRecapError`, `recap_state`, `render_recap`, and `replace_recap`
  --> src/native/meetings/mod.rs:26:5
   |
26 |     recap_state, render_recap, replace_recap, RecapState, ReplaceRecapError,
   |     ^^^^^^^^^^^  ^^^^^^^^^^^^  ^^^^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^^^^^^^
error[E0308]: mismatched types
   --> src/native/meetings/normalize.rs:242:51
    |
242 |             notes.next_steps.push(parse_next_step(line));
    |                                   --------------- ^^^^ expected `String`, found `&str`
    |                                   |
    |                                   arguments to this function are incorrect
    |
note: function defined here
   --> src/native/meetings/normalize.rs:334:4
    |
334 | fn parse_next_step(text: String) -> MeetingNextStep {
    |    ^^^^^^^^^^^^^^^ ------------
help: try using a conversion method
    |
242 |             notes.next_steps.push(parse_next_step(line.to_string()));
    |                                                       ++++++++++++
Some errors have detailed explanations: E0106, E0308.
For more information about an error, try `rustc --explain E0106`.
warning: `bob-obsidian` (lib) generated 4 warnings
error: could not compile `bob-obsidian` (lib) due to 2 previous errors; 4 warnings emitted
error: failed to compile `bob-obsidian v0.6.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)`, intermediate artifacts can be found at `/Users/bbugyi/projects/github/bobs-org/bob-cli/target`.
To reuse those artifacts with a future compilation, set the environment variable `CARGO_BUILD_BUILD_DIR` to that path.
  ✗ build failed after 2:44 · exit 101
      error[E0106]: missing lifetime specifier
         --> src/native/meetings/dossier.rs:348:56
          |
      348 | fn class_fence(line: &str, class_name: &str) -> Option<&str> {
          |                      ----              ----            ^ expected named lifetime parameter
          |
          = help: this function's return type contains a borrowed value, but the signature does not say whether it is borrowed from `line` or `class_name`
      help: consider introducing a named lifetime parameter
          |
      348 | fn class_fence<'a>(line: &'a str, class_name: &'a str) -> Option<&'a str> {
          |               ++++        ++                   ++                 ++

      warning: unused imports: `DossierDocument`, `DossierError`, and `render_dossier`
        --> src/native/meetings/mod.rs:19:20
         |
      19 |     parse_dossier, render_dossier, DossierDocument, DossierError,
         |                    ^^^^^^^^^^^^^^  ^^^^^^^^^^^^^^^  ^^^^^^^^^^^^
         |
         = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default

      warning: unused imports: `MAX_NOTES_BYTES`, `NotesError`, `NotesInput`, `NotesSource`, and `read_notes`
        --> src/native/meetings/mod.rs:22:5
         |
      22 |     read_notes, NotesError, NotesInput, NotesSource, MAX_NOTES_BYTES,
         |     ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^  ^^^^^^^^^^^^^^^

      warning: unused import: `normalize::normalize`
        --> src/native/meetings/mod.rs:24:16
         |
      24 | pub(crate) use normalize::normalize;
         |                ^^^^^^^^^^^^^^^^^^^^

      warning: unused imports: `RecapState`, `ReplaceRecapError`, `recap_state`, `render_recap`, and `replace_recap`
        --> src/native/meetings/mod.rs:26:5
         |
      26 |     recap_state, render_recap, replace_recap, RecapState, ReplaceRecapError,
         |     ^^^^^^^^^^^  ^^^^^^^^^^^^  ^^^^^^^^^^^^^  ^^^^^^^^^^  ^^^^^^^^^^^^^^^^^

      error[E0308]: mismatched types
         --> src/native/meetings/normalize.rs:242:51
      full log  ~/.local/state/bob-cli/install-all/logs/20261124-111919-34110-bob-cli.log
      rerun with  just install-all -v  to stream build output
error: recipe `install` failed with exit code 101
  ✗ 2 new commits · e3e437ba → dbf405e3 · install failed (exit 101)

🧩  BOB-PLUGINS  2/3
────────────────────────────────────────────────
  $ bob plugins sync --dry-run --format json --no-pull --repo ~/projects/github/bobs-org/bob-plugins
  $ bob plugins sync --no-pull --repo ~/projects/github/bobs-org/bob-plugins
  $ bob plugins list --no-pull --repo ~/projects/github/bobs-org/bob-plugins --format json
  ✓ up to date · b5f2f6c · 12/12 plugins in sync

```