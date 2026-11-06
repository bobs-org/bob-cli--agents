# Chat History - ace-run (research.3f.gem)

- **TIMESTAMP:** 2026-11-05 14:04:12 EST
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.3f.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261105_134345.md`

## Prompt

%id(gem, clan=research.3f)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.3f.cdx`, `research.3f.cld`, `research.3f.grk`, `research.3f.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add support for a new `< @foo+f` capture syntax that complements the
existing `> @foo+f` capture syntax.

- This syntax should only be valid in a context that would create a new task.
- When this syntax is used, the task targeted with `@foo+f` (i.e. the `^f` task in the
  ~/bob/foo.md file in this example) will be merged into the newly created task using
  the existing "merged into" task relation label.
- We should be able to specify multiple tasks after the `<` to merge all of those tasks
  into the newly created task.
- For example, the `Some great new task! @foo^great < @foo+f @bar+b` would merge the
  `^b` task in the ~/bob/bar.md file and the `^f` task in the ~/bob/foo.md file into the
  newly created `^great` task (in the ~/bob/foo.md file) by linking them to `^great`
  using the "merged into" task relation label.
- Make sure this syntax supports an excellent and useful (but concise) preview in the
  bob-mac-capture app.
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

# Research & Design: Inward Capture Merge Syntax (`< @foo+f`)

**Author:** Researcher `gem` (Independent 5-Researcher Swarm)  
**Report Artifact:** `research:202611/capture_merge_in_syntax__gem.md`  
**Artifact ID:** `explicit:e2ca92f2141b18277774894a`  
**Stored Snapshot:** `/home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261105134352/capture_merge_in_syntax__gem-fe4800a4be9e.md`

---

## 1. Executive Summary & Verdict

The proposed `< @foo+f` capture syntax introduces **inward task merging** (absorbing existing tasks into a newly authored task). It provides an exact, natural symmetry to the existing outward `> @dest` transfer syntax:

$$\begin{aligned}
\text{Outward Transfer (Existing } \rightarrow \text{ Existing):} \quad & \mathtt{@a+x\ @b+y\ >\ @dest+id} \\
\text{Inward Merge (Existing } \rightarrow \text{ New):} \quad & \mathtt{New\ task\ @dest\string^great\ <\ @a+x\ @b+y}
\end{aligned}$$

### Core Verdict
- **Is this a good idea?** **Yes, absolutely.** During daily capture and triage, users frequently consolidate fragmented inbox captures into a new synthesis or "umbrella" task. Today, doing so requires capturing the new task first and running a secondary `>` transfer line, or writing cumbersome reverse relation directives (`Umbrella ~~a:x|"merged into" ~~b:y|"merged into"`). The `<` operator provides an intuitive, high-speed single gesture.
- **Backend Reusability:** Bob already possesses a battle-tested, transactional task merge engine (`src/native/task_merge/` and `src/native/capture/relations_merge.rs`). Lowering `< @foo+f @bar+b` into the existing relation-merge pipeline reuses 100% of the underlying validation, cycle detection, dependency repointing, link pruning, and tombstoning logic.
- **Frontend / Mac Preview:** By colorizing `<` with Bob's canonical purple merge accent, surfacing a dedicated "Absorbing N tasks" item band, and leveraging existing purple **Merge target** and muted **Merged** landing blocks (`TaskBlockView`), `bob-mac-capture` achieves an elegant, concise, and informative preview.

---

## 2. Key Findings & Requirements Critique

### 2.1 Necessary Refinements & Adjustments

1. **Automatic Block ID Minting**:
   - *Issue*: In drafts like `New task @foo < @bar+b`, the user may omit an explicit `^id`. To write `🪢 LINKS: merged into [[foo#^target]]` on the source tombstone, the target *must* have a block ID.
   - *Adjustment*: When `<` is present and the new task lacks an explicit `^block-id`, Bob must automatically mint one (via `mint_block_id`) from the task title.
2. **Strict Whitespace Delimitation**:
   - *Issue*: `<` appears in everyday prose: math/comparisons (`count < 10`), autolinks (`<https://...>`), HTML tags (`<template>`), and emojis (`<3`).
   - *Adjustment*: The `<` operator MUST be a standalone whitespace-flanked token (` < `) followed immediately by `@route+id` source tokens. Any other `<` remains body prose. Backslash escaping (`\<`) is supported for literal preservation.
3. **Strict Non-New-Task Context Refusal**:
   - *Issue*: What if `< @foo+f` is typed on a sub-bullet line (`@parent+p < @foo+f`), toggle, or completion?
   - *Adjustment*: Silently falling back to prose would append `- < @foo+f` as a Markdown bullet, misleading the user into thinking a merge occurred. Bob must actively refuse non-new-task contexts with `merge_requires_new_task` (`“<” merge syntax is only valid when creating a new task; to merge into an existing task, use transfer syntax (@source+id > @target+id)`).
4. **CLI Shell Quoting Awareness**:
   - *Issue*: In Bash/Zsh, `<` triggers stdin redirection before `bob` executes.
   - *Adjustment*: CLI documentation must explicitly instruct single-quoting (`bob capture 'New task @foo < @bar+b'`), aligning with existing rules for `>`, `*`, `&`, `|`, and `^`. Note that `bob-mac-capture` bypasses shells entirely and is unaffected.
5. **Plural Syntax**:
   - Sources are specified as a space-separated sequence following a single `<`:
     `Some great new task! @foo^great < @foo+f @bar+b @baz+c`

---

## 3. `bob-mac-capture` UI & Preview Architecture

```
┌──────────────────────────────────────────────────────────────────────────────┐
│  New Task → foo.md                              [ 2 tasks merged · purple ]  │
│  ○ Some great new task!                                             ^great   │
├──────────────────────────────────────────────────────────────────────────────┤
│  📥 Absorbing 2 tasks:                                                       │
│     ⊘ ^f · Benchmark logical replication (foo.md:5)    · 3 notes move        │
│     ⊘ ^b · Logical dump script (bar.md:12)             · 1 note move         │
│                                                                              │
│  ↳ 1 open dependent repointed to ^great                                      │
└──────────────────────────────────────────────────────────────────────────────┘
```

1. **Editor Spans & Incomplete State**:
   - `<` is styled with `SpanKind::TransferArrow` or `SpanKind::MergeInArrow`, mapped to `.section` (purple tint).
   - Incomplete `< `: When trailing text is empty, `capture-parse` emits `need: "merge_source"`, rendering an inline prompt (`Pick a task to merge (@route+id)`) rather than an error callout.
2. **Keyboard Autocomplete (`capture-complete`)**:
   - Typing `< @` triggers route suggestions (e.g. `@inbox`, `@work`).
   - Typing `< @foo+` triggers open task selection within `foo.md`.
3. **Item Preview Card**:
   - A purple pill `N tasks merged` highlights the item header.
   - A concise `📥 Absorbing N tasks:` band lists each source locator, origin note, previous status, and moved-line counts.
   - Quiet sub-rows indicate consequence notes (e.g. repointed dependents, pruned Pomodoro links).
4. **Landing Blocks (`TaskBlockView`)**:
   - Targets render with the purple **Merge target** capsule and indented merged notes.
   - Sources render with the muted **Merged** capsule, `[-]` cancelled status, and folded removed notes (`⤵ N lines moved to target`).
5. **Status Line**:
   - Displays: `Would create “Some great new task!” and merge 2 tasks into it · foo.md`.

---

## 4. Implementation Blueprint in `bob-cli`

1. **Scanner (`src/native/capture_language/item.rs` & `transfer.rs`)**:
   - Scan for standalone `< ` in the parent line.
   - Verify new-task context (`CaptureKind::Task`, `TaskWithBlockId`, `Pomodoro`).
   - Parse `@route+block_id` tokens with `transfer::parse_complete_source`.
   - Populate `merge_sources: Vec<TransferSource>` on `ParsedCaptureText`.
2. **Planning & Desugaring (`src/native/capture/plan.rs`)**:
   - If `^block-id` is missing on the target, generate one with `mint_block_id`.
   - Desugar each `TransferSource` into a `ParsedRelation` with `direction: RelationDirection::From` and `label: "merged into"`.
   - Pass directly to `relations_merge::plan_relation_merges`.
3. **Backend Engine**:
   - Reuses `src/native/task_merge/plan.rs` without modifying its core transaction semantics.

---

## 5. Artifact & Repository Snapshot

The full research report has been recorded in the research sidecar repository and registered as a durable SASE artifact:

- **Source File:** `/home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_40/sase/repos/research/202611/capture_merge_in_syntax__gem.md`
- **Artifact Label:** `research:202611/capture_merge_in_syntax__gem.md`
- **Artifact Reference:** `file:explicit:e2ca92f2141b18277774894a`
- **Finalizer Declaration:** Submitted and accepted (`builtin@commit` for `sdd:research`).
