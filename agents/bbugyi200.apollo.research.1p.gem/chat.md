# Chat History - ace-run (research.1p.gem)

- **TIMESTAMP:** 2026-10-16 13:47:57 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.1p.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261016_133648.md`

## Prompt

%id(gem, clan=research.1p)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.1p.cdx`, `research.1p.cld`, `research.1p.grk`, `research.1p.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I'm thinking about integrating qmd (see https://github.com/tobi/qmd) into bob or my
Obsidian vault somehow (agent instructions to use it when searching my Obsidian vault,
for example). Can you do some research with the goal of helping me decide the best way
to implement this? Also, critique this plan in general. Is this a good idea? Would you
take a different approach? Make any adjustments to the requirements that you think are
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

# Research Report & Proposal: Integrating `qmd` into Bob and the Obsidian Vault

**Researcher:** `research.1p.gem` (Swarm Member)  
**Report Path:** [`sase/repos/research/202610/qmd_obsidian_vault_search_integration__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/qmd_obsidian_vault_search_integration__gem.md)  
**Artifact ID:** `explicit:53b82f982709042387d65d6e` (`research:202610/qmd_obsidian_vault_search_integration__gem.md`)

---

## Executive Summary & Strategic Verdict

Integrating Tobias Lütke's **`qmd`** ([github.com/tobi/qmd](https://github.com/tobi/qmd)) into your ecosystem is a **compelling, high-value initiative**, but **only when strictly bounded to conceptual knowledge and reference retrieval**.

`qmd` delivers a local retrieval pipeline that solves the classic dilemma between keyword search (missing conceptual synonyms) and pure vector search (missing exact terminology, code identifiers, and tags). By combining **SQLite FTS5 (BM25)**, **dense vector search (`sqlite-vec`)**, a **fine-tuned 1.7B query expansion LLM**, and a **0.6B local cross-encoder reranker** fused via **Reciprocal Rank Fusion (RRF)**, it significantly outperforms `ripgrep` for associative knowledge discovery across years of notes.

However, a naive integration (e.g. telling agents to run `qmd query` via the CLI or pointing it at your task ledger) introduces severe operational friction. Below is the critique, required adjustments, and recommended architecture.

---

## Critique of the Plan: Strengths & Fatal Pitfalls

### 1. Where `qmd` Shines
- **Bridging the Semantic Gap:** When researching concepts ("how do we handle task decay after repeated review keeps?", "literature on query expansion"), keyword search (`rg`) fails if your query uses words different from what you wrote months ago. `qmd` consistently surfaces the exact relevant document in the top 3 results.
- **Context Trees (`qmd://`):** Allows tagging directory hierarchies with semantic intent (e.g. `qmd context add qmd://vault/ref "Literature notes and reading summaries"`), providing structural grounding that LLMs use to weigh results.
- **First-Class Agent Orientation:** Built with native MCP server support (`qmd mcp --http`), structured JSON AST filtering (`qmd.metadata`), line-range excerpt fetching (`:from:count`), and byte-capped batch retrieval.
- **100% Local & Private:** Runs entirely on-device via GGUF models and `node-llama-cpp`. No OpenAI API keys, zero cloud egress, and complete privacy for personal notes.

### 2. Critical Pitfalls & Friction Points
1. **The Cold-Start CLI Trap (1.5–3.5s per turn):**  
   If an agent executes `qmd query` as a standalone CLI command, `node-llama-cpp` must initialize and load ~2.1 GB of GGUF models into RAM/VRAM on *every single invocation*. In multi-step agent workflows, this causes unacceptable latency and burns GPU/CPU memory bandwidth.
2. **The Task & GTD Mismatch:**  
   Your vault contains dynamic state machines: tasks with derived statuses, sticky lanes, date marks, and Pomodoro blocks (`task-status-is-derived`, `today-is-read-from-the-ledger`). `qmd`'s chunker splits lists, strips line context, and has no concept of active vs. archived GTD state. **`qmd` must never touch tasks or the Pomodoro ledger.**
3. **The Index Staleness Problem:**  
   `qmd` is not an in-memory live watcher; it relies on an offline SQLite database. If notes are captured or edited and `qmd update` has not run, the search index is stale. However, re-embedding (`qmd embed`) 2,000+ notes on every edit is computationally prohibitive.
4. **Platform Heterogeneity:**  
   On macOS with Apple Silicon, Metal inference is nearly instantaneous. On headless Linux servers (such as `apollo` or `athena`), running 1.7B expansion + 0.6B reranker on CPU can trigger CPU saturation (as documented in recent system incident reports).
5. **Architectural Boundary:**  
   `bob-cli` is pure Rust. `qmd` is Node.js/Bun. Rewriting `qmd` in Rust or vendoring Node inside `bob` would violate Bob's clean, zero-dependency architecture.

---

## Justified Adjustments to the Requirements

1. **Strict Domain Boundary (Ban Tasks from QMD):**  
   Explicitly exclude `done/**`, `xlib/**`, `.obsidian/**`, and `day.md` from `qmd` indexing. Instruct agents that `qmd` is strictly for **knowledge and references**; task and schedule queries remain the exclusive domain of `bob task`, `bob plan`, and `bob query --tasks`.
2. **Mandatory Daemonization (`qmd mcp --http --daemon`):**  
   Never invoke standalone CLI inference in agent turns. Run the daemon on localhost:8181 so models remain warm in VRAM, bringing search latency down from 3 seconds to **under 300 milliseconds**.
3. **Decouple Fast Lexical Sync from Heavy Vector Embedding:**  
   Run `qmd update` (FTS5 keyword re-indexing, <500ms) automatically during `bob nightly` and git sync hooks. Defer heavy `qmd embed` (vector embedding) to off-peak scheduled batches or on-demand runs.
4. **Hierarchical Context Annotations:**  
   Configure explicit context strings for `ref/`, `projects/`, `areas/`, `articles/`, and `decisions/` to maximize retrieval precision.

---

## The Recommended Architecture: Three-Tier Vault Retrieval

```
 [Tier 3: Consumers]
       ├─► SASE Autonomous Agents ─────► MCP Tool: qmd_vault (:8181/mcp)
       └─► Human Terminal (Bryan) ─────► bob search <query> (Rust CLI)
                                                │
 [Tier 2: Service Layer]                        ▼ (HTTP Client)
       └─► qmd HTTP Daemon (:8181) ◄────────────┘
             ├── Models Warm in VRAM (~2.2 GB):
             │   ├── embeddinggemma-300M
             │   ├── qwen3-reranker-0.6B
             │   └── qmd-query-expansion-1.7B
             └── SQLite Index: ~/.cache/qmd/index.sqlite
                   ▲
 [Tier 1: Maintenance]
       ├─► bob nightly ────────► runs `qmd update` (instant FTS sync)
       └─► weekly / manual ────► runs `qmd embed`  (vector generation)
```

1. **Tier 1 (Service & Storage):**  
   Run `qmd mcp --http --port 8181` as a user daemon (managed via `launchd` on macOS and `systemd --user` on Linux). Configure `~/.config/qmd/index.yml` with Bryan's vault collection, ignore rules, and path contexts.
2. **Tier 2 (Unified CLI Facade):**  
   Add a native `bob search <query>` subcommand to `bob-cli` in Rust. It queries the local daemon at `http://localhost:8181/query`, prints formatted terminal output with clickable OSC 8 file hyperlinks, and falls back gracefully to `rg` if the daemon is offline.
3. **Tier 3 (Agent Enablement):**  
   Register the MCP endpoint in SASE/Antigravity and deploy a dedicated skill (`/sase_vault_search`). The skill enforces strict domain rules (no tasks) and exposes structured hybrid retrieval to agents.
4. **Maintenance Automation:**  
   Hook `qmd update` into `bob nightly` so newly synced and archived notes are indexed every night without user intervention.

---

## Implementation Roadmap

- **Phase 1: Setup & Configuration**  
  Install `@tobilu/qmd` via Bun/npm, configure `~/.config/qmd/index.yml` with vault ignore rules and context hierarchy, and perform initial FTS indexing and vector embedding.
- **Phase 2: Daemonization & Nightly Hook**  
  Create the `launchd` / `systemd` user service for `qmd mcp --http --port 8181` and insert `qmd update` into `bob nightly`.
- **Phase 3: SASE Agent Skill & MCP Registration**  
  Configure the `qmd_vault` MCP server in Antigravity / Claude Code / Gemini CLI and publish `/sase_vault_search` with strict task guardrails.
- **Phase 4: `bob search` Rust Subcommand**  
  Implement the `bob search` facade in `bob-cli` with HTTP query dispatch and ripgrep fallback.

The complete research report with full technical schemas, configuration templates, benchmark evaluations, and failure mode remediations is recorded in [qmd_obsidian_vault_search_integration__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/qmd_obsidian_vault_search_integration__gem.md).
