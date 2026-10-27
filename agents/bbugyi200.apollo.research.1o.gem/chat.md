# Chat History - ace-run (research.1o.gem)

- **TIMESTAMP:** 2026-10-16 09:36:03 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.1o.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261016_092509.md`

## Prompt

%id(gem, clan=research.1o)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.1o.cdx`, `research.1o.cld`, `research.1o.grk`, `research.1o.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

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
want a way to specify that a particular markdown file in my vault should always be
treated as an article / design doc / some content with sections.

- This will allow us to treat (e.g. format) these files differently from other note
  files in my Obsidian vault.
- For example, the ~/bob/sase_blog_contents.md file is one of these notes.
- As our first use-case, I would like to start auto-formatting (think hard about what
  formatting rules to apply) these files and auto-numbering (starting at 1 with support
  for sub-sections) the sections contained within these files.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

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

# Research Report: Vault Article & Design Doc Specification, Auto-Formatting, and Section Numbering

**Researcher:** `research.1o.gem`  
**Report File:** [`vault_article_docs_auto_formatting_and_section_numbering__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/vault_article_docs_auto_formatting_and_section_numbering__gem.md)  
**Artifact ID:** `explicit:89cb5af3f63c17dd0176ba52` (`research:202610/vault_article_docs_auto_formatting_and_section_numbering__gem.md`)

---

## 1. Executive Summary & Core Conclusion

In Bryan's Obsidian vault (`~/bob/`), notes primarily serve an operational GTD workflow driven by `bob-cli` (tasks, `^prj` lines, Pomodoro ledgers, schedule logs). Because this syntax is fragile, generic markdown formatters like `obsidian-linter` have been intentionally disabled vault-wide.

However, notes such as [`~/bob/sase_blog_contents.md`](file:///home/bryan/bob/sase_blog_contents.md) represent long-form prose and technical design documents. Treating them identically to task scratchpads produces formatting inconsistencies, fragmented footnotes, and unnumbered outlines.

We propose a **three-part solution**:
1. **Unambiguous Specification via Frontmatter:** Designate article/doc notes with `type: "[[article]]"` (or `type: "[[design-doc]]"`), perfectly matching existing vault taxonomy (`type: "[[project]]"`, `type: "[[area]]"`).
2. **Dedicated 10-Rule Auto-Formatting Suite:** Enforce clean vertical rhythm, smart title capitalization, table alignment, and footnote consolidation without corrupting task block IDs or code fences.
3. **Idempotent Section Auto-Numbering (`1`, `1.1`, `1.1.1`):** With intelligent document title auto-detection and section skipping (`Contents`, `References`, `Appendix`).
4. **Hybrid Architecture:** A fast, headless CLI engine in `bob-cli` (`bob doc format`) coupled with an interactive Obsidian plugin in `bob-plugins` (`bob-doc-tools`) and a `.bob-article` CSS typography layout.

---

## 2. Critique of the Plan

### Is This a Good Idea?
**Yes.** Scoping formatting to designated document notes solves the "one linter to rule them all" failure mode. It cleanly separates the *project tracking* note ([`sase_blog.md`](file:///home/bryan/bob/sase_blog.md)) from the *document content* note ([`sase_blog_contents.md`](file:///home/bryan/bob/sase_blog_contents.md)).

### Critical Pitfalls Identified
1. **The Broken Inbound Link Trap:** Physically mutating heading text (e.g. `## The Abstractions` &rarr; `## 1 The Abstractions`) breaks inbound wikilinks (`[[sase_blog_contents#The Abstractions]]`) across the vault.
2. **Git Diff Noise Explosion:** Reordering or inserting an early section rewrites every subsequent heading in the document, polluting git blame and commit histories.
3. **Editing Friction:** Polling every 10 seconds (as plugins like `number-headings-obsidian` do) disrupts typing, jumps the cursor, and destroys undo history.
4. **Task & Metadata Collateral Damage:** Generic formatters inadvertently damage inline task items (`- [ ] #task ...`), schedule logs, and caret block anchors (`^write-intro`).

### Justified Requirement Adjustments
* **Dual-Mode Numbering:** Virtual numbering in Obsidian (via CodeMirror 6 / CSS) keeps raw markdown clean and links unbreakable; physical numbering can be applied or "baked" via an explicit command for external static export.
* **Anchor Generation for Renumbered Headings:** Automatically append stable block IDs (e.g. `## 1.1 Gates -> Plans -> Epics ^gates-plans-epics`) so inbound links never break even when section numbers change.
* **Intelligent Document Title Detection:** If a document begins with a single H1, treat it as an unnumbered Document Title and begin numbering at H2 (`1.0`); if multiple H1s exist, begin numbering at H1 (`1.0`).
* **Footnote Relocation:** Automatically consolidate scattered inline footnote definitions (`[1]: ...`) to a dedicated `## References` section at the end of the document.
* **Event-Driven Formatting:** Trigger formatting explicitly (`Cmd+Shift+F`), debounced on save, or during `bob nightly` / pre-commit, never on arbitrary background timers.

---

## 3. Specification & Schema

### Zero-Configuration Baseline
Any note with `type: "[[article]]"` or `type: "[[design-doc]]"` receives standard formatting and numbering defaults:

```yaml
---
parent: "[[sase_blog]]"
type: "[[article]]"
created: 2026-10-15T15:10:41-04:00
---
```

### Optional Customization Block
```yaml
---
parent: "[[sase_blog]]"
type: "[[article]]"
article:
  numbering: true          # true | false | "virtual" | "physical"
  first_level: auto        # auto | 1 | 2
  max_level: 4             # 1 to 6
  separator: " "           # " " ("1.1 Title") or ". " ("1.1. Title")
  skip: ["Contents", "References", "Appendix*"]
---
```

---

## 4. The 10 Auto-Formatting Rules

1. **Heading Spacing & Isolation:** 2 blank lines before H1/H2; 1 before H3-H6; 1 blank line after every heading before body text.
2. **Heading Hierarchy Normalization:** Eliminate illegal level skips (e.g., H2 straight to H4 without H3).
3. **Smart Title Capitalization:** Capitalize principal words while preserving code terms in backticks and technical acronyms (`SASE`, `VCS`, `CLI`, `YAML`).
4. **Paragraph Whitespace Hygiene:** Single blank line between paragraphs; strip trailing whitespace on all lines.
5. **Footnote Consolidation:** Relocate scattered `[^1]: ...` definitions to the bottom of the article under `## References`.
6. **Code Block Hygiene:** Mandatory language identifier on code fences; 1 blank line before and after fences.
7. **List Marker Standardization:** Enforce `-` bullet markers with consistent 2- or 4-space indentation.
8. **Task & Block Anchor Preservation:** Leave `- [ ] #task ...` and trailing caret anchors (`^anchor`) completely untouched.
9. **GFM Table Alignment:** Pad and align column pipes for clean raw plaintext reading.
10. **Frontmatter Integrity Guard:** Enforce `---` delimiters and a trailing blank line before body text.

---

## 5. Walkthrough on `~/bob/sase_blog_contents.md`

Applying this architecture to [`sase_blog_contents.md`](file:///home/bryan/bob/sase_blog_contents.md):
* **Frontmatter:** Adds `type: "[[article]]"`.
* **Footnotes:** Extracts definitions `[1]: ...`, `[2]: ...`, `[a]: ...`, `[b]: ...` from the body and places them cleanly under `## References`.
* **Section Numbering:**
  * `# 1 The Abstractions`
  * `## 1.1 Gates -> Plans -> Epics`
  * `## 1.2 Beads -> Sidecar Repos`
  * `## 1.3 Agent CLIs`
  * `### 1.3.1 Skills, Memory, Provider Interface, NOT Hooks` *(normalized from H4 to H3)*
  * `### 1.3.2 Agent Presentation / Organization...` *(normalized from H4 to H3)*
  * `## 1.4 VCS and Workspace Operations`
  * `## 1.5 Xprompts / Agent Control Flow`
  * `## 1.6 Project Management`
  * `## 1.7 Routines and Jobs`
* **Layout:** Injects `.bob-article` CSS class for centered, comfortable serif reading typography (max-width 740px) with subtle monospace badges for section numbers.

---

## 6. Implementation Roadmap

1. **Phase 1 (Immediate / Zero Risk):** Deploy `type: "[[article]]"` frontmatter and the `.bob-article` CSS typography snippet to `~/bob/.obsidian/snippets/`.
2. **Phase 2 (Core Engine in `bob-cli`):** Implement `bob doc format` and `bob doc number` in Rust for fast, idempotent, headless formatting and CI/nightly checks.
3. **Phase 3 (Obsidian Plugin in `bob-plugins`):** Build `bob-doc-tools` with `Cmd+Shift+F` command, debounced format-on-save, and backlink refactoring coordination.

The full research report has been saved to [`sase/repos/research/202610/vault_article_docs_auto_formatting_and_section_numbering__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_18/sase/repos/research/202610/vault_article_docs_auto_formatting_and_section_numbering__gem.md) and registered as SASE artifact `explicit:89cb5af3f63c17dd0176ba52`.
