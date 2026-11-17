# Chat History - ace-run (research.53.gem)

- **TIMESTAMP:** 2026-11-16 21:33:49 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.53.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261116_211235.md`

## Prompt

%id(gem, clan=research.53)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.53.cdx`, `research.53.cld`, `research.53.grk`, `research.53.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

Sase agents like the `ei` sase agent, for example, are frequently blocking work (costing
me hours) to confirm that they are allowed to sync the bob-plugins repo by running the
`bob plugins sync` command. I need to find a way to stop this safetly somehow.

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
Write this research to a new markdown file under the $(sase repo path research --ensure)/$(date +%Y%m)/ directory.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

Research completed and registered as a durable snapshot.

- **Report:** [bob_plugins_sync_agent_blocking__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/bob_plugins_sync_agent_blocking__gem.md)
- **Registered Artifact:** `research:202611/bob_plugins_sync_agent_blocking__gem.md` (`file:explicit:44715fdcb62ff730422fff27`, snapshot path `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261116211242/bob_plugins_sync_agent_blocking__gem-8b530052c70e.md`)

---

## Key Findings

1. **Agents are stalling on the `bob plugins sync` deploy guard, not generic command gates:**
   - `~/.sase/interaction_requests/custom_gate` had **0** plugin-sync blocks; `~/.sase/interaction_requests/question` recorded **10** force-sync `UserQuestion` prompts in November 2026 (9 resolved totaling **1,691.0m / 28.18h** of wall-clock waiting including overnight sessions, plus `d8a8aeef` from `ei--6` still unanswered after a ~2h15m `ei--code` → `ei--mon..mon-4` → `ei--1..6` loop).
2. **Root causes (`bob-plugins`, `bob-cli`, `sase`):**
   - **Workflow phase inversion:** `bob-plugins/AGENTS.md` (lines 12–15) mandates `bob plugins sync` before ending the turn, while SASE commits **post-turn** via `builtin@commit` (`sase stitch create`), guaranteeing every compliant agent deploys with `DirtyState::Dirty`.
   - **Phantom cross-plugin locks:** `git_dirty` (`src/native/plugins/deploy.rs:793–812`) inspects the entire monorepo root while default `bob plugins sync` (`src/native/plugins/sync.rs:74–132`) syncs all 11 configured plugins — so modifying one plugin (`bob-emoji` in `bob-cli_10`) dirty-stamps untouched ones (`bob-navigation-hotkeys`), causing the 2026-11-16 `ei` ↔ `bob-cli-mf.6` → `bob-cli-mg.land` deadlock.
   - **`incoming_clean` gating:** `evaluate_guard` (`src/native/plugins/deploy.rs:940`) only runs `find_inclusion_proof` when `incoming_clean` is true, even though proving that the vault's installed bytes exist in Git history does not require incoming cleanliness.
   - **Broken attribution & version noise:** `current_agent()` (`deploy.rs:191–196`) checks unset `SASE_AGENT_ID` instead of `SASE_AGENT_NAME` (leaving `agent: null`), `bob-emoji` still had 4 vault-tracked files omitted from `~/bob/.gitignore`, and `ei--6` misreported incoming `2.86.0` as installed when vault `manifest.json` held `2.85.2`.

## Critique & Requirement Adjustments

- **Why "stop asking before `bob plugins sync`" in the current workflow is a bad idea:** Dropping confirmations or auto-passing `-F` silently reintroduces the regression `bob-cli-cu` was built to prevent (clobbering landed or WIP plugins in `~/bob`). Worse, `bob-plugins` automated E2E tests (`scripts/obsidian-startup-smoke.cjs`, `scripts/obsidian-closed-pomodoro-link-e2e.cjs`) run in **isolated scratch vaults**, so coding agents have no real need to mutate live `~/bob` with unreviewed WIP from ephemeral `bob-cli_<N>` checkouts mid-turn.
- **Adjusted requirements:**
  1. **Remove `bob plugins sync` from ordinary mid-turn coding agent instructions.**
  2. **Deploy only landed, clean `origin/master` commits automatically** (skipping non-destructively with a warning if Bryan holds an intentional manual dirty deploy in `~/bob`), serialized mechanically with `flock` instead of agent wait loops.
  3. **Harden `deploy.rs` provenance and guard checks** as defense-in-depth for human/manual runs.

## Recommended Solution

Adopt **Option C (Post-Commit Clean Sync + Deploy Guard Hardening)**:
1. **Phase 1 (Immediate):** Remove the mid-turn `bob plugins sync` requirement from `bob-plugins/AGENTS.md`, `bob-cli/sase/memory/sase.md`, and `bob-cli/sase/sase.yml`; reserve manual dirty syncs strictly for explicit `-p <id>` targeted smoke tasks; untrack `.obsidian/plugins/bob-emoji` in `~/bob` and add it to `~/bob/.gitignore`.
2. **Phase 2 (`src/native/plugins/deploy.rs`):** Scope `git_dirty` per-plugin (`plugins/<id>/` plus shared build/root inputs), run `find_inclusion_proof` regardless of `incoming_clean`, read `SASE_AGENT_NAME` fallback in `current_agent()`, and surface the installed vault `manifest.json` version clearly.
3. **Phase 3 (Automated clean deploy):** Trigger a `flock`-serialized fast-forward pull and `bob plugins sync --no-pull` on a dedicated clean deploy mirror checkout via `sase`'s post-push `commit_hooks.after` (resolving linked-repo `local_config_command_trust` for `bob-plugins`, skipping vaultless hosts, never overwriting manual human dirty WIP, and verifying built `main.js` freshness across rebases) — or choose **Option D** (identical Phases 1–2, replacing Phase 3's hook with `just install-all` / a host timer if immediate per-commit `~/bob` updates are unnecessary).
