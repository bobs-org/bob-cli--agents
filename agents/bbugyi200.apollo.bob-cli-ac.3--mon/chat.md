# Chat History - ace-run (bob-cli-ac.3--mon)

- **TIMESTAMP:** 2026-10-20 19:42:54 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-ac.3--mon

## Prompt

sase monitor start --command 'gh run watch 39516238570 --exit-status' --reason 'Wait for GitHub CI run 39516238570 on scratch branch ci/ci'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 1 minute ago

[0;1;39mJOBS[0m
[0;33m*[0m [0;1;39mpackage[0m (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;33m*[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 1 minute ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;33m*[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 1 minute ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;33m*[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;31mX[0m [0;1;39mci/ci[0m CI · [0;36m39516238570[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118948957495[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;31mX[0m [0;1;39mtest (macos-latest)[0m in 1m58s (ID [0;36m118948957764[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [0;31mX[0m Lint macOS-only targets
  [38;5;242m-[0m Run tests
  [38;5;242m-[0m Post Install uv
  [38;5;242m-[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 5m11s (ID [0;36m118948957842[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m20s (ID [0;36m118948957934[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Format, clippy, scripts, and release-tool tests
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job

[0;1;39mANNOTATIONS[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m

