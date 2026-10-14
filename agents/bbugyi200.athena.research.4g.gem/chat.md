# Chat History - ace-run (research.4g.gem)

- **TIMESTAMP:** 2026-10-14 10:17:39 EDT
- **MODEL:** agy/gemini-3.8-flash-high
- **AGENT:** research.4g.gem
- **PROMPT:** `~/.sase/multi_prompts/202610/gh_bobs_org__bob_cli-multiprompt-261014_100238.md`

## Prompt

%id(gem, clan=research.4g)
%m:agy/gemini-3.8-flash-high %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 4-researcher swarm.
The other researchers, `research.4g.cdx`, `research.4g.cld`, `research.4g.grk`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md`. Your report will end in `__gem.md`.

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
would like to add support to the `bob capture` command and the corresponding
bob-mac-capture app for a new `*` syntax.

- This syntax should work a lot like the `&` syntax, which allows the user to specify
  that the new task should have a task dep link to a different task.
- This new syntax, however, should allow the user to specify that the new task blocks
  the specified task (i.e. specify a task dependency in the opposite direction).
- When we block a task that has a corresponding task link in today's daily file using
  this method, we should remove that task link (and the pomodoro iff that pomodoro
  section becomes empty after removing that task link).

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

### Executive Research Summary: Reverse Dependency (`*` Blocks) Capture Syntax

The research and architectural critique regarding adding support for a new `*` (blocks target) capture syntax to `bob capture` and `bob-mac-capture` is complete.

The full research report has been written to:
- **File:** [`capture_blocking_task_syntax__gem.md`](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_15/sase/repos/research/202610/capture_blocking_task_syntax__gem.md)
- **Durable Artifact Reference:** `research:202610/capture_blocking_task_syntax__gem.md` (`file:explicit:4230c7a1f182fb9d4805f233`)

---

### Key Findings & Analysis

#### 1. Strategic & Workflow Value
Capturing a blocking prerequisite on the fly is a classic GTD micro-workflow ("blocking subtask discovery"): while working on a planned task, a user realizes a new prerequisite must be resolved first. Currently, capturing this requires a disruptive four-step manual intervention across multiple files. Automating this via capture (`*note:block-id`) preserves workflow flow and directly enforces the system rule that blocked tasks do not linger under open Pomodoros (`decisions:projects-block-from-prj-line` and `decisions:task-status-is-derived`).

#### 2. Critique of the Plan
- **The Concept:** Strong **Yes**. Providing a reverse edge counterpart to `&note:block-id` ("depends on") completes the capture dependency vocabulary.
- **The Sigil (`*`):** The asterisk is heavily overloaded in Markdown (`*italic*`, `**bold**`, `* ` list item) and is a shell wildcard in Unix terminals (`zsh: no matches found: *note:id` if unquoted in macOS `zsh`). While viable and concise, it requires strict lexer guard conditions.
- **Ledger Invariant:** The requirement to unlink the blocked task from today's daily note and remove the Pomodoro if emptied is architecturally sound, but must be strictly guarded so it never mutates completed Pomodoros (`[x]`) or drops user notes.

---

### Proposed Adjustments to Requirements

1. **Strict Lexer Guard Conditions for `*`:**
   - `* ` followed by whitespace is always a bullet list item, never a modifier.
   - `**` is always bold formatting, never a modifier.
   - Paired asterisks without colons (`*italic*`) remain literal Markdown text.
   - Like `&`, directive `*` modifiers are recognized only in the leading run (parent line) or trailing run (past `@route` / `#section`).
   - `\*` escapes to literal `*`.
2. **Ledger Cleanup Scoped Exclusively to Open Pomodoros:**
   - Link removal and Pomodoro deletion apply **only** to open Pomodoro entries (`- [ ]`).
   - Completed (`- [x]`) and canceled (`- [-]`) Pomodoros represent committed historical records of time worked and must never be altered.
3. **Precise "Empty Pomodoro" Definition:**
   - A Pomodoro entry is deleted iff it has **no remaining child list items** of any kind. If other tasks or prose notes exist under the Pomodoro, only the target link is stripped; the Pomodoro entry headline is preserved.
   - The document-level `## Pomodoros` heading section itself is permanent vault scaffolding and is never deleted.
4. **Atomic Batch Replacement:**
   - If a capture simultaneously links the new task to the current Pomodoro and blocks an existing task in that same Pomodoro (`bob capture "Urgent fix = *proj:deploy"`), the Pomodoro must not be deleted in between; the blocker replaces the blocked task in place.
5. **Target Validation & Cycle Prevention:**
   - Refuse blocking completed tasks (`[x]`).
   - Abort if the new dependency would introduce a circular graph.
   - If the target is `^prj`, cascade the project block across all residents (`[?] #prj_is_blocked`) and consume their live links (`project_deps.rs`).
6. **Bob Mac Capture Preview Transparency:**
   - Display a preview badge (`🧱 blocks: [[note#^id]] (becomes [?])`) and an explicit ledger warning chip (`🍅 unlinks from today's Pomodoro <time/name>`) before submission to ensure zero user surprise.

---

### Implementation Blueprint

1. **`bob-cli: capture_language` (`dependencies.rs`, `tokens.rs`):**
   - Parameterize `DependencyDirection` (`Prerequisite` vs. `Blocks`).
   - Parse `*note:block-id` using the existing generalized locator scanner (`scan_modifier_with_sigil`).
   - Add `SpanKind::BlocksSigil`, `SpanKind::BlocksNote`, `SpanKind::BlocksBlockId`.
2. **`bob-cli: capture_complete` (`candidates.rs`, `completion.rs`):**
   - Add `CompletionContext::TaskBlocks` for interactive `*` queries.
   - Offer open vault tasks, excluding ancestors/cycles.
3. **`bob-cli: capture` (`plan.rs`, `dependencies.rs`):**
   - Mint a block ID for the newly captured task (`mint_staged_dependent_id`).
   - Stage `🧱 **BLOCKS:** [[target#^id]]` on the new task.
   - Update `⛓️ **DEPENDS ON:** [[new#^id]]` and `[dependsOn::]` on the target task; set status to `[?]`.
   - Leverage `capture_task_toggle::plan_link_removal` and `task_status_hooks::plan_empty_pomodoro_removals` to stage daily file link and empty Pomodoro cleanup.
   - Track deletions via `PomodoroBlockRef::removed`.
4. **`bob-mac-capture` (`Sources/CaptureCore/`):**
   - Support `task_blocks` completion and syntax highlighting.
   - Render distinct header in picker: `"Choose task to block"`.
   - Show live preview chips for blocked task transitions and ledger removals.
