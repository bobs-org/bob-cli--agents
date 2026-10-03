#gh:gh_bobs-org__bob-cli I want to give the `bob` command excellent command-line completion (like the
sase project has, for example--though that is a Python project, not a Rust project). Can
you help me implement this?

- Review the `sase completion` command's interface (e.g. its sub-commands and options)
  for context and inspiration.
- As a part of this change, we should add a new `just install` target that users can use
  to install this package from source using the `cargo install` command. When
  `just install` is run, command-line completion for the `bob` command should also be
  updated.
- Review the bob_shell_completion_and_just_install.md file in the research sidecar repo for context and inspiration
  before planning. I agree with all of the recommendations made in that research file.
- #beau

#plan %m:@xlarge %auto