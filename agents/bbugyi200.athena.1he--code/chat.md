# Chat History - ace-run (1he--code)

- **TIMESTAMP:** 2026-11-27 14:57:02 EST
- **MODEL:** muse/muse-spark-1.3-contributor
- **AGENT:** 1he--code

## Prompt

%model:@small
#gh:gh_bobs-org__bob-cli @plan:202611/always_show_priority_bars.md

The above plan has been reviewed and approved. Implement it now.


## Response

Done. The approved `always_show_priority_bars` plan is implemented, verified, and deployed.

- [bob-plugins](https://github.com/bobs-org/bob-plugins): removed the priority-bar fold on digit (`p1`–`p4`) rows — Live Preview and Reading view build unfolded widgets, `priorityMarkFoldedForLine/Row`, `blockMarkIsDigitKey`, and `data-folded` are gone, digit-row `.task-priority` clips deleted from `styles.css`, manifest bumped to 1.172.10. Prj/awaiting pill folds unchanged.
- [bob-cli](https://github.com/bobs-org/bob-cli): `docs/blocked-marks.md` and the Priority marks section of `docs/projects.md` now contract that bars always show; BM1/PM18 vectors expect bars shown.
- Verification: `npm run build`, `validate`, `docs:check` pass; 99/99 tests in the touched suites pass; real-Obsidian e2e passes **172/172** including the new cursor-reveals-raw-`[?]` regression case. The full unit suite has one unrelated pre-existing failure (`test-snooze-model-vectors`, fails identically without my changes; my diff touches no snooze files).
- Deploy: `bob plugins sync` hit the overwrite guard (vault held the landed 6827a27 build), so I followed the repo's documented recipe — fetched, fast-forwarded, clean-synced, re-applied, rebuilt, synced — and the vault now runs 1.172.10 with the fold machinery gone.

No `Cargo.toml` or `CHANGELOG.md` changes.
