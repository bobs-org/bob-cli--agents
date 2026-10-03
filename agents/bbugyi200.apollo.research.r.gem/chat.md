# Chat History - ace-run (research.r.gem)

- **TIMESTAMP:** 2026-09-29 17:57:33 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.r.gem
- **PROMPT:** `~/.sase/multi_prompts/202609/gh_bobs_org__bob_cli-multiprompt-260929_175133.md`

## Prompt

%id(gem, clan=research.r)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.r.cdx`, `research.r.cld`, `research.r.grk`, `research.r.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I think I want to
implement a sase memory web that records the more important architectural / policy
decisions that I've made for this project, the bob-plugins project, the bob-mac-capture
project, and my Obsidian vault in general.

- This memory web should be heavily inspired by the decisions memory web defined in the
  "sase" project.
- Think hard about which initial decisions memory strands I should add to this memory
  web.

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
(for example `research:202609/topic__a.md`), including any subdirectory the steps above
put it in. Do not derive the label from the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

# Research Report: SASE Decisions Memory Web for the Bob Ecosystem

- **Researcher:** `gem` (Independent 5-Researcher Swarm)
- **Report File:** [`sase/repos/research/202609/decisions_memory_web_architecture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202609/decisions_memory_web_architecture__gem.md)
- **Artifact Registered:** `research:202609/decisions_memory_web_architecture__gem.md` (`file:explicit:54b5bd61ed1a31ef95b4cc3e`)

---

## 1. Executive Summary & Core Verdict

The proposal to implement a SASE memory web named `decisions` covering `bob-cli`, `bob-plugins`, `bob-mac-capture`, and the Obsidian vault (`~/bob`) is **a great idea and strongly recommended**, subject to **four structural adjustments**:

1. **Flat Namespacing with Domain Prefixes (`<domain>-<slug>`):** SASE memory web discovery explicitly forbids nested directories (`nested_directory` fail-closed error). Because four distinct subsystems are represented in one web, slugs must use domain prefixes (`vault-*`, `cli-*`, `plugins-*`, `mac-*`).
2. **Unified Web in `bob-cli`:** All four domains should live in a single unified `decisions` web in `bob-cli`. Neither `bob-plugins` nor `bob-mac-capture` is a SASE project, and `bob-cli` acts as the operational orchestrator.
3. **Strict ADR Litmus Test:** Strands must be true Architectural Decision Records (ADRs) with **Claim**, **Why** (including rejected alternatives), **Cost** (trade-offs), and **Reopens when** (falsifiable conditions). Runbooks belong in `docs/`, and terms belong in `glossary`.
4. **Context Budget Discipline:** With `roster: list`, every strand's summary is inlined into `AGENTS.md` on every turn. The catalog should start with a curated set of **12–14 load-bearing decisions** (~500 tokens in the baseline prompt).

---

## 2. Critique of the Proposal

### Why It Is a Good Idea
- **Mitigates Agent Rationalization:** LLMs frequently propose "standard" patterns that break deliberate project choices (e.g. proposing TypeScript/bundlers for `bob-plugins`, attempting direct vault file I/O inside `bob-mac-capture`, or reverting Git sync to Obsidian Sync). ADRs make accepted choices and rejected alternatives explicit.
- **Low-Token Roster, On-Demand Depth:** SASE memory webs present a concise index in `AGENTS.md` and keep deep rationales on disk, retrieved only when an agent works in that specific subsystem via `sase memory read decisions:<slug>`.

### Risks and Pitfalls
- **The "Runbook / Documentation Trap":** Agents often mistake syntax references, runbooks, or tutorials for decisions. If an entry does not reject a credible alternative, it belongs in `docs/`, `README.md`, or reference memory.
- **Roster Inlining Bloat:** If dozens of minor code conventions are added, `AGENTS.md` will bloat. Only cross-system boundaries and high-consequence invariants belong in `decisions`.
- **Cross-Repo Context:** While `bob-cli` is the central project, home-level memory (`~/sase/memory/obsidian.md`) must include a pointer so agents working outside `bob-cli` know this decisions web exists.

---

## 3. Justified Requirement Adjustments

| Requirement | Proposed Plan | Recommended Adjustment | Rationale |
| :--- | :--- | :--- | :--- |
| **Directory Structure** | Flat or nested | **Flat with domain prefixes** (`vault-*`, `cli-*`, `plugins-*`, `mac-*`) | SASE discovery forbids subdirectories in memory webs. Prefixes prevent naming collisions. |
| **Hosting Repo** | Across projects | **Centralized in `bob-cli`** | `bob-cli` is the sole SASE project; linked repos are accessed from here via `/sase_repo`. |
| **Record Scope** | General decisions | **Strict 4-part ADR schema only** | Prevents duplicating runbooks, CLI flags, or glossary terms. |
| **Home Memory Link** | Isolated | **Cross-link in `~/sase/memory/obsidian.md`** | Connects home-scoped agent memory with project-scoped decision strands. |

---

## 4. Curated Initial Decisions Catalog (13 Strands)

### Domain 1: Obsidian Vault (`vault-*`)
1. **`vault-git-sync-only`** — *Git Is The Sole Sync Transport:* `~/bob` syncs strictly via Git (`bob vault-sync`); Obsidian Sync is permanently retired and forbidden.
2. **`vault-parent-hierarchy`** — *Notes Require A Parent Frontmatter Link:* Every new Markdown note must declare `parent: "[[Ancestor]]"` to prevent orphan notes.
3. **`vault-now-tag-vs-in-progress`** — *Now Tag Represents Commitment, In Progress Represents Activity:* `#now` is a human-curated weekly bet (≤15 tasks); `[/]` is a machine-derived, auto-decaying Pomodoro footprint. Solves the "status-lock trap".
4. **`vault-task-dependency-ids`** — *Task Dependencies Use Namespaced Vault-Wide Identifiers:* Task dependencies in Dataview/Tasks use sanitized IDs (`projects__Name__blockid`) to eliminate cross-file anchor collisions.

### Domain 2: Bob CLI Architecture (`cli-*`)
5. **`cli-rust-native-core`** — *Native Rust Core Replaces Shell Scripts:* Core CLI commands are native Rust; shell scripts exist solely as fallback shims.
6. **`cli-sync-maintenance-lock`** — *Shared Maintenance Lock Coordinates Vault Mutation:* `bob vault-sync`, `bob nightly`, `bob task-status-hooks`, and `bob randomize` serialize access through `bob_sync.lock`.
7. **`cli-batch-capture-planning`** — *Capture Parses and Plans The Entire Batch Before Writing:* Multi-line captures construct an in-memory plan before modifying files; any syntax error fails closed without partial writes.
8. **`cli-embedded-js-dataview`** — *Headless Dataview Queries Run via Embedded JavaScript:* `bob query` runs Dataview/Tasks logic in embedded QuickJS (`rquickjs`) for 100% semantic fidelity without Electron/Node overhead.

### Domain 3: Bob Plugins Architecture (`plugins-*`)
9. **`plugins-commonjs-no-bundler`** — *CommonJS Monorepo With No Bundler Or TypeScript:* `bob-plugins` are authored in plain CommonJS (`main.js` is source); no Webpack, Babel, or TypeScript build steps.
10. **`plugins-monorepo-source-of-truth`** — *Plugins Monorepo Is Sole Source of Truth:* `bob-plugins` is the source of truth; vault folders (`~/bob/.obsidian/plugins/`) are ephemeral deploy targets synced via `bob plugins sync`.
11. **`plugins-vim-hotkey-partitioning`** — *Strict Partitioning of Vim Leader Chords Across Plugins:* Leader keymaps are strictly partitioned between plugins (e.g. `\p` for ledger tools, `\s` for tab pins) to prevent dropped keystrokes in Obsidian Vim mode.

### Domain 4: Bob Mac Capture Architecture (`mac-*`)
12. **`mac-capture-delegates-mutation`** — *Mac Capture Is Presentation-Only And Delegates All Vault Mutation:* The Swift menu-bar app owns UI/hotkeys and delegates 100% of capture grammar, completion, and vault mutation to `bob-cli` via JSON subprocess calls.
13. **`mac-apple-toolchain-isolation`** — *Apple Toolchain Isolation via Xcode Swift Wrapper:* Builds and tests route through `Scripts/xcode-swift.sh` via `xcrun`, strictly rejecting shadowing Swift binaries on `PATH`.

---

## 5. Implementation Roadmap

1. **Create Descriptor (`sase/memory/decisions.md`):** Configure with `web: true`, `roster: list`, `roster_label: DECISIONS`, and `strand_noun: decision`.
2. **Author Strands (`sase/memory/decisions/<slug>.md`):** Populate the 13 curated strands with exact frontmatter (`keyword:`, `summary:`, `metadata.status: accepted`, `metadata.decided: YYYY-MM-DD`) and body sections (`**Claim.**`, `**Why.**`, `**Cost.**`, `**Reopens when.**`).
3. **Validate Drift:** Run `sase memory init -c` to ensure all strands satisfy SASE's 11 fail-closed rules.
4. **Materialize Roster:** Run `sase memory init` to generate the roster in `decisions.md` and propagate to `AGENTS.md` and provider instruction shims.
5. **Update Home Memory:** Add a cross-reference in `~/sase/memory/obsidian.md` pointing to `bob-cli`'s decisions web.

The full report with complete strand text and detailed analysis is preserved in [`sase/repos/research/202609/decisions_memory_web_architecture__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202609/decisions_memory_web_architecture__gem.md) and registered under `research:202609/decisions_memory_web_architecture__gem.md`.
