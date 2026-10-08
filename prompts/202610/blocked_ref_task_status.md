- **PLAN:**
  [202610/blocked_ref_task_status.md](https://github.com/bobs-org/bob-cli--plans/blob/main/202610/blocked_ref_task_status.md)
- **AGENTS:**
  - [bbugyi200.athena.0y9--plan](https://github.com/bobs-org/bob-cli--agents/blob/main/sessions/bbugyi200.athena.0y9.md)

Can you help me add support to the `bob ref scan` command for allowing `^ref` notes to
have a blocked status? See the command output below for context. The `^ref` task that we
are warning about is rightfully blocked until some other related work gets done. Think
this through thoroughly and create a plan using your `/sase_plan` skill. Choose and
author the appropriate tier, validate and revalidate until it passes, then submit it
with `sase plan propose` (as the skill instructs) before making any file changes.

```
❯ bob ref scan -w
pre_scan_hook: run PATH="$HOME/bin:$PATH" bob_xlib_pull
Scanning 334 PDFs in lib

  error  agent instructions budgeted router  generated PDF task line on line 4 is malformed; expected a generated task with one of [ ], [*], [/], [x], [X], or [-], such as '- [ ] #task #ref [[...pdf]] #hide ^ref'; legacy generated lines without #ref, with [p::2], or without #hide are still accepted
  ok     sase task bead 48h impact rating    updated note + marker
334 pdfs · 0 created · 1 updated · 332 unchanged · 1 marker · 0 tasks · 1 image · 1 failure · writes: note,pdf
bob ref: scan completed with 1 per-PDF failure(s)
planning failures:
  /Users/bbugyi/bob/lib/chat/agent_instructions_budgeted_router.pdf: generated PDF task line on line 4 is malformed; expected a generated task with one of [ ], [*], [/], [x], [X], or [-], such as '- [ ] #task #ref [[...pdf]] #hide ^ref'; legacy generated lines without #ref, with [p::2], or without #hide are still accepted
```
