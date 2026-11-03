# Chat History - ace-run (bob-cli-gh.3--mon)

- **TIMESTAMP:** 2026-11-03 12:31:36 EST
- **MODEL:** codex/gpt-6-luna
- **AGENT:** bob-cli-gh.3--mon

## Prompt

sase monitor start --command 'just all && just docs-check' --reason 'Run bob-cli full checks for the period report phase'

## Response

sase tool run 02125131c1e310c090ec71d92a2360f3

🎨  FORMAT
────────────────────────────────────────────────
cargo fmt --all -- --check

🔍  LINT
────────────────────────────────────────────────
cargo clippy --workspace --all-targets --all-features -- -D unused -A unused_extern_crates -A unused_macro_rules -D private_interfaces -D clippy::bind_instead_of_map -D clippy::bool_assert_comparison -D clippy::bool_comparison -D clippy::chars_next_cmp -D clippy::clone_on_copy -D clippy::cmp_owned -D clippy::collapsible_else_if -D clippy::collapsible_if -D clippy::collapsible_match -D clippy::collapsible_str_replace -D clippy::comparison_to_empty -D clippy::derivable_impls -D clippy::double_comparisons -D clippy::explicit_auto_deref -D clippy::extend_with_drain -D clippy::filter_map_bool_then -D clippy::for_kv_map -D clippy::items_after_test_module -D clippy::iter_cloned_collect -D clippy::len_zero -D clippy::let_and_return -D clippy::manual_contains -D clippy::manual_ignore_case_cmp -D clippy::manual_is_multiple_of -D clippy::manual_pattern_char_comparison -D clippy::manual_range_patterns -D clippy::manual_rem_euclid -D clippy::manual_unwrap_or -D clippy::map_identity -D clippy::needless_as_bytes -D clippy::needless_borrow -D clippy::needless_borrows_for_generic_args -D clippy::needless_option_as_deref -D clippy::needless_return -D clippy::op_ref -D clippy::print_literal -D clippy::question_mark -D clippy::redundant_closure -D clippy::single_char_add_str -D clippy::single_element_loop -D clippy::single_match -D clippy::unnecessary_lazy_evaluations -D clippy::unnecessary_map_or -D clippy::unnecessary_to_owned -D clippy::useless_concat -D clippy::useless_conversion -D clippy::useless_format -D clippy::while_let_on_iterator
    Checking bitflags v2.12.1
    Checking bob-obsidian-assets v0.1.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/crates/bob-obsidian-assets)
    Checking powerfmt v0.2.0
    Checking linux-raw-sys v0.12.1
    Checking num-conv v0.2.2
    Checking time-core v0.1.9
    Checking deranged v0.5.8
    Checking quick-xml v0.41.0
    Checking fallible-streaming-iterator v0.1.9
    Checking base64 v0.22.1
    Checking fastrand v2.5.0
    Checking fallible-iterator v0.3.0
    Checking once_cell v1.21.4
   Compiling libsqlite3-sys v0.38.1
    Checking hashlink v0.12.1
    Checking png v0.18.1
    Checking lopdf v0.40.0
    Checking rustix v1.1.5
    Checking time v0.3.53
    Checking image v0.25.10
    Checking tempfile v3.27.0
    Checking plist v1.10.0
    Checking bob-obsidian v0.4.0 (/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20)
    Checking rusqlite v0.40.1
warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/ledger.rs:563:12
    |
563 |         if child_end >= entry_line_index + 1 {
    |            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `child_end > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one
    = note: `#[warn(clippy::int_plus_one)]` on by default

warning: unnecessary `>= y + 1` or `x - 1 >=`
   --> src/native/capture_task_toggle/links.rs:383:20
    |
383 |                 && entry.line - 1 >= entry_line_index
    |                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: change it to: `entry.line > entry_line_index`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#int_plus_one

warning: this `else` branch is empty
  --> src/native/task_cancel/prune.rs:94:15
   |
94 |               } else {
   |  _______________^
95 | |             }
   | |_____________^ help: you can remove it
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_else
   = note: `#[warn(clippy::needless_else)]` on by default

warning: `format!` in `println!` args
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
    = note: `#[warn(clippy::format_in_format_args)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:58:10
   |
58 |     ) -> Result<bool, CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err
   = note: `#[warn(clippy::result_large_err)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:66:10
   |
66 |     ) -> Result<String, CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:80:10
   |
80 |     ) -> Result<Option<String>, CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/batch.rs:95:10
   |
95 |     ) -> Result<Option<String>, CaptureError> {
   |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:148:10
    |
148 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:167:10
    |
167 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:251:10
    |
251 |     ) -> Result<usize, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/batch.rs:295:6
    |
295 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:38:6
   |
38 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocked_tasks.rs:91:6
   |
91 | ) -> Result<DependentRef, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:226:6
    |
226 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:253:6
    |
253 | ) -> Result<Vec<PlannedDependencyUpdate>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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
    = note: `#[warn(clippy::too_many_arguments)]` on by default

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/blocks_mirror.rs:52:6
   |
52 | ) -> Result<Option<(BlocksLineUpdateJson, TaskBlockRef)>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:237:6
    |
237 | ) -> Result<TaskBlockRef, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:266:6
    |
266 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocks_mirror.rs:293:6
    |
293 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/budget.rs:256:6
    |
256 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:780:10
    |
780 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:822:22
    |
822 |                   .map(|values| {
    |  ______________________^
823 | |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
824 | |                 })
    | |_________________^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:823:32
    |
823 |                     values.map(|raw| parse_inbox_route_pick(raw)).collect()
    |                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:831:22
    |
831 |                 .map(|raw| parse_pull_in_picks(raw))
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:846:6
    |
846 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:860:6
    |
860 | ) -> Result<PullInPicks, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:896:6
    |
896 | ) -> Result<InboxRoutePick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:925:6
    |
925 | ) -> Result<Option<SubBulletTarget>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/cli.rs:936:14
    |
936 |         .map(|task_ref| parse_task_ref(task_ref).map(Some))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:943:6
    |
943 | ) -> Result<SubBulletTarget, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/cli.rs:956:6
    |
956 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1005:6
     |
1005 | ) -> Result<Option<String>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/cli.rs:1036:6
     |
1036 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:26:6
   |
26 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/commit.rs:42:6
   |
42 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:125:6
    |
125 | ) -> Result<Vec<PathBuf>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:170:6
    |
170 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:215:6
    |
215 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:391:6
    |
391 | ) -> Result<PathBuf, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/commit.rs:460:45
    |
460 | pub(super) fn read_target(target: &Path) -> Result<String, CaptureError> {
    |                                             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
  --> src/native/capture/dependencies.rs:65:19
   |
65 |       close_policy: OnceLock<(
   |  ___________________^
66 | |         Vec<config::relations::CancelLabel>,
67 | |         Vec<config::relations::CompleteLabel>,
68 | |         Vec<config::relations::CancelLabel>,
69 | |         Option<String>,
70 | |     )>,
   | |______^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity
   = note: `#[warn(clippy::type_complexity)]` on by default

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1021:6
     |
1021 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1187:6
     |
1187 | ) -> Result<PathBuf, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1304:6
     |
1304 | ) -> Result<&'a note_tasks::NoteTask, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1356:6
     |
1356 | ) -> Result<(String, Option<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1467:6
     |
1467 | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/dependencies.rs:1458:1
     |
1458 | / fn resolve_prerequisites(
1459 | |     ctx: &DependencyContext,
1460 | |     planner: &mut CaptureBatchPlanner,
1461 | |     bob_dir: &Path,
...    |
1466 | |     dependent_desc: &str,
1467 | | ) -> Result<(Vec<ResolvedPrerequisite>, usize, Vec<TargetTouch>), CaptureError>
     | |_______________________________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1557:10
     |
1557 |     ) -> Result<Self, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:1800:24
     |
1800 |         let mut stack: Vec<((String, String), Vec<(String, String)>)> =
     |                        ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:1889:6
     |
1889 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2030:6
     |
2030 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2051:6
     |
2051 | ) -> Result<Vec<TaskBlockRef>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2064:6
     |
2064 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2089:6
     |
2089 | ) -> Result<Vec<TargetTouch>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2179:6
     |
2179 | ) -> Result<Option<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2359:6
     |
2359 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture/dependencies.rs:2359:6
     |
2359 | ) -> Result<(Vec<MergedMember>, BTreeSet<(String, String)>, bool), CaptureError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:2568:6
     |
2568 | ) -> Result<PlannedDependencyUpdate, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3074:6
     |
3074 | ) -> Result<(AugmentedNewTask, PlannedDependencyUpdateParts), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3338:6
     |
3338 | ) -> Result<TaskBlockRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/dependencies.rs:3396:6
     |
3396 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:42:6
   |
42 | ) -> Result<ResolvedLinkGuard, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/dependency_drop.rs:79:6
   |
79 | ) -> Result<DropAttempt, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/ensure_next.rs:23:6
   |
23 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/event_conflict.rs:287:1
    |
287 | / pub(super) fn detect_event_conflict(
288 | |     contents: &str,
289 | |     date: NaiveDate,
290 | |     session_name: Option<&str>,
...   |
295 | |     fit: &FitKind,
296 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
   --> src/native/capture/event_conflict.rs:311:1
    |
311 | / pub(super) fn detect_event_conflict_with<V: CloseVault + ?Sized>(
312 | |     contents: &str,
313 | |     date: NaiveDate,
314 | |     session_name: Option<&str>,
...   |
321 | |     day_relative: Option<&Path>,
322 | | ) -> Option<EventConflictJson> {
    | |______________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/existing_task_link.rs:57:6
   |
57 | ) -> Result<ExistingTaskLinkOutcome, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:141:6
    |
141 | ) -> Result<InboxRouteReport, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/inbox_route.rs:342:6
    |
342 | ) -> Result<AppliedInboxRoutes, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/inbox_route.rs:1131:6
     |
1131 | ) -> Result<VaultSnapshot, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/inbox_route.rs:1173:6
     |
1173 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:327:6
    |
327 | ) -> Result<LinkGuardVerdict, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:597:6
    |
597 | ) -> Result<Option<ConsumePlan>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/link_guard.rs:709:6
    |
709 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:203:6
    |
203 | ) -> Result<i64, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:533:6
    |
533 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:580:6
    |
580 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:599:6
    |
599 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/meet_event_run.rs:804:6
    |
804 | ) -> Result<Option<MeetFinish>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (11/7)
   --> src/native/capture/output.rs:442:5
    |
442 | /     pub(super) fn from_items(
443 | |         items: Vec<CaptureItemResult>,
444 | |         global_destination: Option<GlobalDestinationSummary>,
445 | |         template: Option<capture_language::template::TemplateSummary>,
...   |
453 | |         inbox_route: InboxRouteReport,
454 | |     ) -> Self {
    | |_____________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:53:6
   |
53 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/plan.rs:61:6
   |
61 | ) -> Result<PlannedCaptureBatch, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:435:6
    |
435 | ) -> Result<(PlannedCaptureItem, Option<ref_jobs::NewJob>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:638:6
    |
638 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/plan.rs:742:6
    |
742 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (11/7)
   --> src/native/capture/plan.rs:730:1
    |
730 | / pub(super) fn plan_capture_item(
731 | |     request: &CaptureRequest,
732 | |     parsed_item: ParsedCaptureItem,
733 | |     now: chrono::NaiveDateTime,
...   |
741 | |     task_theme_context: &mut CaptureTaskThemeContext,
742 | | ) -> Result<PlannedCaptureItem, CaptureError> {
    | |_____________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:1337:14
     |
1337 |         .map(|offset| scheduled_date_string(today, offset))
     |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
    --> src/native/capture/plan.rs:1513:11
     |
1513 |     .then(|| child_indent_unit(planner, &target))
     |           ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2594:6
     |
2594 | ) -> Result<Vec<AuthoredSubBullet>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2700:6
     |
2700 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2729:6
     |
2729 | ) -> Result<ResolvedPriority, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2815:6
     |
2815 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:2856:6
     |
2856 | ) -> Result<DependentRef, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/plan.rs:3037:6
     |
3037 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: usage of `&String::new()` for a function expecting a `&str` argument
    --> src/native/capture/plan.rs:3497:13
     |
3497 |             &String::new(),
     |             ^^^^^^^^^^^^^^ help: try: `""`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_owned_empty_strings
     = note: `#[warn(clippy::unnecessary_owned_empty_strings)]` on by default

warning: the `Err`-variant returned from this function is very large
 --> src/native/capture/pomodoro_adjust.rs:8:6
  |
8 | ) -> Result<(), CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:24:6
   |
24 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_adjust.rs:62:6
   |
62 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:131:6
    |
131 | ) -> Result<RunningSessionTarget, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:215:6
    |
215 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:271:6
    |
271 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_adjust.rs:505:6
    |
505 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:582:6
    |
582 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:627:6
    |
627 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_close.rs:810:6
    |
810 | ) -> Result<CloseSuccessorOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1309:6
     |
1309 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1345:6
     |
1345 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1500:6
     |
1500 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1668:6
     |
1668 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:1825:6
     |
1825 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2104:6
     |
2104 | ) -> Result<(String, Placement), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2180:6
     |
2180 | ) -> Result<RunningLinkOutcome, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2293:6
     |
2293 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_close.rs:2825:6
     |
2825 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_insert.rs:56:6
   |
56 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:127:6
    |
127 | ) -> Result<PomodoroBlockLinkInsertion, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:264:6
    |
264 | ) -> Result<DefaultPomodoroPick, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:356:6
    |
356 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:468:6
    |
468 | ) -> Result<NamedPomodoroResolution<'a>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:499:6
    |
499 | ) -> Result<(String, Placement, usize, String), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_insert.rs:572:6
    |
572 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_link.rs:18:6
   |
18 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:230:6
    |
230 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:286:6
    |
286 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:707:6
    |
707 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:792:6
    |
792 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_link.rs:965:6
    |
965 | ) -> Result<(String, Option<MeetFinish>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1010:6
     |
1010 | ) -> Result<CaptureWritePlan, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_link.rs:1802:6
     |
1802 | ) -> Result<&str, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_merge.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `index` is only used to index `lines`
  --> src/native/capture/pomodoro_merge.rs:94:18
   |
94 |     for index in (entry_index + 1)..=end {
   |                  ^^^^^^^^^^^^^^^^^^^^^^^
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
   = note: `#[warn(clippy::needless_range_loop)]` on by default
help: consider using an iterator
   |
94 -     for index in (entry_index + 1)..=end {
94 +     for <item> in lines.iter().take(end + 1).skip((entry_index + 1)) {
   |

warning: the loop variable `index` is used to index `lines`
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:250:6
    |
250 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:448:6
    |
448 | ) -> Result<ResolvedMerge, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_merge.rs:664:6
    |
664 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_split.rs:14:6
   |
14 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the loop variable `index` is only used to index `lines`
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

warning: the loop variable `index` is used to index `lines`
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_split.rs:295:6
    |
295 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:17:6
   |
17 | ) -> Result<(String, String, u64, String), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pomodoro_start.rs:52:6
   |
52 |   ) -> Result<
   |  ______^
53 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
54 | |     CaptureError,
55 | | > {
   | |_^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:105:6
    |
105 |   ) -> Result<
    |  ______^
106 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
107 | |     CaptureError,
108 | | > {
    | |_^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:423:6
    |
423 |   ) -> Result<
    |  ______^
424 | |     (String, Placement, PomodoroStartSummary, PomodoroBlockBefore),
425 | |     CaptureError,
426 | | > {
    | |_^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:516:6
    |
516 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:568:6
    |
568 | ) -> Result<(String, Placement), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:627:6
    |
627 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:646:6
    |
646 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:804:6
    |
804 | ) -> Result<(String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:816:6
    |
816 | ) -> Result<(String, Placement, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:861:6
    |
861 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pomodoro_start.rs:887:6
    |
887 | ) -> Result<PlannedCaptureItem, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1182:6
     |
1182 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:1437:6
     |
1437 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2073:6
     |
2073 | ) -> Result<(), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2176:6
     |
2176 | ) -> Result<String, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2241:6
     |
2241 | ) -> Result<(String, usize, Vec<usize>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/pomodoro_start.rs:2411:6
     |
2411 | ) -> Result<PlannedCaptureItem, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:105:6
    |
105 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:292:6
    |
292 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:311:6
    |
311 | ) -> Result<LiveLinkConsumption, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/project_deps.rs:512:6
    |
512 | ) -> Result<Vec<PomodoroBlockRef>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
 --> src/native/capture/project_note.rs:7:6
  |
7 | ) -> Result<(), CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:25:6
   |
25 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/project_note.rs:67:6
   |
67 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this closure is very large
   --> src/native/capture/project_note.rs:133:14
    |
133 |         .map(|offset| scheduled_date_string(today, offset))
    |              ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:1003:6
     |
1003 | ) -> Result<(String, Vec<PlacedProjectLink>), CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/pull_in.rs:11:6
   |
11 | ) -> Result<(PlannedCaptureBatch, PullInJson), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/pull_in.rs:253:6
    |
253 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relation_sources.rs:55:6
   |
55 | ) -> Result<Option<RelationSourceRead>, super::CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relation_sources.rs:364:6
    |
364 | ) -> Result<(), super::CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:164:6
    |
164 | ) -> Result<PlannedRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:225:10
    |
225 |     ) -> Result<Self, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:254:6
    |
254 | ) -> Result<RelationOwner, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:314:6
    |
314 | ) -> Result<ResolvedRelation, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:391:6
    |
391 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:416:6
    |
416 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:460:6
    |
460 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:494:6
    |
494 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:570:6
    |
570 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:666:6
    |
666 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:715:6
    |
715 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:807:6
    |
807 | ) -> Result<(RelationAction, Option<String>, String, usize), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations.rs:915:1
    |
915 | / fn relation_update_json(
916 | |     direction: RelationDirection,
917 | |     source_relative: &Path,
918 | |     source_line: usize,
...   |
923 | |     previous_label: Option<String>,
924 | | ) -> RelationUpdateJson {
    | |_______________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations.rs:959:6
    |
959 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_cancel.rs:36:6
   |
36 | ) -> Result<Vec<RelationCancelJson>, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:112:6
    |
112 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:148:6
    |
148 | ) -> Result<Option<RelationCancelJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_cancel.rs:383:6
    |
383 | ) -> Result<Vec<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:229:6
    |
229 | ) -> Result<ItemRelationReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture/relations_close.rs:220:1
    |
220 | / pub(super) fn plan_item_relations(
221 | |     ctx: &mut DependencyContext,
222 | |     planner: &mut CaptureBatchPlanner,
223 | |     request: &CaptureRequest,
...   |
228 | |     warnings: &mut Vec<CaptureWarning>,
229 | | ) -> Result<ItemRelationReports, CaptureError> {
    | |______________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:267:6
    |
267 | ) -> Result<RelationCloseReports, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_close.rs:442:6
    |
442 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_complete.rs:38:6
   |
38 | ) -> Result<RelationCompleteReports, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:144:6
    |
144 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_complete.rs:180:6
    |
180 | ) -> Result<Option<PlannedSourceComplete>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/relations_mentions.rs:53:6
   |
53 | ) -> Result<(), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:460:6
    |
460 | ) -> Result<Option<(usize, String)>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:507:6
    |
507 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:547:6
    |
547 | ) -> Result<Option<MirrorSkipReason>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:579:6
    |
579 | ) -> Result<Option<String>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mentions.rs:693:6
    |
693 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:153:6
    |
153 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:268:6
    |
268 | ) -> Result<Option<BlocksLineUpdateJson>, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:405:6
    |
405 | ) -> Result<bool, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/relations_mirror.rs:434:6
    |
434 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:46:6
   |
46 | ) -> Result<capture_language::ParsedCaptureDraft, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
 --> src/native/capture/sub_bullet.rs:8:6
  |
8 | ) -> Result<CaptureWritePlan, CaptureError> {
  |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
  |
  = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
  = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sub_bullet.rs:50:6
   |
50 | ) -> Result<CaptureWritePlan, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:385:6
    |
385 | ) -> Result<CaptureWritePlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
   --> src/native/capture/sub_bullet.rs:375:1
    |
375 | / fn plan_prj_section_capture(
376 | |     planner: &mut CaptureBatchPlanner,
377 | |     bob_dir: &Path,
378 | |     target: &Path,
...   |
384 | |     warnings: &mut Vec<CaptureWarning>,
385 | | ) -> Result<CaptureWritePlan, CaptureError> {
    | |___________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/sub_bullet.rs:698:6
    |
698 | ) -> Result<String, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_complete.rs:49:6
   |
49 | ) -> Result<PlannedCaptureItem, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:166:6
    |
166 | ) -> Result<CompleteExistingTaskOutcome, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_complete.rs:915:6
    |
915 | ) -> Result<(), CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_complete.rs:1182:6
     |
1182 | ) -> Result<Vec<(PathBuf, String)>, CaptureError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:147:10
    |
147 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:187:10
    |
187 |     ) -> Result<AppliedTaskTheme, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:293:10
    |
293 |     ) -> Result<(), CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:307:10
    |
307 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
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

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:338:10
    |
338 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:478:10
    |
478 |     ) -> Result<ExistingTypeMarkerApplication, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:601:10
    |
601 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:644:10
    |
644 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:777:10
    |
777 |     ) -> Result<Option<AppliedLanding>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:824:10
    |
824 |     ) -> Result<Option<usize>, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_theme.rs:881:10
    |
881 |     ) -> Result<String, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1108:10
     |
1108 |     ) -> Result<Option<AppliedMerge>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/task_theme.rs:1172:10
     |
1172 |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
    --> src/native/capture/task_theme.rs:1163:5
     |
1163 | /     pub(super) fn relocate_for_retype(
1164 | |         &mut self,
1165 | |         planner: &mut CaptureBatchPlanner,
1166 | |         block_id: &str,
...    |
1171 | |         warnings: &mut Vec<CaptureWarning>,
1172 | |     ) -> Result<Option<AppliedRelocation>, CaptureError> {
     | |________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/task_toggle.rs:19:6
   |
19 | ) -> Result<(CaptureWritePlan, Option<LinkGuardJson>), CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/task_toggle.rs:447:6
    |
447 | ) -> Result<ToggleRelationPlan, CaptureError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/mod.rs:305:44
    |
305 | fn capture(mut request: CaptureRequest) -> Result<CaptureResult, CaptureError> {
    |                                            ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
   --> src/native/capture_active_tasks.rs:331:12
    |
331 |     tasks: &mut Vec<ActiveTask>,
    |            ^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#ptr_arg
    = note: `#[warn(clippy::ptr_arg)]` on by default
help: change this to
    |
331 -     tasks: &mut Vec<ActiveTask>,
331 +     tasks: &mut [ActiveTask],
    |

warning: this function has too many arguments (9/7)
   --> src/native/capture_complete/candidates.rs:670:1
    |
670 | / fn relationship_disabled_reason(
671 | |     bob_dir: &Path,
672 | |     discovered: &capture_dependency_tasks::DependencyTaskResult,
673 | |     graph: &HashMap<
...   |
682 | |     blocked_tasks: &[ResolvedRelationshipEntry],
683 | | ) -> Option<String> {
    | |___________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/capture_complete/candidates.rs:1302:6
     |
1302 |   ) -> (
     |  ______^
1303 | |     HashMap<capture_dependency_tasks::TaskIdentity, TaskLinks>,
1304 | |     Vec<String>,
1305 | |     Vec<(String, usize)>,
1306 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
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

warning: this boolean expression can be simplified
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
    = note: `#[warn(clippy::nonminimal_bool)]` on by default
help: try
    |
261 ~             || row
262 +                 .name
263 +                 .as_deref().is_none_or(|name| normalize_component(name) != key)
    |

warning: the loop variable `idx` is used to index `lines`
   --> src/native/capture_drawers.rs:665:16
    |
665 |     for idx in start_idx..end_idx.min(lines.len()) {
    |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
665 -     for idx in start_idx..end_idx.min(lines.len()) {
665 +     for (idx, <item>) in lines.iter().enumerate().take(end_idx.min(lines.len())).skip(start_idx) {
    |

warning: the following explicit lifetimes could be elided: 'a
   --> src/native/capture_drawers.rs:898:35
    |
898 | pub(crate) fn rank_drawer_catalog<'a>(
    |                                   ^^
899 |     records: &'a BTreeMap<String, DrawerCatalogRecord>,
    |               ^^
900 | ) -> Vec<&'a DrawerCatalogRecord> {
    |           ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_lifetimes
    = note: `#[warn(clippy::needless_lifetimes)]` on by default
help: elide the lifetimes
    |
898 ~ pub(crate) fn rank_drawer_catalog(
899 ~     records: &BTreeMap<String, DrawerCatalogRecord>,
900 ~ ) -> Vec<&DrawerCatalogRecord> {
    |

warning: called `filter(..).next_back()` on an `DoubleEndedIterator`. This is more succinctly expressed by calling `.rfind(..)` instead
    --> src/native/capture_drawers.rs:1474:5
     |
1474 | /     direct_child_list_indexes(&lines, drawer.line_index(), drawer.block_end)
1475 | |         .into_iter()
1476 | |         .filter(|&index| line_start(&lines, index) < insertion.offset)
1477 | |         .filter(|&index| {
1478 | |             parse_managed_task_log_marker(lines[index].text).is_none()
1479 | |         })
1480 | |         .next_back()
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#filter_next
     = note: `#[warn(clippy::filter_next)]` on by default

warning: redundant guard
   --> src/native/capture_language/close_log.rs:213:23
    |
213 |         Some(list) if list.is_empty() => {
    |                       ^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
    = note: `#[warn(clippy::redundant_guards)]` on by default
help: try
    |
213 -         Some(list) if list.is_empty() => {
213 +         Some([]) => {
    |

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: casting to the same type is unnecessary (`usize` -> `usize`)
    --> src/native/capture_language/completion.rs:1000:19
     |
1000 |     let mut rel = (base_end - token_start) as usize;
     |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `(base_end - token_start)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_cast
     = note: `#[warn(clippy::unnecessary_cast)]` on by default

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
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

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
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

warning: large size difference between variants
   --> src/native/capture_language/editor_model.rs:607:1
    |
607 | / pub(super) enum TokenParse {
608 | |     Marker(MarkerParse),
    | |     ------------------- the largest variant contains at least 344 bytes
609 | |     Invalid(Diagnostic),
    | |     ------------------- the second-largest variant contains at least 72 bytes
610 | | }
    | |_^ the entire enum is at least 344 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
    = note: `#[warn(clippy::large_enum_variant)]` on by default
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
608 -     Marker(MarkerParse),
608 +     Marker(Box<MarkerParse>),
    |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/editor_parse.rs:1815:1
     |
1815 | / fn attach_drawer_bullet_metadata(
1816 | |     item: &CaptureItem<'_>,
1817 | |     mode: &mut EditorMode,
1818 | |     parent_body: &str,
...    |
1823 | |     sub_bullets: &mut [AuthoredSubBullet],
1824 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: found call to `str::trim_start` before `str::split_whitespace`
    --> src/native/capture_language/editor_parse.rs:2387:35
     |
2387 |         let mut words = body_text.trim_start().split_whitespace();
     |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace
     = note: `#[warn(clippy::trim_split_whitespace)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/editor_parse.rs:2805:5
     |
2805 |     seen.clip = has_clip;
     |     ^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::editor_parse::SeenMarkers { clip: has_clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/editor_parse.rs:2804:5
     |
2804 |     let mut seen = SeenMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default
     = note: `#[warn(clippy::field_reassign_with_default)]` on by default

warning: this function has too many arguments (9/7)
   --> src/native/capture_language/editor_pomodoro.rs:290:1
    |
290 | / pub(super) fn parse_editor_named_start_item<'a>(
291 | |     item: &CaptureItem<'a>,
292 | |     parent_trimmed: &str,
293 | |     suffix: String,
...   |
299 | |     spelling: NameSpelling,
300 | | ) -> Option<EditorItemOutcome<'a>> {
    | |__________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: field assignment outside of initializer for an instance created with Default::default()
   --> src/native/capture_language/item.rs:844:5
    |
844 |     aggregate.clip = clip;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
   --> src/native/capture_language/item.rs:843:5
    |
843 |     let mut aggregate = AggregateMarkers::default();
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: found call to `str::trim_start` before `str::split_whitespace`
   --> src/native/capture_language/item.rs:731:35
    |
731 |         let mut words = body_text.trim_start().split_whitespace();
    |                                   ^^^^^^^^^^^^^ help: remove `trim_start()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#trim_split_whitespace

warning: field assignment outside of initializer for an instance created with Default::default()
    --> src/native/capture_language/item.rs:1702:5
     |
1702 |     aggregate.clip = clip;
     |     ^^^^^^^^^^^^^^^^^^^^^^
     |
note: consider initializing the variable with `native::capture_language::line::AggregateMarkers { clip: clip, ..Default::default() }` and removing relevant reassignments
    --> src/native/capture_language/item.rs:1701:5
     |
1701 |     let mut aggregate = AggregateMarkers::default();
     |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#field_reassign_with_default

warning: match expression looks like `matches!` macro
    --> src/native/capture_language/item.rs:2921:31
     |
2921 |               let want_second = match (name.is_some(), first_sigil, second) {
     |  _______________________________^
2922 | |                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
2923 | |                 (false, '~', Some(b'@')) => true,
2924 | |                 _ => false,
2925 | |             };
     | |_____________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
     = note: `#[warn(clippy::match_like_matches_macro)]` on by default
help: use `matches!` directly
     |
2921 -             let want_second = match (name.is_some(), first_sigil, second) {
2922 -                 (true, '~', Some(b'@')) | (true, '@', Some(b'~')) => true,
2923 -                 (false, '~', Some(b'@')) => true,
2924 -                 _ => false,
2925 -             };
2921 +             let want_second = matches!((name.is_some(), first_sigil, second), (true, '~', Some(b'@')) | (true, '@', Some(b'~')) | (false, '~', Some(b'@')));
     |

warning: this function has too many arguments (8/7)
    --> src/native/capture_language/item.rs:3242:1
     |
3242 | / pub(super) fn named_shape_error_with_drop(
3243 | |     token: &str,
3244 | |     suffix: &str,
3245 | |     name: &str,
...    |
3250 | |     is_literal: bool,
3251 | | ) -> String {
     | |___________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: called `expect` on `separator` after checking its variant with `is_some`
   --> src/native/capture_language/relations.rs:689:13
    |
687 |         block_end: if separator.is_some() {
    |                    ---------------------- help: try: `if let Some(<item>) = separator`
688 |             // Block ID ends where `|` starts.
689 |             separator.expect("separator").0
    |             ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap
    = note: `#[warn(clippy::unnecessary_unwrap)]` on by default

warning: this boolean expression can be simplified
   --> src/native/capture_language/rewrite.rs:433:8
    |
433 |       if !raw_text[..run_start]
    |  ________^
434 | |         .chars()
435 | |         .next_back()
436 | |         .is_some_and(|before| !before.is_whitespace())
    | |______________________________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool
help: try
    |
433 ~     if raw_text[..run_start]
434 +         .chars()
435 +         .next_back().is_none_or(|before| before.is_whitespace())
    |

warning: redundant guard
    --> src/native/capture_language/tokens.rs:1366:43
     |
1366 |                 Some((after_x, x_len)) if after_x.is_empty() => {
     |                                           ^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_guards
help: try
     |
1366 -                 Some((after_x, x_len)) if after_x.is_empty() => {
1366 +                 Some(("", x_len)) => {
     |

warning: this `if` has identical blocks
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
    = note: `#[warn(clippy::if_same_then_else)]` on by default

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
   --> src/native/capture_pomodoro_close/ledger.rs:576:24
    |
576 |       let Some(anchor) = scan
    |  ________________________^
577 | |         .entries
578 | |         .iter()
579 | |         .filter(|entry| {
...   |
582 | |         })
583 | |         .last()
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#double_ended_iterator_last
    = note: `#[warn(clippy::double_ended_iterator_last)]` on by default
help: try
    |
583 -         .last()
583 +         .next_back()
    |

warning: large size difference between variants
   --> src/native/capture_pomodoro_close/linked_tasks.rs:154:1
    |
154 | / pub(crate) enum PomodoroCloseOutcome {
155 | |     Close(PomodoroClosePlan),
    | |     ------------------------ the largest variant contains at least 688 bytes
156 | |     Reset(super::reset::ResetPlan),
    | |     ------------------------------ the second-largest variant contains at least 144 bytes
157 | | }
    | |_^ the entire enum is at least 688 bytes
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#large_enum_variant
help: consider boxing the large fields or introducing indirection in some other way to reduce the total size of the enum
    |
155 -     Close(PomodoroClosePlan),
155 +     Close(Box<PomodoroClosePlan>),
    |

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:318:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
318 |     ) -> Result<Option<String>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:365:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
365 |     ) -> Result<Option<TaskKey>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:553:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
553 |     ) -> Result<Option<NoteTask>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:570:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
570 |     ) -> Result<bool, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:590:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
590 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:613:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
613 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:676:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
676 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:749:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
749 |     ) -> Result<BTreeSet<usize>, PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:903:10
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
903 |     ) -> Result<(), PomodoroClosePlanError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture_pomodoro_close/linked_tasks.rs:981:6
    |
149 |     Selection(CloseSelectionError),
    |     ------------------------------ the largest variant contains at least 128 bytes
...
981 | ) -> Result<PomodoroCloseOutcome, PomodoroClosePlanError> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1006:6
     |
 149 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1006 | ) -> Result<PomodoroClosePlan, PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (9/7)
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1294:1
     |
1294 | / fn resolve_close_clock_fact<V: CloseVault, S: HomeSource>(
1295 | |     vault: &V,
1296 | |     resolver: &mut HomeResolver<S>,
1297 | |     events: &[EventNoteRow],
...    |
1303 | |     all_settings: &NoteTaskSettings,
1304 | | ) -> CloseClockFact {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture_pomodoro_close/linked_tasks.rs:1707:6
     |
 149 |     Selection(CloseSelectionError),
     |     ------------------------------ the largest variant contains at least 128 bytes
...
1707 | ) -> Result<(), PomodoroClosePlanError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: try reducing the size of `native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError`, for example by boxing large elements or replacing it with `Box<native::capture_pomodoro_close::linked_tasks::PomodoroClosePlanError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
   --> src/native/capture_pomodoro_start.rs:349:1
    |
349 | / fn resolve_clock_fact<V: CloseVault + ?Sized, S: HomeSource>(
350 | |     vault: Option<&V>,
351 | |     resolver: Option<&mut HomeResolver<S>>,
352 | |     events: &[EventNoteRow],
...   |
357 | |     all_settings: &note_tasks::NoteTaskSettings,
358 | | ) -> CountedLinkFact {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this `if` has identical blocks
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

warning: stripping a prefix manually
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
    = note: `#[warn(clippy::manual_strip)]` on by default
help: try using the `strip_prefix` method
    |
381 ~     if let Some(<stripped>) = rest.strip_prefix("[[") {
382 ~         let close = <stripped>.find("]]")?;
    |

warning: the following explicit lifetimes could be elided: 'a
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

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
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

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
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

warning: match expression looks like `matches!` macro
   --> src/native/gcal/bullet_block.rs:144:5
    |
144 | /     match structural_depth(spans, row_index, end) {
145 | |         Some(depth) if depth >= 2 => false,
146 | |         _ => true,
147 | |     }
    | |_____^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#match_like_matches_macro
help: use `matches!` directly
    |
144 -     match structural_depth(spans, row_index, end) {
145 -         Some(depth) if depth >= 2 => false,
146 -         _ => true,
147 -     }
144 +     !matches!(structural_depth(spans, row_index, end), Some(depth) if depth >= 2)
    |

warning: the loop variable `index` is used to index `lines`
   --> src/native/gcal/bullet_block.rs:158:18
    |
158 |     for index in start..end {
    |                  ^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_range_loop
help: consider using an iterator and enumerate()
    |
158 -     for index in start..end {
158 +     for (index, <item>) in lines.iter().enumerate().take(end).skip(start) {
    |

warning: methods called `from_*` usually take no `self`
  --> src/native/gcal/classify.rs:50:32
   |
50 |     pub(crate) fn from_rfc3339(&self) -> String {
   |                                ^^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention
   = note: `#[warn(clippy::wrong_self_convention)]` on by default

warning: this `if` has identical blocks
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

warning: this if-then-else expression returns a bool literal
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
    = note: `#[warn(clippy::needless_bool)]` on by default

warning: this `if` has identical blocks
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

warning: very complex type used. Consider factoring parts into `type` definitions
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

warning: large size difference between variants
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

warning: enclosing `Some` and `?` operator are unneeded
   --> src/native/gcal/lifecycle.rs:230:5
    |
230 |     Some(text.get(..open)?)
    |     ^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_question_mark
    = note: `#[warn(clippy::needless_question_mark)]` on by default
help: remove the enclosing `Some` and `?` operator
    |
230 -     Some(text.get(..open)?)
230 +     text.get(..open)
    |

warning: consider using `sort_by_key`
   --> src/native/gcal/login.rs:638:5
    |
638 |     paths.sort_by(|a, b| b.0.cmp(&a.0));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
    = note: `#[warn(clippy::unnecessary_sort_by)]` on by default
help: try
    |
638 -     paths.sort_by(|a, b| b.0.cmp(&a.0));
638 +     paths.sort_by_key(|b| std::cmp::Reverse(b.0));
    |

warning: replacing a value of type `T` with `T::default()` is better expressed using `std::mem::take`
  --> src/native/gcal/render.rs:83:22
   |
83 |     let mut suffix = std::mem::replace(&mut spans.suffix, String::new());
   |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `std::mem::take(&mut spans.suffix)`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#mem_replace_with_default
   = note: `#[warn(clippy::mem_replace_with_default)]` on by default

warning: this boolean expression can be simplified
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

warning: writing `&PathBuf` instead of `&Path` involves a new object where a slice will do
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

warning: the following explicit lifetimes could be elided: 'a
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

warning: consider using `sort_by_key`
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

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:1979:1
     |
1979 | / pub(super) fn stamp_overwrite_source(
1980 | |     config: &Config,
1981 | |     plan: &OverwritePreflight,
1982 | |     options: &CreateOptions,
...    |
1987 | |     info: &PdfInfo,
1988 | | ) -> Result<PathBuf> {
     | |____________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2021:1
     |
2021 | / pub(super) fn stage_overwrite_audio(
2022 | |     options: &CreateOptions,
2023 | |     plan: &OverwritePreflight,
2024 | |     request: &OverwriteRequest,
...    |
2029 | |     title: &str,
2030 | | ) -> Result<Option<StagedAudio>> {
     | |________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:2703:1
     |
2703 | / fn plan_target_for(
2704 | |     config: &Config,
2705 | |     stem: &str,
2706 | |     ref_type: &str,
...    |
2711 | |     source_display: &str,
2712 | | ) -> Result<TargetPlan> {
     | |_______________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (10/7)
    --> src/native/highlights_ref/create.rs:3711:1
     |
3711 | / fn stage_overwrite_source_store(
3712 | |     _config: &Config,
3713 | |     plan: &OverwritePreflight,
3714 | |     scratch: &Path,
...    |
3721 | |     catalog: &super::code_catalog::CatalogOutcome,
3722 | | ) -> Result<super::source_store::StagedStoreFiles> {
     | |__________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4392:1
     |
4392 | / fn overwrite_pdf_url(
4393 | |     config: &Config,
4394 | |     url: super::clip_url::WebUrl,
4395 | |     downloaded: PathBuf,
...    |
4400 | |     selection: &OverwriteSelection,
4401 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:4473:1
     |
4473 | / fn create_pdf_url_route(
4474 | |     config: &Config,
4475 | |     url: super::clip_url::WebUrl,
4476 | |     downloaded: PathBuf,
...    |
4481 | |     listen: Option<&super::listen::ListenCommand>,
4482 | | ) -> Result<()> {
     | |_______________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (11/7)
    --> src/native/highlights_ref/create.rs:5207:1
     |
5207 | / fn print_pdf_dry_run(
5208 | |     config: &Config,
5209 | |     styler: &Styler,
5210 | |     source_display: &str,
...    |
5218 | |     legacy: &[sources_mod::RecordedSource],
5219 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/highlights_ref/create.rs:5443:1
     |
5443 | / fn compose_markdown_marker(
5444 | |     status: &str,
5445 | |     parent: &str,
5446 | |     title: &str,
...    |
5451 | |     return_links: bool,
5452 | | ) -> Result<String> {
     | |___________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
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

warning: clamp-like pattern without using clamp function
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
    = note: `#[warn(clippy::manual_clamp)]` on by default
help: replace with clamp
    |
763 ~     DIAGRAM_TIMEOUT_BASE_SECS
764 +         .saturating_add(
765 +             DIAGRAM_ITEM_TIMEOUT_SECS.saturating_mul(item_count as u64),
766 +         ).clamp(1, DEFAULT_TIMEOUT_SECS)
    |

warning: large size difference between variants
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

warning: large size difference between variants
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

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (8/7)
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

warning: methods called `as_*` usually take `self` by reference or `self` by mutable reference
  --> src/native/highlights_ref/note_snapshot/classify.rs:54:32
   |
54 |     pub(crate) const fn as_str(self) -> &'static str {
   |                                ^^^^
   |
   = help: consider choosing a less ambiguous name
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#wrong_self_convention

warning: large size difference between variants
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

warning: writing `&mut Vec` instead of `&mut [_]` involves a new object where a slice will do
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

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/transclusion.rs:607:21
    |
607 |                     *block = Box::new(expanded);
    |                     ^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: replace existing content with inner value instead: `**block = expanded`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box
    = note: `#[warn(clippy::replace_box)]` on by default

warning: very complex type used. Consider factoring parts into `type` definitions
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

warning: this function has too many arguments (10/7)
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

warning: creating a new box
   --> src/native/highlights_ref/note_snapshot/visibility.rs:198:21
    |
198 | /                     *inner = Box::new(
199 | |                         nested.into_iter().next().expect("embedded block"),
200 | |                     );
    | |_____________________^ help: replace existing content with inner value instead: `**inner = nested.into_iter().next().expect("embedded block")`
    |
    = note: this creates a needless allocation
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#replace_box

warning: this function has too many arguments (8/7)
   --> src/native/highlights_ref/pdf_target.rs:128:1
    |
128 | / pub(super) fn plan_pdf_url(
129 | |     url: &WebUrl,
130 | |     downloaded: &Path,
131 | |     name_override: Option<&str>,
...   |
136 | |     progress: Option<&dyn Fn(&str)>,
137 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (9/7)
   --> src/native/highlights_ref/pdf_target.rs:213:1
    |
213 | / pub(super) fn plan_arxiv(
214 | |     paper: &ArxivPaper,
215 | |     name_override: Option<&str>,
216 | |     title_override: Option<&str>,
...   |
222 | |     progress: Option<&dyn Fn(&str)>,
223 | | ) -> Result<PdfPlan> {
    | |____________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this boolean expression can be simplified
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

warning: this boolean expression can be simplified
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (10/7)
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

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (10/7)
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

warning: this boolean expression can be simplified
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

warning: this boolean expression can be simplified
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

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (9/7)
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

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/highlights_ref/overwrite/recovery.rs:1304:16
     |
1304 |     reversals: Vec<(PathBuf, PathBuf, Option<String>, Option<String>, bool)>,
     |                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (14/7)
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

warning: this function has too many arguments (8/7)
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

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/sidecar_render.rs:308:29
    |
308 | ...                   &[member_text_key.clone()],
    |                       ^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&member_text_key)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs
    = note: `#[warn(clippy::cloned_ref_to_slice_refs)]` on by default

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (9/7)
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

warning: all variants have the same postfix: `Host`
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
   = note: `#[warn(clippy::enum_variant_names)]` on by default

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:122:5
    |
122 |     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
122 -     rows.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
122 +     rows.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: this `if` has identical blocks
   --> src/native/periods/note.rs:285:57
    |
285 |               if !name.is_empty() && !name.contains("  ") {
    |  _________________________________________________________^
286 | |                 current = Some(name);
287 | |             } else if !name.is_empty() {
    | |_____________^
    |
note: same as this
   --> src/native/periods/note.rs:287:40
    |
287 |               } else if !name.is_empty() {
    |  ________________________________________^
288 | |                 current = Some(name);
289 | |             }
    | |_____________^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#if_same_then_else

error: useless use of `format!`
  --> src/native/periods/report.rs:53:19
   |
53 |             hint: format!("Pass a period id such as 2026-W45, 2026-Q4, 2026, or all. See docs/periods.md."),
   |                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using `.to_string()`: `"Pass a period id such as 2026-W45, 2026-Q4, 2026, or all. See docs/periods.md.".to_string()`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#useless_format
   = note: requested on the command line with `-D clippy::useless-format`

error: the borrowed expression implements the required traits
    --> src/native/periods/report.rs:1040:49
     |
1040 |                 .and_then(|catalog| catalog.get(&normalize_key(&key)))
     |                                                 ^^^^^^^^^^^^^^^^^^^^ help: change this to: `normalize_key(&key)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#needless_borrows_for_generic_args
     = note: requested on the command line with `-D clippy::needless-borrows-for-generic-args`

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/periods/report.rs:1091:6
     |
1091 | ) -> Result<(Vec<Value>, Vec<Value>, Vec<Value>), ShowError> {
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (15/7)
   --> src/native/plugins/sync.rs:231:1
    |
231 | / fn apply_plugin(
232 | |     options: &SyncOptions,
233 | |     id: &str,
234 | |     captured: &CapturedPlugin,
...   |
246 | |     issues: &mut Vec<String>,
247 | | ) -> PluginSync {
    | |_______________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: consider using `sort_by_key`
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

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
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

warning: very complex type used. Consider factoring parts into `type` definitions
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

warning: this function has too many arguments (8/7)
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

warning: manual implementation of `Option::map`
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
    = note: `#[warn(clippy::manual_map)]` on by default
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

warning: manual implementation of `Option::map`
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

warning: manual implementation of `Option::map`
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

warning: manual implementation of `Option::map`
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

warning: called `Iterator::last` on a `DoubleEndedIterator`; this will needlessly iterate the entire iterator
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: called `unwrap` on `page` after checking its variant with `is_some`
   --> src/native/ref_library/code.rs:587:47
    |
586 |     if blocks.is_empty() && page.is_some() {
    |                             -------------- the check is happening here
587 |         println!("no code blocks on page {}", page.unwrap());
    |                                               ^^^^^^^^^^^^^
    |
    = help: try using `if let` or `match`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_unwrap

warning: the `Err`-variant returned from this function is very large
   --> src/native/ref_library/today.rs:351:6
    |
351 | ) -> Result<ResolvedReadingTask, TaskRefusal> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 184 bytes
    |
    = help: try reducing the size of `native::ref_library::today::TaskRefusal`, for example by boxing large elements or replacing it with `Box<native::ref_library::today::TaskRefusal>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this function has too many arguments (8/7)
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

warning: `format!` in `format!` args
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

warning: doc list item without indentation
   --> src/native/ref_library/mod.rs:919:5
    |
919 | /// Notes without a recorded id stay id-less and earn no diagnostic.
    |     ^
    |
    = help: if this is supposed to be its own paragraph, add a blank line
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#doc_lazy_continuation
    = note: `#[warn(clippy::doc_lazy_continuation)]` on by default
help: indent this line
    |
919 | ///   Notes without a recorded id stay id-less and earn no diagnostic.
    |     ++

warning: the loop variable `index` is used to index `lines`
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

warning: the loop variable `index` is used to index `lines`
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

warning: the variable `count` is used as a loop counter
   --> src/native/ref_tasks/line.rs:126:5
    |
126 |     for (byte, ch) in collapsed.char_indices() {
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: consider using: `for (count, (byte, ch)) in collapsed.char_indices().enumerate()`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#explicit_counter_loop
    = note: `#[warn(clippy::explicit_counter_loop)]` on by default

warning: doc list item without indentation
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

warning: `format!` in `format!` args
   --> src/native/relation_labels/cli.rs:546:22
    |
546 |       let mut counts = format!(
    |  ______________________^
547 | |         "{} {} {} {} {} {}",
548 | |         report.counts.labels,
549 | |         label_word(report.counts.labels),
...   |
553 | |         format!("{} hidden", report.counts.hidden,),
554 | |     );
    | |_____^
    |
    = help: combine the `format!(..)` arguments with the outer `format!(..)` call
    = help: or consider changing `format!` to `format_args!`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#format_in_format_args

warning: consider using `sort_by_key`
   --> src/native/relation_labels/rename.rs:832:5
    |
832 |     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
    |     ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
832 -     ordered.sort_by(|left, right| right.0.start.cmp(&left.0.start));
832 +     ordered.sort_by_key(|right| std::cmp::Reverse(right.0.start));
    |

warning: this function has too many arguments (9/7)
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

warning: match expression looks like `matches!` macro
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

warning: consider using `sort_by_key`
   --> src/native/task_cancel/prune.rs:167:9
    |
167 |         edits.sort_by(|left, right| right.0.cmp(&left.0));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
167 -         edits.sort_by(|left, right| right.0.cmp(&left.0));
167 +         edits.sort_by_key(|right| std::cmp::Reverse(right.0));
    |

warning: this lifetime isn't used in the function definition
   --> src/native/task_cancel/prune.rs:203:22
    |
203 | fn is_dedicated_line<'a>(
    |                      ^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#extra_unused_lifetimes
    = note: `#[warn(clippy::extra_unused_lifetimes)]` on by default

warning: this boolean expression can be simplified
   --> src/native/task_complete/keep_moving.rs:604:9
    |
604 |         !task.scheduled.is_some_and(|date| date > today)
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `task.scheduled.is_none_or(|date| date <= today)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#nonminimal_bool

warning: this function has too many arguments (9/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (8/7)
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

warning: this function has too many arguments (9/7)
   --> src/native/task_complete/successors.rs:833:1
    |
833 | / fn effective_relation_state_map(
834 | |     verdicts: &[DependentVerdict],
835 | |     files: &[FileScan],
836 | |     states: &BTreeMap<
...   |
845 | |     source_paths: &BTreeSet<&Path>,
846 | | ) -> BTreeMap<String, SourceRecovery> {
    | |_____________________________________^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:1103:1
     |
1103 | / fn relation_offer_placement(
1104 | |     group: &RelationOfferGroup,
1105 | |     completed: &[CompletedTask],
1106 | |     baseline_day: &DayView,
...    |
1111 | |     implicit: Option<&ImplicitDest>,
1112 | | ) -> Option<RelationOfferPlacement> {
     | |___________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (8/7)
    --> src/native/task_complete/successors.rs:2508:1
     |
2508 | / fn attach_offer(
2509 | |     verdict: &mut DependentVerdict,
2510 | |     files: &[FileScan],
2511 | |     day: &DayView,
...    |
2516 | |     project: Option<PathBuf>,
2517 | | ) -> bool {
     | |_________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (12/7)
    --> src/native/task_complete/successors.rs:2609:1
     |
2609 | / fn apply_project_member_classes(
2610 | |     verdicts: &mut Vec<DependentVerdict>,
2611 | |     folds: &mut Vec<ProjectFold>,
2612 | |     members: Vec<super::project_close::ProjectResidentClass>,
...    |
2621 | |     _note_settings: &NoteTaskSettings,
2622 | | ) {
     | |_^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: this function has too many arguments (13/7)
    --> src/native/task_complete/successors.rs:3199:1
     |
3199 | / fn apply_verdicts(
3200 | |     input: SuccessorInput,
3201 | |     files: Vec<FileScan>,
3202 | |     verdicts: Vec<DependentVerdict>,
...    |
3212 | |     relation_target_reads: usize,
3213 | | ) -> SuccessorPlan {
     | |__________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: very complex type used. Consider factoring parts into `type` definitions
   --> src/native/task_move/command.rs:644:6
    |
644 | ) -> Result<(Option<(PathBuf, String)>, Vec<RelocatedInfo>), String> {
    |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: very complex type used. Consider factoring parts into `type` definitions
    --> src/native/task_move/plan.rs:1375:6
     |
1375 | ) -> Result<(Vec<String>, Vec<RenameRecord>, BTreeMap<String, String>), PlanError>
     |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#type_complexity

warning: this function has too many arguments (8/7)
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

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:556:5
    |
556 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:364:9
    |
364 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: this function has too many arguments (14/7)
    --> src/native/task_status_hooks/sync.rs:1358:1
     |
1358 | / fn consume_blocked_links_after_compose(
1359 | |     compose: &mut ComposeResult,
1360 | |     files: &[FileScan],
1361 | |     daily_path: &Path,
...    |
1372 | |     project_tasks: &BTreeSet<(PathBuf, String)>,
1373 | | ) -> (Vec<ConsumedBlockedReference>, Vec<RemovedEmptyPomodoro>) {
     | |_______________________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#too_many_arguments

warning: useless use of `vec!`
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
    = note: `#[warn(clippy::useless_vec)]` on by default
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

warning: `bob-obsidian` (lib) generated 404 warnings
error: could not compile `bob-obsidian` (lib) due to 2 previous errors; 404 warnings emitted
warning: build failed, waiting for other jobs to finish...
warning: redundant redefinition of a binding `plans`
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
    = note: `#[warn(clippy::redundant_locals)]` on by default

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:364:10
    |
364 |     ) -> Result<PlannedDependencyUpdate, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
   --> src/native/capture/blocked_tasks.rs:628:10
    |
628 |     ) -> Result<DependentRef, CaptureError> {
    |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
    |
    = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
    --> src/native/capture/project_note.rs:1240:10
     |
1240 |     ) -> Result<PlannedCaptureItem, CaptureError> {
     |          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
     |
     = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:14:6
   |
14 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/sections.rs:31:6
   |
31 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: the `Err`-variant returned from this function is very large
  --> src/native/capture/tests/mod.rs:20:6
   |
20 | ) -> Result<ParsedCaptureText, CaptureError> {
   |      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ the `Err`-variant is at least 200 bytes
   |
   = help: try reducing the size of `native::capture::output::CaptureError`, for example by boxing large elements or replacing it with `Box<native::capture::output::CaptureError>`
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#result_large_err

warning: this match could be written as a `let` statement
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
     = note: `#[warn(clippy::match_single_binding)]` on by default
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

warning: this match could be written as a `let` statement
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

warning: this match could be written as a `let` statement
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

warning: this match could be written as a `let` statement
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

warning: this match could be written as a `let` statement
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

warning: very complex type used. Consider factoring parts into `type` definitions
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

warning: function call inside of `expect`
  --> src/native/capture_language/tests/goto.rs:54:42
   |
54 |         let completion = field(raw, end).expect(&format!("{raw:?} completes"));
   |                                          ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw:?} completes"))`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call
   = note: `#[warn(clippy::expect_fun_call)]` on by default

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:102:22
    |
102 |         execute(raw).expect(&format!("{raw} stays prose"));
    |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
   --> src/native/capture_language/tests/goto.rs:115:35
    |
115 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
    |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2412:35
     |
2412 |         let parsed = execute(raw).expect(&format!("{raw} stays prose"));
     |                                   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} stays prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2449:48
     |
2449 |         let completion = field(raw, raw.len()).expect(&format!("{raw} completes"));
     |                                                ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|| panic!("{raw} completes"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: function call inside of `expect`
    --> src/native/capture_language/tests/grammar.rs:2458:22
     |
2458 |         execute(raw).expect(&format!("{raw} executes as prose"));
     |                      ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^ help: try: `unwrap_or_else(|_| panic!("{raw} executes as prose"))`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#expect_fun_call

warning: unnecessary use of `get(Path::new("b.md")).is_none()`
   --> src/native/capture_pomodoro_close/linked_task_tests.rs:223:28
    |
223 |         plan.changed_files.get(Path::new("b.md")).is_none(),
    |         -------------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |         |
    |         help: replace it with: `!plan.changed_files.contains_key(Path::new("b.md"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check
    = note: `#[warn(clippy::unnecessary_get_then_check)]` on by default

warning: this assertion has a constant value
   --> src/native/file_coordination.rs:225:9
    |
225 |         assert!(!IS_COORDINATED);
    |         ^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: consider moving this into a const block: `const { assert!(..) }`
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#assertions_on_constants
    = note: `#[warn(clippy::assertions_on_constants)]` on by default

warning: initializer for `thread_local` value can be made `const`
  --> src/native/highlights_ref/overwrite/execute.rs:62:58
   |
62 |     static FAILPOINT: Cell<Option<OverwriteFailpoint>> = Cell::new(None);
   |                                                          ^^^^^^^^^^^^^^^ help: replace with: `const { Cell::new(None) }`
   |
   = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#missing_const_for_thread_local
   = note: `#[warn(clippy::missing_const_for_thread_local)]` on by default

warning: field assignment outside of initializer for an instance created with Default::default()
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

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/highlights_ref/tests/continuations.rs:249:42
    |
249 |     let plan = super::plan_continuations(&[first.clone()]);
    |                                          ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&first)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: redundant redefinition of a binding `first`
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

warning: replacing text with itself
    --> src/native/highlights_ref/tests/sections_render.rs:1103:22
     |
1103 |       let at_sidecar = sidecar
     |  ______________________^
1104 | |         .replace("#what-is-it", "@what-is-it")
1105 | |         .replace("# what is it", "# what is it");
     | |________________________________________________^
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#no_effect_replace
     = note: `#[warn(clippy::no_effect_replace)]` on by default

warning: an array of `Range` that is only one element
   --> src/native/highlights_ref/tests/underlines.rs:290:41
    |
290 |         apply_emphasis(already_strong, &[strong_start..strong_end]),
    |                                         ^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#single_range_in_vec_init
    = note: `#[warn(clippy::single_range_in_vec_init)]` on by default
help: if you wanted a `Vec` that contains the entire range, try
    |
290 -         apply_emphasis(already_strong, &[strong_start..strong_end]),
290 +         apply_emphasis(already_strong, &(strong_start..strong_end).collect::<std::vec::Vec<usize>>()),
    |

warning: consider using `sort_by_key`
   --> src/native/periods/list.rs:349:9
    |
349 |         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
    |         ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_sort_by
help: try
    |
349 -         sorted.sort_by(|a, b| sort_key(b).cmp(&sort_key(a)));
349 +         sorted.sort_by_key(|b| std::cmp::Reverse(sort_key(b)));
    |

warning: this call to `clone` can be replaced with `std::slice::from_ref`
   --> src/native/pomodoro.rs:872:51
    |
872 |             render_tmux_theme_name(status, "BOB", &[theme.clone()], true),
    |                                                   ^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&theme)`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: this call to `clone` can be replaced with `std::slice::from_ref`
    --> src/native/ref_library/attach.rs:2353:17
     |
2353 |                 &[later_page.clone()],
     |                 ^^^^^^^^^^^^^^^^^^^^^ help: try: `std::slice::from_ref(&later_page)`
     |
     = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#cloned_ref_to_slice_refs

warning: redundant redefinition of a binding `files`
   --> src/native/task_status_hooks/sync.rs:556:5
    |
556 |     let mut files = files;
    |     ^^^^^^^^^^^^^^^^^^^^^^
    |
help: `files` is initially defined here
   --> src/native/task_status_hooks/sync.rs:364:9
    |
364 |     let mut files = Vec::with_capacity(markdown_files.len());
    |         ^^^^^^^^^
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#redundant_locals

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:698:27
    |
698 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:709:27
    |
709 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("a.md", "dep")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:720:27
    |
720 |     assert!(scanned.edges.get(&edge("a.md", "dep")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("a.md", "dep"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: unnecessary use of `get(&edge("proj.md", "prj")).is_none()`
   --> src/native/task_status_hooks/tests/sync.rs:814:27
    |
814 |     assert!(scanned.edges.get(&edge("proj.md", "prj")).is_none());
    |             --------------^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
    |             |
    |             help: replace it with: `!scanned.edges.contains_key(&edge("proj.md", "prj"))`
    |
    = help: for further information visit https://rust-lang.github.io/rust-clippy/rust-1.95.0/index.html#unnecessary_get_then_check

warning: `bob-obsidian` (lib test) generated 438 warnings (403 duplicates)
error: could not compile `bob-obsidian` (lib test) due to 2 previous errors; 438 warnings emitted
error: recipe `lint` failed on line 70 with exit code 101
failed  exit=101  duration=101938ms

