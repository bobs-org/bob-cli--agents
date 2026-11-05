# Chat History - ace-run (18l--mon-0)

- **TIMESTAMP:** 2026-11-05 10:52:20 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** 18l--mon-0

## Prompt

sase monitor start --command 'set +e; cargo clippy --all-targets -- -D warnings; clippy_rc=$?; cargo test task_status_hooks; hooks_rc=$?; cargo test pomodoro_homes; homes_rc=$?; cargo test --test cli task_status_hooks; cli_rc=$?; just docs-gen; docs_rc=$?; printf "Verification exit codes: clippy=%s task_status_hooks=%s pomodoro_homes=%s cli=%s docs_gen=%s\\n" "$clippy_rc" "$hooks_rc" "$homes_rc" "$cli_rc" "$docs_rc"; test "$clippy_rc" -eq 0 && test "$hooks_rc" -eq 0 && test "$homes_rc" -eq 0 && test "$cli_rc" -eq 0 && test "$docs_rc" -eq 0' --reason 'Run the approved reconcile coalescing verification after clippy fixes'

## Response

sase tool run 08cf56f6ed46d31b9ce77008f87a29aa
    Checking bitflags v2.12.1
   Compiling vcpkg v0.2.15
   Compiling pkg-config v0.3.33
   Compiling rustix v1.1.5
    Checking time-core v0.1.9
    Checking num-conv v0.2.2
    Checking powerfmt v0.2.0
    Checking linux-raw-sys v0.12.1
    Checking deranged v0.5.8
    Checking quick-xml v0.41.0
    Checking once_cell v1.21.4
    Checking fallible-iterator v0.3.0
    Checking fastrand v2.5.0
    Checking fallible-streaming-iterator v0.1.9
    Checking base64 v0.22.1
    Checking hashlink v0.12.1
    Checking png v0.18.1
    Checking lopdf v0.40.0
   Compiling libsqlite3-sys v0.38.1
    Checking time v0.3.53
    Checking image v0.25.10
    Checking tempfile v3.27.0
    Checking plist v1.10.0
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_29)
    Checking rusqlite v0.40.1
error: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:563:12
    |
563 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `-D clippy::int-plus-one` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::int_plus_one)]`

error: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:383:20
    |
383 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

error: this `else` branch is empty
   --> src/native/task_cancel/prune.rs:119:15
    |
119 |               } else {
    |  _______________^
120 | |             }
    | |_____________^ help: you can remove it
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_else
    = note: `-D clippy::needless-else` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::needless_else)]`

error: `format!` in `println!` args
   --> src/native/articles/render.rs:170:5
    |
170 | /     println!(
171 | |         "{} {} {}",
172 | |         styler.cyan("Articles"),
173 | |         styler.separator(),
174 | |         format!("{total} · {}", display_root(root))
175 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `println!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args
    = note: `-D clippy::format-in-format-args` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::format_in_format_args)]`

error: this function has too many arguments (8/7)
   --> src/native/attachments/journal.rs:108:1
    |
108 | / pub(crate) fn append_event(
109 | |     vault: &Path,
110 | |     host: &str,
111 | |     saved: &str,
...   |
116 | |     ts: DateTime<FixedOffset>,
117 | | ) -> io::Result<String> {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments
    = note: `-D clippy::too-many-arguments` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::too_many_arguments)]`

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:23:54
   |
23 |     pub(super) fn validate(&self, bob_dir: &Path) -> Result<(), CaptureError> {
   |                                                      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
   = note: `-D clippy::result-large-err` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::result_large_err)]`

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:81:10
   |
81 |     ) -> Result<(), CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:147:10
    |
147 |     ) -> Result<bool, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:155:10
    |
155 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:169:10
    |
169 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:184:10
    |
184 |     ) -> Result<Option<String>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:237:10
    |
237 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:256:10
    |
256 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:370:10
    |
370 |     ) -> Result<usize, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:395:10
    |
395 |     ) -> Result<Vec<StagedTextFile>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:432:6
    |
432 | ) -> Result<Vec<usize>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:484:6
    |
484 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:25:6
   |
16 |     Capture(CaptureError),
   |     --------------------- the largest variant contains at least 248 bytes
...
25 | ) -> Result<MovePlan, BatchMoveError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: try reducing the size of `native::capture::batch_move::BatchMoveError`, for example by boxing large elements or replacing it with `Box<native::capture::batch_move::BatchMoveError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:40:6
   |
16 |     Capture(CaptureError),
   |     --------------------- the largest variant contains at least 248 bytes
...
40 | ) -> Result<MovePlan, BatchMoveError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: try reducing the size of `native::capture::batch_move::BatchMoveError`, for example by boxing large elements or replacing it with `Box<native::capture::batch_move::BatchMoveError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch_move.rs:70:6
   |
70 | ) -> Result<VaultSnapshot, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch_move.rs:110:6
    |
110 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch_move.rs:130:6
    |
130 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:38:6
   |
38 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:91:6
   |
91 | ) -> Result<DependentRef, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:226:6
    |
226 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:253:6
    |
253 | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/blocked_tasks.rs:244:1
    |
244 | / pub(super) fn plan_blocked_task_writes(
245 | |     ctx: &mut DependencyContext,
246 | |     planner: &mut CaptureBatchPlanner,
247 | |     bob_dir: &Path,
...   |
252 | |     options: ExistingDependencyOptions,
253 | | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    | |_______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocks_mirror.rs:52:6
   |
52 | ) -> Result<Option<(BlocksLineUpdateJson, TaskBlockRef)>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:237:6
    |
237 | ) -> Result<TaskBlockRef, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:266:6
    |
266 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:293:6
    |
293 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/budget.rs:333:6
    |
333 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:841:10
    |
841 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:883:22
    |
883 |                   .map(|values| {
    |  ______________________^
884 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
885 | |                 })
    | |_________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:884:32
    |
884 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
    |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:891:26
    |
891 |                       .map(|vals| {
    |  __________________________^
892 | |                         vals.map(|raw| {
893 | |                             super::move_choice::parse_move_in_picks(raw)
894 | |                         })
895 | |                         .collect::<Result<Vec<_>, _>>()
896 | |                     })
    | |_____________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:892:34
    |
892 |                           vals.map(|raw| {
    |  __________________________________^
893 | |                             super::move_choice::parse_move_in_picks(raw)
894 | |                         })
    | |_________________________^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:905:22
    |
905 |                 .map(|raw| parse_pull_in_picks(raw))
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:920:6
    |
920 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:934:6
    |
934 | ) -> Result<PullInPicks, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:970:6
    |
970 | ) -> Result<InboxRoutePick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:999:6
    |
999 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
    --> src/native/capture/cli.rs:1010:14
     |
1010 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1017:6
     |
1017 | ) -> Result<SubBulletTarget, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1030:6
     |
1030 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1079:6
     |
1079 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1110:6
     |
1110 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:28:6
   |
28 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:44:6
   |
44 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
  --> src/native/capture/commit.rs:59:55
   |
59 |           write_staged_files_guarded(&batch.text_files, || {
   |  _______________________________________________________^
60 | |             batch.read_guards.validate(bob_dir)
61 | |         })
   | |_________^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:132:6
    |
132 | ) -> Result<Vec<PathBuf>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:177:6
    |
177 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:222:6
    |
222 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:223:39
    |
223 |     write_staged_files_guarded(files, || Ok(()))
    |                                       ^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:229:6
    |
229 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/commit.rs:273:35
    |
273 |         validate_reads().and_then(|()| validate_disk_preimages(files))
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:408:6
    |
408 | ) -> Result<PathBuf, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:477:45
    |
477 | pub(super) fn read_target(target: &Path) -> Result<String, CaptureError> {
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/capture/dependencies.rs:65:19
   |
65 |       close_policy: OnceLock<(
   |  ___________________^
66 | |         Vec<config::relations::CancelLabel>,
67 | |         Vec<config::relations::CompleteLabel>,
68 | |         Vec<config::relations::CancelLabel>,
69 | |         Vec<config::relations::CancelLabel>,
70 | |         Option<String>,
71 | |     )>,
   | |______^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
   = note: `-D clippy::type-complexity` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::type_complexity)]`

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture/dependencies.rs:306:10
    |
306 |       ) -> &(
    |  __________^
307 | |         Vec<config::relations::CancelLabel>,
308 | |         Vec<config::relations::CompleteLabel>,
309 | |         Vec<config::relations::CancelLabel>,
310 | |         Vec<config::relations::CancelLabel>,
311 | |         Option<String>,
312 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1035:6
     |
1035 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1201:6
     |
1201 | ) -> Result<PathBuf, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1318:6
     |
1318 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1370:6
     |
1370 | ) -> Result<(String, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1481:6
     |
1481 | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:1472:1
     |
1472 | / fn resolve_prerequisites(
1473 | |     ctx: &DependencyContext,
1474 | |     planner: &mut CaptureBatchPlanner,
1475 | |     bob_dir: &Path,
...    |
1480 | |     dependent_desc: &str,
1481 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1571:10
     |
1571 |     ) -> Result<Self, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1814:24
     |
1814 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1903:6
     |
1903 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2044:6
     |
2044 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2065:6
     |
2065 | ) -> Result<Vec<TaskBlockRef>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2078:6
     |
2078 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2103:6
     |
2103 | ) -> Result<Vec<TargetTouch>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2193:6
     |
2193 | ) -> Result<Option<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2373:6
     |
2373 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2373:6
     |
2373 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2582:6
     |
2582 | ) -> Result<PlannedDependencyUpdate, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3088:6
     |
3088 | ) -> Result<(AugmentedNewTask, PlannedDependencyUpdateParts), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3352:6
     |
3352 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3410:6
     |
3410 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:42:6
   |
42 | ) -> Result<ResolvedLinkGuard, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:79:6
   |
79 | ) -> Result<DropAttempt, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/ensure_next.rs:23:6
   |
23 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/event_conflict.rs:290:1
    |
290 | / pub(super) fn detect_event_conflict(
291 | |     contents: &str,
292 | |     date: NaiveDate,
293 | |     session_name: Option<&str>,
...   |
298 | |     fit: &FitKind,
299 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (10/7)
   --> src/native/capture/event_conflict.rs:314:1
    |
314 | / pub(super) fn detect_event_conflict_with<V: CloseVault + ?Sized>(
315 | |     contents: &str,
316 | |     date: NaiveDate,
317 | |     session_name: Option<&str>,
...   |
324 | |     day_relative: Option<&Path>,
325 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/existing_task_link.rs:57:6
   |
57 | ) -> Result<ExistingTaskLinkOutcome, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:144:6
    |
144 | ) -> Result<InboxRouteReport, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:345:6
    |
345 | ) -> Result<AppliedInboxRoutes, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:327:6
    |
327 | ) -> Result<LinkGuardVerdict, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:597:6
    |
597 | ) -> Result<Option<ConsumePlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:709:6
    |
709 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:203:6
    |
203 | ) -> Result<i64, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:533:6
    |
533 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:580:6
    |
580 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:599:6
    |
599 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:804:6
    |
804 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/move_choice.rs:40:6
   |
40 | ) -> Result<MoveInPicks, super::output::CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/move_choice.rs:367:6
    |
367 | ) -> Result<Option<MoveChoiceSlot>, super::output::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/move_choice.rs:462:14
    |
462 |         .map(|off| super::plan::scheduled_date_string(today, off))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/move_choice.rs:951:6
    |
951 | ) -> Result<Vec<Option<char>>, super::output::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1162:6
     |
1162 | ) -> Result<MoveChoiceReport, super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1378:6
     |
1378 | ) -> Result<MoveChoiceReport, super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/move_choice.rs:1560:6
     |
1560 | ) -> Result<(), super::output::CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/note_pull.rs:58:6
   |
58 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/open_notes.rs:138:1
    |
138 | / fn open_note_for_item(
139 | |     bob_dir: &Path,
140 | |     item: &CaptureItemResult,
141 | |     path: &Path,
...   |
146 | |     settings: &note_tasks::NoteTaskSettings,
147 | | ) -> OpenNoteJson {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (13/7)
   --> src/native/capture/output.rs:503:5
    |
503 | /     pub(super) fn from_items(
504 | |         items: Vec<CaptureItemResult>,
505 | |         global_destination: Option<GlobalDestinationSummary>,
506 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
516 | |         move_choice: super::move_choice::MoveChoiceReport,
517 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/capture/output.rs:6782:5
     |
6782 | /     pub(super) fn pull_in_choice_required(
6783 | |         extra: serde_json::Map<String, serde_json::Value>,
6784 | |         human_unblocked: Vec<TaskCompleteUnblockedJson>,
6785 | |         human_keep_moving_folds: Vec<
...    |
6794 | |         human_note_pull_groups: Vec<PullInGroupJson>,
6795 | |     ) -> Self {
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:66:6
   |
66 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:74:6
   |
74 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:811:6
    |
811 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:907:6
    |
907 | ) -> Result<FanoutClipboardRead, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:968:6
    |
968 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1177:6
     |
1177 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:1284:6
     |
1284 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (14/7)
    --> src/native/capture/plan.rs:1269:1
     |
1269 | / pub(super) fn plan_capture_item(
1270 | |     request: &CaptureRequest,
1271 | |     parsed_item: ParsedCaptureItem,
1272 | |     now: chrono::NaiveDateTime,
...    |
1283 | |     project_moves: &[ProjectMoveLanding],
1284 | | ) -> Result<PlannedCaptureItem, CaptureError> {
     | |_____________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:1963:14
     |
1963 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:2148:11
     |
2148 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3661:6
     |
3661 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3775:6
     |
3775 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3804:6
     |
3804 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3890:6
     |
3890 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3931:6
     |
3931 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:4151:6
     |
4151 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:4612:13
     |
4612 |             &String::new(),
     |             ^^^^^^^^^^^^^^ help: try: `""`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_owned_empty_strings
     = note: `-D clippy::unnecessary-owned-empty-strings` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::unnecessary_owned_empty_strings)]`

error: the `Err`-variant returned from this function is very large
 --> src/native/capture/pomodoro_adjust.rs:8:6
  |
8 | ) -> Result<(), CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:24:6
   |
24 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:62:6
   |
62 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:131:6
    |
131 | ) -> Result<RunningSessionTarget, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:215:6
    |
215 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:271:6
    |
271 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:511:6
    |
511 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:593:6
    |
593 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:638:6
    |
638 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:823:6
    |
823 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1322:6
     |
1322 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1358:6
     |
1358 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1519:6
     |
1519 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1693:6
     |
1693 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1856:6
     |
1856 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2151:6
     |
2151 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2227:6
     |
2227 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2340:6
     |
2340 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2878:6
     |
2878 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_insert.rs:56:6
   |
56 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:127:6
    |
127 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:264:6
    |
264 | ) -> Result<DefaultPomodoroPick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:356:6
    |
356 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:468:6
    |
468 | ) -> Result<NamedPomodoroResolution<'a>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:499:6
    |
499 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (9/7)
   --> src/native/capture/pomodoro_insert.rs:489:1
    |
489 | / pub(super) fn insert_named_pomodoro_child_block(
490 | |     contents: &str,
491 | |     block: &str,
492 | |     selector: &str,
...   |
498 | |     open: &[(usize, &str)],
499 | | ) -> Result<(String, Placement, usize, String), CaptureError> {
    | |_____________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:572:6
    |
572 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_link.rs:18:6
   |
18 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:230:6
    |
230 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:286:6
    |
286 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:707:6
    |
707 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:792:6
    |
792 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:971:6
    |
971 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1016:6
     |
1016 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1808:6
     |
1808 | ) -> Result<&str, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_merge.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the loop variable `index` is only used to index `lines`
  --> src/native/capture/pomodoro_merge.rs:94:18
   |
94 |     for index in (entry_index + 1)..=end {
   |                  ^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
   = note: `-D clippy::needless-range-loop` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::needless_range_loop)]`
help: consider using an iterator
   |
94 -     for index in (entry_index + 1)..=end {
94 +     for <item> in lines.iter().take(end + 1).skip((entry_index + 1)) {
   |

error: the loop variable `index` is used to index `lines`
   --> src/native/capture/pomodoro_merge.rs:114:18
    |
114 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
114 -     for index in (entry_index + 1)..=end {
114 +     for (index, <item>) in lines.iter().enumerate().take(end + 1).skip((entry_index + 1)) {
    |

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:250:6
    |
250 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:448:6
    |
448 | ) -> Result<ResolvedMerge, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:664:6
    |
664 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/pomodoro_merge.rs:655:1
    |
655 | / pub(super) fn plan_pomodoro_merge_item(
656 | |     request: &CaptureRequest,
657 | |     parsed: ParsedCaptureText,
658 | |     spec: PomodoroMergeSpec,
...   |
663 | |     warnings: &mut Vec<CaptureWarning>,
664 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_past.rs:93:6
   |
93 | ) -> Result<PastPreflight, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: manual `!RangeInclusive::contains` implementation
   --> src/native/capture/pomodoro_past.rs:177:24
    |
177 |         if t > 1440 || end > 1440 || end < 0 {
    |                        ^^^^^^^^^^^^^^^^^^^^^ help: use: `!(0..=1440).contains(&end)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_range_contains
    = note: `-D clippy::manual-range-contains` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::manual_range_contains)]`

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:423:6
    |
423 | ) -> Result<Vec<TrimPlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:633:6
    |
633 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:666:6
    |
666 | ) -> Result<(usize, String, PastTargetSource, Option<String>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:802:6
    |
802 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:840:6
    |
840 | ) -> Result<(String, usize, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the variable `idx` is used as a loop counter
   --> src/native/capture/pomodoro_past.rs:888:5
    |
888 |     for line in &block_lines {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (idx, line) in (insert_at..).zip(block_lines.iter())`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
    = note: `-D clippy::explicit-counter-loop` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::explicit_counter_loop)]`

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_past.rs:921:6
    |
921 | ) -> Result<super::plan::PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_split.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the loop variable `index` is only used to index `lines`
   --> src/native/capture/pomodoro_split.rs:194:18
    |
194 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
194 -     for index in (entry_index + 1)..=end {
194 +     for <item> in lines.iter().take(end + 1).skip((entry_index + 1)) {
    |

error: the loop variable `index` is used to index `lines`
   --> src/native/capture/pomodoro_split.rs:214:18
    |
214 |     for index in (entry_index + 1)..=end {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
214 -     for index in (entry_index + 1)..=end {
214 +     for (index, <item>) in lines.iter().enumerate().take(end + 1).skip((entry_index + 1)) {
    |

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_split.rs:295:6
    |
295 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/pomodoro_split.rs:286:1
    |
286 | / pub(super) fn plan_pomodoro_split_item(
287 | |     request: &CaptureRequest,
288 | |     parsed: ParsedCaptureText,
289 | |     spec: PomodoroSplitSpec,
...   |
294 | |     warnings: &mut Vec<CaptureWarning>,
295 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:19:6
   |
19 | ) -> Result<(String, String, u64, String), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:54:6
   |
54 |   ) -> Result<
   |  ______^
55 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
56 | |     CaptureError,
57 | | > {
   | |_^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:107:6
    |
107 |   ) -> Result<
    |  ______^
108 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
109 | |     CaptureError,
110 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:425:6
    |
425 |   ) -> Result<
    |  ______^
426 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
427 | |     CaptureError,
428 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:518:6
    |
518 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:570:6
    |
570 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:629:6
    |
629 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:648:6
    |
648 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:806:6
    |
806 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:818:6
    |
818 | ) -> Result<(String, Placement, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:863:6
    |
863 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:889:6
    |
889 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1190:6
     |
1190 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1451:6
     |
1451 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2093:6
     |
2093 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2196:6
     |
2196 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2261:6
     |
2261 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2431:6
     |
2431 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:105:6
    |
105 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:292:6
    |
292 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:311:6
    |
311 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:512:6
    |
512 | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/project_deps.rs:503:1
    |
503 | / pub(super) fn restamp_changed_timed_entries(
504 | |     planner: &mut CaptureBatchPlanner,
505 | |     bob_dir: &Path,
506 | |     day_file: &Path,
...   |
511 | |     warnings: &mut Vec<CaptureWarning>,
512 | | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    | |________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:18:6
   |
18 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:36:6
   |
36 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:79:6
   |
79 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
   --> src/native/capture/project_note.rs:154:14
    |
154 |         .map(|offset| scheduled_date_string(today, offset))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2135:6
     |
2135 | ) -> Result<Vec<ResolvedProjectMove>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2300:6
     |
2300 | ) -> Result<ProjectMoveExecution, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this closure is very large
    --> src/native/capture/project_note.rs:2312:14
     |
2312 |           .map(|movement| {
     |  ______________^
2313 | |             slot_by_source.get(&movement.source_index).copied().ok_or_else(
2314 | |                 || {
2315 | |                     CaptureError::io(
...    |
2320 | |         })
     | |_________^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:2917:6
     |
2917 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/pull_in.rs:11:6
   |
11 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:289:6
    |
289 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/relation_sources.rs:55:6
   |
55 | ) -> Result<Option<RelationSourceRead>, super::CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relation_sources.rs:364:6
    |
364 | ) -> Result<(), super::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:164:6
    |
164 | ) -> Result<PlannedRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:225:10
    |
225 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:254:6
    |
254 | ) -> Result<RelationOwner, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:314:6
    |
314 | ) -> Result<ResolvedRelation, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:391:6
    |
391 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:416:6
    |
416 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:460:6
    |
460 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:494:6
    |
494 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:570:6
    |
570 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:667:6
    |
667 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:716:6
    |
716 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:808:6
    |
808 | ) -> Result<(RelationAction, Option<String>, String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:916:1
    |
916 | / fn relation_update_json(
917 | |     direction: RelationDirection,
918 | |     source_relative: &Path,
919 | |     source_line: usize,
...   |
924 | |     previous_label: Option<String>,
925 | | ) -> RelationUpdateJson {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:961:6
    |
961 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_cancel.rs:36:6
   |
36 | ) -> Result<Vec<RelationCancelJson>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:112:6
    |
112 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:148:6
    |
148 | ) -> Result<Option<RelationCancelJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:383:6
    |
383 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:231:6
    |
231 | ) -> Result<ItemRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/relations_close.rs:222:1
    |
222 | / pub(super) fn plan_item_relations(
223 | |     ctx: &mut DependencyContext,
224 | |     planner: &mut CaptureBatchPlanner,
225 | |     request: &CaptureRequest,
...   |
230 | |     warnings: &mut Vec<CaptureWarning>,
231 | | ) -> Result<ItemRelationReports, CaptureError> {
    | |______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:269:6
    |
269 | ) -> Result<RelationCloseReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:465:6
    |
465 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this boolean expression can be simplified
   --> src/native/capture/relations_close.rs:489:14
    |
489 |         if !(cancel && complete || cancel && merge || complete && merge) {
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
    = note: `-D clippy::nonminimal-bool` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::nonminimal_bool)]`
help: try
    |
489 -         if !(cancel && complete || cancel && merge || complete && merge) {
489 +         if !(!(!cancel || !complete && !merge) || complete && merge) {
    |
489 -         if !(cancel && complete || cancel && merge || complete && merge) {
489 +         if !((merge || complete) && cancel || complete && merge) {
    |

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_complete.rs:38:6
   |
38 | ) -> Result<RelationCompleteReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:144:6
    |
144 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:180:6
    |
180 | ) -> Result<Option<PlannedSourceComplete>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_mentions.rs:53:6
   |
53 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:460:6
    |
460 | ) -> Result<Option<(usize, String)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:507:6
    |
507 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:547:6
    |
547 | ) -> Result<Option<MirrorSkipReason>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:579:6
    |
579 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/relations_mentions.rs:570:1
    |
570 | / fn source_block_id(
571 | |     ctx: &mut DependencyContext,
572 | |     planner: &mut CaptureBatchPlanner,
573 | |     bob_dir: &Path,
...   |
578 | |     minted_sources: &mut BTreeMap<(PathBuf, usize), String>,
579 | | ) -> Result<Option<String>, CaptureError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:693:6
    |
693 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_merge.rs:43:6
   |
43 | ) -> Result<RelationMergeReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:222:6
    |
222 | ) -> Result<TaskLocator, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:262:6
    |
262 | ) -> Result<VaultSnapshot, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_merge.rs:437:6
    |
437 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/capture/relations_mirror.rs:54:38
   |
54 |   pub(super) fn load_close_policy() -> (
   |  ______________________________________^
55 | |     Vec<config::relations::CancelLabel>,
56 | |     Vec<config::relations::CompleteLabel>,
57 | |     Vec<config::relations::CancelLabel>,
58 | |     Vec<config::relations::CancelLabel>,
59 | |     Option<String>,
60 | | ) {
   | |_^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:159:6
    |
159 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:274:6
    |
274 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:411:6
    |
411 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:440:6
    |
440 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:46:6
   |
46 | ) -> Result<capture_language::ParsedCaptureDraft, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
 --> src/native/capture/sub_bullet.rs:8:6
  |
8 | ) -> Result<CaptureWritePlan, CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/sub_bullet.rs:50:6
   |
50 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
  --> src/native/capture/sub_bullet.rs:41:1
   |
41 | / pub(super) fn plan_sub_bullet_capture(
42 | |     planner: &mut CaptureBatchPlanner,
43 | |     bob_dir: &Path,
44 | |     target: &Path,
...  |
49 | |     warnings: &mut Vec<CaptureWarning>,
50 | | ) -> Result<CaptureWritePlan, CaptureError> {
   | |___________________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:231:6
    |
231 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (9/7)
   --> src/native/capture/sub_bullet.rs:221:1
    |
221 | / fn plan_prj_section_capture(
222 | |     planner: &mut CaptureBatchPlanner,
223 | |     bob_dir: &Path,
224 | |     target: &Path,
...   |
230 | |     warnings: &mut Vec<CaptureWarning>,
231 | | ) -> Result<CaptureWritePlan, CaptureError> {
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:507:6
    |
507 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_complete.rs:49:6
   |
49 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:172:6
    |
172 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:921:6
    |
921 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1188:6
     |
1188 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:147:10
    |
147 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture/task_theme.rs:138:5
    |
138 | /     pub(super) fn apply_new_task(
139 | |         &mut self,
140 | |         planner: &mut CaptureBatchPlanner,
141 | |         target: &Path,
...   |
146 | |         warnings: &mut Vec<CaptureWarning>,
147 | |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    | |_____________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:187:10
    |
187 |     ) -> Result<AppliedTaskTheme, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:293:10
    |
293 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:307:10
    |
307 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (9/7)
   --> src/native/capture/task_theme.rs:297:5
    |
297 | /     pub(super) fn apply_existing_task(
298 | |         &mut self,
299 | |         planner: &mut CaptureBatchPlanner,
300 | |         target: &Path,
...   |
306 | |         warnings: &mut Vec<CaptureWarning>,
307 | |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    | |_____________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:338:10
    |
338 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:478:10
    |
478 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:601:10
    |
601 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:644:10
    |
644 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:777:10
    |
777 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:824:10
    |
824 |     ) -> Result<Option<usize>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:881:10
    |
881 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1127:10
     |
1127 |     ) -> Result<Option<AppliedMerge>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1191:10
     |
1191 |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
    --> src/native/capture/task_theme.rs:1182:5
     |
1182 | /     pub(super) fn relocate_for_retype(
1183 | |         &mut self,
1184 | |         planner: &mut CaptureBatchPlanner,
1185 | |         block_id: &str,
...    |
1190 | |         warnings: &mut Vec<CaptureWarning>,
1191 | |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     | |________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_toggle.rs:19:6
   |
19 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_toggle.rs:447:6
    |
447 | ) -> Result<ToggleRelationPlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/transfer.rs:67:6
   |
67 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:549:6
    |
549 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:575:6
    |
575 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/transfer.rs:641:6
    |
641 |   ) -> Result<
    |  ______^
642 | |     (
643 | |         RelationMergeOutput,
644 | |         Vec<crate::native::task_move::transplant::RepairedFile>,
645 | |     ),
646 | |     CaptureError,
647 | | > {
    | |_^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:332:44
    |
332 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
    |                                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_active_tasks.rs:331:12
    |
331 |     tasks: &mut Vec<ActiveTask>,
    |            ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
    = note: `-D clippy::ptr-arg` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::ptr_arg)]`
help: change this to
    |
331 -     tasks: &mut Vec<ActiveTask>,
331 +     tasks: &mut [ActiveTask],
    |

error: this function has too many arguments (9/7)
    --> src/native/capture_complete/candidates.rs:1081:1
     |
1081 | / fn relationship_disabled_reason(
1082 | |     bob_dir: &Path,
1083 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
1084 | |     graph: &HashMap<
...    |
1093 | |     blocked_tasks: &[ResolvedRelationshipEntry],
1094 | | ) -> Option<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1713:6
     |
1713 |   ) -> (
     |  ______^
1714 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1715 | |     Vec<String>,
1716 | |     Vec<(String, usize)>,
1717 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: this function has too many arguments (8/7)
   --> src/native/capture_complete/theme_menu.rs:186:1
    |
186 | / pub(super) fn compose_task_aware(
187 | |     scan: &PomodoroScan,
188 | |     query: &str,
189 | |     catalog: Option<&Catalog>,
...   |
194 | |     next_up_line: Option<usize>,
195 | | ) -> Vec<PomodoroNameCandidate> {
    | |_______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this boolean expression can be simplified
   --> src/native/capture_complete/theme_menu.rs:261:16
    |
261 |               || !row
    |  ________________^
262 | |                 .name
263 | |                 .as_deref()
264 | |                 .is_some_and(|name| normalize_component(name) == key)
    | |_____________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
261 ~             || row
262 +                 .name
263 +                 .as_deref().is_none_or(|name| normalize_component(name) != key)
    |

error: the loop variable `idx` is used to index `lines`
   --> src/native/capture_drawers.rs:666:16
    |
666 |     for idx in start_idx..end_idx.min(lines.len()) {
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
666 -     for idx in start_idx..end_idx.min(lines.len()) {
666 +     for (idx, <item>) in lines.iter().enumerate().take(end_idx.min(lines.len())).skip(start_idx) {
    |

error: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_drawers.rs:899:35
    |
899 | pub(crate) fn rank_drawer_catalog<'a>(
    |                                   ^^
900 |     records: &'a BTreeMap<String, DrawerCatalogRecord>,
    |               ^^
901 | ) -> Vec<&'a DrawerCatalogRecord> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `-D clippy::needless-lifetimes` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::needless_lifetimes)]`
help: elide the lifetimes
    |
899 ~ pub(crate) fn rank_drawer_catalog(
900 ~     records: &BTreeMap<String, DrawerCatalogRecord>,
901 ~ ) -> Vec<&DrawerCatalogRecord> {
    |

error: called `filter(..).next_back()` on an `DoubleEndedIterator`. This is more succinctly expressed by calling `.rfind(..)` instead
    --> src/native/capture_drawers.rs:1548:5
     |
1548 | /     direct_child_list_indexes(&lines, drawer.line_index(), drawer.block_end)
1549 | |         .into_iter()
1550 | |         .filter(|&index| line_start(&lines, index) < insertion.offset)
1551 | |         .filter(|&index| {
1552 | |             parse_managed_task_log_marker(lines[index].text).is_none()
1553 | |         })
1554 | |         .next_back()
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_next
     = note: `-D clippy::filter-next` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::filter_next)]`

error: redundant guard
   --> src/native/capture_language/close_log.rs:213:23
    |
213 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
    = note: `-D clippy::redundant-guards` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::redundant_guards)]`
help: try
    |
213 -         Some(list) if list.is_empty() => {
213 +         Some([]) => {
    |

error: this function has too many arguments (9/7)
   --> src/native/capture_language/close_log.rs:511:1
    |
511 | / fn check_index_loggable(
512 | |     index: u32,
513 | |     index_range: (usize, usize),
514 | |     close_token: &str,
...   |
520 | |     complete_all: bool,
521 | | ) -> Result<(), CloseLogError> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:680:1
    |
680 | / pub(crate) fn lex_close_inline_entry_with_all(
681 | |     entry_tokens: &[Token<'_>],
682 | |     close_token: &str,
683 | |     in_progress: Option<&[u32]>,
...   |
688 | |     complete_all: bool,
689 | | ) -> Result<CloseInlineLex, CloseLogError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/capture_language/close_log.rs:918:1
    |
918 | / pub(crate) fn lex_close_log_bullets_with_all(
919 | |     child_lines: &[ItemLine<'_>],
920 | |     close_token: &str,
921 | |     in_progress: Option<&[u32]>,
...   |
926 | |     complete_all: bool,
927 | | ) -> Result<CloseLogLexed, CloseLogError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: casting to the same type is unnecessary (`usize` -> `usize`)
    --> src/native/capture_language/completion.rs:1205:19
     |
1205 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast
     = note: `-D clippy::unnecessary-cast` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::unnecessary_cast)]`

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_language/draft.rs:1791:6
     |
1791 |   ) -> Result<
     |  ______^
1792 | |     Vec<(
1793 | |         ParsedCaptureText,
1794 | |         Option<RefParentSource>,
...    |
1797 | |     TemplateCodedError,
1798 | | > {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:382:12
    |
382 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
382 -     spans: &mut Vec<Span>,
382 +     spans: &mut [Span],
    |

error: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_language/editor_classify.rs:439:12
    |
439 |     spans: &mut Vec<Span>,
    |            ^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
439 -     spans: &mut Vec<Span>,
439 +     spans: &mut [Span],
    |

error: large size difference between variants
   --> src/native/capture_language/editor_model.rs:733:1
    |
733 | / pub(super) enum TokenParse {
734 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
735 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
736 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `-D clippy::large-enum-variant` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::large_enum_variant)]`
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
734 -     Marker(MarkerParse),
734 +     Marker(Box<MarkerParse>),
    |

error: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:1780:1
     |
1780 | / fn empty_editor_item(
1781 | |     item: &CaptureItem<'_>,
1782 | |     mode: EditorMode,
1783 | |     route: Option<String>,
...    |
1788 | |     diagnostics: Vec<Diagnostic>,
1789 | | ) -> EditorItemParse {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:2626:1
     |
2626 | / fn attach_drawer_bullet_metadata(
2627 | |     item: &CaptureItem<'_>,
2628 | |     mode: &mut EditorMode,
2629 | |     parent_body: &str,
...    |
2634 | |     sub_bullets: &mut [AuthoredSubBullet],
2635 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:3218:35
     |
3218 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `-D clippy::trim-split-whitespace` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::trim_split_whitespace)]`

error: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:3866:5
     |
3866 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:3865:5
     |
3865 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `-D clippy::field-reassign-with-default` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::field_reassign_with_default)]`

error: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:296:1
    |
296 | / pub(super) fn parse_editor_named_start_item<'a>(
297 | |     item: &CaptureItem<'a>,
298 | |     parent_trimmed: &str,
299 | |     suffix: String,
...   |
305 | |     spelling: NameSpelling,
306 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_pomodoro.rs:3245:1
     |
3245 | / fn editor_past_outcome<'a>(
3246 | |     item: &CaptureItem<'a>,
3247 | |     parent_trimmed: &str,
3248 | |     mode: EditorMode,
...    |
3253 | |     diagnostics: Vec<Diagnostic>,
3254 | | ) -> EditorItemOutcome<'a> {
     | |__________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:105:6
    |
105 |   ) -> Option<
    |  ______^
106 | |     Result<
107 | |         (
108 | |             LineOutcome<'a>,
...   |
113 | |     >,
114 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/item.rs:198:6
    |
198 |   ) -> Option<
    |  ______^
199 | |     Result<
200 | |         (
201 | |             LineOutcome<'a>,
...   |
206 | |     >,
207 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:1395:5
     |
1395 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1394:5
     |
1394 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

error: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/item.rs:1282:35
     |
1282 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

error: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:2094:1
     |
2094 | / fn parse_capture_item_masked<'a>(
2095 | |     item: &CaptureItem<'a>,
2096 | |     forced_route: Option<&str>,
2097 | |     forced_section: Option<&str>,
...    |
2102 | |     target_run: Option<&TargetRunContext>,
2103 | | ) -> Result<ParsedCaptureItemOutcome<'a>, String> {
     | |_________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:2416:5
     |
2416 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:2415:5
     |
2415 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

error: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:4239:1
     |
4239 | / pub(super) fn named_shape_error_with_drop(
4240 | |     token: &str,
4241 | |     suffix: &str,
4242 | |     name: &str,
...    |
4247 | |     is_literal: bool,
4248 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: called `expect` on `separator` after checking its variant with `is_some`
   --> src/native/capture_language/relations.rs:689:13
    |
687 |         block_end: if separator.is_some() {
    |                    ---------------------- help: try: `if let Some(<item>) = separator`
688 |             // Block ID ends where `|` starts.
689 |             separator.expect("separator").0
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap
    = note: `-D clippy::unnecessary-unwrap` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::unnecessary_unwrap)]`

error: this boolean expression can be simplified
   --> src/native/capture_language/rewrite.rs:868:8
    |
868 |       if !raw_text[..run_start]
    |  ________^
869 | |         .chars()
870 | |         .next_back()
871 | |         .is_some_and(|before| !before.is_whitespace())
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
868 ~     if raw_text[..run_start]
869 +         .chars()
870 +         .next_back().is_none_or(|before| before.is_whitespace())
    |

error: this function has too many arguments (9/7)
   --> src/native/capture_language/rewrite.rs:937:1
    |
937 | / fn candidate_selects_plain_marker(
938 | |     candidate: &str,
939 | |     start: usize,
940 | |     end: usize,
...   |
946 | |     id_part: &str,
947 | | ) -> bool {
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this `if` has identical blocks
   --> src/native/capture_language/target_runs.rs:457:51
    |
457 |           } else if is_escaped_priority_token(text) {
    |  ___________________________________________________^
458 | |             break;
459 | |         } else {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/target_runs.rs:459:16
    |
459 |           } else {
    |  ________________^
460 | |             break;
461 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else
    = note: `-D clippy::if-same-then-else` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::if_same_then_else)]`

error: redundant guard
    --> src/native/capture_language/tokens.rs:1406:43
     |
1406 |                 Some((after_x, x_len)) if after_x.is_empty() => {
     |                                           ^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
     |
1406 -                 Some((after_x, x_len)) if after_x.is_empty() => {
1406 +                 Some(("", x_len)) => {
     |

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_language/transfer.rs:489:6
    |
106 | /     Valid {
107 | |         sources: Vec<TransferSource>,
108 | |         arrow: TransferArrow,
109 | |         destination: TransferDestination,
110 | |     },
    | |_____- the largest variant contains at least 184 bytes
...
489 |   ) -> Result<TransferSource, TransferScan> {
    |        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_language::transfer::TransferScan`, for example by boxing large elements or replacing it with `Box<native::capture_language::transfer::TransferScan>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: stripping a prefix manually
   --> src/native/capture_language/transfer.rs:496:20
    |
496 |         let rest = &text[1..];
    |                    ^^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_language/transfer.rs:495:5
    |
495 |     if text.starts_with('@') {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
    = note: `-D clippy::manual-strip` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::manual_strip)]`
help: try using the `strip_prefix` method
    |
495 ~     if let Some(rest) = text.strip_prefix('@') {
496 ~         if let Some(plus) = rest.find('+') {
    |

error: this `if` has identical blocks
   --> src/native/capture_language/type_marker.rs:454:45
    |
454 |           } else if lex.decoded.contains('+') {
    |  _____________________________________________^
455 | |             (
456 | |                 TypeMarkerOccurrence::Invalid {
457 | |                     span: start..raw_end,
...   |
462 | |         } else if marker_end != raw_end {
    | |_________^
    |
note: same as this
   --> src/native/capture_language/type_marker.rs:462:41
    |
462 |           } else if marker_end != raw_end {
    |  _________________________________________^
463 | |             (
464 | |                 TypeMarkerOccurrence::Invalid {
465 | |                     span: start..raw_end,
...   |
470 | |         } else {
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: this function has too many arguments (8/7)
    --> src/native/capture_parse.rs:2344:1
     |
2344 | / fn refusal_diagnostic(
2345 | |     spans: &[Span],
2346 | |     mode: EditorMode,
2347 | |     pomodoro_start: &Option<PomodoroStartSpec>,
...    |
2352 | |     source: &str,
2353 | | ) -> Option<Diagnostic> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_pomodoro_close/ledger.rs:808:24
    |
808 |       let Some(anchor) = scan
    |  ________________________^
809 | |         .entries
810 | |         .iter()
811 | |         .filter(|entry| {
...   |
814 | |         })
815 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `-D clippy::double-ended-iterator-last` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::double_ended_iterator_last)]`
help: try
    |
815 -         .last()
815 +         .next_back()
    |

error: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:155:1
    |
155 | / pub(crate) enum PomodoroCloseOutcome {
156 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 688 bytes
157 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
158 | | }
    | |_^ the entire enum is at least 688 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
156 -     Close(PomodoroClosePlan),
156 +     Close(Box<PomodoroClosePlan>),
    |

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:319:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
319 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:366:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
366 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:554:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
554 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:571:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
571 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:591:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
591 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:614:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
614 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:677:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
677 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:750:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
750 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:904:10
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
904 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:982:6
    |
150 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
982 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1007:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1007 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1036:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1036 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1027:1
     |
1027 | / pub(crate) fn plan_pomodoro_close_for_entry<V: CloseVault>(
1028 | |     day_path: &Path,
1029 | |     day_contents: &str,
1030 | |     entry: &RunningPomodoro,
...    |
1035 | |     policy: LedgerClosePolicy,
1036 | | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     | |______________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1324:1
     |
1324 | / fn resolve_close_clock_fact<V: CloseVault, S: HomeSource>(
1325 | |     vault: &V,
1326 | |     resolver: &mut HomeResolver<S>,
1327 | |     events: &[EventNoteRow],
...    |
1333 | |     all_settings: &NoteTaskSettings,
1334 | | ) -> CloseClockFact {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1737:6
     |
 150 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1737 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/capture_pomodoro_start.rs:409:1
    |
409 | / fn resolve_clock_fact<V: CloseVault + ?Sized, S: HomeSource>(
410 | |     vault: Option<&V>,
411 | |     resolver: Option<&mut HomeResolver<S>>,
412 | |     events: &[EventNoteRow],
...   |
417 | |     all_settings: &note_tasks::NoteTaskSettings,
418 | | ) -> CountedLinkFact {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (13/7)
   --> src/native/capture_related/corpus.rs:163:1
    |
163 | / fn collect_from_note(
164 | |     _bob_dir: &Path,
165 | |     relative: &str,
166 | |     absolute: &Path,
...   |
176 | |     _warnings: &mut Vec<String>,
177 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/capture_related/corpus.rs:256:1
    |
256 | / fn collect_from_archives(
257 | |     bob_dir: &Path,
258 | |     settings: &note_tasks::NoteTaskSettings,
259 | |     today: NaiveDate,
...   |
264 | |     warnings: &mut Vec<String>,
265 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:449:1
    |
449 | / fn draft_match(
450 | |     ranked: bands::RankedMatch<'_>,
451 | |     item: &EditorItemParse,
452 | |     draft: &str,
...   |
457 | |     index: &NoteIndex,
458 | | ) -> RelatedMatch {
    | |_________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/capture_related/draft.rs:580:1
    |
580 | / fn verify_link_action(
581 | |     action: &str,
582 | |     item: &EditorItemParse,
583 | |     draft: &str,
...   |
588 | |     options: &EditorParseOptions<'_>,
589 | | ) -> bool {
    | |_________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this `if` has identical blocks
   --> src/native/capture_related/tokenize.rs:260:54
    |
260 |           if prev.is_lowercase() && cur.is_uppercase() {
    |  ______________________________________________________^
261 | |             starts.push(chars[i].0);
262 | |         } else if prev.is_uppercase()
    | |_________^
    |
note: same as this
   --> src/native/capture_related/tokenize.rs:265:9
    |
265 | /         {
266 | |             starts.push(chars[i].0);
267 | |         }
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: stripping a prefix manually
   --> src/native/capture_related/tokenize.rs:382:21
    |
382 |         let close = rest[2..].find("]]")?;
    |                     ^^^^^^^^^
    |
note: the prefix was tested here
   --> src/native/capture_related/tokenize.rs:381:5
    |
381 |     if rest.starts_with("[[") {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_strip
help: try using the `strip_prefix` method
    |
381 ~     if let Some(<stripped>) = rest.strip_prefix("[[") {
382 ~         let close = <stripped>.find("]]")?;
    |

error: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_task_toggle/ledger.rs:322:49
    |
322 | pub(crate) fn default_pomodoro_link_destination<'a>(
    |                                                 ^^
323 |     scan: &'a capture_pomodoros::PomodoroScan,
    |            ^^
324 |     queue_owner_line: Option<usize>,
325 | ) -> Option<&'a capture_pomodoros::PomodoroEntry> {
    |              ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
    |
322 ~ pub(crate) fn default_pomodoro_link_destination(
323 ~     scan: &capture_pomodoros::PomodoroScan,
324 |     queue_owner_line: Option<usize>,
325 ~ ) -> Option<&capture_pomodoros::PomodoroEntry> {
    |

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_task_toggle/relocation.rs:523:18
    |
523 |       let anchor = scan
    |  __________________^
524 | |         .entries
525 | |         .iter()
526 | |         .filter(|entry| entry.state == PomodoroState::Open)
527 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
527 -         .last()
527 +         .next_back()
    |

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
  --> src/native/capture_task_wikilinks.rs:79:5
   |
79 | /     wikilink_task_tokens(raw)
80 | |         .into_iter()
81 | |         .filter_map(|token| field_at_token(raw, token, cursor))
82 | |         .last()
   | |_______________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
   |
82 -         .last()
82 +         .next_back()
   |

error: match expression looks like `matches!` macro
   --> src/native/gcal/bullet_block.rs:145:5
    |
145 | /     match structural_depth(spans, row_index, end) {
146 | |         Some(depth) if depth >= 2 => false,
147 | |         _ => true,
148 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
    = note: `-D clippy::match-like-matches-macro` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::match_like_matches_macro)]`
help: use `matches!` directly
    |
145 -     match structural_depth(spans, row_index, end) {
146 -         Some(depth) if depth >= 2 => false,
147 -         _ => true,
148 -     }
145 +     !matches!(structural_depth(spans, row_index, end), Some(depth) if depth >= 2)
    |

error: the loop variable `index` is used to index `lines`
   --> src/native/gcal/bullet_block.rs:159:18
    |
159 |     for index in start..end {
    |                  ^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
159 -     for index in start..end {
159 +     for (index, <item>) in lines.iter().enumerate().take(end).skip(start) {
    |

error: methods called `from_*` usually take no `self`
  --> src/native/gcal/classify.rs:50:32
   |
50 |     pub(crate) fn from_rfc3339(&self) -> String {
   |                                ^^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention
   = note: `-D clippy::wrong-self-convention` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::wrong_self_convention)]`

error: this `if` has identical blocks
   --> src/native/gcal/description.rs:477:45
    |
477 |       let first_ok = if first.is_alphabetic() {
    |  _____________________________________________^
478 | |         true
479 | |     } else if !first.is_ascii()
    | |_____^
    |
note: same as this
   --> src/native/gcal/description.rs:481:5
    |
481 | /     {
482 | |         true
483 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: this if-then-else expression returns a bool literal
   --> src/native/gcal/description.rs:479:12
    |
479 |       } else if !first.is_ascii()
    |  ____________^
480 | |         && !matches!(first, '\u{2010}'..='\u{2015}' | '\u{2212}')
481 | |     {
482 | |         true
483 | |     } else {
484 | |         false
485 | |     };
    | |_____^ help: you can reduce it to: `{ !first.is_ascii() && !matches!(first, '\u{2010}'..='\u{2015}' | '\u{2212}') }`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_bool
    = note: `-D clippy::needless-bool` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::needless_bool)]`

error: this `if` has identical blocks
   --> src/native/gcal/diagnostics.rs:98:55
    |
 98 |       let inherited_advice: Option<String> = if on_wins {
    |  _______________________________________________________^
 99 | |         None
100 | |     } else if !input.root_only_off_clock {
    | |_____^
    |
note: same as this
   --> src/native/gcal/diagnostics.rs:100:42
    |
100 |       } else if !input.root_only_off_clock {
    |  __________________________________________^
101 | |         None
102 | |     } else {
    | |_____^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/gcal/journal.rs:130:6
    |
130 |   ) -> std::io::Result<(
    |  ______^
131 | |     BTreeMap<(String, String), OccurrenceState>,
132 | |     Vec<String>,
133 | |     Option<(DateTime<FixedOffset>, String)>,
134 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: large size difference between variants
   --> src/native/gcal/journal.rs:178:1
    |
178 | / enum Update {
179 | |     Row(RowRecord),
    | |     -------------- the largest variant contains at least 264 bytes
180 | |     Link,
181 | |     Gone,
182 | |     Flag(String),
    | |     ------------ the second-largest variant contains at least 24 bytes
183 | | }
    | |_^ the entire enum is at least 264 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
179 -     Row(RowRecord),
179 +     Row(Box<RowRecord>),
    |

error: enclosing `Some` and `?` operator are unneeded
   --> src/native/gcal/lifecycle.rs:241:5
    |
241 |     Some(text.get(..open)?)
    |     ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_question_mark
    = note: `-D clippy::needless-question-mark` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::needless_question_mark)]`
help: remove the enclosing `Some` and `?` operator
    |
241 -     Some(text.get(..open)?)
241 +     text.get(..open)
    |

error: consider using `sort_by_key`
   --> src/native/gcal/login.rs:638:5
    |
638 |     paths.sort_by(|a, b| b.0.cmp(&a.0));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
    = note: `-D clippy::unnecessary-sort-by` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::unnecessary_sort_by)]`
help: try
    |
638 -     paths.sort_by(|a, b| b.0.cmp(&a.0));
638 +     paths.sort_by_key(|b| std::cmp::Reverse(b.0));
    |

error: replacing a value of type `T` with `T::default()` is better expressed using `std::mem::take`
  --> src/native/gcal/render.rs:83:22
   |
83 |     let mut suffix = std::mem::replace(&mut spans.suffix, String::new());
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `std::mem::take(&mut spans.suffix)`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#mem_replace_with_default
   = note: `-D clippy::mem-replace-with-default` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::mem_replace_with_default)]`

error: this boolean expression can be simplified
   --> src/native/gcal/render.rs:190:5
    |
190 | /     !result
191 | |         .suggestion
192 | |         .is_some_and(|suggestion| suggestion.theme.name == "MEET")
    | |__________________________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
190 ~     result
191 +         .suggestion.is_none_or(|suggestion| suggestion.theme.name != "MEET")
    |

error: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
    --> src/native/gcal/sync.rs:1248:47
     |
1248 | fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
     |                                               ^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
     |
1248 - fn display_rel(vault: &std::path::Path, path: &PathBuf) -> String {
1248 + fn display_rel(vault: &std::path::Path, path: &Path) -> String {
     |

error: the following explicit lifetimes could be elided: 'a
   --> src/native/gkeep/imports.rs:422:26
    |
422 | pub(super) fn unfinished<'a>(
    |                          ^^
423 |     files: &'a [(PathBuf, TransactionFile)],
    |             ^^
424 | ) -> Vec<&'a (PathBuf, TransactionFile)> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
help: elide the lifetimes
    |
422 ~ pub(super) fn unfinished(
423 ~     files: &[(PathBuf, TransactionFile)],
424 ~ ) -> Vec<&(PathBuf, TransactionFile)> {
    |

error: consider using `sort_by_key`
    --> src/native/gkeep/migrate_tasks.rs:1952:5
     |
1952 |     ordered.sort_by(|left, right| right.start.cmp(&left.start));
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
     |
1952 -     ordered.sort_by(|left, right| right.start.cmp(&left.start));
1952 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.start));
     |

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1982:1
     |
1982 | / pub(super) fn stamp_overwrite_source(
1983 | |     config: &Config,
1984 | |     plan: &OverwritePreflight,
1985 | |     options: &CreateOptions,
...    |
1990 | |     info: &PdfInfo,
1991 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2024:1
     |
2024 | / pub(super) fn stage_overwrite_audio(
2025 | |     options: &CreateOptions,
2026 | |     plan: &OverwritePreflight,
2027 | |     request: &OverwriteRequest,
...    |
2032 | |     title: &str,
2033 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2706:1
     |
2706 | / fn plan_target_for(
2707 | |     config: &Config,
2708 | |     stem: &str,
2709 | |     ref_type: &str,
...    |
2714 | |     source_display: &str,
2715 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3726:1
     |
3726 | / fn stage_overwrite_source_store(
3727 | |     _config: &Config,
3728 | |     plan: &OverwritePreflight,
3729 | |     scratch: &Path,
...    |
3736 | |     catalog: &super::code_catalog::CatalogOutcome,
3737 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4420:1
     |
4420 | / fn overwrite_pdf_url(
4421 | |     config: &Config,
4422 | |     url: super::clip_url::WebUrl,
4423 | |     downloaded: PathBuf,
...    |
4428 | |     selection: &OverwriteSelection,
4429 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4502:1
     |
4502 | / fn create_pdf_url_route(
4503 | |     config: &Config,
4504 | |     url: super::clip_url::WebUrl,
4505 | |     downloaded: PathBuf,
...    |
4510 | |     listen: Option<&super::listen::ListenCommand>,
4511 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5239:1
     |
5239 | / fn print_pdf_dry_run(
5240 | |     config: &Config,
5241 | |     styler: &Styler,
5242 | |     source_display: &str,
...    |
5250 | |     legacy: &[sources_mod::RecordedSource],
5251 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
    --> src/native/highlights_ref/create.rs:5480:1
     |
5480 | / fn compose_markdown_marker(
5481 | |     status: &str,
5482 | |     parent: &str,
5483 | |     title: &str,
...    |
5489 | |     return_links: bool,
5490 | | ) -> Result<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/highlights_ref/attach.rs:332:1
    |
332 | / pub(super) fn run_attach(
333 | |     config: &Config,
334 | |     listen: &ListenCommand,
335 | |     attach: &AttachTarget,
...   |
340 | |     scratch: &mut super::ScratchDir,
341 | | ) -> Result<()> {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: clamp-like pattern without using clamp function
   --> src/native/highlights_ref/clip_adapter.rs:763:5
    |
763 | /     DIAGRAM_TIMEOUT_BASE_SECS
764 | |         .saturating_add(
765 | |             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
...   |
768 | |         .max(1)
    | |_______________^
    |
    = note: clamp will panic if max < min
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_clamp
    = note: `-D clippy::manual-clamp` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::manual_clamp)]`
help: replace with clamp
    |
763 ~     DIAGRAM_TIMEOUT_BASE_SECS
764 +         .saturating_add(
765 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
766 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

error: large size difference between variants
   --> src/native/highlights_ref/model.rs:736:1
    |
736 | / pub(super) enum PdfSyncOutcome {
737 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
738 | |     Held(ScanHold),
    | |     -------------- the second-largest variant contains at least 104 bytes
739 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
737 -     Written(SyncWriteReport),
737 +     Written(Box<SyncWriteReport>),
    |

error: large size difference between variants
   --> src/native/highlights_ref/model.rs:808:1
    |
808 | / pub(super) enum ScanWriteOutcome {
809 | |     Written(SyncWriteReport),
    | |     ------------------------ the largest variant contains at least 376 bytes
810 | |     Held(ScanHold),
811 | |     Failed(ScanFailure),
    | |     ------------------- the second-largest variant contains at least 144 bytes
812 | | }
    | |_^ the entire enum is at least 376 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
809 -     Written(SyncWriteReport),
809 +     Written(Box<SyncWriteReport>),
    |

error: this function has too many arguments (9/7)
  --> src/native/highlights_ref/note_snapshot/plan.rs:64:1
   |
64 | / pub(crate) fn plan_snapshot<L: SourceLoader>(
65 | |     store: &mut SourceStore<L>,
66 | |     note: ClassifiedNote,
67 | |     settings: &TasksSettings,
...  |
73 | |     parent_default_reason: Option<String>,
74 | | ) -> Result<SnapshotPlan, String> {
   | |_________________________________^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/note_snapshot/bob.rs:1121:1
     |
1121 | / fn push_schedule_group(
1122 | |     blocks: &mut Vec<Block>,
1123 | |     source: &SourceIdentity,
1124 | |     level: HeadingLevel,
...    |
1129 | |     used_ids: &mut BTreeSet<String>,
1130 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: methods called `as_*` usually take `self` by reference or `self` by mutable reference
  --> src/native/highlights_ref/note_snapshot/classify.rs:54:32
   |
54 |     pub(crate) const fn as_str(self) -> &'static str {
   |                                ^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention

error: large size difference between variants
   --> src/native/highlights_ref/note_snapshot/serialize.rs:121:1
    |
121 | / enum InlineFlowPart {
122 | |     Inlines(Vec<Inline>),
    | |     -------------------- the second-largest variant contains at least 24 bytes
123 | |     Block(Block),
    | |     ------------ the largest variant contains at least 336 bytes
124 | | }
    | |_^ the entire enum is at least 336 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
123 -     Block(Block),
123 +     Block(Box<Block>),
    |

error: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:416:17
    |
416 |         blocks: &mut Vec<Block>,
    |                 ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
help: change this to
    |
416 -         blocks: &mut Vec<Block>,
416 +         blocks: &mut [Block],
    |

error: creating a new box
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:607:21
    |
607 |                     *block = Box::new(expanded);
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace existing content with inner value instead: `**block = expanded`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box
    = note: `-D clippy::replace-box` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::replace_box)]`

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:872:10
    |
872 |       ) -> (
    |  __________^
873 | |         BTreeMap<(AnchorIdentity, String), SnapshotAnchor>,
874 | |         BTreeMap<AnchorIdentity, String>,
875 | |         Vec<SnapshotAnchor>,
876 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: this function has too many arguments (10/7)
    --> src/native/highlights_ref/note_snapshot/transclusion.rs:1195:1
     |
1195 | / fn compose_bob_masthead<L: SourceLoader>(
1196 | |     masthead: &mut SnapshotMasthead,
1197 | |     source: &SourceIdentity,
1198 | |     kind: &NoteKind,
...    |
1205 | |     settings: &TasksSettings,
1206 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: creating a new box
   --> src/native/highlights_ref/note_snapshot/visibility.rs:198:21
    |
198 | /                     *inner = Box::new(
199 | |                         nested.into_iter().next().expect("embedded block"),
200 | |                     );
    | |_____________________^ help: replace existing content with inner value instead: `**inner = nested.into_iter().next().expect("embedded block")`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box

error: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:133:1
    |
133 | / pub(super) fn plan_pdf_url(
134 | |     url: &WebUrl,
135 | |     downloaded: &Path,
136 | |     name_override: Option<&str>,
...   |
142 | |     progress: Option<&dyn Fn(&str)>,
143 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:220:1
    |
220 | / pub(super) fn plan_arxiv(
221 | |     paper: &ArxivPaper,
222 | |     name_override: Option<&str>,
223 | |     title_override: Option<&str>,
...   |
229 | |     progress: Option<&dyn Fn(&str)>,
230 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:757:1
    |
757 | / pub(super) fn preflight_for_url(
758 | |     config: &Config,
759 | |     rows: &[RefRow],
760 | |     recorded: &[RecordedSource],
...   |
765 | |     title_fallback: &str,
766 | | ) -> Result<Option<RereadPreflight>, CommandError> {
    | |__________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:804:1
    |
804 | / pub(super) fn preflight_for_url_outcome(
805 | |     config: &Config,
806 | |     rows: &[RefRow],
807 | |     recorded: &[RecordedSource],
...   |
812 | |     title_fallback: &str,
813 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this boolean expression can be simplified
   --> src/native/highlights_ref/recapture.rs:881:9
    |
881 | /         hit.dedupe_key == final_dedupe
882 | |             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 | |                 || !hit.is_ref_note)
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
881 -         hit.dedupe_key == final_dedupe
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
881 +         !(hit.dedupe_key != final_dedupe || hit.is_ref_note && hit.source_pdf.is_none())
    |
881 -         hit.dedupe_key == final_dedupe
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
881 +         (hit.source_pdf.is_some() || !hit.is_ref_note) && hit.dedupe_key == final_dedupe
    |

error: this boolean expression can be simplified
   --> src/native/highlights_ref/recapture.rs:882:16
    |
882 |               && ((hit.is_ref_note && hit.source_pdf.is_some())
    |  ________________^
883 | |                 || !hit.is_ref_note)
    | |____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
882 +             && !(hit.is_ref_note && hit.source_pdf.is_none())
    |
882 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
883 -                 || !hit.is_ref_note)
882 +             && !hit.is_ref_note || hit.source_pdf.is_some()
    |

error: this function has too many arguments (8/7)
   --> src/native/highlights_ref/recapture.rs:912:1
    |
912 | / pub(super) fn preflight_for_stem(
913 | |     config: &Config,
914 | |     rows: &[RefRow],
915 | |     stem: &str,
...   |
920 | |     identity: StemIdentity<'_>,
921 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (10/7)
   --> src/native/highlights_ref/recapture.rs:980:1
    |
980 | / fn url_selection_from_selection(
981 | |     config: &Config,
982 | |     family: SelectedFamily,
983 | |     name: Option<&str>,
...   |
990 | |     overwrite_enabled: bool,
991 | | ) -> Result<CaptureOutcome, CommandError> {
    | |_________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
    --> src/native/highlights_ref/recapture.rs:1006:1
     |
1006 | / fn url_reread_from_selection(
1007 | |     config: &Config,
1008 | |     family: SelectedFamily,
1009 | |     name: Option<&str>,
...    |
1015 | |     attach_available: bool,
1016 | | ) -> Result<Option<RereadPreflight>, CommandError> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (10/7)
    --> src/native/highlights_ref/recapture.rs:1042:1
     |
1042 | / fn finish_selection(
1043 | |     config: &Config,
1044 | |     family: SelectedFamily,
1045 | |     name: Option<&str>,
...    |
1052 | |     overwrite_enabled: bool,
1053 | | ) -> Result<CaptureOutcome, CommandError> {
     | |_________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this boolean expression can be simplified
    --> src/native/highlights_ref/recapture.rs:1366:9
     |
1366 | /         hit.dedupe_key == final_dedupe
1367 | |             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 | |                 || !hit.is_ref_note)
     | |____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
1366 -         hit.dedupe_key == final_dedupe
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1366 +         !(hit.dedupe_key != final_dedupe || hit.is_ref_note && hit.source_pdf.is_none())
     |
1366 -         hit.dedupe_key == final_dedupe
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1366 +         (hit.source_pdf.is_some() || !hit.is_ref_note) && hit.dedupe_key == final_dedupe
     |

error: this boolean expression can be simplified
    --> src/native/highlights_ref/recapture.rs:1367:16
     |
1367 |               && ((hit.is_ref_note && hit.source_pdf.is_some())
     |  ________________^
1368 | |                 || !hit.is_ref_note)
     | |____________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
     |
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1367 +             && !(hit.is_ref_note && hit.source_pdf.is_none())
     |
1367 -             && ((hit.is_ref_note && hit.source_pdf.is_some())
1368 -                 || !hit.is_ref_note)
1367 +             && !hit.is_ref_note || hit.source_pdf.is_some()
     |

error: this function has too many arguments (9/7)
   --> src/native/highlights_ref/overwrite/execute.rs:338:1
    |
338 | / fn overwrite_inside_accessor(
339 | |     config: &Config,
340 | |     locked: &OverwritePreflight,
341 | |     request: &OverwriteRequest,
...   |
347 | |     mut pdf_move: Option<&mut MoveContext<'_>>,
348 | | ) -> Result<OverwriteResult, CommandError> {
    | |__________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
    --> src/native/highlights_ref/overwrite/recovery.rs:1187:1
     |
1187 | / fn plan_endpoint_pair(
1188 | |     vault: &Path,
1189 | |     intent: &OverwriteIntent,
1190 | |     source: &Path,
...    |
1196 | |     plan: &mut ReversalPlan,
1197 | | ) -> std::result::Result<(), CommandError> {
     | |__________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/highlights_ref/overwrite/recovery.rs:1304:16
     |
1304 |     reversals: Vec<(PathBuf, PathBuf, Option<String>, Option<String>, bool)>,
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1178:1
     |
1178 | / pub(super) fn render_fresh_skeleton(
1179 | |     config: &Config,
1180 | |     note_rel: &str,
1181 | |     pdf: &Path,
...    |
1186 | |     audio_path: Option<&Path>,
1187 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1370:1
     |
1370 | / fn render_frozen_note(
1371 | |     old_contents: &str,
1372 | |     live_note: &str,
1373 | |     date: &str,
...    |
1378 | |     annotated: Option<FrozenAnnotated<'_>>,
1379 | | ) -> Result<String, String> {
     | |___________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/overwrite.rs:1472:1
     |
1472 | / fn frozen_body(
1473 | |     body: &str,
1474 | |     live_note: &str,
1475 | |     title: &str,
...    |
1480 | |     annotated_pdf: Option<&str>,
1481 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (14/7)
    --> src/native/highlights_ref/overwrite.rs:1565:1
     |
1565 | / fn plan_annotated_archive(
1566 | |     config: &Config,
1567 | |     live_note: &str,
1568 | |     ref_type: &str,
...    |
1579 | |     assets_relative: Option<&Path>,
1580 | | ) -> Result<AnnotatedArchivePlan, OverwriteRefusal> {
     | |___________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/highlights_ref/sidecar.rs:318:1
    |
318 | / pub(super) fn flush_sidecar_chunk(
319 | |     annotations: &mut Vec<SidecarAnnotation>,
320 | |     chunk: &mut Vec<String>,
321 | |     page_label: Option<&str>,
...   |
326 | |     page_ordinals: &mut BTreeMap<String, usize>,
327 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/sidecar_render.rs:308:29
    |
308 | ...                   &[member_text_key.clone()],
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&member_text_key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs
    = note: `-D clippy::cloned-ref-to-slice-refs` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::cloned_ref_to_slice_refs)]`

error: this function has too many arguments (9/7)
    --> src/native/highlights_ref/sidecar_render.rs:1267:1
     |
1267 | / fn append_resolved_image_notes(
1268 | |     config: &Config,
1269 | |     ref_note_path: &Path,
1270 | |     annotation_order: usize,
...    |
1276 | |     image_asset_writes_by_dest: &mut BTreeMap<PathBuf, ImageAssetWrite>,
1277 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/highlights_ref/sidecar_render.rs:2482:1
     |
2482 | / pub(super) fn render_annotation_block(
2483 | |     config: &Config,
2484 | |     ref_note_path: &Path,
2485 | |     annotation: &SidecarAnnotation,
...    |
2490 | |     strip_return_links: bool,
2491 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
    --> src/native/highlights_ref/source_store.rs:1129:1
     |
1129 | / pub(super) fn write_for_create(
1130 | |     config: &super::model::Config,
1131 | |     target_plan: &super::stamp::TargetPlan,
1132 | |     installed_pdf: &std::path::Path,
...    |
1138 | |     catalog: &CatalogOutcome,
1139 | | ) -> Option<StoreWriteOutcome> {
     | |______________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: all variants have the same postfix: `Host`
  --> src/native/highlights_ref/underline.rs:20:1
   |
20 | / pub(super) enum StandaloneUnderlineReason {
21 | |     NoHost,
22 | |     AmbiguousHost { hosts: usize },
23 | |     RepeatedInHost,
24 | | }
   | |_^
   |
   = help: remove the postfixes and use full paths to the variants instead of glob imports
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#enum_variant_names
   = note: `-D clippy::enum-variant-names` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::enum_variant_names)]`

error: consider using `sort_by_key`
   --> src/native/periods/list.rs:125:5
    |
125 |     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
125 -     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
125 +     rows.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

error: this `if` has identical blocks
   --> src/native/periods/note.rs:317:57
    |
317 |               if !name.is_empty() && !name.contains("  ") {
    |  _________________________________________________________^
318 | |                 current = Some(name);
319 | |             } else if !name.is_empty() {
    | |_____________^
    |
note: same as this
   --> src/native/periods/note.rs:319:40
    |
319 |               } else if !name.is_empty() {
    |  ________________________________________^
320 | |                 current = Some(name);
321 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/periods/report.rs:1092:6
     |
1092 | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: this function has too many arguments (9/7)
   --> src/native/plugins/sync.rs:140:1
    |
140 | / fn sync_one_plugin(
141 | |     options: &SyncOptions,
142 | |     id: &str,
143 | |     repo_plugin_dir: &Path,
...   |
149 | |     issues: &mut Vec<String>,
150 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (16/7)
   --> src/native/plugins/sync.rs:238:1
    |
238 | / fn apply_plugin(
239 | |     options: &SyncOptions,
240 | |     id: &str,
241 | |     captured: &CapturedPlugin,
...   |
254 | |     issues: &mut Vec<String>,
255 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: consider using `sort_by_key`
  --> src/native/pomodoro_homes/label.rs:21:5
   |
21 |     ranked.sort_by(|left, right| right.share.cmp(&left.share));
   |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
   |
21 -     ranked.sort_by(|left, right| right.share.cmp(&left.share));
21 +     ranked.sort_by_key(|right| std::cmp::Reverse(right.share));
   |

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/pomodoro_homes/resolve.rs:467:25
    |
467 | /                         chain[nearest_home..end]
468 | |                             .iter()
469 | |                             .filter(|(_, facts)| {
470 | |                                 facts.kind == NoteKind::Project
471 | |                             })
472 | |                             .last()
    | |___________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
472 -                             .last()
472 +                             .next_back()
    |

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/pomodoro_themes/cache.rs:217:6
    |
217 |   ) -> Option<(
    |  ______^
218 | |     BTreeMap<String, ThemeRecord>,
219 | |     BTreeMap<NaiveDate, BTreeSet<String>>,
220 | |     Vec<String>,
221 | | )> {
    | |__^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: this function has too many arguments (8/7)
   --> src/native/pomodoro_themes/hints.rs:250:1
    |
250 | / fn suggested_hue(
251 | |     moved: &ThemeRecord,
252 | |     current: Hue,
253 | |     window_days: &[(&NaiveDate, &BTreeSet<String>)],
...   |
258 | |     themes: Option<&crate::native::config::ThemesConfig>,
259 | | ) -> Option<Hue> {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:100:13
    |
100 | /             match rename_entry(day_contents, entry.line, &new_name) {
101 | |                 Some(updated) => Some((
102 | |                     updated,
103 | |                     TypeRelocation {
...   |
113 | |                 None => None,
114 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
    = note: `-D clippy::manual-map` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::manual_map)]`
help: try
    |
100 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
101 +                     updated,
102 +                     TypeRelocation {
103 +                         outcome: "rename_entry",
104 +                         from,
105 +                         to: new_name,
106 +                         source_before: line,
107 +                         dest_before: Some(line),
108 +                         dest_after: line,
109 +                         dest_created: false,
110 +                     },
111 +                 ))
    |

error: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:120:13
    |
120 | /             match rename_entry(day_contents, entry.line, &new_name) {
121 | |                 Some(updated) => Some((
122 | |                     updated,
123 | |                     TypeRelocation {
...   |
133 | |                 None => None,
134 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
120 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
121 +                     updated,
122 +                     TypeRelocation {
123 +                         outcome: "rename_placeholder",
124 +                         from,
125 +                         to: new_name,
126 +                         source_before: line,
127 +                         dest_before: Some(line),
128 +                         dest_after: line,
129 +                         dest_created: false,
130 +                     },
131 +                 ))
    |

error: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:140:13
    |
140 | /             match rename_entry(day_contents, entry.line, &new_name) {
141 | |                 Some(updated) => Some((
142 | |                     updated,
143 | |                     TypeRelocation {
...   |
153 | |                 None => None,
154 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
140 ~             rename_entry(day_contents, entry.line, &new_name).map(|updated| (
141 +                     updated,
142 +                     TypeRelocation {
143 +                         outcome: "append_component",
144 +                         from,
145 +                         to: new_name,
146 +                         source_before: line,
147 +                         dest_before: Some(line),
148 +                         dest_after: line,
149 +                         dest_created: false,
150 +                     },
151 +                 ))
    |

error: manual implementation of `Option::map`
   --> src/native/pomodoro_themes/relocation_apply.rs:205:13
    |
205 | /             match create_below_and_move(
206 | |                 day_contents,
207 | |                 source_entry.line,
208 | |                 link.line_index,
...   |
224 | |                 None => None,
225 | |             }
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#manual_map
help: try
    |
205 ~             create_below_and_move(
206 +                 day_contents,
207 +                 source_entry.line,
208 +                 link.line_index,
209 +                 link.subtree_end,
210 +                 &name,
211 +             ).map(|updated| (
212 +                     updated,
213 +                     TypeRelocation {
214 +                         outcome: "create_below",
215 +                         from: from_name,
216 +                         to: name,
217 +                         source_before: source_index,
218 +                         dest_before: None,
219 +                         dest_after,
220 +                         dest_created: true,
221 +                     },
222 +                 ))
    |

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/projects/sync.rs:914:28
    |
914 |       if let Some(depends) = sub_block
    |  ____________________________^
915 | |         .lines
916 | |         .iter()
917 | |         .filter(|line| is_direct_prj_dependency_line(sub_block, line))
918 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
918 -         .last()
918 +         .next_back()
    |

error: this function has too many arguments (8/7)
   --> src/native/ref_jobs/worker.rs:455:5
    |
455 | /     fn record_done(
456 | |         &self,
457 | |         job: &JobFile,
458 | |         outcome: DoneOutcome,
...   |
463 | |         fallback_target: Option<String>,
464 | |     ) {
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/ref_library/code.rs:236:1
    |
236 | / fn render_human(
237 | |     title: &str,
238 | |     path: &str,
239 | |     total_bytes: usize,
...   |
244 | |     hint_number: Option<u32>,
245 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: called `unwrap` on `page` after checking its variant with `is_some`
   --> src/native/ref_library/code.rs:587:47
    |
586 |     if blocks.is_empty() && page.is_some() {
    |                             -------------- the check is happening here
587 |         println!("no code blocks on page {}", page.unwrap());
    |                                               ^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

error: the `Err`-variant returned from this function is very large
   --> src/native/ref_library/today.rs:351:6
    |
351 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this function has too many arguments (8/7)
   --> src/native/ref_library/today.rs:827:1
    |
827 | / fn fail(
828 | |     format: Format,
829 | |     dry_run: bool,
830 | |     code: &str,
...   |
835 | |     listing: &TodayListing,
836 | | ) -> i32 {
    | |________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: `format!` in `format!` args
   --> src/native/ref_library/migrate_tasks/plan.rs:985:20
    |
985 |               return format!(
    |  ____________________^
986 | |                 "{}{}",
987 | |                 &line[..caret + 1],
988 | |                 format!("{new_id}{}", &line[trimmed_end..])
989 | |             );
    | |_____________^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

error: doc list item without indentation
   --> src/native/ref_library/mod.rs:933:5
    |
933 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `-D clippy::doc-lazy-continuation` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::doc_lazy_continuation)]`
help: indent this line
    |
933 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
    |     ++

error: the loop variable `index` is used to index `lines`
  --> src/native/ref_tasks/embed.rs:76:22
   |
76 |         for index in start..end.min(lines.len()) {
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
   |
76 -         for index in start..end.min(lines.len()) {
76 +         for (index, <item>) in lines.iter().enumerate().take(end.min(lines.len())).skip(start) {
   |

error: the loop variable `index` is used to index `lines`
   --> src/native/ref_tasks/embed.rs:118:18
    |
118 |     for index in start..end.min(lines.len()) {
    |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
118 -     for index in start..end.min(lines.len()) {
118 +     for (index, <item>) in lines.iter().enumerate().take(end.min(lines.len())).skip(start) {
    |

error: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop

error: doc list item without indentation
   --> src/native/relation_labels/scan.rs:288:5
    |
288 | /// Every I/O failure is ignored: the sweep never fails a scan.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
help: indent this line
    |
288 | ///   Every I/O failure is ignored: the sweep never fails a scan.
    |     ++

error: `format!` in `format!` args
   --> src/native/relation_labels/cli.rs:607:22
    |
607 |       let mut counts = format!(
    |  ______________________^
608 | |         "{} {} {} {} {} {}",
609 | |         report.counts.labels,
610 | |         label_word(report.counts.labels),
...   |
614 | |         format!("{} hidden", report.counts.hidden,),
615 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

error: consider using `sort_by_key`
   --> src/native/relation_labels/rename.rs:843:5
    |
843 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
843 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
843 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

error: this function has too many arguments (9/7)
   --> src/native/stats/typical.rs:191:1
    |
191 | / pub(crate) fn period_typical_detail(
192 | |     kind: &str,
193 | |     display: Option<&str>,
194 | |     window: &str,
...   |
200 | |     in_progress: bool,
201 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: match expression looks like `matches!` macro
  --> src/native/style.rs:20:5
   |
20 | /     match bob_env::var_os("CLICOLOR_FORCE") {
21 | |         Some(value) if !value.is_empty() && value != "0" => true,
22 | |         _ => false,
23 | |     }
   | |_____^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
help: use `matches!` directly
   |
20 -     match bob_env::var_os("CLICOLOR_FORCE") {
21 -         Some(value) if !value.is_empty() && value != "0" => true,
22 -         _ => false,
23 -     }
20 +     matches!(bob_env::var_os("CLICOLOR_FORCE"), Some(value) if !value.is_empty() && value != "0")
   |

error: consider using `sort_by_key`
   --> src/native/task_cancel/prune.rs:192:9
    |
192 |         edits.sort_by(|left, right| right.0.cmp(&left.0));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
192 -         edits.sort_by(|left, right| right.0.cmp(&left.0));
192 +         edits.sort_by_key(|right| std::cmp::Reverse(right.0));
    |

error: this lifetime isn't used in the function definition
   --> src/native/task_cancel/prune.rs:271:22
    |
271 | fn is_dedicated_line<'a>(
    |                      ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extra_unused_lifetimes
    = note: `-D clippy::extra-unused-lifetimes` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::extra_unused_lifetimes)]`

error: this boolean expression can be simplified
   --> src/native/task_complete/keep_moving.rs:604:9
    |
604 |         !task.scheduled.is_some_and(|date| date > today)
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `task.scheduled.is_none_or(|date| date <= today)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool

error: this function has too many arguments (9/7)
   --> src/native/task_complete/project_pull_in.rs:932:1
    |
932 | / fn emit_keep_moving_recover(
933 | |     plan: &mut SuccessorPlan,
934 | |     completed: &[CompletedTask],
935 | |     day_task_lines: &BTreeMap<String, usize>,
...   |
941 | |     reason: &'static str,
942 | | ) {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/task_complete/relation_successors/classify.rs:529:1
    |
529 | / fn resolve_edge<R: TargetNoteReader>(
530 | |     source_path: &Path,
531 | |     source: &TaskLine,
532 | |     entry: &RelationEntry,
...   |
537 | |     reader: &mut R,
538 | | ) -> Option<ResolvedEdge> {
    | |_________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
   --> src/native/task_complete/relation_successors/classify.rs:623:1
    |
623 | / fn classify_source<R: TargetNoteReader>(
624 | |     input: &RelationClassifyInput<'_>,
625 | |     source: &SourceHit,
626 | |     triggering: &[TriggeringEvent],
...   |
631 | |     baseline: Option<&DayView>,
632 | | ) -> SourceClass {
    | |________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (9/7)
   --> src/native/task_complete/successors.rs:877:1
    |
877 | / fn effective_relation_state_map(
878 | |     verdicts: &[DependentVerdict],
879 | |     files: &[FileScan],
880 | |     states: &BTreeMap<
...   |
889 | |     source_paths: &BTreeSet<&Path>,
890 | | ) -> BTreeMap<String, SourceRecovery> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1147:1
     |
1147 | / fn relation_offer_placement(
1148 | |     group: &RelationOfferGroup,
1149 | |     completed: &[CompletedTask],
1150 | |     baseline_day: &DayView,
...    |
1155 | |     implicit: Option<&ImplicitDest>,
1156 | | ) -> Option<RelationOfferPlacement> {
     | |___________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2558:1
     |
2558 | / fn attach_offer(
2559 | |     verdict: &mut DependentVerdict,
2560 | |     files: &[FileScan],
2561 | |     day: &DayView,
...    |
2566 | |     project: Option<PathBuf>,
2567 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:2659:1
     |
2659 | / fn apply_project_member_classes(
2660 | |     verdicts: &mut Vec<DependentVerdict>,
2661 | |     folds: &mut Vec<ProjectFold>,
2662 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
2671 | |     _note_settings: &NoteTaskSettings,
2672 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this function has too many arguments (13/7)
    --> src/native/task_complete/successors.rs:3254:1
     |
3254 | / fn apply_verdicts(
3255 | |     input: SuccessorInput,
3256 | |     files: Vec<FileScan>,
3257 | |     verdicts: Vec<DependentVerdict>,
...    |
3267 | |     relation_target_reads: usize,
3268 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/payload.rs:482:6
    |
482 | ) -> Result<(Vec<LineRange>, Vec<(String, String)>, usize), MergeError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_merge/retirement.rs:213:15
    |
213 |     repoints: &[((PathBuf, String), (PathBuf, String))],
    |               ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/command.rs:1064:6
     |
1064 | ) -> Result<(Option<(PathBuf, String)>, Vec<RelocatedInfo>), String> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/task_move/plan.rs:342:22
    |
342 |           let parent = tasks
    |  ______________________^
343 | |             .iter()
344 | |             .filter(|candidate| {
345 | |                 candidate.line_index < task.line_index
...   |
348 | |             })
349 | |             .last();
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
help: try
    |
349 -             .last();
349 +             .next_back();
    |

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_move/transplant.rs:121:6
    |
121 |   ) -> Result<
    |  ______^
122 | |     (Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>),
123 | |     RenameError,
124 | | > {
    | |_^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: called `unwrap` on `mention_id` after checking its variant with `is_some`
   --> src/native/task_split/plan.rs:298:33
    |
294 |             && mention_id.is_some()
    |                -------------------- the check is happening here
...
298 |                 format!("#^{}", mention_id.unwrap())
    |                                 ^^^^^^^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

error: called `unwrap` on `mention_id` after checking its variant with `is_some`
   --> src/native/task_split/plan.rs:303:21
    |
294 |             && mention_id.is_some()
    |                -------------------- the check is happening here
...
303 |                     mention_id.unwrap()
    |                     ^^^^^^^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

error: the loop variable `row` is only used to index `transformed_source`
   --> src/native/task_split/plan.rs:269:20
    |
269 |         for row in candidate.line + 1..=candidate.end {
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator
    |
269 -         for row in candidate.line + 1..=candidate.end {
269 +         for <item> in transformed_source.iter_mut().take(candidate.end + 1).skip(candidate.line + 1) {
    |

error: this `if` has identical blocks
   --> src/native/task_split/plan.rs:338:59
    |
338 |           let dest_after = if owner.kind == OwnerKind::Task {
    |  ___________________________________________________________^
339 | |             insert_tasks_section_string(&destination_before, &generated)?
340 | |         } else {
    | |_________^
    |
note: same as this
   --> src/native/task_split/plan.rs:340:16
    |
340 |           } else {
    |  ________________^
341 | |             insert_tasks_section_string(&destination_before, &generated)?
342 | |         };
    | |_________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: this `if` has identical blocks
   --> src/native/task_split/plan.rs:936:55
    |
936 |               if snapshot.notes.contains_key(&with_ext) {
    |  _______________________________________________________^
937 | |                 Ok(with_ext)
938 | |             } else {
    | |_____________^
    |
note: same as this
   --> src/native/task_split/plan.rs:938:20
    |
938 |               } else {
    |  ____________________^
939 | |                 Ok(with_ext)
940 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: the loop variable `index` is used to index `lines`
    --> src/native/task_split/plan.rs:1089:18
     |
1089 |     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
     |                  ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
     |
1089 -     for index in start + 1..=limit.min(lines.len().saturating_sub(1)) {
1089 +     for (index, <item>) in lines.iter().enumerate().take(limit.min(lines.len().saturating_sub(1)) + 1).skip(start + 1) {
     |

error: this function has too many arguments (8/7)
   --> src/native/task_status_groups/emit.rs:105:1
    |
105 | / pub(super) fn emit_grouped_body(
106 | |     node: &HeadingNode,
107 | |     contents: &str,
108 | |     classified: &ClassifiedChildren<'_>,
...   |
113 | |     heading_has_line_ending: bool,
114 | | ) -> String {
    | |___________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:583:5
    |
583 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:372:9
    |
372 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `-D clippy::redundant-locals` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::redundant_locals)]`

error: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1386:1
     |
1386 | / fn consume_blocked_links_after_compose(
1387 | |     compose: &mut ComposeResult,
1388 | |     files: &[FileScan],
1389 | |     daily_path: &Path,
...    |
1400 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1401 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: useless use of `vec!`
   --> src/native/periods/scaffold.rs:209:17
    |
209 |       let parts = vec![
    |  _________________^
210 | |         frontmatter_all_time(),
211 | |         "# All time".to_string(),
212 | |         "[[org|↑ org]]".to_string(),
...   |
216 | |         instructions::render(PeriodId::AllTime),
217 | |     ];
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_vec
    = note: `-D clippy::useless-vec` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::useless_vec)]`
help: you can use an array directly
    |
209 ~     let parts = [frontmatter_all_time(),
210 +         "# All time".to_string(),
211 ~         "[[org|↑ org]]".to_string(),
212 +         "```bob-stats-strip\n\n```".to_string(),
213 +         "## Years\n\n```bob-period-parts\n\n```".to_string(),
214 +         "## Notes".to_string(),
215 ~         instructions::render(PeriodId::AllTime)];
    |

error: could not compile `bob-obsidian` (lib) due to 473 previous errors
warning: build failed, waiting for other jobs to finish...
error: redundant redefinition of a binding `plans`
   --> src/native/articles/inbound.rs:485:9
    |
485 |         let mut plans = plans;
    |         ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `plans` is initially defined here
   --> src/native/articles/inbound.rs:479:13
    |
479 |         let mut plans =
    |             ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `-D clippy::redundant-locals` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::redundant_locals)]`

error: this function has too many arguments (8/7)
  --> src/native/attachments/tests.rs:38:1
   |
38 | / fn record(
39 | |     vault: &std::path::Path,
40 | |     host: &str,
41 | |     ts: &str,
...  |
46 | |     via: &str,
47 | | ) {
   | |_^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

error: this method chain can be written more clearly with `if .. else ..`
   --> src/native/attachments/tests.rs:205:19
    |
205 |         let via = with_via.then_some(",\"via\":\"cli\"").unwrap_or("");
    |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `if with_via { ",\"via\":\"cli\"" } else { "" }`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#obfuscated_if_else
    = note: `-D clippy::obfuscated-if-else` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::obfuscated_if_else)]`

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:364:10
    |
364 |     ) -> Result<PlannedDependencyUpdate, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:628:10
    |
628 |     ) -> Result<DependentRef, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/note_pull.rs:1628:39
     |
1628 |     fn plan(harness: &mut Harness) -> Result<PlannedCaptureItem, CaptureError> {
     |                                       ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:3162:10
     |
3162 |     ) -> Result<PlannedCaptureItem, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:14:6
   |
14 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:31:6
   |
31 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: the `Err`-variant returned from this function is very large
  --> src/native/capture/tests/mod.rs:20:6
   |
20 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 248 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

error: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1345:9
     |
1345 | /         match lex_bullets(close, draft).expect("valid bullets") {
1346 | |             CloseLogLexed { entries, dangling } => {
1347 | |                 assert!(dangling.is_empty(), "unexpected dangling");
1348 | |                 entries
...    |
1353 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
     = note: `-D clippy::match-single-binding` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::match_single_binding)]`
help: consider using a `let` statement
     |
1345 ~         let CloseLogLexed { entries, dangling } = lex_bullets(close, draft).expect("valid bullets");
1346 +         {
1347 +             assert!(dangling.is_empty(), "unexpected dangling");
1348 +             entries
1349 +                 .into_iter()
1350 +                 .map(|entry| (entry.index, entry.text, entry.details))
1351 +                 .collect()
1352 +         }
     |

error: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1451:9
     |
1451 | /         match lex_bullets("x", "x\n- 1").expect("dangling") {
1452 | |             CloseLogLexed { entries, dangling } => {
1453 | |                 assert!(entries.is_empty());
1454 | |                 assert_eq!(dangling.len(), 1);
...    |
1457 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1451 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- 1").expect("dangling");
1452 +         {
1453 +             assert!(entries.is_empty());
1454 +             assert_eq!(dangling.len(), 1);
1455 +             assert_eq!(dangling[0].index, Some(1));
1456 +         }
     |

error: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:1524:9
     |
1524 | /         match lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing") {
1525 | |             error => assert!(
1526 | |                 error.message.contains("- 2 wired"),
1527 | |                 "{}",
1528 | |                 error.message
1529 | |             ),
1530 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
1524 ~         let error = lex_bullets("x~1", "x~1\n- 2 ok\n- wired").expect_err("missing");
1525 +         assert!(
1526 +             error.message.contains("- 2 wired"),
1527 +             "{}",
1528 +             error.message
1529 +         )
     |

error: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2002:9
     |
2002 | /         match lex_bullets("x", "x\n- *").expect("dangling star") {
2003 | |             CloseLogLexed { entries, dangling } => {
2004 | |                 assert!(entries.is_empty());
2005 | |                 assert_eq!(dangling.len(), 1);
...    |
2008 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2002 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *").expect("dangling star");
2003 +         {
2004 +             assert!(entries.is_empty());
2005 +             assert_eq!(dangling.len(), 1);
2006 +             assert_eq!(dangling[0].index, None);
2007 +         }
     |

error: this match could be written as a `let` statement
    --> src/native/capture_language/close_log.rs:2009:9
     |
2009 | /         match lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details")
2010 | |         {
2011 | |             CloseLogLexed { entries, dangling } => {
2012 | |                 assert!(entries.is_empty());
...    |
2016 | |         }
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_single_binding
help: consider using a `let` statement
     |
2009 ~         let CloseLogLexed { entries, dangling } = lex_bullets("x", "x\n- *\n  - dropped").expect("dangling details");
2010 +         {
2011 +             assert!(entries.is_empty());
2012 +             assert_eq!(dangling.len(), 1);
2013 +             assert_eq!(dangling[0].index, None);
2014 +         }
     |

error: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/capture_language/tests/editor_spans.rs:97:16
    |
 97 |       let cases: &[(
    |  ________________^
 98 | |         &str,
 99 | |         &[(usize, usize, SpanKind, Option<ProjectNoteForm>)],
100 | |         &[Need],
101 | |     )] = &[
    | |______^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

error: function call inside of `expect`
  --> src/native/capture_language/tests/goto.rs:54:42
   |
54 |         let completion = field(raw, end).expect(&format!("{raw:?} completes"));
   |                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw:?} completes"))`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call
   = note: `-D clippy::expect-fun-call` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::expect_fun_call)]`

error: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:102:22
    |
102 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

error: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:115:35
    |
115 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

error: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2416:35
     |
2416 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

error: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2453:48
     |
2453 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

error: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2462:22
     |
2462 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

error: unnecessary use of `get(Path::new("b.md")).is_none()`
   --> src/native/capture_pomodoro_close/linked_task_tests.rs:223:28
    |
223 |         plan.changed_files.get(Path::new("b.md")).is_none(),
    |         -------------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |         |
    |         help: replace it with: `!plan.changed_files.contains_key(Path::new("b.md"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
    = note: `-D clippy::unnecessary-get-then-check` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::unnecessary_get_then_check)]`

error: this assertion has a constant value
   --> src/native/file_coordination.rs:225:9
    |
225 |         assert!(!IS_COORDINATED);
    |         ^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: consider moving this into a const block: `const { assert!(..) }`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants
    = note: `-D clippy::assertions-on-constants` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::assertions_on_constants)]`

error: initializer for `thread_local` value can be made `const`
  --> src/native/highlights_ref/overwrite/execute.rs:62:58
   |
62 |     static FAILPOINT: Cell<Option<OverwriteFailpoint>> = Cell::new(None);
   |                                                          ^^^^^^^^^^^^^^^ help: replace with: `const { Cell::new(None) }`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#missing_const_for_thread_local
   = note: `-D clippy::missing-const-for-thread-local` implied by `-D warnings`
   = help: to override `-D warnings` add `#[allow(clippy::missing_const_for_thread_local)]`

error: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/highlights_ref/overwrite/execute.rs:3069:9
     |
3069 |         request.explicit_title = Some("A Better Report".to_string());
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::highlights_ref::overwrite::OverwriteRequest { explicit_title: Some("A Better Report".to_string()), explicit_status: Some("next".to_string()), replacement_audio_path: Some("lib/papers/report.m4a".to_string()), ..Default::default() }` and removing relevant reassignments
    --> src/native/highlights_ref/overwrite/execute.rs:3068:9
     |
3068 |         let mut request = super::super::OverwriteRequest::default();
     |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

error: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/tests/continuations.rs:249:42
    |
249 |     let plan = super::plan_continuations(&[first.clone()]);
    |                                          ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&first)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

error: redundant redefinition of a binding `first`
   --> src/native/highlights_ref/tests/sections.rs:555:9
    |
555 |         let first = first;
    |         ^^^^^^^^^^^^^^^^^^
    |
help: `first` is initially defined here
   --> src/native/highlights_ref/tests/sections.rs:519:14
    |
519 |         let (first, second) = if first_sticky {
    |              ^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

error: replacing text with itself
    --> src/native/highlights_ref/tests/sections_render.rs:1103:22
     |
1103 |       let at_sidecar = sidecar
     |  ______________________^
1104 | |         .replace("#what-is-it", "@what-is-it")
1105 | |         .replace("# what is it", "# what is it");
     | |________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#no_effect_replace
     = note: `-D clippy::no-effect-replace` implied by `-D warnings`
     = help: to override `-D warnings` add `#[allow(clippy::no_effect_replace)]`

error: an array of `Range` that is only one element
   --> src/native/highlights_ref/tests/underlines.rs:290:41
    |
290 |         apply_emphasis(already_strong, &[strong_start..strong_end]),
    |                                         ^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
    = note: `-D clippy::single-range-in-vec-init` implied by `-D warnings`
    = help: to override `-D warnings` add `#[allow(clippy::single_range_in_vec_init)]`
help: if you wanted a `Vec` that contains the entire range, try
    |
290 -         apply_emphasis(already_strong, &[strong_start..strong_end]),
290 +         apply_emphasis(already_strong, &(strong_start..strong_end).collect::<std::vec::Vec<usize>>()),
    |

error: consider using `sort_by_key`
   --> src/native/periods/list.rs:377:9
    |
377 |         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
377 -         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
377 +         sorted.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

error: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/pomodoro.rs:1010:51
     |
1010 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
     |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

error: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

error: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:583:5
    |
583 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:372:9
    |
372 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

error: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:698:27
    |
698 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

error: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:709:27
    |
709 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

error: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:720:27
    |
720 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

error: could not compile `bob-obsidian` (lib test) due to 509 previous errors
   Compiling typenum v1.20.1
   Compiling cfg-if v1.0.4
   Compiling stable_deref_trait v1.2.1
   Compiling shlex v2.0.1
   Compiling equivalent v1.0.2
   Compiling allocator-api2 v0.2.21
   Compiling memchr v2.8.1
   Compiling foldhash v0.2.0
   Compiling litemap v0.8.3
   Compiling writeable v0.6.4
   Compiling simd-adler32 v0.3.9
   Compiling bitflags v2.12.1
   Compiling utf8_iter v1.0.4
   Compiling rand_core v0.10.1
   Compiling adler2 v2.0.1
   Compiling smallvec v1.15.2
   Compiling utf8parse v0.2.2
   Compiling anstyle v1.0.14
   Compiling tinyvec_macros v0.1.1
   Compiling anstyle-query v1.1.5
   Compiling is_terminal_polyfill v1.70.2
   Compiling cpufeatures v0.3.0
   Compiling colorchoice v1.0.5
   Compiling strsim v0.11.1
   Compiling siphasher v1.0.4
   Compiling weezl v0.1.12
   Compiling cpufeatures v0.2.17
   Compiling clap_lex v1.1.0
   Compiling itoa v1.0.18
   Compiling bytecount v0.6.9
   Compiling percent-encoding v2.3.2
   Compiling quick-error v2.0.1
   Compiling regex-syntax v0.8.10
   Compiling byteorder-lite v0.1.0
   Compiling zune-core v0.5.3
   Compiling pxfm v0.1.30
   Compiling unicode-bidi v0.3.18
   Compiling const-oid v0.10.2
   Compiling color_quant v1.1.0
   Compiling iana-time-zone v0.1.65
   Compiling unicode-properties v0.1.4
   Compiling ttf-parser v0.25.1
   Compiling unsafe-libyaml v0.2.11
   Compiling ryu v1.0.23
   Compiling is_executable v1.0.6
   Compiling bytemuck v1.25.2
   Compiling rangemap v1.7.1
   Compiling log v0.4.30
   Compiling bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_29/crates/bob-obsidian-assets)
   Compiling libc v0.2.186
   Compiling serde_core v1.0.228
   Compiling icu_normalizer_data v2.3.0
   Compiling icu_properties_data v2.3.0
   Compiling zmij v1.0.21
   Compiling hex v0.4.3
   Compiling similar v2.7.0
   Compiling linux-raw-sys v0.12.1
   Compiling time-core v0.1.9
   Compiling num-traits v0.2.19
   Compiling deranged v0.5.8
   Compiling powerfmt v0.2.0
   Compiling zerofrom v0.1.8
   Compiling num-conv v0.2.2
   Compiling thiserror v2.0.18
   Compiling fallible-streaming-iterator v0.1.9
   Compiling once_cell v1.21.4
   Compiling crc32fast v1.5.0
   Compiling encoding_rs v0.8.35
   Compiling aho-corasick v1.1.4
   Compiling generic-array v0.14.7
   Compiling hybrid-array v0.4.12
   Compiling nom v8.0.0
   Compiling quick-xml v0.41.0
   Compiling fastrand v2.5.0
   Compiling base64 v0.22.1
   Compiling fallible-iterator v0.3.0
   Compiling yoke v0.8.3
   Compiling tinyvec v1.11.0
   Compiling zune-jpeg v0.5.15
   Compiling hashbrown v0.17.1
   Compiling phf_shared v0.12.1
   Compiling miniz_oxide v0.8.9
   Compiling fdeflate v0.3.7
   Compiling cc v1.2.63
   Compiling chacha20 v0.10.2
   Compiling anstyle-parse v1.0.0
   Compiling getrandom v0.4.2
   Compiling fs2 v0.4.3
   Compiling time v0.3.53
   Compiling image-webp v0.2.4
   Compiling rustix v1.1.5
   Compiling form_urlencoded v1.2.2
   Compiling gif v0.14.2
   Compiling chrono v0.4.44
   Compiling moxcms v0.8.1
   Compiling serde v1.0.228
   Compiling serde_json v1.0.150
   Compiling unicode-normalization v0.1.25
   Compiling regex-automata v0.4.14
   Compiling crypto-common v0.2.2
   Compiling block-buffer v0.12.0
   Compiling nom_locate v5.0.0
   Compiling crypto-common v0.1.7
   Compiling block-padding v0.3.3
   Compiling block-buffer v0.10.4
   Compiling phf v0.12.1
   Compiling flate2 v1.1.9
   Compiling rquickjs-sys v0.12.1
   Compiling libsqlite3-sys v0.38.1
   Compiling zerovec v0.11.8
   Compiling zerotrie v0.2.5
   Compiling indexmap v2.14.0
   Compiling hashlink v0.12.1
   Compiling rand v0.10.1
   Compiling tempfile v3.27.0
   Compiling anstream v1.0.0
   Compiling stringprep v0.1.5
   Compiling chrono-tz v0.10.4
   Compiling tinystr v0.8.4
   Compiling potential_utf v0.1.6
   Compiling digest v0.11.3
   Compiling inout v0.1.4
   Compiling digest v0.10.7
   Compiling png v0.18.1
   Compiling regex v1.12.3
   Compiling rusqlite v0.40.1
   Compiling rquickjs-core v0.12.1
   Compiling clap_builder v4.6.7
   Compiling icu_locale_core v2.3.0
   Compiling serde_yaml v0.9.34+deprecated
   Compiling plist v1.10.0
   Compiling icu_collections v2.3.0
   Compiling sha2 v0.11.0
   Compiling cipher v0.4.4
   Compiling md-5 v0.10.6
   Compiling sha2 v0.10.9
   Compiling icu_provider v2.3.1
   Compiling rquickjs v0.12.1
   Compiling clap v4.6.7
   Compiling image v0.25.10
   Compiling ecb v0.1.2
   Compiling aes v0.8.4
   Compiling cbc v0.1.2
   Compiling icu_properties v2.3.0
   Compiling icu_normalizer v2.3.0
   Compiling clap_complete v4.6.11
   Compiling lopdf v0.40.0
   Compiling idna_adapter v1.2.2
   Compiling idna v1.1.0
   Compiling url v2.5.8
   Compiling bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_29)
    Finished `test` profile [unoptimized + debuginfo] target(s) in 3m 59s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_cli-edb465a55cecd3c2)

running 130 tests
test native::task_status_hooks::reconcile::fields::tests::field_writer_drops_both_fields_for_r9 ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_lands_right_of_fresh_and_replaces_stale ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_removes_depends_on_when_empty ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_places_id_before_depends_on_before_block_id ... ok
test native::task_status_hooks::reconcile::fields::tests::dr_field_projection_vectors ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_field_before_trailing_tags ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_fields_between_tags ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_replaces_parenthesized_metadata ... ok
test native::task_status_hooks::reconcile::fields::tests::field_writer_stamps_target_past_hide_tag ... ok
test native::task_status_hooks::reconcile::fields::tests::reconcile_field_write_preserves_canonical_type ... ok
test native::task_status_hooks::reconcile::fields::tests::reconcile_field_write_preserves_distinctive_root ... ok
test native::task_status_hooks::reconcile::fields::tests::reconcile_field_write_preserves_distinctive_theme ... ok
test native::task_status_hooks::retry::tests::allowed_transient_reasons_are_retried_without_applied_files ... ok
test native::task_status_hooks::retry::tests::any_error_listing_applied_files_is_never_retried ... ok
test native::task_status_hooks::retry::tests::partial_apply_is_never_retried_even_with_no_applied_files ... ok
test native::task_status_hooks::retry::tests::retry_ceiling_progression_caps_at_thirty_seconds ... ok
test native::task_status_hooks::retry::tests::random_unit_interval_varies_and_stays_in_unit_range ... ok
test native::task_status_hooks::retry::tests::retry_delay_stays_within_upper_half_of_ceiling ... ok
test native::task_status_hooks::retry::tests::retry_loop_stops_immediately_on_terminal_reason_without_noise ... ok
test native::task_status_hooks::retry::tests::terminal_and_unknown_reasons_are_never_retried ... ok
test native::task_status_hooks::coalesce::tests::exact_task_guard_refuses_a_join_that_changes_task_shares ... ok
test native::task_status_hooks::coalesce::tests::preserves_crlf_and_child_interior_blank_lines ... ok
test native::task_status_hooks::coalesce::tests::coalesces_credit_neutral_rows_and_preserves_children_in_order ... ok
test native::task_status_hooks::tests::structure::blocks_lines_are_recognized_as_managed ... ok
test native::task_status_hooks::tests::structure::blocks_parser_does_not_claim_other_managed_child_lines ... ok
test native::task_status_hooks::coalesce::tests::repeated_task_dedupes_and_unlinked_sessions_coalesce ... ok
test native::task_status_hooks::tests::blocks::malformed_dependents_are_uncertain_not_edges ... ok
test native::task_status_hooks::tests::blocks::explicit_edges_include_idless_dependents ... ok
test native::task_status_hooks::tests::structure::canceled_subtree_deletion_preserves_crlf_and_no_final_newline ... ok
test native::task_status_hooks::tests::structure::cancellation_classification_uses_recognized_tasks_status_types ... ok
test native::task_status_hooks::tests::blocks::explicit_edges_exclude_implicit_resident_and_br18_br20 ... ok
test native::task_status_hooks::tests::structure::canceled_subtrees_compose_with_nested_and_moving_bullets ... ok
test native::task_status_hooks::tests::structure::both_managed_dependency_lines_are_not_pomodoro_task_links ... ok
test native::task_status_hooks::coalesce::tests::rejects_gaps_types_clock_meet_open_legacy_ids_midnight_and_indent_mix ... ok
test native::task_status_hooks::tests::structure::canceled_reference_removal_deletes_complete_mixed_content_items ... ok
test native::task_status_hooks::tests::structure::capture_consumption_keeps_link_only_notes_as_clean_task_text ... ok
test native::task_status_hooks::tests::structure::completed_fallback_does_not_take_mixed_live_bullets ... ok
test native::task_status_hooks::tests::structure::capture_only_removes_pomodoros_emptied_by_this_consumption ... ok
test native::task_status_hooks::tests::structure::completion_classification_accepts_conventional_and_custom_done_only ... ok
test native::task_status_hooks::tests::structure::conflicting_duplicate_statuses_are_not_normalized ... ok
test native::task_status_hooks::coalesce::tests::component_guard_and_fixed_point_are_exact_and_idempotent ... ok
test native::task_status_hooks::tests::structure::consumes_blocked_live_link_and_keeps_the_entry ... ok
test native::task_status_hooks::tests::structure::consuming_last_child_empties_the_pomodoro ... ok
test native::task_status_hooks::tests::structure::consumption_removes_link_only_subtree_with_child_notes ... ok
test native::task_status_hooks::tests::structure::consumption_skips_closed_entries_and_struck_links ... ok
test native::task_status_hooks::tests::structure::consumption_strips_the_token_from_a_prose_bullet ... ok
test native::task_status_hooks::tests::structure::dependency_line_forms_are_managed ... ok
test native::task_status_hooks::tests::structure::deleted_completed_duplicate_is_not_retired_moved_or_reinserted ... ok
test native::task_status_hooks::tests::structure::deleted_conflict_line_cannot_claim_an_unrelated_task ... ok
test native::task_status_hooks::tests::structure::direct_child_scan_counts_plain_children_but_ignores_fences ... ok
test native::task_status_hooks::tests::structure::duplicate_cleanup_ignores_distinct_unresolved_and_ineligible_links ... ok
test native::task_status_hooks::tests::structure::duplicate_deleted_lines_do_not_report_canceled_reference_edits ... ok
test native::task_status_hooks::tests::structure::empty_blocked_set_does_not_consume_question_status_links ... ok
test native::task_status_hooks::tests::structure::empty_pomodoro_deletion_removes_full_blocks_and_preserves_crlf_eof ... ok
test native::task_status_hooks::tests::structure::empty_timed_entries_are_not_current_targets_or_ambiguity_inputs ... ok
test native::task_status_hooks::tests::structure::duplicate_lines_use_canonical_task_identity_and_first_open_owner ... ok
test native::task_status_hooks::tests::structure::extracts_only_block_links_under_open_pomodoros ... ok
test native::task_status_hooks::tests::structure::entries_emptied_by_duplicate_cleanup_are_removed_in_same_pass ... ok
test native::task_status_hooks::tests::structure::full_line_deletion_preserves_children_crlf_and_final_line_ending ... ok
test native::task_status_hooks::tests::structure::parses_and_normalizes_pomodoro_marker_prefixes_per_link ... ok
test native::task_status_hooks::tests::structure::parses_embedded_alias_and_mixed_block_links ... ok
test native::task_status_hooks::tests::structure::moves_completed_mixed_bullet_subtree_to_current_and_strikes_only_done ... ok
test native::task_status_hooks::tests::structure::moving_last_child_removes_source_but_retains_destination ... ok
test native::task_status_hooks::tests::structure::relation_lines_are_managed_link_lines_not_dependency_lines ... ok
test native::task_status_hooks::retry::tests::retry_loop_with_zero_budget_makes_one_attempt_and_never_sleeps ... ok
test native::task_status_hooks::tests::structure::struck_references_are_retired_and_spans_are_paired ... ok
test native::task_status_hooks::tests::structure::repairs_markers_by_owner_and_marks_completed_fallback_moves ... ok
test native::task_status_hooks::tests::structure::two_non_empty_timed_entries_still_match_the_ambiguity_guard ... ok
test native::task_status_hooks::tests::sync::ambiguous_basename_does_not_resolve ... ok
test native::task_status_hooks::tests::structure::repairs_completed_pomodoro_links_in_place_and_is_idempotent ... ok
test native::task_status_hooks::tests::sync::blocked_transition_precedence_and_recovery_are_explicit ... ok
test native::task_status_hooks::tests::sync::dated_day_file_overrides_effective_anchor_and_malformed_name_falls_back ... ok
test native::task_status_hooks::tests::sync::archive_targets_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::child_links_are_not_dependency_edges ... ok
test native::task_status_hooks::tests::sync::desired_statuses_raise_a_directly_linked_prj ... ok
test native::task_status_hooks::tests::sync::desired_statuses_merge_parents_and_propagate_stronger_intermediates_through_cycles ... ok
test native::task_status_hooks::tests::sync::desired_statuses_walk_through_project_tasks_without_raising_them ... ok
test native::task_status_hooks::tests::sync::dependency_line_links_are_promotion_edges ... ok
test native::task_status_hooks::tests::sync::future_schedule_uses_the_calendar_day_after_the_anchor ... ok
test native::task_status_hooks::tests::sync::fenced_column_zero_content_does_not_end_dependency_scan ... ok
test native::task_status_hooks::tests::sync::hand_blocked_prj_with_no_reasons_recovers ... ok
test native::task_status_hooks::tests::sync::note_kind_uses_shared_area_and_project_frontmatter_predicates ... ok
test native::task_status_hooks::tests::sync::parses_bracket_and_parenthesized_task_dependency_metadata ... ok
test native::task_status_hooks::tests::sync::parses_task_markers_and_preserves_status_offsets ... ok
test native::task_status_hooks::tests::sync::parses_only_calendar_valid_scheduled_metadata_in_supported_forms ... ok
test native::task_status_hooks::tests::sync::previous_daily_selection_uses_latest_canonical_earlier_date ... ok
test native::task_status_hooks::tests::sync::prj_reports_only_own_reasons ... ok
test native::task_status_hooks::tests::sync::reading_embeds_are_not_promotion_edges ... ok
test native::task_status_hooks::tests::sync::recent_links_include_completed_live_links_but_exclude_retired_links ... ok
test native::task_status_hooks::tests::sync::recovery_rank_defaults_blocked_roots_to_next_and_propagates_in_progress ... ok
test native::task_status_hooks::tests::sync::replacement_changes_only_status_and_preserves_crlf ... ok
test native::task_status_hooks::retry::tests::retry_loop_clamps_sleep_to_remaining_budget ... ok
test native::task_status_hooks::tests::sync::dotted_note_names_keep_the_full_basename ... ok
test native::task_status_hooks::tests::sync::resolves_exact_and_unique_case_insensitive_basenames ... ok
test native::task_status_hooks::tests::sync::same_note_recent_links_resolve_in_each_daily_context ... ok
test native::task_status_hooks::tests::sync::sticky_lanes_keep_next_and_in_progress_outside_daily_notes ... ok
test native::task_status_hooks::tests::sync::transition_matrix_promotes_monotonically_and_clears_only_unreferenced_next ... ok
test native::task_status_hooks::tests::sync::residents_inherit_prj_links_as_implicit_edges ... ok
test native::task_status_hooks::tests::sync::task_dependency_index_matches_tasks_duplicate_and_missing_id_semantics ... ok
test native::task_status_hooks::tests::sync::hand_copied_tag_outside_blocked_projects_is_stripped ... ok
test native::task_status_hooks::retry::tests::retry_decision_log_includes_run_attempt_reason_and_recovery_directory ... ok
test native::task_status_hooks::tests::sync::blocked_project_marks_and_tags_residents ... ok
test native::task_status_hooks_write::tests::deletion_prevents_write ... ok
test native::task_status_hooks::tests::sync::parenthesized_repeat_skips_unblocked_write ... ok
test native::task_status_hooks::tests::sync::recovery_strips_tag_and_writes_unblocked ... ok
test native::task_status_hooks_write::tests::future_mtime_defers_without_sleeping ... ok
test native::task_status_hooks_write::tests::changed_previous_daily_prevents_write ... ok
test native::task_status_hooks_write::tests::equal_length_change_with_restored_mtime_prevents_write ... ok
test native::task_status_hooks::tests::sync::stale_unblocked_field_is_pruned_without_status_change ... ok
test native::task_status_hooks_write::tests::noop_creates_no_recovery_or_staging ... ok
test native::task_status_hooks_write::tests::multiply_linked_output_is_rejected ... ok
test native::task_status_hooks::tests::sync::lane_raises_strip_keeps_and_ready_unblock_preserves_them ... ok
test native::task_status_hooks_write::tests::quiet_period_waits_once_then_defers_if_changed ... ok
test native::task_status_hooks_write::tests::replacement_inode_prevents_write ... ok
test native::task_status_hooks_write::tests::live_rescan_sees_new_vault_file ... ok
test native::task_status_hooks::tests::sync::misplaced_existing_tag_is_not_counted_as_added ... ok
test native::task_status_hooks_write::tests::new_or_deleted_scan_candidate_invalidates_plan ... ok
test native::task_status_hooks_write::tests::changed_tasks_settings_prevent_write ... ok
test native::task_status_hooks_write::tests::symlink_substitution_prevents_write ... ok
test native::task_status_hooks::retry::tests::retry_loop_retries_lock_contention_then_succeeds ... ok
test native::task_status_hooks::retry::tests::retry_loop_never_starts_another_attempt_once_budget_is_exhausted ... ok
test native::task_status_hooks_write::tests::edit_between_staging_and_revalidate_survives ... ok
test native::task_status_hooks_write::tests::staging_failure_preserves_notes_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::exclusive_temp_and_mode_and_foreign_temps ... ok
test native::task_status_hooks_write::tests::retention_keeps_incomplete_and_prunes_old_completed ... ok
test native::task_status_hooks_write::tests::fresh_attempt_after_vault_changed_replans_from_intervening_edit ... ok
test native::task_status_hooks_write::tests::tool_scopes_recovery_root_manifest_and_pruning ... ok
test native::task_status_hooks_write::tests::edit_before_later_replacement_reports_partial ... ok
test native::task_status_hooks_write::tests::unchanged_read_set_applies_and_records_recovery_bytes ... ok
test native::task_status_hooks_write::tests::quiet_period_skips_wait_for_stable_files_and_status_only ... ok

test result: ok. 130 passed; 0 failed; 0 ignored; 0 measured; 4906 filtered out; finished in 0.16s

     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob-39abebeb4ad07360)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_notify-f1a59fb8e3d29c43)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_pomodoro-a1880c6eed04140e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tmux_bob_pomodoro-5d65a532f2abf4a7)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/cli-862b59fffc4caf66)

running 178 tests
test help_options::task_status_hooks_help_lists_options_alphabetically ... ok
test task_status_hooks::blocked::reconcile_keeps_prj_internal_links_unprojected ... ok
test task_status_hooks::blocked::reconcile_does_not_promote_same_note_ids_through_resident_edges ... ok
test task_status_hooks::blocked::reconcile_derives_project_schedule_blocking ... ok
test task_status_hooks::blocked::reconcile_cascades_to_child_projects ... ok
test task_status_hooks::blocked::reconcile_does_not_warn_for_an_unfielded_internal_child_link ... ok
test task_status_hooks::blocked::reconcile_filters_project_internal_ids_by_id_field_only ... ok
test task_status_hooks::blocked::reconcile_ignores_two_scheduled_prj_tasks ... ok
test task_status_hooks::blocked::reconcile_keeps_field_only_internal_prj_ids_unprojected ... ok
test task_status_hooks::blocked::reconcile_ignores_terminal_projects ... ok
test task_status_hooks::blocked::reconcile_ignores_notes_with_two_open_prj_lines ... ok
test task_status_hooks::blocked::reconcile_ignores_canonical_daily_note_projects ... ok
test task_status_hooks::blocks::br25_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::blocked::reconcile_warns_inherited_resident_cycle ... ok
test help::task_status_hooks_help_is_native_only ... ok
test task_status_hooks::blocks::br28_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::blocked::reconcile_treats_uppercase_prj_anchor_as_an_ordinary_task ... ok
test task_status_hooks::blocked::task_status_hooks_blocked_status_guard_writes_nothing ... ok
test task_status_hooks::consume::reconcile_keeps_a_link_when_the_block_clears_in_the_same_run ... ok
test task_status_hooks::blocked::reconcile_raises_directly_linked_prj ... ok
test task_status_hooks::blocks::br20_internal_prj_target_is_not_listed ... ok
test task_status_hooks::blocks::br17_malformed_dependent_is_kept_not_newly_added ... ok
test task_status_hooks::blocks::br12_previous_daily_is_never_written_or_listed ... ok
test task_status_hooks::blocks::br18_unresolved_self_and_non_task_are_not_listed ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_unresolved_link_and_breadcrumbs ... ok
test task_status_hooks::dependency_lines::reconcile_warns_dependency_cycle_and_keeps_members_blocked ... ok
test task_status_hooks::dependency_lines::reconcile_never_writes_previous_daily_target ... ok
test task_status_hooks::coalesce::coalescing_dry_run_live_write_and_second_run_are_reported ... ok
test task_status_hooks::dependency_lines::reconcile_skips_closed_dependents ... ok
test task_status_hooks::dependency_lines::reconcile_projection_only_write_defers_in_quiet_interval ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unadoptable_id_and_keeps_field ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unencodable_target_without_projecting ... ok
test task_status_hooks::relations::configured_cancel_label_stays_inert_during_reconcile ... ok
test task_status_hooks::relations::lr12_malformed_linked_from_left_alone ... ok
test task_status_hooks::relations::lr14_unresolved_non_task_self_warned_and_omitted ... ok
test task_status_hooks::dependency_lines::reconcile_daily_note_keeps_adoption_and_stamp ... ok
test task_status_hooks::blocked::reconcile_preserves_crlf_on_tag_rewrite ... ok
test task_status_hooks::blocks::br21_field_only_dependency_is_adopted_and_listed ... ok
test task_status_hooks::blocks::br13_hand_added_entry_without_edge_is_removed ... ok
test task_status_hooks::blocks::br14_canonicalizes_blocking_label ... ok
test task_status_hooks::blocks::br15_deduplicates_and_deletes_orphans ... ok
test task_status_hooks::blocks::br16_malformed_blocks_line_is_left_alone ... ok
test task_status_hooks::blocks::br22_cycle_each_lists_the_other ... ok
test task_status_hooks::relations::lr17_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::blocked::task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test task_status_hooks::relations::lr21_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_deletes_line_and_field ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_with_adoptable_id_deletes_line_and_field ... ok
test task_status_hooks::relations::lr23_duplicate_source_id_not_listed ... ok
test task_status_hooks::blocked::task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test task_status_hooks::blocks::br27_second_run_is_idempotent ... ok
test task_status_hooks::blocks::br6_inserts_after_depends_on_subtree ... ok
test task_status_hooks::blocks::br29_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::dependency_line_writes::summary_reports_dependency_counts ... ok
test task_status_hooks::blocks::br24_kill_switch_removes_open_lines_and_skips_mints ... ok
test task_status_hooks::consume::reconcile_deletes_a_pomodoro_emptied_by_blocked_consumption ... ok
test task_status_hooks::blocks::br7_inserts_second_after_cancel_log ... ok
test task_status_hooks::blocks::br10_closed_owner_is_frozen ... ok
test task_status_hooks::blocks::br4_mints_idless_dependent_without_id_or_fresh_fields ... ok
test task_status_hooks::blocks::br1_same_note_insert ... ok
test task_status_hooks::relations::lr_human_output_includes_knot_group ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw3_dw6_rewrite_keeps_link_order ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw2_inserts_adopted_line_after_cancel_log ... ok
test task_status_hooks::consume::reconcile_does_not_reraise_hand_set_ready_after_blocked_consume ... ok
test task_status_hooks::dependency_lines::reconcile_adopts_field_ids_into_canonical_line ... ok
test task_status_hooks::dependency_lines::reconcile_drops_stale_field_id ... ok
test task_status_hooks::dependency_lines::reconcile_field_writer_handles_trailing_tags ... ok
test task_status_hooks::dependency_lines::reconcile_canonicalizes_legacy_line_variants ... ok
test task_status_hooks::dependency_lines::reconcile_does_not_read_child_links_as_dependencies ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw1_inserts_adopted_line_before_schedule_log ... ok
test task_status_hooks::dependency_lines::reconcile_dependency_chain_settles_in_one_run ... ok
test task_status_hooks::retry::task_status_hooks_defers_when_maintenance_lock_is_held ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_terminal_failure_and_exit_status ... ok
test task_status_hooks::relations::mn_human_output_includes_mention_counts ... ok
test task_status_hooks::blocked::reconcile_terminal_project_prerequisite_does_not_block_residents ... ok
test task_status_hooks::relations::mn_invalid_mentions_switch_uses_enabled_default ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test task_status_hooks::dependency_lines::reconcile_ignores_archive_children_outside_the_depends_on_line ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_creates_no_lock_or_recovery ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_ignores_retry_timeout ... ok
test task_status_hooks::retry::task_status_hooks_rejects_invalid_retry_timeout ... ok
test task_status_hooks::blocked::reconcile_pdf1_databricks_ref_residents ... ok
test task_status_hooks::retry::task_status_hooks_live_noop_may_lock_but_creates_no_recovery ... ok
test task_status_hooks::settle::settle_human_output_names_events ... ok
test task_status_hooks::blocks::br5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test task_status_hooks::dependency_lines::reconcile_projects_line_into_field_and_stamps_target_id ... ok
test task_status_hooks::dependency_lines::reconcile_heals_moved_link ... ok
test task_status_hooks::consume::reconcile_consumes_blocked_resident_links_and_keeps_the_entry ... ok
test task_status_hooks::blocks::br23_hide_ref_inbox_and_daily_are_listed ... ok
test task_status_hooks::dependency_lines::reconcile_breadcrumb_heals_when_target_returns ... ok
test task_status_hooks::dependency_lines::reconcile_removes_empty_line_and_leaves_malformed_alone ... ok
test task_status_hooks::dependency_lines::reconcile_same_index_insert_does_not_clobber_replace ... ok
test task_status_hooks::relations::lr7_done_and_previous_daily_targets_never_written ... ok
test task_status_hooks::blocks::br19_prj_lists_only_the_project_task ... ok
test task_status_hooks::dependency_lines::reconcile_warns_non_task_and_self_links_without_projecting ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test task_status_hooks::relations::lr22_archived_source_keeps_done_form ... ok
test task_status_hooks::subprojects::projects_sync_ignores_cascade_tags_and_keeps_marker_state ... ok
test task_status_hooks::subprojects::descendant_project_targets_stay_unprojected_and_warn ... ok
test task_status_hooks::subprojects::inherited_edges_participate_in_r7_cycle_detection ... ok
test task_status_hooks::subprojects::blocked_subproject_links_are_consumed_and_promote_ancestor_prerequisites ... ok
test task_status_hooks::subprojects::project_parent_cycles_warn_once_and_only_inherit_other_projects_reasons ... ok
test task_status_hooks::consume::consumption_promoted_daily_note_prerequisite_may_clear_next_run ... ok
test task_status_hooks::blocks::br8_prj_order_then_projects_sync_is_noop ... ok
test task_status_hooks::blocks::br3_one_line_sorted_across_notes ... ok
test task_status_hooks::relations::lr10_noncanonical_line_is_canonicalized ... ok
test task_status_hooks::sync::task_status_hooks_nulls_plan_budget_on_invalid_config ... ok
test task_status_hooks::blocks::br2_unique_and_ambiguous_basename_links ... ok
test task_status_hooks::subprojects::reconciled_cascade_tree_has_no_second_run_changes ... ok
test task_status_hooks::subprojects::reconcile_recovers_subprojects_and_keeps_nearest_remaining_reason ... ok
test task_status_hooks::subprojects::reconcile_cascades_reasons_and_tags_through_multiple_project_levels ... ok
test task_status_hooks::dependency_lines::reconcile_stamps_cross_note_target_id ... ok
test task_status_hooks::settle::settle_back_to_back_cluster_and_trims_around_on_clock ... ok
test task_status_hooks::settle::settle_fully_covered_cluster_does_nothing ... ok
test task_status_hooks::settle::settle_ignores_cancelled_done_unlinked_and_on_clock_events ... ok
test task_status_hooks::structure::task_status_hooks_resolves_archive_references_read_only ... ok
test task_status_hooks::sync::task_status_hooks_reports_grouping_warnings_without_noop_text ... ok
test task_status_hooks::structure::task_status_hooks_composes_daily_status_and_structural_edits ... ok
test task_status_hooks::sync::task_status_hooks_reports_plan_budget_in_json_and_human ... ok
test task_status_hooks::structure::task_status_hooks_drops_carried_link_already_in_completed_fallback ... ok
test task_status_hooks::relations::lr13_malformed_links_never_newly_added ... ok
test task_status_hooks::settle::settle_inherited_off_clock_event_settles_once_and_on_stays_open ... ok
test task_status_hooks::relations::lr15_duplicate_linked_from_lines_deduplicated ... ok
test task_status_hooks::structure::task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks::settle::settle_single_ended_off_clock_event ... ok
test task_status_hooks::structure::task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test task_status_hooks::settle::settle_running_on_clock_session_trims_and_mixed_placeholder_keeps_future ... ok
test task_status_hooks::structure::task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test task_status_hooks::structure::task_status_hooks_keeps_archive_out_of_active_dependency_sync ... ok
test task_status_hooks::sync::reconcile_status_only_flips_skip_quiet_period_but_structural_edits_wait ... ok
test task_status_hooks::structure::task_status_hooks_removes_empty_pomodoros_and_reports_them ... ok
test task_status_hooks::settle::settled_meet_children_follow_the_note_indent_unit ... ok
test task_status_hooks::structure::task_status_hooks_normalizes_live_archive_terminal_references ... ok
test task_status_hooks::sync::task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test task_status_hooks::retry::task_status_hooks_exhausts_retry_budget_and_still_fails ... ok
test task_status_hooks::retry::task_status_hooks_human_retry_progress_goes_to_stdout ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_retry_and_final_result ... ok
test projects::schedule::projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test task_status_hooks::blocks::br9_last_dependent_close_removes_line ... ok
test task_status_hooks::relations::lr19_symmetric_edges ... ok
test task_status_hooks::blocks::br11_reopened_owner_is_reprojected ... ok
test task_status_hooks::blocks::br26_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::retry::task_status_hooks_json_retry_progress_stays_off_stdout ... ok
test task_status_hooks::relations::lr24_prj_target_gets_the_mirror ... ok
test task_status_hooks::relations::lr20_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::relations::lr2_labelled_edge ... ok
test task_status_hooks::relations::lr1_same_note_insert ... ok
test task_status_hooks::relations::lr3_sorted_sources_include_done ... ok
test task_status_hooks::relations::lr4_mints_source_id ... ok
test task_status_hooks::relations::lr6_closed_target_still_mirrored ... ok
test task_status_hooks::relations::lr8_done_and_previous_daily_sources_are_listed ... ok
test task_status_hooks::relations::lr9_hand_added_and_deleted_entries ... ok
test task_status_hooks::relations::mention_only_owner_with_mentions_off_loses_only_mention_entries ... ok
test task_status_hooks::relations::mn1_json_reports_mention_subset_and_edges ... ok
test task_status_hooks::relations::mention_and_relation_mint_reports_relation_reason ... ok
test task_status_hooks::relations::mn8_relation_wins_over_mention ... ok
test task_status_hooks::relations::mn9_dependency_suppresses_mention_but_not_relation ... ok
test task_status_hooks::blocked::reconcile_derives_project_blocking_tag_and_unblocked ... ok
test task_status_hooks::sync::reconcile_raises_ready_with_keeps_to_next_without_keeps ... ok
test task_status_hooks::structure::task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test task_status_hooks::relations::lr16_kill_switch_removes_writable_lines_and_skips_mints ... ok
test task_status_hooks::relations::mn11_mints_idless_source_with_mention_reason ... ok
test task_status_hooks::relations::lr5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::relations::lr11_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::sync::task_status_hooks_un_decorates_legacy_groups_holding_only_ready ... ok
test task_status_hooks::structure::task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test task_status_hooks::sync::task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test task_status_hooks::sync::task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test task_status_hooks::sync::task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test task_status_hooks::relations::mn14_rebuilds_identical_bytes_after_deleting_mention_lines ... ok
test task_status_hooks::relations::mn17_mention_writes_are_inert ... ok
test task_status_hooks::relations::mn13_mentions_off_drops_only_mention_entries ... ok
test task_status_hooks::relations::lr18_inert_statuses_and_fields ... ok
test task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses ... ok
test task_status_hooks::relations::mn_fixture_reconcile_mirrors_and_mints ... ok

test result: ok. 178 passed; 0 failed; 0 ignored; 0 measured; 2980 filtered out; finished in 26.77s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/dataview_parity-045096bc8cc5f0cf)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 27 filtered out; finished in 0.00s

     Running tests/gcal_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_auth-5d44594e9efeed44)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 53 filtered out; finished in 0.00s

     Running tests/gcal_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_cli-4853c16bfec90355)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gcal_diagnostics.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_diagnostics-3e6fd7d18ca75de6)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 4 filtered out; finished in 0.00s

     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_lifecycle-0c23bd6bd84e8a6f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 44 filtered out; finished in 0.00s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_list-95d8d3d0d1e7df7e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_sync-fd2f0701023233dc)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_adapter-a41834edd3018b24)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_auth-f4da0806ca5ba93e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 14 filtered out; finished in 0.00s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_cli-a204c8fbda174c45)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_list-36fbd230bb53870f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 23 filtered out; finished in 0.00s

     Running tests/gkeep_migrate.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_migrate-3f3c4b52e1837a47)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_pull-dd0da037d577b7d1)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_pull_recovery.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_pull_recovery-5e7761c13c11d64b)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gkeep_status.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_status-44b7313be29df440)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 26 filtered out; finished in 0.00s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/randomize-f69db91da68364ae)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 15 filtered out; finished in 0.00s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tasks_parity-a579f56c8602ab2e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 33 filtered out; finished in 0.00s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tasks_real_vault_parity-0d2dc2f594a35474)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.14s
     Running unittests src/lib.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_cli-edb465a55cecd3c2)

running 19 tests
test native::pomodoro_homes::tests::fallback_palette_fnv_vector_is_pinned ... ok
test native::pomodoro_homes::tests::closed_session_task_credit_refuses_missing_and_ambiguous_links ... ok
test native::pomodoro_homes::tests::closed_session_task_credit_deduplicates_aliases_and_handles_unlinked_rows ... ok
test native::pomodoro_homes::tests::closed_session_task_credit_uses_stats_split_and_link_identity ... ok
test native::pomodoro_homes::tests::note_facts_parse_canonical_task_type_and_conflict ... ok
test native::pomodoro_homes::tests::leftover_rollup_key_neither_regroups_nor_warns ... ok
test native::pomodoro_homes::tests::note_facts_parse_theme_scalars_lists_and_off ... ok
test native::pomodoro_homes::tests::daily_notes_walk_like_any_other_note ... ok
test native::pomodoro_homes::tests::note_facts_parse_offclock_as_a_strict_tristate ... ok
test native::pomodoro_homes::tests::split_minutes_uses_ledger_order_for_remainder ... ok
test native::pomodoro_homes::tests::session_link_sibling_includes_struck_and_embedded_bare_links_only ... ok
test native::pomodoro_homes::tests::root_flag_makes_a_project_its_own_root_parent ... ok
test native::pomodoro_homes::tests::root_parent_follows_the_examples_table ... ok
test native::pomodoro_homes::tests::home_for_link_uses_spaced_root_key_on_the_block ... ok
test native::pomodoro_homes::tests::home_for_task_uses_set_root_as_if_residence ... ok
test native::pomodoro_homes::tests::note_facts_collect_unique_task_roots_and_skip_duplicates ... ok
test native::pomodoro_homes::tests::effective_clock_uses_tags_and_the_shared_root_note_walk ... ok
test native::pomodoro_homes::tests::resolved_home_keeps_the_residence_note_chain ... ok
test native::pomodoro_homes::tests::shared_vectors_match_indexed_and_disk_sources ... ok

test result: ok. 19 passed; 0 failed; 0 ignored; 0 measured; 5017 filtered out; finished in 0.03s

     Running unittests src/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob-39abebeb4ad07360)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_notify.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_notify-f1a59fb8e3d29c43)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/bob_pomodoro-a1880c6eed04140e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running unittests src/bin/tmux_bob_pomodoro.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tmux_bob_pomodoro-5d65a532f2abf4a7)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 0 filtered out; finished in 0.00s

     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/cli-862b59fffc4caf66)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 3158 filtered out; finished in 0.00s

     Running tests/dataview_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/dataview_parity-045096bc8cc5f0cf)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 27 filtered out; finished in 0.00s

     Running tests/gcal_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_auth-5d44594e9efeed44)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 53 filtered out; finished in 0.00s

     Running tests/gcal_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_cli-4853c16bfec90355)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gcal_diagnostics.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_diagnostics-3e6fd7d18ca75de6)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 4 filtered out; finished in 0.00s

     Running tests/gcal_lifecycle.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_lifecycle-0c23bd6bd84e8a6f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 44 filtered out; finished in 0.00s

     Running tests/gcal_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_list-95d8d3d0d1e7df7e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gcal_sync.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gcal_sync-fd2f0701023233dc)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_adapter.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_adapter-a41834edd3018b24)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_auth.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_auth-f4da0806ca5ba93e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 14 filtered out; finished in 0.00s

     Running tests/gkeep_cli.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_cli-a204c8fbda174c45)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 6 filtered out; finished in 0.00s

     Running tests/gkeep_list.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_list-36fbd230bb53870f)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 23 filtered out; finished in 0.00s

     Running tests/gkeep_migrate.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_migrate-3f3c4b52e1837a47)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 9 filtered out; finished in 0.00s

     Running tests/gkeep_pull.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_pull-dd0da037d577b7d1)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 50 filtered out; finished in 0.00s

     Running tests/gkeep_pull_recovery.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_pull_recovery-5e7761c13c11d64b)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 7 filtered out; finished in 0.00s

     Running tests/gkeep_status.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/gkeep_status-44b7313be29df440)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 26 filtered out; finished in 0.00s

     Running tests/randomize.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/randomize-f69db91da68364ae)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 15 filtered out; finished in 0.00s

     Running tests/tasks_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tasks_parity-a579f56c8602ab2e)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 33 filtered out; finished in 0.00s

     Running tests/tasks_real_vault_parity.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/tasks_real_vault_parity-0d2dc2f594a35474)

running 0 tests

test result: ok. 0 passed; 0 failed; 0 ignored; 0 measured; 1 filtered out; finished in 0.00s

    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.13s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/cli-862b59fffc4caf66)

running 178 tests
test help_options::task_status_hooks_help_lists_options_alphabetically ... ok
test task_status_hooks::blocked::reconcile_ignores_notes_with_two_open_prj_lines ... ok
test task_status_hooks::blocked::reconcile_ignores_two_scheduled_prj_tasks ... ok
test task_status_hooks::blocked::reconcile_ignores_canonical_daily_note_projects ... ok
test task_status_hooks::blocked::reconcile_keeps_field_only_internal_prj_ids_unprojected ... ok
test task_status_hooks::blocked::reconcile_does_not_warn_for_an_unfielded_internal_child_link ... ok
test task_status_hooks::blocked::reconcile_cascades_to_child_projects ... ok
test task_status_hooks::blocked::reconcile_does_not_promote_same_note_ids_through_resident_edges ... ok
test task_status_hooks::blocked::reconcile_keeps_prj_internal_links_unprojected ... ok
test task_status_hooks::blocked::reconcile_derives_project_schedule_blocking ... ok
test task_status_hooks::blocked::reconcile_ignores_terminal_projects ... ok
test task_status_hooks::blocked::reconcile_filters_project_internal_ids_by_id_field_only ... ok
test help::task_status_hooks_help_is_native_only ... ok
test task_status_hooks::blocks::br28_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::blocked::reconcile_treats_uppercase_prj_anchor_as_an_ordinary_task ... ok
test task_status_hooks::blocks::br25_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::blocked::reconcile_warns_inherited_resident_cycle ... ok
test task_status_hooks::blocked::task_status_hooks_blocked_status_guard_writes_nothing ... ok
test task_status_hooks::blocked::reconcile_raises_directly_linked_prj ... ok
test task_status_hooks::blocks::br12_previous_daily_is_never_written_or_listed ... ok
test task_status_hooks::blocks::br18_unresolved_self_and_non_task_are_not_listed ... ok
test task_status_hooks::consume::reconcile_keeps_a_link_when_the_block_clears_in_the_same_run ... ok
test task_status_hooks::blocks::br20_internal_prj_target_is_not_listed ... ok
test task_status_hooks::blocks::br17_malformed_dependent_is_kept_not_newly_added ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_unresolved_link_and_breadcrumbs ... ok
test task_status_hooks::dependency_lines::reconcile_warns_dependency_cycle_and_keeps_members_blocked ... ok
test task_status_hooks::dependency_lines::reconcile_never_writes_previous_daily_target ... ok
test task_status_hooks::coalesce::coalescing_dry_run_live_write_and_second_run_are_reported ... ok
test task_status_hooks::dependency_lines::reconcile_skips_closed_dependents ... ok
test task_status_hooks::dependency_lines::reconcile_projection_only_write_defers_in_quiet_interval ... ok
test task_status_hooks::dependency_lines::task_status_hooks_promotes_prerequisite_through_depends_on_line ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unadoptable_id_and_keeps_field ... ok
test task_status_hooks::relations::configured_cancel_label_stays_inert_during_reconcile ... ok
test task_status_hooks::dependency_lines::reconcile_warns_unencodable_target_without_projecting ... ok
test task_status_hooks::relations::lr12_malformed_linked_from_left_alone ... ok
test task_status_hooks::relations::lr14_unresolved_non_task_self_warned_and_omitted ... ok
test task_status_hooks::blocks::br13_hand_added_entry_without_edge_is_removed ... ok
test task_status_hooks::blocked::reconcile_preserves_crlf_on_tag_rewrite ... ok
test task_status_hooks::blocks::br10_closed_owner_is_frozen ... ok
test task_status_hooks::blocked::task_status_hooks_unblocks_to_final_pomodoro_rank_and_ready ... ok
test task_status_hooks::dependency_lines::reconcile_daily_note_keeps_adoption_and_stamp ... ok
test task_status_hooks::blocks::br22_cycle_each_lists_the_other ... ok
test task_status_hooks::blocks::br16_malformed_blocks_line_is_left_alone ... ok
test task_status_hooks::blocks::br6_inserts_after_depends_on_subtree ... ok
test task_status_hooks::blocks::br15_deduplicates_and_deletes_orphans ... ok
test task_status_hooks::blocks::br21_field_only_dependency_is_adopted_and_listed ... ok
test task_status_hooks::blocks::br7_inserts_second_after_cancel_log ... ok
test task_status_hooks::blocks::br14_canonicalizes_blocking_label ... ok
test task_status_hooks::relations::lr17_invalid_kill_switch_behaves_as_true ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_blocked_status_from_dataview_dependencies ... ok
test task_status_hooks::relations::lr21_owner_future_mtime_defers_structurally ... ok
test task_status_hooks::blocked::task_status_hooks_uses_recent_ledgers_only_for_blocked_recovery ... ok
test task_status_hooks::blocks::br4_mints_idless_dependent_without_id_or_fresh_fields ... ok
test task_status_hooks::relations::lr23_duplicate_source_id_not_listed ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_deletes_line_and_field ... ok
test task_status_hooks::relations::lr_human_output_includes_knot_group ... ok
test task_status_hooks::blocks::br29_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::blocks::br24_kill_switch_removes_open_lines_and_skips_mints ... ok
test task_status_hooks::consume::reconcile_deletes_a_pomodoro_emptied_by_blocked_consumption ... ok
test task_status_hooks::dependency_line_writes::summary_reports_dependency_counts ... ok
test task_status_hooks::blocked::reconcile_terminal_project_prerequisite_does_not_block_residents ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw1_inserts_adopted_line_before_schedule_log ... ok
test task_status_hooks::dependency_lines::reconcile_adopts_field_ids_into_canonical_line ... ok
test task_status_hooks::dependency_lines::reconcile_canonicalizes_legacy_line_variants ... ok
test task_status_hooks::dependency_lines::reconcile_dependency_chain_settles_in_one_run ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw2_inserts_adopted_line_after_cancel_log ... ok
test task_status_hooks::blocks::br19_prj_lists_only_the_project_task ... ok
test task_status_hooks::relations::mn_human_output_includes_mention_counts ... ok
test task_status_hooks::blocks::br27_second_run_is_idempotent ... ok
test task_status_hooks::relations::mn_invalid_mentions_switch_uses_enabled_default ... ok
test task_status_hooks::blocked::reconcile_pdf1_databricks_ref_residents ... ok
test task_status_hooks::blocks::br5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_terminal_failure_and_exit_status ... ok
test task_status_hooks::retry::task_status_hooks_defers_when_maintenance_lock_is_held ... ok
test task_status_hooks::dependency_lines::reconcile_does_not_read_child_links_as_dependencies ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_creates_no_lock_or_recovery ... ok
test task_status_hooks::retry::task_status_hooks_dry_run_ignores_retry_timeout ... ok
test task_status_hooks::dependency_lines::reconcile_drops_stale_field_id ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw5_label_only_line_with_adoptable_id_deletes_line_and_field ... ok
test task_status_hooks::retry::task_status_hooks_rejects_invalid_retry_timeout ... ok
test task_status_hooks::dependency_lines::reconcile_field_writer_handles_trailing_tags ... ok
test task_status_hooks::blocks::br1_same_note_insert ... ok
test task_status_hooks::consume::reconcile_does_not_reraise_hand_set_ready_after_blocked_consume ... ok
test task_status_hooks::dependency_line_writes::reconcile_dw3_dw6_rewrite_keeps_link_order ... ok
test task_status_hooks::retry::task_status_hooks_live_noop_may_lock_but_creates_no_recovery ... ok
test task_status_hooks::dependency_lines::reconcile_ignores_archive_children_outside_the_depends_on_line ... ok
test task_status_hooks::settle::settle_human_output_names_events ... ok
test task_status_hooks::consume::reconcile_consumes_blocked_resident_links_and_keeps_the_entry ... ok
test task_status_hooks::dependency_lines::reconcile_keeps_archive_prerequisite_silently ... ok
test task_status_hooks::dependency_lines::reconcile_projects_line_into_field_and_stamps_target_id ... ok
test task_status_hooks::relations::lr22_archived_source_keeps_done_form ... ok
test task_status_hooks::dependency_lines::reconcile_removes_empty_line_and_leaves_malformed_alone ... ok
test task_status_hooks::relations::lr7_done_and_previous_daily_targets_never_written ... ok
test task_status_hooks::dependency_lines::reconcile_same_index_insert_does_not_clobber_replace ... ok
test task_status_hooks::blocked::task_status_hooks_reconciles_future_schedules_and_combined_blocking_reasons ... ok
test task_status_hooks::structure::task_status_hooks_resolves_archive_references_read_only ... ok
test task_status_hooks::consume::consumption_promoted_daily_note_prerequisite_may_clear_next_run ... ok
test task_status_hooks::subprojects::blocked_subproject_links_are_consumed_and_promote_ancestor_prerequisites ... ok
test task_status_hooks::dependency_lines::reconcile_heals_moved_link ... ok
test task_status_hooks::dependency_lines::reconcile_unblocks_when_last_open_prerequisite_leaves ... ok
test task_status_hooks::dependency_lines::reconcile_breadcrumb_heals_when_target_returns ... ok
test task_status_hooks::blocks::br8_prj_order_then_projects_sync_is_noop ... ok
test task_status_hooks::subprojects::descendant_project_targets_stay_unprojected_and_warn ... ok
test task_status_hooks::blocks::br3_one_line_sorted_across_notes ... ok
test task_status_hooks::blocks::br2_unique_and_ambiguous_basename_links ... ok
test task_status_hooks::subprojects::project_parent_cycles_warn_once_and_only_inherit_other_projects_reasons ... ok
test task_status_hooks::subprojects::inherited_edges_participate_in_r7_cycle_detection ... ok
test task_status_hooks::subprojects::projects_sync_ignores_cascade_tags_and_keeps_marker_state ... ok
test task_status_hooks::dependency_lines::reconcile_warns_non_task_and_self_links_without_projecting ... ok
test task_status_hooks::sync::task_status_hooks_nulls_plan_budget_on_invalid_config ... ok
test task_status_hooks::subprojects::reconcile_recovers_subprojects_and_keeps_nearest_remaining_reason ... ok
test task_status_hooks::subprojects::reconcile_cascades_reasons_and_tags_through_multiple_project_levels ... ok
test task_status_hooks::subprojects::reconciled_cascade_tree_has_no_second_run_changes ... ok
test task_status_hooks::blocks::br23_hide_ref_inbox_and_daily_are_listed ... ok
test task_status_hooks::relations::lr10_noncanonical_line_is_canonicalized ... ok
test task_status_hooks::settle::settle_fully_covered_cluster_does_nothing ... ok
test task_status_hooks::settle::settle_back_to_back_cluster_and_trims_around_on_clock ... ok
test task_status_hooks::dependency_lines::reconcile_stamps_cross_note_target_id ... ok
test task_status_hooks::structure::task_status_hooks_composes_daily_status_and_structural_edits ... ok
test task_status_hooks::structure::task_status_hooks_drops_carried_link_already_in_completed_fallback ... ok
test task_status_hooks::settle::settle_ignores_cancelled_done_unlinked_and_on_clock_events ... ok
test task_status_hooks::sync::task_status_hooks_reports_grouping_warnings_without_noop_text ... ok
test task_status_hooks::structure::task_status_hooks_guard_rails_leave_tasks_unchanged ... ok
test task_status_hooks::sync::task_status_hooks_reports_plan_budget_in_json_and_human ... ok
test task_status_hooks::structure::task_status_hooks_keeps_archive_out_of_active_dependency_sync ... ok
test task_status_hooks::settle::settle_inherited_off_clock_event_settles_once_and_on_stays_open ... ok
test task_status_hooks::settle::settle_single_ended_off_clock_event ... ok
test task_status_hooks::structure::task_status_hooks_strikes_in_place_when_no_relocation_target_exists ... ok
test task_status_hooks::relations::lr13_malformed_links_never_newly_added ... ok
test task_status_hooks::relations::lr15_duplicate_linked_from_lines_deduplicated ... ok
test task_status_hooks::structure::task_status_hooks_uses_custom_done_status_and_completed_fallback ... ok
test task_status_hooks::settle::settle_running_on_clock_session_trims_and_mixed_placeholder_keeps_future ... ok
test task_status_hooks::structure::task_status_hooks_removes_empty_pomodoros_and_reports_them ... ok
test task_status_hooks::sync::reconcile_status_only_flips_skip_quiet_period_but_structural_edits_wait ... ok
test task_status_hooks::settle::settled_meet_children_follow_the_note_indent_unit ... ok
test task_status_hooks::structure::task_status_hooks_normalizes_live_archive_terminal_references ... ok
test task_status_hooks::sync::task_status_hooks_prunes_duplicate_lines_before_dependency_sync ... ok
test task_status_hooks::retry::task_status_hooks_exhausts_retry_budget_and_still_fails ... ok
test task_status_hooks::retry::task_status_hooks_json_retry_progress_stays_off_stdout ... ok
test task_status_hooks::retry::task_status_hooks_human_retry_progress_goes_to_stdout ... ok
test projects::schedule::projects_sync_then_task_status_hooks_blocks_and_recovers_propagated_tasks ... ok
test task_status_hooks::blocks::br11_reopened_owner_is_reprojected ... ok
test task_status_hooks::blocks::br9_last_dependent_close_removes_line ... ok
test task_status_hooks::relations::lr19_symmetric_edges ... ok
test task_status_hooks::relations::lr20_dry_run_matches_apply_rows_without_writing ... ok
test task_status_hooks::relations::lr3_sorted_sources_include_done ... ok
test task_status_hooks::relations::lr2_labelled_edge ... ok
test task_status_hooks::relations::lr24_prj_target_gets_the_mirror ... ok
test task_status_hooks::retry::task_status_hooks_cron_redirection_captures_retry_and_final_result ... ok
test task_status_hooks::relations::lr4_mints_source_id ... ok
test task_status_hooks::relations::lr6_closed_target_still_mirrored ... ok
test task_status_hooks::relations::lr8_done_and_previous_daily_sources_are_listed ... ok
test task_status_hooks::relations::lr1_same_note_insert ... ok
test task_status_hooks::relations::lr9_hand_added_and_deleted_entries ... ok
test task_status_hooks::relations::mention_and_relation_mint_reports_relation_reason ... ok
test task_status_hooks::relations::mention_only_owner_with_mentions_off_loses_only_mention_entries ... ok
test task_status_hooks::relations::lr5_quiet_interval_skips_mint_until_next_run ... ok
test task_status_hooks::blocks::br26_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::relations::mn1_json_reports_mention_subset_and_edges ... ok
test task_status_hooks::relations::mn8_relation_wins_over_mention ... ok
test task_status_hooks::relations::mn9_dependency_suppresses_mention_but_not_relation ... ok
test task_status_hooks::blocked::reconcile_derives_project_blocking_tag_and_unblocked ... ok
test task_status_hooks::relations::mn11_mints_idless_source_with_mention_reason ... ok
test task_status_hooks::structure::task_status_hooks_removes_canceled_open_pomodoro_references ... ok
test task_status_hooks::sync::reconcile_raises_ready_with_keeps_to_next_without_keeps ... ok
test task_status_hooks::relations::lr16_kill_switch_removes_writable_lines_and_skips_mints ... ok
test task_status_hooks::relations::lr11_rebuilds_identical_bytes_after_delete ... ok
test task_status_hooks::structure::task_status_hooks_resolves_duplicate_fragments_by_explicit_note_path ... ok
test task_status_hooks::sync::task_status_hooks_un_decorates_legacy_groups_holding_only_ready ... ok
test task_status_hooks::sync::task_status_hooks_uses_latest_previous_daily_for_scoped_in_progress_tasks ... ok
test task_status_hooks::sync::task_status_hooks_propagates_strongest_rank_and_reports_in_progress_promotions ... ok
test task_status_hooks::sync::task_status_hooks_syncs_fixture_and_is_idempotent ... ok
test task_status_hooks::relations::mn14_rebuilds_identical_bytes_after_deleting_mention_lines ... ok
test task_status_hooks::relations::mn17_mention_writes_are_inert ... ok
test task_status_hooks::relations::mn13_mentions_off_drops_only_mention_entries ... ok
test task_status_hooks::relations::lr18_inert_statuses_and_fields ... ok
test task_status_hooks::sync::task_status_hooks_groups_area_project_tasks_after_final_statuses ... ok
test task_status_hooks::relations::mn_fixture_reconcile_mirrors_and_mints ... ok

test result: ok. 178 passed; 0 failed; 0 ignored; 0 measured; 2980 filtered out; finished in 27.07s


⚙️  DOCS GENERATE
────────────────────────────────────────────────
BOB_UPDATE_GOLDENS=1 cargo test --test cli docs_reference
    Finished `test` profile [unoptimized + debuginfo] target(s) in 0.11s
     Running tests/cli/main.rs (/home/bryan/.cache/sase/tmp/cargo-targets/gh_bobs-org__bob-cli-ws29-261105_103612/build/debug/deps/cli-862b59fffc4caf66)

running 1 test
test docs_reference::cli_reference_is_current ... ok

test result: ok. 1 passed; 0 failed; 0 ignored; 0 measured; 3157 filtered out; finished in 0.74s

uv run --project tools/docs bob-docs gen
Generated inventory for 8 plugins and 111 registered commands.
Verification exit codes: clippy=101 task_status_hooks=0 pomodoro_homes=0 cli=0 docs_gen=0
failed  exit=1  duration=413024ms

