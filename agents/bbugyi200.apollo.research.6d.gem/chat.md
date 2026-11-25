# Chat History - ace-run (research.6d.gem)

- **TIMESTAMP:** 2026-11-25 14:22:59 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6d.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261125_135938.md`

## Prompt

%id(gem, clan=research.6d)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6d.cdx`, `research.6d.cld`, `research.6d.grk`, `research.6d.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to start allowing captures of the form `@foo^bar` that complement the `/`
search capture functionality.

- See the ~/tmp/screenshots/20261125_135534.png screenshot for context.
- Namely, if this capture is submitted, we should jump to the `^bar` task in the
  ~/bob/foo.md file, just as if the user used `/` key to search for the task and select
  it from the capture panel.
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

I completed an independent design research report evaluating direct `@foo^bar` Go To in Bob Capture across `bob-cli`, `bob-mac-capture`, and `bob-plugins`.

### Report & Registered Artifact
- **Report:** [direct_block_id_goto_capture__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/direct_block_id_goto_capture__gem.md)
- **Registered SASE Artifact:** `explicit:93db5043201700ffbb071c36` (`label: research:202611/direct_block_id_goto_capture__gem.md`, stored at [direct_block_id_goto_capture__gem-e4da977a66b3.md](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261125135943/direct_block_id_goto_capture__gem-e4da977a66b3.md))

### Executive Verdict & Critique
- **Good idea — strongly recommended.** `@foo^bar` fills the exact missing cell in Bob's marker-only `@route<op>id` family (`@foo` pull, `@foo:bar` link, `@foo+bar` ensure Next, `@foo+bar!` toggle) and rescues the dead end in `switch_block_id_separator` ([rewrite.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/capture_language/rewrite.rs#L2073)), turning `:`, `+`, and `^` into a zero-retyping 3-way operator cycle.
- **Two traps a naive implementation would hit:**
  1. Handling `@foo^bar` inside `bob capture` with `ok: true` creates an **Old-App × New-Bob silent no-op** (older Bob Mac Capture builds would display success, clear the draft, dismiss, and never open Obsidian).
  2. Hijacking `@foo^` solely for Go To would regress `@foo^new-id Do X` and sealed `@foo^new-proj@` / `@foo^nb@ %n` authoring; meanwhile `sase/memory/cli_rules.md` forbids adding new `capture-*` subcommands.

### Four Justified Requirement Adjustments
1. **Whole-draft, single-token, modifier-free gate only:** Never silently turn drafts with extra text, child bullets, `#type`, `s:N`, `%c`, `@@`, or multiple items into a jump.
2. **Resolve any unique `^bar` block ID + `done/<route>.md` archive fallback:** Support open tasks, closed tasks, notebook notes, and plain bullets/headings (badging archives as `Archived · done/<route>.md`), with an optional ~10-line non-task `^block` drift fallback in [675-plugin-goto-task-uri.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/linked/bob-plugins/plugins/bob-navigation-hotkeys/src/675-plugin-goto-task-uri.js#L176).
3. **Dual-purpose `@foo^` note-scoped Go To picker (`block_id.intent: "goto"`):** Lets users browse/jump inside one note (`↩` opens directly, `⇥` fills `@foo^bar` into the editor) while preserving `+ New ID` creation and `@` type-through sealing for `@foo^new-proj@` (100% forward-compatible with older Mac Capture builds via `.unsupported` fallback).
4. **Strictly read-only outside `bob capture` + bonus `/` indexing:** Keep `bob capture` refusing standalone `@foo^bar` (matching `/` and `//`) and also index `route^block-id` in [capture_link_tasks.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/capture_link_tasks.rs#L336) so `/bob^intention-rollovers` matches too.

### Recommended Solution
- **`bob-cli` (Grammar 31, Schema 1):** Classify solo `@route^block-id` as `mode: "task_goto"` in `bob capture-parse` ([capture_parse.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/capture_parse.rs#L621)), resolve target/line/`ref`/metadata/Pomodoro/suggestions in a single read-only pass, add `BlockIdIntent::Goto` in [capture_block_ids.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/src/native/capture_block_ids.rs#L33), and refuse whole-draft `@route^block-id` in `bob capture`.
- **`bob-mac-capture`:** On `mode == "task_goto"`, skip `bob capture --dry-run` (1 spawn instead of 2), render a calm `CaptureTaskGotoPreviewCard` (with dedicated states for Found, Typo Suggestion with `Tab` accept, Available New ID, and Ambiguous Duplicate), relabel the primary button to **`Open ↗`**, hide the redundant `⌃↩ Open ↗` footer chip, dispatch `obsidian://bob-goto-task` on `↩`/`⌘↩`/`⌃↩` with fast-paste parse await and `taskGotoDispatchInFlight` guarding, and exclude resolved Go To drafts from the canceled-draft stash (`draftIsReadOnlyGoto`).
