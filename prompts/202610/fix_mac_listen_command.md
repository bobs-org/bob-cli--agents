- **PLAN:**
  [202610/fix_mac_listen_command.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/fix_mac_listen_command.md)
- **AGENTS:**
  - [bbugyi200.apollo.6m--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6m.md)

Can you help me fix this error that I'm seeing on my macbook (see the command output
below for context)? Think this through thoroughly and create a plan using your
`/sase_plan` skill. Choose and author the appropriate tier, validate and revalidate
until it passes, then submit it with `sase plan propose` (as the skill instructs) before
making any file changes.

```
bob-cli on  master is 📦 v0.1.0 via 🦀 v1.95.0
❯ bob ref create https://interconnected.org/home/2026/01/15/reminders -i -L -P sase
fetching interconnected.org…
capturing interconnected.org…
listen: run sase-listen render https://interconnected.org/home/2026/01/15/reminders -e full -o /tmp/bb/bob-clip-35305-1791662645553844000/reminders.mp3
sh: sase-listen: command not found
bob ref: error: listen command failed with exit 127
hint: nothing was written to the vault; rerun the same command once the listen error above is fixed
```
