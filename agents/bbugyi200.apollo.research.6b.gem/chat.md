# Chat History - ace-run (research.6b.gem)

- **TIMESTAMP:** 2026-11-25 10:39:14 EST
- **MODEL:** agy/gemini-4-neon-xhigh
- **AGENT:** research.6b.gem
- **PROMPT:** `~/.sase/multi_prompts/202611/gh_bobs_org__bob_cli-multiprompt-261125_101842.md`

## Prompt

%id(gem, clan=research.6b)
%m:agy/gemini-4-neon-xhigh %q(1.5x, w=0.25)
#gh:gh_bobs-org__bob-cli 
You are researcher gem in a 5-researcher swarm.
The other researchers, `research.6b.cdx`, `research.6b.cld`, `research.6b.grk`, `research.6b.mus`, are independently investigating the same request and will write their own self-named reports ending in `__cdx.md` and `__cld.md` and `__grk.md` and `__mus.md`. Your report will end in `__gem.md`.

Conduct your research independently and form your own conclusions. Do NOT attempt to
locate, open, read, or otherwise consult the other researcher's report from this swarm,
even if it becomes available before you finish. Do not obtain that peer's findings
indirectly through its chat transcript, summaries, or requests to the peer. You may
independently use the same external sources, shared input material, and unrelated prior
research. You may check filenames or file existence to avoid overwriting your own
output, but do not inspect the peer's report contents. If you encounter its filename,
leave the report alone. The lead researcher will read every report and synthesize their
findings after you have all finished.

I would like to make the bank card (in the ~/bob/bank.md file) a proper property card
that collapses its schema by default and hides the native Obsidian properties that are
normally shown at the top of files.

- As a part of this change, we should add a new `_` keymap that expands/collapses this
  schema section in the bank card. This keymap should also work to expand/collapse the
  schema section found in album cards (which are expanded by default).
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

I completed the design and implementation research and published the full report:

- **Research report:** [bank_property_card_and_underscore_toggle__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/bank_property_card_and_underscore_toggle__gem.md)
- **Registered SASE artifact:** `research:202611/bank_property_card_and_underscore_toggle__gem.md` (`file:explicit:4793efa4186ad10277e5ba82`)

---

## Executive Summary & Critique

**Verdict: Strongly yes — and the backend is already ready.**

Today `~/bob/bank.md` is the last legacy body-anchored card: it sits beneath `# 🏦 Bank`, leaves Obsidian's native Properties drawer visible, leaves the inline title and `# 🏦 Bank` heading visible, and defaults its Setup panel open (`BANK_SETUP_DEFAULT_EXPANDED = true`), pushing the actionable `bob-bank` queue card below the fold. Meanwhile, `bob props show bank.md` **already emits** `note_kind: "bank"`, `capabilities: ["props_v1", "props_contract_v1"]`, card-owned `bank` (`editor: "=="`), and the full Area Settings `contract` — so **zero `bob-cli` changes are needed**; the entire feature lives in `bob-plugins` (`bob-ledger-tools` + `bob-command-mode`).

The original requirements are solid, with **six justified adjustments** that make the design feel native, cohesive, and bug-free:

1. **Full title-slot adoption with clean emoji extraction (zero vault edits):** Upgrade the Bank Card to own the note's top title slot (`propertyCardAdoptTitle` + `titleOwnership: true`), matching Area, Project, Album, and Reference cards. Add a `propertyCardBankTitleRecognizer` that extracts the leading emoji from `# 🏦 Bank` into the tile while rendering the heading cleanly as `Bank` (avoiding a double `🏦`) and hiding `# 🏦 Bank` in Live Preview.
2. **Honor `bank.md`'s hybrid Area identity:** Render clickable `BANK · ● Cash` kicker ancestry, derive the card accent from the real root-area hue walk (`notebookHostHueName`, replacing `bankCardRootHue`'s hardcoded `"magenta"` fallback), show `summary` as subtitle when authored, render optional Area policy chips only when authored (never empty defaults), and wire truthful foot `where`-marks.
3. **Fix the existing invalid-config collapse lock (`248a`):** Today `expanded: state === "invalid" ? true : expanded` makes an invalid Setup section uncollapsible. Instead, default `valid` to **collapsed** and `invalid`/`missing` to **expanded**, respect explicit user toggles in session state, clear any `false` override once on `valid → invalid` transitions, and surface quiet `⚠ stale` / `✗ delta` / `⚠ N warning` pills on the collapsed bar.
4. **Unify the Setup disclosure bar and clean up header actions:** Replace the small `▾`/`▸` corner button with a full-width clickable disclosure bar matching Album Card (`▸ Setup · WF Checking ✓ · 21 categories · 10 rules`, dropping the redundant `🏦`, with `title="Toggle bank setup (_)"` and Album's `title="Toggle album schema (_)"`). Move `⊞ Setup` into the title-block action slot and drop `↗ YAML` from the collapsed valid header (retaining it on `invalid` / `missing` / `unsupported` / `mobile`).
5. **Route `_` safely through a shared Card-Body Toggle registry + Reading-view command:** Add a view-local registry (`240s-plugin-property-card-body-toggle.js`) invoked from the existing bare-key capture gate (`propertyCardBareKeyGate` in `248m`), paired with a registered Obsidian command (`toggle-card-schema` / `toggle-card-details`) for Reading view and Command Mode discoverability. This preserves all Vim operator-pending (`d_`, `c_`, `y_`, `=_`), counted (`2_`), visual (`v_`), Source-mode, and non-card `_` motions, and scrolls the expanded section into view (`block: "nearest"`) without stealing focus from `.cm-content`.
6. **One explicit scope decision for you — `_` on Area & Project cards:** Area and Project Home Cards (`249c`/`249d`) already have a `▾`/`▸` collapse button with no keymap. Wiring them into the same `240s` registry gives universal Property Card symmetry (`-` = Properties, `_` = card body/schema, `==` = species editor, `+` = Property Editor):
   - **Option A (Recommended):** Universal Property Card body toggle — Bank (`Setup`), Album (`Schema`), and Area/Project (`Card body`).
   - **Option B:** Strictly Bank + Album in v1, keeping `240s` ready for Area/Project later.

---

## Recommended Implementation Plan

1. **Phase 1 — Shared `_` Card-Body Toggle & Album Card Adoption (`bob-ledger-tools`, `bob-command-mode`):**
   - Introduce `240s-plugin-property-card-body-toggle.js` (per-view registry with expand/collapse + smooth scroll-into-view without focus steal).
   - Extend `248m-plugin-schema-double-equals.js` (`propertyCardBareKeyGate`) to dispatch bare `_` in Live Preview Normal mode when no pending operator/count/visual selection is active, plus register the Obsidian command and Command Mode sheet rank.
   - Register Album Card (`241v` / `241x`) and add the `(_)` tooltip hint to its schema toggle button. (Optionally register Area/Project `249d` under Option A.)
2. **Phase 2 — Bank Card Property Card Upgrade (`bob-ledger-tools`):**
   - Split Bank title/frontmatter ownership helpers into `248cb-plugin-bank-setup-title.js` (respecting the `bob-plugins` 1,000-line fragment cap — `248c` is already 798 lines and `240q` is 837 lines).
   - Adopt the title slot (`240q`), hide native Properties via `propertyCardFrontmatterOwnership` (`240d`), wire the `==` / `-` / `+` / `_` key set and foot hints, switch `valid` default to collapsed while fixing the `invalid` collapse lock, and unify the full-width Setup disclosure bar + CSS.
   - **Critical transition guard:** Because Bank keeps `viewPath = "bank.md"` in Source mode for wavy YAML lint, `248c` must add a `shouldRebuild` check on `editorLivePreviewField` transitions and explicitly release title adoption, frontmatter ownership, keys, and foot whenever entering Source mode.

---

*Note:* The research report has been committed via `/sase_final` (`sdd:research`). No changes were made to `bob-cli`, `bob-plugins`, or `~/bob/bank.md`.
The SASE final declaration (`commit` for `sdd:research`) has been accepted and all background tasks have finished cleanly.

### Summary of Deliverables
- **Research report:** [bank_property_card_and_underscore_toggle__gem.md](file:///home/bryan/.local/state/sase/workspaces/bobs-org/bob-cli/bob-cli_20/sase/repos/research/202611/bank_property_card_and_underscore_toggle__gem.md)
- **Registered durable artifact:** `research:202611/bank_property_card_and_underscore_toggle__gem.md` (`file:explicit:4793efa4186ad10277e5ba82`)

### Key Recommendations
1. **Zero `bob-cli` changes needed:** `bob props show bank.md` already exposes `note_kind: "bank"`, `capabilities: ["props_v1", "props_contract_v1"]`, card-owned `bank` (`editor: "=="`), and the full Area Settings `contract`. All implementation lives in `bob-plugins` (`bob-ledger-tools` and `bob-command-mode`).
2. **Full Property Card upgrade for `bank.md`:** Adopt the top title slot (`propertyCardAdoptTitle` + `titleOwnership: true`), hide Obsidian's native Properties (`propertyCardFrontmatterOwnership`), extract the leading emoji from `# 🏦 Bank` via a dedicated `propertyCardBankTitleRecognizer` (avoiding double `🏦` with zero vault edits), honor `bank.md`'s hybrid Area identity (clickable `BANK · ● Cash` kicker, real root-area hue walk via `notebookHostHueName`, optional `summary` subtitle and authored Area policy chips), and release all ownership cleanly on Live Preview → Source transitions (`shouldRebuild` on `editorLivePreviewField`).
3. **Collapse valid Setup by default & fix the invalid collapse lock:** Default `valid` to collapsed and `invalid`/`missing` to expanded while fixing `248a`'s forced-expanded lock so explicit session toggles always work, surfacing quiet `⚠ stale` / `✗ delta` / `⚠ N warning` pills on the unified full-width Setup bar.
4. **Shared `_` Card-Body Toggle (`240s-plugin-property-card-body-toggle.js`):** Route bare `_` through `propertyCardBareKeyGate` (`248m`) in Live Preview Normal mode (preserving Vim operator-pending `d_`/`c_`/`y_`/`=_`, counted `2_`, visual `v_`, Source-mode, and non-card `_`), paired with an Obsidian/Command Mode command (`toggle-card-schema` / `toggle-card-details`) for Reading view. Wire Album Card and Bank Card (and decide between **Option A [Recommended]**: also wiring Area/Project Home Cards for universal Property Card symmetry, vs. **Option B**: strictly Bank + Album in v1).
