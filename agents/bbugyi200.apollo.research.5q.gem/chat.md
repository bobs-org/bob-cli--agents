# Chat History - ace-run (research.5q.gem)

- **TIMESTAMP:** 2026-11-21 10:42:03 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.5q.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261121_102500.md`

## Prompt

%id(gem, clan=research.5q)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.5q.cdx`, `research.5q.cld`, `research.5q.grk`, `research.5q.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

When I review bank rows in the morning, sometimes I would like to leave a note on one of
them (to clarify what the purchase was or why it was made, for example). I think we can
accomplish this via a new `<space>` keymap in the bank row category picker panel that
prompts the user for a note.

- This note should then be added to the bank row in some visually appealing way without
  progressing to the next bank row in the bank row walk.
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

I completed the independent research and design analysis for in-flow bank row notes and wrote the full report to [bank_row_note_keymap_design__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/bank_row_note_keymap_design__gem.md).

- **Registered Artifact:** `file:explicit:669adb3cff5b61f9481ff187` (label: `research:202611/bank_row_note_keymap_design__gem.md`)

### Key Findings & Critique

1. **Strong idea, zero ownership friction:** Leaving a clarification note right inside the Bank Category card without advancing the walk fits Bob's architecture cleanly. `bob-cli` already parses inline `— <note>` rows (`src/native/bank/grammar.rs`), exposes `row.note` in JSON and `bob bank list`, and leaves row edits to the Obsidian editor.
2. **Critical `<Space>` keymap collision:** `<Space>` is **not currently unbound** — it is bound in `BankCategoryCardModal` to **no category** (`close` mode), **remove category** (`set` mode), and **acknowledge** (the sole action in offline/restricted mode).
   - **Recommended adjustment:** Give `<Space>` to the inline Note stage (thumb-ergonomic, safe non-destructive failure mode), relocate **no category / remove category** to **`Backspace`** (aliased to `Delete` and `Ctrl+D`, matching Bob's clear-property convention), and bind **`Enter`** to acknowledge in restricted mode (so `<Space>` also works offline).
   - **Zero-breaking fallback:** Keep `<Space>` as `no-category` and bind **`-`** (mnemonic for `— <note>`, beside `+` and `/`) to Note.
3. **Four latent codebase traps to fix alongside this feature:**
   - `241o-plugin-bank-marks-model.js` computes `noteSpan` excluding `—`, runs it past interleaved tokens (CodeMirror span-overlap risk), and strips single `!` (diverging from Rust `grammar.rs`, which only strips `!!`).
   - `241hc-plugin-bank-subscription.js` inserts `[[subscriptions/<stem>|🔁]]` at `bankIdSpan.start`, which lands *after* an existing `— <note>`.
   - `241o` / `241p` MathJax `$` protection covers only `token.amount`, so typing `$20` inside a note can corrupt bank rows into LaTeX.
   - `246-plugin-bank-category-card-write.js` refuses subsequent edits on ID-less rows unless `modal.context` (`capture.lineText`, `token`, `cardRow.note`) is refreshed in place, and setting `modal.didInteract = true` on Note open would discard in-flight learned category suggestions.

### Recommended Solution

- **Inline Note stage (not a nested modal):** Mirror `+` (New category) and `/` (Subscription picker) inside `BankCategoryCardModal` so the row header stays visible, pre-fill existing notes for edit/clear, lint grammar hazards (`#task` hard block; `::`, `⚑`/`!!`, `—`/`--`, trailing `^id` warnings) live, respect `Esc`/`Ctrl+[` back-out (`q` types normally in the input), save in a single undo step, refresh `modal.context`, and return to the **same row** with `highlightKey` intact.
- **Canonical inline storage (`— <note>`):** Always maintain `[cat::] [acct::] [[links]] ⚑ — <note> ^bank-<hex>` via a pure, token-preserving `bankNoteWritePlan`, and fix subscription linking to insert before `— <note>`.
- **Editorial marginalia styling (no "pill soup"):** Render `— <note>` in Month Notes (Live Preview + Reading view, with full-row `$` MathJax protection) using Bob's signature accent left-hairline, subtle tinted wash, `✎` glyph, and muted italic prose; mirror that strip in the Category card header with instant save confirmation and add a truncated snippet on Queue card rows plus a companion **`Bank: edit note`** command for already-acknowledged rows.
