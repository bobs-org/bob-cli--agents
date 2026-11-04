#gh:gh_bobs-org__bob-cli Can you help me fix this build warning (see the partial command output below for context)? #plan %m:@xlarge 
```
  Installing bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)
    Updating crates.io index
warning: unused import: `std::os::unix::io::AsRawFd`
   --> src/native/capture/shell_guard.rs:124:13
    |
124 |         use std::os::unix::io::AsRawFd;
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = note: `#[warn(unused_imports)]` (part of `#[warn(unused)]`) on by default

warning: `bob-obsidian` (lib) generated 1 warning (run `cargo fix --lib -p bob-obsidian` to apply 1 suggestion)
    Finished `local-install` profile [optimized] target(s) in 0.98s
   Replacing /Users/bbugyi/.cargo/bin/bob
   Replacing /Users/bbugyi/.cargo/bin/bob_notify
   Replacing /Users/bbugyi/.cargo/bin/bob_pomodoro
   Replacing /Users/bbugyi/.cargo/bin/tmux_bob_pomodoro
    Replaced package `bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)` with `bob-obsidian v0.4.0 (/Users/bbugyi/projects/github/bobs-org/bob-cli)` (executables `bob`, `bob_notify`, `bob_pomodoro`, `tmux_bob_pomodoro`)
```