- **PLAN:**
  [202610/pass_shared_recipient.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/pass_shared_recipient.md)
- **AGENTS:**
  - [bbugyi200.apollo.4f--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.4f.md)

When I insert passwords into my password store using the `pass insert` command on my
macbook, I can't read those passwords on this machine (see the command output below for
context). Can you help me diagnose the root cause of this issue and fix it? Think this
through thoroughly and create a plan using your `/sase_plan` skill. Choose and author
the appropriate tier, validate and revalidate until it passes, then submit it with
`sase plan propose` (as the skill instructs) before making any file changes.

```
❯ pass show sase_listen_feed_token
gpg: public key decryption failed: No secret key
gpg: decryption failed: No secret key
```
