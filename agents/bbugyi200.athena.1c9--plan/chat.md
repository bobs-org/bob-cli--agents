# Chat History - ace-run (1c9--plan)

- **TIMESTAMP:** 2026-11-13 17:40:04 EST
- **MODEL:** claude/opus
- **AGENT:** 1c9--plan

**Plan:** /home/bryan/.sase/plans/202611/desktop_notify_macos_dead_code.md


## Proposed Plan Preview

*Plan submitted for review.*

**Plan file:** `/home/bryan/.sase/plans/202611/desktop_notify_macos_dead_code.md`

> # Remove the macOS-dead `command_on_path` from `desktop_notify`
> ## Problem
> On macOS, every build of bob-cli warns:
> ```
> warning: function `command_on_path` is never used
>    --> src/native/desktop_notify.rs:116:15
> ```
> The macOS CI step `Lint macOS-only targets` runs `just lint`, which builds with
> `-D unused`. That turns the warning into a hard error:
> `error: function command_on_path is never used` (CI run 43513864920, master `21d12f23`).

*See full plan file for details.*

## Prompt

#gh:gh_bobs-org__bob-cli Is there a plan to use this function by an in-progress epic? If not, use your /sase_plan skill to plan the appropriate changes.
 See
the command output below for context.

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose and author the appropriate
tier, validate and revalidate until it passes, then submit it with `sase plan propose` (as the skill instructs)
before making any file changes.
 %m:@xlarge

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

## Response

I'm checking whether any in-progress epic (the Gmail-archive epic `bob-cli-kx` is the likely one) plans to use `command_on_path`.

No in-progress epic uses it — it's macOS-only dead code from the `desktop_notify` extraction. I'm checking whether macOS CI is already red because of it.

Confirmed: no epic plans to use it, and it's one of two hard errors failing the macOS `just lint` CI step. Loading the planning skill now.

The macOS `just lint` step has a second, unrelated hard error: `libc::ptsname_r` in the gcal ack PTY tests. I'll keep the plan narrow and file that one as its own CI task bead.

The gcal ack epic `bob-cli-l5` is still active and caused the `ptsname_r` break, so per bead policy it gets a `DISCOVERED ISSUE:` note on that epic, not a new task.

The daily release train runs full CI including macOS, so this dead-code error also blocks the release `bob-cli-kx.5` is waiting on. I'll record that on the Gmail epic, then write the plan.

The `aarch64-apple-darwin` target is installed here, so I'll check whether a Linux cross-check reproduces the macOS warning. That would give the implementer a local check before CI.

A Linux cross-check isn't viable (`rquickjs-sys` needs an Apple C toolchain), so macOS CI stays the gate. Writing the plan now.

Validation passes. Proposing the plan.

No in-progress epic plans to use `command_on_path`. It's dead code on macOS, and I've proposed a small plan that deletes it. It's waiting for your approval, and no code has changed yet.

**Why it's unused:** commit `cd6aefae` (Gmail archive receipts, `bob-cli-kx.3.1.4`) moved the function out of `vault_sync.rs` into the new `src/native/desktop_notify.rs`. In its old home it was marked `#[cfg(not(target_os = "macos"))]`, so it was only compiled on Linux. The move dropped that marking. Its only caller is the Linux-only `notify-send` path, so on the Mac it compiles with nothing calling it.

**Is anything planning to use it?** No:
- The only active epic touching this file is `bob-cli-kx`. Its last open phase, `kx.5`, is live enable and verification (config, a released build, a gated live sync), not new Rust code.
- No plan file or bead mentions `command_on_path`.

**It's more than a warning.** The macOS CI lint step turns unused-code warnings into errors, so it fails on this (run 43513864920 on `21d12f23`). The daily release runs that same CI, so this also blocks the release `kx.5` is waiting for.

**The plan** (`size: small`, one file, `src/native/desktop_notify.rs`):
- Delete `command_on_path`.
- Look up `notify-send` with the existing shared `bob_env::find_on_path`, which `gog`, `xelatex`, `curl` and `uv` already use.
- Keep the command it builds as plain `notify-send`, so the existing test stays as it is.
- One small difference: `find_on_path` also requires the file to be executable. A non-executable `notify-send` couldn't run before either, so nothing visible changes. The plan adds a test that pins this.
- Checks: unit tests and `just lint` on Linux, then the macOS CI log for the pushed commit. I tried a macOS build check from Linux, but it fails building the `rquickjs-sys` dependency, so macOS CI is the only real check.

**macOS CI still won't go green with this alone.** The same lint run has a second error, from the gcal ack epic (`307616ae`, `bob-cli-l5.3.1.3`): `libc::ptsname_r` doesn't exist on macOS. It's in `src/native/gcal/ack.rs:2854` and `tests/gcal_ack_tty.rs:86`. The Ubuntu test job also fails separately, which `bob-cli-l2` tracks.

**Bead notes I added:**
- `bob-cli-l5` (gcal ack epic, which caused the `ptsname_r` break): a note describing it and a possible fix, instead of a new task bead.
- `bob-cli-kx` (Gmail epic): a note explaining the root cause and that this plan fixes it, so its land agent doesn't fix it a second time.
