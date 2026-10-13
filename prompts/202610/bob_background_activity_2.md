- **PLAN:**
  [202610/bob_background_activity_2.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/bob_background_activity_2.md)
- **AGENTS:**
  - [bbugyi200.apollo.7a.f0--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.7a.f0.md)

%macros_enabled:false

# Previous Continuation

This fork uses versioned continuation replay. Blocks are stable, parent-first
projections of exact continuation nodes; any historical source without recoverable node
provenance is represented as an opaque legacy boundary.

- **Projection version:** `1`
- **Ordered nodes:** `1`

## Continuation Block `block:v1:3b27fc50a5f7d9810099a58b64fd68b6`

- **Node:** `agent-delta:20261013050250:249daf5236511c58`
- **Kind:** `agent_delta`
- **Parents:** (none)
- **Content:**
  `local:continuation/records/agent_delta/agent-delta:20261013050250:249daf5236511c58.json`

### User

**Protected user instruction.** Carry this request unless an explicit attributed update
supersedes it.

I keep receiving the "App Background Activity" message on my macbook when running the
`just install-all` command. I need to manually hit the "X" button on this notification
every time so it is pretty annoying. See the ~/tmp/screenshots/20261013_050016.png
screenshot for context.

Can you do some research with the goal of helping me figure out how to stop this
notification from popping up? Make sure your report is concise and easy to understand.

Write this research to a new markdown file under the
$(sase repo path research --ensure)/$(date +%Y%m)/ directory.

After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l
"research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example `research:202609/topic.md`), including any subdirectory the steps above put
it in. Do not derive the label from the current month, the clock, or a guessed name. Do
not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete. %m:@xlarge

### Assistant

Found the likely culprit: a chezmoi-managed `bob-vault-sync` LaunchAgent that runs `bob`
directly. Checking its plist and other LaunchAgents next.

Still verifying: checking whether `install_all` replaces the `bob` binary on every run,
or only when bob-cli has new commits.

The report is registered. Checking that the snapshot includes my last edit, since both
ran at the same time.

I found the cause: your `bob-vault-sync` LaunchAgent starts `~/.cargo/bin/bob` directly.
The fix is a one-line change to that agent's plist so it starts `bob` through `/bin/sh`.

**Why it happens:** each time `just install-all` installs a newly built `bob`,
`cargo install` writes a new binary with only an automatic, throwaway signature. macOS's
background-item tracker identifies that kind of binary by its exact contents. So every
rebuild looks like a brand-new background program, and macOS shows the alert. It's set
to the "Alerts" style, which is why it stays until you click X.

**Evidence from your Mac** (I only read things over SSH; I changed nothing):

- `codesign` shows `bob` has a throwaway signature with no Team ID.
- `bob` was installed at 04:59. At 04:59:59 the logs show macOS dropping the old record
  for the vault-sync agent, and at 05:00:00 posting "“bob” can run in the background",
  which matches your screenshot.
- The logs show nine of these alerts since yesterday morning, each for a newly created
  record.
- The plist hasn't changed since it was added to chezmoi, so the new binary is what
  triggers it.

**Recommended fix:** in chezmoi, change `ProgramArguments` in
`home/Library/LaunchAgents/com.bbugyi.bob-vault-sync.plist` to:

```xml
<string>/bin/sh</string> <string>-c</string> <string>exec /Users/bbugyi/.cargo/bin/bob vault-sync -q</string>
```

Then run `chezmoi apply` and reload the agent with `launchctl bootout` and
`launchctl bootstrap` (exact commands are in the report). macOS will then track
`/bin/sh`, which Apple signs and which never changes. Expect one last alert when you
reload, then none on later installs.

The cause is confirmed by the logs, but I haven't tested the fix on your Mac. It's a
strong inference from how macOS tracks these items. If an alert still shows up after a
rebuild, the fallback is signing `bob` with a real certificate after each install. Your
Mac currently has no signing certificates, so that needs more setup.

**Don't:** switch "bob" off in Login Items & Extensions, because that stops vault sync.
Running `sfltool resetbtm` only helps until the next rebuild.

The report is at `202610/macos_bob_background_activity_notification.md` in the research
repo. It's registered as artifact `explicit:c40fb32ee051403a3c2833b8` (label
`research:202610/macos_bob_background_activity_notification.md`), and the research repo
commit happens automatically when this turn ends.

---

%macros_enabled:true

# New Query

Can you help me implement the recommended fix? Think this through thoroughly and create
a plan using your `/sase_plan` skill. Choose and author the appropriate tier, validate
and revalidate until it passes, then submit it with `sase plan propose` (as the skill
instructs) before making any file changes.
