# Chat History - ace-run (research.6p.gem)

- **TIMESTAMP:** 2026-11-27 14:03:21 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6p.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261127_134153.md`

## Prompt

%id(gem, clan=research.6p)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6p.cdx`, `research.6p.cld`, `research.6p.grk`, `research.6p.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to add configurable task type expansion that is triggered when certain task
types are expanded (by selecting an entry offered by `#` completion in the capture
panel) at the start of the capture.

- `#fix`, `#build`, `#plan`, `#read`, and `#write` should all by configured (in my
  chezmoi repo) to auto-complete the corresponding word when expanded at the start of a
  capture.
- For example, after this change is implemented, when I type `#f` in an empty capture
  panel and then select the `#fix` task type, I would expect `#fix Fix ` to be expanded.
- The goal of this change is to reduce the amount of typing I need to do in some common
  cases when specifying task types in captures.
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

I completed the independent research, wrote the report to [capture_task_type_lead_word_expansion__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_10/sase/repos/research/202611/capture_task_type_lead_word_expansion__gem.md), and registered it as a durable SASE artifact:

- **Artifact ref:** `file:explicit:a40f8b688601c867ff2e56ed`
- **Label:** `research:202611/capture_task_type_lead_word_expansion__gem.md`
- **Stored snapshot:** [capture_task_type_lead_word_expansion__gem-37d206ae60c9.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261127134159/capture_task_type_lead_word_expansion__gem-37d206ae60c9.md)

### Highlights & Recommended Solution

1. **Empirical Critique (`bob query` census across 5,478 vault `#task` rows, 1,240 since 2026-10-31):**
   - **`#fix` → `Fix ` is a clear win:** **81/165 (49.1%)** post-Oct-31 explicit `FIX` captures start with `Fix `, and **81/81 (100.0%)** recent `Fix ...` tasks are `FIX` (97.7% live under `dev`/`bob`/`sase`, overriding `BUILD`).
   - **`#plan` → `Plan ` is borderline:** **3/16 (18.8%)** explicit `PLAN` tasks start with `Plan ` — net positive only with a 1-keystroke rejection path.
   - **`#build`, `#write`, and `#read` have 0.0% historical hit rates:** **0/5,478** vault `#task` rows start with `Build ` (top `BUILD` verbs are `Add`, `Make`, `Migrate`, `Create`, `Use`), **0/17** explicit `WRITE` tasks start with `Write ` (`sase_blog` uses `Draft`/`Convert`), and **0/1** explicit `READ` tasks start with `Read ` (`bob ref` handles reading tasks via `plan.reading_type`, while recent `Read ...` tasks are all recurring `Read Email` chores).
   - **Recommendation:** Build the general configurable expansion engine, but start `chezmoi` with **`FIX: Fix`** (and optionally **`PLAN: Plan`**) rather than enabling `#build`/`#read`/`#write` by default.

2. **Config Placement & Rollout Safety (`decisions:bob-cli-releases-ride-a-daily-train`):**
   - Put the map under **`capture.type_expansions:`** (not nested inside `types:`). Changing `types.FIX: red` into a YAML mapping causes older `bob` builds (`src/native/config/themes.rs:218-240`) to reject and drop the entire `types:` vocabulary, whereas unknown keys inside `capture:` (`src/native/config/capture.rs`) are ignored safely across hosts.
   - Store trimmed strings (`FIX: Fix`) and let Bob append one separating space deterministically, avoiding YAML trailing-whitespace pitfalls. Integrate with `bob types rename` `config_reference()` checks (`src/native/pomodoro_themes/rename.rs:1126`).

3. **Thin-Client Contract & Eligibility Gate (`decisions:mac-capture-is-a-thin-client`):**
   - Keep `bob-cli` as sole authority. Gate expansion in `task_types::build` (never in `build_for_shell` so zsh/bash stays `#fix`) to non-refused picks on a **new task's parent line** where the `#<type>` marker is **leading, body is empty, and nothing non-whitespace follows on the line** — supporting `#f`, `@@sase\n#f`, bulk item 2 (`Buy milk\n\n#f`), and `@sase #f`, while excluding `#f Fix it`, `@sase:id #f`, `@sase^id@ #f`, nested `  - #f`, and `%t #f`.
   - Extend `TaskTypeCandidate` additively at `schema_version: 1` with `replacement: "#fix Fix "`, `cursor_after: 9`, and optional `expansion: { marker, text, range }`.

4. **Intuitive, Reliable, Beautiful UX in Bob Mac Capture:**
   - **Truthful menu preview:** Show a quiet inline `→ Fix` cue beside the tinted `FIX` pill in `CaptureTaskTypeMenuView` (only when `expansion != nil`), plus `inserts “Fix ” · …` in the consequence footer and VoiceOver label.
   - **One-tap atomic Backspace peel:** Arm a one-shot peel on accept so an immediate unmodified `Backspace` deletes `"Fix "` atomically (matching existing `[ ] `, `****`, `,<digit>`, and `- ` Backspace behavior) and disarms on any other edit or caret motion.
   - **Two-step native Undo:** Apply via `CaptureNativeRewriteEdit` with `breakUndoCoalescing()` (`#f` → `#fix `, then insert `Fix `) so first `⌘Z` strips `Fix ` while keeping `#fix `, and second `⌘Z` restores `#f`.
   - **`⌘↩` / `⌃↩` safety guard:** Stop `acceptSelectedCompletionThenSubmitAndOpen()` after accepting when `candidate.expansion != nil`, preventing accidental submission of a bare one-word `"Fix"` task.
