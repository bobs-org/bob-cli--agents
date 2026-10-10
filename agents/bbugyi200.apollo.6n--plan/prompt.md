#gh:gh_bobs-org__bob-cli I don't think the `%` URL suffix (see recent, related git commits) worked for
the bob-mac-capture app. The `https://arxiv.org/pdf/2609.12039 %` input just produced a
task that looked like the following in the ~/bob/mac_inbox.md file:

```
- [ ] #task https://arxiv.org/pdf/2609.12039 [created::2026-10-10]
  - https://arxiv.org/pdf/2609.12039
```

I think there is a conflicting behavior that should be de-prioritized in this case in
favor of `%` meaning that we should use the `bob ref create` command's `-L|--listen`
option. Can you help me confirm/deny my suspicion, diagnose the true root cause, and fix
the issue?

#plan %m:gpt-6-astra %auto