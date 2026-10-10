- **PLAN:**
  [202610/percent_url_listen_precedence.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/percent_url_listen_precedence.md)
- **AGENTS:**
  - [bbugyi200.apollo.6n--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.apollo.6n.md)

I don't think the `%` URL suffix (see recent, related git commits) worked for the
bob-mac-capture app. The `https://arxiv.org/pdf/2609.12039 %` input just produced a task
that looked like the following in the ~/bob/mac_inbox.md file:

```
- [ ] #task https://arxiv.org/pdf/2609.12039 [created::2026-10-10]
  - https://arxiv.org/pdf/2609.12039
```

I think there is a conflicting behavior that should be de-prioritized in this case in
favor of `%` meaning that we should use the `bob ref create` command's `-L|--listen`
option. Can you help me confirm/deny my suspicion, diagnose the true root cause, and fix
the issue?

Think this through thoroughly and create a plan using your `/sase_plan` skill. Choose
and author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.
