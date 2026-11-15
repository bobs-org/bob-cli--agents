# Chat History - ace-run (research.4r.gem)

- **TIMESTAMP:** 2026-11-15 11:41:46 EST
- **MODEL:** agy/gemini-4-hydrogen-xhigh
- **AGENT:** research.4r.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261115_112852.md`

## Prompt

%id(gem, clan=research.4r)
%m:agy/gemini-4-hydrogen-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.4r.cdx`, `research.4r.cld`, `research.4r.grk`, `research.4r.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to make the `bank` frontmatter field of the ~/bob/bank.md file much easier
to read/write from Obsidian.

- This field doesn't render in Obsidian at all at the moment.
- See how we did this for the `record` field of album notes for context and inspiration.
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

Research completed independently and written to [bank_frontmatter_obsidian_ux__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/research/202611/bank_frontmatter_obsidian_ux__gem.md), registered as durable artifact `file:explicit:31d402fe302ab1a0041c75ce` ([snapshot](file:///home/bryan/.sase/artifacts/agents/gh_bobs-org__bob-cli/20261115112903/bank_frontmatter_obsidian_ux__gem-a4d3bd5e9a5d.md)).

### Summary of Findings & Critique

1. **Why `bank:` doesn't render today (two layers):**
   - Like album `record:`, `bank:` in [bank.md](file:///home/bryan/bob/bank.md) is a 3–4 level nested YAML tree (`accounts`, 21 flow-mapped `categories`, optional `rules` list, and `stale_after`) that Obsidian Properties cannot render or edit safely.
   - Worse, [241p-plugin-bank-marks.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241p-plugin-bank-marks.js#L444-L477) (`bankMarkSyncHubProperty()`) already tags `bank.md` with `.bob-bank-hub-note`, and [styles.css](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/styles.css#L9094) sets `.bob-bank-hub-note .metadata-property[data-property-key="bank"] { display: none !important; }` **with no replacement UI**, forcing Source-mode YAML edits.

2. **Critique & Justified Adjustments vs. the Album `record:` Blueprint:**
   - **Keep `bank:` in `bank.md` frontmatter:** Single vault-synced source of truth parsed by [config.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/config.rs) beats `.bob/bank.toml`, body code blocks, or native Properties.
   - **Do not copy Album's top banner 1:1:** `bank.md` already embeds ```` ```bob-bank\nview: queue\n``` ```` ([241m-plugin-bank-cards.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/241m-plugin-bank-cards.js#L462-L487)), which renders `Accounts` status cards (`WF Checking` balanced, `Last import`). Adding another big tinted header banner would create double-chrome.
   - **Four explicit requirement adjustments called out in the report:**
     1. Replace unconditional hiding with a scoped **`.bob-bank-config-surface`** hairline collapsed bar directly beneath frontmatter (above `# 🏦 Bank`).
     2. Render **derived Rust behavior** (4 implicit `Money moves` built-ins, `derive_hotkey` keycap provenance vs. explicit hotkeys, `hidden` hotkey reservations, first-match-wins `rules` precedence, and `has_long_digit_run` 4-digit import-only masking traps in [suggest.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/suggest.rs#L294-L325) / [identity.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/identity.rs#L18-L40)).
     3. Enable **triage-time entry from `bank/YYYY-MM.md`**, especially `+ Rule` inside [247-plugin-bank-category-card-ui.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-ledger-tools/src/247-plugin-bank-category-card-ui.js), where high-frequency rule & category edits actually arise.
     4. Add **bank-specific guardrails & flow-map YAML preservation:** guard `accounts[0]` reorders (silent `[acct::]` default shifts), lock aliases with `.bob/bank/*.jsonl` journal `transaction_key` / ledger usage, nudge `hidden: true` over used-category deletion, ship an in-modal **Live Rule Match Tester**, and preserve single-line flow category maps instead of expanding them into multi-line block YAML like [spans.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/albums/update/spans.rs#L941-L996).

### Recommended Solution (Option C, in 3 Slices)

- **Slice 1 (Zero write risk):** Fix `bank_line_map` in [config.rs](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/src/native/bank/config.rs#L1009-L1046) for `- match:` sequence lines; add read-only `bob bank config inspect -f json`; mount the collapsed `🏦 bank` bar + expandable grouped inspector (`magenta` root hue from [cash.md](file:///home/bryan/bob/cash.md), `tabular-nums`, solid vs. dashed hotkey keycaps) paired with the `y` -> Source YAML -> `Done` excursion.
- **Slice 2 (Guarded writes):** Add `bob bank config test-rule` and `bob bank config update` (`expect` fingerprint, dry-run consequences, flow-preserving span writes with quoted `"0"`–`"9"` hotkeys, `inverse_ops` undo) backing a 4-tab keyboard-first **`Bank Config Card`** modal (`Categories`, `Rules` + live match tester, `Accounts` with default/alias guards, `Settings`).
- **Slice 3 (Triage velocity):** Wire `+ Rule` / `+ Category` directly from `BankCategoryCardModal`, register `edit-bank-config` in [160-sheet-rank.js](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_19/sase/repos/linked/bob-plugins/plugins/bob-command-mode/src/160-sheet-rank.js#L55-L64), and add `Ctrl+Shift+P` fallback on `bank.md`.

SASE final declaration submitted (`commit` for `sdd:research`).
