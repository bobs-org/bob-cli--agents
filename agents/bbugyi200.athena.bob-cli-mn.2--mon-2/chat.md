# Chat History - ace-run (bob-cli-mn.2--mon-2)

- **TIMESTAMP:** 2026-11-17 10:41:26 EST
- **MODEL:** grok/grok-4.6
- **AGENT:** bob-cli-mn.2--mon-2

## Prompt

sase monitor start --command 'BASE=22a95b6425efd7eb560103d574adc3d7689035ac; REPO=bobs-org/bob-mac-capture; until SHA=$(git ls-remote origin refs/heads/master | awk "{print \\$1}"); [ -n "$SHA" ] && [ "$SHA" != "$BASE" ]; do sleep 20; done; echo "landed SHA $SHA"; i=0; RID=; while [ "$i" -lt 30 ]; do RID=$(gh run list --repo "$REPO" --commit "$SHA" --json databaseId --jq ".[0].databaseId // empty"); [ -n "$RID" ] && break; i=$((i+1)); sleep 10; done; [ -n "$RID" ] || { echo "no run for $SHA"; exit 2; }; echo "watching run $RID"; gh run watch "$RID" --repo "$REPO" --exit-status' --reason 'Watch exact-SHA macOS CI after the separator follow-up tip wait lands on bob-mac-capture master'

## Response

sase: running unwrapped (no profile (monitor.tool_wrap is verify))
landed SHA 4d96d4a5a9027967c18f0e25618ef064c4c001ff
watching run 44111365749
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push less than a minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push less than a minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push less than a minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push less than a minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push less than a minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 1 minute ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 2 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 3 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 4 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  * Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 5 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  * Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  * Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  * Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 6 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 7 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 8 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  * Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 9 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 10 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 11 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 12 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 13 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 14 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 15 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 16 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 17 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 18 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 19 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 20 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 21 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 22 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  * Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  * Upload render fixtures
  * Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 23 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 24 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 25 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 26 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 27 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 28 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  * Bundle
  * Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  * Launch smoke test
  * Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 29 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  * Install and reinstall
  * Post Check out repository
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  ✓ Install and reinstall
  ✓ Post Check out repository
  * Complete job
Refreshing run status every 3 seconds. Press Ctrl+C to quit.

* master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
* macOS 26 SwiftPM (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  ✓ Install and reinstall
  ✓ Post Check out repository
  ✓ Complete job
✓ master CI · 44111365749
Triggered via push about 30 minutes ago

JOBS
✓ macOS 26 SwiftPM in 25m12s (ID 134137538402)
  ✓ Set up job
  ✓ Check out repository
  ✓ Check scripts
  ✓ Show toolchain
  ✓ Lint Swift formatting
  ✓ Build
  ✓ Test
  ✓ Upload render fixtures
  - Upload test hang samples
  ✓ Bundle
  ✓ Verify plist and signature
  ✓ Launch smoke test
  - Upload launch smoke test diagnostics
  ✓ Install and reinstall
  ✓ Post Check out repository
  ✓ Complete job

