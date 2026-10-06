# Chat History - ace-run (research.3s.gem)

- **TIMESTAMP:** 2026-10-06 15:11:25 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3s.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261006_145643.md`

## Prompt

%id(gem, clan=research.3s)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3s.cdx`, `research.3s.cld`, `research.3s.grk`, `research.3s.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to migrate the `bob highlights` command to a new `bob ref` command that
supports all of the same commands that the `bob highlights` command currently does but
also adds new commands that make it easy for agents (and myself) to see what references
I have read, which I am tracking / plan to read, which I've finished reading, etc...

- The main use-case for this command would be for agents that are recommending new
  reading material for me (these agents would find it useful to know what articles /
  papers I have already read).
- With that said, I also think it would be useful to be able to read the annotations
  that I left on these reference PDFs (using the Highlights app on my macbook). These
  are automatically written to markdown files in the ~/bob/ref/ directory.

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

# Research Summary: Migrating `bob highlights` to `bob ref`

**Researcher:** `research.3s.gem`  
**Report File:** [`bob_ref_command_migration__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/bob_ref_command_migration__gem.md)  
**Registered Artifact:** `research:202610/bob_ref_command_migration__gem.md` (`file:explicit:0a737d5c9f1a1bc82b1b4bdd`)

---

## 1. Executive Recommendation & Core Critique

### Is this a good idea?
**Yes, strongly.** Migrating `bob highlights` to `bob ref` corrects a fundamental conceptual misnomer in the Bob CLI:
- **"Highlights" is merely an external capture app**, whereas the first-class domain entity across the Bob vault is the **Reference Note** (`type: "[[ref]]"`, `^ref` task, and the `REFERENCES` freshness morning review tier).
- The existing `bob highlights` command suite was an **inbound-only pipeline** (`clip`, `create`, `scan`, `sync`) with **zero query or inspection capabilities**. Adding reading tracking and annotation retrieval closes the loop and empowers coding agents to perform intelligent literature deduplication and context retrieval.

### What should be adjusted or taken differently?
Our empirical audit of Bryan's vault (`~/bob/ref/` containing 590 reference notes) revealed critical architectural realities that require adjustments to the plan:

1. **Decouple "Reference" from "PDF":**
   - Out of 590 reference notes in `~/bob/ref/`, 308 are modern Highlights-managed notes with local PDFs, but **282 are legacy notes** without local PDFs.
   - The query and tracking commands (`list`, `find`, `show`) must operate over reference notes as knowledge entities, regardless of whether a companion PDF exists in `lib/`.
2. **Avoid the Ambiguous Verb `bob ref read`:**
   - In CLI grammar, `read` could mean: (a) mark as read (mutation), (b) read note text/annotations (inspection), or (c) list read items (query).
   - Use clear, unambiguous verbs:
     - `bob ref list`: Browse/filter reference backlog (`--status read|ready|wip|next|all`).
     - `bob ref find`: Check / deduplicate a reference by URL, ArXiv ID, DOI, or title.
     - `bob ref show`: Inspect metadata and extract callout annotations (`[!quote]`, `[!note] Comment`).
3. **Resolve the Dual-Status Disparity (Unified Status Normalizer):**
   - Modern notes use `status: read` and `- [x] #task #ref ... ^ref` (285 read, 17 abandoned, 5 next, 1 ready).
   - Legacy notes use `status: legacy` and `legacy_status: unread` (144 unread, 92 collect fleeting notes, 25 read, 13 review fleeting).
   - A naive query for `status: ready` would return only 1 note and miss 144 unread legacy articles. `bob ref` must implement a unified status projection layer mapping modern and legacy statuses into canonical buckets (`read`, `ready`/`unread`, `wip`, `next`, `abandoned`).
4. **Fix the `url` vs `source_url` Defect:**
   - Across the vault, **283 notes store external URLs under `url:`**, while **only 2 notes use `source_url:`**.
   - The existing `clip.rs` deduplication scanner strictly checks `source_url:`, making it blind to 99% of existing vault references! The migration must treat `url` and `source_url` symmetrically.
5. **Academic URL Normalization for Agents (ArXiv & DOI):**
   - Agents frequently cite ArXiv papers interchangeably using `/abs/`, `/pdf/`, or bare ArXiv IDs. `bob ref find` must extract and match canonical ArXiv IDs and DOIs.
6. **Strict CLI Rule Compliance via Hidden Aliases:**
   - Per `cli_rules.md`, `bob highlights` must remain a permanent hidden alias in `src/runner.rs:ALIASES` forwarding byte-identically to `bob ref`. Existing LaunchAgents and maintenance hooks (`bob highlights scan`) will continue working with zero disruption.

---

## 2. Why Not Just Use `bob query` (Dataview)?

`bob query` executes DQL or Tasks queries against the Bob vault, but is unsuitable for this workflow:
- **Latency:** `bob query` initializes the whole-vault graph (~4.2 seconds on `~/bob`, emitting 16 link ambiguity warnings on stderr). In contrast, a native Rust scanner traversing `~/bob/ref/` executes in **12–15 milliseconds**, essential for responsive agent turns.
- **Domain Incompetence:** Dataview reads raw frontmatter fields without understanding that the `^ref` task checkbox is authoritative over frontmatter, cannot normalize legacy statuses, cannot parse callout annotations from `<!-- highlights:begin -->`, and cannot normalize ArXiv URLs.
- **Agent Token Overhead:** A single command `bob ref find --url <URL> -f json` eliminates complex prompt assembly and AST parsing.

---

## 3. Specification of the Recommended `bob ref` Suite

```text
bob ref
├── Catalog & Knowledge (New)
│   ├── list       # List references with --status, --ref-type, --topic, -f json
│   ├── find       # Deduplicate/find by URL, ArXiv ID, DOI, or title (-f json)
│   └── show       # Display metadata and extract Highlights callout annotations (-f json)
└── Lifecycle Sync (Preserved from `bob highlights`)
    ├── clip       # Clip web article into intake PDF (xlib/blogs/)
    ├── create     # Render Markdown file into Highlights PDF (xlib/chat/)
    ├── doctor     # Check vault reference paths, hooks, and Git status
    ├── marker     # Inspect page-1 standalone /Text PDF marker
    ├── scan       # Move intake to library, pair audio, and sync notes
    └── sync       # Synchronize one PDF marker with its reference note
```

### Key Subcommand Details

1. **`bob ref list`**
   - **Usage:** `bob ref list [-s <status>] [-r <ref-type>] [-t <topic>] [-f human|json]`
   - **Default:** Shows reference reading queue (summary table or JSON).
   - **Filter:** `-s read`, `-s ready` (includes legacy unread), `-s wip`, `-s next`, `-s abandoned`, `-s all`.

2. **`bob ref find` (The Agent Deduplication Primitive)**
   - **Usage:** `bob ref find [QUERY] [-u <URL>] [-a <ARXIV_ID>] [-d <DOI>] [-f human|json]`
   - **Exit Codes:** `0` (match found), `1` (not found), `2` (error).
   - **JSON Contract (`-f json`):**
     ```json
     {
       "found": true,
       "match_kind": "arxiv_id",
       "query": "https://arxiv.org/abs/2608.04278",
       "reference": {
         "path": "ref/papers/ea_graph.md",
         "title": "EA-Graph: Artifact-Anchored Verification Memory...",
         "status": "read",
         "ref_type": "papers",
         "url": "https://arxiv.org/pdf/2608.04278",
         "source_pdf": "lib/papers/ea_graph.pdf",
         "highlights_count": 1,
         "has_annotations": true
       }
     }
     ```

3. **`bob ref show` (Annotation Extraction & Intelligence)**
   - **Usage:** `bob ref show <REF_OR_PATH> [-a|--annotations-only] [-f human|json|markdown]`
   - **Logic:** Isolates `<!-- highlights:begin -->` to `<!-- highlights:end -->` and extracts structured quotes (`[!quote]`), user comments (`[!note] Comment`), images, and `^h-...` block IDs.
   - **JSON Contract (`-f json`):**
     ```json
     {
       "path": "ref/blogs/steve_kinney_agent_memory.md",
       "title": "steve kinney agent memory",
       "status": "read",
       "highlights_count": 30,
       "annotations": [
         {
           "page": "Page 2",
           "kind": "quote",
           "text": "The survey proposes a threeaxis framework...",
           "comment": ":)",
           "block_id": "h-ce8e46d5cb2c"
         }
       ]
     }
     ```

---

## 4. Implementation Roadmap

1. **Phase 1: Canonical Renaming & Backward-Compatible Aliasing**
   - Refactor `src/native/highlights_ref/` to `src/native/reference/`.
   - Mount `ref` in `src/runner.rs` under `Section::TasksAndProjects` (or `Section::Vault`).
   - Add `Alias { from: "highlights", to: &["ref"] }` in `src/runner.rs:ALIASES`.
   - Fix the `source_url` vs `url` defect in `clip.rs`.
2. **Phase 2: Reading Tracking & Search Engine (`list` and `find`)**
   - Implement `status.rs` for unified modern/legacy status projection.
   - Implement `url_norm.rs` for ArXiv ID extraction, DOI normalization, and URL query cleaning.
   - Implement `bob ref list` and `bob ref find` with strict `-f json` schemas.
3. **Phase 3: Annotation Parsing & Extraction (`show`)**
   - Implement `annotation.rs` to parse callout blocks between `<!-- highlights:begin -->` and `<!-- highlights:end -->`.
   - Expose `bob ref show` with `--annotations-only` and `-f json`.
   - Update documentation in `docs/highlights-ref-sync.md`.

---
*The full detailed report, including code structures, vault census metrics, and schema definitions, is available at [`bob_ref_command_migration__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_16/sase/repos/research/202610/bob_ref_command_migration__gem.md) and registered in SASE storage as `research:202610/bob_ref_command_migration__gem.md`.*
