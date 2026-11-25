# Chat History - ace-run (research.6f.gem)

- **TIMESTAMP:** 2026-11-25 16:37:43 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6f.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261125_161645.md`

## Prompt

%id(gem, clan=research.6f)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6f.cdx`, `research.6f.cld`, `research.6f.grk`, `research.6f.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

When a task, say A, has a dependency on another task, say B, then A should not also have
a relationless link to the same task (in either direction). I would like to make this
invalid/confusing state impossible.

- When adding a relationless link to a task B, we should remove any existing dependency
  to task B from the current task. Similarly, when adding a dependency to a task B, we
  should remove any existing relationless link to task B from the current task.
- We should add the `<ctrl+b>` keymap to the link panel in Obsidian, which should be
  able to be used to mark the task as a dependency instead of linking to it. We should
  also be able to do the reverse (make a dependency a relationless link) from the
  dependency panel in Obsidian.
- Make sure it is clear when looking at the dependency/link panels in Obsidian if the
  task already has a relationless link/dependency, respectively.
- I want you to lead the design on this one. Make sure you design this feature so it is intuitive, reliable, and (last but not least) beautiful!

Can you do some research with the goal of helping me decide the best way to implement
this? Also, critique this plan in general. Is this a good idea? Would you take a
different approach? Make any adjustments to the requirements that you think are
justified but clearly call these out. End your analysis with a recommended solution. 
First run `sase repo open research -r "Write this research report"` and use the path it prints as `<research checkout>`. Write this research to a new markdown file under `<research checkout>/202611/`.
Choose a descriptive filename stem yourself, but the filename MUST end with the
`__gem` suffix, i.e. `<stem>__gem.md` (double underscore before the
suffix). Create the report without overwrite: if the exact file already exists, pick a
different stem instead of replacing it.


After the write succeeds, register the report as a durable snapshot:

sase artifact create -p "<absolute-report-path>" -l "research:<repo-relative-report-path>"

Use the report's actual absolute path under the opened research checkout and its path relative to the research repo root
(for example
`research:202609/topic__a.md`),
including any subdirectory the steps above put it in. Do not derive the label from
the current month, the clock, or a guessed name.
Do not pass `--move`; the source stays in the research repo for later reorganization. If
registration itself fails, report that failure — do not report the research task as
fully complete.

## Response

I completed the research and wrote the full design report to [task_dependency_plain_link_mutual_exclusion__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/task_dependency_plain_link_mutual_exclusion__gem.md), registered as durable SASE artifact `file:explicit:62c6e1359669cbfe1dced05d` (`research:202611/task_dependency_plain_link_mutual_exclusion__gem.md`).

### Verdict & Core Critique

**The goal is sound and matches Bob's graph model**, directly paralleling the existing M7 mention-suppression rule (`docs/task-relations.md` §19.2) while keeping labelled relations legal (live vault has 263 labelled links across 14 labels such as `implemented by`, `superseded by`, `inspired by`, and `merged into`).

However, **implementing the rule symmetrically as literal silent auto-replacement has a major safety trap**: upgrading a plain link to a dependency is lossless and inert, whereas silently *removing* a dependency when adding a plain link violates **Relations Inertness** (`LR18`), can accidentally unblock a task or an entire `^prj` project + sub-projects, can unblock a remote task `B` from `A`'s Links panel, and can erase completed prerequisite history (`done/` is also read-only under `LR7`).

### Key Justified Adjustments (Called Out in the Report)

1. **A1 — Asymmetric Guarded Replacement**:
   - **Upgrade (`plain link → dependency`)**: Auto-strips unlabelled `LINKS:` in either direction silently (`Depends on`/`Blocks` `↵`, `Links`/`Linked from` `Ctrl+B`, and `bob capture` `&`/`*`).
   - **Demotion (`dependency → plain link`)**: 1-keystroke explicit via `Ctrl+L` in `Depends on`/`Blocks`; **2-press inline-confirmed** (`↵` arms amber strip, `↵` confirms, `Esc` disarms) in `Links`/`Linked from`—reusing Bob's existing `superseded by` / `merged into` confirmation pattern; **refused with a teaching error** on unlabelled `bob capture ~`/`~~` (while labelled `~...|label` stays 1-step everywhere).
2. **A2 — Full 4-Panel Arrow-Preserving Symmetry**:
   - Wire `Ctrl+B` in both `🪢 Links` (`A → B` ⇒ `A` depends on `B`) and `🪢 Linked from` (`B → A` ⇒ `A` blocks `B`, including `💬 mention` promotion).
   - Wire `Ctrl+L` in both `⛓ Depends on` (`A → B` ⇒ plain link `A → B`, also usable on `RESULTS`/cycle rows) and `🧱 Blocks` (`B → A` ⇒ arrow-preserving plain link `B → A`, keeping exact round-trip symmetry with `Linked from + Ctrl+B` and collapsing `B`'s `DEPENDS ON` removal + `LINKS` add into one single write).
3. **A3 — Open-Dependent Scope**: Enforce the invariant whenever the dependent `D` is open (blocking plain links on `D`, and on `P` when `P` is also open). Closed/archived dependents remain frozen history (`⛓ done prereq` muted pill).
4. **A4 — Close Every Non-Obsidian Backdoor**:
   - Disable `"Plain link (no relation)"` in the `⌃↵` label stage (`428-picker-relation-label-vocabulary.js`) when an active dependency joins the pair.
   - Enforce in `bob capture`, `bob task merge` (when repointing dependents), and a convergent cleanup pass in `bob task reconcile` (`src/native/task_status_hooks/relations.rs`) where **dependency always wins** over redundant plain `LINKS` on writable well-formed notes.
5. **A5–A7 — Visual Parity & Codebase Fixes**:
   - Add the missing fixed-height `.bob-cnp-consequence-strip` to `⛓ Depends on`.
   - Fix the 190px clipping bug on `.bob-cnp-task-badge` (`styles.css:774-791`) by splitting semantic micro-pills (`.bob-cnp-dep-extras`) from the right-edge action glyph (`＋`/`−`/`⇄`), using accent pills for safe plain-link upgrades and amber pills for active dependencies.
   - Fix `isCtrlKey` (`470-keydown-and-freshness.js:35`, missing `!event.shiftKey`) and `reopenDependencyStageFresh()` (`440-picker-vault-commit.js:18-23`, currently reopens `Depends on` on stale conflicts in Link panels).
   - Compose Obsidian cross-relationship edits into **one CodeMirror transaction** on the anchor note (`1× Ctrl+Z`) and **at most one `vault.process`** per remote note, using zero-disk-I/O indices (`api.relationIndex` v2 and in-memory `edges`).

### Recommended Solution

Adopt **Option 4 (Asymmetric Guarded Replacement + 4-Panel Arrow-Preserving Conversion + Convergent Reconcile Backstop)** in four phases detailed in §8 of [task_dependency_plain_link_mutual_exclusion__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/task_dependency_plain_link_mutual_exclusion__gem.md):
1. Decision record + `docs/task-relations.md` / `docs/task-dependencies.md` contract & **LM1–LM12** conformance vectors.
2. `bob-cli` enforcement (`reconcile_relation_lines`, `capture`, `task merge`, additive `capture-complete` fields).
3. `bob-plugins` 4-panel visual polish, composed transactions, `Ctrl+B`/`Ctrl+L`, and bug fixes.
4. `bob-mac-capture` badge parity using the additive `capture-complete` metadata.
