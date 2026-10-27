# Chat History - ace-run (bob-cli-ac.3--mon-4)

- **TIMESTAMP:** 2026-10-20 22:14:49 EDT
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-ac.3--mon-4

## Prompt

sase monitor start --command 'gh run watch 39530816998 --exit-status; s1=$?; gh run watch 39530828412 --exit-status; s2=$?; echo "full-ci-push-exit=$s1 dispatch-exit=$s2"; test "$s1" -eq 0 && test "$s2" -eq 0' --reason 'Wait for GitHub CI full=true runs 39530816998 (ci/full-ci push) and 39530828412 (workflow_dispatch on ci/ci)'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 2 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 3 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 4 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 5 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 6 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (ubuntu-latest)[0m (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 7 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 8 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 9 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 10 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;33m*[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;33m*[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;33m*[0m Post Cache Rust
  [0;33m*[0m Post Check out
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;33m*[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;33m*[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;33m*[0m [0;1;39mtest (macos-latest)[0m (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;33m*[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;1;39mRefreshing run status every 3 seconds. Press Ctrl+C to quit.[0m

[0;33m*[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (macos-latest)[0m in 11m35s (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
[0;32m✓[0m [0;1;39mci/full-ci[0m CI · [0;36m39530816998[0m
Triggered via push about 11 minutes ago

[0;1;39mJOBS[0m
[0;32m✓[0m [0;1;39mpackage[0m in 1m48s (ID [0;36m118996021206[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Check package contents and size
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (ubuntu-latest)[0m in 7m10s (ID [0;36m118996021399[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [38;5;242m-[0m Install macOS bash 5
  [0;32m✓[0m Install full-test tools
  [38;5;242m-[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mtest (macos-latest)[0m in 11m35s (ID [0;36m118996021414[0m)
  [0;32m✓[0m Set up job
  [0;32m✓[0m Check out
  [0;32m✓[0m Install pinned toolchain
  [0;32m✓[0m Cache Rust
  [0;32m✓[0m Install just
  [0;32m✓[0m Install uv
  [0;32m✓[0m Install macOS bash 5
  [38;5;242m-[0m Install full-test tools
  [0;32m✓[0m Lint macOS-only targets
  [0;32m✓[0m Run tests
  [0;32m✓[0m Post Install uv
  [0;32m✓[0m Post Cache Rust
  [0;32m✓[0m Post Check out
  [0;32m✓[0m Complete job
[0;32m✓[0m [0;1;39mlint[0m in 1m43s (ID [0;36m118996021455[0m)
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
[38;5;242mpackage: .github#1
[0m
- "The ubuntu-latest label will migrate to Ubuntu 26 beginning October 19, 2026. For more information, see https://github.com/actions/runner-images/issues/14748"
[38;5;242mlint: .github#1
[0m
Run [0;1;39mCI[0m ([0;36m39530828412[0m) has already completed with 'success'
full-ci-push-exit=0 dispatch-exit=0

