# Chat History - ace-run (research.1k.gem)

- **TIMESTAMP:** 2026-10-15 14:19:58 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.1k.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261015_140531.md`

## Prompt

%id(gem, clan=research.1k)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.1k.cdx`, `research.1k.cld`, `research.1k.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I
would like to add a new `bob ref rename` command and a corresponding keymap in the
bob-mac-capture app's ref panel that allows you to rename the currently selected
reference. For example, I would like to use this to rename the
442a6bf555914893e9891c11519de94f.pdf file, which was clearly misnamed.

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

### Research Summary: `bob ref rename` Command & Bob Mac Capture Ref Panel Keymap

I have completed the independent investigation into adding a `bob ref rename` CLI command and a corresponding keymap in the Bob Mac Capture ref panel, using `ref/blogs/442a6bf555914893e9891c11519de94f.md` (`karpathy/llm-wiki.md`) as the primary case study.

The full research report has been written to:
`/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/ref_rename_command_and_panel_keymap__gem.md`

And registered as durable artifact:
- **Ref:** `file:explicit:53bc4ba4df5b9784493284c8`
- **Label:** `research:202610/ref_rename_command_and_panel_keymap__gem.md`

---

### Key Findings & Analysis

#### 1. Why Did `442a6bf555914893e9891c11519de94f.pdf` Happen? (Root Cause)
The reference originated from clipping `https://gist.github.com/karpathy/442a6bf555914893e9891c11519de94f`.
- In `src/native/highlights_ref/clip_url.rs`, `stem_from_url()` examines URL path segments in reverse (`["karpathy", "442a6bf555914893e9891c11519de94f"]`).
- `stem_from_segment()` checks whether candidate segments are all digits, dates, or skipped stopwords. Because the 32-character Gist ID contains hex characters (`a`, `b`, `d`, `e`, `f`), it bypassed `chars().all(|c| c.is_ascii_digit())`.
- As a result, the hex hash was accepted as the filename stem, ignoring the page's actual extracted title (`karpathy/llm-wiki.md`). This hash propagated across:
  - `lib/blogs/442a6bf555914893e9891c11519de94f.pdf`
  - `ref/blogs/442a6bf555914893e9891c11519de94f.md`
  - PDF page 1 `/Text` annotation marker (`- id: 442a...`)
  - Parent reading task in `sase.md`: `- [ ] #task #ref [[ref/blogs/442a...|karpathy/llm-wiki.md]] ... ^ref-442a6bf555914893e9891c11519de94f`
  - Body embed in the ref note: `![[sase#^ref-442a6bf555914893e9891c11519de94f]]`

#### 2. Critique of the Plan: Is This a Good Idea?
**Yes, but a simple file rename is disastrous.** In Bob, a reference is a tightly coupled **5-tier synchronization graph**:
1. **Tier 1 (Library Assets):** The PDF in `lib/`, companion audio (`.mp3/.m4a`), and Highlights sidecars (`.textbundle/.md`).
2. **Tier 2 (Ref Note):** The note in `ref/` with strict 1:1 filename binding (`io.rs:ref_note_path`), frontmatter (`source_pdf`, `id`, `highlights_marker_base`), and extracted image assets (`ref/<type>/<stem>.assets/`).
3. **Tier 3 (PDF Marker Binary):** Embedded page-1 `/Text` annotation dictionary parsed and written via `lopdf`.
4. **Tier 4 (Parent Reading Task):** The v2 reading task in `sase.md`.
5. **Tier 5 (Vault Graph & Backlinks):** Wikilinks and Pomodoro ledger references pointing to the task block ID (`^ref-<slug>`).

**The "Phantom Duplicate" Trap:** `bob ref scan` binds PDFs to ref notes strictly by relative path. If a rename only moves the PDF or ref note without updating the parent reading task in `sase.md`, `RefTaskIndex` will find zero candidate tasks for the new note path on the next scan. `scan` will conclude the reference is an unindexed birth, **inserting a duplicate reading task** in `sase.md` while leaving the old task orphaned.

---

### Recommended Adjustments to Requirements

1. **Transactional Multi-Entity Scope:** `bob ref rename` must execute an atomic transaction across all 5 tiers (PDF, note, marker, frontmatter, body embed, and parent reading task).
2. **Vault-Wide Graph Rewrite Integration:** Adapt the graph rewrite engine from `src/native/ref_library/migrate_tasks/rewrite.rs` to automatically update all wikilinks (`[[ref/<type>/<old_stem>]]`) and task block IDs (`^ref-<old_slug>`) across the entire vault.
3. **Capture-Time Hash Filter (Prevention):** Update `clip_url.rs:stem_from_segment()` to reject hex hashes (`^[0-9a-fA-F]{16,64}$`) and UUIDs. This forces Gists, arXiv numbers, and hash endpoints to automatically fall back to the extracted document title (`karpathy-llm-wiki`) at birth.
4. **Distinguish Stem vs. Title Renaming:** Provide both stem renaming (the filename slug) and title updating:
   `bob ref rename <REF> <NEW_STEM> [-t|--title <TITLE>]`.

---

### Architectural Design & Recommended Solution

#### CLI Engine: `bob ref rename`
- **Location:** Under the `Library` subcommand group in `src/native/highlights_ref/cli.rs`.
- **Target Resolution:** Reuses `crate::native::ref_library::resolve::resolve_query()`, allowing references to be specified by stem, relative path, or search query.
- **Execution Stages:**
  1. *Preflight:* Validate source, sanitize target stem, verify target paths do not exist in `lib/`, `xlib/`, or `ref/`, check clean git worktree.
  2. *Filesystem Move:* Move PDF, companion audio, sidecars, and `.assets/` directory.
  3. *PDF Marker Rewrite:* Update `id` in the page-1 `/Text` annotation and resave atomically using `lopdf`.
  4. *Ref Note Rewrite:* Update `id`, `source_pdf`, `highlights_marker_base`, body embed (`![[<parent>#^ref-<new_slug>]]`), write new note, remove old note.
  5. *Parent Reading Task Mutation:* Update `[[ref/...]]` link target and block ID in `sase.md`.
  6. *Vault Graph Rewrite:* Rewrite all markdown backlinks and pomodoro ledger citations across the vault.

#### Bob Mac Capture Ref Panel Integration
- **Thin Client Compliance (Decision 6):** Bob Mac Capture never moves files directly; it dispatches `bob ref rename <path> <new_stem> --format json` via `BobProcessClient`.
- **Keymap:** `⇧⌘R` (Shift-Command-R) in `Sources/BobMacCapture/Refs/RefsKeyRouter.swift`. (Avoids colliding with `Cmd+R`, which is Refresh Library).
- **⌘K Action:** Add `"Rename Reference…"` (`⇧⌘R`) to Section 1 of `RefsActionsMenu.swift`.
- **UI Flow (`RefsRenameCardView`):**
  - Smoothly replaces the inspector column on `⇧⌘R`.
  - Shows current filename (`442a6bf555914893e9891c11519de94f.pdf`) and title (`karpathy/llm-wiki.md`).
  - Pre-populates the input field with an **intelligently derived slug from the title** (`llm-wiki`).
  - `Return` submits the rename; `Esc` cancels.
  - On completion, shows a toast banner (`"Renamed to llm-wiki"`), updates panel selection, and refreshes the catalog.
