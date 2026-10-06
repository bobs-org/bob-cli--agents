# Chat History - ace-run (0x9--code)

- **TIMESTAMP:** 2026-10-06 09:50:49 EDT
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 0x9--code

## Linked Chats

- 1. --0 — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-0x9__0-261006_092009.md`
- 2. --1 — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-0x9__1-261006_092009.md`
- **3. --code** — `~/.sase/chats/202610/gh_bobs_org__bob_cli-ace_run-0x9__code-261006_092009.md`

## Prompt

%model:@medium
#gh:gh_bobs-org__bob-cli @plan:202610/ctrl_shift_m_never_advances_walk.md

The above plan has been reviewed and approved. Implement it now.


## Response

Done: Ctrl+Shift+M never advances the review walk. A landed move follows the task to its destination note, parks the walk on a path+text-identified resume, and the next `]s`/`[s` lands on the moved row's walk neighbour. Vault is synced at nav 2.7.0.

What changed:

- bob-plugins (nav 2.7.0): new `537-plugin-review-move-park.js` (`reviewResumeRef`, `findReviewResumeIndex`, `buildReviewMoveAnchor`, `planReviewResume`, `parkReviewWalkAfterMove`); `reviewOutcomeResolves` no longer resolves `move`; `planReviewJump` honours the text resume (cursor-on-resume lands, line-fallback ignored, real text hits still win); move commit parks before focusing and always shows the plain `Moved N task(s) to X` toast; `reviewAnsweredKeys` untouched by moves.
- Tests: rewrote the landed-move test, added successor/predecessor/counted/stale/lock-swallow cases plus pure resume/anchor/planner tests. Full suite: 1873 pass, 0 fail; `npm run build:check` clean.
- Docs: `docs/freshness.md` §§6/13, `docs/getting-started.md`, plugin README (2.7.0). New decision `task-move-never-advances-the-walk`; `answering-advances-the-walk` marked superseded-in-part. Follow-up bug bead `bob-cli-4m` filed for the general `reviewAnsweredKeys` line-key fragility.

Manual smoke checklist (Obsidian, Vim normal mode):

- `]s` to a NEXT/PENDING landing, then Ctrl+Shift+M to an area note. Cursor follows the task, toast is plain `Moved 1 task to …`, and after editing in the destination, `]s` lands on the item after the moved one (even the row right below it).
- Same with `2<Ctrl+Shift+M>`.
- `<C-o>` returns to the source seam, and `]s` from there lands on that seam row.
- Ctrl+Alt+F, then immediate Ctrl+Shift+M, is swallowed.
- Ctrl+Alt+F, Alt+N, Ctrl+Shift+Enter, and Task Card commits still advance from a landing.
